---
title: Een individuele klantaccount maken
description: Bezoekers kunnen eenvoudig een individuele klantenaccount maken om hun aankopen te beheren.
exl-id: 8d08c0e1-f3ba-4423-98a7-ffa8ba5a1b8b
feature: Customers, Storefront
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '1268'
ht-degree: 0%

---

# Een individuele klantaccount maken

Bezoekers in je winkel kunnen een account openen om hun aankopen en activiteiten te beheren. Klanten maken gewoonlijk hun eigen accounts in uw winkel. U kunt echter ook direct vanuit de beheerfunctie klantenaccounts maken. Dit is handig om klanten via de telefoon te helpen.

De volgende instructies vertegenwoordigen de standaardconfiguratie van de klantenrekening. Om de selectie en het gedrag van sommige gebieden in de vorm te veranderen, zie [ Vormende Rekeningen van de Klant ](../customers/customer-account-scope.md).

Als opslagbeheerder, kunt u [ nieuwe rekeningsopties ](../customers/account-options-new.md) ook plaatsen om een bevestigingse-mail naar nieuwe geregistreerde klanten te verzenden, die helpt ervoor te zorgen dat de geregistreerde rekeningen geldig zijn.

>[!NOTE]
>
>Vanaf versie 2.4.7 moeten klanten hun e-mail en wachtwoord opnieuw invoeren om zich aan te melden bij hun account na e-mailbevestiging, ongeacht de browser.

## Account maken van de winkel

Een winkelklant maakt een account op de winkel.

1. Klik in de winkel op **[!UICONTROL Create an Account]** rechtsboven in de koptekst.

   ![ creeer een Rekening ](assets/storefront-create-an-account-link.png){width="700" zoomable="yes"}

1. Voer onder **[!UICONTROL Personal Information]** de **[!UICONTROL First Name]** en **[!UICONTROL Last Name]** ervan in.

   ![ Persoonlijke Informatie ](assets/storefront-create-account-personal-information.png){width="600" zoomable="yes"}

1. Als ze hun naam en e-mailadres aan de lijst met abonnees van nieuwsbrieven willen toevoegen, selecteert de klant het selectievakje **[!UICONTROL Sign Up for Newsletter]** .

   >[!INFO]
   >
   > Deze optie wordt ook weergegeven als de winkel geen nieuwsbrief publiceert.

1. Als zij het personeel van de opslagsteun aan [ willen zien wat zij ](../customers/login-as-customer.md) zien en verre hulp verlenen, selecteert de klant **[!UICONTROL Allow remote shopping assistance]** checkbox.

1. Voer onder **[!UICONTROL Sign-in Information]** het **[!UICONTROL Email]** -adres in.

   >[!INFO]
   >
   > Dit e-mailadres wordt onderdeel van de aanmeldingsgegevens en kan niet aan een andere klantenaccount worden gekoppeld.

   ![ Sign-in Informatie ](assets/storefront-create-account-signin-information.png){width="600" zoomable="yes"}

1. Voert een **[!UICONTROL Password]** in die drie van de volgende soorten informatie bevat:

   - Kleine letters
   - Hoofdletters
   - Getallen
   - Speciale tekens

   Nadat ze op **[!UICONTROL Enter]** hebben gedrukt, wordt de sterkte van het wachtwoord geëvalueerd en onder het veld weergegeven. Als het wachtwoord wordt beschouwd om _Weak_ te zijn, probeer een andere tot het als _Sterk_ geëvalueerd.

   ![ een sterk wachtwoord wordt geadviseerd ](assets/storefront-customer-account-create-password-strong.png){width="600" zoomable="yes"}

1. Vervolgens voert de klant het bestand opnieuw in op **[!UICONTROL Confirm Password]** .

1. Klik zo nodig op **[!UICONTROL Show Password]** om het wachtwoord weer te geven dat u hebt ingevoerd.

1. Wanneer volledig, klik **creeer een Rekening**.

