---
title: Een bedrijfsaccount maken
description: Meer informatie over het maken van bedrijfsaccounts vindt u in Adobe Commerce Admin en op de winkel.
exl-id: 8c06395b-102b-4a41-8eb3-e6a344feac70
feature: B2B, Companies, Configuration, Storefront
role: Admin, User
source-git-commit: 30c988ac7d4108ae85980498472d96363107212c
workflow-type: tm+mt
source-wordcount: '1750'
ht-degree: 0%

---

# Een bedrijfsaccount maken

De rekeningen van het bedrijf kunnen opstelling van de opslagplaats door de klant, of van Admin zijn. Alle verzoeken om een bedrijfsaccount te maken moeten worden goedgekeurd door de beheerder van de winkel voordat de account actief wordt.

Aan de persoon die een bedrijfsaccount instelt vanuit de storefront, krijgt een rol als [bedrijfsbeheerder](account-company-admin.md) toegewezen. Nadat het verzoek om een bedrijfsaccount te maken is goedgekeurd, kan de bedrijfsbeheerder een accountwachtwoord instellen en zich aanmelden bij het account.

## Methode 1: Klant maakt de account vanaf de storefront

>[!IMPORTANT]
>
>Als u deze methode wilt ondersteunen (zodat klanten hun bedrijf via de storefront kunnen registreren), moet u ervoor zorgen dat de [B2B-functies](enable-basic-features.md) zijn ingeschakeld.

1. In de rechterbovenhoek van de storefront-header klikt **[!UICONTROL Create an Account]** de klant en kiest **[!UICONTROL Create New Company Account]** de klant .

   ![ creeer Nieuwe Rekening van het Bedrijf ](./assets/company-account-create-storefront-options.png){width="700" zoomable="yes"}

   >[!NOTE]
   >
   >Als een bezoeker is aangemeld bij een geregistreerde gebruikersaccount, kan hij of zij een bedrijfsaccount maken door naar _[!UICONTROL Customer Profile]_>**[!UICONTROL Company Structure]**>**[!UICONTROL Create a Company Account]**te navigeren.

1. In de sectie _[!UICONTROL Company Information]_doet de klant het volgende:

   - Vul de vereiste velden in:

      - **[!UICONTROL Company Name]**
      - **[!UICONTROL Company Email]**

   - Vul de overige velden in, indien van toepassing:

      - **[!UICONTROL Company Legal Name]**
      - **[!UICONTROL VAT/TAX ID]**
      - **[!UICONTROL Reseller ID]**

   ![ Informatie van het Bedrijf ](./assets/company-information-storefront.png){width="700" zoomable="yes"}

1. Hiermee vult u de vereiste velden in de sectie _[!UICONTROL Legal Address]_in.

   - **[!UICONTROL Street Address]**
   - **[!UICONTROL City]**
   - **[!UICONTROL Country]**
   - **[!UICONTROL State/Province]**
   - **[!UICONTROL ZIP/Postal Code]**
   - **[!UICONTROL Phone Number]**

   ![ Juridisch Adres ](./assets/company-legal-address-storefront.png){width="700" zoomable="yes"}

1. Voer in de sectie _[!UICONTROL Company Administrator]_de volgende handelingen uit:

   - Voer de **[!UICONTROL Email address]** in voor de bedrijfsbeheerder.

     Het e-mailadres van de bedrijfsbeheerder kan hetzelfde zijn als het e-mailadres van het bedrijf of een ander e-mailadres. Als u een ander e-mailadres invoert, wordt naast de beheerdersaccount van het bedrijf ook een gebruikersaccount gemaakt.

   - Voer de **[!UICONTROL First Name]** en **[!UICONTROL Last Name]** van de bedrijfsbeheerder in.

   - Vul desgewenst de volgende velden in:

      - **[!UICONTROL Job Title]**
      - **[!UICONTROL Gender]**

   ![ Beheerder van het Bedrijf ](./assets/company-administrator-account-storefront.png)

1. Hiermee wordt de validatie voltooid als reCAPTCHA is ingeschakeld voor deze storefront-functie.

1. Selecteer **[!UICONTROL Submit]** wanneer de informatie is voltooid.

   Wanneer het verzoek om een bedrijfsaccount te maken door de verkoper wordt goedgekeurd, wordt een e-mailmelding naar de bedrijfsbeheerder verzonden.

   ![ Welkome E-mail van het Voorbeeld ](./assets/company-admin-welcome-email.png){width="500"}

   Wanneer het wachtwoord wordt geplaatst, kan de bedrijfbeheerder [ binnen ](../customers/customer-sign-in.md) aan de rekening ondertekenen.

