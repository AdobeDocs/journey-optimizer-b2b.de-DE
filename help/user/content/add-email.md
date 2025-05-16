---
title: Hinzufügen einer E-Mail zu Ihrem Journey
description: Erfahren Sie, wie Sie E-Mail-Aktionen in Adobe Journey Optimizer B2B hinzufügen, definieren und optimieren. Verbessern Sie Ihre Account-Journey mit zielgerichteter E-Mail-Kommunikation.
feature: Email Authoring, Account Journeys
role: User
exl-id: 21a6ce0f-b59d-4be2-abc3-fda5c6a6334f
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '963'
ht-degree: 0%

---

# Hinzufügen einer E-Mail zu Ihrem Journey

Verwenden Sie Adobe Journey Optimizer B2B edition, um E-Mail-Nachrichten über Account Journey an Ihre Kunden zu senden. Sie können im E-Mail-Design-Bereich Nachrichten erstellen, personalisieren und in der Vorschau anzeigen. Alternativ können Sie auch eine E-Mail senden, die bereits in der verbundenen Marketo Engage-Instanz definiert ist.

>[!NOTE]
>
>Wenn Sie zum ersten Mal eine E-Mail senden, stellen Sie sicher, dass der E-Mail-Kanal in Adobe Marketo Engage konfiguriert ist. Weitere Informationen finden Sie unter [Protokolle für Tracking und E-Mail-Versand](../start/email-protocols.md).

## Hinzufügen eines E-Mail-Aktionsknotens in einer Journey

Sie können den E-Mail-Versand auf einer Journey einrichten, wenn Sie [einen Knoten _[!UICONTROL Aktion durchführen]_ hinzufügen ](../journeys/action-nodes.md) Folgendes tun:

1. Wählen Sie für _[!UICONTROL Ziel]_ Aktion auf“ **[!UICONTROL Personen]**.

1. Wählen Sie für _[!UICONTROL Aktion für Personen]_ die Option **[!UICONTROL E-Mail senden]**.

