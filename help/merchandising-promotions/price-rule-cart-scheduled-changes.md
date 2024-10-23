---
title: Geplande wijzigingen voor de regels betreffende de kartprijs
description: Leer hoe u regels voor winkelwagenprijzen op schema toepast als onderdeel van een campagne en gegroepeerd met andere wijzigingen in de inhoud.
exl-id: 4c9caa04-1e11-440d-b3db-7cc5fc83a08f
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: 0ceb61e6f1629a3bef16c550362c1db25b4aefa5
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 0%

---

# Geplande wijzigingen voor de regels betreffende de kartprijs

{{ee-feature}}

De prijsregels voor winkelwagentjes kunnen volgens schema worden toegepast als onderdeel van een campagne en worden gegroepeerd met andere wijzigingen in de inhoud. U kunt een campagne maken op basis van geplande wijzigingen in een prijsregel, of de wijzigingen toepassen op een bestaande campagne.

>[!NOTE]
>
>De [!UICONTROL From] en [!UICONTROL To] gebieden zijn verwijderd in ![ Adobe Commerce ](../assets/adobe-logo.svg) Adobe Commerce en kunnen niet direct op de regel van de kartprijs worden gewijzigd. U moet een geplande update maken voor deze activeringen.

![ de prijsregels van de Kar - geplande veranderingen ](./assets/content-staging-price-rules-cart-scheduled-changes.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Alle geplande updates worden achtereenvolgens toegepast. Dit betekent dat elke entiteit slechts één geplande update op één tijdstip kan hebben. Elke geplande update wordt toegepast op alle winkelweergaven binnen de opgegeven tijdsperiode. Dientengevolge, kan een entiteit verschillende geplande updates voor verschillende opslagmeningen niet tezelfdertijd hebben. Alle waarden van entiteitattributen binnen alle opslagmeningen, die niet door de huidige geplande update worden beïnvloed, worden genomen van de standaardwaarden, en niet van de vorige geplande update.

Als er in dezelfde campagne meerdere prijsregels worden uitgevoerd, bepaalt de _[!UICONTROL Priority]_-instelling van de prijsregel welke regel voorrang krijgt. Meer leren, zie [ Inhoud het Opvoeren ](../content-design/content-staging.md).

>[!NOTE]
>
>Als een actieve campagne in eerste instantie zonder einddatum wordt gemaakt, kan de campagne later niet worden bewerkt om een einddatum op te nemen. In dat geval moet een dubbele campagne worden gemaakt en moet de gewenste einddatum worden ingevoerd.

>[!NOTE]
>
>Als een campagne met meer dan één regel van de kartprijs verbonden is, kan de campagne slechts van het [ Inhoud Staging Dashboard ](../content-design/content-staging-dashboard.md) worden uitgegeven.

Houd rekening met het volgende:

- Als een campagne met een prijsregel in eerste instantie zonder einddatum wordt gemaakt, kan de campagne later niet worden bewerkt met een einddatum. U wordt aangeraden een einddatum toe te voegen wanneer u de campagne maakt of een dubbele versie van de bestaande campagne te maken en de einddatum desgewenst aan het duplicaat toe te voegen.
- Wanneer u een geplande update gebruikt om een regel voor de winkelwagenprijs met een einddatum in te schakelen, moet u de regel instellen als aanvankelijk uitgeschakeld. Regels die al actief zijn, respecteren de einddatum niet.
- Coupons houden geen verband met de regels voor de kartprijs. Een geplande update biedt geen toegang tot de velden _[!UICONTROL Coupon]_,_[!UICONTROL Coupon Code]_ , _[!UICONTROL Uses per Coupon]_en_[!UICONTROL Uses per Customer]_ op het tabblad _[!UICONTROL Rule Information]_. Bovendien zijn niet alle instellingen op het tabblad_[!UICONTROL Manage Coupon Codes]_ beschikbaar.

>[!IMPORTANT]
>
>De campagne **[!UICONTROL Start Date]** en **[!UICONTROL End Date]** moeten worden bepaald door de **_standaard_** tijdzone Admin te gebruiken, die van de lokale tijdzone van elke website wordt omgezet. Neem bijvoorbeeld een voorbeeld waarin u meerdere websites in verschillende tijdzones hebt, maar u wilt een campagne starten op basis van een Amerikaanse tijdzone. In dit geval moet u een afzonderlijke update voor elke lokale tijdzone plannen en **[!UICONTROL Start Date]** en **[!UICONTROL End Date]** voor elke lokale tijdzone van de website omzetten in de standaardtijdzone van de beheerder.
