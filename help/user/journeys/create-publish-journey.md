---
title: Erstellen und Veröffentlichen einer Journey
description: Erstellen Sie Konto- und Personen-Journey in der visuellen Arbeitsfläche, fügen Sie Aktions- und Ereignisknoten hinzu, konfigurieren Sie die Zeitplanung und veröffentlichen Sie für die Live-Orchestrierung in Journey Optimizer B2B Edition.
feature: Account Journeys
role: User
exl-id: f536b1a1-8dfe-437f-a84d-b66879529621
autotag-review: 2026-03-30T23:14:46.843Z
TQID: 'https://experienceleague.adobe.com/-emMaxlrae40JXP0tThacD3xA27d5OzO8tX6o-mOnfg'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
    internal-label: Journeys
subfeature_v2:
  - id: c31bc6c7-76bc-467b-80c0-7315a4e3f6be
    internal-label: Account Journeys
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
    internal-label: Customer journeys
source-git-commit: 9d5641659907d61be992ed218088a023a5211c56
workflow-type: tm+mt
source-wordcount: '1101'
ht-degree: 5%
---
# Erstellen und Veröffentlichen einer Journey

Um eine neue Journey zu beginnen, erstellen Sie die Journey und erstellen Sie dann den Knoten- und Journey-Fluss in der Journey-Map.

![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Übersichtsvideo ansehen](#overview-video)

## Erstellen einer Journey

Wählen Sie unter **[!UICONTROL Journey]** Verwaltung im linken Navigationsbereich den Journey-Typ aus, den Sie erstellen möchten:

* **[!UICONTROL Account Journey]**
* **[!UICONTROL Personen-Journey]**

_So fügen Sie eine neue Journey hinzu :_

+++Konto-Journey

1. Klicken **[!UICONTROL oben rechts]** der Seite auf „Konto-Journey erstellen“.

1. Geben Sie im Dialogfeld einen eindeutigen **[!UICONTROL Namen“ (]**) und &quot;**[!UICONTROL &quot;]** optional) ein.

   ![Dialogfeld „Konto-Journey erstellen“](./assets/account-journey-create-dialog.png){width="400"}

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

+++

+++Personen-Journey

1. Klicken **[!UICONTROL oben rechts]** der Seite auf &quot;Journey erstellen“.

1. Geben Sie im Dialogfeld einen eindeutigen **[!UICONTROL Namen“ (]**) und &quot;**[!UICONTROL &quot;]** optional) ein.

   ![Dialogfeld &quot;Journey erstellen“](./assets/person-journey-create-dialog.png){width="400"}

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

+++

## Komponenten für das Journey-Design

Die _Journey-Zuordnung_ ist der zentrale Bereich im Journey-Arbeitsbereich. In diesem Bereich können Sie Journey-Knoten hinzufügen und konfigurieren. Klicken Sie auf einen Knoten, um seinen Eigenschaftenbereich rechts von der Arbeitsfläche zu öffnen und ihn entsprechend Ihrem Design festzulegen. Eine Journey beginnt immer mit einem Zielgruppenknoten, auf dem Sie die Eingabe für Ihren Journey definieren können:

* [Konto-Zielgruppenknoten](./account-audience-nodes.md)
* [Zielgruppenknoten Person](./person-audience-nodes.md)

Nachdem Sie eine Konto-Journey erstellt und die Zielgruppe hinzugefügt haben, entwerfen Sie die Journey mit -Knoten. Die Journey-Zuordnung bietet eine Arbeitsfläche, auf der Sie Ihre mehrstufigen B2B-Marketing-Anwendungsfälle mithilfe der folgenden Knotentypen erstellen können, um eine Account-Journey zu erstellen:

* [Durchführen einer Aktion](./action-nodes.md)
* [Warten auf ein Ereignis](./listen-for-event-nodes.md)
* [Pfade aufteilen](./split-merge-paths-nodes.md)
* [Pfade für aufgeteilte Varianten](./variant-split-paths-nodes.md)
* [Nächster bester Pfad](./next-best-path-node.md)
* [Warten](./wait-nodes.md)
* [Pfade zusammenführen](./split-merge-paths-nodes.md)

