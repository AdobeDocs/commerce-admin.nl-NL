---
title: Schakel de Admin-integratie van Commerce met Adobe ID uit
description: Volg deze optionele procedure om de integratie van Adobe Commerce Admin met Adobe IMS uit te schakelen.
exl-id: 0cd02b23-873e-4e65-ae1f-dbe4f7d0a476
feature: Identity Management
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---

# Schakel de Admin-integratie van Commerce met Adobe ID uit

{{ee-feature}}

Handelaars die hun instantie Commerce hebben geïntegreerd met de Adobe IMS-verificatieworkflow moeten deze optionele integratie mogelijk uitschakelen.

De plaatsingen van de handel keren aan het standaard de authentificatiewerkschema en wachtwoordbeleid van de Handel terug nadat de integratie IMS wordt onbruikbaar gemaakt. Alleen de workflows van de beheerder-gebruiker worden beïnvloed wanneer deze integratie is in- of uitgeschakeld.

Zie [Uw beheerdersaccount](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html) voor een overzicht van het aanmelden bij Commerce Admin.

## Stap 1: De integratie uitschakelen

U kunt deze integratie niet uitschakelen via de beheerder. Als u de integratie van Adobe IMS met Commerce wilt uitschakelen en de verificatie van Commerce wilt terugzetten naar de standaardstatus, moet u de integratie uitschakelen via de opdrachtregelinterface.

De integratie uitschakelen:

```bash
bin/magento admin:adobe-ims:disable
```

Adobe Commerce geeft het volgende bericht weer wanneer het programma is geslaagd:

```terminal
Admin Adobe IMS integration is disabled.
```

## Stap 2: Creeer of wint uw wachtwoord van de Handel terug

Na het onbruikbaar maken van de integratie, moeten de admin gebruikers een wachtwoord van de Handel gebruiken om aan login aan Admin. te gebruiken.

* Admin van de handel gebruikers die hun reeds bestaand wachtwoord van de Handel herinneren (namelijk een wachtwoord van de Handel dat vóór de integratie IMS) werd gecreeerd kan het gebruiken om aan binnen aan Admin te registreren.

* Admin-gebruikers van Commerce die geen bestaand wachtwoord voor Handel hebben of zijn vergeten, moeten een nieuw wachtwoord maken. Beheerders kunnen de opdracht [!UICONTROL Forgot your password?] op de aanmeldingspagina van de Handel om een nieuw wachtwoord te maken. Zie [Wachtwoorden van klanten opnieuw instellen](https://experienceleague.adobe.com/docs/commerce-admin/customers/customer-accounts/configure/password-reset.html). De handel zal geen leeg wachtwoordgebied goedkeuren.

## Na het uitschakelen van de integratie

De standaardverificatieworkflow voor handel wordt hervat nadat de IMS-integratie is uitgeschakeld en de beheergebruikers opnieuw om hun wachtwoord wordt gevraagd.

Als u de IMS-integratie uitschakelt, worden de gegevens verwijderd die waren ingevoerd toen de integratie was ingeschakeld (`Organization ID`, `Client ID`, en `Client Secret` waarden) uit de configuratiebestanden van Commerce.
