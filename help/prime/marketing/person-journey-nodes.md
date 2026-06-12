---
title: Hinzufügen von Journey-Knoten
description: Platzhalterseite für Personen-Journey-Knoten.
source-git-commit: 2f19137465c71f2292d37bea5786533b1df6e286
workflow-type: tm+mt
source-wordcount: '1137'
ht-degree: 2%

---

# Journey-Knoten hinzufügen

Nachdem Sie eine Personen-Journey erstellt haben, fügen Sie die Audience hinzu und erstellen Sie die Journey mithilfe von -Knoten. Die Journey-Map bietet eine Arbeitsfläche, auf der Sie Ihre mehrstufigen B2B-Marketing-Anwendungsfälle erstellen können.

Der Knoten _[!UICONTROL Person]_ Zielgruppe ist automatisch der erste Knoten auf der Journey. Nachdem Sie die Audience ausgewählt haben, erstellen Sie Ihren Journey, indem Sie die verschiedenen Aktions-, Ereignis- und Entscheidungsknoten als mehrstufiges kanalübergreifendes Szenario kombinieren. Jeder Knoten einer Journey stellt einen Schritt entlang eines logischen Pfads dar.

## Zielgruppenknoten Person

Der Zielgruppenknoten Person gibt an, welche Personendatensätze in die Journey eingehen. Wenn Sie eine Personen-Journey erstellen, beginnt die Journey immer mit einem Personen-Zielgruppenknoten, der die Eingabe definiert.

1. Klicken Sie auf den Knoten, um ihn auszuwählen.
1. Verwenden Sie im Bedienfeld Knoteneigenschaften auf der rechten Seite eine der folgenden Eingabeoptionen für den Knoten „Zielgruppen-Journey für Personen“:

   * **[!UICONTROL Dynamische Liste]** - Verwenden Sie eine dynamische, regelbasierte Personenliste. Die Listenregeln werden zur Journey-Laufzeit ausgewertet, um Mitglieder der Journey zu qualifizieren. Personen, die sich zu einem späteren Zeitpunkt für die dynamische Liste disqualifizieren, werden nicht von der Journey entfernt.

   * **[!UICONTROL Statische Liste]** - Verwenden Sie eine statische Liste von Personen als Mitglied Ihres Journey. Die aktuelle Listenmitgliedschaft wird zur Journey-Laufzeit ausgewertet, um Mitglieder für die Journey zu qualifizieren. Personen, die später aus der statischen Liste entfernt werden, werden nicht von der Journey entfernt.

## Personen-Aktionsknoten

Verwenden Sie auf einer Personen-Journey eine Aktion für Personen, wenn Sie eine Änderung auf alle Personen im Knotenpfad anwenden möchten. Bei einer Konto-Journey kann dieser Knotentyp im Aufspaltungspfad nach Personen oder im Aufspaltungspfad nach Konten verwendet werden.

### Aktionen und Einschränkungen

| Aktion | Einschränkungen |
| ------ | ---------- |
| **[!UICONTROL E-Mail senden]** | <li>E-Mail erstellen <li>Optimierung des Versandzeitpunkts (optional) |
| **[!UICONTROL Ändern des Datenwerts]** | <li>Personenattribut auswählen <li>Neuen Wert festlegen |

### Aktionsknoten hinzufügen

1. Navigieren Sie zur Journey-Karte.

1. Klicken Sie auf das Pluszeichen ( **+** ) auf einem Pfad und wählen Sie **[!UICONTROL Aktion ausführen]**.

1. Wählen Sie in den Knoteneigenschaften auf der rechten Seite eine Aktion aus der Liste aus und legen Sie beliebige Werte für die Aktion fest.

<!-- ![Person journey node - take an action](./assets/node-take-action-people.png){width="700" zoomable="yes"} -->

+++[!UICONTROL E-Mail senden]

Verwenden Sie diese Aktion, um eine E-Mail zu senden. Nachdem Sie die E-Mail für den Knoten erstellt haben, können Sie E-Mail-Nachrichten im E-Mail-Design-Bereich entwerfen, personalisieren und in der Vorschau anzeigen (siehe [E-Mail-Authoring](../content/email-authoring.md)).

<!-- ![Take an action - Send email](./assets/node-action-send-email-from-marketo.png){width="300"} -->

Sie können die [Optimierung des Versandzeitpunkts](../marketing/email-send-time-optimization.md) verwenden, um den Zeitpunkt des E-Mail-Versands zu personalisieren, indem Sie vorhersagen, wann jedes Profil mit der größten Wahrscheinlichkeit interagieren wird.

