---
title: B2B-functies inschakelen
description: Meer informatie over het inschakelen van B2B-functies voor uw Adobe Commerce-winkel, zoals bedrijfsaccounts, standaardbetalingsmethoden en verzendmethoden, inkooporders en goedkeuringen voor bestellingen.
exl-id: aed203ef-f39b-4f7e-b32f-ded53eca09a8
feature: B2B, Configuration
role: Admin
source-git-commit: 99285b700b91e0072340a2231c39a8050818fd17
workflow-type: tm+mt
source-wordcount: '1635'
ht-degree: 0%

---

# B2B-functies inschakelen

Standaard zijn alle B2B-functies in eerste instantie uitgeschakeld. Een opslagbeheerder kan de B2B-functies naar wens in- of uitschakelen voor Commerce-winkels. Voor een volledige lijst van B2B configuratiemontages, zie [&#x200B; B2B de configuratieverwijzing van Eigenschappen &#x200B;](../configuration-reference/general/b2b-features.md).

Wanneer u ondersteuning voor klantbedrijven inschakelt, worden automatisch extra B2B-functies ingeschakeld:

- [[!DNL Shared Catalog]](catalog-shared.md)

  Ondersteunt aangepaste prijsconfiguratie voor verschillende bedrijven en schakelt ook categorietoestemmingen voor alle winkels in.

- [!DNL Enable Shared Catalog direct products price assigning]

  Verbetert plaatsprestaties door slechts producten op te slaan die aan een gedeelde catalogus in de prijsindex worden toegewezen. Het toelaten van deze eigenschap is een beste praktijk voor Merchants die vele gedeelde catalogi hebben om douaneprijzen voor verschillende bedrijven te beheren.

- [[!DNL B2B Quotes]](quotes.md)

  Verkopers en bedrijven krijgen de mogelijkheid om prijzen te onderhandelen.

- [!DNL B2B default payment and shipping methods]

  Hiermee bepaalt u de keuze van de betalings- en verzendopties die beschikbaar zijn voor B2B-kopers in de winkel.

De configuratie-instellingen voor deze functies zijn alleen zichtbaar wanneer [!DNL Enable Company] is ingesteld op `Yes` .

De functies B2B [[!DNL Quick Order]](quick-order.md) en [[!DNL Requisition List]](requisition-lists.md) kunnen onafhankelijk worden in- en uitgeschakeld.

## B2B-functies configureren

De opties om Adobe Commerce B2B eigenschappen te vormen zijn beschikbaar slechts op de projecten van Commerce die de [&#x200B; geïnstalleerde uitbreiding van Adobe Commerce B2B &#x200B;](install.md) hebben.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

   Als u een installatie met meerdere sites hebt, stelt u het besturingselement **[!UICONTROL Store View]** in de linkerbovenhoek in op de website waarop de configuratie van toepassing is.

1. Kies in het linkerdeelvenster onder _[!UICONTROL General]_&#x200B;de optie **[!UICONTROL B2B Features]**:

   ![&#x200B; B2B configuratie - algemeen &#x200B;](./assets/b2b-features.png){width="600"}

   - Klanten toestaan hun eigen bedrijfsaccounts te beheren en ondersteuning voor extra B2B-functies mogelijk te maken door **[!UICONTROL Enable Company]** in te stellen op `Yes` .

     Wanneer u bedrijfssteun toelaat, worden de Gedeelde Catalogus, de Citaat B2B, de Methoden van de Betaling B2B, en de methodes van de Verzending B2B automatisch toegelaten.

     ![&#x200B; B2B configuratie - bedrijfeigenschappen &#x200B;](assets/b2b-additional-features.png){width="600"}

   - Als u klanten en gasten wilt toestaan snel bestellingen te plaatsen op basis van de SKU- of productnaam, stelt u **[!UICONTROL Enable Quick Order]** in op `Yes` .

   - Stel **[!UICONTROL Enable Requisition List]** in op `Yes` als u klanten wilt toestaan om aanvraaglijsten te maken en te beheren vanuit hun accountdashboard.

     U kunt [&#x200B; ook het maximumaantal lijsten &#x200B;](configure-requisition-lists.md) vormen een klant voor hun rekening kan hebben.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

## Standaard B2B-betalings- en verzendmethoden configureren

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) uit de **[!UICONTROL Default B2B Payment Methods]** sectie.

1. Stel **[!UICONTROL Applicable Payment Methods]** in op een van de volgende opties om de standaardbetalingsmethoden voor B2B-orders vast te stellen:

   - `All Payment Methods`

   - `Selected Payment Methods`

     Voor de specifieke optie selecteert u de **[!UICONTROL Payment Methods]** die u beschikbaar wilt maken voor uw klanten door Ctrl (pc) of Command (Mac) ingedrukt te houden terwijl u op elke optie klikt.

   De lijst van [&#x200B; betaalmethodes &#x200B;](../configuration-reference/sales/payment-methods.md) toont welke opties momenteel of gehandicapt in uw opslag worden toegelaten. Naast de standaardbetalingsmethoden bevat de lijst ook de volgende elementen:

   - Er zijn geen betalingsgegevens vereist
   - [Betaling op rekening](#configure-payment-on-account)
   - Opgeslagen accounts
   - Opgeslagen kaarten

   ![&#x200B; B2B configuratie - de montages van de standaard betalingsmethode &#x200B;](./assets/b2b-features-default-payment-methods.png){width="600"}

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Default B2B Shipping Methods]** sectie uit.

1. Als u de standaardverzendmethoden voor B2B-orders wilt opgeven, stelt u **[!UICONTROL Applicable Shipping Methods]** in op een van de volgende opties:

   - `All Shipping Methods`
   - `Selected Shipping Methods`

     Selecteer voor de specifieke optie de **[!UICONTROL Shipping Methods]** die u beschikbaar wilt maken voor uw klanten door Ctrl (PC) of Command (Mac) ingedrukt te houden terwijl u op elke optie klikt.

     De lijst van het verschepen methodes toont die momenteel [&#x200B; worden toegelaten of &#x200B;](../configuration-reference/sales/delivery-methods.md) onbruikbaar gemaakt.

   ![&#x200B; B2B configuratie - standaard verschepende methodes &#x200B;](./assets/b2b-features-shipping-methods.png){width="600"}

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

## E-mailopties voor bedrijven configureren

De [&#x200B; verkoopvertegenwoordiger &#x200B;](account-company-manage.md#assign-a-sales-representative) die als primair contact voor een bedrijf wordt toegewezen wordt gevormd door gebrek als afzender van vele geautomatiseerde e-mailberichten die naar het bedrijf worden verzonden.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Customers]** uit en kies **[!UICONTROL Company Configuration]** .

1. Indien nodig, plaats **[!UICONTROL Store View]** aan de opslagmening om het [&#x200B; werkingsgebied &#x200B;](../getting-started/websites-stores-views.md#scope-settings) van de configuratie te bepalen.

1. Voltooi de sectie **[!UICONTROL Company Registration]** :

   >[!NOTE]
   >
   >Schakel het selectievakje **[!UICONTROL Use system value]** uit om het veld bewerkbaar te maken.

   - Plaats **[!UICONTROL Company Registration Email Recipient]** aan het [&#x200B; opslagcontact &#x200B;](../getting-started/store-details.md#store-email-addresses) dat moet worden op de hoogte gebracht wanneer een nieuw verzoek van de bedrijfregistratie wordt ontvangen.

   - Voer bij **[!UICONTROL Send Company Registration Email Copy To]** het e-mailadres in van elke persoon die een kopie van het registratiebericht moet ontvangen. Scheid meerdere e-mailadressen met een komma.

   - Om te bepalen hoe het exemplaar van het bericht wordt verzonden, plaats **verzendt de Methode van het E-mailExemplaar** aan één van het volgende:

      - `Bcc` - verzendt a _blinde beleefdheidsexemplaar_ door de ontvanger in de kopbal van zelfde e-mail te omvatten die naar de klant wordt verzonden. De ontvanger BCC is niet zichtbaar aan de klant.
      - `Separate Email` - Verzendt de kopie als een aparte e-mail.

   - Als u een e-mailsjabloon hebt voorbereid voor gebruik in plaats van de standaardsjabloon, stelt u **[!UICONTROL Default Company Registration Email]** in op de naam van de sjabloon. Standaard wordt de sjabloon `Company Registration Request` gebruikt.

     ![&#x200B; configuratie van Klanten - bedrijfregistratie &#x200B;](./assets/company-email-options-company-registration.png){width="600"}

1. Voltooi de sectie **[!UICONTROL Customer-Related Emails]** :

   Als u alternatieve e-mailsjablonen hebt voorbereid voor gebruik in plaats van de standaardinstellingen, kiest u de sjabloon die u wilt gebruiken voor elk van de volgende opties:

   - **[!UICONTROL Default 'Sales Rep Assigned' Email]**
   - **[!UICONTROL Default 'Assign Company to Customer' Email]**
   - **[!UICONTROL Default 'Assign Company Admin' Email]**
   - **[!UICONTROL Default 'Company Admin Inactive' Email]**
   - **[!UICONTROL Default 'Company Admin Changed to Member' Email]**
   - **[!UICONTROL Default 'Customer Status Active' Email]**
   - **[!UICONTROL Default 'Customer Status Inactive' Email]**

   ![&#x200B; configuratie van Klanten - klant verwante e-mails &#x200B;](./assets/company-email-options-customer-related-emails.png){width="600"}

1. Voltooi de sectie **[!UICONTROL Company Status Change]** :

   - Voer bij **[!UICONTROL Send Company Status Change Email Copy To]** het e-mailadres in van elke persoon die een kopie van het bericht over statuswijziging moet ontvangen. Scheid meerdere e-mailadressen met een komma.

   - Om te bepalen hoe het exemplaar van het bericht wordt verzonden, plaats **verzendt de Methode van het E-mailExemplaar** aan één van het volgende:

      - `Bcc` - verzendt a _blinde beleefdheidsexemplaar_ door de ontvanger in de kopbal van zelfde e-mail te omvatten die naar de klant wordt verzonden. De ontvanger BCC is niet zichtbaar aan de klant.
      - `Separate Email` - Verzendt de kopie als een aparte e-mail.

   - Als u een e-mailsjabloon hebt voorbereid die moet worden gebruikt wanneer de status van het bedrijf verandert van `Pending Approval` in `Active` , stelt u **[!UICONTROL Default 'Company Status Change to Active 1' Email]** in op de naam van de sjabloon. Standaard wordt de sjabloon `Company Status Active 1` gebruikt.

   - Als u een e-mailsjabloon hebt voorbereid die moet worden gebruikt wanneer de bedrijfsstatus verandert van `Rejected` of `Blocked` in `Active` , stelt u **[!UICONTROL Default 'Company Status Change to Active 2' Email]** in op de naam van de sjabloon. Standaard wordt de sjabloon `Company Status Active 2` gebruikt.

   - Als u een e-mailsjabloon hebt voorbereid die moet worden gebruikt wanneer de bedrijfsstatus verandert in `Rejected` , stelt u **[!UICONTROL Default 'Company Status Change to Rejected' Email]** in op de naam van de sjabloon. Standaard wordt de sjabloon `Company Status Rejected` gebruikt.

   - Als u een e-mailsjabloon hebt voorbereid die moet worden gebruikt wanneer de bedrijfsstatus verandert in `Blocked` , stelt u **[!UICONTROL Default 'Company Status Change to Blocked' Email]** in op de naam van de sjabloon. Standaard wordt de sjabloon `Company Status Blocked` gebruikt.

   - Als u een e-mailsjabloon hebt voorbereid die moet worden gebruikt wanneer de bedrijfsstatus verandert in `Pending Approval` , stelt u **[!UICONTROL Default 'Company Status Change to Pending Approval' Email]** in op de naam van de sjabloon. Standaard wordt de sjabloon `Company Status Pending Approval` gebruikt.

   ![&#x200B; configuratie van Klanten - de verandering van de bedrijfstatus &#x200B;](./assets/company-email-options-company-status-change.png){width="600"}

1. Voltooi de sectie **[!UICONTROL Company Credit Emails]** :

   - Plaats **[!UICONTROL Company Credit Change Email Sender]** aan het [&#x200B; opslagcontact &#x200B;](../getting-started/store-details.md#store-email-addresses) dat moet worden op de hoogte gebracht wanneer een verandering aan de kredietgrens wordt aangebracht die aan een bedrijf wordt toegewezen. Door gebrek, wordt het bericht verzonden naar _Vertegenwoordiger van de Verkoop_.

   - Voer bij **[!UICONTROL Send Company Credit Change Email Copy To]** het e-mailadres in van elke persoon die een kopie van de kennisgeving van de wijziging van het creditcard moet ontvangen. Scheid meerdere e-mailadressen met een komma.

   - Om te bepalen hoe het exemplaar van het bericht wordt verzonden, plaats **verzendt de Methode van het E-mailExemplaar** aan één van het volgende:

      - `Bcc` - verzendt a _blinde beleefdheidsexemplaar_ door de ontvanger in de kopbal van zelfde e-mail te omvatten die naar de klant wordt verzonden. De ontvanger BCC is niet zichtbaar aan de klant.
      - `Separate Email` - Hiermee verzendt u de kopie als een aparte e-mail.

   - Als u e-mailsjablonen hebt voorbereid voor gebruik in plaats van de standaardinstellingen, kiest u de sjabloon voor elk van de volgende meldingen die naar de bedrijfsbeheerder worden verzonden.

      - **[!UICONTROL Allocated Email Template]**
      - **[!UICONTROL Updated Email Template]**
      - **[!UICONTROL Reimbursed Email Template]**
      - **[!UICONTROL Refunded Email Template]**
      - **[!UICONTROL Reverted Email Template]**

   ![&#x200B; configuratie van Klanten - bedrijfkrediet e-mails &#x200B;](./assets/company-email-options-company-credit.png){width="600"}

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

## Goedkeuring van bestellingen configureren

Door de mogelijkheid om bestellingen te verwerken en aan te schaffen, kunnen bedrijfsbeheerders de handelingen van de kopers van het bedrijf controleren. De functie voor het goedkeuren van bestellingen is beschikbaar wanneer de functie voor het bestellen van inkooporders is ingeschakeld door een beheerder van de winkel.

1. Op _Admin_ sidebar, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL General]** uit en kies **[!UICONTROL B2B Features]** .

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) uit de **[!UICONTROL Order Approval Configuration]** sectie.

   ![&#x200B; de Configuratie van de Goedkeuring van de Orde &#x200B;](./assets/b2b-features-order-approval.png){width="600"}

1. Stel **[!UICONTROL Enable Purchase Orders]** in op `Yes` als u bedrijven wilt toestaan eigen inkooporders te maken.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

   De functie voor inkooporders is ingeschakeld op websiteniveau. Om dit type van orde voor een bedrijf toe te laten, doe het zelfde met de aangewezen montages in elk [&#x200B; bedrijfsprofiel &#x200B;](account-company-manage.md).

## Aankooporders configureren

1. Voor _Admin_ sidebar, ga **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Zoek het bedrijf in de lijst en klik op **[!UICONTROL Edit]** .

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Advanced Settings]** sectie uit.

1. Stel **[!UICONTROL Enable Purchase Orders]** in op `Yes` .

1. Klik op **[!UICONTROL Save]** als u klaar bent.

Na activering, wordt de **[!UICONTROL Approval Rules]** sectie getoond op het storefront [&#x200B; Dashboard van de Rekening &#x200B;](../customers/account-dashboard.md) voor een bedrijfbeheerder.

>[!NOTE]
>
>De toegang van de orde van de aankoop op de storefront moet door de bedrijfbeheerder worden verleend die op [&#x200B; de toestemmingen van de bedrijfs gebruikersrol &#x200B;](account-company-roles-permissions.md) wordt gebaseerd.

## Betaling op account configureren

Betaling op account is een methode voor offline betaling waarmee bedrijven aankopen kunnen doen tot de kredietlimiet die in hun profiel is vastgelegd. Betaling op account kan globaal of per bedrijf worden ingeschakeld en wordt alleen tijdens het uitchecken weergegeven als deze optie is ingeschakeld. Wanneer _Betaling op Rekening_ als betalingsmethode wordt gebruikt, verschijnt een bericht bij de bovenkant van de orde die op de status van de rekening wijst. Om deze betalingsmethode voor een specifiek bedrijf te vormen, zie [&#x200B; BedrijfsRekeningen beheren &#x200B;](account-company-manage.md).

>[!NOTE]
>
>Betaling op rekening wordt niet gesteund voor orden met [&#x200B; veelvoudige verzendadressen &#x200B;](../stores-purchase/shipping-settings.md#multiple-addresses) en verschijnt niet onder de betalingsopties voor deze orden.

Als u Betaling op account voor uw winkel wilt inschakelen:

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Payment Methods]** .

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Payment on Account]** sectie uit.

   ![&#x200B; Betaling op Rekening &#x200B;](./assets/payment-methods-payment-on-account.png){width="600"}

   >[!NOTE]
   >
   >Schakel indien nodig eerst het selectievakje **[!UICONTROL Use system value]** uit om deze instellingen te wijzigen.

1. Stel **[!UICONTROL Enabled]** in op `Yes` als u betaling op rekening wilt toestaan.

1. Voer een **[!UICONTROL Title]** in die de betalingsmethode tijdens het uitchecken aangeeft, of u kunt de standaardtitel van `Payment on Account` accepteren.

1. Als orders doorgaans wachten op goedkeuring, accepteert u de standaardwaarde **[!UICONTROL New Order Status]** als `Pending` totdat deze wordt goedgekeurd.

   U kunt desgewenst de status `Processing` of `Suspected Fraud` gebruiken voor nieuwe bestellingen met deze betalingsmethode.

1. Stel **[!UICONTROL Payment from Applicable Countries]** in op een van de volgende opties:

   - `All Allowed Countries` - de klanten van alle [&#x200B; landen &#x200B;](../getting-started/store-details.md#country-options) die in uw opslagconfiguratie worden gespecificeerd kunnen deze betalingsmethode gebruiken.
   - `Specific Countries` - Nadat u deze optie hebt gekozen, wordt de lijst _[!UICONTROL Payment from Specific Countries]_&#x200B;weergegeven. Als u meerdere landen wilt selecteren, houdt u Ctrl (PC) of Command (Mac) ingedrukt en klikt u op elke optie.

1. Stel **[!UICONTROL Minimum Order Total]** en **[!UICONTROL Maximum Order Total]** in op de orderbedragen die nodig zijn om in aanmerking te komen voor deze betalingsmethode.

   >[!NOTE]
   >
   >Een orde komt in aanmerking als het totaal tussen, of precies aanpast, de minimum of maximumtotale waarden valt.

1. Voer een **[!UICONTROL Sort Order]** getal in dat de positie van dit item instelt in de lijst met betalingsmethoden die tijdens het afrekenen wordt weergegeven.

   De waarde is relatief ten opzichte van de andere betalingsmethoden. (`0` = first, `1` = second, `2` = third, enzovoort.)

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.
