---
title: Geplande productupdates
description: Leer hoe u wijzigingen in uw productaanbiedingen kunt plannen ter ondersteuning van campagnes en promotieprogramma's.
exl-id: ce1aebe6-9032-438d-b950-4b13116b8ed3
feature: Catalog Management, Products
source-git-commit: 2cdf3452f1648dc1ed607d6dfb5ade4be5ed5ce9
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 0%

---

# Productupdates plannen

{{ee-feature}}

Productupdates kunnen volgens schema worden toegepast en met andere inhoudsveranderingen worden gegroepeerd. U kunt [&#x200B; inhoud gebruiken die &#x200B;](../content-design/content-staging.md) staging om een campagne tot stand te brengen die op geplande veranderingen in het product wordt gebaseerd, of de veranderingen op een bestaande campagne toe te passen.

Houd rekening met het volgende wanneer u schema&#39;s voor productupdates en bewerkingscampagnes configureert:

- Alle geplande updates worden opeenvolgend toegepast, wat betekent dat elke entiteit slechts één geplande update tegelijk kan hebben. Elke geplande update wordt toegepast op alle winkelweergaven binnen de opgegeven tijdsperiode. Dientengevolge, kan een entiteit verschillende geplande updates voor verschillende opslagmeningen niet tezelfdertijd hebben. Alle waarden van entiteitattributen binnen alle opslagmeningen, die niet door de huidige geplande update worden beïnvloed, worden genomen van de standaardwaarden, en niet van de vorige geplande update.

- Een het opvoeren voorproef voor een geplande update begint altijd van de **standaard** opslagmening, die de ervaring van de klant navigeert om door de het opvoeren updatecampagne te navigeren.

- Als een campagne met meer dan één product wordt verbonden, kan de campagne slechts van het [&#x200B; Inhoud Staging Dashboard &#x200B;](../content-design/content-staging-dashboard.md) worden uitgegeven.

- Als een actieve campagne in eerste instantie zonder einddatum wordt gemaakt, kan de campagne later niet worden bewerkt om een einddatum op te nemen. In dat geval moet een dubbele campagne worden gemaakt en moet de gewenste einddatum worden ingevoerd.


>[!NOTE]
>
>[!UICONTROL Set Product as New From] en [!UICONTROL To] gebieden en [!UICONTROL Schedule Design Update] lusje zijn verwijderd in ![&#x200B; Adobe Commerce &#x200B;](../assets/adobe-logo.svg) Adobe Commerce en kunnen niet direct op het product worden gewijzigd. U moet een geplande update maken voor deze activeringen.

## Een geplande update maken

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Selecteer een bestaand product en klik op **[!UICONTROL Edit]** .

1. Klik op **[!UICONTROL Schedule New Update]**.

1. Selecteer **[!UICONTROL Save as a New Update]** .

1. Voer bij **[!UICONTROL Update Name]** een naam in voor de nieuwe campagne voor het opslaan van inhoud.

1. Voer een korte **[!UICONTROL Description]** in van de update en hoe deze moet worden gebruikt.

1. Gebruik het hulpmiddel van de Kalender (![&#x200B; kalenderpictogram &#x200B;](../assets/icon-calendar.png)) om **[!UICONTROL Start Date]** en **[!UICONTROL End Date]** voor de campagne te kiezen.

   >[!NOTE]
   >
   >De campagne **[!UICONTROL Start Date]** en **[!UICONTROL End Date]** moeten worden bepaald door de **_standaard_** tijdzone Admin te gebruiken, die van de lokale tijdzone voor elke website wordt omgezet. Als u bijvoorbeeld meerdere websites in verschillende tijdzones hebt waarin u een campagne wilt starten op basis van een Amerikaanse tijdzone, moet u een afzonderlijke update voor elke lokale tijdzone plannen. Stel **[!UICONTROL Start Date]** en **[!UICONTROL End Date]** in voor elke waarde en deze wordt omgezet van de tijdzone van de lokale website naar de standaardtijdzone van Admin.

   ![&#x200B; Programma als nieuwe update &#x200B;](./assets/product-schedule-as-new.png){width="600" zoomable="yes"}

1. Schuif omlaag naar _[!UICONTROL Price]_&#x200B;en klik op **[!UICONTROL Advanced Pricing]**.

1. Voer een **[!UICONTROL Special Price]** voor het product in tijdens de geplande campagne en klik op **[!UICONTROL Done]** .

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

## Toewijzen aan bestaande update

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Selecteer een bestaand product en klik op **[!UICONTROL Edit]** .

1. Klik op **[!UICONTROL Schedule New Update]**.

1. Selecteer **[!UICONTROL Assign to Existing Campaign]** .

1. Selecteer in de lijst de campagne die u wilt wijzigen.

   ![&#x200B; Toewijzend aan een bestaande campagne &#x200B;](./assets/scheduled-changes-assign-to-existing-campaign.png){width="600" zoomable="yes"}

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) **[!UICONTROL Content]** uit.

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

## De geplande wijziging weergeven

De geplande wijziging wordt boven aan de productpagina weergegeven met de begin- en einddatum van de campagne.

![&#x200B; Geplande verandering &#x200B;](./assets/view-product-scheduled-changes.png){width="600" zoomable="yes"}

## De geplande wijziging bewerken

1. Klik in het vak _[!UICONTROL Scheduled Changes]_&#x200B;boven aan de pagina op **[!UICONTROL View/Edit]**.

1. Breng de benodigde wijzigingen aan in de geplande update.

1. Klik op **[!UICONTROL Save]**.

## De geplande wijziging verwijderen

1. Klik in het vak _[!UICONTROL Scheduled Changes]_&#x200B;boven aan de pagina op **[!UICONTROL View/Edit]**.

1. Klik op **[!UICONTROL Remove from Update]** op de bovenste balk.

   ![&#x200B; verwijdert Geplande Verandering &#x200B;](./assets/remove-product-scheduled-changes.png){width="600" zoomable="yes"}

1. Selecteer **[!UICONTROL Delete the Update]** in het dialoogvenster en klik op **[!UICONTROL Done]** .

   Het product wordt verwijderd uit de update en alle geplande wijzigingen gaan verloren.

## Een ontwerpupdate plannen

{{ce-feature}}

Met de sectie _[!UICONTROL Schedule Design Update]_&#x200B;kunt u tijdelijke wijzigingen aanbrengen in de weergave van de productpagina. U kunt ontwerpwijzigingen plannen voor een seizoen, voor speciale acties of alleen om de zaken vers te maken. De veranderingen van het ontwerp kunnen vooraf worden gepland, zodat gaan zij in werking, of_ druppel _, op uw bepaalde programma.

![&#x200B; Geplande Update van het Ontwerp &#x200B;](./assets/product-design-update-scheduled-ce.png){width="600" zoomable="yes"}


| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Schedule Update From/To] | Hiermee bepaalt u het datumbereik wanneer een aangepaste indeling wordt toegepast op het product. |
| [!UICONTROL New Theme] | Hiermee past u een aangepast thema toe op het product. |
| [!UICONTROL New Layout] | Hiermee past u een andere indeling op de productpagina toe. Opties: <br/>**[!UICONTROL No layout updates]**- layout-updates zijn standaard niet beschikbaar voor de productpagina.<br/>**[!UICONTROL Empty]** - Hiermee kunt u uw eigen lay-out definiëren, zoals een pagina met vier kolommen. (Hiervoor is inzicht in XML vereist.) <br/>**[!UICONTROL 1 column]**- Hiermee past u een lay-out van één kolom toe op de productpagina.<br/>**[!UICONTROL 2 columns with left bar]** - Hiermee past u een lay-out met twee kolommen en een linkerzijbalk toe op de productpagina. <br/>**[!UICONTROL 2 columns with right bar]**- Hiermee past u een lay-out met twee kolommen en een rechterzijbalk toe op de productpagina.<br/>**[!UICONTROL 3 columns]** - Hiermee past u een indeling met drie kolommen toe op de productpagina. |

{style="table-layout:auto"}
