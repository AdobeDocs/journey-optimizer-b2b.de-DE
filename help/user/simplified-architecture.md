---
title: Vereinfachte Architektureinrichtung
description: Richten Sie Journey Optimizer B2B edition auf der vereinfachten Architektur ein. Konfigurieren Sie XDM-Schemata, E-Mail-/SMS-Kanäle, Marketo Engage-Journey-Aktionen und Benutzende.
feature: Setup, Administration
role: Admin, Data Engineer
hide: true
hidefromtoc: true
source-git-commit: bbb9ff0deeb55c4cb132c6c97ec04f53a97339c6
workflow-type: tm+mt
source-wordcount: '1385'
ht-degree: 7%

---

# Vereinfachte Architektureinrichtung

Adobe Journey Optimizer B2B Edition ist jetzt in einer vereinfachten Architektur verfügbar. Mit dieser aktualisierten Architektur befinden sich Journey Optimizer B2B Edition und Marketo Engage nicht mehr im selben System und im selben Datenspeicher. Journey Optimizer B2B Edition empfängt Daten nur von Adobe Experience Platform. Es ist jedoch weiterhin auf Marketo Engage-Berechtigungen und einige Konfigurationsfunktionen angewiesen, um das System bereitzustellen und zu konfigurieren.

Die vereinfachte Architektur ist die Grundlage, auf der neue Funktionen in Adobe Journey Optimizer B2B edition freigeschaltet werden:

* **Vereinheitlichen und skalieren Sie Ihre Daten auf einfache Weise:** Die neue Plattform unterstützt komplexe Datenmodelle, einschließlich benutzerdefinierter Objekte, Einkaufsgruppen und Kontoereignisse. 

* **Mehrere Adobe Marketo Engage-Instanzen verbinden:** Verwalten und Vereinheitlichen von Daten aus mehreren Adobe Marketo Engage-Umgebungen an einem Ort.

* **Schützt Ihre Daten:** Erweiterte Datenschutz- und Sicherheitsfunktionen zum Schutz Ihrer Kundendaten. (_in Kürze verfügbar_)

* **Für die Zukunft entwickelt:** Mit diesem Upgrade sind Sie bereit für kontinuierliche Verbesserungen und Innovationen. 

Verwenden Sie für Umgebungen, die für diese Architektur bereitgestellt werden, die folgenden Konfigurationsrichtlinien.

## Namespaces und Schemata

