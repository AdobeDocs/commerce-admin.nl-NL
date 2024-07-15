---
title: Google-sitegereedschappen
description: Leer over de Google tools-integratie die u kunt gebruiken om uw inhoud te optimaliseren, uw verkeer te analyseren en uw catalogus aan te sluiten op winkelaggregators en marketinglocaties.
exl-id: 09c48f1e-792b-4553-82fc-cd1a119b15d0
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---

# Google-sitegereedschappen

Uw winkelconfiguratie is geïntegreerd met de volgende Google-tools om uw inhoud te optimaliseren, uw verkeer te analyseren en uw catalogus aan te sluiten op winkelaggregators en marketinglocaties.

- [ Googles Analytics ](google-analytics.md) - Gebruik _Universele Analytics van Google_ om extra douanedimensies en metriek voor het volgen, met steun voor off-line en mobiele app interactie, en toegang tot aan de gang zijnde updates te bepalen.

- [ de Experimenten van de Inhoud van Google ](google-content-experiments.md) - Opstelling een A/B test voor producten, categorieën, of inhoudspagina&#39;s gebruikend de Experimenten van de Inhoud van Googles Analytics.

- [ de Manager van de Markering van Google ](google-tag-manager.md) - ![ Adobe Commerce ](../assets/adobe-logo.svg) (Adobe Commerce slechts) de Manager van de Markering van Google van het Gebruik om de vele markeringen met betrekking tot marketing campagnegebeurtenissen te beheren.

- [ Google AdWords ](google-adwords.md) - creeer een Google AdWords campagne en spooromzettingen voor uw opslag.

{{gtag-api-note}}

## Google-privacyinstellingen

Als uw zaken wordt vereist om privacyverordeningen zoals [ GDPR ](../getting-started/compliance-gdpr.md) of [ CCPA ](../getting-started/compliance-ccpa.md) na te leven, verander de standaardmontages van de hulpmiddelen van Google om privacyvereisten te ontmoeten. Volg deze stappen om ervoor te zorgen dat uw gebruik van klantengegevens in naleving blijft.

### Stap 1: Google-instellingen bijwerken

1. [ Teken binnen ][1] {: target= &quot;_blank&quot;} aan de rekening van de Googles Analytics van uw bedrijf.

1. Kies onder aan de linkerzijbalk **[!UICONTROL Admin]** en navigeer naar het account dat u wilt bewerken (indien van toepassing).

1. Klik in de kolom **[!UICONTROL Account]** op **[!UICONTROL Account Settings]** .

1. Schakel het delen van gegevens uit om te voldoen aan de vereisten voor privacyregelgeving.

   De standaardinstellingen voor Googles Analytics delen uw bedrijfsgegevens met Google en andere partijen. Schakel het selectievakje voor de volgende instellingen uit als u het delen van gegevens wilt uitschakelen:

   - Google-producten en -services
   - Benchmarking
   - Technische ondersteuning
   - Accountspecialisten

1. Accepteer het _Verandering van de Verwerking van Gegevens_.

   De Google Ads Data Processing Terms beschrijven hoe Google gegevens verwerkt en welke maatregelen het neemt om de gegevensbeveiliging te waarborgen voor bedrijven die onder de GDPR vallen. Met het amendement wordt ook een overzicht bijgehouden van uw juridische entiteiten en contactgegevens. Om [ meer ][2] te leren {: target= &quot;_blank&quot;}, klik de verbinding in het bericht bij de bovenkant van de pagina.

   - Schuif omlaag naar de pagina **[!UICONTROL Data Processing Amendment]** .
   - Klik **[!UICONTROL Review Amendment]** om de _Voorwaarden van de Gegevensverwerking van Google te lezen Adds_.
   - Klik op **[!UICONTROL Accept]**.
   - Klik op **[!UICONTROL Save]**.

1. Voltooi de _details van het Beleid van 0} DPA._

   - Klik op **[!UICONTROL Manage DPA Details]** om een pagina voor DPA-beheer te openen waarin u contactpersonen en juridische entiteiten van uw organisatie kunt bewerken.

   - In de **[!UICONTROL Legal Entities]** sectie, klik _uitgeven_ ( ![ Google geeft pictogram ](./assets/google-icon-edit.png) uit) pictogram en voegt één of meerdere geregistreerde namen voor uw organisatie toe. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

   - In de **sectie van Contacten**, klik _toevoegen_ ( ![ Google voegt pictogram ](./assets/google-icon-add.png) toe) en ga de informatie voor het eerste contact in. Schakel vervolgens het selectievakje van elke toepasselijke rol in en klik op **[!UICONTROL Add]** .

      - Primaire contactpersoon - (E-mailadres melding) De contactpersoon waarnaar berichten worden verzonden.
      - Functionaris voor gegevensbescherming - (indien van toepassing) De persoon die is aangewezen om naleving van de privacyregelgeving te vergemakkelijken.
      - Vertegenwoordiger van de Europese Economische Ruimte (EER) - (indien van toepassing) De persoon die klanten buiten de EU vertegenwoordigt met betrekking tot hun verplichtingen uit hoofde van de GDPR.

     Herhaal dit om, indien van toepassing, nog een contactpersoon toe te voegen.

### Stap 2: De Google JS-bibliotheken wijzigen

Google ondersteunt drie JavaScript-bibliotheken om het gebruik van websites te meten, afhankelijk van het Google-product: `gtag.js`, `analytics.js` en `ga.js` . Om aan privacyvereisten te voldoen, kan de standaardcode als volgt worden gewijzigd:

#### IP-adressen anoniem maken

Om de IP adressen te anonimiseren die door **_Google Universal Analytics_** worden gebruikt, voeg het volgende fragment aan de `analytics.js` bibliotheek op uw Webserver toe:

analytics.js

```
: `ga('set', 'anonymizeIp', true);`
```

Meer leren, zie de [ Referentie van het Gebied Analytics.js ][3] {: target= &quot;_blank&quot;} in de Hulp van Google.

Als u de verouderde `ga.js` bibliotheek gebruikt, voegt u het volgende fragment toe:

ga.js

```
: `ga('set', 'anonymizeIp', true);`
```

Om de IP adressen te anonimiseren die door **_worden gebruikt de Manager van de Markering van Google_**, plaats de `anonymize_ip` parameter aan `true` in de `gtag.js` bibliotheek op uw Webserver.

gtag.js

```
: `gtag('event', 'your_event', { 'anonymize_ip': true })`
```

Meer leren, zie [ IP Anonymization in Analytics ][4] in de Hulp van Google.

#### SSL forceren

Als u wilt dat alle Google-gegevens worden verzonden via een SSL (Secure Socket Layer), voegt u het volgende fragment toe aan de `analytics.js` -bibliotheek op uw webserver.

analytics.js

```
: `ga('set', 'forceSSL', true);`
```

### Stap 3: Je privacybeleid bijwerken

Werk uw [ privacybeleid ](../getting-started/privacy-policy.md) bij om te verklaren dat uw bedrijf:

- Gebruikt Googles Analytics
- Hiermee maskeert u IP-adressen om persoonlijke gegevens te verbergen
- Google Data Sharing is uitgeschakeld
- Gebruikt geen andere Google-services met cookies van Googles Analytics

[1]: https://www.google.com/analytics/
[2]: https://support.google.com/analytics/answer/3379636
[3]: https://developers.google.com/analytics/devguides/collection/analyticsjs/field-reference
[4]: https://support.google.com/analytics/answer/2763052
