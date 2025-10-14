---
title: PayPal-afwikkelingsrapport
description: Meer informatie over het PayPal-afwikkelingsrapport als een hulpmiddel voor het beheer van PayPal-transacties.
exl-id: cd087e15-e6ad-4472-9038-8c64fde316f9
feature: Payments
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/nl/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: cd5b5ebec6e72ab4ba9de775bcfe8f8a89fbbb93
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# PayPal-afwikkelingsrapport

Het PayPal-afwikkelingsrapport geeft verkopers de informatie over elke transactie die de afwikkeling van fondsen beïnvloedt.

>[!NOTE]
>
>Voordat de beheerder van de winkel afwikkelingsrapporten kan genereren, moet hij of zij PayPal Merchant Technical Services vragen een SFTP-gebruikersaccount te maken, het genereren van afwikkelingsrapporten mogelijk te maken en SFTP in te schakelen in hun PayPal-zakelijke account.

Na het configureren en inschakelen van afwikkelingsrapporten op de PayPal Merchant-account, beginnen Adobe Commerce en Magento Open Source rapporten te genereren gedurende de volgende 24 uur. De lijst met beschikbare vereveningsrapporten kan worden bekeken door de beheerder.

**_om schikkingsrapporten te bekijken:_**

1. Voor _Admin_ sidebar, ga **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL PayPal Settlement]**.

   ![&#x200B; PayPal de Rapporten van de Afrekening &#x200B;](../getting-started/assets/reports-sales-paypal-settlement.png){width="600" zoomable="yes"}

1. Voor de meest recente updates klikt u op **[!UICONTROL Fetch Updates]** in de rechterbovenhoek.

   Het systeem maakt verbinding met de PayPal SFTP-server om de rapporten op te halen. Wanneer het proces is voltooid, verschijnt er een bericht met het aantal opgehaalde rapporten. Het rapport bevat voor elke transactie de volgende informatie:

   | Kolom Rapport | Beschrijving |
   | ------------ | ----------- |
   | [!UICONTROL PayPal Reference ID Type] | Één van de volgende verwijzingscodes:<br/> - Orde IDT <br/> - identiteitskaart van de Transactie <br/> - Abonnement identiteitskaart |
   | [!UICONTROL Preapproved Payment ID] | **[!UICONTROL Custom]** - De tekst die door de handelaar bij de transactie bij PayPal is ingevoerd.<br/>**[!UICONTROL Transaction Debit or Credit]**- De richting waarin het bruto bedrag wordt verplaatst.<br/>**[!UICONTROL Fee Debit or Credit]** - De richting waarin geld wordt verplaatst. |

   {style="table-layout:auto"}
