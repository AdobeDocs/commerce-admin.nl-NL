---
title: Uitsnijden (geplande taken)
description: Leer hoe u de uitvoering en planning van Commerce-taken voor uitsnijden kunt regelen via Beheer.
exl-id: e0da08ab-212f-4977-9387-0b4b40560cfb
feature: System, Configuration
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/nl/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---

# Uitsnijden (geplande taken)

Adobe Commerce en Magento Open Source voeren een aantal bewerkingen op schema uit door een script periodiek uit te voeren. U kunt de uitvoering en planning van Commerce-taken voor uitsnijden bepalen via de beheerfunctie. Opslagbewerkingen die worden uitgevoerd volgens een uitsnijdschema zijn onder meer:

- [E-mail](email-communications.md)
- [Catalogusprijsregels](../merchandising-promotions/price-rules-catalog.md)
- [Nieuwsbrieven](../merchandising-promotions/newsletters.md)
- [XML-itemapgeneratie](../merchandising-promotions/sitemap-xml.md)
- [Updates voor wisselkoersen](../stores-purchase/currency-update.md)
- [Inventory management](../inventory-management/introduction.md)

>[!IMPORTANT]
>
>Commerce-services moeten op een tab worden geïnstalleerd om ervoor te zorgen dat kerncomponenten en bepaalde extensies van derden naar behoren werken. Zie de [&#x200B; instructies in de _Gids van de Installatie_ &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/configuration.html?lang=nl-NL) voor gedetailleerde informatie over het installeren van de diensten aan contab.

Daarnaast kunt u het volgende configureren om volgens een uitsnijdschema te worden uitgevoerd:

- Updates en opnieuw indexeren van systeemrasters ordenen
- Betalingslevensduur in behandeling

Zorg ervoor dat [&#x200B; basis URLs &#x200B;](../stores-purchase/store-urls.md) voor de opslag correct wordt geplaatst zodat URLs die tijdens kroonverrichtingen worden geproduceerd correct is. Voor Adobe Commerce op wolkeninfrastructuur, zie [&#x200B; de banen van de opstelling cron &#x200B;](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/app/properties/crons-property.html?lang=nl-NL) in _Commerce op de Gids van de Infrastructuur van de Wolk_. Voor op-gebouw, zie [&#x200B; en looppas pictogram &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html?lang=nl-NL) in de _Gids van de Configuratie_.

## Uitsnede configureren

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Advanced]** uit en kies **[!UICONTROL System]** .

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Cron]** sectie uit.

   ![&#x200B; Geavanceerde configuratie - bouwtaken &#x200B;](../configuration-reference/advanced/assets/system-cron.png){width="600" zoomable="yes"}

1. Voer de volgende instellingen in voor de groepen **[!UICONTROL Index]** en **[!UICONTROL Default]** .

   De instellingen zijn in elke sectie hetzelfde.

   - **[!UICONTROL Generate Schedules Every]** - Hiermee bepaalt u hoe vaak het schema wordt gegenereerd (in minuten). Planningen worden opgeslagen in de database.
   - **[!UICONTROL Schedule Ahead for]** - Hiermee bepaalt u hoe ver van tevoren de taken voor uitsnijden worden gepland (in minuten). Als deze instelling bijvoorbeeld is ingesteld op `10` en de uitsnede wordt uitgevoerd, worden de uitsnijdtaken gepland voor de volgende 10 minuten.
   - **[!UICONTROL Missed if not Run Within]** - Definieert de tijd (in minuten) die wordt gebruikt om een gemiste taak te bepalen. Als de uitsnijdtaak niet op de geplande tijd wordt uitgevoerd en de opgegeven tijd verstrijkt, kan deze niet worden uitgevoerd en wordt de status ervan ingesteld op `Missed` .
   - **[!UICONTROL History Cleanup Every]** - Definieert de tijd (in minuten) dat de geschiedenis van voltooide taken uit de database wordt gewist.
   - **[!UICONTROL Success History Lifetime]** - Hiermee bepaalt u de tijdsduur (in minuten) dat de geschiedenis van uitsnijdtaken met de status `Successful` in de database blijft.
   - **[!UICONTROL Failure History Lifetime]** - Hiermee bepaalt u de tijdsduur (in minuten) dat de geschiedenis van uitsnijdtaken met de status `Error` in de database blijft.
   - **[!UICONTROL Use Separate Process]** - Hiermee wordt gedefinieerd of alle snijtaken van de groep in een afzonderlijk systeemproces worden uitgevoerd. Opties: `Yes` / `No`

   ![&#x200B; Geavanceerde configuratie - de index van de cron groep &#x200B;](../configuration-reference/advanced/assets/system-cron-group-index.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.
