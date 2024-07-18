---
title: Commerce Admin Integration uitschakelen met Adobe ID
description: Volg deze optionele procedure om de integratie van Adobe Commerce Admin met Adobe IMS uit te schakelen.
exl-id: 0cd02b23-873e-4e65-ae1f-dbe4f7d0a476
feature: Identity Management
source-git-commit: 53c3b6c9fa9c152e6619528a43580b0acc71a2a5
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# Commerce Admin Integration uitschakelen met Adobe ID

{{ee-feature}}

Handelaars die hun Commerce-exemplaar hebben geïntegreerd met de Adobe IMS-verificatieworkflow, moeten deze optionele integratie mogelijk uitschakelen.

Commerce-implementaties herstellen de standaard Commerce-verificatieworkflow en het standaard-wachtwoordbeleid nadat de IMS-integratie is uitgeschakeld. Alleen de workflows van de beheerder-gebruiker worden beïnvloed wanneer deze integratie is in- of uitgeschakeld.

Zie [ Uw rekening Admin ](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html) voor een overzicht van Commerce binnen Admin.

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

* Commerce-beheergebruikers die geen bestaand Commerce-wachtwoord hebben of zijn vergeten, moeten een nieuw wachtwoord maken. Als u een nieuw wachtwoord wilt maken, kunnen beheerders met de functie [!UICONTROL Forgot your password?] op de Commerce-aanmeldingspagina een nieuw wachtwoord maken. Zie [ de klantenwachtwoorden van het Terugstellen ](https://experienceleague.adobe.com/docs/commerce-admin/customers/customer-accounts/configure/password-reset.html). Commerce accepteert geen leeg wachtwoordveld.

## Na het uitschakelen van de integratie

De standaard Commerce-verificatieworkflow wordt hervat nadat de IMS-integratie is uitgeschakeld en opnieuw om het wachtwoord wordt gevraagd.

Als u de IMS-integratie uitschakelt, worden de gegevens die zijn ingevoerd toen de integratie werd ingeschakeld (`Organization ID` , `Client ID` en `Client Secret` -waarden), verwijderd uit de Commerce-configuratiebestanden.
