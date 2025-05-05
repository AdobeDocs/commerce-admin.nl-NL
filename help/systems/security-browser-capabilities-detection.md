---
title: Detectie van browsermogelijkheden
description: Leer hoe te om browser capaciteitsopsporing te vormen en een bericht te tonen als de browser van de klant montages moeten worden veranderd.
exl-id: 16caab8b-3ba5-43a1-a6f0-7c1e921be132
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# Detectie van browsermogelijkheden

Net als de meeste websites en toepassingen op internet, vereisen Adobe Commerce en Magento Open Source dat de browser van de bezoeker zowel cookies als JavaScript toestaat voor volledige bewerkingen. Soms wordt de browser van een gebruiker echter ingesteld op de hoogste privacy-instelling die zowel cookies als JavaScript voorkomt. Uw winkel kan worden geconfigureerd om de mogelijkheden van de browser van elke bezoeker te testen en een bericht weer te geven als de instellingen moeten worden gewijzigd.

- Als de browser privacymontages koekjes verbieden, kunt u het systeem vormen om hen aan [ automatisch om te leiden laat Cookies ](../content-design/pages.md#enable-cookies) pagina toe, die verklaart hoe te om de geadviseerde montages met meeste browsers te maken.
- Als de privacyinstellingen van de browser JavaScript niet toestaan, kunt u het systeem zo configureren dat het volgende bericht boven de koptekst van elke pagina wordt weergegeven.

Voor technische informatie, verwijs naar [ Ondersteunde browsers ](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/system-requirements.html?lang=nl-NL#supported-browsers) in de _Gids van de Installatie_.

## Detectie van browsermogelijkheden configureren

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Kies **[!UICONTROL Web]** in het linkerdeelvenster onder _[!UICONTROL General]_.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Browser Capabilities Detection]** sectie uit en doe het volgende:

   - Stel **[!UICONTROL Redirect to CMS-page if Cookies are Disabled]** in op `Yes` als u instructies wilt weergeven die aangeven hoe u de browser kunt configureren om cookies toe te staan.

   - Als u een banner boven de koptekst wilt weergeven wanneer JavaScript is uitgeschakeld in de browser van de gebruiker, stelt u **[!UICONTROL Show Notice if JavaScript is Disabled]** in op `Yes` .

   - Als u een banner boven de koptekst wilt weergeven wanneer Local Storage is uitgeschakeld in de browser van de gebruiker, stelt u **[!UICONTROL Show Notice if Local Storage is Disabled]** in op `Yes` .

   ![ Algemene configuratie - de opsporing van de mogelijkheden van Webbrowser ](../configuration-reference/general/assets/web-browser-capabilities-detection.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.
