---
title: Ontwerpconfiguratie
description: De Configuratie van het Ontwerp maakt het gemakkelijk om op ontwerp betrekking hebbende regels en configuratiemontages uit te geven door de montages op één enkele pagina te tonen.
exl-id: 43fec57f-d76d-45a9-812b-ba1947cea46d
feature: Page Content, Configuration
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '351'
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

1. [!BADGE &#x200B; slechts PaaS &#x200B;]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."} als het thema voor slechts een specifiek apparaat moet worden gebruikt, plaats **[!UICONTROL User Agent Rules]**.

   ![ Gebruiker-Agent Regels ](./assets/configuration-user-agent-rules.png){width="400" zoomable="yes"}

   Voor elk apparatentype waar u een thema wilt specificeren:

   - Klik op **[!UICONTROL Add New User Agent Rule]**.

   - Voer bij **[!UICONTROL Search String]** de browser-id voor het specifieke apparaat in.

     Een onderzoekskoord kan of een normale uitdrukking of Perl Compatible Regular Uitdrukking (PCRE) (zie {de Agent van de Gebruiker 1} voor meer informatie) zijn. [&#128279;](https://en.wikipedia.org/wiki/User_agent) De volgende zoekreeks identificeert Firefox:

         /^mozilla/i
     
   - Kies bij **[!UICONTROL Theme Name]** het thema dat voor het opgegeven apparaat moet worden gebruikt.

   >[!NOTE]
   >
   >U kunt zoveel regels toevoegen voor de apparaten die u wilt aanwijzen. De zoekreeksen komen overeen in de volgorde waarin ze worden ingevoerd.

1. Vouw onder _[!UICONTROL Other Settings]_&#x200B;elke sectie uit en volg de instructies in de gekoppelde onderwerpen om de instellingen naar wens te bewerken.

   - [[!UICONTROL Pagination]](../catalog/navigation-product-listings.md#pagination-controls) [!BADGE &#x200B; slechts PaaS &#x200B;]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."}
   - [[!UICONTROL HTML Head]](page-setup.md#html-head) [!BADGE &#x200B; slechts PaaS &#x200B;]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."}
   - [[!UICONTROL Header]](page-setup.md#header) [!BADGE &#x200B; slechts PaaS &#x200B;]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."}
   - [[!UICONTROL Footer]](page-setup.md#footer) [!BADGE &#x200B; slechts PaaS &#x200B;]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."}
   - [[!UICONTROL Search Engine Robots]](../merchandising-promotions/seo-overview.md#search-engine-robots) [!BADGE &#x200B; slechts PaaS &#x200B;]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."}
   - [[!UICONTROL Product Image Watermarks]](../catalog/product-image.md#watermarks)
   - [[!UICONTROL Transactional Emails]](../systems/email-templates.md#configure-email-templates)

   ![ Andere montages om ontwerp ](./assets/configuration-other-settings.png){width="500" zoomable="yes"} te beïnvloeden

1. Klik op **[!UICONTROL Save Configuration]** als de bewerking is voltooid.
