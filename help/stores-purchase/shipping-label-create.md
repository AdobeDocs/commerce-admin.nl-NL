---
title: Verzendlabels en -pakketten maken
description: Leer hoe u items in een bestelling verpakt en verzendlabels maakt.
exl-id: ed9be72a-0dcd-4dbf-82ba-b1d75a1e76fd
feature: Shipping/Delivery, Orders
source-git-commit: 50b44190a9568a8d6ad38ab29177904596569d75
workflow-type: tm+mt
source-wordcount: '1896'
ht-degree: 0%

---

# Verzendlabels maken

Als je verzendlabels wilt maken, moet je eerst je verzenddrageraccount instellen voor ondersteuning van labels. Volg vervolgens de aanwijzingen om een beschrijving van het pakket en de inhoud ervan in te voeren.

Nadat u de verzendlabelinformatie hebt geconfigureerd en een bestelling hebt verzonden, maakt de Handel verbinding met het transportsysteem, verzendt een bestelling en ontvangt een verzendlabel en een trackingnummer. Als het systeem een verzendlabel voor deze verzending bevat, wordt dit vervangen door een nieuw label. Bestaande volgnummers worden echter niet vervangen. Een nieuw trackingnummer wordt toegevoegd aan het bestaande nummer.

## Stap 1: Neem contact op met je verzendende maatschappijen

Voordat je begint, moet je ervoor zorgen dat je verzendaccounts zijn ingesteld op het verwerken van labels. Sommige vervoerders vragen mogelijk extra kosten om verzendlabels aan je account toe te voegen.

Neem contact op met elke vervoerder die je gebruikt om verzendlabels voor je winkel te activeren.

Volg de instructies van elke vervoerder om ondersteuning voor verzendlabels aan uw account toe te voegen.

- **FedEx** - Contactpersoon [FedEx Web Integration Services][1] voor meer informatie over de vereisten voor labelafdrukken voor uw account.
- **USPS** - Raadpleeg de [Web Tools API Portal][4] onder Shipper Support Center om te leren hoe u de aanmeldingsgegevens voor het afdrukken van labels kunt instellen.
- **UPS**- Contactpersoon [UPS][2] om te bevestigen dat je account verzendlabels ondersteunt. Als u verzendlabels wilt genereren, moet u de optie UPS XML gebruiken.
- **DHL** - Contactpersoon [DHL eCommerce-oplossingen][3] voor meer informatie over de vereisten voor labelafdrukken voor uw account.

## Stap 2: Werk de configuratie voor elke drager bij

1. Zorg ervoor dat uw [Opslaggegevens](../getting-started/store-details.md#store-information) is voltooid.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Sales]** en selecteert u **[!UICONTROL Shipping Settings]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL Origin]** en configureren van de **[!UICONTROL Shipping Origin Address]**.

1. Volg de onderstaande instructies voor elke drageraccount die is geactiveerd voor labelafdrukken.

### UPS-configuratie

United Parcel Service verzendt zowel binnenlands als internationaal. Verzendlabels kunnen echter alleen worden gegenereerd voor zendingen die afkomstig zijn uit de Verenigde Staten.

1. In de _[!UICONTROL Sales]_in het linkerdeelvenster kiest u **[!UICONTROL Delivery Methods]**.

1. Uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL UPS]** sectie.

1. Controleren of uw UPS **[!UICONTROL Shipper Number]** is correct.

   Je verzendnummer wordt alleen weergegeven wanneer [!DNL United Parcel Service XML] is ingeschakeld.

1. Klik op **[!UICONTROL Save Config]**.

### USPS-configuratie

De [!DNL United States Postal Service] zowel binnenlandse als internationale schepen.

1. Het voortzetten in **[!UICONTROL Delivery Methods]** configuratie, uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL USPS]** sectie.

1. Controleer of de **[!UICONTROL Secure Gateway URL]** is correct.

1. Voer de **[!UICONTROL Password]** verstrekt door USPS.

1. Set **[!UICONTROL Size]** tot `Large` en voert u waarden in voor de volgende afmetingen:

   - Lengte
   - Breedte
   - Hoogte
   - Meisje

1. Klik op **[!UICONTROL Save Config]**.

### FedEx-configuratie

FedEx wordt binnenlands en internationaal verzonden. Winkels buiten de Verenigde Staten kunnen alleen FedEx-labels maken voor internationale verzendingen.

{{beta2-updates}}

1. Het voortzetten in **[!UICONTROL Delivery Methods]** configuratie, uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL FedEx]** sectie.

1. Controleer of de volgende FedEx-referenties correct zijn:

   - Meternummer
   - Sleutel
   - Wachtwoord

1. Klik op **[!UICONTROL Save Config]**.

