---
title: Geplande wijzigingen voor categorieën
description: Leer hoe u wijzigingen in rubrieken kunt plannen om marketingcampagnes en winkelaanbiedingen te ondersteunen.
exl-id: 9e25082f-4e76-4148-b76e-dca0b14971eb
feature: Catalog Management, Categories
source-git-commit: 3d04e7213d90bb4c323acce69ac31c1dbcb7ca49
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 0%

---

# Geplande wijzigingen voor categorieën

{{ee-feature}}

Categorieupdates kunnen volgens schema worden toegepast en worden gegroepeerd met andere inhoudswijzigingen. U kunt een campagne maken op basis van geplande wijzigingen in de categorie of de wijzigingen toepassen op een bestaande campagne. Zie voor meer informatie [Inhoud stapelen](../content-design/content-staging.md).

>[!NOTE]
>
>De [!UICONTROL Schedule Design Update] tab is verwijderd in ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce en kan niet rechtstreeks in de categorie worden gewijzigd. U moet een geplande update maken voor deze activeringen.

>[!NOTE]
>
>Alle geplande updates worden opeenvolgend toegepast, wat betekent dat elke entiteit slechts één geplande update tegelijk kan hebben. Elke geplande update wordt toegepast op alle winkelweergaven binnen de opgegeven tijdsperiode. Dientengevolge, kan een entiteit veelvoudige geplande updates voor verschillende opslagmeningen niet tezelfdertijd hebben. Alle waarden van entiteitattributen binnen alle opslagmeningen, die niet door de huidige geplande update worden beïnvloed, worden genomen van de standaardwaarden, en niet van de vorige geplande update.

## Een update voor een categorie plannen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Kies in de categoriestructuur aan de linkerkant de categorie die u wilt wijzigen.

1. In de _Geplande wijzigingen_ klikt u boven aan de pagina op **[!UICONTROL Schedule New Update]**.

   ![Geplande wijzigingen](./assets/category-scheduled-changes.png){width="600" zoomable="yes"}

1. Met de **[!UICONTROL Save as a New Update]** geselecteerde optie, de basisparameters voor de update plaatsen:

   - Voor **[!UICONTROL Update Name]**, voert u een naam in voor de nieuwe campagne voor het opvoeren van inhoud.

   - Voer een korte beschrijving in **[!UICONTROL Description]** van de actualisering en de wijze waarop deze moet worden gebruikt.

   - De kalender gebruiken ( ![Kalenderpictogram](../assets/icon-calendar.png) ) te kiezen. **[!UICONTROL Start Date]** en **[!UICONTROL End Date]** voor de campagne.

   >[!IMPORTANT]
   >
   >Campagne **[!UICONTROL Start Date]** en **[!UICONTROL End Date]** moet worden gedefinieerd met behulp van de **_default_** Tijdzone voor beheerders, die wordt omgezet vanuit de lokale tijdzone van elke website. Als u bijvoorbeeld meerdere websites in verschillende tijdzones hebt waarin u een campagne wilt starten op basis van een Amerikaanse tijdzone, moet u een afzonderlijke update voor elke lokale tijdzone plannen. U stelt de **[!UICONTROL Start Date]** en **[!UICONTROL End Date]** voor elke component, die wordt omgezet van de lokale tijdzone van de websitetijd in de standaardtijdzone van Admin.

   ![Geplande wijzigingen](./assets/category-scheduled-changes-new-update.png){width="600" zoomable="yes"}

1. Breng de benodigde wijzigingen aan in de geplande update.

1. Klik op **[!UICONTROL Preview]** in de knopbalk rechtsboven.

1. Klik op **[!UICONTROL Save]**.

## Toewijzen aan een bestaande update

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Kies in de categoriestructuur aan de linkerkant de categorie die u wilt wijzigen.

1. In de _Geplande wijzigingen_ klikt u boven aan de pagina op **[!UICONTROL Schedule New Update]**.

1. Selecteren **[!UICONTROL Assign to Existing Campaign]**.

1. Zoek in de lijst de gewenste campagne en klik op **[!UICONTROL Select]**.

1. Breng de benodigde wijzigingen aan in de geplande update.

1. Klik op **[!UICONTROL Save]**.
