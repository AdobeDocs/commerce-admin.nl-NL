---
title: Melding van beveiligingsproblemen
description: Leer hoe te om de contactinformatie en veiligheid-verwante verbindingen te vormen die door veiligheidsonderzoekers kunnen worden gebruikt om veiligheidszorgen over uw plaats te melden.
exl-id: 47b95505-51a3-4b7a-a4e3-dbc4b0045797
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 1%

---

# Melding van beveiligingsproblemen

De `security.txt` Het bestand bevat contactgegevens en beveiligingskoppelingen die door beveiligingsonderzoekers kunnen worden gebruikt om beveiligingsproblemen met betrekking tot uw site te melden. Als uw beveiligingsgegevens in de loop der tijd veranderen, controleert u of de gegevens in het dialoogvenster `security.txt` bestand is bijgewerkt.

**_Om security.txt te vormen:_**

1. Op de _Beheerder_ zijbalk, ga naar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. In het linkerdeelvenster onder _[!UICONTROL Security]_, klikt u op **[!UICONTROL Security.txt]**.

1. In de _[!UICONTROL General]_sectie, set **[!UICONTROL Enable]**tot `Yes`.

   ![Algemene beveiligingsconfiguratie](../configuration-reference/security/assets/txt-general.png){width="600" zoomable="yes"}

1. Onder _[!UICONTROL Contact Information]_, voert u het volgende in:

   - Het e-mailadres en telefoonnummer van de persoon die beveiligingsproblemen voor je winkel beheert.

   - De URL van de winkel **[!UICONTROL Contact Page]**. Deze pagina kan een lijst zijn met contactpersonen voor opslagbeveiliging of uw _Contact opnemen_ pagina.

   ![Configuratie contactgegevens](../configuration-reference/security/assets/txt-contact-info.png){width="600" zoomable="yes"}

1. Onder _[!UICONTROL Other Information]_, voert u het volgende in:

   - De URL van uw publiek **[!UICONTROL Encryption]** toets. Bijvoorbeeld: `https://example.com/pgp-key.txt`

   - De URL van een **[!UICONTROL Acknowledgments]** pagina waarop beveiligingsonderzoekers worden herkend voor hun inspanningen namens uw winkel.

   - Uw **[!UICONTROL Preferred Languages]** voor communicatie met betrekking tot veiligheid. Voer het standaardteken van twee tekens in [taalcode](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) voor elke ondersteunde taal, gescheiden door een komma. Als u bijvoorbeeld Engels, Spaans en Frans wilt opgeven, voert u `en, es, fr`. Alle opgegeven talen hebben dezelfde prioriteit, ongeacht de weergavevolgorde.

   - De URL van een **[!UICONTROL Hiring]** pagina die van veiligheid-verwante werkgelegenheidskansen met uw opslag een lijst maakt.

   - De URL van uw beveiliging **[!UICONTROL Policy]** pagina.

   - De URL van een digitaal **[!UICONTROL Signature]** bestand dat op uw server is opgeslagen. Bijvoorbeeld: `https://mystore.com/.well-known/security.txt.sig`

   De digitale handtekening moet zijn ingesteld via de CLI (opdrachtregelinterface) van de server. Zie voor meer informatie [Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) op GitHub.

   ![Overige informatie](../configuration-reference/security/assets/txt-other-info.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Save Config]**.
