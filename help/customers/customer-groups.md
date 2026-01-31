---
title: Klantengroepen
description: Gebruik klantengroepen om te bepalen welke kortingen aan klanten beschikbaar zijn die aan een groep en de belastingklasse worden toegewezen die met de groep wordt geassocieerd.
exl-id: 6b785c4a-a5dc-480c-8182-2a940784218d
feature: Customers, Configuration
source-git-commit: 17469d27128030b54fad6cf563a4b53f5f119eed
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---

# Klantengroepen

Klantgroepen bepalen welke kortingen beschikbaar zijn en welke belastingklasse aan de groep is gekoppeld. De standaardklantengroepen zijn `General`, `Not Logged In`, en `Wholesale`.

![ de Groepen van de Klant ](assets/customer-groups.png){width="700" zoomable="yes"}

## De lijst [!UICONTROL Customer Groups] filteren

1. Voor _Admin_ sidebar, ga **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Klik op **[!UICONTROL Filters]**.

1. Voer criteria in voor het doorzoeken van groepen, waaronder een bereik met id&#39;s, groepen of belastingklassen.

   ![ het Filtreren Opties ](assets/groups-filters.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Apply Filters]** als de bewerking is voltooid.

## Een klantengroep maken

>[!NOTE]
>
>Admin-gebruikers die geen toegang hebben tot alle websites (waaraan een rol is toegewezen met een &#39;Aangepast&#39; [!UICONTROL Role Scope] ) kunnen geen klantengroepen maken, wijzigen of verwijderen.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Klik op **[!UICONTROL Add New Customer Group]**.

1. Voer bij [!DNL **Group Name]** een unieke naam in van minder dan 32 tekens om de groep te identificeren.

1. Selecteer de **[!UICONTROL Tax Class]** die op de groep van toepassing is.

   ![ de Informatie van de Groep ](assets/group-information.png){width="600" zoomable="yes"}

1. Selecteer de **[!UICONTROL Excluded Website(s)]** die u van de groep wilt uitsluiten.

   >[!IMPORTANT]
   >
   >Door websites uit te sluiten, kan de prijs van het product en de tijd voor het indexeren van catalogi afnemen, omdat uitgesloten websites niet worden geïndexeerd. Wanneer een klantengroep met een toegevoegde websiteuitsluiting wordt opgeslagen, worden de de productprijs, catalogusregel, en indexen van het catalogusonderzoek ongeldig gemaakt. Als u veel producten, websites en klantengroepen hebt, is het raadzaam het herindexeringsproces te pauzeren totdat u websites van de klantengroepen hebt uitgesloten.

   Er zijn standaard geen websites uitgesloten. Om veelvoudige waarden te selecteren, onderdruk de _sleutel van CTRL_ (PC) of de _3} sleutel van het Bevel {(Mac) en klik elke optie._

1. Klik op **[!UICONTROL Save Customer Group]** als de bewerking is voltooid.

## Een klantengroep bewerken

1. Voor _Admin_ sidebar, ga **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Open de record in de bewerkingsmodus.

1. Breng de gewenste wijzigingen aan.

1. Klik op **[!UICONTROL Save Customer Group]** als de bewerking is voltooid.

## Een klant toewijzen aan een andere groep

>[!NOTE]
>
>Nadat het veranderen van de bedrijvengroep, moet een bedrijfgebruiker zich afmelden en op Storefront aanmelden om nieuwe prijzen in de catalogus te zien.
>Nadat een klant aan een bedrijf wordt toegewezen, wordt de Groep van de Klant read-only en kan niet door een gebruiker worden bijgewerkt Admin.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Zoek de klant in de lijst en selecteer het selectievakje in de eerste kolom.

1. Plaats de **controle van Acties** aan `Assign a Customer Group` en kies de groep van het menu.

   ![ wijs een Groep van de Klant toe ](assets/group-assign.png){width="600" zoomable="yes"}

1. Wanneer ertoe aangezet om te bevestigen, klik **OK**.

## Een groep klanten koppelen aan specifieke kortingen

1. Op _Admin_ sidebar, ga **[!UICONTROL Marketing]** > _Bevorderingen_ > **[!UICONTROL Cart Price Rules]**.

1. Selecteer de regel van de wortelprijs waar u een groep voor de toegepaste korting wilt associëren, of [ creeer een prijsregel ](../merchandising-promotions/price-rules-catalog.md).

1. Selecteer de klantengroepen waarop de regel van toepassing is.

   ![ Groep van de Klant aan Specifieke Kortingen ](assets/group-discount.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save]**.

>[!NOTE]
>
> U kunt de Geavanceerde prijzen ook gebruiken om productkortingen op klantengroepen toe te passen. Zie [ Geavanceerde tarifering ](../catalog/product-price-group.md).

## Een klantengroep verwijderen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Open de record in de bewerkingsmodus.

1. Klik in de knopbalk op **[!UICONTROL Delete Customer Group]** .

1. Wanneer ertoe aangezet om te bevestigen, klik **OK**.

## Demo voor klantgroepen

Bekijk deze demo om te leren hoe u klantgroepen kunt maken:

>[!VIDEO](https://video.tv.adobe.com/v/343660/?quality=12&learn=on)