De klant kan hun e-mailadres en wachtwoord aan [ binnen ondertekenen ](../customers/customer-sign-in.md) aan hun rekening dan gebruiken en de adresinformatie voltooien.

## Een account maken via de beheerder

Als handelaar, kunt u een klantenrekening van Admin tot stand brengen.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Klik op **[!UICONTROL Add New Customer]**.

### Stap 1: De accountgegevens invullen

![ Informatie van de Klant ](assets/new-information.png){width="700" zoomable="yes"}

1. Ga als volgt te werk in de sectie **[!UICONTROL Account Information]** :

   - Voor een installatie op meerdere sites stelt u **[!UICONTROL Associate to Website]** in op de website waarop de klantenaccount van toepassing is.
   - Wijs, indien van toepassing, de klant aan een andere **[!UICONTROL Customer Group]** toe.
   - Als u [ Validering van identiteitskaart van BTW ](../stores-purchase/vat.md) gebruikt en wilt **[!UICONTROL Disable Automatic Group Change Based on VAT ID]**, checkbox selecteren.

1. Vul de vereiste velden in:

   - **[!UICONTROL First Name]**
   - **[!UICONTROL Last Name]**
   - **[!UICONTROL Email]**

1. Vul de optionele velden naar wens in:

   - **[!UICONTROL Name Prefix]**
   - **[!UICONTROL Middle Name/Initial]**
   - **[!UICONTROL Name Suffix]**
   - **[!UICONTROL Date of Birth]**
   - **[!UICONTROL Tax/VAT Number]**
   - **[!UICONTROL Gender]**

   >[!WARNING]
   >
   >In overeenstemming met de huidige beste praktijken op het gebied van beveiliging en privacy, dient u zich bewust te zijn van mogelijke juridische en veiligheidsrisico&#39;s die verbonden zijn aan de opslag van de volledige geboortedatum van de klant (maand, dag, jaar) met andere persoonlijke identificatoren. U wordt aangeraden de opslag van de volledige geboortedatum van de klant te beperken en u aan te raden het geboortejaar van de klant als alternatief te gebruiken.

1. Plaats **[!UICONTROL Send Welcome Email From]** aan de opslagmening waarvan _Onthaal_ e-mail moet worden verzonden.

   >[!INFO]
   >
   > Als de opslag meningen voor verschillende [ talen ](../stores-purchase/store-localize.md) heeft, bepaalt dit het plaatsen de taal van het Welkome e-mail.

1. Klik op **[!UICONTROL Save and Continue Edit]** boven aan de pagina.

   >[!INFO]
   >
   >Nadat de klantenrekening wordt bewaard, verschijnt de volledige reeks opties in het linkerpaneel en in het menu bij de bovenkant van de pagina. Op het tabblad _[!UICONTROL Customer View]_&#x200B;wordt een overzicht van de account weergegeven.

   ![ Mening van de Klant ](assets/customer-account-create-saved.png){width="600" zoomable="yes"}

### Stap 2: Voltooi de adresinformatie

1. Kies **[!UICONTROL Addresses]** in het linkerdeelvenster en klik op **[!UICONTROL Add New Addresses]** .

1. Als hetzelfde adres wordt gebruikt voor facturering en verzending, schakelt u beide opties in of uit.

   - **[!UICONTROL Default Billing Address]**
   - **[!UICONTROL Default Shipping Address]**

   ![ voeg de informatie van het klantenadres ](assets/information-addresses.png){width="600" zoomable="yes"} toe

1. Blader omlaag en vul de vereiste adresvelden in de tweede kolom in.

   - **[!UICONTROL Street Address]**
   - **[!UICONTROL City]**
   - **[!UICONTROL Country]**
   - **[!UICONTROL State/Province]**
   - **[!UICONTROL ZIP/Postal Code]**

1. Voer de **[!UICONTROL Phone Number]** in voor dit adres.

