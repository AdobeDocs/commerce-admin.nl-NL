---
title: Levensduur van klantensessie
description: Het leven van de klantenzitting bepaalt het leven van een klant het winkelen zitting.
exl-id: 7180631a-3233-40f3-92bf-b329fc260cf9
feature: Customers, Configuration, Security
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 1%

---

# Levensduur van klantensessie

Het leven van een klant het winkelen zitting wordt bepaald door verscheidene factoren, met inbegrip van de lengte van de serverzitting, het gebruik van een [hardnekkig winkelwagentje](../stores-purchase/cart-persistent.md)en de levensduur van de informatie die in de browser wordt opgeslagen. Hoewel deze met de zelfde klantenervaring verwant zijn, zijn zij afzonderlijke processen met verschillende vervalgebeurtenissen en levens.

| Proces | Beschrijving |
| --- | --- |
| Sessie | Informatie die op de server wordt opgeslagen, zoals de inhoud van het winkelwagentje. Als de serversessie verloopt voordat het cookie vervalt, kunnen klanten de inhoud van het winkelwagentje verliezen en het beveiligingsrisico verminderen. |
| Sessiecookie | Informatie die in browser als aantal of koord van karakters wordt opgeslagen. Als het sessiecookie vóór de serversessie verloopt, wordt de klant afgemeld. Het sessiecookie wordt verwijderd wanneer de klant het browservenster sluit. De levensduur van het cookie wordt standaard ingesteld op 3600 seconden of één uur. Als er tijdens die tijd geen toetsenbordactiviteit is, beëindigt de huidige zitting, en de klanten moeten zich terug in hun rekeningen registreren om verder te gaan winkelen. |

{style="table-layout:auto"}

Indien [Blijvend winkelwagen](../stores-purchase/cart-persistent.md) is ingeschakeld, wordt de inhoud van het winkelwagentje opgeslagen voor de volgende keer dat klanten zich aanmelden bij hun accounts. Wanneer u een blijvend winkelwagentje gebruikt, wordt u aangeraden de levensduur van de serversessie en het sessiecookie in te stellen op een lange periode.

Op de server wordt de lengte van de sessie bepaald door de `php.ini` bestand en diverse variabelen. Adobe Commerce heeft momenteel geen beheerconfiguratie-instelling die de lengte van de serversessie bepaalt.

## De levensduur van het cookie configureren

1. Op de _Beheerder_ zijbalk, ga naar [!UICONTROL **Winkels**] > _[!UICONTROL Settings]_>[!UICONTROL **Configuratie**].

1. Als u meerdere opslagruimten hebt, stelt u de **[!UICONTROL Store View]** kiest u in de rechterbovenhoek naar de winkel waar de configuratie van toepassing is.

1. In het linkerdeelvenster onder **[!UICONTROL General]**, kiest u **[!UICONTROL Web]**.

1. Vouw de sectie **[!UICONTROL Default Cookie Settings]** uit.

   ![Standaardcookie-instellingen](../configuration-reference/general/assets/web-default-cookie-settings.png){width="600" zoomable="yes"}

1. Als u de standaardinstelling wilt wijzigen, wist u de knop **[!UICONTROL Use system value]** Schakel het selectievakje in en voer de nieuwe waarde in seconden in.

1. Klik op **[!UICONTROL Save Config]**.

## Configureren _Mijn gegevens onthouden_ functionaliteit

Om aanmelding eenvoudiger te maken, **[!UICONTROL Remember Me]** Met deze functie kunnen gebruikers hun verificatiegegevens niet telkens invoeren wanneer ze de winkel binnenkomen. Om veiligheidsredenen is de functie voor persistentie standaard uitgeschakeld.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Customers]** en kiest u **[!UICONTROL Persistent Shopping Cart]**.

1. Vouw de sectie **[!UICONTROL General Options]** uit.

1. Voor **[!UICONTROL Enable Persistence]**, ingesteld op `Yes`. (Wis de **[!UICONTROL Use system value]** Schakel het selectievakje in om de standaardinstelling te wijzigen.)

1. Voor **[!UICONTROL Enable "Remember Me"]**, ingesteld op `Yes` of `No` volgens uw vereisten.

1. Klik op **[!UICONTROL Save Config]**.
