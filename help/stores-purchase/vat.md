---
title: Belasting over de toegevoegde waarde (btw)
description: '&lt;Hierheen beschrijving toevoegen;'
exl-id: 20dbcb86-e558-47f2-968d-b5c9ec5f665b
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1992'
ht-degree: 0%

---

# Belasting over de toegevoegde waarde (btw)

Sommige landen heffen een belasting over de toegevoegde waarde (BTW) op goederen en diensten. Er kunnen verschillende BTW-tarieven zijn afhankelijk van het stadium in het productie- of distributieproces, de materialen of de diensten die u aan uw klanten verkoopt. Je kunt meer dan één BTW-tarief toepassen om de verschuldigde belasting correct te berekenen.

De handel kan worden gevormd om een belasting over de toegevoegde waarde in rekening te brengen die op of het handels of klantenadres wordt gebaseerd, als beide in het zelfde land zijn. De btw-berekeningen zijn doorgaans gebaseerd op de bestemming van de zending in plaats van op het punt van herkomst. Voor de meeste scenario&#39;s, volstaat een configuratie die BTW berekent die op het adres van de klantenverzending wordt gebaseerd.

## Voorbeeldscenario&#39;s

- Voor een btw-geregistreerd bedrijf in een EU-land dat goederen levert aan een particulier in een ander EU-land, wordt de btw berekend als een &quot;verkoop op afstand&quot; op basis van de locatie van de handelaar.

- Een bedrijf in Nederland dat een aankoop doet van een winkel in het VK die naar een adres in het VK wordt verscheept, is verplicht BTW-tarieven in het VK te betalen.

