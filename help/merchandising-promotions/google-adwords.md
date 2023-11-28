---
title: Google AdWords
description: Leer hoe u de Commerce Store voor Google AdWords-conversie configureert om de advertentie te meten die tot een verkoop of andere waardevolle actie leidt.
exl-id: 3dd3beba-edcf-4f9e-a527-7ed3609ef1ae
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 0%

---

# Google AdWords

[Google AdWords][1] is een service waarmee u advertenties kunt plaatsen in de zoekresultaten van Google en op de pagina&#39;s van bedrijven in het Google Display Network. Het dashboard voor Advertenties bevat gereedschappen voor het beheren van uw campagnes, het bijhouden van reacties en het meten van resultaten.

Bij het bijhouden van de conversie ziet u het aantal advertenties dat tot een verkoop of een andere waardevolle handeling leidt. De _Succes_ De pagina die aan uw klant verschijnt nadat een orde is voorgelegd wordt gebruikt om omzettingen te volgen omdat het slechts na een verkoop verschijnt. Nadat u de configuratie van Google AdWords voor uw winkel hebt voltooid, hoeft u het script voor het bijhouden van de conversie niet meer naar de pagina Success te kopiëren, omdat Commerce al over de benodigde informatie beschikt. Zie voor meer informatie [Help bij Google AdWords][2].

![Zoekresultaten voor advertentie in Google](./assets/google-adwords-adobe-ad.png){width="500"}

## Stap 1. Een Google AdWords-campagne maken

1. Bezoek [Google AdWords][3]en meld u aan voor een account.

1. Volg de instructies om een campagne te maken.

1. Ga als volgt te werk als u conversie bijhouden voor uw campagne wilt instellen:

   - Op de **[!UICONTROL Tools]** tabblad van het dashboard voor Advertenties kiest u **[!UICONTROL Conversions]** en klik op **[!UICONTROL Conversion]**.

   - Kies bij de aanwijzing voor de conversiebron de optie **[!UICONTROL Website]**.

   - Voer een naam in voor de conversieactie die u wilt bijhouden en klik op **[!UICONTROL Done]**.

   - Klikken **[!UICONTROL Value]** en, indien van toepassing, een waarde aan de conversie toewijzen. Bijvoorbeeld:

      - Als je bij elke uitverkoop $5 maakt, kies je `Each time it happens` en wijs een waarde van `$5`.
      - Als de waarde van elke verkoop varieert, laat u de waarde leeg.

     Klik op **[!UICONTROL Done]**.

   - Klikken **[!UICONTROL Conversion windows]** en voltooi de instellingen om te bepalen hoe lang de omzettingen moeten worden bijgehouden, de rapportagecategorie en het toewijzingsmodel.

1. Klik op **[!UICONTROL Save and Continue]**.

## Stap 2. Uw conversietag ophalen

1. Onder **[!UICONTROL Install your tag]** kiest u ervoor om conversies te tellen op **[!UICONTROL Page load]**.

1. Als optie kunt u de optie **[!UICONTROL Google Site Stats]** kennisgeving aan de conversiepagina.

   De melding wordt in de onderhoek weergegeven met een koppeling naar beveiligingsstandaarden en cookiegebruik van Google.

1. Voer een van de volgende handelingen uit om te bepalen hoe u de tag AdWords wilt beheren:

   - Als u het script zelf aan uw winkel wilt toevoegen, kiest u **[!UICONTROL Save instructions and tag]**.
   - Als u wilt dat iemand anders het script aan uw winkel toevoegt, kiest u **[!UICONTROL Email instructions and tag]**.

1. Klik op **[!UICONTROL Done]**.

## Stap 3. Uw winkel configureren

{{gtag-api-note}}

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Ga als volgt te werk als u Google AdWords voor een specifieke winkelweergave configureert:

   - Kies in de linkerbovenhoek de optie **[!UICONTROL Store View]** dat moet worden gevormd.

   - Wanneer ertoe aangezet om werkingsgebiedomschakeling te bevestigen, klik **[!UICONTROL OK]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Sales]** en kiest u **[!UICONTROL Google API]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Google AdWords]** en voer de volgende handelingen uit:

   - Set **[!UICONTROL Enable]** tot `Yes`.

   - Voer de **[!UICONTROL Conversion ID]** in uw Google AdWords-script.

   ![Verkoopconfiguratie - Google Ads API](../configuration-reference/sales/assets/google-api-google-adwords.png){width="600" zoomable="yes"}

1. Ga als volgt te werk om de melding van de Google-sitestaat op te maken:

   - Set **[!UICONTROL Conversion Language]** in de taal die in het Google AdWords-script wordt geïdentificeerd.

   - Voer de **[!UICONTROL Conversion Format]** die moet worden gebruikt voor de kennisgeving van de Google Sites State op de conversiepagina.

      - `1`  - Geeft een bericht van één regel weer met een koppeling naar meer informatie over het bijhouden van Google.
      - `2` - Hiermee wordt een bericht weergegeven met twee regels en een koppeling naar meer informatie over het bijhouden van Google.
      - `3` - Geeft geen klantmelding weer.

   - Voer de [hexadecimale code][4]{:target=&quot;_blank&quot;} voor de **[!UICONTROL Conversion Color]** die u wilt gebruiken voor het meldingslabel voor Google Site Stats.

   - Voer de gecodeerde tekst voor de **[!UICONTROL Conversion Label]** die wordt weergegeven in het bericht voor de Google-sitestaat.

     Bijvoorbeeld: `MlEYCOKBnGoQz6CZoAM`

     **Voorbeeld van Google-code voor advertentietoorden**

     ```html
     <!-- Google Code for Back to School Sale Conversion Page -->
     <script type="text/javascript">
     /* <![CDATA[ */
     var google_conversion_id = 999999999;
     var google_conversion_language = "en";
     var google_conversion_format = "3";
     var google_conversion_color = "ffffff";
     var google_conversion_label = "MlEYCOKBnGoQz6CZoAM";
     var google_remarketing_only = false;
     /* ]]> */
     </script>
     
     <script type="text/javascript" src="//www.googleadservices.com/pagead/conversion.js">
     </script>
     <noscript>
     <div style="display:inline;">
     <img height="1" width="1" style="border-style:none;" alt="" src="//www.googleadservices.com/pagead/conversion/872829007/?label=MlEYCOKBnGoQz6CZoAM&amp;guid=ON&amp;script=0"/>
     
     </noscript>
     ```

1. Set **[!UICONTROL Conversion Value Type]** op een van de volgende wijzen:

   - `Dynamic` - Hiermee wordt bepaald dat er een conversie heeft plaatsgevonden op basis van de dynamische waarde voor Hoeveelheid bestelling.
   - `Constant` - Hiermee wordt bepaald dat een conversie heeft plaatsgevonden op basis van een opgegeven waarde.

   Voor een _Constante_ conversiewaardetype, voer een specifieke waarde in **[!UICONTROL Value]** voor de _[!UICONTROL Order Amount]_om als conversie te kwalificeren.

1. Klik op **[!UICONTROL Save Config]**.

## Stap 4. De configuratie controleren

Binnen een paar uur verandert de trackingstatus in het Google AdWords-dashboard van `Unverified` tot `No recent conversions` of `Recording conversions`. Wanneer iemand op uw advertentie klikt en een aankoop doet, wordt de conversie weergegeven op de pagina Conversiehandelingen van het dashboard en het campagnerapport.

[1]: https://www.google.com/adwords/
[2]: https://support.google.com/adwords/answer/6095821
[3]: https://ads.google.com/
[4]: https://www.w3schools.com/colors/colors_picker.asp
