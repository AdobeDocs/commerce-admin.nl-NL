---
title: Goedkeuringsregels voor inkooporders
description: Leer over de goedkeuringsregels voor inkooporders en hoe bedrijfsbeheerders deze op de winkel kunnen definiëren.
exl-id: e8d8bbc9-41cf-4024-85cc-92f0b0ce32d6
feature: B2B, Companies, Configuration
role: Admin
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '657'
ht-degree: 0%

---

# Goedkeuringsregels voor inkooporders

De meeste bedrijven vereisen goedkeuring van bestellingen voor inkooporders. Door goedkeuringsregels voor hun bedrijfsaccount toe te voegen, kunnen ze bepalen wie inkooporders kan maken en hoeveel ze mogen uitgeven. Bijvoorbeeld:

* Elke inkooporder met een waarde kleiner dan X wordt automatisch goedgekeurd.
* POs groter dan X waarde maar minder dan Q moet door Y worden goedgekeurd.
* Elke inkooporder boven de X-waarde moet door Y en Z worden goedgekeurd.
* Een inkooporder die door iedereen op Director-niveau of hoger is gemaakt, wordt automatisch goedgekeurd.

Afhankelijk van de bedrijfsrol en de toestemmingen, kunnen de gebruikers, goedkeuringsregels tot stand brengen uitgeven, schrappen of bekijken.

