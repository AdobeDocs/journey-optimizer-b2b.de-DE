---
title: E-Mail-Einrichtung
description: Platzhalter
feature: Setup, Channels
role: Admin
source-git-commit: 55ffa7995a8d74d352a52f14bed5dd89d7d1c239
workflow-type: tm+mt
source-wordcount: '1319'
ht-degree: 0%

---

# E-Mail-Setup

Legen Sie die folgenden E-Mail-Optionen fest, um die E-Mail-Bereitstellungsinfrastruktur zu unterstützen, die von der angehängten Marketo Engage-Instanz bereitgestellt wird. Ein Marketo Engage-Produktadministrator kann diese Einstellungen konfigurieren, indem er zum Bereich **[!UICONTROL Admin]** in der Marketo Engage-Instanz navigiert und **[!UICONTROL E-Mail]** auswählt.

## E-Mail-Einstellungen

Um E-Mail-Standardwerte für die angehängte Marketo Engage-Instanz einzurichten, ändern Sie die konfigurierten Werte, um die Verwendung durch Ihre Marketing-Organisation widerzuspiegeln.

### Von E-Mail und Titel

Ändern Sie die Werte für die Beschriftung Absender-E-Mail und , sodass neue E-Mails automatisch mit diesen Standardwerten aufgefüllt werden.

>[!NOTE]
>
>Die Änderung gilt nur für die von Ihnen erstellten E-Mails und nicht für andere Benutzende von Marketo Engage oder Journey Optimizer B2B edition.

1. Wechseln Sie zum Bereich **[!UICONTROL Admin]** in der angehängten Marketo Engage-Instanz und wählen Sie **[!UICONTROL E-Mail]** aus.

1. Geben _[!UICONTROL im Bedienfeld]_ die gewünschten Standardwerte für **[!UICONTROL Von E-Mail]** und **[!UICONTROL Von Beschriftung]** ein.

   ![E-Mail-Einstellungen - Standardwerte für „Von E-Mail“ und „Von Kennzeichnung“](./assets/me-admin-email-settings-from.png){width="500"}

1. Klicken Sie **[!UICONTROL Änderungen speichern]**.

### Abmeldung von Nachrichten

Bei nicht-operativen Marketing-E-Mails werden Text und Links zur Abmeldung unten angehängt. Als Produkt-Administrator sollten Sie die standardmäßige HTML und den Standardtext konfigurieren, der verwendet wird, wenn ein Marketer die E-Mail nicht als funktionsfähig markiert.

1. Wechseln Sie zum Bereich **[!UICONTROL Admin]** in der angehängten Marketo Engage-Instanz und wählen Sie **[!UICONTROL E-Mail]** aus.

1. Geben _[!UICONTROL im Bedienfeld]_ Einstellungen“ die gewünschten Standardwerte für **[!UICONTROL HTML abmelden]** und **[!UICONTROL Abonnement beenden]** ein.

   >[!TIP]
   >
   >Marketing-Experten können die Abmeldeposition von HTML in ihrer E-Mail mithilfe von System-Token ändern.

   ![E-Mail-Einstellungen - Standardwerte für HTML abmelden und Text abmelden](./assets/me-admin-email-settings-unsubscribe.png){width="500"}

   >[!CAUTION]
   >
   >Die folgenden Variablen sind wichtig. **Löschen Sie** nicht.
   >
   >* `%mkt_opt_out_prefix%`
   >* `mkt_unsubscribe=1&mkt_tok=##MKT_TOK##`

1. Klicken Sie **[!UICONTROL Änderungen speichern]**.

Wenn Sie jemals zum Standardsysteminhalt zurückkehren müssen, kopieren Sie Folgendes:

+++ Standardtext zur Abmeldung