### DHL-configuratie

DHL verleent internationale scheepvaartdiensten.

1. Het voortzetten in **[!UICONTROL Delivery Methods]** configuratie, uitbreiden ![Expansiekiezer](../assets/icon-display-expand.png) de **[!UICONTROL DHL]** sectie.

1. Controleer of de **[!UICONTROL Gateway URL]** is correct.

1. Controleer of de volgende gegevens zijn voltooid:

   - Toegang-id
   - Wachtwoord
   - Rekeningnummer

1. Klik op **[!UICONTROL Save Config]**.

## Stap 3: Verzendlabels maken

### Methode 1: Label maken voor nieuwe verzending

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Zoek de volgorde in het raster en open de record.

   De status van de order moet ofwel `Pending` of `Processing`.

1. Klik in de rechterbovenhoek op **[!UICONTROL Ship]**.

1. Bevestig de verzendgegevens op basis van de vereisten van de vervoerder.

1. Selecteer in de rechterbenedenhoek de optie **[!UICONTROL Create Shipping Label]** selectievakje.

1. Klik op **[!UICONTROL Submit Shipment]**.

1. Producten toevoegen of bijwerken in pakket:

   - Als u producten van de volgorde aan het pakket wilt toevoegen, klikt u op **[!UICONTROL Add Products]**. De _[!UICONTROL Quantity]_in de kolom wordt het maximumaantal producten weergegeven dat beschikbaar is voor het pakket.

   - Schakel het selectievakje in van elk product dat u aan het pakket wilt toevoegen en voer het **[!UICONTROL Quantity]** van elk. Klik vervolgens op **[!UICONTROL Add Selected Product(s) to Package]**.

   - Klik op **[!UICONTROL Add Package]**.

   - Als u een pakket wilt verwijderen, klikt u op **[!UICONTROL Delete Package]**.

   - Als u een bestelling wilt annuleren, klikt u op **[!UICONTROL Cancel]**. Er wordt geen verzendlabel gemaakt en de _[!UICONTROL Create Shipping Label]_selectievakje is uitgeschakeld.

   >[!NOTE]
   >
   >Als u een ander pakkettype gebruikt dan de standaardinstelling of een handtekening vereist, kunnen de verzendkosten afwijken van wat u de klant in rekening hebt gebracht. Het verschil in verzendkosten wordt niet in je winkel weergegeven.

1. Klik op **[!UICONTROL OK]**.

   De handel verbindt met het verschepende dragersysteem, legt de orde voor, en ontvangt een verschepend etiket en een volgnummer voor elk pakket.

### Methode 2: Label maken voor bestaande verzending

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Zoek de volgorde in het raster en open het verzendformulier.

1. In de _[!UICONTROL Shipping and Tracking Information]_sectie, klikken **[!UICONTROL Create Shipping Label]**.

1. Verdeel de geordende producten naar de juiste pakketten en klik op **[!UICONTROL OK]**.

1. Als u de pakketgegevens wilt bekijken, klikt u op **[!UICONTROL Show Packages]**.

## Stap 4: De labels afdrukken

Verzendlabels worden gegenereerd in PDF-indeling en kunnen worden afgedrukt via de beheerder. Elk label bevat het ordernummer en het pakketnummer.

>[!NOTE]
>
>Omdat er voor elk pakket een afzonderlijke verzendopdracht wordt gemaakt, kunnen er meerdere verzendlabels worden ontvangen voor één verzending.

### Methode 1: Label afdrukken vanuit verzendformulier

1. Op de _Admin sidebar_, ga naar een van de volgende pagina&#39;s en zoek de ladingsrecord:

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]** - Zoek de volgorde in het raster en open de record. Kies in het linkerdeelvenster de optie **[!UICONTROL Shipments]**. Open vervolgens de ladingsrecord.

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]** - Zoek de zending in het raster en open de record.

1. Ga naar de pagina _[!UICONTROL Shipping and Tracking]_van het formulier en klik op **[!UICONTROL Print Shipping Label]**.

   Afhankelijk van uw browserinstellingen kunnen de verzendlabels rechtstreeks vanuit het PDF-bestand worden weergegeven en afgedrukt.

   De _[!UICONTROL Print Shipping Label]_wordt alleen weergegeven nadat de vervoerder labels voor de verzending heeft gegenereerd. Klik op **[!UICONTROL Create Shipping Label]**. De knoop verschijnt nadat de Handel het etiket van de drager ontvangt.

### Methode 2: etiketten afdrukken voor meerdere bestellingen

