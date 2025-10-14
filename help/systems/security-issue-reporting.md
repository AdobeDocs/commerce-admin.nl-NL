---
title: Melding van beveiligingsproblemen
description: Leer hoe te om de contactinformatie en veiligheid-verwante verbindingen te vormen die door veiligheidsonderzoekers kunnen worden gebruikt om veiligheidszorgen over uw plaats te melden.
exl-id: 47b95505-51a3-4b7a-a4e3-dbc4b0045797
role: Admin
feature: Configuration, Security
badgePaas: label="Alleen PaaS" type="Informative" url="https://experienceleague.adobe.com/nl/docs/commerce/user-guides/product-solutions" tooltip="Is alleen van toepassing op Adobe Commerce op Cloud-projecten (door Adobe beheerde PaaS-infrastructuur) en op projecten in het veld."
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---

# Melding van beveiligingsproblemen

Het bestand `security.txt` bevat contactgegevens en beveiligingskoppelingen die door beveiligingsonderzoekers kunnen worden gebruikt om beveiligingsproblemen met betrekking tot uw site te melden. Als uw beveiligingsgegevens na verloop van tijd veranderen, controleert u of de gegevens in het `security.txt` -bestand up-to-date zijn.

**_om security.txt te vormen:_**

1. Voor _Admin_ sidebar, ga **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Klik in het linkerdeelvenster onder _[!UICONTROL Security]_&#x200B;op **[!UICONTROL Security.txt]**.

1. Stel **[!UICONTROL Enable]** in op `Yes` in de sectie _[!UICONTROL General]_.

   ![&#x200B; Algemene veiligheidsconfiguratie &#x200B;](../configuration-reference/security/assets/txt-general.png){width="600" zoomable="yes"}

1. Voer onder _[!UICONTROL Contact Information]_&#x200B;het volgende in:

   - Het e-mailadres en telefoonnummer van de persoon die beveiligingsproblemen voor je winkel beheert.

   - De URL van de winkels **[!UICONTROL Contact Page]** . Deze pagina zou of een lijst van de contacten van de opslagveiligheid of uw _pagina van het Contact van ons_ kunnen zijn.

   ![&#x200B; configuratie van de Informatie van het Contact &#x200B;](../configuration-reference/security/assets/txt-contact-info.png){width="600" zoomable="yes"}

1. Voer onder _[!UICONTROL Other Information]_&#x200B;het volgende in:

   - De URL van de openbare **[!UICONTROL Encryption]** -toets. Bijvoorbeeld: `https://example.com/pgp-key.txt`

   - De URL van een **[!UICONTROL Acknowledgments]** -pagina waarop beveiligingsonderzoekers worden herkend voor hun inspanningen namens uw winkel.

   - Uw **[!UICONTROL Preferred Languages]** voor communicatie met betrekking tot beveiliging. Ga de standaard twee karakter [&#x200B; taalcode &#x200B;](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) voor elke gesteunde taal in, die door een komma wordt gescheiden. Als u bijvoorbeeld Engels, Spaans en Frans wilt opgeven, voert u `en, es, fr` in. Alle opgegeven talen hebben dezelfde prioriteit, ongeacht de weergavevolgorde.

   - De URL van een **[!UICONTROL Hiring]** -pagina met aan beveiliging gerelateerde werkgelegenheidsmogelijkheden in uw winkel.

   - De URL van de beveiligingspagina **[!UICONTROL Policy]** .

   - De URL van een digitaal **[!UICONTROL Signature]** bestand dat op uw server wordt opgeslagen. Bijvoorbeeld: `https://mystore.com/.well-known/security.txt.sig`

   De digitale handtekening moet zijn ingesteld via de CLI (opdrachtregelinterface) van de server. Meer leren, zie [&#x200B; Security.txt &#x200B;](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) op GitHub.

   ![&#x200B; Andere Informatie &#x200B;](../configuration-reference/security/assets/txt-other-info.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]** als de bewerking is voltooid.
