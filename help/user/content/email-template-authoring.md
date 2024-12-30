---
title: Erstellen von E-Mail-Vorlagen
description: Erfahren Sie, wie Sie Inhalts-E-Mail-Vorlagen erstellen, die für Account-Journey-E-Mails verwendet werden können, um Ihre Designs einfach und effizient wiederzuverwenden.
feature: Email Authoring, Content
exl-id: 2d532f93-c452-400a-8a82-e1f0eb89b199
source-git-commit: 82c4d9f1a46076d4dfad2ac46fca23c11ef8b4a6
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 11%

---

# Erstellen von E-Mail-Vorlagen

Nachdem Sie [E-Mail-Vorlage erstellt haben](./email-templates.md#create-an-email-template) verwenden Sie den visuellen Designer, um die Struktur- und Inhaltskomponenten in Ihrer E-Mail-Vorlage zu erstellen.

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

### Hinzufügen von Fragmenten

Im visuellen Inhaltseditor wird das Symbol _Fragmente_ auf der linken Seite angezeigt. Im folgenden Beispiel werden die Schritte zum Hinzufügen von Fragmenten zum Vorlageninhalt beschrieben.

1. Um die Fragmentliste zu öffnen, wählen Sie das Symbol _Fragmente_ aus (![Fragmentsymbol](../assets/do-not-localize/icon-fragments.svg) ).

   Sie haben folgende Möglichkeiten:

   * Sortieren Sie die Liste.
   * Durchsuchen, Suchen oder Filtern der Liste.
   * Wechseln zwischen Miniatur- und Listenansicht.
   * Aktualisieren Sie die Liste, um die kürzlich erstellten Fragmente anzuzeigen.

   ![Wählen Sie ein Fragment aus der Liste aus](./assets/visual-designer-fragments.png){width="700" zoomable="yes"}

1. Ziehen Sie eines der Fragmente per Drag-and-Drop in den Platzhalter der Strukturkomponente .

   Der Editor rendert das Fragment innerhalb des Abschnitts/Elements der E-Mail-Struktur.

Der Inhalt des Fragments wird innerhalb der Struktur dynamisch aktualisiert, um anzuzeigen, wie der Inhalt in der E-Mail angezeigt wird.

>[!TIP]
>
>Wenn das Fragment das gesamte horizontale Layout in der E-Mail einnehmen soll, fügen Sie eine 1:1-Spaltenstruktur hinzu und ziehen Sie das Fragment dann per Drag-and-Drop hinein.

Nachdem die E-Mail gespeichert wurde, wird sie auf der Seite mit den Fragmentdetails angezeigt, wenn Sie die Registerkarte _[!UICONTROL Verwendet von]_ in der Zusammenfassung auswählen. Fragmente, die einer E-Mail-Vorlage hinzugefügt wurden, können innerhalb der Vorlage nicht bearbeitet werden — das Quellfragment definiert den Inhalt.

### Hinzufügen von Assets

{{$include /help/_includes/content-design-assets.md}}

### Navigieren in den Ebenen, Einstellungen und Stilen

{{$include /help/_includes/content-design-navigation.md}}

### Inhalt personalisieren

{{$include /help/_includes/content-design-personalization.md}}

### Verknüpftes URL-Tracking bearbeiten

{{$include /help/_includes/content-design-links.md}}

## Optionen anzeigen

Nutzen Sie die Ansicht- und Inhaltsvalidierungsoptionen, die im visuellen Designer verfügbar sind.

* Vergrößern/Verkleinern des Inhalts in allen vordefinierten Zoom-Optionen.

* Wechseln der Anzeige von Inhalten zwischen Desktop, Mobilgerät oder Nur-Text-/Nur-Text-Ansicht.
   * Klicken Sie auf das _Auge_-Symbol für die geräteübergreifende Inhaltsvorschau.
   * Wählen Sie eines der standardmäßigen Geräte aus oder geben Sie benutzerdefinierte Dimensionen ein, um eine Vorschau des Inhalts anzuzeigen.

### Mehr Optionen

Im Menü _[!UICONTROL Mehr …]_ oben in Email Designer können Sie die folgenden Aktionen ausführen:

![Klicken Sie auf Mehr , um auf Vorlagenaktionen zuzugreifen](./assets/visual-designer-more-menu.png){width="500"}

* **[!UICONTROL Vorlage zurücksetzen]** - Klicken Sie auf diese Option, um die Arbeitsfläche des visuellen Designers zu leeren und die Inhaltserstellung neu zu starten.
* **[!UICONTROL Als Fragment speichern]** - Speichert die Vorlage ganz oder teilweise als Fragment zur Wiederverwendung in mehreren E-Mails oder E-Mail-Vorlagen. Geben Sie einen Namen und eine Beschreibung für das Fragment ein und speichern Sie es in der Liste der verfügbaren Fragmente.
* **[!UICONTROL Design ändern]** - Kehren Sie zur Seite _Vorlage_ zurück. Dort können Sie Ihre Vorlage von Grund auf neu entwerfen oder eine vorhandene Vorlage verwenden, um den Design-Prozess neu zu starten.
* **[!UICONTROL HTML exportieren]** - Laden Sie den Inhalt auf der visuellen Arbeitsfläche auf Ihr lokales System im HTML-Format herunter, das als ZIP-Datei verpackt ist.
