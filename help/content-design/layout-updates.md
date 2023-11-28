---
title: Layout-updates
description: Leer hoe u layout-updates kunt gebruiken om de lay-out van een pagina aan te passen.
exl-id: e2d8261f-cae1-4bd4-a047-f861dd7ca14e
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '1007'
ht-degree: 0%

---

# Layout-updates

Voordat u begint te werken met aangepaste layoutupdates, is het belangrijk dat u begrijpt hoe de pagina&#39;s van uw winkel zijn samengesteld en wat het verschil is tussen de termen *layout* en *layout bijwerken*. Layout verwijst naar de visuele en structurele samenstelling van de pagina. Layout bijwerken verwijst naar een specifieke set XML-instructies die de manier waarop de pagina wordt samengesteld kan overschrijven of aanpassen.

De XML-indeling van uw [!DNL Commerce] store is een hiërarchische structuur van containers en blokken. Sommige elementen worden op elke pagina weergegeven en andere alleen op specifieke pagina&#39;s. Zie voor meer informatie over lay-out, containers en blokken de [Overzicht van indelingen](https://developer.adobe.com/commerce/frontend-core/guide/layouts/) in de _Frontend Developer Guide_.

De [Widget](widgets.md) is een gemakkelijke manier om een bestaand gereedschap toe te voegen [inhoudblok](blocks.md) op de standaardlay-out van een pagina. Voor geavanceerdere updates moet u de updatecode van de XML-indeling opslaan op de server en het bestand vervolgens verwijzen als een aangepaste update van de layout van de beheerder. Voor een overzicht van het proces raadpleegt u [Layout-updates gebruiken](layout-updates.md#place-a-block-using-layout-updates).

In het volgende diagram zijn de namen die naar containers verwijzen zwart en de bloktypen, of blokklassenpaden, blauw.

![Standaardschema voor bloklay-out](./assets/page-layout-default.png){width="500" zoomable="yes"}

| Bloktype | Beschrijving |
|--- |--- |
| `page/html` | De naam van dit blok is `root` en het is een van de weinige basisblokken in de layout . U kunt ook uw eigen blok maken en dit een naam geven `root`, de standaardnaam voor blokken van dit type. Er kan slechts één blok van dit type per pagina zijn. |
| `page/html_head` | De bloknaam is `head` en het is een onderliggend element van het hoofdblok. Er kan slechts één blok van dit type per pagina zijn en het mag niet worden verwijderd. |
| `page/html_notices` | De bloknaam is `global_notices` en het is een onderliggend element van het hoofdblok. Als dit blok uit de lay-out wordt verwijderd, verschijnen de globale berichten niet op de pagina. Er kan slechts één blok van dit type per pagina zijn. |
| `page/html_header` | De bloknaam is `header` en het is een onderliggend element van het hoofdblok. Dit blok komt overeen met de visuele koptekst boven aan de pagina en bevat verschillende standaardblokken. Er kan slechts één blok van dit type per pagina zijn en het mag niet worden verwijderd. |
| `page/html_wrapper` | Hoewel dit blok is opgenomen in de standaardlay-out, is het afgekeurd en is het alleen opgenomen om achterwaartse compatibiliteit te garanderen. Gebruik geen blokken van dit type. |
| `page/html_breadcrumbs` | De naam van dit blok is `breadcrumbs` en het is een onderliggend element van het headerblok. In dit blok worden broodkruimels voor de huidige pagina weergegeven. Er kan slechts één blok van dit type per pagina zijn. |
| `page/html_footer` | De bloknaam is `footer` en het is een onderliggend element van het hoofdblok. Het voettekstblok komt overeen met de visuele voettekst onder aan de pagina en bevat verschillende standaardblokken. Er kan slechts één blok van dit type per pagina zijn en het mag niet worden verwijderd. |
| `page/template_links` | De standaardlay-out bevat twee blokken van dit type. De `top.links` blok is een onderliggend element van het headerblok en komt overeen met het bovenste navigatiemenu. De `footer_links` blok is een onderliggend element van het voettekstblok en komt overeen met het onderste navigatiemenu. <br/><br/>**_Opmerking:_**U kunt de sjabloonkoppelingen bewerken, zoals in de voorbeelden wordt getoond. |
| `page/switch` | Een standaardlay-out bevat twee blokken van dit type. De `store_language` block is een onderliggend element van het headerblok en komt overeen met de topletaalswitch. De `store_switcher` blok is een onderliggend element van het voettekstblok en komt overeen met de bottom store-switch. |
| kern/berichten | Een standaardlay-out bevat twee blokken van dit type. De `global_messages` blok toont globale berichten. De `messages` blok wordt gebruikt om alle andere berichten te tonen. Als u deze blokken verwijdert, ziet de klant geen berichten. |
| `core/text_list` | Dit type blok wordt overal gebruikt [!DNL Commerce] als plaatsaanduiding voor het renderen van onderliggende blokken. |
| `core/profiler` | Er is slechts één instantie van dit type blok per pagina. Het wordt gebruikt voor de interne [!DNL Commerce] profiler en mag niet voor andere doeleinden worden gebruikt. |

{style="table-layout:auto"}

## Een blok plaatsen met layoutupdates

[Layout-updates](layout-updates.md) kunt u de indeling van een pagina aanpassen. Layout-updates bieden meer flexibiliteit dan een [widget](widgets.md), maar hebt wel toegang tot de server en een basiskennis van XML nodig.

In de volgende stappen wordt getoond hoe u een lay-outupdate kunt gebruiken om een blok op een pagina te plaatsen. Zie voor specifieke voorbeelden en Help bij syntaxis [Algemene aanpassingstaken voor de layout](https://developer.adobe.com/commerce/frontend-core/guide/layouts/) in de _Frontend Developer Guide_.

### Stap 1: Maak het blok

1. Maak de [blok](block-add.md) die u wilt plaatsen.

1. Neem nota van het `block_id`, omdat deze wordt gebruikt in de instructies voor het bijwerken van de layout.

### Stap 2: De layout-update in XML samenstellen

1. Stel de indelingsinstructies in XML samen om [Verwijzen naar een CMS-blok](https://developer.adobe.com/commerce/frontend-core/guide/layouts/xml-manage/).

1. Sla de [indelingsinstructies](https://developer.adobe.com/commerce/frontend-core/guide/layouts/xml-instructions/) op de server in de lay-outmap waarin XML-bestanden voor het thema worden opgeslagen.

   Bijvoorbeeld:

   `<theme_dir>/<Namespace>_<Module>/layout`

   De lay-outgreep is de bestandsnaam die begint met `cms_page_view_selectable_`, gevolgd door de URL-sleutel van de CMS-pagina, de optie voor het bijwerken van de layout en de `xml` achtervoegsel bestand. In het volgende voorbeeld: `customer-service` de URL-sleutel van de pagina is, en `ChatTool` Dit is de optie die u selecteert om de layout-update toe te passen op de pagina.

   `cms_page_view_selectable_`&lt;`customer-service`>`_`&lt;`ChatTool`>`.xml`

   | Element | Beschrijving |
   |--- |--- |
   | CMS-pagina-id | De URL-sleutel van de pagina met een slash (`/`) vervangen door een onderstrepingsteken (`_`). |
   | Naam van update layout | De optie waarvoor _Update voor aangepaste layout_. |

   {style="table-layout:auto"}

### Stap 3: Verwijs naar de layout-update van de pagina

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Zoek de pagina waar u het blok wilt plaatsen en open het in uitgeven wijze.

1. Omlaag schuiven en uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Design]** sectie.

1. Als u alle beschikbare layout-updates wilt weergeven die aan de pagina zijn gekoppeld, klikt u op de knop **[!UICONTROL Custom Layout Update]** -menu.

   ![Update-lijst voor aangepaste layout](./assets/page-design-custom-layout-update.png){width="400" zoomable="yes"}

1. Selecteer de layout-update die u op de pagina wilt toepassen.

### Stap 4: De cache opslaan en vernieuwen

1. Klik op **[!UICONTROL Save & Close]**.

1. Klik in het bericht boven aan de werkruimte op **[!UICONTROL Cache Management]** en vernieuw alle ongeldige cacheitems.
