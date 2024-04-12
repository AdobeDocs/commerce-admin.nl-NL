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
<tr><td><img alt="Adobe Commerce-functie" src="../assets/adobe-logo.svg" width="20" height="20" /> Alleen exclusieve functie in Adobe Commerce (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">Meer informatie</a>)</td></tr>
</table>

Integreer de projecten van Adobe Commerce met Experience Cloud door Admin Verenigde uitbreiding van de Ervaring toe te laten. Als de integratie actief is, hebben beheerders toegang tot Commerce-projecten vanuit Adobe Experience Cloud.

![Commerce openen vanaf de startpagina van het Experience Cloud](./assets/admin-uex-home-page.png){width="700" zoomable="yes"}

## Beschikbare Commerce-projecten weergeven

Beheerders kunnen Commerce-projecten bekijken waartoe ze gemachtigd zijn door **[!UICONTROL Commerce]** op de startpagina van het Experience Cloud.

![De werkruimte Commerce Projecten op Experience Cloud](./assets/admin-uex-commerce-projects-home.png){width="700" zoomable="yes"}

De beheerders kunnen Admin en Storefront voor elk project van openen [!DNL Commerce Projects] en aanvullende informatie weergeven.

- **Momentopname van homepage van Commerce-winkel**—Momentopname van de startpagina van de storefront. Als een project veelvoudige websites heeft, toont de momentopname de homepage voor de standaardplaats.

- **[Projectnaam](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html)**—Identificeert de wolkenprojectomgeving voor de instantie. De projectnaam wordt standaard ingesteld op [Naam vertakking instellen](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/console-branches.html) in het wolkenproject. De projectnaam in het dialoogvenster [Unified Experience Store-configuratie-instellingen](admin-unified-experience-integration-manage.md#manage-the-integration-from-the-admin).

- **[Storefront-URL](../stores-purchase/store-urls.md)**—Geeft de basis-URL voor de standaardwebsite weer.

- **[Type omgeving](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html)**—Commerce-instanties die worden geïmplementeerd in een ontwikkelings- of testomgeving worden aangeduid met een [!UICONTROL Development] of [!UICONTROL Staging] label. Instanties zonder label worden geïmplementeerd in een productieomgeving.

- **Toegang tot Commerce Admin**—Open de beheerder door op **[!UICONTROL Open]**.

- **Toegang tot Storefront**—Open de winkel door **[!UICONTROL Open storefront]** in het menu Opties.

- **Snelle toegang tot geselecteerde projecten**—Selecteren **[!UICONTROL Add to Favorites]** van het optiemenu om een project aan toe te voegen [!UICONTROL Favorites] tab.

## Verificatiestroom

Wanneer de integratie van het Experience Cloud wordt toegelaten, gebruiken de beheerders het volgende werkschema om de projecten van Commerce voor authentiek te verklaren en toegang te hebben.

1. Meld u aan via de aanmeldpagina voor het Experience Cloud.

   ![Pagina Aanmelden bij Experience Cloud](./assets/admin-uex-experience-cloud-login.png){width="600" zoomable="yes"}

   Beheerders moeten zich aanmelden bij Experience Cloud met het bedrijfsprofiel van de Adobe voor de organisatie die is gekoppeld aan de Commerce-instantie. Zie [Profielen voor Adobe beheren](https://helpx.adobe.com/enterprise/using/manage-adobe-profiles.html).

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

     Als de module niet beschikbaar is op de Commerce-instantie, kan deze worden geïnstalleerd met Composer.

   - [Adobe I/O Events, service](https://developer.adobe.com/commerce/extensibility/events/)—Vereist om gebeurtenisgegevens te verzenden om beheerdertoegang tot de projecten van Commerce van Experience Cloud te beheren.

     De integratie van Adobe I/O Events met Commerce wordt ingeschakeld door de extensie Commerce Event (`magento/commerce-eventing`) dat beschikbaar is in Adobe Commerce 2.4.4 en latere versies.

## Integratie inschakelen

Integratie inschakelen door de instructies op te volgen voor [De integratie van het Experience Cloud configureren met Commerce Admin](admin-unified-experience-integration-configure.md).

>[!TIP]
>
>Als de integratie van het Experience Cloud al is ingeschakeld op de Commerce-instantie, raadpleegt u [De integratie van Experiencen Cloud beheren](admin-unified-experience-integration-manage.md) voor details over het veranderen van of het bijwerken van de configuratie, het beheren van beheerdertoegang, en het oplossen van problemen.
