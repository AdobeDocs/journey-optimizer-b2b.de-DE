---
title: Gruppen kaufen
description: Erfahren Sie mehr über den Kauf von Gruppen und deren Komponenten.
feature: Buying Groups
exl-id: ddcd7b62-6a76-4f5e-b6d3-a20944ca8332
source-git-commit: 43fc83e70c4916c6367374a76a63e29110712a36
workflow-type: tm+mt
source-wordcount: '1186'
ht-degree: 6%

---


# Gruppen kaufen

Für B2B-Verkaufs- und Marketingaktivitäten sind Konten der Schlüssel zu jeder Strategie. Jedes Konto hat eine Gruppe von Personen zugeordnet, und diese Personen können Mitarbeiter des Kontos oder Auftragnehmer sein, die mit dem Konto arbeiten. Konten sind hierarchisch aufgebaut und verschiedene Produkte können auf unterschiedlichen Ebenen in der Hierarchie verkauft werden. So kann Adobe Experience Platform beispielsweise auf Unternehmensebene an ein Top-Level-Konto verkauft werden, während Adobe Photoshop an ein Konto verkauft wird, das eine Abteilung oder Abteilung innerhalb eines Unternehmens repräsentiert, z. B. eine Design-Abteilung innerhalb eines größeren Unternehmens.

![Diagramm der Kontorollen](assets/account-roles-diagram.png){width="800"}

Innerhalb des Kontos kann es eine Untergruppe von Personen geben, die die _Einkaufsgruppe_ ausmachen. Dies sind die Personen, die letztendlich die Kaufentscheidung treffen, sodass sie besondere Aufmerksamkeit vom Marketing-Experten benötigen und möglicherweise andere Informationen benötigen, die ihnen bereitgestellt werden als die anderen Personen, die mit dem Konto verbunden sind. Für verschiedene Produktlinien oder Angebote kann es sich bei Einkaufsgruppen um eine andere Personengruppe handeln. Beispielsweise kann ein Cybersicherheitsprodukt in der Regel einen Chief Information Officer oder Chief Security Officer und einen Vertreter der Rechtsabteilung zur Genehmigung eines Kaufs erfordern, aber ein Fehlerverfolgungsprodukt könnte in der Regel einen VP of Engineering und eine IT Director als Mitglieder der Einkaufsgruppe haben.

## Wichtige Komponenten

Sie können die Marketingeffizienz steigern, indem Sie in Journey Optimizer B2B Edition Einkaufsgruppen einrichten, die anhand der Lösungen, für die Ihre Vertriebsteams verantwortlich sind, die für die Liste Ihrer Zielkonten fehlenden Mitglieder identifizieren. Bevor Sie und Ihr Marketing-Team mit der Erstellung Ihrer Einkaufsgruppen beginnen, stellen Sie sicher, dass Sie die wichtigsten Komponenten definiert haben. Diese Komponenten sind für die Erreichung Ihrer Geschäftsziele von entscheidender Bedeutung.

| Komponente | Zweck |
| --------- | ------- |
| Lösungsinteresse | Diese Komponente bietet Antwort auf: <ul><li>Was verkaufen Sie als Marketingorganisation?</li><li>Welches Produkt oder welche Kollektion von Produkten möchten Sie verkaufen?</li></ul>  **_Beispiel:_** Weiterverkauf des neuen Produkts X an bestehende Kunden |
| Konto-Zielgruppe | Diese Komponente bietet Antwort auf: <ul><li>Wem verkaufst du?</li><li>Was ist die Liste der Konten, die Sie als Ziel auswählen?</li></ul> **_Beispiel:_** Kontosegment definiert durch Konten mit Produkt Y mit Umsatz über 1M |
| Kaufen von Gruppenrollenvorlagen | Diese Komponente bietet Antwort auf: <ul><li>Welche Rollen werden im Targeting verwendet?</li><li>Welcher Regelsatz wird verwendet, um zu bestimmen, wer den Käuferrollen zugewiesen ist?</li></ul>  **_Beispiel:_** Weisen Sie eine Person mit CMO-Titel der Rolle &quot;Entscheidungsträger&quot;zu |

## Gruppen-Workflow kaufen

1. Erstellen Sie Warengruppen.

   Optionen:
   * Verwenden Sie [Lösungsinteresse](./solution-interests.md) und [Rollenvorlage](./buying-groups-role-templates.md)
   * Importieren von Drittanbietern verwenden
   * Aus KI/ML generieren

