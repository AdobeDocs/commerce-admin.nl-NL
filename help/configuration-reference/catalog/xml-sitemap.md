---
title: '[!UICONTROL Catalog] &gt; [!UICONTROL XML Sitemap]'
description: Controleer de configuratie-instellingen op het tabblad [!UICONTROL Catalog] &gt; [!UICONTROL XML Sitemap] pagina van de Commerce Admin.
exl-id: 319c34e9-bd5f-46f8-810f-bc4d5228f9c9
feature: Configuration, Site Navigation
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 0%

---

# [!UICONTROL Catalog] > [!UICONTROL XML Sitemap]

{{config}}

## [!UICONTROL Categories Options]

![Categorieopties](./assets/xml-sitemap-categories-options.png)<!-- zoom -->

<!-- [Categories Options](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Frequency] | Winkelweergave | Bepaalt hoe vaak sitemapcategorieën worden bijgewerkt. Opties: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Winkelweergave | Een waarde tussen `0.0` en `1.0` Hiermee wordt de prioriteit bepaald van de sitemap-updates van de categorie ten opzichte van andere inhoud. Nul (`0.0`) heeft de laagste prioriteit. |

{style="table-layout:auto"}

## [!UICONTROL Products Options]

![Productopties](./assets/xml-sitemap-products-options.png)<!-- zoom -->

<!-- [Products Options](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Frequency] | Winkelweergave | Hiermee bepaalt u hoe vaak sitemapproducten worden bijgewerkt. Opties: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Winkelweergave | Een waarde tussen `0.0` en `1.0` dat de prioriteit van sitemap-updates voor producten ten opzichte van andere inhoud bepaalt. Nul (`0.0`) heeft de laagste prioriteit. |
| [!UICONTROL Add Images into Sitemap] | Winkelweergave | Hiermee bepaalt u in welke mate afbeeldingen in de sitemap worden opgenomen. Opties: `None` / `Base Only` / `All` |

{style="table-layout:auto"}

## [!UICONTROL CMS Pages Options]

![Opties voor CMS-pagina&#39;s](./assets/xml-sitemap-cms-pages-options.png)<!-- zoom -->

<!-- [CMS Pages Options](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Frequency] | Winkelweergave | Hiermee bepaalt u hoe vaak CMS-sitemap-pagina&#39;s worden bijgewerkt. Opties: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Winkelweergave | Een waarde tussen `0.0` en `1.0` Hiermee bepaalt u de prioriteit van sitemap-updates van CMS-pagina ten opzichte van andere inhoud. Nul (`0.0`) heeft de laagste prioriteit. |

{style="table-layout:auto"}

## [!UICONTROL Store Url Options]

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Frequency] | Winkelweergave | Hiermee bepaalt u hoe vaak URL&#39;s worden bijgewerkt. Opties: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Winkelweergave | Een waarde tussen `0.0` en `1.0` dat de prioriteit van opslag URL updates met betrekking tot andere inhoud bepaalt. Nul (`0.0`) heeft de laagste prioriteit. |

{style="table-layout:auto"}

## [!UICONTROL Generation Settings]

![Generatie-instellingen](./assets/xml-sitemap-generation-settings.png)<!-- zoom -->

<!-- [Generation Settings](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enabled] | Winkelweergave | Hiermee wordt bepaald of een XML-sitemap beschikbaar is voor de winkel. Opties: `Yes` / `No` |
| [!UICONTROL Start Time] | Winkelweergave | Geeft het uur, de minuut en de seconde aan van de dag waarop de sitemap wordt bijgewerkt. |
| [!UICONTROL Frequency] | Winkelweergave | Bepaalt hoe vaak de sitemap wordt bijgewerkt. Opties: `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Error Email Recipient] | Winkelweergave | Het e-mailadres van de persoon die een melding ontvangt als er een fout optreedt tijdens het updateproces van de sitemap. Voor veelvoudige adressen, scheidt elk met een komma. |
| [!UICONTROL Error Email Sender] | Website | Identificeert het opslagcontact dat als afzender van het foutenbericht verschijnt. Opties: `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Error Email Template] | Website | Identificeert het e-mailmalplaatje dat voor het foutenmelding wordt gebruikt. Standaardsjabloon: `Sitemap generate Warnings` |

{style="table-layout:auto"}

## [!UICONTROL Sitemap File Limits]

![Limieten voor Sitemap-bestanden](./assets/xml-sitemap-sitemap-file-limits.png)<!-- zoom -->

<!-- [Sitemap File Limits](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Maximum No of URLs Per File] | Winkelweergave | Hiermee wordt het maximum aantal URL&#39;s bepaald dat in één sitemap kan worden opgenomen. |
| [!UICONTROL Maximum File Size] | Winkelweergave | Bepaalt de maximumgrootte van de gegenereerde sitemap in bytes. |

{style="table-layout:auto"}

## [!UICONTROL Search Engine Submission Settings]

![Verzendinstellingen zoekmachine](./assets/xml-sitemap-search-engine-submission-settings.png)<!-- zoom -->

<!-- [Search Engine Submission Settings](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enable Submission to Robots.txt] | Winkelweergave | Hiermee kunt u instructies voor het bestand robots.txt indienen. Opties: `Yes` / `No` |

{style="table-layout:auto"}
