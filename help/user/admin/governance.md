---
title: Governance-Funktionen
description: Erfahren Sie mehr über Governance-Funktionen, die derzeit in Journey Optimizer B2B edition verfügbar sind.
feature: Setup
role: Admin
exl-id: 2845272b-987c-4a37-adf4-6ee5bfd59fc0
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 2%

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

Das Einverständnis-Opt-in/Opt-out ist eine Form der Governance, bei der ein Profil sich von einem Kommunikationskanal wie E-Mail oder SMS abmelden kann und ein Profil dann aus dem Kommunikationskanal ausgeschlossen wird.

Mit Journey Optimizer B2B edition können Sie Anwendungsfälle für E-Mail- und SMS-Sendungen erstellen und verwalten, bei denen sich Benutzende abmelden oder abmelden können. Diese Einverständnisvoreinstellungen werden in der Feldergruppe „XDM-Profileinverständnis“ gespeichert und im Rahmen des Datensynchronisierungs-Frameworks mit Journey Optimizer B2B edition synchronisiert und daraus entfernt. Diese Voreinstellungen werden zur Versandzeit verwendet, um abgemeldete Profile von Sendungen auszuschließen.

## Zurücksetzen der Sandbox

Das Zurücksetzen von Sandboxes **für Adobe Journey Optimizer B2B edition** derzeit nicht unterstützt. Das Zurücksetzen oder Löschen einer Sandbox, die Journey Optimizer B2B edition zugeordnet ist, kann zu dauerhaftem Datenverlust in Journey Optimizer B2B edition führen und könnte die Bereitstellung einer neuen Journey Optimizer B2B edition-Instanz erfordern.

## Noch nicht verfügbar

Die folgenden Governance-Funktionen sind noch nicht verfügbar:

* Durchsetzung von Datennutzungskennzeichnungen (DULE)/Nutzungsrichtlinien
* Datenhygiene
* Einverständniserklärungen
* Zugriffskontrolle auf Feldebene (FLAC)
* Zugriffssteuerung auf Objektebene (OLAC)
* CMK-Verschlüsselung für Daten im Ruhezustand
* Platform-Audits-Service
