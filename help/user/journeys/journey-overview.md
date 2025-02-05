---
title: Konto-Journeys
description: Erfahren Sie mehr über Account Journey und wie Sie sie erstellen und verwalten können.
feature: Account Journeys
exl-id: 5c22f11f-1967-4b55-8aee-16371173c040
source-git-commit: 279bc07b90da96c3d497f67a14596a3bed308984
workflow-type: tm+mt
source-wordcount: '1141'
ht-degree: 2%

---


# Account Journey

Erstellen und führen Sie Journey aus, die für jede kaufende Gruppe und jedes kaufende Gruppenmitglied maßgeschneidert sind, indem Sie automatisierte Interaktionen für E-Mail, SMS, Ereignisse und mehr verwenden. Mit Account Journey können Sie die Nachfragegenerierung und die Kaufgruppenqualifizierung optimieren und mehr qualifizierte Nachfrage für Ihre Akquise-, Upsell-/Crosssell- und Kundenbindungsprogramme steigern.

Definieren Sie eine verkaufsgesteuerte Interaktion, die E-Mail, SMS und mehr innerhalb der Account-Journey umfasst, um das eingehende Marketing mit ausgehenden Verkaufsaktivitäten für jedes Mitglied der Einkaufsgruppe zu koordinieren.

## Zugreifen auf und Durchsuchen von Account-Journey

1. Klicken Sie auf Ihrer Adobe Experience Platform-Startseite auf Adobe Journey Optimizer B2B edition.

1. Klicken Sie im linken Navigationsbereich auf **[!UICONTROL Account Journey]**.

   ![Zugriff auf Account Journey](./assets/account-journey-browse.png){width="800" zoomable="yes"}

   Die angezeigte Seite Journey enthält die folgenden Spalten:

   * [!UICONTROL Name] (auf den Namen klicken, um die Konto-Journey zur Bearbeitung zu öffnen)
   * [!UICONTROL Status]
   * [!UICONTROL Beschreibung]
   * [!UICONTROL Erstellt von]
   * [!UICONTROL Zuletzt aktualisiert um]
   * [!UICONTROL Zuletzt aktualisiert von]
   * [!UICONTROL Veröffentlicht am]
   * [!UICONTROL Veröffentlicht von]

Diese Tabelle bietet die Möglichkeit, nach Namen und „Erstellt von“ zu suchen. Die Sortierung ist derzeit nicht verfügbar.

Sie können die angezeigte Tabelle anpassen, indem Sie auf das Symbol _Spalten_ in der oberen rechten Ecke klicken und die Kontrollkästchen aktivieren oder deaktivieren.

![Wählen Sie die Spalten aus, die in der Liste der Konto-Journey angezeigt werden sollen](./assets/account-journeys-list-columns.png){width="800" zoomable="yes"}

## Anatomie einer Account-Journey

Klicken Sie auf den Namen (als Link angezeigt) in der Liste _[!UICONTROL Account-Journey]_, um die Details zu überprüfen, Änderungen vorzunehmen und Maßnahmen zu ergreifen.

![Konto-Journey-Arbeitsbereich](./assets/account-journey-workspace.png){width="800" zoomable="yes"}

Die Editor-Kopfzeile jeder Account-Journey enthält:

* Journey-Name
* Möglichkeit, den Namen zu bearbeiten (_Bearbeiten_-Symbol)
* Status der Journey

Die folgenden Aktionen sind in der Kopfzeile verfügbar:

* **Publish** - Sie können eine Journey veröffentlichen, wenn keine Blocker-Fehler vorliegen. Nach der Veröffentlichung ändert sich der Journey-Status in _Live_. Wenn die Journey Fehler aufweist, ist die Schaltfläche mit folgenden Inhaltsinformationen abgeblendet: `Resolve errors before publishing`.
* **Duplizieren** - Diese Aktion ähnelt einer Klonfunktion, aber die duplizierte Journey enthält keine Assets.
* **Für neue Einträge schließen** - Wenn Sie eine Journey schließen, setzen Konten, die sich derzeit auf der Journey befinden, ihren Pfad auf der Journey fort, sodass kein weiterer Journey-Eintritt möglich ist. Ein geschlossener Journey kann nicht neu gestartet werden. Sie können eine geschlossene Journey duplizieren.
* **Abbruch** - Wenn Sie eine Journey stoppen, stoppen Konten auf der Journey sofort ihren Fortschritt und es kann kein weiterer Journey-Eintritt erfolgen. Ein gestoppter Journey kann nicht neu gestartet werden. Wenn Sie neue Eintritte blockieren, ohne den Fortschritt der Benutzer zu stoppen, sollten Sie stattdessen die Journey schließen.
* **Löschen** - Durch diese Aktion wird die Journey dauerhaft gelöscht.

