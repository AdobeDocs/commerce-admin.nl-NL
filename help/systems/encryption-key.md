---
title: Versleutelingssleutel
description: Leer hoe u uw eigen coderingssleutel wijzigt, wat regelmatig moet worden gedaan om de beveiliging te verbeteren.
exl-id: 78190afb-3ca6-4bed-9efb-8caba0d62078
role: Admin
feature: System, Security
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: 256517ebbbd6e28eb027f26c7f0a43001f5d7904
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 0%

---

# Versleutelingssleutel

>[!NOTE]
>
>Als u hebt geprobeerd om deze stappen te voltooien en kwesties hebt, zie de [ Zeer belangrijke Omwenteling van de Encryptie van het Oplossen van problemen: CVE-2024-34102 ](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/troubleshooting-encryption-key-rotation-cve-2024-34102) artikel van de Kennisbank.

Adobe Commerce en Magento Open Source gebruiken een coderingssleutel om wachtwoorden en andere vertrouwelijke gegevens te beschermen. Een industriestandaard [!DNL ChaCha20-Poly1305] -algoritme wordt gebruikt met een 256-bits sleutel om alle gegevens te coderen die codering vereisen. Hieronder vallen creditcardgegevens en integratiewachtwoorden (betalings- en verzendmodule). Bovendien wordt een sterk Veilig Algorithm (SHA-256) gebruikt om alle gegevens te hashen die geen decryptie vereisen.

Tijdens de eerste installatie wordt u gevraagd of u Commerce een coderingssleutel wilt laten genereren of een van uw eigen coderingssleutels wilt invoeren. Met de coderingssleutel kunt u de sleutel naar wens wijzigen. De coderingssleutel moet regelmatig worden gewijzigd om de beveiliging te verbeteren en op elk moment kan de oorspronkelijke sleutel in gevaar worden gebracht.

Voor technische informatie, zie [ Geavanceerde installatie ](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) in de _Gids van de Installatie_ en [ Gegevens re-encryptie ](https://developer.adobe.com/commerce/php/development/security/data-encryption/) in de _Gids van de Ontwikkelaar PHP_.

>[!IMPORTANT]
>
>- Voordat u de instructies voor het wijzigen van de coderingssleutel uitvoert, moet u controleren of het volgende bestand beschrijfbaar is: `[your store]/app/etc/env.php`
>- De functie voor het wijzigen van de coderingssleutel in de beheerinstellingen is vervangen en is verwijderd in 2.4.8. U moet het CLI bevel gebruiken dat op deze pagina wordt beschreven om uw encryptiesleutel na bevordering aan 2.4.8 te veranderen.
>- Als u de coderingssleutel roteert, worden alle klant- en beheersessies (met uitzondering van integratiegebruikers) onmiddellijk ongeldig en moeten zij zich opnieuw aanmelden.

**om een encryptiesleutel te veranderen:**

De volgende instructies vereisen toegang tot een terminal.

1. Laat [ onderhoudswijze ](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/setup/application-modes#maintenance-mode) toe.

   ```bash
   bin/magento maintenance:enable
   ```

1. Uitsnijdtaken uitschakelen.

   _de infrastructuurprojecten van de Wolk:_

   ```bash
   ./vendor/bin/ece-tools cron:disable
   ```

   _op-gebouwprojecten_

   ```bash
   crontab -e
   ```

1. Wijzig de coderingssleutel met een van de volgende methoden.

   +++CLI, opdracht

   Voer het volgende CLI bevel in werking en zorg ervoor dat het zonder fouten voltooit. Als u bepaalde systeem config waarden of betalingsgebieden moet re-coderen, zie de gedetailleerde [ gids op re-encryptie ](https://developer.adobe.com/commerce/php/development/security/data-encryption/) in _PHP ontwikkelt Gids_.

   ```bash
   bin/magento encryption:key:change
   ```

+++

   +++beheerinstellingen

   >[!IMPORTANT]
   >
   >Deze functie is vervangen en is verwijderd in 2.4.8. Adobe raadt aan coderingssleutels te wijzigen met de CLI.

   1. Voor _Admin_ sidebar, ga **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Manage Encryption Key]**.

      ![ de encryptiesleutel van het Systeem ](./assets/encryption-key.png){width="700" zoomable="yes"}

   1. Voer een van de volgende handelingen uit:

      - Als u een nieuwe sleutel wilt genereren, stelt u **[!UICONTROL Auto-generate Key]** in op `Yes` .
      - Als u een andere toets wilt gebruiken, stelt u **[!UICONTROL Auto-generate Key]** in op `No` . Voer vervolgens in het veld **[!UICONTROL New Key]** de gewenste toets in of plak deze.

   1. Klik op **[!UICONTROL Change Encryption Key]**.

      >[!NOTE]
      >
      >Een record van de nieuwe sleutel op een veilige locatie bewaren. De gegevens moeten worden gedecodeerd als er problemen optreden met de bestanden.

+++

1. Maak de cache leeg.

   _de infrastructuurprojecten van de Wolk:_

   ```bash
   magento-cloud cc
   ```

   _op-gebouw projecten:_

   ```bash
   bin/magento cache:flush
   ```

1. Snijtaken inschakelen.

   _de infrastructuurprojecten van de Wolk:_

   ```bash
   ./vendor/bin/ece-tools cron:enable
   ```

   _op-gebouw projecten:_

   ```bash
   crontab -e
   ```

1. Onderhoudsmodus uitschakelen.

   ```bash
   bin/magento maintenance:disable
   ```
