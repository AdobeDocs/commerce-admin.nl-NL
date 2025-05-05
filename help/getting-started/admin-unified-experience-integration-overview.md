---
title: Adobe Experience Cloud-integratie voor Commerce Admin
description: Leer over Admin verenigde de uitbreiding van de Ervaring die Commerce met Experience Cloud integreert zodat de klanten tot de projecten van Commerce van de homepage van het Experience Cloud kunnen toegang hebben.
feature: Integration
exl-id: e3fb6337-c7d5-4b6f-8f4a-583697a1f2d2
source-git-commit: 61874f3dac4f574ad393e8ae258f3d6c56c8f37e
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---

# Adobe Experience Cloud-integratie voor Commerce

<table style="border:1px solid red">
<tr><td><img alt="Adobe Commerce-functie" src="../assets/adobe-logo.svg" width="20" height="20" /> De exclusieve eigenschap slechts in Adobe Commerce (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html?lang=nl-NL#product-editions"> leert meer </a>)</td></tr>
</table>

Integreer de projecten van Adobe Commerce met Experience Cloud door Admin Verenigde uitbreiding van de Ervaring toe te laten. Als de integratie actief is, hebben beheerders toegang tot Commerce-projecten vanuit Adobe Experience Cloud.

![ Toegang Commerce van de homepage van het Experience Cloud ](./assets/admin-uex-home-page.png){width="700" zoomable="yes"}

## Beschikbare Commerce-projecten weergeven

Beheerders kunnen Commerce-projecten bekijken waartoe ze toegang hebben door **[!UICONTROL Commerce]** te selecteren op de startpagina van het Experience Cloud.

![ de werkruimte van de Projecten van Commerce op Experience Cloud ](./assets/admin-uex-commerce-projects-home.png){width="700" zoomable="yes"}

Beheerders kunnen de opdrachten Admin en Storefront voor elk project openen vanuit de [!DNL Commerce Projects] -werkruimte en aanvullende informatie weergeven.

- **Momentopname van Commerce storefront homepage** - Momentopname van de storefront homepage. Als een project veelvoudige websites heeft, toont de momentopname de homepage voor de standaardplaats.

- **[naam van het Project ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html?lang=nl-NL)** - identificeert het milieu van het wolkenproject voor de instantie. De naam van het Project blijft aan de [ vertakkingsnaam van de it ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/console-branches.html?lang=nl-NL) in het wolkenproject in gebreke. Verandering of werk de projectnaam in de [ Verenigde montages van de de opslagconfiguratie van de Ervaring ](admin-unified-experience-integration-manage.md#manage-the-integration-from-the-admin) bij.

- **[opslag URL](../stores-purchase/store-urls.md)** - toont de basis URL voor de standaardwebsite.

- **[het type van Milieu ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html?lang=nl-NL)** - de instanties van Commerce die aan een ontwikkeling of het opvoeren milieu worden opgesteld worden geïdentificeerd met a [!UICONTROL Development] of [!UICONTROL Staging] etiket. Instanties zonder label worden geïmplementeerd in een productieomgeving.

- **toegang van Admin van Commerce** - open Admin door **[!UICONTROL Open]** te klikken.

- **toegang van de Storefront** - open de storefront door **[!UICONTROL Open storefront]** van het optiemenu te selecteren.

- **Snelle toegang tot uitgezochte projecten** - selecteer **[!UICONTROL Add to Favorites]** van het optiemenu om een project aan [!UICONTROL Favorites] tabel toe te voegen.

## Verificatiestroom

Wanneer de integratie van het Experience Cloud wordt toegelaten, gebruiken de beheerders het volgende werkschema om de projecten van Commerce voor authentiek te verklaren en toegang te hebben.

1. Meld u aan via de aanmeldpagina voor het Experience Cloud.

   ![ het Teken van het Experience Cloud binnen pagina ](./assets/admin-uex-experience-cloud-login.png){width="600" zoomable="yes"}

   Beheerders moeten zich aanmelden bij Experience Cloud met het bedrijfsprofiel van de Adobe voor de organisatie die is gekoppeld aan de Commerce-instantie. Zie [ de profielen van de Adobe beheren ](https://helpx.adobe.com/nl/enterprise/using/manage-adobe-profiles.html).

1. Open op de startpagina van het Experience Cloud de [!UICONTROL Commerce Projects workspace] door **[!UICONTROL Open]** te selecteren.

1. U kunt de beheerder van een project openen door **[!UICONTROL Open]** te selecteren.

1. Selecteer op de Adobe Commerce-pagina Aanmelden **[!UICONTROL Sign in with Adobe ID]** om de verificatie te voltooien en open Admin.

   ![ Adobe Commerce het Teken binnen pagina ](./assets/admin-adobeid-login.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Zie [ de Integratie van het Experience Cloud ](admin-unified-experience-integration-manage.md) voor details op beheren hoe het authentificatiewerkschema wordt beïnvloed wanneer de integratie van het Experience Cloud wordt toegelaten of onbruikbaar gemaakt.

## Vereisten

- Adobe Commerce 2.4.5 of hoger
- Adobe Commerce over cloudinfrastructuur
- Adobe Commerce-extensies

   - Commerce Admin Unified Experience Extension (`magento/module-unified-experience`)

     Als de module niet beschikbaar is op de Commerce-instantie, kan deze worden geïnstalleerd met Composer.

   - [ de dienst van Gebeurtenissen van Adobe I/O ](https://developer.adobe.com/commerce/extensibility/events/) - vereist om gebeurtenisgegevens te verzenden om beheerdertoegang tot de projecten van Commerce van Experience Cloud te beheren.

     De integratie van de Gebeurtenissen van de Adobe I/O met Commerce wordt toegelaten door de uitbreiding van de Gebeurtenis van Commerce (`magento/commerce-eventing`) die met Adobe Commerce 2.4.4 en recentere versies beschikbaar is.

## Integratie inschakelen

Laat de integratie toe door de instructies te volgen om [ de Integratie van het Experience Cloud met Commerce te vormen Admin ](admin-unified-experience-integration-configure.md).

>[!TIP]
>
>Als de integratie van het Experience Cloud reeds op de instantie van Commerce wordt toegelaten, zie [ de Integratie van het Experience Cloud ](admin-unified-experience-integration-manage.md) voor details over het veranderen van of het bijwerken van de configuratie, het beheren van beheerderstoegang, en het oplossen van problemen beheren.
