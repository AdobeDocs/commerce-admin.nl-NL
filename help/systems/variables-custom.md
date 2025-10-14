---
title: Aangepaste variabelen toevoegen
description: Leer hoe u aangepaste variabelen kunt maken en deze kunt invoegen op pagina's, blokken en productinhoud.
exl-id: 8233518a-abcf-4889-b75b-4aa503c7cebb
role: Admin, User
feature: System, Variables, Page Content, Communications
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 1%

---

# Aangepaste variabelen toevoegen

Om aan de specifieke behoeften van uw zaken te voldoen, kunt u douanevariabelen tot stand brengen en hen opnemen in [&#x200B; pagina&#39;s &#x200B;](../content-design/pages.md), [&#x200B; blokken &#x200B;](../content-design/blocks.md), en [&#x200B; e-mailmalplaatjes &#x200B;](email-templates.md). De lijst van toegestane variabelen die verschijnt wanneer u de _Variabele van het Tussenvoegsel_ knoop omvat zowel [&#x200B; vooraf bepaalde &#x200B;](variables-predefined.md) als douanevariabelen. De lijst met beschikbare variabelen voor een specifieke e-mailsjabloon wordt bepaald door de gegevens die aan de sjabloon zijn gekoppeld. Zie de [&#x200B; Veranderlijke Verwijzing &#x200B;](variables-reference.md) voor een lijst van vaak gebruikte e-mailmalplaatjes en hun bijbehorende variabelen.

![&#x200B; de variabelen van de Douane &#x200B;](./assets/variables-custom.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Alleen toegestane vooraf gedefinieerde of aangepaste variabelen kunnen worden gebruikt in sjablonen voor e-mail en nieuwsbrief.

## Stap 1: Een aangepaste variabele maken

1. Voor _Admin_ sidebar, ga **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Custom Variables]**.

1. Klik op **[!UICONTROL Add New Variable]**.

1. Voer een id in voor **[!UICONTROL Variable Code]** , waarbij u alle kleine letters zonder spaties gebruikt.

   Indien nodig kunt u een spatie aangeven met een onderstrepingsteken of afbreekstreepje. Bijvoorbeeld: `my_custom_variable`

1. Voer een **[!UICONTROL Variable Name]** in die wordt gebruikt voor interne referentie. Bijvoorbeeld: `My Custom Variable`

1. Voer een van de volgende handelingen uit om de waarde in te voeren die aan de variabele is gekoppeld:

   - Voer bij **[!UICONTROL Variable HTML Value]** de variabelewaarde in die is opgemaakt met eenvoudige HTML-tags. Bijvoorbeeld:

     `<b>This formatted content appears in place of the variable.</b>`

   - Voer bij **[!UICONTROL Variable Plain Value]** de waarde van de variabele in als onbewerkte tekst zonder opmaak. Bijvoorbeeld:

     `This unformatted content appears in place of the variable.`

   >[!TIP]
   >
   >Als u meer ruimte nodig hebt, sleept u de rechterbenedenhoek van het tekstvak.

   ![&#x200B; Nieuwe douanevariabele &#x200B;](./assets/variable-custom-add.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.

## Stap 2: Voeg de aangepaste variabele in uw inhoud in

Gebruik [!DNL Page Builder] om een aangepaste variabele in te voegen.

1. Open de pagina, het blok, de categorie of het product waar u de variabele aan de inhoud wilt toevoegen.

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Content]** sectie uit.

1. Klik op **[!UICONTROL Edit with Page Builder]**.

1. Klik in het linkerdeelvenster op **[!UICONTROL Elements]** en voer een van de volgende handelingen uit:

   - Klik in een bestaand tekstgebied waar u de variabele wilt invoegen.

   - Sleep een nieuw **[!UICONTROL Text]** -object naar het werkgebied.

1. Helemaal rechts van de redacteurstoolbar, klik ( ![&#x200B; Variabele van het Tussenvoegsel &#x200B;](./assets/editor-btn-insert-variable.png)) om een variabele op te nemen.

   ![[!DNL Page Builder] werkgebied en deelvenster &#x200B;](./assets/variable-custom-pagebuilder-stage.png){width="600" zoomable="yes"}

1. Selecteer in de lijst de aangepaste variabele die u wilt invoegen en klik op **[!UICONTROL Insert Variable]** .

   ![&#x200B; Nieuwe douanevariabele &#x200B;](./assets/variable-custom-insert-select.png){width="600" zoomable="yes"}

   De variabele-id wordt als tijdelijke aanduiding weergegeven in de editor.

   ![[!DNL Page Builder] stage - variable placeholder &#x200B;](./assets/pagebuilder-variable-inserted.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save]** als de bewerking is voltooid.
