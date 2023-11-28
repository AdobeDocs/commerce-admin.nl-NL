---
title: '[!DNL Google Analytics]'
description: Meer informatie over het gebruik van [!DNL Google Analytics] om nuttige metriek voor uw plaatsen van de Handel te verzamelen.
exl-id: d4df2ef2-d67f-46bf-8569-cbee9dde77e4
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# [!DNL Google Analytics]

[!DNL Google Analytics] biedt u de mogelijkheid om extra aangepaste afmetingen en maatstaven voor tracering te definiëren, met ondersteuning voor offline- en mobiele toepassingsinteracties en toegang tot lopende updates. [!DNL Google Analytics] 4 is Google-meetoplossing van de volgende generatie en vervangt [!DNL Universal Analytics]. Op 1 juli 2023 verwerken standaard Universal Analytics-eigenschappen geen nieuwe hits meer.

>[!NOTE]
>
>Als uw bedrijf onderworpen is aan privacyregels zoals [Algemene verordening inzake gegevensbescherming](../getting-started/compliance-gdpr.md) en/of de [California Consumer Privacy Act](../getting-started/compliance-ccpa.md), zie [Google Privacy-instellingen](google-tools.md#google-privacy-settings).

>[!IMPORTANT]
>
>Als u de optie [Modus Cookie-beperking](../getting-started/compliance-cookie-law.md), [!DNL Google Analytics] geen gegevens over bezoekers verzamelen, tenzij ze cookies hebben geaccepteerd.

## [!DNL Google Analytics] 4

{{gtag-api-note}}

### Stap 1: Instellen [!UICONTROL Google Analytics] 4

Als u nog geen [!DNL Google Analytics] Voer een van de volgende handelingen uit als u uw site wilt instellen:

- [Gegevensverzameling voor Analytics voor het eerst instellen](https://support.google.com/analytics/answer/9304153)
- [Googles Analytics 4 aan een site toevoegen met [!DNL Universal Analytics]](https://support.google.com/analytics/answer/9744165)

### Stap 2: Voltooi de configuratie van de Handel

1. Meld u aan bij Admin voor de winkel Commerce.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Sales]** en kiest u **[!UICONTROL Google API]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Google GTag]** sectie.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Google Analytics4]** onderafdeling en voer de volgende handelingen uit:

   - Set **[!UICONTROL Enable]** tot `Yes`.

   - Laat de **[!UICONTROL Account type]** als `Google Analytics4`.

   - Voer uw **[!UICONTROL Measurement ID]**. Zie voor meer informatie [Help bij Googles Analytics](https://support.google.com/analytics/answer/9539598).

   - Als u A/B tests en andere prestatietests op uw inhoud wilt uitvoeren, stelt u **Inhoud-experimenten** tot `Yes`.

   ![Verkoopconfiguratie - Google API voor Googles Analytics 4](../configuration-reference/sales/assets/google-api-gtag-google-analytics4.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]**.

## Google Universal Analytics

>[!IMPORTANT]
>
>Op 1 juli 2023 verwerken standaard Universal Analytics-eigenschappen geen gegevens meer. Als u nog steeds op [!DNL Universal Analytics]wordt u aangeraden [bereiden voor op het gebruik van Googles Analytics 4](https://support.google.com/analytics/answer/10759417) verder.

### Stap 1: Google Universal Analytics instellen

Ga naar de Google-website en meld u aan voor een [Google Universal Analytics][1] account.

### Stap 2: Voltooi de configuratie van de Handel

1. Meld u aan bij Admin voor de winkel Commerce.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Sales]** en kiest u **[!UICONTROL Google API]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Google Analytics]** en voer de volgende handelingen uit:

   - Set **[!UICONTROL Enable]** tot `Yes`.

   - Voer uw [!DNL Google Analytics] **[!UICONTROL Account Number]**.

   - Als u A/B tests en andere prestatietests op uw inhoud wilt uitvoeren, stelt u **[!UICONTROL Content Experiments]** tot `Yes`.

   ![Verkoopconfiguratie - Google API - Googles Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]**.

## Verbeterde e-handel

Verbeterde e-commerce is een plug-in voor [!DNL Google Universal Analytics] dat u inzicht geeft in het winkelen en kopen van uw klanten. U kunt Verbeterde e-commerce gebruiken om rapporten over zeer belangrijke klantenactiviteiten, zoals te produceren wanneer de klanten punten de kar toevoegen, het controleproces beginnen, of een aankoop voltooien. U kunt ook patronen herkennen en analyseren van kopers die hun winkelwagentjes verlaten zonder een aankoop te doen.

De volgende instructies tonen hoe te vormen [!DNL Google Tag Manager] with [!DNL Universal Analytics] om verbeterde e-commercegegevens en -rapporten te produceren.

### Stap 1. Aanmelden voor Google-accounts

1. Aanmelden voor een [Google-tagbeheer](google-tag-manager.md) en voltooi de configuratie van de Handel.

1. Aanmelden voor een nieuwe [Google Universal Analytics][1] account.

### Stap 2. Verbeterde e-handel configureren

1. Meld u aan bij uw Google Universal Analytics-account.

