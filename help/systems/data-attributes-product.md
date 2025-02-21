---
title: Referentie productgegevenskenmerken
description: Gebruik deze referentie van productgegevenskenmerken wanneer u werkt met het importeren en exporteren van productgegevens.
exl-id: 9ffa4d1f-cbf8-4a08-bb79-33f21e698a74
feature: Products, Attributes
source-git-commit: c1f797da417bfdf24b537f8c59f954df58dac11a
workflow-type: tm+mt
source-wordcount: '2473'
ht-degree: 0%

---

# Referentie productgegevenskenmerken

De volgende tabel bevat een lijst met de kenmerken van een typisch exportproduct, in de standaardvolgorde waarin deze worden weergegeven. Elk kenmerk wordt in het CSV-bestand weergegeven als een kolom en productrecords worden weergegeven als rijen. Kolommen die met een onderstrepingsteken beginnen, bevatten servicegegevens zoals eigenschappen of optiewaarden voor complexe gegevens. U kunt [ uitvoeren ](data-export.md) een product van uw catalogus, om te zien hoe elk attribuut in de gegevens wordt vertegenwoordigd.

Voor de installatie die wordt gebruikt om deze gegevens te exporteren, zijn de voorbeeldgegevens geïnstalleerd. Er zijn twee websites en verschillende winkelweergaven. Hoewel deze lijst alle kolommen bevat die doorgaans worden geëxporteerd, is `sku` de enige vereiste waarde. Als u gegevens wilt importeren, kunt u alleen de kolommen met wijzigingen opnemen. De `sku` moet de eerste kolom zijn, maar de volgorde van de overige kenmerken is niet van belang.

## Eenvoudige CSV-bestandsstructuur van product

