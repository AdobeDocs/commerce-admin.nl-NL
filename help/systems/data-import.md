---
title: Gegevens importeren
description: Leer meer over richtlijnen voor het importeren van gegevens en hoe u de bewerkingen voor het importeren van gegevens kunt gebruiken.
exl-id: caae8811-445e-49d4-aa90-226a355732bc
feature: Products, Customers, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1465'
ht-degree: 0%

---

# Gegevens importeren

Gegevens voor alle producttypen kunnen in de winkel worden geïmporteerd. Daarnaast kunt u producten, geavanceerde prijsgegevens, klantgegevens, adresgegevens van de klant en productafbeeldingen importeren. Importeren ondersteunt de volgende bewerkingen:

- Toevoegen/bijwerken
- Vervangen
- Verwijderen

## Richtlijnen voor importeren

### Nieuwe entiteiten

- Entiteiten worden toegevoegd met de kenmerkwaarden die in het CSV-bestand zijn opgegeven.
- Voor een vereist kenmerk zonder standaardwaarde kan de entiteit (de bijbehorende rij of rijen) niet worden geïmporteerd als er geen waarde of een niet-geldige waarde is.
- Voor een vereist kenmerk met een standaardwaarde wordt de entiteit (de corresponderende rij of rijen) geïmporteerd en wordt de standaardwaarde voor het kenmerk ingesteld als er geen waarde of een niet-geldige waarde is.
- Als de complexe gegevens niet geldig zijn, kan de entiteit (de bijbehorende rij of rijen) niet worden geïmporteerd.

### Bestaande entiteiten

- Voor kenmerken die geen complexe gegevens zijn, vervangen de waarden uit het importbestand, inclusief de lege waarden voor de niet-vereiste kenmerken, de bestaande waarden.
- Als er geen waarde is of als er een niet-geldige waarde is voor een vereist kenmerk, wordt de bestaande waarde niet vervangen.
- Als de complexe gegevens voor de entiteit ongeldig zijn, kan de entiteit (de corresponderende rij of rijen) niet worden geïmporteerd, behalve in het geval dat Entiteiten verwijderen is geselecteerd in de vervolgkeuzelijst Gedrag importeren.

### Complexe gegevens

Als er een kenmerk bestaat dat in het importbestand is opgegeven en de waarde ervan wordt afgeleid van een gedefinieerde set waarden, geldt het volgende:

- Als de waarde nog niet is opgenomen in de gedefinieerde reeks waarden, kan de rij worden geïmporteerd en wordt een standaardwaarde (indien gedefinieerd) voor het kenmerk ingesteld.
- Als de waarde al in de gedefinieerde set is opgenomen, kan de bijbehorende rij niet worden geïmporteerd.
- Als in het importbestand een kenmerknaam wordt opgegeven die nog niet in het systeem is gedefinieerd, wordt deze niet gemaakt en worden de waarden ervan niet geïmporteerd.

### Ongeldige bestanden

- Een bestand kan niet worden geïmporteerd als alle rijen ongeldig zijn.
- Er zijn niet-bestaande servicegegevens of complexe gegevensnamen opgegeven in het importbestand, zoals een kolom met een `_<non-existing name>` kop.

## Importeren

| Bewerking | Beschrijving |
| --------- | ----------- |
| Toevoegen/bijwerken | Nieuwe productgegevens worden toegevoegd aan de bestaande productgegevens voor de bestaande vermeldingen in de database. Alle velden behalve `sku` kan worden bijgewerkt.<br><br>Nieuwe belastingklassen die in de importgegevens worden opgegeven, worden automatisch gemaakt.<br><br>Nieuwe productcategorieën die in het importbestand zijn opgegeven, worden automatisch gemaakt.<br><br>Nieuwe SKU&#39;s die in het importbestand zijn opgegeven, worden automatisch gemaakt <br><br>**_Opmerking:_**Voor producten, kunt u alle gebieden behalve SKU door de invoer bijwerken.<br><br>**_Belangrijk:_** Meerdere veldwaarden, zoals websites of categorieën, kunnen niet worden verwijderd met de opdracht _Toevoegen/bijwerken_ importgedrag. Deze velden blijven na het importeren in de database als ze niet in het CSV-bestand worden vermeld. |
| Vervangen | De bestaande productgegevens worden vervangen door nieuwe gegevens.<br><br>**_Belangrijk:_**Wees voorzichtig bij het vervangen van gegevens, omdat de bestaande productgegevens worden gewist en alle referenties in het systeem verloren gaan.<br><br>Als een SKU in de invoergegevens SKU van een bestaande entiteit aanpast, worden alle gebieden, met inbegrip van SKU, geschrapt en een nieuw verslag wordt gecreeerd gebruikend de CSV gegevens. Er treedt een fout op als het CSV-bestand verwijst naar een SKU die niet bestaat in de database. U kunt Gegevens controleren om fout te tonen. |
| Verwijderen | Entiteiten in de importgegevens die in de database aanwezig zijn, worden uit de database verwijderd.<br><br>Met Verwijderen worden alle kolommen in de importgegevens genegeerd, behalve SKU. U kunt alle andere kenmerken in de gegevens negeren.<br><br>Er treedt een fout op als het CSV-bestand verwijst naar een SKU die niet bestaat in de database. U kunt Gegevens controleren om fout te tonen. |

