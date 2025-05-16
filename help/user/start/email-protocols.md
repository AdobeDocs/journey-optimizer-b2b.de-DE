---
title: Protokolle für Tracking und E-Mail-Versand
description: Erfahren Sie, wie Sie Protokolle in Marketo Engage für die Journey Optimizer B2B Edition-Funktionen für Tracking und E-Mail-Kanäle konfigurieren.
feature: Setup, Channels
role: Admin
exl-id: 3d56f147-ad0a-4686-b14e-375c2eca8806
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '1798'
ht-degree: 100%

---

# Protokolle für Tracking und E-Mail-Versand

Adobe Journey Optimizer B2B Edition nutzt die E-Mail-Kanalfunktionen und das Ereignis-Tracking in Marketo Engage. Um sicherzustellen, dass der E-Mail-Versand für Organisationen, die restriktive Firewall- oder Proxy-Server-Einstellungen verwenden, erwartungsgemäß funktioniert, müssen Systemadmins der Zulassungsliste bestimmte Domains und IP-Adressbereiche hinzufügen.

>[!NOTE]
>
>Wenn Ihre Organisation bereits die verbundene Marketo Engage-Instanz zur Ausführung ihrer Marketing-Vorgänge verwendet, sollten diese Protokolle und Konfigurationen bereits vorhanden sein.

Stellen Sie sicher, dass der Zulassungsliste die folgenden Domains (einschließlich Sternchen) hinzugefügt werden, um alle Marketo Engage-Ressourcen und -Websockets zu aktivieren:

* `*.experience.adobe.com`
* `*.adobe.net`
* `*.marketo.com`
* `*.marketodesigner.com`
* `*.mktoweb.com`

Führen Sie folgende Schritte aus, um Tracking und E-Mail-Versand sicherzustellen:

