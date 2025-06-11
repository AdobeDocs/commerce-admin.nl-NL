---
title: Logrotatie configureren
description: Configureer logrotatie voor de AEM Assets Integration voor Commerce.
feature: CMS, Media, Integration
exl-id: f735d086-048c-4555-bc58-ac6736c281b0
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# Experience Manager Assets configureren

AEM Assets Integration for Commerce biedt de volgende logbestanden in uw Commerce-instantie:

- `/var/log/aem-assets-integration.log`
- `/var/log/aem-assets-integration-errors.log`

Vraag uw systeembeheerder om het rotatieschema van het logbestand voor deze logbestanden te controleren om te voorkomen dat deze te groot worden. In sommige omgevingen worden de logbestanden automatisch geroteerd, maar in andere omgevingen moet u de logrotatie handmatig instellen. Raadpleeg de volgende onderwerpen voor meer informatie:

- Voor Adobe Commerce op-gebouw installaties, vraag uw Beheerder van het Systeem aan opstelling [ logboekomwenteling ](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/configuration.html#server-settings).
- Voor Adobe Commerce op de projecten van de wolkeninfrastructuur, zie [ Mening en beheer logboeken ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/test/log-locations.html).
