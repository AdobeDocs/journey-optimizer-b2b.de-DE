---
title: Verfassen von E-Mail-Nachrichten
description: Erfahren Sie, wie Sie E-Mail-Inhalte in Adobe Journey Optimizer B2B erstellen. Verwenden Sie Vorlagen, HTML-Importe und KI-gestützte Tools, um Ihre E-Mail-Kommunikation zu personalisieren und zu optimieren.
feature: Email Authoring, Content Design Tools
role: User
exl-id: 0f4ae644-ade7-49a0-935c-7f4779c25ffb
source-git-commit: db7be2c76039096a743efca11f528815a0e2a7f7
workflow-type: tm+mt
source-wordcount: '927'
ht-degree: 19%

---

# Verfassen von E-Mail-Nachrichten

Nachdem Sie [ein neues<!-- or duplicated --> E-Mail-Asset zu einem Journey-Aktionsknoten hinzugefügt haben](./add-email.md) können Sie den Inhalt für die E-Mail-Nachricht definieren.

Klicken Sie **[!UICONTROL der Registerkarte]** Details _[!UICONTROL im rechten Bedienfeld auf]_ E-Mail-Inhalt bearbeiten“.

![Klicken Sie auf E-Mail-Inhalt bearbeiten ](./assets/add-email-content.png){width="700" zoomable="yes"}

Diese Aktion startet die E-Mail-Design-Tools, in denen Sie aus den folgenden Optionen auswählen können, wie Sie Ihre E-Mail gestalten möchten:

