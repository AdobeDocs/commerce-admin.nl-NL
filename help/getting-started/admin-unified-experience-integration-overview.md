---
title: Adobe Experience Cloud Integration for Commerce Admin
description: Leer over Admin verenigde de uitbreiding van de Ervaring die Handel met Experience Cloud integreert zodat de klanten tot de projecten van de Handel van de homepage van het Experience Cloud kunnen toegang hebben.
feature: Integration
exl-id: e3fb6337-c7d5-4b6f-8f4a-583697a1f2d2
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 0%

---

# Adobe Experience Cloud Integration for Commerce

{{ee-feature}}

{{$include /help/_includes/admin-unified-experience-beta-note.md}}

Integreer de projecten van Adobe Commerce met Experience Cloud door Admin Verenigde uitbreiding van de Ervaring toe te laten. Wanneer de integratie actief is, kunnen de beheerders tot de projecten van de Handel van Adobe Experience Cloud toegang hebben.

![Access Commerce vanaf de homepage van het Experience Cloud](./assets/admin-uex-home-page.png){width="700" zoomable="yes"}

## Beschikbare Commerce-projecten weergeven

De beheerders kunnen de projecten van de Handel bekijken die zij toestemming hebben om toegang te hebben door te selecteren **[!UICONTROL Commerce]** op de startpagina van het Experience Cloud.

![Werkruimte voor handelsprojecten op Experience Cloud](./assets/admin-uex-commerce-projects-home.png){width="700" zoomable="yes"}

De beheerders kunnen Admin en Storefront voor elk project van openen [!DNL Commerce Projects] en aanvullende informatie weergeven.

- **Homepage van de handels-winkelpagina Momentopname**—Momentopname van de startpagina van de storefront. Als een project veelvoudige websites heeft, toont de momentopname de homepage voor de standaardplaats.

- **[Projectnaam](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html)**—Identificeert de wolkenprojectomgeving voor de instantie. De projectnaam wordt standaard ingesteld op [Naam vertakking instellen](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/console-branches.html) in het wolkenproject. De projectnaam in het dialoogvenster [Unified Experience Store-configuratie-instellingen](admin-unified-experience-integration-manage.md#manage-the-integration-from-the-admin).

- **[Storefront-URL](../stores-purchase/store-urls.md)**—Geeft de basis-URL voor de standaardwebsite weer.

- **[Type omgeving](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html)**—Commerciële instanties die worden ingezet in een ontwikkelings- of testomgeving worden aangeduid met een [!UICONTROL Development] of [!UICONTROL Staging] label. Instanties zonder label worden geïmplementeerd in een productieomgeving.

- **Toegang tot Commerce Admin**—Open de beheerder door op **[!UICONTROL Open]**.

- **Toegang tot Storefront**—Open de winkel door **[!UICONTROL Open storefront]** in het menu Opties.

- **Snelle toegang tot geselecteerde projecten**—Selecteren **[!UICONTROL Add to Favorites]** van het optiemenu om een project aan toe te voegen [!UICONTROL Favorites] tab.

## Verificatiestroom

Wanneer de integratie van het Experience Cloud wordt toegelaten, gebruiken de beheerders het volgende werkschema om tot de projecten van de Handel voor authentiek te verklaren en toegang te hebben.

1. Meld u aan via de aanmeldpagina voor het Experience Cloud.

   ![Pagina Aanmelden bij Experience Cloud](./assets/admin-uex-experience-cloud-login.png){width="600" zoomable="yes"}

   De beheerders moeten binnen aan Experience Cloud met het bedrijfsprofiel van de Adobe voor de organisatie ondertekenen verbonden aan de instantie van de Handel. Zie [Profielen voor Adobe beheren](https://helpx.adobe.com/enterprise/using/manage-adobe-profiles.html).

1. Open op de startpagina van het Experience Cloud de [!UICONTROL Commerce Projects workspace] door **[!UICONTROL Open]**.

1. Heb toegang tot Admin voor een project door te selecteren **[!UICONTROL Open]**.

1. Selecteer op de pagina Aanmelden bij Adobe Commerce de optie **[!UICONTROL Sign in with Adobe ID]** om de verificatie te voltooien en de beheerder te openen.

   ![Adobe Commerce-aanmeldpagina](./assets/admin-adobeid-login.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Zie [De integratie van Experiencen Cloud beheren](admin-unified-experience-integration-manage.md) voor meer informatie over hoe de authentificatiewerkstroom wordt beïnvloed wanneer de Experience Cloud integratie wordt toegelaten of onbruikbaar gemaakt.

## Vereisten

- Adobe Commerce 2.4.5 of hoger
- Adobe Commerce over cloudinfrastructuur
- Adobe Commerce-extensies

   - Commerce Admin Unified Experience Extension (`magento/module-unified-experience`)

     Als de module niet beschikbaar op de instantie van de Handel is, kan het worden geïnstalleerd gebruikend Composer.

   - [Adobe I/O Events, service](https://developer.adobe.com/commerce/extensibility/events/)—Vereist om gebeurtenisgegevens te verzenden om beheerdertoegang tot de projecten van de Handel van Experience Cloud te beheren.

     De integratie van de Gebeurtenissen van Adobe I/O met Handel wordt toegelaten door de uitbreiding van de Gebeurtenis van de Handel (`magento/commerce-eventing`) dat beschikbaar is in Adobe Commerce 2.4.4 en latere versies.

## Integratie inschakelen

Integratie inschakelen door de instructies op te volgen voor [Vorm de Integratie van het Experience Cloud met Commerce Admin](admin-unified-experience-integration-configure.md).

>[!TIP]
>
>Als de integratie van het Experience Cloud reeds op de instantie van de Handel wordt toegelaten, zie [De integratie van Experiencen Cloud beheren](admin-unified-experience-integration-manage.md) voor details over het veranderen van of het bijwerken van de configuratie, het beheren van beheerdertoegang, en het oplossen van problemen.
