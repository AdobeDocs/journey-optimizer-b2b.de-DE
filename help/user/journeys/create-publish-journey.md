---
title: Konto-Journey erstellen und veröffentlichen
description: Erfahren Sie, wie Sie Account Journey erstellen und veröffentlichen.
feature: Account Journeys
source-git-commit: d03e0e2d8070916d38bb956adff8dea3f3873aad
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 1%

---

# Konto-Journey erstellen und veröffentlichen

Um mit einer Konto-Journey zu beginnen, erstellen Sie die Journey und erstellen Sie dann den Knoten- und Journey-Fluss im Journey-Editor.

![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Übersichtsvideo ansehen](#overview-video)

## Konto-Journey erstellen

1. Klicken Sie im linken Navigationsbereich auf **[!UICONTROL Account Journey]**.

1. Klicken **[!UICONTROL oben rechts]** der Seite auf „Konto-Journey erstellen“.

1. Geben Sie im Dialogfeld einen eindeutigen **[!UICONTROL Namen“ (]**) und &quot;**[!UICONTROL &quot;]** optional) ein.

   ![Dialogfeld „Konto-Journey erstellen“](./assets/account-journey-create-dialog.png){width="400"}

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

## Bausteine einer Journey

Die _Journey-Zuordnung_ ist der zentrale Bereich im Journey-Designer. In diesem Bereich können Sie Journey-Knoten hinzufügen und konfigurieren. Klicken Sie auf einen Knoten, um seinen Eigenschaftenbereich rechts von der Arbeitsfläche zu öffnen und ihn entsprechend Ihrem Design festzulegen. Eine Konto-Journey beginnt immer mit einem [Konto-Zielgruppenknoten](./account-audience-nodes.md) in dem Sie Ihrer Journey Eingaben hinzufügen können.

Nachdem Sie eine Konto-Journey erstellt und die Audience hinzugefügt haben, erstellen Sie die Journey mithilfe von -Knoten. Die Journey-Zuordnung bietet eine Arbeitsfläche, auf der Sie Ihre mehrstufigen B2B-Marketing-Anwendungsfälle mithilfe der folgenden Knotentypen erstellen können, um eine Account-Journey zu erstellen:

* [Aktion ausführen](./action-nodes.md)
* [Überwachen eines Ereignisses](./listen-for-event-nodes.md)
* [Pfade aufteilen](./split-merge-paths-nodes.md)
* [Warten](./wait-nodes.md)
* [Zusammenführen von Pfaden](./split-merge-paths-nodes.md)

## Leitplanken

Die folgenden Leitplanken sind vorhanden, damit Sie eine Journey erstellen können, ohne Fehler zu verursachen:

* _Löschen eines Knotens mit aufgeteiltem Pfad_: Zum Löschen eines Knotens müssen alle nachfolgenden Knoten in jedem Pfad gelöscht werden.
* _Löschen eines Zusammenführungsknotens_: Ein Zusammenführungsknoten kann nur gelöscht werden, wenn ein Pfad mit ihm verbunden ist. Um einen Zusammenführungsknoten zu löschen, lassen Sie nur einen Pfad ausgewählt.
* _Wechseln zwischen Konto und Personen_: Sie können die Auswahl von Konten zu Personen nicht ändern, ohne alle nachfolgenden Knoten in jedem Pfad zu löschen.

## Knoten hinzufügen

1. Navigieren Sie zum Journey-Editor.

1. Klicken Sie auf das Pluszeichen ( **+** ) im Pfad und wählen Sie den Knotentyp aus.

1. Legen Sie die Knoteneigenschaften rechts fest.

## Löschen eines Knotens

1. Navigieren Sie zum Journey-Editor.

1. Klicken Sie in den Knoteneigenschaften auf der rechten Seite auf das Symbol _Löschen_ ( ![Löschsymbol](../assets/do-not-localize/icon-delete.svg) ).

1. Klicken Sie im Bestätigungsdialogfeld auf **[!UICONTROL Löschen]**.

## Hinzufügen und Löschen eines Pfads

1. Navigieren Sie zum Journey-Editor.

