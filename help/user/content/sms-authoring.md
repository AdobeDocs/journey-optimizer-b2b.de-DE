---
title: SMS-Authoring
description: Erfahren Sie, wie Sie Ihren Kunden auf ihren Mobilgeräten Textnachrichten (SMS) senden und Nachrichten im Textformat personalisieren und im SMS-Editor in der Vorschau anzeigen können.
feature: SMS Authoring, Content
exl-id: bd648253-74de-4083-a37a-ab7ceaea2746
source-git-commit: e38ec0f128e811fd4ac21c624d9018854b91c78b
workflow-type: tm+mt
source-wordcount: '2041'
ht-degree: 4%

---

# SMS-Authoring

Verwenden Sie Adobe Journey Optimizer B2B edition , um Ihren Kunden auf ihren Mobilgeräten Textnachrichten (SMS) zu senden. Mit dem SMS-Editor können Sie Nachrichten im Textformat erstellen, personalisieren und in der Vorschau anzeigen.

## SMS-Konfigurationen

Adobe Journey Optimizer B2B Edition sendet Textnachrichten über SMS-Dienstleister (oder SMS Gateway Provider). Konfigurieren Sie vor der Erstellung Ihrer SMS-Nachricht Ihren Dienstleister über die Einstellungen für _Administrator_.

### SMS-Gateway-Dienstleister

Adobe Journey Optimizer B2B edition lässt sich derzeit mit Drittanbietern integrieren, die unabhängig voneinander Textnachrichtendienste anbieten. Unterstützte Anbieter für Textnachrichten sind Sinch, Twilio und Infobip.

Bevor Sie einen SMS-Kanal in Adobe Journey Optimizer B2B edition konfigurieren, müssen Sie ein Konto bei einem dieser Anbieter erstellen, um Ihr API-Token und Ihre Service-ID zu erhalten. Diese Anmeldeinformationen sind erforderlich, um die Verbindung zwischen Adobe Journey Optimizer B2B edition und dem entsprechenden Provider zu konfigurieren.

>[!IMPORTANT]
>
>Ihre Nutzung von Textnachrichten-Services unterliegt zusätzlichen Bedingungen des jeweiligen Anbieters. Als Drittanbieterlösungen stehen Benutzern von Adobe Journey Optimizer B2B edition über eine Integration Sinch, Twilio und Infobip zur Verfügung. Adobe kontrolliert keine Produkte von Drittanbietern und ist nicht für diese verantwortlich. Wenden Sie sich bei Problemen oder Ersuchen um Unterstützung im Zusammenhang mit den Textnachrichtendiensten (SMS) an Ihren Provider.

### Vorhandene SMS-API-Konfiguration überprüfen

>[!NOTE]
>
>Die beschriebenen Einstellungen sind nur für Benutzer mit SMS-Administratorrechten zugänglich.

1. Erweitern Sie im linken Navigationsbereich den Abschnitt **[!UICONTROL Administrator]** und klicken Sie auf **[!UICONTROL Kanäle]**.

   ![Zugriff auf die Konfiguration der SMS-API-Anmeldeinformationen](./assets/config-sms-api.png){width="800" zoomable="yes"}

1. Wählen Sie im Navigationsfenster **[!UICONTROL API-Anmeldeinformationen]** aus.

   Auf der Seite werden die verfügbaren API-Konfigurationen für Ihre Instanz aufgelistet.

1. Klicken Sie bei Bedarf auf das Symbol _Filter_ ( ![Symbol für Filter ein- oder ausblenden](../assets/do-not-localize/icon-filter.svg) ) und wählen Sie Optionen aus, um die Liste der konfigurierten API-Anmeldeinformationen vom SMS-Dienstleister oder -Ersteller anzuzeigen.

   ![Klicken Sie auf das Filtersymbol, um die Liste der API-Anmeldeinformationen zu verfeinern.](./assets/config-sms-api-filter.png){width="600" zoomable="yes"}

