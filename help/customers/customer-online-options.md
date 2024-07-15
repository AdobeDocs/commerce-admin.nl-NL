---
title: Levensduur van klantensessie
description: Het leven van de klantenzitting bepaalt het leven van een klant het winkelen zitting.
exl-id: 7180631a-3233-40f3-92bf-b329fc260cf9
feature: Customers, Configuration, Security
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 1%

---

# Levensduur van klantensessie

Het leven van een klant het winkelen zitting wordt bepaald door verscheidene factoren, met inbegrip van de lengte van de serverzitting, het gebruik van a [ blijvende kar ](../stores-purchase/cart-persistent.md), en het leven van informatie die in browser wordt opgeslagen. Hoewel deze met de zelfde klantenervaring verwant zijn, zijn zij afzonderlijke processen met verschillende vervalgebeurtenissen en levens.

| Proces | Beschrijving |
| --- | --- |
| Sessie | Informatie die op de server wordt opgeslagen, zoals de inhoud van het winkelwagentje. Als de serversessie verloopt voordat het cookie vervalt, kunnen klanten de inhoud van het winkelwagentje verliezen en het beveiligingsrisico verminderen. |
| Sessiecookie | Informatie die in browser als aantal of koord van karakters wordt opgeslagen. Als het sessiecookie vóór de serversessie verloopt, wordt de klant afgemeld. Het sessiecookie wordt verwijderd wanneer de klant het browservenster sluit. De levensduur van het cookie wordt standaard ingesteld op 3600 seconden of één uur. Als er tijdens die tijd geen toetsenbordactiviteit is, beëindigt de huidige zitting, en de klanten moeten zich terug in hun rekeningen registreren om verder te gaan winkelen. |

{style="table-layout:auto"}

Als [ het Aanhoudende Kart ](../stores-purchase/cart-persistent.md) wordt toegelaten, wordt de inhoud van het karretje bewaard voor de volgende tijd de klanten in hun rekeningen ondertekenen. Wanneer u een blijvend winkelwagentje gebruikt, wordt u aangeraden de levensduur van de serversessie en het sessiecookie in te stellen op een lange periode.

Op de server wordt de lengte van de sessie bepaald door het `php.ini` -bestand en diverse variabelen. Adobe Commerce heeft momenteel geen beheerconfiguratie-instelling die de lengte van de serversessie bepaalt.

## De levensduur van het cookie configureren

1. Op _Admin_ sidebar, ga naar [!UICONTROL **Opslag**] > _[!UICONTROL Settings]_>[!UICONTROL **Configuratie**].

1. Als u meerdere opslagruimten hebt, stelt u de **[!UICONTROL Store View]** -kiezer in de rechterbovenhoek in op de opslagplaats waar de configuratie van toepassing is.

1. Kies in het linkerdeelvenster onder **[!UICONTROL General]** de optie **[!UICONTROL Web]** .

1. Vouw de sectie **[!UICONTROL Default Cookie Settings]** uit.

   ![ Standaard de Montages van het Koekje ](../configuration-reference/general/assets/web-default-cookie-settings.png){width="600" zoomable="yes"}

1. Als u de standaardwaarde wilt wijzigen, schakelt u het selectievakje **[!UICONTROL Use system value]** uit en voert u de nieuwe waarde in seconden in.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.

## Vorm _me_ functionaliteit herinneren

Om het aanmelden gemakkelijker te maken, kan de functie **[!UICONTROL Remember Me]** voorkomen dat gebruikers hun referenties hoeven in te voeren telkens wanneer ze de winkel binnenkomen. Om veiligheidsredenen is de functie voor persistentie standaard uitgeschakeld.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Customers]** uit en kies **[!UICONTROL Persistent Shopping Cart]** .

1. Vouw de sectie **[!UICONTROL General Options]** uit.

1. Stel voor **[!UICONTROL Enable Persistence]** in op `Yes` . (Schakel het selectievakje **[!UICONTROL Use system value]** uit als u de standaardinstelling wilt wijzigen.)

1. Stel voor **[!UICONTROL Enable "Remember Me"]** de waarde in op `Yes` of `No` volgens uw vereisten.

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.
