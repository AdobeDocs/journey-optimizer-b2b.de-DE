---
title: Fragmente
description: Erfahren Sie, wie Sie visuelle Inhaltsfragmente als wiederverwendbare Komponenten für E-Mails und E-Mail-Vorlagen in Adobe Journey Optimizer B2B edition erstellen und verwenden.
feature: Content, Email Authoring
exl-id: 3c1d2ca0-d009-4a2a-9d81-1a838845b7fa
source-git-commit: 472ec05b4da1c5e91a2aa0da6bc9f5dedf03a862
workflow-type: tm+mt
source-wordcount: '2624'
ht-degree: 1%

---

# Fragmente

Ein Fragment ist eine wiederverwendbare Komponente, die in einer oder mehreren E-Mails und E-Mail-Vorlagen in Adobe Journey Optimizer B2B edition referenziert werden kann. Normalerweise handelt es sich dabei um einen Inhaltsblock (Text, Bild oder beides), der vorab erstellt und schnell in eine E-Mail- oder E-Mail-Vorlage eingefügt werden kann. Mit dieser Funktion können Sie mehrere benutzerdefinierte Inhaltsbausteine vorab erstellen, die von Ihren Mitgliedern des Marketing-Teams verwendet werden können, um E-Mail-Inhalte für einen verbesserten Design-Prozess zusammenzustellen. Häufige Anwendungsfälle sind Kopf-/Fußzeilen-Inhaltsbausteine für E-Mails, Einladungsbanner für Veranstaltungen und saisonale Grußformeln.

>[!BEGINSHADEBOX]

**Visuelle Fragmente**

Visuelle Fragmente sind vordefinierte visuelle Bausteine, die mit dem visuellen Inhalts-Designer erstellt wurden und die Sie in mehreren E-Mail-Adressen oder E-Mail-Vorlagen wiederverwenden können. Der aktuelle Umfang von Journey Optimizer B2B edition und diese Dokumentation beziehen sich nur auf visuelle Fragmente. Ausdrucksbasierte Fragmente werden in Journey Optimizer B2B edition noch nicht unterstützt.

>[!ENDSHADEBOX]

So verwenden Sie Fragmente in Ihren Workflows optimal:

* _Eigene Fragmente erstellen_ - Erstellen Sie visuelle Fragmente von Grund auf neu oder indem Sie Inhalte als Fragment aus dem visuellen Inhaltseditor speichern.
* _Fragmente_ wiederverwenden – Verwenden Sie sie so oft wie nötig in Ihrem Inhalte.

## Zugreifen auf und Verwalten von Fragmenten

Um auf visuelle Fragmente in Adobe Systems Journey Optimizer B2B Edition zuzugreifen, gehen Sie zur linken Navigation und klicken Sie auf **[!UICONTROL Content Management]** > **[!UICONTROL Fragments]**. Hierdurch wird eine Auflistungs-Seite geöffnet, in der alle in der Instanz erstellten Fragmente in einer Tabelle aufgeführt sind.

![Zugreifen auf die Fragmente Bibliothek](./assets/fragments-list.png){width="700" zoomable="yes"}

Die Tabelle wird nach der _[!UICONTROL Spalte &quot;Geändert]_ &quot; sortiert, wobei die zuletzt aktualisierten Fragmente standardmäßig ganz oben stehen. Klicken Sie auf den Spaltentitel, um zwischen aufsteigender und absteigender Reihenfolge zu wechseln.

### Fragmentstatus und -lebenszyklus

Der Fragmentstatus bestimmt seine Verfügbarkeit zur Verwendung in einer E-Mail oder E-Mail-Vorlage und die Änderungen, die Sie daran vornehmen können.

