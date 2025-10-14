---
title: Beveiliging
description: Leer over de hulpmiddelen beschikbaar om uw opslag en gegevens te beveiligen, en richtlijnen voor een veiligheidsplan als u een compromis ontdekt.
exl-id: 10eef4ac-de83-4083-9ba3-e42c8eb33781
feature: Security, Site Management
source-git-commit: fede05a413428520eec89d46f41a1cdd9c9c3a2e
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# Beveiliging

U kunt uw winkel op meerdere manieren beveiligen en uw gegevensbeveiliging handhaven:

- De opstelling [&#x200B; twee-factor authentificatie &#x200B;](security-two-factor-authentication.md)
- Voer [&#x200B; CAPTCHA &#x200B;](security-captcha.md) of [&#x200B; reCAPTCHA &#x200B;](security-google-recaptcha.md) uit
- Opstelling het Scannen van de a [&#x200B; Veiligheid &#x200B;](security-scan.md) voor elk domein in uw Adobe Commerce of Magento Open Source installatie.

>[!NOTE]
>
>Voor opslagruimten waarvoor verificatie met [!DNL Adobe Identity Management Services] (IMS) is ingeschakeld, zijn Adobe Commerce en Magento Open Source 2FA uitgeschakeld. Admin-gebruikers die zich bij hun Commerce-instantie hebben aangemeld met hun aanmeldingsgegevens voor de Adobe, hoeven niet opnieuw te worden geverifieerd voor een groot aantal beheertaken. De verificatie wordt uitgevoerd door Adobe IMS wanneer de Admin-gebruiker zich aanmeldt bij de huidige sessie. Zie [[!DNL Adobe Identity Management Service]  (IMS) Overzicht van de Integratie &#x200B;](../getting-started/adobe-ims-integration-overview.md).

Bezoek het [&#x200B; Centrum van de Veiligheid &#x200B;](https://helpx.adobe.com/nl/security.html) {:target= &quot;_blank&quot;} om het recentste nieuws over potentiële kwetsbaarheid te krijgen, voor de berichten van de Veiligheid van de Adobe te registreren, en tot het Centrum van het Vertrouwen van de Adobe toegang te hebben.

![&#x200B; Centrum van de Veiligheid &#x200B;](./assets/product-security-home.png){width="700" zoomable="yes"}

Voor informatie over veiligheid beste praktijken, zie [&#x200B; uw Plaats en Infrastructuur van Commerce beveiligen &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html?lang=nl-NL) in _Playbook van de Implementatie_.

## Actieplan voor veiligheid

Als u vermoedt dat uw Adobe Commerce- of Magento Open Source-site in gevaar is, volgt u dit actieplan onverwijld.

1. **Diagnose**: stel een aftasten in werking om de veiligheidsstatus van uw opslag van Commerce te vestigen. Het Scannen van de Veiligheid van Commerce [&#128279;](security-scan.md) is de vrije dienst die door Adobe wordt aangeboden die u toestaat om uw plaatsen van Commerce voor bekende veiligheidsrisico&#39;s en malware te controleren, en veiligheidsberichten te ontvangen.

1. **Schone**: Huur a [&#x200B; gekwalificeerde adviseur &#x200B;](https://solutionpartners.adobe.com/s/directory/?partner_type=1) of de online dienst om uw plaats van al kwaadwillige code te zuiveren. Sommige leden van de Commerce-gemeenschap raden aan [[!DNL Sucuri Website Malware Removal] &#x200B;](https://sucuri.net/website-antivirus/malware-removal) te gebruiken. Controleer de map `/media` op uitvoerbare code van de overgebleven map. Verwijder alle onbekende Admin-gebruikers en stel alle Admin-wachtwoorden opnieuw in.

1. **Protect**: Houd uw installatie van Commerce bijgewerkt met de huidigste versie. Als u een oudere versie gebruikt, past u alle beveiligingspatches toe zodra deze beschikbaar zijn. Het overzicht en volgt [&#x200B; de veiligheid beste praktijken van Commerce &#x200B;](https://www.adobe.com/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adobe-commerce-best-practices-guide.pdf). Abonneren aan [&#x200B; de Alarm van de Veiligheid van Commerce &#x200B;](https://www.adobe.com/subscription/adbeSecurityNotifications.html).

1. **Rapport**: Als u denkt dat u een specifieke kwetsbaarheid in Commerce hebt gevonden, [&#x200B; open een kwestie met Adobe &#x200B;](https://hackerone.com/adobe?type=team) en omvat technische details.

1. **Verbetering**: Voor de extra vrede van mening die uit 24/7 steun komt, plan uw verbetering aan [&#x200B; Adobe Commerce op onze Architectuur van de Wolk &#x200B;](https://business.adobe.com/products/magento/cloud-delivery.html) nu.
