---
title: Geplande wijzigingen voor de regels betreffende de kartprijs
description: Leer hoe u regels voor winkelwagenprijzen op schema toepast als onderdeel van een campagne en gegroepeerd met andere wijzigingen in de inhoud.
exl-id: 4c9caa04-1e11-440d-b3db-7cc5fc83a08f
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# Geplande wijzigingen voor de regels betreffende de kartprijs

{{ee-feature}}

De prijsregels voor winkelwagentjes kunnen volgens schema worden toegepast als onderdeel van een campagne en worden gegroepeerd met andere wijzigingen in de inhoud. U kunt een campagne maken op basis van geplande wijzigingen in een prijsregel, of de wijzigingen toepassen op een bestaande campagne.

![Prijsregels voor winkelwagentjes - geplande wijzigingen](./assets/content-staging-price-rules-cart-scheduled-changes.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Alle geplande updates worden achtereenvolgens toegepast. Dit betekent dat elke entiteit slechts één geplande update op één tijdstip kan hebben. Elke geplande update wordt toegepast op alle winkelweergaven binnen de opgegeven tijdsperiode. Dientengevolge, kan een entiteit verschillende geplande updates voor verschillende opslagmeningen niet tezelfdertijd hebben. Alle waarden van entiteitattributen binnen alle opslagmeningen, die niet door de huidige geplande update worden beïnvloed, worden genomen van de standaardwaarden, en niet van de vorige geplande update.

Als er in dezelfde campagne meerdere prijsregels worden uitgevoerd, _[!UICONTROL Priority]_het bepalen van de prijsregel bepaalt welke regel voorrang krijgt . Zie voor meer informatie [Inhoud stapelen](../content-design/content-staging.md).

Houd rekening met het volgende:

- Als een campagne met een prijsregel in eerste instantie zonder einddatum wordt gemaakt, kan de campagne later niet worden bewerkt met een einddatum. U wordt aangeraden een einddatum toe te voegen wanneer u de campagne maakt of een dubbele versie van de bestaande campagne te maken en de einddatum desgewenst aan het duplicaat toe te voegen.
- Wanneer u een geplande update gebruikt om een regel voor de winkelwagenprijs met een einddatum in te schakelen, moet u de regel instellen als aanvankelijk uitgeschakeld. Regels die al actief zijn, respecteren de einddatum niet.
- Coupons houden geen verband met de regels voor de kartprijs. Een geplande update biedt geen toegang tot de _[!UICONTROL Coupon]_,_[!UICONTROL Coupon Code]_, _[!UICONTROL Uses per Coupon]_, en_[!UICONTROL Uses per Customer]_ velden op de _[!UICONTROL Rule Information]_tab. Alle instellingen van het dialoogvenster_[!UICONTROL Manage Coupon Codes]_ zijn niet beschikbaar.

>[!IMPORTANT]
>
>Campagne **[!UICONTROL Start Date]** en **[!UICONTROL End Date]** moet worden gedefinieerd met behulp van de **_default_** Tijdzone voor beheer, die wordt omgezet vanuit de lokale tijdzone van elke website. Neem bijvoorbeeld een voorbeeld waarin u meerdere websites in verschillende tijdzones hebt, maar u wilt een campagne starten op basis van een Amerikaanse tijdzone. In dit geval moet u voor elke lokale tijdzone een afzonderlijke update plannen en instellen **[!UICONTROL Start Date]** en **[!UICONTROL End Date]** omgezet van elke lokale tijdzone van de websitetijd in standaardtijdzone Admin.