| Kenmerk | Beschrijving |
|--- |--- |
| `sku` | (Vereist) De voorraadbewaareenheid is een unieke alfanumerieke identificatiecode die wordt gebruikt om de inventaris bij te houden. Een SKU kan maximaal 64 tekens lang zijn. Bijvoorbeeld: `sku123`<br/>**_Nota:_**Een SKU langer dan 64 karakters veroorzaakt invoer om te ontbreken. |
| `store_view_code` | Hiermee geeft u de specifieke opmaakweergaven aan van de locatie waar het product beschikbaar is. Als dit leeg is, is het product beschikbaar in de standaardwinkelweergave. Bijvoorbeeld: `storeview1`, `english`, `spanish` |
| `attribute_set_code` | Hiermee wijst u het product toe aan een specifieke kenmerkset of productsjabloon, afhankelijk van het producttype. Nadat het product is gemaakt, kan de kenmerkset niet meer worden gewijzigd. Bijvoorbeeld: `default` |
| `product_type` | Geeft het type product aan. Waarden:<br/>`simple` — Materiële goederen die gewoonlijk als afzonderlijke eenheden of in vaste hoeveelheden worden verkocht.<br/>`grouped` — Een groep afzonderlijke producten die als een set wordt verkocht.<br/>`configurable` — Een product met meerdere opties die de klant moet selecteren voordat hij een aankoop doet. De inventaris kan voor elke reeks variaties worden beheerd omdat zij een afzonderlijk product met verschillende SKU vertegenwoordigen. Een combinatie van kleur en grootte voor een configureerbaar product is bijvoorbeeld gekoppeld aan een specifieke SKU in de catalogus.<br/>`virtual` — Een niet-tastbaar product waarvoor geen verzending vereist is en dat niet in voorraad wordt gehouden. Voorbeelden zijn services, abonnementen en abonnementen.<br/>`bundle` — Een aanpasbare productset met eenvoudige producten die samen worden verkocht. |
| `categories` | Hiermee geeft u elke categorie aan die aan het product is toegewezen. Afzonderlijke categorieën en subcategorieën met een slash. Als u meerdere categoriepaden wilt aangeven, scheidt u elk pad met een verticale balk \| symbool. Bijvoorbeeld: `Default Category/Gear\|Default Category/Gear/Bags` |
| `product_websites` | De websitecode van elke website waar het product beschikbaar is. Een enkel product kan aan meerdere websites worden toegewezen of tot één worden beperkt. Als u meerdere websites opgeeft, scheidt u deze met een komma en zonder spatie. Bijvoorbeeld: `base` of `base,website2` |
| `name` | De productnaam wordt in alle productaanbiedingen weergegeven en is de naam die klanten gebruiken om het product te identificeren. |
| `description` | De productbeschrijving bevat gedetailleerde informatie over het product, waaronder eenvoudige HTML-tags. |
| `short_description` | Het gebruik van de korte productbeschrijving is afhankelijk van het thema. Het wordt mogelijk in productaanbiedingen weergegeven en wordt soms gebruikt in RSS-voederaanbiedingen die naar winkelsites worden gestuurd. |
| `weight` | Het gewicht van het afzonderlijke product. Het werkelijke productgewicht wordt door de vervoerder bepaald op het tijdstip van verzending. |
| product_online | Hiermee wordt bepaald of het product beschikbaar is voor verkoop in de winkel. Waarden:<br/>`1` — (ja) het product wordt toegelaten, en beschikbaar voor verkoop.<br/>`2` — (Nee) Het product is uitgeschakeld en niet te koop. |
| `tax_class_name` | De naam van de belastingklasse die aan dit product is gekoppeld. |
| `visibility` | Hiermee bepaalt u of het product zichtbaar is in de catalogus en beschikbaar wordt gemaakt voor zoekopdrachten. Waarden:<br/>`Not Visible Individually` — Het product is niet opgenomen in productlijsten, hoewel het beschikbaar kan zijn als een variant van een ander product.<br/>`Catalog` — Het product wordt in alle cataloguslijsten weergegeven.<br/>`Search` —Het product is beschikbaar voor zoekbewerkingen.<br/>`Catalog, Search` — Het product is opgenomen in cataloguslijsten en is ook beschikbaar voor zoekopdrachten. |
| `price` | De prijs die het product in je winkel te koop wordt aangeboden. |
| `special_price` | De gedisconteerde prijs van het product gedurende het opgegeven datumbereik. |
| `special_price_from_date` | De begindatum van de periode waarin de bijzondere prijs van kracht is. |
| `special_price_to_date` | De laatste datum van de periode waarin de bijzondere prijs van kracht is. |
| `url_key` | Het gedeelte van de URL dat het product identificeert. De standaardwaarde is gebaseerd op de productnaam. Bijvoorbeeld: `product-name` |
| save_rewrites_history | Als de waarde `1` wordt voorzien van een nieuwe `url_key` , wordt een nieuwe URL van 301 gegenereerd zodat de oude URL wordt omgeleid naar de nieuwe URL. |
| `meta_title` | De titel van de meta verschijnt in de titelbar en het lusje van browser en onderzoeksresultaten lijsten. De titel van de meta zou uniek aan het product moeten zijn, high-value sleutelwoorden omvatten, en minder dan 70 karakters in lengte zijn. |
| `meta_keywords` | Meta-trefwoorden zijn alleen zichtbaar voor zoekmachines en worden door sommige zoekprogramma&#39;s genegeerd. Kies trefwoorden met een hoge waarde, gescheiden door een komma. Bijvoorbeeld: `keyword1`, `keyword2`, `keyword3` |
| `meta_description` | Meta-beschrijvingen bieden een kort overzicht van het product voor aanbiedingen met zoekresultaten. In het ideale geval moet een metabeschrijving tussen 150 en 160 tekens lang zijn, hoewel het veld maximaal 255 tekens accepteert. |
| `base_image` | Het relatieve pad voor de hoofdafbeelding op de productpagina. Commerce slaat bestanden intern op in een alfabetische mapstructuur. U kunt de exacte locatie van elke afbeelding in de geëxporteerde gegevens zien. Bijvoorbeeld: `/sample_data/m/b/mb01-blue-0.jpg`<br/> om een nieuw beeld te uploaden of over een bestaand beeld te schrijven, ga het dossier in - naam, voorafgegaan door een voorwaartse schuine streep. Bijvoorbeeld: `/image.jpg` |
| `base_image_label` | Het label dat aan de basisafbeelding is gekoppeld. |
| `small_image` | De bestandsnaam van de kleine afbeelding die wordt gebruikt op cataloguspagina&#39;s, voorafgegaan door een slash. Bijvoorbeeld: `/image.jpg` |
| `small_image_label` | Het label dat aan de kleine afbeelding is gekoppeld. Bijvoorbeeld: `Small Image 1` , `Small Image 2` |
| `thumbnail_image` | De bestandsnamen van miniatuurafbeeldingen die in de galerie op de productpagina worden weergegeven, voorafgegaan door een slash. Bijvoorbeeld: `/image.jpg` |
| `thumbnail_image_label` | Het label dat aan miniatuurafbeeldingen is gekoppeld. Bijvoorbeeld: `Thumbnail 1` , `Thumbnail 2` |
| `created_at` | Geeft de datum aan waarop het product is gemaakt. De datum wordt automatisch gegenereerd wanneer het product wordt gemaakt, maar kan later worden bewerkt. |
| `updated_at` | Geeft de datum aan waarop het product voor het laatst is bijgewerkt. |
| `new_from_date` | Hiermee geeft u de datum &quot;van&quot; op voor nieuwe productaanbiedingen en bepaalt u of het product als een nieuw product wordt aangeboden. |
| `new_to_date` | Hiermee geeft u de datum op waarop het product moet worden aangeboden voor nieuwe producten en bepaalt u of het product als een nieuw product wordt aangeboden. |
| `display_product_options_in` | Als het product meerdere opties heeft, bepaalt u waar deze op de productpagina worden weergegeven. Waarden: Kolom productinformatie / Blok na kolom Info |
| `map_price` | De minimale geadverteerde prijs van het product. (Wordt alleen weergegeven als MAP is ingeschakeld.) |
| `msrp_price` | De door de fabrikant voorgestelde detailhandelsprijs voor het product. (Wordt alleen weergegeven als MAP is ingeschakeld.) |
| `map_enabled` | Hiermee bepaalt u of Minimale geadverteerde prijs is ingeschakeld in de configuratie. Waarden:<br/>`1` — (Ja) MAP is ingeschakeld.<br/>`0` (of leeg) — (Geen) KAART is niet ingeschakeld. |
| `gift_message_available` | Hiermee bepaalt u of een cadeaubericht kan worden opgenomen in de productaankoop. Waarden:<br/>`1` — (Ja) De optie om een geschenkbericht op te nemen wordt voorgesteld aan de klant.<br/>`0` (of leeg) — (Nee) De optie om een cadeaubericht op te nemen wordt niet aan de klant getoond. |
| `custom_design` | Hier worden de beschikbare thema&#39;s weergegeven die op de productpagina kunnen worden toegepast. |
| `custom_design_from` | Hiermee geeft u de begindatum op waarop het geselecteerde thema wordt toegepast op de productpagina. |
| `custom_design_to` | Hiermee geeft u de einddatum op waarop het geselecteerde thema wordt toegepast op de productpagina. |
| `custom_layout_update` | Aanvullende XML-code die wordt toegepast als een lay-outupdate op de productpagina. |
| `page_layout` | Bepaalt de pagina-indeling van de productpagina. Waarden:<br/>`No layout updates` — De paginalay-out wordt niet gewijzigd.<br/>`1 column` — Hiermee past u een lay-out van één kolom toe op de productpagina.<br/>`2 columns with left bar` — Hiermee past u een lay-out met twee kolommen en een linkerzijbalk toe op de productpagina.<br/>`2 columns with right bar` — Hiermee past u een lay-out met twee kolommen en een rechterzijbalk toe op de productpagina.<br/>`3 columns` — Hiermee past u een indeling met drie kolommen toe op de productpagina.<br/>`empty` — Hiermee wordt een lege lay-out toegepast op de productpagina. |
| `product_options_container` | Als het product meerdere opties heeft, bepaalt u waar deze op de productpagina worden weergegeven. Waarden: Kolom productinformatie / Blok na kolom Info |
| `msrp_display_actual_price_type` | Hiermee bepaalt u waar de werkelijke prijs van een product zichtbaar is voor de klant. Waarden:<br/>`In Cart` — Geeft de werkelijke productprijs weer in het winkelwagentje.<br/>`Before Order Confirmation` — Geeft de werkelijke productprijs weer aan het einde van het afrekenproces, vlak voordat de bestelling wordt bevestigd.<br/>`On Gesture` — Toont de daadwerkelijke productprijs in popup wanneer de klant _klikt voor prijs_ of _wat dit is?_ . |
| `country_of_manufacture` | Identificeert het land waar het product is vervaardigd. |
| `additional_attributes` | Extra kenmerken die voor het product zijn gemaakt. Bijvoorbeeld: <br/>`has_options=0,required_options=0color=Black,has_options=0,required_options=0,size_general=XS` |
| `qty` | De hoeveelheid product die momenteel in voorraad is. |
| `out_of_stock_qty` | Het voorraadniveau dat bepaalt welk product uit voorraad is. |
| `use_config_min_qty` | Hiermee wordt bepaald of de standaardwaarde in de configuratie wordt gebruikt en of deze overeenkomt met het selectievakje Configuratie-instellingen gebruiken. Waarden:<br/>`1` — (ja) de standaardconfiguratie die voor de waarde van dit attribuut plaatst wordt gebruikt.<br/>`0` (of leeg) — (Geen) De standaardconfiguratie kan voor de waarde van dit kenmerk worden overschreven. |
| `is_qty_decimal` | Bepaalt of het kenmerk qty een decimale waarde heeft. Waarden:<br/>`1` — (ja) de waarde van het attribuut qty is een decimale waarde.<br/>`0` (of leeg) — (Nee) De waarde van het kenmerk qty is een geheel getal (geheel getal). |
| `allow_backorders` | Hiermee bepaalt u of in uw winkel backorders zijn toegestaan en hoe deze worden beheerd. |
| `use_config_backorders` | Hiermee wordt bepaald of de standaardconfiguratie-instelling voor backorders wordt gebruikt en of deze overeenkomt met de status van het selectievakje Configuratie-instellingen gebruiken. Waarden:<br/>`1` — (ja) de waarde van het attribuut qty is een decimale waarde.<br/>`0` (of leeg) — (Nee) De waarde van het kenmerk qty is een geheel getal (geheel getal). |
| `min_cart_qty` | Hiermee geeft u de minimale hoeveelheid van het item op die in één bestelling kan worden aangeschaft. |
| `use_config_min_sale_qty` | Hiermee wordt bepaald of de standaardconfiguratie-instelling voor de minimale hoeveelheid wordt gebruikt. Deze instelling komt overeen met de status van het selectievakje Configuratie-instellingen gebruiken. Waarden:<br/>`1` — (ja) <br/>`0` (of leeg) — (Geen) |
| `max_cart_qty` | Hiermee geeft u de maximale hoeveelheid van het product op die in één bestelling kan worden aangeschaft. |
| `use_config_max_sale_qty` | Hiermee wordt bepaald of de standaardconfiguratie-instelling voor de maximale hoeveelheid wordt gebruikt. Deze instelling komt overeen met de status van het selectievakje Configuratie-instellingen gebruiken. Waarden:<br/>`1` — (ja) <br/>`0` (of leeg) — (Geen) |
| `is_in_stock` | Geeft aan of het product in voorraad is. |
| `notify_on_stock_below` | Specificeert het voorraadniveau dat een _uit voorraad_ bericht teweegbrengt. |
| `use_config_notify_stock_qty` | Hiermee wordt bepaald of de standaardconfiguratie-instelling wordt gebruikt om meldingen op voorraadniveau te activeren. Deze instelling komt overeen met de status van het selectievakje Configuratie-instellingen gebruiken. Waarden:<br/>`1` — (ja) <br/>`0` (of leeg) — (Geen) |
| `manage_stock` | Hiermee bepaalt u of voorraadbeheer wordt gebruikt voor het beheer van het product. Waarden:<br/>`1` — (ja) activeert volledige inventariscontrole om voorraadniveaus van het product te beheren.<br/>`0` (of leeg) — (Nee) Het systeem houdt niet bij hoeveel items momenteel in voorraad zijn. |
| `use_config_manage_stock` | Hiermee wordt bepaald of de standaardconfiguratie-instelling voor het beheer van de voorraad wordt gebruikt en of deze overeenkomt met de status van het selectievakje Configuratie-instellingen gebruiken. Waarden:<br/>`1` — (ja) <br/>`0` (of leeg) — (Geen) |
| `use_config_qty_increments` | Hiermee wordt bepaald of de standaardconfiguratie-instelling voor de toename van het aantal wordt gebruikt en of deze overeenkomt met de status van het selectievakje Configuratie-instellingen gebruiken. Waarden:<br/>`1` — (ja) <br/>`0` (of leeg) — (Geen) |
| `qty_increments` | Hiermee wordt het aantal producten vastgesteld waaruit een verhoging van de hoeveelheid bestaat. |
| `use_config_enable_qty_inc` | Hiermee wordt bepaald of de standaardconfiguratie-instelling voor het inschakelen van kwantitatieve toenamen wordt gebruikt. Deze instelling komt overeen met de status van het selectievakje Configuratie-instellingen gebruiken. Waarden:<br/>`1` — (ja) <br/>`0` (of leeg) — (Geen) |
| `enable_qty_increments` | Hiermee bepaalt u of toename van de hoeveelheid is ingeschakeld voor het product. |
| `is_decimal_divided` | Hiermee wordt bepaald of onderdelen van het product afzonderlijk kunnen worden verzonden. Opties: `Yes` / `No` |
| `website_id` | Voor installaties met meerdere websites, identificeert u een specifieke website waar het product beschikbaar is. Als dit leeg is, is het product beschikbaar op alle websites. |
| `related_skus` | Hiermee geeft u de SKU weer van elk product dat is geïdentificeerd als een verwant product. Bijvoorbeeld: `24-WG080,24-UG03,24-UG01,24-UG02` |
| `related_position` | Bepaalt de positie (soortorde) van SKUs die als Verwante Producten in de related_skuskolom worden vermeld. Bijvoorbeeld: `1,2,3,4` |
| `crosssell_skus` | Vermeldt de SKU van elk product dat als cross-sell is geïdentificeerd. |
| `crosssell_position` | Bepaalt de positie (sorteervolgorde) van de SKU&#39;s die als Cross-sell Producten in de kolom `crosssell_skus` worden vermeld. |
| `upsell_skus` | Hiermee geeft u de SKU weer van elk product dat is geïdentificeerd als een Up-verkoop. |
| `upsell_position` | Hiermee bepaalt u de positie (sorteervolgorde) van de SKU&#39;s die als up-sell-producten in de kolom `upsell_skus` worden vermeld. |
| `additional_images` | De bestandsnamen van extra afbeeldingen die aan het product moeten worden gekoppeld, voorafgegaan door een slash. Bijvoorbeeld: `/image.jpg` |
| `additional_image_labels` | De labels die aan extra afbeeldingen zijn gekoppeld. Bijvoorbeeld: `Label 1` , `Label 2` |
| `custom_options` | Hiermee geeft u de eigenschappen en waarden op die aan elke aangepaste optie zijn toegewezen. Bijvoorbeeld: <br/>`name=Color, type=drop_down, required=1, price= price_type=fixed, sku=, option_title=Black|name=Color, type=drop_down, required=1, price=, price_type=fixed, sku=, option_title=White` |

