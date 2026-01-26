---
title: Verzendlabels en -pakketten maken
description: Leer hoe u items in een bestelling verpakt en verzendlabels maakt.
exl-id: ed9be72a-0dcd-4dbf-82ba-b1d75a1e76fd
feature: Shipping/Delivery, Orders
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '1944'
ht-degree: 0%

---

# Verzendlabels maken

Als je verzendlabels wilt maken, moet je eerst je verzenddrageraccount instellen voor ondersteuning van labels. Volg vervolgens de aanwijzingen om een beschrijving van het pakket en de inhoud ervan in te voeren.

Nadat u de verzendlabelgegevens hebt geconfigureerd en een bestelling hebt verzonden, maakt Commerce verbinding met het transportsysteem, verzendt het een bestelling en ontvangt het een verzendlabel en trackingnummer. Als het systeem een verzendlabel voor deze verzending bevat, wordt dit vervangen door een nieuw label. Bestaande volgnummers worden echter niet vervangen. Een nieuw trackingnummer wordt toegevoegd aan het bestaande nummer.

## Stap 1: Neem contact op met je verzendende maatschappijen

Voordat je begint, moet je ervoor zorgen dat je verzendaccounts zijn ingesteld op het verwerken van labels. Sommige vervoerders vragen mogelijk extra kosten om verzendlabels aan je account toe te voegen.

Neem contact op met elke vervoerder die je gebruikt om verzendlabels voor je winkel te activeren.

Volg de instructies van elke vervoerder om ondersteuning voor verzendlabels aan uw account toe te voegen.

