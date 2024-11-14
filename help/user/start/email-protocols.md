---
title: Protokolle für Tracking und E-Mail-Versand
description: Erfahren Sie, wie Sie Protokolle auf Marketo Engage konfigurieren, um sie von Journey Optimizer B2B edition für Tracking- und E-Mail-Kanal-Funktionen zu verwenden.
feature: Setup
role: Admin
source-git-commit: a8ca8b99ddf33b4a64b42b751f7be798274d0084
workflow-type: tm+mt
source-wordcount: '1798'
ht-degree: 0%

---

# Protokolle für Tracking und E-Mail-Versand

Adobe Journey Optimizer B2B edition nutzt die E-Mail-Kanalfunktionen und die Ereignisverfolgung im Marketo Engage. Um sicherzustellen, dass der E-Mail-Versand für Organisationen, die restriktive Firewall- oder Proxy-Server-Einstellungen verwenden, erwartungsgemäß funktioniert, muss ein Systemadministrator bestimmte Domänen und IP-Adressbereiche zur Zulassungsliste hinzufügen.

>[!NOTE]
>
>Wenn Ihr Unternehmen bereits die verbundene Marketo Engage-Instanz zur Ausführung seiner Marketingvorgänge verwendet, sollten diese Protokolle und Konfigurationen bereits vorhanden sein.

Stellen Sie sicher, dass die folgenden Domänen (einschließlich des Sternchen) zur Zulassungsliste &quot;&quot;hinzugefügt werden, um alle Marketo Engage-Ressourcen und Websockets zu aktivieren:

* `*.experience.adobe.com`
* `*.adobe.net`
* `*.marketo.com`
* `*.marketodesigner.com`
* `*.mktoweb.com`

Führen Sie die folgenden Schritte aus, um das Tracking und den E-Mail-Versand sicherzustellen:

1. [DNS-Einträge für ](#create-dns-records-for-landing-pages-and-email)
1. [Einrichten von SPF und DKIM](#set-up-spf-and-dkim)
1. [Einrichten von DMARC](#set-up-dmarc)
1. [Einrichten von MX-Datensätzen für Ihre Domäne](#set-up-mx-records-for-your-domain)
1. [Ausgehende IP-Adressen zur auf die Zulassungsliste setz hinzufügen](#outbound-ip-addresses)

## DNS-Einträge für <!-- landing pages and -->E-Mail erstellen

Durch die Verbindung eines CNAME-Eintrags können Marketingexperten Webversionen von E-Mails, Landingpages und Blogs mit konsistentem Branding hosten, das Traffic und Konversionen verbessert. Es wird dringend empfohlen, die CNAMEs zu Ihrem Stammdomänenhost hinzuzufügen, damit Marketo Engage Ihre Marketing-orientierten Web-Assets hosten kann. Als Administrator sollten Sie mit Ihrem Marketing-Team zusammenarbeiten, um einen CNAME-Eintrag für die Tracking-Links zu planen und zu implementieren, die in den über Marketo Engage gesendeten E-Mails enthalten sind.
<!-- As an administrator, you should work with your Marketing team to plan and implement two CNAME records. The first one is for landing page URLs, so that the landing pages appear in URLs that reflect your domain and not Adobe Marketo Engage (the actual host). The second one is for the tracking links that are included in the emails sent through Marketo Engage.

### Add the CNAME for landing pages

Add the landing page CNAME to your DNS record, so that `[YourLandingPageCNAME]` points to the unique account string that is assigned to your landing pages. Log in to your domain registrar's site and enter the landing page CNAME and account string. This entry usually involves three fields:

* Alias: Enter `[YourLandingPageCNAME]`
* Type: CNAME
* Point to: Enter `[MunchkinID].mktoweb.com`
-->

### Hinzufügen des CNAME für E-Mail-Tracking-Links

Fügen Sie den E-Mail-CNAME hinzu, damit `[YourEmailCNAME]` auf `[MktoTrackingLink]` verweist, den standardmäßigen Tracking-Link, den Marketo Engage zugewiesen hat, und zwar im folgenden Format:

`[YourEmailCNAME].[YourDomain].com` IN CNAME `[MktoTrackingLink]`

Beispiel:

`pages.abc.com IN CNAME mkto-a0244.com`

>[!NOTE]
>
>Der Wert `[MktoTrackingLink]` muss die Standard-Branding-Domäne sein.

### Bereitstellen des SSL-Zertifikats

Wenden Sie sich an den [Adobe-Support](https://experienceleague.adobe.com/home?lang=en&amp;support-tab=home#support){target="_blank"} , um mit der Bereitstellung eines SSL-Zertifikats zu beginnen.

Dieser Vorgang kann bis zu drei Werktage dauern.

## Einrichten von SPF und DKIM

Ihr Marketing-Team sollte die DKIM-Informationen (Domain Keys Identified Mail) bereitstellen, die zu Ihrem DNS-Ressourcendatensatz hinzugefügt werden sollen. Führen Sie diese Schritte aus, um DKIM und SPF (Sender Policy Framework) zu konfigurieren, und benachrichtigen Sie dann Ihr Marketing-Team, wenn es aktualisiert wird.

1. Um SPF einzurichten, fügen Sie den DNS-Einträgen die folgende Zeile hinzu:

   ```
   [CompanyDomain] IN TXT v=spf1 mx ip4:[CorpIP]  
   include: mktomail.com ~all
   ```

   Wenn Sie bereits einen vorhandenen SPF-Eintrag im DNS-Eintrag haben, fügen Sie einfach Folgendes hinzu:

   ```
   include: mktomail.com
   ```

   Ersetzen Sie `CompanyDomain` durch die Hauptdomäne Ihrer Website (z. B. `company.com/`) und `CorpIP` durch die IP-Adresse Ihres Unternehmens-E-Mail-Servers (z. B. `255.255.255.255`). Wenn Sie E-Mails von mehreren Domänen über Marketo Engage senden möchten, fügen Sie diese Zeile für jede Domäne (in einer Zeile) hinzu.

1. Erstellen Sie für DKIM DNS-Ressourcendatensätze für jede Domäne.

   Fügen Sie die Hostdatensätze und TXT-Werte für jede Domäne hinzu:

   `[DKIMDomain1]`: Host-Eintrag ist `[HostRecord1]` und der TXT-Wert ist `[TXTValue1]`.

   `[DKIMDomain2]`: Host-Eintrag ist `[HostRecord2]` und der TXT-Wert ist `[TXTValue2]`.

   Kopieren Sie die `HostRecord` und `TXTValue` für jede DKIM-Domäne, nachdem Sie die [Anweisungen](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"} in der Marketo Engage-Dokumentation befolgt haben. Sie können die Domänen in Journey Optimizer B2B edition überprüfen (siehe [SPF/DKIM](../admin/configure-channels-emails.md#spfdkim)).

## Einrichten von DMARC

DMARC (Domain-based Message Authentication, Reporting and Conformance) ist ein Authentifizierungsprotokoll, das Unternehmen beim Schutz ihrer Domain vor unbefugter Verwendung unterstützt. Sie erweitert die vorhandenen Authentifizierungsprotokolle wie SPF und DKIM, um Empfängerserver über die Aktionen zu informieren, die bei einem Authentifizierungsfehler in ihrer Domäne durchgeführt werden sollen. DMARC ist optional, wird jedoch dringend empfohlen, da es Ihnen hilft, Ihre Marke und Ihre Reputation zu schützen. Wichtige Anbieter wie Google und Yahoo haben seit Februar 2024 mit der Verwendung von DMARC für Massensender begonnen.

Damit DMARC funktioniert, muss mindestens einer der folgenden DNS-TXT-Einträge vorhanden sein:

* Eine gültige SPF
* Ein gültiger DKIM-Datensatz für Ihre FROM:-Domäne (empfohlen für Marketo Engage und Journey Optimizer B2B edition)

Sie müssen außerdem über einen DMARC-spezifischen DNS-TXT-Eintrag für Ihre `FROM:` -Domäne verfügen. Optional können Sie eine E-Mail-Adresse definieren, die angibt, wohin DMARC-Berichte in Ihrem Unternehmen zur Berichtsüberwachung gehen sollen.

### Beispiel für einen DMARC-Workflow

>[!TIP]
>
>Es empfiehlt sich, DMARC als _langsamen Rollout_ zu implementieren. Eskalieren Sie Ihre DMARC-Richtlinie von `p=none` auf `p=quarantine` und dann auf `p=reject`, sobald Sie sich ein Bild von den potenziellen Auswirkungen machen, und legen Sie Ihre DMARC-Richtlinie auf eine lockere Ausrichtung auf SPF und DKIM fest.

Wenn Sie DMARC-Berichte erhalten, sollten Sie Folgendes tun:

1. Verwenden Sie `p=none` und analysieren Sie das Feedback und die Berichte, die Sie erhalten. Die Berichte weisen den Empfänger an, keine Aktionen für Nachrichten durchzuführen, die die Authentifizierung nicht erfolgreich durchführen, und E-Mail-Berichte an den Absender zu senden.

   * Wenn die Authentifizierung legitimer Nachrichten fehlschlägt, überprüfen und beheben Sie die Probleme mit SPF/DKIM.

   * Bestimmen Sie, ob SPF oder DKIM abgestimmt sind, und übergeben Sie die Authentifizierung für alle legitimen E-Mails.

   * Überprüfen Sie die Berichte, um sicherzustellen, dass die Ergebnisse basierend auf Ihren SPF/DKIM-Richtlinien erwartet werden.

1. Passen Sie die Richtlinie auf &quot;`p=quarantine`&quot;an, wodurch der E-Mail-Empfangs-Server E-Mails unter Quarantäne stellt, die bei der Authentifizierung fehlschlagen (in der Regel werden diese Nachrichten im Spam-Ordner abgelegt).

   Überprüfen Sie die Berichte, um sicherzustellen, dass die Ergebnisse Ihren Erwartungen entsprechen.

1. Wenn Sie mit dem Verhalten von Nachrichten auf `p=quarantine` -Ebene zufrieden sind, können Sie die Richtlinie auf (`p=reject`) anpassen.

   Die Zurückweisungsrichtlinie weist den Empfänger an, jede E-Mail für die Domain, bei der die Authentifizierung fehlschlägt, zu verweigern (Bounce). Wenn diese Richtlinie aktiviert ist, hat nur E-Mails, die zu 100 % von Ihrer Domäne authentifiziert wurden, die Möglichkeit, die Platzierung im Posteingang durchzuführen.

   >[!CAUTION]
   >
   >Verwenden Sie diese Richtlinie mit Vorsicht und stellen Sie fest, ob sie für Ihre Organisation geeignet ist.

### DMARC Reporting

DMARC bietet die Möglichkeit, Berichte zu E-Mails zu erhalten, die SPF/DKIM nicht unterstützen. Im Rahmen des Authentifizierungsprozesses werden zwei verschiedene Berichte von ISP-Dienstern generiert. Absender können diese Berichte über die RUA/RUF-Tags in ihrer DMARC-Richtlinie erhalten.

* **Aggregat-Berichte (RUA)**: Enthält keine personenbezogenen Daten, bei denen DSGVO (Datenschutz-Grundverordnung) beachtet werden könnte.

* **Forensic Reports (RUF)** - Enthält E-Mail-Adressen, bei denen DSGVO-konform ist. Bevor Sie diesen Bericht implementieren, überprüfen Sie Ihre Unternehmensrichtlinie auf Informationen, die mit der DSGVO konform sein müssen.

Diese Berichte dienen hauptsächlich dazu, einen Überblick über E-Mails zu erhalten, die versucht werden, Nachrichten zu spoofing zu senden. Es handelt sich dabei um hochtechnische Berichte, die am besten mit einem Tool von Drittanbietern aufbereitet werden.

### Beispiele für DMARC-Datensätze

* Mindestdatensatz: `v=DMARC1; p=none`

* Datensatz, der zu einer E-Mail-Adresse weiterleitet, um Berichte zu erhalten: `v=DMARC1; p=none;  rua=mailto:emaill@domain.com;  ruf=mailto:email@domain.com`

### DMARC-Tags

DMARC-Datensätze verfügen über mehrere Komponenten namens _DMARC-Tags_. Jedes Tag verfügt über einen Wert, der einen bestimmten Aspekt von DMARC angibt.

| Tag-Name | Verwenden von  | Funktion | Beispiel | Standardwert |
|-----------|------------------------|-----------|----------|-----------------------------------|
| `v` | Erforderlich | Gibt die Version an. Es gibt nur eine Version, daher hat sie den festen Wert `v=DMARC1` | V=DMARC1 DMARC1 | DMARC1 |
| `p` | Erforderlich | Gibt die DMARC-Richtlinie an, die den Empfänger anweist, E-Mails zu melden, unter Quarantäne zu stellen oder abzulehnen, die bei Authentifizierungsprüfungen fehlschlagen. | `p=none`, `p=quarantine` oder `p=reject` | – |
| `fo` | Optional | Ermöglicht es dem Domäneninhaber, Berichtsoptionen anzugeben. | `0`: Bericht erzeugen, wenn sowohl SPF als auch DKIM fehlschlagen <br> `1` - Bericht erzeugen, wenn SPF oder DKIM fehlschlagen <br> `d` - Bericht erzeugen, wenn DKIM fehlschlägt <br> `s` - Bericht erzeugen, wenn SPF fehlschlägt | `1` (empfohlen für DMARC-Berichte) |
| `pct` | Optional | Gibt den Prozentsatz der zu filternden Nachrichten an. | `pct=20` | `100` |
| `rua` | Optional (empfohlen) | Gibt an, wo aggregierte Berichte bereitgestellt werden. | `rua=mailto:aggrep@example.com` | – |
| `ruf` | Optional (empfohlen) | Gibt an, wo forensische Berichte bereitgestellt werden. | `ruf=mailto:authfail@example.com` | – |
| `sp` | Optional | Gibt die DMARC-Richtlinie für Subdomänen der übergeordneten Domäne an. | `sp=reject` | – |
| `adkim` | Optional | Gibt entweder eine strikte (`s`) oder eine lockere (`r`) Ausrichtung an. Eine verzögerte Ausrichtung bedeutet, dass die Domäne in der DKIM-Signatur verwendet wird und eine Subdomäne der `From:` -Adresse sein kann. Eine strikte Ausrichtung bedeutet, dass die Domäne in der DKIM-Signatur verwendet wird und exakt mit der Domäne übereinstimmen muss, die in der `From:` -Adresse verwendet wird. | `adkim=r` | `r` |
| `aspf` | Optional | Kann entweder streng (`s`) oder entspannt (`r`) sein. Der Modus &quot;Relaxed&quot;bedeutet, dass die Domäne &quot;Return-Path&quot;eine Subdomäne der `From:` -Adresse sein kann. Der strikte Modus bedeutet, dass die Domäne &quot;Return-Path&quot;exakt mit der `From:` -Adresse übereinstimmen muss. | `aspf=r` | `r` |

Detaillierte Informationen zu DMARC und allen seinen Optionen finden Sie unter [https://dmarc.org/](https://dmarc.org/){target="_blank"}.

### DMARC-Implementierung für Marketo Engage

Für DMARC gibt es zwei Arten der Ausrichtung:

* Ausrichtung von **DKIM** (Domain Keys Identified Mail): Die in der Kopfzeile `From:` einer E-Mail angegebene Domain stimmt mit der DKIM-Signatur überein. Die DKIM-Signatur enthält einen `d=` -Wert, bei dem die Domäne für die Übereinstimmung mit der `From:` -Header-Domäne angegeben ist.

  Die DKIM-Ausrichtung validiert, ob der Absender berechtigt ist, E-Mails von der Domain zu senden, und stellt sicher, dass während der E-Mail-Übertragung kein Inhalt verändert wurde. So implementieren Sie DKIM-orientierte DMARC:

   * Richten Sie DKIM für die Domäne MAIL FROM Ihrer Nachricht ein. Verwenden Sie die [Anweisungen](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"} in der Marketo Engage-Dokumentation.

   * Konfigurieren Sie DMARC für die DKIM MAIL FROM-Domäne.

  >[!NOTE]
  >
  >Für Marketo Engage wird die DKIM-Ausrichtung empfohlen.

* Ausrichtung von **SPF** (Sender Policy Framework): Die Domäne im `From:` -Header muss mit der Domäne im Rückgabepfad: -Header übereinstimmen. Wenn beide DNS-Domänen identisch sind, stimmt der SPF überein (ausgerichtet) und liefert ein Ergebnis für den Durchgang. So implementieren Sie SPF-orientierte DMARC:

   * Richten Sie die Domäne &quot;Return-Path&quot;ein.

      * Konfigurieren Sie den entsprechenden SPF-Datensatz.
      * Ändern Sie den MX-Datensatz so, dass er auf den Standard-MX für das Rechenzentrum verweist, von dem Ihre E-Mail gesendet wird.

   * Konfigurieren Sie DMARC für die Domäne &quot;Return-Path&quot;.

  >[!NOTE]
  >
  >Eine strikte SPF-Ausrichtung wird für Marketo Engage nicht unterstützt oder empfohlen.

### Dedizierte IPs und freigegebener Pool

Wenn Sie E-Mails über eine dedizierte IP-Adresse per Marketo Engage senden und keinen &quot;Branded Return&quot;-Pfad implementiert haben (oder nicht sicher sind, ob Sie dies tun), öffnen Sie ein Ticket mit dem [Adobe-Support](https://experienceleague.adobe.com/home?lang=en&amp;support-tab=home#support){target="_blank"}.

Vertrauenswürdige IPs sind ein freigegebener IP-Pool, der für Benutzer mit niedrigerem Volumen reserviert ist, die weniger als 75.000 pro Monat senden und nicht für eine dedizierte IP-Adresse qualifiziert sind. Diese Benutzer müssen auch die Best Practices-Anforderungen erfüllen.

* Wenn Sie E-Mails über Marketo Engage mit einem freigegebenen IP-Pool senden, können Sie prüfen, ob Sie sich für vertrauenswürdige IPs qualifizieren, indem Sie [für das Programm für vertrauenswürdige IP-Sendebereiche beantragen](https://na-sjg.marketo.com/lp/marketoprivacydemo/Trusted-IP-Sending-Range-Program.html){target="_blank"}. Der gezeichnete Rückgabepfad ist beim Senden von Marketo Engage-vertrauenswürdigen IPs enthalten. Wenn Sie für dieses Programm genehmigt wurden, wenden Sie sich an den Adobe-Support , um den Branded Return-Path einzurichten.

* Wenn Sie monatlich mehr als 100.000 Nachrichten senden und E-Mails über Marketo Engage über freigegebene IPs versenden möchten, wenden Sie sich an das Adobe Account Team (Ihren Kundenbetreuer), um eine dedizierte IP zu erwerben.

## Einrichten von MX-Datensätzen für Ihre Domäne

Ein MX-Datensatz ermöglicht es Ihnen, E-Mails an die Domain zu erhalten, von der Sie E-Mails senden, um Antworten und Autoreaktoren zu verarbeiten. Wenn Sie von Ihrer Unternehmensdomäne aus senden, ist dies wahrscheinlich bereits konfiguriert. Wenn nicht, können Sie es normalerweise so einrichten, dass es Ihrem MX-Eintrag für die Unternehmensdomäne zugeordnet wird.

## Ausgehende IP-Adressen

Eine ausgehende Verbindung wird durch Marketo Engage an einen Server im Internet in Ihrem Namen hergestellt. Ihre IT-Organisation und einige Partner/Anbieter können Zulassungslisten verwenden, um den Zugriff auf Server zu beschränken. In diesem Fall müssen Sie ihnen ausgehende IP-Adressblöcke mit Marketo Engage zur Verfügung stellen, um sie zu ihren auf die Zulassungsliste setz hinzuzufügen.

<!-- ### Webhooks

Marketo Engage webhooks are an outbound integration mechanism. When a Smart Campaign executes a _Call Webhook_ flow action, it makes an HTTP request to an external web service. If the web service publisher uses an allowlist on the firewall of the network where the external web service is located, the publisher must add the IP address blocks listed below to their allowlist. For more information, see [Create a webhook](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/additional-integrations/create-a-webhook){target="_blank"} and [Call Webhook](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/flow-actions/call-webhook){target="_blank"} in the Marketo Engage documentation.

### CRM sync

Marketo Engage Salesforce CRM Sync and Microsoft Dynamics Sync are integration mechanisms that make outbound HTTP requests to APIs published by your CRM vendor. Ensure that your IT organization does not block any of the IP address blocks below from accessing your CRM vendor APIs. For more information, see [Add an Existing Salesforce Field to the Marketo Sync](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/salesforce-sync/sfdc-sync-details/add-an-existing-salesforce-field-to-the-marketo-sync){target="_blank"} and [Understanding the Microsoft Dynamics Sync](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/understanding-the-microsoft-dynamics-sync){target="_blank"} in the Marketo Engage documentation. -->

## Ausgehende IP-Adressblöcke

Die folgenden Listen decken alle Marketo Engage-Server ab, die ausgehende Aufrufe durchführen. In diesen Listen finden Sie Informationen zum Konfigurieren einer IP-Zulassungsliste, eines Servers, einer Firewall, einer Zugriffssteuerungsliste, einer Sicherheitsgruppe oder eines Drittanbieterdienstes, um ausgehende Verbindungen von Marketo Engage zu empfangen.

| IP-Block (CIDR-Notation) | Einzelne IP-Adresse |
| ------------------------ | --------------------- |
| <ul><li>`94.236.119.0/26`</li><li>`103.237.104.0/22`</li><li>`130.248.172.0/24`</li><li>`130.248.173.0/24`</li><li>`130.248.244.88/29`</li><li>`185.28.196.0/22`</li><li>`192.28.144.0/20`</li><li>`192.28.160.0/19`</li><li>`199.15.212.0/22`</li></ul> | <ul><li>`13.237.155.207`</li><li>`13.55.192.247`</li><li>`18.200.201.81`</li><li>`34.247.24.245`</li><li>`35.165.244.220`</li><li>`44.235.171.179`</li><li>`52.20.211.99`</li><li>`52.64.109.86`</li><li>`54.160.246.246`</li><li>`54.212.167.17`</li><li>`54.220.138.65`</li><li>`54.237.141.197`</li><li>`130.248.168.16`</li><li>`130.248.168.17`</li></ul> |
