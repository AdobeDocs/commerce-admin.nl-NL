---
title: persistentie van winkelwagentjes
description: Leer hoe een hardnekkig winkelwagentje niet-aangeschafte winkelartikelen bijhoudt en de informatie voor het volgende bezoek van de klant opslaat.
exl-id: 95c336b3-77ac-4cf6-8fb5-23f4ac4b67d6
feature: Shopping Cart, Configuration
source-git-commit: 26d4bb35c6e1878a8ea8c5f05a982559e5d6dc35
workflow-type: tm+mt
source-wordcount: '1473'
ht-degree: 0%

---

# persistentie van winkelwagentjes

Een hardnekkig winkelwagentje volgt niet-aangeschafte artikelen die in het winkelwagentje blijven staan en slaat de informatie op voor het volgende bezoek van de klant. Klanten die _onthouden_ De volgende keer dat ze uw winkel bezoeken, kan de inhoud van hun winkelwagentjes worden hersteld.

Een hardnekkig winkelwagentje kan helpen het aantal verlaten winkelwagentjes te verminderen en de verkoop te verhogen. Het is belangrijk te begrijpen dat het hardnekkige winkelwagentje op geen enkel moment gevoelige accountinformatie blootstelt. Terwijl het hardnekkige winkelwagentje in gebruik is, moeten zowel geregistreerde klanten als gastklanten zich aanmelden bij een bestaande account of een account maken voordat ze de afhandeling kunnen uitvoeren. Voor gastkopers is een hardnekkig winkelwagentje de enige manier om informatie van een vorige sessie op te halen.

