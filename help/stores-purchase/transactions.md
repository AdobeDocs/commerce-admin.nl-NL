---
title: Transacties
description: Meer informatie over de pagina Transacties en hoe je de activiteiten tussen je winkel en een betalingssysteem kunt volgen.
exl-id: 5970db88-146d-4caf-aab4-d9315357a4fe
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---

# Transacties

De _pagina van Transacties_ maakt een lijst van alle betalingsactiviteit die tussen uw opslag en een betalingssysteem heeft plaatsgevonden, en verleent toegang tot meer gedetailleerde informatie.

## Transacties weergeven

Voor _Admin_ sidebar, ga **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Transactions]**.

![&#x200B; het net van Transacties &#x200B;](./assets/transactions.png){width="600" zoomable="yes"}

| Kolom | Beschrijving |
|--- |--- |
| [!UICONTROL ID] | Een unieke numerieke id die aan elke transactie is toegewezen. |
| [!UICONTROL Order ID] | Een unieke id die wordt toegewezen wanneer een klant een bestelling plaatst. |
| [!UICONTROL Transaction ID] | Een unieke numerieke id die wordt toegewezen wanneer een transactie plaatsvindt nadat een klant een order heeft geplaatst. |
| [!UICONTROL Parent Transaction ID] | Het id-nummer van de bovenliggende transactie. |
| [!UICONTROL Payment Method] | De betalingsmethode die aan een transactie is gekoppeld. |
| [!UICONTROL Transaction Type] | Type transactie, dat kan zijn: Order, Authorization, Capture, Void of Refund. |
| [!UICONTROL Closed] | Of een transactie gesloten is of niet. |
| [!UICONTROL Created] | Tijd en datum waarop de transactie is gemaakt. |

{style="table-layout:auto"}

## Transactiegegevens weergeven

Klik op het item dat u wilt weergeven.

Op de pagina met transactiedetails kunt u de transactiedetails en het raster van onderliggende transacties zien.

### Transactiegegevens

Deze sectie omvat informatie betreffende de transactie, en verstrekt een verbinding aan de ordepagina in de **identiteitskaart van de Orde** kolom.

| Kolom | Beschrijving |
|--- |--- |
| [!UICONTROL Transaction ID] | Het transactie-id-nummer. |
| [!UICONTROL Parent Transaction ID] | Een corresponderend identificatienummer van de moedertransactie, indien van toepassing. |
| [!UICONTROL Transaction Type] | Type transactie, dat kan zijn: Order, Authorization, Capture, Void of Refund. |
| [!UICONTROL Is Closed] | Of een transactie gesloten is of niet. |
| [!UICONTROL Created At] | Tijd en datum waarop de transactie is gemaakt. |

{style="table-layout:auto"}

### Onderliggende transacties

De transacties van het kind worden getoond in het net na het creëren van facturen voor [&#x200B; orden &#x200B;](orders.md). Met deze indeling kunt u de transactiegeschiedenis bijhouden aan de hand van een transactiehiërarchie.

### [!UICONTROL Transaction Details]

Deze sectie bevat de aanvullende informatie voor een bepaalde transactie. De informatie wordt weergegeven in de vorm van toetsen en waarden. De beschikbare toetsen zijn:

- authAmount
- authCode
- aVSResponse
- billTo
- cardCodeResponse
- klant
- customerIP
- lineItems
- marketType
- bestellen
- betaling
- product
- terugkerendeFacturering
- responseCode
- responseReasonCode
- responseReasonDescription
- resolveAmount
- oplossing
- submitTimeLocal
- submitTimeUTC
- taxVrijgesteld
- transactionStatus

>[!NOTE]
>
>Als de transactiedetails niet beschikbaar of verouderd zijn, klik **[!UICONTROL Fetch]** in de knoopbar om hen bij te werken.
