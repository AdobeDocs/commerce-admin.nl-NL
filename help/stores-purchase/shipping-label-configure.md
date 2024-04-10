---
title: Verzendlabels configureren
description: Leer hoe u winkel kunt configureren voor het genereren van verzendlabels.
exl-id: 0693d74b-8b36-4a36-8739-c9fe5a934ff0
feature: Shipping/Delivery, Orders
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 0%

---

# Verzendlabels configureren

De volgende montages moeten op het productniveau, en in de configuratie van elke drager worden aangebracht die wordt gebruikt om etiketten te drukken. Als u labels wilt afdrukken, moet u voor alle carriers een account openen. Dan, voltooi de configuratie in uw opslag voor elke drager die u van plan bent te gebruiken.

## Vereisten voor vervoerders

| [!UICONTROL Carrier] | Vereisten |
|-------|--------|
| [USPS](usps.md) | Vereist een USPS-account. Vanaf 23 februari 2018 vereist USPS dat alle verzendlabels verzendingen bevatten. |
| [UPS](ups.md) | Vereist een UPS-account. Verzendlabels zijn alleen beschikbaar voor verzendingen die afkomstig zijn van de Amerikaanse specifieke gegevens die vereist zijn voor winkels buiten de VS. |
| [FedEx](fedex.md) | Vereist een FedEx-account. Voor winkels buiten de VS worden verzendlabels alleen ondersteund voor internationale verzendingen. FedEx staat binnenlandse zendingen die buiten de VS afkomstig zijn niet toe |
| [DHL](dhl.md) | Vereist een DHL-account. Verzendlabels worden alleen ondersteund voor verzendingen die afkomstig zijn uit de VS. |

{style="table-layout:auto"}

## Stap 1: Controleer het land van vervaardiging

Het land van vervaardiging is vereist voor alle producten die internationaal door USPS en FedEx worden verzonden. Als u veel producten hebt die moeten worden bijgewerkt, kunt u [import](../systems/data-import.md) de updates, of gebruik het net van de Inventaris om veelvoudige verslagen bij te werken.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Werk de record met het verzendlabel bij met een van de volgende methoden.

### Methode 1: één record bijwerken

1. Zoek in het raster het product dat u wilt bijwerken en open het in de bewerkingsmodus.

1. Werk de **Land van vervaardiging** indien nodig.

   ![Land van vervaardiging](./assets/product-country-of-manufacture.png){width="700" zoomable="yes"}

1. Klik op **[!UICONTROL Save]**.

### Methode 2: meerdere records bijwerken

1. Schakel in het raster het selectievakje in van elk product dat u wilt bijwerken.

   Bijvoorbeeld alle producten die in China worden vervaardigd.

1. Stel de **[!UICONTROL Actions]** controle op `Update Attributes` en klik op **[!UICONTROL Submit]**.

1. In de _Kenmerken bijwerken_ formulier, zoeken naar de **Land van vervaardiging** en selecteer de **Wijzigen** selectievakje.

1. Kies het land.

1. Klik op **[!UICONTROL Save]**.

## Stap 2 verifieert de opslaginformatie

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Sales]** en kiest u **[!UICONTROL Shipping Settings]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Origin]** en controleert u of de volgende velden zijn voltooid:

   - **[!UICONTROL Street Address]** - Het adres van de plaats van verzending. Bijvoorbeeld, de plaats van uw bedrijf of pakhuis. Dit veld is vereist voor verzendlabels.
   - **[!UICONTROL Street Address Line 2]** - Eventuele aanvullende adresgegevens, zoals de vloer of ingang. Het wordt aanbevolen dit veld te gebruiken.

   ![Oorsprong](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. In de _Verkoop_ in het linkerdeelvenster kiest u **[!UICONTROL Delivery Methods]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL USPS]** en controleert u of de volgende velden zijn voltooid:

   - **[!UICONTROL Secure Gateway URL]** - Het systeem voert automatisch de gateway-URL in.
   - **[!UICONTROL Password]** - Het wachtwoord wordt verstrekt door USPS en geeft u toegang tot hun systeem door de Diensten van het Web.
   - **Lengte, breedte, hoogte, breedte** - De standaardafmetingen van het pakket. Als u deze velden wilt weergeven, stelt u **[!UICONTROL Size]** tot `Large`.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **FedEx** en controleert u of de volgende velden zijn voltooid:

   - Meternummer
   - Sleutel
   - Wachtwoord

   Deze informatie wordt verstrekt door de drager, en wordt vereist om toegang tot hun systeem door de Diensten van het Web te verkrijgen.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL General]** en kiest u **[!UICONTROL General]** onder.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Store Information]** en controleert u of de volgende velden zijn voltooid:

   - **[!UICONTROL Store Name]** - De naam van de winkel- of winkelweergave.
   - **[!UICONTROL Store Contact Telephone]** - Het telefoonnummer van de primaire contactpersoon voor de winkel- of winkelweergave.
   - **[!UICONTROL Country]** - Het land waar je winkel is gevestigd.
   - **[!UICONTROL VAT Number]** - Indien van toepassing, het BTW-nummer van je winkel. (Niet vereist voor winkels die zijn gebaseerd in de VS.)
   - **[!UICONTROL Store Contact Address]** - Het adres van de straat van het primaire contact voor de winkel- of winkelweergave.

1. Als u meerdere opslagruimten hebt en de contactgegevens afwijken van de standaardinstelling, stelt u **[!UICONTROL Store View]** voor elke informatie en gaat zij na of de informatie volledig is.

   Als de informatie ontbreekt, wordt een fout weergegeven wanneer u de labels probeert af te drukken.

   ![Opslaggegevens](../configuration-reference/general/assets/general-store-information.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]**.
