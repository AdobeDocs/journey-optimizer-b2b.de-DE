---
title: Erstellung von E-Mail-Vorlagen
description: Erstellen Sie wiederverwendbare E-Mail-Vorlagen mit visuellen Design-Tools, benutzerdefiniertem CSS, Fragmenten und Personalisierung für Account Journey in Journey Optimizer B2B edition.
feature: Templates, Email Authoring, Content
role: User
exl-id: 2d532f93-c452-400a-8a82-e1f0eb89b199
source-git-commit: 9f8953423e3b6d578155431c7638e4fec9abf86a
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 3%

---

# Erstellung von E-Mail-Vorlagen

Nachdem Sie [E-Mail-Vorlage erstellt haben](./email-templates.md#create-an-email-template) verwenden Sie den visuellen Design-Bereich, um die Struktur- und Inhaltskomponenten in Ihrer E-Mail-Vorlage zu erstellen.

## Hinzufügen von Struktur und Inhalten {#structure-content}

{{$include /help/_includes/content-design-components.md}}

### Hinzufügen von benutzerdefiniertem CSS

Sie können Ihr eigenes benutzerdefiniertes CSS direkt im Design-Bereich der E-Mail-Vorlage hinzufügen. Verwenden Sie benutzerdefiniertes CSS, um erweiterte und spezifische Stile anzuwenden, um die Flexibilität und Kontrolle über das Erscheinungsbild Ihrer Inhalte zu erhöhen. Es empfiehlt sich, diese Formatierung auf höchster Ebene hinzuzufügen, bevor Sie Komponenten wie Bilder, Schaltflächen und Text einbeziehen.

Wählen Sie bei mindestens einer Inhaltskomponente auf der Arbeitsfläche die Komponente **[!UICONTROL Hauptteil]** in der linken Navigationsstruktur aus, um auf den benutzerdefinierten CSS-Editor zuzugreifen.

![Zugriff auf Textkörperstile](./assets/email-template-body-styles.png){width="800" zoomable="yes"}

{{$include /help/_includes/content-design-custom-css.md}}

### Hinzufügen von Fragmenten

>[!NOTE]
>
>Fragmente sind nicht kreuzkompatibel zwischen dem _Design-Modus_ und dem _manuellen Modus_ im E-Mail-Inhalt. Um ein Fragment in E-Mail-Inhalten zu verwenden, auf die ein Design angewendet wird, muss das Fragment auch im _Design-Modus_ erstellt werden.

{{$include /help/_includes/content-design-use-fragments.md}}

Nachdem die Vorlage gespeichert wurde, wird sie auf der Seite mit den Fragmentdetails angezeigt, wenn Sie die Registerkarte _[!UICONTROL Verwendet von]_ in der Zusammenfassung auswählen.

### Hinzufügen von Bild-Assets

{{$include /help/_includes/content-design-assets.md}}

### Navigieren in den Ebenen, Einstellungen und Stilen

{{$include /help/_includes/content-design-navigation.md}}

### Personalisieren von Inhalten

{{$include /help/_includes/content-design-personalization-email.md}}

### Verknüpftes URL-Tracking bearbeiten

{{$include /help/_includes/content-design-links.md}}

### Anwenden des Dunkelmodus-Stils

Verwenden Sie _Dunkler Modus_, um Ihre E-Mail-Anzeige auf ein dunkles Design in einem E-Mail-Client zu überprüfen. Ein Dunkelmodus oder Design ermöglicht es einem unterstützenden E-Mail-Client oder einer unterstützenden Mobile App, E-Mails mit dunkleren Hintergründen und helleren Farben für Text, Schaltflächen und andere visuelle Elemente anzuzeigen. Ändern Sie oben rechts auf der Design-Arbeitsfläche die Auswahl in _Dunkler Modus_ (![Symbol für den Dunkelmodus](../assets/do-not-localize/icon-content-dark-mode.svg) ). Zeigen Sie dann eine Vorschau an und definieren Sie spezifische benutzerdefinierte Einstellungen, die von unterstützenden E-Mail-Clients zur Anzeige verwendet werden, wenn deren dunkles Design aktiviert ist.

![E-Mail-Design-Arbeitsfläche mit der Auswahl für den Dunkelmodus und den im Dunkelmodus angezeigten E-Mail-Inhalten](./assets/email-color-mode-dark-selector.png){width="700" zoomable="yes"}

Weitere Informationen zu Stilen und Best Practices für den Dunkelmodus finden Sie unter [Dunkelmodus für E-Mail-Inhalte](./email-dark-mode.md).

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
* **[!UICONTROL Design ändern]** - Kehren Sie zur Seite _E-Mail gestalten_ zurück. Dort können Sie eine andere Vorlage auswählen, um den Design-Prozess neu zu starten. Sie können den Inhalt auch mit einer leeren Arbeitsfläche (_Classic-Modus_) oder mit einem [Markendesign](./brand-themes.md) (_Design-Modus_) von Grund auf gestalten.
* **[!UICONTROL HTML exportieren]** - Laden Sie den Inhalt auf der visuellen Arbeitsfläche in HTML im Format herunter, das als ZIP-Datei verpackt ist.
