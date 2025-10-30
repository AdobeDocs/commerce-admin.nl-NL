---
title: Verzendlabels configureren
description: Leer hoe u winkel kunt configureren voor het genereren van verzendlabels.
exl-id: 0693d74b-8b36-4a36-8739-c9fe5a934ff0
feature: Shipping/Delivery, Orders
source-git-commit: d5beff4d450dab21f74e5baec6b718b844963858
workflow-type: tm+mt
source-wordcount: '593'
ht-degree: 0%

---

# Verzendlabels configureren

De volgende montages moeten op het productniveau, en in de configuratie van elke drager worden aangebracht die wordt gebruikt om etiketten te drukken. Als u labels wilt afdrukken, moet u voor alle carriers een account openen. Dan, voltooi de configuratie in uw opslag voor elke drager die u van plan bent te gebruiken.

## Vereisten voor vervoerders

| [!UICONTROL Carrier] | Vereisten |
|-------|--------|
| [ USPS ](usps.md) | Vereist een USPS-account voor verzendlabel. |
| [ UPS ](ups.md) | Vereist een UPS-account. Verzendlabels zijn alleen beschikbaar voor verzendingen die afkomstig zijn van de Amerikaanse specifieke gegevens die vereist zijn voor winkels buiten de VS. |
| [ FedEx ](fedex.md) | Vereist een FedEx-account. Voor winkels buiten de VS worden verzendlabels alleen ondersteund voor internationale verzendingen. FedEx staat binnenlandse zendingen die buiten de VS afkomstig zijn niet toe |
| [ DHL ](dhl.md) | Vereist een DHL-account. Verzendlabels worden alleen ondersteund voor verzendingen die afkomstig zijn uit de VS. |

{style="table-layout:auto"}

## Stap 1: Controleer het land van vervaardiging

Het land van vervaardiging is vereist voor alle producten die internationaal door USPS en FedEx worden verzonden. Als u vele producten hebt die zouden moeten worden bijgewerkt, kunt u of [ invoeren ](../systems/data-import.md) de updates, of het net van de Inventaris gebruiken om veelvoudige verslagen bij te werken.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Werk de record met het verzendlabel bij met een van de volgende methoden.

### Methode 1: één record bijwerken

1. Zoek in het raster het product dat u wilt bijwerken en open het in de bewerkingsmodus.

1. Werk het **Land van Vervaardiging** zoals nodig bij.

   ![ Land van Vervaardiging ](./assets/product-country-of-manufacture.png){width="700" zoomable="yes"}

1. Klik op **[!UICONTROL Save]**.

### Methode 2: meerdere records bijwerken

1. Schakel in het raster het selectievakje in van elk product dat u wilt bijwerken.

   Bijvoorbeeld alle producten die in China worden vervaardigd.

1. Stel het besturingselement **[!UICONTROL Actions]** in op `Update Attributes` en klik op **[!UICONTROL Submit]** .

1. In de _vorm van Attributen van de Update_, vind het **Land van Vervaardiging** gebied en selecteer **checkbox van de Verandering**.

1. Kies het land.

1. Klik op **[!UICONTROL Save]**.

## Stap 2 verifieert de opslaginformatie

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Shipping Settings]** .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Origin]** sectie uit, en verifieer dat de volgende gebieden volledig zijn:

   - **[!UICONTROL Street Address]** - Het adres van de straat van de plaats van verzending. Bijvoorbeeld, de plaats van uw bedrijf of pakhuis. Dit veld is vereist voor verzendlabels.
   - **[!UICONTROL Street Address Line 2]** - Eventuele aanvullende adresgegevens, zoals de vloer of ingang. Het wordt aanbevolen dit veld te gebruiken.

   ![ Oorsprong ](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. In de _sectie van de Verkoop_ in het linkerpaneel, kies **[!UICONTROL Delivery Methods]**.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL USPS]** sectie uit, en verifieer dat de volgende gebieden volledig zijn:

   - **[!UICONTROL Secure Gateway URL]** - Het systeem voert automatisch de gateway-URL in.
   - **[!UICONTROL Password]** - Het wachtwoord wordt verstrekt door USPS en geeft u toegang tot hun systeem door de Diensten van het Web.
   - **Lengte, Breedte, Hoogte, Meisje** - de standaardafmetingen van het pakket. Als u deze velden wilt weergeven, stelt u **[!UICONTROL Size]** in op `Large` .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) uit de **** sectie FedEx en verifieer dat de volgende gebieden volledig zijn:

   - Meternummer
   - Sleutel
   - Wachtwoord

   Deze informatie wordt verstrekt door de drager, en wordt vereist om toegang tot hun systeem door de Diensten van het Web te verkrijgen.

1. Vouw in het linkerdeelvenster **[!UICONTROL General]** uit en kies **[!UICONTROL General]** eronder.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Store Information]** sectie uit en verifieer dat de volgende gebieden volledig zijn:

   - **[!UICONTROL Store Name]** - De naam van de winkel- of opslagweergave.
   - **[!UICONTROL Store Contact Telephone]** - Het telefoonnummer van de primaire contactpersoon voor de winkel- of winkelweergave.
   - **[!UICONTROL Country]** - Het land waar je winkel is gevestigd.
   - **[!UICONTROL VAT Number]** - Indien van toepassing, het BTW-nummer van je winkel. (Niet vereist voor winkels die zijn gebaseerd in de VS.)
   - **[!UICONTROL Store Contact Address]** - Het adres van de straat van de primaire contactpersoon voor de winkel- of winkelweergave.

1. Als u meerdere opslagruimten hebt en de contactgegevens afwijken van de standaardinstelling, stelt u **[!UICONTROL Store View]** voor elke opslagruimte in en controleert u of de gegevens volledig zijn.

   Als de informatie ontbreekt, wordt een fout weergegeven wanneer u de labels probeert af te drukken.

   ![ Informatie van de Opslag ](../configuration-reference/general/assets/general-store-information.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]**.
