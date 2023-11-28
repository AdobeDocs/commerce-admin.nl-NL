---
title: Kenmerksets
description: Leer hoe u kenmerken in groepen indeelt, die bepalen waar ze in de productrecord worden weergegeven.
exl-id: de0c5fa2-158c-44ff-b84d-e4904ed8aa7d
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 0%

---

# Kenmerksets

Een van de eerste stappen bij het maken van een product is het kiezen van de kenmerkset die wordt gebruikt als een sjabloon voor de productrecord. De kenmerkset bepaalt de velden die beschikbaar zijn tijdens gegevensinvoer en de waarden die naar de klant worden weergegeven.

De kenmerken zijn ingedeeld in groepen die bepalen waar ze in de productrecord worden weergegeven. Uw winkel bevat een eerste kenmerkset (ook wel _default_) die een set veelgebruikte kenmerken bevat. Als u slechts enkele kenmerken wilt toevoegen, kunt u deze toevoegen aan deze standaardkenmerkset. Als u producten verkoopt die specifieke soorten informatie vereisen, zou het beter kunnen zijn om een specifieke attributenreeks tot stand te brengen die de specifieke attributen nodig voor het product omvat.

![Kenmerksets](./assets/attribute-sets.png){width="700" zoomable="yes"}

## Een kenmerkset maken

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

1. Klik op **[!UICONTROL Add New Set]**.

   ![Kenmerkset - naam bewerken](./assets/attribute-set-new.png){width="600" zoomable="yes"}

1. Voer een **[!UICONTROL Name]** voor de kenmerkset.

1. Set **[!UICONTROL Based On]** naar een bestaand kenmerk dat is ingesteld om als sjabloon te worden gebruikt.

1. klikken **[!UICONTROL Save]**.

   Op de volgende pagina wordt het volgende weergegeven:

   - In de linkerkolom wordt de naam van de kenmerkset weergegeven. De naam is bedoeld voor interne referentie en kan zo nodig worden gewijzigd.
   - In het midden van de pagina wordt de huidige selectie van kenmerkgroepen weergegeven.
   - In de rechterkolom wordt de selectie weergegeven van kenmerken die momenteel niet zijn toegewezen aan de kenmerkset.

1. Als u een kenmerk aan de set wilt toevoegen, sleept u het kenmerk van het gereedschap **[!UICONTROL Unassigned Attributes]** aan de aangewezen omslag in **[!UICONTROL Groups]** kolom.

   >[!NOTE]
   >
   >Systeemkenmerken zijn gemarkeerd met een punt en kunnen niet uit het _[!UICONTROL Groups]_lijst. Ze kunnen echter naar een andere groep in de kenmerkset worden gesleept.

1. Klik op **[!UICONTROL Save]**.

![Kenmerkset - bewerken](./assets/attribute-set-edit.png){width="600" zoomable="yes"}

## Een kenmerkengroep maken

1. In de _[!UICONTROL Groups]_kolom de kenmerkset, klik **[!UICONTROL Add New]**.

1. Voer een **[!UICONTROL Name]** voor de nieuwe groep en klik op **[!UICONTROL OK]**.

1. Voer een van de volgende handelingen uit:

   - Slepen **[!UICONTROL Unassigned Attributes]** aan de nieuwe groep.
   - Sleep kenmerken van een andere groep naar de nieuwe groep.

   De nieuwe groep wordt een sectie van attributen in om het even welk product dat op de kenmerkreeks gebaseerd is.

## Een kenmerkset verwijderen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

1. Selecteer de kenmerkset in de lijst en open in de bewerkingsmodus.

1. Klik op **[!UICONTROL Delete]**.

1. Klik wanneer u wordt gevraagd om te bevestigen **[!UICONTROL OK]**.
