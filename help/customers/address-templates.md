---
title: Adressjablonen van de klant
description: Leer hoe u de malplaatjes van het klantenadres kunt aanpassen.
exl-id: 9fd32c0a-ff9a-47f9-84e2-f5d6bf307d8c
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# Adressjablonen van de klant

{{ee-feature}}

U kunt de sjabloon wijzigen die de indeling bepaalt van de facturerings- en verzendadressen van klanten die worden weergegeven op gedrukte facturen, verzendingen en terugbetalingen, en in het adresboek van de klantenaccount. Als u extra informatie wilt omvatten, kunt u [&#x200B; douaneattributen &#x200B;](attribute-properties.md) tot stand brengen die met de klantenrekening en [&#x200B; adres &#x200B;](address-attributes.md) worden geassocieerd, en hen opnemen in het malplaatje.

## Voorbeeld 1: korte notatie

Voor [!UICONTROL Text One Line] adressjabloon:

```text
{{depend prefix}}{{var prefix}} {{/depend}}{{var firstname}} {{depend middlename}}{{var middlename}} {{/depend}}{{var lastname}}{{depend suffix}} {{var suffix}}{{/depend}}, {{var street}}, {{var city}}, {{var region}} {{var postcode}}, {{var country}}
```

## Voorbeeld 2: lange notatie

Voor de adressjablonen [!UICONTROL Text] , [!UICONTROL HTML] en [!UICONTROL PDF] :

```text
{{depend prefix}}{{var prefix}} {{/depend}}{{var firstname}} {{depend middlename}}{{var middlename}} {{/depend}}{{var lastname}}{{depend suffix}} {{var suffix}}{{/depend}}{{depend company}}{{var company}}{{/depend}}{{if street1}}{{var street1}}{{/if}}{{depend street2}}{{var street2}}{{/depend}}{{depend street3}}{{var street3}}{{/depend}}{{depend street4}}{{var street4}}{{/depend}}{{if city}}{{var city}},  {{/if}}{{if region}}{{var region}}, {{/if}}{{if postcode}}{{var postcode}}{{/if}}{{var country}}{{depend telephone}}T: {{var telephone}}{{/depend}}{{depend fax}}F: {{var fax}}{{/depend}}{{depend vat_id}}VAT: {{var vat_id}}{{/depend}}
```

![&#x200B; het adresmalplaatjes van de Klant &#x200B;](../configuration-reference/customers/assets/customer-configuration-address-templates.png){width="600" zoomable="yes"}

## De volgorde van adresvelden wijzigen

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Customers]** uit en selecteer **[!UICONTROL Customer Configuration]** .

1. Klik om de sectie **[!UICONTROL Address Templates]** uit te vouwen.

   De sectie bevat een aparte set opmaakinstructies voor elk van de volgende onderdelen:

   - [!UICONTROL Text]
   - [!UICONTROL Text One Line]
   - [!UICONTROL HTML]
   - [!UICONTROL PDF]

1. Bewerk indien nodig elke sjabloon met behulp van de voorbeelden ter referentie.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.