## Methode 2: Merchant maakt het account van de beheerder

Het proces om een bedrijf van Admin te creëren is in wezen het zelfde als van de winkel, maar met extra gebieden.

![ voeg een nieuw bedrijf van Admin ](./assets/company-add-new.png){width="700" zoomable="yes"} toe

1. Op _Admin_ sidebar, ga naar **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Klik op **[!UICONTROL Add New Company]** en voer de volgende handelingen uit:

   - Vul de volgende vereiste velden in:

      - **[!UICONTROL Company Name]**
      - **[!UICONTROL Company Email]**

   - Als u nog niet klaar bent om het account live te laten gaan, stelt u de optie **[!UICONTROL Status]** in op `Pending Approval`. (Ingesteld op `Active` standaard.)

   - Kies, indien van toepassing, het beheerdersaccount van de **[!UICONTROL Sales Representative]** beheerder die het account moet beheren.

1. Ga in de _[!UICONTROL Account Information]_sectie als volgt te werk:

   - Vul de volgende velden in, indien van toepassing:

      - **[!UICONTROL Company Legal Name]**
      - **[!UICONTROL VAT/TAX ID]**
      - **[!UICONTROL Reseller ID]**

   - Voer voor **[!UICONTROL Comment]** aanvullende informatie in over de klant die nodig kan zijn.

     De opmerkingen zijn alleen zichtbaar vanuit de beheerder.

   ![ de Informatie van de Rekening ](./assets/company-create-account-information-admin.png){width="700" zoomable="yes"}

1. Bij het maken van het eerste bedrijf is het raster _[!UICONTROL Company Hierarchy]_leeg wanneer u het uitbreidt. Nadat u het bedrijf hebt opgeslagen, kunt u het in een bedrijfshiërarchie opnemen. Zie [ Beheer van het Bedrijf ](manage-companies.md).

1. Voer in de sectie _[!UICONTROL Legal Address]_de volgende vereiste velden in:

   - **[!UICONTROL Street Address]**
   - **[!UICONTROL City Country]**
   - **[!UICONTROL ZIP/Postal Code]**
   - **[!UICONTROL Phone Number]**

1. Ga als volgt te werk in de sectie _[!UICONTROL Company Admin]_:

   - Vul de volgende vereiste velden in:

      - **[!UICONTROL Email]**
      - **[!UICONTROL First Name]**
      - **[!UICONTROL Last Name]**

   - Vul de volgende optionele onderdelen van de naam in, die mogelijk van toepassing zijn op bepaalde klantnamen, meer dan andere, en die naar uw goeddunken kunnen worden gebruikt:

      - **[!UICONTROL Prefix]**
      - **[!UICONTROL Middle Name/Initial]**
      - **[!UICONTROL Suffix]**

   - Als de informatie beschikbaar is, voltooi de resterende gebieden om de bedrijfbeheerder te beschrijven:

      - **[!UICONTROL Website]**
      - **[!UICONTROL Job Title]**
      - **[!UICONTROL Gender]**
      - **[!UICONTROL Send Welcome Email From]**

   ![ Bedrijf Admin ](./assets/company-create-company-admin.png){width="700" zoomable="yes"}

1. Voer in de sectie _[!UICONTROL Company Credit]_, die een overzicht weergeeft van de kredietactiviteiten van de klant, zoveel velden in het onderste gedeelte van de sectie in als van toepassing is:

   - **[!UICONTROL Credit Currency]**
   - **[!UICONTROL Credit Limit]**
   - **[!UICONTROL Allow to Exceed Credit Limit]**
   - **[!UICONTROL Reason for Change]**

   ![ Krediet van het Bedrijf ](./assets/company-create-credit-admin.png){width="700" zoomable="yes"}

