---
title: Fragmenten
description: Hergebruikte notities en visuele elementen om een functie of pagina te noteren die van toepassing is op een specifieke editie
source-git-commit: 1f84bf9ab20aeccacf56eab396b2778140964d17
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 0%

---

# Fragmenten

## Alleen EE-functie {#ee-feature}

<table style="border:1px solid red">
<tr><td><img alt="Adobe Commerce-functie" src="../assets/adobe-logo.svg" width="20" height="20" /> Alleen exclusieve functie in Adobe Commerce (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">Meer informatie</a>)</td></tr>
</table>

## Alleen B2B-functie {#b2b-feature}

<table style="border:1px solid green">
<tr><td><img alt="B2B voor Adobe Commerce-functie" src="../assets/b2b.svg" width="20" height="20" /> Exclusieve functie alleen beschikbaar met <a href="https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=en">B2B voor Adobe Commerce</a></td></tr>
</table>

## Alleen CE-functie {#ce-feature}

<table style="border:1px solid orange">
<tr><td><img alt="Magento Open Source, functie" src="../assets/open-source.svg" width="20" height="20" /> Alternatieve methode is vereist voor Magento Open Source (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">Meer informatie</a>)</td></tr>
</table>

## Bèta 1-updates {#beta-updates}

>[!NOTE]
>
>[!BADGE 2.4.7-bèta1]{type=Informative url="https://experienceleague.adobe.com/docs/commerce-operations/release/notes/adobe-commerce/2-4-7.html" tooltip="Alleen beschikbaar in 2.4.7 bèta1"}[releaseopmerkingen](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/adobe-commerce/2-4-7.html) voor gedetailleerde informatie over de wijzigingen.

## Bèta 2-updates {#beta2-updates}

>[!NOTE]
>
[!BADGE 2.4.7-bèta2]{type=Informative url="https://experienceleague.adobe.com/docs/commerce-operations/release/notes/adobe-commerce/2-4-7.html" tooltip="Alleen beschikbaar in 2.4.7 bèta2"}[releaseopmerkingen](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/adobe-commerce/2-4-7.html) voor gedetailleerde informatie over de wijzigingen.

## Bèta 2- en patchupdates {#beta2-patches-updates}

>[!NOTE]
>
[!BADGE 2.4.6-p3]{type=Informative tooltip="Updates in 2.4.6-p3"}[!BADGE 2.4.7-bèta2]{type=Informative tooltip="Updates in 2.4.7-bèta2"}[2.4.7-bèta2](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/adobe-commerce/2-4-7.html) en [2.4.6-p3](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p3.html) versies die verbeteringen bieden voor de beschreven functionaliteit. Controleer de releaseopmerkingen als u een van deze releaseversies gebruikt.

## IMS-beheerdersverificatienota {#ims-admin-note}

>[!NOTE]
>
Adobe Commerce-handelaren die een Adobe ID hebben en een gestroomlijnde aanmelding bij Adobe Commerce en Adobe Business-producten willen, kunnen verificatie met behulp van Commerce Admin integreren met de verificatieworkflow van Adobe IMS. Nadat deze integratie voor uw opslag van de Handel wordt toegelaten, moet elke gebruiker Admin hun geloofsbrieven van de Adobe — niet hun de rekeningsgeloofsbrieven van de Handel gebruiken om binnen te registreren. Zie [Overzicht van Adobe Commerce integreren met Adobe IMS](/help/getting-started/adobe-ims-integration-overview.md).

## Opmerking GTag-API&#39;s {#gtag-api-note}

>[!NOTE]
>
Vanaf de release 2.4.5 wordt de integratie met Google-services bijgewerkt om het gebruik van de GTag-API&#39;s te ondersteunen. GTag is een verenigd mechanisme voor integratie met de functionaliteit van Google voor webpagina&#39;s en ondersteunt de nieuwste mogelijkheden en mogelijkheden voor het bijhouden en beheren van inhoud via Google Services. Zie de klasse [Documentatie voor ontwikkelaars van Googles Analytics](https://developers.google.com/analytics/devguides/collection/gtagjs).

## URL herschrijven automatische overgeslagen nota {#url-rewrite-skip}

>[!NOTE]
>
Wanneer automatische omleidingen zijn ingeschakeld en u een categorie opslaat, worden alle product- en categorierefversies in real-time gegenereerd en standaard opgeslagen in herschrijftabellen. Dit proces kan leiden tot aanzienlijke prestatieproblemen voor categorieën met veel toegewezen producten. De oplossing is deze standaard te wijzigen en het genereren van categorie/producten-URL&#39;s van producten voor het opslaan van categorieën over te slaan. In dit geval worden herschrijfbewerkingen van het product alleen gegenereerd voor de URL van het canonieke product. Zie [Automatische productomleiding](/help/merchandising-promotions/url-redirect-product-automatic.md) voor meer informatie .

## Notitie voor parameters voor URL herschrijven {#url-rewrite-params}

>[!IMPORTANT]
>
Tijdens het omleidingsproces worden alle in de URL opgegeven GET-parameters uit veiligheidsoverwegingen verwijderd.

## Nieuwe prijsregel {#new-price-rule}

>[!NOTE]
>
Prijsregels worden automatisch verwerkt met andere systeemregels. De verwerkingsfrequentie is afhankelijk van de [uitsnijdconfiguratie](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html). Wanneer u een prijsregel maakt, moet u voldoende tijd toestaan om deze in het systeem te krijgen. Als u zeker bent dat het in het systeem is, test de regel.

## Configuratie-instellingen {#config}

Om tot de montages van de archiefconfiguratie toegang te hebben, verkies **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**van de_ Beheerder _zijbalk.

## Veroudering van UPS API {#ups-api}

>[!IMPORTANT]
>
Vanaf juni 2024 kunnen Adobe Commerce-handelaren niet langer communiceren met de huidige UPS-integratie. De reden hiervoor is dat de API&#39;s van United Parcel Service (UPS) die door de native Adobe Commerce-integratie worden gebruikt, momenteel niet het vereiste OAuth 2.0-beveiligingsmodel ondersteunen. Voor meer informatie over deze wijziging raadpleegt u [_Beheerdersportaal Toegang Key-migratiehandleiding_](https://developer.ups.com/oauth-developer-guide). <br/>
>
Handelaren moeten [patch-update voor kwaliteit toepassen](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/ups-shipping-method-integration-migration-from-soap-to-restful-api.html) aan hun opslag om van de API van de ZEEP aan RESTful te migreren API, die OAuth 2.0 authentificatieprotocollen steunt.


## Beschikbare documentatie {#docs-links}

| Documentatiebron | Beschrijving |
|----------------------- | ----------- |
| [Adobe Commerce 2.4 Handelsdocumentatie](../landing/home.md) | Bedrijfsgerichte documentatie voor zowel Adobe Commerce als Magento Open Source |
| [Services voor Adobe Commerce-documentatie](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html) | Documentatie om een inzameling van de diensten te steunen die handelaren helpen zeer belangrijke componenten van hun zaken met hun opslag integreren. |
| [Handleiding Commerce on Cloud Infrastructure](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/overview.html) | Stapsgewijze procedures voor de implementatie van Adobe Commerce op een beheerd, geautomatiseerd hostingplatform voor de cloud. |
| [Adobe Commerce 2.4-handleidingen](https://experienceleague.adobe.com/docs/commerce-operations/operational-guides/home.html) | De documentatie van systemen over de concepten, de processen, de hulpmiddelen, en beste praktijken om, projecten te ontwikkelen op Adobe Commerce en de platforms van de Magento Open Source op te stellen en te handhaven. |
| [Adobe Commerce 2.4-documentatie voor ontwikkelaars](https://developer.adobe.com/commerce/docs) | Documentatie gericht op ontwikkelaars die wordt gebruikt om Adobe Commerce of Magento Open Source te bouwen en aan te passen |

{style="table-layout:auto"}