<!--
>[!NOTE]
>
>You can use email deduplication in account journeys to ensure that the same email is not sent multiple times to the same email address within a journey. For more information, see [Email deduplication](../content/email-deduplication.md).
-->

+++

+++[!UICONTROL Ändern des Datenwerts]

Verwenden Sie diese Aktion, um den Wert eines Personenprofilattributs in der Datenbank zu ändern. Wählen Sie das Attribut aus und legen Sie dann den neuen Wert fest.

<!-- ![Take an action - Update person profile](./assets/node-action-update-person-profile.png){width="300"} -->

+++

## Ereignisknoten

Fügen Sie den Knoten _Auf ein Ereignis warten_ hinzu, um Ihre Zielgruppe beim Eintreten eines Ereignisses zum nächsten Schritt auf dem Journey zu bewegen.

### Filter für Personenereignisse

| Filter | Beschreibung |
| ------- | ----------- |
| Aktivitätsverlauf > E-Mail | E-Mail-Aktivitäten basierend auf Bedingungen, die mithilfe einer oder mehrerer ausgewählter E-Mail-Nachrichten ausgewertet werden: <li>Link in E-Mail angeklickt <li>Hat E-Mail geöffnet |
| Aktivitätsverlauf > Datenwert geändert | Für ein ausgewähltes Personenattribut wurde ein Wert geändert. Zu diesen Änderungstypen gehören: <li>Neuer Wert <li>Vorheriger Wert <li>Grund <li>Quelle <li>Datum der Aktivität <li> Min. Häufigkeit |

### Ereignisknoten hinzufügen

1. Navigieren Sie zur Journey-Karte.

1. Klicken Sie auf das Pluszeichen ( **+** ) in einem Pfad und wählen Sie **[!UICONTROL Auf ein Ereignis überwachen]**.

1. Wählen Sie in den Knoteneigenschaften auf der rechten Seite **[!UICONTROL Ereignistyp]** Personen“ aus.

   <!-- ![Journey node - listen to events on people](./assets/node-listen-events-people.png){width="700" zoomable="yes"} -->

1. Wählen Sie ein Ereignis aus der Liste aus.

1. Klicken Sie **[!UICONTROL Ereignis bearbeiten]** und definieren Sie Details für das Ereignis.

>[!NOTE]
>
>Die Zeitüberschreitungsfunktion für „Auf einen Ereignisknoten warten“ funktioniert derzeit nicht und wird in einer späteren Phase aktiviert.

## Pfade von Knoten teilen

Verwenden Sie geteilte Knoten, um Personen entsprechend den von Ihnen definierten Bedingungen zu segmentieren. Erstellen Sie Pfade für die Audience-Liste gemäß Bedingungen, definieren Sie jeden Pfad mit Aktions- und Ereignisknoten für das Segment, kombinieren Sie dann die Pfade und setzen Sie das Journey fort.

Ein Knoten für aufgeteilte Pfade definiert einen oder mehrere segmentierte Pfade, die auf Personenfiltern basieren.

<!-- A split based on a people filter is automatically closed with a merge paths node so that all people can move forward to the next step. Split by people paths can include only people actions. These paths cannot be split again and automatically join back. _not currently true_ -->


_&#x200B;**Wie funktioniert ein aufgeteilter Pfad nach Personenknoten**&#x200B;_

* Die Auswertung jedes Pfads erfolgt von oben nach unten. Wenn eine Person für den ersten und zweiten Pfad eine Übereinstimmung findet, fährt sie nur entlang des ersten Pfads fort.
* Der Knoten unterstützt die Definition eines Pfads _Andere Personen_, in dem Sie Aktionen oder Ereignisse für Personen hinzufügen können, die nicht mit einem der definierten Segmente/Pfade übereinstimmen.

### Übereinstimmende Filter

Verwenden Sie für jeden Pfad, den Sie für den Knoten definieren, die folgenden Filtertypen, um Personen entsprechend einer oder mehreren Bedingungen abzugleichen:

* Aktivitätsverlauf - Sie können einen Pfad entsprechend der Aktivität der Person definieren, die mit Folgendem zusammenhängt:

   * E-Mail-Nachrichten
   * Änderung des Datenwerts

* Personenattribute - Definieren Sie eine Bedingung anhand der Attribute einer Person, z. B. Land, Berufsbezeichnung oder Listenmitgliedschaft.

