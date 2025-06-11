---
title: Een widget invoegen in de editor
description: Voeg verschillende inhoudselementen aan een pagina toe gebruikend het widgethulpmiddel in de redacteur van WYSIWYG.
exl-id: bbc5e059-06d8-4dda-89a7-6c9826b73fd3
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%

---

# Een widget invoegen in de editor

Het [ widget ](widget-create.md) hulpmiddel kan worden gebruikt om diverse inhoudselementen aan de pagina toe te voegen, met inbegrip van verbindingen aan om het even welke de inhoudspagina of knoop van Commerce, product, of categorie. Koppelingen kunnen in blokindeling op de pagina worden geplaatst of rechtstreeks in de inhoud worden opgenomen. Met het gereedschap Widget kunt u koppelingen maken naar de volgende typen inhoud:

- [Inhoudspagina&#39;s](pages.md)
- [Cataloguscategorieën](../catalog/categories.md)
- [Catalogusproducten](../catalog/product-create.md)

Koppelingen nemen hun stijl standaard over van de stijlpagina van het thema.

{{$include /help/_includes/directives-caution.md}}

1. Open een pagina, blok of dynamisch blok in de bewerkingsmodus.

1. Ga naar de sectie _[!UICONTROL Content]_&#x200B;en klik op een element dat de editor ondersteunt.

1. Plaats de curseur waar u widget wilt verschijnen en het _pictogram van Widget van het Tussenvoegsel_ klikken.

   ![ toolbar van de Redacteur - Tussenvoegsel Widget ](./assets/editor-toolbar-widget-button.png){width="700" zoomable="yes"}

   Klik op **[!UICONTROL Show / Hide Editor]** als u Page Builder niet hebt ingeschakeld en liever met de code werkt. Plaats de invoegpositie op de plaats in de tekst waar u de widget wilt weergeven. Klik vervolgens op **[!UICONTROL Insert Widget]** .

1. Kies de **[!UICONTROL Widget Type]** .

   Voor meer informatie over deze opties, zie {de Types van Widget 0} [&#128279;](widgets.md#widget-types).  In de volgende stappen wordt een voorbeeld gebruikt voor het invoegen van een koppeling naar een product.

1. Laat het veld **[!UICONTROL Anchor Custom Text]** leeg als u de productnaam wilt gebruiken.

1. Voer een **[!UICONTROL Anchor Custom Title]** in voor de beste SEO-praktijk.

   Deze titel is niet zichtbaar op de pagina.

1. Stel **[!UICONTROL Template]** in op een van de volgende opties:

   - Selecteer `Product Link Inline Template` als u de koppeling in de tekst wilt opnemen.

   - Selecteer `Product Link Block Template` als u de koppeling op een aparte regel wilt plaatsen.

1. Klik op **[!UICONTROL Select Product]** en voer de volgende handelingen uit:

   - Navigeer in de boomstructuur naar de gewenste categorie.

   - Kies het gekoppelde product in de lijst.

1. Klik op **[!UICONTROL Insert Widget]** om de koppeling op de pagina te plaatsen.

   Als u met de code van HTML werkt, verschijnt a [ prijsverhogingsmarkering ](../systems/markup-tags.md) voor de verbinding bij de bovenkant van de pagina, die in dubbele krullende steunen wordt ingesloten. Indien nodig, gebruik _Besnoeiing en Deeg_ om de prijsverhogingsmarkering in de code te plaatsen waar u de verbinding wilt verschijnen.

1. Klik op **[!UICONTROL Save]** wanneer de bewerkingen van de inhoud zijn voltooid.
