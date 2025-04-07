---
title: E-Mail-Erstellung
description: Erfahren Sie, wie Sie personalisierte E-Mail-Inhalte erstellen, die auf einer Konto-Journey verwendet werden.
feature: Email Authoring, Content
exl-id: 0f4ae644-ade7-49a0-935c-7f4779c25ffb
source-git-commit: 797d049cc5aefe710a39a980107f63e75cae12d2
workflow-type: tm+mt
source-wordcount: '1297'
ht-degree: 15%

---

# E-Mail-Erstellung

Verwenden Sie Adobe Journey Optimizer B2B edition, um E-Mail-Nachrichten an Ihre Kunden zu senden. Sie können Nachrichten im visuellen Designer erstellen, personalisieren und in der Vorschau anzeigen.

## Hinzufügen einer E-Mail-Aktion zu einer Konto-Journey

Sie können den E-Mail-Versand auf einer Konto-Journey einrichten, wenn Sie einen Knoten _[!UICONTROL Aktion ausführen]_ hinzufügen und dann Folgendes ausführen:

1. Wählen Sie für _[!UICONTROL Ziel]_ Aktion auf“ **[!UICONTROL Personen]**.
1. Wählen Sie für _[!UICONTROL Aktion für Personen]_ die Option **[!UICONTROL E-Mail senden]**.
1. Wählen Sie für _[!UICONTROL E-Mail]_ die Option **[!UICONTROL Neue E-Mail erstellen]**.

   Alternativ können Sie auch die Option _[!UICONTROL E-Mail aus Adobe Marketo Engage auswählen]_ auswählen, um eine der vorab erstellten E-Mails in Marketo Engage zu verwenden und als Teil der Konto-Journey zu senden.

   >[!NOTE]
   >
   >Wenn Sie zum ersten Mal eine E-Mail erstellen, stellen Sie sicher, dass der E-Mail-Kanal in Adobe Marketo Engage konfiguriert ist. Weitere Informationen finden Sie unter [Sicherstellen der E-Mail](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/setup-steps#ensure-email-deliverability) in der Dokumentation zu Marketo Engage.

   ![Aktion durchführen - E-Mail senden](assets/journey-node-send-email.png){width="700" zoomable="yes"}

1. Klicken Sie unten im Bedienfeld _[!UICONTROL Aktion ausführen]_ auf **[!UICONTROL E-Mail erstellen]**.

1. Geben Sie im Dialogfeld einen eindeutigen **[!UICONTROL Namen“ für die E]** Mail und eine **[!UICONTROL Betreffzeile]** ein.

   ![Dialogfeld „Neue E-Mail erstellen“](assets/create-new-email.png){width="400"}

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

   Im Abschnitt _[!UICONTROL E]_ Mail-Eigenschaften“ der E-Mail-Inhaltsseite sind die Felder _[!UICONTROL Von E-Mail]_ und _[!UICONTROL Antwort an Adresse]_ bereits konfiguriert. Sie können Werte für die Felder _[!UICONTROL Absendername]_ und _[!UICONTROL Beschreibung]_ (optional) eingeben.

## Erstellen des E-Mail-Inhalts

Klicken Sie **[!UICONTROL E-Mail-]** hinzufügen“ oben im Vorschaufenster _[!UICONTROL E-Mail]_.

![Klicken Sie auf E-Mail-Inhalt hinzufügen ](./assets/add-email-content.png){width="700" zoomable="yes"}

Diese Aktion startet die E-Mail-Designer, in der Sie aus den folgenden Optionen auswählen können, wie Sie Ihre E-Mail gestalten möchten:

* [Erstellen Sie Ihre E-Mail von Grund auf ](#design-your-email-from-scratch) mithilfe der Benutzeroberfläche von E-Mail-Designer.

* [Importieren Sie vorhandene HTML-Inhalte](#import-existing-html-content) aus einer Datei oder einem ZIP-Ordner.

* [Wählen Sie eine vorhandene ](#select-a-template) aus einer Liste integrierter oder benutzerdefinierter E-Mail-Vorlagen aus.

Um die Betreffzeile mit dem Ausdruckseditor zu konfigurieren und zu personalisieren, klicken Sie auf das Symbol _Personalization_ und fügen Sie eines der Marketo Engage-Token hinzu.

Nachdem Sie den E-Mail-Inhalt erstellt und personalisiert haben, können Sie den Inhalt zur Validierung oder zur späteren Verwendung exportieren. Klicken Sie **[!UICONTROL HTML exportieren]**, um den Inhalt als ZIP-Datei zu speichern, die Ihre HTML und Assets enthält.

>[!TIP]
>
>Verwenden Sie den KI-Assistenten in Adobe Journey Optimizer B2B edition, der auf generativer KI basiert, um Ihre Inhalte auf die nächste Ebene zu heben. Der KI-Assistent kann Ihnen dabei helfen, die Wirkung Ihrer Sendungen zu optimieren, indem er ganze E-Mails und zielgerichtete Textinhalte generiert und KI-Assistenten-Empfehlungen für Bilder abgibt, die bei Ihrer Audience Anklang finden. [Weitere Informationen](./ai-assistant-emails.md)

### Gestalten Ihrer E-Mail von Grund auf neu {#design-from-scratch}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_landing_page"
>title="Hinzufügen von Strukturkomponenten"
>abstract="Strukturkomponenten definieren das Layout der Landingpage. Ziehen Sie eine **Struktur**-Komponente per Drag-and-Drop auf die Arbeitsfläche, um mit der Gestaltung Ihres Landingpage-Inhalts zu beginnen."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_landing_page"
>title="Über Inhaltskomponenten"
>abstract="Inhaltskomponenten sind leere Platzhalter für Inhalte, mit denen Sie das Layout einer Landingpage erstellen können."

Verwenden Sie den visuellen Inhaltseditor, um die Struktur des E-Mail-Inhalts zu definieren. Durch das Hinzufügen und Verschieben von Strukturkomponenten mit einfachen Drag-and-Drop-Aktionen können Sie die Form des wiederverwendbaren E-Mail-Inhalts innerhalb von Sekunden entwerfen.

1. Wählen Sie auf _[!UICONTROL Startseite]_ Vorlage entwerfen“ die Option **[!UICONTROL Erstellen von neuen]** aus.

1. [Struktur und Inhalt hinzufügen](#add-structure-and-content) zur E-Mail-Nachricht.
1. [Hinzufügen von Bild-](#add-assets)) zur E-Mail-Nachricht.
1. [Personalisieren des E-Mail-Inhalts](#personalize-content).
1. [Links überprüfen und ](#preview-and-edit-linked-urls).

<!-- If needed, you can further personalize your email by clicking **[!UICONTROL Switch to code editor]** from the advanced menu. The code editor allows you to edit the email source code, such as adding tracking or custom HTML tags.

>[!CAUTION]
>
>You cannot revert back to the visual designer for this email after switching to the code editor. -->

Wenn Ihr Inhalt fertig ist, klicken Sie oben auf **[!UICONTROL Inhalt simulieren]**, um das Rendering zu überprüfen. Sie können zwischen der Desktop- oder der mobilen Ansicht wählen.

Wenn Sie mit dem Inhalt zufrieden sind, klicken Sie auf **[!UICONTROL Speichern]**.

### Vorhandenen HTML-Inhalt importieren

{{$include /help/_includes/content-design-import.md}}

![Importieren Sie HTML-Inhalte in eine ZIP-Datei](./assets/email-import-zip-file.png){width="500"}

>[!NOTE]
>
>Einen `<table>`-Tag als erste Ebene in einer HTML-Datei zu verwenden kann zum Verlust des Stils führen, einschließlich der Einstellungen für Hintergrund und Breite im Tag der obersten Ebene.

Sie können den importierten Inhalt nach Bedarf mit den visuellen E-Mail-Editor-Tools personalisieren.

### Vorlage auswählen

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

### Inhalt personalisieren

{{$include /help/_includes/content-design-personalization.md}}

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

### Mehr Optionen

Im Menü _[!UICONTROL Mehr …]_ oben in Email Designer können Sie die folgenden Aktionen ausführen:

![Klicken Sie auf Mehr , um auf Vorlagenaktionen zuzugreifen](./assets/email-designer-more-menu.png){width="500"}

* **[!UICONTROL E-Mail zurücksetzen]** - Klicken Sie auf diese Option, um die visuelle E-Mail-Designer-Arbeitsfläche zu löschen und mit der Erstellung Ihres Inhalts neu zu beginnen.
* **[!UICONTROL Als Fragment speichern]** - Speichert die E-Mail ganz oder teilweise als Fragment, das für mehrere E-Mails oder E-Mail-Vorlagen wiederverwendet werden soll. Geben Sie einen Namen und eine Beschreibung für das Fragment ein und speichern Sie es in der Liste der verfügbaren Fragmente.
* **[!UICONTROL Design ändern]** - Kehren Sie zur Seite _E-Mail gestalten_ zurück. Dort können Sie eine andere Vorlage auswählen, um den Design-Prozess neu zu starten, oder den Inhalt von Grund auf auf auf einer schwarzen Arbeitsfläche entwerfen.\
* **[!UICONTROL Als Inhaltsvorlage speichern]** - Speichern Sie den E-Mail-Textkörper als E-Mail-Vorlage, die für mehrere E-Mails oder E-Mail-Vorlagen wiederverwendet werden kann. Geben Sie einen Namen und eine Beschreibung für die Vorlage ein und speichern Sie sie in der Liste der gespeicherten E-Mail-Vorlagen.
* **[!UICONTROL HTML exportieren]** - Laden Sie den Inhalt auf der visuellen Arbeitsfläche in HTML im Format herunter, das als ZIP-Datei verpackt ist.

## Prüfen von Warnhinweisen

Während Sie den Inhalt Ihrer E-Mail-Nachricht entwerfen, werden Warnhinweise in der Benutzeroberfläche (oben rechts auf der Seite) angezeigt, wenn wichtige Einstellungen fehlen.

Wenn diese Schaltfläche nicht angezeigt wird, treten keine Probleme auf.

Es können zwei Arten von Warnhinweisen erkannt werden:

* **_Warnhinweise_** die auf Empfehlungen und Best Practices verweisen, z. B.:

   * `The opt-out link is not present in the email body`: Es wird empfohlen, einen Abmelde-Link in Ihren E-Mail-Textkörper einzufügen.

     >[!NOTE]
     >
     >E-Mail-Nachrichten im Marketing-Stil müssen einen Ausschluss-Link enthalten, der für Transaktionsnachrichten nicht erforderlich ist.

   * `Text version of HTML is empty`: Vergessen Sie nicht, eine Textversion Ihres E-Mail-Textkörpers zu definieren, die verwendet wird, wenn HTML-Inhalte nicht angezeigt werden können.

   * `Empty link is present in email body`: Vergewissern Sie sich, dass alle Links in Ihrer E-Mail korrekt sind.

   * `Email size has exceeded the limit of 100KB`: Stellen Sie sicher, dass die Größe Ihrer E-Mail 100 KB nicht überschreitet, um einen optimalen Versand zu erzielen.

* **_Fehler_** die verhindern, dass Sie die Journey/Kampagne testen oder aktivieren, solange nicht alle Fehler behoben sind, z. B.:

   * `The subject line is missing`: E-Mail-Betreffzeile ist obligatorisch.

   * `The email version of the message is empty`: Dieser Fehler wird angezeigt, wenn der E-Mail-Inhalt nicht konfiguriert wurde.

## Überprüfen und Testen der E-Mail {#preview-test}

>[!CONTEXTUALHELP]
>id="ajo-b2b_email_preview_simulate"
>title="Überprüfen des Inhalt-Renderings"
>abstract="Wenn Ihr Inhalt definiert wurde, können Sie ihn in der Vorschau anzeigen und überprüfen, ob das Rendering entsprechend dem verwendeten Kanal korrekt ist."

Wenn der Nachrichteninhalt definiert ist, können Sie ihn mithilfe von Testprofilen in der Vorschau anzeigen, Testsendungen durchführen und das Rendering in gängigen Desktop-, Mobile- und Web-basierten Clients steuern. Wenn Sie personalisierten Inhalt eingefügt haben, können Sie mithilfe von Testprofildaten eine Vorschau der Anzeige dieses Inhalts in der Nachricht anzeigen.

Um eine Vorschau des E-Mail-Inhalts anzuzeigen, klicken Sie **[!UICONTROL Inhalt simulieren]** und fügen Sie dann ein Testprofil hinzu, um Ihre Nachricht mithilfe der Testprofildaten zu überprüfen.

![Simulieren Sie den E-Mail-Inhalt, um Ihr Design zu überprüfen](./assets/email-designer-simulate-content.png){width="700" zoomable="yes"}