>[!IMPORTANT]
>
>De opstelling van de goedkeuringsregel vereist een bepaalde [&#x200B; bedrijfstructuur &#x200B;](account-company-structure.md) om goedkeuring door de manager van de koopklant te specificeren.

## Betalingsmethoden

Goedkeuringsstromen voor inkooporders ondersteunen zowel online- als offline betalingsmethoden. Alle standaardmethoden voor offline betalingen worden ondersteund voor goedkeuringen van inkooporders. Voor online betalingen worden de volgende methoden ondersteund:

* PayPal Express
* Braintreeën


## Goedkeuringsregelinstelling

Met de vereiste [&#x200B; toestemmingen voor hun rol &#x200B;](account-company-roles-permissions.md), kunnen de klanten B2B opstelling goedkeuringsregels om bedrijfbeleid af te dwingen door **[!UICONTROL Approval Rules]** in het linkerpaneel voor hun klantenrekening te klikken.

![&#x200B; Regels van de Goedkeuring van het Bedrijf &#x200B;](./assets/approval-rules.png){width="700" zoomable="yes"}

Om een goedkeuringsregel tot stand te brengen, voltooit een klant de volgende stappen:

1. Klik op **[!UICONTROL Add New Rule]** om een regel te maken.

1. Wijzig zo nodig de regel van **[!UICONTROL Enabled]** in **[!UICONTROL Disabled]** .

   De regel is zoals toegelaten als gebrek, maar een klant kan de regel tot stand brengen gebruikend gehandicapten die en dan het toelaten later wanneer zij bereid zijn om het af te dwingen.

1. Voor **[!UICONTROL Rule name]** voert u een korte, maar beschrijvende naam in voor de regel, zoals `Orders less than $100` .

   Regelnamen moeten uniek zijn.

1. Voor **[!UICONTROL Description]** voert u een langere uitleg van de regel in.

1. Kies voor **[!UICONTROL Applies to]** een of meer rollen van het bedrijf die worden gebruikt voor het toepassen van de regel.

1. Hiermee kiest u de **[!UICONTROL Rule Type]** en definieert u de regel.

   De volgende secties verstrekken een gedetailleerde verklaring en een voorbeeld voor elk regeltype.

   ![&#x200B; Creërend een nieuwe goedkeuringsregel &#x200B;](./assets/approval-rules-create.png){width="700" zoomable="yes"}

1. Kies voor **[!UICONTROL Requires approval from]** een of meer vereiste fiatteurs op basis van het type goedkeuring.

   >[!NOTE]
   >
   >* Wanneer u een rol als fiatteur toewijst, moet u ervoor zorgen dat er ten minste één gebruiker in die rol is.
   >* Als er twee of meer gebruikers met dezelfde fiatteur zijn, kan de maker van de kooporder deze niet goedkeuren. In dit geval is handmatige goedkeuring vereist door elke andere gebruiker met deze goedkeurende rol. Nochtans, als `Auto-approve POs created within this role` optie in de [&#x200B; Toestemmingen van de Rol &#x200B;](account-company-roles-permissions.md) wordt geplaatst, wordt de kooporde automatisch goedgekeurd.
   >* Als er slechts één gebruiker met de goedkeurende rol is en die gebruiker de schepper is, wordt de kooporder altijd automatisch goedgekeurd-het `Auto-approve POs created within this role` toestemmingsplaatsen wordt genegeerd.

1. Klik op **[!UICONTROL Save]**.

### [!UICONTROL Order Total]

Dit regeltype wordt gebruikt om een goedkeuring van PO te vereisen die op het ordertotaal, met inbegrip van belasting wordt gebaseerd.

1. Hiermee kiest u een optie **[!UICONTROL Order Total amount]** :

   * `is more than`
   * `is less than`
   * `is more than or equal to`
   * `is less than or equal to`

1. Selecteert het valutatype en voer het bedrag in.

![&#x200B; de Totale Regel van de Goedkeuring van de Orde &#x200B;](./assets/approval-rules-order-total.png){width="600" zoomable="yes"}

### [!UICONTROL Shipping Cost]

Dit regeltype wordt gebruikt om een goedkeuring te vereisen van PO die op verzendkosten wordt gebaseerd, die vele bedrijven vereisen.

1. Hiermee stelt u de **[!UICONTROL Shipping cost value]** in:

   * `is more than`
   * `is less than`
   * `is more than or equal to`
   * `is less than or equal to`

1. Hiermee stelt u het gewenste verzendbedrag in.

![&#x200B; Verzendkosten Goedkeuringsregel &#x200B;](./assets/approval-rules-shipping-cost.png){width="600" zoomable="yes"}

### [!UICONTROL Number of SKUs]

Dit regeltype wordt gebruikt om een goedkeuring van PO te vereisen die op het aantal SKUs of unieke producten in de orde wordt gebaseerd. Het controleert het aantal verschillende punttypes, niet het aantal punten die worden bevolen. Een inkooporder kan bijvoorbeeld het volgende bevatten:

* Twee grote witte hemden
* Drie middelgrote witte hemden

Dit voorbeeld specificeert vijf punten, maar twee verschillende SKUs.

1. Hiermee wordt de waarde **[!UICONTROL Number of SKUs]** ingesteld:

   * `is more than`
   * `is less than`
   * `is more than or equal to`
   * `is less than or equal to`

1. Hiermee stelt u de hoeveelheid SKU&#39;s in.

![&#x200B; Aantal Regel van de Goedkeuring van SKUs &#x200B;](./assets/approval-rules-number-skus.png){width="600" zoomable="yes"}

## Goedkeuringsregels bewerken

Om een bestaande goedkeuringsregel te wijzigen, kan een klant de volgende stappen voltooien:

1. In de zijbalk van hun account selecteert de klant **[!UICONTROL Approval Rules]** .

1. Vindt de ingang van de goedkeuringsregel die moet worden uitgegeven.

1. Klik op **[!UICONTROL Edit]** .

1. Hiermee brengt u alle benodigde wijzigingen aan en klikt u op **[!UICONTROL Save]** .

## Goedkeuringsregels verwijderen

Om een bestaande goedkeuringsregel te verwijderen, kan een klant de volgende stappen voltooien:

1. Selecteer **[!UICONTROL Approval Rules]** in de zijbalk van hun account.

1. Vindt de ingang van de goedkeuringsregel die moet worden geschrapt.

1. Klik op **[!UICONTROL Delete]** .

1. Klik op **[!UICONTROL OK]** om de handeling te bevestigen.

## Goedkeuringsdemo voor inkooporders

Bekijk deze video voor meer informatie over goedkeuringen van inkooporders:

>[!VIDEO](https://video.tv.adobe.com/v/344450?quality=12&learn=on)
