---
title: Exportierte Experience Platform-Datensätze
description: Referenz für die Adobe Experience Platform-Datensatznamen und Schlüsselfeldpfade, die von Adobe Journey Optimizer B2B Edition exportiert wurden.
feature: Setup, Data Management
role: Admin
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
    internal-label: Experience Platform
feature_v2:
  - id: f2da1b69-6919-4386-a5d2-9c7b5c9033db
    internal-label: Data management
  - id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
    internal-label: Integrations
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
    internal-label: Data integration
autotag-review: '2026-09-29T00:00:00.000Z'
source-git-commit: 801025ee02617d56fc8ab933b59385bca38f5097
workflow-type: tm+mt
source-wordcount: '4845'
ht-degree: 7%
---

# [!DNL Experience Platform] Datensätze exportiert

[!DNL Adobe Journey Optimizer B2B Edition] stellt Informationen zu Konto, Person, Einkaufsgruppe und Journey in [!DNL Adobe Experience Platform] zur Verfügung. Ein Datensatz ist eine Sammlung verwandter Datensätze. Ein Personendatensatz beschreibt beispielsweise Personen, ein Mitgliedschaftsdatensatz verbindet Personen mit Konten oder Journey und ein Ereignisdatensatz zeichnet Aktionen auf, wie das Öffnen einer E-Mail.

Verwenden Sie dieses Handbuch, um zu verstehen, was jeder Datensatz enthält, was seine Felder bedeuten und wie sich verwandte Datensätze verbinden. Datensatznamen folgen diesem Muster:

**`AJOB2B-<datasetVersion>-<entity>`**

Hier werden `<entity>` Informationen wie `person`, `account_relational` oder `person_event` beschrieben. `<datasetVersion>` identifiziert die Version der Felddefinitionen des Datensatzes. Die Abschnittsüberschriften zeigen die dokumentierten Namen an; Ihre [!DNL Experience Platform] kann auch ältere Versionen enthalten.

Informationen zu den Namespaces und Schemata, die diese Exporte unterstützen, finden Sie unter [B2B-Namespaces und -Schemata](./namespaces-schemas.md).

>[!NOTE]
>
>Adobe behält ältere Datensatzversionen bei, um eine Unterbrechung der bestehenden Nutzung zu vermeiden. Daher finden Sie möglicherweise mehrere Versionen desselben Datensatzes in Ihrer Sandbox. Wenn Sie einen älteren Datensatz nicht mehr verwenden, können Sie ihn von Adobe entfernen lassen. Bevor Sie eine Entfernung anfordern, bestätigen Sie, dass der Datensatz nicht mehr verwendet wird.

## Lesen dieses Handbuchs

- **Feldname:** Der genaue Name, den Sie in [!DNL Experience Platform] sehen. Punkte trennen Ebenen innerhalb eines Felds, z. B. `consents.marketing.email.val`.
- **Datensatz-ID:** identifiziert den Datensatz in diesem Datensatz.
- **Beziehung:** benennt den Datensatz und das Feld, mit denen die Kennung übereinstimmt. Beispiel: `Matches AJOB2B-1_5_4-buying_group (_id)` bedeutet, dass sich das Feld auf den `_id` einer Einkaufsgruppe bezieht. Übereinstimmung mit der vollständigen Kennung; nicht kürzen oder versuchen, sie neu zu erstellen.
- **Standard-Adobe-Format** Verwendet die freigegebenen Felddefinitionen von Adobe.
- **Datensatzformat für verwandte Daten:** Organisiert Informationen als Datensätze, die mithilfe von übereinstimmenden Kennungen verbunden werden können.

Beispiel: `buying_group_member.buyingGroupID` stimmt mit `buying_group._id` überein, und sein `personID` stimmt mit `person_relational._id` oder dem `personKey.sourceKey` des Personendatensatzes überein. Diese Links helfen Ihnen zu verstehen, wer zu einer Einkaufsgruppe gehört. [!DNL Experience Platform] erstellt Berichte oder Zielgruppen nicht automatisch nur aus den Links.

Einige Kennungen beziehen sich auf Informationen, die in diesem Handbuch keinen separaten Datensatz enthalten, z. B. ein Marketing-Programm. In der Spalte Beziehung wird dies anstelle der Benennung eines Datensatzes, der hier nicht vorhanden ist, erwähnt.

`isDeleted` wird `true`, wenn der Datensatz als gelöscht markiert wird, und `false`, wenn dies nicht der Fall ist. Behandeln Sie sie nicht als allgemeines aktives Mitglied oder Einverständnisindikator. `lastUpdatedDate` beschreibt die letzte Datenaktualisierung des Datensatzes. Bei Ereignissen verwenden Sie `timestamp`, um zu verstehen, wann die Aktivität stattgefunden hat. Ein leeres Feld bedeutet, dass die Informationen nicht verfügbar sind oder nicht für diesen Datensatz gelten.

Die Datensätze mit verwandten Datensätzen verwenden Version `1_5_4`. Wenn ein Feld derzeit nicht ausgefüllt ist oder eine besondere Behandlung erfordert, wird im entsprechenden Abschnitt die für den Kunden sichtbare Einschränkung erläutert.

Eine Zielgruppe ist eine Gruppe von Personen, die ausgewählte Kriterien erfüllen. Die Verfügbarkeit der Zielgruppenerstellung hängt von Ihrer [!DNL Experience Platform] Einrichtung ab, um Informationen in Personenprofilen zu kombinieren. Das Vorhandensein eines Datensatzes in [!DNL Experience Platform] bedeutet für sich genommen nicht, dass er für die Segmentierung verfügbar ist.

## Auswählen eines Datensatzes

| Was Sie verstehen möchten | Datensätze, nach denen gesucht werden soll |
|---|---|
| Personen und ihre E-Mail-Voreinstellungen | `person` |
| Kontodetails und Kontaktdaten der Person | `account_relational`, `person_relational` |
| Welche Personen mit einem Konto verknüpft sind | `account_member`, `account_person` |
| Einkaufsgruppen, ihre Mitglieder und Statusänderungen | `buying_group`, `buying_group_member`, `buying_group_event` |
| Account Journey und teilnehmende Accounts | `account_journey`, `account_journey_member`, `account_event` |
| Personen-Journey und teilnehmende Personen | `person_journey`, `person_journey_member` |
| Schritte innerhalb eines Journey | `account_journey_node`, `person_journey_node`, `journey_node` |
| E-Mail, Web und andere unterstützte Personenaktivitäten | `person_event`, `person_event_relational` |

Die folgenden Abschnitte enthalten die vollständigen Datensatznamen und Felddetails. Eine Journey beschreibt das Gesamterlebnis, eine Mitgliedschaft verbindet eine Person oder ein Konto mit dieser Journey, ein Ereignis beschreibt etwas, das passiert ist.

+++Entitätsbeziehungsdiagramm

![Entitätsbeziehungsdiagramm für in [!DNL Adobe Experience Platform]](./assets/ajo-b2b-data-model.svg) exportierte Datensätze

+++

## `AJOB2B-1_5_1-person`

Jeder Datensatz beschreibt eine Person, ihre Kennungen und ihre E-Mail-Marketing-Voreinstellungen. Verwenden Sie es für Berichte auf Personenebene und, wenn das Profil konfiguriert ist, um Zielgruppen zu erstellen.

**format:** Standard-Adobe-Format

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `personID` | Datensatz-ID | Kennung für die Person. Verwenden Sie den vollständigen Wert, um verwandte Datensätze abzugleichen. |
| `personKey.sourceID` |  | Personenkennung im verbundenen System. |
| `personKey.sourceInstanceID` |  | Kennung der [!DNL Experience Platform] oder des verbundenen Kontos. |
| `personKey.sourceType` |  | Name des verbundenen Produkts. |
| `personKey.sourceKey` |  | Vollständige Personenkennung zum Abgleichen verwandter Datensätze. |
| `identityMap` |  | Andere Kennungen, mit denen [!DNL Experience Platform] dieselbe Person in Ihren verbundenen Daten erkennen können. |
| `consents.marketing.email.val` |  | E-Mail-Marketing-Voreinstellung: `n` gibt eine Abmeldung an; `y` zeigt an, dass in diesem Feld keine Abmeldung aufgezeichnet wurde. Dieses Feld allein begründet keine Berechtigung zum Senden von Marketing-E-Mails. |
| `consents.marketing.email.time` |  | Datum und Uhrzeit der letzten Aktualisierung der E-Mail-Voreinstellung. |
| `consents.marketing.email.reason` |  | Grund für die Abmeldung, sofern angegeben (nur festgelegt, wenn das Abonnement beendet wurde). |
| `isDeleted` |  | Ob dieser Personendatensatz als gelöscht markiert ist. |

>[!NOTE]
>
>Ihr Unternehmen verfügt möglicherweise über zusätzliche Personenfelder, die über die hier aufgeführten hinausgehen.

