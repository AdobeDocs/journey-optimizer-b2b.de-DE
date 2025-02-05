---
title: E-Mail-Vorlagen
description: Erfahren Sie, wie Sie E-Mail-Vorlagen verwalten und erstellen, die zur einfachen und effizienten Erstellung von Account-Journey-E-Mails verwendet werden.
feature: Email Authoring, Content
exl-id: 4e146802-e3ef-4528-b581-191e28afe86f
source-git-commit: 81c2f7be29e3fdb0b279a2ec8b786e4cf68596da
workflow-type: tm+mt
source-wordcount: '1316'
ht-degree: 4%

---

# E-Mail-Vorlagen

Für einen beschleunigten und verbesserten Design-Prozess können Sie eigenständige E-Mail-Vorlagen erstellen, um benutzerdefinierte Inhalte in den Journey der Adobe Journey Optimizer B2B edition-Konten wiederzuverwenden. Mithilfe von Vorlagen können Ihre inhaltsorientierten Team-Mitglieder an E-Mail-Inhalten außerhalb von Journey arbeiten. Marketing-Strategen können diese eigenständigen Vorlagen dann in ihren Account-Journey wiederverwenden und anpassen. Beispielsweise ist ein Teammitglied nur für den Inhalt verantwortlich, es hat jedoch keinen Zugriff auf die Journey des Kontos. Sie können jedoch eine E-Mail-Vorlage erstellen, die Marketing-Experten als Ausgangspunkt für E-Mail-Nachrichten auswählen und entsprechend den Anforderungen für den Journey anpassen können.

## Zugreifen auf und Verwalten von E-Mail-Vorlagen

Um auf E-Mail-Vorlagen in Adobe Journey Optimizer B2B edition zuzugreifen, navigieren Sie zum linken Navigationsbereich und klicken Sie auf **[!UICONTROL Content-Management]** > **[!UICONTROL Vorlagen]**. Diese Aktion öffnet eine Listenseite mit allen E-Mail-Vorlagen, die in der Instanz erstellt wurden, die in einer Tabelle aufgeführt ist.

Die Tabelle wird standardmäßig nach der Spalte _[!UICONTROL Geändert]_ sortiert, wobei die zuletzt aktualisierten Vorlagen oben stehen. Klicken Sie auf den Spaltentitel, um zwischen aufsteigender und absteigender Reihenfolge zu wechseln.

Um nach einer Vorlage anhand des Namens zu suchen, geben Sie eine Textzeichenfolge in die Suchleiste ein. Klicken Sie _oben links auf_ Symbol „Filtern“, um die Liste nach Erstellungs- oder Änderungsdatum und nach Vorlagen zu filtern, die Sie erstellt oder geändert haben.

![Greifen Sie auf die E-Mail-Vorlagenbibliothek zu und filtern Sie nach Name und Datum](./assets/templates-list-search-filter.png){width="700" zoomable="yes"}

Passen Sie die Spalten an, die Sie in der Tabelle anzeigen möchten, indem Sie oben rechts auf _Tabelle anpassen_ klicken. Wählen Sie die anzuzeigenden Spalten aus und klicken Sie auf **[!UICONTROL Anwenden]**.

Aus der angezeigten Vorlagenliste können Sie die in den folgenden Abschnitten beschriebenen Aktionen durchführen.

## E-Mail-Vorlage erstellen

Sie können eine E-Mail-Vorlage auf der Seite mit der E-Mail-Vorlagenauflistung erstellen, indem **[!UICONTROL oben rechts]** Vorlage erstellen“ klicken.

