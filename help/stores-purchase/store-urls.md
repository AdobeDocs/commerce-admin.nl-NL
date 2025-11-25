---
title: URL's opslaan
description: Leer over opslag URLs en hoe te om basisURL en opslagcodes te vormen.
exl-id: dd7a6317-b0cf-4d0c-9b31-a963c467026b
feature: Site Management, System
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: 15118877bb8cc533b2323819db34da0513899e25
workflow-type: tm+mt
source-wordcount: '1529'
ht-degree: 0%

---

# URL&#39;s opslaan

Elke website in een Adobe Commerce- of Magento Open Source-installatie heeft een basis-URL die is toegewezen aan de storefront en een andere URL die is toegewezen aan de beheerder. Adobe gebruikt variabelen om interne koppelingen te definiëren met betrekking tot de basis-URL, waardoor het mogelijk wordt om een volledige winkel van de ene locatie naar de andere te verplaatsen zonder de koppelingen bij te werken. Standaard basis-URL&#39;s beginnen met `http` en veilige basis-URL&#39;s beginnen met `https` .

- **Basis URL** — `http://www.yourdomain.com/magento/`
- **Veilige Basis URL** — `https://www.yourdomain.com/magento/`
- **URL met IP adres** — `http://###.###.###.###/magento/` of `https://###.###.###.###/magento/`

