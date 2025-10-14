---
title: Commerce Admin Integration uitschakelen met Adobe ID
description: Volg deze optionele procedure om de integratie van Adobe Commerce Admin met Adobe IMS uit te schakelen.
exl-id: 0cd02b23-873e-4e65-ae1f-dbe4f7d0a476
feature: Identity Management
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/nl/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Commerce Admin Integration uitschakelen met Adobe ID

{{ee-feature}}

Handelaars die hun Commerce-exemplaar hebben geïntegreerd met de Adobe IMS-verificatieworkflow, moeten deze optionele integratie mogelijk uitschakelen.

Commerce-implementaties herstellen de standaard Commerce-verificatieworkflow en het standaard-wachtwoordbeleid nadat de IMS-integratie is uitgeschakeld. Alleen de workflows van de beheerder-gebruiker worden beïnvloed wanneer deze integratie is in- of uitgeschakeld.

Zie [&#x200B; Uw rekening Admin &#x200B;](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html?lang=nl-NL) voor een overzicht van Commerce binnen Admin.

## Stap 1: De integratie uitschakelen

U kunt deze integratie niet uitschakelen via de beheerder. Als u de integratie van Adobe IMS met Commerce wilt uitschakelen en de standaardstatus van Commerce-verificatie wilt herstellen, moet u de integratie uitschakelen via de opdrachtregelinterface.

De integratie uitschakelen:

```bash
bin/magento admin:adobe-ims:disable
```

Adobe Commerce geeft het volgende bericht weer wanneer het programma is geslaagd:

```
Admin Adobe IMS integration is disabled.
```

## Stap 2: Maak of haal uw Commerce-wachtwoord op

Nadat de integratie is uitgeschakeld, moeten de gebruikers van de beheerder een Commerce-wachtwoord gebruiken om zich aan te melden bij de beheerder.

* Commerce-beheerders die hun bestaande Commerce-wachtwoord onthouden (dat wil zeggen een Commerce-wachtwoord dat is gemaakt voordat de IMS-integratie is voltooid), kunnen dit gebruiken om u aan te melden bij de Admin.

* Commerce-beheergebruikers die geen bestaand Commerce-wachtwoord hebben of zijn vergeten, moeten een nieuw wachtwoord maken. Als u een nieuw wachtwoord wilt maken, kunnen beheerders met de functie [!UICONTROL Forgot your password?] op de Commerce-aanmeldingspagina een nieuw wachtwoord maken. Zie [&#x200B; de klantenwachtwoorden van het Terugstellen &#x200B;](https://experienceleague.adobe.com/docs/commerce-admin/customers/customer-accounts/configure/password-reset.html?lang=nl-NL). Commerce accepteert geen leeg wachtwoordveld.

## Na het uitschakelen van de integratie

De standaard Commerce-verificatieworkflow wordt hervat nadat de IMS-integratie is uitgeschakeld en opnieuw om het wachtwoord wordt gevraagd.

Als u de IMS-integratie uitschakelt, worden de gegevens die zijn ingevoerd toen de integratie werd ingeschakeld (`Organization ID` , `Client ID` en `Client Secret` -waarden), verwijderd uit de Commerce-configuratiebestanden.
