---
title: Fragmente
description: Erfahren Sie, wie Sie visuelle Inhaltsfragmente als wiederverwendbare Komponenten für E-Mails und E-Mail-Vorlagen in Adobe Journey Optimizer B2B Edition erstellen und verwenden.
feature: Content, Email Authoring
exl-id: 3c1d2ca0-d009-4a2a-9d81-1a838845b7fa
source-git-commit: d0bf71dd1503d824391df7d7a7c59e3c2c925f03
workflow-type: tm+mt
source-wordcount: '2687'
ht-degree: 3%

---

# Fragmente

Ein Fragment ist eine wiederverwendbare Komponente, die in einer oder mehreren E-Mail- und E-Mail-Vorlagen in Adobe Journey Optimizer B2B Edition referenziert werden kann. Normalerweise handelt es sich dabei um einen Inhaltsbaustein (Text, Bild oder beides), der vorab erstellt und schnell in eine E-Mail- oder E-Mail-Vorlage eingefügt werden kann. Mit dieser Funktion können Sie mehrere benutzerdefinierte Inhaltsbausteine für die Verwendung durch Ihre Marketing-Team-Mitglieder erstellen, um E-Mail-Inhalte zusammenzustellen und so einen verbesserten Designprozess zu ermöglichen. Häufige Anwendungsfälle sind Kopfzeilen-/Fußzeilen-Inhaltsbausteine für E-Mails, Einladungsbanner für Ereignisse und saisonale Grußformeln.

So nutzen Sie Fragmente in Ihren Workflows optimal:

* _Eigene Fragmente erstellen_ - Erstellen Sie visuelle Fragmente entweder von Grund auf neu oder durch Speichern von Inhalt als Fragment aus dem Visual Content Editor.
* _Fragmente wiederverwenden_ - Verwenden Sie sie so oft wie nötig in Ihrem Inhalt.

## Visuelle Fragmente

Visuelle Fragmente sind vordefinierte visuelle Bausteine, die mit dem Visual Content Editor erstellt wurden und die Sie über mehrere E-Mails oder E-Mail-Vorlagen hinweg wiederverwenden können. Der aktuelle Umfang von Journey Optimizer B2B Edition und dieser Dokumentation ist nur der von visuellen Fragmenten. Ausdrucksbasierte Fragmente werden in Journey Optimizer B2B Edition noch nicht unterstützt.

## Zugreifen auf und Verwalten von Fragmenten

Um auf visuelle Fragmente in Adobe Journey Optimizer B2B Edition zuzugreifen, navigieren Sie zum linken Navigationsbereich und klicken Sie auf **[!UICONTROL Inhaltsverwaltung]** > **[!UICONTROL Fragmente]**. Durch diese Aktion wird eine Listenseite mit allen Fragmenten geöffnet, die in der in einer Tabelle aufgelisteten Instanz erstellt wurden.

![Zugriff auf die Fragmentbibliothek](./assets/fragments-list.png){width="700" zoomable="yes"}

Die Tabelle wird nach der Spalte _[!UICONTROL Geändert]_ sortiert, wobei sich die zuletzt aktualisierten Fragmente standardmäßig oben befinden. Klicken Sie auf den Spaltentitel, um ihn zwischen auf- und absteigend zu ändern.

### Fragmentstatus und -lebenszyklus

Der Fragmentstatus bestimmt seine Verfügbarkeit für die Verwendung in einer E-Mail- oder E-Mail-Vorlage sowie die Änderungen, die Sie daran vornehmen können.