{style="table-layout:auto"}

## Servicegegevens voor productvariaties

| Kenmerk | Beschrijving | Van toepassing op |
|--- |--- | --- |
| `_super_products_sku` | De gegenereerde SKU voor een configureerbare productvariatie. Bijvoorbeeld: WB03-XS-Green | Configureerbare producten |
| `_super_attribute_code` | De kenmerkcode van een configureerbare productvariatie. Bijvoorbeeld: kleur | Configureerbare producten |
| `_super_attribute_option` | De waarde van een configureerbare productvariatie. Bijvoorbeeld: groen | Configureerbare producten |
| `_super_attribute_price_corr` | Een prijsaanpassing die aan een configureerbare productvariatie wordt geassocieerd. | Configureerbare producten |
| `_associated_sku` | De SKU van een product dat met een gegroepeerd product wordt geassocieerd. | Gegroepeerde Producten <br/> Bundel Producten |
| `_associated_default_qty` | Hiermee bepaalt u de hoeveelheid van het bijbehorende product die wordt opgenomen. | De configureerbare Producten <br/> Gegroepeerde Producten <br/> Bundel Producten |
| `_associated_position` | Bepaalt de positie van het bijbehorende product wanneer vermeld met andere bijbehorende producten. | De configureerbare Producten <br/> Gegroepeerde Producten <br/> Bundel Producten |

