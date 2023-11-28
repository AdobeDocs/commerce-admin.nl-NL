---
title: Cadeaucreditcardrekeningen
description: Leer over geschenkkaartrekeningen en hoe te om de standaardmontages voor het beheer van de codepool te vormen.
exl-id: f8caff04-38fd-4195-ab11-77dae900976d
feature: Products, Gift, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '930'
ht-degree: 0%

---

# Cadeaucreditcardrekeningen

Er wordt automatisch een cadeaukaartaccount aangemaakt voor elke cadeaukaart die wordt aangeschaft. De waarde van de cadeaukaart kan vervolgens worden toegepast op de aankoop van een product in uw winkel. U kunt ook cadeaukaartaccounts maken via de beheerfunctie als speciale actie of service voor klanten. Het rekeningnummer van de cadeaukaart komt overeen met de code van de cadeau-kaart.

![Cadeaucreditcardrekeningen](./assets/marketing-gift-card-accounts-grid.png){width="700" zoomable="yes"}

## Kaartaccounts configureren

De configuratie van de cadeaukaart bepaalt de standaardinstellingen voor alle cadeaukaarten voor de winkelweergave en beheert de codepool. De codepool is een reeks unieke kaartcodes in een specifiek formaat. De codes van de pool worden gebruikt telkens als een geschenkkaartrekening wordt gecreeerd. De beheerder van de winkel moet ervoor zorgen dat er voldoende codes beschikbaar zijn voor de verkoop van cadeaukaarten. Zorg ervoor dat u een codepool genereert voordat u cadeaukaarten te koop aanbiedt. Adobe Commerce genereert standaard 1.000 codes. Er wordt geen nieuwe codepool gegenereerd totdat er geen codes meer beschikbaar zijn in de huidige pool.

### Stap 1: E-mailmeldingen configureren

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Sales]** en kiest u **[!UICONTROL Gift Cards]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de _[!UICONTROL Gift Card Email Settings]_en voer de volgende handelingen uit:

   - Set **[!UICONTROL Gift Card Notification Email Sender]** aan de winkelidentiteit die wordt weergegeven als de afzender van kaartmeldingen.

   - Set **[!UICONTROL Gift Card Notification Email Template]** aan het malplaatje dat voor het bericht wordt gebruikt.

   ![E-mailinstellingen creditcard](../configuration-reference/sales/assets/gift-cards-gift-card-email-settings.png){width="600" zoomable="yes"}

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de _[!UICONTROL Email Sent from Gift Card Account Management]_en voer de volgende handelingen uit:

   - Set **[!UICONTROL Gift Card Email Sender]** aan de winkelidentiteit om te worden weergegeven als de afzender van de cadeaukaarten.

   - Set **[!UICONTROL Gift Card Template]** naar de sjabloon die u voor de cadeaukaart wilt gebruiken.

Zie [E-mailadressen van winkel](../configuration-reference/general/store-email-addresses.md) voor specifieke configuratiegebieden en opties.

### Stap 2: De algemene instellingen voltooien

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de _[!UICONTROL Gift Card General Settings]_sectie.

1. Om de klant in staat te stellen de waarde op de kaart in te wisselen voor contanten, stelt u **[!UICONTROL Redeemable]** tot `Yes`.

1. Voor **[!UICONTROL Lifetime (days)]** Voer het aantal dagen in voordat de kaart verloopt.

   Laat het veld leeg als er geen vervaldatum is.

   >[!NOTE]
   >
   >Afhankelijk van uw locatie kan het ongeldig zijn om cadeaukaarten te laten verlopen. Controleer uw lokale wetten voordat u een leven instelt voor uw cadeaukaarten.

1. Als u klanten de optie wilt geven om een bericht bij de cadeaukaart in te voeren, stelt u **[!UICONTROL Allow Gift Message]** tot `Yes` en voer het aantal tekens in dat beschikbaar is voor het bericht voor **[!UICONTROL Gift Message Maximum Length]**.

1. Set **[!UICONTROL Generate Gift Card Account when Orders Item is]** op een van de volgende wijzen:

   - `Ordered` - De rekening van de cadeaukaart wordt gecreeerd wanneer de orde wordt geplaatst.
   - `Invoiced` - De rekening van de cadeaukaart wordt gecreeerd nadat de betaling wordt gevangen en de orde wordt gefactureerd.

   ![Algemene instellingen voor creditcard](../configuration-reference/sales/assets/gift-cards-gift-card-general-settings.png){width="600" zoomable="yes"}

### Stap 3: Bepaal de groep van de cadeaukaartcode

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de _[!UICONTROL Gift Card Account General Settings]_en voer de volgende handelingen uit:

   ![Algemene instellingen Cadeaukaartaccount](../configuration-reference/sales/assets/gift-cards-gift-card-account-general-settings.png){width="600" zoomable="yes"}

   - Als u de code wilt aanpassen, voert u het volgende in op basis van uw voorkeur:

      - Lengte code
      - Codeopmaak
      - Codevoorvoegsel
      - Codeachtervoegsel
      - Streep om de X-tekens

   - Om het aantal te produceren codes te bepalen, ga in **[!UICONTROL New Pool Size]**.

   - Om te specificeren wanneer u bericht ontvangt om de codepool te hervoorraaden, ga in **[!UICONTROL Low Code Pool Threshold]**.

