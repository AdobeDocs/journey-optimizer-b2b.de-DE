---
title: SMS-Konfigurationen
description: Erfahren Sie, wie Sie Verbindungen zu unterstützten SMS-Anbietern für die Verwendung von Journey Optimizer B2B edition SMS Messaging konfigurieren.
feature: Setup
source-git-commit: c3352db2235af08e31ba7e4d8690bc9e330dd41f
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 6%

---

# SMS-Konfigurationen

Adobe Journey Optimizer B2B edition sendet Textnachrichten über SMS-Dienstleister (oder SMS Gateway Provider). Konfigurieren Sie vor der Erstellung Ihrer SMS-Nachricht Ihren Dienstleister über die Einstellungen für _Administrator_.

## SMS-Gateway-Dienstleister

Adobe Journey Optimizer B2B edition lässt sich derzeit mit Drittanbietern integrieren, die unabhängig voneinander Textnachrichtendienste anbieten. Unterstützte Anbieter für Textnachrichten sind Sinch, Twilio und Infobip.

Bevor Sie einen SMS-Kanal in Adobe Journey Optimizer B2B edition konfigurieren, müssen Sie ein Konto bei einem dieser Anbieter erstellen, um Ihr API-Token und Ihre Service-ID zu erhalten. Diese Anmeldeinformationen sind erforderlich, um die Verbindung zwischen Adobe Journey Optimizer B2B edition und dem entsprechenden Provider zu konfigurieren.

>[!IMPORTANT]
>
>Ihre Nutzung von Textnachrichten-Services unterliegt zusätzlichen Bedingungen des jeweiligen Anbieters. Als Drittanbieterlösungen stehen Benutzern von Adobe Journey Optimizer B2B edition über eine Integration Sinch, Twilio und Infobip zur Verfügung. Adobe kontrolliert keine Produkte von Drittanbietern und ist nicht für diese verantwortlich. Wenden Sie sich bei Problemen oder Ersuchen um Unterstützung im Zusammenhang mit den Textnachrichtendiensten (SMS) an Ihren Provider.

## Vorhandene SMS-API-Konfiguration überprüfen

>[!NOTE]
>
>Die beschriebenen Einstellungen sind nur für Benutzer mit SMS-Administratorrechten zugänglich.

1. Erweitern Sie im linken Navigationsbereich den Abschnitt **[!UICONTROL Administrator]** und klicken Sie auf **[!UICONTROL Kanäle]**.

   ![Zugriff auf die Konfiguration der SMS-API-Anmeldeinformationen](./assets/config-sms-api.png){width="800" zoomable="yes"}

1. Wählen Sie im Navigationsfenster **[!UICONTROL API-Anmeldeinformationen]** aus.

   Auf der Seite werden die verfügbaren API-Konfigurationen für Ihre Instanz aufgelistet.

1. Klicken Sie bei Bedarf auf das Symbol _Filter_ ( ![Symbol für Filter ein- oder ausblenden](../assets/do-not-localize/icon-filter.svg) ) und wählen Sie Optionen aus, um die Liste der konfigurierten API-Anmeldeinformationen vom SMS-Dienstleister oder -Ersteller anzuzeigen.

   ![Klicken Sie auf das Filtersymbol, um die Liste der API-Anmeldeinformationen zu verfeinern.](./assets/config-sms-api-filter.png){width="600" zoomable="yes"}

## Erstellen neuer API-Anmeldeinformationen für einen SMS-Dienstanbieter

>[!BEGINTABS]

>[!TAB Sinch]

_So konfigurieren Sie Sinch wie Ihren SMS-Provider mit Adobe Journey Optimizer B2B edition:_

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

_So konfigurieren Sie Twilio als Ihren SMS-Provider mit Adobe Journey Optimizer B2B edition:_

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
