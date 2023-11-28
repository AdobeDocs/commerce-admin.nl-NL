---
title: Widget bestellingen en geretourneerde opdrachten
description: Leer hoe u de widget voor bestellingen en retourneringen kunt gebruiken om klanten de mogelijkheid te bieden de status van hun bestellingen, facturen afdrukken en verzendingen bij te houden.
exl-id: 1c3948e6-a0de-4ee4-8abf-10ab845a94a7
feature: Page Content, Orders, Returns
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 0%

---

# Widget bestellingen en geretourneerde opdrachten

De _Orders en retourzendingen_ widget biedt gasten de mogelijkheid om de status van hun bestellingen , facturen voor afdrukken en verzendingen te controleren . Wanneer de widget aan de winkel wordt toegevoegd, is deze alleen zichtbaar voor gasten en voor klanten die niet zijn aangemeld bij hun accounts. Gasten kunnen bestellingen zoeken door de bestellings-id, de naam van de factureringsnaam en het e-mailadres of de postcode op te geven.

![De widget bestellingen en retourneert deze in de zijbalk van de winkelbrowser](./assets/storefront-widget-orders-returns-sidebar.png){width="600" zoomable="yes"}

## De widget bestellingen en retourneert deze op de storefront

1. De klant kan de **[!UICONTROL Find Order By]** kiest u een van de volgende parameters om de volgorde te zoeken:

   - E-mailadres
   - Postcode

1. De klant gaat de **[!UICONTROL Order ID]** en **[!UICONTROL Billing Last Name]**.

1. Voert de facturering in **[!UICONTROL Email Address]** of **[!UICONTROL ZIP Code]** die aan de orde wordt geassocieerd.

1. Klikken **[!UICONTROL Search]** om de bestelling op te halen.

   ![Orderinformatie weergegeven in de winkel](./assets/storefront-widget-orders-returns-view.png){width="700" zoomable="yes"}

## De widget voor bestellingen en geretourneerde meldingen instellen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Klik in de rechterbovenhoek op **[!UICONTROL Add Widget]**.

1. In de _[!UICONTROL Settings]_Ga als volgt te werk:

   - Set **[!UICONTROL Type]** tot `Orders and Returns`.

   - Kies de optie **[!UICONTROL Design Theme]** die door de winkel wordt gebruikt.

1. Klik op **[!UICONTROL Continue]**.

1. In de _[!UICONTROL Storefront Properties]_Ga als volgt te werk:

   - Voor **[!UICONTROL Widget Title]**, voert u een beschrijvende titel in voor de widget.

     Deze titel is alleen zichtbaar vanuit de beheerder.

   - Voor **[!UICONTROL Assign to Store Views]** selecteert u de winkelweergaven waarin de widget zichtbaar is.

     U kunt een specifieke winkelweergave selecteren, of `All Store Views`. Als u meerdere weergaven wilt selecteren, houdt u Ctrl (PC) of Command (Mac) ingedrukt en klikt u op elke optie.

   - (Optioneel) Voor **[!UICONTROL Sort Order]** Voer een getal in om de volgorde te bepalen waarin dit item wordt weergegeven met andere items op hetzelfde deel van de pagina. (`0` = eerst, `1` = seconde, `3` = derde, enzovoort.)

1. In de _[!UICONTROL Layout Updates]_sectie, klikken **[!UICONTROL Add Layout Update]**en voer de volgende handelingen uit:

   - Set **[!UICONTROL Display On]** op het type pagina waarop u de widget wilt weergeven.

   - Om te bepalen waar de widget op de pagina wordt weergegeven, vult u de rest van de layout-update-informatie in.

1. Klik op **[!UICONTROL Save]**.

1. Wanneer ertoe aangezet om het geheime voorgeheugen te verfrissen, klik de verbinding in het bericht bij de bovenkant van de pagina en volg de instructies.