- **FedEx** - de Diensten van de Integratie van het Web van het Contact [ FedEx ](https://www.fedex.com/en-us/api/get-support.html) om over de vereisten van de etiketdruk voor uw rekening te leren.
- **USPS** - verwijs naar het [ Web Tools API Portal ](https://www.usps.com/business/web-tools-apis/#ssc) onder het Centrum van de Steun van de Schepper om te leren hoe te opstelling uw geloofsbrieven van de etiketdruk.
- **UPS** - Contacteer [ UPS ](https://www.ups.com/us/en/support/contact-us.page) om te bevestigen dat uw rekening het verschepen etiketten steunt. Als u verzendlabels wilt genereren, moet u de optie UPS XML gebruiken.
- **DHL** - de Oplossingen van de eCommerce van het Contact [ ](https://www.dhl.com/us-en/home/our-divisions/ecommerce-solutions.html) om over de vereisten van de etiketdruk voor uw rekening te leren.

## Stap 2: Werk de configuratie voor elke drager bij

1. Zorg ervoor dat uw [ Informatie van de Opslag ](../getting-started/store-details.md#store-information) volledig is.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en selecteer **[!UICONTROL Shipping Settings]** .

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL Origin]** sectie uit en vorm **[!UICONTROL Shipping Origin Address]**.

1. Volg de onderstaande instructies voor elke drageraccount die is geactiveerd voor labelafdrukken.

### UPS-configuratie

United Parcel Service verzendt zowel binnenlands als internationaal. Verzendlabels kunnen echter alleen worden gegenereerd voor zendingen die afkomstig zijn uit de Verenigde Staten.

1. Kies _[!UICONTROL Sales]_in de sectie **[!UICONTROL Delivery Methods]**in het linkerdeelvenster.

1. Breid ![ selecteur van de Uitbreiding ](../assets/icon-display-expand.png) de **[!UICONTROL UPS]** sectie uit.

1. Controleer of uw UPS **[!UICONTROL Shipper Number]** juist is.

   Het verzendnummer wordt alleen weergegeven wanneer [!DNL United Parcel Service XML] is ingeschakeld.

1. Klik op **[!UICONTROL Save Config]**.

### USPS-configuratie

De [!DNL United States Postal Service] wordt zowel intern als internationaal verzonden.

{{$include /help/_includes/usps-api-type-configuration-note.md}}

1. Voortdurend in de **[!UICONTROL Delivery Methods]** configuratie, breid ![ de selecteur van de Uitbreiding ](../assets/icon-display-expand.png) uit de **[!UICONTROL USPS]** sectie.

1. Selecteer **[!UICONTROL USPS Type]** als `USPS Rest APIs` of `USPS Web Tools API` .

1. Controleer of **[!UICONTROL Secure Gateway URL]** correct is.

1. Voer de **[!UICONTROL Password]** in die door USPS aan u is verstrekt.

1. Controleer of de volgende configuratie is voltooid op basis van de geselecteerde **[!UICONTROL USPS Type]** :

   Als u de webtools-API van USPS gebruikt:
   - Gebruikersnaam
   - Wachtwoord

   Als u de REST-API&#39;s van USPS gebruikt:
   - Consumentencode
   - Consumentengeheim
   - Prijsopties
   - Accounttype
   - Rekeningnummer
   - Klantenregistratie-ID (CRID)
   - Id van stramien (MID)
   - Manifest MID
   - AES/ITN

1. Stel **[!UICONTROL Size]** in op `Large` en voer waarden in voor de volgende afmetingen:

   - Lengte
   - Breedte
   - Hoogte
   - Meisje

1. Klik op **[!UICONTROL Save Config]**.

### FedEx-configuratie

FedEx wordt binnenlands en internationaal verzonden. Winkels buiten de Verenigde Staten kunnen alleen FedEx-labels maken voor internationale verzendingen.

1. Voortdurend in de **[!UICONTROL Delivery Methods]** configuratie, breid ![ de selecteur van de Uitbreiding ](../assets/icon-display-expand.png) uit de **[!UICONTROL FedEx]** sectie.

1. Controleer of de volgende FedEx-referenties correct zijn:

   - Meternummer
   - Sleutel
   - Wachtwoord

1. Klik op **[!UICONTROL Save Config]**.

### DHL-configuratie

DHL verleent internationale scheepvaartdiensten.

1. Voortdurend in de **[!UICONTROL Delivery Methods]** configuratie, breid ![ de selecteur van de Uitbreiding ](../assets/icon-display-expand.png) uit de **[!UICONTROL DHL]** sectie.

1. Controleer of **[!UICONTROL Gateway URL]** correct is.

1. Controleer of de volgende gegevens zijn voltooid:

   - Toegang-id
   - Wachtwoord
   - Rekeningnummer

1. Klik op **[!UICONTROL Save Config]**.

## Stap 3: Verzendlabels maken

### Methode 1: Label maken voor nieuwe verzending

1. Voor _Admin_ sidebar, ga **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Zoek de volgorde in het raster en open de record.

   De status van de volgorde moet `Pending` of `Processing` zijn.

1. Klik in de rechterbovenhoek op **[!UICONTROL Ship]** .

1. Bevestig de verzendgegevens op basis van de vereisten van de vervoerder.

1. Selecteer in de rechterbenedenhoek het selectievakje **[!UICONTROL Create Shipping Label]** .

1. Klik op **[!UICONTROL Submit Shipment]**.

1. Producten toevoegen of bijwerken in pakket:

   - Klik op **[!UICONTROL Add Products]** om producten uit de volgorde aan het pakket toe te voegen. In de kolom _[!UICONTROL Quantity]_wordt het maximumaantal producten weergegeven dat beschikbaar is voor het pakket.

   - Schakel het selectievakje in van elk product dat aan het pakket moet worden toegevoegd en voer de **[!UICONTROL Quantity]** van elk product in. Klik vervolgens op **[!UICONTROL Add Selected Product(s) to Package]** .

   - Klik op **[!UICONTROL Add Package]** om een pakket toe te voegen.

   - Als u een pakket wilt verwijderen, klikt u op **[!UICONTROL Delete Package]** .

   - Als u een bestelling wilt annuleren, klikt u op **[!UICONTROL Cancel]** . Er wordt geen verzendlabel gemaakt en het selectievakje _[!UICONTROL Create Shipping Label]_wordt gewist.

   >[!NOTE]
   >
   >Als u een ander pakkettype gebruikt dan de standaardinstelling of een handtekening vereist, kunnen de verzendkosten afwijken van wat u de klant in rekening hebt gebracht. Het verschil in verzendkosten wordt niet in je winkel weergegeven.

1. Klik op **[!UICONTROL OK]**.

   Commerce maakt verbinding met het transportsysteem, verzendt de bestelling en ontvangt een verzendlabel en trackingnummer voor elk pakket.

### Methode 2: Label maken voor bestaande verzending

1. Voor _Admin_ sidebar, ga **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Zoek de volgorde in het raster en open het verzendformulier.

1. Klik in de sectie _[!UICONTROL Shipping and Tracking Information]_op **[!UICONTROL Create Shipping Label]**.

1. Verdeel de geordende producten naar de juiste pakketten en klik op **[!UICONTROL OK]** .

1. Klik op **[!UICONTROL Show Packages]** om de pakketgegevens te bekijken.

## Stap 4: De labels afdrukken

Verzendlabels worden gegenereerd in PDF-indeling en kunnen worden afgedrukt via de beheerfunctie. Elk label bevat het ordernummer en het pakketnummer.

>[!NOTE]
>
>Omdat er voor elk pakket een afzonderlijke verzendopdracht wordt gemaakt, kunnen er meerdere verzendlabels worden ontvangen voor één verzending.

### Methode 1: Label afdrukken vanuit verzendformulier

1. Voor _Admin sidebar_, ga naar één van de volgende pagina&#39;s en bepaal de plaats van het ladingsverslag:

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]** - Zoek de volgorde in het raster en open de record. Kies **[!UICONTROL Shipments]** in het linkerdeelvenster. Open vervolgens de ladingsrecord.

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]** - Zoek de verzending in het raster en open de record.

1. Als u het PDF-bestand wilt downloaden, gaat u naar de _[!UICONTROL Shipping and Tracking]_-sectie van het formulier en klikt u op **[!UICONTROL Print Shipping Label]**.

   Afhankelijk van uw browserinstellingen kunnen de verzendlabels rechtstreeks vanuit het PDF-bestand worden weergegeven en afgedrukt.

   De knop _[!UICONTROL Print Shipping Label]_wordt alleen weergegeven nadat de provider labels voor de verzending heeft gegenereerd. Klik op **[!UICONTROL Create Shipping Label]**als de knop ontbreekt. De knop wordt weergegeven nadat Commerce het label van de carrier heeft ontvangen.

### Methode 2: etiketten afdrukken voor meerdere bestellingen

1. Voor _Admin sidebar_, ga naar één van de volgende pagina&#39;s en selecteer dan de orden of de transporten voor druk:

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]** - Schakel in het raster het selectievakje van elke bestelling in met de verzendlabels die u wilt afdrukken.

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]** - Schakel in het raster het selectievakje in van elke verzending met labels die u wilt afdrukken.