```
<p><font face="Verdana" size="1">If you no longer wish to receive these emails, click on the following link: <a href="%mkt_opt_out_prefix%UnsubscribePage.html?mkt_unsubscribe=1&mkt_tok=##MKT_TOK##">Unsubscribe</a><br/></font></p>` [!UICONTROL Unsubscribe Text]:
%mkt_opt_out_prefix%UnsubscribePage.html?mkt_unsubscribe=1&mkt_tok=##MKT_TOK##
```

+++

### Als Web-Seite anzeigen

E-Mail-Inhalte haben eingeschränkte Anzeigefunktionen (eingeschränktes CSS und keine JavaScript oder Formulare). Marketing-Experten können die Option _Als Web-Seite anzeigen_ verwenden, um ein Cookie für den E-Mail-Empfänger mithilfe der Marketo Munchkin anzuwenden. Als Produkt-Administrator sollten Sie die standardmäßige HTML und den Standardtext konfigurieren, der eingefügt wird, wenn ein Marketer diese Option auswählt.

1. Wechseln Sie zum Bereich **[!UICONTROL Admin]** in der angehängten Marketo Engage-Instanz und wählen Sie **[!UICONTROL E-Mail]** aus.

1. HTML Ändern Sie im Bedienfeld _[!UICONTROL Einstellungen]_ den Inhalt in den Feldern **[!UICONTROL Als Web-Seite anzeigen]** und **[!UICONTROL Als Web-Seiten-Text anzeigen]**, um Ihren Ton und Ihre Nachricht widerzuspiegeln.

   ![E-Mail-Einstellungen - HTML als Webseite anzeigen und Standardwerte für „Als Webseite anzeigen“](./assets/me-admin-email-settings-view-as-web-page.png){width="500"}

   >[!CAUTION]
   >
   >Die folgenden Variablen sind wichtig. **Löschen Sie** nicht.
   >
   >`%mkt_webview_url%?mkt_tok=##MKT_TOK##`
   >
   >Der zweite Teil `##MKT_TOK##` ist das Munchkin-Cookie dieser Person. Dadurch wird sichergestellt, dass Cookies angemessen angewendet werden, wenn der E-Mail-Empfänger auf den Link klickt.
   >
   >Vermeiden Sie Folgendes:
   >
   >* Hinzufügen zusätzlicher URLs zu einem der HTML-Felder
   >* Einbetten von HTML in die Textversion

1. Klicken Sie **[!UICONTROL Änderungen speichern]**.

Wenn Sie jemals zum Standardsysteminhalt zurückkehren müssen, kopieren Sie Folgendes:

+++ Systemstandardwebseite HTML

```
<div style="text-align: center"><font face="Verdana" size="1">To view this email as a web page, <a href="%mkt_webview_url%?mkt_tok=##MKT_TOK##">click here</a></font></div>
```

+++

+++ Standardtext der Web-Seite des Systems