1. Maak een eigenschap voor verbeterde e-commerceanalyses met de volgende instellingen:

   - Status: AAN
   - Verwante producten: ON
   - Uitgebreide e-commercportage inschakelen: ON
   - Afhandelingslabel: (niet vereist)

1. Klik op **[!UICONTROL Submit]**.

### Stap 3. Tags en triggers maken

1. Aanmelden bij uw [!DNL Google Tag Manager] account en maak de volgende triggers:

   | Naam | Type gebeurtenis | Filter |
   |--- |--- |--- |
   | `addToCart` | Aangepaste gebeurtenis |  |
   | `checkout` | Aangepaste gebeurtenis |  |
   | `checkout only` | Paginaweergave | Pagina-URL komt overeen met RegEx /checkout/.* |
   | `checkoutOption` | Aangepaste gebeurtenis |  |
   | `gtm.dom` | Aangepaste gebeurtenis |  |
   | `productClick` | Aangepaste gebeurtenis |  |
   | `promotionClick` | Aangepaste gebeurtenis |  |
   | `removeFromCart` | Aangepaste gebeurtenis |  |

   >[!NOTE]
   >
   >De [!UICONTROL Checkout] gebeurtenis wordt alleen geactiveerd voor de ingebouwde basisbetalingsmethoden voor handel (zoals `Check / Money Order` en `Cash On Delivery Payment`). Deze gebeurtenis wordt niet uitgevoerd voor `PayPal checkout` en andere methoden voor externe betalingen, waarbij wordt omgeschakeld naar de uitbetaling uit externe middelen.

1. Maak de volgende Universal Analytics-tags met dezelfde basisconfiguratie.

   - Universal Analytics-tags

     | Naam | Type | Vuurtriggers |
     |--- |--- |--- |
     | `Add to cart tracking` | Universal Analytics | addToCart |
     | `Checkout option tracking` | Universal Analytics | checkoutOption |
     | `Checkout tracking` | Universal Analytics | uitchecken |
     | `Pageview tracking` | Universal Analytics | gtm.dom |
     | `Product click tracking` | Universal Analytics | productClick |
     | `Promo click tracking` | Universal Analytics | promotieKlik |
     | `Remove from cart tracking` | Universal Analytics | removeFromCart |

   - Configuratie van de basiscode

     | Instelling | Waarde |
     |--- |--- |
     | [!UICONTROL Product] | Googles Analytics |
     | [!UICONTROL Tag Type] | Universal Analytics |
     | [!UICONTROL Tracking ID] | UA-XXX (De id voor bijhouden van uw Universal Analytics-account.) |
     | [!UICONTROL Enable Enhanced Ecommerce Features] | Waar |
     | [!UICONTROL Use data layer] | Waar |
     | [!UICONTROL Use Debug version] | Waar |

1. Voltooi de afzonderlijke configuraties voor bijhouden.

   - Voer het volgende in **[!UICONTROL Add to Cart]** instellingen voor bijhouden:

     | Instelling | Waarde |
     |--- |--- |
     | [!UICONTROL Track Type] | Gebeurtenis |
     | [!UICONTROL Category] | Ecommerce |
     | [!UICONTROL Action] | Toevoegen aan winkelwagentje |
     | [!UICONTROL Trigger] | addToCart |

   - Voer het volgende in **[!UICONTROL Checkout option]** instellingen voor bijhouden:

     | Instelling | Waarde |
     |--- |--- |
     | [!UICONTROL Track Type] | Gebeurtenis |
     | [!UICONTROL Category] | Ecommerce |
     | [!UICONTROL Action] | Afhandelingsoptie |
     | [!UICONTROL Trigger] | checkoutOption |

   - Voer het volgende in **[!UICONTROL PageView]** instellingen voor bijhouden:

     | Instelling | Waarde |
     |--- |--- |
     | [!UICONTROL Track Type] | PageView |
     | [!UICONTROL Trigger] | gtm.dom |

   - Voer de volgende handelingen uit **[!UICONTROL Product Click]** configuratie bijhouden:

     | Instelling | Waarde |
     |--- |--- |
     | [!UICONTROL Track Type] | Gebeurtenis |
     | [!UICONTROL Category] | Ecommerce |
     | [!UICONTROL Action] | Product klikken |
     | [!UICONTROL Trigger] | productClick |

   - Voer de volgende handelingen uit **[!UICONTROL Promotion Click]** configuratie bijhouden:

     | Instelling | Waarde |
     |--- |--- |
     | [!UICONTROL Track Type] | Gebeurtenis |
     | [!UICONTROL Category] | Ecommerce |
     | [!UICONTROL Action] | Aanbieding klikken |
     | [!UICONTROL Trigger] | promotieKlik |

   - Voer de volgende handelingen uit **[!UICONTROL Remove from Cart]** configuratie bijhouden:

     | Instelling | Waarde |
     |--- |--- |
     | [!UICONTROL Track Type] | Gebeurtenis |
     | [!UICONTROL Category] | Ecommerce |
     | [!UICONTROL Action] | Verwijderen uit winkelwagen |
     | [!UICONTROL Trigger] | removeFromCart |

1. Klik op **[!UICONTROL Preview]** en controleert u of de labels correct werken.

1. Klik na verificatie van de instellingen op **[!UICONTROL Publish]**.


[1]: https://support.google.com/analytics/answer/2817075?hl=en