1. Stel het besturingselement **[!UICONTROL Actions]** in op `Print Shipping Labels` .

1. Klik op **[!UICONTROL Submit]**.

Voor elke verzending die betrekking heeft op de geselecteerde bestellingen, wordt een volledige set verzendlabels afgedrukt.

## Vereiste instellingen voor drager

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Type] | De types van pakket verschillen door drager en methode. Het standaardpakkettype voor elke drager wordt aanvankelijk geselecteerd. USPS vereist niet het pakkettype voor binnenlandse verzendingen. |
| [!UICONTROL Customs Value] | (Alleen internationale zendingen) De opgegeven waarde of verkoopprijs van de inhoud van een internationale zending. |
| [!UICONTROL Total Weight] | Het totale gewicht van alle aan de verpakking toegevoegde producten wordt automatisch berekend. U kunt de waarde ook handmatig wijzigen en invoeren in kilogram of in kilogram. |
| [!UICONTROL Length, Width, Height] | (Optioneel) De pakketafmetingen worden alleen gebruikt voor aangepaste pakketten. U kunt de maateenheden opgeven als inches of centimeters.<br/><br/>**[!UICONTROL Not Required]**: de verzendende maatschappij stuurt de winkel geen bevestiging van levering.<br/><br/>**[!UICONTROL No Signature]**: de verzendende maatschappij stuurt een leveringsbevestiging zonder de handtekening van de ontvanger naar de winkel.<br/><br/>**[!UICONTROL Signature Required]**: De verzendende vervoerder verkrijgt de handtekening van de ontvanger en verstrekt de winkel een afgedrukte kopie.<br/><br/>**[!UICONTROL Direct]**: (Alleen FedEx) FedEx verkrijgt een handtekening van iemand op het bezorgadres. Als er geen persoon beschikbaar is om voor het pakket te ondertekenen, probeert de vervoerder het pakket op een ander tijdstip te leveren.<br/><br/>**[!UICONTROL Indirect]**: (Alleen FedEx-eigen leveringen) FedEx verkrijgt de handtekening van iemand (mogelijk een buur of manager van gebouwen) op het bezorgadres. De ontvanger kan een ondertekende FedEx-deurtag achterlaten om ervoor te zorgen dat het pakket wordt verlaten zonder dat er iemand aanwezig is om ervoor te ondertekenen.<br/><br/>**[!UICONTROL Contents]**: (Alleen USPS) Selecteer een van de volgende beschrijvingen van het pakket:<br/> - Cadeautje <br/> - Documenten <br/> - Handelsvoorbeeld <br/> - Geretourneerde goederen <br/> - Merchandise <br/> - Overige <br/><br/>**[!UICONTROL Explanation]**: (Alleen USPS) Een gedetailleerde beschrijving van de pakketinhoud.<br/><br/>**[!UICONTROL Adult Required]**: De verzendende vervoerder verkrijgt de handtekening van een volwassen ontvanger en verstrekt de winkel een afgedrukte kopie. |

