---
title: Adobe Commerce B2B-wijzigingen die niet compatibel zijn met oudere versies
description: Meer informatie over de wijzigingen in de Adobe Commerce B2B-releases waardoor u mogelijk uw aangepaste code moet bijwerken.
exl-id: 79b66843-3f34-4fe9-9670-53d19b749eb4
source-git-commit: 29663b8a88abc581b9543621ddb475f7d7903027
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# Adobe Commerce B2B-wijzigingen die niet compatibel zijn met oudere versies

Bekijk de informatie op hoog niveau voor alle achterwaarts incompatibele wijzigingen in B2B voor Adobe Commerce-releases. Zie de sectie met hooglichten voor incompatibele wijzigingen die een grote impact hebben en die gedetailleerde uitleg en speciale instructies vereisen.

## Hooglichten

### 1.4.2 t/m 1.5.0

Door de toevoeging van de toewijzing van meerdere bedrijven kunnen bedrijfsgebruikersaccounts nu meerdere `company_id` waarden hebben. `Magento\Company\Api\Data\CompanyCustomerInterface` is bijgewerkt om de standaardwaarde `company_id` voor een gebruiker in te stellen. Het gebrek wordt geplaatst aan het eerste bedrijf dat aan de rekening van de bedrijfgebruiker wordt toegewezen.

Als u een upgrade uitvoert vanaf een eerdere versie, raadt Adobe u aan de volgende methoden te implementeren in klassen die de instructie `Magento\Company\Api\Data\CompanyCustomerInterface` gebruiken.

- Magento\Company\Api\Data\CompanyCustomerInterface:getIsDefault
- Magento\Company\Api\Data\CompanyCustomerInterface::setIsDefault

## Referentie

{{$include /help/_includes/backward-incompatible-changes/1.4.2-1.5.0.md}}

{{$include /help/_includes/backward-incompatible-changes/1.4.1-1.4.2.md}}

{{$include /help/_includes/backward-incompatible-changes/1.4.0-1.4.1.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.5-1.4.0.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.4-1.3.5.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.3-1.3.4.md}}