1. Op de _Admin sidebar_ gaat u naar een van de volgende pagina&#39;s en selecteert u de bestellingen of verzendingen die u wilt afdrukken:

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]** - Schakel in het raster het selectievakje in van elke bestelling met de verzendlabels die u wilt afdrukken.

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]** - Schakel in het raster het selectievakje in van elke zending met labels die u wilt afdrukken.

1. Stel de **[!UICONTROL Actions]** controle op `Print Shipping Labels`.

1. Klik op **[!UICONTROL Submit]**.

Voor elke verzending die betrekking heeft op de geselecteerde bestellingen, wordt een volledige set verzendlabels afgedrukt.

## Vereiste instellingen voor drager

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Type] | De types van pakket verschillen door drager en methode. Het standaardpakkettype voor elke drager wordt aanvankelijk geselecteerd. USPS vereist niet het pakkettype voor binnenlandse verzendingen. |
| [!UICONTROL Customs Value] | (Alleen internationale zendingen) De opgegeven waarde of verkoopprijs van de inhoud van een internationale zending. |
| [!UICONTROL Total Weight] | Het totale gewicht van alle aan de verpakking toegevoegde producten wordt automatisch berekend. U kunt de waarde ook handmatig wijzigen en invoeren in kilogram of in kilogram. |
| [!UICONTROL Length, Width, Height] | (Optioneel) De pakketafmetingen worden alleen gebruikt voor aangepaste pakketten. U kunt de maateenheden opgeven als inches of centimeters.<br/><br/>**[!UICONTROL Not Required]**: De verzendende maatschappij stuurt geen bevestiging van levering naar de winkel.<br/><br/>**[!UICONTROL No Signature]**: De verzendende maatschappij stuurt een leveringsbevestiging zonder de handtekening van de ontvanger naar de winkel.<br/><br/>**[!UICONTROL Signature Required]**: De verzendende vervoerder verkrijgt de handtekening van de ontvanger en verstrekt de winkel een afgedrukte kopie.<br/><br/>**[!UICONTROL Direct]**: (Alleen FedEx) FedEx verkrijgt een handtekening van iemand op het bezorgadres. Als er geen persoon beschikbaar is om voor het pakket te ondertekenen, probeert de vervoerder het pakket op een ander tijdstip te leveren.<br/><br/>**[!UICONTROL Indirect]**: (Alleen FedEx-eigen leveringen) FedEx verkrijgt de handtekening van iemand (mogelijk een buur of bouwmanager) op het bezorgadres. De ontvanger kan een ondertekende FedEx-deurtag achterlaten om ervoor te zorgen dat het pakket wordt verlaten zonder dat er iemand aanwezig is om ervoor te ondertekenen.<br/><br/>**[!UICONTROL Contents]**: (Alleen USPS) Selecteer een van de volgende beschrijvingen van het pakket:<br/>- Cadeautje<br/>- Documenten<br/>- Handelsmonster<br/>- Terugkerende goederen<br/>- Merchandise<br/>- Overige <br/><br/>**[!UICONTROL Explanation]**: (Alleen USPS) Een gedetailleerde beschrijving van de inhoud van het pakket.<br/><br/>**[!UICONTROL Adult Required]**: De verzendende vervoerder verkrijgt de handtekening van een volwassen ontvanger en verstrekt de winkel een gedrukte kopie. |

{style="table-layout:auto"}

## Pakketten maken

De _[!UICONTROL Create Packages]_wordt weergegeven wanneer u ervoor kiest een verzendlabel te maken. U kunt direct beginnen het eerste pakket te vormen.

### Een pakket configureren

>[!NOTE]
>
>Als u de niet-standaardwaarde voor de optie [!UICONTROL Type] of kies ervoor een handtekeningbevestiging te vereisen, kan de prijs van een verzending afwijken van die welke u aan de klant in rekening brengt.

1. Als u een lijst met verscheepte producten wilt weergeven en toevoegen aan het pakket, klikt u op **[!UICONTROL Add Products]**.

   - Vermeld de producten en de hoeveelheden.

     De _[!UICONTROL Qty]_wordt de maximale hoeveelheid weergegeven die kan worden toegevoegd. Voor de eerste verpakking is het nummer de totale hoeveelheid van het te verzenden product.

   - Om de producten aan het pakket toe te voegen, klik **[!UICONTROL Add Selected Product(s) to Package]**.

1. Klik op **[!UICONTROL Add Package]**.

   U kunt meerdere pakketten toevoegen en tegelijkertijd bewerken.

1. Als u een pakket wilt verwijderen, klikt u op **[!UICONTROL Delete Package]**.

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

Nadat u alle producten hebt verdeeld, is het totale aantal pakketten dat u gaat gebruiken gelijk aan het nummer van het laatste pakket in de lijst. De _OK_ De knop is uitgeschakeld totdat alle verzonden items naar pakketten zijn gedistribueerd en alle benodigde informatie is voltooid.

