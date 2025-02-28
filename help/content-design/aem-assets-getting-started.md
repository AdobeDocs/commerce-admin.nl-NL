---
title: AEM Assets Integration instellen voor Commerce
description: Leer hoe te aan boord van Experience Manager Assets met uw  [!DNL Commerce]  instantie om tot ontelbare media activa voor gebruik in uw opslag toegang te hebben.
feature: CMS, Media, Configuration
source-git-commit: c109edc9d9277baafd61da1df0f1917f07089353
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---

# AEM Assets Integration instellen voor Commerce

Voor het instellen van de AEM Assets-integratie is beheerderstoegang vereist om de toepassings- en omgevingsconfiguratie aan te passen.

- Administratieve toegang tot het Cloud Manager-programma waar de AEM Assets as a Cloud Service-omgevingen zijn ingericht.

- Beheerbare toegang tot de Adobe Commerce-omgeving en mogelijkheid om API-sleutels op te halen of te genereren die vereist zijn voor verificatie.

## Vereisten voor het gebruik van de integratie

Om van deze integratie te profiteren, moeten de ondernemingen aan de volgende vereisten voldoen:

- De actieve vergunningen voor Adobe Commerce, AEM Assets, en [ Dynamische Media van AEM ](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/dynamic/administering-dynamic-media).

- Adobe Commerce 2.4.5+

   - PHP 8.1, 8.2, 8.3
   - Composer: 2.x

- Adobe Experience Manager is provisioned met [ Adobe Experience Manager Assets as a Cloud Service ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/overview)

- De gebruiker die van Adobe Commerce de integratie vormt moet toegang tot de [ IMS Organisatie ](https://experienceleague.adobe.com/en/docs/core-services/interface/administration/organizations#concept_EA8AEE5B02CF46ACBDAD6A8508646255) hebben waar het project van AEM Assets provisioned is.

## Belangrijkste voordelen

- **Geen Extra Kosten** - Deze integratie wordt verstrekt kosteloos voor verkopers die aan de vergunningsvereisten voldoen.

- **Officiële Oplossing van Adobe** - ontwikkeld, gehandhaafd, en volledig gesteund door Adobe, die stabiliteit en groepering met toekomstige platformverhogingen verzekeren.

- **Adobe Beheerde Model van de Steun** - de hulp en het oplossen van problemen worden behandeld direct door Adobe, die vrede van mening en gestroomlijnde probleemresolutie verstrekt.

## Volgende stappen

De integratie van Commerce met Experience Manager Assets mogelijk maken is een driestappenproces:

1. [ vorm uw de activa van AEM project om de activa van Adobe Commerce te beheren ](aem-assets-configure-aem.md).

1. [ installeer de de montagesintegratieuitbreiding van AEM en vorm Adobe Commerce ](aem-assets-configure-aem.md).

1. [ laat activasynchronisatie ](aem-assets-setup-synchronization.md) toe.