>[!IMPORTANT]
>
>Wijzig de URL van de beheerder niet vanuit de standaard basis-URL-configuratie. Om Admin URL of weg te veranderen, zie [&#x200B; Gebruik een douane Admin URL &#x200B;](#use-a-custom-admin-url).

## Beveiligd protocol gebruiken

De basis-URL&#39;s voor uw winkel zijn aanvankelijk ingesteld tijdens de Adobe Commerce-installatie. Als een beveiligingscertificaat op dat moment beschikbaar was, kunt u opgeven dat `HTTPS` URL&#39;s moeten worden gebruikt voor de winkel, beheerder of beide. Als uw Adobe Commerce-installatie meerdere winkels bevat of als u later meer winkels wilt toevoegen, kunt u de winkelcode opnemen in de URL. Alle Adobe-bronnen en -bewerkingen kunnen met een beveiligd protocol worden gebruikt.

Als een beveiligingscertificaat niet beschikbaar was voor het domein op het moment van de installatie, moet u de configuratie bijwerken voordat u de winkel start. Nadat een veiligheidscertificaat voor uw domein wordt gevestigd, kunt u één van beide of beide basis URLs vormen om met gecodeerde Veilige Laag van Contactdozen (SSL) en [ het protocol van de Veiligheid van de Laag van het Vervoer van de Laag ][1] (TLS) in werking te stellen.

>[!IMPORTANT]
>
>Adobe raadt ten zeerste aan alle pagina&#39;s van een productiesite, inclusief de inhoud en productpagina&#39;s, via een beveiligd protocol over te brengen.

Adobe Commerce en Magento Open Source kunnen standaard worden geconfigureerd om alle pagina&#39;s via `HTTPS` te leveren. Als uw opslag met standaardprotocol in werking is gesteld, kunt u veiligheid verbeteren door [ de Strikte Veiligheid van het Vervoer van HTTP toe te laten ][2] (HSTS) en om het even welke onveilige paginaverzoeken te bevorderen. HSTS is een opt-in protocol dat browsers verhindert standaard `HTTP` pagina&#39;s terug te geven die met onbeveiligd protocol voor het gespecificeerde domein worden overgebracht. Omdat zoekprogramma&#39;s elke pagina van uw winkel mogelijk al hebben geïndexeerd met standaard `HTTP` URL&#39;s, kunt u Commerce zo configureren dat onveilige paginaaanvragen automatisch worden bijgewerkt naar `HTTPS` , zodat er geen verkeer verloren gaat. Wanneer Commerce is geconfigureerd voor het gebruik van beveiligde URL&#39;s voor zowel de winkel als de beheerder, worden twee extra velden weergegeven waarmee u `HSTS` kunt inschakelen.

## De basis-URL configureren

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Onder _Algemeen_ in het linkerpaneel, kies **[!UICONTROL Web]**.

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Base URL]** sectie uit.

   - **[!UICONTROL Base URL]** — Voer de volledig gekwalificeerde basis-URL voor uw winkel in. Zorg ervoor dat u de URL beëindigt met een slash, zodat deze kan worden uitgebreid met extra URL-sleutels uit uw winkel. Bijvoorbeeld: `http://yourdomain.com/`

     >[!NOTE]
     >
     >Wijzig de plaatsaanduiding in het veld _[!UICONTROL Base Link URL]_&#x200B;niet. Deze tijdelijke aanduiding wordt gebruikt om relatieve koppelingen naar de basis-URL te maken.

   - **[!UICONTROL Base URL for Static View Files]** — (Optioneel) Geef een alternatieve locatie op voor de basis-URL voor statische weergavebestanden door het pad in te voeren, te beginnen met de volgende plaatsaanduiding:

     \{unsecure_base_url}

   - **[!UICONTROL Base URL for User Media Files]** — (Optioneel) Geef een alternatieve locatie op voor de basis-URL voor gebruikersmediabestanden door het pad in te voeren, te beginnen met de volgende plaatsaanduiding:

     \{unsecure_base_url}

     Voor een gebruikelijke installatie is het niet nodig de paden voor de statische weergavebestanden of mediabestanden bij te werken, omdat deze relatief zijn ten opzichte van de basis-URL.

   ![&#x200B; Algemene configuratie - Web basis URLs &#x200B;](../configuration-reference/general/assets/web-base-urls.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Plaatsaanduidingen tussen dubbele accolades zijn opmaakcodes voor variabelen.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

## De beveiligde basis-URL configureren

Als uw domein een geldig veiligheidscertificaat heeft, kunt u URLs van zowel de storefront als Admin vormen om gegevens over een veilig (https) kanaal over te brengen. Zonder geldig beveiligingscertificaat kan uw winkel niet werken met het veilige protocol (SSL/TLS).

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) uit _[!UICONTROL Base URLs (Secure])_ sectie en doe het volgende:

   ![&#x200B; Algemene configuratie - veilige basis URLs &#x200B;](../configuration-reference/general/assets/web-base-urls-secure.png){width="600" zoomable="yes"}

   - **[!UICONTROL Secure Base URL]** — Voer de volledige beveiligde basis-URL in, gevolgd door een slash. Bijvoorbeeld: `https://yourdomain.com/`

   - **[!UICONTROL Secure Base Link URL]** — Wijzig de plaatsaanduiding niet in het veld voor de beveiligde basiskoppeling van de URL. Deze wordt gebruikt om relatieve koppelingen naar de beveiligde basis-URL te maken.

   - **[!UICONTROL Secure Base URL for Static View Files]** — (Optioneel) Geef een alternatieve locatie op voor de beveiligde basis-URL voor statische weergavebestanden door het pad in te voeren, te beginnen met de volgende tijdelijke aanduiding:

     \{secure_base_url}

   - **[!UICONTROL Secure Base URL for User Media Files]** — (Optioneel) Geef een alternatieve locatie op voor de beveiligde basis-URL voor gebruikersmediabestanden door het pad in te voeren, te beginnen met de volgende tijdelijke aanduiding:

     \{secure_base_url}

1. Stel beide volgende opties in op `Yes` om de beveiliging te verbeteren.

   - **[!UICONTROL Use Secure URLs on Storefront]**
   - **[!UICONTROL Use Secure URLs in Admin]**

1. Voer voor _[!UICONTROL Enhanced Security Settings]_&#x200B;de volgende handelingen uit:

   - **[!UICONTROL Enable HTTP Strict Transport Security (HSTS)]** — Als u wilt dat uw winkel alleen beveiligde HTTPS-paginaaanvragen weergeeft, stelt u deze in op `Yes` .

   - **[!UICONTROL Upgrade Insecure Requests]** — Als u aanvragen voor standaard onbeveiligde HTTP-pagina&#39;s wilt bijwerken om HTTPS te beveiligen, stelt u deze in op `Yes` .

1. Stel de **[!UICONTROL Offloader Header]** voor uw server in.

   De meeste Commerce-installaties gebruiken de standaardwaarde `X-Forward-Proto` om het protocol als `HTTP` of `HTTPS` aan te duiden. Als uw serverconfiguratie een verschillende offloader_header gebruikt, ga het hier in.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

## De winkelcode opnemen in URL&#39;s

>[!NOTE]
>
>Wanneer _de Add optie van de Opslag Code aan URLs_ aan `Yes` wordt geplaatst, moet u opslagcodes in uw browser URLs omvatten. Dit het plaatsen zorgt ervoor dat URL herschrijft correct in kaart wordt gebracht en alle pagina&#39;s met succes worden geopend, zonder _&quot;404 Pagina niet gevonden&quot;_ fouten.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Kies onder _[!UICONTROL General]_&#x200B;in het linkerdeelvenster de optie **[!UICONTROL Web]**.

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL URL Options]** sectie uit.

