---
title: Email Authoring
description: Erfahren Sie, wie Sie personalisierte E-Mail-Inhalte erstellen, die in einer Konto-Journey verwendet werden.
feature: Email Authoring, Content
exl-id: 0f4ae644-ade7-49a0-935c-7f4779c25ffb
source-git-commit: 5f53f4156c670d1c7b751844ab0bda0aef352973
workflow-type: tm+mt
source-wordcount: '1221'
ht-degree: 16%

---

# E-Mail-Authoring

Verwenden Sie Adobe Journey Optimizer B2B Edition, um Ihren Kunden E-Mail-Nachrichten zu senden. Mithilfe des E-Mail-Designers können Sie Nachrichten erstellen, personalisieren und in der Vorschau anzeigen.

## Hinzufügen einer E-Mail-Aktion auf einer Konto-Journey

Sie können E-Mail-Sendungen in einer Konto-Journey einrichten, wenn Sie einen Knoten _[!UICONTROL Aktion ausführen]_ hinzufügen und folgende Schritte ausführen:

1. Wählen Sie für die _[!UICONTROL Aktion auf]_ Ziel **[!UICONTROL Personen]** aus.
1. Wählen Sie für die _[!UICONTROL Aktion für Personen]_ **[!UICONTROL E-Mail senden]** aus.
1. Wählen Sie für die _[!UICONTROL E-Mail-Quelle]_ **[!UICONTROL Neue E-Mail erstellen]** aus.

   Alternativ können Sie auch die Option _[!UICONTROL E-Mail aus Adobe Marketo Engage auswählen]_ auswählen, um eine der vorab erstellten E-Mails in Marketo Engage zu verwenden und sie als Teil der Konto-Journey zu senden.

   >[!NOTE]
   >
   >Wenn Sie eine E-Mail zum ersten Mal erstellen, stellen Sie sicher, dass der E-Mail-Kanal in Adobe Marketo Engage konfiguriert ist. Weitere Informationen finden Sie unter [Zustellbarkeit von E-Mails sicherstellen](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/setup-steps#ensure-email-deliverability) in der Marketo Engage-Dokumentation.

   ![Aktion durchführen - E-Mail senden](assets/journey-node-send-email.png){width="700" zoomable="yes"}

1. Klicken Sie unten im Bedienfeld _[!UICONTROL Aktion durchführen]_ auf **[!UICONTROL E-Mail erstellen]**.

1. Geben Sie im Dialogfeld einen eindeutigen **[!UICONTROL Namen]** für die E-Mail und eine **[!UICONTROL Betreffzeile]** ein.

   ![Neues E-Mail-Dialogfeld erstellen](assets/create-new-email.png){width="400"}

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

   Im Abschnitt _[!UICONTROL E-Mail-Eigenschaften]_ der E-Mail-Inhaltsseite sind die Felder _[!UICONTROL Von E-Mail]_ und _[!UICONTROL An Adresse antworten]_ bereits konfiguriert. Sie können Werte für die Felder _[!UICONTROL Von Name]_ und _[!UICONTROL Beschreibung]_ (optional) eingeben.

## Erstellen des E-Mail-Inhalts

Klicken Sie oben im Vorschaufenster für die _[!UICONTROL E-Mail]_ auf **[!UICONTROL E-Mail-Inhalt hinzufügen]** .

![Klicken Sie auf E-Mail-Inhalt hinzufügen ](./assets/add-email-content.png){width="700" zoomable="yes"}

Mit dieser Aktion wird E-Mail-Designer gestartet, in der Sie aus den folgenden Optionen auswählen können, wie Sie Ihre E-Mail erstellen möchten:

* [Gestalten Sie Ihre E-Mail mit der Benutzeroberfläche von Email Designer von Grund auf neu](#design-your-email-from-scratch).

* [Importieren Sie vorhandene HTML-Inhalte](#import-existing-html-content) aus einer Datei oder einem ZIP-Ordner.

* [Wählen Sie eine vorhandene Vorlage ](#select-a-template) aus einer Liste integrierter oder benutzerdefinierter E-Mail-Vorlagen.

Um die Betreffzeile mit dem Ausdruckseditor zu konfigurieren und zu personalisieren, klicken Sie auf das Symbol _Personalization_ und fügen Sie einen der Marketo Engage-Token hinzu.

Nachdem Sie den E-Mail-Inhalt erstellt und personalisiert haben, können Sie ihn zur Validierung oder zur späteren Verwendung exportieren. Klicken Sie auf **[!UICONTROL HTML exportieren]** , um den Inhalt als ZIP-Datei zu speichern, die Ihre HTML und Assets enthält.

>[!TIP]
>
>Verwenden Sie den KI-Assistenten in Adobe Journey Optimizer B2B Edition, der auf generativer KI basiert, um Ihre Inhalte auf die nächste Stufe zu heben. Der KI-Assistent kann Sie dabei unterstützen, die Wirkung Ihrer Sendungen zu optimieren, indem er komplette E-Mails, zielgerichtete Textinhalte und Empfehlungen für den KI-Assistenten für Bilder generiert, die Ihrer Zielgruppe entsprechen. [Weitere Informationen](./ai-assistant-emails.md)

### Gestalten Ihrer E-Mail von Grund auf neu {#design-from-scratch}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_landing_page"
>title="Hinzufügen von Strukturkomponenten"
>abstract="Strukturkomponenten definieren das Layout der Landingpage. Ziehen Sie eine **Struktur**-Komponente per Drag-and-Drop auf die Arbeitsfläche, um mit der Gestaltung Ihres Landingpage-Inhalts zu beginnen."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_landing_page"
>title="Über Inhaltskomponenten"
>abstract="Inhaltskomponenten sind leere Platzhalter für Inhalte, mit denen Sie das Layout einer Landingpage erstellen können."

Verwenden Sie den visuellen Inhaltseditor, um die Struktur des E-Mail-Inhalts zu definieren. Durch das Hinzufügen und Verschieben von Strukturkomponenten mit einfachen Drag &amp; Drop-Aktionen können Sie die Form des wiederverwendbaren E-Mail-Inhalts innerhalb von Sekunden gestalten.

1. Wählen Sie auf der Homepage _[!UICONTROL Vorlage entwerfen]_ die Option **[!UICONTROL Neu entwerfen]** aus.

1. [Fügen Sie der E-Mail-Nachricht Struktur und Inhalt hinzu](#add-structure-and-content).
1. [ Bild-Assets hinzufügen](#add-assets) zur E-Mail-Nachricht.
1. [Personalisieren Sie den E-Mail-Inhalt](#personalize-content).
1. [Überprüfen und aktualisieren Sie die Links](#preview-and-edit-linked-urls).

<!-- If needed, you can further personalize your email by clicking **[!UICONTROL Switch to code editor]** from the advanced menu. The code editor allows you to edit the email source code, such as adding tracking or custom HTML tags.

>[!CAUTION]
>
>You cannot revert back to the visual designer for this email after switching to the code editor. -->

Wenn Ihr Inhalt fertig ist, klicken Sie oben auf **[!UICONTROL Inhalt simulieren]** , um das Rendering zu überprüfen. Sie können zwischen der Desktop- oder der mobilen Ansicht wählen.

Wenn Sie mit dem Inhalt zufrieden sind, klicken Sie auf **[!UICONTROL Speichern]**.

### Vorhandenen HTML-Inhalt importieren

{{$include /help/_includes/content-design-import.md}}

![HTML-Inhalt in eine ZIP-Datei importieren](./assets/email-import-zip-file.png){width="500"}

>[!NOTE]
>
>Einen `<table>`-Tag als erste Ebene in einer HTML-Datei zu verwenden kann zum Verlust des Stils führen, einschließlich der Einstellungen für Hintergrund und Breite im Tag der obersten Ebene.

Mit den visuellen E-Mail-Editor-Tools können Sie den importierten Inhalt nach Bedarf personalisieren.

### Vorlage auswählen

{{$include /help/_includes/content-design-select-template.md}}

## Struktur und Inhalt hinzufügen {#structure-content}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_email"
>title="Hinzufügen von Strukturkomponenten"
>abstract="Strukturkomponenten definieren das Layout der E-Mail. Ziehen Sie eine **Struktur**-Komponente per Drag-and-Drop auf die Arbeitsfläche, um mit der Gestaltung Ihres E-Mail-Inhalts zu beginnen."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_email"
>title="Über Inhaltskomponenten"
>abstract="Inhaltskomponenten sind leere Platzhalter für Inhalt, die Sie zum Erstellen des E-Mail-Layouts verwenden können."

{{$include /help/_includes/content-design-components.md}}

### Fragmente hinzufügen

Im visuellen Inhaltseditor wird links das Symbol _Fragmente_ angezeigt. Im folgenden Beispiel werden die Schritte zum Hinzufügen von Fragmenten zum Vorlageninhalt beschrieben.

1. Um die Fragmentliste zu öffnen, klicken Sie auf das Symbol _Fragmente_.

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
>Wenn Sie das Fragment so hinzufügen möchten, dass es das gesamte horizontale Layout der E-Mail einnimmt, fügen Sie eine 1:1-Spaltenstruktur hinzu und ziehen Sie das Fragment per Drag-and-Drop in die E-Mail.

Nachdem die E-Mail gespeichert wurde, wird sie auf der Seite mit den Fragmentdetails angezeigt, wenn Sie in der Zusammenfassung die Registerkarte _[!UICONTROL Verwendet von]_ auswählen. Zu einer E-Mail-Vorlage hinzugefügte Fragmente können nicht in der Vorlage bearbeitet werden. Der Inhalt wird durch das Quellfragment definiert.

### Hinzufügen von Assets

{{$include /help/_includes/content-design-assets.md}}

### Navigieren in den Ebenen, Einstellungen und Stilen

{{$include /help/_includes/content-design-navigation.md}}

### Inhalt personalisieren

{{$include /help/_includes/content-design-personalization.md}}

### Linked URL-Tracking bearbeiten

{{$include /help/_includes/content-design-links.md}}

### Anzeigeoptionen

Nutzen Sie die im visuellen E-Mail-Editor verfügbaren Ansicht- und Inhaltsvalidierungsoptionen.

* Vergrößern/Verkleinern Sie den Inhalt über vordefinierte Zoom-Optionen.

* Wechseln Sie zwischen der Anzeige des Inhalts über Desktop, Mobilgeräte oder Nur-Text/Nur-Text.
   * Klicken Sie auf das Symbol _Auge_ für die geräteübergreifende Inhaltsvorschau.
   * Wählen Sie eines der nativen Geräte aus oder geben Sie benutzerdefinierte Dimensionen ein, um die Vorschau des Inhalts anzuzeigen.

## Prüfen von Warnhinweisen

Während Sie den Inhalt Ihrer E-Mail-Nachricht erstellen, werden Warnhinweise in der Benutzeroberfläche (oben rechts auf der Seite) angezeigt, wenn wichtige Einstellungen fehlen.

Wenn diese Schaltfläche nicht angezeigt wird, gibt es keine erkannten Probleme.

Zwei Arten von Warnhinweisen können erkannt werden:

* **_Warnungen_**, die auf Empfehlungen und Best Practices verweisen, z. B.:

   * `The opt-out link is not present in the email body`: Es empfiehlt sich, einen Abmelde-Link in Ihren E-Mail-Textkörper einzufügen.

     >[!NOTE]
     >
     >E-Mail-Nachrichten im Marketing-Stil müssen einen Ausschluss-Link enthalten, der für Transaktionsnachrichten nicht erforderlich ist.

   * `Text version of HTML is empty`: Vergessen Sie nicht, eine Textversion Ihres E-Mail-Textkörpers zu definieren, die verwendet wird, wenn kein HTML-Inhalt angezeigt werden kann.

   * `Empty link is present in email body`: Überprüfen Sie, ob alle Links in Ihrer E-Mail korrekt sind.

   * `Email size has exceeded the limit of 100KB`: Stellen Sie für einen optimalen Versand sicher, dass die Größe Ihrer E-Mail 100 KB nicht überschreitet.

* **_Fehler_**, die Sie daran hindern, die Journey/Kampagne zu testen oder zu aktivieren, solange sie nicht aufgelöst werden, z. B.:

   * `The subject line is missing`: E-Mail-Betreffzeile ist obligatorisch.

   * `The email version of the message is empty`: Dieser Fehler wird angezeigt, wenn der E-Mail-Inhalt nicht konfiguriert wurde.

## Überprüfen und Testen der E-Mail {#preview-test}

>[!CONTEXTUALHELP]
>id="ajo-b2b_email_preview_simulate"
>title="Überprüfen des Inhalt-Renderings"
>abstract="Wenn Ihr Inhalt definiert wurde, können Sie ihn in der Vorschau anzeigen und überprüfen, ob das Rendering entsprechend dem verwendeten Kanal korrekt ist."

Wenn Ihr Nachrichteninhalt definiert ist, können Sie mithilfe von Testprofilen die Vorschau anzeigen, Testsendungen durchführen und das Rendering in beliebten Desktop-, Mobile- und Web-basierten Clients steuern. Wenn Sie personalisierten Inhalt eingefügt haben, können Sie mithilfe von Testprofildaten eine Vorschau des Inhalts in der Nachricht anzeigen.

Um den E-Mail-Inhalt in der Vorschau anzuzeigen, klicken Sie auf **[!UICONTROL Inhalt simulieren]** und fügen Sie dann ein Testprofil hinzu, um Ihre Nachricht mithilfe der Testprofildaten zu überprüfen.

![Simulieren Sie den E-Mail-Inhalt, um Ihren Entwurf zu überprüfen](./assets/email-designer-simulate-content.png){width="700" zoomable="yes"}