1. Identifizieren Sie fehlende Personen.

   Analysieren Sie die Kaufgruppe mithilfe von Filtern.

   **_Beispiel:_** Die Rolle &quot;Entscheidungsträger&quot;fehlt und der Vollständigkeitswert ist &lt; 50

1. Füllen Sie die Definitionen für die Bestellgruppen aus.
<!--
   * Acquire missing people
   * Send to LinkedIn Destination
   * Enrich with Zoominfo -->

1. Verwenden Sie in einer Konto-Journey über das zugehörige Lösungsinteresse.

## Anzeigen von Einkaufsgruppen und Komponenten

Erweitern Sie im linken Navigationsbereich **[!UICONTROL Konten]** und klicken Sie auf **[!UICONTROL Gruppen kaufen]**.

Die Seite _[!UICONTROL Gruppen kaufen]_ ist in Form von Registerkarten organisiert:

| Tab | Beschreibung |
| --- | ----------- |
| [!UICONTROL Übersicht] | Diese Registerkarte ist die Standardeinstellung und zeigt das Dashboard [Gruppen kaufen](../dashboards/buying-groups-dashboard.md) an. |
| [!UICONTROL Durchsuchen] | Dieser Tab unterstützt die folgenden Aktivitäten: <ul><li>Zeigen Sie die Liste der vorhandenen Einkaufsgruppen an. </li><li>Suche nach dem Namen der Gruppe. </li><li>Filtern nach Lösungsinteresse </li><li>Führen Sie einen Drilldown zum Kauf von Gruppendetails durch. </li><li>Erstellen Sie eine Kaufgruppe. Eine Kaufgruppe löschen.</li></ul> |
| [!UICONTROL Interessen der Lösung] | Dieser Tab unterstützt die folgenden Aktivitäten: <ul><li>Zeigen Sie die Liste der vorhandenen Einkaufsgruppen an. </li><li>Suche nach dem Namen der Gruppe. </li><li>Öffnen und bearbeiten Sie die Interessenseigenschaften der Lösung. </li><li>Erstellen Sie ein Lösungsinteresse. </li><li>Löschen Sie ein Lösungsinteresse. </li><li>Anzeigen und Löschen von Aufträgen für Gruppen </li></ul> |
| [!UICONTROL Benutzerrollen-Vorlagen] | Dieser Tab unterstützt die folgenden Aktivitäten: <ul><li>Zeigen Sie die Liste der vorhandenen Benutzervorlagen an. </li><li>Suchen Sie nach dem Namen der Benutzervorlage. </li><li>Zugriff und Bearbeitung von Eigenschaften und Bedingungen von Benutzervorlagen </li><li>Erstellen Sie eine Rollenvorlage. </li><li>Löschen Sie eine Rollenvorlage. </li></ul> |

## Gruppensuche und -filter kaufen

Verwenden Sie die Registerkarte _[!UICONTROL Durchsuchen]_ , um die Liste der Kaufgruppen anzuzeigen. Sie können nach Namen suchen und die Liste nach Lösungsinteresse filtern.

![Seite zum Durchsuchen von Gruppen kaufen](assets/buying-groups-browse.png){width="800" zoomable="yes"}

## Gruppendetails kaufen

Um auf Details für eine Gruppe zuzugreifen, klicken Sie auf den Namen der Gruppe &quot;Kauf&quot;auf der Registerkarte _[!UICONTROL Durchsuchen]_ .

![Kaufen von Gruppendetails](assets/buying-group-details.png){width="600" zoomable="yes"}

### Gesamtergebnis der Gruppe kaufen

Die Vollständigkeitsbewertung wird verwendet, um festzustellen, ob die Kaufgruppe abgeschlossen ist. Das bedeutet, dass ihr die richtigen Mitglieder zugewiesen sind und bereit sind, in einer Konto-Journey verwendet zu werden. Dieser Punktstand basiert auf der Anzahl der Rollen innerhalb der Gruppe, die den Kauf abschließen, und darauf, wie viele Rollen mindestens einem Lead zugewiesen sind.

Wenn beispielsweise eine Einkaufsgruppe vier Rollen hat und drei der vier Rollen mindestens einem Lead zugewiesen sind, ist die Einkaufsgruppe zu 75 % abgeschlossen.

Der Wert für die Vollständigkeit der Einkaufsgruppe wird jedes Mal neu berechnet, wenn eine Einkaufsgruppe erstellt oder aktualisiert wird.

### Interaktionsbewertung der Gruppe kaufen

Der Interaktionswert der Gruppe &quot;Kauf&quot;ist eine Zahl, mit der die Interaktion der Mitglieder einer Einkaufsgruppe anhand der von ihnen ausgeführten Aktivitäten bestimmt wird. Jede eingehende Aktivität, die von den Mitgliedern der Einkaufsgruppe in den letzten 30 Tagen durchgeführt wurde, wird zur Berechnung des Ergebnisses verwendet.