{style="table-layout:auto"}

## Importproces

De grootte van het importbestand wordt bepaald door de instellingen in het dialoogvenster `php.ini` op de server. Het systeembericht op de _Importeren_ geeft de huidige maximale grootte aan. De standaardgrootte is 2 MB.

Speciale tekens (zoals het gelijkteken, groter en kleiner dan symbolen, enkele en dubbele aanhalingstekens, backslash, pipe en en ampersand-symbolen) kunnen problemen veroorzaken tijdens de gegevensoverdracht. Om ervoor te zorgen dat dergelijke speciale tekens correct worden geïnterpreteerd, kunnen ze worden gemarkeerd als een _escapereeks_. Als de gegevens bijvoorbeeld een tekenreeks bevatten, zoals `code="str"`, `code="str2"`Als u ervoor kiest de tekst tussen dubbele aanhalingstekens te plaatsen, zorgt u ervoor dat de oorspronkelijke dubbele aanhalingstekens worden beschouwd als onderdeel van de gegevens. Wanneer het systeem een dubbele reeks dubbele citaten ontmoet, begrijpt het dat de buitenste reeks dubbele citaten de daadwerkelijke gegevens omsluit.

Bij het importeren van productgegevens worden nieuwe productgegevens toegevoegd aan bestaande productgegevens in de database. Alle velden behalve SKU kunnen via importeren worden bijgewerkt. Alle bestaande productgegevens worden vervangen door de geïmporteerde nieuwe gegevens. Wees voorzichtig bij het vervangen van gegevens. Alle bestaande productgegevens worden gewist en alle referenties in het systeem gaan verloren.

![Gegevens importeren](./assets/import-options.png){width="600" zoomable="yes"}

### Stap 1: De gegevens voorbereiden

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. Onder _Instellingen importeren_, set **[!UICONTROL Entity Type]** op een van de volgende wijzen:

   - `Advanced Pricing`
   - `Products`
   - `Customer Finances`
   - `Customers and Addresses`
   - `Customers Main File`
   - `Customer Addresses`
   - `Stock Sources`

1. Klik op **[!UICONTROL Download Sample File]**.

1. Zoek het exportbestand op de downloadlocatie voor uw webbrowser en open het bestand.

   Het voorbeeldbestand bevat kolomkoppen met plaatsaanduidingsgegevens voor de producttypen.

   ![Gegevensvoorbeeldbestand importeren](./assets/data-export-sample-data.png){width="600" zoomable="yes"}

1. Onderzoek de structuur van het steekproefdossier en gebruik het om uw CSV het invoerdossier voor te bereiden, ervoor zorgend dat de kolomrubrieken correct worden gespeld.

1. Controleer of de grootte van het importbestand de limiet die in het bericht wordt weergegeven, niet overschrijdt.

   ![Gegevensimportgroottemelding](./assets/data-import-size-notification.png){width="600"}

1. Als de importgegevens paden naar productafbeeldingen bevatten, moet u ervoor zorgen dat de afbeeldingsbestanden naar de juiste locatie zijn geüpload.

   De standaardlocatie op de Commerce-server is: `pub/media/import`.

   Als de afbeeldingen zich op een externe server bevinden, controleert u of u de volledige URL naar de map met de afbeeldingen hebt.

### Stap 2: kies het importgedrag

![Gedrag bij importeren van gegevens](./assets/data-import-import-behavior.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Import Behavior]** op een van de volgende wijzen:

   - `Add/Update` (Voor producten kunt u alle velden bijwerken, behalve SKU via importeren.)
   - `Replace`
   - `Delete`

1. Kies een van de volgende opties om te bepalen wat er gebeurt wanneer er een fout optreedt bij het importeren van gegevens:

   - `Stop on Error`
   - `Skip error entries`

1. Voor **[!UICONTROL Allowed Errors Count]** Voer het aantal fouten in dat kan optreden voordat het importeren wordt geannuleerd.

   De standaardwaarde is 10.

1. Accepteer de standaardwaarde van een komma (`,`) voor **[!UICONTROL Field separator]**.

