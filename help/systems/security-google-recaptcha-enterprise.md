---
title: Google reCAPTCHA Enterprise
description: Leer hoe u Google reCAPTCHA Enterprise configureert om uw Adobe Commerce as a Cloud Service-winkel te beschermen tegen bots en frauduleuze activiteiten.
role: Admin
feature: Configuration, Security
badgeSaas: label="Alleen SaaS" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Alleen van toepassing op Adobe Commerce as a Cloud Service-projecten (door Adobe beheerde SaaS-infrastructuur)."
source-git-commit: 8d73a3a635c20e636c4b8bde41a4f807d3fd9f2e
workflow-type: tm+mt
source-wordcount: '545'
ht-degree: 0%

---

# Google reCAPTCHA Enterprise

[&#x200B; Google reCAPTCHA Onderneming &#x200B;](https://cloud.google.com/security/products/recaptcha#protect-against-fraud-and-abuse-with-modern-bot-protection-and-fraud-prevention-platform) verstrekt geavanceerde botbescherming voor uw Adobe Commerce as a Cloud Service storefront door adaptieve risicoanalyse en machine het leren te gebruiken om tussen menselijke gebruikers en bots te onderscheiden. Zo voorkomt u frauduleuze activiteiten, spam en misbruik op uw site.

>[!NOTE]
>
>Deze functie biedt GEEN reCAPTCHA-ondersteuning voor de beheerder.

Zie [&#x200B; Google reCAPTCHA V3 en V2 &#x200B;](security-google-recaptcha.md) voor informatie over het vormen van andere versies van Google reCAPTCHA.

## Functies

Google reCAPTCHA Enterprise bevat de volgende functies:

- **Geavanceerde botopsporing**: Gebruikt machine het leren van modellen van Google Cloud voor superieure botopsporing
- **de score van het Risico analyse**: Verstrekt gedetailleerde risicocores (0.0-1.0) voor elke interactie
- **Configureerbare drempels**: Plaats minimum aanvaardbare risicocores per huurder
- **Multi-huurderssteun**: Configuratie per-huurder met geïsoleerde projecten van de Wolk van Google
- **Gecodeerde geloofsbrieven**: De geloofsbrieven van de rekening van de dienst die in een gegevensbestand worden opgeslagen
- **de bescherming van de Vorm**: beschermt alle standaardvormen van Commerce, met inbegrip van login, controle, productrevisies, en meer.

## Vereisten

U hebt de volgende bronnen nodig voordat u Google reCAPTCHA Enterprise voor uw Adobe Commerce as a Cloud Service-winkel kunt configureren:

- Een actief Google Cloud-account met reCAPTCHA Enterprise ingeschakeld.
- Toegang tot de Google Cloud Console voor het maken en beheren van reCAPTCHA Enterprise-sleutels.

Bij Adobe Commerce as a Cloud Service-installaties met meerdere huurders moet elke huurder zijn eigen Google Cloud-project en reCAPTCHA Enterprise keys hebben.

## Stap 1: Google reCAPTCHA Enterprise instellen

Voer de volgende algemene stappen uit om Google reCAPTCHA Enterprise in te stellen voor uw winkel. Voor gedetailleerde instructies, zie de [&#x200B; documentatie van de Onderneming van Google reCAPTCHA &#x200B;](https://docs.cloud.google.com/recaptcha/docs/overview).

1. [&#x200B; creeer een project van de Wolk van Google &#x200B;](https://developers.google.com/workspace/guides/create-project) voor uw reCAPTCHA implementatie van de Onderneming.

1. Laat [&#x200B; reCAPTCHA Onderneming API &#x200B;](https://docs.cloud.google.com/recaptcha/docs/prepare-environment) toe.

1. Creeer op score-gebaseerde reCAPTCHA de plaats sleutel [&#x200B; &#x200B;](https://docs.cloud.google.com/recaptcha/docs/choose-key-type).

1. Maak een serviceaccount met de `roles/recaptchaenterprise.admin` IAM-rol.

1. Download het JSON-sleutelbestand van de serviceaccount, dat de gegevens bevat die nodig zijn om uw Adobe Commerce as a Cloud Service-winkel te verifiëren met Google reCAPTCHA Enterprise.

## Stap 2: Vorm Google reCAPTCHA voor de storefront

1. Kies in het linkerdeelvenster onder _[!UICONTROL Security]_&#x200B;de optie **[!UICONTROL Google reCAPTCHA Storefront]**.

1. Vul de sectie **[!UICONTROL reCAPTCHA Enterprise]** als volgt in.

   - Voor **[!UICONTROL Site Key]** kopieert en plakt u de reCAPTCHA Enterprise-site-sleutel uit uw Google Cloud Console.

   - Kopieer en plak voor **[!UICONTROL Google Cloud Project ID]** de project-id uit uw Google Cloud-project.

   - Voor **[!UICONTROL Service Account JSON]**, kopieer de inhoud van het de zeer belangrijke dossier van de Rekening van de Dienst JSON dat u in [&#x200B; Stap 1 downloadde: De Onderneming van Google reCAPTCHA &#x200B;](#step-1-set-up-google-recaptcha-enterprise).

   - Voer voor **[!UICONTROL Minimum Score Threshold]** de minimumscore (0,0-1,0) in om te bepalen wanneer een gebruikersinteractie wordt gemarkeerd als een potentieel risico. Een score van 1,0 is een typische gebruikersinteractie, en 0,0 is waarschijnlijk een bot.

   - Kies bij **[!UICONTROL Badge Position]** de positie van het onzichtbare reCAPTCHA-symbool op elke pagina. Opties: `Inline` / `Bottom Right` / `Bottom Left` .

   - Kies bij **[!UICONTROL Theme]** de optie `Light Theme` (standaardwaarde) of `Dark Theme` om de stijl van het vak Google reCAPTCHA te bepalen.

   - Voor **[!UICONTROL Language Code]**, ga a [&#x200B; twee-karakter code &#x200B;](https://developers.google.com/recaptcha/docs/language) in die de taal specificeert die voor de tekst en het overseinen van Google reCAPTCHA wordt gebruikt.

   - Voor **[!UICONTROL Validation Failure Message]** kunt u desgewenst het bericht wijzigen dat in de winkel wordt weergegeven wanneer de validatie is mislukt.


1. Vouw de sectie **[!UICONTROL Storefront]** uit en stel elk storefront formulier dat u wilt beveiligen in op **[!UICONTROL reCAPTCHA Enterprise]** .

   {{recaptcha-forms-list}}

   ![&#x200B; de optieconfiguratie van de Storefront &#x200B;](../configuration-reference/security/assets/recaptcha-storefront.png){width="600" zoomable="yes"}

## Stap 3: Sparen de configuratie

1. Klik op **[!UICONTROL Save Config]** wanneer de configuratie-instellingen zijn voltooid.

1. Klik in het bericht boven aan de werkruimte op **[!UICONTROL Cache Management]** en vernieuw elke ongeldige cache.
