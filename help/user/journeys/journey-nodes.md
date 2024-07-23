---
title: Journey-Knoten des Kontos
description: Erfahren Sie mehr über die Knotentypen, mit denen Sie Ihre Journey erstellen können.
feature: Account Journeys
exl-id: 4edb87d9-cdf8-47a4-968b-6dc76d97b89c
source-git-commit: 90946e472ba4757a2594e4303495a20ceb4fc890
workflow-type: tm+mt
source-wordcount: '1748'
ht-degree: 2%

---

# Journey-Knoten des Kontos

Nachdem Sie [ein Konto-Journey](journey-overview.md#create-an-account-journey) und [die Audience hinzugefügt haben](journey-overview.md#add-the-account-audience-for-your-journey), erstellen Sie die Journey mithilfe von Knoten. Die Journey-Karte bietet eine Arbeitsfläche, auf der Sie Ihre mehrstufigen B2B-Marketing-Anwendungsfälle erstellen können.

Erstellen Sie Ihre Konto-Journey, indem Sie die verschiedenen Aktions-, Ereignis- und Orchestrierungsknoten als mehrstufiges, kanalübergreifendes Szenario kombinieren. Jeder Knoten einer Journey stellt einen Schritt entlang eines logischen Pfads dar.

## Knoten &quot;Kontozielgruppe&quot;

Der Knoten [Zielgruppe des Kontos](journey-overview.md#add-the-account-audience-for-your-journey) definiert die Zielgruppe des Eingabedokuments (in Adobe Experience Platform erstellt und verwaltet) für die Journey. Dieser Knoten ist immer der erste Knoten und wird standardmäßig automatisch erstellt.

## Handeln

Führen Sie eine Aktion wie den Versand einer E-Mail, die Änderung der Punktzahl usw. aus.

**Aktion für Konten**: Die Aktion wird auf alle Personen angewendet, die Teil der Konten auf diesem Pfad sind.

**Aktion für Personen**: Die Aktion wird auf alle Personen auf diesem Pfad angewendet. Eine Aktion für Personen kann innerhalb des Aufspaltungspfads von Personen verwendet oder durch Konten aufgeteilt werden.

| Knotenkontext | Funktion | Einschränkungen |
| ------------ | -------- | ----------- |
| [Personen](#add-a-people-action) | Zuweisen zu einer Kaufgruppe | Lösungsinteresse auswählen<br/>Rolle auswählen |
| | Entfernen aus der Gruppe &quot;Kaufen&quot; | Lösungsinteresse auswählen |
| | SMS senden | SMS erstellen |
| | Zur Marketo Engage-Anforderungskampagne hinzufügen | Marketo Engage-Arbeitsbereich auswählen<br/>Auswahl der Anforderungskampagne |
| | Ändern der Personenpartition in Marketo Engage | Neue Partition |
| | Person interessant Moment | Typ<br/>Beschreibung |
| | Bewertung ändern | Score name<br/>change |
| | E-Mail senden | Neue E-Mail erstellen<br/>E-Mail aus Marketo Engage auswählen |
| [Konten](#add-an-account-action) | Versandwarnung | Lösungsinteresse auswählen<br/>E-Mail an senden |
| | Konto zur (anderen) Journey hinzufügen | Live-Konto-Journey auswählen |
| | Aktualisieren des Status der Gruppe kaufen | Lösungsinteresse<br/>Status (erforderlich, max. 50 Zeichen) |
| | Konto aus (aktueller) Journey entfernen | Live-Konto-Journey auswählen |
| | Moment des Kontointeressens | Typ (E-Mail, Meilenstein oder Web)<br/>Beschreibung (optional) |
| | Datenwert für Kontoänderung | Attribut auswählen<br/>Neuer Wert |

### Hinzufügen einer Kontoaktion

1. Navigieren Sie zum Journey-Editor.

1. Klicken Sie auf das Pluszeichen ( **+** ) auf einem Pfad und wählen Sie **[!UICONTROL Aktion durchführen]**.

   ![Journey-Knoten hinzufügen - geteilte Pfade](./assets/add-node-action.png){width="400"}

1. Wählen Sie in den Knoteneigenschaften auf der rechten Seite **[!UICONTROL Konten]** für die Aktion.

1. Wählen Sie eine Aktion aus der Liste aus und legen Sie die Werte für die Aktion fest.

   ![Journey-Knoten - Ausführen einer Aktion für ein Konto](./assets/node-take-action-account.png){width="700" zoomable="yes"}

### Hinzufügen einer Personenaktion

1. Navigieren Sie zum Journey-Editor.

1. Klicken Sie auf das Pluszeichen ( **+** ) auf einem Pfad und wählen Sie **[!UICONTROL Aktion durchführen]**.

1. Wählen Sie in den Knoteneigenschaften auf der rechten Seite **[!UICONTROL Personen]** für die Aktion.

1. Wählen Sie eine Aktion aus der Liste aus und legen Sie die Werte für die Aktion fest.

![Journey-Knoten - Ausführen einer Aktion für Personen](./assets/node-take-action-people.png){width="700" zoomable="yes"}

## Suchen nach einem Ereignis

Verschieben Sie Ihre Zielgruppe zum nächsten Schritt im Journey, wenn ein Ereignis auftritt.

* Sie können auch festlegen, wie lange die Journey auf dieses Ereignis wartet. Die Journey endet nach einer Zeitüberschreitung.
* Darüber hinaus können Sie weitere Knoten zu Ihrem Timeout-Pfad hinzufügen.

**Ereignisse in Konten verfolgen**: Wenn mindestens eine Person aus einem Konto ein Trigger ist, wechselt das Konto zum nächsten Schritt auf der Journey.

**Ereignisse für Personen überwachen**: Ereignisse für Personen können nur auf einen Kontopfad angewendet werden. Es ist nicht für eine Aufspaltung durch Personen-Knoten verfügbar.

| Knotenkontext | Funktion | Einschränkungen |
| ------------ | -------- | ----------- |
| [Personen](#add-a-people-event) | Datenwertänderungen | Attribut<br/>Zusätzliche Einschränkungen (optional)<br/>Timeout (optional) |
| | Klickt auf Link in E-Mail | E-Mail<br/>Zusätzliche Einschränkungen (optional)<br/>Timeout (optional) |
| | Zugeordnet zur Einkaufsgruppe | Lösungsinteresse<br/>Zusätzliche Einschränkungen (optional)<br/>Zeitüberschreitung (optional) |
| | Öffnet E-Mail | E-Mail<br/>Zusätzliche Einschränkungen (optional)<br/>Timeout (optional) |
| | Bewertung wird geändert | Score name<br/>Zusätzliche Einschränkungen (optional)<br/>Timeout (optional) |
| | Aus der Kaufgruppe entfernt | Lösungsinteresse<br/>Aktivitätsdatum (optional)<br/>Zeitüberschreitung (optional) |
| [Konten](#add-an-account-event) | Änderung des Status der gekauften Gruppe | Lösungsinteresse<br/>Zusätzliche Einschränkungen (optional)<br/>Zeitüberschreitung (optional) |
| | Änderung der Vollständigkeitsbewertung | Lösungsinteresse<br/>Zusätzliche Einschränkungen (optional)<br/>Zeitüberschreitung (optional) |
| | Konto hatte einen interessanten Moment | Typ<br/>Zusätzliche Einschränkungen (optional)<br/>Zeitüberschreitung (optional) |
| | Änderung der Interaktionsbewertung | Lösungsinteresse<br/>Zusätzliche Einschränkungen (optional)<br/>Zeitüberschreitung (optional) |
| | Änderung des Kontodatenwerts | Attribut<br/>Zusätzliche Einschränkungen (optional)<br/>Timeout (optional) |

### Hinzufügen eines Kontoereignisses

1. Navigieren Sie zum Journey-Editor.

1. Klicken Sie auf das Pluszeichen ( **+** ) auf einem Pfad und wählen Sie **[!UICONTROL Nach einem Ereignis suchen]**.

1. Wählen Sie in den Knoteneigenschaften auf der rechten Seite **[!UICONTROL Konten]** für den Ereignistyp aus.

   ![Journey-Knoten - Ereignisse auf Konto überwachen](./assets/node-listen-events-account.png){width="700" zoomable="yes"}

1. Wählen Sie ein Ereignis aus der Liste aus.

1. Klicken Sie auf **[!UICONTROL Ereignis bearbeiten]** und definieren Sie Details für das Ereignis.

### Hinzufügen eines Personenereignisses

1. Navigieren Sie zum Journey-Editor.

1. Klicken Sie auf das Pluszeichen ( **+** ) auf einem Pfad und wählen Sie **[!UICONTROL Nach einem Ereignis suchen]**.

1. Wählen Sie in den Knoteneigenschaften auf der rechten Seite **[!UICONTROL Personen]** für den Ereignistyp aus.

   ![Journey-Knoten - Ereignisse auf Personen überwachen](./assets/node-listen-events-people.png){width="700" zoomable="yes"}

1. Wählen Sie ein Ereignis aus der Liste aus.

1. Klicken Sie auf **[!UICONTROL Ereignis bearbeiten]** und definieren Sie Details für das Ereignis.

### Timeout zu einem Ereignisknoten hinzufügen

Definieren Sie bei Bedarf die Zeitdauer, die die Journey auf das Ereignis wartet. Die Journey endet nach Zeitüberschreitung.

1. Aktivieren Sie den Timeout-Umschalter.

1. Wählen Sie die Dauer aus, für die die Journey auf das Eintreten eines Ereignisses wartet, bevor eine Zeitüberschreitung eintritt.

   Sie können den Pfad hier beenden oder einen anderen Handlungsweg wählen, indem Sie einen anderen Pfad festlegen.

1. Um einen neuen Pfad auf der Journey zu erstellen, in dem Sie Aktionen und Ereignisse hinzufügen können, die auf Konten angewendet werden, wenn das Ereignis nicht eintritt, aktivieren Sie das Kontrollkästchen **[!UICONTROL Pfad für Zeitüberschreitung festlegen]** .

   ![Journey-Ereignisknoten - set timeout path](./assets/node-event-timeout-set-path.png){width="700" zoomable="yes"}

## Geteilte Pfade

Aufspaltung der Audience anhand von Filterbedingungen.

>[!NOTE]
>
>Es werden maximal 25 Pfade unterstützt.

**Pfade nach Konten aufteilen**: Pfade, die nach Konten aufgeteilt sind, können sowohl Konto- als auch Personenaktionen und -ereignisse umfassen. Diese Pfade können weiter aufgeteilt werden.

_Wie funktioniert ein Aufspaltungspfad nach Kontoknoten?_

* Wenn Sie einen geteilten Pfad-Knoten hinzufügen und _Konto_ auswählen, enthält jeder hinzugefügte Pfad einen Endknoten, der jedem Edge Knoten hinzufügen kann.
* Es ist möglich, den Pfad wiederholt durch Konten aufzuteilen, z. B. auf verschachtelte Weise. Ein Aufspaltungspfad enthält eine Option, um den Standardpfad nicht hinzuzufügen.
* Konten/Personen, die sich nicht für einen der Aufspaltungspfade qualifizieren, werden im Journey nicht weitergeführt.
* Diese Pfade können mithilfe eines Zusammenführungsknotens kombiniert werden.

![Journey-Knoten - Pfade nach Konto aufteilen](./assets/node-split-paths-account.png){width="700" zoomable="yes"}

**Pfade nach Personen aufteilen**: Pfade, die durch Personen aufgeteilt sind und nur Aktionen für Personen umfassen können. Diese Pfade können nicht mehr aufgeteilt werden. Pfade schließen sich automatisch wieder an.

_Wie funktioniert ein Aufspaltungspfad nach Personen-Knoten?_

* Geteilter Pfad nach Personenknoten sind gruppierte Knoten. Sie werden automatisch zusammengeführt, sodass alle Personen in der Zielgruppe zum nächsten Schritt übergehen können, ohne den Kontext der Konten zu verlieren, zu denen sie gehören.
* Aufspaltungspfad für Personen kann nicht verschachtelt werden. Sie können keinen Aufspaltungspfad für Personen hinzufügen, die sich in diesem gruppierten Knoten befinden.
* Aufspaltungspfad enthält eine Option, um keinen Standardpfad hinzuzufügen. Konten/Personen, die sich nicht qualifizieren, kommen nicht in der Journey voran.

![Journey-Knoten - geteilte Pfade nach Personen](./assets/node-split-paths-people.png){width="700" zoomable="yes"}

| Knotenkontext | Pfadbedingungen | Beschreibung |
| ------------ | -------- | ----------- |
| [Personen](#add-a-split-path-by-people-node) | Personenattribute | |
| | Datenwert geändert (z. B. nach Aktivitätsverlauf filtern) | |
| | Geöffnete E-Mail | |
| | Link in E-Mail angeklickt | |
| | Link auf Web-Seite angeklickt | |
| | Hatte einen interessanten Moment | |
| | Mitglied der Einkaufsgruppe | |
| [Konten](#add-a-split-path-by-account-node) | Änderung des Kontodatenwerts (z. B. Filterung des Aktivitätsverlaufs) | |

### Aufspaltungspfad nach Konto-Knoten hinzufügen

1. Navigieren Sie zum Journey-Editor.

1. Klicken Sie auf das Pluszeichen ( **+** ) auf einem Pfad und wählen Sie **[!UICONTROL Geteilte Pfade]** aus.

   ![Journey-Knoten hinzufügen - geteilte Pfade](./assets/add-node-split.png){width="300"}

1. Wählen Sie in den Knoteneigenschaften auf der rechten Seite **[!UICONTROL Konten]** für die Aufteilung aus.

1. Um eine Bedingung für _[!UICONTROL Pfad 1]_ zu definieren, klicken Sie auf **[!UICONTROL Bedingung anwenden]**.

   ![Aufspaltungspfadknoten - Bedingung hinzufügen](./assets/node-split-properties-apply-condition.png){width="500"}

1. Fügen Sie im Bedingungseditor einen oder mehrere Filter hinzu, um den Aufspaltungspfad zu definieren.

   * Ziehen Sie Filterattribute per Drag-and-Drop aus der linken Navigation und füllen Sie die Übereinstimmungsdefinition aus.

   * Passen Sie Ihre Bedingungen an, indem Sie oben die **[!UICONTROL Filterlogik]** anwenden. Sie können alle Attributbedingungen oder eine beliebige Bedingung erfüllen.

     ![Aufspaltungspfadknoten - Bedingungsfilterlogik](./assets/node-split-conditions.png){width="700" zoomable="yes"}

   * Klicken Sie auf **[!UICONTROL Fertig]**.

1. Um weitere Pfade hinzuzufügen, klicken Sie auf **[!UICONTROL Pfad hinzufügen]** und wiederholen Sie die vorherigen Schritte, um Bedingungen hinzuzufügen, die für diesen Pfad gelten.

   Sie können auch jeden Pfad anhand dieser Bedingungen beschriften oder die Standardbeschriftungen verwenden.

1. (Optional) Fügen Sie einen Standardpfad für Konten hinzu, die für die anderen Pfade nicht qualifiziert sind. Ist dies nicht der Fall, endet die Journey für diese Konten.

   ![ Aufspaltungspfad - Knoteneigenschaften - andere Konten](./assets/node-split-properties-other-accounts.png){width="700" zoomable="yes"}

### Hinzufügen eines Aufspaltungspfads nach dem Knoten Personen

1. Navigieren Sie zum Journey-Editor.

1. Klicken Sie auf das Pluszeichen ( **+** ) auf einem Pfad und wählen Sie **[!UICONTROL Geteilte Pfade]** aus.

   ![Journey-Knoten hinzufügen - geteilte Pfade](./assets/add-node-split.png){width="300"}

1. Wählen Sie in den Knoteneigenschaften auf der rechten Seite **[!UICONTROL Personen]** für die Aufteilung aus.

1. Um eine Bedingung für _[!UICONTROL Pfad 1]_ zu definieren, klicken Sie auf **[!UICONTROL Bedingung anwenden]**.

1. Fügen Sie im Bedingungseditor einen oder mehrere Filter hinzu, um den Aufspaltungspfad zu definieren.

   * Ziehen Sie Filterattribute per Drag-and-Drop aus der linken Navigation und füllen Sie die Übereinstimmungsdefinition aus.

   * Passen Sie Ihre Bedingungen an, indem Sie oben die **[!UICONTROL Filterlogik]** anwenden. Sie können alle Attributbedingungen oder eine beliebige Bedingung erfüllen.

   * Klicken Sie auf **[!UICONTROL Fertig]**.

1. Um weitere Pfade hinzuzufügen, klicken Sie auf **[!UICONTROL Pfad hinzufügen]** und wiederholen Sie die vorherigen Schritte, um Bedingungen hinzuzufügen, die für diesen Pfad gelten.

   Sie können auch jeden Pfad anhand dieser Bedingungen beschriften oder die Standardbeschriftungen verwenden.

1. Schließlich können Sie einen Standardpfad für Personen hinzufügen, die für die oben genannten Pfade nicht qualifiziert sind. Wenn nicht, endet die Journey für diese Personen

Wenn Sie Bedingungen für jeden Pfad definiert haben, den Sie Ihre Zielgruppe auf der Personenebene aufteilen, können Sie Aktionen hinzufügen, die Sie für Personen durchführen möchten.

>[!NOTE]
>
>Wenn Sie die Zielgruppe nach Personen aufteilen, können Sie nur Aktionen für Personen hinzufügen.

## Warten

Warten Sie eine bestimmte Dauer, bevor Sie mit dem nächsten Schritt fortfahren.

1. Navigieren Sie zum Journey-Editor.

1. Klicken Sie auf das Pluszeichen ( **+** ) auf einem Pfad und wählen Sie **[!UICONTROL Warten]** aus.

1. Legen Sie in den Knoteneigenschaften auf der rechten Seite die **[!UICONTROL Dauer]** der Zeit fest, die gewartet werden soll, bevor der Journey zum nächsten Knoten im Pfad wechselt.

![Journey-Knoten - wait](./assets/node-wait.png){width="700" zoomable="yes"}

## Zusammenführungspfade

Verschiedene Pfade in Ihrer Journey können mithilfe dieses Knotens zusammengeführt und entsperrt werden.

1. Navigieren Sie zum Journey-Editor.

1. Klicken Sie auf das Pluszeichen ( **+** ) auf einem Pfad und wählen Sie **[!UICONTROL Geteilte Pfade]** aus.

1. Klicken Sie auf den Knoten split , um seine Eigenschaften auf der rechten Seite zu öffnen.

1. Klicken Sie auf [!UICONTROL Pfad hinzufügen] , um drei Pfade zu erstellen.

1. Fügen Sie jedem Pfad eine Kombination aus Aktionen und Ereignissen hinzu.

1. Klicken Sie auf das Pluszeichen ( **+** ) für einen dieser Pfade und wählen Sie aus den angezeigten Optionen die Option **[!UICONTROL Zusammenführen]** aus.

   ![Journey-Knoten - Zusammenführungspfade](./assets/node-plus-icon-merge-paths.png){width="400"}

1. Wählen Sie in den Eigenschaften des Zusammenführungsknotens die Pfade aus, die Sie zusammenführen möchten.

   ![Journey-Knoten - Zusammenführungspfade](./assets/node-merge-select-paths.png){width="600" zoomable="yes"}

   Sie sollten jetzt sehen, dass die Pfade zusammengeführt werden, sodass Konten aus den ausgewählten Pfaden zu einem einzigen Pfad kombiniert werden und weiterhin über die Journey weitergehen können.

1. Bei Bedarf können Sie die Zusammenführung von Pfaden aufheben, indem Sie zurück zu den Eigenschaften des Zusammenführungsknotens navigieren und das Kontrollkästchen für alle Pfade deaktivieren, die Sie entfernen möchten.