1. Geben Sie im Dialogfeld einen nützlichen **[!UICONTROL (Name]** und **[!UICONTROL Beschreibung]** (optional) ein.

   ![Geben Sie die ersten Eigenschaften für die neue E-Mail-Vorlage ein](./assets/templates-create-dialog.png){width="400"}

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

Die _[!UICONTROL Design your template]_ wird geöffnet und bietet mehrere Optionen zum Erstellen der Vorlage: _[!UICONTROL Erstellen von]_, _[!UICONTROL HTML importieren]_ oder _[!UICONTROL Design-Vorlage auswählen]_.

![Wählen Sie aus, wie Sie mit dem Design Ihrer E-Mail-Vorlage beginnen möchten](./assets/templates-create-design.png){width="800" zoomable="yes"}

Nachdem Sie die Methode ausgewählt haben, mit der Sie mit dem Design Ihrer E-Mail-Vorlage beginnen möchten, verwenden Sie den visuellen Designer, um [Inhalt Ihrer E-Mail-Vorlage zu erstellen](./email-template-authoring.md).

### Von Grund auf gestalten

Verwenden Sie den visuellen Inhaltseditor, um die Struktur des E-Mail-Inhalts zu definieren. Durch das Hinzufügen und Verschieben von Strukturkomponenten mit einfachen Drag-and-Drop-Aktionen können Sie die Form des wiederverwendbaren E-Mail-Inhalts innerhalb von Sekunden entwerfen.

>[!NOTE]
>
>Die verfügbaren Design-Tools entsprechen den Tools für die [E-Mail-Erstellung](./email-authoring.md). Der Unterschied besteht darin, dass dieser Inhalt dann als Vorlage gespeichert wird, die über mehrere E-Mail-_-Knoten_ Konto-Journey hinweg wiederverwendet werden kann.

1. Wählen Sie auf _[!UICONTROL Startseite]_ Vorlage entwerfen“ die Option **[!UICONTROL Erstellen von neuen]** aus.

1. [Struktur und Inhalt hinzufügen](./email-authoring.md#add-structure-and-content) zur Vorlage hinzufügen.

### Importieren von HTML

Mit Adobe Journey Optimizer B2B edition können Sie vorhandenen HTML-Inhalt importieren, um Ihre E-Mail-Vorlagen zu entwerfen.

{{$include /help/_includes/content-design-import.md}}

![Importieren Sie HTML-Inhalte in eine ZIP-Datei](./assets/templates-import-zip-file.png){width="500"}

>[!NOTE]
>
>Einen `<table>`-Tag als erste Ebene in einer HTML-Datei zu verwenden kann zum Verlust des Stils führen, einschließlich der Einstellungen für Hintergrund und Breite im Tag der obersten Ebene.

Sie können den importierten Inhalt nach Bedarf mit dem visuellen Designer personalisieren.

### Design-Vorlage auswählen

{{$include /help/_includes/content-design-select-template.md}}

## E-Mail-Vorlagendetails anzeigen

Klicken Sie auf der Seite Vorlagenauflistung auf den Namen einer E-Mail-Vorlage, um die Seite mit den E-Mail-Vorlagendetails zu öffnen. Von hier aus können Sie grundlegende Eigenschaften für die E-Mail-Vorlage anzeigen und auf den Visual Content Editor zugreifen, um Änderungen am Vorlageninhalt vorzunehmen.

![Greifen Sie auf die E-Mail-Vorlagenbibliothek zu und filtern Sie nach Name und Datum](./assets/template-details.png){width="700" zoomable="yes"}

* Zeigen Sie die Details der E-Mail-Vorlage an, z. B. Name und Beschreibung. Diese Einstellungen können bearbeitet werden. Klicken Sie auf eine Stelle außerhalb des Beschreibungsfelds, um die Änderungen automatisch zu speichern.

* Zeigen Sie die Eigenschaften der E-Mail-Vorlage an, z. B. Erstellt von, Erstellt am, Zuletzt aktualisiert am und Geändert von.

* Klicken Sie **[!UICONTROL rechts oben]** „Mehr“, um schnell mit der E-Mail-Vorlage umzugehen, z. B _„Duplizieren_ und _Löschen_.

* Wenn aktive Warnhinweise vorhanden sind (Fehler und Warnung für die E-Mail-Vorlage), klicken Sie oben ]**auf**[!UICONTROL  Warnhinweise), um die Informationen anzuzeigen.

  Diese Warnhinweise verbieten nicht die Verwendung der E-Mail-Vorlage für die E-Mail-Erstellung. Die Informationen bieten Marketing-Fachleuten in Ihrem Team einen Überblick darüber, was möglicherweise nicht funktioniert, und über die erforderlichen Aktualisierungen, bevor sie für die Bereitstellung verwendet werden können.

## Anzeigen der von Verweisen verwendeten E-Mail-Vorlage

Klicken Sie auf der Detailseite für E **[!UICONTROL Mail-Vorlagen auf die Registerkarte]** Verwendet von“, um Details dazu anzuzeigen, wo diese E-Mail-Vorlage in E-Mails in Account-Journey verwendet wird.

![Klicken Sie auf die Registerkarte Verwendet von , um die Verwendung der Vorlage zu überprüfen](./assets/template-details-used-by.png){width="400"}

E-Mails in Journey Optimizer B2B edition sind in Journey eingebettet und verfasst, sodass die übergeordnete Journey der E-Mail, die die Vorlage verwendet, als Referenzen angezeigt wird.

* Durch Klicken auf den Link gelangen Sie zu der entsprechenden Journey-E-Mail, in der die E-Mail-Vorlage verwendet wird.

* Sie können die Ansicht jederzeit verlassen, indem Sie auf den Rückwärtspfeil klicken, der Sie zur Auflistungsseite zurückführt.

## E-Mail-Vorlagen bearbeiten

Diese Aktion kann übernommen werden aus:

* Die Detailseite - Klicken Sie auf **[!UICONTROL E-Mail-Vorlage bearbeiten]**.
* Die Auflistungsseite - Klicken Sie auf die Auslassungspunkte (**…**) neben einer E-Mail-Vorlage und wählen Sie **[!UICONTROL Bearbeiten]**.

Diese Aktion führt Sie zur Seite _Vorlage entwerfen_ oder zur Seite des visuellen Inhaltseditors (basierend auf dem zuletzt gespeicherten Status der E-Mail-Vorlage). Von hier aus können Sie den Inhalt Ihrer E-Mail-Vorlage nach Bedarf bearbeiten. Weitere [ zu den Bearbeitungsoptionen finden Sie ](#create-email-templates) „E-Mail-Vorlagen erstellen“.

## E-Mail-Vorlagen duplizieren

Sie können eine E-Mail-Vorlage mit einer der folgenden Methoden duplizieren:

* Erweitern Sie in den E-Mail-Vorlagendetails auf der rechten Seite **[!UICONTROL Mehr]** und klicken Sie auf **[!UICONTROL Duplizieren]**.

  ![Klicken Sie auf Mehr , um auf Aktionen zum Löschen und Duplizieren zuzugreifen](./assets/template-details-more-menu.png){width="400"}

* Klicken Sie auf der _E_ Mail-Vorlagen“ auf die Auslassungspunkte (…) neben der Vorlage und wählen Sie **[!UICONTROL Duplizieren]**.

Geben Sie im Dialogfeld einen nützlichen Namen (eindeutig) und eine Beschreibung ein. Klicken Sie **[!UICONTROL Duplizieren]**, um die Aktion abzuschließen.

Die duplizierte (neue) E-Mail-Vorlage wird dann in der Liste _E-Mail-Vorlagen_ angezeigt.

## E-Mail-Vorlagen löschen

Das Entfernen einer E-Mail-Vorlage kann nicht rückgängig gemacht werden. Überprüfen Sie dies, bevor Sie eine Löschaktion starten. Sie können eine E-Mail-Vorlage mit einer der folgenden Methoden löschen:

* Erweitern Sie in den Vorlagendetails auf der rechten Seite &quot;**[!UICONTROL &quot;]** klicken Sie auf **[!UICONTROL Löschen]**.
* Klicken Sie auf der _E_ Mail-Vorlagen“ auf die Auslassungspunkte (…) neben der Vorlage und wählen Sie **[!UICONTROL Löschen]**.

  ![Klicken Sie auf … , um auf Aktionen zum Duplizieren und Löschen zuzugreifen](./assets/templates-list-more-menu.png){width="500"}

Diese Aktion öffnet ein Bestätigungsdialogfeld. Sie können den Vorgang abbrechen, indem Sie auf **[!UICONTROL Abbrechen]** klicken oder auf **[!UICONTROL Löschen]** klicken, um die Entfernung zu bestätigen.

## Massenaktionen durchführen

Wählen Sie auf der Seite mit der Liste der E-Mail-Vorlagen mehrere Vorlagen gleichzeitig aus, indem Sie die Kontrollkästchen links auswählen. Ein Banner wird unten angezeigt, wenn Sie mehrere Vorlagen auswählen.

![Ein Banner zeigt die Anzahl der ausgewählten Vorlagen und das Symbol „Löschen“ an](./assets/templates-multi-select-banner.png){width="600"}

**[!UICONTROL Löschen]** - Sie können bis zu 20 Vorlagen gleichzeitig löschen. In einem Bestätigungsdialogfeld können Sie die Aktion abbrechen oder das Entfernen der Vorlagen bestätigen.

## Erstellen einer E-Mail aus einer gespeicherten Vorlage

Verwenden Sie auf dem Bildschirm _E-Mail erstellen_ den Abschnitt _Design-Vorlage auswählen_, um Ihren Inhalt aus einer Vorlage zu erstellen.

Gehen Sie wie folgt vor, um mit der Erstellung Ihres Inhalts mit einer der erstellten E-Mail-Vorlagen zu beginnen:

1. Greifen Sie über die Seite _Inhalt bearbeiten_ auf die E-Mail-Designer zu.

   Auf der _E-Mail erstellen_ ist die Registerkarte _Beispielvorlagen_ standardmäßig ausgewählt.

1. Um eine benutzerdefinierte E-Mail-Vorlage zu verwenden, wählen Sie die Registerkarte **[!UICONTROL Gespeicherte Vorlagen]** aus.

   Auf dieser Registerkarte wird eine Liste aller in der Sandbox erstellten E-Mail-Vorlagen angezeigt. Sie können sie sortieren _nach_, _Zuletzt geändert_ und _Zuletzt erstellt_.

1. Wählen Sie aus der Liste die gewünschte Vorlage aus.

   Nach der Auswahl wird eine Vorschau der Vorlage angezeigt. Im Vorschaumodus können Sie mit den Rechts- und Linkspfeilen zwischen allen Vorlagen einer Kategorie (Beispielvorlage oder gespeicherte Vorlagen, je nach Ihrer Auswahl) navigieren.

1. Klicken **[!UICONTROL oben]** auf „Diese Vorlage verwenden“.

1. Bearbeiten Sie den Inhalt nach Bedarf im visuellen Content Designer.
