---
title: Naam en adresopties van de klant
description: De naam- en adresopties van de klant bepalen welke velden worden opgenomen in de naam- en adresformulieren.
exl-id: 28949cfc-2c96-4d0a-a35b-b37b3aa2d1e9
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '806'
ht-degree: 0%

---

# Naam en adresopties van de klant

De _Opties van de Naam en van het Adres_ bepalen welke gebieden in de naam en adresvormen inbegrepen zijn wanneer de klanten een [ rekening ](../customers/account-create.md) met uw opslag creëren.

![ de aanmeldingsvorm van de Rekening van de Klant ](assets/storefront-customer-account-address-book.png){width="500" zoomable="yes"}

De stappen voor het configureren van de naam- en adresopties verschillen voor Adobe Commerce en Magento Open Source.

## Naam- en adresopties configureren voor Adobe Commerce

U kunt de naam- en adresopties configureren die aan klanten in de winkel worden voorgesteld wanneer zij hun account maken.

### Stap 1: Plaats het werkingsgebied van de configuratie

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Customers]** uit en kies **[!UICONTROL Customer Configuration]** .

1. Vouw de sectie **[!UICONTROL Name and Address Options]** uit.

   >[!INFO]
   >
   >Het bereik van de naam- en adresopties is van toepassing op het niveau `website` .

1. Schuif omhoog naar de bovenkant van de pagina en stel het bereik van de configuratie in op een van de volgende opties:

   - `Default Config`
   - `Main Website` (of specifieke site voor installaties met meerdere sites)

   >[!INFO]
   >
   >De sectie _[!UICONTROL Name and Address Options]_&#x200B;wordt niet weergegeven wanneer het bereik is ingesteld op `Default Store View` .

   ![ Toepassingsgebied van de Configuratie ](assets/customer-configuration-scope-ee.png){width="700" zoomable="yes"}

### Stap 2: Vorm de naam en adresopties

1. Terugkeer aan de [!UICONTROL _sectie van de Opties van de Naam en van het Adres_] van de pagina van de Configuratie van de Klant.

   >[!INFO]
   >
   > Als u de instelling voor het bereik `Default config` niet gebruikt, moet u het selectievakje `Use Default` voor elk veld wissen voordat u de waarde wijzigt.

   ![ de Opties van de Naam en van het Adres ](../configuration-reference/customers/assets/customer-configuration-name-address-options-ee.png){width="600" zoomable="yes"}

1. Voer bij **[!UICONTROL Prefix Dropdown Options]** elk voorvoegsel in dat u in de lijst wilt weergeven, gescheiden door een puntkomma.

   >[!IMPORTANT]
   >
   >Plaats een puntkomma voor de eerste waarde om een lege waarde boven aan de lijst weer te geven.

1. Voer bij **[!UICONTROL Suffix Dropdown Options]** elk achtervoegsel in dat u in de lijst wilt weergeven, gescheiden door een puntkomma.

1. Als u de volgende velden in klantformulieren wilt opnemen, stelt u de waarde van elk veld in op `Optional` of `Required` , indien nodig.

   - **[!UICONTROL Show Telephone]**
   - **[!UICONTROL Show Company]**
   - **[!UICONTROL Show Fax]**

### Stap 3: Opslaan en vernieuwen

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

1. In het bericht bij de bovenkant van de pagina, klik **[!UICONTROL Cache Management]** en [ vernieuw ](../systems/cache-management.md) elk ongeldig geheime voorgeheugen.

## Naam- en adresopties configureren voor Magento Open Source

Configureer de naam- en adresopties die aan klanten in de winkel worden gepresenteerd wanneer ze hun account maken.

![ de aanmeldingsvorm van de Rekening van de Klant ](assets/storefront-customer-account-signup.png){width="500" zoomable="yes"}

### Stap 1: Plaats het werkingsgebied van de configuratie

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Customers]** uit en kies **[!UICONTROL Customer Configuration]** .

1. Vouw de sectie **[!UICONTROL Name and Address Options]** uit.

   >[!IMPORTANT]
   >
   > Het bereik van de naam- en adresopties is van toepassing op het niveau `website` .

   ![ de Opties van de Naam en van het Adres ](../configuration-reference/customers/assets/customer-configuration-name-address-options-ce.png){width="600" zoomable="yes"}

