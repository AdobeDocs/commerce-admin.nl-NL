---
title: Commerce Admin Integration met ID configureren
description: Volg deze optionele procedure voor het integreren van Adobe Commerce Admin-gebruikersaccountaanmeldingen met Adobe ID.
exl-id: 518b7c21-e6b3-47d7-81a5-c34fbe0f197c
feature: Identity Management
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/nl/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: e1518775bf43f5493b61d21951a0b1126dfc49aa
workflow-type: tm+mt
source-wordcount: '875'
ht-degree: 0%

---

# De integratie van Commerce Admin met Adobe ID configureren

{{ee-feature}}

Deze integratie ondersteunt Commerce-handelaren met Admin-gebruikers die een Adobe ID hebben en die hun aanmelding bij Adobe Commerce- en Adobe Business-producten willen stroomlijnen. Het is optioneel en wordt per geval ingeschakeld. Alleen de workflows van de Admin-gebruiker worden beïnvloed wanneer deze worden ingeschakeld. 

>[!IMPORTANT]
>
>De integratie met AdobeIms wordt globaal toegepast. Zodra deze optie is ingeschakeld, moeten alle gebruikers zich verifiëren via AdobeIms. Individuele gebruikers kunnen niet van deze configuratie worden uitgesloten, en gebruikersbenaming en wachtwoordlogin is niet meer beschikbaar voor individuele gebruikers.
>
>Admin-gebruikers moeten hun Commerce Admin-gegevens (gebruikersnaam en wachtwoord) en 2FA-gegevens opslaan voordat ze deze integratie kunnen inschakelen. Deze referenties zijn vereist als de IMS-integratie is uitgeschakeld.

## Vereisten

