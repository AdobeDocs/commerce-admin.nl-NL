---
title: Hulp bieden aan winkeliers
description: Wanneer u de Login als eigenschap van de Klant gebruikt, kunt u zien wat de klanten zien en updates namens hen maken.
exl-id: 6842ae7a-6440-45f1-af18-e6427088d29d
feature: Customers, Customer Service
source-git-commit: 29f3a8bb019d464e6d7646e0ebc7a4fa2ed0dd74
workflow-type: tm+mt
source-wordcount: '1077'
ht-degree: 0%

---

# Hulp bieden aan winkeliers

Klanten hebben soms hulp nodig bij hun bestelling. De beheerders van de opslag kunnen _Login als Klant_ gebruiken, die hen toestaat om te zien wat de klant ziet en updates maken om hen bij te staan.

Alle acties die tijdens het aanmelden als de klant worden uitgevoerd, worden toegepast op de account van de werkelijke klant.

>[!BEGINTABS]

>[!TAB  Adobe Commerce ]

[!BADGE &#x200B; slechts PaaS &#x200B;]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."}

Wanneer het voor een _Admin_ gebruiker wordt toegelaten, verschijnt de _[!UICONTROL Login as Customer]_&#x200B;knoop in veelvoudige pagina&#39;s:

* [Bewerkingspagina van klant](../customers/update-account.md)
* [Weergavepagina Volgorde](../stores-purchase/order-processing.md)
* [Factuurweergave](../stores-purchase/invoices.md)
* [Pagina Verzendweergave](../stores-purchase/shipments.md)
* [Weergavepagina creditcard](../stores-purchase/credit-memo-create.md)

![&#x200B; Login als Klant &#x200B;](assets/login-as-customer.png){width="600" zoomable="yes"}

>[!TAB  Adobe Commerce as a Cloud Service ]

[!BADGE &#x200B; slechts SaaS &#x200B;]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Alleen van toepassing op Adobe Commerce as a Cloud Service- en Adobe Commerce Optimizer-projecten (door Adobe beheerde SaaS-infrastructuur)."}

In Adobe Commerce as a Cloud Service, gebruikt de Login als eigenschap van de Klant a **Eenmalige Code (OTC)** werkschema in plaats van directe login. Beheerders genereren een kortstondige code voor eenmalig gebruik voor een klant. Deze code kan vervolgens via GraphQL worden uitgewisseld voor een toegangstoken voor klanten, zodat gebruikers zich zonder wachtwoord kunnen aanmelden als workflows van de klant voor winkelscenario&#39;s voor verkopers.

Het onderdeel bestaat uit de volgende onderdelen:

* **Admin UI** - op de klant geeft pagina uit, kunnen de beheerders om een éénmalige code (OTC) in plaats van direct het programma openen als klant verzoeken.
* **[REST API &#x200B;](https://developer.adobe.com/commerce/webapi/rest/saas-integrations/login-as-customer/)** - een programmatic eindpunt voor OTC generatie, nuttig voor admin manuscripten en derdesintegratie.
* **GraphQL API** - Mutaties die een OTC voor een teken van de klantentoegang voor opslag of headless handelsstromen ruilen.

>[!ENDTABS]

## Aanmelden als klant inschakelen

Het toelaten van _Login als Klant_ vereist dat u de eigenschap in uw instantie van Commerce toelaat en dan toegang voor Admin gebruikers in de toestemmingen van de gebruikersrol toelaat.

### De functie inschakelen

1. Ga op de zijbalk Beheerder naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Customers]** uit en kies **[!UICONTROL Login as Customer]** .

   ![&#x200B; de opties van de Configuratie - Login als Klant &#x200B;](../configuration-reference/customers/assets/login-as-customer.png){width="600" zoomable="yes"}

1. Stel **[!UICONTROL Enable Login as Customer]** in op `Yes` .

1. _(Optioneel)_ Stel **[!UICONTROL Disable Page Cache for Admin User]** in op `No` om de paginacache in te schakelen wanneer de Admin-gebruiker zich aanmeldt als een klant.

   >[!WARNING]
   >
   > Als u de paginacache uitschakelt (`Yes` - standaard), zorgt u ervoor dat de gebruiker die zich aanmeldt als Klant, nieuwe gegevens krijgt die niet in de cache zijn opgeslagen.

1. _(Optioneel)_ Stel **[!UICONTROL Store View to Log in]** in op `Manual Selection` als u meerdere sites en/of meerdere winkels hebt ingesteld en de Admin-gebruiker de winkelweergave moet selecteren wanneer hij of zij zich aanmeldt als klant.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

### Toegang voor Admin-gebruikers inschakelen

1. Op _Admin_ sidebar, ga **[!UICONTROL System]** > _Toestemmingen_ > **[!UICONTROL User Roles]**.

1. Klik op de rol in de lijst.

1. In het [!UICONTROL _linkerpaneel van de Informatie van de Rol 0&rbrace; &lbrace;, klik_].**[!UICONTROL Role Resources]**

1. Wijzig **[!UICONTROL Role Resources]** op de pagina in `Custom` .

   >[!INFO]
   >
   > Als deze optie is geselecteerd, wordt de bronhiërarchie op de pagina weergegeven.

1. Blader naar het bovenliggende item **[!UICONTROL Customers]** en het onderliggende item **[!UICONTROL Login as Customer]** . Selecteer vervolgens de bronnen die u voor de rol wilt inschakelen:

   * **[!UICONTROL Allow Login as Customer]** - staat de gebruiker Admin toe om het _Login als eigenschap van de Klant_ te gebruiken.
   * **[!UICONTROL View Login as Customer Log]** - staat de gebruiker Admin toe om het _Login als Login van de Klant_ te zien.

   ![&#x200B; Bronnen van de Rol - Login als Klant &#x200B;](assets/customers-login-as-customer-role-resources.png){width="400" zoomable="yes"}

1. Klik op **[!UICONTROL Save Role]**.

## Toestemming voor klantenaccount voor hulp bij externe winkelen

Om toegang tot uw account mogelijk te maken voor medewerkers van de opslagondersteuning van de beheerder, moet een klant de functie voor hun account inschakelen:

>[!BEGINTABS]

>[!TAB  Adobe Commerce ]

[!BADGE &#x200B; slechts PaaS &#x200B;]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."}

1. De klant gaat naar de pagina **[!UICONTROL Account Information]** .

1. Selecteert het selectievakje **[!UICONTROL Allow remote shopping assistance]** .

1. De klant klikt op **[!UICONTROL Save]** .

![&#x200B; pagina van de Informatie van de Rekening &#x200B;](assets/permission.png){width="700" zoomable="yes"}

>[!TAB  Adobe Commerce as a Cloud Service ]

[!BADGE &#x200B; slechts SaaS &#x200B;]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Alleen van toepassing op Adobe Commerce as a Cloud Service- en Adobe Commerce Optimizer-projecten (door Adobe beheerde SaaS-infrastructuur)."}

De klant moet de `login_as_customer_assistance_allowed` uitbreidingsattributen hebben die aan **worden geplaatst 2**. Dit kan op **worden gevormd geeft Klant** pagina in Admin of door GraphQL uit wanneer het creëren van of het uitgeven van een klant.

>[!WARNING]
>
>Zonder deze toestemming kan een Admin-gebruiker zich niet aanmelden als deze klant.

![&#x200B; de attributenconfiguratie van de de toestemmingsuitbreiding van de Klant op de Edit pagina van de Klant &#x200B;](assets/customer-consent-attribute.png){width="600" zoomable="yes"}

Om deze toestemming met GraphQL voor een bestaande klantenrekening te plaatsen, plaats `allow_remote_shopping_assistance` input aan `true` gebruikend [`updateCustomerV2` &#x200B;](https://developer.adobe.com/commerce/webapi/graphql/schema/customer/mutations/update-v2/) of [`createCustomerV2` &#x200B;](https://developer.adobe.com/commerce/webapi/graphql/schema/customer/mutations/create-v2/) mutaties.

>[!ENDTABS]

## Aanmelden als klant van de beheerder

>[!BEGINTABS]

>[!TAB  Adobe Commerce ]

[!BADGE &#x200B; slechts PaaS &#x200B;]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."}

1. Op _Admin_ sidebar, ga **[!UICONTROL Customers]** > [!UICONTROL _Alle Klanten_].

1. Open een gebruiker in de bewerkingsmodus.

1. Kies in het deelvenster **[!UICONTROL Customer Information]** de sectie **[!UICONTROL Account Information]** .

1. Stel de waarde **[!UICONTROL Allow remote shopping assistance]** in op `Yes` .

   >[!INFO]
   >
   >De beheerder kan zich nu aanmelden als een gebruiker zonder hun toestemming van de winkel.

>[!TAB  Adobe Commerce as a Cloud Service ]

[!BADGE &#x200B; slechts SaaS &#x200B;]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Alleen van toepassing op Adobe Commerce as a Cloud Service- en Adobe Commerce Optimizer-projecten (door Adobe beheerde SaaS-infrastructuur)."}

>[!NOTE]
>
>Voor begeleiding bij het uitvoeren van deze eigenschap die REST gebruikt, zie de [&#x200B; Login als de documentatie van het TUSSENRUIMTE van de Klant &#x200B;](https://developer.adobe.com/commerce/webapi/rest/saas-integrations/login-as-customer/) REST API.

### Een eenmalige code (OTC) aanvragen bij de beheerder

1. Navigeer naar **[!UICONTROL Customers]** en selecteer een klant om de bewerkingspagina te openen.

1. Klik op de pagina Klant bewerken op **[!UICONTROL Get Customer Login OTC]** .

   ![&#x200B; krijgt de OTC knoop van de Login van de Klant op de Edit pagina van de Klant &#x200B;](assets/get-customer-login-otc-button.png){width="600" zoomable="yes"}

1. Voer een **[!UICONTROL Reason]** (vereist) in en klik op **[!UICONTROL Request]** .

   ![&#x200B; OTC verzoek modaal met het gebied van de Reden &#x200B;](assets/otc-reason-modal.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Het **gebied van de Reden** wordt vereist. Het wordt overgegaan tot de OTP generatiestroom en is gereserveerd voor gebruik in komende controle en gebeurtenisregistrereneigenschappen.

1. De gegenereerde OTC wordt weergegeven in het modaal. Gebruik deze code met de `generateCustomerToken` - of `exchangeOtpForCustomerToken` GraphQL-mutatie voor toestemming van de klant.

   ![&#x200B; Gegenereerde OTC die in modaal &#x200B;](assets/otc-generated-code.png){width="300" zoomable="yes"} wordt getoond

>[!IMPORTANT]
>
>De gegenereerde One-Time Code OTC is standaard 30 seconden geldig en wordt na één gebruik ongeldig gemaakt. TTL kan worden gevormd door a [&#x200B; steunkaartje &#x200B;](https://experienceleague.adobe.com/home?support-tab=home#support) voor te leggen.

Nadat de Eenmalige Code wordt geproduceerd, kunt u het gebruiken door aan uw storefront te navigeren en het programma te openen gebruikend de volgende geloofsbrieven:

* **E-mail**: Het e-mailadres van de klant
* **Wachtwoord**: De geproduceerde Eenmalige Code (OTC)

>[!ENDTABS]

## Aanmelden als klant gebruiken

>[!INFO]
>
>Om _Login als Klant_ te gebruiken, zorg ervoor dat uw Admin zoals vroeger beschreven wordt gevormd.

_Login als Klant_ staat u toe om de plaats te zien enkel aangezien de klant doet, en staat u toe om andere acties voor de klant problemen op te lossen en te nemen. Als u een toegewezen gebruikersrol met de vereiste toestemmingen hebt:

1. U kunt op **[!UICONTROL Login as Customer]** klikken op de pagina&#39;s in de vorige sectie.
1. De acties Aanmelden als klant zijn beschikbaar in het Actions Report.

>[!WARNING]
>
>Om het even welke genomen acties terwijl het programma geopend [!UICONTROL _als Klant_] (zoals toevoegen/verwijderen producten) worden toegepast op de daadwerkelijke orde van de klant. In de winkel wordt een banner weergegeven wanneer u `logged in as customer_name` bent om een herinnering aan de speciale status te geven.

## Aanmelden als aanmelden bij klant

{{ee-feature}}

Adobe Commerce verstrekt het registreren voor het _Login als acties van de Klant_. Hierin worden alle sessies weergegeven waarbij een Admin-gebruiker de functie benadert. Om tot de geregistreerde acties toegang te hebben, ga naar het [&#x200B; Rapport van Acties Admin &#x200B;](../systems/action-log-report.md).

U kunt de rapportinstelling **[!UICONTROL Action Group]** naar `Login As Customer` boven aan de pagina filteren en op **[!UICONTROL Search]** klikken.

![&#x200B; filter het Rapport van Acties &#x200B;](assets/customers-login-as-customer-log-filter.png){width="700" zoomable="yes"}