1. Blader naar de bovenkant van de pagina en stel het bereik van de configuratie in op een van de volgende opties:

   - `Default Config`
   - `Main Website` (of specifieke site voor installaties met meerdere sites)

   >[!NOTE]
   >
   >De _sectie van de Opties van de Naam en van het Adres_ verschijnt niet wanneer het werkingsgebied aan `Default Store View` wordt geplaatst.

   ![ Toepassingsgebied van de Configuratie ](assets/configuration-scope.png){width="600" zoomable="yes"}

### Stap 2: Vorm de naam en adresopties

1. Terugkeer aan de [!UICONTROL _sectie van de Opties van de Naam en van het Adres_] van de pagina van de Configuratie van de Klant.

   >[!INFO]
   >
   >Als u de instelling voor het bereik `Default config` niet gebruikt, moet u het selectievakje `Use Default` voor elk veld wissen voordat u de waarde wijzigt.

1. Voor **Aantal Lijnen in een Adres van de Straat**, ga een aantal van 1 tot 4 in.

   >[!WARNING]
   >
   >Standaard is het adres van de straat drie regels.

1. Om een prefix (zoals Mr of Mw.) als deel van de naam te omvatten, plaats **toont Prefix** aan `Yes`.

   ![ Prefix in klant onderteken omhoog vorm ](assets/storefront-customer-account-prefix.png){width="600" zoomable="yes"}

   >[!INFO]
   >
   >Voor **Opties van de Vervolgkeuzelijst van het Prefix**, ga elke prefix in die u in de lijst wilt verschijnen, die door een puntkomma wordt gescheiden. U kunt een puntkomma vóór de eerste waarde plaatsen om een lege waarde boven aan de lijst weer te geven.

1. Als u een optioneel veld voor de middelste of oorspronkelijke naam van de klant wilt opnemen, stelt u **[!UICONTROL Show Middle Name (initial)]** in op `Yes` .

1. Een achtervoegsel opnemen (zoals Jr. of Sr.) na de naam van de klant, stel **[!UICONTROL Show Suffix]** in op een van de volgende waarden:

   - `Optional`
   - `Required`

   >[!INFO]
   >
   >Voor **Opties van de Dropdown van het Achtervoegsel van het Achtervoegsel**, ga elk achtervoegsel in dat u in de lijst wilt verschijnen, die door een puntkomma wordt gescheiden. U kunt een puntkomma vóór de eerste waarde plaatsen om een lege waarde boven aan de lijst weer te geven.

1. Als u de geboortedatum wilt opnemen, stelt u **[!UICONTROL Show Date of Birth]** in op een van de volgende opties:

   - `Optional`
   - `Required`

   >[!INFO]
   >
   >In overeenstemming met de huidige beste praktijken op het gebied van beveiliging en privacy, dient u zich bewust te zijn van mogelijke juridische en veiligheidsrisico&#39;s die verbonden zijn aan de opslag van de volledige geboortedatum van de klant (maand, dag, jaar) met andere persoonlijke identificatoren. U wordt aangeraden de opslag van de volledige geboortedatum van de klant te beperken en u aan te raden het geboortejaar van de klant als alternatief te gebruiken.

   Klanten kunnen het kalenderpictogram na het veld gebruiken om de geboortedatum in een pop-upkalender te kiezen.

   ![ Datum van Opkomst in klant onderteken vorm ](assets/storefront-customer-account-date-of-birth.png){width="600" zoomable="yes"}

1. Om klanten toe te staan om hun belasting of [ BTW ](../stores-purchase/vat.md) aantal in te gaan, plaats **[!UICONTROL Show Tax/VAT Number]** aan één van het volgende:

   - `Optional`
   - `Required`

1. Als u een veld voor geslacht wilt opnemen in het klantformulier, stelt u **[!UICONTROL Show Gender]** in op een van de volgende opties:

   - `Optional`
   - `Required`

   ![ de Opties van het Geslacht in de vorm van de klantenaanmelding ](assets/storefront-customer-account-gender.png){width="600" zoomable="yes"}

1. Als u de volgende velden in klantformulieren wilt opnemen, stelt u de waarde van elk veld in op `Optional` of `Required` , indien nodig.

   - **[!UICONTROL Show Telephone]**
   - **[!UICONTROL Show Company]**
   - **[!UICONTROL Show Fax]**

### Stap 3: Opslaan en vernieuwen

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

1. In het bericht bij de bovenkant van de pagina, klik **[!UICONTROL Cache Management]** en [ vernieuw ](../systems/cache-management.md) elk ongeldig geheime voorgeheugen.
