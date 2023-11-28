---
title: Inhoud toevoegen - Product Recommendations
description: Meer informatie over het Recommendations-inhoudssoort Product waarmee u een lijst met aanbevelingen kunt toevoegen aan de [!DNL Page Builder] in het werkgebied.
exl-id: ca90c10d-8d7a-42a2-bb13-2602aa9d6eef
feature: Page Builder, Page Content, Recommendations
source-git-commit: 13d00168e1253a7d2698b898caa30d9ca2ad3800
workflow-type: tm+mt
source-wordcount: '950'
ht-degree: 0%

---

# Inhoud toevoegen - Product Recommendations

Gebruik de _Product Recommendations_ inhoudstype om een bestaand, actief [aanbeveling-eenheid](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/admin/create.html) aan de [[!DNL Page Builder] stadium](workspace.md#stage) voor een CMS-pagina, -blok of -blok.

>[!NOTE]
>
>De [!DNL Page Builder] _Product Recommendations_ inhoudstype wordt ondersteund in Adobe Commerce 2.4.4 en hoger en is beschikbaar in het dialoogvenster [Product Recommendations-metapakketversie 3.0.x of hoger](https://marketplace.magento.com/magento-product-recommendations.html). Toevoegen [!DNL Page Builder] ondersteuning voor Product Recommendations; [zie de installatiegegevens](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure.html#pbsupport). **Dit inhoudstype is niet beschikbaar voor Magento Open Source.**

{{$include /help/_includes/page-builder-save-timeout.md}}

## De Recommendations-gereedschapset voor producten

| Gereedschap | Pictogram | Beschrijving |
| --- | --| --- |
| Verplaatsen | ![Pictogram Verplaatsen](./assets/pb-icon-move.png){width="25"} | Hiermee verplaatst u de container met productaanbevelingen en de inhoud ervan naar een andere positie in het werkgebied. |
| Instellingen | ![Instellingenpictogram](./assets/pb-icon-settings.png){width="25"} | Opent de Edit pagina van de Aanbeveling van het Product, waar u de aanbeveling eenheid kunt kiezen en de eigenschappen van de container veranderen. |
| Verbergen | ![Pictogram verbergen](./assets/pb-icon-hide.png){width="25"} | Hiermee verbergt u de huidige container met productaanbevelingen en de inhoud ervan. |
| Tonen | ![Pictogram tonen](./assets/pb-icon-show.png){width="25"} | Toont de verborgen container van de productaanbeveling en zijn inhoud. |
| Dupliceren | ![Pictogram Dupliceren](./assets/pb-icon-duplicate.png){width="25"} | Hiermee maakt u een gedupliceerde kopie van de container met productaanbevelingen en de inhoud ervan. |
| Verwijderen | ![Pictogram verwijderen](./assets/pb-icon-remove.png){width="25"} | Hiermee verwijdert u de container met productaanbevelingen en de inhoud ervan uit het werkgebied. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Een bestaande aanbevolen eenheid toevoegen

1. Controleer of u al [heeft een aanbevolen eenheid gecreëerd](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/admin/create.html) voor de [!DNL Page Builder] paginatype.

>[!NOTE]
>
>U kunt aanbevelingen maken voor de [!DNL Page Builder] paginatype alleen in de standaardwinkelweergave.

1. Open de pagina, het blok of het dynamische blok in de bewerkingsmodus.

1. Breid uit _[!UICONTROL Content]_sectie en klik op **[!UICONTROL Edit with Page Builder]**of in het voorvertoningsgebied van de inhoud om het dialoogvenster [!DNL Page Builder] werkruimte.

1. In de [!DNL Page Builder] paneel onder _[!UICONTROL Layout]_, sleept u **[!UICONTROL Row]**tijdelijke aanduiding naar het werkgebied.

1. In de [!DNL Page Builder] paneel onder _[!UICONTROL Add Content]_, sleept u **[!UICONTROL Product Recommendation]**tijdelijke aanduiding voor de rij.

   ![Het inhoudstype Productaanbeveling toevoegen](./assets/pb-add-prex-drag.png){width="600" zoomable="yes"}

1. Voer een van de volgende handelingen uit:

   - Klik op **[!UICONTROL Edit Product Recommendation]**.
   - Houd de muisaanwijzer boven de lege container om de gereedschapset weer te geven en klik op de knop _Instellingen_ (![Instellingenpictogram](./assets/pb-icon-settings.png){width="20"} ).

   ![Productaanbeveling bewerken](./assets/pb-prex-toolbox.png){width="600" zoomable="yes"}

1. In de _[!UICONTROL Selection]_sectie, klikken **[!UICONTROL Select]**.

1. Zoek in de lijst met actieve productaanbevelingen de rij met de aanbevolen eenheid die u wilt toevoegen en klik op **[!UICONTROL Select]** in de laatste kolom.

   ![Geselecteerde productaanbeveling](./assets/pb-prex-select.png){width="600" zoomable="yes"}

1. Klik in de rechterbovenhoek op **[!UICONTROL Add Selected]**.

   De naam van de geselecteerde productaanbeveling wordt weergegeven in het dialoogvenster _[!UICONTROL Selection]_van de_[!UICONTROL Edit Product Recommendation]_ pagina.

1. Breng desgewenst wijzigingen aan in de [Geavanceerde instellingen](#advanced-settings).

   ![Productaanbeveling bewerken](./assets/pb-prex-edit.png){width="600" zoomable="yes"}

1. Voer de volgende handelingen uit wanneer deze zijn voltooid:

   - Als u met een volledig gemaximaliseerd browservenster werkt, klikt u op de knop _Volledig scherm sluiten_ (![Pictogram Volledig scherm sluiten](./assets/pb-icon-reduce.png)) in de rechterbovenhoek van de werkruimte.

   - Klikken **[!UICONTROL Save]** om de instellingen toe te passen en terug te keren naar de [!DNL Page Builder] werkruimte.

   Wanneer u terugkeert naar het werkgebied, worden voorlopige afbeeldingen van het product weergegeven in de container.

## Aanbevolen eenheidsinstellingen bewerken

1. Houd de muisaanwijzer boven de container van de aanbevolen eenheid om de gereedschapset weer te geven en klik op de knop _Instellingen_ (![Instellingenpictogram](./assets/pb-icon-settings.png){width="20"} ).

   ![Gereedschap Aanbeveling](./assets/pb-placeholder-toolbox.png){width="600" zoomable="yes"}

1. Breng desgewenst wijzigingen aan in de [Geavanceerde instellingen](#advanced-settings).

1. Klik op **[!UICONTROL Save]** om de instellingen toe te passen en terug te keren naar de [!DNL Page Builder] werkruimte.

## Een aanbevolen eenheid dupliceren

1. Houd de muisaanwijzer boven de container van de aanbevolen eenheid om de gereedschapset weer te geven en klik op de knop _Dupliceren_ ( ![Dubbele koppeling](./assets/pb-icon-duplicate.png){width="20"} ) in de gereedschapset.

   Het duplicaat wordt net onder het origineel weergegeven.

1. Als u de gedupliceerde aanbevolen eenheid naar een nieuwe positie wilt verplaatsen, houdt u de muisaanwijzer boven de container en klikt u op de knop _Verplaatsen_ ( ![Pictogram Verplaatsen](./assets/pb-icon-move.png){width="20"} ) in de gereedschapset.

1. Selecteer en sleep de aanbevolen eenheid totdat de rode hulplijn op de nieuwe positie wordt weergegeven.

   De boven- en onderrand van elke container worden weergegeven als onderbroken lijnen terwijl de aanbevolen eenheid wordt verplaatst.

## Een aanbevolen eenheid uit het werkgebied verwijderen

1. Houd de muisaanwijzer boven de container van de aanbevolen eenheid en klik op de knop _Verwijderen_ ( ![Pictogram verwijderen](./assets/pb-icon-remove.png){width="20"} ) in de gereedschapset.

1. Klik wanneer u wordt gevraagd om te bevestigen **[!UICONTROL OK]**.

## Geavanceerde instellingen

1. Als u de plaatsing van de Product Recommendations-eenheid in de bovenliggende container wilt bepalen, kiest u de optie **[!UICONTROL Alignment]**:

   | Optie | Beschrijving |
   | ------ | ----------- |
   | `Default` | Hiermee past u de standaardinstelling voor uitlijning toe die is opgegeven in het stijlblad van het huidige thema. |
   | `Left` | Hiermee lijnt u de eenheid uit langs de linkerrand van de bovenliggende container, waarbij rekening wordt gehouden met de opgegeven opvulling. |
   | `Center` | Hiermee lijnt u de eenheid in het midden van de bovenliggende container uit, waarbij rekening wordt gehouden met de opgegeven opvulling. |
   | `Right` | Hiermee lijnt u de eenheid uit langs de rechterrand van de bovenliggende container, waarbij rekening wordt gehouden met de opgegeven opvulling. |

   {style="table-layout:auto"}

1. Stel de **[!UICONTROL Border]** stijl die wordt toegepast op alle vier zijden van de Product Recommendations-eenheid:

   | Optie | Beschrijving |
   | ------ | ----------- |
   | `Default` | Past de standaardrandstijl toe die door het bijbehorende stijlblad wordt gespecificeerd. |
   | `None` | Geeft geen zichtbare indicatie van de eenheidsgrenzen. |
   | `Dotted` | De rand van de eenheid wordt weergegeven als een stippellijn. |
   | `Dashed` | De rand van de eenheid wordt weergegeven als een onderbroken lijn. |
   | `Solid` | De rand van de eenheid wordt weergegeven als een effen lijn. |
   | `Double` | De rand van de eenheid wordt weergegeven als een dubbele lijn. |
   | `Groove` | De rand van de eenheid wordt weergegeven als een gegroefde lijn. |
   | `Ridge` | De rand van de eenheid wordt weergegeven als een afgeronde lijn. |
   | `Inset` | De rand van de eenheid wordt weergegeven als een inzetlijn. |
   | `Outset` | De rand van de eenheid wordt weergegeven als een omtreklijn. |

   {style="table-layout:auto"}

1. Als u een andere randstijl dan `None`, vult u de weergaveopties voor de rand in:

   | Optie | Beschrijving |
   | ------ |------------ |
   | [!UICONTROL Border Color] | Geef de kleur op door een staal te kiezen, op de kleurkiezer te klikken of door een geldige kleurnaam of een gelijkwaardige hexadecimale waarde in te voeren. |
   | [!UICONTROL Border Width] | Voer het aantal pixels in voor de lijnbreedte van de rand. |
   | [!UICONTROL Border Radius] | Voer het aantal pixels in om de grootte te bepalen van de straal die wordt gebruikt om elke hoek van de rand te afronden. |

   {style="table-layout:auto"}

1. (Optioneel) Geef de namen op van **[!UICONTROL CSS classes]** in het huidige stijlblad toe te passen op de eenheid.

   Scheid meerdere klassennamen met een spatie.

1. Voer in pixels waarden in voor de **[!UICONTROL Margins and Padding]** om de buitenste marges en de binnenopvulling van de eenheid te bepalen.

   Voer de overeenkomende waarden in het diagram in.

   | Containergebied | Beschrijving |
   | ------ | ----------- |
   | [!UICONTROL Margins] | De hoeveelheid lege ruimte die wordt toegepast op de buitenrand van alle zijden van de eenheid. Opties: `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | De hoeveelheid lege ruimte die wordt toegepast op de binnenrand van alle zijden van de eenheid. Opties: `Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}