1. Voer, indien van toepassing, de **[!UICONTROL VAT Number]** in die aan de klant is gekoppeld.

1. Als dit het enige adres is dat nodig is voor het account, klikt u op **[!UICONTROL Save]** .

   Anders klikt u op **[!UICONTROL Save and Continue Edit]** en herhaalt u de vorige stappen om extra adressen toe te voegen.

   Het nieuwe adres wordt weergegeven op de pagina [!UICONTROL Addresses] met de geselecteerde _[!UICONTROL Default Billing]_- en&#x200B;_[!UICONTROL Default Shipping]_ -adressen boven de volledige lijst.

   ![ mening van Adressen ](assets/address-list.png){width="600" zoomable="yes"}

### Stap 3: Het wachtwoord opnieuw instellen

Aan accounts van klanten die zijn gemaakt met de beheerder worden aanvankelijk geen wachtwoorden toegewezen.

1. Zoek het nieuwe klantenaccount in het raster.

1. Klik op **[!UICONTROL Edit]** in de kolom _[!UICONTROL Action]_.

1. Klik op **[!UICONTROL Reset Password]** in de menubalk boven aan de pagina.

1. Deze melding wordt verzonden naar de rekeninghouder, met instructies voor het instellen van het wachtwoord.

## Knopbalk

Aanvullende knoppen worden beschikbaar wanneer het profiel voor de eerste keer wordt opgeslagen. Meer leren, zie [ een klantenprofiel ](../customers/update-account.md) bijwerken.

| Knop | Beschrijving |
|--- |--- |
| **[!UICONTROL Back]** | Hiermee gaat u terug naar de _[!UICONTROL Customers]_-pagina zonder wijzigingen op te slaan. |
| **[!UICONTROL Delete Customer]** | Verwijdert de huidige klant. Voltooide bestellingen die aan de klant zijn gekoppeld, worden niet verwijderd. |
| **[!UICONTROL Reset]** | Hiermee herstelt u eventuele niet-opgeslagen wijzigingen in het klantformulier naar de vorige waarden. |
| **[!UICONTROL Create Order]** | Maakt een bestelling voor de klant. |
| **[!UICONTROL Reset Password]** | Verzendt de verbinding van het a [ teruggestelde wachtwoord ](../customers/password-reset.md) aan de klant door e-mail. |
| **[!UICONTROL Force Sign-in]** | Hiermee worden de OAuth-toegangstokens ingetrokken die aan de klantenaccount zijn gekoppeld. Deze functie kan slechts met klantenrekeningen worden gebruikt die tekenen OAuth als deel van een Web API [ integratie ](../systems/integrations.md) zijn toegewezen. Meer leren, zie [ Op OAuth-Gebaseerde authentificatie ](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) in de ontwikkelaarsdocumentatie. |
| **[!UICONTROL Manage Shopping Cart]** | Staat de beheerder toe om het winkelwagentje voor de klant te beheren. |
| **[!UICONTROL Save and Continue Edit]** | Hiermee slaat u wijzigingen op en houdt u het profiel van de klant open. |
| **[!UICONTROL Save Customer]** | Hiermee slaat u wijzigingen op en sluit u het klantprofiel. |

{style="table-layout:auto"}

## Veldomschrijvingen

### [!UICONTROL Account Information]

