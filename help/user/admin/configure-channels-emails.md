---
title: Konfigurationen des E-Mail-Kanals
description: Konfigurieren Sie E-Mail-Versandeinstellungen, Kommunikationsbeschränkungen und Authentifizierungsprotokolle, um die Zustellbarkeit in Journey Optimizer B2B edition zu optimieren.
feature: Setup, Channels
role: Admin
exl-id: fb16b5e5-f1a5-4e59-b8c6-56985f03225a
source-git-commit: 7d150069e7af582d837411aa52f6e8caa2b5e89e
workflow-type: tm+mt
source-wordcount: '1648'
ht-degree: 0%

---

# E-Mail-Kanalkonfigurationen

Adobe Journey Optimizer B2B edition nutzt die Kanalfunktionen und die Ereignisverfolgung in Marketo Engage. Admins sollten sicherstellen, dass die Versand- und Tracking-Konfigurationen vorhanden sind, um den Kanalversand für Marketing-Fachleute zu ermöglichen. Informationen zu den Protokollen, die für den E-Mail-Versand und das Tracking über Marketo Engage erforderlich sind, finden Sie unter [Protokolle für das Tracking und den E-Mail-Versand](../start/email-protocols.md).

## Versandeinstellungen

Die standardmäßigen E-Mail-Einstellungen werden verwendet, wenn Marketing-Experten eine E-Mail auf einer Konto-Journey erstellen. Die Einstellungen für den E-Mail-Versand finden Sie unter **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]**. Wählen _[!UICONTROL im]_ unter „E-Mail“ die Option **[!UICONTROL Versandeinstellungen]**.

![Zugriff auf die E-Mail-Versandeinstellungen](./assets/config-email-delivery-email-header.png){width="800" zoomable="yes"}

Die Einstellungen sind in Journey Optimizer B2B edition schreibgeschützt. Klicken Sie **[!UICONTROL oben]** auf „Einstellungen bearbeiten“, um auf die Konfigurationsoptionen in der verbundenen Marketo Engage-Instanz zuzugreifen.

>[!NOTE]
>
>Um auf diese Einstellungen in Adobe Marketo Engage zugreifen und sie bearbeiten zu können, benötigen Sie die Berechtigung eines Produktadministrators.

Wählen Sie jede der folgenden Registerkarten aus, um die aktuellen Einstellungen zu überprüfen.

### [!UICONTROL E-Mail-Kopfzeilenparameter] {#email-header}

Die E-Mail-Header-Parameter definieren die Standardwerte für Folgendes:

* **[!UICONTROL Von E]** Mail: Die E-Mail-Adresse, die im Feld _Von_ in der E-Mail-Kopfzeile aufgeführt ist.

* **[!UICONTROL From Label]** - Der angezeigte Name für die E-Mail-Absenderadresse.

* **[!UICONTROL HTML abmelden]** - Die HTML (für unterstützte E-Mail-Clients), die in nicht operativen E-Mails angezeigt wird, um Empfängerinnen und Empfängern Abmeldeaktionen zu erklären. Dieser Text und die Links werden unten angehängt.

* **[!UICONTROL Abmeldetext]** - Der Text, der in nicht-operativen E-Mails angezeigt wird, um Empfängerinnen und Empfängern die Abmeldeaktionen zu erklären. Dieser Text und die Links werden unten angehängt.

* HTML **[!UICONTROL Als Webseite anzeigen]** - Die HTML (für unterstützte E-Mail-Clients), die für _Als Webseite anzeigen_ verwendet wird, die einen Link zum Anzeigen einer E-Mail in einem Browser bereitstellt.

* **[!UICONTROL Als Webseitentext anzeigen]** - Der für „Als _anzeigen_ verwendete Klartext, der einen Link zum Anzeigen einer E-Mail in einem Browser bereitstellt.

### [!UICONTROL Branding-Domains] {#branding-domains}

Um die Branding-Domains zu überprüfen, klicken Sie auf die Registerkarte **[!UICONTROL Branding-Domains]** .

![Zugriff auf die Einstellungen der Branding-Domains](./assets/config-email-delivery-branding-domains.png){width="700" zoomable="yes"}