```
To view this email as a web page, go to the following address:
`%mkt_webview_url%?mkt_tok=##MKT_TOK##`
```

+++

## Beschränkungen beim Abrufen benutzerdefinierter Objekte

Wenn Sie [!DNL Velocity Script] verwenden, um benutzerdefinierte Objektdaten in E-Mails anzuzeigen, passen Sie das übergeordnete Limit für den Abruf benutzerdefinierter Objekte an. Standardmäßig lässt das Limit den Zugriff auf zehn übergeordnete benutzerdefinierte Objekte über das Velocity-Skript zu. Sie können diese Grenze bei Bedarf erhöhen.

[[!DNL Apache Velocity]](https://velocity.apache.org/) ist eine Sprache, die auf [!DNL Java] basiert und für die Vorlage und Skripterstellung von HTML-Inhalten entwickelt wurde. Die Marketo Engage-E-Mail-Infrastruktur unterstützt ihre Verwendung im Kontext von E-Mails durch Skript-Token, die Zugriff auf in benutzerdefinierten Objekten gespeicherte Daten bieten.

Sie können auf übergeordnete und untergeordnete benutzerdefinierte Objekte verweisen, die direkt mit dem Lead oder Kontakt verbunden sind, jedoch keine benutzerdefinierten Objekte der dritten Ebene. Für jedes benutzerdefinierte Objekt sind die 10 zuletzt aktualisierten Datensätze pro Person/Kontakt zur Laufzeit verfügbar und werden von der zuletzt aktualisierten Version (um `0`) zur ältesten aktualisierten Version (um `9`) sortiert.

_So ändern Sie das Limit :_

1. Wechseln Sie zum Bereich **[!UICONTROL Admin]** in der angehängten Marketo Engage-Instanz und wählen Sie **[!UICONTROL E-Mail]** aus.

1. Scrollen Sie zum _[!UICONTROL Benutzerdefinierte Objektabrufbeschränkungen]_ und geben Sie einen neuen Wert in das **[!UICONTROL Übergeordnetes Objektabruflimit“]**
Feld.

   ![Marketo Engage-E-Mail-Administrator - Standardwerte für benutzerdefinierte Objektabrufe sind begrenzt](./assets/me-admin-email-custom-object-retrieval-limits.png){width="500"}

   Es werden Werte von 10 bis 100 unterstützt. Das _[!UICONTROL Limit für untergeordnete]_&quot; wird automatisch festgelegt, indem 1.000 durch das übergeordnete Limit geteilt wird. Wenn Sie beispielsweise das übergeordnete Limit auf 50 festlegen, wird das untergeordnete Limit als 20 berechnet (1000 ÷ 50 = 20).

1. Klicken Sie **[!UICONTROL Änderungen speichern]**.

## Benutzerdefinierte Kopfzeilenoptionen

Ändern Sie die _[!UICONTROL Benutzerdefinierte Kopfzeilenoptionen)]_ E-Mail, um E-Mail-Tracking-Link-Kopfzeilen zu konfigurieren. Aktivieren Sie diese Optionen, um sichere Tracking-Links mit HTTPS unter Verwendung des strikten Transports zu implementieren.

1. Wechseln Sie zum Bereich **[!UICONTROL Admin]** in der angehängten Marketo Engage-Instanz und wählen Sie **[!UICONTROL E-Mail]** aus.

1. Scrollen Sie zum Bedienfeld _[!UICONTROL Benutzerdefinierte Kopfzeilenoptionen]_ und ändern Sie die Einstellung entsprechend Ihren Richtlinien zum Tracking von Links:

   ![Marketo Engage-E-Mail-Admin - Standardeinstellungen für benutzerdefinierte Header-Optionen](./assets/me-admin-email-custom-object-retrieval-limits.png){width="500"}

   * **[!UICONTROL Strenge Transportsicherheit]** - Legen Sie diese Option auf Aktiviert fest, um zu gewährleisten, dass Tracking-Links immer über HTTPS bereitgestellt werden (sollte nur für Abonnements mit Tracking-Links festgelegt werden, die über SSL gesichert sind).
   * **[!UICONTROL Max-age]** - Dieses Feld unterstützt die obligatorische Anweisung, die Zeit in Sekunden anzugeben, die der Browser daran denken soll, nur auf die Domain über HTTPS zuzugreifen.
   * **[!UICONTROL IncludeSubDomains]** - Verwenden Sie diese Option, um die Direktive einzuschließen, die die HSTS-Richtlinie auf alle Subdomains des Hosts anwendet.

   >[!IMPORTANT]
   >
   >Überprüfen Sie diese Einstellungen mit Ihrem IT-Team, um sicherzustellen, dass sie mit den Richtlinien Ihrer Organisation übereinstimmen. Falsche Einstellungen können manche Besucher daran hindern, auf Ihre E-Mail-Links zuzugreifen.

1. Klicken Sie **[!UICONTROL Änderungen speichern]**.

## Bot-Aktivität für E-Mails filtern {#filter-email-bots}

Die Aktivität „E-Mail-Bot“, auch als Nicht-menschliche Interaktionen (NHI) bezeichnet, kann Ihre E-Mail-Daten _Öffnungen_ und _Klicks_ aufblähen, Ihre Interaktionsmetriken verzerren und einen ereignisbasierten Journey-Fortschritt auslösen. Verwenden Sie die E-Mail-Bot-Filterung , um die Integrität von Metriken und Einblicken zu Klick-Interaktionen aufrechtzuerhalten. Es gibt zwei Methoden, um verdächtige Bot-Aktivitäten zu identifizieren:

* _&#x200B;**[!UICONTROL Übereinstimmung mit IAB-Bot-Liste]**&#x200B;_ - Aktivitäten, die mit einem Element auf der [Interactive Advertising Bureau Bot List](https://www.iab.com/guidelines/iab-abc-international-spiders-bots-list/){target="_blank"} (User Agent/IP Address) übereinstimmen, werden als Bots markiert.
* _&#x200B;**[!UICONTROL Übereinstimmung mit Übereinstimmungsmuster]**&#x200B;_ - Zwei oder mehr Aktivitäten, die gleichzeitig (in weniger als einer Sekunde) stattfinden, werden als Bots identifiziert. Beim Vergleich werden folgende Attribute berücksichtigt:
   * Lead-ID (muss gleich sein)
   * E-Mail-Asset (muss dasselbe sein)
   * Link-Klick oder E-Mail öffnen

Für die Aktivität E-Mail-Link-Klick und E-Mail-Öffnen werden Attribute mit den folgenden Werten ausgefüllt:

* Aktivitäten, die als Bots identifiziert werden - _Bot-Aktivität_ = `true` und _Bot-Aktivitätsmuster_ = identifiziertes Muster/Methode
* Aktivitäten, die als nicht Bots identifiziert werden - _Bot-Aktivität_ = `false` und _Bot-Aktivitätsmuster_ = `n/a`

### Filter festlegen

1. Wechseln Sie zum Bereich **[!UICONTROL Admin]** in der angehängten Marketo Engage-Instanz und wählen Sie **[!UICONTROL E-Mail]** aus.

1. Wählen Sie die Registerkarte **[!UICONTROL Bot]** Aktivität aus.

   ![Marketo Engage-E-Mail-Admin - Registerkarte „Bot-Aktivität“](./assets/me-admin-email-bot-activity.png){width="700" zoomable="yes"}

   Im Bedienfeld zur Identifizierung der Bot-Aktivität werden zwei Schieberegler angezeigt, mit denen Sie die Bot-Aktivität identifizieren können.

1. Schalten Sie den Schieberegler um, um einen oder beide zu aktivieren.

   Wählen Sie für jede Methode, die Sie aktivieren, _[!UICONTROL Bot-Aktivität protokollieren]_ oder _[!UICONTROL Bot-Aktivität filtern]_.

   >[!IMPORTANT]
   >
   >Wenn Sie [!UICONTROL Bot-Aktivität filtern] auswählen, werden möglicherweise weniger E-Mail-Öffnungen und -Klicks angezeigt, da falsche Aktivitäten eliminiert werden.

   ![Marketo Engage-E-Mail-Admin - Identifizierungsoptionen für Bot-Aktivitäten](./assets/me-admin-email-bot-activity-set-filters.png){width="500"}

   Für &quot;_[!UICONTROL mit Übereinstimmungsmuster]_ können Sie auch die Anzahl der Sekunden für &quot;**[!UICONTROL zwischen Aktivitäten“]** Standard ist `0`, Maximum ist `3`).

   >[!NOTE]
   >
   >Wenn _Dauer zwischen Aktivitäten_ auf `0` Sekunden eingestellt ist, identifiziert Marketo Engage E-Mail-Aktivitäten, die genau in der gleichen Sekunde stattfinden. Wenn innerhalb der angegebenen Anzahl von Sekunden mehrere E-Mail-Aktivitäten auftreten, wird dies als Bot-Aktivität identifiziert.

   Um eine der Filtermethoden zu deaktivieren, schalten Sie den Schieberegler nach links. Andernfalls werden die Daten nicht zurückgesetzt.

### IP-Blockierungsliste

Adobe hat eine Liste von IP-Adressen identifiziert, die für die Generierung von Millionen von gefälschten Interaktionen verantwortlich sind, da solche Interaktionen, die von einer der folgenden IPs empfangen werden, automatisch herausgefiltert und nicht zu Ihrer Marketo Engage-Instanz hinzugefügt werden. Diese Filterung kann zu einer Verringerung der E-Mail-Öffnungen, Klicks und anderer damit verbundener Aktivitäten führen. Diese Liste kann regelmäßig aktualisiert werden.

+++ Blockierte IP-Adressen

* 40.94.34.52
* 40.94.34.86
* 52.34.76.65
* 54.70.53.60
* 54.71.187.124
* 60.28.2.248
* 64.235.150.252
* 64.235.153.10
* 64.235.153.2
* 64.235.154.105
* 64.235.154.109
* 64.235.154.140
* 64.74.215.1
* 64.74.215.100
* 64.74.215.138
* 64.74.215.139
* 64.74.215.142
* 64.74.215.146
* 64.74.215.150
* 64.74.215.154
* 64.74.215.158
* 64.74.215.162
* 64.74.215.164
* 64.74.215.166
* 64.74.215.170
* 64.74.215.174
* 64.74.215.176
* 64.74.215.178
* 64.74.215.51
* 64.74.215.56
* 64.74.215.58
* 64.74.215.59
* 64.74.215.86
* 64.74.215.98
* 65.154.226.101
* 66.249.91.149
* 70.42.131.106
* 74.125.217.116
* 74.217.90.250
* 104.129.41.4
* 104.47.55.126
* 104.47.58.126
* 104.47.70.126
* 104.47.73.126
* 104.47.73.254
* 104.47.74.126
* 128.220.160.1
* 155.70.39.101
* 162.129.251.14
* 162.129.251.42
* 208.52.157.204

>[!NOTE]
>
>Jede IP-Adresse wird sorgfältig analysiert und geprüft, bevor sie in diese Liste aufgenommen wird, um sicherzustellen, dass nur die kritischsten und schädlichsten IPs blockiert werden.

+++

