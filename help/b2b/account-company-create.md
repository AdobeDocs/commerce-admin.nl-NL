---
title: Een bedrijfsaccount maken
description: Meer informatie over het maken van bedrijfsaccounts vindt u in Adobe Commerce Admin en op de winkel.
exl-id: 8c06395b-102b-4a41-8eb3-e6a344feac70
feature: B2B, Companies, Configuration, Storefront
role: Admin, User
source-git-commit: 582f15c422e43af9acec6313c7b777b3126030f8
workflow-type: tm+mt
source-wordcount: '1784'
ht-degree: 0%

---

# Een bedrijfsaccount maken

De rekeningen van het bedrijf kunnen opstelling van de opslagplaats door de klant, of van Admin zijn. Alle verzoeken om een bedrijfsaccount te maken moeten worden goedgekeurd door de beheerder van de winkel voordat de account actief wordt.

De persoon die opstelling een bedrijfrekening van de opslag wordt toegewezen een rol als [ bedrijfbeheerder ](account-company-admin.md). Nadat het verzoek om een bedrijfrekening tot stand te brengen wordt goedgekeurd, kan de bedrijfbeheerder een rekeningswachtwoord plaatsen en login aan de rekening.

## Methode 1: de klant maakt de account aan via de winkel

>[!IMPORTANT]
>
>Om deze methode te steunen (die klanten toestaat om hun bedrijf van de winkel te registreren), zorg ervoor dat de [ Functies B2B ](enable-basic-features.md) worden gevormd zodat **[!UICONTROL Allow Company Registration from the Storefront]** aan `Yes` wordt geplaatst.

1. In de rechterbovenhoek van de winkelkoptekst klikt de klant op **[!UICONTROL Create an Account]** en kiest de klant **[!UICONTROL Create New Company Account]** .

   ![ creeer Nieuwe Rekening van het Bedrijf ](./assets/company-account-create-storefront-options.png){width="700" zoomable="yes"}

   >[!NOTE]
   >
   >Als een bezoeker is aangemeld bij een geregistreerde gebruikersaccount, kan hij of zij een bedrijfsaccount maken door naar _[!UICONTROL Customer Profile]_>**[!UICONTROL Company Structure]**>**[!UICONTROL Create a Company Account]**te navigeren. Na het aanmaken van de bedrijfsaccount wordt de account van de klant als primaire contactpersoon toegewezen. Anders maakt het systeem een klant die een e-mail ontvangt om een wachtwoord in te stellen.

1. In de sectie _[!UICONTROL Company Information]_doet de klant het volgende:

   - Vul de vereiste velden in:

      - **[!UICONTROL Company Name]**
      - **[!UICONTROL Company Email]**

   - Vul de overige velden in, al naargelang van toepassing:

      - **[!UICONTROL Company Legal Name]**
      - **[!UICONTROL VAT/TAX ID]**
      - **[!UICONTROL Reseller ID]**

   ![ Informatie van het Bedrijf ](./assets/company-information-storefront.png){width="700" zoomable="yes"}

1. Voltooit de vereiste velden in de sectie _[!UICONTROL Legal Address]_.

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

   - De volgende velden worden optioneel ingevuld:

      - **[!UICONTROL Job Title]**
      - **[!UICONTROL Gender]**

   ![ Beheerder van het Bedrijf ](./assets/company-administrator-account-storefront.png)

1. Hiermee wordt de validatie voltooid als reCAPTCHA is ingeschakeld voor deze storefront-functie.

1. Selecteer **[!UICONTROL Submit]** wanneer de informatie is voltooid.

   Wanneer het verzoek om een bedrijfsrekening tot stand te brengen door de handelaar wordt goedgekeurd, wordt de e-mailkennisgeving verzonden naar de bedrijfbeheerder.

   ![ E-mail van het Welkome E-mail van het Voorbeeld ](./assets/company-admin-welcome-email.png){width="500"}

   Wanneer het wachtwoord wordt geplaatst, kan de bedrijfbeheerder [ binnen ondertekenen ](../customers/customer-sign-in.md) aan de rekening.

## Methode 2: Merchant maakt de account via Beheer

Het proces om een bedrijf van Admin tot stand te brengen is in wezen het zelfde als van storefront, maar met extra gebieden.

![ voeg een nieuw bedrijf van Admin ](./assets/company-add-new.png){width="700" zoomable="yes"} toe

