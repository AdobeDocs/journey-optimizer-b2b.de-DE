---
title: Authoring von E-Mail-Vorlagen
description: Erfahren Sie, wie Sie E-Mail-Vorlagen für Content-Journey-E-Mails erstellen, die für Konto-E-Mails verwendet werden können, um Ihre Designs einfach und effizient wiederzuverwenden.
feature: Email Authoring, Content
source-git-commit: 8315c760e573aa36819652798a400206e6268ccc
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 11%

---

# Authoring von E-Mail-Vorlagen

Nachdem Sie [eine E-Mail-Vorlage erstellt haben](./email-templates.md#create-an-email-template), verwenden Sie den visuellen Designer, um die Struktur- und Inhaltskomponenten in Ihrer E-Mail-Vorlage zu erstellen.

## Hinzufügen von Struktur und Inhalt {#structure-content}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_template"
>title="Hinzufügen von Strukturkomponenten"
>abstract="Strukturkomponenten definieren das Layout der Vorlage. Ziehen Sie eine **Strukturkomponente** per Drag-and-Drop auf die Arbeitsfläche, um mit der Gestaltung Ihres Vorlageninhalts zu beginnen."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_template"
>title="Über Inhaltskomponenten"
>abstract="Inhaltskomponenten sind leere Platzhalter für Inhalte, mit denen Sie das Layout einer Vorlage erstellen können."

{{$include /help/_includes/content-design-components.md}}

### Fragmente hinzufügen

Im visuellen Inhaltseditor wird links das Symbol _Fragmente_ angezeigt. Im folgenden Beispiel werden die Schritte zum Hinzufügen von Fragmenten zum Vorlageninhalt beschrieben.

1. Um die Fragmentliste zu öffnen, wählen Sie das Symbol _Fragmente_ ( ![Fragmentsymbol](../assets/do-not-localize/icon-fragments.svg) ).

   Sie haben folgende Möglichkeiten:

   * Sortieren Sie die Liste.
   * Suchen, Suchen oder Filtern Sie die Liste.
   * Zwischen Miniatur- und Listenansichten wechseln.
   * Aktualisieren Sie die Liste, um eines der kürzlich erstellten Fragmente widerzuspiegeln.

   ![Wählen Sie ein Fragment aus der Liste aus](./assets/visual-designer-fragments.png){width="700" zoomable="yes"}

1. Ziehen Sie eines der Fragmente in den Platzhalter für die Strukturkomponente.

   Der Editor rendert das Fragment innerhalb des Bereichs/Elements der E-Mail-Struktur.

Der Inhalt des Fragments wird innerhalb der Struktur dynamisch aktualisiert, um anzuzeigen, wie der Inhalt in der E-Mail angezeigt wird.

>[!TIP]
>
>Wenn das Fragment das gesamte horizontale Layout in der E-Mail einnehmen soll, fügen Sie eine 1:1-Spaltenstruktur hinzu und ziehen Sie das Fragment per Drag-and-Drop in die E-Mail.

Nachdem die E-Mail gespeichert wurde, wird sie auf der Seite mit den Fragmentdetails angezeigt, wenn Sie in der Zusammenfassung die Registerkarte _[!UICONTROL Verwendet von]_ auswählen. Zu einer E-Mail-Vorlage hinzugefügte Fragmente können nicht in der Vorlage bearbeitet werden. Das Quellfragment definiert den Inhalt.

### Hinzufügen von Assets

{{$include /help/_includes/content-design-assets.md}}

### Navigieren in den Ebenen, Einstellungen und Stilen

{{$include /help/_includes/content-design-navigation.md}}

### Inhalt personalisieren

{{$include /help/_includes/content-design-personalization.md}}

### Linked URL-Tracking bearbeiten

{{$include /help/_includes/content-design-links.md}}

## Anzeigeoptionen

Nutzen Sie die im visuellen Designer verfügbaren Ansicht- und Inhaltsvalidierungsoptionen.

* Vergrößern/Verkleinern Sie den Inhalt über vordefinierte Zoom-Optionen.

* Wechseln Sie zwischen der Anzeige des Inhalts über Desktop, Mobilgeräte oder Nur-Text/Nur-Text.
   * Klicken Sie auf das Symbol _Auge_ für die geräteübergreifende Inhaltsvorschau.
   * Wählen Sie eines der nativen Geräte aus oder geben Sie benutzerdefinierte Dimensionen ein, um die Vorschau des Inhalts anzuzeigen.

### Mehr Optionen

Im Menü _[!UICONTROL Mehr ...]_ oben im E-Mail-Designer können Sie die folgenden Aktionen ausführen:

![Klicken Sie auf Mehr , um auf Vorlagenaktionen zuzugreifen](./assets/visual-designer-more-menu.png){width="500"}

* **[!UICONTROL Vorlage zurücksetzen]** - Klicken Sie auf diese Option, um die Arbeitsfläche des visuellen Designers zu leeren Arbeitsbereich zu leeren Arbeitsbereich zu leeren Arbeitsbereich zu löschen und die Erstellung von Inhalten neu zu starten.
* **[!UICONTROL Als Fragment speichern]** - Speichern Sie alle oder Teile der Vorlage als Fragment, das über mehrere E-Mails oder E-Mail-Vorlagen hinweg wiederverwendet werden soll. Geben Sie einen Namen und eine Beschreibung für das Fragment ein und speichern Sie es in der Liste der verfügbaren Fragmente.
* **[!UICONTROL Ändern Sie Ihren Entwurf]** - Kehren Sie zur Seite _Design Ihrer Vorlage_ zurück. Dort können Sie auswählen, ob Sie Ihre Vorlage von Grund auf neu erstellen oder eine vorhandene Vorlage verwenden möchten, um den Designprozess neu zu starten.
* **[!UICONTROL HTML exportieren]** - Laden Sie den Inhalt der visuellen Arbeitsfläche in das lokale HTML-Format herunter, das als ZIP-Datei gepackt ist.
