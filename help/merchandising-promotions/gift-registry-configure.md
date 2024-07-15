---
title: Cadeauregisters configureren
description: Leer hoe u cadeauregisters inschakelt en de bijbehorende e-mailmeldingen configureert.
exl-id: 48193621-731d-4640-8ea8-5b201915cdf1
feature: Gift, Storefront, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---

# Cadeauregisters configureren

{{ee-feature}}

Voordat u cadeauregisters aan uw klanten kunt aanbieden, moet u cadeauregisters inschakelen en de bijbehorende e-mailmeldingen configureren. Adobe Commerce verzendt de volgende e-mailmeldingen als reactie op gebeurtenissen in de workflow voor het register van cadeaus.

- Wanneer een nieuw cadeauregister wordt gemaakt, wordt een e-mail naar de eigenaar verzonden met een koppeling naar het register die kan worden gedeeld.
- Optioneel kan de winkel een melding met een koppeling naar het cadeauregister verzenden aan vrienden en familie van de eigenaar van het cadeauregister.
- De eigenaar wordt op de hoogte gesteld wanneer items worden aangeschaft in het cadeauregister, maar geeft de koper niet aan.

Adobe Commerce heeft vooraf gedefinieerde sjablonen voor elk van deze e-mailberichten die voor uw merk kunnen worden aangepast.

## Stap 1. Cadeauregisters inschakelen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Customers]** uit en kies **[!UICONTROL Gift Registry]**

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL General Options]** sectie uit en doe het volgende:

   ![ de configuratie van Klanten - het register van het gift algemene ](../configuration-reference/customers/assets/gift-registry-general-options.png){width="600" zoomable="yes"}

   - De Register van het Cadeautje wordt toegelaten door gebrek. Indien nodig, stelt u **[!UICONTROL Enable Gift Registry]** in op `Yes` .

   - Voer voor **[!UICONTROL Maximum Registrants]** het maximumaantal personen in dat kan worden uitgenodigd om deel te nemen aan een cadeauregistergebeurtenis.

## Stap 2. E-mailmeldingen configureren

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Owner Notification]** sectie uit en doe het volgende:

   ![ configuratie van Klanten - bericht van de bezitsregistratie van het cadeau ](../configuration-reference/customers/assets/gift-registry-owner-notification.png){width="600" zoomable="yes"}

   - Kies **[!UICONTROL Email Template]** die de eigenaars van cadeauregisters op de hoogte brengt wanneer hun registers worden gemaakt.

   - Kies het [ opslagcontact ](../getting-started/store-details.md#store-email-addresses) dat als **[!UICONTROL Email Sender]** van het bericht verschijnt.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Gift Registry Sharing]** sectie uit en doe het volgende:

   ![ de configuratie van Klanten - het delen van het giftenregister ](../configuration-reference/customers/assets/gift-registry-gift-registry-sharing.png){width="600" zoomable="yes"}

   - Kies **[!UICONTROL Email Template]** die de ontvangers van het cadeauregister op de hoogte brengt wanneer een register met hen wordt gedeeld.

   - Kies de opslaglocatie die wordt weergegeven als de **[!UICONTROL Email Sender]** van het bericht.

   - Voer bij **[!UICONTROL Maximum Sent Emails Threshold]** het maximumaantal e-mailberichten in dat tegelijkertijd kan worden verzonden.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Gift Registry Update]** sectie uit en doe het volgende:

   ![ configuratie van Klanten - de update van de giftenregister ](../configuration-reference/customers/assets/gift-registry-gift-registry-update.png){width="600" zoomable="yes"}

   - Kies **[!UICONTROL Email Template]** die de eigenaars van cadeauregisters op de hoogte brengt van wijzigingen in het register.

   - Kies de opslaglocatie die wordt weergegeven als de **[!UICONTROL Email Sender]** van het bericht.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

1. Werk de cache bij wanneer hierom wordt gevraagd.

   Nadat het geheime voorgeheugen wordt verfrist, verschijnt de Registratie van het Cadeautje in het menu van Opslag onder Andere Montages en wordt beschikbaar in klantenrekeningen.