1. Accepteer de standaardwaarde van een komma (`,`) voor **[!UICONTROL Multiple value separator]**.

   In een CSV-bestand is een komma het standaardscheidingsteken. Als u een ander teken wilt gebruiken, moet u ervoor zorgen dat de gegevens in het CSV-bestand overeenkomen met het teken dat u opgeeft.

1. De standaardwaarde accepteren `_EMPTY_VALUE_` for **[!UICONTROL Empty attribute value constant]**.

1. Als u speciale tekens wilt insluiten die in de gegevens kunnen worden gevonden als een _escapereeks_, selecteert u de **[!UICONTROL Fields Enclosure]** selectievakje.

### Stap 3: het importbestand identificeren

![Gegevensimportbestand](./assets/data-import-file-to-import.png){width="600" zoomable="yes"}

1. Klikken **[!UICONTROL Choose File]** om het te importeren bestand te selecteren.

1. Zoek het CSV-bestand dat u wilt importeren en klik op **[!UICONTROL Open]**.

1. Voor **[!UICONTROL Images File Directory]**, voert u het relatieve pad in naar de locatie op de Commerce-server waar de geüploade afbeeldingen worden opgeslagen.

   Bijvoorbeeld: `product_images`.

   >[!NOTE]
   >
   >Vanaf de Adobe Commerce en de Magento Open Source `2.3.2` release, het pad dat is opgegeven in _[!UICONTROL Images File Directory]_schakelt voor het importeren naar de basismap van de afbeelding samengevoegd: `<Magento-root-folder>/var/import/images`. Plaats bijvoorbeeld de `product_images` in de `<Magento-root-directory>/var/import/images/product_images` map. De basismap met importimages kan worden geconfigureerd in de `\Magento\ImportExport\etc\config.xml` bestand. Als de externe opslagmodule is ingeschakeld, importeert u bestanden naar de `<remote-storage-root-directory>/var/import/images/product_images` map.

   Ga voor meer informatie over het importeren van productafbeeldingen naar [Afbeeldingen van producten importeren](data-import-product-images.md).

### Stap 4: controleer de importgegevens

1. Klik in de rechterbovenhoek op **[!UICONTROL Check Data]**.

1. Wacht even totdat het validatieproces is voltooid.

   Als de importgegevens geldig zijn, wordt het volgende bericht weergegeven:

   ![Bericht met succes - bestand is geldig](./assets/data-import-validation-message.png){width="600"}

1. Als het bestand geldig is, klikt u **[!UICONTROL Import]**.

   Als dat niet het geval is, verhelpt u elk probleem met de gegevens in het bericht en probeert u het bestand opnieuw te importeren.

1. Het importproces gaat door tot het einde van de gegevens, tenzij er een fout optreedt.

   Als een foutbericht wordt weergegeven in de resultaten van de validatie, verhelpt u het probleem in de gegevens en importeert u het bestand opnieuw.

   ![Foutbericht - URL-sleutel bestaat al](./assets/data-import-validation-error-url-key-exists.png){width="600"}

   Er verschijnt een bericht wanneer het importeren is voltooid.

## Historie importeren

De handel houdt een verslag van gegevens bij die in uw opslag zijn ingevoerd, met inbegrip van de begindatum en de tijd, de gebruiker, de uitvoeringstijd, en een verbinding aan het ingevoerde dossier. De _Uitvoeringstijd_ is de duur van het importproces.

**_De importgeschiedenis bekijken:_**

Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import History]**.

![Importgeschiedenis gegevens](./assets/data-import-history.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Standaard bevinden bestanden met importgeschiedenis zich in de `<Magento-root-directory>/var/import_history` map. Als de externe opslagmodule is ingeschakeld, bevinden de bestanden met importhistorie zich in het dialoogvenster `<remote-storage-root-directory>/import_export/import_history` map.

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL ID] | Een intern nummer dat wordt gebruikt om een overdracht aan te wijzen. |
| [!UICONTROL Start Date & Time] | Een specifieke datum en tijd waarop de overdracht heeft plaatsgevonden. |
| [!UICONTROL User] | De klant die de overdracht heeft uitgevoerd. |
| [!UICONTROL Imported file] | Koppeling voor het downloaden van het geïmporteerde bestand. |
| [!UICONTROL Error file] | Het bijbehorende foutbestand. |
| [!UICONTROL Execution Time] | Tijdsinterval van het importproces. |
| [!UICONTROL Summary] | Het aantal items dat is gemaakt, bijgewerkt en verwijderd, of het foutbericht. |

{style="table-layout:auto"}

Als u het dialoogvenster _Geïmporteerd/Fout_ bestand, klikt u op **[!UICONTROL Download]**.