1. Wählen Sie für _[!UICONTROL E-Mail-]_), wie Sie die zu sendende E-Mail beziehen möchten.

   ![Aktion durchführen - E-Mail senden](assets/journey-node-send-email.png){width="700" zoomable="yes"}

   * Wählen Sie **[!UICONTROL Neue E-Mail erstellen]**, um die E-Mail nativ in Journey Optimizer B2B edition zu erstellen.

     Mit dieser Option können Sie den E-Mail-Inhalt nativ in Journey Optimizer B2B edition verwalten. Klicken Sie **[!UICONTROL E-Mail erstellen]**, um das Dialogfeld _Neue E-Mail erstellen_ zu öffnen. Sie können ein neues E-Mail-Inhalts-Asset <!-- or duplicate an existing email content asset-->.

     Geben Sie in das Dialogfeld einen eindeutigen **[!UICONTROL Namen]** für die E-Mail und eine **[!UICONTROL Betreffzeile]** ein und klicken Sie dann auf **[!UICONTROL Erstellen]**.

     ![Dialogfeld „Neue E-Mail erstellen“ - neue E-Mail](assets/create-new-email-no-duplicate.png){width="400"}

     Im Abschnitt _[!UICONTROL E]_ Mail-Eigenschaften“ der E-Mail-Inhaltsseite sind die Felder _[!UICONTROL Von E-Mail]_ und _[!UICONTROL Antwort an Adresse]_ bereits konfiguriert. Sie können Werte für die Felder _[!UICONTROL Absendername]_ und _[!UICONTROL Beschreibung]_ (optional) eingeben.

     Definieren Sie die E[Mail](#define-the-email-settings)Einstellungen und klicken Sie auf **[!UICONTROL E-Mail-Inhalt bearbeiten]** um [Inhalt zu entwerfen](./email-authoring.md).

     <!-- +++New email {#new-email}
     When you want to create an email using an empty canvas or an email template, use the _[!UICONTROL New email]_ option. 

     1. In the dialog, choose **[!UICONTROL New email]**.

     1. Enter a unique **[!UICONTROL Name]** for the email and a **[!UICONTROL Subject line]**.

        ![Create new email dialog - new email](assets/create-new-email.png){width="400"}

     1. Click **[!UICONTROL Create]**.

       In the _[!UICONTROL Email properties]_ section of the email content page, the _[!UICONTROL From email]_ and _[!UICONTROL Reply to address]_ fields are already configured. You can enter values for the _[!UICONTROL From name]_ and _[!UICONTROL Description]_ (optional) fields.

     1. Click **[!UICONTROL Edit email]** to define the email [settings](#define-the-email-settings) and design the [content](./email-authoring.md).

     +++

     +++Duplicate existing email {#duplicate-email}
     When you want to create an email using an existing email from the current journey or from another journey, use the Duplicate existing journey option. You can make changes to the duplicated email according to your objective for the journey node.

     1. In the dialog, choose **[!UICONTROL Duplicate existing email]**.

     1. For **[!UICONTROL Existing email to duplicate]**, click the _Select email_ icon and select the email you want to duplicate and use for the journey node.

      You can filter the list of emails by entering a text string in the search field to match the email name.

      ![Select email](assets/create-new-email-duplicate-select-email.png){width="600" zoomable="yes"}

      Select the checkbox for the email that you want to duplicate and click **[!UICONTROL Select]**. 

     1. Enter a unique **[!UICONTROL Name]** for the email and a **[!UICONTROL Subject line]**.

        ![Create new email dialog - duplciate existing email](assets/create-new-email.png){width="400"}

     1. Click **[!UICONTROL Create]**.

        In the _[!UICONTROL Email properties]_ section of the email content page, the _[!UICONTROL From email]_ and _[!UICONTROL Reply to address]_ fields are already configured. You can enter values for the _[!UICONTROL From name]_ and _[!UICONTROL Description]_ (optional) fields.

     1. If needed, click **[!UICONTROL Edit email]** to modify the email [settings](#define-the-email-settings) and [content](./email-authoring.md).

     +++
   —>
   * Wählen Sie **[!UICONTROL E-Mail aus Adobe Marketo Engage auswählen]**, um eine der vorab erstellten E-Mails in Marketo Engage zu verwenden und als Teil der Journey zu senden.

     ![Marketo Engage-E-Mail auswählen](./assets/email-select-marketo.png){width="500" zoomable="yes"}

     Mit dieser Option wird der Knoten festgelegt und der E-Mail-Inhalt muss auf der Journey nicht weiter definiert werden.

## E-Mail-Einstellungen definieren

Wenn die Registerkarte **[!UICONTROL Details]** im Bedienfeld _Zusammenfassung_ auf der rechten Seite ausgewählt ist, scrollen Sie nach unten, um die E-Mail-Optionen anzuzeigen und festzulegen.

![E-Mail-Einstellungen](./assets/email-summary-details-settings.png){width="600" zoomable="yes"}

| Option | Beschreibung |
| ------ | ----------- |
| [!UICONTROL Absendername] | Der in der E-Mail-Kopfzeile verwendete Absendername. Geben Sie den Absendernamen so ein, wie er dem Empfänger angezeigt werden soll. Klicken Sie auf das _Personalisieren_-Symbol ( ![Personalisieren-Symbol](../assets/do-not-localize/icon-personalize.svg) ), um ein Personalisierungs-Token in diesem Feld zu verwenden. |
| [!UICONTROL Von E-Mail] | Die in der E-Mail-Kopfzeile verwendete Absenderadresse. Der Standardwert wird aus den [E-Mail-Kanal-Versandeinstellungen](../admin/configure-channels-emails.md#delivery-settings) übernommen. Klicken Sie auf das _Personalisieren_-Symbol ( ![Personalisieren-Symbol](../assets/do-not-localize/icon-personalize.svg) ), um ein Personalisierungs-Token in diesem Feld zu verwenden. |
| [!UICONTROL Antwortadresse] | Die in der E-Mail-Kopfzeile verwendete Absenderadresse. Der Standardwert wird aus den [E-Mail-Kanal-Versandeinstellungen](../admin/configure-channels-emails.md#delivery-settings) ([!UICONTROL From Label]) gefüllt. Geben Sie die E-Mail-Adresse ein, die Sie ausfüllen möchten, wenn der Empfänger die Antwortfunktion verwendet (sie kann anders oder mit der Absenderadresse identisch sein). Klicken Sie auf das _Personalisieren_-Symbol ( ![Personalisieren-Symbol](../assets/do-not-localize/icon-personalize.svg) ), um ein Personalisierungs-Token in diesem Feld zu verwenden. |
| [!UICONTROL Betreffzeile] | Der Text, der im Feld Betreff für die E-Mail angezeigt wird. Der Standardwert wird aus dem Text gefüllt, den Sie im Dialogfeld _[!UICONTROL Neue E-Mail erstellen]_ eingegeben haben. Sie können den Text bei Bedarf ändern. Klicken Sie auf das _Personalisieren_-Symbol ( ![Personalisieren-Symbol](../assets/do-not-localize/icon-personalize.svg) ), um ein Personalisierungs-Token im Feld zu verwenden.<!-- Click the AI Assistant button ( ![AI Assistant icon](../../assets/do-not-localize/icon-gen-ai.svg){width="30" zoomable="no"} ) to generate the subject line based on the current email content.--> |
| [!UICONTROL Operative E-Mail] | Aktivieren Sie das Kontrollkästchen, wenn Sie die E-Mail als betriebsbereit kennzeichnen möchten. Operative E-Mails sind von Opt-out-/Abmeldelisten und von Kommunikationsbeschränkungen ausgeschlossen. Wählen Sie diese Option nur aus, wenn der Empfänger die E-Mail-Nachricht nicht als unerwünschte Werbenachricht (SPAM) betrachten kann. |
| [!UICONTROL Als Webseite anzeigen] | Aktivieren Sie das Kontrollkästchen, um einen Link zu einer Web-Seite einzufügen, die aus dem Inhalt der E-Mail-Nachricht generiert wird. E-Mail-Nachrichten verfügen über eingeschränktere Funktionen als Web-Seiten. Daher ist sie für JavaScript, erweitertes CSS und Formulare nützlich. Der Text, der zum Generieren des Links verwendet wird, wird in den [Versandeinstellungen des E-Mail-Kanals](../admin/configure-channels-emails.md#delivery-settings) konfiguriert ([!UICONTROL Als Webseite anzeigen, HTML] und [!UICONTROL Als Webseite anzeigen, Text ]). |
| [!UICONTROL Öffnungs-Tracking deaktivieren] | Aktivieren Sie das Kontrollkästchen, wenn Sie die Aktivität zum Öffnen von E-Mails nicht verfolgen möchten. Wenn die Funktion deaktiviert ist, wird die Anzahl der Öffnungen von E-Mails nur dann erhöht, wenn eine eindeutige Person die E-Mail öffnet. Sie können [Tracking für E-Mail-Inhaltslinks verwalten](./email-authoring.md#content-authoring---link-tracking) wenn Sie den Inhalt des E-Mail-Textkörpers entwerfen. |
| [!UICONTROL Preheader] | Aktivieren Sie das Kontrollkästchen, um einen Preheader einzuschließen. Ein Preheader ist der kurze Zusammenfassungstext, der in einigen E-Mail-Clients nach der Betreffzeile angezeigt wird. Sie bietet in der Regel eine kurze Zusammenfassung der E-Mail und besteht normalerweise aus einem einzigen Satz. Geben Sie den Zusammenfassungstext in das Feld <!-- , or click the AI Assistant button ( ![AI Assistant icon](../../assets/do-not-localize/icon-gen-ai.svg){width="30" zoomable="no"} ) to generate summary text based on the current email content -->. |
| [!UICONTROL Felder als CC-Adressen] | Wählen Sie, falls verfügbar, bis zu 25 Lead- oder Firmenfelder aus, die in Marketo Engage mithilfe des `Email` eingerichtet werden. |

## Prüfen von Warnhinweisen

Während Sie den Inhalt Ihrer E-Mail-Nachricht entwerfen, werden Warnhinweise in der Benutzeroberfläche (oben rechts auf der Seite) angezeigt, wenn wichtige Einstellungen fehlen. Wenn diese Schaltfläche nicht angezeigt wird, treten keine Probleme auf.

![E-Mail-Warnungen](./assets/email-alerts.png){width="600" zoomable="yes"}

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