1. Klicken Sie auf das Pluszeichen ( **+** ) auf dem Pfad und fügen Sie den [Pfadknoten aufteilen“ ](./split-merge-paths-nodes.md#split-paths).

1. Klicken Sie in den Knoteneigenschaften auf der rechten Seite auf **[!UICONTROL Konto]**.

1. Um weitere Pfade hinzuzufügen, klicken Sie auf **[!UICONTROL Pfad hinzufügen]**.

   Bei jedem Pfad, der auf der Journey erstellt wird, wird eine neue Pfadkarte in den Eigenschaften angezeigt.

1. Navigieren Sie zu einem der Pfade auf der Journey und fügen Sie [action](./action-nodes.md) oder [event](./listen-for-event-nodes.md)-Knoten mithilfe des Pluszeichens zu diesem Pfad hinzu.

1. Wählen Sie den [Aufspaltungspfad](./split-merge-paths-nodes.md)-Knoten aus, um die Eigenschaften auf der rechten Seite zu öffnen.

   Die Pfade mit Knoten auf ihnen können nicht gelöscht werden.

1. Um diese Pfade zu löschen, müssen Sie zuerst alle Knoten in diesem Pfad löschen.

## Journey planen

Wenn Sie eine Journey veröffentlichen, kann diese sofort oder an einem geplanten Datum in der Zukunft gestartet werden. Das Enddatum kann maximal drei Jahre ab dem Startdatum betragen. Nach der Veröffentlichung einer Journey (_Live_-Status) können Sie das Enddatum der Journey, nicht aber das Startdatum aktualisieren.

1. Navigieren Sie zur Journey-Karte.

1. Planen Sie den Journey, indem Sie in der Kopfzeile auf **[!UICONTROL Journey]** Einstellungen} klicken.

1. Legen Sie im Dialogfeld die Zeitplanoptionen fest:

   * Wählen Sie einen Zeitplantyp aus.

     Um die Journey zum Zeitpunkt der Veröffentlichung zu aktivieren, wählen Sie **[!UICONTROL Sofort]**.

     Um die Journey für ein Datum in der Zukunft zu aktivieren, wählen Sie **[!UICONTROL An einem bestimmten Datum]** und klicken Sie auf das _Kalender_-Symbol, um das Datum auszuwählen.

     Dialogfeld für ![Journey-Einstellungen](./assets/account-journey-settings-dialog.png){width="400" zoomable="no"}

   * Geben Sie das **[!UICONTROL Enddatum]** für die Journey an. Sie kann maximal drei Jahre vom Startdatum entfernt sein (dieses Feld ist für die Veröffentlichung erforderlich).

1. Klicken Sie auf **[!UICONTROL Speichern]**.

   Wenn Sie bereit sind, Ihren Journey zu veröffentlichen, können Sie diese Einstellungen überprüfen, wenn Sie auf &quot;_[!UICONTROL &quot;]_.

## Konto-Journey veröffentlichen

Wenn die Konto-Journey fehlerfrei ist, können Sie sie veröffentlichen.

1. Klicken Sie oben rechts in der Journey-Zuordnung auf **[!UICONTROL Veröffentlichen]**.

1. Legen Sie _[!UICONTROL Dialogfeld &quot;Journey-Einstellungen überprüfen]_ die Journey-Startoptionen fest.

   Wenn Sie die Journey-Einstellungen bereits festgelegt haben, um einen Zeitplan zu definieren, überprüfen Sie die Einstellungen.

   Wenn Sie die Journey-Aktivierung festlegen müssen, wählen Sie einen Zeitplantyp aus:

   * Um die Journey zum Zeitpunkt der Veröffentlichung zu aktivieren, wählen Sie **[!UICONTROL Sofort]**.

   * Um die Journey für ein Datum in der Zukunft zu aktivieren, wählen Sie **[!UICONTROL An einem bestimmten Datum]** und klicken Sie auf das _Kalender_-Symbol, um das Datum auszuwählen.

1. Geben Sie bei Bedarf das **[!UICONTROL Enddatum]** für die Journey an.

   Dialogfeld für ![Journey-Einstellungen](./assets/journey-publish-dialog.png){width="400" zoomable="no"}

   Sie kann maximal drei Jahre vom Startdatum entfernt sein (dieses Feld ist für die Veröffentlichung erforderlich).

1. Klicken Sie auf **[!UICONTROL Weiter]**.

1. Klicken Sie im Bestätigungsdialogfeld auf **[!UICONTROL Veröffentlichen]**.

## Übersichtsvideo

>[!VIDEO](https://video.tv.adobe.com/v/3443204/?learn=on)