| Status | Beschreibung |
| -------------------- | ----------- |
| Entwurf | Wenn Sie ein Fragment erstellen, befindet es sich im Entwurfsstatus. Dieser Status behält sich den Status vor, da Sie den visuellen Inhalt definieren oder bearbeiten, bis Sie ihn zur Verwendung in einer E-Mail- oder E-Mail-Vorlage veröffentlichen. Verfügbare Aktionen:<br/><ul><li>Alle Details bearbeiten<li>In Visual Designer bearbeiten<li>Veröffentlichen Sie<li>Doppelt<li>Löschen |
| Veröffentlicht | Wenn Sie ein Fragment veröffentlichen, wird es zur Verwendung in einer E-Mail- oder E-Mail-Vorlage verfügbar. Veröffentlichte Fragmentinhalte können im visuellen Designer nicht geändert werden. Verfügbare Aktionen:<br/><ul><li>Beschreibung bearbeiten.<li>Hinzufügen zu einer E-Mail oder Vorlage<li>Entwurfsversion erstellen<li>Doppelt<li>Löschen (falls nicht bereits verwendet) |
| Mit Entwurf veröffentlicht | Wenn Sie einen Entwurf aus einem veröffentlichten Fragment erstellen, bleibt die veröffentlichte Version für die Verwendung in einer E-Mail- oder E-Mail-Vorlage verfügbar. Der Inhalt des Entwurfs kann im visuellen Designer geändert werden. Wenn Sie den Entwurf veröffentlichen, ersetzt er die aktuelle veröffentlichte Version und der Inhalt wird in den E-Mails und E-Mail-Vorlagen aktualisiert, in denen er verwendet wird. Verfügbare Aktionen:<br/><ul><li>Beschreibung bearbeiten.<li>Hinzufügen zu einer E-Mail oder Vorlage<li>Entwurfsversion in Visual Designer bearbeiten<li>Publish-Entwurfsversion<li>Doppelt<li>Löschen (falls nicht bereits verwendet) |

![Lebenszyklus des Fragmentstatus](./assets/status-lifecycle-diagram.png){width="800" zoomable="yes"}

>[!IMPORTANT]
>
>Der Fragmentstatus wurde in der Journey Optimizer B2B Edition August-Version eingeführt. Alle vor dieser Version erstellten Fragmente haben den Status _Entwurf_ , auch wenn sie in einer E-Mail oder Vorlage verwendet werden. Wenn Sie Änderungen an diesen Fragmenten vornehmen, müssen Sie das Fragment veröffentlichen, um die Änderungen zu übernehmen.

### Filtern der Fragmentliste

Um nach einem Fragment anhand des Namens zu suchen, geben Sie eine Textzeichenfolge in die Suchleiste für eine Übereinstimmung ein. Klicken Sie auf das Symbol _Filter_ ( ![Symbol zum Ein- oder Ausblenden von Filtern](../assets/do-not-localize/icon-filter.svg) ), um die verfügbaren Filteroptionen anzuzeigen und die Einstellungen zu ändern, um die angezeigten Elemente gemäß Ihren angegebenen Kriterien zu filtern.

![Filtern der angezeigten Fragmente](./assets/fragments-list-filtered.png){width="700" zoomable="yes"}

### Spaltenanzeige anpassen

Passen Sie die Spalten, die in der Tabelle angezeigt werden sollen, an, indem Sie oben rechts auf das Symbol _Tabelle anpassen_ ( ![Tabellensymbol anpassen](../assets/do-not-localize/icon-column-settings.svg) ) klicken.

Wählen Sie im Dialogfeld die anzuzeigenden Spalten aus und klicken Sie auf **[!UICONTROL Anwenden]**.

![Wählen Sie die Spalten aus, die angezeigt werden sollen](./assets/fragments-customize-table-dialog.png){width="300"}

## Erstellen von Fragmenten

Sie können neue visuelle Fragmente in Journey Optimizer B2B Edition erstellen, indem Sie oben rechts auf **[!UICONTROL Fragment erstellen]** klicken.

