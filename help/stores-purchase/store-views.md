---
title: Winkelweergaven
description: Leer hoe u een winkelweergave toevoegt en bewerkt.
exl-id: aa1f7f1c-a6d0-4ec2-83fe-15fb9646634a
feature: Site Management, System
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 0%

---

# Winkelweergaven

Winkelweergaven worden doorgaans gebruikt om de winkel in verschillende landinstellingen beschikbaar te maken. Klanten kunnen de taalkiezer in de koptekst van de winkel gebruiken om de winkelweergave te wijzigen.

![&#x200B; Reikwijdte - veelvoudige opslagmeningen &#x200B;](./assets/scope-multiview.svg){width="550"}

## Winkelweergave toevoegen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

   ![&#x200B; Alle opslag &#x200B;](./assets/stores-all.png){width="700" zoomable="yes"}

1. Klik op **[!UICONTROL Create Store View]** .

   ![&#x200B; creeer opslagmening &#x200B;](./assets/create-store-view.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL Store]** in op de bovenliggende opslag van deze weergave.

1. Voer een **[!UICONTROL Name]** in voor deze winkelweergave.

   De naam wordt weergegeven in de taalkiezer in de koptekst van de winkel. Bijvoorbeeld: `Spanish` .

1. Voer bij **[!UICONTROL Code]** de code in die de weergave identificeert (in kleine letters).

   Bijvoorbeeld: `spanish` .

1. Als u de weergave wilt activeren, stelt u **[!UICONTROL Status]** in op `Enabled` .

1. (Optioneel) Voer een **[!UICONTROL Sort Order]** -getal in om de volgorde te bepalen waarin deze weergave bij andere weergaven wordt weergegeven.

1. Klik op **[!UICONTROL Save Store View]**.

## Een winkelweergave bewerken

Omdat de weergavenaam wordt weergegeven in de taalkiezer, kunt u de naam van de standaardweergave wijzigen in iets beschrijvender. Het _gebied van de Naam_ is eenvoudig een etiket en kan gemakkelijk worden veranderd.

Als uw Adobe Commerce- of Magento Open Source-installatie meerdere sites of meerdere winkels heeft, wijzigt u het veld Code opslaan niet zonder te controleren of naar de waarde niet wordt verwezen in het `index.php` -bestand. Als u geen toegang hebt tot de server om het bestand te onderzoeken, vraagt u een ontwikkelaar om hulp.

| Veld | Oorspronkelijke waarde | Bijgewerkte waarde |
| ----- | -------------- | ------------- |
| [!UICONTROL Name] | `Default Store View` | `English` |
| [!UICONTROL Code] | `default` | `english` |

{style="table-layout:auto"}

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. Klik in de kolom _[!UICONTROL Store View]_&#x200B;van het raster op de naam van de weergave die u wilt bewerken.

   Wanneer u de standaardweergave bewerkt, zijn de velden _[!UICONTROL Store]_&#x200B;en&#x200B;_[!UICONTROL Status]_ niet beschikbaar.

   ![&#x200B; mening van de Opslag - geef standaardmening uit &#x200B;](./assets/edit-store-view-info.png){width="600" zoomable="yes"}

1. Werk indien nodig de volgende velden bij:

   - **[!UICONTROL Store]** (alleen niet-standaardweergave)
   - **[!UICONTROL Name]**
   - **[!UICONTROL Code]** (alleen als deze methode niet wordt gebruikt in `index.php`)
   - **[!UICONTROL Status]** (alleen niet-standaardweergave)
   - **[!UICONTROL Sort Order]**

1. Klik op **[!UICONTROL Save Store View]**.
