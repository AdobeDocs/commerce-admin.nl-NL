---
title: Abonnees voor nieuwsbrieven beheren
description: Leer hoe u abonnees van nieuwsbrieven beheert met een eenvoudige lijst met actieve abonnementen.
exl-id: c7e8e642-e3fd-4979-9ea3-2d96839730b2
feature: Customers, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 0%

---

# Abonnees voor nieuwsbrieven beheren

U kunt het beste regelmatig uw abonnementenlijst beheren en alle aanvragen om uw abonnement op te zeggen verwerken. In sommige rechtsgebieden is het wettelijk vereist dat verzoeken tot opzegging binnen een bepaalde termijn worden verwerkt.

U kunt uw abonnees eenvoudig beheren met een eenvoudige lijst met actieve abonnementen. Wanneer een klant een unsubscribe verzoek voorlegt, kunt u eenvoudig een _Unsubscribe_ actie op één of meerdere geselecteerde abonnementen toepassen.

In installaties met één site met meerdere winkelweergaven kan een abonnement op een klantenaccount worden gekoppeld aan een specifieke winkelweergave.

In multi-store en multi-site montages met een globaal [ werkingsgebied van de klantenrekening ](../customers/customer-account-scope.md), kan een klantenrekening aan nieuwsbrieven voor veelvoudige plaatsen/opslag worden ingetekend. In dit geval kunt u de klantenaccount bewerken om een groep abonnementen te beheren of een abonnement voor een specifieke site/winkel annuleren om een aanvraag in te willigen.

Als u nieuwsbrieven wilt verzenden met een externe service, kunt u uw abonnementenlijst exporteren als een CSV- of XML-bestand.

## Abonnementen voor een klant beheren

1. Voor _Admin_ sidebar, ga **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Zoek de klant in het raster en klik op **[!UICONTROL Edit]** in de kolom _[!UICONTROL Action]_.

1. Klik op **[!UICONTROL Newsletter]** in het linkerdeelvenster.

1. Wijzig de abonnementen voor de klant volgens uw plaats/opslagopstelling.

   Voor één site of één winkel kunt u gewoon het selectievakje **[!UICONTROL Subscribed to Newsletter]** in- of uitschakelen.

   ![ Enige checkbox van het de bulletin van de archiefklant ](./assets/newsletter-customer-single-store.png){width="500" zoomable="yes"}

   Voor één site/meerdere winkels kunt u het selectievakje **[!UICONTROL Subscribed to Newsletter]** in- of uitschakelen en **[!UICONTROL Subscribed on Store View]** instellen op de juiste winkelweergave voor het abonnement.

   ![ multi-store checkbox van het de bulletin van de klant en de selecteur van de opslagmening ](./assets/newsletter-customer-multi-store.png){width="500" zoomable="yes"}

   Voor een installatie van meerdere sites/meerdere winkels met een algemeen bereik voor klantenaccounts geeft de pagina de abonnementsstatus voor alle sites weer. U kunt het selectievakje **[!UICONTROL Subscribed]** in- of uitschakelen en/of de **[!UICONTROL Store View]** voor het abonnement wijzigen.

   ![ Multisite checkboxes van het de bulletin van de klant en de selecteurs van de opslagmening ](./assets/newsletter-customer-multi-site.png){width="500" zoomable="yes"}

1. Klik op **[!UICONTROL Save Customer]**.

## Abonnement annuleren in de lijst met abonnees

1. Voor _Admin_ sidebar, ga **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Subscribers]**.

   Voor een installatie op meerdere sites waarbij sommige klanten abonnementen hebben voor meerdere sites, wordt elk abonnement weergegeven als een lijstitem in het raster.

1. Zoek de abonnee in het raster en selecteer het selectievakje in de eerste kolom.

   >[!NOTE]
   >
   >Als u het abonnement op grote hoeveelheden opzegt, schakelt u het selectievakje in van elke abonnee die u wilt annuleren.

1. Stel het besturingselement _[!UICONTROL Action]_&#x200B;in op **[!UICONTROL Unsubscribe]**&#x200B;en klik op **[!UICONTROL Submit]**.

   ![ Unsubscribe nieuwsbrief ](./assets/newsletter-unsubscribe.png){width="600" zoomable="yes"}

   De status van de record verandert in `Unsubscribed` .

## De lijst met abonnees exporteren

1. Van de _[!UICONTROL Newsletter Subscribers]_&#x200B;lijst, gebruik de filtercontroles om slechts verslagen met a_ Status _van `Subscribed` en voor de aangewezen website, opslag, of opslagmening te omvatten.

1. Stel het besturingselement **[!UICONTROL Export to]** in op een van de volgende opties:

   - `CSV`
   - `XML`

1. Klik op **[!UICONTROL Export]** en zoek de vraag onder aan het scherm en sla het bestand op.

   ![ de nieuwsbrief van de Uitvoer abonnees ](./assets/newsletter-subscribers-export.png){width="600" zoomable="yes"}

## Een abonnee verwijderen uit de lijst met abonnees

1. Voor _Admin_ sidebar, ga **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Subscribers]**.

1. Zoek de abonnee in het raster en selecteer het selectievakje in de eerste kolom.

1. Stel het besturingselement _[!UICONTROL Action]_&#x200B;in op **[!UICONTROL Delete]**&#x200B;en klik op **[!UICONTROL Submit]**.

1. Klik op **[!UICONTROL OK]** wanneer u wordt gevraagd om te bevestigen.
