---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Reward Points]'
description: Controleer de configuratie-instellingen op de pagina [!UICONTROL Customers] &gt; [!UICONTROL Reward Points] van Commerce Admin.
exl-id: 0b7f8806-74c5-4467-87da-0faae50f164b
feature: Configuration, Rewards
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '781'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Reward Points]

{{ee-feature}}

{{config}}

>[!NOTE]
>
>{de 1} configuratie van de Tarieven van de Uitwisseling van 0} wordt de Winst {vereist voor terugbetaling van beloningspunten door klanten en beheerders tijdens controle.[](../../merchandising-promotions/reward-exchange-rates.md)

## [!UICONTROL Reward Points]

![ de Punten van de Beloning ](./assets/reward-points-reward-points.png)<!-- zoom -->

<!-- [Reward Points](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/merchandising/reward-points/rewards-loyalty#enable-reward-point-operations-for-your-store) -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Reward Points Functionality] | Algemeen | Hiermee activeert of deactiveert u bonuspunten. Opties: `Yes` / `No` . |
| [!UICONTROL Enable Reward Points Functionality on Storefront] | Website | Wanneer toegelaten, kunnen de klanten punten door hun activiteiten verdienen, en hen terugbetalen bij kassa. Als deze optie is uitgeschakeld, kunnen alleen Admin-gebruikers punten toewijzen en inwisselen namens klanten. Opties: `Yes` / `No` . |
| [!UICONTROL Customers May See Reward Points History] | Website | Wanneer deze optie is ingeschakeld, kunnen klanten een gedetailleerde geschiedenis zien met elke opgebouwde versie, terugbetaling en vervaldatum van de Punten in het dashboard voor hun account. Opties: `Yes` / `No` |
| [!UICONTROL Reward Points Balance Redemption Threshold] | Website | Vereist dat klanten een minimale puntbalans bereiken voordat ze deze voor orders kunnen inwisselen. Laat minimaal leeg. |
| [!UICONTROL Cap Reward Points Balance At] | Website | Voorkomt dat klanten meer dan dit maximale puntensaldo ontvangen. Laat maximaal leeg. |
| [!UICONTROL Reward Points Expire in (days)] | Website | Geeft de levensduur van de bonuspunten in dagen aan. Elke partij punten die tijdens afzonderlijke activiteiten wordt verdiend, heeft een aparte levensduur. Elke batch in de geschiedenis van de Punten achteruit geeft het aantal dagen aan dat resteert voordat de punten verlopen. De geschiedenis kan worden bekeken vanaf het accountdashboard van de klant, indien ingeschakeld, en vanaf de beheerder. Laat de spatie leeg voor geen vervaldatum. |
| [!UICONTROL Reward Points Expiry Calculation] | Website | Bepaalt de methode die wordt gebruikt om te bepalen wanneer de bonuspunten verlopen. Opties: <br/>**`Static`**- bepaalt de resterende levensduur van bonuspunten op basis van het aantal dagen dat is ingesteld in de configuratie. Als de vervallimiet in de configuratie verandert, verandert de vervaldatum van bestaande punten niet.<br/>**`Dynamic`** - Berekent het aantal dagen dat resteert wanneer de evenwicht van het beloningspunt stijgt. Als de vervallimiet in de configuratie verandert, worden de verloopberekeningen voor alle bestaande punten dienovereenkomstig bijgewerkt. |
| [!UICONTROL Refund Reward Points Automatically] | Algemeen | Hiermee wordt bepaald of beschikbare bonuspunten automatisch worden terugbetaald. Opties: `Yes` / `No` |
| [!UICONTROL Deduct Reward Points from Refund Amount Automatically] | Algemeen | Hiermee bepaalt u of de beloningspunten die via aankopen worden verdiend, geheel of gedeeltelijk worden ingetrokken bij de terugbetaling van bestellingen, wanneer deze functie is ingeschakeld. Alleen bonuspunten uit de bestelling die ze heeft verdiend, worden beïnvloed wanneer die bestelling wordt terugbetaald. Opties: `Yes` / `No` . |
| [!UICONTROL Landing Page] | Winkelweergave | Hier geeft u de CMS-pagina op die uw bonuspuntprogramma uitlegt. Er verschijnt een koppeling naar de pagina met standaardbeloningen op de locaties in de winkel waar punten kunnen worden verdiend. |

{style="table-layout:auto"}

## [!UICONTROL Actions for Acquiring Reward Points by Customers]

![ Acties voor het Ophalen van de Punten van de Beloning door Klanten ](./assets/reward-points-actions-for-acquiring.png)<!-- zoom -->

<!-- [Actions for Acquiring Reward Points by Customers](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/merchandising/reward-points/rewards-loyalty#enable-reward-point-operations-for-your-store) -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Purchase] | Website | Bepaalt als de beloningspunten voor de aankopen worden verdiend die op de gevormde [ Winst Tarieven van de Uitwisseling ](../../merchandising-promotions/reward-exchange-rates.md) worden gebaseerd. Opties: `Yes` / `No` |
| [!UICONTROL Registration] | Website | Hiermee geeft u het aantal punten op dat wordt verdiend voor het openen van een klantenaccount. |
| [!UICONTROL Newsletter Signup] | Website | Geeft het aantal punten op dat wordt verdiend door geregistreerde klanten die zich abonneren op een nieuwsbrief. (Punten zijn niet beschikbaar voor abonnementen door gasten.) Als een klant zich afmeldt en zich vervolgens opnieuw abonneert, worden punten niet verdiend voor het tweede abonnement. |
| [!UICONTROL Converting Invitation to Customer] | Website | Specificeert het aantal punten die door een klant worden verdiend die een uitnodiging verzendt, wanneer de ontvanger dan een klantenrekening opent. |
| [!UICONTROL Invitation to Customer Conversions Quantity Limit] | Website | Beperkt het aantal uitnodigingsomzettingen die kunnen worden gebruikt om punten voor de klant te verdienen die de uitnodiging verzendt. Laat het veld leeg voor geen limiet. |
| [!UICONTROL Converting Invitation to Order] | Website | Specificeert het aantal punten die door een klant worden verdiend die een uitnodiging verzendt wanneer de ontvanger een aanvankelijke orde plaatst. |
| [!UICONTROL Invitation to Order Conversions Quantity Limit] | Website | Beperkt het aantal ordeconversies die punten voor de persoon kunnen verdienen die de uitnodiging verzendt. Indien leeg, is er geen maximumgrens. |
| [!UICONTROL Invitation Conversion to Order Reward] | Website | Geeft aan hoe vaak een klant beloningspunten kan verdienen wanneer een genodigde een aankoop doet. Opties: <br/>**`Each`**- De klant ontvangt bonuspunten voor elke gefactureerde opdracht die door de genodigde wordt geplaatst. Retourpunten worden gegeven volgens de wisselkoersen die zijn vastgesteld voor de vereiste combinatie van een website en een klantengroep.<br/>**`First`** - De klant ontvangt alleen bonuspunten voor de eerste gefactureerde order die door de genodigden wordt geplaatst. Als meer dan één genodigde zich registreert en een orde plaatst, slechts wordt het bedrag van de eerste orde omgezet in beloningspunten en aan de klant verleend. |
| [!UICONTROL Review Submission] | Website | Bepaalt het aantal punten die door een klant worden verdiend die een overzicht voorlegt dat voor publicatie wordt goedgekeurd. |
| [!UICONTROL Rewarded Reviews Submission Quantity Limit] | Website | Hiermee beperkt u het aantal revisies dat kan worden gebruikt om punten per klant te verdienen. Laat het veld leeg voor geen limiet. |

{style="table-layout:auto"}

## [!UICONTROL Email Notification Settings]

![ de Montages van het Bericht E-mail ](./assets/reward-points-email-notification-settings.png)<!-- zoom -->

<!-- [Email Notification Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/merchandising/reward-points/rewards-loyalty#enable-reward-point-operations-for-your-store) -->

| Veld | [ Reikwijdte ](../../getting-started/websites-stores-views.md#scope-settings) | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Email Sender] | Winkelweergave | Hiermee bepaalt u de contactpersoon van de winkel die wordt weergegeven als de afzender van de e-mails met de bijgewerkte balans en de vervaldatum. |
| [!UICONTROL Subscribe Customers by Default] | Algemeen | Hiermee bepaalt u de standaardabonnementsstatus van klanten voor zowel de e-mails voor het bijwerken van de balans als voor de vervaldatumberichten. |
| [!UICONTROL Balance Update Email] | Winkelweergave | Bepaalt het malplaatje voor het bericht wordt gebruikt dat naar klanten wordt verzonden wanneer hun puntsaldo wordt bijgewerkt. Standaardsjabloon: `Reward Points Balance Update` |
| [!UICONTROL Reward Points Expiry Warning Email] | Winkelweergave | Bepaalt het malplaatje van e-mail dat klanten ontvangen wanneer de grens van de vervalwaarschuwing voor een partij punten is bereikt. Standaardsjabloon: `Reward Points Expiry Warning` |
| [!UICONTROL Expiry Warning before (days)] | Algemeen | Hier geeft u het aantal dagen vóór het verlopen van het punt op waarop het bericht moet worden verzonden. Laat leeg om geen vervalmeldingen te verzenden. Er wordt geen melding verzonden als het aantal ingevoerde dagen groter is dan de resterende levensduur van de punten. |

{style="table-layout:auto"}