### Hinzufügen eines Knotens mit aufgeteilten Pfaden

<!--
>[!NOTE]
>
>When you split paths by people, a _Close split paths_ node is automatically inserted to end the split. A split-by-people path allows only _Take an action_ on people nodes.
-->

1. Navigieren Sie zur Journey-Karte.

1. Klicken Sie auf das Pluszeichen ( **+** ) auf einem Pfad und wählen Sie **[!UICONTROL Pfade aufteilen]**.

   <!-- ![Add journey node - split paths](./assets/add-node-split.png){width="300" zoomable="no"} -->

1. Um eine Bedingung zu definieren, die für _[!UICONTROL Pfad 1]_ gilt, klicken Sie auf **[!UICONTROL Bedingung anwenden]**.

1. Fügen Sie im Bedingungseditor einen oder mehrere Filter hinzu, um den Aufspaltungspfad zu definieren.

   * Ziehen Sie einen beliebigen Personenfilter aus dem linken Navigationsbereich und füllen Sie die Definition der Übereinstimmung aus.

   * Passen Sie Ihre Bedingungen durch Anwendung der **[!UICONTROL Filterlogik]** oben an. Sie wählen, ob alle Bedingungen oder nur eine der Bedingungen erfüllt sein sollen.

     <!-- ![Split path node - conditions person filter logic](./assets/node-split-conditions-people.png){width="700" zoomable="yes"} -->

   * Klicken Sie auf **[!UICONTROL Fertig]**.

1. Um weitere Pfade hinzuzufügen, klicken Sie auf **[!UICONTROL Pfad hinzufügen]** und wiederholen Sie die vorherigen Schritte, um die für den Pfad geltenden Bedingungen hinzuzufügen.

   Sie können auch jeden Pfad anhand dieser Bedingungen beschriften oder die Standardbeschriftungen verwenden.

1. Ordnen Sie die Pfade bei Bedarf entsprechend der Priorität neu an, die Sie für die Aufspaltung festlegen möchten.

   Die Pfadfilterung wird in der Reihenfolge von oben nach unten bewertet. Jede Person fährt auf dem ersten Pfad fort, der übereinstimmt.

   Klicken Sie auf die Pfeile nach oben und unten oben rechts auf jeder Pfadkarte, um sie in der Liste der Pfade nach oben oder unten zu verschieben.

   <!-- ![Split path node - reorder paths](./assets/node-split-reorder-paths-people.png){width="500" zoomable="yes"} -->

1. Aktivieren Sie die Option **[!UICONTROL Andere Personen]**, um einen Standardpfad für Personen hinzuzufügen, die den definierten Pfaden nicht entsprechen.

   Wenn diese Option nicht aktiviert ist, bewegen sich Personen, die mit keinem definierten Segment/Pfad übereinstimmen, an der Teilung vorbei und fahren mit dem nächsten Schritt auf der Journey fort.

Wenn Sie für jeden Pfad Bedingungen definiert haben, können Sie Aktions- oder Ereignisknoten hinzufügen, die Sie auf Personen in einem Pfad anwenden möchten.

## Zusammenführen von Pfadknoten

1. Navigieren Sie zur Journey-Zuordnung und suchen Sie den aufgeteilten Pfadknoten mit zwei oder mehr Pfaden.

   Jeder Pfad sollte eine Kombination aus Aktionen und Ereignissen auf jedem Pfad enthalten.

1. Klicken Sie auf das Pluszeichen ( **+** ) am Ende eines dieser Pfade und wählen Sie **[!UICONTROL Zusammenführungspfade]** aus den angezeigten Optionen aus.

   <!-- ![Journey node - merge paths](./assets/node-plus-icon-merge-paths.png){width="400" zoomable="no"} -->

1. Wählen Sie in den Knoteneigenschaften rechts die Pfade aus, die Sie zusammenführen möchten.

   <!-- ![Journey node - merge paths](./assets/node-merge-select-paths.png){width="600" zoomable="yes"} -->

   An dieser Stelle werden die Pfade zusammengeführt, sodass Personen aus den ausgewählten Pfaden zu einem einzigen Pfad kombiniert werden, der durch den Journey weiter ausgeführt werden kann.

1. Bei Bedarf können Sie die Zusammenführung von Pfaden aufheben, indem Sie zurück zu den Knoteneigenschaften der Zusammenführungspfade navigieren und das Kontrollkästchen für alle Pfade deaktivieren, die Sie entfernen möchten.
