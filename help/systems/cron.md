---
title: Uitsnijden (geplande taken)
description: Leer hoe u de uitvoering en het plannen van de Bouwbanen van de Handel van Admin kunt controleren.
exl-id: e0da08ab-212f-4977-9387-0b4b40560cfb
feature: System, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Uitsnijden (geplande taken)

Adobe Commerce en Magento Open Source voeren sommige bewerkingen volgens schema uit door een script periodiek uit te voeren. U kunt de uitvoering en het plannen van de de bouwbanen van de Handel van Admin controleren. Opslagbewerkingen die worden uitgevoerd volgens een uitsnijdschema zijn onder meer:

- [E-mail](email-communications.md)
- [Catalogusprijsregels](../merchandising-promotions/price-rules-catalog.md)
- [Nieuwsbrieven](../merchandising-promotions/newsletters.md)
- [XML-itemapgeneratie](../merchandising-promotions/sitemap-xml.md)
- [Updates voor wisselkoersen](../stores-purchase/currency-update.md)
- [Inventory management](../inventory-management/introduction.md)

>[!IMPORTANT]
>
>De diensten van de handel moeten in contab worden geïnstalleerd om ervoor te zorgen dat de kerncomponenten, en sommige derdeuitbreidingen, aan werking zoals verwacht. Zie de [in de _Installatiehandleiding_](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/configuration.html) voor gedetailleerde informatie over het installeren van de diensten aan crontab.

Daarnaast kunt u het volgende configureren om volgens een uitsnijdschema te worden uitgevoerd:

- Updates en opnieuw indexeren van systeemrasters ordenen
- Betalingslevensduur in behandeling

Zorg ervoor dat de [basis-URL&#39;s](../stores-purchase/store-urls.md) voor de opslag correct zijn ingesteld, zodat de URL&#39;s die tijdens uitsnijdbewerkingen worden gegenereerd, correct zijn. Voor Adobe Commerce over cloud-infrastructuur raadpleegt u [Uitsnijdtaken instellen](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/app/properties/crons-property.html) in de _Handleiding voor handel in Cloud-infrastructuur_. Voor on-premise, zie [Pictogram configureren en uitvoeren](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html) in de _Configuratiegids_.

## Uitsnede configureren

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Advanced]** en kiest u **[!UICONTROL System]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Cron]** sectie.

   ![Geavanceerde configuratie - uitsnijdtaken](../configuration-reference/advanced/assets/system-cron.png){width="600" zoomable="yes"}

1. Vul de volgende instellingen in voor de **[!UICONTROL Index]** en **[!UICONTROL Default]** groepen.

   De instellingen zijn in elke sectie hetzelfde.

   - **[!UICONTROL Generate Schedules Every]** - Hiermee bepaalt u hoe vaak het schema wordt gegenereerd (in minuten). Planningen worden opgeslagen in de database.
   - **[!UICONTROL Schedule Ahead for]** - Hiermee bepaalt u hoe ver van tevoren de taken voor uitsnijden worden gepland (in minuten). Als deze instelling bijvoorbeeld is ingesteld op `10` en de kraan loopt uit , de kraan banen zijn gepland voor de komende 10 minuten .
   - **[!UICONTROL Missed if not Run Within]** - Definieert de tijd (in minuten) die wordt gebruikt om een gemiste taak te bepalen. Als de uitsnijdtaak niet op de geplande tijd wordt uitgevoerd en de opgegeven tijd verstreken is, kan deze niet worden uitgevoerd en wordt de status ingesteld op `Missed`.
   - **[!UICONTROL History Cleanup Every]** - Definieert de tijd (in minuten) dat de geschiedenis van voltooide taken uit de database wordt gewist.
   - **[!UICONTROL Success History Lifetime]** - Hiermee bepaalt u de tijdsduur (in minuten) dat de geschiedenis van bijtaken met een `Successful` status blijft in de database.
   - **[!UICONTROL Failure History Lifetime]** - Hiermee bepaalt u de tijdsduur (in minuten) dat de geschiedenis van bijtaken met een `Error` status blijft in de database.
   - **[!UICONTROL Use Separate Process]** - Hiermee wordt gedefinieerd of alle snijtaken van de groep in een afzonderlijk systeemproces worden uitgevoerd. Opties: `Yes` / `No`

   ![Geavanceerde configuratie - uitsnijdgroepindex](../configuration-reference/advanced/assets/system-cron-group-index.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]**.
