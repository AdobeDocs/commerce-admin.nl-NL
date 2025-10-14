---
title: Bedrijfshiërarchieën beheren
description: Bouw en beheer bedrijfshiërarchieën om B2B organisaties met complexe operationele modellen te steunen.
feature: B2B, Companies
role: Admin
hide: false
hidefromtoc: false
exl-id: a277ed95-7935-4d27-adb2-35116972732b
source-git-commit: 1fc1e07f20e2c22ac430f384e9e2b278edae405c
workflow-type: tm+mt
source-wordcount: '827'
ht-degree: 0%

---

# Bedrijfshiërarchieën beheren

Met de functie [!UICONTROL Company Hierarchy] kunt u meerdere verbonden bedrijven organiseren in één bovenliggende bedrijfsstructuur. Dit is ideaal voor ondernemingen met dochterondernemingen, franchises, veelvoudige plaatsen, of complexe organisatorische structuren die gecentraliseerd beheer terwijl het handhaven van individuele bedrijfsidentiteiten vereisen.

## Gebruik hoofdletters

* **centraliseer Beheer** - pas montages en configuraties over veelvoudige bedrijven van één enkel ouderbedrijf toe
* **handhaaf Structuur** - organiseer bedrijven in een logische hiërarchie die op uw bedrijfsorganisatie wijst
* **Gestroomlijnde Verrichtingen** - beheer citaten, kooporden, betalingsmethodes, en verschepende montages voor de volledige organisatie
* **de Autonome** - Individuele bedrijven behouden hun identiteit terwijl het profiteren van gedeelde configuraties

## Vereisten

Voordat u een bedrijfshiërarchie maakt, moet u ervoor zorgen dat:

* B2B-functies zijn ingeschakeld in uw Commerce-installatie
* U hebt beheerderstoegang om bedrijven te beheren
* Ouder- en kinderbedrijven zijn al opgericht als afzonderlijke bedrijven
* U begrijpt dat het toepassen van oudermontages bestaande configuraties van het kindbedrijf zal met voeten treden

## Hoe werkt het

Beheerders kunnen een bedrijfshiërarchie opbouwen door verwante bedrijven toe te wijzen aan een aangewezen moedermaatschappij, het bedrijf boven aan de organisatiehiërarchie.

Creëer in Beheer een moederbedrijf door een afzonderlijk bedrijf (`[!UICONTROL Company Type] = Company`) te bewerken en verwante bedrijven toe te wijzen in de [!UICONTROL Company Hierarchy] -configuratie.