Für jede Aktivität gilt eine tägliche Frequenzlimitierung von 20. Wenn ein Mitglied einer Einkaufsgruppe dieselbe Aktivität mehr als 20-mal am Tag ausführt, wird die Anzahl der Aktivitäten auf 20 begrenzt und nicht auf eine höhere Anzahl.

Die angezeigte Punktzahl wird gerundet. Beispielsweise wird ein Wert von 75.89999 als 76 angezeigt.

#### Gewichtung

Benutzer können jeder Rolle in der Rollenvorlage _Gewichtung_ zuweisen, um einer Rolle unterschiedliche Gewichtungen zuzuweisen, um das Interaktionsergebnis zu berechnen.

![Legen Sie die Gewichtung für jede Rolle in der Rollenvorlage fest](./assets/roles-templates-weighting.png){width="700" zoomable="yes"}

Jede Gewichtungsstufe entspricht einem Wert, der zur Berechnung des Interaktionswerts verwendet wird:

* [!UICONTROL Trivial] = 20
* [!UICONTROL Minor] = 40
* [!UICONTROL Normal] = 60
* [!UICONTROL Wichtig] = 80
* [!UICONTROL Vital] = 100

Eine Rollenvorlage mit drei als _[!UICONTROL Vital]_, _[!UICONTROL Wichtig]_ und _[!UICONTROL Normal]_ gewichteten Rollen konvertiert in die folgenden gewichteten Prozentsätze:

| Role | Gewichtung | Backend-Wert | Werteberechnung | Prozentsatz |
|-------------- |--------- |------------- |------------------ |---------- |
|               |          |              |                   |           |
| Entscheidungsträger | Vital | 100 | 24.10.2010 | 41,67% |
| Beeinflusser | Wichtig | 80 | 240.80 | 33,33% |
| Praktitioner | Normal | 60 | 240.60 | 25 % |
|               | Gesamt | 240 |                   |           |

#### Berechnungsbeispiel

Das folgende Beispiel zeigt die Berechnung des Interaktionswerts anhand des festgelegten Rollengewichtsprozentsatzes, der Anzahl der eingehenden Aktivitäten für jedes Mitglied der Kaufgruppe und einer täglichen Obergrenze von 20 Zählern für jedes Ereignis (wenn es mehrmals aufgetreten ist).

| Role | Mitglied | Typ der Aktivität | Anzahl gestern | Heute zählt | Berechnung | Gesamtbewertung |
|-------------- |--------- |-------------|-----------------|-------------|------|-----------|
|               |          |             |                 |             |      |           |
| Entscheidungsträger | Adam | Besuchte Website | 37 | 15 | 20 + 15 | 35 |
|               |          | Angeklickte E-Mail | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Mark | Besuchte Website | 5 | 3 | 5 + 3 | 8 |
|               |          | Angeklickte E-Mail | 1 | 1 | 1 + 1 | 2 |
|               |          | heruntergeladene Pinnwand | 3 | 2 | 3 + 2 | 5 |
| **Gesamtwert der Entscheidungsfindung** |         |             |                 |             |      | **52** |
|               |          |             |                 |             |      |           |
| Beeinflusser | John | Besuchte Website | 19 | 9 | 19 + 9 | 28 |
| **Gesamtwert der Einflussnehmer** |         |             |                 |             |      | **28** |
|               |          |             |                 |             |      |           |
| Praktitioner | Bob | Angeklickte E-Mail | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Paul | Angeklickte E-Mail | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Calvin | Angeklickte E-Mail | 1 | 1 | 1 + 1 | 2 |
|               |          | Besuchte Website | 1 | 7 | 1 + 7 | 8 |
|               |          | heruntergeladene Pinnwand | 1 | 2 | 1 + 2 | 3 |
| **Gesamtergebnis der Praktizierenden** |         |             |                 |             |      | **17** |

Der endgültige Interaktionswert wird durch Anwendung der Gewichtung für die einzelnen Rollenbewertungen berechnet:

| Role | Gesamtbewertung der Rolle | Rollengewicht % | X-Gewicht des Score % |
|-------------- |---------------- |------------- |---------------- |
| Entscheidungsträger | 52 | 41,67% | 21,67 |
| Influencers | 28 | 33,33% | 9,33 |
| Praktikanten | 17 | 25 % | 4,25 |
| **Endgültige Interaktionsbewertung** |                |             | **35.25** |
