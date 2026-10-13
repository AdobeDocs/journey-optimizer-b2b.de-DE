---
title: Datensatzabfragen
description: Erfahren Sie, wie Sie SQL-Abfragebeispiele in Query Service verwenden, um von Adobe Journey Optimizer B2B Edition exportierte Konto-, Einkaufsgruppen-, Personen- und Journey-Daten zu analysieren.
feature: Reporting, Data Management
role: Admin, Developer
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
    internal-label: Experience Platform
feature_v2:
  - id: f2da1b69-6919-4386-a5d2-9c7b5c9033db
    internal-label: Data management
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
    internal-label: Data integration
source-git-commit: 6db81a0b993f450a3ff448dcb4c417e3e81ec70a
workflow-type: tm+mt
source-wordcount: '844'
ht-degree: 1%
---

# Datensatzabfragen

Finden Sie einsatzbereite SQL-Abfragebeispiele für die Analyse der Konto-, Personen-, Einkaufsgruppen- und Journey-Daten, die [!DNL Adobe Journey Optimizer B2B Edition] nach [!DNL Adobe Experience Platform] exportiert. Führen Sie die Abfragen in [!DNL Query Service] aus, um Berichte zu Konten, Einkaufsgruppen, E-Mail-Interaktionen und Journey-Aktivitäten zu erstellen.

Beschreibungen der in diesen Abfragen verwendeten Datensätze und Felder finden Sie unter [Exportierte Datensätze](./aep-exported-datasets.md).

## Voraussetzungen {#prerequisites}

Bevor Sie eine Abfrage auf dieser Seite ausführen, stellen Sie Folgendes sicher:

* **Zugriff auf [!DNL Query Service]:** Sie müssen Zugriff auf [Abfrage-Service](https://experienceleague.adobe.com/de/docs/experience-platform/query/home){target="_blank"} in Ihrer [!DNL Experience Platform] Sandbox haben.
* **Verfügbare Datensätze:** Abfragen zielen auf die exportierten [!DNL Journey Optimizer B2B Edition] ab. Wechseln Sie in Ihrer Sandbox zu **[!UICONTROL Datensätze]** und überprüfen Sie, ob die Datensätze vorhanden sind und Daten enthalten.
* **Schemafeldwerte:** Stellen Sie sicher, dass die Felder in Ihren Abfragen Werte im entsprechenden Schema enthalten. Leere Felder geben keine Ergebnisse zurück und erzeugen keine Fehler.

>[!NOTE]
>
>Die Beispiele verwenden kurze Tabellennamen wie `account_table` und `person_activity_table`. Ersetzen Sie jeden Tabellennamen durch den Namen des entsprechenden Datensatzes in Ihrer Sandbox. Wenn ein Datensatzname Bindestriche enthält, setzen Sie ihn in doppelte Anführungszeichen. Ersetzen Sie Platzhalterwerte wie `Example Company` und `PASTE_COMPLETE_JOURNEY_ID_HERE` durch Werte aus Ihrer Umgebung.

## Ausführen einer Abfrage {#run}

So führen Sie ein Beispiel auf dieser Seite aus:

1. Wählen Sie in [!DNL Experience Platform] **[!UICONTROL Abfrage-Service]** > **[!UICONTROL Abfragen]** aus.
1. Fügen Sie das Beispiel in den Abfrage-Editor ein und ersetzen Sie dann die Tabellennamen und Platzhalterwerte.
1. Wählen Sie **[!UICONTROL Ausführen]** aus.

Die Beispiele, die nach Datum filtern, verwenden die letzten 30 Tage. Um den Zeitbereich zu ändern, bearbeiten Sie den `INTERVAL '30' DAY`.

## Abfrage auswählen

Verwenden Sie die folgende Tabelle, um eine Abfrage für Ihre Berichtsaufgabe auszuwählen.

| Ich möchte | Aufrufen |
|---|---|
| Überprüfen von Kontonamen, Branchen und Standorten | [Überprüfen der Kontodetails](#account-details) |
| Einkaufsgruppen nach Interaktion vergleichen | [Einkaufsgruppeninteraktion vergleichen](#buying-group-engagement) |
| Personen suchen, die mit einem Konto verknüpft sind | [Personen in einem Konto suchen](#account-people) |
| Änderungen am Einkaufsgruppenstatus verfolgen | [Änderungen des Einkaufsgruppenstatus überprüfen](#buying-group-status-changes) |
| Personen finden, die auf eine E-Mail geklickt haben | [Personen finden, die auf eine E-Mail geklickt haben](#email-clicks) |
| Vergleichen der letzten Aktivitäten nach Typ | [Aktuelle Personenaktivität vergleichen](#person-activity) |
| Journey des Kontos nach Größe vergleichen | [Kontoanzahl nach Journey vergleichen](#account-journey-counts) |
| Auflisten der Konten auf einer Journey | [Listen Sie Konten in einer Journey auf](#journey-accounts) |
| Tägliche Konto-Journey-Aktivität verfolgen | [Tägliche Kontoaktivität verfolgen](#account-daily-activity) |
| Untersuchen des Verlaufs eines Accounts in einer Journey | [Überprüfen der Zeitleiste für die Journey eines Kontos](#account-timeline) |
| Journey von Personen nach Größe und Status vergleichen | [Personenzahlen nach Journey vergleichen](#person-journey-counts) |
| Personen in einer Journey auflisten | [Personen in einer Journey auflisten](#journey-people) |
| Anzeigen, wo sich Personen auf einer Journey befinden | [Personenzahlen schrittweise vergleichen](#person-step-counts) |
| Verfolgen der letzten Journey-Aktivität einer Person | [Verfolgen der letzten Journey-Aktivität](#person-journey-activity) |
| Untersuchen des Verlaufs einer Person in einem Journey | [Zeitleiste für das Journey einer Person überprüfen](#person-timeline) |

## Konto- und Einkaufsgruppenabfragen

Verwenden Sie diese Abfragen, um die Konten, Einkaufsgruppen und für das Reporting verfügbaren Personen zu überprüfen.

### Überprüfen der Kontodetails {#account-details}

Überprüfen Sie Kontonamen, Branchen, Standorte und Unternehmensgrößen, um die für das Reporting verfügbaren Konten zu verstehen.

```sql
SELECT
a._id AS accountID,
a.accountName,
a.industry,
a.country,
a.numberOfEmployees
FROM account_table a
WHERE a.isDeleted = FALSE
ORDER BY a.accountName
LIMIT 100;
```

### Einkaufsgruppeninteraktion vergleichen {#buying-group-engagement}

Vergleichen Sie Einkaufsgruppen nach aufgezeichnetem Interaktionswert sowie Vollständigkeit und Interesse an der Lösung.

```sql
SELECT
bg._id AS buyingGroupID,
bg.buyingGroupName,
bg.engagementScore,
bg.completenessScore,
bg.solutionInterest,
bg.buyingGroupStatus
FROM buying_group_table bg
WHERE bg.isDeleted = FALSE
ORDER BY bg.engagementScore DESC NULLS LAST, bg.buyingGroupName
LIMIT 100;
```

### Personen in einem Konto suchen {#account-people}

Finden Sie die Personen und Stellenbezeichnungen, die mit einem Konto verknüpft sind, um dessen Kontakte zu verstehen. Ersetzen Sie `Example Company` durch einen Kontonamen aus Ihrer Sandbox.

```sql
SELECT DISTINCT
a._id AS accountID,
a.accountName,
p._id AS personID,
p.firstName,
p.lastName,
p.email,
p.jobTitle
FROM account_member_table m
JOIN account_table a ON m.accountID = a._id
JOIN person_table p ON m.personID = p._id
WHERE m.isDeleted = FALSE
AND a.isDeleted = FALSE
AND p.isDeleted = FALSE
AND a.accountName = 'Example Company'
ORDER BY p.lastName, p.firstName
LIMIT 100;
```

### Änderungen des Einkaufsgruppenstatus überprüfen {#buying-group-status-changes}

Überprüfen Sie die Änderungen des Einkaufsgruppenstatus in den letzten 30 Tagen, um zu verstehen, wie sich die Gruppen im Laufe der Zeit ändern.

```sql
SELECT
bg._id AS buyingGroupID,
bg.buyingGroupName,
e.timestamp AS changedAt,
e.newStatus
FROM buying_group_event_table e
JOIN buying_group_table bg ON e.buyingGroupID = bg._id
WHERE bg.isDeleted = FALSE
AND e.eventType = 'buyingGroup.changeStatus'
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
ORDER BY e.timestamp DESC
LIMIT 100;
```

## Personeninteraktionsabfragen

Verwenden Sie diese Abfragen, um E-Mail-Interaktionen und andere aufgezeichnete Personenaktivitäten zu überprüfen.

### Personen finden, die auf eine E-Mail geklickt haben {#email-clicks}

Um die aktuelle E-Mail-Interaktion zu überprüfen, identifizieren Sie Personen mit aufgezeichneten E-Mail-Klicks in den letzten 30 Tagen.

```sql
SELECT DISTINCT
p._id AS personID,
p.firstName,
p.lastName,
p.email
FROM person_activity_table e
JOIN person_table p ON e.personID = p._id
WHERE e.isDeleted = FALSE
AND p.isDeleted = FALSE
AND e.eventType = 'directMarketing.emailClicked'
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
ORDER BY p.lastName, p.firstName
LIMIT 100;
```

### Aktuelle Personenaktivität vergleichen {#person-activity}

Vergleichen Sie aufgezeichnete Aktivitätstypen und die Anzahl der beteiligten Personen, um die jüngste Interaktion zu verstehen.

```sql
SELECT
e.eventType,
COUNT(*) AS recordedRows,
COUNT(DISTINCT e.personID) AS distinctPeople
FROM person_activity_table e
WHERE e.isDeleted = FALSE
AND e.personID IS NOT NULL
AND e.personID <> ''
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
GROUP BY e.eventType
ORDER BY recordedRows DESC
LIMIT 100;
```

## Account Journey Queries

Verwenden Sie diese Abfragen, um Account Journey zu analysieren. Ersetzen Sie `PASTE_COMPLETE_JOURNEY_ID_HERE` durch den `_id` des Konto-Journey und `PASTE_COMPLETE_ACCOUNT_ID_HERE` durch den `_id` des Kontos.

### Kontoanzahl nach Journey vergleichen {#account-journey-counts}

Vergleichen Sie Account-Journey nach Status und aufgezeichneter Mitgliederzahl, um zu sehen, welche Journey die größten Account-Populationen haben.

```sql
SELECT
j._id AS journeyID,
j.accountJourneyName,
j.accountJourneyStatus,
COUNT(DISTINCT m.accountID) AS accountsWithRecordedMembership
FROM account_journey_table j
LEFT JOIN account_journey_member_table m
ON m.journeyID = j._id
AND m.isDeleted = FALSE
AND m.accountID <> ''
WHERE j.isDeleted = FALSE
GROUP BY j._id, j.accountJourneyName, j.accountJourneyStatus
ORDER BY accountsWithRecordedMembership DESC, j.accountJourneyName
LIMIT 100;
```

### Auflisten von Konten auf einer Journey {#journey-accounts}

Überprüfen Sie die mit einer bestimmten Journey verbundenen Konten, einschließlich ihrer Branchen und Länder.

```sql
SELECT DISTINCT
a._id AS accountID,
a.accountName,
a.industry,
a.country
FROM account_journey_member_table m
JOIN account_table a ON m.accountID = a._id
WHERE m.isDeleted = FALSE
AND a.isDeleted = FALSE
AND m.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
ORDER BY a.accountName, accountID
LIMIT 100;
```

### Tägliche Kontoaktivität verfolgen {#account-daily-activity}

Verfolgen Sie tägliche Kontohinzufügungen, -entfernungen und Schrittänderungen, um die Aktivitäten auf einer Journey in den letzten 30 Tagen zu verstehen.

```sql
SELECT
CAST(e.timestamp AS DATE) AS activityDate,
e.eventType,
COUNT(*) AS recordedRows,
COUNT(DISTINCT e.accountID) AS distinctAccounts
FROM account_activity_table e
WHERE e.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
AND e.accountID IS NOT NULL
AND e.accountID <> ''
AND e.eventType IN (
'account.addAccountToJourney',
'account.removeAccountFromJourney',
'account.changeAccountJourneyNode'
)
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
GROUP BY CAST(e.timestamp AS DATE), e.eventType
ORDER BY activityDate DESC, e.eventType
LIMIT 100;
```

### Überprüfen der Zeitleiste für die Journey eines Kontos {#account-timeline}

Untersuchen Sie den aktuellen Journey-Verlauf eines Accounts, indem Sie seine aufgezeichneten Events und Journey-Schritte überprüfen.

```sql
SELECT
e.timestamp AS activityAt,
e.eventType,
e.journeyNodeID,
n.nodeType,
e.previousJourneyNodeID,
e.buyingGroupID
FROM account_activity_table e
LEFT JOIN account_journey_node_table n
ON e.journeyNodeID = n._id
AND e.journeyID = n.accountJourneyID
AND n.isDeleted = FALSE
WHERE e.accountID = 'PASTE_COMPLETE_ACCOUNT_ID_HERE'
AND e.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
ORDER BY e.timestamp DESC
LIMIT 100;
```

## Personen-Journey-Abfragen

Verwenden Sie diese Abfragen, um Personen-Journey zu analysieren. Ersetzen Sie `PASTE_COMPLETE_JOURNEY_ID_HERE` durch den `_id` der Personen-Journey und `PASTE_COMPLETE_PERSON_ID_HERE` durch den `_id` der Person.

### Personenzahlen nach Journey vergleichen {#person-journey-counts}

Vergleichen Sie die Journey der Person nach Anzahl, Status und Datum der aufgezeichneten Mitgliedschaft, um ihre Größe und ihren Lebenszyklus zu verstehen.

```sql
SELECT
j._id AS journeyID,
j.personJourneyName,
j.personJourneyStatus,
j.startDate,
j.endDate,
COUNT(DISTINCT m.personID) AS peopleWithRecordedMembership
FROM person_journey_table j
LEFT JOIN person_journey_member_table m
ON m.journeyID = j._id
AND m.isDeleted = FALSE
AND m.personID <> ''
WHERE j.isDeleted = FALSE
GROUP BY
j._id,
j.personJourneyName,
j.personJourneyStatus,
j.startDate,
j.endDate
ORDER BY peopleWithRecordedMembership DESC, j.personJourneyName
LIMIT 100;
```

### Personen in einer Journey auflisten {#journey-people}

Überprüfen Sie, wer mit einer Journey in Verbindung steht, wann sie zuletzt eingetreten ist und wie oft sie eingetreten sind.

```sql
SELECT DISTINCT
m.personID,
p.firstName,
p.lastName,
p.email,
m.membershipDate,
m.lastEntryDate,
m.entryCount,
m.reentryOpensAt,
m.journeyNodeID
FROM person_journey_member_table m
LEFT JOIN person_table p
ON m.personID = p._id
AND p.isDeleted = FALSE
WHERE m.isDeleted = FALSE
AND m.personID IS NOT NULL
AND m.personID <> ''
AND m.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
ORDER BY m.lastEntryDate DESC NULLS LAST, m.personID
LIMIT 100;
```

### Personenzahlen schrittweise vergleichen {#person-step-counts}

Sehen Sie, wie die Personen über die in ihren Journey-Mitgliedschaften aufgezeichneten Schritte verteilt sind.

```sql
SELECT
m.journeyNodeID,
n.nodeType,
COUNT(DISTINCT m.personID) AS peopleWithRecordedStep
FROM person_journey_member_table m
LEFT JOIN person_journey_node_table n
ON m.journeyNodeID = n._id
AND m.journeyID = n.personJourneyID
AND n.isDeleted = FALSE
WHERE m.isDeleted = FALSE
AND m.personID IS NOT NULL
AND m.personID <> ''
AND m.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
GROUP BY m.journeyNodeID, n.nodeType
ORDER BY peopleWithRecordedStep DESC, m.journeyNodeID
LIMIT 100;
```

### Nachverfolgen der letzten Journey-Aktivität {#person-journey-activity}

Vergleichen Sie Beginn, Ende und Transitionen einer aufgezeichneten Journey, um die Aktivität der Personen auf einer Journey in den letzten 30 Tagen zu verstehen.

```sql
SELECT
e.eventType,
COUNT(*) AS recordedRows,
COUNT(DISTINCT e.personID) AS distinctPeople
FROM person_activity_table e
WHERE e.isDeleted = FALSE
AND e.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
AND e.personID IS NOT NULL
AND e.personID <> ''
AND e.eventType IN (
'person.journeyAdd',
'person.journeyRemove',
'person.journeyStart',
'person.journeyEnd',
'person.journeyNodeTransition',
'person.journeySplitNode'
)
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
GROUP BY e.eventType
ORDER BY recordedRows DESC, e.eventType
LIMIT 100;
```

### Überprüfen der Zeitleiste für das Journey einer Person {#person-timeline}

Untersuchen Sie den aktuellen Journey-Verlauf einer Person, einschließlich Schrittübergängen, Aufspaltungsoptionen und Journey-zugewiesenen Profilaktualisierungen.

```sql
SELECT
e.timestamp AS activityAt,
e.eventType,
e.journeyNodeID,
e.previousJourneyNodeID,
e.newJourneyNodeID,
e.journeyChoiceNumber,
e.journeyEntryCount,
e.attributeName,
e.attributeOldValue,
e.attributeNewValue
FROM person_activity_table e
WHERE e.isDeleted = FALSE
AND e.personID = 'PASTE_COMPLETE_PERSON_ID_HERE'
AND e.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
ORDER BY e.timestamp DESC
LIMIT 100;
```