1. Voor _Admin_ sidebar, ga **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Klik op **[!UICONTROL Add New Company]** en voer de volgende handelingen uit:

   - Vul de volgende vereiste velden in:

      - **[!UICONTROL Company Name]**
      - **[!UICONTROL Company Email]**

   - Stel **[!UICONTROL Status]** in op `Pending Approval` als u niet klaar bent voor de live account. (Standaard ingesteld op `Active` .)

   - Kies, indien van toepassing, de beheerdersaccount van de **[!UICONTROL Sales Representative]** die de account moet beheren.

1. Ga als volgt te werk in de sectie _[!UICONTROL Account Information]_:

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
   >De toewijzing van de klantengroep bepaalt welke gedeelde catalogus aan het bedrijf en zijn werknemers beschikbaar is. Door gebrek, wordt het bedrijf toegewezen aan de klantengroep die als gebrek in de configuratie wordt geplaatst.

   - U kunt de **[!UICONTROL Customer Group]** taak voor het bedrijf en zijn werknemers in een groep veranderen die toegang tot een verschillende gedeelde catalogus of tot een standaardklantengroep heeft. U wordt gevraagd te bevestigen voordat de groep wordt gewijzigd.

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

   - Als u de **[!UICONTROL Applicable Shipping Methods]** wilt wijzigen die beschikbaar zijn voor het bedrijf, schakelt u het selectievakje **[!UICONTROL Use config settings]** uit en kiest u een van de volgende opties:

     | Optie | Beschrijving |
     |--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
     | `B2B Shipping Methods` | (Gebrek) laat alle [ verschepende methodes toe die als gebrek ](../configuration-reference/general/b2b-features.md#default-b2b-shipping-methods) voor B2B- orden worden geplaatst. |
     | `All Enabled Shipping Methods` | Maakt alle [ toegelaten verschepende methodes ](../configuration-reference/sales/delivery-methods.md) beschikbaar voor klantenrekeningen verbonden aan de bedrijfrekening. |
     | `Selected Shipping Methods` | Hiermee kunt u de verzendmethoden selecteren die beschikbaar zijn voor klantenaccounts die zijn gekoppeld aan het bedrijfsaccount. Als u meerdere verzendmethoden wilt selecteren, houdt u Ctrl (PC) of Command (Mac) ingedrukt en selecteert u elke optie. |

     {style="table-layout:auto"}

1. Selecteer **[!UICONTROL Save]** wanneer deze bewerking is voltooid.

   Wanneer het verzoek om een bedrijfsaccount te maken door de handelaar wordt goedgekeurd, wordt een e-mailmelding verzonden naar het e-mailadres van de bedrijfsbeheerder.

   Wanneer het wachtwoord wordt geplaatst, kan de bedrijfbeheerder [ binnen ondertekenen ](../customers/customer-sign-in.md) aan de rekening.

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
| [!UICONTROL Status] | (Alleen beheerder) Geeft de huidige status van de bedrijfsaccount aan. Opties: <br/>**[!UICONTROL Active]**- Het bedrijfsaccount wordt goedgekeurd door de beheerder van de winkel. De bedrijfsbeheerder en geassocieerde leden kunnen zich bij de winkel aanmelden en aankopen doen.<br/>**[!UICONTROL Pending Approval]** - Er is een verzoek ingediend om een bedrijfsaccount te openen, maar dit is nog niet goedgekeurd door de beheerder van de winkel. <br/>**[!UICONTROL Rejected]**- Een verzoek om een bedrijfsaccount te openen is ingediend, maar niet goedgekeurd door de beheerder van de winkel. De initiële aanmeldingsgegevens die zijn gebruikt om het verzoek in te dienen, worden geblokkeerd.<br/>** Geblokkeerd **- De leden van het Bedrijf kunnen login en tot de catalogus toegang hebben, maar kunnen geen aankopen maken. De opslagbeheerder zou een bedrijfrekening kunnen blokkeren die niet in goede staat is. Het blok op de rekening kan door de opslagbeheerder op elk ogenblik worden verwijderd. |
| [!UICONTROL Company Email] | Het e-mailadres dat aan het bedrijfsaccount is gekoppeld. |
| [!UICONTROL Sales Representative] | (Alleen beheerder) De Admin-gebruiker die de primaire contactpersoon voor het bedrijfsaccount is. |

{style="table-layout:auto"}

### [!UICONTROL Account Information]

| Veld | Beschrijving |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Legal Name] | De volledige wettelijke naam van de onderneming. |
| [!UICONTROL VAT / TAX ID] | Het [ waarde-toegevoegde belasting ](../stores-purchase/vat.md) aantal dat aan het bedrijf door sommige jurisdicties voor belastingrapporteringsdoeleinden wordt toegewezen. Om de klant BTW/BELASTINGidentiteitskaart te vormen om in de storefront te verschijnen, zie [ de Nieuwe Opties van de Rekening ](../configuration-reference/customers/customer-configuration.md) creëren. <br/> **_Nota:_** de bedrijfbeheerder en andere bedrijfgebruikers hebben hun eigen afzonderlijke BTW/BELASTINGaantallen in hun klantenrekeningen niet. |
| [!UICONTROL Reseller ID] | Het wederverkoopnummer dat aan de onderneming wordt toegekend voor belastingverslagleggingsdoeleinden. |
| [!UICONTROL Comment] | (Alleen beheerder) Deze opmerkingen over de bedrijfsaccount zijn ter referentie en zijn alleen zichtbaar vanuit de beheerder. |

