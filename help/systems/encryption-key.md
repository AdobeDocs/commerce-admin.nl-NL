---
title: Coderingssleutel
description: Leer hoe u uw eigen coderingssleutel kunt wijzigen, wat regelmatig moet worden gedaan om de beveiliging te verbeteren.
exl-id: 78190afb-3ca6-4bed-9efb-8caba0d62078
role: Admin
feature: System, Security
source-git-commit: 48f3431faa5db50f896b7a8e3db59421c639185b
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# Coderingssleutel

>[!NOTE]
>
>Als u hebt geprobeerd deze stappen uit te voeren en problemen ondervindt, raadpleegt u het [Knowledge Base-artikel Problemen met versleutelingssleutelrotatie: CVE-2024-34102](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/troubleshooting-encryption-key-rotation-cve-2024-34102) Knowledge Base.

Adobe Commerce en Magento Open Source gebruiken een versleutelingssleutel om wachtwoorden en andere gevoelige gegevens te beschermen. Een industriestandaard [!DNL ChaCha20-Poly1305] algoritme wordt gebruikt met een 256-bits sleutel om alle gegevens te versleutelen die versleuteling vereisen. Dit omvat creditcardgegevens en integratiewachtwoorden (betalings- en verzendmodule). Bovendien wordt een sterk Secure Hash Algorithm (SHA-256) gebruikt om alle gegevens te hashen die niet hoeven te worden ontsleuteld.

Tijdens de eerste installatie wordt u gevraagd om Commerce een coderingssleutel te laten genereren of om een eigen coderingssleutel in te voeren. Met de coderingssleutel kunt u de sleutel naar behoefte wijzigen. De coderingssleutel moet regelmatig worden gewijzigd om de beveiliging te verbeteren, en op elk moment kan de oorspronkelijke sleutel worden gecompromitteerd.

Zie [Geavanceerde on-premises installatie](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) in de _installatiehandleiding_ en [versleuteling van gegevens in de _PHP-ontwikkelaarshandleiding](https://developer.adobe.com/commerce/php/development/security/data-encryption/)_ voor technische informatie.

>[!IMPORTANT]
>
>- Voordat u deze instructies volgt om de coderingssleutel te wijzigen, moet u ervoor zorgen dat het volgende bestand beschrijfbaar is: `[your store]/app/etc/env.php`
>- De functie voor het wijzigen van de coderingssleutel in de beheerdersinstellingen is afgeschaft en is verwijderd in 2.4.8. U moet de CLI-opdracht gebruiken die op deze pagina wordt beschreven om uw coderingssleutel te wijzigen na het upgraden naar 2.4.8.

**Een versleutelingssleutel wijzigen:**

Voor de volgende instructies is toegang tot een terminal vereist.

1. Schakel de onderhoudsmodus[&#128279;](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/setup/application-modes#maintenance-mode) in.

   ```bash
   bin/magento maintenance:enable
   ```

1. Schakel cron-taken uit.

   _Projecten voor cloudinfrastructuur:_

   ```bash
   ./vendor/bin/ece-tools cron:disable
   ```

   _Projecten op locatie_

   ```bash
   crontab -e
   ```

1. Wijzig de coderingssleutel met behulp van een van de volgende methoden.

   +++CLI opdracht

   Voer de volgende CLI-opdracht uit en zorg ervoor dat deze zonder fouten wordt voltooid. Als je bepaalde systeemconfiguratiewaarden of betalingsvelden opnieuw moet versleutelen, bekijk dan de gedetailleerde [gids over herversleuteling](https://developer.adobe.com/commerce/php/development/security/data-encryption/) in de _PHP Develop Guide_.

   ```bash
   bin/magento encryption:key:change
   ```

   +++

   +++Admin instellingen

   >[!IMPORTANT]
   >
   >Deze functie is afgeschaft en is verwijderd in 2.4.8. Adobe raadt aan om versleutelingssleutels te wijzigen met de CLI.

   1. Ga in de _zijbalk voor beheerders_ naar **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Manage Encryption Key]**.

      ![Systeem encryptie sleutel](./assets/encryption-key.png){width="700" zoomable="yes"}

   1. Voer een van de volgende handelingen uit:

      - Als u een nieuwe sleutel wilt genereren, stelt u deze in **[!UICONTROL Auto-generate Key]** op `Yes`.
      - Als u een andere toets wilt gebruiken, stelt u deze in **[!UICONTROL Auto-generate Key]** op `No`. Voer vervolgens in het **[!UICONTROL New Key]** veld de sleutel in of plak deze die u wilt gebruiken.

   1. Klik op **[!UICONTROL Change Encryption Key]**.

      >[!NOTE]
      >
      >Bewaar de nieuwe sleutel op een veilige locatie. Het is vereist om de gegevens te decoderen als er problemen optreden met uw bestanden.

   +++

1. Leeg de cache.

   _Projecten voor cloudinfrastructuur:_

   ```bash
   magento-cloud cc
   ```

   _Projecten op locatie:_

   ```bash
   bin/magento cache:flush
   ```

1. Schakel cron-taken in.

   _Projecten voor cloudinfrastructuur:_

   ```bash
   ./vendor/bin/ece-tools cron:enable
   ```

   _Projecten op locatie:_

   ```bash
   crontab -e
   ```

1. Schakel de onderhoudsmodus uit.

   ```bash
   bin/magento maintenance:disable
   ```
