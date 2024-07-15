---
title: Google AdWords
description: Leer hoe u uw Commerce-winkel configureert voor het bijhouden van Google AdWords-conversies om de advertentie te meten die tot een verkoop of andere waardevolle actie leidt.
exl-id: 3dd3beba-edcf-4f9e-a527-7ed3609ef1ae
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 0%

---

# Google AdWords

[ Google AdWords ][1] is de dienst die u kunt gebruiken om advertenties in de resultaten van het Onderzoek van Google en op de pagina&#39;s van bedrijven in het Netwerk van de Vertoning van Google te plaatsen. Het dashboard voor Advertenties bevat gereedschappen voor het beheren van uw campagnes, het bijhouden van reacties en het meten van resultaten.

Bij het bijhouden van de conversie ziet u het aantal advertenties dat tot een verkoop of een andere waardevolle handeling leidt. De _pagina van het Succes_ die aan uw klant verschijnt nadat een orde is voorgelegd wordt gebruikt om omzettingen te volgen omdat het slechts na een verkoop verschijnt. Nadat u de configuratie van Google AdWords voor uw winkel hebt voltooid, hoeft u het script voor het bijhouden van de conversie niet meer naar de pagina Success te kopiëren, omdat Commerce al over de benodigde informatie beschikt. Meer leren, zie [ Hulp AdWords van Google ][2].

![ Adobe en in de Resultaten van het Onderzoek van Google ](./assets/google-adwords-adobe-ad.png){width="500"}

## Stap 1. Een Google AdWords-campagne maken

1. Bezoek [ Google AdWords ][3], en onderteken omhoog voor een rekening.

1. Volg de instructies om een campagne te maken.

1. Ga als volgt te werk als u conversie bijhouden voor uw campagne wilt instellen:

   - Kies **[!UICONTROL Conversions]** op het tabblad **[!UICONTROL Tools]** van het dashboard voor AdWords en klik op **[!UICONTROL Conversion]** .

   - Kies **[!UICONTROL Website]** wanneer hierom wordt gevraagd.

   - Voer een naam in voor de conversieactie die u wilt bijhouden en klik op **[!UICONTROL Done]** .

   - Klik op **[!UICONTROL Value]** en wijs, indien van toepassing, een waarde toe aan de conversie. Bijvoorbeeld:

      - Als u bij elke uitverkoop $5 maakt, kiest u `Each time it happens` en wijst u een waarde van `$5` toe.
      - Als de waarde van elke verkoop varieert, laat u de waarde leeg.

     Klik op **[!UICONTROL Done]** om te voltooien.

   - Klik op **[!UICONTROL Conversion windows]** en voer de instellingen in om te bepalen hoe lang de conversies moeten worden bijgehouden, welke rapportcategorie en welk toewijzingsmodel.

1. Klik op **[!UICONTROL Save and Continue]** als de bewerking is voltooid.

## Stap 2. Uw conversietag ophalen

1. Kies onder **[!UICONTROL Install your tag]** om conversies te tellen op **[!UICONTROL Page load]** .

1. Als optie kunt u het **[!UICONTROL Google Site Stats]** -bericht toevoegen aan de conversiepagina.

   De melding wordt in de onderhoek weergegeven met een koppeling naar beveiligingsstandaarden en cookiegebruik van Google.

1. Voer een van de volgende handelingen uit om te bepalen hoe u de tag AdWords wilt beheren:

   - Kies **[!UICONTROL Save instructions and tag]** als u het script zelf aan uw winkel wilt toevoegen.
   - Kies **[!UICONTROL Email instructions and tag]** als u wilt dat iemand anders het script aan uw winkel toevoegt.

1. Klik op **[!UICONTROL Done]** als de bewerking is voltooid.

## Stap 3. Uw winkel configureren

{{gtag-api-note}}

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Ga als volgt te werk als u Google AdWords voor een specifieke winkelweergave configureert:

   - Kies in de linkerbovenhoek de **[!UICONTROL Store View]** die moet worden geconfigureerd.

   - Klik op **[!UICONTROL OK]** wanneer u wordt gevraagd het schakelen tussen bereik en bereik te bevestigen.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Google API]** .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Google AdWords]** sectie uit en doe het volgende:

   - Stel **[!UICONTROL Enable]** in op `Yes` .

   - Voer de **[!UICONTROL Conversion ID]** in uit uw Google AdWords-script.

   ![ de configuratie van de Verkoop - de Advertentie API van Google ](../configuration-reference/sales/assets/google-api-google-adwords.png){width="600" zoomable="yes"}

1. Ga als volgt te werk om de melding van de Google-sitestaat op te maken:

   - Stel **[!UICONTROL Conversion Language]** in op de taal die wordt geïdentificeerd in het Google AdWords-script.

   - Voer de **[!UICONTROL Conversion Format]** in die u wilt gebruiken voor het bericht van de Google-sitestaat op de conversiepagina.

      - `1` - Geeft een bericht van één regel weer met een koppeling naar meer informatie over het bijhouden van Google.
      - `2` - Hiermee wordt een bericht weergegeven met twee regels en een koppeling naar meer informatie over het bijhouden van Google.
      - `3` - Geeft geen klantmelding weer.

   - Ga de [ hexadecimale code ][4] {:target= &quot;_blank&quot;} voor **[!UICONTROL Conversion Color]** in die u voor het het berichtetiket van de Staten van de Plaats van Google wilt gebruiken.

   - Voer de gecodeerde tekst in voor de **[!UICONTROL Conversion Label]** die wordt weergegeven in het bericht voor de Google-sitestatus.

     Bijvoorbeeld: `MlEYCOKBnGoQz6CZoAM`

     **Voorbeeld Google AdWords de Code van de Markering**

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

1. Stel **[!UICONTROL Conversion Value Type]** in op een van de volgende opties:

   - `Dynamic` - Hiermee wordt bepaald dat er een conversie heeft plaatsgevonden op basis van de dynamische waarde voor Hoeveelheid volgorde.
   - `Constant` - Hiermee wordt bepaald dat er een conversie heeft plaatsgevonden op basis van een specifieke ingevoerde waarde.

   Voor het type van a _Constante_ omzetwaarde, ga specifiek **[!UICONTROL Value]** voor _[!UICONTROL Order Amount]_in om als omzetting te kwalificeren.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

## Stap 4. De configuratie controleren

Binnen een paar uur verandert de trackingstatus in het Google AdWords-dashboard van `Unverified` in `No recent conversions` of `Recording conversions` . Wanneer iemand op uw advertentie klikt en een aankoop doet, wordt de conversie weergegeven op de pagina Conversiehandelingen van het dashboard en het campagnerapport.

[1]: https://www.google.com/adwords/
[2]: https://support.google.com/adwords/answer/6095821
[3]: https://ads.google.com/
[4]: https://www.w3schools.com/colors/colors_picker.asp