{style="table-layout:auto"}

### [!UICONTROL Company Hierarchy]

| Veld | Beschrijving |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company ID] | Het ID-nummer van het bedrijf. |
| [!UICONTROL Company Name] | De volledige naam van de onderneming. <br/> A `current company indicator` verschijnt in de bedrijflijn die wordt uitgegeven. |
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
| [!UICONTROL Street Address] | Het adres van de straat waar de onderneming is geregistreerd om zaken te doen. |
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
| [!UICONTROL Email] | Het e-mailadres van de bedrijfsbeheerder kan hetzelfde zijn als het e-mailadres van het bedrijf. Als u een ander e-mailadres opgeeft, wordt naast het bedrijfsaccount een aparte account aangemaakt voor de beheerder van het bedrijf. |
| [!UICONTROL Prefix] | Indien van toepassing, het voorvoegsel dat is gekoppeld aan de naam van de bedrijfsbeheerder (bijvoorbeeld `Mr.` , `Ms.` , `Mrs.` of `Dr.` ). Afhankelijk van de configuratie kan het invoerveld een tekstveld of lijst zijn. |
| [!UICONTROL First Name] | De voornaam van de bedrijfbeheerder. |
| [!UICONTROL Middle Name/Initial] | De middelste naam of de aanvankelijke naam van de bedrijfbeheerder. |
| [!UICONTROL Last Name] | De achternaam van de bedrijfsbeheerder. |
| [!UICONTROL Suffix] | Indien van toepassing, het achtervoegsel dat aan de naam van de bedrijfbeheerder (zoals `Jr.`, `Sr.`, of `III.`) wordt geassocieerd. Afhankelijk van de configuratie kan het invoerveld een tekstveld of lijst zijn. |
| [!UICONTROL Gender] | Het geslacht van de bedrijfsbeheerder. Opties: `Male` / `Female` / `Not Specified` |
| [!UICONTROL Send Welcome Email From] | De winkelweergave vanwaar het welkomstbericht moet worden verzonden. |

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
| [!UICONTROL Allow Quotes] | (Alleen beheerder) Hiermee wordt bepaald of leden van het bedrijf namens het bedrijf verhandelbare noteringen kunnen opstellen en indienen. |
| [!UICONTROL Enable Purchase Orders] | (Alleen Admin) Hiermee bepaalt u of leden van het bedrijf orders kunnen indienen als [ inkooporders ](account-dashboard-my-purchase-orders.md) namens het bedrijf. |
| Toepasselijke betalingsmethoden | (Alleen beheerder) Geeft de betalingsmethoden aan die beschikbaar zijn voor aankopen door bedrijven. Opties: `B2B Payment Methods` / `All Enabled Payment Methods` / `Selected Payment Methods` |
| [!UICONTROL Payment Methods] | (Alleen beheerder) Wordt actief als specifieke betalingsmethoden worden geactiveerd. Als u meerdere betalingsmethoden beschikbaar wilt maken voor de bedrijfsaccount, houdt u Ctrl (PC) of Command (Mac) ingedrukt en selecteert u elke optie. |
| [!UICONTROL Applicable Shipping Methods] | (Alleen beheerder) Geeft de verzendmethoden aan die beschikbaar zijn voor aankopen door bedrijven. Opties: `B2B Shipping Methods` / `All Enabled Shipping Methods` / `Selected Shipping Methods` |
| [!UICONTROL Shipping Methods] | (Alleen beheerder) Wordt actief als specifieke verzendmethoden worden geactiveerd. Als u meerdere betalingsmethoden beschikbaar wilt maken voor de bedrijfsaccount, houdt u Ctrl (PC) of Command (Mac) ingedrukt en selecteert u elke optie. |

{style="table-layout:auto"}
