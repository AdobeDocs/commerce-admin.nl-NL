---
title: Ontwerpconfiguratie
description: De Configuratie van het Ontwerp maakt het gemakkelijk om op ontwerp betrekking hebbende regels en configuratiemontages uit te geven door de montages op één enkele pagina te tonen.
exl-id: 43fec57f-d76d-45a9-812b-ba1947cea46d
feature: Page Content, Configuration
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Ontwerpconfiguratie

De configuratie van het Ontwerp maakt het gemakkelijk om op ontwerp betrekking hebbende regels en configuratiemontages uit te geven door de montages op één enkele pagina te tonen.

![ pagina van de Configuratie van het Ontwerp ](./assets/configuration.png){width="700" zoomable="yes"}

## De ontwerpconfiguratie wijzigen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Zoek de winkelweergave die u wilt configureren en klik op **[!UICONTROL Edit]** in de kolom _[!UICONTROL Action]_.

   Op de pagina worden de huidige ontwerpinstellingen voor de winkelweergave weergegeven.

1. Als u het standaardthema wilt wijzigen, stelt u **[!UICONTROL Applied Theme]** in op het thema dat u op de weergave wilt toepassen.

   Als geen thema wordt gespecificeerd, wordt het systeemstandaardthema gebruikt. Sommige externe extensies wijzigen het standaardthema van het systeem.

1. Als het thema alleen voor een specifiek apparaat moet worden gebruikt, stelt u de **[!UICONTROL User Agent Rules]** in.

   ![ Gebruiker-Agent Regels ](./assets/configuration-user-agent-rules.png){width="400" zoomable="yes"}

   Voor elk apparatentype waar u een thema wilt specificeren:

   - Klik op **[!UICONTROL Add New User Agent Rule]**.

   - Voer bij **[!UICONTROL Search String]** de browser-id voor het specifieke apparaat in.

     Een onderzoekskoord kan of een normale uitdrukking of Perl Compatible Regular Uitdrukking (PCRE) (zie {de Agent van de Gebruiker 1} voor meer informatie) zijn. [](https://en.wikipedia.org/wiki/User_agent) De volgende zoekreeks identificeert Firefox:

         /^mozilla/i
     
   - Kies bij **[!UICONTROL Theme Name]** het thema dat voor het opgegeven apparaat moet worden gebruikt.

   >[!NOTE]
   >
   >U kunt zoveel regels toevoegen voor de apparaten die u wilt aanwijzen. De zoekreeksen komen overeen in de volgorde waarin ze worden ingevoerd.

1. Vouw onder _[!UICONTROL Other Settings]_elke sectie uit en volg de instructies in de gekoppelde onderwerpen om de instellingen naar wens te bewerken.

   - [[!UICONTROL Pagination]](../catalog/navigation-product-listings.md#pagination-controls)
   - [[!UICONTROL HTML Head]](page-setup.md#html-head)
   - [[!UICONTROL Header]](page-setup.md#header)
   - [[!UICONTROL Footer]](page-setup.md#footer)
   - [[!UICONTROL Search Engine Robots]](../merchandising-promotions/seo-overview.md#search-engine-robots)
   - [[!UICONTROL Product Image Watermarks]](../catalog/product-image.md#watermarks)
   - [[!UICONTROL Transactional Emails]](../systems/email-templates.md#configure-email-templates)

   ![ Andere montages om ontwerp ](./assets/configuration-other-settings.png){width="500" zoomable="yes"} te beïnvloeden

1. Klik op **[!UICONTROL Save Configuration]** als de bewerking is voltooid.
