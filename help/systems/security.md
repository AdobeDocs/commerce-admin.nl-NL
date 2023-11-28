---
title: Beveiliging
description: Leer over de hulpmiddelen beschikbaar om uw opslag en gegevens te beveiligen, en richtlijnen voor een veiligheidsplan als u een compromis ontdekt.
exl-id: 10eef4ac-de83-4083-9ba3-e42c8eb33781
feature: Security, Site Management
source-git-commit: 671ec7015c37b24ca0acc615ae3715b8b870a453
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# Beveiliging

U kunt uw winkel op meerdere manieren beveiligen en uw gegevensbeveiliging handhaven:

- Instellen [tweeledige verificatie](security-two-factor-authentication.md)
- Implementeren [CAPTCHA](security-captcha.md) of [reCAPTCHA](security-google-recaptcha.md)
- Een [Beveiligingsscan](security-scan.md) voor elk domein in uw Adobe Commerce of Magento Open Source installatie.

Ga naar [Beveiligingscentrum](https://helpx.adobe.com/security.html){:target=&quot;_blank&quot;} en meld u aan bij het Beveiligingswaarschuwingsregister voor het meest recente nieuws over potentiële kwetsbaarheden. Voor informatie over best practices op het gebied van beveiliging raadpleegt u [Beveilig uw Plaats van de Handel en Infrastructuur](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html) in de _Afspeelmap voor implementatie_.

>[!NOTE]
>
>Winkels die zijn ingeschakeld [!DNL Adobe Identity Management Services] (IMS)-verificatie heeft native Adobe Commerce en Magento Open Source 2FA uitgeschakeld. De gebruikers Admin die in hun instantie van de Handel met hun geloofsbrieven van de Adobe worden geregistreerd hoeven niet voor vele Admin taken opnieuw voor authentiek te verklaren. De verificatie wordt uitgevoerd door Adobe IMS wanneer de Admin-gebruiker zich aanmeldt bij de huidige sessie. Zie [[!DNL Adobe Identity Management Service] (IMS) Overzicht van integratie](../getting-started/adobe-ims-integration-overview.md).

![Beveiligingscentrum](./assets/product-security-home.png){width="700" zoomable="yes"}

## Actieplan voor veiligheid

Als u vermoedt dat uw Adobe Commerce- of Magento Open Source-site in gevaar is, volgt u dit actieplan onverwijld.

1. **Diagnose**: Voer een scan uit om de beveiligingsstatus van uw winkel te bepalen. Handel [Beveiligingsscan](security-scan.md) is een vrije dienst die door Adobe wordt aangeboden die u toestaat om uw plaatsen van de Handel voor bekende veiligheidsrisico&#39;s en malware te controleren, en veiligheidsberichten te ontvangen.

1. **Reinigen**: Hire a [gekwalificeerde consultant](https://solutionpartners.adobe.com/s/directory/?partner_type=1) of online service om uw site van alle kwaadaardige code te reinigen. Sommige leden van de gemeenschap van de Handel adviseren [[!DNL Sucuri Website Malware Removal]](https://sucuri.net/website-antivirus/malware-removal). Controleer de `/media` map voor uitvoerbare code van de overgebleven server. Verwijder alle onbekende Admin-gebruikers en stel alle Admin-wachtwoorden opnieuw in.

1. **Protect**: Houd uw installatie van de Handel bijgewerkt met de recentste versie. Als u een oudere versie gebruikt, past u alle beveiligingspatches toe zodra deze beschikbaar zijn. Controleren en volgen [Best practices op het gebied van handelsbeveiliging](https://www.adobe.com/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adobe-commerce-best-practices-guide.pdf). Aanmelden bij [Beveiligingswaarschuwingen voor handel](https://www.adobe.com/subscription/adbeSecurityNotifications.html).

1. **Rapport**: Als u denkt dat u een specifieke kwetsbaarheid in de Handel hebt gevonden, [een probleem met Adobe openen](https://hackerone.com/adobe?type=team) en bevat technische details.

1. **Upgrade**: Voor de extra gemoedsrust die uit 24/7 steun komt, plan uw verbetering aan [Adobe Commerce op onze cloudarchitectuur](https://business.adobe.com/products/magento/cloud-delivery.html) nu.