1. Geben Sie im Dialogfeld _[!UICONTROL Fragment erstellen]_ einen nützlichen **[!UICONTROL Namen]** und **[!UICONTROL Beschreibung]** ein (optional).

   Fragmentanforderungen:

   * Name - Maximal 100 Zeichen, muss eindeutig sein, Groß-/Kleinschreibung nicht berücksichtigt

   * Beschreibung - Maximal 300 Zeichen

   * Alpha-, numerische und Sonderzeichen sind zulässig

   * Reservierte Zeichen sind **_nicht erlaubt_**: `\ / : * ? " < > |`

   ![Dialogfeld &quot;Fragment erstellen&quot;](./assets/assets-fragments-create-dialog.png){width="400"}

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

   Der visuelle Designer wird mit einer leeren Arbeitsfläche geöffnet.

1. Verwenden Sie die Inhaltserstellungswerkzeuge, um den Inhalt des visuellen Fragments zu erstellen:

   * [Hinzufügen von Struktur und Inhalt](#add-structure-and-content)
   * [Assets hinzufügen](#add-assets)
   * [Navigieren in den Ebenen, Einstellungen und Stilen](#navigate-the-layers-settings-and-styles)
   * [Inhalt personalisieren](#personalize-content)
   * [Linked URL-Tracking bearbeiten](#edit-linked-url-tracking)

1. Klicken Sie jederzeit auf **[!UICONTROL Speichern]** , um den Entwurf des Fragments zu speichern.

1. Wenn Sie bereit sind, das Fragment für die Verwendung in einer E-Mail- oder E-Mail-Vorlage verfügbar zu machen, klicken Sie auf **[!UICONTROL Publish]**.

### Hinzufügen von Struktur und Inhalt {#design-fragment}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_fragment"
>title="Hinzufügen von Strukturkomponenten"
>abstract="Strukturkomponenten definieren das Layout des Fragments. Ziehen Sie eine **Struktur**-Komponente per Drag-and-Drop auf die Arbeitsfläche, um mit der Gestaltung Ihres Fragmentinhalts zu beginnen."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_fragment"
>title="Über Inhaltskomponenten"
>abstract="Inhaltskomponenten sind leere Platzhalter für Inhalte, mit denen Sie das Layout eines Fragments erstellen können."

{{$include /help/_includes/content-design-components.md}}

### Hinzufügen von Assets

{{$include /help/_includes/content-design-assets.md}}

### Navigieren in den Ebenen, Einstellungen und Stilen

{{$include /help/_includes/content-design-navigation.md}}

### Inhalt personalisieren

{{$include /help/_includes/content-design-personalization.md}}

### Linked URL-Tracking bearbeiten

{{$include /help/_includes/content-design-links.md}}

## Fragmentdetails anzeigen

Klicken Sie auf den Namen eines beliebigen Fragments auf der Listenseite, um die Seite mit den Fragmentdetails zu öffnen. Sie können das Fragment bearbeiten, es umbenennen oder die Fragmentbeschreibung aktualisieren. Nehmen Sie Aktualisierungen vor und klicken Sie außerhalb des Namens- oder Beschreibungsfelds auf , um die Änderungen automatisch zu speichern.

>[!NOTE]
>
>Wenn ein veröffentlichtes Fragment von einer E-Mail- oder E-Mail-Vorlage verwendet wird, können Sie den Namen nicht ändern oder den Inhalt bearbeiten. Sie können eine Entwurfsversion erstellen, wenn Sie Änderungen am Fragment vornehmen möchten.

![Details für ein veröffentlichtes Fragment anzeigen](./assets/fragment-details-published.png){width="600" zoomable="yes"}

Klicken Sie auf **[!UICONTROL Fragment bearbeiten]** , um das Fragment im Visual Content Editor zu öffnen.

Beenden Sie die Ansicht jederzeit, indem Sie auf den Pfeil _Zurück_ oben links klicken, wodurch Sie zur Listenseite _Fragmente_ zurückkehren.

## Von Verweisen verwendetes Fragment anzeigen

Klicken Sie auf der Seite mit den Fragmentdetails auf die Registerkarte &quot;**[!UICONTROL Verwendet von]**&quot;, um Details dazu anzuzeigen, wo das Fragment derzeit in Journey Optimizer B2B Edition verwendet wird - für E-Mails, E-Mail-Vorlagen und Fragmente.

>[!IMPORTANT]
>
>Jedes Fragment, das aktuell von einer E-Mail- oder E-Mail-Vorlage verwendet wird, kann nicht gelöscht werden.

Verweise werden nach Kategorie angezeigt: _E-Mail_ oder _E-Mail-Vorlage_. E-Mails in Journey Optimizer B2B Edition werden in Konto-Journey eingebettet und verfasst, sodass die übergeordnete Journey der E-Mail, die das Fragment verwendet, in Verweisen angezeigt wird.

![Wird von Verweisen für das Fragment verwendet](./assets/fragment-used-by-published.png){width="600" zoomable="yes"}

Klicken Sie auf den Link, um die entsprechende E-Mail- oder E-Mail-Vorlage zu öffnen, in der das Fragment verwendet wird.

## Fragmente löschen

Jedes Fragment, das aktuell von einer E-Mail- oder E-Mail-Vorlage verwendet wird, kann nicht gelöscht werden. Überprüfen Sie daher vor dem Starten eines Fragmenterlöschens die Verweise _used-by_ . Außerdem kann eine Entfernung nicht rückgängig gemacht werden. Überprüfen Sie daher, bevor Sie eine Löschaktion starten.

Sie können ein Fragment mit einer der folgenden Methoden löschen:

* Klicken Sie in den Fragmentdetails auf der rechten Seite auf **[!UICONTROL Löschen]**.
* Klicken Sie auf der Listenseite _[!UICONTROL Fragmente]_ auf das Auslassungszeichen neben dem Fragment und wählen Sie **[!UICONTROL Löschen]**.

Durch diese Aktion wird ein Bestätigungsdialogfeld geöffnet. Sie können den Vorgang abbrechen, indem Sie auf **[!UICONTROL Abbrechen]** klicken oder auf **[!UICONTROL Löschen]** klicken, um den Löschvorgang zu bestätigen.

![Dialogfeld &quot;Fragment löschen&quot;](./assets/fragment-delete-dialog.png){width="400"}

Wenn das Fragment derzeit verwendet wird, öffnet die Aktion ein Informationsdialogfeld, das Sie darauf hinweist, dass das Fragment nicht gelöscht werden kann. Klicken Sie auf **[!UICONTROL OK]** , wodurch die Löschaktion abgebrochen wird.

![Dialogfeld &quot;Fragment löschen&quot;- Fragment in Verwendung kann nicht gelöscht werden](./assets/fragment-delete-dialog-in-use.png){width="400"}

## Bearbeiten von Fragmenten

Die Bearbeitung eines Fragments hängt vom aktuellen Status ab:

* Wenn ein Fragment den Status _Entwurf_ aufweist, können Sie alle Details und den visuellen Inhalt bearbeiten.
* Wenn ein Fragment den Status _Veröffentlicht_ aufweist, können Sie die Fragmentbeschreibung bearbeiten, nicht jedoch den Namen. Sie können den visuellen Inhalt nicht bearbeiten.
* Befindet sich ein Fragment im Status _Veröffentlicht mit Entwurf_ , ist die Bearbeitung der Details auf die Beschreibung beschränkt. Sie können auch den visuellen Inhalt für die Entwurfsversion bearbeiten.

>[!BEGINTABS]

>[!TAB Entwurf]

1. Klicken Sie auf der Listenseite _[!UICONTROL Fragmente]_ auf den Fragmentnamen, um ihn zu öffnen.

   Daraufhin wird eine Vorschau des visuellen Inhalts mit den Fragmentdetails auf der rechten Seite angezeigt.

1. Ändern Sie alle Details, z. B. den Namen und die Beschreibung.

   ![Details für Fragment mit Entwurfsstatus](./assets/fragment-draft-details.png){width="600" zoomable="yes"}

1. Um Änderungen am Inhalt im visuellen Designer vorzunehmen, klicken Sie auf **[!UICONTROL Fragment bearbeiten]**.

   Verwenden Sie die Visual Designer-Tools nach Bedarf:

   * [Hinzufügen von Struktur und Inhalt](#add-structure-and-content)
   * [Assets hinzufügen](#add-assets)
   * [Navigieren in den Ebenen, Einstellungen und Stilen](#navigate-the-layers-settings-and-styles)
   * [Inhalt personalisieren](#personalize-content)
   * [Linked URL-Tracking bearbeiten](#edit-linked-url-tracking)

   Klicken Sie auf **[!UICONTROL Speichern]** oder auf **[!UICONTROL Speichern und schließen]** , um zu den Fragmentdetails zurückzukehren.

1. Wenn das Fragment Ihre Kriterien erfüllt und zur Verwendung in einer E-Mail- oder E-Mail-Vorlage verfügbar sein soll, klicken Sie auf **[!UICONTROL Publish]**.

>[!TAB Veröffentlicht]

1. Klicken Sie auf der Listenseite _[!UICONTROL Fragmente]_ auf den Fragmentnamen, um ihn zu öffnen.

   Daraufhin wird eine Vorschau des visuellen Inhalts mit den Fragmentdetails auf der rechten Seite angezeigt.

1. Ändern Sie bei Bedarf die Beschreibung.

   Bei einem veröffentlichten Fragment können nicht alle anderen Details geändert werden.

1. Wenn Sie den Inhalt aktualisieren möchten, klicken Sie oben rechts auf **[!UICONTROL Entwurfsversion erstellen]** .

   Klicken Sie im Dialogfeld auf **[!UICONTROL OK]** , um die Entwurfsversion im Visual Designer zu öffnen. Sie können bei Bedarf die [Bildquelle](./assets-overview.md#choose-an-asset-source) ändern.

   ![Dialogfeld &quot;Entwurfsversion erstellen&quot;](./assets/fragments-create-draft-version.png){width="300"}

   Verwenden Sie die Visual Designer-Tools nach Bedarf:

   * [Hinzufügen von Struktur und Inhalt](#add-structure-and-content)
   * [Assets hinzufügen](#add-assets)
   * [Navigieren in den Ebenen, Einstellungen und Stilen](#navigate-the-layers-settings-and-styles)
   * [Inhalt personalisieren](#personalize-content)
   * [Linked URL-Tracking bearbeiten](#edit-linked-url-tracking)

   Klicken Sie auf **[!UICONTROL Speichern]** oder auf **[!UICONTROL Speichern und schließen]** , um zu den Fragmentdetails zurückzukehren.

1. Wenn der Entwurf des Fragments Ihre Kriterien erfüllt und Sie die Änderungen zur Verwendung in einer E-Mail- oder E-Mail-Vorlage verfügbar machen möchten, klicken Sie auf **[!UICONTROL Publish]**.

   Wenn Sie den Entwurf veröffentlichen, ersetzt er die aktuelle veröffentlichte Version und der Inhalt wird in den E-Mails und E-Mail-Vorlagen aktualisiert, wo er bereits verwendet wird.

>[!TAB  Veröffentlicht mit Entwurf]

Es gibt zwei Möglichkeiten, die Entwurfsversion zur Bearbeitung über die Listenseite _[!UICONTROL Fragmente]_ zu öffnen:

* Klicken Sie auf das Symbol &quot;_Mehr_&quot;(**...**) neben dem Fragmentnamen und wählen Sie &quot;**[!UICONTROL Entwurfsversion öffnen]**&quot;.

  ![Entwurfsversion öffnen](./assets/fragments-create-draft-version.png){width="300"}

* Klicken Sie auf den Fragmentnamen, um ihn zu öffnen. Klicken Sie dann oben rechts auf **[!UICONTROL Entwurfsversion öffnen]** .

  Eine Vorschau des visuellen Inhalts für die Entwurfsversion wird mit den Fragmentdetails auf der rechten Seite angezeigt.

So aktualisieren Sie den Inhalt:

1. Klicken Sie oben rechts auf **[!UICONTROL Fragment bearbeiten]** . Verwenden Sie die Visual Designer-Tools nach Bedarf:

   * [Hinzufügen von Struktur und Inhalt](#add-structure-and-content)
   * [Assets hinzufügen](#add-assets)
   * [Navigieren in den Ebenen, Einstellungen und Stilen](#navigate-the-layers-settings-and-styles)
   * [Inhalt personalisieren](#personalize-content)
   * [Linked URL-Tracking bearbeiten](#edit-linked-url-tracking)

   Klicken Sie auf **[!UICONTROL Speichern]** oder auf **[!UICONTROL Speichern und schließen]** , um zu den Fragmentdetails zurückzukehren.

1. Wenn der Entwurf des Fragments Ihre Kriterien erfüllt und Sie die Änderungen zur Verwendung in einer E-Mail- oder E-Mail-Vorlage verfügbar machen möchten, klicken Sie auf **[!UICONTROL Publish]**.

   Wenn Sie den Entwurf veröffentlichen, ersetzt er die aktuelle veröffentlichte Version und der Inhalt wird in den E-Mails und E-Mail-Vorlagen aktualisiert, wo er bereits verwendet wird.

>[!ENDTABS]

## Fragmente duplizieren

Sie können ein Fragment mit einer der folgenden Methoden duplizieren:

* Klicken Sie auf der Listenseite _[!UICONTROL Fragmente]_ auf das Symbol _Mehr_ (**...**) neben dem Fragmentnamen und wählen Sie **[!UICONTROL Duplizieren]**.
* Klicken Sie oben rechts auf der Seite mit den Fragmentdetails auf **[!UICONTROL ... Mehr]** und wählen Sie **[!UICONTROL Duplizieren]**.

![Duplizieren des Fragments](./assets/fragment-details-duplicate.png){width="600" zoomable="yes"}

Geben Sie im Dialogfeld einen nützlichen Namen (eindeutig) und eine Beschreibung ein. Klicken Sie auf **[!UICONTROL Duplizieren]** , um die Aktion abzuschließen.

![Geben Sie einen Namen und eine Beschreibung für das duplizierte Fragment ein](./assets/fragment-duplicate-dialog.png){width="400"}

Das duplizierte (neue) Fragment wird dann in der Liste _Fragmente_ angezeigt.

## Neues Fragment aus E-Mail- oder Vorlageninhalt speichern

Wenn Sie eine E-Mail- oder E-Mail-Vorlage im Visual Content Editor erstellen/bearbeiten, können Sie festlegen, dass alle oder Teile des Inhalts als Fragment gespeichert werden sollen, damit er zur Wiederverwendung verfügbar ist.

1. Wenn Sie Inhalt als Fragment speichern möchten, klicken Sie auf **[!UICONTROL Mehr]** und wählen Sie **[!UICONTROL Als Fragment speichern]**.

1. Wählen Sie die verschiedenen Elemente aus, die in das Fragment aufgenommen werden sollen.

   Wählen Sie mehrere Strukturen aus, indem Sie die Umschalt- oder die Steuerungstaste gedrückt halten.

   Sie können nur nebeneinander liegende Strukturen auswählen, in der Benutzeroberfläche ist es nicht möglich, nicht nebeneinander liegende Elemente auszuwählen.

1. Klicken Sie bei ausgewähltem Inhalt oben rechts auf **[!UICONTROL Erstellen]** .

1. Geben Sie im Dialogfeld einen nützlichen Namen und eine Beschreibung für das Fragment ein. Klicken Sie dann auf **[!UICONTROL Erstellen]**.

   Das neue Fragment wird dann auf der Listenseite _Fragmente_ angezeigt und kann auch in E-Mails und E-Mail-Vorlagen verwendet werden.

## Hinzufügen visueller Fragmente zum E-Mail- oder Vorlageninhalt

Fragmente sind zur Wiederverwendung konzipiert und können zum Authoring von E-Mail- und E-Mail-Vorlagen eingefügt werden. Sie können bis zu 30 Fragmente in einer E-Mail oder Vorlage hinzufügen. Fragmente können nur bis zu einer Ebene verschachtelt werden.

>[!BEGINTABS]

>[!TAB Fragmente zu einer E-Mail hinzufügen]

1. Navigieren Sie zu **[!UICONTROL Konto-Journey]** und öffnen Sie eine bestehende Journey oder erstellen Sie eine neue Journey.

1. Erstellen Sie einen [_[!UICONTROL E-Mail senden ]_-Knoten](./email-authoring.md#add-an-email-action-in-an-account-journey).

1. Erstellen oder bearbeiten Sie [E-Mail-Inhalt für den Knoten](./email-authoring.md#create-the-email-content).

1. Ziehen Sie ein Element aus dem Menü **[!UICONTROL Komponenten]** und legen Sie es ab, um eine _Struktur_ für das Fragment bereitzustellen.

1. Um die Liste der veröffentlichten Fragmente zu öffnen, klicken Sie auf das Symbol _Fragmente_ .

   Sie haben folgende Möglichkeiten:
   * Sortieren Sie die Liste.
   * Suchen, durchsuchen und filtern Sie die Liste.
   * Zwischen Karten- (Miniaturansicht) und Listenansichten wechseln.
   * Aktualisieren Sie die Liste, um eines der kürzlich erstellten Fragmente widerzuspiegeln.

   ![Suchen nach einem Fragment im visuellen Designer](./assets/fragments-list-designer-search.png){width="600"}

1. Ziehen Sie eines der Fragmente in den Platzhalter der Strukturkomponente.

   Der Editor rendert das Fragment innerhalb des Bereichs/Elements der E-Mail-Struktur.

Der Inhalt des Fragments wird innerhalb der Struktur dynamisch aktualisiert, um eine visuelle Darstellung des Inhalts in der E-Mail zu erhalten.

>[!TIP]
>
>Wenn das Fragment das gesamte horizontale Layout in der E-Mail einnehmen soll, fügen Sie eine Struktur mit der Spalte [!UICONTROL 1:1 column] hinzu und ziehen Sie das Fragment per Drag-and-Drop hinzu.

Nachdem die E-Mail gespeichert wurde, wird sie auf der Seite mit den Fragmentdetails angezeigt, wenn die Registerkarte _[!UICONTROL Verwendet von]_ ausgewählt ist. Zu einer E-Mail hinzugefügte Fragmente können nicht in der E-Mail oder Vorlage bearbeitet werden. Das veröffentlichte Quellfragment definiert den Inhalt.

>[!TAB Fragmente zu einer E-Mail-Vorlage hinzufügen]

1. Klicken Sie im linken Navigationsbereich auf **[!UICONTROL Content Management]** > **[!UICONTROL Vorlagen]**.

1. Erstellen Sie eine neue Vorlage oder öffnen Sie eine vorhandene E-Mail-Vorlage und klicken Sie auf **[!UICONTROL E-Mail-Vorlage bearbeiten]**.

1. Ziehen Sie ein Element aus dem Menü **[!UICONTROL Komponenten]** und legen Sie es ab, um eine _Struktur_ für das Fragment bereitzustellen.

1. Um die Fragmentliste zu öffnen, klicken Sie auf das Symbol _Fragmente_.

   Sie haben folgende Möglichkeiten:
   * Sortieren Sie die Liste.
   * Suchen, durchsuchen und filtern Sie die Liste.
   * Zwischen Karten- (Miniaturansicht) und Listenansichten wechseln.
   * Aktualisieren Sie die Liste, um eines der kürzlich erstellten Fragmente widerzuspiegeln.

   ![Suchen nach einem Fragment im visuellen Designer](./assets/fragments-list-designer-search.png){width="600"}

1. Ziehen Sie eines der Fragmente in den Platzhalter der Strukturkomponente.

   Der Editor rendert das Fragment innerhalb des Bereichs/Elements der E-Mail-Vorlagenstruktur.

1. Ziehen Sie eines der Fragmente in den Platzhalter der Strukturkomponente.

   Der Editor rendert das Fragment innerhalb des Bereichs/Elements der E-Mail-Vorlagenstruktur.

>[!TIP]
>
>Wenn das Fragment das gesamte horizontale Layout der E-Mail-Vorlage einnehmen soll, fügen Sie eine Struktur mit der Spalte _[!UICONTROL 1:1 column]_ hinzu und ziehen Sie das Fragment per Drag-and-Drop in die Vorlage.

Nach dem Speichern der E-Mail-Vorlage wird sie auf der Seite mit den Fragmentdetails angezeigt, wenn die Registerkarte _[!UICONTROL Verwendet von]_ ausgewählt wird. Zu einer E-Mail-Vorlage hinzugefügte Fragmente können nicht in der Vorlage bearbeitet werden. Das veröffentlichte Quellfragment definiert den Inhalt.

>[!ENDTABS]

## Fragmentaktionen während der E-Mail- und Vorlagenbearbeitung

Wenn ein Fragment zu einer E-Mail- oder E-Mail-Vorlage hinzugefügt wird, kann der Fragmentinhalt nicht in der E-Mail oder Vorlage bearbeitet werden. Sie können jedoch die folgenden Aktionen durchführen:

* **[!UICONTROL Löschen]** - Dadurch wird das Fragment aus dem aktuellen E-Mail- oder E-Mail-Vorlageninhalt entfernt (die Fragmentquelle ist nicht betroffen).
* **[!UICONTROL Aktualisieren]** - Mit dieser Aktion wird der Inhalt des Fragments in der aktuellen E-Mail- oder E-Mail-Vorlage aktualisiert. Die Aktualisierung ist nützlich, wenn Sie Änderungen am Fragment nach dem Hinzufügen zur E-Mail oder E-Mail-Vorlage übernehmen möchten.
* **[!UICONTROL Duplizieren]** - Mit dieser Aktion wird das Fragment innerhalb derselben E-Mail- oder E-Mail-Vorlage im Editor mit denselben Dimensionen dupliziert und direkt darunter hinzugefügt.
* **[!UICONTROL Fragment öffnen]** - Mit dieser Aktion wird eine neue Browser-Registerkarte mit der Seite des Fragment-Editors und Details geöffnet.
* **[!UICONTROL Vererbung unterbrechen]** - Diese Aktion unterbricht die Vererbung des Fragments (und seiner Änderungen) aus der Quelle. Verwenden Sie diese Aktion, um den Fragmentinhalt als unabhängigen und bearbeitbaren Inhalt in der E-Mail- oder E-Mail-Vorlage verfügbar zu machen. Durch diese Aktion wird auch die E-Mail- oder E-Mail-Vorlage aus dem Verweis _Verwendet von_ für das ursprüngliche Fragment entfernt.

Wenn Sie das Fragment auf der Editor-Seite auswählen, sind diese Aktionen in der Kontextsymbolleiste und im Eigenschaftenbedienfeld auf der rechten Seite verfügbar.

![Aktionen auf das ausgewählte Fragment anwenden](./assets/fragment-actions-email-authoring.png){width="600" zoomable="yes"}