Klik op **[!UICONTROL OK]**.

U kunt op **[!UICONTROL Cancel]** het proces indien nodig te beëindigen. De pakketten worden niet opgeslagen en het verzendlabel wordt geannuleerd.

### Veldomschrijvingen

| Veld | Beschrijving |
|--- |--- |
| [!UICONTROL Type] | Geeft het type pakket aan. Selecteer een van de vooraf gedefinieerde waarden. De beschikbare pakkettypen zijn verschillend voor elke verzender. Als het pop-upvenster Pakketten maken wordt geopend, wordt het standaardpakket voor de verzendende provider weergegeven in het veld Type. Als u een pakket selecteert dat niet door een verzendende vervoerder is ontworpen, moet u de afmetingen van het pakket invoeren. Voor verzendlabels die zijn gemaakt voor DHL-, FedEx- en UPS-verzendingen, wordt het veld Type goederen ingesteld op `Merchandise`. Voor USPS geeft het veld de waarde van de _Inhoud_ in het veld _[!UICONTROL Create Packages]_venster. |
| [!UICONTROL Total Weight] | Het totale gewicht van een verpakking. Het veld wordt voorgevuld met het totale gewicht van de producten in een verpakking. De meeteenheid kan worden ingesteld op kilogram of kilogram. |
| [!UICONTROL Length] | De lengte van een pakket, geheel getal en drijvende-kommagetallen. Het veld wordt ingeschakeld als het aangepaste pakkettype wordt gebruikt. De maateenheid kan worden ingesteld op inches of centimeters. |
| [!UICONTROL Width] | De breedte van een pakket, geheel getal en drijvende-kommagetallen. Het veld wordt ingeschakeld als het aangepaste pakkettype wordt gebruikt. U kunt de maateenheden opgeven in het vervolgkeuzemenu naast het veld Hoogte. U kunt deze eenheden selecteren tussen inches en centimeters. |
| [!UICONTROL Height] | De hoogte van een pakket, geheel getal en drijvende-kommagetallen. Het veld wordt ingeschakeld als het aangepaste pakkettype wordt gebruikt. U kunt de maateenheden opgeven in het vervolgkeuzemenu naast het veld Hoogte. U kunt deze eenheden selecteren tussen inches en centimeters. |
| [!UICONTROL Signature] | Definieert leveringsbevestiging. Opties:<br/><br/>**[!UICONTROL Not Required]**: Er is geen bevestigingsbrief voor de levering naar u verzonden.<br/><br/>**[!UICONTROL No Signature]**: Er wordt een bevestigingsbrief voor de levering verzonden zonder handtekening van de ontvanger.<br/><br/>**[!UICONTROL Signature Required]**: De verzendende vervoerder verkrijgt de handtekening van de ontvanger en geeft u de afgedrukte kopie ervan.<br/><br/>**[!UICONTROL Adult Required]**: De verzendende maatschappij verkrijgt de handtekening van de volwassen ontvanger en geeft u de afgedrukte kopie ervan.<br/><br/>**[!UICONTROL Direct (FedEx only)]**: FedEx verkrijgt een handtekening van iemand op het bezorgadres en maakt levering mogelijk als er niemand beschikbaar is om voor het pakket te ondertekenen.<br/><br/>**[!UICONTROL Indirect (FedEx only)]**: FedEx verkrijgt een handtekening op drie manieren:<br/>1) van iemand op het bezorgadres; <br/>(2) van een buur, bouwbeheerder of andere persoon op het adres; of <br/>(3) de ontvanger kan een ondertekende FedEx-deurtag verlaten waarmee het pakket kan worden vrijgegeven zonder dat er iemand aanwezig is. Alleen beschikbaar voor leveringen in woningen. De opties kunnen enigszins afwijken voor verschillende verzendmethoden. Raadpleeg voor de meest recente informatie de bronnen van de scheepvaartmaatschappij. |
| [!UICONTROL Contents] | (Alleen beschikbaar voor verzendingen naar USPS) Beschrijving van de inhoud van het pakket. Opties: `Gift` / `Documents` / `Commercial Sample` / `Returned Goods` / `Merchandise` / `Other` |
| [!UICONTROL Explanation] | (Alleen USPS-verzendingen) Gedetailleerde beschrijving van de pakketinhoud. |

{style="table-layout:auto"}

[1]: https://www.fedex.com/en-us/api/get-support.html
[2]: https://www.ups.com/us/en/support/contact-us.page
[3]: https://www.dhl.com/us-en/home/our-divisions/ecommerce-solutions.html
[4]: https://www.usps.com/business/web-tools-apis/#ssc