{style="table-layout:auto"}

## Pakketten maken

Het venster _[!UICONTROL Create Packages]_wordt weergegeven wanneer u een verzendlabel maakt. U kunt direct beginnen het eerste pakket te vormen.

### Een pakket configureren

>[!NOTE]
>
>Als u de niet-standaardwaarde voor [!UICONTROL Type] selecteert of een handtekeningbevestiging vereist, kan de prijs van een verzending afwijken van de prijs die u aan de klant in rekening brengt.

1. Klik op **[!UICONTROL Add Products]** om een lijst met verscheepte producten weer te geven en deze aan het pakket toe te voegen.

   - Vermeld de producten en de hoeveelheden.

     In de kolom _[!UICONTROL Qty]_wordt de maximale hoeveelheid weergegeven die u kunt toevoegen. Voor de eerste verpakking is het nummer de totale hoeveelheid van het te verzenden product.

   - Klik op **[!UICONTROL Add Selected Product(s) to Package]** om de producten aan het pakket toe te voegen.

1. Klik op **[!UICONTROL Add Package]** om een pakket toe te voegen.

   U kunt meerdere pakketten toevoegen en tegelijkertijd bewerken.

1. Als u een pakket wilt verwijderen, klikt u op **[!UICONTROL Delete Package]** .

Nadat de producten aan de verpakking zijn toegevoegd, kan de hoeveelheid niet rechtstreeks worden bewerkt.

### De hoeveelheid vergroten

1. Klik op **[!UICONTROL Add Selection]**.

1. Voer de extra hoeveelheid in.

   Het nummer wordt toegevoegd aan de vorige hoeveelheid van het product in de verpakking.

### De hoeveelheid verlagen

1. Verwijder het product uit de verpakking.

1. Klik op **[!UICONTROL Add Selection]**.

1. Voer de nieuwe, kleinere waarde in.

### Verzendlabels genereren

Nadat u alle producten hebt verdeeld, is het totale aantal pakketten dat u gaat gebruiken gelijk aan het nummer van het laatste pakket in de lijst. De _O.K._ knoop wordt onbruikbaar gemaakt tot alle verscheepte punten aan pakketten worden verdeeld, en alle noodzakelijke informatie is volledig.

Klik op **[!UICONTROL OK]** om de labels te genereren.

U kunt desgewenst op **[!UICONTROL Cancel]** klikken om het proces te stoppen. De pakketten worden niet opgeslagen en het verzendlabel wordt geannuleerd.

