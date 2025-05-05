---
title: Een netwerk voor inhoudslevering gebruiken
description: Leer hoe u een CDN (Content Delivery Network) gebruikt om mediabestanden op te slaan.
exl-id: cb612b79-f3e3-4f1b-8cf9-d47886486686
feature: Page Content, Media, Configuration
level: Experienced
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%

---

# Een netwerk voor inhoudslevering gebruiken

U kunt een CDN (Content Delivery Network) gebruiken om mediabestanden op te slaan. Adobe Commerce op wolkeninfrastructuur omvat snelst CDN (zie [ Fastly ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/cdn/fastly.html) in _Commerce op de Gids van de Infrastructuur van de Wolk_). Een instantie van Commerce die _op gebouw_ geïnstalleerd is omvat geen integratie met om het even welke specifieke CDN, kunt u CDN van uw keus gebruiken.

Na het vormen van CDN, moet u de configuratie van Admin voltooien. De wijzigingen kunnen op globaal niveau of op het niveau van de website worden aangebracht. Wanneer een CDN wordt gebruikt voor mediaopslag, worden alle paden naar media op Commerce-winkelpagina&#39;s gewijzigd in de CDN-paden die in de configuratie zijn opgegeven.

## CDN-workflow

1. **Browser verzoekt media** - een pagina van de opslag opent in browser van de klant, en browser verzoekt de media die in de HTML wordt gespecificeerd.
1. **Verzoek dat naar CDN wordt verzonden; de beelden die** worden gevonden en worden gediend - het verzoek wordt eerst verzonden naar CDN. Als de CDN de afbeeldingen in opslag heeft, dienen de mediabestanden naar de browser van de klant.
1. **gevonden niet Media, verzoek dat naar [!DNL Commerce] Webserver** wordt verzonden - als CDN niet de media dossiers heeft, wordt het verzoek verzonden naar de [!DNL Commerce] Webserver. Als de mediabestanden in het bestandssysteem worden gevonden, stuurt de webserver ze naar de browser van de klant.

>[!IMPORTANT]
>
>Om veiligheidsredenen, wanneer een CDN als media opslag wordt gebruikt, JavaScript kan niet behoorlijk functioneren als CDN buiten uw subdomain wordt gevestigd.

## Een netwerk voor de levering van inhoud configureren

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Kies in het linkerdeelvenster onder _[!UICONTROL General]_&#x200B;de optie **[!UICONTROL Web]**.

1. Stel in de linkerbovenhoek **[!UICONTROL Store View]** naar wens in.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Base URLs]** sectie uit en doe het volgende:

   ![ Algemene configuratie - Web basis URLs ](./assets/web-base-urls.png){width="600" zoomable="yes"}

   - Werk **[!UICONTROL Base URL for Static View Files]** met URL van de plaats op CDN bij waar de statische meningsdossiers worden opgeslagen.

   - Werk **[!UICONTROL Base URL for User Media Files]** met URL van de dossiers van JavaScript op CDN bij.

     Beide velden kunnen leeg worden gelaten of beginnen met de tijdelijke aanduiding: `{% raw %}{{unsecure_base_url}}{% endraw %}`

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Base URLs (Secure)]** sectie uit en doe het volgende:

   ![ Algemene configuratie - Web basis URLs (veilig) ](./assets/web-base-urls-secure.png){width="600" zoomable="yes"}

   - Werk **[!UICONTROL Secure Base URL for Static View Files]** met URL van de plaats op CDN bij waar de statische meningsdossiers worden opgeslagen.

   - Werk **[!UICONTROL Secure Base URL for User Media Files]** met URL van de dossiers van JavaScript op CDN bij.

     Beide velden kunnen leeg worden gelaten of beginnen met de tijdelijke aanduiding: `{% raw %}{{unsecure_base_url}}{% endraw %}`

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.
