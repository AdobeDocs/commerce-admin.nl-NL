---
title: AEM Assets-integratie instellen
description: Meer informatie over de vereisten en stappen voor het opzetten van de integratie tussen Adobe Commerce en AEM Assets as a Cloud Service.
feature: CMS, Media, Configuration, Integration
source-git-commit: df21ea9a797a4f11d0104cf34134ced3bbabbdf4
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---


# AEM Assets-integratie instellen

Schakel geavanceerde mogelijkheden voor middelenbeheer in door uw AEM Assets-omgeving in te stellen en de AEM Assets-integratie voor Commerce te installeren en te configureren.

Wanneer de integratie actief is, kunnen beheerders Experience Manager Assets as a Cloud Service gebruiken als enige bron van waarheid voor het creëren en beheren van bedrijfsmiddelen, en als centraal hulpmiddel van het beheer van digitale activa (DAM) om activa voor de projecten van Commerce te creëren, te beheren, te organiseren en te verdelen.

## Vereisten

- Adobe Commerce 2.4.5+
   - PHP 8.1, 8.2, 8.3
   - Composer: 2.x
- Adobe Experience Manager wordt provisioned met [ Adobe Experience Manager Assets as a Cloud Service ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/overview)
- De gebruiker die van Adobe Commerce de integratie vormt moet toegang tot de [ IMS Organisatie ](https://experienceleague.adobe.com/en/docs/core-services/interface/administration/organizations#concept_EA8AEE5B02CF46ACBDAD6A8508646255) hebben waar het project van AEM Assets provisioned is.

## Integratie instellen

>[!BEGINSHADEBOX]

**Eerste vereisten**

Voor het instellen van de AEM Assets-integratie is beheerderstoegang vereist om de toepassings- en omgevingsconfiguratie aan te passen.

- Administratieve toegang tot het Cloud Manager-programma waar de as a Cloud Service AEM Assets-omgevingen zijn ingericht.
- Beheerbare toegang tot de Adobe Commerce-omgeving en mogelijkheid om API-sleutels op te halen of te genereren die vereist zijn voor verificatie.

>[!ENDSHADEBOX]

De integratie van Commerce met Experience Manager Assets mogelijk maken is een driestappenproces:

1. [ vorm uw project van Experience Manager Assets om de activa van Commerce te beheren ](aem-assets-configure-aem.md).

1. [ installeer de uitbreiding van de Integratie van Experience Manager Assets en vorm Adobe Commerce ](aem-assets-configure-aem.md).

1. [ laat activasynchronisatie ](aem-assets-setup-synchronization.md) toe.