* [Erstellen Sie Ihre E-Mail von Grund auf ](#design-your-email-from-scratch) mithilfe der Benutzeroberfläche von E-Mail-Designer.

* [Importieren Sie vorhandene HTML-Inhalte](#import-existing-html-content) aus einer Datei oder einem ZIP-Ordner.

* [Wählen Sie eine vorhandene ](#select-a-template) aus einer Liste integrierter oder benutzerdefinierter E-Mail-Vorlagen aus.

Nachdem Sie den E-Mail-Inhalt erstellt und personalisiert haben, können Sie den Inhalt zur Validierung oder zur späteren Verwendung exportieren. Klicken Sie **[!UICONTROL HTML exportieren]**, um den Inhalt als ZIP-Datei zu speichern, die Ihre HTML und Assets enthält.

>[!TIP]
>
>Verwenden Sie den KI-Assistenten in Adobe Journey Optimizer B2B edition, der auf generativer KI basiert, um Ihre Inhalte auf die nächste Ebene zu heben. Der KI-Assistent kann Ihnen dabei helfen, die Wirkung Ihrer Sendungen zu optimieren, indem er ganze E-Mails und zielgerichtete Textinhalte generiert und KI-Assistenten-Empfehlungen für Bilder abgibt, die bei Ihrer Audience Anklang finden. [Weitere Informationen](./ai-assistant-emails.md)

## Gestalten Ihrer E-Mail von Grund auf neu {#design-from-scratch}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_landing_page"
>title="Hinzufügen von Strukturkomponenten"
>abstract="Strukturkomponenten definieren das Layout der Landingpage. Ziehen Sie eine **Struktur**-Komponente per Drag-and-Drop auf die Arbeitsfläche, um mit der Gestaltung Ihres Landingpage-Inhalts zu beginnen."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_landing_page"
>title="Über Inhaltskomponenten"
>abstract="Inhaltskomponenten sind leere Platzhalter für Inhalte, mit denen Sie das Layout einer Landingpage erstellen können."

Verwenden Sie den visuellen Inhaltsdesignbereich, um die Struktur und den Inhalt der E-Mail zu definieren. Durch das Hinzufügen und Verschieben von Strukturkomponenten mit einfachen Drag-and-Drop-Aktionen können Sie die Form des wiederverwendbaren E-Mail-Inhalts innerhalb von Sekunden entwerfen.

1. Wählen Sie auf _[!UICONTROL Startseite]_ Vorlage entwerfen“ die Option **[!UICONTROL Erstellen von neuen]** aus.
1. [Struktur und Inhalt hinzufügen](#add-structure-and-content) zur E-Mail-Nachricht.
1. [Hinzufügen von Bild-](#add-assets)) zur E-Mail-Nachricht.
1. [Personalisieren des E-Mail-Inhalts](#personalize-content).
1. [Links überprüfen und ](#preview-and-edit-linked-urls).
1. [Testen Sie die E-Mail](#check-and-test-the-email).

<!-- If needed, you can further personalize your email by clicking **[!UICONTROL Switch to code editor]** from the advanced menu. The code editor allows you to edit the email source code, such as adding tracking or custom HTML tags.

>[!CAUTION]
>
>You cannot revert back to the visual designer for this email after switching to the code editor. -->

Wenn Sie mit dem Inhalt zufrieden sind, klicken Sie auf **[!UICONTROL Speichern]**.

## Vorhandenen HTML-Inhalt importieren

{{$include /help/_includes/content-design-import.md}}

![Importieren Sie HTML-Inhalte in eine ZIP-Datei](./assets/email-import-zip-file.png){width="500"}

>[!NOTE]
>
>Einen `<table>`-Tag als erste Ebene in einer HTML-Datei zu verwenden kann zum Verlust des Stils führen, einschließlich der Einstellungen für Hintergrund und Breite im Tag der obersten Ebene.

Sie können den importierten Inhalt nach Bedarf mit den visuellen E-Mail-Editor-Tools personalisieren.

## Vorlage auswählen

{{$include /help/_includes/content-design-select-template.md}}

>[!NOTE]
>
> Auf gespeicherte Vorlagen können Governance-Einstellungen (Inhaltssperrung) für eine oder mehrere Komponenten angewendet werden. Der visuelle Designer bietet Richtlinien zu gesperrten Komponenten, wenn Sie [E-Mail aus einer verwalteten Vorlage erstellen](./email-authoring-governance.md).

## Hinzufügen von Struktur und Inhalten {#structure-content}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_email"
>title="Hinzufügen von Strukturkomponenten"
>abstract="Strukturkomponenten definieren das Layout der E-Mail. Ziehen Sie eine **Struktur**-Komponente per Drag-and-Drop auf die Arbeitsfläche, um mit der Gestaltung Ihres E-Mail-Inhalts zu beginnen."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_email"
>title="Über Inhaltskomponenten"
>abstract="Inhaltskomponenten sind leere Platzhalter für Inhalt, die Sie zum Erstellen des E-Mail-Layouts verwenden können."

{{$include /help/_includes/content-design-components.md}}

### Hinzufügen von Fragmenten

{{$include /help/_includes/content-design-use-fragments.md}}

Nachdem die E-Mail gespeichert wurde, wird sie auf der Seite mit den Fragmentdetails angezeigt, wenn Sie die Registerkarte _[!UICONTROL Verwendet von]_ in der Zusammenfassung auswählen.

### Hinzufügen von Assets

{{$include /help/_includes/content-design-assets.md}}

### Navigieren in den Ebenen, Einstellungen und Stilen

{{$include /help/_includes/content-design-navigation.md}}

### Personalisieren von Inhalten

{{$include /help/_includes/content-design-personalization-email.md}}

>[!NOTE]
>
>Wenn _[!UICONTROL Meine Token]_ für die Konto-Journey definiert sind, können Sie diese Journey-spezifischen Token auch für Ihren E-Mail-Inhalt verwenden. Weitere Informationen finden [ unter „Benutzerdefinierte Token ](./personalization-my-tokens.md) E-Mail-Personalisierung“.

### Verknüpftes URL-Tracking bearbeiten

{{$include /help/_includes/content-design-links.md}}

### Optionen anzeigen

Nutzen Sie die Ansicht- und Inhaltsvalidierungsoptionen, die im visuellen E-Mail-Editor verfügbar sind.

* Vergrößern/Verkleinern des Inhalts in allen vordefinierten Zoom-Optionen.

* Wechseln der Anzeige von Inhalten zwischen Desktop, Mobilgerät oder Nur-Text-/Nur-Text-Ansicht.
   * Klicken Sie auf das _Anzeigen_-Symbol für die geräteübergreifende Inhaltsvorschau.
   * Wählen Sie eines der standardmäßigen Geräte aus oder geben Sie benutzerdefinierte Dimensionen ein, um eine Vorschau des Inhalts anzuzeigen.

## Mehr Optionen

Im Menü _[!UICONTROL Mehr …]_ oben im E-Mail-Design-Bereich können Sie die folgenden Aktionen ausführen:

![Klicken Sie auf Mehr , um auf Vorlagenaktionen zuzugreifen](./assets/email-designer-more-menu.png){width="500"}

* **[!UICONTROL E-Mail zurücksetzen]** - Klicken Sie auf diese Option, um die visuelle E-Mail-Designer-Arbeitsfläche zu löschen und mit der Erstellung Ihres Inhalts neu zu beginnen.
* **[!UICONTROL Als Fragment speichern]** - Speichert die E-Mail ganz oder teilweise als Fragment, das für mehrere E-Mails oder E-Mail-Vorlagen wiederverwendet werden soll. Geben Sie einen Namen und eine Beschreibung für das Fragment ein und speichern Sie es in der Liste der verfügbaren Fragmente.
* **[!UICONTROL Design ändern]** - Kehren Sie zur Seite _E-Mail gestalten_ zurück. Dort können Sie eine andere Vorlage auswählen, um den Design-Prozess neu zu starten, oder den Inhalt von Grund auf auf auf einer schwarzen Arbeitsfläche entwerfen.\
* **[!UICONTROL Als Inhaltsvorlage speichern]** - Speichern Sie den E-Mail-Textkörper als E-Mail-Vorlage, die für mehrere E-Mails oder E-Mail-Vorlagen wiederverwendet werden kann. Geben Sie einen Namen und eine Beschreibung für die Vorlage ein und speichern Sie sie in der Liste der gespeicherten E-Mail-Vorlagen.
* **[!UICONTROL HTML exportieren]** - Laden Sie den Inhalt auf der visuellen Arbeitsfläche in HTML im Format herunter, das als ZIP-Datei verpackt ist.

## Überprüfen und Testen der E-Mail {#email-testing}

>[!CONTEXTUALHELP]
>id="ajo-b2b_email_preview_simulate"
>title="Überprüfen des Inhalt-Renderings"
>abstract="Wenn Ihr Inhalt definiert wurde, können Sie ihn in der Vorschau anzeigen und überprüfen, ob das Rendering entsprechend dem verwendeten Kanal korrekt ist."

Wenn der Nachrichteninhalt definiert ist, können Sie ihn mithilfe von Testprofilen in der Vorschau anzeigen, einen Testversand durchführen und die Darstellung im Seitenverhältnis für Desktop-Computer und Mobilgeräte überprüfen. Wenn Sie personalisierten Inhalt eingefügt haben, können Sie mithilfe von Testprofildaten eine Vorschau der Anzeige dieses Inhalts in der Nachricht anzeigen.

Um [Vorschau des E-Mail](./email-simulate-content.md)Inhalts anzuzeigen, klicken Sie auf **[!UICONTROL Inhalt simulieren]** und wählen Sie ein Testprofil aus, um Ihre Nachricht mithilfe der Daten des Personenprofils zu überprüfen.

![Simulieren Sie den E-Mail-Inhalt, um Ihr Design zu überprüfen](./assets/email-designer-simulate-content.png){width="700" zoomable="yes"}

Sie können auf zusätzliche Tools zugreifen, um den E-Mail-Inhalt zu validieren und zu überprüfen:

* [Durchführen eines Testversands](./email-simulate-content.md#send-proofs)
* [Testrendering in E-Mail Clients](./email-test-rendering.md)
<!-- * Generate a spam report -->
