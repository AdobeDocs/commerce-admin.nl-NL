---
title: Inventarisatie uitbreiden en herstructureren
description: Leer hoe u kunt uitbreiden naar een multi-source-winkel of de handel kunt terugbrengen naar een single-source-winkel.
exl-id: 880474e3-6533-4b2f-adf7-4312787ff736
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---

# Inventarisatie uitbreiden en herstructureren

Naarmate uw bedrijf groeit en verandert, biedt [!DNL Inventory Management] ondersteuning voor uw behoeften. U kunt met gemak uitbreiden naar een merchant met meerdere bronnen of omlaag reduceren naar een koopman met één bron.

## Uitbreiden naar meerdere bronnen

Single-source-handelaren kunnen nieuwe winkels, opslagplaatsen, verlader en nog veel meer toevoegen. Voor uitbreiding zijn slechts enkele toevoegingen en voorraadupdates nodig om uit te breiden naar multi-sourcing:

1. Voeg [ douanebronnen ](sources-add.md) voor elke nieuwe plaats toe.

   U gebruikt alleen de standaard-Source voor bundelproducten.

1. Voeg [ douanevoorraden ](stocks-add.md) toe zoals nodig voor uw nieuwe bronnen.

   U kunt bijvoorbeeld bestanden maken per website, land, landinstelling of andere methode. U kunt bronnen toewijzen aan uw aangepaste bestanden. U gebruikt alleen de standaardvoorraad voor bundelproducten.

1. Werk [ brontaken en hoeveelheden ](quantities-manage.md) voor uw producten bij.

   U kunt het [ Hulpmiddel van de Acties van de Massa ](bulk-assignment.md) en [ invoer-Uitvoer ](inventory-import-export.md) eigenschap ook gebruiken om bronnen en productgegevens snel toe te voegen.

## Herstructureren naar één bron

Voor leveranciers met meerdere leveranciers die de onlineverkoop willen beperken tot één locatie voor verzending, wijzigt u de bronnen, voorraad en hoeveelheden die u wilt bijwerken:

1. Maak [ douanebronnen ](sources-disable.md) onbruikbaar.

1. Breng de productvoorraad over naar uw standaard Source.

   Het gebruik van massaacties wordt aanbevolen. Zie [ Overbrengend Overzicht aan Source ](inventory-transfer.md).

1. Wijs alle websites aan de [ StandaardVoorraad ](stocks-manage.md) toe.
