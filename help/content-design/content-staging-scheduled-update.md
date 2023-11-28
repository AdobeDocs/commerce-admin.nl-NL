---
title: Een inhoudsupdate plannen
description: Bekijk dit campagnevoorbeeld dat wordt gebruikt om een tijdelijke prijswijziging voor een product te plannen.
exl-id: 36b7d7f6-4590-4192-a82b-e5f645b05f62
feature: Page Content, Staging
source-git-commit: b3897ba034770229ef8f3117231bed286abdddb9
workflow-type: tm+mt
source-wordcount: '636'
ht-degree: 0%

---

# Een inhoudsupdate plannen

{{ee-feature}}

In het volgende voorbeeld ziet u hoe u een tijdelijke prijswijziging voor een product kunt plannen. Dit omvat het plannen en voorvertonen van wijzigingen en het weergeven van geplande updates in de kalender. Hoewel dit voorbeeld slechts één wijziging omvat, kan een campagne meerdere veranderingen in producten, prijsregels, CMS-pagina&#39;s, en andere entiteiten omvatten die tezelfdertijd moeten plaatsvinden. Voer een vergelijkbare methode uit om de datum van/tot en met de datum van [!UICONTROL Set Product As New] kenmerk.

>[!NOTE]
>U moet een geplande update maken om een begin- (en einddatum) op te geven voor [!UICONTROL Set Product As New]. Voor [!UICONTROL Special Price] en [!UICONTROL Design Change], worden de van/tot datumvelden verwijderd uit Adobe Commerce en zijn alleen beschikbaar in Magento Open Source.
>
>Alle geplande updates worden opeenvolgend toegepast, wat betekent dat elke entiteit slechts één geplande update tegelijk kan hebben. Elke geplande update wordt toegepast op alle winkelweergaven binnen de opgegeven tijdsperiode. Dientengevolge, kan een entiteit geen verschillende geplande update voor verschillende opslagmeningen tezelfdertijd hebben. Alle waarden van entiteitattributen binnen alle opslagmeningen, die niet door de huidige geplande update worden beïnvloed, worden genomen van de standaardwaarden, en niet van de vorige geplande update.

## Een update voor een product plannen

1. Van de _[!UICONTROL Products]_, opent u een product in de bewerkingsmodus.

1. In de _[!UICONTROL Scheduled Changes]_klikt u boven aan de pagina op **[!UICONTROL Schedule New Update]**.

   ![Nieuwe update plannen](./assets/content-staging-product-schedule-new-update.png){width="600" zoomable="yes"}

1. Met de **[!UICONTROL Save as a New Update]** Selecteer de optie, stel de basisparameters voor de update in:

   - Voor **[!UICONTROL Update Name]**, voert u een naam in voor de nieuwe campagne voor het opvoeren van inhoud.

   - Voer een korte beschrijving in **[!UICONTROL Description]** van de actualisering en de wijze waarop deze moet worden gebruikt.

   - De kalender gebruiken (![Kalenderpictogram](../assets/icon-calendar.png)) te kiezen. **Begindatum** en **Einddatum** voor de campagne.

     Geef geen einddatum op als u een campagne met een open einde wilt maken. Voor dit voorbeeld is de campagne gepland om vanaf middernacht te beginnen voor het nieuwe jaar, 1 januari 2021 om 12:00 uur PST.


     Voor een prijsregelcampagne die zonder einddatum is gemaakt, kan een einddatum niet later worden toegevoegd. In dat geval moet een campagne worden opgezet en moet de begindatum worden ingesteld op de datum waarop de oude campagne moet worden beëindigd en de nieuwe campagne moet worden gestart. Op die begindatum eindigt de oude campagne en begint de nieuwe campagne zoals gedefinieerd.

     ![Een productupdate plannen](./assets/content-staging-campaign-schedule-update.png){width="600" zoomable="yes"}

     >[!NOTE]
     >
     >De begindatum en einddatum van de campagne moeten worden gedefinieerd met de **_default_** Tijdzone voor beheerders, die wordt omgezet vanuit de lokale tijdzone van elke website. Wanneer u bijvoorbeeld meerdere websites in verschillende tijdzones hebt, maar u wilt een campagne starten op basis van een tijdzone in de VS (de standaardtijdzone), moet u een afzonderlijke update voor elke lokale tijdzone plannen. In dit geval stelt u **[!UICONTROL Start Date]** en **[!UICONTROL End Date]** zoals omgezet van elke lokale tijdzone van de websitetijd in de standaardtijdzone van Admin.

1. Omlaag schuiven naar _[!UICONTROL Price]_en klik op **[!UICONTROL Advanced Pricing]**.

1. Voer een **[!UICONTROL Special Price]** voor het product tijdens de geplande campagne en klik op **[!UICONTROL Done]**.

1. Klik op **[!UICONTROL Save]**.

   De geplande wijziging wordt boven aan de productpagina weergegeven met de begin- en einddatum van de campagne.

   ![Geplande wijziging](./assets/content-staging-product-scheduled-update-preview-rope.png){width="600" zoomable="yes"}

## De geplande wijziging bewerken

1. In de _Geplande wijzigingen_ klikt u boven aan de pagina op **[!UICONTROL View/Edit]**.

1. Breng de benodigde wijzigingen aan in de geplande update.

1. Klik op **[!UICONTROL Save]**.

## Voorbeeld van geplande wijziging bekijken

In de _Geplande wijzigingen_ klikt u boven aan de pagina op **[!UICONTROL Preview]**.

De voorvertoning opent een nieuw browsertabblad en toont hoe het product tijdens de geplande campagne wordt weergegeven.

>[!NOTE]
>
>Een voorvertoning van een geprogrammeerde update wordt altijd gestart vanaf het tabblad **default** de mening van de opslag, die de ervaring van de klant navigeert door de het opvoeren updatecampagne.

Voor meer informatie over het gebruik van de gereedschappen voor voorvertoningen van inhoud om de datum en het bereik van de voorvertoning te wijzigen, raadpleegt u [Een voorvertoning van een campagne weergeven](content-staging-preview.md). U kunt ook een koppeling naar de voorvertoning van de winkel delen met uw collega&#39;s.
