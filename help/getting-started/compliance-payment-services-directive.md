---
title: PSD2-compatibiliteit
description: Meer informatie over de vereisten van de Richtlijn Betalingsdiensten (PSD2) die van invloed kunnen zijn op je winkel.
exl-id: efe94cac-a170-48df-88cf-36019ca52951
feature: Compliance
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# PSD2-compatibiliteit

Vanaf 14 september 2019 vereist de Europese Unie dat alle handelaren in de EU en het Verenigd Koninkrijk voldoen aan de [&#x200B; Strong Customer Authentication &#x200B;](https://www.cardinalcommerce.com/content-hub/mandates/psd2-sca/understanding-psd2-sca) (SCA) vereisten van de Richtlijn Betalingsdiensten (PSD2). Handelaren in alle andere landen worden aangemoedigd om als beste praktijk aan PSD 2 te voldoen.

>[!NOTE]
>
>Dit onderwerp is uitsluitend bedoeld voor informatieve doeleinden en mag niet worden opgevat als juridisch advies. Neem contact op met uw juridisch adviseur om te bepalen of en hoe uw bedrijf aan wettelijke verplichtingen moet voldoen.

De sterke Authentificatie van de Klant is een zeer belangrijk onderdeel van PSD2, en vereist twee van het volgende:

- Iets wat alleen de klant heeft (wachtwoord of pincode)
- Iets alleen de klant weet (uniek beveiligingstoken dat door telefoon of sleutelfob wordt gegenereerd)
- Alleen de klant heeft iets (biometrische verificatie, zoals vingerafdruk of gezichtsherkenning)

Europese banken kunnen betalingen die niet aan de vereisten voldoen, verlagen. Het is echter mogelijk dat transacties met een laag risico en transacties met een lage waarde nog steeds worden geaccepteerd, en latere betalingen in een terugkerend abonnement.

Vanwege deze belangrijke wijziging en om ervoor te zorgen dat klantbetalingen niet worden afgekeurd, heeft Adobe de volgende wijzigingen aangebracht en aanbevelingen gedaan voor geïntegreerde [!DNL Commerce] betalingen.

| Betalingsmethode | Nalevingsvereisten |
|--- |--- |
| [&#x200B; PayPal &#x200B;](../stores-purchase/paypal.md) | Voor de meeste PayPal-oplossingen is geen actie vereist om aan PSD2 te voldoen, omdat de vereisten door PayPal worden afgehandeld. Zie de opmerking boven aan elk PayPal-onderwerp voor informatie over specifieke oplossingen. |
| [&#x200B; Braintree &#x200B;](../stores-purchase/braintree.md) | Vanaf de overgang naar de geïnstalleerde extensie in 2.4.0 worden de vereisten afgehandeld binnen de meegeleverde Braintree Betalingsmodule en is er geen actie vereist om te voldoen aan PSD 2. <br /><br />**_Nota:_**&#x200B;om aan PSD2 te voldoen die de kernintegratie in vorige versies gebruiken, doe één van het volgende:<br/> - (Geadviseerd) installeer de officiële de integratieuitbreiding van de Braintree van [[!DNL Adobe Commerce Marketplace] &#x200B;](https://marketplace.magento.com/catalogsearch/result/?q=braintree#q=braintree&idx=m2_cloud_prod_default_products&p=0&nR%5Bvisibility_search%5D%5B%3D%5D%5B0%5D=1) {:target= &quot;_blank&quot;}.<br/> - Schakel de betalingsmethode voor Braintreeën in en configureer deze in de [!DNL Commerce] -configuratie.<br/><br/> deze vroegere kernintegratie steunt 3D Veilige 2.0 controle. Braintree-implementaties die worden uitgevoerd op JavaScript SDK v2 ondersteunen 3D Secure 2.0 echter niet. |
| Overige | Voor alle andere betalingsintegraties, controleer de beschikbare uitbreidingen op [[!DNL Commerce Marketplace] &#x200B;](https://marketplace.magento.com/extensions/payments-security/payment-integration.html?_ga=2.108129217.2105547619.1564067043-238341041.1564067043){:target=&quot;_blank&quot;}. Vraag uw betalingsprovider om een oplossing voor het ondersteunen van PSD 2-vereisten aan te bevelen. |

{style="table-layout:auto"}
