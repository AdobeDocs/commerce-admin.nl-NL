---
title: Wachtrijen voor nieuwsbrief
description: Leer hoe u nieuwsbrieven in de wachtrij kunt plaatsen voor het verzenden van meerdere batches voor nieuwsbrieven.
exl-id: bf85b3ff-3093-49a1-8a9a-d3ea71fe3f09
feature: Customers, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---

# Wachtrijen voor nieuwsbrief

Om de lading op de server te beheren, worden de nieuwsbrieven met vele abonnees verzonden in een rij van veelvoudige partijen. U kunt de nieuwsbrief rij periodiek controleren om de status te controleren, en te zien hoeveel zijn verwerkt. Eventuele problemen die zich tijdens de transmissie voordoen, worden weergegeven op het tabblad _Probleem met nieuwsbrief_ verslag.

## Een nieuwsbrief verzenden

1. Op de _Beheerder_ menu, ga naar **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Template]**.

1. Zoek in het raster de [nieuwsbrief, sjabloon](newsletter-template.md) die moet worden verzonden en stelt de **[!UICONTROL Action]** kolom naar `Queue Newsletter`.

1. Voor **[!UICONTROL Queue Date Start]** selecteert u de datum waarop de verzending moet beginnen in de kalender (![Kalenderpictogram](../assets/icon-calendar.png)).

1. Voor **[!UICONTROL Subscribers From]** selecteert u elke winkelweergave die in de e-mailballast moet worden opgenomen.

1. Voer de e-mailheadergegevens in:

   - Voer een korte beschrijving in van de nieuwsbrief voor de **[!UICONTROL Subject]** regel van de e-mailkoptekst.

   - Voer de **[!UICONTROL Sender Name]**.

   - Voor **[!UICONTROL Sender Email]**, voert u het e-mailadres van de afzender in.

     De standaardnaam en het e-mailadres van de afzender worden gespecificeerd in de configuratie.

     ![Informatie over wachtrij voor nieuwsbrief](./assets/newsletter-queue-information1.png){width="600" zoomable="yes"}

1. Voer, indien van toepassing, een notitie in in de **[!UICONTROL Message]** boven de instructies om uw abonnement op te zeggen.

   >[!NOTE]
   >
   >Verwijder niet de instructies, die in veel rechtsgebieden wettelijk vereist zijn.

1. Als u aangepaste stijlen op een nieuwsbrief wilt toepassen, voegt u deze toe aan de **[!UICONTROL Newsletter Styles]** veld.

1. Klik op **[!UICONTROL Save and Resume]**.

   De nieuwsbrief verschijnt in de rij wachtend om te worden verwerkt.

## Controleren op problemen

Op de _Beheerder_ menu, ga naar **[!UICONTROL Reports]** > _[!UICONTROL Marketing]_>**[!UICONTROL Newsletter Problem Reports]**.

## Knopbalk

| Knop | Beschrijving |
|--- |--- |
| **[!UICONTROL Back]** | Hiermee gaat u terug naar de pagina Sjablonen voor nieuwsbrief zonder wijzigingen op te slaan. |
| **[!UICONTROL Reset]** | Hiermee herstelt u eventuele niet-opgeslagen wijzigingen in het formulier met de gegevens in de wachtrij naar de vorige waarden. |
| **[!UICONTROL Preview Template]** | Hiermee opent u een voorvertoningspagina op een afzonderlijk tabblad. |
| **[!UICONTROL Save and Resume]** | Hiermee slaat u alle aangebrachte wijzigingen op. Hiermee plaatst u de nieuwsbrief in de wachtrij. |
| **[!UICONTROL Save Newsletter]** | Hiermee slaat u alle aangebrachte wijzigingen op. Hiermee plaatst u de nieuwsbrief in de wachtrij. |

{style="table-layout:auto"}

## Kolommen

| Kolom | Beschrijving |
|--- |--- |
| [!UICONTROL ID] | Een unieke numerieke id die wordt toegewezen aan elke nieuwsbrief sjabloon. |
| [!UICONTROL Queue Start] | De datum waarop de nieuwsbrief is verzonden. |
| [!UICONTROL Queue End] | De datum waarop de nieuwsbrief het verzenden beëindigde. |
| [!UICONTROL Subject] | Onderwerp van de sjabloon voor nieuwsbrieven. |
| [!UICONTROL Status] | Geeft een status van de nieuwsbrief aan. Mogelijke waarden: `Sent`, `Canceled`, `Not Sent`, `Sending`, of `Paused`. |
| [!UICONTROL Processed] | Geeft aan hoeveel nieuwsbrieven zijn verzonden. |
| [!UICONTROL Recipients] | Geeft aan hoeveel nieuwsbrieven door abonnees zijn ontvangen. |
| [!UICONTROL Actions] | **[!UICONTROL Preview]**: hiermee opent u een apart venster waarin u een voorvertoning van de sjabloon kunt weergeven. |

{style="table-layout:auto"}
