---
title: Wachtwoorden van klanten opnieuw instellen
description: Klanten stellen hun wachtwoorden gewoonlijk opnieuw in bij de winkel, maar een beheerder van de winkel kan een wachtwoordinstelling of een geforceerde aanmelding bij de beheerder starten.
exl-id: bca1ef3e-2bc6-4146-ac86-d6c58c8995e4
feature: Customers, Configuration, Security
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Wachtwoorden van klanten opnieuw instellen

Klanten kunnen hun wachtwoorden meestal opnieuw instellen vanuit de winkel door op _[!UICONTROL Forgot Your Password?]_&#x200B;te klikken. De beheerder van de winkel kan echter een opnieuw instellen van het wachtwoord of een geforceerde aanmelding starten vanuit de beheerder.

| Functie | Beschrijving |
| --- | --- |
| Wachtwoord opnieuw instellen | Er wordt een e-mailbericht met wachtwoordinstellingen rechtstreeks verzonden naar de e-mailaccount van de klant. De opslagbeheerder kan geen toegang tot het wachtwoord van de klant krijgen. |
| Aanmelden forceren | Hiermee worden de OAuth-toegangstokens ingetrokken die aan de klantenaccount zijn gekoppeld. Dit kan slechts met klantenrekeningen worden gebruikt die tekenen OAuth, als deel van een Web API [&#x200B; integratie &#x200B;](../systems/integrations.md) zijn toegewezen. Meer leren, zie [&#x200B; Op OAuth-Gebaseerde authentificatie &#x200B;](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) in de ontwikkelaarsdocumentatie. <br/><br/> Standaard klantenrekeningen die van storefront of van Admin worden gecreeerd hebben geen Tokens OAuth. |

{style="table-layout:auto"}

## Een wachtwoord opnieuw instellen vanuit de winkel

1. Op de aanmeldingspagina klikt de klant op **[!UICONTROL Forgot Your Password?]** .

1. Wanneer hierom wordt gevraagd, voert u de **[!UICONTROL Email Address]** in die aan het account is gekoppeld en klikt u op **[!UICONTROL Reset My Password]** .

   ![&#x200B; vergeten Uw Wachtwoord &#x200B;](assets/forgot-password.png){width="600" zoomable="yes"}

   >[!INFO]
   >
   >Als het ingevoerde e-mailadres overeenkomt met het e-mailadres dat aan de account is gekoppeld, ontvangt de klant een bevestigingsbericht met een koppeling voor het opnieuw instellen van het wachtwoord.

1. Wanneer e-mail aankomt, klikt de klant de _terugstellings wachtwoord_ verbinding en gaat hun **[!UICONTROL New Password]** in wanneer ertoe aangezet.

1. Voer het nogmaals in om het te bevestigen en te klikken **[!UICONTROL Reset Password]**.

   >[!IMPORTANT]
   >
   >Het nieuwe wachtwoord moet uit minimaal zes tekens bestaan, zonder spaties. Als ze bevestiging ontvangen dat het wachtwoord is bijgewerkt, kunnen ze zich met het nieuwe wachtwoord aanmelden bij hun account. Door gebrek, is de _terugstellings wachtwoord_ verbinding geldig voor 24 uren.

## Een wachtwoord opnieuw instellen via de beheerder

1. Voor _Admin_ sidebar, ga **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Vind de klantenrekening in het net en klik **[!UICONTROL Edit]** in de _kolom van de Actie_.

1. Klik op **[!UICONTROL Reset Password]** in de reeks opties boven aan de pagina.

   Het aantal verzoeken van het wachtwoordterugstellen die binnen een uur worden toegestaan wordt geplaatst in het [&#x200B; configuratie](../configuration-reference/customers/customer-configuration.md) onderwerp.

## OAuth-tokens van een klant intrekken

>[!IMPORTANT]
>
>Ga alleen door als u een volledig begrip hebt van API-verificatie.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Vind de klantenrekening in het net en klik **[!UICONTROL Edit]** in de _kolom van de Actie_.

1. Klik op **[!UICONTROL Force Sign In]** in de reeks opties boven aan de pagina.

1. Wanneer ertoe aangezet om te bevestigen, klik **OK**.
