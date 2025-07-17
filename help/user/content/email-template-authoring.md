---
title: Erstellen von E-Mail-Vorlagen
description: Erfahren Sie, wie Sie Inhalts-E-Mail-Vorlagen erstellen, die für Account-Journey-E-Mails verwendet werden können, um Ihre Designs einfach und effizient wiederzuverwenden.
feature: Templates, Email Authoring, Content
role: User
exl-id: 2d532f93-c452-400a-8a82-e1f0eb89b199
source-git-commit: 9b053f81e3074f03740fe1f3b69f632219ad269a
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 14%

---

# Erstellung von E-Mail-Vorlagen

Nachdem Sie [E-Mail-Vorlage erstellt haben](./email-templates.md#create-an-email-template) verwenden Sie den visuellen Design-Bereich, um die Struktur- und Inhaltskomponenten in Ihrer E-Mail-Vorlage zu erstellen.

## Hinzufügen von Struktur und Inhalten {#structure-content}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_template"
>title="Hinzufügen von Strukturkomponenten"
>abstract="Strukturkomponenten definieren das Layout der Vorlage. Ziehen Sie eine **Strukturkomponente** per Drag-and-Drop auf die Arbeitsfläche, um mit der Gestaltung Ihres Vorlageninhalts zu beginnen."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_template"
>title="Über Inhaltskomponenten"
>abstract="Inhaltskomponenten sind leere Platzhalter für Inhalte, mit denen Sie das Layout einer Vorlage erstellen können."

{{$include /help/_includes/content-design-components.md}}

### Hinzufügen von benutzerdefiniertem CSS

Sie können Ihr eigenes benutzerdefiniertes CSS direkt im Design-Bereich der E-Mail-Vorlage hinzufügen. Verwenden Sie benutzerdefiniertes CSS, um erweiterte und spezifische Stile anzuwenden, um die Flexibilität und Kontrolle über das Erscheinungsbild Ihrer Inhalte zu erhöhen. Es empfiehlt sich, diese Formatierung auf höchster Ebene hinzuzufügen, bevor Sie Komponenten wie Bilder, Schaltflächen und Text einbeziehen.

Wählen Sie bei mindestens einer Inhaltskomponente auf der Arbeitsfläche die Komponente **[!UICONTROL Hauptteil]** in der linken Navigationsstruktur aus, um auf den benutzerdefinierten CSS-Editor zuzugreifen.

![Zugriff auf Textkörperstile](./assets/email-template-body-styles.png){width="800" zoomable="yes"}

{{$include /help/_includes/content-design-custom-css.md}}

### Hinzufügen von Fragmenten

{{$include /help/_includes/content-design-use-fragments.md}}

Nachdem die Vorlage gespeichert wurde, wird sie auf der Seite mit den Fragmentdetails angezeigt, wenn Sie die Registerkarte _[!UICONTROL Verwendet von]_ in der Zusammenfassung auswählen.

### Hinzufügen von Assets

{{$include /help/_includes/content-design-assets.md}}

### Navigieren in den Ebenen, Einstellungen und Stilen

{{$include /help/_includes/content-design-navigation.md}}

### Personalisieren von Inhalten

{{$include /help/_includes/content-design-personalization-email.md}}

### Verknüpftes URL-Tracking bearbeiten

{{$include /help/_includes/content-design-links.md}}

## Optionen anzeigen

Nutzen Sie die Ansicht- und Inhaltsvalidierungsoptionen, die im visuellen Design-Bereich verfügbar sind.

* Vergrößern/Verkleinern des Inhalts in allen vordefinierten Zoom-Optionen.

* Wechseln der Anzeige von Inhalten zwischen Desktop, Mobilgerät oder Nur-Text-/Nur-Text-Ansicht.
   * Klicken Sie auf das _Auge_-Symbol für die geräteübergreifende Inhaltsvorschau.
   * Wählen Sie eines der standardmäßigen Geräte aus oder geben Sie benutzerdefinierte Dimensionen ein, um eine Vorschau des Inhalts anzuzeigen.

### Mehr Optionen

Im Menü _[!UICONTROL Mehr …]_ oben im E-Mail-Design-Bereich können Sie die folgenden Aktionen ausführen:

![Klicken Sie auf Mehr , um auf Vorlagenaktionen zuzugreifen](./assets/visual-designer-more-menu.png){width="500"}

* **[!UICONTROL Vorlage zurücksetzen]** - Klicken Sie auf diese Option, um die Arbeitsfläche des Designs zu leeren und die Inhaltserstellung neu zu starten.
* **[!UICONTROL Als Fragment speichern]** - Speichert die Vorlage ganz oder teilweise als Fragment zur Wiederverwendung in mehreren E-Mails oder E-Mail-Vorlagen. Geben Sie einen Namen und eine Beschreibung für das Fragment ein und speichern Sie es in der Liste der verfügbaren Fragmente.
* **[!UICONTROL Design ändern]** - Kehren Sie zur Seite _Vorlage_ zurück. Dort können Sie Ihre Vorlage von Grund auf neu entwerfen oder eine vorhandene Vorlage verwenden, um den Design-Prozess neu zu starten.
* **[!UICONTROL HTML exportieren]** - Laden Sie den Inhalt auf der visuellen Arbeitsfläche in HTML im Format herunter, das als ZIP-Datei verpackt ist.
