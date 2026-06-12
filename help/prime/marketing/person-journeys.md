---
title: Personen-Journeys
description: Platzhalterseite für Personen-Journey.
autotag-review: '2026-06-12T23:03:17.139Z'
TQID: 'https://experienceleague.adobe.com/MhkAuypbebo-n9uwxFPUKbNgyHijaTnaVsqhs9-lXC0'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: ba367494-9862-4596-bd6f-299c7e10a46b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: cb3217c9fd7beb712d0c61638d143b798010d2b7
workflow-type: tm+mt
source-wordcount: 683
ht-degree: 22%

---

# Personen-Journeys

In Journey Optimizer B2B edition Prime sind Personen-Journey automatisierte, mehrstufige Lead-basierte Marketing-Pläne, die Marketo Engage-Daten verwenden und personalisierte Erlebnisse als Reaktion auf Interaktionen, Geschäftsereignisse oder geplante Kampagnen kanalübergreifend orchestrieren.

So beginnen Sie mit Ihrer First Person Journey:

1. Erstellen Sie eine Personen-Journey.
1. Fügen Sie die Knoten hinzu und definieren Sie den Journey-Fluss in der Journey-Zuordnung.
1. Veröffentlichen Sie die Journey.

## Zugreifen auf und Durchsuchen von Journey-Personen

Erweitern Sie in der linken Navigationsleiste **[!UICONTROL Marketing-]**) und wählen Sie **[!UICONTROL Personen-Journey]**.

Um die angezeigte Liste nach Namen zu filtern _können Sie oben in der Liste_ Text in das Tool „Suchen“ eingeben.

### Journey von Listenspalten

Die Listenseite Journey enthält die folgenden Spalten:

Name (klicken Sie auf den Namen, um die Journey-Zuordnung zur Bearbeitung zu öffnen)
Status
Erstellungsdatum
Erstellt von
Letzte Aktualisierung
Zuletzt aktualisiert von
Veröffentlicht am
Veröffentlicht von
Startdatum
Enddatum

Sie können die Liste nach Status, Erstellungsdatum oder Letztes Update sortieren, indem Sie auf die Spaltenüberschrift klicken.

Um die in der Tabelle angezeigten Spalten anzupassen (ein-/auszublenden), klicken Sie auf das Symbol Tabelle anpassen ( ) in der oberen rechten Ecke. Aktivieren oder deaktivieren Sie die Kontrollkästchen im Dialogfeld und klicken Sie auf Anwenden.

### Journey-Status

Der Status einer Journey kann sich entsprechend den von Ihnen durchgeführten Aktionen ändern. Je nach Status einer Journey stehen bestimmte Aktionen rechts in der Kopfzeile zur Verfügung oder nicht.

| Status | Beschreibung | Verfügbare Aktionen |
| ------ | ----------- | ----------------- |
| Entwurf | Eine unveröffentlichte Journey, die bearbeitet werden kann. | <li>Veröffentlichen <li>Duplizieren <li>Löschen |
| Live | Der Journey-Status ändert sich von Entwurf zu Live, wenn eine Journey veröffentlicht wird. In diesem Status kann sie nicht mehr bearbeitet werden. | <li>Duplizieren |
| Beendet | Wenn alle Mitglieder der Konto- oder Personen-Zielgruppe auf einer Journey die Journey abgeschlossen haben, ändert sich der Status von Live oder Geschlossen zu Neue Einträge zu Beendet. | <li>Duplizieren <li>Löschen |

## Erstellen einer Personen-Journey

1. Klicken **[!UICONTROL oben rechts]** der Journey-Liste auf &quot;Journey erstellen“.

1. Geben Sie im Dialogfeld einen eindeutigen **[!UICONTROL Namen“ (]**) und &quot;**[!UICONTROL &quot;]** optional) ein.

<!-- 
   ![Create Journey dialog](./assets/person-journey-create-dialog.png){width="400"}
-->

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

### Journey-Design

Die _Journey-Zuordnung_ ist der zentrale Bereich im Journey-Arbeitsbereich. Hier können Sie Journey-Knoten hinzufügen und konfigurieren. Klicken Sie auf einen Knoten, um seine Eigenschaften im Bedienfeld rechts neben dem Layout zu öffnen und sie entsprechend Ihrem Design festzulegen. Eine Personen-Journey beginnt immer mit einem _[!UICONTROL Personen-Zielgruppe]_-Knoten, auf dem Sie die Eingabe für die Journey definieren können.

<!--
   ![Journey map for newly created journey](./assets/person-journey-create-dialog.png){width="400"}