Als u het gebruik van winkelwagentpersistentie voor uw site of in specifieke winkelweergaven wilt beheren, kunt u [permanent winkelwagentje configureren](#configure-a-persistent-cart) instellingen. Voor meer informatie over hoe deze montages de verkoopervaring in uw winkel beïnvloeden, zie [Blijvende workflow voor winkelwagentjes](#persistent-cart-workflow).

>[!NOTE]
>
>Wanneer u een blijvend winkelwagentje gebruikt, wordt u aangeraden de levensduur van de serversessie en het sessiecookie in te stellen op een lange periode. Zie [Sessielevensduur](../customers/customer-online-options.md) voor meer informatie .

Als u het hardnekkige winkelwagentje wilt gebruiken, moet de browser van de klant zo zijn ingesteld dat cookies zijn toegestaan. Er worden twee soorten cookies gebruikt voor winkelwagentjes:

- **Sessiecookie** - Er bestaat een sessiecookie voor de korte termijn tijdens één bezoek aan uw site en deze vervalt wanneer de klant verlaat of na een bepaalde periode.

- **Blijvende cookie** - Een langdurige, permanente cookie blijft bestaan na het einde van de sessie en slaat een record op van de inhoud van het winkelwagentje van de klant voor toekomstig gebruik.

## Blijvende workflow voor winkelwagentjes

Wanneer de hardnekkige winkelwagentje [enabled](#configure-a-persistent-cart), is de workflow afhankelijk van:

- De waarden van _Onthouden inschakelen_ en _Persistentie bij afmelden wissen_ instellingen
- Het besluit van de klant om de _Mijn gegevens onthouden_ selectievakje
- Wanneer de permanente cookie wordt gewist

Wanneer een permanente cookie wordt toegepast, wordt een `Not Jane Smith?` wordt weergegeven in de koptekst van de pagina. Deze herinnering geeft de klant de capaciteit om de blijvende zitting te eindigen en beginnen werkend als gast, of aan login als verschillende klant. Het systeem houdt een register bij van de inhoud van het winkelwagentje, zelfs als de klant later andere apparaten gebruikt om in uw winkel te winkelen. Een klant kan bijvoorbeeld een item vanaf een laptop aan het winkelwagentje toevoegen, meer items van een mobiel apparaat toevoegen en het afrekenproces vanaf een tablet voltooien.

Er is een afzonderlijke, onafhankelijke, permanente cookie voor elke browser. Als de klant meerdere browsers gebruikt tijdens het bezoeken van uw winkel tijdens één permanente sessie, worden de wijzigingen die in de ene browser zijn aangebracht, doorgevoerd in elke andere browser nadat de pagina is vernieuwd. Terwijl de persistente winkelwagentje is ingeschakeld, maakt en onderhoudt uw winkel een aparte, permanente cookie voor elke browser die door een klant wordt gebruikt om zich aan te melden of een account te maken.

### Voorbeeld: een open sessie op een gedeelde computer

Jane voltooit haar vakantiewinkelen met een blijvende sessie. Ze voegt een cadeautje voor John toe aan haar kar en iets voor haar moeder. Dan gaat ze naar de keuken voor een snack.

John zit op de computer om snel te winkelen terwijl Jane in de keuken is. Zonder de `Not Jane Smith?` boven aan de pagina vindt hij een leuk cadeau voor Jane en voegt het toe aan de wagen . Als hij uitcheckt en zich aanmeldt als zichzelf, worden beide items in Jane&#39;s winkelwagen aan zijn winkelwagen toegevoegd. John heeft zo&#39;n haast dat hij de extra items niet opmerkt tijdens _Ordercontrole_ en dient de bestelling in. Jane&#39;s winkelwagen is nu leeg en John heeft alle geschenken gekocht.

### Mijn gegevens onthouden

Klanten kunnen de _Mijn gegevens onthouden_ Schakel het selectievakje op de aanmeldingspagina in om de inhoud van hun winkelwagentjes op te slaan.

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
| **[!UICONTROL Enable Remember Me]** is ingesteld op `No`.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**heeft een willekeurige waarde.<br/><br/>De** Mijn gegevens onthouden **het selectievakje is niet beschikbaar op de aanmeldings- en registratiepagina. | De permanente cookie wordt niet gebruikt. |
| **[!UICONTROL Enable Remember Me]** is ingesteld op `Yes`.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**heeft een willekeurige waarde.<br/><br/>** Mijn gegevens onthouden **is niet geselecteerd. | De sessiecookie wordt op de gebruikelijke manier toegepast; de permanente cookie wordt niet gebruikt. |
| **[!UICONTROL Enable Remember Me]** is ingesteld op `Yes`.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**is ingesteld op `Yes`.<br/><br/>** Mijn gegevens onthouden **is ingesteld op `Yes`. | Wanneer een klant zich aanmeldt, worden beide cookies toegepast. Wanneer een klant zich afmeldt, worden beide cookies verwijderd. Als een klant zich niet aanmeldt maar het sessiecookie verloopt, wordt de permanente cookie nog steeds gebruikt. Naast het afmelden wordt de permanente cookie verwijderd wanneer de levensduur van de cookie is verstreken of wanneer de klant op de knop `Not Jane Smith` koppeling. |
| **[!UICONTROL Enable Remember Me]** is ingesteld op `Yes`.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**is ingesteld op `No`.<br/><br/>** Mijn gegevens onthouden **is ingesteld op `Yes` | Wanneer een klant zich aanmeldt, worden beide cookies toegepast. Wanneer een klant zich afmeldt, wordt het sessiecookie verwijderd, wordt de permanente sessie voortgezet. De permanente cookie wordt verwijderd wanneer de levensduur van de cookie is verstreken of wanneer de klant op de knop `Not Jane Smith` koppeling. |

{style="table-layout:auto"}

## Een blijvende poort configureren

Tijdens de opstelling van een blijvend winkelwagentje, kunt u de levensduur van de koekjes specificeren, en welke opties u voor diverse klantenactiviteiten ter beschikking wilt stellen.

Voor meer informatie over hoe het klantenwerkschema door deze montages wordt bepaald, zie [Blijvende workflow voor winkelwagentjes](#persistent-cart-workflow).

>[!NOTE]
>
>Als het sessiecookie verloopt terwijl de klant is aangemeld, blijft de permanente cookie actief.

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster uit **[!UICONTROL Customers]** en kiest u **[!UICONTROL Persistent Shopping Cart]**.

1. Als u het hardnekkige winkelwagentje wilt inschakelen en extra opties wilt weergeven, stelt u **[!UICONTROL Enable Persistence]** tot `Yes`.

   ![Het toelaten van en het vormen van het karretpersistentie](../configuration-reference/customers/assets/persistent-shopping-cart-general.png){width="600" zoomable="yes"}

   Voor meer informatie over elk van deze configuratiemontages, zie [_Configuratieverwijzing_](../configuration-reference/customers/persistent-shopping-cart.md)

   >[!NOTE]
   >
   >Wis indien nodig de **[!UICONTROL Use system value]** Schakel het selectievakje in om deze instellingen te wijzigen.

1. Voor **[!UICONTROL Persistence Lifetime (seconds)]**, voert u de tijdsduur in seconden in waarin de permanente cookie moet duren.

   De standaardwaarde van 31.536.000 seconden is gelijk aan één jaar. De maximaal toegestane tijd is 100 jaar.

1. Set **[!UICONTROL Enable "Remember Me"]** op een van de volgende wijzen:

   - `Yes` - Geeft de _Mijn gegevens onthouden_ Schakel het selectievakje op de aanmeldingspagina van uw winkel in, zodat klanten hun winkelwagengegevens kunnen opslaan.

   - `No` - Persistentie kan nog steeds worden ingeschakeld, maar klanten krijgen niet de mogelijkheid om te kiezen of ze hun gegevens willen opslaan.

1. Als u de optie _Mijn gegevens onthouden_ selectievakje voor de klant instellen **[!UICONTROL Remember Me Default Value]** tot `Yes`.

   De klant kan deze optie desgewenst wissen.

1. Set **[!UICONTROL Clear Persistence on Log Out]** op een van de volgende wijzen:

   - `Yes` - Het winkelwagentje wordt gewist wanneer een geregistreerde klant zich afmeldt.

   - `No` - Het winkelwagentje wordt opgeslagen wanneer een geregistreerde klant zich afmeldt.

   >[!NOTE]
   >
   >Als het sessiecookie verloopt terwijl de klant nog steeds is aangemeld, blijft de permanente cookie in gebruik.

1. Set **[!UICONTROL Persist Shopping Cart]** op een van de volgende wijzen:

   - `Yes` - Als het sessiecookie verloopt, blijft de permanente cookie behouden. Als een gast later zich aanmeldt of een account maakt, wordt het winkelwagentje hersteld.

   - `No` - Het winkelwagentje blijft niet bewaard voor gasten nadat het sessiecookie is verlopen.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (alleen Adobe Commerce) Instellen **[!UICONTROL Persist Wish List]** om te bepalen of de staat van klant wenst lijsten wordt behouden wanneer de zitting beëindigt:

   - `Yes` - De inhoud van de wensenlijst wordt opgeslagen wanneer de sessie wordt beëindigd.

   - `No` - De lijst met wensen wordt niet opgeslagen wanneer de sessie wordt beëindigd.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (alleen Adobe Commerce) Instellen **[!UICONTROL Persist Recently Ordered Items]** om te bepalen of de staat van onlangs bevolen punten wordt behouden wanneer de zitting beëindigt:

   - `Yes` - De status van onlangs bestelde items wordt opgeslagen wanneer de sessie wordt beëindigd.

   - `No` - De status van onlangs bestelde items wordt niet opgeslagen wanneer de sessie wordt beëindigd.

1. Set **[!UICONTROL Persist Currently Compared Products]** tot `Yes` of `No`.

1. Set **[!UICONTROL Persist Comparison History]** tot `Yes` of `No`.

1. Set **[!UICONTROL Persist Recently Viewed Products]** tot `Yes` of `No`.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (alleen Adobe Commerce) Instellen **[!UICONTROL Persist Customer Group Membership and Segmentation]** om te bepalen of de staat van het groepslidmaatschap en de segmenteringscriteria van de klant worden behouden wanneer de zitting beëindigt:

   - `Yes` - De status van het groepslidmaatschap van de klant en de segmentatiegegevens worden opgeslagen wanneer de sessie wordt beëindigd.

   - `No` - De status van het groepslidmaatschap van de klant en de segmentatiegegevens worden niet opgeslagen wanneer de sessie wordt beëindigd.

1. Klik op **[!UICONTROL Save Config]**.