| Status | Beschreibung |
| -------------------- | ----------- |
| Entwurf | Wenn Sie ein Fragment erstellen, befindet es sich im Entwurfsstatus . Dieser Status bleibt erhalten, während Sie den visuellen Inhalt definieren oder bearbeiten, bis Sie ihn zur Verwendung in einer E-Mail- oder E-Mail-Vorlage veröffentlichen. Verfügbare Aktionen:<br/><ul><li>Alle Details bearbeiten<li>In Visual Designer bearbeiten<li>Veröffentlichen<li>Duplizieren<li>Löschen |
| Veröffentlicht | Wenn Sie ein Fragment veröffentlichen, wird es zur Verwendung in einer E-Mail oder E-Mail-Vorlage verfügbar. Veröffentlichte Fragmentinhalte können im visuellen Designer nicht geändert werden. Verfügbare Aktionen:<br/><ul><li>Beschreibung bearbeiten.<li>Hinzufügen zu einer E-Mail oder Vorlage<li>Versionsentwurf erstellen<li>Duplizieren<li>Löschen (wenn nicht in Gebrauch) |
| Mit Entwurf veröffentlicht | Wenn Sie einen Entwurf aus einem veröffentlichten Fragment erstellen, bleibt die veröffentlichte Version zur Verwendung in einer E-Mail- oder E-Mail-Vorlage verfügbar und der Entwurfsinhalt kann im visuellen Designer geändert werden. Wenn Sie die Entwurfsversion veröffentlichen, ersetzt sie die aktuelle veröffentlichte Version, und der Inhalt wird in den E-Mails und E-Mail-Vorlagen, in denen sie verwendet wird, aktualisiert. Verfügbare Aktionen:<br/><ul><li>Beschreibung bearbeiten.<li>Hinzufügen zu einer E-Mail oder Vorlage<li>Bearbeiten der Entwurfsversion in Visual Designer<li>Entwurfsversion veröffentlichen<li>Duplizieren<li>Löschen (wenn nicht in Gebrauch) |

![Lebenszyklus des Fragmentstatus](./assets/status-lifecycle-diagram.png){zoomable="yes"}

>[!IMPORTANT]
>
>Der Fragmentstatus wurde mit der Journey Optimizer B2B edition-Version vom August eingeführt. Alle Fragmente, die vor dieser Version erstellt wurden _haben den Status „Entwurf_, auch wenn sie in einer E-Mail oder Vorlage verwendet werden. Wenn Sie Änderungen an diesen Fragmenten vornehmen, müssen Sie das Fragment veröffentlichen, um die Änderungen weiterzugeben.

### Filtern der Fragmentliste

Um nach einem Fragment anhand des Namens zu suchen, geben Sie eine Textzeichenfolge in die Suchleiste für eine Übereinstimmung ein. Klicken Sie auf _Filter_-Symbol ( ![Filtersymbol ein- oder ausblenden](../assets/do-not-localize/icon-filter.svg) ), um die verfügbaren Filteroptionen anzuzeigen und die Einstellungen zu ändern, um die angezeigten Elemente entsprechend Ihren angegebenen Kriterien zu filtern.

![Filtern Sie die angezeigten Fragmente](./assets/fragments-list-filtered.png){width="700" zoomable="yes"}

### Spaltenanzeige anpassen

Passen Sie die Spalten an, die Sie in der Tabelle anzeigen möchten, indem Sie oben rechts auf _Tabelle anpassen_ (![Symbol „Tabelle ](../assets/do-not-localize/icon-column-settings.svg)„) klicken.

Wählen Sie im Dialogfeld die anzuzeigenden Spalten aus und klicken Sie auf **[!UICONTROL &quot;Übernehmen]**&quot;.

![Wählen Sie die Spalten aus, die Sie anzeigen möchten](./assets/fragments-customize-table-dialog.png){width="300"}

## Erstellen von Fragmenten

Sie können neue visuelle Fragmente in Journey Optimizer B2B edition erstellen, indem Sie oben **[!UICONTROL auf „Fragment]**&quot; klicken.

