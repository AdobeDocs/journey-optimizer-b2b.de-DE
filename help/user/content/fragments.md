---
title: Fragmente
description: Erfahren Sie, wie Sie visuelle Inhaltsfragmente als wiederverwendbare Komponenten für E-Mails und E-Mail-Vorlagen in Adobe Journey Optimizer B2B edition erstellen und verwenden.
feature: Content, Email Authoring
exl-id: 3c1d2ca0-d009-4a2a-9d81-1a838845b7fa
source-git-commit: 7deb914dfb9d6979b4dc4a497ed2d15bbabd3011
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
* _Fragmente wiederverwenden_ - Verwenden Sie sie so oft wie nötig in Ihren Inhalten.

## Zugreifen auf und Verwalten von Fragmenten

Um auf visuelle Fragmente in Adobe Journey Optimizer B2B edition zuzugreifen, navigieren Sie zum linken Navigationsbereich und klicken Sie auf **[!UICONTROL Content-Management]** > **[!UICONTROL Fragments]**. Diese Aktion öffnet eine Listenseite mit allen in der Instanz erstellten Fragmenten, die in einer Tabelle aufgeführt sind.

![Zugriff auf die Fragmentbibliothek](./assets/fragments-list.png){width="700" zoomable="yes"}

Die Tabelle wird nach der Spalte _[!UICONTROL Geändert]_ sortiert, wobei die zuletzt aktualisierten Fragmente standardmäßig oben stehen. Klicken Sie auf den Spaltentitel, um zwischen aufsteigender und absteigender Reihenfolge zu wechseln.

### Fragmentstatus und -lebenszyklus

Der Fragmentstatus bestimmt seine Verfügbarkeit zur Verwendung in einer E-Mail oder E-Mail-Vorlage und die Änderungen, die Sie daran vornehmen können.

| Status | Beschreibung |
| -------------------- | ----------- |
| Entwurf | Wenn Sie ein Fragment erstellen, befindet es sich im Entwurfsstatus . Dieser Status bleibt erhalten, während Sie den visuellen Inhalt definieren oder bearbeiten, bis Sie ihn zur Verwendung in einer E-Mail- oder E-Mail-Vorlage veröffentlichen. Verfügbare Aktionen:<br/><ul><li>Alle Details bearbeiten<li>In Visual Designer bearbeiten<li>Veröffentlichen<li>Doppelt<li>Löschen |
| Veröffentlicht | Wenn Sie ein Fragment veröffentlichen, wird es zur Verwendung in einer E-Mail oder E-Mail-Vorlage verfügbar. Veröffentlichte Fragmentinhalte können im visuellen Designer nicht geändert werden. Verfügbare Aktionen:<br/><ul><li>Beschreibung bearbeiten.<li>Hinzufügen zu einer E-Mail oder Vorlage<li>Entwurfsversion erstellen<li>Doppelt<li>Löschen (wenn nicht in Gebrauch) |
| Mit Entwurf veröffentlicht | Wenn Sie einen Entwurf aus einem veröffentlichten Fragment erstellen, bleibt die veröffentlichte Version zur Verwendung in einer E-Mail- oder E-Mail-Vorlage verfügbar und der Entwurfsinhalt kann im visuellen Designer geändert werden. Wenn Sie die Entwurfsversion veröffentlichen, ersetzt sie die aktuelle veröffentlichte Version, und der Inhalt wird in den E-Mails und E-Mail-Vorlagen, in denen sie verwendet wird, aktualisiert. Verfügbare Aktionen:<br/><ul><li>Beschreibung bearbeiten.<li>Hinzufügen zu einer E-Mail oder Vorlage<li>Bearbeiten der Entwurfsversion in Visual Designer<li>Entwurfsversion veröffentlichen<li>Doppelt<li>Löschen (wenn nicht in Gebrauch) |

![Lebenszyklus des Fragmentstatus](./assets/status-lifecycle-diagram.png){zoomable="yes"}

>[!IMPORTANT]
>
>Der Fragmentstatus wurde mit der Journey Optimizer B2B edition-Version vom August eingeführt. Alle Fragmente, die vor dieser Version erstellt wurden _haben den Status „Entwurf_, auch wenn sie in einer E-Mail oder Vorlage verwendet werden. Wenn Sie Änderungen an diesen Fragmenten vornehmen, müssen Sie das Fragment veröffentlichen, um die Änderungen weiterzugeben.

### Filtern der Fragmentliste