| Veld | Beschrijving |
|--- |--- |
| **[!UICONTROL Associate to Website]** | Identificeert de website die is gekoppeld aan de klantenaccount. |
| **[!UICONTROL Group]** | Identificeert de [ klantengroep ](../customers/customer-groups.md) waar de klant een lid is. Selecteer, indien van toepassing, het selectievakje om automatische groepswijziging op basis van BTW uit te schakelen. |
| **[!UICONTROL Name Prefix]** | Indien gebruikt, het voorvoegsel dat aan de naam van de klant (zoals Mr., Mw., of Dr.) wordt geassocieerd. De prefixwaarden worden bepaald door de [ configuratie ](../configuration-reference/customers/customer-configuration.md). Afhankelijk van de configuratie, zou de inputcontrole een tekstgebied of een lijst van opties kunnen zijn. |
| **[!UICONTROL First Name]** | De voornaam van de klant. |
| **[!UICONTROL Middle Name / Initial]** | De middelste naam of initiaal van de klant. Dit gebied is inbegrepen slechts als gespecificeerd in het [ configuratie](../configuration-reference/customers/customer-configuration.md) onderwerp. |
| **[!UICONTROL Last Name]** | De achternaam van de klant. |
| **[!UICONTROL Name Suffix]** | Indien gebruikt, het achtervoegsel dat met de naam van de klant (zoals Jr., Sr., of III) wordt geassocieerd. De achtervoegselwaarden worden bepaald door de [ configuratie ](../configuration-reference/customers/customer-configuration.md). Afhankelijk van de configuratie kan het invoerbesturingselement een tekstveld of een vervolgkeuzelijst met opties zijn. |
| **[!UICONTROL Email]** | Het e-mailadres van de klant |
| **[!UICONTROL Date of Birth]** | De geboortedatum van de klant. De geboortedatum is inbegrepen als gespecificeerd in het [ configuratie](../configuration-reference/customers/customer-configuration.md) onderwerp. <br><br> in overeenstemming met huidige veiligheid en privacy beste praktijken, ben zich bewust van om het even welke potentiële wettelijke en veiligheidsrisico&#39;s verbonden aan de opslag van de volledige geboortedatum van klanten (maand, dag, jaar) met andere persoonlijke herkenningstekens. U wordt aangeraden de opslag van de volledige geboortedatum van de klant te beperken en u aan te raden het geboortejaar van de klant als alternatief te gebruiken. |
| **[!UICONTROL Tax / VAT Number]** | Het BTW-nummer of BTW-nummer van de klant, indien van toepassing. |
| **[!UICONTROL Gender]** | Identificeert het geslacht van de klant. Het geslacht is inbegrepen als gespecificeerd in de [ configuratie ](../configuration-reference/customers/customer-configuration.md). Opties: `Male` / `Female` / `Not Specified` |
| **[!UICONTROL Send Welcome Email From]** | Als u meerdere winkelweergaven hebt, geeft deze instelling de winkelweergave aan waaruit het welkomstbericht wordt verzonden. Als de opslagmeningen voor verschillende talen worden gebruikt, bepaalt dit het plaatsen de taal van welkome e-mail. |

### [!UICONTROL Addresses]

| Veld | Beschrijving |
|--- |--- |
| **[!UICONTROL New Addresses]** | Identificeert het type van nieuw adres. Opties: `Default Billing Address` / `Default Shipping Address` |
| **[!UICONTROL Add New Addresses]** | Toont een andere Nieuwe sectie van het Adres om het type van het adres te identificeren dat moet worden ingegaan. |
| **[!UICONTROL Company]** | De bedrijfsnaam, indien van toepassing voor dit adres. |
| **[!UICONTROL Street Address]** | Het adres van de klant. Een tweede lijn van het straatadres is beschikbaar als gespecificeerd in het [ configuratie](../configuration-reference/customers/customer-configuration.md) onderwerp. |
| **[!UICONTROL City]** | De plaats waar het klantenadres wordt gevestigd. |
| **[!UICONTROL Country]** | Het land waar het klantenadres wordt gevestigd. |
| **[!UICONTROL State/Province]** | De staat of provincie waar het klantenadres wordt gevestigd. |
| **[!UICONTROL Zip/Postal Code]** | De postcode of postcode waar het klantenadres wordt gevestigd. |
| **[!UICONTROL Phone Number]** | Het telefoonnummer van de klant dat aan het adres is gekoppeld. |
| **[!UICONTROL VAT Number]** | Indien van toepassing, het btw-nummer dat op dit adres op de klant van toepassing is. |
