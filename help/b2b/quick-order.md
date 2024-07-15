---
title: Snelle bestellingen
description: Meer informatie over de functionaliteit voor snelle bestellingen en het inschakelen ervan voor uw klanten.
exl-id: 7007e1b4-a64f-46fe-a235-3ca9f64e77e4
feature: B2B, Orders
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---

# Snelle bestellingen

De _Snelle eigenschap van de Orde_ vermindert het ordeproces aan verscheidene kliks voor klanten die de productnaam of SKU van de producten kennen die zij willen tot opdracht geven. Orders met meerdere SKU&#39;s kunnen handmatig worden ingevoerd of in het formulier Snelle volgorde worden ingevoerd. De snelle orde kan door klanten worden gebruikt die aan hun rekeningen, en door gasten worden het programma geopend. Wanneer toegelaten, verschijnt de _Snelle verbinding van de Orde_ bij de bovenkant van de pagina, naast de klantennaam.

![ Snelle verbinding van de Orde ](./assets/quick-order-link.png){width="700" zoomable="yes"}

## Snelle bestellingen inschakelen voor uw winkel

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Kies **[!UICONTROL B2B Features]** in de sectie _[!UICONTROL General]_in het linkerdeelvenster.

1. Stel **[!UICONTROL Enable Quick Order]** in op `Yes` .

   ![ laat Snelle Orde ](./assets/quick-orders-config.png){width="600" zoomable="yes"} toe

1. Klik op **[!UICONTROL Save Config]**.

1. Wanneer ertoe aangezet, klik [ Beheer van het Geheime voorgeheugen ](../systems/cache-management.md) en vernieuw om het even welke ongeldige geheime voorgeheugens.

## Workflows voor snelle volgorde

Klanten kunnen producten voor snelle bestellingen opgeven met een van de volgende methoden.

### Methode 1: afzonderlijke producten invoeren

1. De klant klikt op de koppeling **[!UICONTROL Quick Order]** .

1. Selecteert het product op SKU of productnaam:

   Om a **snelle orde door SKU** te plaatsen, doet de klant het volgende:

   - Voer de **[!UICONTROL SKU]** in.

   - Klik op **[!UICONTROL Add to List]** .

     De SKU verschijnt in de inputlijn, met de productdetails hieronder.

     ![ Snel Detail van de Orde ](./assets/quick-order-product-detail.png){width="600" zoomable="yes"}

   Om a **snelle orde door de productnaam** te plaatsen, doet de klant het volgende:

   - Voer de eerste paar tekens van de **[!UICONTROL Product Name]** in.

     >[!NOTE]
     >
     >Gebruik niet _ga_ sleutel in om de naam van het product te kiezen.

   - Wanneer de lijst met mogelijke overeenkomsten wordt weergegeven, klikt de klant op het product dat hij of zij wil bestellen.

     ![ klik om de Naam van het Product te kiezen ](./assets/quick-order-product-name.png){width="700" zoomable="yes"}

1. Voer de **[!UICONTROL Qty]** in.

1. Gebruikend de volgende inputlijn, herhaalt dit proces zo vaak als noodzakelijk.

1. Klik op **[!UICONTROL Add to Cart]** .

### Methode 2: meerdere producten invoeren

1. In het vak **[!UICONTROL Enter Multiple SKUs]** voert de klant een van de volgende handelingen uit:

   - voert één SKU per regel in

   - Hiermee voert u alle SKU&#39;s op dezelfde regel in, gescheiden door komma&#39;s en zonder spaties.

     ![ ga Veelvoudige SKUs ](./assets/quick-order-skus.png){width="600" zoomable="yes"} in

1. Als u de producten aan de lijst wilt toevoegen, klikt u op **[!UICONTROL Add to List]** .

1. Voert de **[!UICONTROL Qty]** in die voor elk item in de lijst moet worden geordend.

   ![ Snelle Lijst van de Orde ](./assets/quick-order-skus-detail.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Als het product de vereiste opties heeft, wordt de klant gevraagd om de opties te kiezen. Ze kunnen wachten tot ze het winkelwagentje bereiken om productopties toe te voegen.

   ![ kies Opties ](./assets/quick-order-skus-product-options.png){width="600" zoomable="yes"}

### Methode 3: Een lijst met producten uploaden

1. Klik in de sectie _[!UICONTROL Add from File]_op **[!UICONTROL Download Sample]**om een ordersjabloon te downloaden.

   ![ voeg van Dossier ](./assets/quick-order-skus-add-from-file.png){width="600" zoomable="yes"} toe

1. Hiermee opent u het gedownloade bestand.

1. Gebruikt de sjabloon om de product-SKU&#39;s toe te voegen die u wilt uploaden voor de lijst Snelle volgorde.

1. Klik op **[!UICONTROL Save]** wanneer dit is voltooid.

   ![ SKUs aan Upload ](./assets/quick-order-skus-add-from-file-sample.png){width="400" zoomable="yes"}

1. Als u het bestand wilt uploaden, klikt u op **[!UICONTROL Choose]** en selecteert u het bestand van het systeem.

   De items worden toegevoegd aan de lijst Snelle volgorde.

1. Klik indien gereed op **[!UICONTROL Add to Cart]** .

Nadat de klant de snelle bestelling heeft gemaakt, kan hij of zij op de gebruikelijke wijze de afhandeling voltooien.

![ Snelle Orde ](./assets/quick-order-add-to-cart.png){width="700" zoomable="yes"}
