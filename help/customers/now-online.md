---
title: Klanten zijn nu online
description: De _Now Online_ optie op het [!UICONTROL Customers ] menu maakt een lijst van alle klanten en bezoekers die momenteel online in uw opslag zijn.
exl-id: 69af669d-f9aa-471b-9d62-5657f3fb2103
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 0%

---

# Klanten zijn nu online

De optie **[!UICONTROL Now Online]** in het menu [!DNL Customers] bevat een lijst met alle klanten en bezoekers die momenteel online in uw winkel zijn. Het tijdsinterval dat klanten zoals momenteel online wordt getoond wordt geplaatst in de configuratie, en bepaalt hoe lang de [!DNL Customer's] activiteit van Admin zichtbaar is. Standaard is het interval 15 minuten. De sessie wordt beëindigd als het toetsenbord tijdens deze periode niet wordt gebruikt en klanten zich opnieuw moeten aanmelden bij hun accounts om verder te gaan met winkelen. Het is belangrijk op te merken dat de inhoud van de winkelwagentjes wordt bewaard voor latere toegang.

![ Online Klanten ](assets/customers-now-online.png){width="700" zoomable="yes"}

De onlinestatus van klanten wordt alleen bijgewerkt wanneer de klant zich aanmeldt, zich registreert of een andere statusveranderende gebeurtenis. Het omvat gebeurtenissen met betrekking tot winkelwagentjes, zoals het toevoegen, verwijderen en wijzigen van producten.

>[!NOTE]
>
>Bij paginabezoeken alleen wordt de online status van de klant niet bijgewerkt. Om dergelijke informatie te verzamelen, wordt het geadviseerd aan [ opstellings Googles Analytics ](../merchandising-promotions/google-analytics.md) (alleen of met [ de Manager van de Markering van Google ](../merchandising-promotions/google-tag-manager.md)) of andere analysesoftware met Adobe Commerce te gebruiken.

## Alle klanten die momenteel online zijn bekijken

Voor _Admin_ sidebar, ga **[!UICONTROL Customers]** > **[!UICONTROL Online Now]**.

>[!TIP]
>
>Voor informatie over het helpen van een online klant voltooit een aankoop, zie [ Shopping hulp ](../stores-purchase/introduction.md#shopping-assistance).

## Vorm het tijdinterval

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Customers]** uit en kies **[!UICONTROL Customer Configuration]** .

1. Vouw de sectie **[!UICONTROL Online Customers Options]** uit en voer de volgende handelingen uit:

   ![ Online de opties van de Klant ](../configuration-reference/customers/assets/customer-configuration-online-customers-options.png){width="600" zoomable="yes"}

   - Voer bij **[!UICONTROL Online Minutes Interval]** het aantal minuten in dat de sessie van de klant van de beheerder moet worden weergegeven. Laat het veld leeg om het standaardinterval van 15 minuten te accepteren.

   - Voer bij **[!UICONTROL Customer Data Lifetime]** het aantal minuten in voordat de niet-opgeslagen gegevens die de klant heeft ingevoerd, verlopen.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

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
