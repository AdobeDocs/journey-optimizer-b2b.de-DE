---
title: E-Mail-Authoring
description: Erfahren Sie, wie Sie personalisierte E-Mail-Inhalte erstellen, die in Account Journey verwendet werden.
feature: Email Authoring, Content
exl-id: 0f4ae644-ade7-49a0-935c-7f4779c25ffb
source-git-commit: ec72c46a57109814464542fd4a8e4a9828982136
workflow-type: tm+mt
source-wordcount: '1314'
ht-degree: 11%

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

### E-Mail von Grund auf neu erstellen

1. Wählen Sie auf der Startseite von Designer die Option **[!UICONTROL Erstellen von neuen Inhalten]** aus.

1. Ziehen Sie zum Starten Ihres Inhaltsdesigns ein Element aus den **[!UICONTROL Strukturen]** und legen Sie es auf der Arbeitsfläche ab.

   Wiederholen Sie diesen Schritt für jede Strukturkomponente , um das Layout Ihrer E-Mail zu erstellen.

1. Fügen Sie so viele Elemente aus _Strukturen_ hinzu, wie Sie benötigen, und bearbeiten Sie die Einstellungen für jedes Element im Bereich auf der rechten Seite.

   Wählen Sie die n:n-Spaltenkomponente aus, um die Anzahl der Spalten Ihrer Wahl zu definieren (zwischen drei und zehn). Sie können auch die Breite jeder Spalte definieren, indem Sie die Pfeile unter die Spalte verschieben.

   Die Spaltengröße darf nicht weniger als 10 % der Gesamtbreite der Strukturkomponente betragen. Es können nur leere Spalten entfernt werden.

1. Erweitern Sie den Abschnitt **[!UICONTROL Inhalt]** und fügen Sie beliebig viele Elemente zu einer oder mehreren Strukturkomponenten hinzu.

1. Bei Bedarf können Sie auf den Registerkarten _[!UICONTROL Einstellungen]_ oder _[!UICONTROL Stil]_ zusätzliche Anpassungen für jede Komponente vornehmen.

   Sie können beispielsweise den Textstil, den Abstand oder den Rand jeder Komponente ändern.

1. Über die Asset-Auswahl können Sie direkt in der Assets-Bibliothek gespeicherte Assets auswählen.

   Doppelklicken Sie auf den Ordner, der Ihre Assets enthält. Ziehen Sie die Elemente in eine Strukturkomponente.

1. Fügen Sie Personalisierungsfelder ein, um Ihren Inhalt aus Profilattributen, Zielgruppenmitgliedschaften, Kontextattributen und mehr anzupassen.

1. Klicken Sie auf **[!UICONTROL Bedingungsinhalt aktivieren]** , um dynamischen Inhalt hinzuzufügen und den Inhalt basierend auf Bedingungsregeln an die Zielprofile anzupassen.

1. Wählen Sie im linken Bereich die Registerkarte **[!UICONTROL Links]** aus, um alle getrackten URLs Ihres Inhalts anzuzeigen.

   Sie können den _Trackingtyp_ oder den _Titel_ ändern und bei Bedarf Tags hinzufügen.

Bei Bedarf können Sie Ihre E-Mail weiter personalisieren, indem Sie im erweiterten Menü auf **[!UICONTROL Zum Code-Editor wechseln]** klicken. Mit dem Code-Editor können Sie den E-Mail-Quellcode bearbeiten, z. B. das Hinzufügen von Tracking- oder benutzerdefinierten HTML-Tags.

>[!CAUTION]
>
>Sie können nach dem Wechsel zum Code-Editor nicht zum visuellen Designer für diese E-Mail zurückkehren.

Wenn Ihr Inhalt fertig ist, klicken Sie oben auf **[!UICONTROL Inhalt simulieren]** , um das Rendering zu überprüfen. Sie können zwischen der Desktop- oder der mobilen Ansicht wählen.

Wenn Sie fertig sind, klicken Sie auf Speichern.

