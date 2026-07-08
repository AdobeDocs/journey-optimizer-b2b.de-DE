---
title: Governance- und Datenschutzfunktionen
description: Erfahren Sie mehr über Governance-Funktionen, die derzeit in Journey Optimizer B2B edition verfügbar sind.
feature: Setup
role: Admin
exl-id: 2845272b-987c-4a37-adf4-6ee5bfd59fc0
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: d6e625c1-468f-4d73-9f32-fd1edb87f96b
  - id: f2da1b69-6919-4386-a5d2-9c7b5c9033db
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
autotag-review: 2026-03-27T23:18:44.352Z
TQID: https://experienceleague.adobe.com/PwH34suDPc84nB9eiAWtrkVzsOw82RRGw4hrRogf9zE
source-git-commit: 61481d57fb8eca805d9a9bc545124aed568b5416
workflow-type: tm+mt
source-wordcount: 697
ht-degree: 2%

---

# Governance- und Datenschutzfunktionen

[!DNL Journey Optimizer B2B Edition] ist eine integrierte Adobe Experience Platform-App. Sie verwendet mehrere Tools und Services, die die Kontrolle über Ihre erfassten Erlebnisdaten in Übereinstimmung mit Ihren Geschäftspraktiken, rechtlichen Verpflichtungen und Entwicklungsprozessen ermöglichen. Die folgenden Abschnitte enthalten eine Zusammenfassung jeder dieser Governance-Funktionen.

## Datenschutz

Es gibt verschiedene Vorschriften, die für [!DNL Journey Optimizer B2B Edition] Kunden gelten, die Daten von betroffenen Personen besitzen, die in den oben genannten Regionen oder Ländern (EU, Kalifornien, Thailand, Brasilien, Neuseeland) ansässig sind. Diese Informationen auf dieser Seite sind keine Rechtsberatung und garantieren nicht die Einhaltung des geltenden Rechts.

### DSGVO

Die Datenschutz-Grundverordnung (DSGVO) ist das Datenschutzrecht der Europäischen Union (EU), das die [Datenschutzanforderungen) für &#x200B;](https://commission.europa.eu/law/law-topic/data-protection/data-protection-explained_en){target="_blank"} EU-Länder harmonisiert und modernisiert.

[!DNL Journey Optimizer B2B Edition] verwendet die vorhandenen Marketo Engage-DSGVO-Governance-Funktionen, die von Privacy Service und Marketo Privacy Broker Service bereitgestellt werden.

### CNIL

Am 14. April 2026 veröffentlichte die Commission nationale de l&#39;informatique et des libertés ([) eine Empfehlung &#x200B;](https://cnil.fr/sites/default/files/2026-05/recommandation_tracking_pixels_emails.pdf) die Verwendung von Tracking-Pixeln in E-Mails. In der Anleitung wird klargestellt, wann eine Zustimmung erforderlich ist, und die Bedeutung ordnungsgemäßer Zustimmungspraktiken für das E-Mail-Pixel-Tracking hervorgehoben. Diese Richtlinie wirkt sich auf alle Entitäten aus, die E-Mails an Abonnentinnen und Abonnenten mit Sitz in Frankreich senden.

CNIL räumte Unternehmen ab dem Datum der Empfehlung einen Zeitraum von drei Monaten ein, um ihre E-Mail-Empfänger über das Vorhandensein der Tracking-Pixel, ihren Zweck und das Recht der Empfänger auf Opt-out zu informieren. Während dieser Übergangsphase wird von Marketo Engage-Benutzenden erwartet, dass sie ihre Empfängerinnen und Empfänger über das Pixel-Tracking informieren und bei Bedarf eine Abmeldung ermöglichen. CNIL wird voraussichtlich nach dem 14. Juli 2026 mit Durchsetzungsmaßnahmen beginnen.

Während die CNIL und andere Regulierungsbehörden die Richtlinien zur Verfolgung von Pixeln und damit zusammenhängenden Problemen erläutern, wird Adobe weiterhin Aktualisierungen überwachen und Sie über sich ändernde technische Möglichkeiten informieren.

