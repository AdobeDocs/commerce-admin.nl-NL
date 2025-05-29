---
title: 2-voudige verificatie beheren
description: Leer hoe u verificatie met twee factoren beheert en de authenticators voor Admin-gebruikers opnieuw instelt.
exl-id: 68256214-2d50-4c42-846f-306ffc305f25
role: Admin
feature: Configuration, Security, User Account
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---

# 2-voudige verificatie beheren

De gebruikers die niet binnen aan _Admin_ met twee-factor authentificatie (2FA) kunnen ondertekenen proberen om het probleem te synchroniseren of problemen op te lossen. U kunt ook de verificateurs herstellen die aan het account zijn gekoppeld. Wanneer teruggesteld, moet de gebruiker opnieuw binnen ondertekenen en de vereiste authentificators opnieuw vormen.

Als u zich niet kunt aanmelden met 2FA, kunt u het volgende overwegen:

- Sommige mobiele apps bevatten synchronisatieopties. Met deze optie maakt u opnieuw verbinding met de app en de server en synchroniseert u de tijdinstellingen op het apparaat en de server.
- Als u een apparaat intrekt of een verificator opnieuw instelt, kunnen gebruikers gemakkelijker verbinding maken.
- Ook het wissen van webcache en cookies voor de Adobe Commerce- of Magento Open Source-installatie kan u helpen. Authenticatoren gebruiken, net als Google, gegenereerde cookies om toegang en duur op te slaan. Wis de koekjes voor uw specifieke browser en opslagdomein.
- Door het blokkeren van cookies voorkomt u dat sommige verificateurs, zoals [!DNL Google Authenticator], het verificatieproces voltooien. Voeg een regel toe aan uw browser die cookies toestaat voor uw Adobe Commerce-installatie.

Om authentificators van de bevellijn en meer geavanceerde het oplossen van problemeninformatie terug te stellen, zie [ Two-Factor Authentificatie ](https://developer.adobe.com/commerce/testing/functional-testing-framework/two-factor-authentication/) in de ontwikkelaarsdocumentatie.

**_om authentificators voor een gebruikersrekening terug te stellen:_**

>[!NOTE]
>
>Om 2FA leveranciers voor andere gebruikers terug te stellen, moet u een _beheerder_ met `All` toestemmingen zijn, of `Custom` toestemmingen voor uw rol hebben met [!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL Two Factor Auth] en [!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL All Users] geselecteerd. Meer leren, zie [ Rollen van de Gebruiker ](permissions-user-roles.md).

1. Voor _Admin_ sidebar, ga **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. Selecteer de gebruiker en open de account in de bewerkingsmodus.

1. Blader omlaag naar de sectie _[!UICONTROL Current User Identity Verification]_&#x200B;en voer uw wachtwoord in.

1. Klik in het linkerdeelvenster op **[!UICONTROL 2FA]** .

1. Klik in de sectie _[!UICONTROL Configuration reset]_&#x200B;op **[!UICONTROL Reset]**&#x200B;en **[!UICONTROL OK]**&#x200B;om te bevestigen.

   ![ rekening van de Gebruiker - laat 2FA ](./assets/admin-2fa-config-reset-providers.png){width="600" zoomable="yes"} toe

   Als de gebruiker de vereiste methodes 2FA aan hun rekening wil herstellen, moeten zij elk van de _Ondertekenen_ pagina opnieuw vormen.

1. Klik op **[!UICONTROL Save User]** als de bewerking is voltooid.
