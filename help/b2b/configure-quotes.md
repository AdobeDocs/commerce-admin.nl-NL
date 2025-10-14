---
title: Aanhalingstekens configureren
description: Leer over citaatconfiguratie, die het minimale vereiste ordebedrag voor citaatverzoeken, het citaatleven, en dossiergehechtheid controleert.
exl-id: 865f6624-df9b-4f78-abfa-1f9a3d82bc0d
feature: B2B, Companies, Configuration, Quotes
role: Admin
source-git-commit: d4c3ea4b49e30ae3af249516d32fb28437d218b8
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Aanhalingstekens configureren

Als de citaten in de algemene [&#x200B; B2B eigenschappen &#x200B;](enable-basic-features.md) worden toegelaten, kunt u steun voor citaten in Admin vormen. De configuratie met aanhalingstekens bepaalt de minimale vereiste volgordehoeveelheid voor aanhalingsverzoeken, de levensduur van de aanhalingstekens en de ondersteunde bestandsindelingen voor bijgevoegde bestanden.

>[!NOTE]
>
>De configuratieopties van het citaat en de capaciteit om de functies van de citaatonderhandeling te gebruiken worden gecontroleerd gebruikend de [&#x200B; rolmiddelen &#x200B;](../systems/permissions-user-roles.md#role-resources). Deze rolmiddelen moeten voor de Admin gebruikersrol worden geselecteerd die aan de Admin gebruikersrekening wordt toegewezen. Om toegang tot citaatfuncties in Admin te verlenen, ga **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**, selecteer de rol, en navigeer aan [!UICONTROL Sales] > [!UICONTROL Operations] > [!UICONTROL Quotes] in de_ Bron van de Rol _boom.

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Vouw in het linkerdeelvenster **[!UICONTROL Sales]** uit en kies **[!UICONTROL Quotes]** .

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL General]** sectie uit en doe het volgende:

   ![&#x200B; configuratie van de citaten van de Verkoop - algemeen &#x200B;](./assets/quotes-general.png){width="700" zoomable="yes"}

   Zie [&#x200B; Citaten &#x200B;](../configuration-reference/sales/quotes.md) in de _Verwijzing van de Configuratie_ voor een volledige lijst van de eigenschapopties van Citaten en hun functies.

   - Voer de **[!UICONTROL Minimum Amount]** in het winkelwagentje in waaraan moet worden voldaan voordat een prijsaanvraag kan worden ingediend.

   - Voer bij **[!UICONTROL Minimum Amount Message]** het bericht in dat u wilt weergeven wanneer het totaal van het winkelwagentje niet aan de vereiste minimumhoeveelheid voldoet.

   - Voer bij **[!UICONTROL Default Expiration Period]** het nummer in van **[!UICONTROL days]** , **[!UICONTROL weeks]** of **[!UICONTROL months]** dat een aanhalingsteken geldig moet blijven.

1. Breid ![&#x200B; selecteur van de Uitbreiding &#x200B;](../assets/icon-display-expand.png) de **[!UICONTROL Attached files]** sectie uit en doe het volgende:

   - Voer bij **[!UICONTROL File formats for upload]** het achtervoegsel in van elk bestandstype dat u ondersteunt voor bestanden die aan een aanhalingsteken zijn gekoppeld.

     Voer elk achtervoegsel in kleine letters in, gescheiden door een komma.

     De volgende indelingen worden standaard ondersteund: `doc`, `docx`, `xls`, `xlsx`, `pdf`, `txt`, `jpg`, `png` en `jpeg`

   - Voer bij **[!UICONTROL Maximum file size]** de maximale grootte van een bijgevoegd bestand in megabytes in.

     De waarde die u invoert, wordt mogelijk overschreven door de serverinstelling.

     ![&#x200B; configuratie van de citaten van de Verkoop - in bijlage dossiers &#x200B;](./assets/quotes-attached-files.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.
