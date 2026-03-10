---
title: Uitchecken door gast
description: Leer hoe je uitcheckmogelijkheden voor gasten inschakelt in je winkel.
exl-id: ce25eba3-7503-46aa-a5cd-9b7d5662164b
feature: Checkout
source-git-commit: 347321ec5b0722f06240780136cb29816aab559f
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# Uitchecken door gast

Uw winkel kan zo worden geconfigureerd dat kopers een account moeten openen voordat ze een aankoop doen. Met de standaardinstelling kunnen gasten aankopen doen, met een optie om zich voor een account te registreren nadat ze het afrekenen hebben voltooid.

![&#x200B; de vertoningenControle van de opslag van de Luma uit als Gast &#x200B;](./assets/storefront-checkout-as-guest.png){width="600" zoomable="yes"}

**_Het uitchecken van gasten uitschakelen:_**

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Checkout]** .

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Checkout Options]** sectie uit.

   ![&#x200B; uitcheckopties die op de configuratiepagina &#x200B;](./assets/checkout-checkout-options.png){width="700" zoomable="yes"} worden uitgebreid

Voor een gedetailleerde beschrijving van elk van deze configuratiemontages, zie [&#x200B; Opties van de Controle &#x200B;](../configuration-reference/sales/checkout.md#checkout-options) in de _Gids van de Verwijzing van de Configuratie_.

1. Als het plaatsen voor een specifieke opslagmening is, [&#x200B; kies de opslagmening &#x200B;](../configuration-reference/scope-change.md#set-the-scope) waar de configuratie van toepassing is.

   Klik op **[!UICONTROL OK]** als u daarom wordt gevraagd om door te gaan.

1. Stel **[!UICONTROL Allow Guest Checkout]** in op `No` .

   Schakel indien nodig het selectievakje **[!UICONTROL Use system value]** uit om wijzigingen in deze instelling in te schakelen.

1. Klik op **[!UICONTROL Save Config]**.

## Toegang tot geregistreerde e-mails voor gasten toestaan

[!BADGE &#x200B; slechts SaaS &#x200B;]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Alleen van toepassing op Adobe Commerce as a Cloud Service-projecten (door Adobe beheerde SaaS-infrastructuur)."}

Een facultatieve, store-level configuratie, die door gebrek wordt onbruikbaar gemaakt, staat gastkopers toe om hun geplaatste orden te volgen gebruikend een e-mailadres dat een geregistreerd klantenrekening aanpast.

Als deze optie is ingeschakeld, blijven opdrachten voor uitchecken door gasten die met een geregistreerd e-mailadres zijn geplaatst, toegankelijk, terwijl deze ook in de ordergeschiedenis van de klant worden weergegeven.

Om deze eigenschap toe te laten, navigeer aan **Opslag** > Montages > **Configuratie** > Verkoop > **Verkoop** > **Uitchecken van de Gast** en plaats **Toestaan de Toegang van de Orde van de Gast voor Geregistreerde E-mail** plaatsen aan `Yes`.