[!DNL Journey Optimizer B2B Edition] bietet Steuerelemente, mit denen Sie das Öffnungs-Tracking auf E-Mail-Ebene verwalten können. Benutzer sind dafür verantwortlich, ihre eigenen Compliance-Verpflichtungen gemäß den geltenden CNIL-Leitlinien und anderen Gesetzen zu bestimmen. Informationen zur Verwendung dieser Funktionen zum Verwalten des Öffnungs-Trackings von E-Mails finden Sie unter [_Verwalten des E-Mail-Trackings_](../content/email-tracking-manage.md).

## Rollenbasierte Zugriffskontrolle (RBAC)

Mit Journey Optimizer B2B edition und Zugriff auf Adobe Admin Console können Admins einem Benutzer Berechtigungen für einen Entitätstyp erteilen (Anzeigen von Segmenten, Verwalten von Segmenten, Verwalten von Journey-Segmenten usw.). Diese Funktion ist Teil des Unified Permissions Framework (UPF), mit dem alle Adobe Experience Platform-Kunden Rollen und Berechtigungen für ihr Unternehmen definieren und verwalten können.

## Datenverschlüsselung

**_Verschlüsselung ruhender Daten_** - Alle von Adobe Experience Platform in Journey Optimizer B2B edition übertragenen Konto- und Personenprofildaten werden verschlüsselt, um die bestehende Konformität von Experience Platform aufrechtzuerhalten. Alle Entitäten mit Ursprung in Journey Optimizer B2B edition, z. B. Journeys und Einkaufsgruppen, werden ebenfalls verschlüsselt.

**_Verschlüsselung von Daten bei der Übertragung_** (über ein öffentliches Netzwerk): Alle Journey Optimizer B2B edition-APIs und -Entitäten werden während der Übertragung mit TLS 1.2 verschlüsselt.

## Opt-in/Opt-out für Einverständnis

Journey Optimizer B2B edition liest die in den XDM-Profilen von Adobe Experience Platform gespeicherten Einverständnisvoreinstellungen pro Person und erzwingt diese zum Zeitpunkt des Nachrichtenversands für E-Mail-, SMS- und WhatsApp-Kanäle. Eine Person, die sich gegen einen Kanal entschieden hat, wird vom Versand ausgeschlossen, bevor Inhalte vom Kanal oder nachgelagerten Messaging-Anbieter gesendet werden.

Das Einverständnis wird zum Zeitpunkt des Versands mithilfe von XDM-Feldern aus der Feldergruppe „Profileinverständnis“ ausgewertet. Das standardmäßige Einverständnisverhalten unterscheidet sich je nach Kanal - E-Mail ist standardmäßig aktiviert, wenn keine Voreinstellung festgelegt ist, während SMS und WhatsApp standardmäßig deaktiviert sind.

Einzelheiten zu den für jeden Kanal ausgewerteten XDM-Attributen und deren Standardverhalten finden Sie unter [Einverständnisvoreinstellungen](../content/channels-consent-preferences.md).

## Zurücksetzen der Sandbox

Das Zurücksetzen von Sandboxes **für Adobe Journey Optimizer B2B edition** derzeit nicht unterstützt. Das Zurücksetzen oder Löschen einer Journey Optimizer B2B edition zugeordneten Sandbox kann zu dauerhaftem Datenverlust führen und die Bereitstellung einer neuen Instanz erfordern.

## Noch nicht verfügbar

Die folgenden Governance-Funktionen sind noch nicht verfügbar:

* Durchsetzung von Datennutzungskennzeichnungen (DULE)/Nutzungsrichtlinien
* Datenhygiene
* Einverständniserklärungen
* Zugriffskontrolle auf Feldebene (FLAC)
* Zugriffssteuerung auf Objektebene (OLAC)
* CMK-Verschlüsselung für Daten im Ruhezustand
* Platform-Audits-Service
