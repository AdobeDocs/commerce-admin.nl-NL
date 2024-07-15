---
title: Verwijzing naar kenmerken van klantgegevens
description: Gebruik deze verwijzing van de attributen van klantengegevens wanneer u met de invoer en de uitvoer van klantgegevens werkt.
exl-id: d22ebfed-f439-4a3f-b39e-e957b65c8c21
feature: Customers, Attributes
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---

# Verwijzing naar kenmerken van klantgegevens

De volgende lijsten maken een lijst van de attributen van een typische uitvoer van het de belangrijkste dossier van klanten en klantenadressen. De installatie die werd gebruikt om deze gegevens uit te voeren heeft twee websites en verscheidene opslagmeningen, met de geïnstalleerde steekproefgegevens.

Elk attribuut, of gebied, wordt vertegenwoordigd in het CSV- dossier als kolom, en klantenverslagen worden vertegenwoordigd door rijen. Kolommen die met een onderstrepingsteken beginnen, zijn service-entiteiten die eigenschappen of complexe gegevens bevatten.

## Hoofdbestand van klanten

| Kenmerk | Beschrijving |
|--- |--- |
| `email` | Het e-mailadres van de klant |
| `_website` |  |
| `_store` |  |
| `confirmation` | Bevestigingsmarkering. |
| `created_at` | De datum waarop de klantenaccount is gemaakt. |
| `created_in` | De winkelweergave waar het account is gemaakt. |
| `disable_auto_group_change` | Hiermee bepaalt u of klantgroepen dynamisch kunnen worden toegewezen tijdens de validatie van BTW-id. |
| `dob` | De geboortedatum van de klant. <br><br>**_Belangrijk:_**in overeenstemming met huidige veiligheid en privacy beste praktijken, herzie de opslag en de verwerking van de volledige geboortedatum van klanten (maand, dag, jaar). Wanneer verzameld met andere persoonlijke herkenningstekens (zoals_ volledige naam _), is het een potentieel wettelijk en veiligheidsrisico. We raden u aan om de volledige geboortedatum van klanten te beperken en in plaats daarvan het geboortejaar van de klant als alternatief te gebruiken. |
| `firstname` | De voornaam van de klant. |
| `gender` | The customer gender. |
| `group_id` | De id van de klantengroep waaraan de klant is toegewezen. |
| `lastname` | De achternaam van de klant. |
| `middlename` | De middelste naam of middelste startnaam van de klant. |
| `password_hash` | Wachtwoordhash |
| `prefix` | Elk voorvoegsel dat met de naam van de klant wordt gebruikt (zoals `Mr.` , `Ms.` , `Mrs.` en `Dr.` ). |
| `rp_token` | Wachtwoordtoken opnieuw instellen. |
| `rp_token_created_at` | Datum waarop het wachtwoord opnieuw is ingesteld. |
| `store_id` | WinkelID |
| `suffix` | Een achtervoegsel dat wordt gebruikt met de naam van de klant (zoals `Jr.` , `Sr.` en `Esquire` ). |
| `taxvat` |  |
| `website_id` | De website-id van de site waar de klantenaccount is gemaakt. |
| `password` | Het klantwachtwoord. |

{style="table-layout:auto"}

## Klantenadressen

| Kenmerk | Beschrijving |
|--- |--- |
| `_website` |  |
| `_email` |  |
| `_entity_id` |  |
| `city` | De plaats waar het klantenadres wordt gevestigd. |
| `company` | De bedrijfsnaam, indien van toepassing voor dit adres. |
| `country_id` | De land-id waar het klantadres zich bevindt. |
| `fax` | Het faxnummer van de klant, indien van toepassing. |
| `firstname` | De voornaam van de klant. |
| `lastname` | De achternaam van de klant. |
| `middlename` | De middelste naam of middelste startnaam van de klant. |
| `postcode` | De postcode of postcode waar het klantenadres wordt gevestigd. |
| `prefix` | Elk voorvoegsel dat met de naam van de klant wordt gebruikt (zoals `Mr.` , `Ms.` , `Mrs.` en `Dr.` ). |
| `region` | Het gebied waar het klantenadres wordt gevestigd. |
| `region_id` | Regio-id |
| `street` | Het adres van de klant. Een tweede regel van het adres van de straat is beschikbaar als gespecificeerd in de configuratie. |
| `suffix` | Indien gebruikt, het achtervoegsel dat aan de naam van de klant (zoals `Jr.`, `Sr.`, of `III`) wordt geassocieerd. |
| `telephone` | Het telefoonnummer van de klant dat aan het adres is gekoppeld. |
| `vat_id` | Het BTW-identificatienummer is een intern identificatienummer voor het BTW-nummer van de afnemer bij BTW-validatie. |
| `vat_is_valid` |  |
| `vat_request_date` |  |
| `vat_request_id` |  |
| `vat_request_success` |  |
| `_address_default_billing_` | Identificeert het standaardfactureringsadres. De waarde `1` geeft aan dat het adres het standaardfactuuradres van de klant is. Waarden: 1 / 0 |
| `_address_default_shipping_` | Identificeert het standaardverzendadres. De waarde `1` geeft aan dat het adres het standaardverzendadres van de klant is. Waarden: `1` / `0` |

{style="table-layout:auto"}
