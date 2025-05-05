---
title: Integraties
description: Leer hoe u OAuth-referenties configureert en URL omleidt voor integratie van derden.
exl-id: b7632994-b07b-4cdb-b62c-79bc7a3a01c8
role: Admin, Developer
feature: System, Integration, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---

# Integraties

Door een integratie in Commerce Admin te definiëren, wordt de locatie van OAuth-referenties vastgesteld en wordt de URL omgeleid voor integratie van derden. Verder worden de beschikbare API-bronnen aangegeven die nodig zijn voor de integratie. Voor meer gedetailleerde informatie over het proces van de integratieregistratie, zie [ op OAuth-Gebaseerde authentificatie ](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) in de de ontwikkelaarsdocumentatie van Commerce.

![ Integraties ](./assets/integrations.png){width="700" zoomable="yes"}

## Workflow voor onboarding

1. **machtigt de integratie** - ga naar **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**&#x200B;pagina, vind de relevante integratie, en autoriseer.
1. **verifieer en vestigt login** - wanneer ertoe aangezet, keur de gevraagde toegang goed. Als u een account hebt omgeleid naar een derde, meldt u zich aan bij het systeem of maakt u een account. Na een geslaagde aanmelding keert u terug naar de integratiepagina.
1. **ontvang bevestiging van erkende integratie** - het systeem verzendt bericht dat de integratie met succes is gemachtigd. Na vestiging is een integratie en het ontvangen van de geloofsbrieven, het niet meer noodzakelijk om vraag aan toegang of verzoektekenen te maken.

## Integratie toevoegen

1. Voor _Admin_ sidebar, ga **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

   ![ Nieuwe integratie ](./assets/integration-new.png){width="600" zoomable="yes"}

1. Voer de volgende integratiegegevens in:

   - Voer de **[!UICONTROL Name]** van de integratie en het contactadres **[!UICONTROL Email]** in.

   - Voer de **[!UICONTROL Callback URL]** in waar OAuth-referenties kunnen worden verzonden bij het gebruik van OAuth voor het uitwisselen van tokens. Het gebruik van `https://` wordt ten zeerste aanbevolen.

   - Voer **[!UICONTROL Identity Link URL]** in om de gebruikers om te leiden naar een externe account met deze Adobe Commerce- of Magento Open Source-integratiegegevens.

   >[!NOTE]
   >
   > Het waarschuwingslabel `Integration not secure` wordt bij elke integratienaam op het [!UICONTROL Integrations] -raster weergegeven als een herinnering, totdat HTTPS-URL&#39;s worden opgeslagen in [!UICONTROL Callback URL] - en [!UICONTROL Identity Link URL] -velden.

   - Voer desgevraagd uw wachtwoord in om uw identiteit te bevestigen.

1. Kies **[!UICONTROL API]** in het linkerdeelvenster en voer de volgende handelingen uit:

   - Stel **[!UICONTROL Resource Access]** in op een van de volgende opties:

      - `All`
      - `Custom`

   - Voor douanetoegang, selecteer checkbox van elk middel dat nodig is.

     ![ Integraties - beschikbare API ](./assets/integrations-available-api.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

## Integratie activeren

Standaard wordt op het raster een opgeslagen integratie weergegeven met de status `Inactive` . Voer de volgende stappen uit om het te activeren:

1. Voor _Admin_ sidebar, ga **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

1. Zoek de nieuwe integratie en klik op de koppeling **[!UICONTROL Activate]** .

1. Klik in de rechterbovenhoek op **[!UICONTROL Allow]** .

   Deze actie toont de Tokens van de Integratie voor Uitbreidingen. Kopieer deze gegevens naar een veilige, gecodeerde locatie voor gebruik met uw integratie.

   ![ Tokens van de Integratie voor Uitbreidingen ](./assets/integration-tokens-for-extensions.png){width="600" zoomable="yes"}

1. Klik in de rechterbovenhoek op **[!UICONTROL Done]** .

## Integratie opnieuw autoriseren

Om een nieuwe Token van de Toegang van de Integratie en het Geheime Geheim van de Toegang te produceren, verkondigde de integratie van Admin opnieuw:

1. Voor _Admin_ sidebar, ga **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

1. De integratie met de status **[!UICONTROL Active]** zoeken.

1. Klik in de kolom _[!UICONTROL Activate]_&#x200B;op **[!UICONTROL Reauthorize]**.

1. Klik op **[!UICONTROL Reauthorize]** om de toegang tot de API-bronnen goed te keuren.

1. Sla de nieuwe integratie-tokens voor extensies op en klik op **[!UICONTROL Done]** .

## De beveiligingsinstelling voor de API-gasttoegang wijzigen

Door gebrek, laat het systeem anonieme gasttoegang tot CMS, catalogus, en andere opslagmiddelen niet toe. Ga als volgt te werk als u de instelling moet wijzigen:

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Services]** uit en kies **[!UICONTROL Magento Web API]** .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Web API Security Setting]** sectie uit.

   ![ de configuratie van de Diensten - Web API veiligheidsmontages ](../configuration-reference/services/assets/web-api-security.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL Allow Anonymous Guest Access]** in op `Yes` .

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

Voor extra informatie, zie [ Beperkend toegang tot anonieme Web APIs ](https://developer.adobe.com/commerce/webapi/rest/use-rest/anonymous-api-security/) in de de ontwikkelaarsdocumentatie van Commerce.

## Integratie verwijderen

1. Voor _Admin_ sidebar, ga **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

1. Vind de bestaande integratie en klik het pictogram ( ![ trashcan pictogram ](../assets/icon-delete-trashcan-solid.png)) in de **[!UICONTROL Delete]** kolom.

1. Klik op **[!UICONTROL OK]** om uw handeling te bevestigen.
