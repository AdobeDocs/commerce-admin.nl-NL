---
title: '[!DNL Google Content Experiments]'
description: Leren gebruiken [!DNL Google Content Experiments] om een A/B-test van de producten, categorieën of inhoudspagina's van de Handel op te zetten.
exl-id: ae03bc5a-de84-4dad-932e-e79e509feebe
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 0%

---

# [!DNL Google Content Experiments]

In het volgende voorbeeld ziet u hoe u een A/B-test van producten, categorieën of inhoudspagina&#39;s instelt met behulp van Googles Analytics Content Experiments. We raden u aan twee browsertabbladen open te houden terwijl u de instructies doorloopt, omdat u heen en weer moet springen tussen Commerce Admin en uw [!DNL Google Analytics] account.

>[!NOTE]
>
>[!DNL Google Content Experiments] is vervangen en is gepland voor vervanging door [Google optimaliseren](https://support.google.com/optimize/answer/7084762?hl=en).

## Stap 1. Inhoud-experimenten inschakelen (handel)

1. Meld u aan bij de beheerder van de installatie van Commerce.

1. Volg de instructies om in te schakelen [Googles Analytics](google-analytics.md) met Content Experiments in de configuratie Commerce.

   ![Verkoopconfiguratie - Google API - Googles Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

## Stap 2. Variaties instellen (Handel)

Maak meerdere variaties van hetzelfde product, dezelfde categorie of dezelfde pagina.

- Elke variatie moet een unieke [URL-sleutel](../catalog/catalog-urls.md).
- Elke variatie moet dezelfde zijn [winkelweergave](../getting-started/websites-stores-views.md#scope-settings) geselecteerd.

U kunt maximaal tien variaties maken van elke entiteit die u wilt testen. Voor producten, gebruik [Opslaan en dupliceren](../catalog/product-workspace.md) tijd besparen.

## Stap 3. Het experiment instellen (Google)

>[!NOTE]
>
>U moet over de juiste machtigingen voor de Google-account beschikken om een experiment te kunnen maken.

1. Open een ander browsertabblad en meld u aan bij [Googles Analytics][2] account.

   Ga zo nodig naar de **[!UICONTROL Account]** en **[!UICONTROL Property]**.

1. Kies in het zijpaneel links de optie **[!UICONTROL Admin]** en gebruik een van de volgende methoden:

   **Methode 1:** Een bestaande weergave kiezen

   In de koptekst van het dialoogvenster _[!UICONTROL View]_klikt u op de pijl-omlaag en kiest u de weergave die de gegevens voor het experiment moet leveren.

   **Methode 2:** Een nieuwe rapportweergave maken

   - In de koptekst van het dialoogvenster _Weergave_ kolom, klik **[!UICONTROL Create View]** en voer de volgende handelingen uit:

      - De locatie van het experiment aangeven als: `Website` of `Mobile app`.

      - Voer een beschrijving in **[!UICONTROL Reporting View Name]**.

      - Geef de **[!UICONTROL Reporting Time Zone]**.

   - Klik op **[!UICONTROL Create View]** en klik vervolgens op de pijl Vorige om terug te keren naar de vorige pagina.

1. In het linkerdeelvenster onder _[!UICONTROL Reports]_, kiest u **[!UICONTROL Behavior]**>**[!UICONTROL Experiments]**.

1. Klikken **[!UICONTROL Create experiment]** en voer de volgende handelingen uit:

   - Geef het percentage van het verkeer op dat moet worden omgeleid.

   - Geef de **[!UICONTROL Original Page URL]** en de URL&#39;s van elk **[!UICONTROL page variation]** die u wilt testen.

   - Vul de overige opties in.

1. Wanneer het experiment is ingesteld, klikt u op **[!UICONTROL Manually Insert the Code]** en kopieer het codefragment.

## Stap 4. Codefragment plakken (Handel)

1. Ga terug naar de beheerder van uw installatie van de Handel en open de originele versie van het product, de categorie, of de pagina in uitgeven wijze.

1. Breid uit **[!UICONTROL View Optimization]** voor het product, de categorie of de pagina.

1. Plak het codefragment dat u van Googles Analytics hebt gekopieerd naar het deelvenster **[!UICONTROL Experiment Code]** tekstvak.

   >[!NOTE]
   >
   >Plak het codefragment niet in een van de variaties.

   ![Optimalisatie van de productweergave](../catalog/assets/product-view-optimization.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save]**.

## Stap 5: Het experiment evalueren en starten (Google)

1. Ga terug naar uw [Googles Analytics][2] account.

1. Controleer de instellingen voor het experiment.

1. Als u gereed bent, klikt u op **[!UICONTROL Start Experiment]**.

   Anders klikt u op **[!UICONTROL Save for Later]**.


[2]: https://analytics.google.com/