1. Stel **[!UICONTROL Add Store Code]** in op uw voorkeur:

   - **[!UICONTROL URL with Store Code]**: `http://www.yourdomain.com/magento/[store-code]/index.php/url-identifier`
   - **[!UICONTROL URL without Store Code]**: `http://www.yourdomain.com/magento/index.php/url-identifier`

   ![&#x200B; Algemene configuratie - Web URL opties &#x200B;](../configuration-reference/general/assets/web-url-options.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

1. Klik op de koppeling **[!UICONTROL Cache Management]** in het bericht boven aan de werkruimte. Volg vervolgens de instructies om de cache te vernieuwen.

   ![&#x200B; het beheersbericht van het Geheime voorgeheugen &#x200B;](./assets/msg-cache-management.png)

## URL-probleemoplossing

Als na het volgen van de configuratieinstructies, sommige pagina&#39;s met onveilige URL (`http://`) blijven worden gediend, doe het volgende:

- Wijzig de (onveilige) basis-URL in de beveiligde HTTPS-URL.
- Bewerk het bestand `.htaccess` (of het taakverdelingsmechanisme) op de server, zodat de onveilige URL wordt omgeleid naar de beveiligde URL.

## Een aangepaste Admin URL gebruiken

Als beste praktijken van de a [&#x200B; veiligheid &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html), adviseert Adobe dat u unieke Admin URL in plaats van standaard _admin_ of een gemeenschappelijke termijn zoals _achterste_ gebruikt. Hoewel uw site niet direct wordt beschermd tegen een bepaalde slechte actor, kan de site de blootstelling aan scripts verminderen die proberen onbevoegde toegang te krijgen.

>[!NOTE]
>
>Vraag uw hostingprovider om advies voordat u een aangepaste Admin-URL implementeert. Sommige hostingproviders hebben een standaard-URL nodig om te voldoen aan de beveiligingsregels voor firewalls.

In een standaardinstallatie volgen de URL en het pad van de beheerder direct de basis-URL. Het beheerpad bevindt zich in een map onder het hoofdknooppunt.

- **StandaardBasis URL**: `http://yourdomain.com/magento/`
- **Standaard Admin Weg**: `admin`
- **Standaard Admin URL en Weg**: `http://yourdomain.com/magento/admin`

Hoewel het mogelijk is de URL en het pad van de beheerder naar een andere locatie te wijzigen, verwijdert elke fout de toegang tot de beheerder en moet deze worden gecorrigeerd vanaf de server.

>[!NOTE]
>
>Als voorzorgsmaatregel, probeer niet om Admin URL zelf te veranderen tenzij u weet hoe te om configuratiedossiers op de server uit te geven. Voor de projecten van Adobe Commerce die op wolkeninfrastructuur worden opgesteld, verander Admin URL door de [&#x200B; instructies &#x200B;](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/stage/variables-admin.html#admin-url) in *Adobe Commerce op de Gids van de Infrastructuur van de Wolk te volgen*.

### Methode 1: Wijzigen ten opzichte van de beheerder

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Advanced]** uit en kies **[!UICONTROL Admin]** .

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Admin Base URL]** sectie uit.

1. Stel de configuratieopties voor de aangepaste URL in:

   ![&#x200B; Geavanceerde configuratie - basisURL Admin &#x200B;](../configuration-reference/advanced/assets/admin-admin-base-url.png){width="600" zoomable="yes"}

   Schakel indien nodig het selectievakje **[!UICONTROL Use system value]** uit om de instelling te wijzigen.

   - Stel **[!UICONTROL Use Custom Admin URL]** in op `Yes` .

   - Voer de **[!UICONTROL Custom Admin URL]** in: `http://yourdomain.com/magento/`

     >[!NOTE]
     >
     >De Admin-URL moet zich in dezelfde Commerce-installatie bevinden en moet dezelfde hoofdmap van het document hebben als de storefront.

   - Stel **[!UICONTROL Custom Admin Path]** in op `Yes` .

   - Voer bij **[!UICONTROL Custom Admin Path]** het pad in dat u wilt gebruiken als de naam van de aangepaste beheermap.

     Voorbeeld: `sample_custom_admin`

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

1. Nadat de wijzigingen zijn opgeslagen, meldt u zich af bij Beheer en meldt u zich weer aan met de nieuwe Admin-URL en het nieuwe pad.

### Methode 2: Wijzig het beheerpad van de opdrachtregel van de server

1. Open het bestand `app/etc/env.php` in een teksteditor en wijzig de waarde van de parameter `frontName` in de sectie `backend` . Sla het bestand vervolgens op.

   Gebruik alleen kleine letters.

   >[!NOTE]
   >
   >   Met deze methode kunt u het beheerpad wijzigen, maar niet de beheerdersURL.

   >[!TIP]
   >
   >Voor Adobe Commerce op cloudinfrastructuur kunt u een aangepast beheerpad instellen met de variabele `ADMIN_URL` in de interface van de cloud. Zie het [&#x200B; onderwerp van Admin variabelen &#x200B;](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/stage/variables-admin.html) in _Commerce op de Gids van de Infrastructuur van de Wolk_.

   - **Standaard Admin Weg**

     ```php?start_inline=1
     'backend' => [
      'frontName' => 'admin'
     ],
     ```

   - **Nieuwe Admin Weg**

     ```php?start_inline=1
     'backend' => [
         'frontName' => 'backend'
     ],
     ```

1. Gebruik een van de volgende methoden om de cache te wissen:

   - Voor _Admin_ sidebar, ga **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**. Klik vervolgens op **[!UICONTROL Flush Magento Cache]**.
   - Voer op de server het volgende uit:

     ```bash
     php bin/magento cache:flush
     ```

   >[!NOTE]
   >
   >De wijzigingen die zijn aangebracht met methode 1 hebben voorrang op de wijzigingen die zijn aangebracht in het bestand `app/etc/env.php` .

### Methode 3: Wijzig het beheerpad met de Commerce CLI

U kunt de CLI `setup:config:set` opdracht gebruiken om het Admin-pad te wijzigen. In het volgende voorbeeld wordt de optie `--backend-frontname` gebruikt om het pad van de Commerce-hoofdmap te wijzigen in een nieuw beheerpad:

```bash
bin/magento setup:config:set --backend-frontname="backend_front_name"
```

Met deze opdracht werkt u de configuratieoptie `backend` > `frontName` in het `app/etc/env.php` -bestand bij.

## Het standaardpad voor Admin URL en Admin herstellen

Als u een ongeldige Admin URL of een Weg van Admin hebt geplaatst en toegang tot het achterste eind verliest, is er een manier om het van de bevellijn te bevestigen.

1. Voer de volgende opdracht uit om terug te keren naar de standaard URL voor Admin:

   ```bash
   php bin/magento config:set admin/url/use_custom 0
   ```

1. Als u het standaardbeheerpad wilt herstellen (ingesteld in de `app/etc/env.php` , zoals beschreven in methode 2), voert u deze opdracht uit:

   ```bash
   php bin/magento config:set admin/url/use_custom_path 0
   ```

1. Gebruik een van de volgende methoden om de cache te wissen:

   - Voor _Admin_ sidebar, ga **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**. Klik vervolgens op **[!UICONTROL Flush Magento Cache]**.
   - Voer op de server het volgende uit:

     ```bash
     php bin/magento cache:flush
     ```


[1]: https://en.wikipedia.org/wiki/Transport_Layer_Security
[2]: https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security