1. Klik voordat u de codegroep genereert op **[!UICONTROL Save Config]**.

1. Klik op **[!UICONTROL Generate]**.

1. Klik op **[!UICONTROL Save Config]**.

## Een bestaande cadeaukaartaccount bekijken

1. Ga als volgt te werk om het nummer van het kaartenaccount voor een huidige bestelling te zoeken:

   - Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

   - Zoek de volgorde in de lijst en klik op **[!UICONTROL View]** in de _[!UICONTROL Action]_kolom.

   - Omlaag schuiven naar de _[!UICONTROL Items Ordered]_sectie.

   Het nummer staat in de _[!UICONTROL Product]_kolom, onder **[!UICONTROL Gift Card Accounts]**.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Gift Card Accounts]**.

1. Zoek het kaartenaccount in het raster en open het in de bewerkingsmodus.

   De code van de cadeau-kaart wordt boven aan het scherm weergegeven _Informatie_ sectie.

   ![Cadeaukaartgegevens](./assets/gift-card-account-information.png){width="600" zoomable="yes"}

## Een kaartenaccount voor cadeaus maken

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Gift Card Accounts]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Add Gift Card Account]**.

1. In de _[!UICONTROL Information]_sectie, set **[!UICONTROL Active]**tot `Yes` en voer de volgende handelingen uit:

   - Om het creditsaldo van de kaart bij afhandeling terug te betalen of naar het winkelkrediet van de klant over te dragen, stelt u **[!UICONTROL Redeemable]** tot `Yes`.

   - Kies de optie **[!UICONTROL Website]** waar het geschenkkaartaccount kan worden gebruikt.

   - Voer de initiaal in **[!UICONTROL Balance]** op de cadeaukaart.

   - _(Optioneel)_ Om een **[!UICONTROL Expiration Date]** voor de cadeaukaart selecteert u de datum in de kalender ![Kalenderpictogram](../assets/icon-calendar.png).

     Als deze optie leeg blijft, verloopt de rekening van de cadeaukaart niet.

     ![Nieuw account](./assets/gift-card-account-add-new.png){width="600" zoomable="yes"}

1. Kies in het linkerdeelvenster de optie **[!UICONTROL Send Gift Card]** en voer de volgende handelingen uit:

   - Voer de **[!UICONTROL Recipient Email]** adres.

   - Voer de **[!UICONTROL Recipient Name]**.

   - Set **[!UICONTROL Send Email from the Following Store View]** in de winkelweergave die wordt weergegeven als de verzender van het bericht voor de cadeaukaart.

   ![Cadeauinstellingen verzenden](./assets/marketing-gift-card-accounts-new-send.png){width="600" zoomable="yes"}

1. Voer een van de volgende handelingen uit om het nieuwe account op te slaan:

   - Als u niet klaar bent om de cadeaukaart te verzenden, klikt u op **[!UICONTROL Save]**.

   - Klik op **E-mail opslaan en verzenden**.

## Accountgeschiedenis van cadeaukaart weergeven

1. Ga naar **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Gift Card Accounts]**.

1. Open de cadeaukaart in de bewerkingsmodus.

1. De **[!UICONTROL History]** van de cadeaukaart wordt weergegeven.

   ![Cadeaugeschiedenis](./assets/gift-card-history.png){width="600" zoomable="yes"}

| Kolom | Beschrijving |
|--- |--- |
| [!UICONTROL ID] | Een unieke numerieke actie met een cadeaukaart. |
| [!UICONTROL Date] | Datum van actie. |
| [!UICONTROL Action] | Hiermee bepaalt u alle mogelijke handelingen met een cadeaukaart. Opties: `Created` / `Updated` / `Sent` / `Used` / `Redeemed` / `Expired` |
| [!UICONTROL Balance Change] | Hiermee geeft u het bedrag weer waarmee het saldo van de cadeaukaart is gewijzigd. |
| [!UICONTROL Balance] | Geeft de beschikbare balans aan. |
| [!UICONTROL More Information] | Hier wordt informatie weergegeven over wie de balans van de cadeaukaart heeft gewijzigd. |

{style="table-layout:auto"}

## Een kaartenaccount voor cadeaus verwijderen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Gift Card Accounts]**.

1. Selecteer het kaartenaccount dat u wilt verwijderen en open het in de bewerkingsmodus.

1. Klik in de menubalk op **[!UICONTROL Delete]**.

1. Klik op **[!UICONTROL OK]**.

## Kolombeschrijvingen

| Kolom | Beschrijving |
|--- |--- |
| [!UICONTROL ID] | Een unieke numerieke id die is toegewezen aan een cadeaukaartaccount. |
| [!UICONTROL Code] | De code die moet worden ingevoerd om een cadeaukaart toe te passen. |
| [!UICONTROL Website] | Geeft de websites aan waar het account voor de cadeaukaart beschikbaar is. |
| [!UICONTROL Created] | Aanmaakdatum. |
| [!UICONTROL End] | Vervaldatum van creditcard, indien gepland. |
| [!UICONTROL Active] | Hiermee bepaalt u of de cadeaukaart actief is. |
| [!UICONTROL Status] | Hiermee bepaalt u of de cadeaukaart wordt afgelost in de account van de klant of beschikbaar is. Opties: `Used` / `Redeemed` / `Expired` |
| [!UICONTROL Balance] | Geeft de beschikbare balans aan. |

{style="table-layout:auto"}