### Veldomschrijvingen

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Type] | Geeft het type pakket aan. Selecteer een van de vooraf gedefinieerde waarden. De beschikbare pakkettypen zijn verschillend voor elke verzender. Als het pop-upvenster Pakketten maken wordt geopend, wordt het standaardpakket voor de verzendende provider weergegeven in het veld Type. Als u een pakket selecteert dat niet door een verzendende vervoerder is ontworpen, moet u de afmetingen van het pakket invoeren. Voor verzendlabels die zijn gemaakt voor DHL-, FedEx- en UPS-verzendingen, wordt het veld Type van goederen ingesteld op `Merchandise` . Voor USPS, wijst het gebied op de waarde van het _gebied van de Inhoud_ in het _[!UICONTROL Create Packages]_venster. |
| [!UICONTROL Total Weight] | Het totale gewicht van een verpakking. Het veld wordt voorgevuld met het totale gewicht van de producten in een verpakking. De meeteenheid kan worden ingesteld op kilogram of kilogram. |
| [!UICONTROL Length] | De lengte van een pakket, geheel getal en drijvende-kommagetallen. Het veld wordt ingeschakeld als het aangepaste pakkettype wordt gebruikt. De maateenheid kan worden ingesteld op inches of centimeters. |
| [!UICONTROL Width] | De breedte van een pakket, geheel getal en drijvende-kommagetallen. Het veld wordt ingeschakeld als het aangepaste pakkettype wordt gebruikt. U kunt de maateenheden opgeven in het vervolgkeuzemenu naast het veld Hoogte. U kunt deze eenheden selecteren tussen inches en centimeters. |
| [!UICONTROL Height] | De hoogte van een pakket, geheel getal en drijvende-kommagetallen. Het veld wordt ingeschakeld als het aangepaste pakkettype wordt gebruikt. U kunt de maateenheden opgeven in het vervolgkeuzemenu naast het veld Hoogte. U kunt deze eenheden selecteren tussen inches en centimeters. |
| [!UICONTROL Signature] | Definieert leveringsbevestiging. Opties:<br/><br/>**[!UICONTROL Not Required]**: er wordt geen bevestigingsbrief voor de levering naar u verzonden.<br/><br/>**[!UICONTROL No Signature]**: er wordt een bevestigingsbrief voor de levering verzonden zonder handtekening van de ontvanger.<br/><br/>**[!UICONTROL Signature Required]**: De verzendende vervoerder verkrijgt de handtekening van de ontvanger en geeft u de afgedrukte kopie ervan.<br/><br/>**[!UICONTROL Adult Required]**: De verzendende vervoerder verkrijgt de handtekening van de volwassen ontvanger en verstrekt u de afgedrukte kopie.<br/><br/>**[!UICONTROL Direct (FedEx only)]**: FedEx verkrijgt een handtekening van iemand op het bezorgadres en maakt levering mogelijk als er niemand beschikbaar is om voor het pakket te ondertekenen.<br/><br/>**[!UICONTROL Indirect (FedEx only)]**: FedEx verkrijgt een handtekening op een van de volgende drie manieren: <br/> (1) van iemand op het bezorgadres; <br/> (2) van een buur, gebouwmanager of andere persoon op het adres; of <br/> (3) de ontvanger kan een ondertekende FedEx-deurtag verlaten die vrijgave van het pakket toestaat zonder dat er iemand aanwezig is. Alleen beschikbaar voor leveringen in woningen. De opties kunnen enigszins afwijken voor verschillende verzendmethoden. Raadpleeg voor de meest recente informatie de bronnen van de scheepvaartmaatschappij. |
| [!UICONTROL Contents] | (Alleen beschikbaar voor verzendingen naar USPS) Beschrijving van de inhoud van het pakket. Opties: `Gift` / `Documents` / `Commercial Sample` / `Returned Goods` / `Merchandise` / `Other` |
| [!UICONTROL Explanation] | (Alleen USPS-verzendingen) Gedetailleerde beschrijving van de pakketinhoud. |

{style="table-layout:auto"}


<!-- Last updated from includes: 2025-11-26 10:55:00 -->
