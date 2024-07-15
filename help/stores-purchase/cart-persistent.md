---
title: persistentie van winkelwagentjes
description: Leer hoe een hardnekkig winkelwagentje niet-aangeschafte winkelartikelen bijhoudt en de informatie voor het volgende bezoek van de klant opslaat.
exl-id: 95c336b3-77ac-4cf6-8fb5-23f4ac4b67d6
feature: Shopping Cart, Configuration
source-git-commit: 26d4bb35c6e1878a8ea8c5f05a982559e5d6dc35
workflow-type: tm+mt
source-wordcount: '1475'
ht-degree: 0%

---

# persistentie van winkelwagentjes

Een hardnekkig winkelwagentje volgt niet-aangeschafte artikelen die in het winkelwagentje blijven staan en slaat de informatie op voor het volgende bezoek van de klant. De klanten die _worden herinnerd_ kunnen de inhoud van hun winkelwagentjes hebben worden hersteld de volgende tijd zij uw opslag bezoeken.

Een hardnekkig winkelwagentje kan helpen het aantal verlaten winkelwagentjes te verminderen en de verkoop te verhogen. Het is belangrijk te begrijpen dat het hardnekkige winkelwagentje op geen enkel moment gevoelige accountinformatie blootstelt. Terwijl het hardnekkige winkelwagentje in gebruik is, moeten zowel geregistreerde klanten als gastklanten zich aanmelden bij een bestaande account of een account maken voordat ze de afhandeling kunnen uitvoeren. Voor gastkopers is een hardnekkig winkelwagentje de enige manier om informatie van een vorige sessie op te halen.

