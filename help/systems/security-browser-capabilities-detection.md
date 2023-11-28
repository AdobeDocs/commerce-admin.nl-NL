---
title: Detectie van browsermogelijkheden
description: Leer hoe te om browser capaciteitsopsporing te vormen en een bericht te tonen als de browser van de klant montages moeten worden veranderd.
exl-id: 16caab8b-3ba5-43a1-a6f0-7c1e921be132
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 0%

---

# Detectie van browsermogelijkheden

Net als de meeste websites en toepassingen op internet, vereisen Adobe Commerce en Magento Open Source dat de browser van de bezoeker zowel cookies als JavaScript voor volledige bewerkingen toestaat. Soms wordt de browser van een gebruiker echter ingesteld op de hoogste privacy-instelling die zowel cookies als JavaScript voorkomt. Uw winkel kan worden geconfigureerd om de mogelijkheden van de browser van elke bezoeker te testen en een bericht weer te geven als de instellingen moeten worden gewijzigd.

- Als de privacyinstellingen van de browser cookies niet toestaan, kunt u het systeem zo configureren dat deze automatisch worden doorgestuurd naar de [Cookies inschakelen](../content-design/pages.md#enable-cookies) pagina, waarin wordt uitgelegd hoe u in de meeste browsers de aanbevolen instellingen kunt opgeven.
- Als JavaScript niet is toegestaan door de privacyinstellingen van de browser, kunt u het systeem zo configureren dat het volgende bericht boven de koptekst van elke pagina wordt weergegeven.

Voor technische informatie, zie [Ondersteunde browsers](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/system-requirements.html#supported-browsers) in de _Installatiehandleiding_.

## Detectie van browsermogelijkheden configureren

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. In het linkerdeelvenster onder _[!UICONTROL General]_, kiest u **[!UICONTROL Web]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Browser Capabilities Detection]** en voer de volgende handelingen uit:

   - Om instructies te tonen die verklaren hoe te browser vormen om koekjes toe te staan, plaats **[!UICONTROL Redirect to CMS-page if Cookies are Disabled]** tot `Yes`.

   - Als u een banner boven de koptekst wilt weergeven wanneer JavaScript is uitgeschakeld in de browser van de gebruiker, stelt u **[!UICONTROL Show Notice if JavaScript is Disabled]** tot `Yes`.

   - Als u een banner boven de koptekst wilt weergeven wanneer Lokale opslag is uitgeschakeld in de browser van de gebruiker, stelt u **[!UICONTROL Show Notice if Local Storage is Disabled]** tot `Yes`.

   ![Algemene configuratie - detectie van de mogelijkheden van webbrowsers](../configuration-reference/general/assets/web-browser-capabilities-detection.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]**.
