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

Naarmate uw bedrijf groeit en verandert, [!DNL Inventory Management] ondersteunt uw behoeften. U kunt met gemak uitbreiden naar een merchant met meerdere bronnen of omlaag reduceren naar een koopman met één bron.

## Uitbreiden naar meerdere bronnen

Single-source-handelaren kunnen nieuwe winkels, opslagplaatsen, verlader en nog veel meer toevoegen. Voor uitbreiding zijn slechts enkele toevoegingen en voorraadupdates nodig om uit te breiden naar multi-sourcing:

1. Toevoegen [aangepaste bronnen](sources-add.md) voor elke nieuwe locatie.

   U gebruikt alleen de standaardbron voor bundelproducten.

1. Toevoegen [aangepaste voorraden](stocks-add.md) voor uw nieuwe bronnen.

   U kunt bijvoorbeeld bestanden maken per website, land, landinstelling of andere methode. U kunt bronnen toewijzen aan uw aangepaste bestanden. U gebruikt alleen de standaardvoorraad voor bundelproducten.

1. Bijwerken [brontoewijzingen en -hoeveelheden](quantities-manage.md) voor uw producten.

   U kunt ook de opdracht [Gereedschap Mengacties](bulk-assignment.md) en [Importeren en exporteren](inventory-import-export.md) om snel bronnen en productgegevens toe te voegen.

## Herstructureren naar één bron

Voor leveranciers met meerdere leveranciers die de onlineverkoop willen beperken tot één locatie voor verzending, wijzigt u de bronnen, voorraad en hoeveelheden die u wilt bijwerken:

1. Uitschakelen [aangepaste bronnen](sources-disable.md).

1. Breng de productvoorraad over naar de standaardbron.

   Het gebruik van massaacties wordt aanbevolen. Zie [Overdracht van voorraad naar bron](inventory-transfer.md).

1. Alle websites toewijzen aan de [Standaardvoorraad](stocks-manage.md).
