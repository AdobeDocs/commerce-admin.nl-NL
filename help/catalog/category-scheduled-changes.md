---
title: Geplande wijzigingen voor categorieën
description: Leer hoe u wijzigingen in rubrieken kunt plannen om marketingcampagnes en winkelaanbiedingen te ondersteunen.
exl-id: 9e25082f-4e76-4148-b76e-dca0b14971eb
feature: Catalog Management, Categories
source-git-commit: 74cc26e74c3efabc914c27b6d8327a85a77fd6e6
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 0%

---

# Geplande wijzigingen voor categorieën

{{ee-feature}}

Categorieupdates kunnen volgens schema worden toegepast en worden gegroepeerd met andere inhoudswijzigingen. U kunt een campagne maken op basis van geplande wijzigingen in de categorie of de wijzigingen toepassen op een bestaande campagne. Meer leren, zie [ Inhoud het Opvoeren ](../content-design/content-staging.md).

>[!NOTE]
>
>Het [!UICONTROL Schedule Design Update] lusje is verwijderd in ![ Adobe Commerce ](../assets/adobe-logo.svg) Adobe Commerce en kan niet direct op de categorie worden gewijzigd. U moet een geplande update maken voor deze activeringen.

>[!NOTE]
>
>Alle geplande updates worden opeenvolgend toegepast, wat betekent dat elke entiteit slechts één geplande update tegelijk kan hebben. Elke geplande update wordt toegepast op alle winkelweergaven binnen de opgegeven tijdsperiode. Dientengevolge, kan een entiteit veelvoudige geplande updates voor verschillende opslagmeningen niet tezelfdertijd hebben. Alle waarden van entiteitattributen binnen alle opslagmeningen, die niet door de huidige geplande update worden beïnvloed, worden genomen van de standaardwaarden, en niet van de vorige geplande update.

## Een update voor een categorie plannen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Kies in de categoriestructuur aan de linkerkant de categorie die u wilt wijzigen.

1. In _Geplande Veranderingen_ doos bij de bovenkant van de pagina, klik **[!UICONTROL Schedule New Update]**.

   ![ Geplande Veranderingen ](./assets/category-scheduled-changes.png){width="600" zoomable="yes"}

1. Selecteer de optie **[!UICONTROL Save as a New Update]** en stel de basisparameters voor de update in:

   - Voer bij **[!UICONTROL Update Name]** een naam in voor de nieuwe campagne voor het opslaan van inhoud.

   - Voer een korte **[!UICONTROL Description]** in van de update en hoe deze moet worden gebruikt.

   - Gebruik het hulpmiddel van de Kalender ( ![ het pictogram van de Kalender ](../assets/icon-calendar.png)) om **[!UICONTROL Start Date]** en **[!UICONTROL End Date]** voor de campagne te kiezen.

   >[!IMPORTANT]
   >
   >De campagne **[!UICONTROL Start Date]** en **[!UICONTROL End Date]** moeten worden bepaald door de **_standaard_** tijdzone Admin te gebruiken, die van de lokale tijdzone van elke website wordt omgezet. Als u bijvoorbeeld meerdere websites in verschillende tijdzones hebt waarin u een campagne wilt starten op basis van een Amerikaanse tijdzone, moet u een afzonderlijke update voor elke lokale tijdzone plannen. U stelt de tijdzone **[!UICONTROL Start Date]** en **[!UICONTROL End Date]** voor elk in. Deze worden van de tijdzone van de lokale website omgezet in de standaardtijdzone van Admin.

   ![ Geplande Veranderingen ](./assets/category-scheduled-changes-new-update.png){width="600" zoomable="yes"}

1. Breng de benodigde wijzigingen aan in de geplande update.

1. Klik op **[!UICONTROL Preview]** in de knopbalk rechtsboven om een voorvertoning van de wijzigingen weer te geven.

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

## Toewijzen aan een bestaande update

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Kies in de categoriestructuur aan de linkerkant de categorie die u wilt wijzigen.

1. In _Geplande Veranderingen_ doos bij de bovenkant van de pagina, klik **[!UICONTROL Schedule New Update]**.

1. Selecteer **[!UICONTROL Assign to Existing Campaign]** .

1. Zoek in de lijst de gewenste campagne en klik op **[!UICONTROL Select]** .

1. Breng de benodigde wijzigingen aan in de geplande update.

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

   >[!NOTE]
   >
   >Als een campagne met meer dan één categorie wordt verbonden, kan de campagne slechts van het [ Inhoud Staging Dashboard ](../content-design/content-staging-dashboard.md) worden uitgegeven.