1. Ga als volgt te werk in de sectie _[!UICONTROL Advanced Settings]_:

   >[!NOTE]
   >
   >De toewijzing van de klantengroep bepaalt welke gedeelde catalogus aan het bedrijf en zijn werknemers beschikbaar is. Standaard wordt het bedrijf toegewezen aan de klantgroep die als standaard in de configuratie is ingesteld.

   - U kunt de toewijzing **[!UICONTROL Customer Group]** voor het bedrijf en zijn werknemers wijzigen in een groep die toegang heeft tot een andere gedeelde catalogus of tot een standaardklantengroep. U wordt gevraagd te bevestigen voordat de groep wordt gewijzigd.

     ![ Veranderend de klantengroep ](./assets/company-advanced-settings-customer-group-admin.png){width="600"}

   - Stel **[!UICONTROL Allow Quotes]** in op `Yes` als u wilt toestaan dat bedrijfswerknemers aanhalingstekens kunnen genereren van hun account.

   - Stel **[!UICONTROL Enable Purchase Orders]** in op `Yes` als u wilt toestaan dat bedrijfswerknemers kooporders van hun account kunnen maken en gebruiken.

   - Als u de **[!UICONTROL Applicable Payment Methods]** wilt wijzigen die beschikbaar zijn voor het bedrijf, schakelt u het selectievakje **[!UICONTROL Use config settings]** uit en kiest u een van de volgende opties:

     | Optie | Beschrijving |
     |-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
     | `B2B Payment Methods` | (Gebrek) laat alle [ betalingsmethodes toe die als gebrek ](../configuration-reference/general/b2b-features.md#default-b2b-payment-methods) voor B2B- orden worden geplaatst. |
     | `All Enabled Payment Methods` | Maakt alle [ toegelaten betalingsmethodes ](../configuration-reference/sales/payment-methods.md) beschikbaar voor klantenrekeningen verbonden aan de bedrijfrekening. |
     | `Selected Payment Methods` | Hiermee kunt u de betalingsmethoden selecteren die beschikbaar zijn voor klantenaccounts die bij het bedrijfsaccount horen. Als u meerdere betalingsmethoden wilt selecteren, houdt u Ctrl (PC) of Command (Mac) ingedrukt en selecteert u elke optie. |

     {style="table-layout:auto"}

   - Als u de **[!UICONTROL Applicable Shipping Methods]** beschikbare opties voor het bedrijf wilt wijzigen, schakelt u het **[!UICONTROL Use config settings]** selectievakje uit en kiest u een van de volgende opties:

     | Optie | Beschrijving |
     |--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
     | `B2B Shipping Methods` | (Standaardinstelling) Hiermee kunnen alle [verzendmethoden als standaard](../configuration-reference/general/b2b-features.md#default-b2b-shipping-methods) worden ingesteld voor B2B-bestellingen. |
     | `All Enabled Shipping Methods` | Maakt alle [ toegelaten verschepende methodes ](../configuration-reference/sales/delivery-methods.md) beschikbaar voor klantenrekeningen verbonden aan de bedrijfrekening. |
     | `Selected Shipping Methods` | Hiermee kunt u de verzendmethoden selecteren die beschikbaar zijn voor klantenaccounts die zijn gekoppeld aan het bedrijfsaccount. Als u meerdere verzendmethoden wilt selecteren, houdt u Ctrl (PC) of Command (Mac) ingedrukt en selecteert u elke optie. |

     {style="table-layout:auto"}

1. Selecteer **[!UICONTROL Save]** wanneer deze bewerking is voltooid.

   Wanneer het verzoek om een bedrijfsaccount te maken door de verkoper wordt goedgekeurd, wordt een e-mailmelding verzonden naar het e-mailadres van de bedrijfsbeheerder.

   Wanneer het wachtwoord wordt geplaatst, kan de bedrijfbeheerder [ binnen ](../customers/customer-sign-in.md) aan de rekening ondertekenen.

## Knopbalk

| Knop | Beschrijving |
|---------------------------|------------------------------------------------------------------|
| [!UICONTROL Back] | Hiermee gaat u terug naar de pagina Companies zonder de wijzigingen op te slaan. |
| [!UICONTROL Reset] | Hiermee herstelt u de oorspronkelijke waarden in alle velden met niet-opgeslagen wijzigingen. |
| [!UICONTROL Save] | Hiermee slaat u wijzigingen op in het bedrijf en houdt u het profiel open. |
| [!UICONTROL Save & Close] | Hiermee slaat u wijzigingen op in het bedrijf en sluit u het profiel. |

{style="table-layout:auto"}

## Veldomschrijvingen

| Veld | Beschrijving |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Name] | De bedrijfsnaam wordt ingevoerd wanneer het bedrijfsaccount voor het eerst wordt gemaakt en kan een verkorte versie van de volledige juridische naam zijn. |
| [!UICONTROL Status] | (Alleen beheerder) Geeft de huidige status van het bedrijfsaccount aan. Opties: <br/>**[!UICONTROL Active]**- Het bedrijfsaccount wordt goedgekeurd door de beheerder van de winkel. De bedrijfsbeheerder en de gekoppelde leden kunnen zich bij de winkel aanmelden bij het account en aankopen doen.<br/>**[!UICONTROL Pending Approval]** - Er is een verzoek ingediend om een bedrijfsaccount te openen, maar dit is nog niet goedgekeurd door de beheerder van de winkel. <br/>**[!UICONTROL Rejected]**- Er is een verzoek ingediend om een bedrijfsaccount te openen, maar dit is niet goedgekeurd door de beheerder van de winkel. De initiële aanmeldingsgegevens die zijn gebruikt om de aanvraag in te dienen, worden geblokkeerd.<br/>** Geblokkeerd **- de leden van het bedrijf kunnen login en tot de catalogus toegang hebben, maar kunnen geen aankopen maken. De opslagbeheerder kan een bedrijfsaccount blokkeren die niet in goede staat is. Het blok op het account kan op elk moment worden verwijderd door de beheerder van de winkel. |
| [!UICONTROL Company Email] | Het e-mailadres dat aan het bedrijfsaccount is gekoppeld. |
| [!UICONTROL Sales Representative] | (Alleen beheerder) De beheerder die de primaire contactpersoon voor het bedrijfsaccount is. |

{style="table-layout:auto"}

### [!UICONTROL Account Information]

| Veld | Beschrijving |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Legal Name] | De volledige juridische naam van het bedrijf. |
| [!UICONTROL VAT / TAX ID] | Het [btw-nummer](../stores-purchase/vat.md) dat door sommige jurisdicties aan het bedrijf is toegewezen voor belastingaangifte. Zie [Nieuwe accountopties](../configuration-reference/customers/customer-configuration.md) maken om het btw-/belastingnummer van de klant te configureren zodat deze in de etalage wordt weergegeven. <br/> **_Opmerking:_** De bedrijfsbeheerder en andere gebruikers van het bedrijf hebben geen eigen btw-nummer of btw-nummer in hun klantenaccount. |
| [!UICONTROL Reseller ID] | Het wederverkoopnummer dat aan de onderneming is toegekend voor belastingverslagleggingsdoeleinden. |
| [!UICONTROL Comment] | (Alleen beheerder) Deze opmerkingen over het bedrijfsaccount zijn ter referentie en zijn alleen zichtbaar voor de beheerder. |