{style="table-layout:auto"}

## Complexe productgegevenskenmerken

De term complexe gegevens verwijst naar de gegevens die zijn gekoppeld aan meerdere productopties. De volgende productsoorten gebruiken gegevens die uit afzonderlijke producten voortkomen om productvariaties en veelvoudige opties tot stand te brengen.

- [Configureerbaar](../catalog/product-create-configurable.md)
- [Gegroepeerd](../catalog/product-create-grouped.md)
- [Bundel](../catalog/product-create-bundle.md)

Als u een configureerbaar product exporteert, vindt u de standaardkenmerken van een eenvoudig product plus de aanvullende kenmerken die nodig zijn voor het beheer van complexe gegevens.

![ Configureerbaar product - uitgevoerde gegevens ](./assets/data-exported-configurable-product.png){width="600" zoomable="yes"}

### Configureerbare producten

| Kenmerk | Beschrijving |
|--- |--- |
| `configurable_variation_labels` | Labels die productvariaties identificeren. Bijvoorbeeld: `Choose Color:` of `Choose Size:` |
| `configurable_variations` | Beschrijft de waarden verbonden aan een productvariatie. Bijvoorbeeld: `sku=sku-red xs,color=red,size=xs,price=10.99,display=1,image=/pub/media/import/image1.png|sku=sku-red-m,color=red,size=m,price=20.88,display=1,image=/pub/media/import/image2.png` |