![&#x200B; Raster van de Hiërarchie van het Bedrijf &#x200B;](./assets/company-hierarchy-grid.png){width="700"}

>[!NOTE]
>
>Voor details over het [!UICONTROL Company Hierarchy] net, zie [&#x200B; de 2&rbrace; gebiedsbeschrijvingen van de Hiërarchie van het Bedrijf &lbrace;.](account-company-create.md#company-hierarchy)

Beheer bedrijfstoewijzingen door een moederbedrijf te bewerken en het raster *[!UICONTROL Company Hierarchy]* te gebruiken om bedrijven toe te voegen of te verwijderen. Gebruik de *[!UICONTROL Actions]* controle om de [&#x200B; geavanceerde montagesconfiguratie &#x200B;](#change-company-settings) voor bedrijven in de organisatie te beheren.

## Bedrijven toewijzen aan een moedermaatschappij

1. Voor _Admin_ sidebar, navigeer aan **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![&#x200B; het Net van Bedrijven &#x200B;](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. Open vanuit het [!UICONTROL Companies] -raster de pagina met bedrijfsdetails om de toewijzingen te maken.

   * Als u extra bedrijven wilt toewijzen aan een bestaand moederbedrijf, selecteert u de handeling **[!UICONTROL Edit]** voor het moederbedrijf.
   * Als u een moedermaatschappij wilt maken, selecteert u de handeling **[!UICONTROL Edit]** voor het bedrijf dat als moedermaatschappij is aangewezen.

     U kunt geen nieuw moederbedrijf van een bestaand ouder of kindbedrijf tot stand brengen.

1. Vouw op de pagina Bedrijfsgegevens **[!UICONTROL Company Hierarchy]** uit en selecteer vervolgens **[!UICONTROL Assign Companies]** .

   ![&#x200B; creeer ouderbedrijf &#x200B;](./assets/company-hierarchy-grid.png){width="675" zoomable="yes"}

1. Kies in de lijst met beschikbare bedrijven de bedrijven die u wilt toewijzen en selecteer vervolgens **[!UICONTROL Assign Selected Companies]** .

   ![&#x200B; Uitgezochte bedrijven om toe te wijzen &#x200B;](./assets/company-hierarchy-select-companies-assign.png){width="675" zoomable="yes"}

1. Als hierom wordt gevraagd, voltooit u de bedrijfstoewijzing door **[!UICONTROL Assign]** te selecteren.

## Ondernemingen van een moedermaatschappij ontkoppelen

1. Open op de pagina Companies de pagina met bedrijfsgegevens voor het moederbedrijf door de handeling **[!UICONTROL Edit]** te selecteren.

   ![&#x200B; pagina van het bedrijfdetail van de Ouder &#x200B;](./assets/company-update.png){width="700" zoomable="yes"}

1. U kunt de lijst met toegewezen bedrijven weergeven door **[!UICONTROL Company Hierarchy]** uit te breiden.

1. Verwijder het bedrijf uit de organisatie.

   * In de kolom [!UICONTROL Action] die het bedrijf moet verwijderen, **[!UICONTROL Select]** > **[!UICONTROL Unassign from parent]** .

     ![&#x200B; verwijder een bedrijf uit een organisatie &#x200B;](./assets/company-hierarchy-grid-unassign.png){width="640" zoomable="yes"}

   * Als daarom wordt gevraagd, verwijdert u het toegewezen bedrijf uit de hiërarchie door **[!UICONTROL Unassign]** te selecteren.

## Bedrijfsinstellingen voor een organisatie beheren

Werk de [&#x200B; Geavanceerde configuratie van Montages &#x200B;](account-company-create.md#advanced-settings) voor een organisatie bij. U kunt:

* Pas de montages van de ouderconfiguratie op alle kindbedrijven toe
* Dezelfde instellingen toepassen op geselecteerde bedrijven in de organisatie

U kunt de volgende instellingen toepassen:

* **Beheer van het Citaat** - laat of maak de capaciteit voor bedrijven toe om citaten te verzoeken en te beheren
* **Inkooporders** - controle of de bedrijven tot aanschaforders kunnen leiden en leiden
* **Configuratie van de Methode van de Betaling** - bepaal welke betalingsmethodes aan bedrijven beschikbaar zijn
* **Montages van de Methode van de Betaling** - vorm specifieke parameters en grenzen van de betalingsmethode
* **Verschepende Beschikbaarheid van de Methode** - reeks welke verschepende methodes bedrijven kunnen gebruiken
* **Verschepende Configuratie van de Methode** - bepaal de montages en de beperkingen van de verschepende methode

Tijdens het updateproces blijven de aanvankelijke configuratiewaarden aan de huidige waarden in gebreke die voor het ouderbedrijf worden gevormd. U moet het selectievakje voor wijzigen inschakelen voor minstens één instelling om instellingen toe te passen op de geselecteerde bedrijven. U kunt ook de standaardwaarde voor elke instelling bijwerken voordat u de wijzigingen toepast.

>[!WARNING]
>
>Het toepassen van de montages van het moederbedrijf vervangt bestaande configuraties van het kindbedrijf, met inbegrip van kredietgrenzen, betalingsmethodes, verzendmontages, en douanebeperkingen. Nadat u de instellingen hebt toegepast, kunt u de geavanceerde instellingen voor afzonderlijke bovenliggende en onderliggende bedrijven nog steeds beheren en aanpassen door het item voor de bedrijfsregel te bewerken.

### Aanbevolen procedures

Houd rekening met de volgende aanbevolen procedures wanneer u instellingen van het moederbedrijf toepast op onderliggende bedrijven:

* Bestaande instellingen van het onderliggende bedrijf controleren voordat bovenliggende configuraties worden toegepast
* Wijzigingen in de testinstellingen voor één onderliggend bedrijf eerst
* Communiceer veranderingen aan bedrijfbeheerders die kunnen worden beïnvloed

### De montages van de ouderconfiguratie op kindbedrijven toepassen

1. Voor _Admin_ sidebar, navigeer aan **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Bewerk in het raster [!UICONTROL Companies] het bovenliggende bedrijf door **[!UICONTROL Edit]** in de kolom **[!UICONTROL Action]** te selecteren.

1. Vouw de sectie **[!UICONTROL Company Hierarchy]** op de detailpagina van het moederbedrijf uit om bedrijven in de organisatie weer te geven.

1. Selecteer de bedrijven die u wilt configureren.

   ![&#x200B; Uitgezochte bedrijven van bedrijfshiërarchie &#x200B;](assets/company-hierarchy-select-companies.png){width="675" zoomable="yes"}

1. Selecteer **[!UICONTROL Actions]** bij het **[!UICONTROL Change company settings]** -besturingselement boven het raster.

   ![&#x200B; bedrijfmontages van de Verandering voor bedrijfshiërarchie &#x200B;](assets/company-hierarchy-change-company-settings-action.png){width="675" zoomable="yes"}

1. Wijzig de configuratie van de instellingen.

   * Zoek op de pagina [!UICONTROL Change company settings] naar de configuratie-instelling die u wilt wijzigen.

   * Schakel het selectievakje **[!UICONTROL Change]** in om de instelling in te schakelen.

   * Werk indien nodig de waarde bij.

     ![&#x200B; bedrijfmontages van de Verandering voor veelvoudige bedrijven &#x200B;](assets/company-hierarchy-change-settings-config.png){width="575" zoomable="yes"}

1. Selecteer **[!UICONTROL Apply Changes]** nadat u de configuratie hebt bijgewerkt.

1. Wanneer ertoe aangezet, selecteer **[!UICONTROL Change settings]** om de configuratie voor de geselecteerde bedrijven bij te werken.

>[!MORELIKETHIS]
>
>* [&#x200B; creeer een bedrijfrekening &#x200B;](account-company-create.md) - leer hoe te om individuele bedrijven tot stand te brengen alvorens hiërarchieën te bouwen
>* [&#x200B; de rollen en de toestemmingen van het Bedrijf &#x200B;](account-company-roles-permissions.md) - Begrijp gebruikerstoegang binnen bedrijfstructuren
>* [&#x200B; het kredietbeheer van het Bedrijf &#x200B;](credit-company.md) - vorm kredietgrenzen en betalingstermijnen voor bedrijven
>* [&#x200B; beheert bedrijven &#x200B;](manage-companies.md) - Overzicht van bedrijfbeheerseigenschappen
>* [&#x200B; laat B2B eigenschappen &#x200B;](enable-basic-features.md) toe - laat en vorm B2B functionaliteit toe
