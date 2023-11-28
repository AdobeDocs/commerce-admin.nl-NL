---
title: '[!UICONTROL Services] &gt; [!UICONTROL Magento Web API]'
description: Controleer de configuratie-instellingen op het tabblad [!UICONTROL Services] &gt; [!UICONTROL Magento Web API] pagina van de Commerce Admin.
exl-id: 9e9857e7-6f5c-4273-9e82-c861e627827a
feature: Configuration, Integration
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 0%

---

# [!UICONTROL Services] > [!UICONTROL Magento Web API]

{{config}}

<!-- [X-ref](../systems/integrations.md) -->

## [!UICONTROL SOAP Settings]

![SOAP-instellingen](./assets/web-api-soap-settings.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Default Response Charset] | Winkelweergave | Bepaalt de standaardtekenset. Indien leeg, wordt UTF-8 gebruikt. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL GraphQl Input Limits]

![Limieten voor grafischeQL-invoer](./assets/web-api-graphql-input-limits.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enable Input Limits] | Winkelweergave | Bepaalt of de inputgrenzen voor de vraag van GraphQL worden toegelaten. Standaardwaarde: `No`. |
| [!UICONTROL Maximum Page Size] | Winkelweergave | Hiermee stelt u het maximum aantal items in dat is toegestaan in een gepagineerd zoekresultaat in de GraphQL-reactie. Deze optie is niet beschikbaar als _Invoerlimieten inschakelen_ = `No`. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Web Api Input Limits]

![Invoerbeperkingen voor API voor web](./assets/web-api-input-limits.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Enable Input Limits] | Winkelweergave | Bepaalt als de inputgrenzen voor Web API vraag worden toegelaten. Standaardwaarde: `No`. |
| Limiet invoerlijst | Winkelweergave | Hiermee wordt het maximum aantal items ingesteld dat is toegestaan in een eigenschap voor een entiteitsarray in de API-aanvraag van het web. Deze optie is niet beschikbaar als _Invoerlimieten inschakelen_ = `No`. |
| [!UICONTROL Maximum Page Size] | Winkelweergave | Hiermee stelt u het maximum aantal items in dat is toegestaan in een gepagineerd zoekresultaat in de Web API-respons. Deze optie is niet beschikbaar als _Invoerlimieten inschakelen_ = `No`. |
| [!UICONTROL Default Page Size] | Winkelweergave | Plaatst het standaardaantal punten in een gepagineerd onderzoeksresultaat in de Web API reactie. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Web API Security]

![Web API-beveiliging](./assets/web-api-security.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Allow Anonymous Guest Access] | Algemeen | Determines is dat gasten anoniem toegang hebben tot CMS, catalogus en bronnen van SOAP en REST API&#39;s kunnen opslaan. Standaard is anonieme toegang voor gasten niet toegestaan. Opties: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL JWT Authentication]

![JWT-verificatie](./assets/web-api-jwt-authentication.png)<!-- zoom -->

| Veld | [Toepassingsgebied](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Algorithm to sign/encrypt JWTs used for authentication] | Algemeen | Hiermee wordt het type JWS- of JWE-algoritme opgegeven dat wordt gebruikt voor JWT-codering (JSON Web Token) |
| [!UICONTROL Content encryption algorithm for JWEs] | Algemeen | Hiermee geeft u het type algoritme voor inhoudscodering op dat wordt gebruikt voor JWT-codering wanneer het JWE-algoritme wordt geselecteerd. Deze optie wordt genegeerd voor JWS-algoritmen. |
| [!UICONTROL Customer JWT Expires In] | Algemeen | Hiermee stelt u de tijdsduur (in minuten) in voordat een JWT-token van een klant verloopt. De JWT-token van de klant verloopt over 30 minuten als dit veld leeg is of een negatieve waarde heeft. Standaardwaarde: `60` |
| [!UICONTROL Admin User JWT Expires In] | Algemeen | Hiermee stelt u de tijdsduur (in minuten) in voordat de token voor JWT-gebruiker Admin verloopt. De JWT-token voor beheerders verloopt over 30 minuten als dit veld leeg is of een negatieve waarde heeft. Standaardwaarde: `60` |

{:style=&quot;table-layout:auto&quot;}
