---
title: E-mailherinneringen
description: Meer informatie over e-mailherinneringen die automatisch naar klanten kunnen worden verzonden wanneer aan een bepaalde set voorwaarden wordt voldaan.
exl-id: 3293caca-9dd3-4d64-a80c-58c92a9208e5
feature: Merchandising, Communications
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/nl/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 0%

---

# E-mailherinneringen

{{ee-feature}}

Het doel van een e-mailherinnering is om mensen die je winkel hebben bezocht aan te moedigen om gebruik te maken van een speciale actie en een aankoop te doen. E-mailherinneringen kunnen automatisch naar klanten worden verzonden wanneer aan een bepaalde set voorwaarden wordt voldaan. U kunt bijvoorbeeld een herinnering sturen aan klanten die iets aan hun winkelwagentje of wenslijst hebben toegevoegd, maar nog geen aankoop hebben gedaan. U kunt e-mailherinneringen gebruiken om klanten aan te moedigen om aan uw opslag terug te keren, en a [&#x200B; couponcode &#x200B;](price-rules-cart-coupon.md) als stimulans te omvatten. Couponcodes kunnen automatisch worden gegenereerd voor elke batch met e-mailherinneringen, zodat u de opties kunt bepalen die aan elke batch zijn gekoppeld.

E-mailherinneringen kunnen worden geactiveerd nadat een bepaald aantal dagen is verstreken sinds een winkelwagentje is verlaten of voor een andere voorwaarde die u wilt definiëren. Veelvoorkomende voorwaarden zijn de totale waarde van het winkelwagentje, de hoeveelheid, de artikelen in het winkelwagentje, enzovoort.

>[!NOTE]
>
>Als een klant meer dan één geëvenaard karretje, verlanglijst, of combinatie van beide heeft, wordt de e-mailherinnering slechts eenmaal geactiveerd voor die klant. Als u dezelfde e-mailherinnering opnieuw wilt activeren, gebruikt u het veld _[!UICONTROL Repeat Schedule]_&#x200B;om het aantal dagen tussen de e-mailberichten in te stellen.

![&#x200B; E-mailherinneringen &#x200B;](./assets/email-reminders.png){width="700" zoomable="yes"}

## E-mailherinneringen configureren

Regels voor e-mailherinneringen kunnen met regelmatige intervallen worden verzonden per minuut, uur of dag. De configuratie bepaalt hoeveel e-mails in een batch worden verzonden, en de opslagidentiteit die als verzender van het bericht wordt weergegeven.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Customers]** uit en kies **[!UICONTROL Promotions]** .

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Automated Email Reminder Rules]** sectie uit en doe het volgende:

   ![&#x200B; configuratie van Klanten - geautomatiseerde e-mailherinneringsregels &#x200B;](../configuration-reference/customers/assets/promotions-automated-email-reminder-rules.png){width="600" zoomable="yes"}

   - Stel **[!UICONTROL Enable Reminder Emails]** in op `Yes` .

   - Stel **[!UICONTROL Frequency]** in op een van de volgende opties om in te stellen hoe vaak controles moeten worden uitgevoerd voor nieuwe klanten die in aanmerking komen voor automatische e-mailherinneringen:

      - `Minute Intervals`
      - `Hourly`
      - `Daily`

   - Stel de juiste **[!UICONTROL Interval]** in op basis van de instelling _[!UICONTROL Frequency]_.

   - Stel **[!UICONTROL Start Time]** in op het uur, de minuut en de seconde waarop het e-mailbericht wordt verzonden op basis van een 24-uurs klok.

   - Als u het aantal e-mailberichten dat in een batch kan worden verzonden wilt beperken, voert u het nummer in het veld **[!UICONTROL Maximum Emails per One Run]** in.

   - Als u wilt voorkomen dat pogingen om mislukte e-mail te verzenden, worden herhaald, voert u in het veld **[!UICONTROL Email Send Failure Threshold]** het maximumaantal pogingen in.

   - Plaats **[!UICONTROL Reminder Email Sender]** aan het [&#x200B; opslagcontact &#x200B;](../getting-started/store-details.md#store-email-addresses) dat als afzender van herinnering e-mail verschijnt.

   Voor een gedetailleerde lijst van deze opties, zie [&#x200B; Geautomatiseerde Regels van de Herinnering E-mail &#x200B;](../configuration-reference/customers/promotions.md#automated-email-reminder-rules) in de _Verwijzing van de Configuratie_.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

## E-mailherinneringssjablonen

De standaardsjabloon voor e-mailherinneringen kan worden aangepast en er kunnen aanvullende sjablonen worden gemaakt voor verschillende aanbiedingen. E-mailherinneringen bevatten een selectie van specifieke variabelen die in het bericht kunnen worden opgenomen. De informatie in deze variabelen wordt bepaald door de e-mailherinneringsregel die u hebt ingesteld en door de regel voor de winkelwagenprijs die aan de coupon is gekoppeld. Met de knop Variabele invoegen kunt u de opmaakcode met de variabele in de sjabloon invoegen. Meer leren, zie [&#x200B; E-mail &#x200B;](../systems/email-templates.md).

![&#x200B; E-mail herinneringsvoorproef &#x200B;](./assets/email-reminder-preview-promotion-template.png){width="600" zoomable="yes"}

### Een sjabloon voor een e-mailherinnering aanpassen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Klik op **[!UICONTROL Add New Template]**.

1. Kies in de lijst **[!UICONTROL Template]** onder `Magento_Reminder` de sjabloon **[!UICONTROL Promotion Notification/Reminder]** .

1. Klik op **[!UICONTROL Load Template]**.

Volg de standaard [&#x200B; instructies &#x200B;](../systems/email-template-custom.md) om het malplaatje aan te passen.

### E-mailherinneringsvariabelen

#### Couponcode

```
{{var coupon.getCode()|escape}}
```

#### Gebruikslimiet voor coupon

```
{{var coupon.usage_limit|escape}}
```

#### Coupongebruik per klant

```
{{var coupon.usage_per_customer|escape}}
```

#### URL van klantenaccount

```
{{var this.getUrl($store,'customer/account/',[_nosid:1])}}
```

#### Naam klant

```
{{var customer_data.name|escape}}
```

#### E-mailvoettekstsjabloon

```
{{template config_path="design/email/footer_template"}}
```

#### E-mailkopsjabloon

```
{{template config_path="design/email/header_template"}}
```

#### Afbeelding van e-maillogo Alt

```
{{var logo_alt}}
```

#### URL afbeelding e-maillogo

```
{{var logo_url}}
```

#### Beschrijving van aanbieding

```
{{var promotion_description|escape|nl2br}}
```

#### Aanbiedingsnaam

```
{{var promotion_name|escape}}
```

#### Winkelnaam

```
{{var store.frontend_name}}
```

#### URL van winkel

```
{{store url=""}}
```
