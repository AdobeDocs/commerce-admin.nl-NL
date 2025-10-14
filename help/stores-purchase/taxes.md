---
title: Belastingen
description: Leer hoe u uw winkel configureert om belastingen te berekenen volgens de vereisten van uw landinstelling.
exl-id: bf807132-416f-497a-82c4-b00dba4d3092
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1100'
ht-degree: 0%

---

# Belastingen

Configureer uw winkel om belastingen te berekenen volgens de vereisten van uw landinstelling. U kunt opstelling [&#x200B; belastingklassen &#x200B;](tax-class.md) voor producten en klantengroepen, en [&#x200B; belastingregels &#x200B;](tax-rules.md) creëren die product en klantenklassen, belastingstreken, en tarieven combineren. Commerce biedt ook configuratie-instellingen voor vaste productbelastingen, samengestelde belastingen en prijzen over de internationale grenzen heen. Als u wordt vereist om a [&#x200B; toegevoegde belasting &#x200B;](vat.md) te verzamelen, kunt u opstelling uw opslag om de aangewezen hoeveelheid met bevestiging automatisch te berekenen.

>[!NOTE]
>
>Adobe Commerce en Magento Open Source versie 2.4.0 tot en met 2.4.3 bevatten de door de leverancier ontwikkelde Vertex-extensie die wordt gebruikt voor integratie met de Vertex Cloud om belastingbeheer en adreszuivering te bieden. Vanaf de release 2.4.4 wordt deze extensie niet meer gebundeld met de kernrelease en moet deze worden geïnstalleerd en bijgewerkt vanaf de Commerce Marketplace of rechtstreeks vanaf de leverancier. [&#x200B; Vertex van het Contact &#x200B;](https://marketplace.magento.com/partner/vertex_inc) voor informatie over de uitbreiding en de documentatie.<br><br>
>
>Als u de gebundelde toegelaten en gevormde uitbreiding hebt, moet u uw composer.json- dossier als deel van het 2.4.4 verbeteringsproces bijwerken en om extensie updates te beheren die door:gaan. Zie [&#x200B; modules van de Verbetering &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html?lang=nl-NL) in de _Gids van de Verbetering_.

## Snelle verwijzing

Sommige belastinginstellingen hebben een keuze uit opties die bepalen hoe de belasting wordt berekend en aan de klant wordt gepresenteerd. Voor meer informatie, zie [&#x200B; Internationale Richtsnoeren van de Belasting &#x200B;](international-tax-guidelines.md).

Gebruik de volgende tabellen ter referentie bij het configureren van instellingen voor belastingberekening:

### Methoden voor belastingberekening

De opties voor de berekeningsmethode voor belastingen omvatten [!UICONTROL Unit Price] , [!UICONTROL Row Total] en [!UICONTROL Total] . In de volgende tabel wordt uitgelegd hoe afronden (tot twee cijfers) wordt verwerkt voor verschillende instellingen.

| Instelling | Berekening en weergave |
|--- |--- |
| [!UICONTROL Unit Price] | Commerce berekent de belasting voor elk object en geeft de prijzen inclusief btw weer. Om het totaal van de belasting te berekenen, wordt de belasting voor elk punt afgerond, en dan voegt hen samen. |
| [!UICONTROL Row Total] | Commerce berekent de belasting voor elke regel. Om het totaal van de belasting te berekenen, rondt het de belasting voor elke lijnpost en voegt dan hen samen. |
| [!UICONTROL Total] | Commerce berekent de belasting voor elk item en voegt deze belastingwaarden toe om het totale niet-afgeronde belastingbedrag voor de order te berekenen. Vervolgens wordt de opgegeven afrondingsmodus toegepast op de totale belasting om de totale belasting voor de bestelling te bepalen. |

{style="table-layout:auto"}

### Catalogusprijzen met of zonder belasting

De mogelijke weergavevelden zijn afhankelijk van de berekeningsmethode en of in de catalogusprijzen belastingen zijn opgenomen of niet. Weergavevelden hebben twee decimale precisie in normale berekeningen. Bij sommige combinaties van prijsinstellingen worden prijzen weergegeven die zowel belasting als geen belasting bevatten. Wanneer allebei op het zelfde lijnpunt verschijnen, kan het aan klanten verwarrend zijn, en a [&#x200B; waarschuwing &#x200B;](taxes.md#warning-messages) teweegbrengt.

| Instelling | Berekening en weergave |
|--- |--- |
| [!UICONTROL Excluding Tax] | Met deze instelling wordt de prijs van het basisitem gebruikt zoals deze wordt ingevoerd en worden de methoden voor belastingberekening toegepast. |
| [!UICONTROL IncludingTax] | Met deze instelling wordt eerst de prijs van het basisitem exclusief belasting berekend. Deze waarde wordt gebruikt als de basisprijs en de methoden voor belastingberekening worden toegepast. |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>Er zijn veranderingen ten opzichte van eerdere versies voor EU-handelaren of andere btw-handelaren die prijzen, inclusief belastingen, weergeven en actief zijn in verschillende landen met meerdere opvattingen over winkels. Als je prijzen met meer dan twee cijfers nauwkeurig laadt, geeft Commerce automatisch alle prijzen weer op twee cijfers zodat kopers een consistente prijs krijgen te zien.

### Verzendprijzen met of zonder btw

| Instelling | Weergave | Berekening |
|--- |--- |--- |
| [!UICONTROL Excluding Tax] | Wordt zonder belasting weergegeven. | Normale berekening. De verzending wordt toegevoegd aan het totaal van de winkelwagentjes, meestal weergegeven als een afzonderlijk object. |
| [!UICONTROL Including Tax] | Kan inclusief belastingen zijn, of de belasting kan afzonderlijk worden weergegeven. | Verzending wordt met dezelfde berekeningen behandeld als een ander artikel in de winkelwagen met belastingen. |

{style="table-layout:auto"}

### Belastingbedragen als posten

Om twee verschillende belastingbedragen als afzonderlijke lijnpunten, zoals GST en PST voor Canadese opslag te tonen, moet u verschillende prioriteiten voor de verwante belastingregels plaatsen. In eerdere belastingberekeningen zouden belastingen met verschillende prioriteiten echter automatisch worden aangevuld. Om afzonderlijke belastingbedragen zonder een onjuiste samenstelling van de belastingbedragen correct te tonen, kunt u verschillende prioriteiten plaatsen, en ook _selecteren berekent van subtotaal slechts_ checkbox. Deze instelling resulteert in correct berekende belastingbedragen die als afzonderlijke regelitems worden weergegeven.

## Waarschuwingsberichten

Sommige combinaties van belastinggerelateerde opties kunnen verwarrend zijn voor klanten en een waarschuwing veroorzaken. Deze voorwaarden kunnen zich voordoen wanneer de methode voor belastingberekening is ingesteld op `Row` of `Total` en de klant prijzen krijgt die zowel belasting uitsluiten als opnemen. Dit kan ook gebeuren wanneer er belasting per artikel in de winkelwagen is. Omdat de belastingberekening is afgerond, kan het bedrag dat in de winkelwagen wordt weergegeven afwijken van het bedrag dat een klant verwacht te betalen.

Als uw belastingberekening op een problematische configuratie gebaseerd is, verschijnen de volgende waarschuwingen:

![&#128279;](../assets/icon-warning.png) **Waarschuwing** van het 0&rbrace; Uitroepingspunt `Tax discount configuration might result in different discounts than a customer might expect for store(s); Europe Website (French), Europe Website (German). Please see source for more details.`.

![&#128279;](../assets/icon-warning.png) **Waarschuwing** van het 0&rbrace; Uitroepingspunt `Tax configuration can result in rounding errors for store(s): Europe Websites (French), Europe Websites (German).`.

## Plaats van levering van digitale goederen (EU)

Handelaren in de Europese Unie (EU) moeten hun digitale goederen die per kwartaal aan elke lidstaat worden verkocht, melden. Digitale goederen worden belast op basis van het verzendadres van de klant. De wet schrijft voor dat handelaren een belastingrapport moeten opstellen en de relevante belastingbedragen voor digitale goederen moeten vaststellen, in tegenstelling tot fysieke goederen.

Handelaren moeten alle digitale goederen die door EU-lidstaten worden verkocht op kwartaalbasis aan een centrale belastingdienst rapporteren, samen met de betaling die verschuldigd is voor de in de periode geïnde belasting.

Handelaren die de drempel nog niet hebben bereikt (50 k/100 kB euro per jaaromzet) moeten fysieke goederen blijven rapporteren die worden verkocht aan de EU-landen waar zij BTW-nummers hebben geregistreerd.

Handelaren die worden gecontroleerd op voor digitale goederen betaalde belastingen, moeten twee ondersteunende gegevens verstrekken om de verblijfplaats van de afnemer te bepalen.

- Het verzendadres van de klant en een overzicht van een geslaagde betalingstransactie kunnen worden gebruikt om de woonplaats van de klant vast te stellen. (Betaling wordt alleen geaccepteerd als het verzendadres overeenkomt met de gegevens van de betalingsprovider.)
- De informatie kan ook rechtstreeks worden vastgelegd via de gegevensopslag in de Commerce-databasetabellen.

_&#x200B;**om digitale goederen belastinginformatie te verzamelen:**&#x200B;_

1. De belastingtarieven voor alle EU-lidstaten laden.

1. Maak een categorie voor productbelasting voor digitale goederen.

1. Wijs al uw digitale goederen aan de de belastingklasse van het digitale goederenproduct toe.

1. Creeer [&#x200B; belastingregels &#x200B;](tax-rules.md) voor uw fysieke goederen, gebruikend fysieke klassen van de productbelasting, en associeer hen met de aangewezen belastingtarieven.

1. Maak belastingregels voor uw digitale goederen, gebruik de productbelastingklasse voor digitale goederen, en associeer deze met de juiste belastingtarieven voor EU-lidstaten.

1. Voer het belastingrapport voor de juiste periode uit en verzamel de vereiste informatie over digitale goederen.

1. Exporteer de belastingbedragen die verband houden met de belastingtarieven voor de categorie belasting digitale goederen.

Aanvullende bronnen:

- [ Belastingen en Douane-unie van de Europese Commissie ][1]
- [ EU 1015 Plaats van de Veranderingen van de Levering ][2]

[1]: https://europa.eu/youreurope/business/taxation/vat/vat-rules-rates/index_en.htm
[2]: https://www2.deloitte.com/global/en/services/tax.html
