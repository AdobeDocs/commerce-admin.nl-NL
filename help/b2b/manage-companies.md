---
title: Bedrijfsbeheer
description: Stroomlijnd beheer en beheer van B2B-organisaties met complexe operationele modellen.
feature: B2B, Companies, Storefront
role: Admin
hide: false
hidefromtoc: false
exl-id: 8246be3d-ff9f-4f9f-875d-1b999befc534
source-git-commit: 1fc1e07f20e2c22ac430f384e9e2b278edae405c
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 0%

---

# Bedrijfsbeheer

Het beheer van het bedrijf in Adobe Commerce verstrekt uitvoerige hulpmiddelen voor beheerders om, B2B bedrijfsverhoudingen te organiseren te vormen en te controleren. Deze eigenschap is essentieel voor ondernemingen die met veelvoudige collectieve klanten, dochterondernemingen, of complexe organisatorische structuren werken.

Met bedrijfsbeheer kunt u:

* **organiseer BedrijfsVerhoudingen** - creeer en beheer individuele bedrijfrekeningen voor uw klanten B2B
* **bouwt Organisatorische Hiërarchieën** - de ouder-kind verhoudingen van de Structuur die real-world bedrijfsorganisaties weerspiegelen
* **centraliseer Beleid** - beheer veelvoudige bedrijven en hun montages van één enkele administratieve interface
* **Stroomlijn Verrichtingen** - pas verenigbare configuraties en beleid over verwante bedrijven toe
* **de Complexe Structuren van de Steun** - leidt dochterondernemingen, franchises, multi-locatieondernemingen, en collectieve afdelingen

De gebruikers van Admin kunnen een bedrijfshiërarchie bouwen om een organisatie te weerspiegelen B2B door bedrijven aan een aangewezen ouderbedrijf toe te wijzen. Met deze toewijzing kan de beheerder van het moederbedrijf bedrijven binnen de organisatie weergeven en beheren.

Start bedrijfsbeheertaken vanuit de *[!UICONTROL Companies]* -weergave. Ga vanuit Beheer naar **[!UICONTROL Customers]** > **[!UICONTROL Companies]** .