-->

Nachdem Sie eine Personen-Journey erstellt und die Personen-Audience hinzugefügt haben, erstellen Sie die Journey mithilfe von -Knoten. Die Journey-Zuordnung bietet eine Arbeitsfläche, auf der Sie Ihre mehrstufigen B2B-Marketing-Anwendungsfälle erstellen können, indem Sie die folgenden Knotentypen verwenden, um die Journey zu erstellen:

* [Durchführen einer Aktion](./action-nodes.md)
* [Auf ein Ereignis lauschen](./listen-for-event-nodes.md)
* [Warten](./wait-nodes.md)
* [Pfade aufteilen](./split-merge-paths-nodes.md)
* [Nächster bester Pfad](./next-best-path.md)
* [Pfade zusammenführen](./split-merge-paths-nodes.md)


## Journey-Verwaltung



## Journey Map

Klicken Sie auf den Namen (als Link angezeigt) in der Liste Journey , um die Details zu überprüfen, Änderungen vorzunehmen und Maßnahmen zu ergreifen.

Die Kopfzeile jeder Journey-Zuordnung enthält:

Journey-Name
Bearbeitungswerkzeug für den Journey-Namen (Bearbeitungssymbol)
Status der Journey
Über die Journey-Zuordnung können Sie die Knoten hinzufügen und den Journey-Fluss definieren.

### Journey-Aktionen

Die Journey-Listenseite enthält alle Journey von Konten oder Personen in Ihrer Journey Optimizer B2B edition-Instanz. Auf der Listenseite können Sie eine Reihe von Aktionen auf eine Journey anwenden.



#### Duplizieren einer Journey

Die Aktion „Duplizieren“ ähnelt einer Klonfunktion, wobei eine duplizierte Journey aber keine erstellten Journey-Inhalts-Assets enthält. Sie können die Details für die Journey duplizieren, oder nur ein einfaches Skelett der Fluss- und Pfadstruktur.

HINWEIS

Klicken Sie auf das Symbol Mehr (…) neben dem Journey-Namen und wählen Sie Duplizieren.

Abhängig vom Status der Journey können Sie über die Journey-Details oder die Journey-Zuordnung auch auf die Duplikataktion zugreifen:

Für eine Journey als Entwurf klicken Sie oben rechts auf das Menü Mehr… und wählen Sie Duplizieren.
Klicken Sie für alle anderen Journey-Status oben rechts auf Duplizieren .
Legen Sie im Dialogfeld Journey duplizieren den Namen und die Beschreibung für die neue Journey fest.
Standardmäßig verwendet das Dialogfeld den Namen der duplizierten Journey, an die _copy angehängt wird. Geben Sie bei Bedarf einen anderen eindeutigen Namen für die Journey ein.

Auswahl des Duplikatstyps:
Partielle Inhaltsduplizierung - Verwenden Sie diesen Typ, um alles auf der Journey zu kopieren, mit Ausnahme aller erstellten E-Mails oder SMS-Nachrichten. Knoten, die auf eine Marketo Engage-E-Mail- oder -SMS-Nachricht verweisen, sind vollständig intakt.
Ohne Details duplizieren - Verwenden Sie diesen Typ, um nur die Knotenstruktur und die Pfade zu kopieren. Alle Knoteneinstellungen und Pfadbedingungen sind nicht definiert (Standard), sodass Sie den grundlegenden Fluss mit verschiedenen Zielgruppen-, Aktionen- und Pfadsegmentierungseinstellungen wiederverwenden können. Für alle Warteknoten wird der Standardwert von fünf Tagen verwendet.
Klicken Sie auf Duplizieren.
Die duplizierte Journey wird in der Journey-Zuordnung geöffnet, wo Sie die Details festlegen und Journey-Inhalte nach Bedarf erstellen können.

Löschen einer Journey

Verwenden Sie die Aktion „Löschen“, um eine Journey dauerhaft zu löschen. Live-Journeys oder geplante Journeys können nicht gelöscht werden.

Klicken Sie auf das Symbol Mehr (…) neben dem Journey-Namen und wählen Sie Löschen .
Je nach Status der Journey können Sie auch über die Journey-Details oder die Journey-Zuordnung auf die Löschaktion zugreifen:

Für eine Journey als Entwurf klicken Sie oben rechts auf das Menü Mehr… und wählen Sie Löschen.
Klicken Sie für andere Journey-Status wie „Beendet“ oder „Abgebrochen“ oben rechts auf „Löschen“.
Klicken Sie im Bestätigungsdialogfeld auf Löschen.






