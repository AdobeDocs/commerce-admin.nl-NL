---
title: Vorm de Integratie Admin van de Handel met identiteitskaart
description: Volg deze optionele procedure voor het integreren van Adobe Commerce Admin-gebruikersaccountaanmeldingen met Adobe ID.
exl-id: 518b7c21-e6b3-47d7-81a5-c34fbe0f197c
feature: Identity Management
source-git-commit: 20b2560ce2b8071c740907292544519f8b1c3ddf
workflow-type: tm+mt
source-wordcount: '758'
ht-degree: 1%

---

# De integratie van Commerce Admin met Adobe ID configureren

{{ee-feature}}

Deze integratie ondersteunt handelaars met Admin-gebruikers die een Adobe ID hebben en die hun aanmelding bij Adobe Commerce en Adobe Business-producten willen stroomlijnen. Het is optioneel en wordt per geval ingeschakeld. Alleen de workflows van de Admin-gebruiker worden beïnvloed wanneer deze worden ingeschakeld. 

>[!IMPORTANT]
>
>Admin-gebruikers moeten hun Admin-gebruikersgegevens (gebruikersnaam en wachtwoord) en 2FA-gegevens van Commerce opslaan voordat ze deze integratie kunnen inschakelen. Deze referenties zijn vereist als de IMS-integratie is uitgeschakeld.

## Vereisten

