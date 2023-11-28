---
title: PSD2-compatibiliteit
description: Meer informatie over de vereisten van de Richtlijn Betalingsdiensten (PSD2) die van invloed kunnen zijn op je winkel.
exl-id: efe94cac-a170-48df-88cf-36019ca52951
feature: Compliance
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '392'
ht-degree: 0%

---

# PSD2-compatibiliteit

Vanaf 14 september 2019 eist de Europese Unie dat alle handelaren in de EU en het Verenigd Koninkrijk de [Sterke verificatie voor klanten](https://www.cardinalcommerce.com/content-hub/mandates/psd2-sca/understanding-psd2-sca) (SCA) vereisten van de Richtlijn Betalingsdiensten (PSD2). Handelaren in alle andere landen worden aangemoedigd om als beste praktijk aan PSD 2 te voldoen.

>[!NOTE]
>
>Dit onderwerp is uitsluitend bedoeld voor informatieve doeleinden en mag niet worden opgevat als juridisch advies. Neem contact op met uw juridisch adviseur om te bepalen of en hoe uw bedrijf aan wettelijke verplichtingen moet voldoen.

De sterke Authentificatie van de Klant is een zeer belangrijk onderdeel van PSD2, en vereist twee van het volgende:

- Iets wat alleen de klant heeft (wachtwoord of pincode)
- Iets alleen de klant weet (uniek beveiligingstoken dat door telefoon of sleutelfob wordt gegenereerd)
- Alleen de klant heeft iets (biometrische verificatie, zoals vingerafdruk of gezichtsherkenning)

Europese banken kunnen betalingen die niet aan de vereisten voldoen, verlagen. Het is echter mogelijk dat transacties met een laag risico en transacties met een lage waarde nog steeds worden geaccepteerd, en latere betalingen in een terugkerend abonnement.

Vanwege deze belangrijke wijziging en om ervoor te zorgen dat de betalingen van klanten niet worden afgekeurd, heeft de Adobe de volgende wijzigingen aangebracht en aanbevelingen gedaan voor native [!DNL Commerce] integratie van betalingen.

| Betalingsmethode | Nalevingsvereisten |
|--- |--- |
| [PayPal](../stores-purchase/paypal.md) | Voor de meeste PayPal-oplossingen is geen actie vereist om aan PSD2 te voldoen, omdat de vereisten door PayPal worden afgehandeld. Zie de opmerking boven aan elk PayPal-onderwerp voor informatie over specifieke oplossingen. |
| [Braintree](../stores-purchase/braintree.md) | Vanaf de overgang naar de geïnstalleerde extensie in 2.4.0 worden de vereisten afgehandeld binnen de meegeleverde Braintree Betalingsmodule en is er geen actie vereist om te voldoen aan PSD 2. <br /><br />**_Opmerking:_**Voer een van de volgende handelingen uit om te voldoen aan PSD2 met behulp van de kernintegratie in vorige releases:<br/>- (Aanbevolen) Installeer de extensie voor de officiële integratie van Braintreeën vanaf [[!DNL Adobe Commerce Marketplace]](https://marketplace.magento.com/catalogsearch/result/?q=braintree#q=braintree&amp;idx=m2_cloud_prod_default_products&amp;p=0&amp;nR%5Bvisibility_search%5D%5B%3D%5D%5B0%5D=1){:target=&quot;_blank&quot;}.<br/>- De betalingsmethode voor Braintreeën in de [!DNL Commerce] configuratie.<br/><br/>Deze eerdere kernintegraties ondersteunen 3D Secure 2.0-verificatie. Implementaties van Braintreeën die worden uitgevoerd met JavaScript SDK v2 ondersteunen 3D Secure 2.0 echter niet. |
| Overige | Voor alle andere betalingsintegraties kunt u de beschikbare extensies controleren op [[!DNL Commerce Marketplace]](https://marketplace.magento.com/extensions/payments-security/payment-integration.html?_ga=2.108129217.2105547619.1564067043-238341041.1564067043){:target=&quot;_blank&quot;}. Vraag uw betalingsprovider om een oplossing voor het ondersteunen van PSD 2-vereisten aan te bevelen. |

{style="table-layout:auto"}
