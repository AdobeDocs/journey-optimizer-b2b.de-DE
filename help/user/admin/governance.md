---
title: Governance-Funktionen
description: Erfahren Sie mehr über Governance-Funktionen, die derzeit in Journey Optimizer B2B edition verfügbar sind.
exl-id: 2845272b-987c-4a37-adf4-6ee5bfd59fc0
source-git-commit: 8c191cd86a9aa9e7094b7d3464b3179cfdb4789e
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 3%

---

# Governance-Funktionen

Als integrierte Adobe Experience Platform-App nutzt Journey Optimizer B2B edition verschiedene Services und Tools, mit denen Sie Ihre erfassten Erlebnisdaten sicher kontrollieren können, um Ihre Geschäftspraktiken, rechtlichen Verpflichtungen und Entwicklungsprozesse zu erfüllen. Die folgenden Abschnitte enthalten eine Zusammenfassung jeder dieser Governance-Funktionen.

## Datenschutz - DSGVO

Journey Optimizer B2B edition verwendet die vorhandenen Marketo Engage-DSGVO-Governance-Funktionen, die vom Privacy Service und Marketo Privacy Broker Service bereitgestellt werden.

## Rollenbasierte Zugriffskontrolle (RBAC)

Mit Journey Optimizer B2B edition und Zugriff auf Adobe Admin Console können Admins einem Benutzer Berechtigungen für einen Entitätstyp erteilen (Anzeigen von Segmenten, Verwalten von Segmenten, Verwalten von Journey-Segmenten usw.). Diese Funktion ist Teil des Unified Permissions Framework (UPF), mit dem alle Adobe Experience Platform-Kunden Rollen und Berechtigungen für ihr Unternehmen definieren und verwalten können.

## Datenverschlüsselung

**_Verschlüsselung ruhender Daten_** - Alle von Adobe Experience Platform in Journey Optimizer B2B edition übertragenen Konto- und Personenprofildaten werden verschlüsselt, um die bestehende Konformität von Experience Platform beizubehalten. Alle Entitäten mit Ursprung in Journey Optimizer B2B edition, z. B. Journeys und Einkaufsgruppen, werden ebenfalls verschlüsselt.

**_Verschlüsselung von Daten bei der Übertragung_** (über ein öffentliches Netzwerk): Alle Journey Optimizer B2B edition-APIs und -Entitäten werden während der Übertragung mit TLS 1.2 verschlüsselt.

## Opt-in/Opt-out für Einverständnis

Das Einverständnis-Opt-in/Opt-out ist eine Form der Governance, bei der ein Profil sich von einem Kommunikationskanal wie E-Mail oder SMS abmelden kann und ein Profil dann aus diesem Kommunikationskanal ausgeschlossen werden sollte.

Mit Journey Optimizer B2B edition können Sie Anwendungsfälle für E-Mail- und SMS-Sendungen erstellen und verwalten, bei denen sich Benutzende abmelden oder abmelden können. Diese Einverständnisvoreinstellungen werden in der Feldergruppe „XDM-Profileinverständnis“ gespeichert und im Rahmen des Datensynchronisierungs-Frameworks mit Journey Optimizer B2B edition synchronisiert und daraus entfernt. Diese Voreinstellungen werden zur Versandzeit verwendet, um abgemeldete Profile von Sendungen auszuschließen.

## Noch nicht verfügbar

Die folgenden Governance-Funktionen sind noch nicht verfügbar:

* Durchsetzung von Datennutzungskennzeichnungen (DULE)/Nutzungsrichtlinien
* Datenhygiene
* Zurücksetzen der Sandbox
* Einverständniserklärungen
* Zugriffskontrolle auf Feldebene (FLAC)
* Zugriffssteuerung auf Objektebene (OLAC)
* CMK-Verschlüsselung für Daten im Ruhezustand
* Platform-Audits-Service