* Adobe Commerce 2.4.5 of hoger
* Een Adobe.com-account met toegang tot de [Adobe Admin Console](https://adminconsole.adobe.com/).

De beheerder die deze integratie vormt vereist de volgende geloofsbrieven tijdens moduleenactivering:

* Organisatie-id (verkregen uit [Adobe Admin Console](https://adminconsole.adobe.com/)), die minimaal 24 tekens lang moet zijn. De geverifieerde gebruiker moet deel uitmaken van deze IMS-organisatie. Voor informatie over het vinden van uw organisatie-id raadpleegt u [Organisaties in Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html).
* 2FA moet op het niveau van de Organisatie in Adobe Admin Console worden gehandhaafd om de module toe te laten. Controleren [Verificatieinstellingen](https://helpx.adobe.com/enterprise/using/authentication-settings.html#two-step-verification).
* Client-id
* Clientgeheim
* Client ID en clientgeheim zijn beschikbaar nadat API-sleutels zijn opgehaald uit de [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/credentials/).

De gebruikers van Admin van de handel moeten een rekening met een Adobe ID tot stand brengen login.

## Algemene stappen

* Adobe-id ophalen van de [Adobe Admin Console](https://adminconsole.adobe.com/)
* Genereer een nieuw project, de sleutels IMS API en geheim van het [Adobe Developer Console](https://developer.adobe.com/)
* De optie `AdminAdobeIms` module
* Adobe Commerce-gebruikers configureren in de Adobe Admin Console.

Voor een geslaagde integratie moeten alle Adobe Commerce-gebruikers beschikken over Admin-gebruikersaccounts met dezelfde naam en hetzelfde primaire e-mailadres. Als er geen overeenkomende Admin-gebruikersaccount bestaat, moet een gebruiker met de vereiste machtigingen (doorgaans met de rol Beheerder) handmatig [De Admin-gebruikersaccount maken](../systems/permissions-users-all.md#create-a-user) met dezelfde naam en e-mail.

## De integratie configureren

Nadat de volgende stappen door een beheerder of een ontwikkelaar met systeemtoegang worden voltooid, _[!UICONTROL Sign into Adobe Commerce with Adobe IMS]_Deze knop wordt weergegeven op de aanmeldingspagina voor Admin-gebruikers van Commerce.

### Stap 1: Adobe-ID ophalen

Lidmaatschap in ten minste één IMS-organisatie is vereist om deze functie in te schakelen. Als u een Adobe ID hebt, behoort u standaard tot minstens één Adobe organisatie. Aanmelden bij de [Adobe Admin Console](https://adminconsole.adobe.com/) om uw organisatie-id op te halen.

### Stap 2: Genereer een nieuw project, de sleutels IMS API en geheim

Om projecten voor een organisatie tot stand te brengen, moet de rekening Admin van de Adobe voor de organisatie de systeembeheerder of ontwikkelaarrol hebben. Zie de [Handleiding voor ontwikkelconsole](https://developer.adobe.com/developer-console/docs/guides/projects/).

1. Aanmelden bij [Adobe Developer Console](https://developer.adobe.com/).
1. Ga naar de **[!UICONTROL Projects]** tab (adobe.io/projects) en klik op **[!UICONTROL Create a new project]**.
1. Klikken **[!UICONTROL Add API]** op de nieuwe projectpagina.
1. Selecteren **[!UICONTROL Adobe Services]** > **[!UICONTROL Adobe Commerce with Adobe ID]**.
1. Selecteren **[!UICONTROL Oauth 2.0 Web]**.
1. Geef de **[!UICONTROL Redirect URI]**: `https://<hostname>/`
1. Geef de **[!UICONTROL Redirect URI pattern]**: `https://<hostname>/.*`

   Hiermee worden punten in de hostnaam genummerd door de punten met `\\`. Als u een jokerteken toevoegt aan het einde van de URL, wordt de geheime sleutel Adobe Commerce Admin ondersteund.

1. Klik op **[!UICONTROL Save configured API]**.
1. De [!UICONTROL Client ID] en [!UICONTROL Client Secret] van het gemaakte project.

### Stap 3: De module AdminAdobeIms inschakelen

De `AdminAdobeIms` is verantwoordelijk voor de integratie tussen Adobe Commerce en Adobe IMS. Nadat u het nieuwe project hebt ingesteld en uw organisatie-id, client-id en clientgeheim hebt gekopieerd, kunt u de optie `AdminAdobeIms` -module.

Enter `bin/magento admin:adobe-ims:enable`. U wordt gevraagd de volgende parameters in te voeren. Gebruik de waarden die zijn gegenereerd tijdens het maken van een project.

* Organisatie-id
* Client-id
* Clientgeheim
* 2FA ingeschakeld

Adobe Commerce geeft een bericht weer dat aangeeft of de activering is geslaagd of mislukt.

Nadat deze functie is ingeschakeld, kunt u andere Adobe Commerce-gebruikersaccounts overzetten naar Adobe IMS-accounts. Adobe Commerce-gebruikers moeten tot de geconfigureerde Adobe-organisatie behoren om zich aan te melden met een Adobe ID.

### Stap 4: Adobe Commerce-gebruikers configureren in de Adobe Admin Console

Nadat deze functie is ingeschakeld, kunt u andere Adobe Commerce-gebruikersaccounts overzetten naar Adobe IMS-accounts. Adobe Commerce-gebruikers moeten tot minstens één Adobe-organisatie behoren om zich aan te melden met een Adobe ID.

1. In de [Admin Console](https://helpx.adobe.com/nl/enterprise/using/admin-console.html), navigeer naar **[!UICONTROL Users]**  > **[!UICONTROL Users]**.

1. Klik op **[!UICONTROL Add User]**.

1. Voer het e-mailadres van de gebruiker in.

   Indien van toepassing wordt het aanbevolen ID-type automatisch ingevuld. U kunt deze instelling wijzigen in een van de product-id&#39;s in de lijst. Deze is gebaseerd op het aankoopplan van uw organisatie.

   U kunt maximaal tien gebruikers tegelijk toevoegen. Als u meer wilt toevoegen, herhaalt u de voorgaande stappen nadat u de wijzigingen hebt opgeslagen.

1. Klik op **[!UICONTROL Save]**.

De gebruiker wordt toegevoegd en weergegeven in het dialoogvenster [!UICONTROL Users] lijst.