Der Status einer Journey ändert sich je nach den von Ihnen durchgeführten Aktionen. Je nach Status einer Journey sind bestimmte Aktionen in der Kopfzeile nicht verfügbar.

| Status | Beschreibung | Verfügbare Aktionen |
| ------ | ----------- | ----------------- |
| _**Entwurf**_ | Eine unveröffentlichte Journey, die bearbeitbar ist. | <ul><li>Veröffentlichen Sie</li><li>Doppelt </li><li>Löschen </li></ul> |
| _**Live**_ | Der Journey-Status ändert sich von Entwurf zu Live, wenn eine Journey veröffentlicht wird. In diesem Zustand ist er nicht mehr bearbeitbar. | <ul><li>Doppelt </li><li>Für neue Einträge schließen </li><li>Abbrechen </li></ul> |
| _**Für neue Einträge geschlossen**_ | Der Journey-Status ändert sich von _Live_ zu _Geschlossen zu neuen Einträgen_ wenn Sie im oberen Navigationsbereich auf [!UICONTROL Für neue Einträge schließen] klicken. | <ul><li>Doppelt </li><li>Abbrechen </li></ul> |
| _**abgebrochen**_ | Der Journey-Status ändert sich von _Live_ oder _Geschlossen zu neuen_, wenn Sie eine Journey abbrechen. Eine abgebrochene Journey kann nicht neu gestartet werden. | <ul><li>Doppelt </li><li>Löschen </li></ul> |
| _**BEENDET**_ | Wenn alle Konten auf einer Journey die Journey abgeschlossen haben, ändert sich der Status von Live oder Geschlossen zu Neue Einträge zu Beendet. | <ul><li>Doppelt </li><li>Löschen </li></ul> |

## Erste Schritte mit einer Journey

Um mit einer Konto-Journey zu beginnen, erstellen Sie die Journey und erstellen Sie dann den Knoten- und Journey-Fluss im Journey-Editor.

### Konto-Journey erstellen

1. Klicken Sie im linken Navigationsbereich auf **[!UICONTROL Account Journey]**.

1. Klicken **[!UICONTROL oben rechts]** der Seite auf „Konto-Journey erstellen“.

1. Geben Sie im Dialogfeld einen eindeutigen **[!UICONTROL Namen“ (]**) und &quot;**[!UICONTROL &quot;]** optional) ein.

   ![Dialogfeld „Konto-Journey erstellen“](./assets/account-journey-create-dialog.png){width="400"}

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

### Bausteine einer Journey

Die _Journey-Zuordnung_ ist der zentrale Bereich im Journey-Designer. In diesem Bereich können Sie Journey-Knoten hinzufügen und konfigurieren. Klicken Sie auf einen Knoten, um seinen Eigenschaftenbereich rechts von der Arbeitsfläche zu öffnen und ihn entsprechend Ihrem Design festzulegen. Eine Konto-Journey beginnt immer mit einem [Konto-Zielgruppenknoten](./account-audience-nodes.md) in dem Sie Ihrer Journey Eingaben hinzufügen können.

Nachdem Sie eine Konto-Journey erstellt und die Audience hinzugefügt haben, erstellen Sie die Journey mithilfe von -Knoten. Die Journey-Zuordnung bietet eine Arbeitsfläche, auf der Sie Ihre mehrstufigen B2B-Marketing-Anwendungsfälle mithilfe der folgenden Knotentypen erstellen können, um eine Account-Journey zu erstellen:

* [Aktion ausführen](./action-nodes.md)
* [Überwachen eines Ereignisses](./listen-for-event-nodes.md)
* [Pfade aufteilen](./split-merge-paths-nodes.md)
* [Warten](./wait-nodes.md)
* [Zusammenführen von Pfaden](./split-merge-paths-nodes.md)

### Leitplanken

Die folgenden Leitplanken sind vorhanden, damit Sie eine Journey erstellen können, ohne Fehler zu verursachen:

