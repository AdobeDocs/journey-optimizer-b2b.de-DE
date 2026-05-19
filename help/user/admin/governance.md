---
title: Governance-Funktionen
description: Erfahren Sie mehr über Governance-Funktionen, die derzeit in Journey Optimizer B2B edition verfügbar sind.
feature: Setup
role: Admin
exl-id: 2845272b-987c-4a37-adf4-6ee5bfd59fc0
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: d6e625c1-468f-4d73-9f32-fd1edb87f96bid: f2da1b69-6919-4386-a5d2-9c7b5c9033db
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
autotag-review: 2026-03-27T23:18:44.352Z
TQID: https://experienceleague.adobe.com/PwH34suDPc84nB9eiAWtrkVzsOw82RRGw4hrRogf9zE
source-git-commit: 94a8ed9584459cf85a72448cd698740ef450ddb2
workflow-type: tm+mt
source-wordcount: 418
ht-degree: 3%

---

# Governance-Funktionen

Journey Optimizer B2B edition ist eine integrierte Adobe Experience Platform-App. Sie verwendet mehrere Tools und Services, die die Kontrolle über Ihre erfassten Erlebnisdaten in Übereinstimmung mit Ihren Geschäftspraktiken, rechtlichen Verpflichtungen und Entwicklungsprozessen ermöglichen. Die folgenden Abschnitte enthalten eine Zusammenfassung jeder dieser Governance-Funktionen.

## Datenschutz - DSGVO

Journey Optimizer B2B edition verwendet die vorhandenen Marketo Engage-DSGVO-Governance-Funktionen, die von Privacy Service und Marketo Privacy Broker Service bereitgestellt werden.

## Rollenbasierte Zugriffskontrolle (RBAC)

Mit Journey Optimizer B2B edition und Zugriff auf Adobe Admin Console können Admins einem Benutzer Berechtigungen für einen Entitätstyp erteilen (Anzeigen von Segmenten, Verwalten von Segmenten, Verwalten von Journey-Segmenten usw.). Diese Funktion ist Teil des Unified Permissions Framework (UPF), mit dem alle Adobe Experience Platform-Kunden Rollen und Berechtigungen für ihr Unternehmen definieren und verwalten können.

## Datenverschlüsselung

**_Verschlüsselung ruhender Daten_** - Alle von Adobe Experience Platform in Journey Optimizer B2B edition übertragenen Konto- und Personenprofildaten werden verschlüsselt, um die bestehende Konformität von Experience Platform aufrechtzuerhalten. Alle Entitäten mit Ursprung in Journey Optimizer B2B edition, z. B. Journeys und Einkaufsgruppen, werden ebenfalls verschlüsselt.

**_Verschlüsselung von Daten bei der Übertragung_** (über ein öffentliches Netzwerk): Alle Journey Optimizer B2B edition-APIs und -Entitäten werden während der Übertragung mit TLS 1.2 verschlüsselt.

## Opt-in/Opt-out für Einverständnis

Journey Optimizer B2B edition liest die in den XDM-Profilen von Adobe Experience Platform gespeicherten Einverständnisvoreinstellungen pro Person und erzwingt diese zum Zeitpunkt des Nachrichtenversands für E-Mail-, SMS- und WhatsApp-Kanäle. Personen, die sich gegen einen Kanal entschieden haben, werden vom Versand ausgeschlossen, bevor Inhalte vom Kanal oder nachgelagerten Messaging-Anbieter gesendet werden.

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