- Voor de verkoop van [downloadbare producten](../catalog/product-create-downloadable.md), of _digitale goederen_ Het BTW-tarief is echter gebaseerd op de bestemming van de scheepvaart en niet op de locatie van de handelaar. Zie [Plaats van levering van digitale goederen](taxes.md#place-of-supply-for-digital-goods-eu).

>[!TIP]
>
>Sommige grensoverschrijdende en B2B-overbrengingen hebben complexere belastingvereisten. Om de inheemse mogelijkheden van uw installatie van de Handel uit te breiden, denk na toevoegend een oplossing van het belastingbeheer van [Marketplace](https://marketplace.magento.com/extensions/accounting-finance/taxes.html).

## BTW configureren

De volgende instructies omvatten een steekproefprocedure om een BTW van 20% in het V.K. voor verkoop aan kleinhandelsklanten op te zetten. Voor andere belastingtarieven en landen volgt u de algemene procedure, maar voert u specifieke gegevens in die overeenkomen met uw land, BTW-tarief, soort klant, enzovoort.

>[!NOTE]
>
>Voordat u verdergaat, moet u weten welke regels en regels van toepassing zijn op de BTW in uw gebied.

Bij bepaalde business-to-business transacties wordt de btw niet beoordeeld. Handel kan het BTW-identificatienummer van een klant valideren om ervoor te zorgen dat de btw correct wordt beoordeeld (of niet wordt beoordeeld). Zie [Validatie van BTW-id](#vat-id-validation).

### Stap 1: Klantbelastingklassen instellen

Het proces om een belastingregel tot stand te brengen begint door een belastingtarief toe te voegen.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

   ![Klantbelastingklassen instellen](./assets/vat-zones.png){width="600" zoomable="yes"}

1. Zorg ervoor dat er een klasse van de klantenbelasting is die geschikt om met de BTW te gebruiken is.

   In dit voorbeeld moet u ervoor zorgen dat er een klasse met de naam Customer Tax is _Detailklant_. Als deze belastingklasse niet bestaat, klikt u op **[!UICONTROL Add New Tax Rate]**.

1. Voer de **[!UICONTROL Tax Identifier]** voor de nieuwe belastingklasse.

   Alle belastingtarieven worden weergegeven in het dialoogvenster _Belastingtarief_ in het veld _Informatie over belastingregels_ wanneer u belastingregels maakt.

1. Als u het postcodebereik wilt instellen (van / tot), selecteert u de optie **[!UICONTROL Zip/Post is Range]** selectievakje.

1. Kies de optie **[!UICONTROL Country]** wanneer het belastingtarief van toepassing is.

1. Voer de **[!UICONTROL Rate Percent]** die zouden worden gebruikt voor de berekening van het belastingtarief bij aankoop.

1. Klik op **[!UICONTROL Save Rate]**.

Op basis van het verzonden BTW-tarief kunt u volgende belastingregels maken. Bij gebrek aan belastingtarieven wordt het onmogelijk om belastingregels op te stellen.

### Stap 2: Klassen voor productbelasting instellen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** >  _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**.

1. Klik op **[!UICONTROL Add New Tax Rule]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Additional Settings]** sectie.

   ![Productbelastingklassen instellen](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. Onder _Productbelastingklasse_, klikt u op **[!UICONTROL Add New Tax Class]**.

1. Als u de nieuwe klasse wilt toevoegen aan de lijst met beschikbare productbelastingklassen en drie nieuwe klassen wilt maken, voert u de opdracht **[!UICONTROL Name]** van de nieuwe belastingklasse en klik op het vinkje:

   - `VAT Standard`
   - `VAT Reduced`
   - `VAT Zero`

1. Klikken **[!UICONTROL Save Class]** voor elke nieuwe klasse die u toevoegt.

1. Klik op **[!UICONTROL Save Rule]**.

### Stap 3: Instellen van belastingzones en -tarieven

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** >  _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

   In dit voorbeeld kunt u de Amerikaanse belastingtarieven verwijderen of ze ongewijzigd laten.

1. Klik op **[!UICONTROL Add New Tax Rate]**.

   ![Belastingzones en -tarieven instellen](./assets/tax-rate-create-new.png){width="600" zoomable="yes"}

1. Definieer de nieuwe tarieven als volgt:

   **BTW-standaard**

   - BTW-identificatienummer: `VAT Standard`
   - Land en land: `United Kingdom`
   - Percentage van snelheid: `20.00`

   **Verlaagde BTW**

   - BTW-identificatienummer: `VAT Reduced`
   - Land en land: `United Kingdom`
   - Percentage van snelheid: `5.00`

1. Klikken **[!UICONTROL Save Rate]** voor elk tarief.

### Stap 4: Belastingregels instellen

Een belastingregel is een combinatie van een klasse van de klantenbelasting, een klasse van de productbelasting, en een belastingtarief.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**.

1. Voeg als volgt nieuwe belastingregels toe:

   **BTW-standaard**

   - Naam: `VAT Standard`
   - Belastingklasse van klant: `Retail Customer`
   - Productbelastingklasse: `VAT Standard`
   - Belastingtarief: `VAT Standard Rate`

   **Vat verlaagd**

   - Naam: `VAT Reduced`
   - Belastingklasse van klant: `Retail Customer`
   - Productbelastingklasse: `VAT Reduced`
   - Belastingtarief: `VAT Reduced Rate`

1. Klikken **[!UICONTROL Save Rule]** voor elk tarief.

### Stap 5: Belastingsklassen toepassen op producten

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Catalog]** > **[!UICONTROL Manage Products]**.

1. Open een product uit uw catalogus in de bewerkingsmodus.

1. Op de _Algemeen_ pagina, zoek de **[!UICONTROL Tax Class]** en selecteert u de **[!UICONTROL VAT Class]** dat op het product van toepassing is.

1. Klik op **[!UICONTROL Save]**.

   ![Belastingsklassen toepassen op producten](./assets/vat-apply-classes.png){width="600" zoomable="yes"}

## Veldomschrijvingen

### Winkelgegevens

De handel gebruikt het volgende [Configuratie-instellingen voor opslaggegevens](../configuration-reference/general/general.md#store-information) om de BTW te berekenen op basis van handelsinformatie.

**[!UICONTROL VAT Number]** - Het BTW-nummer dat aan de handelaar wordt toegekend.

**[!UICONTROL Validate VAT Number]** - [Btw-validatie](#vat-id-validation) bevestigt dat het btw-nummer overeenkomt met de desbetreffende record in het [Europese Commissie](https://ec.europa.eu/taxation_customs/vies/) database.

### Klantgegevens

De handel gebruikt de volgende gebieden om BTW te berekenen gebaseerd op [klantgegevens](../customers/account-dashboard-account-information.md)).

#### Accountgegevens

**[!UICONTROL Tax/VAT Number]** - Indien van toepassing, het belastingnummer of BTW-nummer dat aan de afnemer is toegekend.

#### Adressen

**[!UICONTROL VAT Number]** - Indien van toepassing, het BTW-nummer dat gekoppeld is aan een specifiek factuuradres of verzendadres van de klant. Voor de verkoop van [digitale goederen](taxes.md#place-of-supply-for-digital-goods-eu)) binnen de EU is het BTW-bedrag gebaseerd op de bestemming van de schepen.

### Klantenaccount

De handel gebruikt het volgende [klantconfiguratie-instellingen](../customers/account-options-new.md) om de BTW te berekenen.

**[!UICONTROL Show VAT Number on Storefront]** - Hiermee bepaalt u of het veld BTW-nummer van de klant is opgenomen in het adresboek dat beschikbaar is in de klantenaccount.

**[!UICONTROL Default Value for Disable Automatic Group Changes Based on VAT ID]** - Het BTW-identificatienummer is een intern identificatienummer voor het BTW-nummer van de afnemer bij BTW-waarmerking. Tijdens de btw-validering bevestigt de Handel dat het getal overeenkomt met het [Europese Commissie](https://ec.europa.eu/taxation_customs/vies/) database. Klanten kunnen automatisch worden toegewezen aan een van de vier standaardklantengroepen op basis van de validatieresultaten.

## Validatie van BTW-id

_Validatie BTW-ID_ berekent automatisch de vereiste belasting voor B2B-transacties die binnen de Europese Unie (EU) plaatsvinden, op basis van de landinstelling van de handelaar en de klant. De handel voert de bevestiging van BTW identiteitskaart uit gebruikend de Webdiensten van [Europese Commissie][1] server.

>[!NOTE]
>
>De btw-regels beïnvloeden andere belastingregels niet en belemmeren de toepassing van andere belastingregels niet. Er kan slechts één belastingregel tegelijk worden toegepast.

- Er wordt BTW in rekening gebracht als de handelaar en de klant zich in hetzelfde EU-land bevinden.
- Er wordt geen btw geheven als de handelaar en de klant in verschillende EU-landen zijn, en beide partijen zijn in de EU geregistreerde ondernemingen.

De opslagbeheerder leidt tot meer dan één standaardklantengroep die automatisch aan de klant tijdens rekeningsverwezenlijking, adresverwezenlijking of update, en controle kan worden toegewezen. Het gevolg is dat verschillende belastingregels worden gebruikt voor verkoop binnen het land (binnenlands) en binnen de EU.

>[!IMPORTANT]
>
>Als u virtuele of downloadbare producten verkoopt waarvoor geen verzending vereist is, moet het BTW-tarief van het land van vestiging van de klant worden gebruikt voor zowel intracommunautaire als binnenlandse verkoop. Maak aanvullende individuele belastingregels voor productbelastingklassen die overeenkomen met de virtuele producten.

### Workflow voor klantregistratie

Als Validering van BTW-identificatienummer is ingeschakeld, wordt na registratie aan elke klant voorgesteld het BTW-identificatienummer in te voeren. Van alleen kopers met een btw-registratie wordt echter verwacht dat ze dit veld invullen.

Nadat een klant het BTW-nummer en andere adresvelden heeft opgegeven en ervoor kiest om op te slaan, slaat het systeem het adres op en verzendt het verzoek tot validatie van het BTW-identificatienummer naar de server van de Europese Commissie. Volgens de resultaten van de validatie wordt een van de standaardgroepen toegewezen aan een klant. Deze groep kan worden gewijzigd als een klant of een beheerder het BTW-identificatienummer van het standaardadres wijzigt of het volledige standaardadres wijzigt. Soms kan de groep tijdelijk worden gewijzigd (groepswijziging wordt geëmuleerd) tijdens het uitchecken van één pagina.

Indien ingeschakeld, kunt u de BTW-ID-validatie voor individuele klanten overschrijven door het selectievakje in het dialoogvenster _[!UICONTROL Customer Information]_pagina.

### Workflow voor uitchecken

Als de btw-validatie van een klant tijdens de afhandeling wordt uitgevoerd, worden de btw-aanvraagidentificatiecode en de datum van het btw-verzoek opgeslagen in de sectie Geschiedenis van opmerkingen van de bestelling.

Het systeemgedrag betrokken bij de bevestiging van BTW identiteitskaart en de verandering van de klantengroep tijdens de controle hangt af van hoe Valideren op Elke Transactie en de onbruikbaar maken Automatische montages van de Verandering van de Groep worden gevormd. In dit gedeelte wordt de implementatie beschreven van de Validering van het BTW-identificatienummer voor de afhandeling aan de voorzijde.

Als de klant Google Express Checkout, PayPal Express Checkout of een andere externe betalingsmethode gebruikt, wordt het afrekenen volledig uitgevoerd aan de zijkant van de externe betaalgateway. Voor dit scenario wordt _Valideren bij elke transactie_ deze instelling kan niet worden toegepast en de klantengroep kan tijdens het afrekenen niet worden gewijzigd.

![Workflow voor BTW-validatie](./assets/vat-id-validation2.png){width="550" zoomable="yes"}

### Validatie van BTW-id configureren

Om de bevestiging van BTW identiteitskaart te vormen, moet u eerst opstelling de klantengroepen die nodig zijn, en de verwante belastingklassen, tarieven, en regels tot stand brengen. Schakel vervolgens de validatie van BTW-ID in voor de winkel en voltooi de configuratie.

In de volgende voorbeelden ziet u hoe belastingklassen en -tarieven worden gebruikt voor validatie van BTW-id&#39;s. Bekijk de voorbeelden en volg vervolgens de instructies voor het instellen van de belastingklassen en -regels die nodig zijn voor uw winkel.

#### Voorbeeld: minimale belastingregels vereist voor validatie van BTW-ID

| Belastingregel 1 |  |
|--- |--- |
| Belastingsklasse van klant | Klantbelastingklassen moeten het volgende omvatten: <br />Een klasse voor binnenlandse klanten. <br />Een klasse voor klanten met onjuist opgemaakte BTW-id&#39;s.<br />Een klasse voor klanten wier validatie van BTW-id is mislukt. |
| Productbelastingklasse | Productbelastingklassen moeten een klasse voor alle typen producten bevatten, behalve bundel en virtueel. |
| Belastingtarief | Het belastingtarief moet het BTW-tarief van het land van de handelaar omvatten. |

{style="table-layout:auto"}

| Belastingregel 2 |   |
|--- |--- |
| Belastingsklasse van klant | Een klasse voor klanten binnen de unie. |
| Productbelastingklasse | Een klasse voor producten van alle types, behalve virtueel. |
| Belastingtarief | BTW-tarieven voor alle EU-landen, met uitzondering van het land van de handelaar. Momenteel is dit percentage 0%. |

{style="table-layout:auto"}

| Belastingregel 3 | (Vereist voor virtuele en downloadbare producten) |
|--- |--- |
| Belastingsklasse van klant | Klantbelastingklassen moeten het volgende omvatten: <br/>Een klasse voor binnenlandse klanten <br/>Een klasse voor klanten met een ongeldig BTW-identificatienummer A voor klanten voor wie de validatie van BTW-identificatienummer is mislukt |
| Productbelastingklasse | Een klasse voor virtuele producten. |
| Belastingtarief | BTW-tarief van het land van de handelaar. |

{style="table-layout:auto"}

| Belastingregel 4 | (Vereist voor virtuele en downloadbare producten) |
|--- |--- |
| Belastingsklasse van klant | Een klasse voor klanten binnen de unie. |
| Productbelastingklasse | Een klasse voor virtuele producten. |
| Belastingtarief | BTW-tarieven voor alle EU-landen, met uitzondering van het land van de handelaar. Momenteel is dit percentage 0%. |

{style="table-layout:auto"}

#### Stap 1: Btw-gerelateerde klantgroepen maken

De Validering van BTW-ID wijst automatisch een van de vier standaardklantengroepen toe aan klanten volgens de resultaten van de BTW-ID-validatie:

- Binnenland
- Intra-EU
- Ongeldig BTW-identificatienummer
- Validatiefout

U kunt klantengroepen voor de Bevestiging van BTW-identiteitskaart tot stand brengen of bestaande groepen gebruiken, als zij aan uw bedrijfslogica voldoen. Wanneer u Validatie BTW-id configureert, moet u elk van de gemaakte klantengroepen als een standaardinstelling voor klanten met de juiste resultaten voor BTW-id-validatie toewijzen.

#### Stap 2: Maak aan BTW gerelateerde klassen, tarieven en regels

Elke belastingregel wordt gedefinieerd door drie entiteiten:

- Belastingklassen voor klanten
- Productbelastingklassen
- Belastingtarieven

Maak de [belastingregels](tax-rules.md) voor effectief gebruik van BTW-ID-validatie.

- Belastingregels omvatten belastingtarieven en [belastingklassen](tax-class.md).
- Belastingklassen worden toegewezen aan [klantengroepen](../customers/customer-groups.md).

#### Stap 3: Validering van BTW-id inschakelen en configureren

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Indien nodig stelt u de **[!UICONTROL Store View]** voor de configuratie.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Customers]** en kiest u **[!UICONTROL Customer Configuration]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Create New Account Options]** sectie.

   In het volgende voorbeeld zijn de algemene klantinstellingen die niet gerelateerd zijn aan BTW-validatie grijs.

   ![Nieuwe accountopties maken](../configuration-reference/customers/assets/customer-configuration-create-new-account-options-vat.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Enable Automatic Assignment to Customer Group]** tot `Yes` en vul de volgende velden naar wens in.

   - **[!UICONTROL Default Group]**
   - **[!UICONTROL Default Value for Disable Automatic Group Changes Based on VAT ID]**
   - **[!UICONTROL Show VAT Number on Storefront]**

1. Klik op **[!UICONTROL Save Config]**.

#### Stap 4: Je BTW-identificatienummer en het land van vestiging instellen

1. Vouw in het linkerdeelvenster uit **[!UICONTROL General]** en kiest u **[!UICONTROL General]** onder.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Store Information]** sectie.

   ![Opslaggegevens](../configuration-reference/general/assets/general-store-information.png){width="600" zoomable="yes"}

1. Selecteer uw **[!UICONTROL Country]**.

1. Voer uw **[!UICONTROL VAT Number]** en klik op **[!UICONTROL Validate VAT Number]**.

   Het resultaat wordt direct weergegeven.

1. Klik op **[!UICONTROL Save Config]**.

#### Stap 5: De lijst van EU-lidstaten verifiëren

1. Het voortzetten in _Algemeen_ configuratiepagina, uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Countries Options]** sectie.

   ![Laagopties](../configuration-reference/general/assets/general-country-options.png){width="600" zoomable="yes"}

1. In de **[!UICONTROL European Union Countries]** , controleert of elk land van de EU is geselecteerd.

   Als u de standaardinstelling wilt wijzigen, schakelt u de optie **Systeemwaarden gebruiken** selectievakje. Houd Ctrl (PC) of Command (Mac) ingedrukt en klik op elk land dat u wilt toevoegen of verwijderen.

1. Klik op **[!UICONTROL Save Config]**.


[1]: https://ec.europa.eu/taxation_customs/vies/
