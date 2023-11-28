---
title: voorraadbronnen uitschakelen
description: Leer hoe u bronnen kunt uitschakelen en informatie kunt wijzigen, zoals de locatie en het contactpunt.
exl-id: 3fcbfa3c-8bb7-4e08-a395-9760bbd69f04
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# Bronnen uitschakelen

Om ervoor te zorgen dat alle ordergegevens behouden blijven in [!DNL Commerce], kunnen bronnen niet worden verwijderd. Bronnen, bestellingen en overbrengingen zijn rechtstreeks met elkaar verbonden. U kunt bronnen uitschakelen en informatie wijzigen, zoals de locatie en het contactpunt.

Afhankelijk van de status van uw locaties kunt u een bron uitschakelen. Een uitgeschakelde bron behoudt alle toewijzingen per voorraad en product, maar heeft geen toegang tot voorraad en bestellingen.

Wanneer een bron is uitgeschakeld:

- [!DNL Inventory Management] negeert en maakt geen lijst van de bron voor verzending of ordeverwerking.
- De voorraden hebben geen toegang tot de inventarishoeveelheden van de bron voor de geaggregeerde inventaristotalen.
- Overbrengingen van bestellingen kunnen niet worden toegewezen aan uitgeschakelde locaties.

U kunt de standaardbron niet uitschakelen. [!DNL Commerce] gebruikt deze bron voor alle nieuwe, geïmporteerde producten, voor bundelproducten en voor systeemondersteuning van derden. U kunt aangepaste bronnen op elk gewenst moment in- of uitschakelen.

Een bron instellen op `disabled` is nuttig voor de volgende situaties:

- Een winkel of opslagplaats toevoegen - Als u nieuwe winkelcentra opent of nieuwe opslagplaatsen en verzendlocaties online brengt, voegt u een bronitem toe aan de productinventaris die u met import kunt instellen en aan de potentiële voorraden kunt koppelen.
- Seizoensgebonden verzendingen - Vakanties kunnen een drukke tijd van het jaar zijn. Mogelijk wilt u de verzending beperken tot bepaalde verzendlocaties, zoals pakhuizen, om baksteen- en mortierlocaties goed te bewaren en te concentreren op lokale kopers. U kunt ook voor een beperkte tijd nieuwe verzendlocaties toevoegen om hogere verkoopsnelheden en inkomende bestellingen af te handelen.
- Een locatie sluiten - Als u een locatie sluit voor verplaatsing naar nieuwe faciliteiten of permanent, schakelt u deze uit om nieuwe verzendingen vanaf de locatie te stoppen.

## Een of meer aangepaste bronnen uitschakelen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**.

1. Schakel het selectievakje in voor elke ingeschakelde aangepaste bron die u wilt uitschakelen.

1. Klik op de knop _Handelingen_ in de linkerbovenhoek en kies **[!UICONTROL Disable]**.

   ![[!DNL Inventory Management] bronnen - Menu Handelingen](assets/inventory-source-disable.png){width="600" zoomable="yes"}

1. Klik in het bevestigingsdialoogvenster op **[!UICONTROL OK]**.

## Eén aangepaste bron in- of uitschakelen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**.

1. Een aangepaste bron zoeken en klikken **[!UICONTROL Edit]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de _Algemeen_ sectie en wijziging **[!UICONTROL Is Enabled]**:

   | Optie | Beschrijving |
   | ----- | ----- |
   | `Yes` | Bron is ingeschakeld. De hoeveelheid wordt toegevoegd aan de verkoopbare hoeveelheid. De bronlijst met het huidige aantal bij verzendopdrachten. Het Algoritme van de Selectie Bron controleert het de bron voor het verschepen. |
   | `No` | De bron is uitgeschakeld. De hoeveelheden worden niet toegevoegd aan de verkoopbare hoeveelheden. De bron wordt niet vermeld wanneer verzendopdrachten worden geplaatst. Met de verzendopties slaat u deze bron over. |

1. Klik op **[!UICONTROL Save and Close]**.