{style="table-layout:auto"}

### Gegroepeerde producten

| Kenmerk | Beschrijving |
|--- |--- |
| `associated_skus` | Identificeert SKUs van de individuele producten die de groep vormen. |

{style="table-layout:auto"}

### Bundelproducten

| Kenmerk | Beschrijving |
|--- |--- |
| `bundle_price_type` | Hiermee wordt bepaald of de prijs van een bundelitem vast of dynamisch is. |
| `bundle_sku_type` | Bepaalt als elk punt een variabele, dynamische SKU wordt toegewezen, of als vaste SKU voor de bundel wordt gebruikt. Opties: vast / dynamisch |
| `bundle_weight_type` | Hiermee wordt bepaald of het gewicht van een bundelitem variabel of vast is. |
| `bundle_values` | Beschrijft onderwijzen waarde verbonden aan een bundeloptie. Bijvoorbeeld: `name=Bundle Option One,type=dropdown; required=1, sku=sku-option2,price=10, price_type=fixed` |

{style="table-layout:auto"}

## Geavanceerde prijskenmerken

Met de geavanceerde functie Prijs importeren/exporteren kunt u snel prijsinformatie voor productgroepen en laagprijzen bijwerken. Het proces om [ in te voeren ](data-import.md) en [ uitvoer ](data-export.md) geavanceerde prijsgegevens is het zelfde als een ander entiteitstype. Het CSV-bestand met voorbeelden bevat niveau- en groepsprijzen voor elk producttype dat geavanceerde prijzen ondersteunt. Het wijzigen van geavanceerde prijzen heeft geen invloed op de rest van de productrecord.

