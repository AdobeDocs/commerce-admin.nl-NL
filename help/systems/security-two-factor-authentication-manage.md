---
title: 2-voudige verificatie beheren
description: Leer hoe u verificatie met twee factoren beheert en de authenticators voor Admin-gebruikers opnieuw instelt.
exl-id: 68256214-2d50-4c42-846f-306ffc305f25
role: Admin
feature: Configuration, Security, User Account
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---

# 2-voudige verificatie beheren

Gebruikers die zich niet kunnen aanmelden bij de _Beheerder_ met tweevoudige verificatie (2FA) kan proberen het probleem te synchroniseren of problemen op te lossen. U kunt ook de verificateurs herstellen die aan het account zijn gekoppeld. Wanneer teruggesteld, moet de gebruiker opnieuw binnen ondertekenen en de vereiste authentificators opnieuw vormen.

Als u zich niet kunt aanmelden met 2FA, kunt u het volgende overwegen:

- Sommige mobiele apps bevatten synchronisatieopties. Met deze optie maakt u opnieuw verbinding met de app en de server en synchroniseert u de tijdinstellingen op het apparaat en de server.
- Als u een apparaat intrekt of een verificator opnieuw instelt, kunnen gebruikers gemakkelijker verbinding maken.
- Ook het wissen van webcache en cookies voor de installatie van Adobe Commerce of Magento Open Source kan hierbij helpen. Authenticatoren gebruiken, net als Google, gegenereerde cookies om toegang en duur op te slaan. Wis de koekjes voor uw specifieke browser en opslagdomein.
- Door het blokkeren van cookies worden sommige authenticatoren voorkomen, zoals [!DNL Google Authenticator], na voltooiing van het verificatieproces. Voeg een regel toe aan uw browser die cookies toestaat voor uw Adobe Commerce-installatie.

Om authentificators van de bevellijn en meer geavanceerde het oplossen van problemeninformatie terug te stellen, zie [Verificatie met twee factoren](https://developer.adobe.com/commerce/testing/functional-testing-framework/two-factor-authentication/) in de ontwikkelaarsdocumentatie.

**_Om authentificators voor een gebruikersrekening terug te stellen:_**

>[!NOTE]
>
>Als u 2FA-providers wilt herstellen voor andere gebruikers, moet u een _beheerder_ with `All` of beschikken over `Custom` machtigingen voor uw rol met [!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL Two Factor Auth] en [!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL All Users] geselecteerd. Zie voor meer informatie [Gebruikersrollen](permissions-user-roles.md).

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. Selecteer de gebruiker en open de account in de bewerkingsmodus.

1. Omlaag schuiven naar de _[!UICONTROL Current User Identity Verification]_en voer uw wachtwoord in.

1. Klik in het linkerdeelvenster op **[!UICONTROL 2FA]**.

1. In de _[!UICONTROL Configuration reset]_sectie, klikken **[!UICONTROL Reset]**en **[!UICONTROL OK]**ter bevestiging.

   ![Gebruikersaccount - 2FA inschakelen](./assets/admin-2fa-config-reset-providers.png){width="600" zoomable="yes"}

   Als de gebruiker de vereiste 2FA-methoden wil herstellen naar zijn of haar account, moet hij of zij elk opnieuw configureren vanuit de _Aanmelden_ pagina.

1. Klik op **[!UICONTROL Save User]**.
