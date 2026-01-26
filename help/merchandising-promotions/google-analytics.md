---
title: '[!DNL Google Analytics]'
description: Leer hoe u  [!DNL Google Analytics]  kunt gebruiken om nuttige metriek voor uw plaatsen van Commerce te verzamelen.
exl-id: d4df2ef2-d67f-46bf-8569-cbee9dde77e4
feature: Marketing Tools, Integration
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 0%

---

# [!DNL Google Analytics]

Met [!DNL Google Analytics] kunt u aanvullende aangepaste afmetingen en maatstaven voor tracering definiëren, met ondersteuning voor offline- en mobiele-toepassingsinteracties en toegang tot lopende updates. [!DNL Google Analytics] 4 is een Google-meetoplossing van de volgende generatie die [!DNL Universal Analytics] vervangt. Op 1 juli 2023 verwerken standaard Universal Analytics-eigenschappen geen nieuwe hits meer.

>[!NOTE]
>
>Als uw zaken aan privacyverordeningen zoals de [&#x200B; Algemene Verordening van de Bescherming van Gegevens &#x200B;](../getting-started/compliance-gdpr.md) en/of de [&#x200B; Wet van de Privacy van de consument van Californië &#x200B;](../getting-started/compliance-ccpa.md) onderworpen zijn, zie [&#x200B; de Montages van de Privacy van Google &#x200B;](google-tools.md#google-privacy-settings).

>[!IMPORTANT]
>
>Als u de [&#x200B; Wijze van de Beperking van het Koekje &#x200B;](../getting-started/compliance-cookie-law.md) toelaat, [!DNL Google Analytics] verzamelt geen gegevens over bezoekers tenzij zij koekjes hebben goedgekeurd.

## [!DNL Google Analytics] 4

{{gtag-api-note}}

### Stap 1: Instellen [!UICONTROL Google Analytics] 4

Als u nog geen [!DNL Google Analytics] 4-instelling voor uw site hebt, voert u een van de volgende methoden uit:

- [&#x200B; de gegevensinzameling van de Analyse van de opstelling voor de eerste keer &#x200B;](https://support.google.com/analytics/answer/9304153)
- [&#x200B; voeg Google Analytics 4 aan een plaats met  [!DNL Universal Analytics] toe &#x200B;](https://support.google.com/analytics/answer/9744165)

### Stap 2: De Commerce-configuratie voltooien

1. Meld u aan bij de beheerder voor uw Commerce-winkel.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Google API]** .

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Google GTag]** sectie uit.

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Google Analytics4]** onderafdeling uit en doe het volgende:

   - Stel **[!UICONTROL Enable]** in op `Yes` .

   - Laat **[!UICONTROL Account type]** als `Google Analytics4` staan.

   - Voer uw **[!UICONTROL Measurement ID]** in. Meer leren, zie [&#x200B; Hulp van Google Analytics &#x200B;](https://support.google.com/analytics/answer/9539598).

   - Als u A/B het testen en andere prestatietests op uw inhoud wilt leiden, plaats **Experimenten van de Inhoud** aan `Yes`.

   ![&#x200B; de configuratie van de Verkoop - Google API voor Google Analytics 4 &#x200B;](../configuration-reference/sales/assets/google-api-gtag-google-analytics4.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

## Google Universal Analytics

>[!IMPORTANT]
>
>Op 1 juli 2023 verwerken standaard Universal Analytics-eigenschappen geen gegevens meer. Als u nog op [!DNL Universal Analytics] vertrouwt, wordt het geadviseerd dat u [&#x200B; voorbereidingen treft om Google Analytics 4 &#x200B;](https://support.google.com/analytics/answer/10759417) vooruit te gebruiken.

### Stap 1: Google Universal Analytics instellen

Bezoek de website van Google, en onderteken omhoog voor a [&#x200B; Google Universal Analytics &#x200B;](https://support.google.com/analytics/answer/2817075?hl=en) rekening.

### Stap 2: De Commerce-configuratie voltooien

1. Meld u aan bij de beheerder voor uw Commerce-winkel.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Google API]** .

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Google Analytics]** sectie uit en doe het volgende:

   - Stel **[!UICONTROL Enable]** in op `Yes` .

   - Voer uw [!DNL Google Analytics] **[!UICONTROL Account Number]** in.

   - Als u A/B-tests en andere prestatietests wilt uitvoeren op uw inhoud, stelt u **[!UICONTROL Content Experiments]** in op `Yes` .

   ![&#x200B; de configuratie van de Verkoop - Google API - Google Analytics &#x200B;](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

## Verbeterde e-handel

Enhanced Ecommerce is een plug-in voor [!DNL Google Universal Analytics] die u insight in staat stelt uw klanten te kopen en te winkelen. U kunt Verbeterde e-commerce gebruiken om rapporten over zeer belangrijke klantenactiviteiten, zoals te produceren wanneer de klanten punten de kar toevoegen, het controleproces beginnen, of een aankoop voltooien. U kunt ook patronen herkennen en analyseren van kopers die hun winkelwagentjes verlaten zonder een aankoop te doen.

De volgende instructies tonen hoe u [!DNL Google Tag Manager] met [!DNL Universal Analytics] kunt configureren voor het produceren van uitgebreide e-commercegegevens en -rapporten.

### Stap 1. Aanmelden voor Google-accounts

1. Teken omhoog voor a [&#x200B; Google de rekening van de Manager van de Markering &#x200B;](google-tag-manager.md), en voltooi de configuratie van Commerce.

1. Teken omhoog voor een nieuwe [&#x200B; Universele rekening van Analytics van Google &#x200B;](https://support.google.com/analytics/answer/2817075?hl=en).

### Stap 2. Verbeterde e-handel configureren

1. Meld u aan bij uw Google Universal Analytics-account.

1. Maak een eigenschap voor verbeterde e-commerceanalyses met de volgende instellingen:

   - Status: AAN
   - Verwante producten: ON
   - Uitgebreide e-commercportage inschakelen: ON
   - Afhandelingslabel: (niet vereist)

1. Klik op **[!UICONTROL Submit]** als de bewerking is voltooid.

### Stap 3. Tags en triggers maken

1. Meld u aan bij uw [!DNL Google Tag Manager] -account en maak de volgende triggers:

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
   >De [!UICONTROL Checkout] -gebeurtenis wordt alleen geactiveerd voor de ingebouwde Commerce-basisbetalingsmethoden (zoals `Check / Money Order` en `Cash On Delivery Payment` ). Deze gebeurtenis wordt niet uitgevoerd voor `PayPal checkout` en andere externe betalingsmethoden, die gebruikmaken van omleiding naar de kassa vanuit externe bronnen.

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
     | [!UICONTROL Product] | Google Analytics |
     | [!UICONTROL Tag Type] | Universal Analytics |
     | [!UICONTROL Tracking ID] | UA-XXX (De id voor bijhouden van uw Universal Analytics-account.) |
     | [!UICONTROL Enable Enhanced Ecommerce Features] | Waar |
     | [!UICONTROL Use data layer] | Waar |
     | [!UICONTROL Use Debug version] | Waar |

1. Voltooi de afzonderlijke configuraties voor bijhouden.

   - Voer de volgende **[!UICONTROL Add to Cart]** instellingen voor bijhouden in:

     | Instelling | Waarde |
     |--- |--- |
     | [!UICONTROL Track Type] | Gebeurtenis |
     | [!UICONTROL Category] | Ecommerce |
     | [!UICONTROL Action] | Toevoegen aan winkelwagentje |
     | [!UICONTROL Trigger] | addToCart |

   - Voer de volgende **[!UICONTROL Checkout option]** instellingen voor bijhouden in:

     | Instelling | Waarde |
     |--- |--- |
     | [!UICONTROL Track Type] | Gebeurtenis |
     | [!UICONTROL Category] | Ecommerce |
     | [!UICONTROL Action] | Afhandelingsoptie |
     | [!UICONTROL Trigger] | checkoutOption |

   - Voer de volgende **[!UICONTROL PageView]** instellingen voor bijhouden in:

     | Instelling | Waarde |
     |--- |--- |
     | [!UICONTROL Track Type] | PageView |
     | [!UICONTROL Trigger] | gtm.dom |

   - Voltooi de volgende **[!UICONTROL Product Click]** trackingconfiguratie:

     | Instelling | Waarde |
     |--- |--- |
     | [!UICONTROL Track Type] | Gebeurtenis |
     | [!UICONTROL Category] | Ecommerce |
     | [!UICONTROL Action] | Product klikken |
     | [!UICONTROL Trigger] | productClick |

   - Voltooi de volgende **[!UICONTROL Promotion Click]** trackingconfiguratie:

     | Instelling | Waarde |
     |--- |--- |
     | [!UICONTROL Track Type] | Gebeurtenis |
     | [!UICONTROL Category] | Ecommerce |
     | [!UICONTROL Action] | Aanbieding klikken |
     | [!UICONTROL Trigger] | promotieKlik |

   - Voltooi de volgende **[!UICONTROL Remove from Cart]** trackingconfiguratie:

     | Instelling | Waarde |
     |--- |--- |
     | [!UICONTROL Track Type] | Gebeurtenis |
     | [!UICONTROL Category] | Ecommerce |
     | [!UICONTROL Action] | Verwijderen uit winkelwagen |
     | [!UICONTROL Trigger] | removeFromCart |

1. Klik na voltooiing op **[!UICONTROL Preview]** en controleer of de labels goed werken.

1. Klik op **[!UICONTROL Publish]** nadat u de instellingen hebt gecontroleerd.
