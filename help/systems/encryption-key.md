---
title: Versleutelingssleutel
description: Leer hoe u automatisch uw eigen coderingssleutel genereert of toevoegt. Deze sleutel moet regelmatig worden gewijzigd om de beveiliging te verbeteren.
exl-id: 78190afb-3ca6-4bed-9efb-8caba0d62078
role: Admin
feature: System, Security
source-git-commit: 21be3c7a56cb72d685b2b3605bc27266e8e55f37
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Versleutelingssleutel

Adobe Commerce en Magento Open Source gebruiken een coderingssleutel om wachtwoorden en andere vertrouwelijke gegevens te beschermen. Een industriestandaard [!DNL ChaCha20-Poly1305] -algoritme wordt gebruikt met een 256-bits sleutel om alle gegevens te coderen die codering vereisen. Hieronder vallen creditcardgegevens en integratiewachtwoorden (betalings- en verzendmodule). Bovendien wordt een sterk Veilig Algorithm (SHA-256) gebruikt om alle gegevens te hashen die geen decryptie vereisen.

Tijdens de eerste installatie wordt u gevraagd of u Commerce een coderingssleutel wilt laten genereren of een van uw eigen coderingssleutels wilt invoeren. Met de coderingssleutel kunt u de sleutel naar wens wijzigen. De coderingssleutel moet regelmatig worden gewijzigd om de beveiliging te verbeteren en op elk moment kan de oorspronkelijke sleutel in gevaar worden gebracht. Wanneer de sleutel wordt gewijzigd, worden alle oude gegevens opnieuw gecodeerd met de nieuwe sleutel.

Voor technische informatie, zie [ Geavanceerde op-gebouwinstallatie ](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) in de _Gids van de Installatie_.

## Stap 1: Maak het bestand schrijfbaar

Als u de coderingssleutel wilt wijzigen, moet u controleren of het volgende bestand beschrijfbaar is: `[your store]/app/etc/env.php`

## Stap 2: Wijzig de coderingssleutel

1. Voor _Admin_ sidebar, ga **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Manage Encryption Key]**.

   ![ de encryptiesleutel van het Systeem ](./assets/encryption-key.png){width="700" zoomable="yes"}

1. Voer een van de volgende handelingen uit:

   - Als u een nieuwe sleutel wilt genereren, stelt u **[!UICONTROL Auto-generate Key]** in op `Yes` .
   - Als u een andere toets wilt gebruiken, stelt u **[!UICONTROL Auto-generate Key]** in op `No` . Voer vervolgens in het veld **[!UICONTROL New Key]** de gewenste toets in of plak deze.

1. Klik op **[!UICONTROL Change Encryption Key]**.

1. Een record van de nieuwe sleutel op een veilige locatie bewaren.

   De gegevens moeten worden gedecodeerd als er problemen optreden met de bestanden.