* Adobe Commerce 2.4.5 of hoger
* Een Adobe.com rekening met toegang tot [&#x200B; Adobe Admin Console &#x200B;](https://adminconsole.adobe.com/).

  >[!NOTE]
  >
  >Als u geen toegang hebt tot de Adobe Commerce Admin Console, dient u een verzoek in bij uw accountteam om toegang te verlenen.

De beheerder die deze integratie vormt vereist de volgende geloofsbrieven tijdens moduleenactivering:

* Identiteitskaart van de organisatie (die uit [&#x200B; wordt verkregen Adobe Admin Console &#x200B;](https://adminconsole.adobe.com/)), die minstens 24 karakters in lengte moet zijn. De geverifieerde gebruiker moet deel uitmaken van deze IMS-organisatie. Voor informatie over het vinden van uw organisatie identiteitskaart, zie [&#x200B; Organisaties in Experience Cloud &#x200B;](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=nl-NL).
* 2FA moet op het niveau van de Organisatie in Adobe Admin Console worden gehandhaafd om de module toe te laten. Controle [&#x200B; de montages van de Authentificatie &#x200B;](https://helpx.adobe.com/nl/enterprise/using/authentication-settings.html#two-step-verification).
* Client-id
* Clientgeheim
* Identiteitskaart van de cliënt en cliëntgeheim zijn beschikbaar na het terugwinnen van API sleutels van [&#x200B; Adobe Developer Console &#x200B;](https://developer.adobe.com/developer-console/docs/guides/credentials).

Gebruikers van Commerce Admin moeten een account met een Adobe ID maken om zich aan te melden.

## Algemene stappen

* Krijg Adobe Org identiteitskaart van [&#x200B; Adobe Admin Console &#x200B;](https://adminconsole.adobe.com/)
* Produceer een nieuw project, IMS API sleutels, en geheim van [&#x200B; Adobe Developer Console &#x200B;](https://developer.adobe.com/)
* Adobe Commerce-gebruikers configureren in de Adobe Admin Console
* Schakel de module `AdminAdobeIms` in.

Voor een geslaagde integratie moeten alle Adobe Commerce-gebruikers beschikken over Admin-gebruikersaccounts met dezelfde naam en hetzelfde primaire e-mailadres. Als een passende Admin gebruikersrekening niet bestaat, moet een gebruiker met de vereiste toestemmingen (typisch toegewezen de rol van de Beheerder) manueel [&#x200B; tot de Admin gebruikersrekening &#x200B;](../systems/permissions-users-all.md#create-a-user) met de zelfde naam en e-mail leiden.

## De integratie configureren

Nadat de volgende stappen zijn uitgevoerd door een beheerder of ontwikkelaar met systeemtoegang, wordt de knop _[!UICONTROL Sign into Adobe Commerce with Adobe IMS]_&#x200B;weergegeven op de aanmeldingspagina voor Commerce Admin voor alle Admin-gebruikers.

### Stap 1: Adobe-organisatie-id ophalen

Lidmaatschap in ten minste één IMS-organisatie is vereist om deze functie in te schakelen. Als u een Adobe ID hebt, behoort u standaard tot minstens één Adobe-organisatie. Login aan [&#x200B; Adobe Admin Console &#x200B;](https://adminconsole.adobe.com/) om uw organisatieidentiteitskaart terug te winnen

### Stap 2: Genereer een nieuw project, de sleutels IMS API en geheim

Om projecten voor een organisatie tot stand te brengen, moet de rekening van Adobe Admin voor de organisatie de systeembeheerder of ontwikkelaarrol hebben. Zie de [&#x200B; Gids van Developer Console &#x200B;](https://developer.adobe.com/developer-console/docs/guides/projects/).

1. Login aan [&#x200B; Adobe Developer Console &#x200B;](https://developer.adobe.com/).
1. Ga naar het tabblad **[!UICONTROL Projects]** (adobe.io/projects) en klik op **[!UICONTROL Create a new project]** .
1. Klik op **[!UICONTROL Add API]** op de nieuwe projectpagina.
1. Selecteer **[!UICONTROL Adobe Services]** > **[!UICONTROL Adobe Commerce with Adobe ID]** .
1. Selecteer **[!UICONTROL Oauth 2.0 Web]** .
1. Geef de waarde **[!UICONTROL Redirect URI]** op: `https://<commerce_base_url>/`
1. Geef de waarde **[!UICONTROL Redirect URI pattern]** op: `https://<commerce_base_url>/.*`

   U kunt punten in de hostnaam laten springen door vóór de punten `\\` te gaan. Als u een jokerteken toevoegt aan het einde van de URL, wordt de geheime sleutel Adobe Commerce Admin ondersteund.

1. Klik op **[!UICONTROL Save configured API]**.
1. Kopieer de toetsen [!UICONTROL Client ID] en [!UICONTROL Client Secret] van het gemaakte project.

### Stap 3: Adobe Commerce-gebruikers configureren in de Adobe Admin Console

Voordat u de integratie inschakelt, controleert u of elke Adobe Commerce Admin-gebruikersaccount een overeenkomende Adobe IMS-account heeft. Adobe Commerce-gebruikers moeten tot een specifieke Adobe-organisatie behoren om zich aan te melden met een Adobe ID.

>[!TIP]
>
>U kunt meerdere gebruikersaccounts maken door de gebruikersgegevens van een CSV-bestand te uploaden. Zie [&#x200B; veelvoudige gebruikers beheren &#x200B;](https://helpx.adobe.com/nl/enterprise/using/bulk-upload-users.html).

1. In [&#x200B; Adobe Admin Console &#x200B;](https://helpx.adobe.com/nl/enterprise/using/admin-console.html), navigeer aan **[!UICONTROL Users]** > **[!UICONTROL Users]**.

1. Klik op **[!UICONTROL Add User]**.

1. Voer het e-mailadres van de gebruiker in.

   Indien van toepassing wordt het aanbevolen ID-type automatisch ingevuld. U kunt deze instelling wijzigen in een van de product-id&#39;s in de lijst. Deze is gebaseerd op het aankoopplan van uw organisatie.

   U kunt maximaal tien gebruikers tegelijk toevoegen. Als u meer wilt toevoegen, herhaalt u de voorgaande stappen nadat u de wijzigingen hebt opgeslagen.

1. Klik op **[!UICONTROL Save]**.

De gebruiker wordt toegevoegd en weergegeven in de lijst [!UICONTROL Users] .

### Stap 4: De module AdminAdobeIms inschakelen

De module `AdminAdobeIms` is verantwoordelijk voor de integratie tussen Adobe Commerce en Adobe IMS. Nadat u het nieuwe project hebt ingesteld en uw organisatie-id, client-id en clientgeheim hebt gekopieerd, kunt u de module `AdminAdobeIms` inschakelen.

Voer `bin/magento admin:adobe-ims:enable` in. U wordt gevraagd de volgende parameters in te voeren. Gebruik de waarden die zijn gegenereerd tijdens het maken van een project.

* Organisatie-id
* Client-id
* Clientgeheim
* 2FA ingeschakeld

Adobe Commerce geeft een bericht weer dat aangeeft of de activering is geslaagd of mislukt.

Nadat deze functie is ingeschakeld, kunt u andere Adobe Commerce-gebruikersaccounts overzetten naar Adobe IMS-accounts. Adobe Commerce-gebruikers moeten tot de geconfigureerde Adobe-organisatie behoren om zich aan te melden met een Adobe ID.

## Identiteit en eenmalige aanmelding

Voor informatie over de opties van de identiteitsconfiguratie met inbegrip van Adobe ID, Enterprise ID, en Federated ID, en instructies voor het vormen Enige Sign-On (SSO) voor veilige toegang tot Adobe apps, zie [&#x200B; de identiteit van de Opstelling en Enige Sign-On &#x200B;](https://helpx.adobe.com/nl/enterprise/using/set-up-identity.html) in de *Admin Console van de Onderneming* documentatie.
