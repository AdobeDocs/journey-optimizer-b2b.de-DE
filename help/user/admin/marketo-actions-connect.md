---
title: Aktivieren von Marketo Engage zur Unterstützung von Journey-Aktionen
description: Aktivieren Sie Marketo Engage-Verbindungen, um Journey-Aktionen zu unterstützen, damit Marketer Kampagnen zwischen Marketo Engage und Journey Optimizer B2B edition koordinieren können.
feature: Integrations, Audiences, Buying Groups
role: User, Admin
source-git-commit: de7f5620556a48fe6f12ed1c70e925e11ec770f1
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 2%

---


# Aktivieren von Marketo Engage-Instanzen zur Unterstützung von Aktionen

Marketo Engage-Aktionen sind _personenbasierte_ Aktionen, mit denen Sie Ihre _Account-basierte_ Marketing-Orchestrierung zwischen Journey Optimizer B2B edition und Ihren _Lead-basierten_ Marketing-Maßnahmen in Marketo Engage koordinieren können. Verwenden Sie diese Aktionen, um die Mitgliedschaft in statischen Listen zu orchestrieren und Personen in Kampagnen zu platzieren.

Um Marketo Engage-Aktionen zu verwenden, erstellt ein Administrator zunächst einen [benutzerdefinierten Service](https://experienceleague.adobe.com/de/docs/marketo-developer/marketo/rest/custom-services#) in Marketo Engage, der die für die Authentifizierung erforderlichen Anmeldeinformationen bereitstellt.
Anschließend erstellt ein Produktadministrator für Journey Optimizer B2B edition eine Verbindung zu Marketo Engage, indem er die Anmeldeinformationen eingibt.
Journey Optimizer B2B edition-Benutzer können dann auf die Verbindung verweisen, um Marketo Engage-Aktionen in <!-- Person and -->Account-Journey zu konfigurieren, z. B. Personen zu Marketo Engage-Listen hinzuzufügen oder daraus zu entfernen oder sie zu Anfragekampagnen hinzuzufügen.

Die Sichtbarkeit von Marketo Engage Workspace für Assets, z. B. Listen und Kampagnen, wird durch die im benutzerdefinierten Service zugewiesenen Rollenberechtigungen gesteuert.

Dieselbe Verbindung kann mehrmals auf einer Journey verwendet werden, und verschiedene Marketo Engage-Verbindungen können auf einer einzigen Journey nebeneinander bestehen.

Wenn eine Aktion ausgeführt wird, verwendet sie die Auswahlrichtlinie, um zu bestimmen, welche Personendatensätze in Marketo Engage ausgewählt werden sollen, wenn mehrere Kennungen im einheitlichen Personenprofil vorhanden sind. Zu den Optionen gehören die Auswahl des ältesten, neuesten oder aller passenden Marketo Engage-Datensätze. Personen durchlaufen die Journey unabhängig von einer Übereinstimmung, es sei denn, es tritt ein Fehler auf.

## Konfigurieren einer Marketo Engage-Verbindung

Konfigurieren Sie eine Remote-Marketo Engage-Instanz zur Verwendung mit Marketo Engage-Journey-Aktionen.

### Erstellen des benutzerdefinierten Marketo Engage-Service

1. Melden Sie sich bei Marketo Engage als Administrator an und erstellen Sie einen benutzerdefinierten Service.
1. Notieren Sie sich die folgenden Werte für die Verbindung:

   * Munchkin-ID
   * Client-ID
   * Client-Geheimnis

### Integration hinzufügen

![Integrationsdetails hinzufügen](assets/integration-connection-details.png)

1. Navigieren Sie in Journey Optimizer B2B edition zu **Administration** > **Konfigurationen**.
1. Wählen Sie auf der Registerkarte **Integrationen** aus.
1. Klicken Sie **[!UICONTROL Verbindung erstellen]**.
1. Geben Sie einen Namen (erforderlich) und eine Beschreibung (optional) ein.
1. Wählen Sie eine **Auswahlrichtlinie** für übereinstimmende Personendatensätze aus.
1. Geben Sie Ihre Munchkin-ID, Client-ID und Ihr Client-Geheimnis ein.
1. Klicken Sie **[!UICONTROL Mit Marketo verbinden]**.
1. Klicken Sie auf **[!UICONTROL Erstellen]**.

Wenn ein Marketer eine Marketo Engage-Aktion auf einer Journey verwendet, kann er den Knoten mithilfe des Verbindungsnamens konfigurieren.

Nach abgeschlossener Integration sind Marketo Engage-Aktionen unter **Aktionen auf:** in den Knoteneigenschaften verfügbar.

![Marketo-Aktionsliste](assets/marketo-actions-list.png)