## Leitlinien

Die folgenden Leitplanken sind vorhanden, um beim Erstellen eines Journey ohne Fehler zu helfen:

* _Löschen eines Knotens mit aufgeteiltem Pfad_: Zum Löschen eines Knotens müssen alle nachfolgenden Knoten in jedem Pfad gelöscht werden.
* _Löschen eines Zusammenführungsknotens_: Ein Zusammenführungsknoten kann nur gelöscht werden, wenn ein Pfad mit ihm verbunden ist. Um einen Zusammenführungsknoten zu löschen, lassen Sie nur einen Pfad ausgewählt.
* _Wechseln zwischen Konten und Personen_: Wenn Sie die Auswahl von Konten auf Personen ändern, werden alle nachfolgenden Knoten in jedem Pfad gelöscht.

## Knoten hinzufügen

1. Navigieren Sie zur Journey-Karte.

1. Klicken Sie auf das Pluszeichen ( **+** ) im Pfad und wählen Sie den Knotentyp aus.

   ![Klicken Sie auf + und wählen Sie den Typ aus, um dem Pfad einen Journey-Knoten hinzuzufügen](./assets/node-add-menu.png){width="400" zoomable="no"}

   Die verfügbaren Knotentypen hängen vom Journey-Typ und dem Pfadkontext ab. Weitere Informationen finden Sie unter {0 _[&#128279;](./journey-nodes.md)Journey-Knoten}._

1. Legen Sie die Knoteneigenschaften rechts fest.

   Die Eigenschaften hängen vom Knotentyp ab.

## Kennzeichnen von Knoten {#label-a-node}

[!DNL Adobe Journey Optimizer B2B Edition] zeigt jeder Knoten auf der Journey-Zuordnung seinen Standardnamen an, z. B. _Warten_ oder _E-Mail senden_. Fügen Sie Anzeigebeschriftungen hinzu, um Knoten desselben Typs zu unterscheiden und den Zweck jedes Schritts anzugeben. Verwenden Sie beispielsweise _48-Stunden-_ oder _Begrüßungs-E-Mail_.

Sie können einem beliebigen Knoten auf einer Konto-Journey oder Personen-Journey eine Anzeigelabel hinzufügen.

1. Wählen Sie in der Journey-Zuordnung den Knoten aus, den Sie beschriften möchten.

1. Geben Sie in den Knoteneigenschaften den Text in das Feld **[!UICONTROL Titel anzeigen]** ein.

   Die Bezeichnung kann bis zu 255 Zeichen lang sein.

1. Klicken Sie außerhalb des Felds, um die Bezeichnung anzuwenden.

   ![Fügen Sie eine Anzeigebeschriftung hinzu, um den Knoten auf der Journey zu unterscheiden](./assets/node-display-label.png){width="500" zoomable="no"}

   Die Beschriftung ersetzt den Standardnamen auf dem Knoten in der Journey-Zuordnung.

Um den Standardnamen wiederherzustellen, löschen Sie das Feld **[!UICONTROL Beschriftung anzeigen]** und klicken Sie außerhalb des Felds.

Beim Veröffentlichen der Journey wird die Anzeigebeschriftung für jeden Knoten mit der veröffentlichten Journey gespeichert.

>[!NOTE]
>
>Anzeigebeschriftungen sind nicht für Knoten in Journey verfügbar, die erstellt wurden, bevor diese Funktion verfügbar war.

Knotenbezeichnungen sind im `AJOB2B - 1.5.4 - journey node` und `AJOB2B-1_5_4-journey_node` Datensatz verfügbar. Sie können in [!DNL Adobe Experience Platform] Kennzeichnungen abfragen und sie für das Reporting in [!DNL Adobe Customer Journey Analytics] verwenden. Weitere Informationen zum Abfragen der exportierten Daten finden Sie im Abschnitt [Voraussetzungen für Datensatzabfragen](../data/aep-query-examples.md#prerequisites).

## Löschen eines Knotens

1. Navigieren Sie zur Journey-Karte.

1. Klicken Sie in den Knoteneigenschaften auf der rechten Seite auf das Symbol _Löschen_ ( ![Löschsymbol](../assets/do-not-localize/icon-delete.svg) ).

1. Klicken Sie im Bestätigungsdialog auf **[!UICONTROL Löschen]**.

## Hinzufügen und Löschen eines Pfads

1. Klicken Sie in der Journey-Zuordnung auf das Pluszeichen ( **+** ) auf dem Pfad und fügen Sie den [Pfadknoten aufteilen](./split-merge-paths-nodes.md#split-paths) hinzu.

1. Klicken Sie in den Knoteneigenschaften auf der rechten Seite auf **[!UICONTROL Konto]**.

1. Um weitere Pfade hinzuzufügen, klicken Sie auf **[!UICONTROL Pfad hinzufügen]**.

   Für jeden Pfad, der auf der Journey erstellt wird, wird eine neue Pfadkarte in den Eigenschaften angezeigt.

1. Navigieren Sie zu einem der Pfade auf der Journey und fügen Sie [action](./action-nodes.md) oder [event](./listen-for-event-nodes.md)-Knoten mithilfe des Pluszeichens zu diesem Pfad hinzu.

1. Wählen Sie den [Aufspaltungspfad](./split-merge-paths-nodes.md)-Knoten aus, um die Eigenschaften auf der rechten Seite zu öffnen.

   Pfade mit -Knoten können nicht gelöscht werden.

1. Um einen Pfad zu löschen, müssen Sie zuerst alle Knoten auf diesem Pfad löschen.

## Journey planen

Wenn Sie eine Journey veröffentlichen, kann diese sofort oder an einem geplanten Datum in der Zukunft gestartet werden. Das Enddatum kann maximal drei Jahre ab dem Startdatum betragen. Nach der Veröffentlichung einer Journey (_Live_-Status) können Sie das Enddatum der Journey, nicht aber das Startdatum aktualisieren.

1. Navigieren Sie zur Journey-Karte.

1. Planen Sie den Journey, indem Sie in der Kopfzeile auf **[!UICONTROL Journey]** Einstellungen&rbrace; klicken.

1. Legen Sie im Dialogfeld die Zeitplanoptionen fest:

   * Wählen Sie einen Zeitplantyp aus.

     Um die Journey zum Zeitpunkt der Veröffentlichung zu aktivieren, wählen Sie **[!UICONTROL Sofort]**.

     Um die Journey für ein Datum in der Zukunft zu aktivieren, wählen Sie **[!UICONTROL An einem bestimmten Datum]** und klicken Sie auf das _Kalender_-Symbol, um das Datum auszuwählen.

     Dialogfeld für ![Journey-Einstellungen](./assets/account-journey-settings-dialog.png){width="400" zoomable="no"}

   * Geben Sie das **[!UICONTROL Enddatum]** für die Journey an. Sie kann maximal drei Jahre vom Startdatum entfernt sein (dieses Feld ist für die Veröffentlichung erforderlich).

1. Klicken Sie auf **[!UICONTROL Speichern]**.

   Wenn Sie bereit sind, Ihren Journey zu veröffentlichen, können Sie diese Einstellungen überprüfen, wenn Sie auf &quot;_[!UICONTROL &quot;]_.

## Veröffentlichen einer Journey

Sie können eine Journey veröffentlichen, wenn keine Blocker-Fehler vorliegen. Nach der Veröffentlichung ändert sich der Journey-Status in _Live_. Wenn der Journey Fehler aufweist, ist die Schaltfläche _[!UICONTROL Veröffentlichen]_ mit folgenden Inhaltsinformationen abgeblendet: `Resolve errors before publishing`.

>[!NOTE]
>
>Nach der Veröffentlichung einer Account-Journey gibt es eine Verzögerung von bis zu 24 Stunden, bis qualifizierte Accounts die Journey betreten können.

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
