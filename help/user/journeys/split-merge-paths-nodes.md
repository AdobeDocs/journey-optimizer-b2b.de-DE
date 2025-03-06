---
title: Pfade aufteilen und zusammenführen
description: Erfahren Sie mehr über die Knotentypen „Aufspaltungspfade“ und „Zusammenführungspfade“, die Sie zur Orchestrierung Ihrer Account-Journey in Journey Optimizer B2B edition verwenden können.
feature: Account Journeys
exl-id: 563d6a85-504d-4c70-b075-8a9a9e88bd6b
source-git-commit: e0fc061b55af4fd79248c2255db94280ee41e2c8
workflow-type: tm+mt
source-wordcount: '1584'
ht-degree: 4%

---

# Pfade aufteilen und zusammenführen

Verwenden Sie Split- und Merge-Path-Knoten auf Ihrer Account-Journey, um Ihre Account-Journey zu orchestrieren. Sie können die Zielgruppe gemäß Bedingungen segmentieren, die Sie definieren, und die Segmente kombinieren, um fortzufahren.

![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Übersichtsvideo ansehen](#overview-video)

## Pfade aufteilen

Fügen Sie einen Knoten _Pfade aufteilen_ hinzu, um einen oder mehrere segmentierte Pfade basierend auf Konto- oder Personenattributen zu definieren.

>[!NOTE]
>
>Es werden maximal 25 Pfade unterstützt.

**Pfade nach Konten aufteilen**: Pfade, die nach Konten aufgeteilt sind, können sowohl Konto- als auch Personenaktionen und -ereignisse enthalten. Diese Pfade können weiter aufgeteilt werden.

_Wie funktioniert ein aufgeteilter Pfad nach Kontenknoten?_

* Jeder Pfad, den Sie hinzufügen, enthält einen Endknoten mit der Möglichkeit, Knoten zu jedem Edge hinzuzufügen.
* Nach Kontoknoten aufgeteilt können verschachtelt werden. Sie können den Pfad wiederholt nach Konten aufteilen.
* Wertet Pfade von oben nach unten aus. Wenn ein Konto für den ersten und zweiten Pfad übereinstimmt, wird es nur entlang des ersten Pfads fortgesetzt.
* Zwei oder mehr Pfade können mithilfe eines Zusammenführungsknotens kombiniert werden.
* Unterstützt die Definition eines Pfads _[!UICONTROL Andere Konten]_, in dem Sie Aktionen oder Ereignisse für Konten hinzufügen können, die nicht mit einem der definierten Segmente/Pfade übereinstimmen.

![Journey-Knoten - Pfade nach Konto aufteilen](./assets/node-split-paths-account.png){width="700" zoomable="yes"}

**Pfade nach Personen aufteilen**: Pfade werden nach Personen aufgeteilt und können nur Personenaktionen enthalten. Diese Pfade können nicht erneut aufgeteilt und automatisch wieder verbunden werden.

_Wie funktioniert ein aufgeteilter Pfad nach Personenknoten?_

* Funktionen innerhalb einer Kombination _gruppierter Knoten_ Aufspaltung und Zusammenführung. Die Pfade der Aufspaltung werden automatisch zusammengeführt, sodass alle Personen in der Zielgruppe mit dem nächsten Schritt fortfahren können, ohne ihren Kontokontext zu verlieren.
* Nach Personen aufgeteilte Knoten können nicht verschachtelt werden. Sie können keinen aufgeteilten Pfad für Personen auf einem Pfad hinzufügen, der sich in diesem gruppierten Knoten befindet.
* Wertet Pfade von oben nach unten aus. Wenn eine Person für den ersten und zweiten Pfad eine Übereinstimmung findet, fährt sie nur entlang des ersten Pfads fort.
* Unterstützt die Verwendung von _Konto-Personen-Beziehungen_ mit denen Sie Personen nach ihrer Rolle filtern können (z. B. Auftragnehmer oder Vollzeit-Mitarbeiter), wie in den Rollenvorlagen definiert.
* Unterstützt die Definition eines Pfads _[!UICONTROL Andere Personen]_, in dem Sie Aktionen oder Ereignisse für Personen hinzufügen können, die nicht mit einem der definierten Segmente/Pfade übereinstimmen.

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
| | [!UICONTROL Spezialfilter] > [!UICONTROL Mitglied der Liste] | Die Person ist oder ist nicht Mitglied in einer oder mehreren Marketo Engage-Listen. |
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

1. Aktivieren Sie die Option **[!UICONTROL Andere Konten]**, um den Standardpfad für Konten zu definieren, die nicht mit den definierten Segmenten/Pfaden übereinstimmen.

   Wenn diese Option nicht aktiviert ist, endet das Journey für Konten, die nicht mit einem definierten Segment/Pfad innerhalb der Aufspaltung übereinstimmen.

### Fügen Sie einen Pfad für die Aufspaltung nach Personenknoten hinzu

>[!NOTE]
>
>Wenn Sie Pfade nach Personen aufteilen, wird _Knoten „Aufspaltungspfade schließen_ automatisch eingefügt, um die Aufspaltung zu beenden. Bei einem Pfad, der nach Personen aufgeteilt ist, ist nur _Aktion ausführen_ auf Personenknoten zulässig.

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
     >Wenn Sie benutzerdefinierte Personenfelder im Konto-Zielgruppenschema in Experience Platform definiert haben, sind diese Felder auch verfügbar, um als Personenattribute in Bedingungen zu verwenden.

   * Passen Sie Ihre Bedingungen durch Anwendung der **[!UICONTROL Filterlogik]** oben an. Sie wählen, ob alle Attributbedingungen oder eine beliebige Bedingung erfüllt werden sollen.

     ![Pfadknoten aufteilen - Bedingungen für Personenfilterlogik](./assets/node-split-conditions-people.png){width="700" zoomable="yes"}

   * Klicken Sie auf **[!UICONTROL Fertig]**.

1. Um weitere Pfade hinzuzufügen, klicken Sie auf **[!UICONTROL Pfad hinzufügen]** und wiederholen Sie die vorherigen Schritte, um die für diesen Pfad geltenden Bedingungen hinzuzufügen.

   Sie können auch jeden Pfad anhand dieser Bedingungen beschriften oder die Standardbeschriftungen verwenden.

1. Ordnen Sie die Pfade bei Bedarf entsprechend der Priorität neu an, die Sie für die Aufspaltung festlegen möchten.

   Die Pfadfilterung wird in der Reihenfolge von oben nach unten bewertet. Jede Person fährt auf dem ersten Pfad fort, der übereinstimmt.

   Klicken Sie auf die Pfeile nach oben und unten oben rechts auf jeder Pfadkarte, um sie in der Liste der Pfade nach oben oder unten zu verschieben.

   ![Pfadknoten aufteilen - Pfade neu anordnen](./assets/node-split-reorder-paths-people.png){width="500" zoomable="yes"}

1. Aktivieren Sie die Option **[!UICONTROL Andere Personen]**, um einen Standardpfad für Personen hinzuzufügen, die den definierten Pfaden nicht entsprechen.

   Wenn diese Option nicht aktiviert ist, bewegen sich Personen, die nicht mit einem definierten Segment/Pfad übereinstimmen, über die Teilung hinaus und fahren mit dem nächsten Schritt auf der Journey fort.

>[!BEGINSHADEBOX &quot;Marketo Engage List Membership“]

Überprüfen Sie in Marketo Engage _Smart_ Kampagnen) die Programmmitgliedschaft, um sicherzustellen, dass Leads keine doppelten E-Mails erhalten und nicht gleichzeitig Mitglieder mehrerer E-Mail-Streams sind. In Journey Optimizer B2B können Sie die Marketo Engage-Listenmitgliedschaft als Bedingung für Ihren Aufspaltungspfad nach Personen überprüfen, um doppelte Journey-Aktivitäten zu vermeiden.

