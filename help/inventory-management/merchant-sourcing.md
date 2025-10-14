---
title: Handelsgewijze aankooptypes
description: Leer over de twee brontypes die op het aantal plaatsen, of bronnen, in uw zaken worden gebaseerd.
exl-id: ec928929-5826-4504-9fd0-84256b37cb39
feature: Inventory, Products
source-git-commit: 023716935a6657b0dc2317876debe608e65bf010
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 0%

---

# Handelsgewijze aankooptypes

[!DNL Commerce] biedt ondersteuning voor [!DNL Inventory Management] voor alle grootten van bedrijven, waaronder één winkel met één website, voor een internationaal netwerk van websites, winkels, pakhuizen en verlader. Alle verkopers die Adobe Commerce of Magento Open Source gebruiken vallen in twee types op basis van het aantal plaatsen, of bronnen, in uw zaken.

- Single-source-handelaren verzenden producten van één locatie. U wordt beschouwd als een single-source handel/wijze tot u begint douanebronnen en voorraden aan uw installatie toe te voegen.

- Meerbronhandelaren verzenden producten van meer dan één locatie, zoals baksteen- en mortierwinkels, opslagplaatsen, slagschepen en distributiecentra. Nadat u aangepaste bronnen per locatie hebt toegevoegd, wordt u automatisch een leverancier van meerdere bronnen.

## Single-source-handelaren

Single-source-handelaren hebben één locatie die de voorraad in handen beheert en bestellingen uitvoert. Gewoonlijk zijn er meerdere websites (of verkoopkanalen) die producten uit dezelfde catalogus, voorraad en locatie verkopen.

U hebt bijvoorbeeld één website of een implementatie van meerdere sites met sites voor de Verenigde Staten, Duitsland, Frankrijk en Brazilië die alle producten uit één groot pakhuis halen. Deze enige bron beheert alle inventarishoeveelheden, verzendingen en retourneert, ongeacht welk verkoopkanaal de bestelling ontvangt.

Aan de slag:

- Vorm [&#x200B; globale en productmontages &#x200B;](configuration.md) voor de inventaris van uw opslag zoals nodig.

- Werk [&#x200B; Standaard Source &#x200B;](sources-manage.md) met informatie voor uw enige inventarisplaats bij. Het maken van aanvullende bronnen is niet vereist.

- Werk de [&#x200B; Standaardvoorraad &#x200B;](stocks-manage.md) bij. Zorg ervoor dat al uw websites zijn geselecteerd als verkoopkanalen. Als u nieuwe websites toevoegt, voegt [!DNL Commerce] deze automatisch toe aan de standaardvoorraad. Het is niet nodig extra bestanden te maken.

>[!NOTE]
>
>Naarmate uw bedrijf zich uitbreidt, voegt u extra bronnen en voorraden toe en werkt u uw [!DNL Inventory Management] -configuratie bij, zodat deze een multisource-leverancier wordt. Zie [&#x200B; Inventaris van de Uitbreiding en van de Herstructurering &#x200B;](expand-restructure.md) voor alle details.

## Meerbronproducten

Meerbronhandelaren beschikken over één website of een implementatie met meerdere sites en beheren de voorraad aan en voldoen orders via meerdere locaties.

U hebt bijvoorbeeld een implementatie van meerdere sites met websites voor de Verenigde Staten, Duitsland, Frankrijk en Brazilië. Uw bedrijf omvat veelvoudige pakhuizen en opslagplaatsen in deze landen en laat de verzenddiensten vallen die al inventarisvoorraad beheren en orden vervullen. Deze locaties en websites worden bronnen en bestanden in [!DNL Commerce] . U kunt een voorraad voor Noord- en Zuid-Amerika en een andere voorraad voor Europa aanmaken door websites en bronnen toe te wijzen op basis van landinstellingen en locaties. Klanten die op elke website winkelen, hebben alleen toegang tot verkoopbare voorraden van de toegewezen bronnen.

Aan de slag:

- Configureer zo nodig algemene instellingen voor de inventarisatie van uw winkel.

- Voeg [&#x200B; douanebronnen &#x200B;](sources-add.md) voor uw inventarisplaatsen toe: pakhuizen, opslag, distributiecentra, en dalingsexpediteurs.

- Voeg [&#x200B; douanevoorraden &#x200B;](stocks-add.md) voor elk gebied toe om uw websites met veelvoudige bronnen in kaart te brengen. U kunt de bronnen in elk bestand opnieuw rangschikken, zodat u ze bij het uitvoeren van uw bestellingen kunt gebruiken.

- Bronnen toewijzen aan producten en hoeveelheden per locatie toevoegen.

- Voltooi alle verdere configuraties per product voor drempelwaarden voor hoeveelheden, backorders enzovoort.
