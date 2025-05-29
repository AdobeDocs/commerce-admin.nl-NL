---
title: Sessiebeheer
description: Leer hoe u sessiebeheer configureert om de beheerder en winkel te beveiligen.
exl-id: ad954218-aa3e-44e6-b23f-008de7fc7543
role: Admin
feature: Configuration, Security
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 0%

---

# Sessiebeheer

[ het beheer van de Zitting ](https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html) is een anti-ontkenning van de dienst (Dos) beste praktijken voor API veiligheid. Een sessie geeft aan hoeveel tijd een bezoeker aan uw site besteedt en heeft geen betrekking op hoe lang Admin-gebruikers of -klanten zijn aangemeld bij hun accounts.

Een sessie is een reeks HTTP-aanvraag- en responstransacties voor het netwerk die aan dezelfde gebruiker zijn gekoppeld. Dit is een manier om een client (Admin) aan de gegevens te koppelen wanneer deze toegang krijgen tot de server. Sessies worden gebruikt om variabelen tot stand te brengen, zoals toegangsrechten en lokalisatie-instellingen, die van toepassing zijn op elke interactie die een gebruiker tijdens de sessie met een webtoepassing heeft.

## Sessieformaat

Gebruik de volgende configuratie-instellingen om de maximale sessiegrootte voor Admin-gebruikers en winkelbezoekers te beperken:

- **[!UICONTROL Max Session Size in Admin]** - Beperk de maximale sessiegrootte in bytes. Gebruik `0` om uit te schakelen.
- **[!UICONTROL Max Session Size in Storefront]** - Beperk de maximale sessiegrootte in bytes. Gebruik `0` om uit te schakelen.

>[!TIP]
>
>Beide instellingen worden gemeten in bytes en standaard ingesteld op `256000` bytes (of 256 KB).

**_om maximumzittingsgrootte te vormen:_**

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Advanced]** uit en kies **[!UICONTROL System]** .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Security]** sectie uit om tot de zittingsmontages toegang te hebben.

   ![ montages van de Zitting ](../configuration-reference/advanced/assets/system-security.png){width="600" zoomable="yes"}

1. Voer nieuwe sessiegrootten in bytes in.

   >[!WARNING]
   >
   >Als u de waarde te laag instelt, kunnen er problemen optreden. Als u een van de opties onder de standaardwaarde van 256000 bytes instelt, wordt een waarschuwingsbericht weergegeven. Als u op **[!UICONTROL No]** klikt, wijzigt het systeem de waarde in `256000` .

1. Klik op **[!UICONTROL Save Config]**.

### Admin-sessies

Als u de maximale sessiegrootte overschrijdt, wordt een foutbericht weergegeven en wordt de sessiegrootte door het systeem vastgelegd in de map `var/log` .

Als u toegang tot Admin verliest nadat het plaatsen van de zittingsgrootte aan laag, gebruik CLI om de configuratie terug te stellen:

```bash
bin/magento config:set system/security/max_session_size_admin 256000
```

### Storefront-sessies

Als u de maximale sessiegrootte overschrijdt, wordt er geen fout weergegeven, maar wordt de sessiegrootte door het systeem vastgelegd in de map `var/log` .

## Sessievalidatie

Met Adobe Commerce en Magento Open Source kunt u sessievariabelen valideren als een beschermende maatregel tegen mogelijke aanvallen van sessiefixaties of pogingen om gebruikerssessies te vergiftigen of te kapen. De instellingen voor sessievalidering bepalen hoe sessievariabelen worden gevalideerd tijdens elk bezoek in de winkel en of de sessie-id is opgenomen in de URL van de winkel.

Voor technische informatie, zie [ Redis van het Gebruik voor zittingsopslag ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/redis/redis-session.html) in de _Gids van de Configuratie_.

![ Algemene configuratie - de zittingsbevestiging van het Web ](../configuration-reference/general/assets/web-session-validation-settings.png){width="600" zoomable="yes"}

De validatie controleert of bezoekers zeggen dat ze dit zijn door de waarde in de validatievariabelen te vergelijken met de sessiegegevens die in `$_SESSION` -gegevens voor de gebruiker zijn opgeslagen. Validatie mislukt als de informatie niet naar behoren wordt verzonden en de bijbehorende variabele leeg is. Als een sessievariabele het validatieproces mislukt, wordt de clientsessie onmiddellijk beëindigd, afhankelijk van de instellingen voor sessievalidatie.

Het toelaten van alle bevestigingsvariabelen kan aanvallen helpen verhinderen, maar zou ook de prestaties van de server kunnen beïnvloeden. Standaard is alle validatie van sessievariabelen uitgeschakeld. We raden u aan met de instellingen te experimenteren om de beste combinatie voor uw Adobe Commerce- of Magento Open Source-installatie te vinden. Het activeren van alle validatievariabelen kan onnodig beperkend zijn en kan toegang tot klanten verhinderen die de verbindingen van Internet hebben die door een volmachtsserver overgaan of van achter een firewall voortkomen. Raadpleeg de documentatie over systeembeheer voor uw Linux®-systeem voor meer informatie over sessievariabelen en het gebruik ervan.

**_om de zittingsbevestiging te vormen:_**

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster _[!UICONTROL General]_&#x200B;uit en kies **[!UICONTROL Web]**.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Session Validation Settings]** sectie uit.

1. Stel elk van de configuratieopties in:

   - **[!UICONTROL Validate REMOTE_ADDR]** — Ingesteld op `Yes` om te controleren of het IP-adres van een aanvraag overeenkomt met wat is opgeslagen in de variabele `$_SESSION` .

   - **[!UICONTROL Validate HTTP_VIA]** — Ingesteld op `Yes` om te controleren of het proxyadres van een binnenkomend verzoek overeenkomt met wat is opgeslagen in de variabele `$_SESSION` .

   - **[!UICONTROL Validate HTTP_X_FORWARDED_FOR]** — Ingesteld op `Yes` om te controleren of het doorgestuurde adres van een aanvraag overeenkomt met wat is opgeslagen in de variabele `$_SESSION` .

   - **[!UICONTROL Validate HTTP_USER_AGENT]** — Ingesteld op `Yes` om te controleren of de browser of het apparaat dat wordt gebruikt om de winkel te openen tijdens een sessie, overeenkomt met de inhoud van de variabele `$_SESSION` .

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

## Levensduur beheersessie

Als veiligheidsmaatregel, is _Admin_ aanvankelijk geplaatst aan tijd uit na 900 seconden (15 minuten) van toetsenbordinactiviteit. U kunt de levensduur van de sessie aanpassen aan uw werkstijl.

**_om Admin zittingsleven aan te passen:_**

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Schuif omlaag en vouw **[!UICONTROL Advanced]** uit in het linkerdeelvenster.

1. Klik op **[!UICONTROL Admin]**.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Security]** sectie uit.

1. Voer bij **[!UICONTROL Admin Session Lifetime (seconds)]** het aantal seconden in dat een sessie actief blijft voordat deze wordt beëindigd.

   ![ Geavanceerde configuratie - de veiligheidsmontages van Admin ](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.