1. Geben _[!UICONTROL im Dialogfeld Fragment erstellen]_ einen nützlichen Wert **[!UICONTROL Name]** und **[!UICONTROL Beschreibung]** (optional) ein.

   Fragmentanforderungen:

   * Name - Maximal 100 Zeichen, muss eindeutig sein, Groß-/Kleinschreibung wird nicht beachtet

   * Beschreibung - Maximal 300 Zeichen

   * Alpha-, numerische und Sonderzeichen sind zulässig

   * Reservierte Zeichen sind **_nicht zulässig_**: `\ / : * ? " < > |`

   ![Dialogfeld „Fragment erstellen“](./assets/assets-fragments-create-dialog.png){width="400"}

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

   Der visuelle Designer wird mit einer leeren Arbeitsfläche geöffnet.

1. Verwenden Sie die Inhaltserstellungs-Tools, um den visuellen Fragmentinhalt zu erstellen:

   * [Hinzufügen von Struktur und Inhalten](./fragment-authoring.md#add-structure-and-content)
   * [Assets hinzufügen](./fragment-authoring.md#add-assets)
   * [Navigieren in den Ebenen, Einstellungen und Stilen](./fragment-authoring.md#navigate-the-layers-settings-and-styles)
   * [Personalisieren Inhalte](./fragment-authoring.md#personalize-content)
   * [Benutzerdefinierte Felder aktivieren](./fragment-authoring.md#enable-fragment-customization)
   * [Bearbeiten URL Tracking verknüpft](./fragment-authoring.md#edit-linked-url-tracking)

1. Klicken Sie jederzeit auf **[!UICONTROL Speichern]** , um den Entwurf des Fragments zu speichern.

1. Wenn Sie bereit sind, das Fragment zur Verwendung in einer E-Mail oder einem E-Mail-Vorlage bereitzustellen, klicken Sie auf Publish **&#x200B;**.

## Anzeigen von Fragmentdetails

Klicken Sie auf den Namen eines beliebigen Fragments auf der Listenseite, um die Fragmentdetailseite zu öffnen. Sie können wählen, ob Sie das Fragment bearbeiten, das Fragment umbenennen oder die Fragmentbeschreibung aktualisieren möchten. Nehmen Sie Aktualisierungen vor und klicken Sie außerhalb des Namens- oder Beschreibungsfelds, um Änderungen automatisch zu speichern.

>[!NOTE]
>
>Wenn ein veröffentlichtes Fragment von einer E-Mail- oder E-Mail-Vorlage verwendet wird, können Sie den Namen nicht ändern oder den Inhalt bearbeiten. Sie können eine Entwurfsversion erstellen, wenn Sie Änderungen am Fragment vornehmen möchten.

![Details für ein veröffentlichtes Fragment anzeigen](./assets/fragment-details-published.png){width="600" zoomable="yes"}

Klicken Sie **[!UICONTROL Fragment bearbeiten]**, um das Fragment im visuellen Inhaltseditor zu öffnen.

Sie können die Ansicht jederzeit verlassen, indem Sie oben links auf _Zurück_-Pfeil klicken, der Sie zur Listenseite _Fragmente_ zurückbringt.

## Anzeigen von durch Verweise verwendeten Fragmenten

Klicken Sie auf der Seite mit den Fragmentdetails auf die Registerkarte **[!UICONTROL Verwendet von]**, um Details zur aktuellen Verwendung des Fragments in Journey Optimizer B2B edition sowie zu E-Mails, E-Mail-Vorlagen und Fragmenten anzuzeigen.

>[!IMPORTANT]
>
>Fragment, das derzeit von einer E-Mail oder E-Mail-Vorlage verwendet wird, kann nicht gelöscht werden.

Verweise werden nach Kategorie angezeigt: _E-_ oder _E-Mail-Vorlage_. E-Mails in Journey Optimizer B2B edition sind in Account Journey eingebettet und verfasst, sodass die übergeordnete Journey der E-Mail, die das Fragment verwendet, als Referenzen angezeigt wird.

![Wird von Verweisen für das Fragment verwendet](./assets/fragment-used-by-published.png){width="600" zoomable="yes"}

Klicken Sie auf den Link, um die entsprechende E-Mail oder E-Mail-Vorlage zu öffnen, in der das Fragment verwendet wird.

## Löschen von Fragmenten

Fragment, das derzeit von einer E-Mail- oder E-Mail-Vorlage verwendet wird, kann nicht gelöscht werden. Stellen Sie daher sicher, dass Sie die Verweise _Verwendet von_ überprüfen, bevor Sie mit dem Entfernen eines Fragments beginnen. Außerdem kann eine Entfernung nicht rückgängig gemacht werden. Überprüfen Sie dies, bevor Sie eine Löschaktion starten.

Sie können ein Fragment mit einer der folgenden Methoden löschen:

* Klicken Sie in den Fragmentdetails auf der rechten Seite auf **[!UICONTROL Löschen]**.
* Klicken Sie auf _[!UICONTROL Listenseite]_ Fragmente“ auf das Auslassungszeichen neben dem Fragment und wählen Sie **[!UICONTROL Löschen]**.

Diese Aktion öffnet ein Bestätigungsdialogfeld. Sie können den Vorgang abbrechen, indem Sie auf **[!UICONTROL Abbrechen]** klicken oder auf **[!UICONTROL Löschen]** klicken, um den Löschvorgang zu bestätigen.

![Dialogfeld „Fragment löschen“](./assets/fragment-delete-dialog.png){width="400"}

Wenn das Fragment derzeit verwendet wird, wird durch die Aktion ein Informationsdialogfeld geöffnet, in dem Sie darauf hingewiesen werden, dass es nicht gelöscht werden kann. Klicken Sie auf **[!UICONTROL OK]**, wodurch die Löschaktion abgebrochen wird.

![Dialogfeld Löschen Fragment - verwendetes Fragment kann nicht gelöscht werden](./assets/fragment-delete-dialog-in-use.png){width="400"}

## Bearbeiten von Fragmenten

Die Bearbeitung eines Fragments hängt von seinem aktuellen Status ab:

* Wenn sich ein Fragment im _Entwurfsstatus_ befindet, können Sie alle seine Details und den visuellen Inhalte bearbeiten.
* Wenn sich ein Fragment im _Status &quot;Veröffentlicht_ &quot; befindet, können Sie die Fragmentbeschreibung, nicht aber den Namen bearbeiten. Die visuelle Inhalte kann nicht bearbeitet werden.
* Wenn sich ein Fragment im _Entwurfsstatus_ &quot;Veröffentlicht&quot; befindet, ist die Bearbeitung der Details auf die Beschreibung beschränkt. Sie können auch die visuellen Inhalte für die Entwurfsversion bearbeiten.

>[!BEGINTABS]

>[!TAB Entwurf]

1. Klicken Sie in der _[!UICONTROL Seite der Liste &quot;Fragmente&quot; auf den Namen des Fragments]_ , um es zu öffnen.

   Daraufhin wird eine Vorschau der visuellen Inhalte angezeigt, mit den Fragmentdetails auf der rechten Seite.

1. Ändern Sie alle Details, z. B. Namen und Beschreibung.

   ![Details für Fragment mit Entwurfsstatus](./assets/fragment-draft-details.png){width="600" zoomable="yes"}

1. Um Änderungen am Inhalt im visuellen Designer vorzunehmen, klicken Sie auf **[!UICONTROL Fragment bearbeiten]**.

   Verwenden Sie nach Bedarf die visuellen Designer-Tools:

   * [Hinzufügen von Struktur und Inhalten](./fragment-authoring.md#add-structure-and-content)
   * [Assets hinzufügen](./fragment-authoring.md#add-assets)
   * [Navigieren in den Ebenen, Einstellungen und Stilen](./fragment-authoring.md#navigate-the-layers-settings-and-styles)
   * [Inhalt personalisieren](./fragment-authoring.md#personalize-content)
   * [Benutzerdefinierte Felder aktivieren](./fragment-authoring.md#enable-fragment-customization)
   * [Verknüpftes URL-Tracking bearbeiten](./fragment-authoring.md#edit-linked-url-tracking)

   Klicken Sie **[!UICONTROL Speichern]** oder **[!UICONTROL Speichern und schließen]** um zu den Fragmentdetails zurückzukehren.

1. Wenn das Fragment Ihren Kriterien entspricht und Sie es in einer E-Mail oder E-Mail-Vorlage verfügbar machen möchten, klicken Sie auf **[!UICONTROL Veröffentlichen]**.

>[!TAB Veröffentlicht]

1. Klicken Sie auf _[!UICONTROL Listenseite]_ Fragmente“ auf den Fragmentnamen, um das Fragment zu öffnen.

   Eine Vorschau des visuellen Inhalts wird mit den Fragmentdetails auf der rechten Seite angezeigt.

1. Ändern Sie bei Bedarf die Beschreibung.

   Für ein veröffentlichtes Fragment können alle anderen Details nicht geändert werden.

1. Wenn Sie den Inhalt aktualisieren möchten, klicken Sie oben **[!UICONTROL auf „Entwurfsversion]**&quot;.

   Klicken Sie **[!UICONTROL Dialogfeld]** OK“, um die Entwurfsversion im visuellen Designer zu öffnen.

   ![Dialogfeld „Entwurfsversion erstellen“](./assets/fragments-create-draft-version.png){width="300"}

   Verwenden Sie nach Bedarf die visuellen Designer-Tools:

   * [Hinzufügen von Struktur und Inhalten](./fragment-authoring.md#add-structure-and-content)
   * [hinzufügen Assets](./fragment-authoring.md#add-assets)
   * [Navigieren in den Ebenen, Einstellungen und Stilen](./fragment-authoring.md#navigate-the-layers-settings-and-styles)
   * [Personalisieren Inhalte](./fragment-authoring.md#personalize-content)
   * [Benutzerdefinierte Felder aktivieren](./fragment-authoring.md#enable-fragment-customization)
   * [Bearbeiten URL Tracking verknüpft](./fragment-authoring.md#edit-linked-url-tracking)

   Klicken Sie **[!UICONTROL Speichern]** oder **[!UICONTROL Speichern und schließen]** um zu den Fragmentdetails zurückzukehren.

1. Wenn das Entwurfsfragment Ihren Kriterien entspricht und Sie die Änderungen zur Verwendung in einer E-Mail oder E-Mail-Vorlage bereitstellen möchten, klicken Sie auf **[!UICONTROL Veröffentlichen]**.

   Wenn Sie die Entwurfsversion veröffentlichen, ersetzt sie die aktuelle veröffentlichte Version, und der Inhalt wird in den E-Mails und E-Mail-Vorlagen aktualisiert, in denen sie bereits verwendet wird.

>[!TAB Veröffentlicht mit Entwurf]

Es gibt zwei Möglichkeiten, die Entwurfsversion zur Bearbeitung über die Listenseite _[!UICONTROL Fragmente]_ zu öffnen:

* Klicken Sie auf das _Mehr_-Symbol (**…**) neben dem Fragmentnamen und wählen Sie **[!UICONTROL Entwurfsversion öffnen]**.

  ![Entwurfsversion öffnen](./assets/fragments-create-draft-version.png){width="300"}

* Klicken Sie auf den Fragmentnamen, um das Fragment zu öffnen. Klicken Sie dann oben **[!UICONTROL auf]** Entwurfsversion öffnen“.

  Eine Vorschau des visuellen Inhalts für die Entwurfsversion wird mit den Fragmentdetails auf der rechten Seite angezeigt.

So aktualisieren Sie den Inhalt:

1. Klicken **[!UICONTROL oben]** auf „Fragment bearbeiten“. Verwenden Sie nach Bedarf die visuellen Designer-Tools:

   * [Hinzufügen von Struktur und Inhalten](./fragment-authoring.md#add-structure-and-content)
   * [hinzufügen Assets](./fragment-authoring.md#add-assets)
   * [Navigieren in den Ebenen, Einstellungen und Stilen](./fragment-authoring.md#navigate-the-layers-settings-and-styles)
   * [Personalisieren Inhalte](./fragment-authoring.md#personalize-content)
   * [Benutzerdefinierte Felder aktivieren](./fragment-authoring.md#enable-fragment-customization)
   * [Bearbeiten URL Tracking verknüpft](./fragment-authoring.md#edit-linked-url-tracking)

   Klicken Sie **[!UICONTROL Speichern]** oder **[!UICONTROL Speichern und schließen]** um zu den Fragmentdetails zurückzukehren.

1. Wenn das Entwurfsfragment Ihren Kriterien entspricht und Sie die Änderungen zur Verwendung in einer E-Mail oder E-Mail-Vorlage bereitstellen möchten, klicken Sie auf **[!UICONTROL Veröffentlichen]**.

   Wenn Sie die Entwurfsversion veröffentlichen, ersetzt sie die aktuell veröffentlichte Version und die Inhalte wird in den E-Mails und E-Mail-Vorlagen aktualisiert, in denen sie bereits verwendet wird.

>[!ENDTABS]

## Duplizieren Fragmente

Sie können ein Fragment mit einer der folgenden Methoden Duplikat:

* Klicken Sie in der _[!UICONTROL Liste &quot;Fragmente]_ &quot; Seite auf das _Mehr-Symbol_ (**...**) neben dem Namen des Fragments und wählen Sie &quot; **[!UICONTROL Duplizieren]**&quot;.
* Klicken Sie oben rechts in der Seite &quot;Fragmentdetails&quot; auf ... **&#x200B;**&#x200B;Mehr und wählen Sie **[!UICONTROL Duplizieren]**.

![Duplizieren des Fragments](./assets/fragment-details-duplicate.png){width="600" zoomable="yes"}

Geben Sie im Dialogfeld einen nützlichen Namen (eindeutig) und eine Beschreibung ein. Klicken Sie auf **[!UICONTROL Duplizieren]** , um die Aktion abzuschließen.

![Geben Sie einen Namen und eine Beschreibung für das duplizierte Fragment ein](./assets/fragment-duplicate-dialog.png){width="400"}

Das duplizierte (neue) Fragment wird dann in der Liste &quot; _Fragmente_ &quot; angezeigt.

## Neues Fragment aus E-Mail oder Vorlage Inhalte Speichern

Beim Erstellen/Bearbeiten einer E-Mail oder eines E-Mail-Vorlage in der Visual Inhalte Bearbeiter können Sie die Inhalte ganz oder teilweise als Fragment speichern, damit sie zur Wiederverwendung zur Verfügung steht.

1. Wenn einige Inhalte als Fragment gespeichert werden sollen, klicken Sie auf **[!UICONTROL Mehr]** und wählen Sie Speichern als Fragment **aus**.

1. Wählen Sie die verschiedenen Elemente aus, die in das Fragment aufgenommen werden sollen.

   Wählen Sie mehrere Strukturen aus, indem Sie die Umschalt- oder die Strg-Taste gedrückt halten.

   Sie können nur nebeneinanderliegende Strukturen auswählen, und die Schnittstelle erlaubt es Ihnen nicht, nicht benachbarte Elemente auszuwählen.

1. Klicken Sie bei ausgewähltem Inhalt oben **[!UICONTROL auf]** Erstellen“.

1. Geben Sie im Dialogfeld einen nützlichen Namen und eine Beschreibung für das Fragment ein. Klicken Sie dann auf **[!UICONTROL Erstellen]**.

   Das neue Fragment wird dann auf der Seite _Fragmente_ angezeigt und ist auch für die Verwendung in E-Mails und E-Mail-Vorlagen verfügbar.

## hinzufügen visuelle Fragmente in Ihre E-Mail oder Vorlage Inhalte

Fragmente sind zur Wiederverwendung konzipiert und können für die Erstellung von E-Mail-Vorlagen und E-Mail-Vorlagen eingefügt werden. Sie können einer E-Mail oder Vorlage bis zu 30 Fragmente hinzufügen. Fragmente können nur bis zu einer Ebene verschachtelt werden.

>[!BEGINTABS]

>[!TAB Hinzufügen von Fragmenten zu einer E-Mail]

1. Navigieren Sie zu **[!UICONTROL Account-Journey]** und öffnen Sie eine bestehende Journey oder erstellen Sie eine neue Journey.

1. Erstellen Sie einen [_[!UICONTROL E-Mail senden &#x200B;]_-Knoten](./email-authoring.md#add-an-email-action-in-an-account-journey).

1. Erstellen oder bearbeiten [E-Mail-Inhalt für den Knoten](./email-authoring.md#create-the-email-content).

1. Ziehen Sie ein Element per Drag-and-Drop aus dem **[!UICONTROL Komponenten]**-Menü, um eine _Struktur_ für das Fragment bereitzustellen.

1. Um die Liste der veröffentlichten Fragmente zu öffnen, klicken Sie auf das Symbol _Fragmente_ .

   Sie haben folgende Möglichkeiten:
   * Sortieren Sie die Liste.
   * Durchsuchen, Durchsuchen und Filtern der Liste.
   * Wechseln zwischen Karten- (Miniatur-) und Listenansicht.
   * Aktualisieren Sie die Liste, um die kürzlich erstellten Fragmente anzuzeigen.

   ![Suchen nach einem Fragment im visuellen Designer](./assets/fragments-list-designer-search.png){width="600"}

1. Ziehen Sie eines der Fragmente in den Platzhalter der Strukturkomponente.

   Die Bearbeiter rendert das Fragment innerhalb des Abschnitts/Elements der E-Mail-Struktur.

Die Inhalte des Fragments wird innerhalb der Struktur dynamisch aktualisiert, um die Darstellung der Inhalte in der E-Mail visuell darzustellen.

>[!TIP]
>
>Wenn das Fragment das gesamte horizontale Layout in der E-Mail einnehmen soll, fügen Sie eine [!UICONTROL 1:1-Spaltenstruktur] hinzu und ziehen Sie das Fragment dann per Drag &amp; Drop hinein.

Nachdem die E-Mail gespeichert wurde, wird sie in der Seite &quot;Fragmentdetails&quot; angezeigt, wenn das _[!UICONTROL Tab &quot;Verwendet von]_ &quot; ausgewählt wurde. Zu einer E-Mail hinzugefügte Fragmente können nicht innerhalb der E-Mail oder Vorlage bearbeitet werden – das veröffentlichte Quellfragment definiert die Inhalte.

>[!TAB hinzufügen von Fragmenten zu einer E-Mail-Vorlage]

1. Klicken Sie in der linken Navigation auf **[!UICONTROL Content-]** > **[!UICONTROL Vorlagen]**.

1. Erstellen Sie eine neue Vorlage oder öffnen Sie eine vorhandene E-Mail-Vorlage und klicken Sie auf **[!UICONTROL E-Mail-Vorlage bearbeiten]**.

1. Ziehen Sie ein Element per Drag-and-Drop aus dem **[!UICONTROL Komponenten]**-Menü, um eine _Struktur_ für das Fragment bereitzustellen.

1. Um die Fragmentliste zu öffnen, klicken Sie auf das Symbol _Fragmente_ .

   Sie haben folgende Möglichkeiten:
   * Sortieren Sie die Liste.
   * Durchsuchen, Durchsuchen und Filtern der Liste.
   * Wechseln zwischen Karten- (Miniatur-) und Listenansicht.
   * Aktualisieren Sie die Liste, um die kürzlich erstellten Fragmente anzuzeigen.

   ![Suchen nach einem Fragment im visuellen Designer](./assets/fragments-list-designer-search.png){width="600"}

1. Ziehen Sie eines der Fragmente in den Platzhalter der Strukturkomponente.

   Der Editor rendert das Fragment innerhalb des Abschnitts/Elements der E-Mail-Vorlagenstruktur.

1. Ziehen Sie ein beliebiges Fragment in den Platzhalter der Strukturkomponente.

   Die Bearbeiter rendert das Fragment innerhalb des Abschnitts/Elements der Vorlage-Struktur der E-Mail.

>[!TIP]
>
>Wenn das Fragment das gesamte horizontale Layout innerhalb der E-Mail-Vorlage einnehmen soll, fügen Sie eine _[!UICONTROL 1:1-Spaltenstruktur]_ hinzu und ziehen Sie das Fragment dann per Drag &amp; Drop hinein.

Nachdem die E-Mail-Vorlage gespeichert wurde, wird sie in der Seite &quot;Fragmentdetails&quot; angezeigt, wenn das _[!UICONTROL Tab &quot;Verwendet von]_ &quot; ausgewählt wurde. Zu einer E-Mail-Vorlage hinzugefügte Fragmente können innerhalb der Vorlage nicht bearbeitet werden. Das veröffentlichte Quellfragment definiert die Inhalte.

>[!ENDTABS]

## Fragmentaktionen beim Authoring von E-Mails und Vorlage

Wenn ein Fragment zu einer E-Mail oder E-Mail-Vorlage hinzugefügt wird, kann der Fragmentinhalt nicht innerhalb der E-Mail oder Vorlage bearbeitet werden. Sie können jedoch die folgenden Aktionen anwenden:

* **[!UICONTROL Löschen]** - Mit dieser Aktion wird das Fragment aus dem aktuellen Inhalt der E-Mail oder E-Mail-Vorlage entfernt (die Fragmentquelle ist nicht betroffen).
* **&#x200B;**&#x200B;Aktualisieren - Diese Aktion aktualisiert die Inhalte des Fragments in der aktuellen E-Mail oder E-Mail-Vorlage. Die Aktualisierung ist nützlich, wenn Sie alle kürzlich vorgenommenen Änderungen am Fragment nach dem Hinzufügen zur E-Mail oder E-Mail-Vorlage widerspiegeln möchten.
* **&#x200B;**&#x200B;Duplizieren - Mit dieser Aktion wird das Fragment in derselben E-Mail oder E-Mail-Vorlage innerhalb der Bearbeiter mit denselben Abmessungen dupliziert und direkt darunter hinzugefügt.
* **[!UICONTROL Fragment]** öffnen: Mit dieser Aktion wird eine neue Browser Tab mit dem Fragment Bearbeiter Seite und Details geöffnet.
* **[!UICONTROL Vererbung]** unterbrechen - Diese Aktion unterbricht die Vererbung des Fragments (und seiner Änderungen) von der Quelle. Verwenden Sie diese Aktion, um das Fragment Inhalte als unabhängiges und bearbeitbares Inhalte in der E-Mail oder E-Mail-Vorlage verfügbar zu machen. Außerdem wird die E-Mail-Adresse oder der E-Mail-Vorlage aus der _Referenz &quot;Verwendet von_ &quot; für das ursprüngliche Fragment entfernt.

Wenn Sie das Fragment auf der Bearbeiter Seite auswählen, sind diese Aktionen in der Kontextsymbolleiste und im Eigenschaftenbereich auf der rechten Seite verfügbar.

![Übernehmen Aktionen für das ausgewählte Fragment](./assets/fragment-actions-email-authoring.png){width="600" zoomable="yes"}