Diese Einstellung definiert Ihre primäre Domain für einen oder mehrere Arbeitsbereiche in der verbundenen Marketo Engage-Instanz. Für neue E-Mails wird diese Domain als Standard verwendet, aber Marketing-[&#x200B; können sie pro E-Mail überschreiben](../content/add-email.md#define-the-email-settings). Weitere Informationen zur Definition der Standard-Branding-Domain finden Sie in der [Dokumentation zu Marketo Engage](https://experienceleague.adobe.com/de/docs/marketo/using/product-docs/administration/email-setup/add-multiple-branding-domains/edit-your-default-branding-domain){target="_blank"}.

>[!NOTE]
>
>Wenn Sie mehrere Marken vermarkten und jeweils eigene Marken-Tracking-Links verwenden möchten, können Sie eine zusätzliche Branding-Domain hinzufügen. Weitere Informationen zum Hinzufügen mehrerer Branding-Domains finden Sie in der [Dokumentation zu Marketo Engage](https://experienceleague.adobe.com/de/docs/marketo/using/product-docs/administration/email-setup/add-multiple-branding-domains/add-an-additional-branding-domain){target="_blank"}.

### [!UICONTROL Benutzerdefinierte Kopfzeilenoptionen] {#custom-header-options}

Um die benutzerdefinierten Kopfzeilenoptionen zu überprüfen, klicken Sie auf die **[!UICONTROL Benutzerdefinierte Kopfzeilenoptionen]** .

![Zugriff auf die benutzerdefinierten Header-Optionen](./assets/config-email-delivery-custom-header.png){width="700" zoomable="yes"}

Wenn _[!UICONTROL Strict Transport Security]_ aktiviert ist, wird garantiert, dass Tracking-Links über HTTPS bereitgestellt werden (nur für Abonnements mit Tracking-Links, die durch SSL gesichert sind).

## Kommunikationsbeschränkungen

Kommunikationsbeschränkungen steuern die Anzahl der E-Mails, die ein Kontakt von Ihrer Organisation erhält. Die von Ihnen festgelegten Beschränkungen werden von Journey Optimizer B2B edition und der verbundenen Marketo Engage-Instanz gemeinsam genutzt. Durch die Festlegung dieser Beschränkungen wird sichergestellt, dass ein Lead in einem bestimmten Zeitraum nicht mehr als eine maximale Anzahl von E-Mails erhält.

>[!AVAILABILITY]
>
>Die Kommunikationsbeschränkungen sind für Journey Optimizer-B2B edition-Umgebungen verfügbar, die auf der [vereinfachten Architektur“ bereitgestellt &#x200B;](../simplified-architecture.md).

Beispielsweise stellt das System mit einem definierten Limit von fünf E-Mails pro Tag sicher, dass ein Kontakt innerhalb eines Tages keine sechste E-Mail erhält, indem es die sechste E-Mail unterdrückt. Bei gemeinsam genutzten Kommunikationsbeschränkungen zwischen Journey Optimizer B2B edition und Marketo Engage werden die Regeln für Kommunikationsbeschränkungen an einem Ort definiert. Die sechste E-Mail wird unabhängig von der Sendeaktion von Journey Optimizer B2B edition oder Marketo Engage unterdrückt.

Für alle Marketo Engage-Produktionsinstanzen sind standardmäßig Kommunikationsbeschränkungen definiert (weitere Informationen finden Sie in der [&#x200B; zu &#x200B;](https://experienceleague.adobe.com/de/docs/marketo/using/product-docs/administration/email-setup/enable-communication-limits){target="_blank"}Marketo Engage). Um freigegebene Kommunikationsbeschränkungen zu verwenden, definieren Sie die Regeln in Journey Optimizer B2B edition und erweitern Sie die Freigabe dieser Beschränkungen auf die Marketo Munchkin-Codes.

>[!IMPORTANT]
>
>Wenden Sie sich an Ihr Adobe-Account-Management-Team, um den Kommunikationsregelsatz auf die Marketo Munchkin-Codes zu erweitern. Diese Konfiguration ist in der Regel Teil des Onboarding-Prozesses.

Um die Regeln für Kommunikationsbeschränkungen zu überprüfen oder festzulegen, gehen Sie zu **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]**. Wählen _[!UICONTROL im]_ unter „E-Mail“ die Option **[!UICONTROL Kommunikationsbeschränkungen]** aus.

![Zugriff auf die Konfiguration der Kommunikationsbeschränkungen](./assets/config-email-communication-limits.png){width="700" zoomable="yes"}

Standardmäßig gibt es einen globalen Regelsatz, mit dem Sie je nach Ihren Anforderungen mehrere Regeln definieren, aktivieren und deaktivieren können. Klicken Sie auf den Namen des Regelsatzes, um die Regelliste anzuzeigen.

### Erstellen einer Regel

1. Klicken **[!UICONTROL oben]** auf „Regel erstellen“.

   ![Zugriff auf die Konfiguration der Kommunikationsbeschränkungen](./assets/config-email-communication-limits-create-rule-select.png){width="600" zoomable="yes"}

1. Geben Sie den **[!UICONTROL Regelnamen“]**.

1. Legen Sie den **[!UICONTROL Begrenzungsbetrag]** fest.

   Geben Sie den Wert ein, oder klicken Sie auf den _Nach_ oder _Nach-unten_ Pfeil rechts, um den Wert zu erhöhen oder zu verkleinern.

1. Wählen Sie den Wert **[!UICONTROL Begrenzungshäufigkeit zurücksetzen]** entsprechend der Art und Weise, wie Sie den Zeitraum für das Limit definieren möchten.

   Sie können zwischen _[!UICONTROL Stündlich]_, _[!UICONTROL Täglich]_, _[!UICONTROL Wöchentlich]_ oder _[!UICONTROL Monatlich]_ wählen.

   ![Zugriff auf die Konfiguration der Kommunikationsbeschränkungen](./assets/config-email-communication-limits-create-rule-settings.png){width="600" zoomable="yes"}

1. Legen Sie den **[!UICONTROL Alle]**-Wert fest, entsprechend der Anzahl der Häufigkeitseinheiten, die in den Zeitraum aufgenommen werden sollen.

   Wenn Sie beispielsweise _Täglich_ als Häufigkeit verwenden und diesen Wert auf `3` setzen, wird der Zeitraum als drei Tage definiert.

1. Klicken **[!UICONTROL oben]** auf „Regel erstellen“.

Die neue Regel befindet sich im Status _Entwurf_ und wird erst dann auf die Kommunikationsbeschränkungen angewendet, wenn Sie sie aktivieren.

### Verwalten von Regeln

Solange sich eine Regel im Status _Entwurf_ befindet, können Sie die Definition bearbeiten oder die Regel löschen. Wenn die Regel angewendet werden soll, können Sie sie aktivieren. Klicken Sie auf _Mehr Menü_ (***…***) neben dem Namen der Entwurfsregel in der Liste und wählen Sie **[!UICONTROL Aktivieren]** aus.

![Klicken Sie auf das Menü Mehr für eine Regel für Kommunikationsgrenzwerte im Entwurf](./assets/config-email-communication-limits-draft-more-menu.png){width="400" zoomable="yes"}

Klicken Sie dann **[!UICONTROL Bestätigungsdialogfeld]** Aktivieren“.

Eine aktive Regel kann nicht bearbeitet oder gelöscht werden, sondern nur deaktiviert werden. Für eine aktive Regel, die Sie aus den angewendeten Kommunikationsbeschränkungen entfernen möchten, klicken Sie auf das Symbol _Deaktivieren_ ( ![Deaktivierungssymbol](../assets/do-not-localize/icon-deactivate.svg) ) neben dem Namen der aktiven Regel.

![Klicken Sie auf das Symbol Deaktivieren für eine Regel der aktiven Kommunikationsbeschränkungen](./assets/config-email-communication-limits-active-deactivate.png){width="400" zoomable="yes"}

Klicken Sie dann **[!UICONTROL Bestätigungsdialog auf]** Deaktivieren“.

Die Regel wird mit dem Status _Inaktiv_ angezeigt. Es ähnelt einer Entwurfsregel, und Sie können sie bei Bedarf bearbeiten, löschen oder aktivieren.

## SPF/DKIM

Verbessern Sie Ihre E-Mail-Versandraten, indem Sie SPF (Sender Policy Framework) und DKIM (Domain Keys Identified Mail) in Ihre DNS-Einstellungen integrieren. Diese Technologien stellen sicher, dass Ihre Empfänger und Empfängerinnen keine Spam-Mails erhalten. Um zu verhindern, dass die Spam-Filter der Empfänger E-Mails ablehnen, stellen Sie sicher, dass SPF und DKIM für Ihre Domains eingerichtet sind.

Um die aktuellen Einstellungen zu überprüfen, gehen Sie zu **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]**. Wählen _[!UICONTROL im]_ unter „E-Mail“ die Option **[!UICONTROL SPF/DKIM]** aus.

![Zugriff auf die SPF/DKIM-Konfiguration](./assets/config-email-spf-dkim.png){width="700" zoomable="yes"}

Die Einstellungen sind in Journey Optimizer B2B edition schreibgeschützt. Klicken Sie **[!UICONTROL oben]** auf „Einstellungen bearbeiten“, um auf die Konfigurationsoptionen in der verbundenen Marketo Engage-Instanz zuzugreifen.

>[!NOTE]
>
>Um auf diese Einstellungen in Adobe Marketo Engage zugreifen und sie bearbeiten zu können, benötigen Sie die Berechtigung eines Produktadministrators.

### SPF-Einrichtung

Der Netzwerkadministrator sollte die folgende Zeile zu Ihren DNS-Einträgen hinzufügen:

`[domain] IN TXT v=spf1 mx ip4:[corpIP] include:mktomail.com ~all`

Ersetzen Sie in diesem Eintrag `[domain]` durch die primäre Domain Ihrer Website (z. B. `company.com`) und `[corpIP]` durch die IP-Adresse Ihres E-Mail-Servers (z. B. `255.255.255.255`). Wenn Sie E-Mails von mehreren Domains über Marketo Engage senden, fügen Sie diesen Eintrag für jede Domain in einer Zeile hinzu.

Wenn Sie bereits über einen SPF-Eintrag in Ihrem DNS-Eintrag verfügen, fügen Sie Folgendes hinzu:

`include:mktomail.com`

### DKIM-Setup

DKIM ist ein Authentifizierungsprotokoll, das von E-Mail-Empfängern verwendet wird, um den Absender der E-Mail-Nachricht zu validieren. Oft wird die Zustellbarkeit von E-Mails an den Posteingang verbessert, da ein Empfänger sicher sein kann, dass die Nachricht keine Fälschung ist.

Wenn Sie den öffentlichen Schlüssel in Ihrem DNS-Eintrag haben und die Versand-Domain in der verbundenen Marketo Engage-Instanz aktiviert ist, wird für Ihre ausgehenden Nachrichten das benutzerdefinierte DKIM-Signieren verwendet. Die benutzerdefinierte DKIM-Signatur enthält zu jeder gesendeten E-Mail eine verschlüsselte digitale Signatur. Die Empfänger können dann die digitale Signatur entschlüsseln, indem sie den _öffentlichen Schlüssel_ im DNS Ihrer Versand-Domain nachschlagen. Wenn der Schlüssel in der E-Mail mit dem Schlüssel im DNS-Eintrag übereinstimmt, akzeptiert der empfangende E-Mail-Server die über Marketo Engage gesendete E-Mail mit höherer Wahrscheinlichkeit.

Weitere Informationen zum Konfigurieren einer benutzerdefinierten DKIM-Signatur für den E-Mail-Versand finden Sie in der [Marketo Engage-Dokumentation](https://experienceleague.adobe.com/de/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"}.

## Bot-Aktivität

Die Aktivität „E-Mail-Bot“ kann fälschlicherweise Ihre E-Mail-Öffnungs- und Klickdaten aufblähen.

Marketo Engage verwendet zwei Methoden zum Bestätigen von Bot-Aktivitäten:

* **Übereinstimmung mit der Liste des Interactive Advertising Bureau (IAB)** - Aktivitäten, die irgendetwas auf der IAB UA/IP (User Agent/IP address)-Liste enthalten, werden als Bots markiert.

* **Übereinstimmung mit Übereinstimmungsmuster** - Wenn zwei oder mehr Aktivitäten gleichzeitig (innerhalb einer Sekunde) stattfinden, werden sie als Bots identifiziert. Diese Methode berücksichtigt die folgenden Attribute für einen Vergleich:

   * Lead-ID (muss gleich sein)
   * E-Mail-Asset (muss dasselbe sein)
   * Link-Klick oder E-Mail öffnen
   * Zeitdifferenz (sollte weniger als eine Sekunde betragen)

Für die Aktivitäten E-Mail-Link-Klick und E-Mail-Öffnen werden neue Attribute mit den folgenden Werten ausgefüllt:

* Aktivitäten, die als Bots identifiziert werden, haben _Bot-Aktivität_ als `True` und _Bot-Aktivitätsmuster_ als identifiziertes Muster/Methode.
* Aktivitäten, die als nicht Bots identifiziert werden, haben _Bot-Aktivität_ als `False` und _Bot-Aktivitätsmuster_ als `N/A`.
* Aktivitäten, die vor der Einführung der Attribute stattfinden, haben _Bot-Aktivität_ als leer (null) und _Bot-_) als leer (null)

Um die aktuellen Einstellungen zu überprüfen, gehen Sie zu **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]**. Wählen _[!UICONTROL im]_ unter „E-Mail“ die Option **[!UICONTROL Bot-Aktivität]** aus.

![Konfiguration der Bot-Aktivität für den E-Mail-Versand aufrufen](./assets/config-email-bot-activity.png){width="700" zoomable="yes"}

Die Einstellungen sind in Journey Optimizer B2B edition schreibgeschützt. Klicken Sie **[!UICONTROL oben]** auf „Einstellungen bearbeiten“, um auf die Konfigurationsoptionen in der verbundenen Marketo Engage-Instanz zuzugreifen.

>[!NOTE]
>
>Um auf diese Einstellungen in Adobe Marketo Engage zugreifen und sie bearbeiten zu können, benötigen Sie die Berechtigung eines Produktadministrators.

Weitere Informationen zum Konfigurieren der Bot-Aktivitätsoptionen finden Sie in der [Dokumentation zu Marketo Engage](https://experienceleague.adobe.com/de/docs/marketo/using/product-docs/administration/email-setup/filtering-email-bot-activity#select-filter-type){target="_blank"}.
