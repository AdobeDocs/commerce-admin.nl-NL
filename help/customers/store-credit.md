---
title: Winkelkrediet
description: Winkelkrediet is een bedrag dat wordt teruggezet naar een klantenrekening en kan worden gebruikt voor aankopen of voor terugbetalingen.
exl-id: 1fe627dd-5c49-4ff8-85e0-3c987285726d
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---

# Winkelkrediet

{{ee-feature}}

Winkelkrediet is een bedrag dat wordt teruggezet naar een klantenaccount. Klanten kunnen hun winkelkrediet gebruiken om aankopen te betalen en beheerders kunnen krediet opslaan voor terugbetalingen in contanten. Cadeaucreditcardsaldi kunnen op de rekening van de klant worden gecrediteerd, in plaats van de code van de cadeaukaart voor toekomstige aankopen te gebruiken.

Nadat een orde wordt betaald en gefactureerd, kan de orde, of een gedeelte van het, worden terugbetaald door [ het uitgeven van een creditnota ](../stores-purchase/credit-memo-create.md). Een creditnota verschilt van een terugbetaling omdat het bedrag van het krediet wordt teruggegeven aan de rekening van de klant waar het voor toekomstige aankopen kan worden gebruikt. Soms kan een terugbetaling tegelijk met de uitgifte van een creditnota worden gegeven en worden toegepast op het creditsaldo van de winkel van de klant. Het bedrag aan winkelkrediet dat beschikbaar is in de rekening van de klant wordt gespecificeerd in de configuratie.

>[!NOTE]
>
>De [_Nul SubtotalCheckout_](../stores-purchase/zero-subtotal-checkout.md) betalingsmethode moet worden toegelaten in het geval dat de opslagkredieten het ordertotaal behandelen.

## Kredietworkflow opslaan

1. **login van de Klant** - de Logboeken van de Klant in rekening alvorens met het controleproces te beginnen.

1. **Opslag van het Gebruik** - Krediet tijdens de [!UICONTROL _Controle &amp; de stap van Betalingen_] van het controleproces, selecteert de klant [!UICONTROL _Krediet van de Opslag van het Gebruik_] als betalingsoptie. De beschikbare balans wordt tussen haakjes weergegeven. Als het beschikbare saldo groter is dan het totaal-generaal, worden de andere betalingsmethoden niet meer weergegeven.

1. **Krediet dat op orde** wordt toegepast - de hoeveelheid opslagkrediet dat op de orde wordt toegepast verschijnt met de ordetotalen, en van het grote totaal afgetrokken.

1. **Correcte het saldo van de Klant** - het beschikbare saldo van de Klant wordt aangepast wanneer de orde wordt geplaatst.
