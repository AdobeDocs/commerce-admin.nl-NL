---
title: Nieuwe opties voor klantenaccount
description: Leer over de configuratieopties voor nieuwe klantenrekeningen in uw opslag.
exl-id: aa19f0e2-ffbe-433d-8bd5-c14700b67b37
feature: Customers, Configuration
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---

# Nieuwe opties voor klantenaccount

In de _[!UICONTROL Create New Account Options]_in de configuratie worden de basisaccountopties gecombineerd met meer geavanceerde opties die betrekking hebben op de validatie van BTW-id&#39;s en aangepaste integratie. De volgende instructies hebben alleen betrekking op de meest gebruikte opties. Om over automatische klantengroepstaken te leren, zie [Btw-validatie](../stores-purchase/vat.md).

![Nieuwe accountopties maken](assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

## De basisopties voor klantenaccounts instellen

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Customers]** en kiest u **[!UICONTROL Customer Configuration]**.

1. Breid uit **[!UICONTROL Create New Account Options]** sectie:

   ![Standaardinstellingen voor Nieuwe accountopties maken](../configuration-reference/customers/assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

1. Stel elk van de opties in op basis van de ervaring van de klant die u op uw winkel moet ondersteunen:

   - Set **[!UICONTROL Default Group]** aan de klantengroep die aan nieuwe klanten wordt toegewezen wanneer een rekening wordt gecreeerd.

   - Als u een _BTW_ nummer en wil dat het zichtbaar is voor klanten, stel **[!UICONTROL Show VAT Number on Storefront]** tot `Yes`.

   - Als u een klant tijdens het aanmaken van een Admin-order een e-mail wilt sturen, stelt u **[!UICONTROL Email is required field for Admin order creation]** tot `Yes`.

   - Voer de **[!UICONTROL Default Email Domain]** voor de winkel, zoals `mystore.com`

   - Set **[!UICONTROL Default Welcome Email]** naar de sjabloon die wordt gebruikt voor het welkomstbericht dat naar nieuwe klanten wordt verzonden.

   - Als u wilt dat klanten hun verzoek om een account te openen bij uw winkel bevestigen, stelt u **[!UICONTROL Require Emails Confirmation]** tot `Yes`. Vervolgens stelt u **[!UICONTROL Confirmation Link Email]** naar de sjabloon die wordt gebruikt voor de bevestigingsmail.

     >[!NOTE]
     >
     >Vanaf versie 2.4.7 moeten klanten hun e-mail en wachtwoord opnieuw invoeren om zich aan te melden bij hun account na e-mailbevestiging, ongeacht de browser.

   - Set **[!UICONTROL Welcome Email]** naar de sjabloon die wordt gebruikt voor het welkomstbericht dat wordt verzonden nadat de account is bevestigd.

   - Set **[!UICONTROL Default Welcome Email without Password]** aan het malplaatje dat wordt gebruikt wanneer een klantenrekening wordt gecreeerd die nog geen wachtwoord heeft. Er is bijvoorbeeld nog geen wachtwoord toegewezen aan een klantenaccount die is gemaakt met de beheerder.

   - Set **[!UICONTROL Email Sender]** naar de contactpersoon van de winkel die wordt weergegeven als de afzender van het welkomstbericht.

   - Als u wilt dat klanten hun verzoek om een account te openen bij uw winkel bevestigen, stelt u **[!UICONTROL Require Emails Confirmation]** tot `Yes`. Vervolgens stelt u **[!UICONTROL Confirmation Link Email]** naar de sjabloon die wordt gebruikt voor de bevestigingsmail.

   ![Nieuwe accountopties maken met BTW ingeschakeld](../configuration-reference/customers/assets/customer-configuration-create-new-account-options-vat.png){width="600" zoomable="yes"}

   Voor gedetailleerde informatie over elk van de opties beschikbaar in deze reeks van configuratieoptie, zie _Nieuwe accountopties maken_ [configuratieverwijzing](../configuration-reference/customers/customer-configuration.md).

1. Klik op **[!UICONTROL Save Config]**.
