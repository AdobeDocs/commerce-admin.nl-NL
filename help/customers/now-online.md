---
title: Klanten zijn nu online
description: De optie _Now Online_ op de knop [!UICONTROL Customers ]worden alle klanten en bezoekers weergegeven die momenteel online in uw winkel zijn.
exl-id: 69af669d-f9aa-471b-9d62-5657f3fb2103
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---

# Klanten zijn nu online

De **[!UICONTROL Now Online]** de optie [!DNL Customers] worden alle klanten en bezoekers weergegeven die momenteel online in uw winkel zijn. Het tijdsinterval dat de klanten zoals momenteel online worden getoond wordt geplaatst in de configuratie, en bepaalt hoe lang [!DNL Customer's] activiteit is zichtbaar vanuit de beheerder. Standaard is het interval 15 minuten. De sessie wordt beëindigd als het toetsenbord tijdens deze periode niet wordt gebruikt en klanten zich opnieuw moeten aanmelden bij hun accounts om verder te gaan met winkelen. Het is belangrijk op te merken dat de inhoud van de winkelwagentjes wordt bewaard voor latere toegang.

![Online klanten](assets/customers-now-online.png){width="700" zoomable="yes"}

De onlinestatus van klanten wordt alleen bijgewerkt wanneer de klant zich aanmeldt, zich registreert of een andere statusveranderende gebeurtenis. Het omvat gebeurtenissen met betrekking tot winkelwagentjes, zoals het toevoegen, verwijderen en wijzigen van producten.

>[!NOTE]
>
>Bij paginabezoeken alleen wordt de online status van de klant niet bijgewerkt. Om dergelijke informatie te verzamelen, wordt aanbevolen [Googles Analytics instellen](../merchandising-promotions/google-analytics.md) (alleen of met [Google-tagbeheer](../merchandising-promotions/google-tag-manager.md)) of gebruik andere analysesoftware met Adobe Commerce.

## Alle klanten die momenteel online zijn bekijken

Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Customers]** > **[!UICONTROL Online Now]**.

>[!TIP]
>
>Voor informatie over hoe een online klant een aankoop kan voltooien, raadpleegt u [Hulp bij winkelen](../stores-purchase/introduction.md#shopping-assistance).

## Vorm het tijdinterval

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Customers]** en kiest u **[!UICONTROL Customer Configuration]**.

1. Breid uit **[!UICONTROL Online Customers Options]** en voer de volgende handelingen uit:

   ![Online klantopties](../configuration-reference/customers/assets/customer-configuration-online-customers-options.png){width="600" zoomable="yes"}

   - Voor **[!UICONTROL Online Minutes Interval]**, voert u het aantal minuten in dat de sessie van de klant van de beheerder kan worden weergegeven. Laat het veld leeg om het standaardinterval van 15 minuten te accepteren.

   - Voor **[!UICONTROL Customer Data Lifetime]**, voert u het aantal minuten in voordat de niet-opgeslagen gegevens die de klant heeft ingevoerd, verlopen.

1. Klik op **[!UICONTROL Save Config]**.

## Kolombeschrijvingen

| Kolom | Beschrijving |
| --- | --- |
| **[!UICONTROL ID]** | De klant-id van een geregistreerde klant. |
| **[!UICONTROL First Name]** | De voornaam van een geregistreerde klant. |
| **[!UICONTROL Last Name]** | De achternaam van een geregistreerde klant. |
| **[!UICONTROL Email]** | Het e-mailadres van een geregistreerde klant. |
| **[!UICONTROL Last Activity]** | De datum en tijd van de laatste activiteit van de klant in uw winkel. |
| **[!UICONTROL Type]** | Opties: `Customer` / `Visitor` |
| **[!UICONTROL Last URL]** | De laatste URL die de klant heeft bezocht. |
| **[!UICONTROL Company]** | De naam van het bedrijf waartoe de gebruiker behoort. |

{style="table-layout:auto"}