![ de uitvoergegevens van het Voorbeeld - geavanceerde tarifering ](./assets/data-advanced-pricing-export-sample.png){width="600" zoomable="yes"}

| Kenmerk | Beschrijving |
|--- |--- |
| `sku` | (Vereist) De voorraadbewaareenheid is een unieke alfanumerieke identificatiecode die wordt gebruikt om de inventaris bij te houden. Een SKU kan maximaal 64 tekens lang zijn. Bijvoorbeeld: `sku123`<br/>**_Nota:_**Een SKU langer dan 64 karakters veroorzaakt invoer om te ontbreken. |
| `tier_price_website` | De [ websitecode ](../stores-purchase/stores.md#add-websites) identificeert elke website waar de rij tarifering beschikbaar is. Bijvoorbeeld: `-  website1 -  All Websites [USD]` |
| `tier_price_customer` | Identificeert de [ groepen van klanten ](../customers/customer-groups.md) waar de rij tarifering beschikbaar is. Bijvoorbeeld: `-  ALL GROUPS -  NOT LOGGED IN -  General -  Wholesale -  Retailer` |
| `tier_price_customer_group` | Identificeert de klantengroepen waar de rijprijs beschikbaar is. Bijvoorbeeld: `-  ALL GROUPS -  NOT LOGGED IN -  General -  Wholesale -  Retailer` |
| `tier_price_qty` | De hoeveelheid van het product die moet worden besteld om de korting op de tier-prijs te ontvangen. |
| `tier_price` | De gedisconteerde tier-prijs van het product. Voor [ bundelproducten ](../catalog/product-create-bundle.md), wordt de laagprijs berekend als percentage. |
| `group_price_website` | De [ websitecode ](../stores-purchase/stores.md#add-websites) van elke website waar de groepsprijzen beschikbaar zijn. Als u meerdere websites opgeeft, scheidt u deze met een komma en zonder spatie. Bijvoorbeeld: `-  website1 -  All Websites [USD]` |
| `group_price_customer_group` | Identificeert de groepen van klanten waar de groepsprijzen beschikbaar zijn. Bijvoorbeeld: `-  NOT LOGGED IN -  General -  Wholesale -  Retailer` |
| `group_price` | De gedisconteerde groepsprijs van het product. Voor [ bundelproducten ](../catalog/product-create-bundle.md), wordt de groepsprijs berekend als percentage. |

{style="table-layout:auto"}