### Vorhandenen HTML-Inhalt importieren

Importierte Inhalte können:

* Eine HTML-Datei mit integriertem Stylesheet
* Ein ZIP-Ordner mit einer HTML-Datei, dem Stylesheet (.css) und Bilddateien

>[!NOTE]
>
>Die Dateistruktur des komprimierten Ordners ist freigestellt. Verweise müssen jedoch relativ sein und mit der Baumstruktur des ZIP-Ordners übereinstimmen.

_So importieren Sie eine Datei mit HTML-Inhalt:_

1. Wählen Sie auf der Startseite des E-Mail-Designers die Option **[!UICONTROL HTML importieren]**.

1. Ziehen Sie die HTML- oder ZIP-Datei mit Ihrem HTML-Inhalt per Drag-and-Drop und klicken Sie auf [!UICONTROL Importieren].

   Wenn der HTML-Inhalt-Upload abgeschlossen ist, befindet sich Ihr Inhalt im _Kompatibilitätsmodus_. In diesem Modus können Sie nur Ihren Text personalisieren, Links hinzufügen oder Assets zu Ihrem Inhalt hinzufügen.

### Vorlage auswählen

Sie können aus folgenden Optionen wählen:

* Beispielvorlagen. Die Benutzeroberfläche von Journey Optimizer bietet 20 vordefinierte E-Mail-Vorlagen, aus denen Sie auswählen können.

* Gespeicherte Vorlagen

* Eine benutzerdefinierte Vorlage, die Sie entweder mit dem Menü _Vorlagen_ von Grund auf neu erstellt oder mithilfe der Option _[!UICONTROL Als Inhaltsvorlage speichern]_ aus einer E-Mail in einer Journey gespeichert haben.

_So erstellen Sie Ihren Inhalt mit einer der Beispiel- oder gespeicherten Vorlagen:_

1. Greifen Sie über den Arbeitsbereich zur Bearbeitung von E-Mail-Inhalten auf die _E-Mail-Designer_ zu.

   Auf der Seite _[!UICONTROL E-Mail erstellen]_ ist standardmäßig der Tab **[!UICONTROL Beispielvorlagen]** ausgewählt.

1. Um eine benutzerdefinierte Vorlage zu verwenden, wählen Sie die Registerkarte **[!UICONTROL Gespeicherte Vorlagen]** aus.

   Die Liste aller in der aktuellen Sandbox erstellten Inhaltsvorlagen wird angezeigt. Sie können sie nach Name, Letzte Änderung oder Letzte Erstellung sortieren.

1. Wählen Sie aus der Liste die gewünschte Vorlage aus.

1. Nachdem Sie eine Kategorie ausgewählt haben, können Sie mithilfe der Rechts- und Linkspfeile zwischen allen Vorlagen dieser Kategorie (Beispiel oder je nach Auswahl gespeichert) navigieren.

1. Klicken Sie oben rechts auf der Seite auf **[!UICONTROL Diese Vorlage verwenden]** .

1. Bearbeiten Sie den Inhalt nach Bedarf in der _E-Mail-Designer_.

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

## E-Mail überprüfen und testen

Wenn Ihr Nachrichteninhalt definiert ist, können Sie mithilfe von Testprofilen die Vorschau anzeigen, Testsendungen durchführen und das Rendering in beliebten Desktop-, Mobile- und Web-basierten Clients steuern. Wenn Sie personalisierten Inhalt eingefügt haben, können Sie mithilfe von Testprofildaten eine Vorschau des Inhalts in der Nachricht anzeigen.

Um den E-Mail-Inhalt in der Vorschau anzuzeigen, klicken Sie auf **[!UICONTROL Inhalt simulieren]** und fügen Sie dann ein Testprofil hinzu, um Ihre Nachricht mithilfe der Testprofildaten zu überprüfen.

![Simulieren Sie den E-Mail-Inhalt, um Ihren Entwurf zu überprüfen](./assets/email-designer-simulate-content.png){width="700" zoomable="yes"}
