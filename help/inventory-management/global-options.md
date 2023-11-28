---
title: "Configureren [!DNL Inventory Management] globale opties"
description: Leer hoe te om het gebrek te vormen [!DNL Inventory Management] configuratieopties voor product en voorraad voor uw websites.
exl-id: 1a8c9605-ae61-4d45-b549-64911b329203
feature: Inventory, Configuration
source-git-commit: 7384481d1a4a2a04882d4c99448cca75abc9be31
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 0%

---

# Configureren [!DNL Inventory Management] globale opties

Configureer de standaardconfiguratieopties voor product en voorraad voor uw websites. Sommige van deze instellingen kunnen per product worden overschreven via [Productopties configureren](product-options.md). Om de montages van de Prioriteit van de Afstand te vormen, zie [Algorithm Distance Priority configureren](distance-priority-algorithm.md).

## Wereldwijd product- en voorraadopties configureren

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Catalog]** en kiest u **[!UICONTROL Inventory]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Stock Options]** en stel de opties in:

   ![Opties voor voorraad](assets/config-catalog-inventory-stock-options.png){width="600" zoomable="yes"}

   - Als u de hoeveelheid op de hand wilt aanpassen wanneer een bestelling wordt geplaatst, stelt u **[!UICONTROL Decrease Stock When Order is Placed]** tot `Yes`.

   - Om items in voorraad te retourneren als een bestelling wordt geannuleerd, **[!UICONTROL Set Items' Status to be in Stock When Order in Cancelled]** tot `Yes`.

   - Als u wilt doorgaan met het weergeven van producten in de catalogus die niet meer in voorraad zijn, stelt u **[!UICONTROL Display Out of Stock Products]** tot `Yes`.

   - Indien [prijswaarschuwingen](alert-setup.md) zijn ingeschakeld, kunnen klanten zich aanmelden om op de hoogte te worden gesteld wanneer het product weer in voorraad is.

   - Als u het begin wilt instellen voor de weergave van de laatste resterende voorraad op de productpagina, voert u een bedrag in voor **[!UICONTROL Only X left Threshold]**.

     Het bericht wordt weergegeven wanneer de voorraad de drempel bereikt. Als u bijvoorbeeld instelt op `3`, het bericht `Only 3 left` wordt weergegeven wanneer de voorraad meer dan drie bedraagt. Het bericht wordt aangepast aan de hoeveelheid in voorraad tot de hoeveelheid nul bereikt.

   - Als u een bericht &quot;In voorraad&quot; of &quot;Uit voorraad&quot; wilt weergeven op de productpagina, stelt u **[!UICONTROL Display Products Availability In Stock on Storefront]** tot `Yes`.

   - Als u de voorraad wilt controleren tijdens het laden van een product in het winkelwagentje, stelt u **[!UICONTROL Enable Inventory Check On Cart Load]** tot `Yes`. Als deze optie is uitgeschakeld, wordt de voorraadcontrole overgeslagen. Als u deze optie uitschakelt, wordt het afrekenen versneld, vooral als er veel winkelwagentjes zijn. Als u de pre-validatie echter overslaat, kunnen klanten later tijdens het afrekenen fouten van het type &quot;out of stock&quot; zien.

   - Als u de consistentie tussen de voorraad en de catalogus wilt behouden, stelt u **[!UICONTROL Synchronize with Catalog]** tot `Yes`. Als deze optie is ingeschakeld, worden de inventarisgegevens aangepast aan de wijzigingen in de catalogus (zoals het verwijderde product, de gewijzigde productSKU en het gewijzigde producttype).

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Product Stock Options]** en stel de opties in:

   - Om te activeren [inventariscontrole](enable.md) voor uw catalogus, set **[!UICONTROL Manage Stock]** tot `Yes`.

     ![Opties voor productvoorraad](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - Set **[!UICONTROL Backorders]** op een van de volgende wijzen:

     | Optie | Beschrijving |
     | ----- | ----- |
     | `No Backorders` | [Achtergronden](backorders.md) worden niet geaccepteerd als het product uit voorraad is. |
     | `Allow Qty Below 0` | Achterorden worden geaccepteerd als de hoeveelheid onder nul daalt. |
     | `Allow Qty Below 0 and Notify Customer` | Backorders worden geaccepteerd als het aantal minder is dan nul en het systeem de klant meldt dat de bestelling nog steeds kan worden geplaatst. |

   - Voer de **[!UICONTROL Maximum Qty Allowed in Shopping Cart]**.

   - Voer een bedrag in voor de **[!UICONTROL Out-of-Stock Threshold]**:

     | Waarde | Beschrijving |
     | ----- |-----|
     | Positief bedrag | Voer een positieve waarde in als Achterordes uitgeschakeld is. |
     | Nul | Als Achterorden ingeschakeld, voert u `0` staat voor oneindige achterorden toe. |
     | Negatief bedrag | Als Achterorden ingeschakeld, wordt u aangeraden een negatief bedrag in te voeren. Het bedrag wordt toegevoegd aan de verkoopbare hoeveelheid. Voer bijvoorbeeld `-50` om opdrachten tot dit bedrag toe te staan. |

   - Voer de **[!UICONTROL Minimum Qty Allowed in Shopping Cart]** voor de geselecteerde groep en bedragen.

   - Voor **[!UICONTROL Notify for Quantity Below]** Voer het voorraadniveau in dat de melding activeert dat het item niet langer in voorraad is.

   - Als u de hoeveelheid wilt verhogen voor het product, stelt u **[!UICONTROL Enable Qty Increments]** tot `Yes`. Dan, voor **[!UICONTROL Qty Increments]** Voer het aantal objecten in dat moet worden aangeschaft om aan de vereiste te voldoen.

     Een artikel dat in stappen van zes wordt verkocht, kan bijvoorbeeld in hoeveelheden van `6`, `12`, `18`, enzovoort.

   - Voor [!DNL Inventory Management], **[!UICONTROL Automatically Return Credit Memo Item to Stock]** is ingesteld op `No`. Wanneer u een creditnota indient, voert u deze in en selecteert u deze om de voorraad terug te brengen naar bronnen.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Admin bulk operations]** en stel de opties in:

   ![Bulkbewerkingen voor beheerders](assets/config-catalog-inventory-admin-bulk-operations.png){width="600" zoomable="yes"}

   - Set **[!UICONTROL Run asynchronously]** bulkbewerkingen asynchroon uitvoeren voor acties voor massaproducten

     Deze bewerkingen omvatten bulk [Bronnen toewijzen en de toewijzing ervan opheffen](bulk-assignment.md), en [inventariseren naar bron](inventory-transfer.md). Het verzamelt bulkacties tot de Asynchrone partijgrootte, dan stelt die acties in werking. Deze optie is standaard uitgeschakeld. U wordt aangeraden de prestaties te beoordelen met acties in bulk voordat u deze inschakelt.

     >[!NOTE]
     >
     >Configureren en ondersteunen _asynchrone rijmanagers_, moet u een bevel uitgeven gebruikend de bevellijn. Voor deze stap is mogelijk hulp van ontwikkelaars nodig. Zie [Gebruikers in de wachtrij met berichten starten](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html) in de _Configuratiegids_.

   - Indien ingeschakeld, stelt u de **[!UICONTROL Asynchronous batch size]**. De standaardbatch-grootte is 100. Wanneer de bulkprocessen dit bedrag bereiken, teweegbrengt het systeem het.

1. Klik op **[!UICONTROL Save Config]**.