{style="table-layout:auto"}

### [!UICONTROL Company Hierarchy]

| Veld | Beschrijving |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company ID] | Het ID-nummer van het bedrijf. |
| [!UICONTROL Company Name] | De volledige naam van het bedrijf. <br/> A `current company indicator` wordt weergegeven in de bedrijfslijn die wordt bewerkt. |
| [!UICONTROL Company Email] | Het e-mailadres dat aan het bedrijfsaccount is gekoppeld. |
| [!UICONTROL Phone Number] | Het primaire telefoonnummer van het bedrijf. |
| [!UICONTROL Country] | Het land waar de onderneming is geregistreerd om zaken te doen. |
| [!UICONTROL State/Province] | De staat of provincie waar het bedrijf is geregistreerd om zaken te doen. |
| [!UICONTROL City] | De stad waar de onderneming is geregistreerd om zaken te doen. |
| [!UICONTROL Group/Shared Catalog] | (Admin slechts) wijst op de [ klantengroep ](../customers/customer-groups.md) of [ gedeelde catalogus ](catalog-shared.md) die aan het bedrijf wordt toegewezen. |
| [!UICONTROL Company Admin] | De volledige naam van de bedrijfbeheerder. |
| [!UICONTROL Action] | De lijst van mogelijke acties voor die bedrijfslijn. |

{style="table-layout:auto"}

### [!UICONTROL Legal Address]

| Veld | Beschrijving |
|------------------------------|-----------------------------------------------------------------------------|
| [!UICONTROL Street Address] | Het adres waar de onderneming is geregistreerd om zaken te doen. |
| [!UICONTROL City] | De stad waar de onderneming is geregistreerd om zaken te doen. |
| [!UICONTROL Country] | Het land waar de onderneming is geregistreerd om zaken te doen. |
| [!UICONTROL State/Province] | De staat of provincie waar het bedrijf is geregistreerd om zaken te doen. |
| [!UICONTROL ZIP/Postal Code] | De postcode of postcode waar de onderneming geregistreerd is om zaken te doen. |
| [!UICONTROL Phone Number] | Het primaire telefoonnummer van het bedrijf. |

{style="table-layout:auto"}

### [!UICONTROL Company Admin]