* _Löschen eines Knotens mit aufgeteiltem Pfad_: Sie können einen Knoten nicht löschen, ohne alle nachfolgenden Knoten in jedem Pfad zu löschen.
* _Löschen eines Zusammenführungsknotens_: Ein Zusammenführungsknoten kann nur gelöscht werden, wenn ein Pfad mit ihm verbunden ist. Um einen Zusammenführungsknoten zu löschen, lassen Sie nur einen Pfad ausgewählt.
* _Wechseln zwischen Konto und Personen_: Sie können die Auswahl von Konten zu Personen nicht ändern, ohne alle nachfolgenden Knoten in jedem Pfad zu löschen.

### Knoten hinzufügen

1. Navigieren Sie zum Journey-Editor.

1. Klicken Sie auf das Pluszeichen ( **+** ) im Pfad und wählen Sie den Knotentyp aus.

1. Legen Sie die Knoteneigenschaften rechts fest.

### Löschen eines Knotens

1. Navigieren Sie zum Journey-Editor.

1. Klicken Sie in den Knoteneigenschaften auf der rechten Seite auf das Symbol _Löschen_ ( ![Löschsymbol](../assets/do-not-localize/icon-delete.svg) ).

1. Klicken Sie im Bestätigungsdialogfeld auf **[!UICONTROL Löschen]**.

### Hinzufügen und Löschen eines Pfads

1. Navigieren Sie zum Journey-Editor.

1. Klicken Sie auf das Pluszeichen ( **+** ) auf dem Pfad und fügen Sie den [Pfadknoten aufteilen“ ](./split-merge-paths-nodes.md#split-paths).

1. Klicken Sie in den Knoteneigenschaften auf der rechten Seite auf **[!UICONTROL Konto]**.

1. Um weitere Pfade hinzuzufügen, klicken Sie auf **[!UICONTROL Pfad hinzufügen]**.

   Bei jedem Pfad, der auf der Journey erstellt wird, wird eine neue Pfadkarte in den Eigenschaften angezeigt.

1. Navigieren Sie zu einem der Pfade auf der Journey und fügen Sie [action](./action-nodes.md) oder [event](./listen-for-event-nodes.md)-Knoten mithilfe des Pluszeichens zu diesem Pfad hinzu.

1. Wählen Sie den [Aufspaltungspfad](./split-merge-paths-nodes.md)-Knoten aus, um die Eigenschaften auf der rechten Seite zu öffnen.

   Die Pfade mit Knoten auf ihnen können nicht gelöscht werden.

1. Um diese Pfade zu löschen, müssen Sie zuerst alle Knoten in diesem Pfad löschen.

### Journey planen

Wenn Sie eine Journey veröffentlichen, kann diese sofort oder an einem geplanten Datum in der Zukunft gestartet werden. Das Enddatum kann maximal drei Jahre ab dem Startdatum betragen. Nach der Veröffentlichung einer Journey (_Live_-Status) können Sie das Enddatum der Journey, nicht aber das Startdatum aktualisieren.

1. Navigieren Sie zum Journey-Editor.

1. Planen Sie den Journey, indem Sie in der Kopfzeile auf [!UICONTROL Journey]Einstellungen} klicken.

1. Legen Sie im Dialogfeld die Zeitplanoptionen fest:

   * Wählen Sie einen Zeitplantyp aus.

     Um die Journey zum Zeitpunkt der Veröffentlichung zu aktivieren, wählen Sie **[!UICONTROL Sofort]**.

     Um die Journey für ein Datum in der Zukunft zu aktivieren, wählen Sie **[!UICONTROL An einem bestimmten Datum]** und klicken Sie auf das _Kalender_-Symbol, um das Datum auszuwählen.

     Dialogfeld für ![Journey-Einstellungen](./assets/account-journey-settings-dialog.png){width="400" zoomable="no"}

   * Geben Sie das **[!UICONTROL Enddatum]** für die Journey an. Sie kann maximal drei Jahre vom Startdatum entfernt sein (dieses Feld ist erforderlich).

1. Klicken Sie auf **[!UICONTROL Speichern]**.

   Wenn Sie bereit sind, Ihren Journey zu veröffentlichen, können Sie diese Einstellungen überprüfen, wenn Sie auf _[!UICONTROL Publish]_ klicken.

### Publish - eine Konto-Journey


