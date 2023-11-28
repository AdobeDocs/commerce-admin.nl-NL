---
title: Wachtwoorden van klanten opnieuw instellen
description: Klanten stellen hun wachtwoorden gewoonlijk opnieuw in bij de winkel, maar een beheerder van de winkel kan een wachtwoordinstelling of een geforceerde aanmelding bij de beheerder starten.
exl-id: bca1ef3e-2bc6-4146-ac86-d6c58c8995e4
feature: Customers, Configuration, Security
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---

# Wachtwoorden van klanten opnieuw instellen

Klanten kunnen hun wachtwoorden doorgaans opnieuw instellen in de winkel door op _[!UICONTROL Forgot Your Password?]_. De beheerder van de winkel kan echter een opnieuw instellen van het wachtwoord of een geforceerde aanmelding starten vanuit de beheerder.

| -functie | Beschrijving |
| --- | --- |
| Wachtwoord opnieuw instellen | Er wordt een e-mailbericht met wachtwoordinstellingen rechtstreeks verzonden naar de e-mailaccount van de klant. De opslagbeheerder kan geen toegang tot het wachtwoord van de klant krijgen. |
| Aanmelden forceren | Hiermee worden de OAuth-toegangstokens ingetrokken die aan de klantenaccount zijn gekoppeld. Dit kan slechts met klantenrekeningen worden gebruikt die tekenen OAuth, als deel van een Web API zijn toegewezen [integratie](../systems/integrations.md). Zie voor meer informatie [Verificatie op basis van OAuth](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) in de ontwikkelaarsdocumentatie. <br/><br/>De standaardklantenrekeningen die van storefront of van Admin worden gecreeerd hebben geen Tokens OAuth. |

{style="table-layout:auto"}

## Een wachtwoord opnieuw instellen vanuit de winkel

1. Op de aanmeldingspagina klikt de klant **[!UICONTROL Forgot Your Password?]**.

1. Wanneer ertoe aangezet, gaat binnen **[!UICONTROL Email Address]** die aan hun rekening wordt geassocieerd en klikt **[!UICONTROL Reset My Password]**.

   ![Wachtwoord vergeten](assets/forgot-password.png){width="600" zoomable="yes"}

   >[!INFO]
   >
   >Als het ingevoerde e-mailadres overeenkomt met het e-mailadres dat aan de account is gekoppeld, ontvangt de klant een bevestigingsbericht met een koppeling voor het opnieuw instellen van het wachtwoord.

1. Wanneer het e-mailbericht arriveert, klikt de klant op de knop _wachtwoord opnieuw instellen_ koppelen en hun **[!UICONTROL New Password]** wanneer hierom wordt gevraagd.

1. Hiermee wordt het opnieuw ingevoerd ter bevestiging en klik op **[!UICONTROL Reset Password]**.

   >[!IMPORTANT]
   >
   >Het nieuwe wachtwoord moet uit minimaal zes tekens bestaan, zonder spaties. Als ze bevestiging ontvangen dat het wachtwoord is bijgewerkt, kunnen ze zich met het nieuwe wachtwoord aanmelden bij hun account. Standaard worden de _wachtwoord opnieuw instellen_ de koppeling is 24 uur geldig.

## Een wachtwoord opnieuw instellen via de beheerder

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Zoek de klantenaccount in het raster en klik op **[!UICONTROL Edit]** in de _Handeling_ kolom.

1. Klik in de reeks opties boven aan de pagina op **[!UICONTROL Reset Password]**.

   Het aantal verzoeken om het opnieuw instellen van het wachtwoord dat binnen een uur is toegestaan, wordt ingesteld in het dialoogvenster [configuratie](../configuration-reference/customers/customer-configuration.md) onderwerp.

## OAuth-tokens van een klant intrekken

>[!IMPORTANT]
>
>Ga alleen door als u een volledig begrip hebt van API-verificatie.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Zoek de klantenaccount in het raster en klik op **[!UICONTROL Edit]** in de _Handeling_ kolom.

1. Klik in de reeks opties boven aan de pagina op **[!UICONTROL Force Sign In]**.

1. Klik wanneer u wordt gevraagd om te bevestigen **OK**.
