---
title: Governance-Funktionen
description: Erfahren Sie mehr über Governance-Funktionen, die derzeit in Journey Optimizer B2B Edition verfügbar sind.
source-git-commit: 1353defe804947617a4d7489592d380bf372c7df
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 1%

---

# Governance-Funktionen

Als integrierte Adobe Experience Platform-App verwendet Journey Optimizer B2B Edition mehrere Dienste und Tools, mit denen Sie Ihre erfassten Erlebnisdaten sicher steuern können, um Ihre Geschäftspraktiken, rechtlichen Verpflichtungen und Entwicklungsprozesse einzuhalten. Die folgenden Abschnitte enthalten eine Zusammenfassung dieser einzelnen Governance-Funktionen.

## Datenschutz - DSGVO

Journey Optimizer B2B Edition verwendet die bestehenden Marketo Engage DSGVO-Governance-Funktionen, die vom Privacy Service und Marketo Privacy Broker Service bereitgestellt werden.

## Rollenbasierte Zugriffssteuerung (RBAC)

Mit Journey Optimizer B2B Edition und Zugriff auf Adobe Admin Console können Administratoren einem Entitätstyp Benutzerberechtigungen erteilen (Anzeigen von Segmenten, Verwalten von Segmenten, Verwalten von Journey usw.). Diese Funktion ist Teil des Unified Permissions Framework (UPF), das es allen Adobe Experience Platform-Kunden ermöglicht, Rollen und Berechtigungen für ihre Organisation zu definieren und zu verwalten.

## Datenverschlüsselung

**_Verschlüsselung für ruhende Daten_** - Alle von Adobe Experience Platform in Journey Optimizer B2B Edition übertragenen Konto- und Personenprofildaten werden verschlüsselt, um die Einhaltung der bestehenden Experience Platform-Anforderungen zu gewährleisten. Alle Entitäten mit Ursprung in Journey Optimizer B2B Edition, wie Journey und Einkaufsgruppen, werden ebenfalls verschlüsselt.

**_Verschlüsselung für Daten während der Übertragung_** (über ein öffentliches Netzwerk) - Alle Journey Optimizer B2B Edition-APIs und -Entitäten werden bei der Übertragung mit TLS 1.2 verschlüsselt.

## Einverständniserklärung/Opt-out

Die Zustimmung zum Opt-in/Opt-out ist eine Form der Governance, bei der ein Profil von einem Kommunikationskanal, wie E-Mail oder SMS, abgemeldet werden kann und ein Profil dann aus diesem Kommunikationskanal ausgeschlossen werden sollte.

Mit Journey Optimizer B2B Edition können Sie Anwendungsfälle für den Abonnieren/Abmelden für E-Mail- und SMS-Versand erstellen und verwalten. Diese Zustimmungsvoreinstellungen werden in der Feldergruppe &quot;XDM Profile Consent Field&quot;gespeichert und im Rahmen des Data Sync Framework in und aus Journey Optimizer B2B Edition synchronisiert. Diese Voreinstellungen werden zum Zeitpunkt des Versands verwendet, um abgemeldete Profile aus Sendungen auszuschließen.

## Noch nicht verfügbar

Die folgenden Governance-Funktionen sind noch nicht verfügbar, sind jedoch in der Produkt-Roadmap enthalten:

* Durchsetzung der Datennutzungsbezeichnung (DULE)/Nutzungsrichtlinien
* Datenhygiene
* Zurücksetzen der Sandbox
* Einverständnisrichtlinien
* Zugriffskontrolle auf Feldebene (FLAC)
* Zugriffskontrolle auf Objektebene (OLAC)
* CMK-Verschlüsselung für ruhende Daten
* Plattform-Auditdienst