Um die Listenmitgliedschaft in einer aufgeteilten Bedingung zu verwenden, erweitern Sie **[!UICONTROL Spezielle Filter]** und ziehen Sie die **[!UICONTROL Mitglied der Liste]** Bedingung in den Filterbereich. Vervollständigen Sie die Filterdefinition, um die Zugehörigkeit zu einer oder mehreren Marketo Engage-Listen zu bewerten.

![Aufspaltungspfad nach Personen-Bedingung für die Marketo Engage-Listenmitgliedschaft](./assets/node-split-paths-conditions-people-member-of-list.png){width="700" zoomable="yes"}

>[!ENDSHADEBOX]

Wenn Sie für jeden Pfad zur Aufteilung Ihrer Zielgruppe auf Personenebene Bedingungen definiert haben, können Sie Aktionen hinzufügen, die Sie für Personen durchführen möchten.

>[!NOTE]
>
>Wenn Sie die Zielgruppe nach Personen aufteilen, können Sie nur Personenaktionen hinzufügen, bis die Pfade geschlossen oder zusammengeführt werden.

## Zusammenführen von Pfaden

Fügen Sie einen Knoten _Zusammenführungspfade_ hinzu, um verschiedene Aufspaltungspfade nach Konto in Ihrem Journey zu kombinieren.

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

## Übersichtsvideo

>[!VIDEO](https://video.tv.adobe.com/v/3443231/?learn=on)
