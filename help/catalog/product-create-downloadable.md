---
title: Downloadbaar product
description: Leer hoe u een downloadbaar product maakt dat als digitaal bestand kan worden geleverd.
exl-id: c3dd4c5f-adc1-4a8f-a9da-7f0dedd1ee34
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1622'
ht-degree: 0%

---

# Downloadbaar product

Een downloadbaar product kan alles zijn wat u als bestand kunt leveren, zoals een eBook, muziek, video, softwaretoepassing of update. U kunt elk nummer afzonderlijk in een album te koop aanbieden en verkopen. U kunt ook een downloadbaar product gebruiken om een elektronische versie van uw productcatalogus te leveren.

Omdat de download pas na de aankoop beschikbaar is, kunt u samples opgeven, zoals een fragment uit een boek, een clip uit een audiobestand of een trailer van een video. Een voorbeeld is iets dat de klant kan proberen voordat hij het product koopt. De bestanden die u ter beschikking stelt om te downloaden, kunnen worden geüpload naar uw server of van een andere server.

![ Downloadbaar product ](./assets/storefront-product-downloadable.png){width="700" zoomable="yes"}

Downloadbare producten kunnen worden geconfigureerd om te vereisen dat de klant zich aanmeldt bij een account om de koppeling te ontvangen of kunnen via e-mail worden verzonden en met anderen worden gedeeld. De status van de order voordat de download beschikbaar wordt, standaardwaarden en andere leveringsopties worden ingesteld in de configuratie. Houd rekening met het volgende wanneer u downloadbare catalogustoevoegingen wilt plannen:

- Downloadbare producten kunnen worden geüpload naar de server of worden gekoppeld vanaf een andere server op internet.

- U kunt bepalen hoe vaak een klant een product kan downloaden.

- Klanten die een downloadbaar product aanschaffen, kunnen zich eerst aanmelden voordat ze de kassa doorlopen.

- De levering van een downloadbaar product kan plaatsvinden wanneer de bestelling de status `Pending` of `Invoiced` heeft.

- Omdat de downloadbare producten niet worden verscheept, wordt de _Verschepende_ stap van de controle overgeslagen wanneer de kar slechts het downloadbare product bevat.


## Downloadopties configureren

