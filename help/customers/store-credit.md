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

Nadat een bestelling is betaald en gefactureerd, kan de bestelling, of een deel ervan, worden terugbetaald door [creditnota uitgeven](../stores-purchase/credit-memo-create.md). Een creditnota verschilt van een terugbetaling omdat het bedrag van het krediet wordt teruggegeven aan de rekening van de klant waar het voor toekomstige aankopen kan worden gebruikt. Soms kan een terugbetaling tegelijk met de uitgifte van een creditnota worden gegeven en worden toegepast op het creditsaldo van de winkel van de klant. Het bedrag aan winkelkrediet dat beschikbaar is in de rekening van de klant wordt gespecificeerd in de configuratie.

>[!NOTE]
>
>De [_Afhandeling nul subtotaal_](../stores-purchase/zero-subtotal-checkout.md) betalingsmethode moet worden ingeschakeld in het geval dat het krediet het totale orderbedrag dekt.

## Kredietworkflow opslaan

1. **Aanmelden bij klant** - De klant registreert zich in rekening alvorens het controleproces te beginnen.

1. **Winkel gebruiken** - Krediet gedurende de looptijd [!UICONTROL _Reviseren en betalen_] stap van het uitcheckproces, selecteert de klant [!UICONTROL _Winkelkrediet gebruiken_] als betalingsoptie. De beschikbare balans wordt tussen haakjes weergegeven. Als het beschikbare saldo groter is dan het totaal-generaal, worden de andere betalingsmethoden niet meer weergegeven.

1. **Krediet dat op bestelling is toegepast** - Het bedrag van winkelkrediet dat op de orde wordt toegepast verschijnt met de ordertotalen, en wordt afgetrokken van het grote totaal.

1. **Klantenbalans aangepast** - Het beschikbare saldo van de klant wordt aangepast wanneer de bestelling wordt geplaatst.
