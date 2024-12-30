---
title: Account Journey Nodes
description: Erfahren Sie mehr über die Knotentypen, mit denen Sie Ihre Account-Journey in Journey Optimizer B2B edition erstellen können.
feature: Account Journeys
exl-id: 4edb87d9-cdf8-47a4-968b-6dc76d97b89c
source-git-commit: af72f5183cb1de56804340cbc9148de82faeca35
workflow-type: tm+mt
source-wordcount: '2443'
ht-degree: 9%

---

# Konto-Journey-Knoten

Nachdem Sie [Konto-Journey erstellen](journey-overview.md#create-an-account-journey) und [Zielgruppe hinzufügen](journey-overview.md#add-the-account-audience-for-your-journey) erstellen Sie die Journey mithilfe von -Knoten. Die Journey-Map bietet eine Arbeitsfläche, auf der Sie Ihre mehrstufigen B2B-Marketing-Anwendungsfälle erstellen können.

Erstellen Sie Ihre Konto-Journey, indem Sie die verschiedenen Aktions-, Ereignis- und Orchestrierungsknoten als mehrstufiges kanalübergreifendes Szenario kombinieren. Jeder Knoten einer Journey stellt einen Schritt entlang eines logischen Pfads dar. Verwenden Sie die folgenden Knotentypen, um eine Konto-Journey zu erstellen:

* [Konto-Zielgruppe](#account-audience-node)
* [Aktion ausführen](#take-an-action)
* [Überwachen eines Ereignisses](#listen-for-an-event)
* [Pfade aufteilen](#split-paths)
* [Warten](#wait)
* [Zusammenführen von Pfaden](#merge-paths)

## Konto-Zielgruppen-Knoten

Der [Account-Zielgruppe](journey-overview.md#add-the-account-audience-for-your-journey) definiert die Eingabekonto-Zielgruppe (in Adobe Experience Platform erstellt und verwaltet) für den Journey. Dieser Knoten ist immer der erste Knoten und wird standardmäßig automatisch erstellt.

## Aktion ausführen

Ausführen einer Aktion wie Senden einer E-Mail, Ändern einer Bewertung, Zuweisen zu einer Einkaufsgruppe usw.

**Aktion für Konten**: Die Aktion wird auf alle Personen angewendet, die Teil von Konten auf diesem Pfad sind.

**Aktion für Personen**: Die Aktion wird auf alle Personen auf diesem Pfad angewendet. Eine Aktion für Personen kann im Aufspaltungspfad nach Personen oder im Aufspaltungspfad nach Konten verwendet werden.

### Aktionen und Einschränkungen {#action-nodes}

| Knotenkontext | Aktion | Begrenzungen |
| ------------ | ------ | ----------- |
| [„Personen“](#add-a-people-action) | Zu Liste hinzufügen | Marketo Engage Workspace/<br/> auswählen |
| | Zur Marketo Engage-Anfragekampagne hinzufügen | Marketo Engage-Arbeitsbereich auswählen<br/>Kampagne anfordern auswählen |
| | Zu Einkaufsgruppe zuweisen | Lösungsinteresse auswählen<br/>Rolle auswählen |
| | Personenpartition in Marketo Engage ändern | Neue Partition |
| | Bewertung ändern | Score-Name<br/>Änderung |
| | Interessanter Moment der Person | type<br/>description |
| | Aus Einkaufsgruppe entfernen | Interesse an der Lösung auswählen |
| | Aus Liste entfernen | Marketo Engage Workspace/<br/> auswählen |
| | E-Mail senden | Neue E-Mail erstellen<br/>E-Mail von Marketo Engage auswählen |
| | SMS senden | SMS erstellen |
| [Konten](#add-an-account-action) | Datenwert der Kontoänderung | Attribut/<br/> Wert auswählen |
| | Interessanter Moment des Kontos | Typ (E-Mail, Meilenstein oder Web)<br/>Beschreibung (optional) |
| | Konto zu (anderer) Journey hinzufügen | Live-Konto-Journey auswählen |
| | Konto von Journey entfernen | Live-Konto-Journey auswählen |
| | Verkaufswarnung senden | Lösungsinteresse auswählen<br/> E-Mail senden an |
| | Einkaufsgruppenstufe aktualisieren | Lösungsinteresse auswählen<br/>Einkaufsgruppenstufe auswählen |
| | Status der Einkaufsgruppe aktualisieren | Lösungsinteresse/<br/> auswählen (erforderlich, max. 50 Zeichen) |

### Hinzufügen einer Kontoaktion

1. Navigieren Sie zum Journey-Editor.

1. Klicken Sie auf das Pluszeichen ( **+** ) auf einem Pfad und wählen Sie **[!UICONTROL Aktion ausführen]**.

   ![Journey-Knoten hinzufügen - eine Aktion ausführen](./assets/add-node-action.png){width="400"}

1. Wählen Sie in den Knoteneigenschaften auf der rechten Seite **[!UICONTROL Konten]** für die Aktion aus.

1. Wählen Sie eine Aktion aus der Liste aus und legen Sie beliebige Werte für die Aktion fest.

   ![Journey-Knoten - Aktion für ein Konto durchführen](./assets/node-take-action-account.png){width="700" zoomable="yes"}

### Hinzufügen einer Personen-Aktion

1. Navigieren Sie zum Journey-Editor.

1. Klicken Sie auf das Pluszeichen ( **+** ) auf einem Pfad und wählen Sie **[!UICONTROL Aktion ausführen]**.

1. Wählen Sie in den Knoteneigenschaften auf der rechten Seite **[!UICONTROL Personen]** für die Aktion aus.

1. Wählen Sie eine Aktion aus der Liste aus und legen Sie beliebige Werte für die Aktion fest.

![Journey-Knoten - Eine Aktion auf Personen durchführen](./assets/node-take-action-people.png){width="700" zoomable="yes"}

## Überwachen eines Ereignisses

Wechseln Sie im Journey zum nächsten Schritt, wenn ein Ereignis auftritt.

* Sie können auch festlegen, wie lange die Journey auf dieses Ereignis warten soll. Die Journey endet nach einer Zeitüberschreitung.
* Darüber hinaus können Sie weitere Knoten zu Ihrem Zeitüberschreitungspfad hinzufügen.

**Ereignisse auf Konten überwachen**: Wenn mindestens eine Person aus einem Konto ein Ereignis Trigger, wird das Konto zum nächsten Schritt auf der Journey weitergeleitet.

**Ereignisse auf Personen überwachen**: Ereignisse auf Personen können nur auf einen Kontopfad angewendet werden. Er ist nicht für eine Aufspaltung nach Personenknoten verfügbar.

### Ereignisse und Einschränkungen {#event-nodes}

| Knotenkontext | Veranstaltung | Begrenzungen |
| ------------ | ----- | ----------- |
| [„Personen“](#add-a-people-event) | Der Einkaufsgruppe zugewiesen | Lösungsinteresse<br/>Zusätzliche Einschränkungen (optional): <li>Role</li><li>Datum der Aktivität</li><br/>Zeitüberschreitung (optional) |
| | Klickt auf Link in E-Mail | E<br/>Mail: Zusätzliche Einschränkungen (optional): <li>Link</li><li>Link-ID</li><li>Ist ein mobiles Gerät</li><li>Gerät</li><li>Plattform</li><li>Browser</li><li>Ist prädiktiv Inhalt</li><li>Ist Bot-Aktivität</li><li>Bot-Aktivitätsmuster</li><li>Browser</li><li>Datum der Aktivität</li><li>Min. Häufigkeit</li><br/>Zeitüberschreitung (optional) |
| | Klickt auf Link in SMS | E<br/>Mail: Zusätzliche Einschränkungen (optional): <li>Link</li><li>Gerät</li><li>Plattform</li><li>Datum der Aktivität</li><li>Min. Häufigkeit</li><br/>Zeitüberschreitung (optional) |
| | Datenwertänderungen | Personenattribut<br/>Zusätzliche Einschränkungen (optional): <li>Neuer Wert</li><li>Vorheriger Wert</li><li>Grund</li><li>Quelle</li><li>Datum der Aktivität</li><li>Min. Häufigkeit</li><br/>Zeitüberschreitung (optional) |
| | Öffnet E-Mail | E<br/>Mail: Zusätzliche Einschränkungen (optional): <li>Link</li><li>Link-ID</li><li>Ist ein mobiles Gerät</li><li>Gerät</li><li>Plattform</li><li>Browser</li><li>Ist prädiktiv Inhalt</li><li>Ist Bot-Aktivität</li><li>Bot-Aktivitätsmuster</li><li>Browser</li><li>Datum der Aktivität</li><li>Min. Häufigkeit</li><br/>Zeitüberschreitung (optional) |
| | Aus Einkaufsgruppe entfernt | Lösungsinteresse<br/>Datum der Aktivität (optional)<br/>Zeitüberschreitung (optional) |
| | Bewertung wird geändert | Score-<br/>: Zusätzliche Einschränkungen (optional):<li>Ändern</li><li>Neue Bewertung</li><li>Dringlichkeit</li><li>Priorität</li><li>Relative Bewertung</li><li>Relative Dringlichkeit</li><li>Datum der Aktivität</li><li>Min. Häufigkeit</li><br/>Zeitüberschreitung (optional) |
| | SMS-Bounces | SMS-<br/>: Zusätzliche Einschränkungen (optional): <li>Datum der Aktivität</li><li>Min. Anzahl</li><br/>Zeitüberschreitung (optional) |
| [Konten](#add-an-account-event) | Account hatte interessanten Moment | Typ (E-Mail, Meilenstein oder Web)<br/>Zusätzliche Einschränkungen (optional): <li>Beschreibung</li><li>Quelle</li><li>Datum der Aktivität</li> <br/>Zeitüberschreitung (optional) |
| | Änderung des Kontodatenwerts | Attribut<br/>Zusätzliche Einschränkungen (optional): <li>Neuer Wert</li><li>Vorheriger Wert</li><li>Datum der Aktivität</li> <br/>Zeitüberschreitung (optional) |
| | Änderung in der Einkaufsgruppenphase | Lösungsinteresse<br/>Zusätzliche Einschränkungen (optional): <li>Neue Phase</li><li>Vorheriges Stadium</li><li>Datum der Aktivität</li><br/>-Timeout (optional) |
| | Änderung des Status der Einkaufsgruppe | Lösungsinteresse<br/>Zusätzliche Einschränkungen (optional): <li>Neuer Status</li><li>Vorheriger Status</li><li>Datum der Aktivität</li><br/>-Timeout (optional) |
| | Änderung der Vollständigkeitsbewertung | Lösungsinteresse<br/>Zusätzliche Einschränkungen (optional): <li>Neue Bewertung</li><li>Vorherige Bewertung</li><li>Datum der Aktivität</li><br/>-Timeout (optional) |
| | Änderung des Interaktionswerts | Lösungsinteresse<br/>Zusätzliche Einschränkungen (optional): <li>Neue Bewertung</li><li>Vorherige Bewertung</li><li>Datum der Aktivität</li><br/>-Timeout (optional) |

### Hinzufügen eines Kontoereignisses

1. Navigieren Sie zum Journey-Editor.

1. Klicken Sie auf das Pluszeichen ( **+** ) in einem Pfad und wählen Sie **[!UICONTROL Auf ein Ereignis überwachen]**.

1. Wählen Sie in den Knoteneigenschaften auf der rechten Seite **[!UICONTROL Ereignistyp]** Konten“ aus.

   ![Journey-Knoten - Überwachen von Ereignissen auf Konto](./assets/node-listen-events-account.png){width="700" zoomable="yes"}

1. Wählen Sie ein Ereignis aus der Liste aus.

1. Klicken Sie **[!UICONTROL Ereignis bearbeiten]** und definieren Sie Details für das Ereignis.

### Personen-Ereignis hinzufügen

1. Navigieren Sie zum Journey-Editor.

1. Klicken Sie auf das Pluszeichen ( **+** ) in einem Pfad und wählen Sie **[!UICONTROL Auf ein Ereignis überwachen]**.

1. Wählen Sie in den Knoteneigenschaften auf der rechten Seite **[!UICONTROL Ereignistyp]** Personen“ aus.

   ![Journey-Knoten - Überwachen von Ereignissen auf Personen](./assets/node-listen-events-people.png){width="700" zoomable="yes"}

1. Wählen Sie ein Ereignis aus der Liste aus.

1. Klicken Sie **[!UICONTROL Ereignis bearbeiten]** und definieren Sie Details für das Ereignis.

### Hinzufügen einer maximalen Wartezeit zu einem Ereignisknoten

Legen Sie bei Bedarf fest, wie lange die Journey auf das Ereignis warten soll. Die Journey endet nach einer Zeitüberschreitung.

1. Aktivieren Sie den Umschalter Zeitüberschreitung .

1. Wählen Sie die Dauer aus, für die der Journey auf ein Ereignis wartet, bevor eine Zeitüberschreitung eintritt.

   Sie können den Pfad hier beenden oder eine andere Vorgehensweise wählen, indem Sie einen anderen Pfad festlegen.

1. Um einen neuen Pfad auf der Journey zu erstellen, in dem Sie Aktionen und Ereignisse hinzufügen können, die für Konten gelten, wenn das Ereignis nicht eintritt, aktivieren Sie das Kontrollkästchen **[!UICONTROL Zeitüberschreitungspfad festlegen]**.

   ![Journey-Ereignisknoten - Zeitüberschreitungspfad festlegen](./assets/node-event-timeout-set-path.png){width="700" zoomable="yes"}

## Pfade teilen

Teilen Sie Ihre Zielgruppe basierend auf Filterbedingungen auf.

>[!NOTE]
>
>Es werden maximal 25 Pfade unterstützt.

**Pfade nach Konten aufteilen**: Pfade, die nach Konten aufgeteilt sind, können sowohl Konto- als auch Personenaktionen und -ereignisse enthalten. Diese Pfade können weiter aufgeteilt werden.

_Wie funktioniert ein aufgeteilter Pfad nach Kontenknoten?_

* Wenn Sie einen aufgeteilten Pfadknoten hinzufügen und &quot;_&quot;_, enthält jeder hinzugefügte Pfad einen Endknoten mit der Möglichkeit, Knoten zu jeder Edge hinzuzufügen.
* Es ist möglich, den Pfad wiederholt nach Konten aufzuteilen, z. B. auf verschachtelte Weise. Ein aufgeteilter Pfad enthält eine Option zum Nicht-Hinzufügen des Standardpfads.
* Wenn ein Konto/eine Person nicht für einen der Aufspaltungspfade qualifiziert ist, wird sie auf der Journey nicht weitergeleitet.
* Diese Pfade können mithilfe eines Zusammenführungsknotens kombiniert werden.

![Journey-Knoten - Pfade nach Konto aufteilen](./assets/node-split-paths-account.png){width="700" zoomable="yes"}

**Pfade nach Personen aufteilen**: Pfade werden nach Personen aufgeteilt und können nur Personenaktionen enthalten. Diese Pfade können nicht erneut aufgeteilt und automatisch wieder verbunden werden.

_Wie funktioniert ein aufgeteilter Pfad nach Personenknoten?_

* Bei einem aufgeteilten Pfad nach Personen-Knoten handelt es sich um gruppierte Knoten. Die Pfade werden automatisch zusammengeführt, sodass alle Personen in der Zielgruppe mit dem nächsten Schritt fortfahren können, ohne ihren Kontokontext zu verlieren.
* Aufspaltungspfad für Personen kann nicht verschachtelt werden. Sie können keinen Aufspaltungspfad für Personen auf einem Pfad hinzufügen, der sich in diesem gruppierten Knoten befindet.
* Der Split-Pfad enthält eine Option zum Auslassen eines Standardpfads. Konten/Personen ohne Übereinstimmung für einen definierten Pfad werden auf der Journey nicht weitergeleitet.
* Der Split-Pfad nach Personen unterstützt die Verwendung von _Konto-Personen-Beziehungen_ mit denen Sie Personen nach ihrer Rolle filtern können (z. B. Auftragnehmer oder Vollzeit-Mitarbeiter), wie in den Rollenvorlagen definiert.

![Journey-Knoten - Pfade nach Personen aufteilen](./assets/node-split-paths-people.png){width="700" zoomable="yes"}

### Pfadbedingungen {#path-conditions}

| Knotenkontext | Pfadbedingungen | Beschreibung |
| ------------ | --------------- | ----------- |
| [Konten](#add-a-split-path-by-account-node) | Kontoattribute | Attribute aus dem Kontoprofil, einschließlich: <li>Jahresumsatz</li><li>Stadt</li><li>Land</li><li>Mitarbeiterzahl</li><li>Branche</li><li>Name</li><li>SIC-Code</li><li>Land</li> |
| | [!UICONTROL Sonderfilter] > [!UICONTROL Hat Einkaufsgruppe] | Das Konto hat Mitglieder von Einkaufsgruppen, die anhand eines oder mehrerer der folgenden Kriterien bewertet wurden oder nicht: <li>Interesse an der Lösung</li><li>Einkaufsgruppenstatus</li><li>Vollständigkeitsindex</li><li>Engagement-Bewertung</li> |
| [Personen](#add-a-split-path-by-people-node) > [!UICONTROL Nur Personenattribute] | [!UICONTROL Personenattribute] | Attribute aus dem Personenprofil, einschließlich: <li>Stadt</li><li>Land</li><li>Geburtsdatum</li><li>E-Mail-Adresse</li><li>E-Mail-Adresse ungültig</li><li>E-Mail angehalten</li><li>Vorname</li><li>Abgeleitetes Bundesland/abgeleitete Region</li><li>Stellenbezeichnung</li><li>Last name</li><li>Mobiltelefonnummer</li><li>Telefonnummer</li><li>Postleitzahl</li><li>Land</li><li>Abbestellt</li><li>Grund für Abmeldung</li> |
| | [!UICONTROL Aktivitätsverlauf] > [!UICONTROL E-Mail] | Mit der Journey verbundene E-Mail-Aktivitäten: <li>[!UICONTROL Link in E-Mail angeklickt]</li><li>Geöffnete E-Mail</li><li>Bekam E-Mail zugestellt</li><li>Bekam E-Mail zugesendet</li> Diese Bedingungen werden mithilfe einer ausgewählten E-Mail-Nachricht aus einem früheren Abschnitt der Journey ausgewertet. |
| | [!UICONTROL Aktivitätsverlauf] > [!UICONTROL Datenwert geändert] | Für ein ausgewähltes Personenattribut wurde ein Wert geändert. Zu diesen Änderungstypen gehören: <li>Neuer Wert</li><li>Vorheriger Wert</li><li>Grund</li><li>Quelle</li><li>Datum der Aktivität</li><li>Min. Häufigkeit</li> |
| | [!UICONTROL Aktivitätsverlauf] > [!UICONTROL Hatte einen interessanten Moment] | Interessante Momentaktivität, die in der zugehörigen Marketo Engage-Instanz definiert ist. Zu den Einschränkungen gehören: <li>Meilenstein</li><li>E-Mail</li><li>Web</li> |
| | [!UICONTROL Sonderfilter] > [!UICONTROL Mitglied der Einkaufsgruppe] | Die Person ist oder ist kein Kauf-Gruppenmitglied, das anhand eines oder mehrerer der folgenden Kriterien bewertet wird: <li>Interesse an der Lösung</li><li>Einkaufsgruppenstatus</li><li>Vollständigkeitsindex</li><li>Engagement-Bewertung</li><li>Role</li> |
| [Personen](#add-a-split-path-by-people-node) > [!UICONTROL Nur Konto-Personen-Attribute] | Funktion in Kontoattributen | Der Person wird eine Rolle im Konto zugewiesen oder ihr wird keine Rolle zugewiesen. Optionale Einschränkungen: <li>Rollennamen eingeben</li> |

### Fügen Sie einen aufgeteilten Pfad nach Kontenknoten hinzu

1. Navigieren Sie zum Journey-Editor.

1. Klicken Sie auf das Pluszeichen ( **+** ) auf einem Pfad und wählen Sie **[!UICONTROL Pfade aufteilen]**.

   ![Journey-Knoten hinzufügen - Aufspaltungspfade](./assets/add-node-split.png){width="300"}

1. Wählen Sie in den Knoteneigenschaften auf der rechten Seite **[!UICONTROL Konten]** für die Aufspaltung aus.

1. Um eine Bedingung zu definieren, die für _[!UICONTROL Pfad 1]_ gilt, klicken Sie auf **[!UICONTROL Bedingung anwenden]**.

   ![Pfadknoten aufteilen - Bedingung hinzufügen](./assets/node-split-properties-apply-condition.png){width="500"}

1. Fügen Sie im Bedingungseditor einen oder mehrere Filter hinzu, um den Aufspaltungspfad zu definieren.

   * Ziehen Sie Filterattribute per Drag-and-Drop aus dem linken Navigationsbereich und füllen Sie die Übereinstimmungsdefinition aus.

   * Passen Sie Ihre Bedingungen durch Anwendung der **[!UICONTROL Filterlogik]** oben an. Sie wählen, ob alle Attributbedingungen oder eine beliebige Bedingung erfüllt werden sollen.

     ![Pfadknoten aufteilen - Filterlogik für Bedingungskonten](./assets/node-split-conditions-accounts.png){width="700" zoomable="yes"}

   * Klicken Sie auf **[!UICONTROL Fertig]**.

1. Um weitere Pfade hinzuzufügen, klicken Sie auf **[!UICONTROL Pfad hinzufügen]** und wiederholen Sie die vorherigen Schritte, um die für diesen Pfad geltenden Bedingungen hinzuzufügen.

   Sie können auch jeden Pfad anhand dieser Bedingungen beschriften oder die Standardbeschriftungen verwenden.

1. Ordnen Sie die Pfade bei Bedarf entsprechend der Priorität neu an, die Sie für die Aufspaltung festlegen möchten.

   Die Pfadfilterung wird in der Reihenfolge von oben nach unten bewertet. Jedes Konto fährt auf dem ersten Pfad fort, der übereinstimmt.

   Klicken Sie auf die Pfeile nach oben und unten oben rechts auf jeder Pfadkarte, um sie in der Liste der Pfade nach oben oder unten zu verschieben.

   ![Pfadknoten aufteilen - Pfade neu anordnen](./assets/node-split-reorder-paths-accounts.png){width="500" zoomable="yes"}

1. Aktivieren Sie die Option **[!UICONTROL Andere Konten]**, um einen Standardpfad für Konten hinzuzufügen, die nicht mit den definierten Pfaden übereinstimmen. Wenn nicht, endet die Journey für diese Menschen.

### Fügen Sie einen Pfad für die Aufspaltung nach Personenknoten hinzu

1. Navigieren Sie zum Journey-Editor.

1. Klicken Sie auf das Pluszeichen ( **+** ) auf einem Pfad und wählen Sie **[!UICONTROL Pfade aufteilen]**.

   ![Journey-Knoten hinzufügen - Aufspaltungspfade](./assets/add-node-split.png){width="300"}

1. Wählen Sie in den Knoteneigenschaften auf der rechten Seite **[!UICONTROL Personen]** für die Teilung aus.

1. Legen Sie die **[!UICONTROL Attribute für Bedingungen“]**.

   * Wählen Sie **[!UICONTROL Nur Personenattribute]** aus, um Bedingungen im Zusammenhang mit dem Personenprofil und den Ereignissen zu verwenden.
   * Wählen Sie **[!UICONTROL Nur Konto-Personen-Attribute]** aus, um Bedingungen im Zusammenhang mit der Rollenmitgliedschaft der Person in einem Konto zu verwenden.

1. Um eine Bedingung zu definieren, die für _[!UICONTROL Pfad 1]_ gilt, klicken Sie auf **[!UICONTROL Bedingung anwenden]**.

1. Fügen Sie im Bedingungseditor einen oder mehrere Filter hinzu, um den Aufspaltungspfad zu definieren.

   * Ziehen Sie eines der Personenattribute per Drag-and-Drop aus dem linken Navigationsbereich und füllen Sie die Definition der Übereinstimmung aus.

     >[!NOTE]
     >
     >Wenn Sie benutzerdefinierte Personenfelder im Konto-Zielgruppenschema auf Experience Platform definiert haben, sind diese Felder auch verfügbar, um als Personenattribute in Bedingungen zu verwenden.

   * Passen Sie Ihre Bedingungen durch Anwendung der **[!UICONTROL Filterlogik]** oben an. Sie wählen, ob alle Attributbedingungen oder eine beliebige Bedingung erfüllt werden sollen.

     ![Pfadknoten aufteilen - Bedingungen für Personenfilterlogik](./assets/node-split-conditions-people.png){width="700" zoomable="yes"}

   * Klicken Sie auf **[!UICONTROL Fertig]**.

1. Um weitere Pfade hinzuzufügen, klicken Sie auf **[!UICONTROL Pfad hinzufügen]** und wiederholen Sie die vorherigen Schritte, um die für diesen Pfad geltenden Bedingungen hinzuzufügen.

   Sie können auch jeden Pfad anhand dieser Bedingungen beschriften oder die Standardbeschriftungen verwenden.

1. Ordnen Sie die Pfade bei Bedarf entsprechend der Priorität neu an, die Sie für die Aufspaltung festlegen möchten.

   Die Pfadfilterung wird in der Reihenfolge von oben nach unten bewertet. Jede Person fährt auf dem ersten Pfad fort, der übereinstimmt.

   Klicken Sie auf die Pfeile nach oben und unten oben rechts auf jeder Pfadkarte, um sie in der Liste der Pfade nach oben oder unten zu verschieben.

   ![Pfadknoten aufteilen - Pfade neu anordnen](./assets/node-split-reorder-paths-people.png){width="500" zoomable="yes"}

1. Aktivieren Sie die Option **[!UICONTROL Andere Personen]**, um einen Standardpfad für Personen hinzuzufügen, die den definierten Pfaden nicht entsprechen. Wenn nicht, endet die Journey für diese Menschen.

Wenn Sie für jeden Pfad zur Aufteilung Ihrer Zielgruppe auf Personenebene Bedingungen definiert haben, können Sie Aktionen hinzufügen, die Sie für Personen durchführen möchten.

>[!NOTE]
>
>Wenn Sie die Zielgruppe nach Personen aufteilen, können Sie nur Personenaktionen hinzufügen, bis die Pfade geschlossen oder zusammengeführt werden.

## Warten

Warten Sie eine bestimmte Zeit, bevor Sie mit dem nächsten Schritt fortfahren.

1. Navigieren Sie zum Journey-Editor.

1. Klicken Sie auf das Pluszeichen ( **+** ) in einem Pfad und wählen Sie **[!UICONTROL Warten]** aus.

1. Legen Sie in den Knoteneigenschaften auf der rechten Seite die **[!UICONTROL Dauer]** fest, die gewartet werden soll, bevor die Journey zum nächsten Knoten im Pfad fortgesetzt wird.

![Journey-Knoten - Warten](./assets/node-wait.png){width="700" zoomable="yes"}

## Zusammenführen von Pfaden

Verschiedene Pfade in Ihrem Journey können mit diesem Knoten zusammengeführt und entfernt werden.

1. Navigieren Sie zum Journey-Editor.

1. Klicken Sie auf das Pluszeichen ( **+** ) auf einem Pfad und wählen Sie **[!UICONTROL Pfade aufteilen]**.

1. Klicken Sie auf den geteilten Knoten, um seine Eigenschaften auf der rechten Seite zu öffnen.

1. Klicken Sie [!UICONTROL Pfad hinzufügen], um drei Pfade zu erstellen.

1. Fügen Sie jedem Pfad eine Kombination aus Aktionen und Ereignissen hinzu.

1. Klicken Sie auf das Pluszeichen ( **+** ) für einen dieser Pfade und wählen Sie **[!UICONTROL Zusammenführen]** aus den angezeigten Optionen aus.

   ![Journey-Knoten - Zusammenführungspfade](./assets/node-plus-icon-merge-paths.png){width="400"}

1. Wählen Sie in den Knoteneigenschaften „Zusammenführungspfade“ die Pfade aus, die zusammengeführt werden sollen.

   ![Journey-Knoten - Zusammenführungspfade](./assets/node-merge-select-paths.png){width="600" zoomable="yes"}

   An dieser Stelle werden die Pfade zusammengeführt, sodass Konten aus den ausgewählten Pfaden zu einem einzigen Pfad kombiniert werden, der durch den Journey weiter ausgeführt werden kann.

1. Bei Bedarf können Sie die Zusammenführung von Pfaden aufheben, indem Sie zurück zu den Knoteneigenschaften der Zusammenführungspfade navigieren und das Kontrollkästchen für alle Pfade deaktivieren, die Sie entfernen möchten.
