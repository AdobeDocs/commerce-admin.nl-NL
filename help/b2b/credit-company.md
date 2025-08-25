---
title: Bedrijfskrediet beheren
description: Meer informatie over bedrijfskredietlijnen, parameters instellen en vooruitbetalingen verwerken.
exl-id: 62ff2a36-053d-4ba0-9969-0f05701afbff
feature: B2B, Companies, Payments
role: Admin
source-git-commit: 1fc1e07f20e2c22ac430f384e9e2b278edae405c
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 0%

---

# Bedrijfskrediet beheren

Bedrijfskrediet stelt B2B-ondernemingen in staat aankopen te doen tegen een vooraf goedgekeurde kredietlijn in plaats van onmiddellijke betaling te eisen. Wanneer [ Betaling op Rekening ](../b2b/enable-basic-features.md#configure-payment-on-account) wordt toegelaten, kunnen de bedrijven tot hun kredietgrens kopen en hun creditstatus van het rekeningsdashboard bekijken.

![ Krediet van het Bedrijf ](./assets/company-create-credit-admin.png){width="700" zoomable="yes"}

Met bedrijfskrediet kunt u:

* **breidt krediettermijnen** uit - staat vertrouwde op bedrijfsklanten toe om op rekening met uitgestelde betaling te kopen
* **Vastgestelde kredietgrenzen** - controle financiële blootstelling door kredietgrenzen voor elk bedrijf te bepalen
* **de kredietactiviteit van het Spoor** - monitor alle krediettransacties, betalingen, en uitstaande saldi in real time
* **Stroomlijn B2B transacties** - vereenvoudig het koopgedrag voor bedrijven met gevestigde kredietverhoudingen
* **de complexe werkschema&#39;s van de Steun** - integreer met aankooporden, citaten, en goedkeuringsprocessen

## Vereisten

Controleer voordat u het bedrijfskrediet instelt of:

* B2B-functies zijn ingeschakeld in uw Adobe Commerce-installatie
* [ Betaling op Rekening ](../b2b/enable-basic-features.md#configure-payment-on-account) wordt gevormd en toegelaten
* De bedrijfsrekeningen worden correct opgezet met noodzakelijke bedrijfsinformatie
* U hebt beheerdersmachtigingen om bedrijfskredietinstellingen te beheren
* Valuta-instellingen worden geconfigureerd als deze in meerdere valuta&#39;s werken

## Gebruik hoofdletters

Bedrijfskrediet is ideaal voor:

* **Vestigde relaties B2B** - Van de lange termijn zakelijke klanten met bewezen betalingsgeschiedenis
* **Grote ondernemingsklanten** - De bedrijven die significante, regelmatige aankopen maken die uitgebreide betalingsvoorwaarden vereisen
* **seizoensgebonden ondernemingen** - Bedrijven met cyclische kasstroom die flexibele betalingstijdstip vereisen
* **Collectieve aanbesteding** - Organisaties met gecentraliseerde aankoop maar verdeelde betalingsverwerking
* **de ketenpartners van de Levering** - Verdelers, resellers, en kanaalpartners die kredietfaciliteiten vereisen

## Bedrijfskredietinstellingen

U kunt de volgende credit-related parameters voor elk bedrijfsprofiel vormen:

* **de munt van het Krediet** - Valuta voor alle krediettransacties en saldi
* **Grens van het Krediet** - Maximum bedrag het bedrijf kan op elk ogenblik zijn verschuldigd
* **Toestaan om Kredietgrens te overschrijden** — Of de bedrijven orden kunnen plaatsen die beschikbare kredieten overschrijden
* **Reden voor Verandering** - Documentatieveld voor het registreren van kredieten die wijzigingen plaatsen

Voor details over deze montages en het vormen van het bedrijfsprofiel, zie [ een Rekening van het Bedrijf ](account-company-create.md) creëren.

>[!NOTE]
>
>Als een bedrijf een openstaand saldo heeft, verschijnt een bericht aan de archiefbeheerder bij de bovenkant van verkooporden wanneer bekeken van Admin. Hierdoor wordt u tijdens de verwerking van bestellingen beter bewust gemaakt van de kredietstatus.

## Bedrijfskredietactiviteiten

In het gedeelte [!UICONTROL Company Credit] van het bedrijfsprofiel wordt een volledige geschiedenis van alle krediettransacties, balanswijzigingen en betalingsactiviteiten in rasterformaat weergegeven.

![ activiteit van het Krediet van het Bedrijf ](./assets/company-credit-reimbursements-grid.png){width="700" zoomable="yes"}

In het raster wordt voor elke transactie de volgende informatie weergegeven:

| Kolom | Beschrijving |
|--- |--- |
| [!UICONTROL Date] | De datum van de transactie. Houd de muisaanwijzer boven de datum en tijd om de datum en tijd weer te geven. |
| [!UICONTROL Operation] | Het type activiteit dat aan de transactie is gekoppeld. Waarden: <br/>**[!UICONTROL Allocated]**- Aan het bedrijf toegewezen krediet.<br/>**[!UICONTROL Updated]** - Er is een wijziging toegepast op een van de volgende velden: [!UICONTROL Credit limit] / [!UICONTROL Credit currency] / [!UICONTROL Allow to exceed credit limit] <br/>**[!UICONTROL Purchased]**- Er is een volgorde geplaatst.<br/>**[!UICONTROL Reimbursed]** - Het uitstaande saldo is vergoed. <br/>**[!UICONTROL Refunded]**- Er is een bedrag op creditnota terugbetaald.<br/>**[!UICONTROL Reverted]** - De bestelling is geannuleerd en het bedrag is geretourneerd naar het creditsaldo. |
| [!UICONTROL Amount] | Het bedrag van de transactie dat aan de volgende transactietypen is gekoppeld: `Purchased` / `Reimbursed` / `Refunded` / `Reverted` <br/> Voor aankoopbedragen wordt het bedrag weergegeven in de weergavevaluta van de winkel en in de notatie van de creditvalutaset, gevolgd door de huidige omrekeningskoers (indien van toepassing). Bijvoorbeeld: <br/> EUR 20.000.00 ($22.400.00) <br/> USD/EUR 0.8928 |
| [!UICONTROL Outstanding Balance] | Het terugbetaalde bedrag, verminderd met het totale verschuldigde bedrag van alle orders die zijn geplaatst met de betalingsmethode op rekening. De waarde kan positief of negatief zijn. <br/>**[!UICONTROL Positive value]**- Een vooruitbetaling wordt weergegeven als een positieve waarde.<br/>**[!UICONTROL Negative value]** - Een verschuldigd bedrag wordt weergegeven als een negatieve waarde. |
| [!UICONTROL Available Credit] | De som van de _[!UICONTROL Credit Limit]_en de_[!UICONTROL Outstanding Balance]_ . Als de onderneming de kredietlimiet heeft overschreden, wordt het bedrag weergegeven als een negatieve waarde. |
| [!UICONTROL Credit Limit] | Het bedrag van het aan de onderneming verstrekte krediet. |
| [!UICONTROL Updated By] | De naam van de persoon die de bewerking heeft gestart. |
| [!UICONTROL Custom Reference Number] | Het aangepaste referentienummer dat aan de transactie is gekoppeld. |
| [!UICONTROL Comment] | Een compilatie van de waarden van het `Reason for Change` gebied, volgens verrichtingstype. <br/>**[!UICONTROL Purchased]**- Bevat opmerkingen van de aankoop en het ordernummer en de koppeling naar de bestelling.<br/>**[!UICONTROL Reimbursed]** - Bevat opmerkingen van de vergoede transactie. |
| [!UICONTROL Action] | Alleen voor `Reimbursed` -bewerkingen. **[!UICONTROL Edit]** - Hiermee kan het restitutiebedrag worden bijgewerkt. |

{style="table-layout:auto"}

## De kredietgegevens bijwerken

Wanneer klanten betalingen verrichten, werken beheerders de kredietgegevens in Admin bij.

1. Op _Admin_ sidebar, ga naar **Klanten > Bedrijven**.

1. Vind het bedrijf in het net en open op _geef_ wijze uit.

1. Breid de **sectie van het Krediet van het Bedrijf** uit.

1. Voor **Kredietgrens**, ga de nieuwe waarde in.

1. Wijzig desgewenst de andere waarden.

1. Klik op **[!UICONTROL Save]** als de updates zijn voltooid.

## Betalingen ontvangen

Een vergoed saldo is een offline betaling die door een bedrijf wordt gedaan naar het saldo van hun rekening. De opslagbeheerder gaat het bedrag manueel in het bedrijfprofiel in, gebruikend de _knoop van het Saldo van de Terugbetaling_. Wanneer het bedrag wordt ingediend, herberekent het systeem het uitstaande saldo en het beschikbare bedrijfskrediet en registreert het de actie in de geschiedenis van het bedrijfskrediet. Het terugbetaalde bedrag wordt geboekt in de creditvaluta, zoals aangegeven in de configuratie.

### Betaling toepassen op een bedrijfsaccount

1. Voor _Admin_ sidebar, ga **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Zoek de bedrijfsrecord in de lijst en open in de modus **[!UICONTROL Edit]** .

1. Bij de bovenkant van de pagina, klik **vergoeden Saldo**.

1. Voeg in het dialoogvenster de betalingsgegevens toe:

   ![ Saldo van de Terugbetaling ](./assets/company-reimburse-balance.png){width="500"}

   * Ga het **Bedrag** van de betaling in.

     Het bedrag kan als positieve of negatieve waarde worden vermeld.

   * Indien van toepassing, ga het **Aantal van de Verwijzing van de Douane** voor verwijzing in.

     Per vergoeding kan slechts één aangepast referentienummer worden ingevoerd. Als u de betaling op meerdere inkooporder&#39;s wilt toepassen, maakt u voor elke PO een aparte vergoeding.

   * Zoals nodig, ga a **Commentaar** in om de terugbetaling te beschrijven.

1. Klik **Terugbetaling**.

   Het systeem werkt de saldi en de kredietgeschiedenis automatisch bij om de terugbetaling te weerspiegelen.

### Een vergoeding bewerken

1. Open het bedrijfsprofiel in de modus **[!UICONTROL Edit]** .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) uit de **sectie van het Krediet van het Bedrijf**.

1. Zoek de terugbetalingstransactie in het raster en klik op **[!UICONTROL Edit]** .

1. Breng om het even welke veranderingen noodzakelijk aan **Aantal van de Verwijzing van de Douane** en **Commentaar** aan.

   Het terugbetalingsbedrag kan niet worden gewijzigd.

1. Klik op **[!UICONTROL Save]**.

## Winefront-kredietgegevens

Bedrijfsbeheerders kunnen hun kredietgegevens op het dashboard van de account bekijken, waaronder het uitstaande saldo, het beschikbare krediet, de kredietlimiet en uitstaande facturen. Wanneer orders worden geannuleerd, worden de bedragen teruggezet naar het bedrijfssaldo en weergegeven in het veld Historie van krediettoewijzing.

![ Krediet van het Bedrijf ](./assets/company-credit.png){width="700" zoomable="yes"}

## Bedrijfskredietdemo

Bekijk deze demo-video voor meer informatie over het beheren van bedrijfskrediet:

>[!VIDEO](https://video.tv.adobe.com/v/344445?quality=12&learn=on)

## Beveiligingsoverwegingen

Voer bij het beheer van het bedrijfskrediet krachtige beveiligingsmaatregelen uit om gevoelige financiële gegevens te beschermen:

* **Controle van de Toegang** - Beperk de toestemmingen van het kredietbeheer tot bevoegd slechts personeel
* **de Trails van de Controle** - handhaaf uitvoerige logboeken van alle krediettransacties en wijzigingen
* **Bescherming van Gegevens** - codeer gevoelige financiële informatie zowel in doorvoer als in rust
* **de Werkschema&#39;s van de Goedkeuring** - voer multi-vlakke goedkeuringsprocessen voor significante kredietaanpassingen uit
* **Regelmatige Herzieningen** - voer periodieke controles van gebruikerstoegang en kredietverhoudingen uit

## Aanbevolen procedures

* 
   * **Beheer van het Beleid van het Krediet** - wanneer het beheren van bedrijfskrediet, duidelijk beleid voor het plaatsen van kredietgrenzen bepalen die op de geschiedenis van de klantenbetaling en bedrijfsverhoudingen worden gebaseerd. Herzie regelmatig uitstaande saldi en betalingspatronen om risico te beoordelen, en documenteer altijd veranderingen in kredietinstellingen met gedetailleerde redenen voor controledoeleinden.

Verwerk de betalingen direct om de juiste saldi te behouden en zorg ervoor dat de instellingen van de kredietvaluta in overeenstemming zijn met de primaire bedrijfsactiviteiten van elke onderneming.

* **Naleving en veiligheid** - Beperk de toestemmingen van het kredietbeheer tot bevoegd personeel slechts, voer goedkeuringswerkschema&#39;s voor significante kredietaanpassingen uit, en beschermt gevoelige financiële informatie volgens het veiligheidsbeleid van uw organisatie. Regelmatige beoordelingen van gebruikerstoegang en kredietrelaties helpen bij het handhaven van behoorlijk toezicht en naleving.

>[!MORELIKETHIS]
>
>* [ laat Eigenschappen B2B ](enable-basic-features.md) toe * Vorm Betaling op Rekening en andere functionaliteit B2B
>* [ creeer een Rekening van het Bedrijf ](account-company-create.md) * De rekeningen van het opstellingenbedrijf met kredietmogelijkheden
>* [ beheert Bedrijven ](manage-companies.md) * Overzicht van bedrijfbeheerseigenschappen
>* [ Rollen van het Bedrijf en Toestemmingen ](account-company-roles-permissions.md) * Vorm gebruikerstoegang voor kredietbeheer
>* [ Werkschema van de Orde van de Aankoop ](purchase-order-flow.md) * Begrijp hoe het krediet met kooporders integreert
>* [ B2B de Verwijzing van de Configuratie ](../configuration-reference/general/b2b-features.md) - Gedetailleerde configuratiemontages voor eigenschappen B2B
