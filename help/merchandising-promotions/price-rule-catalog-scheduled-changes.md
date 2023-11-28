---
title: Geplande wijzigingen voor prijsregels voor catalogi
description: Leer hoe u de prijsregels voor catalogi op schema toepast als onderdeel van een campagne en gegroepeerd met andere wijzigingen in de inhoud.
exl-id: ec4b915f-0a27-438d-b1b0-f1bcd297af6d
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '797'
ht-degree: 0%

---

# Geplande wijzigingen voor prijsregels voor catalogi

{{ee-feature}}

Het vak Geplande wijzigingen wordt boven aan de pagina weergegeven wanneer een nieuwe prijsregel wordt opgeslagen of bijgewerkt. De catalogusprijsregels kunnen volgens schema worden toegepast als onderdeel van een campagne en worden gegroepeerd met andere inhoudswijzigingen. U kunt een campagne maken op basis van geplande wijzigingen in een prijsregel, of de wijzigingen toepassen op een bestaande campagne.

>[!NOTE]
>
>Alle geplande updates worden achtereenvolgens toegepast. Dit betekent dat elke entiteit slechts één geplande update op één tijdstip kan hebben. Elke geplande update wordt toegepast op alle winkelweergaven binnen de opgegeven tijdsperiode. Dientengevolge, kan een entiteit verschillende geplande updates voor verschillende opslagmeningen niet tezelfdertijd hebben. Alle waarden van entiteitattributen binnen alle opslagmeningen, die niet door de huidige geplande update worden beïnvloed, worden genomen van de standaardwaarden, en niet van de vorige geplande update.

Als er meerdere prijsregels in dezelfde campagne worden uitgevoerd, bepaalt de instelling bij Prioriteit van de prijsregel welke regel voorrang krijgt. Zie voor meer informatie [Inhoud stapelen](../content-design/content-staging.md).

>[!IMPORTANT]
>
>Als een campagne met een prijsregel in eerste instantie zonder einddatum wordt gemaakt, kan de campagne later niet worden bewerkt om een einddatum op te nemen. U wordt aangeraden een einddatum toe te voegen wanneer u de campagne maakt of een dubbele versie van de bestaande campagne te maken en de einddatum desgewenst aan het duplicaat toe te voegen.

![Catalogusprijsregel - geplande wijzigingen](./assets/price-rule-catalog-scheduled.png){width="600" zoomable="yes"}

## Een update van een regel voor catalogusprijzen plannen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**Catalogusprijsregel**.

1. Open de regel in de bewerkingsmodus.

1. In de **[!UICONTROL Scheduled Changes]** klikt u boven aan de pagina op **[!UICONTROL Schedule New Update]**.

1. Met de **[!UICONTROL Save as a New Update]** geselecteerde optie, doe het volgende:

   - Voor **[!UICONTROL Update Name]**, voert u een naam in voor de update van de regel.

   - Voer een korte beschrijving in **[!UICONTROL Description]** van de actualisering, met inbegrip van de wijze waarop of waarom deze wordt toegepast.

   - Gebruik de _Kalender_ (![Kalenderpictogram](../assets/icon-calendar.png)) om de **[!DNL Start Date]** en **[!UICONTROL End Date]** de geplande wijziging van kracht wordt. Laat de einddatum leeg als u een wijziging met een open einde wilt maken.

   ![Regels voor catalogusprijzen - nieuwe geplande wijzigingen](./assets/price-rule-catalog-schedule-update.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >De begin- en einddatum/tijd worden bepaald door de standaarddatum/tijd en tijdzone van het deelvenster Beheer, niet door de tijdzone van een bepaalde website. Neem de tijdzone van de website in overweging om de begin- en eindtijd correct te bepalen. Maak aparte regels voor websites in verschillende tijdzones die op specifieke lokale tijdstippen moeten starten en/of stoppen.

1. Omlaag schuiven naar de **[!UICONTROL Rule Information]** en wijzigt u de regel naar wens.

   U kunt veranderingen voor om het even welke regelparameter, met inbegrip van de websites (werkingsgebied)/klantengroepen voor de regel, voorwaarden van de regel, en acties plannen die door de regel worden toegepast. Zie voor meer informatie [Een regel voor catalogusprijzen maken](price-rules-catalog-create.md).

   >[!NOTE]
   >
   >Als u in om het even welke parameters van de regelinformatie verandert, zorg ervoor dat _[!UICONTROL Status]_correct is ingesteld. Als u wilt dat de wijziging resulteert in een actief toegepaste regel, moet de status`Active`.

1. Klik op **[!UICONTROL Save]**.

   De geplande wijziging wordt boven aan de pagina weergegeven met de begin- en einddatum van de campagne.

## Een geplande regelwijziging bewerken

1. In de **[!UICONTROL Scheduled Changes]** klikt u boven aan de pagina op **[!UICONTROL View/Edit]**.

1. Breng de benodigde wijzigingen aan in de geplande update.

1. Klik op **[!UICONTROL Save]**.

## Voorvertoning van geplande regelwijziging

1. In de **[!UICONTROL Scheduled Changes]** klikt u boven aan de pagina op **[!UICONTROL Preview]**.

   In Voorvertoning wordt een nieuw browsertabblad geopend waarin uw winkelpatroon wordt geladen met de toegepaste geplande wijziging. Navigeer naar een product dat door de wijziging wordt beïnvloed.

   ![Voorvertoning geplande wijziging](./assets/price-rule-catalog-scheduled-update-preview.png){width="600" zoomable="yes"}

1. Klik in de linkerbovenhoek van het voorvertoningsvenster op **[!UICONTROL Calendar]**.

   De kalenderdetails tonen andere campagnes die voor de zelfde dag gepland zijn. Elke record in de lijst is een afzonderlijke regelupdate.

   ![Lijst van geplande updates voor een specifieke datum](./assets/price-rule-catalog-scheduled-preview-calendar.png){width="600" zoomable="yes"}

1. Als u een andere dag of tijd wilt voorvertonen, klikt u op de knop **[!UICONTROL Date & Time]** kalender ![Kalenderpictogram](../assets/icon-calendar.png) en voer de volgende handelingen uit:

   - Kies een andere datum en/of tijd.

   - Klik op **[!UICONTROL Preview]**.

1. Als u wilt terugkeren naar de agenda, klikt u op **[!UICONTROL Calendar]** in de koptekst van de pagina Voorvertoning.

   Vanaf hier kunt u het volgende doen:

   **Een koppeling naar de voorvertoning delen**

   Als u een koppeling naar de voorvertoning van de winkel wilt delen met uw collega&#39;s, klikt u op **[!UICONTROL Share]**. Kopieer de koppeling naar het klembord en plak deze in de hoofdtekst van een e-mailbericht.

   >[!NOTE]
   >
   >Een Admin-gebruikersaccount is vereist om een gedeelde voorvertoning te kunnen zien. Als uw [rol heeft toegang](../systems/permissions-user-roles.md) als u een Admin-gebruikersaccount wilt maken, moet u eerst een account voor een nieuwe gebruiker maken voordat u een account kunt delen.

   **Het bereik van de voorvertoning wijzigen**

   Als u de geplande wijzigingen voor verschillende winkelweergaven wilt zien, klikt u op **[!UICONTROL Scope]** in de koptekst van de pagina Voorvertoning. Kies de website-, opslag- of opslagweergave die u wilt voorvertonen.

1. Ga zo nodig terug naar de kalender en klik op **[!UICONTROL View/Edit]** in de _[!UICONTROL Action]_om een andere geplande update te openen.