Um nach einem Fragment anhand des Namens zu suchen, geben Sie eine Textzeichenfolge in die Suchleiste für eine Übereinstimmung ein. Klicken Sie auf _Filter_-Symbol ( ![Filtersymbol ein- oder ausblenden](../assets/do-not-localize/icon-filter.svg) ), um die verfügbaren Filteroptionen anzuzeigen und die Einstellungen zu ändern, um die angezeigten Elemente entsprechend Ihren angegebenen Kriterien zu filtern.

![Filtern Sie die angezeigten Fragmente](./assets/fragments-list-filtered.png){width="700" zoomable="yes"}

### Spaltenanzeige anpassen

Passen Sie die Spalten an, die Sie in der Tabelle anzeigen möchten, indem Sie oben rechts auf _Tabelle anpassen_ (![Symbol „Tabelle ](../assets/do-not-localize/icon-column-settings.svg)„) klicken.

Wählen Sie im Dialogfeld die anzuzeigenden Spalten aus und klicken Sie auf **[!UICONTROL Anwenden]**.

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
   * [Inhalt personalisieren](./fragment-authoring.md#personalize-content)
   * [Benutzerdefinierte Felder aktivieren](./fragment-authoring.md#enable-custom-fields)
   * [Verknüpftes URL-Tracking bearbeiten](./fragment-authoring.md#edit-linked-url-tracking)

1. Klicken Sie **[!UICONTROL auf &quot;]**&quot;, um das Entwurfsfragment zu speichern.

1. Wenn Sie bereit sind, das Fragment für die Verwendung in einer E-Mail- oder E-Mail-Vorlage verfügbar zu machen, klicken Sie auf **[!UICONTROL Veröffentlichen]**.

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

![Dialogfeld „Fragment löschen“ - In Verwendung befindliches Fragment kann nicht gelöscht werden](./assets/fragment-delete-dialog-in-use.png){width="400"}

## Bearbeiten von Fragmenten

Änderungen an einem Fragment hängen vom aktuellen Status ab:

* Wenn sich ein Fragment im _Entwurf_-Status befindet, können Sie alle zugehörigen Details und den visuellen Inhalt bearbeiten.
* Wenn sich ein Fragment im Status _Veröffentlicht_ befindet, können Sie die Fragmentbeschreibung bearbeiten, jedoch nicht den Namen. Visuelle Inhalte können nicht bearbeitet werden.
* Wenn sich ein Fragment im Status _Veröffentlicht mit Entwurf_ befindet, ist die Bearbeitung der Details auf die Beschreibung beschränkt. Sie können auch den visuellen Inhalt für die Entwurfsversion bearbeiten.

>[!BEGINTABS]

>[!TAB Entwurf]

1. Klicken Sie auf _[!UICONTROL Listenseite]_ Fragmente“ auf den Fragmentnamen, um das Fragment zu öffnen.

   Eine Vorschau des visuellen Inhalts wird mit den Fragmentdetails auf der rechten Seite angezeigt.

1. Ändern Sie alle Details, z. B. Namen und Beschreibung.

   ![Details für Fragment mit Entwurfsstatus](./assets/fragment-draft-details.png){width="600" zoomable="yes"}

1. Um Änderungen am Inhalt im visuellen Designer vorzunehmen, klicken Sie auf **[!UICONTROL Fragment bearbeiten]**.

   Verwenden Sie nach Bedarf die visuellen Designer-Tools:

   * [Hinzufügen von Struktur und Inhalten](./fragment-authoring.md#add-structure-and-content)
   * [Assets hinzufügen](./fragment-authoring.md#add-assets)
   * [Navigieren in den Ebenen, Einstellungen und Stilen](./fragment-authoring.md#navigate-the-layers-settings-and-styles)
   * [Inhalt personalisieren](./fragment-authoring.md#personalize-content)
   * [Benutzerdefinierte Felder aktivieren](./fragment-authoring.md#enable-custom-fields)
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
   * [Assets hinzufügen](./fragment-authoring.md#add-assets)
   * [Navigieren in den Ebenen, Einstellungen und Stilen](./fragment-authoring.md#navigate-the-layers-settings-and-styles)
   * [Inhalt personalisieren](./fragment-authoring.md#personalize-content)
   * [Benutzerdefinierte Felder aktivieren](./fragment-authoring.md#enable-custom-fields)
   * [Verknüpftes URL-Tracking bearbeiten](./fragment-authoring.md#edit-linked-url-tracking)

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
   * [Assets hinzufügen](./fragment-authoring.md#add-assets)
   * [Navigieren in den Ebenen, Einstellungen und Stilen](./fragment-authoring.md#navigate-the-layers-settings-and-styles)
   * [Inhalt personalisieren](./fragment-authoring.md#personalize-content)
   * [Benutzerdefinierte Felder aktivieren](./fragment-authoring.md#enable-custom-fields)
   * [Verknüpftes URL-Tracking bearbeiten](./fragment-authoring.md#edit-linked-url-tracking)

   Klicken Sie **[!UICONTROL Speichern]** oder **[!UICONTROL Speichern und schließen]** um zu den Fragmentdetails zurückzukehren.

1. Wenn das Entwurfsfragment Ihren Kriterien entspricht und Sie die Änderungen zur Verwendung in einer E-Mail oder E-Mail-Vorlage bereitstellen möchten, klicken Sie auf **[!UICONTROL Veröffentlichen]**.

   Wenn Sie die Entwurfsversion veröffentlichen, ersetzt sie die aktuelle veröffentlichte Version, und der Inhalt wird in den E-Mails und E-Mail-Vorlagen aktualisiert, in denen sie bereits verwendet wird.

>[!ENDTABS]

## Fragmente duplizieren

Sie können ein Fragment mit einer der folgenden Methoden duplizieren:

* Klicken Sie auf _[!UICONTROL Listenseite]_ Fragmente“ auf das Symbol _Mehr_ (**…**) neben dem Fragmentnamen und wählen Sie **[!UICONTROL Duplizieren]**.
* Klicken Sie oben rechts auf der Seite mit den Fragmentdetails auf **[!UICONTROL … Mehr]** und wählen Sie **[!UICONTROL Duplizieren]**.

![Duplizieren Sie das Fragment](./assets/fragment-details-duplicate.png){width="600" zoomable="yes"}

Geben Sie im Dialogfeld einen nützlichen Namen (eindeutig) und eine Beschreibung ein. Klicken Sie **[!UICONTROL Duplizieren]**, um die Aktion abzuschließen.

![Geben Sie einen Namen und eine Beschreibung für das duplizierte Fragment ein](./assets/fragment-duplicate-dialog.png){width="400"}

Das duplizierte (neue) Fragment wird dann in der Liste _Fragmente_ angezeigt.

## Speichern eines neuen Fragments aus E-Mail- oder Vorlageninhalten

Wenn Sie eine E-Mail- oder E-Mail-Vorlage im visuellen Inhaltseditor erstellen/bearbeiten, können Sie den gesamten Inhalt oder Teile davon als Fragment speichern, damit er wiederverwendet werden kann.

1. Wenn Sie Inhalte haben, die als Fragment gespeichert werden sollen, klicken Sie auf **[!UICONTROL Mehr]** und wählen Sie **[!UICONTROL Als Fragment speichern]**.

1. Wählen Sie die verschiedenen Elemente aus, die in das Fragment aufgenommen werden sollen.

   Wählen Sie mehrere Strukturen aus, indem Sie die Umschalt- oder die Strg-Taste gedrückt halten.

   Sie können nur nebeneinanderliegende Strukturen auswählen, und die Schnittstelle erlaubt es Ihnen nicht, nicht benachbarte Elemente auszuwählen.

1. Klicken Sie bei ausgewähltem Inhalt oben **[!UICONTROL auf]** Erstellen“.

1. Geben Sie im Dialogfeld einen nützlichen Namen und eine Beschreibung für das Fragment ein. Klicken Sie dann auf **[!UICONTROL Erstellen]**.

   Das neue Fragment wird dann auf der Seite _Fragmente_ angezeigt und ist auch für die Verwendung in E-Mails und E-Mail-Vorlagen verfügbar.

## Hinzufügen visueller Fragmente zu E-Mail- oder Vorlageninhalten

Fragmente sind zur Wiederverwendung konzipiert und können für die Erstellung von E-Mail-Vorlagen und E-Mail-Vorlagen eingefügt werden. Sie können einer E-Mail oder Vorlage bis zu 30 Fragmente hinzufügen. Fragmente können nur bis zu einer Ebene verschachtelt werden.

>[!BEGINTABS]

>[!TAB Hinzufügen von Fragmenten zu einer E-Mail]

1. Navigieren Sie zu **[!UICONTROL Account-Journey]** und öffnen Sie eine bestehende Journey oder erstellen Sie eine neue Journey.

1. Erstellen Sie einen [_[!UICONTROL E-Mail senden ]_-Knoten](./email-authoring.md#add-an-email-action-in-an-account-journey).

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

   Der Editor rendert das Fragment innerhalb des Abschnitts/Elements der E-Mail-Struktur.

Der Inhalt des Fragments wird innerhalb der Struktur dynamisch aktualisiert, um eine visuelle Darstellung des Inhalts in der E-Mail zu rendern.

>[!TIP]
>
>Wenn Sie möchten, dass das Fragment das gesamte horizontale Layout in der E-Mail einnimmt, fügen Sie eine [!UICONTROL 1:1-] hinzu und ziehen Sie das Fragment dann per Drag-and-Drop hinein.

Nachdem die E-Mail gespeichert wurde, wird sie auf der Seite mit den Fragmentdetails angezeigt, wenn die Registerkarte _[!UICONTROL Verwendet von]_ ausgewählt ist. Fragmente, die einer E-Mail hinzugefügt wurden, können innerhalb der E-Mail oder Vorlage nicht bearbeitet werden — das veröffentlichte Quellfragment definiert den Inhalt.

>[!TAB Hinzufügen von Fragmenten zu einer E-Mail-Vorlage]

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

1. Ziehen Sie eines der Fragmente in den Platzhalter der Strukturkomponente.

   Der Editor rendert das Fragment innerhalb des Abschnitts/Elements der E-Mail-Vorlagenstruktur.

>[!TIP]
>
>Wenn das Fragment das gesamte horizontale Layout in der E-Mail-Vorlage einnehmen soll, fügen Sie eine _[!UICONTROL 1:1-]_ hinzu und ziehen Sie das Fragment dann per Drag-and-Drop hinein.

Nachdem die E-Mail-Vorlage gespeichert wurde, wird sie auf der Seite mit Fragmentdetails angezeigt, wenn die Registerkarte _[!UICONTROL Verwendet von]_ ausgewählt ist. Fragmente, die einer E-Mail-Vorlage hinzugefügt wurden, können innerhalb der Vorlage nicht bearbeitet werden — das veröffentlichte Quellfragment definiert den Inhalt.

>[!ENDTABS]

## Fragmentaktionen beim Verfassen von E-Mails und Vorlagen

Wenn ein Fragment zu einer E-Mail oder E-Mail-Vorlage hinzugefügt wird, kann der Fragmentinhalt nicht innerhalb der E-Mail oder Vorlage bearbeitet werden. Sie können jedoch die folgenden Aktionen anwenden:

* **[!UICONTROL Löschen]** - Mit dieser Aktion wird das Fragment aus dem aktuellen Inhalt der E-Mail oder E-Mail-Vorlage entfernt (die Fragmentquelle ist nicht betroffen).
* **[!UICONTROL Aktualisieren]** - Mit dieser Aktion wird der Inhalt des Fragments in der aktuellen E-Mail- oder E-Mail-Vorlage aktualisiert. Eine Aktualisierung ist nützlich, wenn Sie die letzten Änderungen am Fragment nach dem Hinzufügen zur E-Mail- oder E-Mail-Vorlage berücksichtigen möchten.
* **[!UICONTROL Duplizieren]** - Mit dieser Aktion wird das Fragment innerhalb derselben E-Mail- oder E-Mail-Vorlage im Editor mit denselben Dimensionen dupliziert und direkt darunter hinzugefügt.
* **[!UICONTROL Fragment öffnen]** - Diese Aktion öffnet eine neue Browser-Registerkarte mit der Fragment-Editor-Seite und Details.
* **[!UICONTROL Vererbung unterbrechen]** - Mit dieser Aktion wird die Vererbung des Fragments (und seiner Änderungen) von der Quelle unterbrochen. Verwenden Sie diese Aktion, um den Fragmentinhalt als unabhängigen und bearbeitbaren Inhalt in der E-Mail- oder E-Mail-Vorlage verfügbar zu machen. Diese Aktion entfernt auch die E-Mail- oder E-Mail-Vorlage aus der Referenz _Verwendet von_ für das ursprüngliche Fragment.

Wenn Sie das Fragment auf der Editor-Seite auswählen, sind diese Aktionen in der Kontextsymbolleiste und im Bedienfeld Eigenschaften auf der rechten Seite verfügbar.

![Aktionen auf das ausgewählte Fragment anwenden](./assets/fragment-actions-email-authoring.png){width="600" zoomable="yes"}