### Erstellen neuer API-Anmeldeinformationen für einen SMS-Dienstanbieter

>[!BEGINTABS]

>[!TAB Sinch]

_So konfigurieren Sie Sinch als SMS-Provider mit Adobe Journey Optimizer B2B Edition:_

1. Erweitern Sie im linken Navigationsbereich den Abschnitt **[!UICONTROL Administrator]** und klicken Sie auf **[!UICONTROL Konfiguration]**.

1. Klicken Sie oben rechts in der Liste _[!UICONTROL API-Anmeldeinformationen]_ auf die Schaltfläche **[!UICONTROL Neue API-Anmeldeinformationen erstellen]** .

1. Konfigurieren Sie Ihre SMS-API-Anmeldedaten:

   ![Konfigurieren der Single-SMS-API-Anmeldeinformationen](./assets/config-sms-api-sinch.png){width="500"}

   * **[!UICONTROL SMS-Anbieter]** - Wählen Sie `Sinch` als SMS-Provider aus.

   * **[!UICONTROL Name]** - Geben Sie einen Namen für Ihre API-Berechtigung ein.

   * **[!UICONTROL Dienst-ID]** und **[!UICONTROL API-Token]** - Greifen Sie über Ihr Einzelkonto auf die API-Seite zu (Ihre Anmeldeinformationen finden Sie auf der Registerkarte SMS ).

   Weitere Informationen zum Auffinden dieser Informationen für Ihr Einzelkonto finden Sie in der [Dokumentation für Einzelentwickler](https://developers.sinch.com/docs/sms/getting-started/#2-get-credentials)

1. Klicken Sie auf **[!UICONTROL Senden]** , wenn die Konfigurationsdetails Ihrer API-Anmeldeinformationen abgeschlossen sind.

>[!TAB Twilio]

_So konfigurieren Sie Twilio als SMS-Provider mit Adobe Journey Optimizer B2B Edition:_

1. Erweitern Sie im linken Navigationsbereich den Abschnitt **[!UICONTROL Administrator]** und klicken Sie auf **[!UICONTROL Konfiguration]**.

1. Klicken Sie oben rechts in der Liste _[!UICONTROL API-Anmeldeinformationen]_ auf die Schaltfläche **[!UICONTROL Neue API-Anmeldeinformationen erstellen]** .

1. Konfigurieren Sie Ihre SMS-API-Anmeldedaten:

   ![Konfigurieren der Twilio-SMS-API-Anmeldeinformationen](./assets/config-sms-api-twilio.png){width="500"}

   * **[!UICONTROL SMS-Anbieter]** - Wählen Sie `Twilio` als SMS-Provider aus.

   * **[!UICONTROL Name]** - Geben Sie einen Namen für Ihre API-Anmeldedefinition ein.

   * **[!UICONTROL Konto-SID]** und **[!UICONTROL Authentifizierungstoken]** - Greifen Sie auf den Bereich _Kontoinformationen_ Ihrer Twilio Console-Dashboard-Seite zu, um Ihre Anmeldeinformationen zu finden.

   Weitere Informationen zum Auffinden dieser Informationen für Ihr Twilio-Konto finden Sie im [Twilio Help Center](https://help.twilio.com/articles/14726256820123-What-is-a-Twilio-Account-SID-and-where-can-I-find-it-).

1. Klicken Sie oben rechts auf der Seite auf **[!UICONTROL Senden]** , wenn die Konfigurationsdetails Ihrer API-Anmeldeinformationen abgeschlossen sind.

>[!TAB Infobip]

_So konfigurieren Sie Infobip als SMS-Provider mit Adobe Journey Optimizer B2B edition:_

1. Erweitern Sie im linken Navigationsbereich den Abschnitt **[!UICONTROL Administrator]** und klicken Sie auf **[!UICONTROL Konfiguration]**.

1. Klicken Sie oben rechts in der Liste _[!UICONTROL API-Anmeldeinformationen]_ auf die Schaltfläche **[!UICONTROL Neue API-Anmeldeinformationen erstellen]** .

1. Konfigurieren Sie Ihre SMS-API-Anmeldedaten:

   ![Konfigurieren der Anmeldeinformationen der Infobip-SMS-API](./assets/config-sms-api-infobip.png){width="500"}

   * **[!UICONTROL SMS-Anbieter]** - Wählen Sie `Infobip` als SMS-Provider aus.

   * **[!UICONTROL Name]** - Geben Sie einen Namen für Ihre API-Anmeldedefinition ein.

   * **[!UICONTROL API-Basis-URL]** und **[!UICONTROL API-Schlüssel]** - Greifen Sie auf die Homepage Ihrer Web-Oberfläche oder die API-Schlüsselverwaltungsseite für Ihr Infobip-Konto zu, um Ihre Anmeldeinformationen zu finden.

   Weitere Informationen zum Auffinden dieser Informationen für Ihr Infobip-Konto finden Sie in der [Infobip-Dokumentation](https://www.infobip.com/docs/api/_blank).

1. Klicken Sie oben rechts auf der Seite auf **[!UICONTROL Senden]** , wenn die Konfigurationsdetails Ihrer API-Anmeldeinformationen abgeschlossen sind.

>[!ENDTABS]

Wenn Sie auf _[!UICONTROL Senden]_ klicken, werden die Anmeldeinformationen sofort validiert und gespeichert und Sie werden zur Seite mit der Auflistung der _[!UICONTROL API-Anmeldeinformationen]_ weitergeleitet. Wenn die übermittelten Anmeldeinformationen ungültig sind, zeigt das System auf der Listenseite eine Fehlermeldung an. In diesem Fall können Sie die Konfiguration abbrechen oder aktualisieren und erneut senden.

## Hinzufügen einer SMS-Aktion auf einer Konto-Journey

Sie können Textnachrichten-Sendungen in einer Konto-Journey einrichten, wenn Sie einen Knoten _[!UICONTROL Aktion ausführen]_ hinzufügen und folgende Schritte ausführen:

1. Wählen Sie für die _[!UICONTROL Aktion auf]_ Ziel **[!UICONTROL Personen]** aus.

1. Wählen Sie für die Aktion _[!UICONTROL für Personen]_ die Option **[!UICONTROL SMS senden]**.

   ![Aktion durchführen - SMS senden](assets/journey-node-send-sms.png){width="800" zoomable="yes"}

1. Klicken Sie unten im Bedienfeld _[!UICONTROL Aktion durchführen]_ auf **[!UICONTROL SMS erstellen]**.

1. Geben Sie im Dialogfeld einen eindeutigen **[!UICONTROL Namen]** für die SMS-Nachricht ein.

   ![Neues SMS-Dialogfeld erstellen](assets/create-new-sms.png){width="400"}

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

   Der _Journey Content Designer_ wird geöffnet. Sie können die Nachricht erstellen und die SMS-Eigenschaften für den Nachrichtenversand festlegen.

### SMS erstellen

>[!IMPORTANT]
>
>**Verwaltung der SMS-Einwilligung**<br/>
>
>In Übereinstimmung mit den Branchenstandards und -vorschriften müssen alle SMS-Marketingnachrichten eine Möglichkeit enthalten, mit der sich die Empfänger leicht abmelden können. Zu diesem Zweck können SMS-Empfänger mit Keywords zum Opt-in oder Opt-out antworten. Alle standardmäßigen Opt-in- und Opt-out-Suchbegriffe werden unterstützt und berücksichtigt. Darüber hinaus werden alle benutzerdefinierten Suchbegriffe unterstützt und berücksichtigt, die für Ihr SMS-Dienstanbieterkonto konfiguriert wurden.

Geben Sie im Feld **[!UICONTROL Nachricht]** den Text ein, den Sie senden möchten.

Sie können eine Nachricht mit bis zu 1600 Zeichen erstellen, wobei jede 160 Zeichen als eine SMS-Nachricht betrachtet wird.

![Klicken Sie auf das Personalisierungssymbol, um der Nachricht Token hinzuzufügen](./assets/sms-message-compose.png){width="800" zoomable="yes"}

#### Textnachricht personalisieren

1. Klicken Sie beim Verfassen der Textnachricht jederzeit auf das Symbol _Personalize_ ( ![Personalize icon](../assets/do-not-localize/icon-personalize.svg) ) rechts neben dem Textfeld.

   Die angezeigte Seite bietet Zugriff auf Ihre Adobe Marketo Engage-Lead- und System-Token. Sowohl Standard- als auch benutzerdefinierte Token sind enthalten. Sie können die Leiste _Suchen_ verwenden, um das benötigte Token zu finden, oder durch die Ordnerstruktur navigieren, um eines der Lead-/System-Token zu suchen und auszuwählen.

1. Platzieren Sie den Cursor an der Stelle in der Nachricht, an der Sie das Token hinzufügen möchten.

1. Fügen Sie ein Token hinzu, indem Sie auf das Pluszeichen ( **+** ) daneben klicken.

   Wenn Sie das Token mit einem Fallback hinzufügen möchten (Standardeinstellung, die angezeigt wird, falls dieses Feld für einen Lead nicht verfügbar ist), klicken Sie auf das Symbol _Mehr_ ( **...** ) und wählen Sie **[!UICONTROL Mit Fallback-Text einfügen]**.

   ![Klicken Sie auf die Auslassungspunkte, um eine Ausweichmöglichkeit für das Token zu verwenden](./assets/sms-message-personalize-ellipsis-fallback.png){width="700" zoomable="yes"}

1. Geben Sie im Dialogfeld _[!UICONTROL Fallback-Wert eingeben]_ den Text ein, der als Fallback angezeigt wird, und klicken Sie dann auf **[!UICONTROL Hinzufügen]**.

   ![Geben Sie den Fallback-Text für das Token ein](./assets/sms-message-personalize-fallback-text.png){width="400"}

1. Wenn Ihre Personalisierungstoken platziert werden, klicken Sie auf **[!UICONTROL Speichern]** , um die Änderungen zu speichern und zum SMS-Authoring-Hauptarbeitsbereich zurückzukehren.

   Sie können die Nachricht mit den Token nach Bedarf weiter bearbeiten.

#### Links (URLs) zur Textnachricht hinzufügen

1. Klicken Sie nach Eingabe des Nachrichtentextes auf das Symbol _Link_ ( ![Verknüpfungssymbol](../assets/do-not-localize/icon-link.svg) ) rechts neben dem Textfeld.

1. Wählen Sie im Dialogfeld den Typ der zu verknüpfenden URLs aus:

   * **[!UICONTROL Landingpage]** - Wählen Sie diese Option, um eine der genehmigten Adobe Marketo Engage Design Studio-Landingpages aus Ihrer Marketo Engage-Instanz auszuwählen. Wählen Sie den Arbeitsbereich und dann die Landingpage aus.

   * **[!UICONTROL Externe URL]** - Dieser Typ ist eine externe URL, die Sie in das Textfeld eingeben.

1. Wenn Sie sich für die Verwendung einer Landingpage entscheiden, legen Sie die Tracking-Optionen fest.

   * **[!UICONTROL Tracking aktivieren]** - Aktivieren Sie dieses Kontrollkästchen, um das Tracking zu aktivieren. Dafür ist eine _Verkürzung_ der URL erforderlich. Bei einer Landingpage wird die Marketo Engage-Subdomäne für die gekürzte URL verwendet. Ein Beispiel für das gekürzte URL-Format wird angezeigt. Die tatsächliche URL wird erstellt, wenn die SMS an den Empfänger gesendet wird.

   * **[!UICONTROL mkt_tok einschließen]** - Aktivieren Sie dieses Kontrollkästchen, um die Aktivität gegen einen Benutzer zu verfolgen.

     >[!NOTE]
     >
     >Wenn Sie das Tracking zulassen, aber _[!UICONTROL mkt_tok einschließen]_ deaktivieren, enthält die Ziel-URL nach der Umleitung nicht den Abfragezeichenfolgenparameter `mkt_tok` . Dieser Parameter wird von Marketo Engage-Landingpages und Munchkin verwendet, um sicherzustellen, dass die Verfolgung von Personenaktivitäten (z. B. wenn sich eine Person von einer E-Mail abmeldet) gewährleistet ist. Deaktivieren Sie diese Option nur, wenn der Parameter Probleme auf Ihrer Website verursacht.<br/>
     >Weitere Informationen zur Verwendung von Munchkin-Trackingcodes auf Ihrer Website finden Sie in der [Marketo Engage-Dokumentation](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/additional-integrations/add-munchkin-tracking-code-to-your-website){target="_blank"}.

   ![Dialogfeld &quot;Link hinzufügen&quot;für SMS-Nachricht](./assets/sms-add-link-dialog.png){width="470"}

1. Wenn die Link-Optionen abgeschlossen sind, klicken Sie auf **[!UICONTROL Hinzufügen]** , um die Änderungen zu speichern und den URL-Link zur SMS-Nachricht hinzuzufügen.

### SMS-Eigenschaften festlegen

1. Geben Sie im Abschnitt _[!UICONTROL SMS-Eigenschaften]_ einen **[!UICONTROL Namen]** (erforderlich, maximal 100 Zeichen) und eine **[!UICONTROL Beschreibung]** (optional, maximal 300 Zeichen) für Ihre Nachricht ein.

   Für diese Felder sind Alpha-, numerische, Sonderzeichen zulässig. Die folgenden reservierten Zeichen sind **nicht erlaubt**: `\`, `/`, `:`, `*`, `?`, `"`, `<`, `>` und `|`.

1. Wählen Sie den **[!UICONTROL SMS-Typ]** aus:

   * Verwenden Sie `Marketing` für Werbetexte, für die die Zustimmung des Benutzers erforderlich ist.
   * Verwenden Sie `Transactional` für nicht kommerzielle Nachrichten, wie z. B. Bestellbestätigungen, Benachrichtigungen beim Zurücksetzen des Kennworts oder Versandinformationen.

1. Wählen Sie für die **[!UICONTROL SMS-Konfiguration]** eine der vordefinierten API-Konfigurationen aus.

   Diese Einstellung legt fest, welcher SMS Gateway-Dienstleister und welches Konto für den Nachrichtenversand verwendet wird.

1. Geben Sie die **[!UICONTROL Absendernummer]** &#x200B; ein, die Sie für Ihre Kommunikation verwenden möchten.

   ![Aktion durchführen - SMS senden](./assets/sms-properties.png){width="700" zoomable="yes"}

   Die Empfängernummer wird immer dem Feld `Lead.mobilePhone` im Marketo Engage zugeordnet.

### Simulieren des Inhalts der Textnachricht {#preview-test}

>[!CONTEXTUALHELP]
>id="ajo-b2b_sms_preview_simulate"
>title="Überprüfen des Inhalt-Renderings"
>abstract="Wenn Ihr Inhalt definiert wurde, können Sie ihn in der Vorschau anzeigen und überprüfen, ob das Rendering entsprechend dem verwendeten Kanal korrekt ist."

Wenn Ihr Nachrichteninhalt definiert ist, können Sie mithilfe von Testprofilen dessen Inhalt simulieren (in der Vorschau anzeigen). Wenn Sie personalisierten Inhalt eingefügt haben, können Sie anhand von Testprofildaten überprüfen, wie dieser Inhalt in der Nachricht angezeigt wird.

>[!IMPORTANT]
>
>Speichern Sie Ihre SMS-Nachricht, bevor Sie mit der Simulation der Textnachricht fortfahren.

1. Klicken Sie oben im SMS-Authoring-Arbeitsbereich auf **[!UICONTROL Inhalt simulieren]** .

1. Klicken Sie auf der Seite _[!UICONTROL Inhalt simulieren]_ auf **[!UICONTROL Personen hinzufügen]**.

1. Verwenden Sie die Seite _Inhalt simulieren_ , um die Leads zu verwalten, die für Ihr Testprofil verwendet werden.

   In der angezeigten Liste können Sie nach Leads suchen und diese (bis zu 10 Leads gleichzeitig) aus der Marketo Engage-Lead-Datenbank hinzufügen.

   Geben Sie zum Durchsuchen die gesamte E-Mail-Adresse ein und drücken Sie die _Eingabetaste_. Das entsprechende Lead-Profil wird zur Auswahl angezeigt.

   Die Vorschau aktualisiert die Personalisierungsfelder für das ausgewählte Profil.

   Alle hinzugefügten Leads werden links angezeigt.

   Sie können diese Liste verwalten, indem Sie weitere Personen hinzufügen und einzelne Leads aus der Profilliste löschen (sie werden nicht aus der Datenbank entfernt).

1. Inhalt für einen ausgewählten Lead simulieren.

   Wählen Sie eine der links aufgelisteten Leads aus. Die SMS-Vorschau auf der Seite wird für den ausgewählten Lead aktualisiert.

   Sie können auch einen Lead aus dem Selektor über dem Vorschaubereich auswählen, um die SMS-Vorschau auf der Seite für den entsprechenden Lead zu aktualisieren.

1. Um die Seite _[!UICONTROL Inhalt simulieren]_ zu verlassen und zum SMS-Authoring-Arbeitsbereich zurückzukehren, klicken Sie oben rechts auf **[!UICONTROL Schließen]** .

## Verwaltung von SMS-Einverständnissen

Es ist gesetzlich vorgeschrieben, Empfängern die Möglichkeit zu geben, sich vom Erhalt von Nachrichten einer Marke abzumelden und diese Entscheidung zu befolgen. Die Nichteinhaltung dieser Vorschriften birgt rechtliche Risiken für Ihre Marke. Diese Funktion hilft Ihnen auch, den Versand unerwünschter Nachrichten an Ihre Empfänger zu vermeiden, was dazu führen könnte, dass diese Ihre Nachrichten als Spam markieren und Ihrer Reputation schaden.

Wenn Sie diese Option bereitstellen, können SMS-Empfänger mit Opt-in- und Opt-out-Keywords antworten. Alle standardmäßigen Opt-in- und Opt-out-Suchbegriffe werden unterstützt und berücksichtigt sowie alle benutzerdefinierten Suchbegriffe, die beim SMS-Dienstanbieter konfiguriert sind. Bei der Abmeldung werden die Profile automatisch aus der Audience künftiger Marketing-Nachrichten entfernt.

Journey Optimizer B2B edition bietet die Möglichkeit, das Opt-out in SMS-Nachrichten mithilfe der folgenden Logik zu verwalten:

* Wenn ein Lead sich vom Erhalt von Nachrichten von Ihnen abgemeldet hat, wird das entsprechende Profil standardmäßig von nachfolgenden SMS-Sendungen ausgeschlossen

* Diese Lead-Einwilligung aus verschiedenen Quellen (z. B. AEP oder der SMS-Dienstleister) wird mit Journey Optimizer B2B edition synchronisiert. Derzeit unterstützt es nur einen einzelnen Zustimmungsstatus pro Lead auf Instanzenebene (ein Lead &quot;John Doe&quot;wird entweder für alle Promotion-SMS in der Instanz angemeldet oder von dieser abgemeldet). Es wird derzeit keine Anmeldung mit zweifacher Bestätigung für die Zustimmung auf Markenniveau oder auf Ebene der individuellen Abonnementliste unterstützt.