Wenn Ihr Unternehmen seine eigenen konfigurierten Konto- oder Personendatensätze verwendet, können diese Datensätze auch `isDeleted` enthalten. Siehe [Kundeneigene Datensätze](#customer-owned-datasets).

## `AJOB2B-1_5_4-account_member`

Jeder Datensatz verknüpft ein Konto mit einer Person. Verwenden Sie diesen Datensatz, um zu melden, welche Personen mit jedem Konto verknüpft sind. Er beschreibt die Beziehung und nicht eines der Profile.

**format:** Related-record format

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id` | Datensatz-ID | Kennung des Beziehungsdatensatzes. |
| `accountID` | Stimmt überein mit `AJOB2B-1_5_4-account_relational` (`_id`) | Kontokennung |
| `personID` | Stimmt überein mit `AJOB2B-1_5_4-person_relational` (`_id`) | Personenkennung. |
| `isDeleted` |  | Gibt an, ob dieser Datensatz als gelöscht markiert ist. |
| `lastUpdatedDate` |  | Zeit der letzten Änderung. |

## `AJOB2B-1_5_4-buying_group`

Jeder Datensatz beschreibt eine mit einem Konto verknüpfte Einkaufsgruppe, einschließlich ihres Namens, ihres Status, ihres Lösungsinteresses sowie ihrer Interaktions- und Vollständigkeitswerte. Die Phase der Einkaufsgruppe ist derzeit nicht ausgefüllt.

**format:** Related-record format

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id` | Datensatz-ID | Kauf-Gruppendatensatz-ID (verwenden Sie den vollständigen Wert). |
| `buyingGroupName` |  | Name der Einkaufsgruppe. |
| `engagementScore` |  | Interaktionswert. |
| `completenessScore` |  | Vollständigkeitswert. |
| `accountID` | Stimmt überein mit `AJOB2B-1_5_4-account_relational` (`_id`) | Kennung des zugehörigen Kontos. |
| `solutionInterest` |  | Bezeichnung für Lösungsinteresse. |
| `buyingGroupStatus` |  | Status. |
| `buyingGroupStage` |  | Name der Einkaufsgruppe. |
| `isDeleted` |  | Gibt an, ob dieser Datensatz als gelöscht markiert ist. |
| `lastUpdatedDate` |  | Zeit der letzten Änderung. |

>[!NOTE]
>
>**Hinweis zur Verfügbarkeit:** `buyingGroupStage` ist zurzeit leer. Verwenden Sie sie nicht, um Einkaufsgruppen nach Stadium zu filtern oder zu gruppieren.

## `AJOB2B-1_5_4-buying_group_member`

Jeder Datensatz verknüpft eine Person mit einer Einkaufsgruppe und zeichnet die Rolle dieser Person auf. Verwenden Sie diese Option, um die Zusammensetzung der Einkaufsgruppe und die Funktionsabdeckung zu melden.

`isDeleted` gibt nicht immer an, ob eine Person aus einer Einkaufsgruppe entfernt wurde. Verwenden Sie dieses Feld nicht allein, um die aktuelle Mitgliedschaft zu bestimmen. Der Rollenname kann leer sein, wenn keine Rolleninformationen verfügbar sind.

**format:** Related-record format

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id` | Datensatz-ID | Kennung des Mitgliedschaftsdatensatzes. |
| `buyingGroupID` | Stimmt überein mit `AJOB2B-1_5_4-buying_group` (`_id`) | Einkaufsgruppenkennung. |
| `personID` | Stimmt überein mit `AJOB2B-1_5_4-person_relational` (`_id`) | Personenkennung. |
| `buyingGroupMemberRole` |  | Rollenname, falls verfügbar. |
| `isDeleted` |  | Gibt an, ob dieser Datensatz als gelöscht markiert ist. |
| `lastUpdatedDate` |  | Zeit der letzten Änderung. |

## `AJOB2B-1_5_4-account_journey`

Jeder Datensatz beschreibt eine Konto-Journey mit dem Namen, dem Status sowie dem Start- und Enddatum. Hiermit können Sie den Lebenszyklus und den Status von Journey-Konten melden.

**format:** Related-record format

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id` | Datensatz-ID | Journey-Datensatz-ID (vollständigen Wert verwenden). |
| `accountJourneyName` |  | Journey. |
| `accountJourneyStatus` |  | Status (z. B. Entwurf, Live, Abgeschlossen). |
| `startDate` |  | Start timestamp. |
| `endDate` |  | Ende-Zeitstempel. |
| `isDeleted` |  | Gibt an, ob dieser Datensatz als gelöscht markiert ist. |
| `lastUpdatedDate` |  | Zeit der letzten Änderung. |

## `AJOB2B-1_5_4-account_journey_member`

Jeder Eintrag verbindet ein Konto mit einer Konto-Journey. Ermitteln Sie damit, welche Konten an den einzelnen Journey teilnehmen, und melden Sie diese an.

**format:** Related-record format

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id` | Datensatz-ID | Kennung des Mitgliedschaftsdatensatzes. |
| `accountID` | Stimmt überein mit `AJOB2B-1_5_4-account_relational` (`_id`) | Kontokennung |
| `journeyID` | Stimmt überein mit `AJOB2B-1_5_4-account_journey` (`_id`) | Kennung der Konto-Journey. |
| `isDeleted` |  | Gibt an, ob dieser Datensatz als gelöscht markiert ist. |
| `lastUpdatedDate` |  | Zeit der letzten Änderung. |

## `AJOB2B-1_5_4-person_journey`

Jeder Datensatz beschreibt eine Personen-Journey mit ihrem Namen, Status sowie Start- und Enddatum. Verwenden Sie sie, um den Lebenszyklus und den Status von Journey für personenorientierte Journey zu melden.

**format:** Related-record format

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id` | Datensatz-ID | Journey-Datensatz-ID (vollständigen Wert verwenden). |
| `personJourneyName` |  | Journey. |
| `personJourneyStatus` |  | Status (z. B. Entwurf, Live, Abgeschlossen). |
| `startDate` |  | Start timestamp. |
| `endDate` |  | Ende-Zeitstempel. |
| `isDeleted` |  | Gibt an, ob dieser Datensatz als gelöscht markiert ist. |
| `lastUpdatedDate` |  | Zeit der letzten Änderung. |

## `AJOB2B-1_5_4-person_journey_member`

Jeder Datensatz beschreibt die Zugehörigkeit einer Person zu einer Journey, einschließlich des aktuellen Journey-Knotens, der Zugehörigkeits- und Eingabedaten und der Anzahl der Einträge. Sie können damit den Fortschritt bei der Registrierung, der erneuten Eingabe und dem Journey melden.

**format:** Related-record format

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id` | Datensatz-ID | Kennung des Mitgliedschaftsdatensatzes. |
| `marketingProgramID` |  | Kennung des Marketing-Programms, zu dem die Journey gehört. |
| `personID` | Stimmt überein mit `AJOB2B-1_5_4-person_relational` (`_id`) | Personenkennung. |
| `journeyID` | Stimmt überein mit `AJOB2B-1_5_4-person_journey` (`_id`) | Journey-Kennung |
| `journeyNodeID` | Stimmt überein mit `AJOB2B-1_5_4-person_journey_node` (`_id`) | Kennung des Journey-Knotens, auf dem sich die Person derzeit befindet. |
| `membershipDate` |  | Wann die Person Mitglied des Marketing-Programms wurde. |
| `lastEntryDate` |  | Wann die Person die Journey zuletzt betreten hat. |
| `reentryOpensAt` |  | Wenn die Person die Journey erneut betreten kann. |
| `entryCount` |  | Anzahl, wie oft die Person die Journey betreten hat. |
| `createdDate` |  | Zeitpunkt der Erstellung des Datensatzes. |
| `updatedDate` |  | Zeitpunkt der letzten Änderung des Datensatzes. |
| `isDeleted` |  | Gibt an, ob dieser Datensatz als gelöscht markiert ist. |
| `lastUpdatedDate` |  | Zeit der letzten Änderung. |

## `AJOB2B-1_5_4-account_journey_node`

Jeder Datensatz beschreibt einen Schritt auf einer Journey, einschließlich der Art des Schritts und der Journey, zu der er gehört. Ein Journey-Knoten ist ein Schritt, z. B. ein Start, eine Wartezeit oder eine Entscheidung. Dieselben Schritte können in `person_journey_node` angezeigt werden. Ordnen Sie `accountJourneyID` einer Konto-Journey zu, bevor Sie einen Schritt als kontospezifisch behandeln.

**format:** Related-record format

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id` | Datensatz-ID | Knotensatz-ID (verwenden Sie den vollständigen Wert). |
| `accountJourneyID` | Stimmt überein mit `AJOB2B-1_5_4-account_journey` (`_id`) | Kennung der übergeordneten Journey. |
| `uuid` |  | Zusätzliche Kennung für den Journey-Schritt. |
| `journeyNodeTypeID` |  | Nummer, die den Typ des Journey-Schritts angibt. |
| `nodeType` |  | Titel, der den Typ des Journey-Schritts angibt. |
| `isDeleted` |  | Gibt an, ob dieser Datensatz als gelöscht markiert ist. |
| `createdDate` |  | Zeitpunkt der Erstellung des Datensatzes. |
| `lastUpdatedDate` |  | Zeit der letzten Änderung. |

## `AJOB2B-1_5_4-person_journey_node`

Jeder Datensatz beschreibt einen Schritt auf einer Journey, einschließlich der Art des Schritts und der Journey, zu der er gehört. Dieselben Schritte können in `account_journey_node` angezeigt werden. Ordnen Sie `personJourneyID` einer Personen-Journey zu, bevor Sie einen Schritt als personenspezifisch behandeln.

**format:** Related-record format

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id` | Datensatz-ID | Knotensatz-ID (verwenden Sie den vollständigen Wert). |
| `personJourneyID` | Stimmt überein mit `AJOB2B-1_5_4-person_journey` (`_id`) | Kennung der übergeordneten Journey. |
| `uuid` |  | Zusätzliche Kennung für den Journey-Schritt. |
| `journeyNodeTypeID` |  | Nummer, die den Typ des Journey-Schritts angibt. |
| `nodeType` |  | Titel, der den Typ des Journey-Schritts angibt. |
| `isDeleted` |  | Gibt an, ob dieser Datensatz als gelöscht markiert ist. |
| `createdDate` |  | Zeitpunkt der Erstellung des Datensatzes. |
| `lastUpdatedDate` |  | Zeit der letzten Änderung. |

## `AJOB2B-1_5_4-account_event`

Jeder Datensatz erfasst ein Konto-Journey-Ereignis: ein Konto, das einem Journey hinzugefügt oder daraus entfernt wird, oder das zwischen Journey-Knoten wechselt. Verwenden Sie `eventType` und `timestamp`, um eine Zeitleiste für die Kontoaktivität zu erstellen. `buyingGroupID` ist verfügbar, wenn das Ereignis einer Einkaufsgruppe zugeordnet ist.

**format:** Related-record format

`eventType` liefert Informationen darüber, was passiert ist. In den folgenden Tabellen werden die Felder für die einzelnen Aktivitätstypen beschrieben.

`lastUpdatedDate` wird derzeit nicht für diese Ereignisse ausgefüllt. Verwenden Sie `timestamp` für das Aktivitätsdatum.

### Konto zu einer Journey hinzugefügt (`account.addAccountToJourney`)

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id` | Datensatz-ID | Aktivitätskennung. |
| `eventType` |  | `account.addAccountToJourney`. |
| `timestamp` |  | Zeitpunkt, zu dem die Aktivität stattfand. |
| `accountID` | Stimmt überein mit `AJOB2B-1_5_4-account_relational` (`_id`) | Kontokennung |
| `journeyID` | Stimmt überein mit `AJOB2B-1_5_4-account_journey` (`_id`) | Journey-Kennung |
| `journeyNodeID` | Stimmt überein mit `AJOB2B-1_5_4-account_journey_node` (`_id`) | Journey-Knotenkennung. |
| `buyingGroupID` | Stimmt überein mit `AJOB2B-1_5_4-buying_group` (`_id`) | Einkaufsgruppenkennung, wenn die Journey-Hinzufügung der Einkaufsgruppe zugeordnet wird. |
| `lastUpdatedDate` |  | Aktualisierungszeit des Datensatzes Derzeit leer; Zeitstempel für das Aktivitätsdatum verwenden. |

### Konto von einer Journey entfernt (`account.removeAccountFromJourney`)

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id` | Datensatz-ID | Aktivitätskennung. |
| `eventType` |  | `account.removeAccountFromJourney`. |
| `timestamp` |  | Zeitpunkt, zu dem die Aktivität stattfand. |
| `accountID` | Stimmt überein mit `AJOB2B-1_5_4-account_relational` (`_id`) | Kontokennung |
| `journeyID` | Stimmt überein mit `AJOB2B-1_5_4-account_journey` (`_id`) | Journey-Kennung |
| `journeyNodeID` | Stimmt überein mit `AJOB2B-1_5_4-account_journey_node` (`_id`) | Journey-Knotenkennung. |
| `buyingGroupID` | Stimmt überein mit `AJOB2B-1_5_4-buying_group` (`_id`) | Einkaufsgruppenkennung, wenn die Journey-Entfernung der Einkaufsgruppe zugeordnet wird. |
| `lastUpdatedDate` |  | Aktualisierungszeit des Datensatzes Derzeit leer; Zeitstempel für das Aktivitätsdatum verwenden. |

### Konto wurde zwischen Journey-Schritten verschoben (`account.changeAccountJourneyNode`)

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id` | Datensatz-ID | Aktivitätskennung. |
| `eventType` |  | `account.changeAccountJourneyNode`. |
| `timestamp` |  | Zeitpunkt, zu dem die Aktivität stattfand. |
| `accountID` | Stimmt überein mit `AJOB2B-1_5_4-account_relational` (`_id`) | Kontokennung |
| `journeyID` | Stimmt überein mit `AJOB2B-1_5_4-account_journey` (`_id`) | Journey-Kennung |
| `journeyNodeID` | Stimmt überein mit `AJOB2B-1_5_4-account_journey_node` (`_id`) | Journey-Knotenkennung. |
| `previousJourneyNodeID` | Bezieht sich auf `AJOB2B-1_5_4-account_journey_node` (`_id`); Werte können nicht übereinstimmen | Kennung des vorherigen Journey-Schritts. Dieser Wert stimmt möglicherweise nicht mit dem entsprechenden Schrittdatensatz überein. Verwenden Sie ihn nicht allein, um Datensätze zu verbinden. |
| `buyingGroupID` | Stimmt überein mit `AJOB2B-1_5_4-buying_group` (`_id`) | Einkaufsgruppenkennung, wenn die Knotenänderung der Einkaufsgruppe zugeordnet wird. |
| `lastUpdatedDate` |  | Aktualisierungszeit des Datensatzes Derzeit leer; Zeitstempel für das Aktivitätsdatum verwenden. |

## `AJOB2B-1_5_4-buying_group_event`

Jeder Datensatz erfasst eine Änderung des Status einer Einkaufsgruppe, einschließlich des neuen Status und des Zeitpunkts der Änderung. Das Feld „Neue Phase“ ist derzeit nicht ausgefüllt.

**format:** Related-record format

### Status der Einkaufsgruppe geändert (`buyingGroup.changeStatus`)

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id` | Datensatz-ID | Aktivitätskennung. |
| `eventType` |  | `buyingGroup.changeStatus`. |
| `timestamp` |  | Zeitpunkt, zu dem die Aktivität stattfand. |
| `buyingGroupID` | Stimmt überein mit `AJOB2B-1_5_4-buying_group` (`_id`) | Einkaufsgruppenkennung. |
| `newStatus` |  | Neuer Statuswert. |
| `newStage` |  | Neue Einkaufsgruppenphase. Derzeit leer. |
| `lastUpdatedDate` |  | Aktualisierungszeit des Datensatzes |

>[!NOTE]
>
>**Verfügbarkeitshinweis:** Verwenden Sie `newStatus`, um Statusänderungen zu melden. Verwenden Sie `newStage` nicht zum Melden von Stufenänderungen, da es derzeit leer ist.

## `AJOB2B-1_5-person_event`

Jeder Datensatz beschreibt ein Web-, E-Mail- oder anderes unterstütztes Aktivitätsereignis auf Personenebene. Verwenden Sie `eventType` und `timestamp`, um das Verhalten im Zeitverlauf zu analysieren, wobei ereignisspezifische Details nur für den entsprechenden Ereignistyp ausgefüllt werden.

**format:** Standard-Adobe-Format

`eventType` erzählt euch, was passiert ist. In den folgenden Tabellen werden die Felder für die einzelnen Aktivitätstypen beschrieben. Details, die nicht für ein Ereignis gelten, sind leer.

### E-Mail gesendet (`directMarketing.emailSent`)

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id` | Datensatz-ID | Aktivitätskennung. |
| `eventType` |  | `directMarketing.emailSent`. |
| `timestamp` |  | Zeitpunkt, zu dem die Aktivität stattfand. |
| `personID` | Stimmt überein mit `AJOB2B-1_5_1-person` (`personID`) | Personenkennung. |
| `personKey.sourceID` |  | Personenkennung im verbundenen System. |
| `personKey.sourceType` |  | Name des verbundenen Produkts. |
| `personKey.sourceInstanceID` |  | Kennung der [!DNL Experience Platform] oder des verbundenen Kontos. |
| `personKey.sourceKey` |  | Vollständige Personenkennung zum Abgleichen verwandter Datensätze. |
| `directMarketing.emailSent.mailingKey.sourceID` |  | Asset-ID wird gesendet. |
| `directMarketing.emailSent.mailingKey.sourceType` |  | Name des verbundenen Produkts. |
| `directMarketing.emailSent.mailingKey.sourceInstanceID` |  | Instanz-ID. |
| `directMarketing.emailSent.mailingKey.sourceKey` |  | Vollständige E-Mail-Inhaltskennung. |
| `directMarketing.emailSent.mailingName` |  | Mailing-Name. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Stimmt überein mit `AJOB2B-1_5_4-person_journey` (`_id`) | Journey-ID (falls zugeordnet). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Stimmt überein mit `AJOB2B-1_5_4-person_journey_node` (`_id`) | Journey-Knoten-ID (falls zugeordnet). |

### E-Mail zugestellt (`directMarketing.emailDelivered`)

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id` | Datensatz-ID | Aktivitätskennung. |
| `eventType` |  | `directMarketing.emailDelivered`. |
| `timestamp` |  | Zeitpunkt, zu dem die Aktivität stattfand. |
| `personID` | Stimmt überein mit `AJOB2B-1_5_1-person` (`personID`) | Personenkennung. |
| `personKey.sourceID` |  | Personenkennung im verbundenen System. |
| `personKey.sourceType` |  | Name des verbundenen Produkts. |
| `personKey.sourceInstanceID` |  | Kennung der [!DNL Experience Platform] oder des verbundenen Kontos. |
| `personKey.sourceKey` |  | Vollständige Personenkennung zum Abgleichen verwandter Datensätze. |
| `directMarketing.mailingKey.sourceID` |  | Asset-ID wird gesendet. |
| `directMarketing.mailingKey.sourceType` |  | Name des verbundenen Produkts. |
| `directMarketing.mailingKey.sourceInstanceID` |  | Instanz-ID. |
| `directMarketing.mailingKey.sourceKey` |  | Vollständige E-Mail-Inhaltskennung. |
| `directMarketing.mailingName` |  | Mailing-Name. |
| `directMarketing.email` |  | E-Mail-Adresse |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Stimmt überein mit `AJOB2B-1_5_4-person_journey` (`_id`) | Journey-ID (falls zugeordnet). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Stimmt überein mit `AJOB2B-1_5_4-person_journey_node` (`_id`) | Journey-Knoten-ID (falls zugeordnet). |

### E-Mail-Abo beenden (`directMarketing.emailUnsubscribed`)

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id` | Datensatz-ID | Aktivitätskennung. |
| `eventType` |  | `directMarketing.emailUnsubscribed`. |
| `timestamp` |  | Zeitpunkt, zu dem die Aktivität stattfand. |
| `personID` | Stimmt überein mit `AJOB2B-1_5_1-person` (`personID`) | Personenkennung. |
| `personKey.sourceID` |  | Personenkennung im verbundenen System. |
| `personKey.sourceType` |  | Name des verbundenen Produkts. |
| `personKey.sourceInstanceID` |  | Kennung der [!DNL Experience Platform] oder des verbundenen Kontos. |
| `personKey.sourceKey` |  | Vollständige Personenkennung zum Abgleichen verwandter Datensätze. |
| `directMarketing.mailingKey.sourceID` |  | Asset-ID wird gesendet. |
| `directMarketing.mailingKey.sourceType` |  | Name des verbundenen Produkts. |
| `directMarketing.mailingKey.sourceInstanceID` |  | Instanz-ID. |
| `directMarketing.mailingKey.sourceKey` |  | Vollständige E-Mail-Inhaltskennung. |
| `directMarketing.mailingName` |  | Mailing-Name. |
| `directMarketing.email` |  | E-Mail-Adresse |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Stimmt überein mit `AJOB2B-1_5_4-person_journey` (`_id`) | Journey-ID (falls zugeordnet). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Stimmt überein mit `AJOB2B-1_5_4-person_journey_node` (`_id`) | Journey-Knoten-ID (falls zugeordnet). |

### E-Mail geöffnet (`directMarketing.emailOpened`)

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id` | Datensatz-ID | Aktivitätskennung. |
| `eventType` |  | `directMarketing.emailOpened`. |
| `timestamp` |  | Zeitpunkt, zu dem die Aktivität stattfand. |
| `personID` | Stimmt überein mit `AJOB2B-1_5_1-person` (`personID`) | Personenkennung. |
| `personKey.sourceID` |  | Personenkennung im verbundenen System. |
| `personKey.sourceType` |  | Name des verbundenen Produkts. |
| `personKey.sourceInstanceID` |  | Kennung der [!DNL Experience Platform] oder des verbundenen Kontos. |
| `personKey.sourceKey` |  | Vollständige Personenkennung zum Abgleichen verwandter Datensätze. |
| `directMarketing.mailingKey.sourceID` |  | Asset-ID wird gesendet. |
| `directMarketing.mailingKey.sourceType` |  | Name des verbundenen Produkts. |
| `directMarketing.mailingKey.sourceInstanceID` |  | Instanz-ID. |
| `directMarketing.mailingKey.sourceKey` |  | Vollständige E-Mail-Inhaltskennung. |
| `directMarketing.mailingName` |  | Mailing-Name. |
| `directMarketing.email` |  | E-Mail-Adresse |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Stimmt überein mit `AJOB2B-1_5_4-person_journey` (`_id`) | Journey-ID (falls zugeordnet). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Stimmt überein mit `AJOB2B-1_5_4-person_journey_node` (`_id`) | Journey-Knoten-ID (falls zugeordnet). |
| `device.isMobileDevice` |  | Ob für die Aktivität ein Mobilgerät aufgezeichnet wurde. |
| `device.model` |  | Geräte- oder E-Mail-Client-Informationen. |
| `environment.browserDetails.userAgent` |  | Browser- oder E-Mail-Client-Informationen. |
| `environment.operatingSystem` |  | Betriebssystem. |

### E-Mail-Link angeklickt (`directMarketing.emailClicked`)

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id` | Datensatz-ID | Aktivitätskennung. |
| `eventType` |  | `directMarketing.emailClicked`. |
| `timestamp` |  | Zeitpunkt, zu dem die Aktivität stattfand. |
| `personID` | Stimmt überein mit `AJOB2B-1_5_1-person` (`personID`) | Personenkennung. |
| `personKey.sourceID` |  | Personenkennung im verbundenen System. |
| `personKey.sourceType` |  | Name des verbundenen Produkts. |
| `personKey.sourceInstanceID` |  | Kennung der [!DNL Experience Platform] oder des verbundenen Kontos. |
| `personKey.sourceKey` |  | Vollständige Personenkennung zum Abgleichen verwandter Datensätze. |
| `directMarketing.mailingKey.sourceID` |  | Asset-ID wird gesendet. |
| `directMarketing.mailingKey.sourceType` |  | Name des verbundenen Produkts. |
| `directMarketing.mailingKey.sourceInstanceID` |  | Instanz-ID. |
| `directMarketing.mailingKey.sourceKey` |  | Vollständige E-Mail-Inhaltskennung. |
| `directMarketing.mailingName` |  | Mailing-Name. |
| `directMarketing.email` |  | E-Mail-Adresse |
| `directMarketing.linkURL` |  | Link-URL angeklickt. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Stimmt überein mit `AJOB2B-1_5_4-person_journey` (`_id`) | Journey-ID (falls zugeordnet). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Stimmt überein mit `AJOB2B-1_5_4-person_journey_node` (`_id`) | Journey-Knoten-ID (falls zugeordnet). |
| `device.isMobileDevice` |  | Ob für die Aktivität ein Mobilgerät aufgezeichnet wurde. |
| `device.model` |  | Geräte- oder E-Mail-Client-Informationen. |
| `environment.browserDetails.userAgent` |  | Browser- oder E-Mail-Client-Informationen. |
| `environment.operatingSystem` |  | Betriebssystem. |

### E-Mail gebounct (`directMarketing.emailBounced`)

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id` | Datensatz-ID | Aktivitätskennung. |
| `eventType` |  | `directMarketing.emailBounced`. |
| `timestamp` |  | Zeitpunkt, zu dem die Aktivität stattfand. |
| `personID` | Stimmt überein mit `AJOB2B-1_5_1-person` (`personID`) | Personenkennung. |
| `personKey.sourceID` |  | Personenkennung im verbundenen System. |
| `personKey.sourceType` |  | Name des verbundenen Produkts. |
| `personKey.sourceInstanceID` |  | Kennung der [!DNL Experience Platform] oder des verbundenen Kontos. |
| `personKey.sourceKey` |  | Vollständige Personenkennung zum Abgleichen verwandter Datensätze. |
| `directMarketing.mailingKey.sourceID` |  | Asset-ID wird gesendet. |
| `directMarketing.mailingKey.sourceType` |  | Name des verbundenen Produkts. |
| `directMarketing.mailingKey.sourceInstanceID` |  | Instanz-ID. |
| `directMarketing.mailingKey.sourceKey` |  | Vollständige E-Mail-Inhaltskennung. |
| `directMarketing.mailingName` |  | Mailing-Name. |
| `directMarketing.email` |  | E-Mail-Adresse |
| `directMarketing.emailBouncedCode` |  | Bounce-Kategorie/Code. |
| `directMarketing.emailBouncedDetails` |  | Detailtext. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Stimmt überein mit `AJOB2B-1_5_4-person_journey` (`_id`) | Journey-ID (falls zugeordnet). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Stimmt überein mit `AJOB2B-1_5_4-person_journey_node` (`_id`) | Journey-Knoten-ID (falls zugeordnet). |

### Softbounce bei E-Mails (`directMarketing.emailBouncedSoft`)

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id` | Datensatz-ID | Aktivitätskennung. |
| `eventType` |  | `directMarketing.emailBouncedSoft`. |
| `timestamp` |  | Zeitpunkt, zu dem die Aktivität stattfand. |
| `personID` | Stimmt überein mit `AJOB2B-1_5_1-person` (`personID`) | Personenkennung. |
| `personKey.sourceID` |  | Personenkennung im verbundenen System. |
| `personKey.sourceType` |  | Name des verbundenen Produkts. |
| `personKey.sourceInstanceID` |  | Kennung der [!DNL Experience Platform] oder des verbundenen Kontos. |
| `personKey.sourceKey` |  | Vollständige Personenkennung zum Abgleichen verwandter Datensätze. |
| `directMarketing.mailingKey.sourceID` |  | Asset-ID wird gesendet. |
| `directMarketing.mailingKey.sourceType` |  | Name des verbundenen Produkts. |
| `directMarketing.mailingKey.sourceInstanceID` |  | Instanz-ID. |
| `directMarketing.mailingKey.sourceKey` |  | Vollständige E-Mail-Inhaltskennung. |
| `directMarketing.mailingName` |  | Mailing-Name. |
| `directMarketing.email` |  | E-Mail-Adresse |
| `directMarketing.emailBouncedCode` |  | Bounce-Kategorie/Code. |
| `directMarketing.emailBouncedDetails` |  | Detailtext. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Stimmt überein mit `AJOB2B-1_5_4-person_journey` (`_id`) | Journey-ID (falls zugeordnet). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Stimmt überein mit `AJOB2B-1_5_4-person_journey_node` (`_id`) | Journey-Knoten-ID (falls zugeordnet). |

### Angezeigte Web-Seite (`web.webpagedetails.pageViews`)

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id` | Datensatz-ID | Aktivitätskennung. |
| `eventType` |  | `web.webpagedetails.pageViews`. |
| `timestamp` |  | Zeitpunkt, zu dem die Aktivität stattfand. |
| `personID` | Stimmt überein mit `AJOB2B-1_5_1-person` (`personID`) | Personenkennung. |
| `personKey.sourceID` |  | Personenkennung im verbundenen System. |
| `personKey.sourceType` |  | Name des verbundenen Produkts. |
| `personKey.sourceInstanceID` |  | Kennung der [!DNL Experience Platform] oder des verbundenen Kontos. |
| `personKey.sourceKey` |  | Vollständige Personenkennung zum Abgleichen verwandter Datensätze. |
| `web.webPageDetails.webPageKey.sourceID` |  | Seiten-Asset-ID. |
| `web.webPageDetails.webPageKey.sourceType` |  | Name des verbundenen Produkts. |
| `web.webPageDetails.webPageKey.sourceInstanceID` |  | Instanz-ID. |
| `web.webPageDetails.webPageKey.sourceKey` |  | Vollständige Seitenkennung. |
| `web.webPageDetails.name` |  | Seitenname. |
| `web.webPageDetails.URL` |  | Seiten-URL. |
| `web.webPageDetails.queryParameters` |  | Zusätzliche Informationen in einer Web-Adresse. |
| `web.webPageDetails.webPageID` |  | Seiten-ID. |
| `environment.browserDetails.userAgent` |  | Browser- oder E-Mail-Client-Informationen. |
| `web.webReferrer.URL` |  | Referrer-URL. |

### Weblink angeklickt (`web.webinteraction.linkClicks`)

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id` | Datensatz-ID | Aktivitätskennung. |
| `eventType` |  | `web.webinteraction.linkClicks`. |
| `timestamp` |  | Zeitpunkt, zu dem die Aktivität stattfand. |
| `personID` | Stimmt überein mit `AJOB2B-1_5_1-person` (`personID`) | Personenkennung. |
| `personKey.sourceID` |  | Personenkennung im verbundenen System. |
| `personKey.sourceType` |  | Name des verbundenen Produkts. |
| `personKey.sourceInstanceID` |  | Kennung der [!DNL Experience Platform] oder des verbundenen Kontos. |
| `personKey.sourceKey` |  | Vollständige Personenkennung zum Abgleichen verwandter Datensätze. |
| `web.webInteraction.webInteractionKey.sourceID` |  | Asset-ID für Interaktion. |
| `web.webInteraction.webInteractionKey.sourceType` |  | Name des verbundenen Produkts. |
| `web.webInteraction.webInteractionKey.sourceInstanceID` |  | Instanz-ID. |
| `web.webInteraction.webInteractionKey.sourceKey` |  | Vollständige Interaktionskennung. |
| `web.webInteraction.linkID` |  | Link-ID. |
| `web.webInteraction.linkURL` |  | Ziel-URL. |
| `web.webPageDetails.queryParameters` |  | Zusätzliche Informationen in einer Web-Adresse. |
| `web.webPageDetails.webPageID` |  | Seiten-ID. |
| `environment.browserDetails.userAgent` |  | Browser- oder E-Mail-Client-Informationen. |
| `web.webReferrer.URL` |  | Referrer-URL. |

### Formular gesendet (`web.formFilledOut`)

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id` | Datensatz-ID | Aktivitätskennung. |
| `eventType` |  | `web.formFilledOut`. |
| `timestamp` |  | Zeitpunkt, zu dem die Aktivität stattfand. |
| `personID` | Stimmt überein mit `AJOB2B-1_5_1-person` (`personID`) | Personenkennung. |
| `personKey.sourceID` |  | Personenkennung im verbundenen System. |
| `personKey.sourceType` |  | Name des verbundenen Produkts. |
| `personKey.sourceInstanceID` |  | Kennung der [!DNL Experience Platform] oder des verbundenen Kontos. |
| `personKey.sourceKey` |  | Vollständige Personenkennung zum Abgleichen verwandter Datensätze. |
| `web.fillOutForm.webFormKey.sourceID` |  | Formular-Asset-ID. |
| `web.fillOutForm.webFormKey.sourceType` |  | Name des verbundenen Produkts. |
| `web.fillOutForm.webFormKey.sourceInstanceID` |  | Instanz-ID. |
| `web.fillOutForm.webFormKey.sourceKey` |  | Vollständige Formular-ID. |
| `web.fillOutForm.webFormID` |  | Formular-ID. |
| `web.fillOutForm.webFormName` |  | Formularname. |
| `web.webPageDetails.queryParameters` |  | Zusätzliche Informationen in einer Web-Adresse. |
| `web.webPageDetails.webPageID` |  | Seiten-ID. |
| `environment.browserDetails.userAgent` |  | Browser- oder E-Mail-Client-Informationen. |
| `web.webReferrer.URL` |  | Referrer-URL. |

### Interessanter Moment aufgezeichnet (`leadOperation.interestingMoment`)

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id` | Datensatz-ID | Aktivitätskennung. |
| `eventType` |  | `leadOperation.interestingMoment`. |
| `timestamp` |  | Zeitpunkt, zu dem die Aktivität stattfand. |
| `personID` | Stimmt überein mit `AJOB2B-1_5_1-person` (`personID`) | Personenkennung. |
| `personKey.sourceID` |  | Personenkennung im verbundenen System. |
| `personKey.sourceType` |  | Name des verbundenen Produkts. |
| `personKey.sourceInstanceID` |  | Kennung der [!DNL Experience Platform] oder des verbundenen Kontos. |
| `personKey.sourceKey` |  | Vollständige Personenkennung zum Abgleichen verwandter Datensätze. |
| `leadOperation.interestingMoment.date` |  | Datum/Uhrzeit des Moments. |
| `leadOperation.interestingMoment.description` |  | Beschreibung |
| `leadOperation.interestingMoment.source` |  | Name des zugehörigen Produkts oder der Kampagne. |
| `leadOperation.interestingMoment.type` |  | Titel eingeben. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Stimmt überein mit `AJOB2B-1_5_4-person_journey` (`_id`) | Journey-ID (falls zugeordnet). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Stimmt überein mit `AJOB2B-1_5_4-person_journey_node` (`_id`) | Journey-Knoten-ID (falls zugeordnet). |

## `AJOB2B-1_5_4-journey_node`

Jeder Datensatz beschreibt einen Journey-Schritt, die Journey, zu der er gehört, und die Art des Schritts. Die gleichen Schritte können in den Konto- und Personen-Journey-Schritt-Datensätzen angezeigt werden. `journeyID` mit der entsprechenden Journey abgleichen; einen Schritt nicht öfter als einmal zählen, da er in mehreren Datensätzen vorkommt.

**format:** Related-record format

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id` | Datensatz-ID | Knotensatz-ID (verwenden Sie den vollständigen Wert). |
| `journeyID` | Entspricht `AJOB2B-1_5_4-account_journey` oder `AJOB2B-1_5_4-person_journey` (`_id`) | Kennung der übergeordneten Journey. |
| `nodeType` |  | Art des Journey-Schritts, z. B. Start, Ende, Warten oder Entscheidung. |
| `isDeleted` |  | Gibt an, ob dieser Datensatz als gelöscht markiert ist. |
| `lastUpdatedDate` |  | Zeit der letzten Änderung. |

## `AJOB2B-1_5_4-account_relational`

Jeder Datensatz beschreibt ein Konto, einschließlich seiner Organisationsdetails, Position, Größe, Umsatz und benutzerdefinierten Felder. Verwenden Sie diese Informationen, um den Kauf-Gruppen- und Journey-Berichten einen Kontokontext hinzuzufügen.

**format:** Related-record format

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id` | Datensatz-ID | Datensatz-ID des Kontos (vollständigen Wert verwenden). |
| `accountName` |  | Kontoname. |
| `industry` |  | Branchenklassifizierung. |
| `country` |  | Land. |
| `sicCode` |  | Standard Industrial Classification Code. |
| `domainName` |  | Primäre Web-Domain. |
| `primaryEmailDomain` |  | Primäre E-Mail-Domain. |
| `street` |  | Straße. |
| `city` |  | Stadt. |
| `state` |  | Bundesland oder Region. |
| `postalCode` |  | Postleitzahl. |
| `region` |  | Geografische Region. |
| `phoneNumber` |  | Telefonnummer. |
| `logoUrl` |  | URL des Kontologos. |
| `annualRevenue` |  | Jährliche Einnahmen. |
| `numberOfEmployees` |  | Anzahl der Mitarbeiter. |
| `createdDate` |  | Zeitpunkt der Erstellung des Datensatzes. |
| `sourceType` |  | Name des verbundenen Systems, das das Konto identifiziert. |
| `sourceInstanceID` |  | Kennung Ihres Unternehmens oder Kontos in diesem verbundenen System. |
| `sourceID` |  | Kontokennung in diesem verbundenen System. |
| `customAttributes` |  | Benutzerdefinierte Feldnamen und Werte werden zusammen als Text gespeichert. |
| `isDeleted` |  | Gibt an, ob dieser Datensatz als gelöscht markiert ist. |
| `lastUpdatedDate` |  | Zeit der letzten Änderung. |

## `AJOB2B-1_5_4-person_relational`

Jeder Datensatz beschreibt eine Person, einschließlich ihrer Kontaktinformationen, Auftragsdetails, Kennungen und benutzerdefinierten Felder. Verwenden Sie diese Option, um Personeninformationen zu Mitgliedschafts-, Journey- und Aktivitätsberichten hinzuzufügen.

**format:** Related-record format

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id` | Datensatz-ID | Vollständige Personenkennung zum Abgleichen verwandter Datensätze. |
| `email` |  | E-Mail-Adresse |
| `firstName` |  | Vorname. |
| `middleName` |  | Zweiter Vorname. |
| `lastName` |  | Nachname. |
| `jobTitle` |  | Position. |
| `personType` |  | Personentyp: Kontakt, Interessent oder ausstehender Lead. |
| `isLead` |  | Ob die Person ein Lead ist. |
| `isAnonymous` |  | Ob die Person anonym ist. |
| `salutation` |  | Anrede oder ehrenvoll. |
| `phone` |  | Primäre Telefonnummer. |
| `mobile` |  | Mobiltelefonnummer. |
| `sourceType` |  | Name des verbundenen Systems, das die Person identifiziert, z. B. [!DNL Marketo Engage]. |
| `sourceInstanceID` |  | Kennung Ihres Unternehmens oder Kontos in diesem verbundenen System. |
| `sourceID` |  | Personenkennung in diesem verbundenen System. |
| `identityNamespace` |  | Titel, der die Art der zusätzlichen Personenkennung angibt. |
| `identityValue` |  | Wert der sekundären Identität. |
| `customAttributes` |  | Benutzerdefinierte Feldnamen und Werte werden zusammen als Text gespeichert. |
| `isDeleted` |  | Gibt an, ob dieser Datensatz als gelöscht markiert ist. |
| `lastUpdatedDate` |  | Zeit der letzten Änderung. |

## `AJOB2B-1_5_4-account_person`

Jeder Datensatz verknüpft ein Kontoprofil mit einem Personenprofil. Verwenden Sie sie, um Beziehungen über die Konto- und Personenprofildatensätze hinweg zu melden.

**format:** Related-record format

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id` | Datensatz-ID | Datensatz-ID der Konto-Personen-Beziehung (verwenden Sie den vollständigen Wert). |
| `accountID` | Stimmt überein mit `AJOB2B-1_5_4-account_relational` (`_id`) | Vollständige Kontokennung (`account_relational._id`). |
| `personID` | Stimmt überein mit `AJOB2B-1_5_4-person_relational` (`_id`) | Vollständige Personenkennung (Verweise `person_relational._id`). |
| `createdDate` |  | Zeitpunkt der Erstellung der Konto-Personen-Beziehung. |
| `isDeleted` |  | Gibt an, ob dieser Datensatz als gelöscht markiert ist. |
| `lastUpdatedDate` |  | Zeit der letzten Änderung. |

## `AJOB2B-1_5_4-person_event_relational`

Jeder Datensatz beschreibt eine unterstützte Personenaktivität, z. B. das Anzeigen einer Webseite, die Interaktion mit einer E-Mail oder das Durchlaufen einer Journey. Benutzen Sie `eventType` und `activityTypeID`, um zu verstehen, was passiert ist. Es werden nur Details ausgefüllt, die für diese Art von Aktivität relevant sind.

**format:** Related-record format

Die folgende Feldliste deckt alle unterstützten Aktivitätstypen ab. Ein einzelner Datensatz enthält nur die Details, die für seine Aktivität gelten.

>[!NOTE]
>
>**Verfügbarkeit:** einige Aktivitäten können eine leere `_id` haben. Gehen Sie nicht davon aus, dass jede Aktivität über eine verwendbare Datensatzkennung verfügt. Der Datensatz ist keine Garantie für einen vollständigen Aktivitätsverlauf.

Journey-Details (`journeyID`, `journeyNodeID`, `journeyStepID` und ähnliche Felder) werden für Journey-Aktivitäten (`person.journeyAdd`, `person.journeyRemove`, `person.journeyStart`, `person.journeyEnd`, `person.journeyNodeTransition`, `person.journeySplitNode`) und für `person.attributeChanged` Aktivitäten bereitgestellt, die mit einem Journey-Schritt „Benutzerprofil aktualisieren“ verbunden sind.

Felder für Attributänderungen (`attributeName`, `attributeID`, `attributeNewValue`, `attributeOldValue`, `attributeChangeReason`) werden nur zur `person.attributeChanged` ausgefüllt.

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id` | Datensatz-ID | Kennung für die Aktivität, falls verfügbar. |
| `timestamp` |  | Zeitpunkt, zu dem die Aktivität stattfand. |
| `eventType` |  | Aktivitäts-Kennzeichnung. Werte: `web.webpagedetails.pageViews`, `web.formFilledOut`, `web.webinteraction.linkClicks`, `directMarketing.emailSent`, `directMarketing.emailDelivered`, `directMarketing.emailBounced`, `directMarketing.emailBouncedSoft`, `directMarketing.emailUnsubscribed`, `directMarketing.emailOpened`, `directMarketing.emailClicked`, `leadOperation.interestingMoment`, `person.attributeChanged`, `person.journeyAdd`, `person.journeyStart`, `person.journeyRemove`, `person.journeyEnd`, `person.journeyNodeTransition`, `person.journeySplitNode`. |
| `activityTypeID` |  | Aktivitätscode. Verwenden Sie sie mit `eventType`, um Aktivitäten zu unterscheiden, die dieselbe Ereignisbeschriftung aufweisen. |
| `personID` | Stimmt überein mit `AJOB2B-1_5_4-person_relational` (`_id`) | Vollständige Personenkennung, mit der die Aktivität einem Personendatensatz zugeordnet wird. |
| `journeyID` | Stimmt überein mit `AJOB2B-1_5_4-person_journey` (`_id`) | Vollständige Journey-Kennung. Leer für Aktivitäten, die nicht mit einer Journey verbunden sind. |
| `journeyNodeID` | Stimmt überein mit `AJOB2B-1_5_4-person_journey_node` (`_id`) | Vollständige Journey-Schritt-Kennung. Leer für Aktivitäten, die nicht mit einer Journey verbunden sind. |
| `previousJourneyNodeID` | Stimmt überein mit `AJOB2B-1_5_4-person_journey_node` (`_id`) | Vorheriger Journey-Knoten (für `person.journeyNodeTransition` und `person.journeySplitNode` ausgefüllt). |
| `newJourneyNodeID` | Stimmt überein mit `AJOB2B-1_5_4-person_journey_node` (`_id`) | Ziel-Journey-Knoten-ID (`person.journeyNodeTransition` und `person.journeySplitNode`). In der Regel ist gleich `journeyNodeID`. |
| `journeyStepID` |  | Kennung des der Aktivität zugeordneten Journey-Schritts. |
| `journeyChoiceNumber` |  | Split-Choice-Nummer für `person.journeySplitNode`. Wird als ganze Zahl aufgezeichnet. |
| `journeyEntryCount` |  | Häufigkeit, mit der diese Person die Journey betreten hat (wird bei Journey-Hinzufügen-/Startereignissen ausgefüllt). Wird als ganze Zahl aufgezeichnet. |
| `journeyProgramID` | Kein separater Datensatz für Marketing-Programme in diesem Handbuch | Kennung des Marketing-Programms, das mit der Journey-Aktivität verknüpft ist. |
| `activitySource` |  | Name des Produkts oder der Aktion, das/die mit der Aktivität verbunden ist. |
| `campaignID` |  | Kampagnen-ID [!DNL Marketo Engage], wenn die Aktivität kampagnenbezogen ist. |
| `attributeName` |  | Name des geänderten Feldes (nur `person.attributeChanged`). |
| `attributeID` |  | Kennung des geänderten Feldes (nur `person.attributeChanged`). |
| `attributeNewValue` |  | Neuer Feldwert, als Text aufgezeichnet (nur `person.attributeChanged`). |
| `attributeOldValue` |  | Vorheriger Feldwert, als Text aufgezeichnet (nur `person.attributeChanged`). |
| `attributeChangeReason` |  | Titel des Grundes für die Änderung (nur `person.attributeChanged`) |
| `assetID` |  | Kennung des zugehörigen E-Mail-Inhalts, der zugehörigen Seite oder des zugehörigen Formulars. |
| `assetName` |  | Name des zugehörigen Inhalts. |
| `recipientEmail` |  | E-Mail-Adresse des Empfängers, falls verfügbar. Ausgefüllt nur für Aktivitäts-Codes **27** (Softbounce) und **48** (Verkaufs-E-Mail-Softbounce); leer für andere E-Mail-Aktivitäten. Suchen Sie für diese Aktivitäten den Personendatensatz mithilfe von `personID`. `assetName` identifiziert den E-Mail-Inhalt, nicht die Adresse des Empfängers. |
| `bouncedCode` |  | Bounce-Kategoriecode (nur emailBounced/emailBouncedSoft). |
| `bouncedDetails` |  | Detaillierter Bounce-Grund (nur emailBounced/emailBouncedSoft). |
| `isMobileDevice` |  | Ob ein Mobilgerät für ein Öffnen oder Klicken einer E-Mail aufgezeichnet wurde. |
| `deviceModel` |  | Gerätemodell (nur emailOpened / emailClicked). |
| `operatingSystem` |  | Betriebssystem (nur emailOpened/emailClicked). |
| `userAgent` |  | Browser- oder E-Mail-Client-Informationen für E-Mail-Öffnungen, E-Mail-Klicks und Web-Aktivitäten. |
| `clickedLinkUrl` |  | Auf E-Mail-Link geklickt URL (nur emailClicked). |
| `webPageUrl` |  | Web-Seiten-URL (nur `web.webpagedetails.pageViews`) |
| `queryParameters` |  | Zusätzliche Informationen in einer Web-Adresse für Seitenansichten, Formularübermittlungen oder Weblink-Klicks. |
| `webPageID` |  | [!DNL Marketo Engage] Web-Seiten-ID (pageViews, formFilledOut, linkClicks). |
| `referrerUrl` |  | Referrer-URL (pageViews, formFilledOut, linkClicks). |
| `formID` |  | [!DNL Marketo Engage] Formular-ID (nur `web.formFilledOut`). |
| `linkID` |  | [!DNL Marketo Engage] Link-ID (nur `web.webinteraction.linkClicks`). |
| `interestingMomentDate` |  | Datum des Augenblicks (nur `leadOperation.interestingMoment`). |
| `interestingMomentDescription` |  | Beschreibung im freien Text (nur interessante Momente). |
| `interestingMomentSource` |  | Verwandtes Produkt oder Kampagne (nur interessanter Moment). |
| `interestingMomentType` |  | Kategorie/Typ (nur interessanterMoment). |
| `isDeleted` |  | Gibt an, ob dieser Datensatz als gelöscht markiert ist. |
| `lastUpdatedDate` |  | Zeit der letzten Änderung. |

### Feldverweis nach Aktivitätstyp

Die folgenden Tabellen zeigen, welche Details für jede Aktivität gelten. Andere Details sind leer. Einige Aktivitäten haben denselben `eventType`: Die Codes 8 und 48 verwenden beide `directMarketing.emailBounced`. Verwenden Sie `activityTypeID`, um sie zu unterscheiden.

#### Angezeigte Web-Seite (`web.webpagedetails.pageViews`) (Aktivitätstyp 1)

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | Datensatz-ID: `_id`; `personID` entspricht `AJOB2B-1_5_4-person_relational` (`_id`) | Gemeinsame Felder. |
| `assetID` |  | Seiten-ID. |
| `assetName` |  | Seitenname. |
| `webPageUrl` |  | Seiten-URL. |
| `queryParameters` |  | Zusätzliche Informationen in einer Web-Adresse. |
| `webPageID` |  | [!DNL Marketo Engage] Web-Seiten-ID. |
| `referrerUrl` |  | Referrer-URL. |
| `userAgent` |  | Browser- oder E-Mail-Client-Informationen. |
| `isDeleted`, `lastUpdatedDate` |  | Gemeinsame Felder. |

#### Formular eingereicht (`web.formFilledOut`) (Aktivitätstyp 2)

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | Datensatz-ID: `_id`; `personID` entspricht `AJOB2B-1_5_4-person_relational` (`_id`) | Gemeinsame Felder. |
| `assetID` |  | Formular-ID. |
| `assetName` |  | Formularname. |
| `formID` |  | [!DNL Marketo Engage] Formular-ID. |
| `queryParameters` |  | Zusätzliche Informationen in einer Web-Adresse. |
| `webPageID` |  | [!DNL Marketo Engage] Web-Seiten-ID. |
| `referrerUrl` |  | Referrer-URL. |
| `userAgent` |  | Browser- oder E-Mail-Client-Informationen. |
| `isDeleted`, `lastUpdatedDate` |  | Gemeinsame Felder. |

#### Weblink angeklickt (`web.webinteraction.linkClicks`) (Aktivitätstyp 3)

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | Datensatz-ID: `_id`; `personID` entspricht `AJOB2B-1_5_4-person_relational` (`_id`) | Gemeinsame Felder. |
| `assetID` |  | Interaction/Link-ID. |
| `assetName` |  | Ziel-URL. |
| `linkID` |  | Link-ID [!DNL Marketo Engage]. |
| `queryParameters` |  | Zusätzliche Informationen in einer Web-Adresse. |
| `webPageID` |  | [!DNL Marketo Engage] Web-Seiten-ID. |
| `referrerUrl` |  | Referrer-URL. |
| `userAgent` |  | Browser- oder E-Mail-Client-Informationen. |
| `isDeleted`, `lastUpdatedDate` |  | Gemeinsame Felder. |

#### E-Mail gesendet (`directMarketing.emailSent`) (Aktivitätstypen 6, 39)

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | Datensatz-ID: `_id`; `personID` entspricht `AJOB2B-1_5_4-person_relational` (`_id`) | Gemeinsame Felder. |
| `assetID` |  | Mailing-ID. |
| `assetName` |  | Mailing-Name. |
| `campaignID` |  | [!DNL Marketo Engage] Kampagnen-ID, wenn kampagnenzugeschrieben. |
| `isDeleted`, `lastUpdatedDate` |  | Gemeinsame Felder. |

#### Zugestellte E-Mail (`directMarketing.emailDelivered`) (Aktivitätstypen 7, 45)

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | Datensatz-ID: `_id`; `personID` entspricht `AJOB2B-1_5_4-person_relational` (`_id`) | Gemeinsame Felder. |
| `assetID` |  | Mailing-ID. |
| `assetName` |  | Mailing-Name. |
| `campaignID` |  | [!DNL Marketo Engage] Kampagnen-ID, wenn kampagnenzugeschrieben. |
| `isDeleted`, `lastUpdatedDate` |  | Gemeinsame Felder. |

#### E-Mail-Abmeldung (`directMarketing.emailUnsubscribed`) (Aktivitätstyp 9)

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | Datensatz-ID: `_id`; `personID` entspricht `AJOB2B-1_5_4-person_relational` (`_id`) | Gemeinsame Felder. |
| `assetID` |  | Mailing-ID. |
| `assetName` |  | Mailing-Name. |
| `campaignID` |  | [!DNL Marketo Engage] Kampagnen-ID, wenn kampagnenzugeschrieben. |
| `isDeleted`, `lastUpdatedDate` |  | Gemeinsame Felder. |

#### Geöffnete E-Mails (`directMarketing.emailOpened`) (Aktivitätstypen 10, 40)

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | Datensatz-ID: `_id`; `personID` entspricht `AJOB2B-1_5_4-person_relational` (`_id`) | Gemeinsame Felder. |
| `assetID` |  | Mailing-ID. |
| `assetName` |  | Mailing-Name. |
| `isMobileDevice` |  | Ob für die Aktivität ein Mobilgerät aufgezeichnet wurde. |
| `deviceModel` |  | Gerätemodell |
| `operatingSystem` |  | Betriebssystem. |
| `userAgent` |  | Browser- oder E-Mail-Client-Informationen. |
| `campaignID` |  | [!DNL Marketo Engage] Kampagnen-ID, wenn kampagnenzugeschrieben. |
| `isDeleted`, `lastUpdatedDate` |  | Gemeinsame Felder. |

#### E-Mail-Link angeklickt (`directMarketing.emailClicked`) (Aktivitätstypen 11, 41)

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | Datensatz-ID: `_id`; `personID` entspricht `AJOB2B-1_5_4-person_relational` (`_id`) | Gemeinsame Felder. |
| `assetID` |  | Mailing-ID. |
| `assetName` |  | Mailing-Name. |
| `clickedLinkUrl` |  | Link-URL angeklickt. |
| `isMobileDevice` |  | Ob für die Aktivität ein Mobilgerät aufgezeichnet wurde. |
| `deviceModel` |  | Gerätemodell |
| `operatingSystem` |  | Betriebssystem. |
| `userAgent` |  | Browser- oder E-Mail-Client-Informationen. |
| `campaignID` |  | [!DNL Marketo Engage] Kampagnen-ID, wenn kampagnenzugeschrieben. |
| `isDeleted`, `lastUpdatedDate` |  | Gemeinsame Felder. |

#### E-Mail gebounct (`directMarketing.emailBounced`): Hardbounce (Aktivitätstyp 8)

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | Datensatz-ID: `_id`; `personID` entspricht `AJOB2B-1_5_4-person_relational` (`_id`) | Gemeinsame Felder. |
| `assetID` |  | Mailing-ID. |
| `assetName` |  | Mailing-Name. |
| `bouncedCode` |  | Bounce-Kategoriecode. |
| `bouncedDetails` |  | Detaillierter Bounce-Grund. |
| `campaignID` |  | [!DNL Marketo Engage] Kampagnen-ID, wenn kampagnenzugeschrieben. |
| `isDeleted`, `lastUpdatedDate` |  | Gemeinsame Felder. |

Diese Aktivität verwendet den gleichen `directMarketing.emailBounced` wie der Aktivitäts-Code 48, `recipientEmail` jedoch für Code 8 leer ist. Verwenden Sie `activityTypeID`, um die beiden zu unterscheiden.

#### E-Mail gebounct (`directMarketing.emailBounced`): Verkaufs-E-Mail-Softbounce (Aktivitätstyp 48)

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | Datensatz-ID: `_id`; `personID` entspricht `AJOB2B-1_5_4-person_relational` (`_id`) | Gemeinsame Felder. |
| `assetID` |  | Mailing-ID. |
| `assetName` |  | Mailing-Name. |
| `recipientEmail` |  | E-Mail-Adresse des Empfängers |
| `bouncedCode` |  | Bounce-Kategoriecode. |
| `bouncedDetails` |  | Detaillierter Bounce-Grund. |
| `campaignID` |  | [!DNL Marketo Engage] Kampagnen-ID, wenn kampagnenzugeschrieben. |
| `isDeleted`, `lastUpdatedDate` |  | Gemeinsame Felder. |

#### Softbounce (`directMarketing.emailBouncedSoft`) bei E-Mails (Aktivitätstyp 27)

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | Datensatz-ID: `_id`; `personID` entspricht `AJOB2B-1_5_4-person_relational` (`_id`) | Gemeinsame Felder. |
| `assetID` |  | Mailing-ID. |
| `assetName` |  | Mailing-Name. |
| `recipientEmail` |  | E-Mail-Adresse des Empfängers |
| `bouncedCode` |  | Bounce-Kategoriecode. |
| `bouncedDetails` |  | Detaillierter Bounce-Grund. |
| `campaignID` |  | [!DNL Marketo Engage] Kampagnen-ID, wenn kampagnenzugeschrieben. |
| `isDeleted`, `lastUpdatedDate` |  | Gemeinsame Felder. |

#### Interessantes aufgezeichnetes Moment (`leadOperation.interestingMoment`) (Aktivitätstyp 46)

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | Datensatz-ID: `_id`; `personID` entspricht `AJOB2B-1_5_4-person_relational` (`_id`) | Gemeinsame Felder. |
| `interestingMomentDate` |  | Datum/Uhrzeit des Moments. |
| `interestingMomentDescription` |  | Beschreibung im Freien Text. |
| `interestingMomentSource` |  | Name des zugehörigen Produkts oder der Kampagne. |
| `interestingMomentType` |  | Titel eingeben. |
| `isDeleted`, `lastUpdatedDate` |  | Gemeinsame Felder. |

`assetID` und `assetName` werden für diesen Aktivitätstyp nicht ausgefüllt.

#### Personenfeld geändert (`person.attributeChanged`) (Aktivitätstyp 13)

Nur eingeschlossen, wenn die Änderung mit einer Journey verbunden ist, z. B. ein Schritt „Personenprofil aktualisieren“. Änderungen außerhalb einer Journey sind nicht enthalten.

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | Datensatz-ID: `_id`; `personID` entspricht `AJOB2B-1_5_4-person_relational` (`_id`) | Gemeinsame Felder. |
| `attributeName` |  | Name des geänderten Felds. |
| `attributeID` |  | Kennung des geänderten Feldes. |
| `attributeNewValue` |  | Neuer Feldwert, als Text aufgezeichnet. |
| `attributeOldValue` |  | Vorheriger Feldwert, als Text aufgezeichnet. |
| `attributeChangeReason` |  | Grund-Bezeichnung für die Änderung. |
| `journeyID` | Stimmt überein mit `AJOB2B-1_5_4-person_journey` (`_id`) | Journey-Kennung |
| `journeyNodeID` | Stimmt überein mit `AJOB2B-1_5_4-person_journey_node` (`_id`) | Journey-Knotenkennung. |
| `journeyStepID` |  | Kennung des Journey-Schritts. |
| `journeyProgramID` | Kein separater Datensatz für Marketing-Programme in diesem Handbuch | Journey-Programm-ID. |
| `activitySource` |  | Produkt oder Aktion, das/die mit der Aktivität verbunden ist. |
| `isDeleted`, `lastUpdatedDate` |  | Gemeinsame Felder. |

#### Person wurde zu einer Journey hinzugefügt oder hat sie gestartet (`person.journeyAdd`, `person.journeyStart`) (Aktivitätstypen 182, 184)

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | Datensatz-ID: `_id`; `personID` entspricht `AJOB2B-1_5_4-person_relational` (`_id`) | Gemeinsame Felder. |
| `journeyID` | Stimmt überein mit `AJOB2B-1_5_4-person_journey` (`_id`) | Journey-Kennung |
| `journeyNodeID` | Stimmt überein mit `AJOB2B-1_5_4-person_journey_node` (`_id`) | Journey-Knotenkennung. |
| `journeyStepID` |  | Kennung des Journey-Schritts. |
| `journeyEntryCount` |  | Häufigkeit, mit der diese Person die Journey betreten hat. |
| `journeyProgramID` | Kein separater Datensatz für Marketing-Programme in diesem Handbuch | Journey-Programm-ID. |
| `activitySource` |  | Produkt oder Aktion, das/die mit der Aktivität verbunden ist. |
| `isDeleted`, `lastUpdatedDate` |  | Gemeinsame Felder. |

#### Person von einer Journey entfernt oder eine beendet (`person.journeyRemove`, `person.journeyEnd`) (Aktivitätstypen 183, 185)

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | Datensatz-ID: `_id`; `personID` entspricht `AJOB2B-1_5_4-person_relational` (`_id`) | Gemeinsame Felder. |
| `journeyID` | Stimmt überein mit `AJOB2B-1_5_4-person_journey` (`_id`) | Journey-Kennung |
| `journeyNodeID` | Stimmt überein mit `AJOB2B-1_5_4-person_journey_node` (`_id`) | Journey-Knotenkennung. |
| `journeyStepID` |  | Kennung des Journey-Schritts. |
| `journeyProgramID` | Kein separater Datensatz für Marketing-Programme in diesem Handbuch | Journey-Programm-ID. |
| `activitySource` |  | Produkt oder Aktion, das/die mit der Aktivität verbunden ist. |
| `isDeleted`, `lastUpdatedDate` |  | Gemeinsame Felder. |

#### Person folgte einer Journey-Verzweigung (`person.journeySplitNode`) (Aktivitätstyp 186)

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | Datensatz-ID: `_id`; `personID` entspricht `AJOB2B-1_5_4-person_relational` (`_id`) | Gemeinsame Felder. |
| `journeyID` | Stimmt überein mit `AJOB2B-1_5_4-person_journey` (`_id`) | Journey-Kennung |
| `journeyNodeID` | Stimmt überein mit `AJOB2B-1_5_4-person_journey_node` (`_id`) | Journey-Knotenkennung (der Aufspaltungsknoten) |
| `previousJourneyNodeID` | Stimmt überein mit `AJOB2B-1_5_4-person_journey_node` (`_id`) | Knoten, an dem sich die Person vor der Aufspaltung befand. |
| `newJourneyNodeID` | Stimmt überein mit `AJOB2B-1_5_4-person_journey_node` (`_id`) | Knoten, in den die Person verschoben wurde (entspricht normalerweise `journeyNodeID`). |
| `journeyStepID` |  | Kennung des Journey-Schritts. |
| `journeyChoiceNumber` |  | Welcher Zweig der Teilung genommen wurde. |
| `journeyProgramID` | Kein separater Datensatz für Marketing-Programme in diesem Handbuch | Journey-Programm-ID. |
| `activitySource` |  | Produkt oder Aktion, das/die mit der Aktivität verbunden ist. |
| `isDeleted`, `lastUpdatedDate` |  | Gemeinsame Felder. |

#### Person wurde zwischen Journey-Schritten verschoben (`person.journeyNodeTransition`) (Aktivitätstyp 600)

| Feldname | Beziehung | Was es Ihnen sagt |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | Datensatz-ID: `_id`; `personID` entspricht `AJOB2B-1_5_4-person_relational` (`_id`) | Gemeinsame Felder. |
| `journeyID` | Stimmt überein mit `AJOB2B-1_5_4-person_journey` (`_id`) | Journey-Kennung |
| `journeyNodeID` | Stimmt überein mit `AJOB2B-1_5_4-person_journey_node` (`_id`) | Kennung des aktuellen Journey-Knotens. |
| `previousJourneyNodeID` | Stimmt überein mit `AJOB2B-1_5_4-person_journey_node` (`_id`) | Knoten, von dem die Person gewechselt ist. |
| `newJourneyNodeID` | Stimmt überein mit `AJOB2B-1_5_4-person_journey_node` (`_id`) | Knoten, zu dem die Person gewechselt ist (entspricht normalerweise `journeyNodeID`). |
| `journeyStepID` |  | Kennung des Journey-Schritts. |
| `journeyProgramID` | Kein separater Datensatz für Marketing-Programme in diesem Handbuch | Journey-Programm-ID. |
| `activitySource` |  | Produkt oder Aktion, das/die mit der Aktivität verbunden ist. |
| `isDeleted`, `lastUpdatedDate` |  | Gemeinsame Felder. |

## Kundeneigene Datensätze {#customer-owned-datasets}

Ihr Unternehmen kann eigene [!DNL Experience Platform] für Konten oder Personen verwenden. Nach der Konfiguration können [!DNL Adobe Journey Optimizer B2B Edition] diesen Datensätzen Informationen hinzufügen, anstatt einen weiteren Konto- oder Personendatensatz zu erstellen.

Die Namen und verfügbaren Felder hängen von der Einrichtung Ihres Unternehmens ab. Verwenden Sie die konfigurierte Konto- oder Personenkennung, um übereinstimmende Datensätze zu erkennen. Datensätze in diesen Datensätzen machen sie nicht automatisch für Zielgruppen verfügbar. Die Verfügbarkeit hängt von Ihrer [!DNL Experience Platform] ab.