Einen [&#x200B; Überblick finden Sie unter „B2B](https://experienceleague.adobe.com/en/docs/experience-platform/sources/connectors/adobe-applications/marketo/marketo-namespaces)Namespaces und -Schemata“ in der Experience Platform-Dokumentation.

### Einrichten der Umgebung

Richten Sie eine Postman-Umgebung ein, um den B2B-Namespace und das Dienstprogramm zur automatischen Schemaerstellung zu unterstützen.

* Sie können den Namespace und die Dienstprogrammsammlung zur automatischen Schemaerstellung sowie die Umgebung aus dem GitHub[Repository &#x200B;](https://github.com/adobe/experience-platform-postman-samples/tree/master/Postman%20Collections/CDP%20Namespaces%20and%20Schemas%20Utility).

* Informationen zur Verwendung von Experience Platform-APIs, einschließlich Details zum Erfassen von Werten für erforderliche Kopfzeilen und zum Lesen von Beispiel-API-Aufrufen, finden Sie [&#x200B; Handbuch Erste Schritte mit Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/landing/platform-apis/api-guide).

* Informationen zum Generieren Ihrer Anmeldeinformationen für Experience Platform-APIs finden Sie im Tutorial zum [Authentifizieren und Zugreifen auf Experience Platform-APIs](https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/api-authentication).

* Informationen zum Einrichten von Postman für Experience Platform-APIs finden Sie in den detaillierten Schritten unter [Postman in Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/postman).

Wenn eine Experience Platform-Entwicklerkonsole und Postman eingerichtet sind, können Sie jetzt damit beginnen, die entsprechenden Umgebungswerte auf Ihre Postman-Umgebung anzuwenden.

### Skripte ausführen

Bei der Einrichtung Ihrer Postman-Sammlung und -Umgebung können Sie das Skript über die Postman-Benutzeroberfläche ausführen.

Wählen Sie in der Benutzeroberfläche von Postman den Stammordner des Dienstprogramms zur automatischen Generierung und dann **Ausführen** aus der oberen Kopfzeile aus.

Wenn die Runner-Benutzeroberfläche angezeigt wird, stellen Sie sicher, dass alle Kontrollkästchen aktiviert sind, und wählen Sie dann **Dienstprogramm zur automatischen Generierung von Namespaces und Schemata ausführen**.

Bei einer erfolgreichen Anfrage werden die für B2B erforderlichen Namespaces und Schemata erstellt.

## XDM-Feldauswahl

Sie können die XDM-Felder verwalten, die in der gesamten Anwendung in der Benutzeroberfläche von Journey Optimizer B2B edition verfügbar sind. Diese Felder helfen, Ihre Instanz zu optimieren, indem sie nur die Felder verfügbar machen, die für das Erstellen von **_Journey_**, **_Einkaufsgruppen_** oder **_E-Mail-Personalisierungen_** relevant sind.

### XDM-Klassen

#### Standardklassen

Gehen Sie wie folgt vor, um Felder für standardmäßige XDM-Klassen zu definieren:

1. Navigieren Sie **[!UICONTROL Administration] > [!UICONTROL Konfigurationen]**.

1. Wählen Sie im Navigationsbereich die Option **[!UICONTROL XDM-Klassen]** aus.

1. Wählen Sie die Registerkarte **[!UICONTROL Standard]** aus, um die verfügbaren XDM-Klassen anzuzeigen:

   * XDM-Profil für Einzelpersonen

   * XDM-Geschäftskonto

#### Verwaltete Felder

Definieren, welche Felder im gesamten Programm verfügbar sind.

1. Klicken Sie auf das _Mehr Menü_ (**…**) und wählen Sie **[!UICONTROL Verwaltete Felder bearbeiten]**.

1. Überprüfen Sie die Liste der verfügbaren Felder (klicken Sie auf das Symbol _Informationen_ für Feldmetadaten).

1. Wählen Sie die Felder aus, die Sie einbeziehen möchten, und heben Sie die Auswahl für die nicht benötigten Felder auf.

1. Verwenden Sie den Regler **[!UICONTROL Nur ausgewählte Felder anzeigen]**, um Ihre Auswahl zu überprüfen.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

#### Aktualisierbare Felder

Journey Wählen Sie aus, welche Felder durch die Aktionen **[!UICONTROL Kontoprofil aktualisieren]** oder **[!UICONTROL Personenprofil aktualisieren]** geändert werden können.

1. Klicken Sie auf das _Mehr Menü_ (**…**) und wählen Sie **[!UICONTROL Aktualisierbare Felder bearbeiten]**.

1. Wählen Sie **[!UICONTROL Schema]** und dann **[!UICONTROL Datensatz]** aus.

   Diese Schemata und Datensätze werden von Ihrem Unternehmen bereitgestellt.

1. Überprüfen Sie die Liste der aktualisierbaren Felder (klicken Sie bei Metadaten auf _Informationssymbol_).

   Nur die verwalteten Felder können bearbeitet werden.

1. Wählen Sie die Felder aus, die Sie für das Update von Journey verfügbar machen möchten.

1. Klicken Sie auf **Speichern**.

### Relationale Schemata

Wählen Sie [relationale Schemata](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/relational) zur Verwendung beim **_Journey-Decisioning_** und **_Personalisierung_** aus. Derzeit sind diese Schemata für Anwendungsfälle von benutzerdefinierten Objekten vorgesehen. In Zukunft können relationale Schemata auch für andere Objektanwendungsfälle verwendet werden.

1. Wählen Sie die Registerkarte **[!UICONTROL Relational]** aus.

1. Klicken Sie **[!UICONTROL Relationale XDM-Klasse auswählen]**.

   Derzeit wird nur das benutzerdefinierte Objekt „Viele-zu-eins-Konto“ unterstützt.

1. Überprüfen Sie die Liste der Schemafelder (klicken Sie auf das Symbol _Informationen_, um die Metadaten anzuzeigen).

1. Wählen Sie die Felder aus, die Sie einbeziehen möchten.

1. Verwenden Sie den Regler **[!UICONTROL Nur ausgewählte Felder anzeigen]**, um Ihre Auswahl zu überprüfen.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

>[!NOTE]
>
>Beachten Sie, dass relationale Schemata die folgenden Konfigurationen aufweisen müssen:
>
><li>Verhalten: Datensatz
>&gt; <li>Segmentierung: Aktiviert
>&gt; <li>Beziehungstyp: Viele-zu-eins
>&gt; <li>Referenzschema: [B2B-Konto - XDM Business Account-Schema](https://experienceleague.adobe.com/en/docs/platform-learn/tutorials/schemas/create-schemas-for-b2b-data)
>&gt; <li>Erforderliche Felder: Primärer Schlüssel, Fremdschlüssel und Versionsdeskriptor
>&gt; <li>Zugeordneter Datensatz: definiert und dem Schema zugeordnet

### Ereignisse

Wählen Sie die Erlebnisereignisse aus, die in der **_Journey-Entscheidungsfindung verwendet werden_**.

1. Wählen Sie die **[!UICONTROL Ereignisse]** aus.

1. Klicken Sie **[!UICONTROL Erlebnisereignis auswählen]**.

1. Klicken Sie **[!UICONTROL Ereignistyp auswählen]** wählen Sie den Ereignistyp aus und klicken Sie auf **[!UICONTROL Auswählen]**.

1. Klicken Sie **[!UICONTROL Felder auswählen]** wählen Sie die gewünschten Felder aus und klicken Sie auf **[!UICONTROL Auswählen]**.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

## E-Mail-Konfiguration

Folgendes sollte konfiguriert werden, um E-Mails aus Journey Optimizer B2B edition zu senden.  

[https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols)

### Protokolle für Tracking und E-Mail-Versand

1. [DNS-Einträge für E-Mail erstellen](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols#create-dns-records-for-landing-pages-and-email)

1. [Einrichten von SPF und DKIM](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols#set-up-spf-and-dkim)

1. [Einrichten von DMARC](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols#set-up-dmarc)

1. [MX-Einträge für Ihre Domain einrichten](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols#set-up-mx-records-for-your-domain)

1. auf die Zulassungsliste setzen [Ausgehende IP-Adressen zu hinzufügen](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols#outbound-ip-addresses)

1. Wenn Sie den dedizierten IP-Pool freigeben müssen, wenden Sie sich bezüglich der Durchführbarkeit und der unterstützten Einrichtung an das Zustellbarkeits-Team.

### E-Mail-Kanalkonfigurationen

In der vereinfachten Architektur werden E-Mail-Einstellungen über die Marketo Engage-Benutzeroberfläche konfiguriert. Führen Sie die Einrichtungsschritte für die E-Mail aus: [https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/setup-steps](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/setup-steps)

[https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/channels/configure-channels-emails](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/channels/configure-channels-emails)

### Kommunikationsbeschränkungen

1. Wählen Sie in der linken Navigation **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]**.

1. Wählen Sie im Navigationsbereich die Option **[!UICONTROL Kommunikationsgrenze]** aus.

1. Erstellen Sie einen Regelsatz für globale Kommunikationsbeschränkungen (dieser Regelsatz wird standardmäßig in jeder Journey Optimizer B2B edition-Instanz erstellt).

   Es gibt keine Kommunikationsbeschränkung, wenn der globale Regelsatz nicht erstellt wird.

<!-- In the future, you can also add local communication limit rule sets (AJO B2C doc can be found here [https://experienceleague.adobe.com/en/docs/journey-optimizer/using/conflict-prioritization/capping-rules/rule-sets](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/conflict-prioritization/capping-rules/rule-sets). We may need a small update for our B2B version.) -->

### Freigegebene Kommunikationsbeschränkungen

Innerhalb der neuen Architektur haben Journey Optimizer B2B edition und Marketo Engage standardmäßig unabhängige Kommunikationsbeschränkungen.

Wenn Sie möchten, dass die Marketo Engage-Instanz das in der Journey Optimizer-B2B edition-Instanz festgelegte Kommunikationslimit teilt, wenden Sie sich an den Adobe-Support, um Hilfe bei der Konfiguration zu erhalten, oder öffnen Sie ein Support-Ticket. Auf Anfrage kann das Engineering-Team die Freigabe von Kommunikationsbeschränkungen zwischen Journey Optimizer B2B edition und einer oder mehreren Marketo Engage-Instanzen aktivieren.

Derzeit muss das freigegebene Kommunikationslimit in der Marketo Engage-Instanz über einen API-Aufruf eingerichtet werden.

Wenn zum Beispiel:

* Die munchkinId der Journey Optimizer B2B edition-Instanz ist `JKL-567-MNO`.
* Die munchkinId der Marketo Engage-Instanz ist `ABC-123-DEF` und befindet sich im SJ-Rechenzentrum

Die API-Anfrage sollte etwa wie folgt aussehen:

```
curl --location --request POST 'http://sjrest2a.marketo.org/rest/v1/fm.json?_munchkinId=ABC-123-DEF&featureName=Mktmail%20Config&paramName=ajoB2bMappingMunchkinId&dataType=string&value=JKL-567-MNO'
```

## SMS-Kanalkonfiguration

Siehe [_SMS-_](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/channels/configure-channels-sms)) für detaillierte Informationen.

## Marketo Engage-Aktionen von Journey

Sie können eine oder mehrere Remote-**_Marketo Engage_**-Instanzen für die Verwendung mit den folgenden Journey-Aktionen konfigurieren:

* Zur Marketo-Liste hinzufügen
* Aus Marketo-Liste entfernen
* Zur Marketo-Anfragekampagne hinzufügen

Führen Sie die folgenden Schritte aus, um diese Verbindungen zu konfigurieren:

1. Navigieren Sie **[!UICONTROL Administration] > [!UICONTROL Konfigurationen]**.

1. Wählen Sie im Navigationsbereich die Option **[!UICONTROL XDM-Klassen]** aus.

1. Wählen Sie die **[!UICONTROL Integrationen]** aus.

1. Klicken Sie **[!UICONTROL Verbindung erstellen]**.

1. Geben Sie **[!UICONTROL Name]** und &quot;**[!UICONTROL &quot;]**.

1. Wählen Sie **[!UICONTROL Richtlinie aktualisieren]** für übereinstimmende Personendatensätze aus.

1. Geben Sie **[!UICONTROL Munchkin ID]**, **[!UICONTROL Client ID]**, **[!UICONTROL Client Secret]** ein und klicken Sie auf **[!UICONTROL Mit Marketo verbinden]**.

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

## Onboarding von Benutzern

Einen Überblick [&#x200B; Sie auf der Seite &#x200B;](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/user-management)Benutzerverwaltung“.

### Vorhandene Benutzergruppen

Wenn alle bestehenden Journey Optimizer B2B edition-Benutzenden Zugriff auf die neue Architektur benötigen, verwenden Sie die bestehende Journey Optimizer B2B edition-Benutzergruppe. Ein System- oder Produktadministrator kann die folgenden Schritte ausführen.

1. Erstellen Sie ein Produktprofil in der dedizierten Marketo Engage.

1. Fügen Sie eine vorhandene Benutzergruppe zum erstellten Produktprofil hinzu.

Die Profile gewähren allen Rollen und Berechtigungen, die dieser Benutzergruppe bereits zugewiesen sind. Diese sollte bereits für den Zugriff der Benutzer auf Journey Optimizer B2B edition konfiguriert sein. Wenn nur eine Untergruppe von Benutzern auf die neue Architektur zugreifen soll, führen Sie die folgenden Schritte aus. Weitere Informationen finden Sie in [aktuellen Dokumentation](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/user-management).

### Erstellen einer neuen Benutzergruppe

1. Erstellen Sie ein Produktprofil in der dedizierten Marketo Engage-Instanz.
1. Erstellen Sie eine Benutzergruppe für neue Benutzer.
1. Wählen Sie die erforderlichen Produktprofile aus und weisen Sie sie der Benutzergruppe zu:

   * Das von Ihnen erstellte Marketo Engage-Profil
   * Adobe Experience Platform-Profile
      * AEP-default-all-users
      * Adobe Experience Platform – Datenerfassung
      * Zugriff auf alle Datenerfassungen

1. Fügen Sie die Benutzer der Benutzergruppe hinzu.
1. Fügen Sie eine neue Benutzergruppe zu Journey Optimizer B2B edition-Rollen in Experience Platform hinzu.