De downloadbare configuratiemontages bepalen de standaardwaarden en de leveringsopties voor downloadbare producten en specificeren als de gasten downloads kunnen kopen.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Catalog]** uit en kies **[!UICONTROL Catalog]** eronder.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de _[!UICONTROL Downloadable Product Options]_&#x200B;sectie uit.

   ![ Downloadbare Opties van het Product ](../configuration-reference/catalog/assets/catalog-downloadable-product-options.png){width="700" zoomable="yes"}

   Voor een gedetailleerde lijst van deze configuratieopties, zie [_Downloadbare Opties van het Product_](../configuration-reference/catalog/catalog.md#downloadable-product-options) in de _Verwijzing van de Configuratie_.

1. Stel **[!UICONTROL Order Item Status to Enable Downloads]** in op een van de volgende opties om de status van het orderproces te bepalen wanneer het downloaden beschikbaar wordt:

   - `Pending`
   - `Invoiced`

1. Als u een standaardlimiet wilt instellen voor het aantal downloads dat één klant kan uitvoeren, voert u het aantal voor **[!UICONTROL Default Maximum Number of Downloads]** in.

1. Stel **[!UICONTROL Shareable]** in op een van de volgende opties:

   - `Yes` - Hiermee kunnen klanten de downloadkoppeling naar anderen e-mailen.
   - `No` - Hiermee voorkomt u dat klanten de downloadkoppeling delen met anderen door te vereisen dat klanten zich aanmelden bij hun accounts om toegang te krijgen tot downloadkoppelingen.

1. Voer bij **[!UICONTROL Default Sample Title]** de kop in die u boven de selectie van monsters wilt weergeven.

   ![ Titel van de Steekproef ](./assets/product-downloadable-config-sample-title.png){width="400"}

1. Voer bij **[!UICONTROL Default Link Title]** de standaardtekst in die u voor downloadkoppelingen wilt gebruiken.

1. Als u de downloadkoppeling in een nieuw browservenster wilt openen, stelt u **[!UICONTROL Opens Links in New Window]** in op `Yes` .

   Deze instelling wordt gebruikt om het browservenster naar de winkel open te houden.

1. Stel **[!UICONTROL Use Content Disposition]** in op een van de volgende opties om te bepalen hoe downloadbare inhoud wordt geleverd:

   - `Attachment` - Levert de downloadkoppeling per e-mail als bijlage.
   - `Inline` - Levert de downloadkoppeling als een koppeling op een webpagina.

1. Stel **[!UICONTROL Disable Guest Checkout if Cart Contains Downloadable Items]** in op `Yes` als u wilt dat kopers zich registreren voor een klantenaccount en zich aanmelden voordat ze een download aanschaffen.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

## Een downloadbaar product maken

De volgende instructies tonen het proces aan om een downloadbaar product te creëren gebruikend a [ productmalplaatje ](attribute-sets.md), vereiste gebieden, en basismontages. Elk vereist gebied is duidelijk met een rode asterisk (`*`). Wanneer u de basisbeginselen hebt voltooid, kunt u de overige productinstellingen naar wens voltooien.

>[!NOTE]
>
>Downloadbare bestandsnamen kunnen letters en cijfers bevatten. Een streepje of onderstrepingsteken kan worden gebruikt om een spatie tussen woorden te vertegenwoordigen. Ongeldige tekens in de bestandsnaam worden vervangen door een onderstrepingsteken.

### Stap 1: Kies het producttype

1. Voor _Admin_ sidebar, ga **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Voor _[!UICONTROL Add Product]_( ![ de pijl van het Menu ](../assets/icon-menu-down-arrow-red.png){width="25"}) menu bij de hoger-juiste hoek, kies `Downloadable Product`.

   ![ voeg Downloadbaar Product ](./assets/product-add-downloadable.png){width="700" zoomable="yes"} toe

### Stap 2: Kies de kenmerkset

De steekproefgegevens omvatten een [ geplaatste attributen ](attribute-sets.md) genoemd _Downloadbaar_ die speciale gebieden voor downloadbare producten heeft. U kunt een bestaande sjabloon gebruiken of een andere sjabloon maken voordat het product wordt opgeslagen.

Voer een van de volgende handelingen uit om de kenmerkset te kiezen die als sjabloon voor het product wordt gebruikt:

- Voer bij **[!UICONTROL Search]** de naam in van de kenmerkset.

- Kies in de lijst de kenmerkset `Downloadable` .

Het formulier wordt bijgewerkt met de wijziging.

![ kies Vastgestelde Attributen ](./assets/product-create-choose-attribute-set-downloadable.png){width="600" zoomable="yes"}

### Stap 3: Voer de vereiste instellingen in

1. Voer de **[!UICONTROL Product Name]** in.

1. Accepteer de standaardwaarde **[!UICONTROL SKU]** die is gebaseerd op de productnaam of voer een andere naam in.

1. Voer het product **[!UICONTROL Price]** in.

1. Stel **[!UICONTROL Enable Product]** in op `No` omdat het product nog niet kan worden gepubliceerd.

1. Klik op **[!UICONTROL Save]** en ga verder.

   Wanneer het product wordt bewaard, verschijnt de [ verkiesster van de Mening van de Opslag ](introduction.md#product-scope) in de upper-left hoek.

1. Kies de locatie **[!UICONTROL Store View]** waar het product beschikbaar moet zijn.

   ![ kies de Mening van de Opslag ](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

### Stap 4: De basisinstellingen voltooien

1. Stel **[!UICONTROL Tax Class]** in op een van de volgende opties:

   - `None`
   - `Taxable Goods`

1. Voer de **[!UICONTROL Quantity]** in van het product dat in voorraad is.

   Let op het volgende:

   - Standaard is **[!UICONTROL Stock Status]** ingesteld op `Out of Stock` .

   - Omdat downloadbare producten niet worden verzonden, wordt het veld **[!UICONTROL Weight]** niet gebruikt. Als u deze eigenschap toelaat, wordt het a [ Eenvoudig product ](product-create-simple.md) en _is dit downloadbare product?_ kan niet worden gebruikt.

   >[!NOTE]
   >
   >Als u [ Inventory management ](../inventory-management/introduction.md) toelaat, plaatsen de Enige verkopers van Source de hoeveelheid in deze sectie. De multi handelaars van Source voegen bronnen en hoeveelheden in de Bronsectie toe. Zie het volgende _toewijzen Bronnen en Hoeveelheden (Inventory management)_ sectie.

1. Accepteer de standaardinstelling **[!UICONTROL Visibility]** van `Catalog, Search` .

1. Om het product in de [ lijst van nieuwe producten ](../content-design/widget-new-products-list.md) te voorzien, selecteer **[!UICONTROL Set Product as New]** checkbox.

1. Als u _[!UICONTROL Categories]_&#x200B;aan het product wilt toewijzen, klikt u op het vak **[!UICONTROL Select…]**&#x200B;en voert u een van de volgende handelingen uit:

   **kies een bestaande categorie**:

   - Typ in het vak totdat u een overeenkomst hebt gevonden.

   - Schakel het selectievakje in van elke categorie die u wilt toewijzen.

   **creeer een categorie**:

   - Klik op **[!UICONTROL New Category]**.

   - Ga **[!UICONTROL Category Name]** in en kies **[!UICONTROL Parent Category]**, die zijn positie in de [ menustructuur ](category-root.md) bepaalt.

   - Klik op **[!UICONTROL Create Category]**.

1. Stel **[!UICONTROL Format]** in op een van de volgende opties:

   - `Download`
   - `DVD`

   Indien nodig, kunt u de [ attributen ](attribute-product-create.md) uitgeven om meer waarden toe te voegen.

   Er kunnen aanvullende kenmerken zijn die het product beschrijven. De selectie varieert per kenmerkset en u kunt deze later voltooien.

#### Bronnen en hoeveelheden toewijzen ([!DNL Inventory Management])

{{$include /help/_includes/inventory-assign-sources.md}}

### Stap 5: Voer de downloadbare gegevens in

De rol neer, breidt ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de _[!UICONTROL Downloadable Information]_&#x200B;sectie uit, en selecteert checkbox **[!UICONTROL Is this downloadable product?]**.

Als deze optie is ingeschakeld, heeft de sectie _[!UICONTROL Downloadable Information]_&#x200B;twee delen. In het eerste deel wordt elke downloadkoppeling beschreven en in het tweede deel wordt elk voorbeeldbestand beschreven. De standaardwaarde voor vele van deze opties kan in de [ configuratie ](#configure-the-download-options) worden geplaatst.

![ Downloadbare Informatie ](./assets/product-downloadable-information.png){width="600" zoomable="yes"}

#### De koppelingen voltooien

1. Voer in de sectie _[!UICONTROL Links]_&#x200B;de **[!UICONTROL Title]**&#x200B;in die u als kop voor de downloadkoppelingen wilt gebruiken.

1. Selecteer, indien van toepassing, het selectievakje **[!UICONTROL Links can be purchased separately]** .

1. Klik op **[!UICONTROL Add Link]** en voer de volgende handelingen uit:

   - Voer de **[!UICONTROL Title]** en **[!UICONTROL Price]** van de download in.

   - Kies voor zowel **[!UICONTROL File]** als **[!UICONTROL Sample]** -bestanden een van de volgende verspreidingsmethoden voor de downloads:

      - `Upload File` - Kies deze methode om het distributiebestand naar de server te uploaden. Blader naar het bestand en selecteer het voor uploaden.
      - `URL` - Kies deze methode om het distributiebestand te openen via een URL. Voer de volledige URL in naar het downloadbestand.

   >[!NOTE]
   >
   >Koppelingen naar externe bronnen kunt u niet gebruiken als downloadbare producten. De geldige verbindingsdomeinen zijn vooraf bepaald programmatically in het `env.php` dossier (zie [ env.php- verwijzing ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/files/config-reference-envphp.html) in de _Gids van de Configuratie_).

   - Stel **[!UICONTROL Shareable]** in op een van de volgende opties:

      - `No` - Vereist dat klanten zich aanmelden bij hun accounts om toegang te krijgen tot de downloadkoppeling.

      - `Yes` - Verzendt de koppeling via e-mail, die klanten met anderen kunnen delen.

      - `Use Config` - gebruikt de methode die in de [ Downloadbare configuratie van de Opties van het Product ](../configuration-reference/catalog/catalog.md) wordt gespecificeerd.

   - Voer een van de volgende handelingen uit:

      - Als u het downloaden per klant wilt beperken, voert u het maximumaantal voor **[!UICONTROL Max. Downloads]** in.
      - Schakel het selectievakje **[!UICONTROL Unlimited]** in om onbeperkt downloaden toe te staan.

   ![ Detail van de Verbinding ](./assets/product-downloadable-link-detail.png){width="600" zoomable="yes"}

1. Als u nog een koppeling wilt toevoegen, klikt u op **[!UICONTROL Add Link]** en herhaalt u deze stappen.

#### De monsters invullen

1. Voer in de sectie _[!UICONTROL Samples]_&#x200B;de **[!UICONTROL Title]**&#x200B;in die u als kop voor de voorbeelden wilt gebruiken.

1. Klik op **[!UICONTROL Add Link]** om de gegevens voor elk voorbeeld te voltooien.

   ![ Steekproeven ](./assets/product-downloadable-samples.png){width="600" zoomable="yes"}

1. Vul de koppelingsdetails als volgt in:

   - Voer de **[!UICONTROL Title]** van het afzonderlijke voorbeeld in.

   - Kies een van de volgende verspreidingsmethoden:

      - `Upload File` - Kies deze methode om het distributiebestand naar de server te uploaden. Blader naar het bestand en selecteer het voor uploaden.
      - `URL` - Kies deze methode om het distributiebestand te openen via een URL. Voer de volledige URL in naar het downloadbestand.

   - Als u nog een voorbeeld wilt toevoegen, klikt u op **[!UICONTROL Add Link]** en herhaalt u deze stappen.

   - Om de orde van de steekproeven te veranderen, pak het _pictogram van de Orde van de Verandering_ ( ![ het controlemechanisme van de Positie ](../assets/icon-sort-order.png) ) en sleep de steekproef aan een nieuwe positie.

### Stap 6: De productinformatie invullen

Schuif omlaag en voltooi indien nodig de informatie in de volgende secties:

- [Inhoud](product-content.md)
- [Afbeeldingen en video&#39;s](product-images-and-video.md)
- [Optimalisatie zoekmachine](product-search-engine-optimization.md)
- [Verwante producten, Up-Sells en Cross-Sells](related-products-up-sells-cross-sells.md)
- [Aanpasbare opties](settings-advanced-custom-options.md)
- [Producten op websites](settings-basic-websites.md)
- [Ontwerp](settings-advanced-design.md)
- [Cadeauopties](product-gift-options.md)

### Stap 7: Publish het product

Als u het product wilt publiceren in de catalogus, stelt u **[!UICONTROL Enable Product]** in op `Yes` en voert u een van de volgende handelingen uit:

**Methode 1:** sparen en Voorproef

- Klik in de rechterbovenhoek op **[!UICONTROL Save]** .

- Om het product in uw opslag te bekijken, verkies **[!UICONTROL Customer View]** op _Admin_ ( ![ pijl van het Menu ](../assets/icon-menu-down-arrow-black.png)) menu.

  De winkel wordt geopend in een nieuw browsertabblad.

  ![ Mening van de Klant ](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

**Methode 2:** sparen en sluit

Voor _[!UICONTROL Save]_( ![ de pijl van het Menu ](../assets/icon-menu-down-arrow-red.png){width="25"}) menu, kies **[!UICONTROL Save & Close]**.

## Storefront-ervaring

In het dashboard voor de klantenaccount koppelt de pagina _[!UICONTROL My Downloadable Products]_&#x200B;naar elke volgorde van downloadbare producten. De downloads worden beschikbaar via de account van de klant wanneer de bestelling is voltooid.

![ Mijn downloadbare Producten ](./assets/customer-account-my-downloadable-products.png){width="700" zoomable="yes"}

De volgende lijst beschrijft de _Mijn Downloadbare Producten_ waarden:

| Kolom | Beschrijving |
|--- |--- |
| [!UICONTROL Order#] | De [ orde ](../stores-purchase/orders.md) waarin het downloadbare product werd gekocht. Verzekert een verbinding aan het ordendetail. |
| [!UICONTROL Date] | Aanmaakdatum van bestelling. |
| [!UICONTROL Title] | De naam van het downloadbare product dat bij de bestelling is aangeschaft. Verzekert een verbinding aan het downloadbare product. |
| [!UICONTROL Status] | Status van orderverwerking. |
| [!UICONTROL Remaining Downloads] | Aantal beschikbare downloads van het gedownloade product. |

_&#x200B;**om een productdossier van het rekeningsdashboard**&#x200B;_ te downloaden

1. In hun accountdashboard kiest de klant **[!UICONTROL My Downloadable Products]** .

1. Hiermee zoekt u de volgorde in de lijst en klikt u op de koppeling na de titel.

1. In de laag-juiste hoek van het downloadvenster, klikt het _download_ pictogram.

1. Hiermee zoekt u het bestand op de downloadlocatie en slaat u het bestand op de gewenste locatie op.