Om het gebruik van kartpersistentie voor uw plaats of binnen specifieke archiefmeningen te beheren, kunt u [ blijvende het winkelen kar ](#configure-a-persistent-cart) montages vormen. Voor meer informatie over hoe deze montages de verkoopervaring in uw winkelfront beïnvloeden, zie [ het Blijvende werkschema van het karretje ](#persistent-cart-workflow).

>[!NOTE]
>
>Wanneer u een blijvend winkelwagentje gebruikt, wordt u aangeraden de levensduur van de serversessie en het sessiecookie in te stellen op een lange periode. Zie [ Levensduur van de Zitting ](../customers/customer-online-options.md) voor meer informatie.

Als u het hardnekkige winkelwagentje wilt gebruiken, moet de browser van de klant zo zijn ingesteld dat cookies zijn toegestaan. Er worden twee soorten cookies gebruikt voor winkelwagentjes:

- **koekje van de Zitting** - een kortetermijnzittingskoekje bestaat tijdens één enkel bezoek aan uw plaats, en verloopt wanneer de klant, of na een vastgestelde tijdspanne verlaat.

- **Persistent Koekje** - een langdurige, blijvende koekje blijft bestaan na het eind van de zitting en bewaart een verslag van het het winkelwagentje van de klant voor toekomstige verwijzing.

## Blijvende workflow voor winkelwagentjes

Wanneer het blijvende het winkelwagentje [ ](#configure-a-persistent-cart) wordt toegelaten, hangt het werkschema van af:

- De waarden van _toelaten herinneren me_ en _Duidelijke Persistence op Logout_ montages
- Het besluit van de klant om _te selecteren of te ontruimen herinner me_ checkbox
- Wanneer de permanente cookie wordt gewist

Wanneer een permanente cookie wordt toegepast, wordt een koppeling `Not Jane Smith?` weergegeven in de paginakoptekst. Deze herinnering geeft de klant de capaciteit om de blijvende zitting te eindigen en beginnen werkend als gast, of aan login als verschillende klant. Het systeem houdt een register bij van de inhoud van het winkelwagentje, zelfs als de klant later andere apparaten gebruikt om in uw winkel te winkelen. Een klant kan bijvoorbeeld een item vanaf een laptop aan het winkelwagentje toevoegen, meer items van een mobiel apparaat toevoegen en het afrekenproces vanaf een tablet voltooien.

Er is een afzonderlijke, onafhankelijke, permanente cookie voor elke browser. Als de klant meerdere browsers gebruikt tijdens het bezoeken van uw winkel tijdens één permanente sessie, worden de wijzigingen die in de ene browser zijn aangebracht, doorgevoerd in elke andere browser nadat de pagina is vernieuwd. Terwijl de persistente winkelwagentje is ingeschakeld, maakt en onderhoudt uw winkel een aparte, permanente cookie voor elke browser die door een klant wordt gebruikt om zich aan te melden of een account te maken.

### Voorbeeld: een open sessie op een gedeelde computer

Jane voltooit haar vakantiewinkelen met een blijvende sessie. Ze voegt een cadeautje voor John toe aan haar kar en iets voor haar moeder. Dan gaat ze naar de keuken voor een snack.

John zit op de computer om snel te winkelen terwijl Jane in de keuken is. Zonder de koppeling `Not Jane Smith?` boven aan de pagina te zien, vindt hij een leuk cadeau voor Jane en voegt hij deze toe aan de wagen. Als hij uitcheckt en zich aanmeldt als zichzelf, worden beide items in Jane&#39;s winkelwagen aan zijn winkelwagen toegevoegd. John is in zulk een haast dat hij niet de extra punten tijdens _Overzicht van de Orde_ opmerkt, en legt de orde voor. Jane&#39;s winkelwagen is nu leeg en John heeft alle geschenken gekocht.

### Mijn gegevens onthouden

De klanten kunnen _selecteren me_ checkbox op de login pagina herinneren om de inhoud van hun winkelwagentjes te bewaren.

| Herinner me? | Resultaat |
| ------------ |  ------ |
| Geselecteerd | Maakt een permanente cookie en slaat de inhoud van het winkelwagentje op voor de volgende aangemelde sessie van de klant. |
| Niet geselecteerd | Er wordt geen permanente cookie gemaakt en de winkelwagengegevens worden niet opgeslagen voor de volgende aangemelde sessie van de klant. |

{style="table-layout:auto"}

### Doorgaan met persistentie bij afmelden - nee

| Handeling | Resultaat |
| ------ | ------ |
| Aanmelden bij klant | Roept de permanente cookie aan naast de sessiecookie die al in gebruik is. |
| Klant meldt zich af | Verwijdert de sessiecookie maar de permanente cookie blijft van kracht. De volgende keer dat de klant zich aanmeldt, worden de winkelwagentjes weer hersteld of worden ze toegevoegd aan nieuwe items die in het winkelwagentje zijn geplaatst. |
| De klant meldt zich niet af en het sessiecookie verloopt | De permanente cookie blijft van kracht. |

{style="table-layout:auto"}

### Doorhaling van afmelding wissen

| Handeling | Resultaat |
| ------ | ------ |
| Aanmelden bij klant | Roept de permanente cookie aan naast de sessiecookie die al in gebruik is. |
| Klant meldt zich af | Hiermee verwijdert u beide cookies. |
| De klant meldt zich niet uit maar het sessiecookie verloopt | De permanente cookie blijft van kracht. |

{style="table-layout:auto"}

## Blijvende tekeninstellingen en effecten

| Instellingen | Effect |
|----------|--------|
| **[!UICONTROL Enable Remember Me]** wordt ingesteld op `No` .<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**heeft een willekeurige waarde.<br/><br/>** herinner me **checkbox niet beschikbaar op login en registratiepagina. | De permanente cookie wordt niet gebruikt. |
| **[!UICONTROL Enable Remember Me]** wordt ingesteld op `Yes` .<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**heeft een willekeurige waarde.<br/><br/>** herinner me **niet wordt geselecteerd. | De sessiecookie wordt op de gebruikelijke manier toegepast; de permanente cookie wordt niet gebruikt. |
| **[!UICONTROL Enable Remember Me]** wordt ingesteld op `Yes` .<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**wordt ingesteld op `Yes` .<br/><br/>** herinner me **wordt geplaatst aan `Yes`. | Wanneer een klant zich aanmeldt, worden beide cookies toegepast. Wanneer een klant zich afmeldt, worden beide cookies verwijderd. Als een klant zich niet aanmeldt maar het sessiecookie verloopt, wordt de permanente cookie nog steeds gebruikt. Naast het afmelden wordt de permanente cookie verwijderd wanneer de levensduur van de cookie is verstreken of wanneer de klant op de koppeling `Not Jane Smith` klikt. |
| **[!UICONTROL Enable Remember Me]** wordt ingesteld op `Yes` .<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**wordt ingesteld op `No` .<br/><br/>** herinner me **wordt geplaatst aan `Yes` | Wanneer een klant zich aanmeldt, worden beide cookies toegepast. Wanneer een klant zich afmeldt, wordt het sessiecookie verwijderd, wordt de permanente sessie voortgezet. De permanente cookie wordt verwijderd wanneer de levensduur van de cookie is verstreken of wanneer de klant op de koppeling `Not Jane Smith` klikt. |

{style="table-layout:auto"}

## Een blijvende poort configureren

Tijdens de opstelling van een blijvend winkelwagentje, kunt u de levensduur van de koekjes specificeren, en welke opties u voor diverse klantenactiviteiten ter beschikking wilt stellen.

Voor meer informatie over hoe het klantenwerkschema door deze montages wordt bepaald, zie [ het Blijvende werkschema van het winkelwagentje ](#persistent-cart-workflow).

>[!NOTE]
>
>Als het sessiecookie verloopt terwijl de klant is aangemeld, blijft de permanente cookie actief.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Customers]** uit en kies **[!UICONTROL Persistent Shopping Cart]** .

1. Stel **[!UICONTROL Enable Persistence]** in op `Yes` als u het permanente winkelwagentje wilt inschakelen en extra opties wilt weergeven.

   ![ toelatend en vormend de klokpersistentie ](../configuration-reference/customers/assets/persistent-shopping-cart-general.png){width="600" zoomable="yes"}

   Voor meer informatie over elk van deze configuratiemontages, zie de [_Verwijzing van de Configuratie_](../configuration-reference/customers/persistent-shopping-cart.md)

   >[!NOTE]
   >
   >Schakel indien nodig het selectievakje **[!UICONTROL Use system value]** uit om deze instellingen te wijzigen.

1. Voer voor **[!UICONTROL Persistence Lifetime (seconds)]** de tijdsduur in seconden in waarin de permanente cookie moet duren.

   De standaardwaarde van 31.536.000 seconden is gelijk aan één jaar. De maximaal toegestane tijd is 100 jaar.

1. Stel **[!UICONTROL Enable "Remember Me"]** in op een van de volgende opties:

   - `Yes` - Toont _me_ checkbox op de Login pagina van uw opslag herinnert, zodat de klanten kunnen verkiezen om hun het winkelwagentinformatie te bewaren.

   - `No` - Persistentie kan nog steeds worden ingeschakeld, maar klanten krijgen niet de optie om te kiezen of ze hun gegevens willen opslaan.

1. Om _vooraf te selecteren herinner me_ checkbox voor de klant, plaats **[!UICONTROL Remember Me Default Value]** aan `Yes`.

   De klant kan deze optie desgewenst wissen.

1. Stel **[!UICONTROL Clear Persistence on Log Out]** in op een van de volgende opties:

   - `Yes` - Het winkelwagentje wordt gewist wanneer een geregistreerde klant zich afmeldt.

   - `No` - Het winkelwagentje wordt opgeslagen wanneer een geregistreerde klant zich afmeldt.

   >[!NOTE]
   >
   >Als het sessiecookie verloopt terwijl de klant nog steeds is aangemeld, blijft de permanente cookie in gebruik.

1. Stel **[!UICONTROL Persist Shopping Cart]** in op een van de volgende opties:

   - `Yes` - Als het sessiecookie verloopt, blijft de permanente cookie behouden. Als een gast later zich aanmeldt of een account maakt, wordt het winkelwagentje hersteld.

   - `No` - Het winkelwagentje blijft niet behouden voor gasten nadat het sessiecookie is verlopen.

1. ![ Adobe Commerce ](../assets/adobe-logo.svg) (Adobe Commerce slechts) Reeks **[!UICONTROL Persist Wish List]** om te bepalen als de staat van klant wenst lijsten wordt behouden wanneer de zitting beëindigt:

   - `Yes` - De inhoud van de wensenlijst wordt opgeslagen wanneer de sessie wordt beëindigd.

   - `No` - De lijst met wensen wordt niet opgeslagen wanneer de sessie wordt beëindigd.

1. ![ Adobe Commerce ](../assets/adobe-logo.svg) (Adobe Commerce slechts) Reeks **[!UICONTROL Persist Recently Ordered Items]** om te bepalen als de staat van onlangs bevolen punten wordt behouden wanneer de zitting beëindigt:

   - `Yes` - De status van recent bestelde items wordt opgeslagen wanneer de sessie wordt beëindigd.

   - `No` - De status van recent bestelde items wordt niet opgeslagen wanneer de sessie wordt beëindigd.

1. Stel **[!UICONTROL Persist Currently Compared Products]** in op `Yes` of `No` .

1. Stel **[!UICONTROL Persist Comparison History]** in op `Yes` of `No` .

1. Stel **[!UICONTROL Persist Recently Viewed Products]** in op `Yes` of `No` .

1. ![ Adobe Commerce ](../assets/adobe-logo.svg) (Adobe Commerce slechts) Reeks **[!UICONTROL Persist Customer Group Membership and Segmentation]** om te bepalen als de staat van het de groepslidmaatschap en segmenteringscriteria van de klant worden behouden wanneer de zitting beëindigt:

   - `Yes` - De status van het groepslidmaatschap van de klant en de segmentatiegegevens worden opgeslagen wanneer de sessie wordt beëindigd.

   - `No` - De status van het groepslidmaatschap van de klant en de segmentatiegegevens worden niet opgeslagen wanneer de sessie wordt beëindigd.

1. Klik op **[!UICONTROL Save Config]**.
