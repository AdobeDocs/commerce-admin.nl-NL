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

- De opstelling [ twee-factor authentificatie ](security-two-factor-authentication.md)
- Voer [ CAPTCHA ](security-captcha.md) of [ reCAPTCHA ](security-google-recaptcha.md) uit
- Opstelling het Scannen van de a [ Veiligheid ](security-scan.md) voor elk domein in uw Adobe Commerce of Magento Open Source installatie.

>[!NOTE]
>
>Voor opslagruimten waarvoor verificatie met [!DNL Adobe Identity Management Services] (IMS) is ingeschakeld, zijn Adobe Commerce en Magento Open Source 2FA uitgeschakeld. Admin-gebruikers die zich bij hun Commerce-instantie hebben aangemeld met hun aanmeldingsgegevens voor de Adobe, hoeven niet opnieuw te worden geverifieerd voor een groot aantal beheertaken. De verificatie wordt uitgevoerd door Adobe IMS wanneer de Admin-gebruiker zich aanmeldt bij de huidige sessie. Zie [[!DNL Adobe Identity Management Service]  (IMS) Overzicht van de Integratie ](../getting-started/adobe-ims-integration-overview.md).

Bezoek het [ Centrum van de Veiligheid ](https://helpx.adobe.com/nl/security.html) {:target= &quot;_blank&quot;} om het recentste nieuws over potentiële kwetsbaarheid te krijgen, voor de berichten van de Veiligheid van de Adobe te registreren, en tot het Centrum van het Vertrouwen van de Adobe toegang te hebben.

![ Centrum van de Veiligheid ](./assets/product-security-home.png){width="700" zoomable="yes"}

Voor informatie over veiligheid beste praktijken, zie [ uw Plaats en Infrastructuur van Commerce beveiligen ](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html?lang=nl-NL) in _Playbook van de Implementatie_.

## Actieplan voor veiligheid

Als u vermoedt dat uw Adobe Commerce- of Magento Open Source-site in gevaar is, volgt u dit actieplan onverwijld.

1. **Diagnose**: stel een aftasten in werking om de veiligheidsstatus van uw opslag van Commerce te vestigen. Het Scannen van de Veiligheid van Commerce [&#128279;](security-scan.md) is de vrije dienst die door Adobe wordt aangeboden die u toestaat om uw plaatsen van Commerce voor bekende veiligheidsrisico&#39;s en malware te controleren, en veiligheidsberichten te ontvangen.

1. **Schone**: Huur a [ gekwalificeerde adviseur ](https://solutionpartners.adobe.com/s/directory/?partner_type=1) of de online dienst om uw plaats van al kwaadwillige code te zuiveren. Sommige leden van de Commerce-gemeenschap raden aan [[!DNL Sucuri Website Malware Removal] ](https://sucuri.net/website-antivirus/malware-removal) te gebruiken. Controleer de map `/media` op uitvoerbare code van de overgebleven map. Verwijder alle onbekende Admin-gebruikers en stel alle Admin-wachtwoorden opnieuw in.

1. **Protect**: Houd uw installatie van Commerce bijgewerkt met de huidigste versie. Als u een oudere versie gebruikt, past u alle beveiligingspatches toe zodra deze beschikbaar zijn. Het overzicht en volgt [ de veiligheid beste praktijken van Commerce ](https://www.adobe.com/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adobe-commerce-best-practices-guide.pdf). Abonneren aan [ de Alarm van de Veiligheid van Commerce ](https://www.adobe.com/subscription/adbeSecurityNotifications.html).

1. **Rapport**: Als u denkt dat u een specifieke kwetsbaarheid in Commerce hebt gevonden, [ open een kwestie met Adobe ](https://hackerone.com/adobe?type=team) en omvat technische details.

1. **Verbetering**: Voor de extra vrede van mening die uit 24/7 steun komt, plan uw verbetering aan [ Adobe Commerce op onze Architectuur van de Wolk ](https://business.adobe.com/products/magento/cloud-delivery.html) nu.
