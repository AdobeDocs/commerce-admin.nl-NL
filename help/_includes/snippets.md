---
title: Fragmenten
description: Hergebruikte notities en visuele elementen om een functie of pagina te noteren die van toepassing is op een specifieke editie
source-git-commit: 0ffeaa42e0207322da1b55a9fd6b6b2cf24ff4ba
workflow-type: tm+mt
source-wordcount: '640'
ht-degree: 0%

---

# Fragmenten

## Alleen EE-functie {#ee-feature}

<table style="border:1px solid red">
<tr><td><img alt="Adobe Commerce-functie" src="../assets/adobe-logo.svg" width="20" height="20" /> De exclusieve eigenschap slechts in Adobe Commerce (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html?lang=nl-NL#product-editions"> leert meer </a>)</td></tr>
</table>

## Alleen B2B-functie {#b2b-feature}

<table style="border:1px solid green">
<tr><td><img alt="Adobe Commerce B2B-functie" src="../assets/b2b.svg" width="20" height="20" /> Exclusieve eigenschap beschikbaar slechts met <a href="https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=nl-NL"> Adobe Commerce B2B </a></td></tr>
</table>

## Alleen CE-functie {#ce-feature}

<table style="border:1px solid orange">
<tr><td><img alt="Magento Open Source-functie" src="../assets/open-source.svg" width="20" height="20" /> Alternatieve methode wordt vereist voor Magento Open Source (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html?lang=nl-NL#product-editions"> Leer meer </a>)</td></tr>
</table>

## IMS-beheerdersverificatienota {#ims-admin-note}

>[!NOTE]
>
>Adobe Commerce-handelaren die een Adobe ID hebben en een gestroomlijnde aanmelding bij Adobe Commerce en Adobe Business-producten willen, kunnen Commerce Admin-verificatie integreren met de Adobe IMS-verificatieworkflow. Nadat deze integratie is ingeschakeld voor uw Commerce-winkel, moet elke Admin-gebruiker zich aanmelden met zijn Adobe-gegevens, niet met de Commerce-accountgegevens. Zie [ Integrating Adobe Commerce met het overzicht van Adobe IMS ](/help/getting-started/adobe-ims-integration-overview.md).

## Opmerking GTag-API's {#gtag-api-note}

>[!NOTE]
>
>Vanaf de release 2.4.5 wordt de integratie met Google-services bijgewerkt om het gebruik van de GTag-API&#39;s te ondersteunen. GTag is een verenigd mechanisme voor integratie met de functionaliteit van Google voor webpagina&#39;s en ondersteunt de nieuwste mogelijkheden en mogelijkheden voor het bijhouden en beheren van inhoud via Google Services.

## URL herschrijven automatische overgeslagen nota {#url-rewrite-skip}

>[!NOTE]
>
>Wanneer automatische omleidingen zijn ingeschakeld en u een categorie opslaat, worden alle product- en categorierefversies in real-time gegenereerd en standaard opgeslagen in herschrijftabellen. Dit proces kan leiden tot aanzienlijke prestatieproblemen voor categorieën met veel toegewezen producten. De oplossing is deze standaard te wijzigen en het genereren van categorie/producten-URL&#39;s van producten voor het opslaan van categorieën over te slaan. In dit geval worden herschrijfbewerkingen van het product alleen gegenereerd voor de URL van het canonieke product. Zie [ Automatische productomleidingen ](/help/merchandising-promotions/url-redirect-product-automatic.md) voor meer informatie.

## Notitie voor parameters voor URL herschrijven {#url-rewrite-params}

>[!IMPORTANT]
>
>Tijdens het omleidingsproces worden alle GET-parameters die in de URL zijn opgegeven, uit veiligheidsoverwegingen verwijderd.

## Nieuwe prijsregel {#new-price-rule}

>[!NOTE]
>
>Prijsregels worden automatisch verwerkt met andere systeemregels. De verwerkingsfrequentie hangt van de [ kroonconfiguratie ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html?lang=nl-NL) af. Wanneer u een prijsregel maakt, moet u voldoende tijd toestaan om deze in het systeem te krijgen. Als u zeker bent dat het in het systeem is, test de regel.

## Configuratie-instellingen {#config}

Om tot de montages van de opslagconfiguratie toegang te hebben, verkies **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;van_ Admin _sidebar.

## Veroudering van UPS API {#ups-api}

>[!IMPORTANT]
>
>Vanaf juni 2024 kunnen Adobe Commerce-handelaren niet langer communiceren met de huidige UPS-integratie. De reden hiervoor is dat de API&#39;s van United Parcel Service (UPS) die door de native Adobe Commerce-integratie worden gebruikt, momenteel niet het vereiste OAuth 2.0-beveiligingsmodel ondersteunen. Om de integratie toe te laten, [ creeer een toepassing op het de ontwikkelaarsplatform van UPS ](https://developer.ups.com/get-started) om de geloofsbrieven te verkrijgen die voor OAuth 2.0 worden vereist. Gebruik de nieuwe referenties als de `username` en `password` in de configuratie voor verzending van Commerce UPS. Om meer over de verandering van het veiligheidsmodel te leren, zie [ Belangrijkste Gids van de Migratie van de Toegang van het Portaal van de Ontwikkelaar 1&rbrace;. <br/>](https://developer.ups.com/oauth-developer-guide)
>
>De handelaren zouden [ een update van het kwaliteitspatch ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/ups-shipping-method-integration-migration-from-soap-to-restful-api.html?lang=nl-NL) op hun opslag moeten toepassen om van SOAP API aan RESTful API te migreren, die OAuth 2.0 authentificatieprotocollen steunt.


## Beschikbare documentatie {#docs-links}

| Documentatiebron | Beschrijving |
|----------------------- | ----------- |
| [ Adobe Commerce 2.4 de Gidsen van de Gebruiker Admin ](../landing/home.md) | Documentatie en bronnen voor handelaren die in de Admin werken. |
| [ de Diensten voor de Documentatie van Adobe Commerce ](https://experienceleague.adobe.com/docs/commerce/user-guides/home.html?lang=nl-NL) | Documentatie om een inzameling van de koophandel te steunen de diensten die handelaars helpen zeer belangrijke componenten van hun zaken met hun opslag integreren. |
| [ Commerce op de Gids van de Infrastructuur van de Wolk ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/overview.html?lang=nl-NL) | Stapsgewijze procedures voor de implementatie van Adobe Commerce op een beheerd, geautomatiseerd hostingplatform voor cloud. |
| [ Adobe Commerce 2.4 Operationele Gidsen ](https://experienceleague.adobe.com/docs/commerce-operations/operational-guides/home.html?lang=nl-NL) | Documentatie van systemen over de concepten, processen, hulpmiddelen, en beste praktijken om Adobe Commerce op Cloud en op-gebouw projecten te ontwikkelen, op te stellen en te handhaven. |
| [ Adobe Commerce 2.4 Documentatie van de Ontwikkelaar ](https://developer.adobe.com/commerce/docs) | Documentatie gericht op ontwikkelaars die wordt gebruikt om Adobe Commerce aan te passen en te integreren met systemen van derden. |

{style="table-layout:auto"}

## B2B-compatibiliteit {#b2b-compatibility}

>[!IMPORTANT]
>
>Adobe Commerce B2B versie 1.4.2+ is compatibel met PHP 8.2. Als u de Commerce-instantie upgradet naar versie 2.4.7+, moet u ervoor zorgen dat de instantie PHP versie 8.2 gebruikt om compatibiliteit met de Adobe Commerce B2B-release te behouden. Bovendien, steunt de B2B 1.4.2+ versie niet de [ Server van de Toepassing van GraphQL ](https://experienceleague.adobe.com/nl/docs/commerce-operations/performance-best-practices/concepts/application-server).
