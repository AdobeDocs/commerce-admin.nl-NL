---
title: '[!DNL Google Content Experiments]'
description: Leer hoe te om  [!DNL Google Content Experiments]  aan opstelling te gebruiken A/B test van de producten, de categorieën van Commerce, of inhoudspagina's.
exl-id: ae03bc5a-de84-4dad-932e-e79e509feebe
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 0%

---

# [!DNL Google Content Experiments]

In het volgende voorbeeld ziet u hoe u een A/B-test van producten, categorieën of inhoudspagina&#39;s instelt met behulp van Googles Analytics Content Experiments. We raden u aan twee browsertabbladen open te houden terwijl u de instructies doorloopt, omdat u heen en weer moet springen tussen Commerce Admin en uw [!DNL Google Analytics] -account.

>[!NOTE]
>
>[!DNL Google Content Experiments] is afgekeurd en voor vervanging gepland door [ Google optimaliseert ](https://support.google.com/optimize/answer/7084762?hl=en).

## Stap 1. Inhoud-experimenten inschakelen (Commerce)

1. Meld u aan bij de beheerder van uw Commerce-installatie.

1. Volg de instructies om [ Googles Analytics ](google-analytics.md) met de Experimenten van de Inhoud in de configuratie van Commerce toe te laten.

   ![ de configuratie van de Verkoop - Google API - Googles Analytics ](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

## Stap 2. Variaties instellen (Commerce)

Maak meerdere variaties van hetzelfde product, dezelfde categorie of dezelfde pagina.

- Elke variatie moet een unieke [ sleutel URL ](../catalog/catalog-urls.md) hebben.
- Elke variatie moet de zelfde [ geselecteerde opslagmening ](../getting-started/websites-stores-views.md#scope-settings) hebben.

U kunt maximaal tien variaties maken van elke entiteit die u wilt testen. Voor producten, gebruik [ sparen &amp; Dupliceer ](../catalog/product-workspace.md) om tijd te besparen.

## Stap 3. Het experiment instellen (Google)

>[!NOTE]
>
>U moet over de juiste machtigingen voor de Google-account beschikken om een experiment te kunnen maken.

1. Open een ander browser lusje, en logboek in uw [ Googles Analytics ][2] rekening.

   Navigeer zo nodig naar de **[!UICONTROL Account]** en **[!UICONTROL Property]** .

1. Kies in het zijpaneel links de optie **[!UICONTROL Admin]** en gebruik een van de volgende methoden:

   **Methode 1:** kies een Bestaande Mening

   Klik in de koptekst van de kolom _[!UICONTROL View]_op de pijl-omlaag en kies de weergave die de gegevens voor het experiment moet leveren.

   **Methode 2:** creeer een Nieuwe Rapporterende Mening

   - In de kopbal van de _kolom van de Mening_, klik **[!UICONTROL Create View]** en doe het volgende:

      - Identificeer de locatie van het experiment als `Website` of `Mobile app`.

      - Voer een beschrijving in **[!UICONTROL Reporting View Name]** .

      - Geef de waarde **[!UICONTROL Reporting Time Zone]** op.

   - Klik, wanneer deze bewerking is voltooid, op **[!UICONTROL Create View]** en vervolgens op de pijl Vorige om terug te keren naar de vorige pagina.

1. Kies in het linkerdeelvenster onder _[!UICONTROL Reports]_de optie **[!UICONTROL Behavior]**>**[!UICONTROL Experiments]**.

1. Klik op **[!UICONTROL Create experiment]** en voer de volgende handelingen uit:

   - Geef het percentage van het verkeer op dat moet worden omgeleid.

   - Geef de **[!UICONTROL Original Page URL]** en de URL&#39;s op van elke **[!UICONTROL page variation]** die u wilt testen.

   - Vul de overige opties in.

1. Wanneer het experiment is ingesteld, klikt u op **[!UICONTROL Manually Insert the Code]** en kopieert u het codefragment.

## Stap 4. Codefragment plakken (Commerce)

1. Ga terug naar de beheerder van uw Commerce-installatie en open de originele versie van het product, de categorie of de pagina in de bewerkingsmodus.

1. Vouw de sectie **[!UICONTROL View Optimization]** voor het product, de categorie of de pagina uit.

1. Plak het codefragment dat u van Googles Analytics hebt gekopieerd in het tekstvak **[!UICONTROL Experiment Code]** .

   >[!NOTE]
   >
   >Plak het codefragment niet in een van de variaties.

   ![ de meningsoptimalisering van het Product ](../catalog/assets/product-view-optimization.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

## Stap 5: Het experiment evalueren en starten (Google)

1. Keer aan uw [ Googles Analytics ][2] rekening terug.

1. Controleer de instellingen voor het experiment.

1. Klik op **[!UICONTROL Start Experiment]** als u klaar bent om te beginnen.

   Klik anders op **[!UICONTROL Save for Later]** .


[2]: https://analytics.google.com/