![&#x200B; B2B beheert het Net van Bedrijven &#x200B;](./assets/companies-grid-view.png){width="700" zoomable="yes"}

## Vereisten

Controleer voordat u bedrijven beheert of:

* B2B-functies zijn ingeschakeld in uw Adobe Commerce-installatie
* U hebt beheerdersrechten met bedrijfsbeheermachtigingen
* De rekeningen van het bedrijf worden behoorlijk gevormd met noodzakelijke bedrijfsinformatie
* Gebruikersrollen en -machtigingen zijn gedefinieerd voor bedrijfsbeheerders en gebruikers

## Gebruik hoofdletters

Bedrijfsbeheer is ideaal voor:

* **Multilocation ondernemingen** met gecentraliseerde het kopen maar plaats-specifieke behoeften
* **verrichtingen van de franchise** die zowel collectief toezicht als lokale autonomie vereisen
* **Collectieve dochterondernemingen** met gedeeld beleid maar onafhankelijke verrichtingen
* **Grote ondernemingen** met veelvoudige afdelingen of bedrijfseenheden
* **de netwerken van de Distributie** met resellers, dealers, of kanaalpartners

## Het begrip van de Hiërarchie van het Bedrijf en Bedrijfstypes

De hiërarchie van het bedrijf bouwt bedrijfsverhoudingen door veelvoudige ondernemingen onder één enkele moederonderneming te organiseren. Deze functie weerspiegelt de reëel-wereld organisatiestructuren terwijl het toelaten van gecentraliseerd beheer en het bewaren van individuele bedrijfsidentiteiten.

### Bedrijfstypen

De kolom *[!UICONTROL Company Type]* in het raster Bedrijven toont hoe elk bedrijf binnen uw B2B-organisatie past:

* **ouder** - Centrale hub met één of meerdere toegewezen bedrijven
   * Beheert veelvoudige kindbedrijven maar kan niet aan een andere ouder worden toegewezen
   * **het geval van het gebruik** - Collectief hoofdkwartier, belangrijkste franchise organisatie, of holding bedrijf

* **Kind** - Bedrijf dat aan een ouderorganisatie wordt toegewezen
   * Werkt onder bovenliggend beheer en kan configuraties overerven
   * Kan slechts één bovenliggend item tegelijk hebben
   * **geval** - de bijkantoren van het Gebruik, franchiselocaties, of regionale afdelingen

* **Bedrijf** - Onafhankelijk enig bedrijf
   * Werkt onafhankelijk zonder hiërarchische relaties
   * Kan worden omgezet in bovenliggend element (door bedrijven toe te wijzen) of onderliggend element (door toewijzing aan bovenliggend element)
   * **geval van het Gebruik** - Individuele bedrijfsklanten of standalone cliënten

### Bedrijfstypen converteren

* **Enig Bedrijf → De ouder** - wijst andere bedrijven aan het toe
* **Enig Bedrijf → Kind** - wijs het aan een bestaand ouderbedrijf toe
* **Kind → Enig** - wijs het kindbedrijf van zijn ouder toe
* **Ouder → Kind** - niet mogelijk zonder eerst alle toegewezen bedrijven te verwijderen

### Bedrijfshiërarchieën beheren

Vouw *[!UICONTROL Company Hierarchy]* uit om alle verwante bedrijven weer te geven wanneer u bedrijven in een hiërarchie bewerkt. Een markering `Current` geeft het bedrijf aan dat wordt bewerkt.

![&#x200B; B2B het net van de Hiërarchie van het Bedrijf &#x200B;](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}

Voor gedetailleerde geleidelijke instructies, zie [&#x200B; leiden de Hiërarchie van het Bedrijf &#x200B;](manage-company-hierarchy.md).

## Bedrijfstaken

Wanneer beheerders bedrijven beheren vanuit het bedrijfsraster, kunnen ze de volgende taken uitvoeren vanuit het *[!UICONTROL Company Hierarchy]* -raster:

* **Mening en beheer bedrijfsverhoudingen**
   * **Mening Verwante Bedrijven** - zie alle bedrijven verbonden aan een ouderorganisatie in één gecentraliseerde mening
   * **de Status van het Bedrijf van de Monitor &lbrace;** - Spoor actief, in afwachting van, en inactieve bedrijven binnen de hiërarchie
   * **Van het Bedrijf van de Toegang Details** - navigeer direct aan individuele pagina&#39;s van de bedrijfconfiguratie

* **bouwt en wijzigt hiërarchieën**
   * **wijs bedrijven** toe - voeg bestaande bedrijven aan een ouderorganisatie van de pagina van het bedrijfdetails toe
   * **creeer ouder-kind verhoudingen** - de bedrijven van de Structuur om echte bedrijfsverhoudingen te weerspiegelen
   * **reorganize structuren** - Verplaats bedrijven tussen verschillende ouderorganisaties aangezien de bedrijfsbehoeften veranderen

* **Bulk configuratiebeheer**
   * **pas montages over bedrijven** toe - Update geavanceerde montages voor veelvoudige bedrijven gelijktijdig gebruikend de [!UICONTROL Actions] controle op het net van het Bedrijf
   * **normaliseer configuraties** - verzeker verenigbaar beleid over verwante organisaties
   * **met voeten treedt individuele montages** - duw de configuraties van het ouderbedrijf aan geselecteerde kindbedrijven

* **Administratieve acties**
   * **verwijder bedrijfverhoudingen** - gebruik de *[!UICONTROL Unassign from parent]* actie om organisatorische banden op te lossen
   * **beheert bedrijftoegang** - Controle die de beheerders bedrijfverhoudingen kunnen bekijken en wijzigen
   * **de hiërarchieveranderingen van de Monitor** - de wijzigingen van het Spoor aan organisatorische structuren

## Aanbevolen procedures

Houd bij het beheren van bedrijven rekening met de volgende aanbevolen procedures:

* **de bedrijfhiërarchieën van de Bouw** - wanneer het beheren van complexe bedrijfstructuren, plan uw hiërarchie om echte bedrijfsverhoudingen aan te passen terwijl het houden van structuren eenvoudig om gebruikersverwarring te vermijden. Documenteer alle bedrijfsverhoudingen en hun bedrijfsverbindingen voor toekomstige verwijzing.

* **het beheer van de Configuratie** - de configuratieveranderingen van de Test op individuele bedrijven alvorens hen op volledige hiërarchieën toe te passen, en altijd huidige montages van het document alvorens bulkveranderingen aan te brengen. Deel geplande veranderingen aan beïnvloede bedrijfbeheerders vooraf mee.

* **Veiligheid** - Beperk de toestemmingen van het bedrijfbeheer tot vertrouwde op beheerders slechts, voer regelmatige overzichten van bedrijfverhoudingen en toegangstoestemmingen, en controleer alle hiërarchiefveranderingen voor controledoeleinden.

>[!MORELIKETHIS]
>
>* [&#x200B; creeer een bedrijfrekening &#x200B;](account-company-create.md)
>* [&#x200B; beheer bedrijfhiërarchieën &#x200B;](manage-company-hierarchy.md)
>* [&#x200B; de rollen en toestemmingen van het Bedrijf &#x200B;](account-company-roles-permissions.md)
>* [&#x200B; Het kredietbeheer van het Bedrijf &#x200B;](credit-company.md)
>* [&#x200B; laat B2B eigenschappen &#x200B;](enable-basic-features.md) toe