1. [Erstellen von DNS-Einträgen für ](#create-dns-records-for-landing-pages-and-email)
1. [Einrichten von SPF und DKIM](#set-up-spf-and-dkim)
1. [Einrichten von DMARC](#set-up-dmarc)
1. [Einrichten von MX-Einträgen für Ihre Domain](#set-up-mx-records-for-your-domain)
1. [Hinzufügen ausgehender IP-Adressen zu Zulassungslisten](#outbound-ip-addresses)

## Erstellen von DNS-Einträgen für <!-- landing pages and -->E-Mails

Durch Verbinden eines CNAME-Eintrags können Marketing-Fachleute Web-Versionen von E-Mails, Landingpages und Blogs mit konsistentem Branding hosten. Dadurch werden Traffic und Konversionen optimiert. Es wird dringend empfohlen, die CNAME-Einträge zu Ihrem Stamm-Domain-Host hinzuzufügen, damit Marketo Engage Ihre Marketing-orientierten Web-Assets hosten kann. Als Admin sollten Sie mit Ihrem Marketing-Team zusammenarbeiten, um einen CNAME-Eintrag für die Trackinglinks zu planen und zu implementieren, die in den über Marketo Engage gesendeten E-Mails enthalten sind.
<!-- As an administrator, you should work with your Marketing team to plan and implement two CNAME records. The first one is for landing page URLs, so that the landing pages appear in URLs that reflect your domain and not Adobe Marketo Engage (the actual host). The second one is for the tracking links that are included in the emails sent through Marketo Engage.

### Add the CNAME for landing pages

Add the landing page CNAME to your DNS record, so that `[YourLandingPageCNAME]` points to the unique account string that is assigned to your landing pages. Log in to your domain registrar's site and enter the landing page CNAME and account string. This entry usually involves three fields:

* Alias: Enter `[YourLandingPageCNAME]`
* Type: CNAME
* Point to: Enter `[MunchkinID].mktoweb.com`
-->

### Hinzufügen von CNAME für E-Mail-Trackinglinks

Fügen Sie den E-Mail-CNAME so hinzu, dass `[YourEmailCNAME]` auf `[MktoTrackingLink]` verweist. Dies ist der von Marketo Engage zugewiesene Standard-Trackinglink. Befolgen Sie dabei das folgende Format:

`[YourEmailCNAME].[YourDomain].com` IN CNAME `[MktoTrackingLink]`

Beispiel:

`pages.abc.com IN CNAME mkto-a0244.com`

>[!NOTE]
>
>Der `[MktoTrackingLink]`-Wert muss der standardmäßigen Branding-Domain entsprechen.

### Bereitstellen des SSL-Zertifikats

Wenden Sie sich an den [Adobe-Support](https://experienceleague.adobe.com/home?lang=de&amp;support-tab=home#support){target="_blank"}, um mit der Bereitstellung eines SSL-Zertifikats zu beginnen.

Dieser Vorgang kann bis zu drei Werktage dauern.

## Einrichten von SPF und DKIM

Ihr Marketing-Team sollte die DKIM(Domain Keys Identified Mail)-Informationen bereitstellen, die Sie Ihrem DNS-Ressourceneintrag hinzufügen möchten. Führen Sie die folgenden Schritte aus, um DKIM und SPF (Sender Policy Framework) zu konfigurieren, und benachrichtigen Sie anschließend Ihr Marketing-Team.

1. Fügen Sie zur SPF-Einrichtung den DNS-Einträgen die folgende Zeile hinzu:

   ```
   [CompanyDomain] IN TXT v=spf1 mx ip4:[CorpIP]  
   include: mktomail.com ~all
   ```

   Wenn Sie bereits über einen SPF-Eintrag im DNS-Eintrag verfügen, fügen Sie einfach Folgendes hinzu:

   ```
   include: mktomail.com
   ```

   Ersetzen Sie `CompanyDomain` durch die Haupt-Domain Ihrer Website (z. B. `company.com/`) und `CorpIP` durch die IP-Adresse des E-Mail-Servers Ihres Unternehmens (z. B. `255.255.255.255`). Wenn Sie E-Mails von mehreren Domains über Marketo Engage senden möchten, fügen Sie diese Zeile für jede Domain hinzu (in einer Zeile).

1. Erstellen Sie zur DKIM-Einrichtung DNS-Ressourceneinträge für jede Domain.

   Fügen Sie die Host-Einträge und TXT-Werte für jede Domain hinzu:

   `[DKIMDomain1]`: Der Host-Eintrag lautet `[HostRecord1]` und der TXT-Wert `[TXTValue1]`.

   `[DKIMDomain2]`: Der Host-Eintrag lautet `[HostRecord2]` und der TXT-Wert `[TXTValue2]`.

   Kopieren Sie `HostRecord` und `TXTValue` für jede DKIM-Domain, nachdem Sie die [Anweisungen](https://experienceleague.adobe.com/de/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"} in der Dokumentation zu Marketo Engage befolgt haben. Sie können die Domains in Journey Optimizer B2B Edition überprüfen (siehe [SPF/DKIM](../admin/configure-channels-emails.md#spfdkim)).

## Einrichten von DMARC

DMARC (Domain-based Message Authentication, Reporting, and Conformance) ist ein Authentifizierungsprotokoll, mit dem Organisationen ihre Domain vor unbefugter Nutzung schützen können. Es erweitert die bestehenden Authentifizierungsprotokolle wie SPF und DKIM, um Empfangs-Server über die Maßnahmen zu informieren, die bei einem Authentifizierungsfehler in ihrer Domain zu ergreifen sind. DMARC ist optional, wird jedoch ausdrücklich empfohlen, da dieses Protokoll zum Schutz Ihrer Marke und Ihrer Reputation beiträgt. Bedeutende Anbieter wie Google und Yahoo verlangen seit Februar 2024, dass DMARC bei massenhaft versendeten Nachrichten verwendet wird.

Damit DMARC funktioniert, müssen Sie über mindestens einen der folgenden DNS-TXT-Einträge verfügen:

* Einen gültigen SPF-Eintrag
* Einen gültigen DKIM-Eintrag für Ihre FROM:-Domain (empfohlen für Marketo Engage und Journey Optimizer B2B Edition)

Sie müssen auch über einen DMARC-spezifischen DNS-TXT-Eintrag für Ihre `FROM:`-Domain verfügen. Optional können Sie eine E-Mail-Adresse definieren, die angibt, wohin DMARC-Berichte innerhalb Ihrer Organisation zum Berichts-Monitoring gesendet werden sollen.

### Beispielhafter DMARC-Workflow

>[!TIP]
>
>Es hat sich bewährt, DMARC als _langsames Rollout_ zu implementieren. Stufen Sie Ihre DMARC-Richtlinie von `p=none` auf `p=quarantine` und dann auf `p=reject` hoch, wenn Sie die potenziellen Auswirkungen nachvollziehen können, und legen Sie für Ihre DMARC-Richtlinie eine lockere SPF- und DKIM-Ausrichtung fest.

Wenn Sie DMARC-Berichte erhalten, sollten Sie wie folgt vorgehen:

1. Verwenden Sie `p=none` und analysieren Sie das Feedback und die Berichte, die Sie erhalten. Die Berichte weisen die Empfängerin bzw. den Empfänger an, keine Maßnahmen für Nachrichten durchzuführen, die bei der DMARC-Authentifizierung fehlschlagen, und E-Mail-Berichte an die Absenderin bzw. den Absender zu senden.

   * Wenn die Authentifizierung bei legitimen Nachrichten fehlschlägt, überprüfen und korrigieren Sie die Probleme mit SPF/DKIM.

   * Prüfen Sie, ob SPF oder DKIM entsprechend abgestimmt sind und die Authentifizierungsprüfung für alle legitimen E-Mails bestehen.

   * Überprüfen Sie die Berichte, um sicherzustellen, dass die Ergebnisse den Erwartungen gemäß Ihren SPF/DKIM-Richtlinien entsprechen.

1. Stellen Sie die Richtlinie auf `p=quarantine` ein. Dadurch wird der empfangende E-Mail-Server angewiesen, E-Mails, die nicht authentifiziert werden können, unter Quarantäne zu stellen (in der Regel werden diese Nachrichten im Spam-Ordner abgelegt).

   Überprüfen Sie die Berichte, um sicherzustellen, dass die Ergebnisse den Erwartungen entsprechen.

1. Wenn Sie mit dem Verhalten von Nachrichten auf `p=quarantine`-Ebene zufrieden sind, können Sie die Richtlinie auf `p=reject` einstellen.

   Die Ablehnungsrichtlinie weist die Empfängerin oder den Empfänger an, jede E-Mail für die Domain, bei der die Authentifizierung fehlschlägt, abzulehnen (Bounce). Wenn diese Richtlinie aktiviert ist, haben nur E-Mails, die von Ihrer Domain zu 100 % authentifiziert wurden, die Möglichkeit, in den Posteingang zu gelangen.

   >[!CAUTION]
   >
   >Verwenden Sie diese Richtlinie mit Vorsicht und ermitteln Sie, ob sie für Ihre Organisation geeignet ist.

### DMARC-Berichte

DMARC bietet die Möglichkeit, Berichte zu E-Mails zu erhalten, bei denen SPF/DKIM fehlschlägt. Es gibt zwei verschiedene Berichte, die von Internet-Dienstanbietern im Rahmen des Authentifizierungsprozesses generiert werden. Absenderinnen und Absender können diese Berichte über die RUA/RUF-Tags in ihrer DMARC-Richtlinie erhalten.

* **Aggregierte Berichte (RUA)**: Enthalten keine personenbezogenen Daten (Personally Identifiable Information, PII), die möglicherweise unter die DSGVO (Datenschutz-Grundverordnung) fallen.

* **Forensische Berichte (RUF)**: Enthalten E-Mail-Adressen, die DSGVO-sensibel sind. Bevor Sie diesen Bericht implementieren, überprüfen Sie Ihre Organisationsrichtlinie im Hinblick auf den Umgang mit Informationen, die DSGVO-konform sein müssen.

Diese Berichte dienen hauptsächlich dazu, einen Überblick über die E-Mails mit Spoofing-Versuchen zu erhalten. Es handelt sich um hochtechnische Berichte, die am besten über das Tool eines Drittanbieters verarbeitet werden können.

### Beispielhafte DMARC-Einträge

* Minimaler Eintrag: `v=DMARC1; p=none`

* Eintrag, der zum Empfang von Berichten an eine E-Mail-Adresse weiterleitet: `v=DMARC1; p=none;  rua=mailto:emaill@domain.com;  ruf=mailto:email@domain.com`

### DMARC-Tags

DMARC-Einträge umfassen mehrere Komponenten, die als _DMARC-Tags_ bezeichnet werden. Jedes Tag hat einen Wert, der einen bestimmten Aspekt von DMARC festlegt.

| Tag-Name | Verwenden | Funktion | Beispiel | Standardwert |
|-----------|------------------------|-----------|----------|-----------------------------------|
| `v` | Erforderlich | Gibt die Version an. Es gibt nur eine Version, sodass der feste Wert hier `v=DMARC1` ist. | V=DMARC1 DMARC1 | DMARC1 |
| `p` | Erforderlich | Gibt die DMARC-Richtlinie an, die die Empfängerin oder den Empfänger anweist, E-Mails mit fehlgeschlagener Authentifizierungsprüfung zu melden, unter Quarantäne zu stellen oder abzulehnen. | `p=none`, `p=quarantine` oder `p=reject` | – |
| `fo` | Optional | Ermöglicht der oder dem Domain-Verantwortlichen das Festlegen von Berichtsoptionen. | `0`: Bericht generieren, wenn sowohl SPF als auch DKIM fehlschlagen <br> `1`: Bericht generieren, wenn entweder SPF oder DKIM fehlschlägt <br> `d`: Bericht generieren, wenn DKIM fehlschlägt <br> `s`: Bericht generieren, wenn SPF fehlschlägt | `1` (empfohlen für DMARC-Berichte) |
| `pct` | Optional | Gibt den Prozentsatz der Nachrichten an, die gefiltert werden. | `pct=20` | `100` |
| `rua` | Optional (empfohlen) | Gibt an, wohin aggregierte Berichte gesendet werden. | `rua=mailto:aggrep@example.com` | – |
| `ruf` | Optional (empfohlen) | Gibt an, wohin forensische Berichte gesendet werden. | `ruf=mailto:authfail@example.com` | – |
| `sp` | Optional | Gibt die DMARC-Richtlinie für Subdomains der übergeordneten Domain an. | `sp=reject` | – |
| `adkim` | Optional | Gibt entweder eine strikte (`s`) oder lockere Ausrichtung (`r`) an. Eine lockere Ausrichtung bedeutet, dass die Domain in der DKIM-Signatur verwendet wird und eine Subdomain der `From:`-Adresse sein kann. Eine strikte Ausrichtung bedeutet, dass die Domain in der DKIM-Signatur verwendet wird und genau mit der Domain übereinstimmen muss, die in der `From:`-Adresse verwendet wird. | `adkim=r` | `r` |
| `aspf` | Optional | Kann entweder strikt (`s`) oder locker (`r`) sein. Der lockere Modus bedeutet, dass die Domain für den Rücksendepfad eine Subdomain der `From:`-Adresse sein kann. Der strikte Modus bedeutet, dass die Domain des Rücksendepfads genau mit der `From:`-Adresse übereinstimmen muss. | `aspf=r` | `r` |

Ausführliche Informationen zu DMARC und allen zugehörigen Optionen finden Sie unter [https://dmarc.org/](https://dmarc.org/){target="_blank"}.

### DMARC-Implementierung für Marketo Engage

Bei DMARC gibt es zwei Arten der Ausrichtung:

* **DKIM**(Domain Keys Identified Mail)-Ausrichtung: Die im `From:`-Header einer E-Mail angegebene Domain stimmt mit der DKIM-Signatur überein. Die DKIM-Signatur enthält einen `d=`-Wert, bei dem die Domain für die Übereinstimmung mit der `From:`-Header-Domain angegeben ist.

  Im Rahmen der DKIM-Ausrichtung wird überprüft, ob die Absenderin bzw. der Absender zum Senden von E-Mails über die Domain autorisiert ist, und es wird sichergestellt, dass während der E-Mail-Übertragung kein Inhalt geändert wurde. So implementieren Sie ein DMARC-Protokoll mit DKIM-Ausrichtung:

   * Richten Sie DKIM für die MAIL FROM-Domain Ihrer Nachricht ein. Befolgen Sie die [Anweisungen](https://experienceleague.adobe.com/de/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"} in der Dokumentation zu Marketo Engage.

   * Konfigurieren Sie DMARC für die DKIM MAIL FROM-Domain.

  >[!NOTE]
  >
  >Eine DKIM-Ausrichtung wird für Marketo Engage empfohlen.

* **SPF**(Sender Policy Framework)-Ausrichtung: Die Domain im `From:`-Header muss mit der Domain im Rücksendepfad-Header übereinstimmen. Wenn beide DNS-Domains identisch sind, stimmt SPF überein (SPF-Ausrichtung) und gibt dieses Ergebnis zurück. So implementieren Sie ein DMARC-Protokoll mit SPF-Ausrichtung:

   * Richten Sie die Rücksendepfad-Domain mit Branding ein.

      * Konfigurieren Sie den entsprechenden SPF-Eintrag.
      * Ändern Sie den MX-Eintrag so, dass er auf Standard-MX für das Rechenzentrum verweist, von dem aus Ihre E-Mails gesendet werden.

   * Konfigurieren Sie DMARC für die Rücksendepfad-Domain mit Branding.

  >[!NOTE]
  >
  >Eine strikte SPF-Ausrichtung wird für Marketo Engage nicht unterstützt oder empfohlen.

### Dedizierte IP-Adressen und gemeinsam genutzter Pool

Wenn Sie E-Mails durch Marketo Engage über eine dedizierte IP-Adresse senden und keinen Rücksendepfad mit Branding implementiert haben (oder sich nicht sicher sind, ob dies der Fall ist), erstellen Sie ein Ticket beim [Adobe-Support](https://experienceleague.adobe.com/home?lang=de&amp;support-tab=home#support){target="_blank"}.

Vertrauenswürdige IP-Adressen sind ein gemeinsam genutzter Pool von IP-Adressen, die für Benutzende mit geringerem Sendevolumen von weniger als 75.000 Nachrichten pro Monat reserviert sind, die nicht für eine dedizierte IP-Adresse infrage kommen. Auch diese Benutzenden müssen die Best-Practice-Anforderungen erfüllen.

* Wenn Sie E-Mails durch Marketo Engage über einen gemeinsam genutzten Pool von IP-Adressen senden, können Sie überprüfen, ob Sie für vertrauenswürdige IP-Adressen infrage kommen, indem [Sie sich für das Programm vertrauenswürdiger IP-Adressen bewerben](https://na-sjg.marketo.com/lp/marketoprivacydemo/Trusted-IP-Sending-Range-Program.html){target="_blank"}. Der Rücksendepfad mit Branding ist bei Sendevorgänge über vertrauenswürdige Marketo Engage-IPs enthalten. Wurden Ihr Antrag für eine Teilnahme an diesem Programm genehmigt, wenden Sie sich an den Adobe-Support, um den Rücksendepfad mit Branding einzurichten.

* Wenn Sie mehr als 100.000 Nachrichten pro Monat versenden und E-Mails durch Marketo Engage über gemeinsam genutzte IP-Adressen versenden möchten, wenden Sie sich an das Adobe-Accountteam (Ihre Kundenbetreuung), um eine dedizierte IP zu erwerben.

## Einrichten von MX-Einträgen für Ihre Domain

Ein MX-Eintrag ermöglicht es Ihnen, E-Mails über die Domain zu empfangen, von der aus Sie E-Mails senden, um Antworten und Abwesenheitsnachrichten zu verarbeiten. Erfolgt der Versand über Ihre Unternehmens-Domain, ist dies wahrscheinlich bereits konfiguriert. Falls nicht, können Sie den Vorgang in der Regel so einrichten, dass er dem MX-Eintrag Ihrer Unternehmens-Domain zugeordnet wird.

## Ausgehende IP-Adressen

Eine ausgehende Verbindung ist eine Verbindung, die Marketo Engage zu einem Server im Internet in Ihrem Namen herstellt. Ihre IT-Organisation und einige Partner/Anbieter verwenden möglicherweise Zulassungslisten, um den Zugriff auf Server einzuschränken. In diesem Fall müssen Sie ihnen die Blöcke ausgehender Marketo Engage-IP-Adressen bereitstellen, damit sie sie ihren Zulassungslisten hinzufügen können.

<!-- ### Webhooks

Marketo Engage webhooks are an outbound integration mechanism. When a Smart Campaign executes a _Call Webhook_ flow action, it makes an HTTP request to an external web service. If the web service publisher uses an allowlist on the firewall of the network where the external web service is located, the publisher must add the IP address blocks listed below to their allowlist. For more information, see [Create a webhook](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/additional-integrations/create-a-webhook){target="_blank"} and [Call Webhook](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/flow-actions/call-webhook){target="_blank"} in the Marketo Engage documentation.

### CRM sync

Marketo Engage Salesforce CRM Sync and Microsoft Dynamics Sync are integration mechanisms that make outbound HTTP requests to APIs published by your CRM vendor. Ensure that your IT organization does not block any of the IP address blocks below from accessing your CRM vendor APIs. For more information, see [Add an Existing Salesforce Field to the Marketo Sync](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/salesforce-sync/sfdc-sync-details/add-an-existing-salesforce-field-to-the-marketo-sync){target="_blank"} and [Understanding the Microsoft Dynamics Sync](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/understanding-the-microsoft-dynamics-sync){target="_blank"} in the Marketo Engage documentation. -->

## Blöcke ausgehender IP-Adressen

In den folgenden Listen sind alle Marketo Engage-Server aufgeführt, die ausgehende Aufrufe ausführen. In diesen Listen finden Sie Informationen zum Konfigurieren von IP-Zulassungslisten, Servern, Firewalls, Zugriffssteuerungslisten, Sicherheitsgruppen oder Drittanbieterdiensten für den Empfang ausgehender Verbindungen von Marketo Engage.

| IP-Block (CIDR-Notation) | Einzelne IP-Adresse |
| ------------------------ | --------------------- |
| <ul><li>`94.236.119.0/26`</li><li>`103.237.104.0/22`</li><li>`130.248.172.0/24`</li><li>`130.248.173.0/24`</li><li>`130.248.244.88/29`</li><li>`185.28.196.0/22`</li><li>`192.28.144.0/20`</li><li>`192.28.160.0/19`</li><li>`199.15.212.0/22`</li></ul> | <ul><li>`13.237.155.207`</li><li>`13.55.192.247`</li><li>`18.200.201.81`</li><li>`34.247.24.245`</li><li>`35.165.244.220`</li><li>`44.235.171.179`</li><li>`52.20.211.99`</li><li>`52.64.109.86`</li><li>`54.160.246.246`</li><li>`54.212.167.17`</li><li>`54.220.138.65`</li><li>`54.237.141.197`</li><li>`130.248.168.16`</li><li>`130.248.168.17`</li></ul> |
