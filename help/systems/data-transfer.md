---
title: Gegevensoverdracht
description: Meer informatie over ondersteuning voor gegevensoverdracht, waaronder gegevensvalidatie.
exl-id: 5057e398-c458-42e9-8ec0-bf116a667a3c
feature: System, Data Import/Export
source-git-commit: 62978d10bc1b53d3a7983b0a37ccd64e6ab0f740
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 0%

---

# Gegevensoverdracht

Met de gereedschappen voor importeren en exporteren kunt u meerdere records in één bewerking beheren. U kunt nieuwe items importeren en bestaande productsets bijwerken, vervangen en verwijderen.

U kunt bijvoorbeeld nieuwe producten aan uw voorraad toevoegen, productgegevens en geavanceerde prijsgegevens bijwerken en een reeks bestaande producten vervangen door nieuwe producten. Met de gereedschappen voor importeren en exporteren kunt u grote productcatalogi efficiënter beheren, omdat u de gegevens kunt exporteren, bewerken in een spreadsheet en deze weer in uw winkel kunt importeren in plaats van meerdere bewerkingen uit te voeren in de beheerfunctie.

Naast de import- en exportfuncties heeft Adobe Commerce processen zoals [catalogussync](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/data-services/catalog-sync.html) die productgegevens van de Commerce-server naar SaaS-diensten exporteren. Voor functies zoals [Product Recommendations](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/overview.html), maakt deze synchronisatie het mogelijk om aanbevelingen met correcte namen, tarifering, en beschikbaarheid nauwkeurig terug te keren.

## Gegevensvalidatie

Alle gegevens moeten validatie doorstaan om de kwaliteit, nauwkeurigheid en integriteit van de waarden te garanderen voordat ze in de winkel worden geïmporteerd. Validatie begint wanneer u klikt **[!UICONTROL Check Data]**. Tijdens het proces worden alle entiteiten in het importbestand gecontroleerd op het volgende:

- **Attributen** - Kolomkopnamen worden geverifieerd om ervoor te zorgen dat ze overeenkomen met de corresponderende kenmerken in de systeemdatabase. De waarde van elk attribuut wordt gecontroleerd om ervoor te zorgen dat het aan de vereisten van het gegevenstype (decimaal, geheel, varchar, tekst, en datetime) voldoet.
- **Complexe gegevens** - Waarden die afkomstig zijn van een gedefinieerde set, zoals een vervolgkeuzelijst of meerdere invoertypen die u selecteert, worden gecontroleerd om te controleren of de waarden in de gedefinieerde set aanwezig zijn.
- **Servicegegevens** - De waarden in de kolommen van de de dienstgegevens worden geverifieerd om ervoor te zorgen dat de eigenschappen of de complexe gegevenswaarden verenigbaar zijn met wat reeds in het systeemgegevensbestand wordt bepaald.
- **Vereiste waarden** - Voor nieuwe entiteiten wordt de aanwezigheid van vereiste kenmerkwaarden in het bestand gecontroleerd. Voor bestaande entiteiten is het niet nodig opnieuw te controleren of er vereiste kenmerkwaarden bestaan.
- **Scheidingstekens** - Hoewel de scheidingstekens niet zichtbaar zijn in een spreadsheet, worden de gegevenswaarden in een CSV-bestand gescheiden door komma&#39;s en worden tekstwaarden ingesloten door dubbele aanhalingstekens. Tijdens het validatieproces wordt de opmaak gecontroleerd voor de scheidingstekens en elke set aanhalingstekens die tekenreeksen omsluiten.

De resultaten van de validatie worden weergegeven in de sectie Validatieresultaten en bevatten de volgende informatie:

- Aantal gecontroleerde entiteiten
- Het aantal ongeldige rijen
- Het aantal gevonden fouten

Als de gegevens geldig zijn, kan een _Importeren voltooid_ wordt weergegeven.

![Systeembericht - bestand is geldig](./assets/data-import-validation-message.png){width="500" zoomable="yes"}

Als de validatie mislukt, leest u de beschrijving van elke fout en corrigeert u het probleem in het CSV-bestand. Als een rij bijvoorbeeld een ongeldige SKU bevat, stopt het importproces en worden die rij en alle volgende rijen niet geïmporteerd. Importeer de gegevens opnieuw nadat het probleem correct is opgelost. Als er veel fouten worden aangetroffen, kan het meerdere pogingen duren om voor de validatie te slagen.

### Gegevensvalidatieberichten

#### Validatie

- `Product with specified SKU not found in rows: 1`
- `URL key for specified store already exists`
- `'7z' file extension is not supported`
- `TXT file extension is not supported`

#### Fouten

- `Wrong field type. Type in the imported file %decimal%, expected type is %text%.`
- `Value is not allowed. Attribute value does not exist in the system.`
- `Field %column name% is required.Wrong value separator is used.`
- `Wrong encoding used. Supported character encoding is UTF-8 and Windows-1252.`
- `Imported file does not contain SKU field.`
- `SKU does not exist in the system.`
- `Column name %column name% is invalid. Should start with a letter. Alphanumeric.`
- `Imported file does not contain a header.`
- `%website name% website does not exist in the system.`
- `%storeview name% storeview does not exist in the system.`
- `Imported attribute %attribute name% does not exist in the system.`
- `Imported resource (image) could not be downloaded from external resource due to timeout or access permissions.`
- `Imported resource (image) does not exist in the local media storage.`
- `Product creation error displayed to the user equal to the one seen during manual product save.`
- `Advanced Price creation error displayed to the user equal to the one seen during the manual product save.`
- `Customer creation error displayed to the user equal to the one seen during the manual customer save.`
