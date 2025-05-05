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

Om de lading op de server te beheren, worden de nieuwsbrieven met vele abonnees verzonden in een rij van veelvoudige partijen. U kunt de nieuwsbrief rij periodiek controleren om de status te controleren, en te zien hoeveel zijn verwerkt. Om het even welke problemen die tijdens transmissie voorkomen verschijnen op het _1&rbrace; rapport van het Probleem van de Nieuwsbrief &lbrace;._

## Een nieuwsbrief verzenden

1. Voor het _Admin_ menu, ga **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Template]**.

1. In het net, vind het [ nieuwsbrief malplaatje ](newsletter-template.md) dat moet worden verzonden en de **[!UICONTROL Action]** kolom plaatsen aan `Queue Newsletter`.

1. Voor **[!UICONTROL Queue Date Start]**, selecteer de datum dat de transmissie van de kalender moet beginnen (![ pictogram van de Kalender ](../assets/icon-calendar.png)).

1. Selecteer voor **[!UICONTROL Subscribers From]** elke winkelweergave die in de e-mailballast moet worden opgenomen.

1. Voer de e-mailheadergegevens in:

   - Voer een korte beschrijving van de nieuwsbrief in voor de regel **[!UICONTROL Subject]** van de e-mailkoptekst.

   - Voer de **[!UICONTROL Sender Name]** in.

   - Voer bij **[!UICONTROL Sender Email]** het e-mailadres van de afzender in.

     De standaardnaam en het e-mailadres van de afzender worden gespecificeerd in de configuratie.

     ![ de rijinformatie van de de rij van de Nieuwsbrief ](./assets/newsletter-queue-information1.png){width="600" zoomable="yes"}

1. Voer, indien van toepassing, een opmerking in het vak **[!UICONTROL Message]** boven de instructies om het abonnement op te zeggen.

   >[!NOTE]
   >
   >Verwijder niet de instructies, die in veel rechtsgebieden wettelijk vereist zijn.

1. Als u aangepaste stijlen op een nieuwsbrief wilt toepassen, voegt u deze toe aan het veld **[!UICONTROL Newsletter Styles]** .

1. Klik op **[!UICONTROL Save and Resume]** als de bewerking is voltooid.

   De nieuwsbrief verschijnt in de rij wachtend om te worden verwerkt.

## Controleren op problemen

Voor het _Admin_ menu, ga **[!UICONTROL Reports]** > _[!UICONTROL Marketing]_>**[!UICONTROL Newsletter Problem Reports]**.

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
| [!UICONTROL Status] | Geeft een status van de nieuwsbrief aan. Mogelijke waarden: `Sent` , `Canceled` , `Not Sent` , `Sending` of `Paused` . |
| [!UICONTROL Processed] | Geeft aan hoeveel nieuwsbrieven zijn verzonden. |
| [!UICONTROL Recipients] | Geeft aan hoeveel nieuwsbrieven door abonnees zijn ontvangen. |
| [!UICONTROL Actions] | **[!UICONTROL Preview]** : hiermee wordt een apart venster geopend waarin een voorvertoning van de sjabloon wordt weergegeven. |

{style="table-layout:auto"}