| Veld | Beschrijving |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Website] | Hiermee bepaalt u de website waartoe de beheerder van het bedrijf behoort. |
| [!UICONTROL Job Title] | De titel van de bedrijfsbeheerder die de bedrijfsaccount beheert. |
| [!UICONTROL Email] | Het e-mailadres van de bedrijfsbeheerder kan hetzelfde zijn als het e-mailadres van het bedrijf. Als een ander e-mailadres wordt ingevoerd, wordt naast het bedrijfsaccount ook een apart individueel account gemaakt voor de bedrijfsbeheerder. |
| [!UICONTROL Prefix] | Indien van toepassing, het voorvoegsel dat aan de naam van de bedrijfsbeheerder is gekoppeld (zoals `Mr.`, `Ms.`, `Mrs.`of `Dr.`). Afhankelijk van de configuratie kan het invoerveld een tekstveld of lijst zijn. |
| [!UICONTROL First Name] | De voornaam van de beheerder van het bedrijf. |
| [!UICONTROL Middle Name/Initial] | De middelste naam of initialen van de beheerder van het bedrijf. |
| [!UICONTROL Last Name] | De achternaam van de bedrijfsbeheerder. |
| [!UICONTROL Suffix] | Indien van toepassing, het achtervoegsel dat aan de naam van de bedrijfbeheerder (zoals `Jr.`, `Sr.`, of `III.`) wordt geassocieerd. Afhankelijk van de configuratie kan het invoerveld een tekstveld of lijst zijn. |
| [!UICONTROL Gender] | Het geslacht van de bedrijfsbeheerder. Opties: `Male` / `Female` / `Not Specified` |
| [!UICONTROL Send Welcome Email From] | De winkelweergave van waaruit de welkomstmail moet worden verzonden. |

{style="table-layout:auto"}

### [!UICONTROL Company Credit]

| Veld | Beschrijving |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Credit Currency] | (Alleen beheerder) De valuta die door de winkel wordt geaccepteerd voor aankopen op bedrijfskrediet. |
| [!UICONTROL Credit Limit] | (Alleen beheerder) De kredietlimiet die wordt uitgebreid naar de bedrijfsaccount. |
| [!UICONTROL Allow to Exceed Credit Limit] | (Alleen beheerder) Geeft aan of het bedrijf toestemming heeft om de kredietlimiet te overschrijden. Opties: `Yes` / `No` |
| [!UICONTROL Reason for Change] | (Alleen beheerder) Een opmerking die verklaart waarom het bedrijf de kredietlimiet mag of mag overschrijden. Dit veld is alleen actief als de toestemming om de kredietlimiet te overschrijden wordt gewijzigd. |

{style="table-layout:auto"}

### [!UICONTROL Advanced Settings]

| Veld | Beschrijving |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Customer Group] | (Admin slechts) wijst op de [ klantengroep ](../customers/customer-groups.md) of [ gedeelde catalogus ](catalog-shared.md) die aan het bedrijf wordt toegewezen. |
| [!UICONTROL Allow Quotes] | (Alleen beheerder) Hiermee bepaalt u of leden van het bedrijf namens het bedrijf onderhandelbare offertes kunnen opstellen en indienen. |
| [!UICONTROL Enable Purchase Orders] | (Slechts Admin) bepaalt als de bedrijfsleden bestellingen als [ koopgeorden ](account-dashboard-my-purchase-orders.md) namens het bedrijf kunnen voorleggen. |
| Toepasselijke betalingsmethoden | (Alleen beheerder) Hiermee geeft u de betaalmethoden aan die beschikbaar zijn voor aankopen door bedrijven. Opties: `B2B Payment Methods` / `All Enabled Payment Methods` / `Selected Payment Methods` |
| [!UICONTROL Payment Methods] | (Alleen beheerder) Wordt actief als specifieke betaalmethoden worden geactiveerd. Als u meerdere betaalmethoden beschikbaar wilt maken voor het bedrijfsaccount, houdt u Ctrl (pc) of Command (Mac) ingedrukt en selecteert u elke optie. |
| [!UICONTROL Applicable Shipping Methods] | (Alleen beheerder) Geeft de verzendmethoden aan die beschikbaar zijn voor aankopen door bedrijven. Opties: `B2B Shipping Methods` / `All Enabled Shipping Methods` / `Selected Shipping Methods` |
| [!UICONTROL Shipping Methods] | (Alleen beheerder) Wordt actief als specifieke verzendmethoden zijn geactiveerd. Als u meerdere betaalmethoden beschikbaar wilt maken voor het bedrijfsaccount, houdt u Ctrl (pc) of Command (Mac) ingedrukt en selecteert u elke optie. |

{style="table-layout:auto"}
