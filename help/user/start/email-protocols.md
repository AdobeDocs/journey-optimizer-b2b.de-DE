---
title: Protokolle für Tracking und E-Mail-Versand
description: Erfahren Sie, wie Sie Protokolle in Marketo Engage für die Verwendung durch Journey Optimizer B2B edition für Tracking- und E-Mail-Kanalfunktionen konfigurieren.
feature: Setup
role: Admin
exl-id: 3d56f147-ad0a-4686-b14e-375c2eca8806
source-git-commit: 4ba1beb7f252c94379f984b32d8f581ee57038e3
workflow-type: tm+mt
source-wordcount: '1798'
ht-degree: 0%

---

# Protokolle für Tracking und E-Mail-Versand

Adobe Journey Optimizer B2B edition nutzt die E-Mail-Kanalfunktionen und die Ereignisverfolgung in Marketo Engage. Um sicherzustellen, dass der E-Mail-Versand für Unternehmen, die restriktive Firewall- oder Proxy-Server-Einstellungen verwenden, erwartungsgemäß funktioniert, muss ein Systemadministrator bestimmte Domains und IP-Adressbereiche zur Zulassungsliste hinzufügen.

>[!NOTE]
>
>Wenn Ihr Unternehmen bereits die verbundene Marketo Engage-Instanz zur Ausführung seiner Marketing-Vorgänge verwendet, sollten diese Protokolle und Konfigurationen bereits vorhanden sein.

Stellen Sie sicher, dass die folgenden Domains (einschließlich Sternchen) zur Zulassungsliste hinzugefügt werden, um alle Marketo Engage-Ressourcen und Web-Sockets zu aktivieren:

* `*.experience.adobe.com`
* `*.adobe.net`
* `*.marketo.com`
* `*.marketodesigner.com`
* `*.mktoweb.com`

Führen Sie folgende Schritte aus, um das Tracking und den E-Mail-Versand sicherzustellen:

1. [DNS-Einträge erstellen für ](#create-dns-records-for-landing-pages-and-email)
1. [Einrichten von SPF und DKIM](#set-up-spf-and-dkim)
1. [Einrichten von DMARC](#set-up-dmarc)
1. [MX-Einträge für Ihre Domain einrichten](#set-up-mx-records-for-your-domain)
1. [Hinzufügen ausgehender IP-Adressen zu Zulassungslisten](#outbound-ip-addresses)

## DNS-Einträge für E<!-- landing pages and -->Mail erstellen

Wenn Sie einen CNAME-Eintrag verbinden, können Marketing-Experten Web-Versionen von E-Mails, Landingpages und Blogs mit konsistentem Branding hosten, wodurch der Traffic und die Konversionen verbessert werden. Es wird dringend empfohlen, die CNAMEs zu Ihrem Stamm-Domain-Host für Marketo Engage hinzuzufügen, um Ihre Marketing-orientierten Web-Assets zu hosten. Als Administrator sollten Sie mit Ihrem Marketing-Team zusammenarbeiten, um einen CNAME-Eintrag für die Tracking-Links zu planen und zu implementieren, die in den über Marketo Engage gesendeten E-Mails enthalten sind.
<!-- As an administrator, you should work with your Marketing team to plan and implement two CNAME records. The first one is for landing page URLs, so that the landing pages appear in URLs that reflect your domain and not Adobe Marketo Engage (the actual host). The second one is for the tracking links that are included in the emails sent through Marketo Engage.

### Add the CNAME for landing pages

Add the landing page CNAME to your DNS record, so that `[YourLandingPageCNAME]` points to the unique account string that is assigned to your landing pages. Log in to your domain registrar's site and enter the landing page CNAME and account string. This entry usually involves three fields:

* Alias: Enter `[YourLandingPageCNAME]`
* Type: CNAME
* Point to: Enter `[MunchkinID].mktoweb.com`
-->

### Hinzufügen des CNAME für E-Mail-Tracking-Links

Fügen Sie den E-Mail-CNAME so hinzu, dass `[YourEmailCNAME]` auf `[MktoTrackingLink]` verweist, den von Marketo Engage zugewiesenen Standard-Tracking-Link, und zwar im folgenden Format:

`[YourEmailCNAME].[YourDomain].com` IN CNAME-`[MktoTrackingLink]`

Beispiel:

`pages.abc.com IN CNAME mkto-a0244.com`

>[!NOTE]
>
>Der `[MktoTrackingLink]` muss die Standard-Branding-Domain sein.

### Bereitstellen des SSL-Zertifikats

Wenden Sie sich an den [Adobe](https://experienceleague.adobe.com/home?lang=en&amp;support-tab=home#support){target="_blank"}Support, um mit der Bereitstellung eines SSL-Zertifikats zu beginnen.

Dieser Vorgang kann bis zu drei Werktage dauern.

## Einrichten von SPF und DKIM

Ihr Marketing-Team sollte die DKIM (Domain Keys Identified Mail)-Informationen bereitstellen, die Ihrem DNS-Ressourceneintrag hinzugefügt werden sollen. Führen Sie die folgenden Schritte aus, um DKIM und SPF (Sender Policy Framework) zu konfigurieren, und benachrichtigen Sie dann Ihr Marketing-Team, wenn es aktualisiert wird.

1. Fügen Sie den DNS-Einträgen die folgende Zeile hinzu, um SPF einzurichten:

   ```
   [CompanyDomain] IN TXT v=spf1 mx ip4:[CorpIP]  
   include: mktomail.com ~all
   ```

   Wenn Sie bereits über einen SPF-Eintrag im DNS-Eintrag verfügen, fügen Sie einfach Folgendes hinzu:

   ```
   include: mktomail.com
   ```

   Ersetzen Sie `CompanyDomain` durch die Haupt-Domain Ihrer Website (z. B. `company.com/`) und `CorpIP` durch die IP-Adresse Ihres E-Mail-Servers (z. B. `255.255.255.255`). Wenn Sie E-Mails von mehreren Domains über Marketo Engage senden möchten, fügen Sie diese Zeile für jede Domain hinzu (in einer Zeile).

1. Erstellen Sie für DKIM DNS-Ressourceneinträge für jede Domain.

   Fügen Sie die Host-Einträge und TXT-Werte für jede Domain hinzu:

   `[DKIMDomain1]`: Hosteintrag ist `[HostRecord1]` und der TXT-Wert ist `[TXTValue1]`.

   `[DKIMDomain2]`: Hosteintrag ist `[HostRecord2]` und der TXT-Wert ist `[TXTValue2]`.

   Kopieren Sie die `HostRecord` und `TXTValue` für jede DKIM-Domain, nachdem Sie die [Anweisungen](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"} in der Marketo Engage-Dokumentation befolgt haben. Sie können die Domains in Journey Optimizer B2B edition überprüfen (siehe [SPF/DKIM](../admin/configure-channels-emails.md#spfdkim)).

## Einrichten von DMARC

DMARC (Domain-based Message Authentication, Reporting, and Conformance - Domain-basierte Nachrichtenauthentifizierung, Berichterstellung und Konformität) ist ein Authentifizierungsprotokoll, das Unternehmen dazu verwendet wird, ihre Domain vor unbefugter Verwendung zu schützen. Sie erweitert die bestehenden Authentifizierungsprotokolle wie SPF und DKIM, um Empfängerserver über die Maßnahmen zu informieren, die bei einem Authentifizierungsfehler in ihrer Domain ergriffen werden. DMARC ist optional, wird jedoch dringend empfohlen, da zum Schutz Ihrer Marke und Ihrer Reputation beiträgt. Wichtige Anbieter wie Google und Yahoo verlangten ab Februar 2024 die Verwendung von DMARC für Massenversender.

Damit DMARC funktioniert, müssen Sie über mindestens einen der folgenden DNS-TXT-Einträge verfügen:

* Ein gültiger SPF
* Ein gültiger DKIM-Eintrag für Ihre VON: -Domain (empfohlen für Marketo Engage und Journey Optimizer B2B edition)

Sie müssen auch über einen DMARC-spezifischen DNS-TXT-Eintrag für Ihre `FROM:`-Domain verfügen. Optional können Sie eine E-Mail-Adresse definieren, die angibt, wohin DMARC-Berichte innerhalb Ihrer Organisation zur Berichtsüberwachung gehen sollen.

### Beispiel für einen DMARC-Workflow

>[!TIP]
>
>Es empfiehlt sich, DMARC als _Rollout_ implementieren. Eskalieren Sie Ihre DMARC-Richtlinie von `p=none` nach `p=quarantine` und dann nach `p=reject`, wenn Sie die potenziellen Auswirkungen verstehen, und stellen Sie Ihre DMARC-Richtlinie auf eine entspannte Ausrichtung auf SPF und DKIM ein.

Wenn Sie DMARC-Berichte erhalten, sollten Sie Folgendes tun:

1. Verwenden Sie `p=none` und analysieren Sie das Feedback und die Berichte, die Sie erhalten. In den Berichten wird der Empfänger angewiesen, keine Aktionen gegen Nachrichten durchzuführen, bei denen die Authentifizierung fehlschlägt, und E-Mail-Berichte an den Absender zu senden.

   * Wenn die Authentifizierung bei legitimen Nachrichten fehlschlägt, überprüfen Sie die Probleme mit SPF/DKIM und beheben Sie sie.

   * Prüfen Sie, ob SPF oder DKIM abgestimmt sind und die Authentifizierung für alle legitimen E-Mails weitergegeben wird.

   * Überprüfen Sie die Berichte, um sicherzustellen, dass die Ergebnisse den Erwartungen entsprechen, die auf Ihren SPF-/DKIM-Richtlinien basieren.

1. Passen Sie die Richtlinie so an, dass `p=quarantine` den empfangenden E-Mail-Server anweist, E-Mails, die nicht authentifiziert werden können, unter Quarantäne zu stellen (in der Regel werden diese Nachrichten im Spam-Ordner abgelegt).

   Überprüfen Sie die Berichte, um sicherzustellen, dass die Ergebnisse Ihren Erwartungen entsprechen.

1. Wenn Sie mit dem Verhalten von Nachrichten auf `p=quarantine` zufrieden sind, können Sie die Richtlinie an (`p=reject`) anpassen.

   Die Ablehnungsrichtlinie weist den Empfänger an, alle E-Mails für die Domain, bei der die Authentifizierung fehlschlägt, zu verweigern (Bounce). Wenn diese Richtlinie aktiviert ist, haben nur E-Mails, die zu 100 % von Ihrer Domain authentifiziert wurden, eine Chance auf die Platzierung im Posteingang.

   >[!CAUTION]
   >
   >Verwenden Sie diese Richtlinie mit Vorsicht und ermitteln Sie, ob sie für Ihr Unternehmen geeignet ist.

### DMARC-Berichte

DMARC bietet die Möglichkeit, Berichte zu E-Mails zu erhalten, bei denen SPF/DKIM fehlschlägt. Es gibt zwei verschiedene Berichte, die von ISP-Services im Rahmen des Authentifizierungsprozesses generiert werden. Absender können diese Berichte über die RUA/RUF-Tags in ihrer DMARC-Richtlinie erhalten.

* **Aggregierte Berichte (RUA)**: Enthält keine personenbezogenen Daten (Personally Identifiable Information), die möglicherweise unter die DSGVO (Datenschutz-Grundverordnung) fallen.

* **Forensische Berichte (RUF)** enthalten E-Mail-Adressen, die DSGVO-sensibel sind. Bevor Sie diesen Bericht implementieren, überprüfen Sie Ihre Organisationsrichtlinie für den Umgang mit Informationen, die DSGVO-konform sein müssen.

Diese Berichte dienen hauptsächlich dazu, einen Überblick über E-Mails zu erhalten, bei denen ein Spoofing-Versuch unternommen wird. Es handelt sich um hochtechnische Berichte, die am besten über ein Tool eines Drittanbieters verdaut werden können.

### Beispiel für DMARC-Einträge

* Bare minimum record: `v=DMARC1; p=none`

* Eintrag, der zum Empfang von Berichten an eine E-Mail-Adresse weiterleitet: `v=DMARC1; p=none;  rua=mailto:emaill@domain.com;  ruf=mailto:email@domain.com`

### DMARC-Tags

DMARC-Datensätze enthalten mehrere Komponenten namens _DMARC-Tags_. Jedes Tag hat einen -Wert, der einen bestimmten Aspekt von DMARC angibt.

| Tag-Name | Verwenden von  | Funktion | Beispiel | Standardwert |
|-----------|------------------------|-----------|----------|-----------------------------------|
| `v` | Erforderlich | Gibt die Version an. Es gibt nur eine Version, daher ist der Wert `v=DMARC1` festgelegt | v=DMARC1 DMARC1 | DMARC1 |
| `p` | Erforderlich | Gibt die DMARC-Richtlinie an, die den Empfänger anweist, E-Mails zu melden, unter Quarantäne zu stellen oder abzulehnen, wenn die Authentifizierungsprüfungen fehlschlagen. | `p=none`, `p=quarantine` oder `p=reject` | – |
| `fo` | Optional | Ermöglicht dem Domain-Inhaber das Festlegen von Berichtsoptionen. | `0`: Bericht wird generiert, wenn sowohl SPF als auch DKIM <br> `1` - Bericht wird generiert, wenn entweder SPF oder DKIM fehlschlägt <br> `d` - Generieren eines Berichts, wenn DKIM <br> fehlschlägt `s` - Bericht erzeugen, wenn SPF fehlschlägt | `1` (empfohlen für DMARC-Berichte) |
| `pct` | Optional | Gibt den Prozentsatz der zu filternden Nachrichten an. | `pct=20` | `100` |
| `rua` | Optional (empfohlen) | Gibt an, wo aggregierte Berichte bereitgestellt werden. | `rua=mailto:aggrep@example.com` | – |
| `ruf` | Optional (empfohlen) | Gibt an, wo forensische Berichte zugestellt werden. | `ruf=mailto:authfail@example.com` | – |
| `sp` | Optional | Gibt die DMARC-Richtlinie für Subdomains der übergeordneten Domain an. | `sp=reject` | – |
| `adkim` | Optional | Gibt entweder eine strikte (`s`) oder eine entspannte (`r`) Ausrichtung an. Eine entspannte Ausrichtung bedeutet, dass die Domain in der DKIM-Signatur verwendet wird und eine Subdomain der `From:` sein kann. Strenge Ausrichtung bedeutet, dass die Domain in der DKIM-Signatur verwendet wird und exakt mit der Domain übereinstimmen muss, die in der `From:` verwendet wird. | `adkim=r` | `r` |
| `aspf` | Optional | Kann entweder streng (`s`) oder entspannt (`r`) sein. Der entspannte Modus bedeutet, dass die Domain für den Rückpfad eine Subdomain der `From:` sein kann. Der strikte Modus bedeutet, dass die Domain des Rückgabepfads exakt mit der `From:` übereinstimmen muss. | `aspf=r` | `r` |

Detaillierte Informationen zu DMARC und allen zugehörigen Optionen finden Sie unter [https://dmarc.org/](https://dmarc.org/){target="_blank"}.

### DMARC-Implementierung für Marketo Engage

Für DMARC gibt es zwei Arten der Ausrichtung:

* Ausrichtung **DKIM** (Domain Keys Identified Mail): Die in der `From:`-Kopfzeile einer E-Mail angegebene Domain stimmt mit der DKIM-Signatur überein. Die DKIM-Signatur enthält einen `d=`, bei dem die Domain für den Abgleich mit der `From:`-Header-Domain angegeben ist.

  Die DKIM-Ausrichtung überprüft, ob der Absender zum Senden von E-Mails über die Domain autorisiert ist, und stellt sicher, dass während der E-Mail-Übertragung kein Inhalt geändert wurde. Implementieren von DKIM-abgestimmtem DMARC:

   * Richten Sie DKIM für die Domain MAIL FROM Ihrer Nachricht ein. Verwenden Sie die [Anweisungen](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"} in der Marketo Engage-Dokumentation.

   * Konfigurieren Sie DMARC für die Domain DKIM MAIL FROM .

  >[!NOTE]
  >
  >DKIM-Ausrichtung wird für das Marketo Engage empfohlen.

* Ausrichtung **SPF** (Sender Policy Framework): Die Domain im `From:`-Header muss mit der Domain im Return-Path:-Header übereinstimmen. Wenn beide DNS-Domains identisch sind, stimmt der SPF überein (wird ausgerichtet) und gibt ein Ergebnis zurück. Implementieren von SPF-abgestimmtem DMARC:

   * Richten Sie die gebrandete Domain für Rückgabepfade ein.

      * Konfigurieren Sie den entsprechenden SPF-Eintrag.
      * Ändern Sie den MX-Eintrag so, dass er auf den Standard-MX für das Rechenzentrum verweist, von dem Ihre E-Mail gesendet wird.

   * Konfigurieren Sie DMARC für die gebrandete Domain „Return-Path“.

  >[!NOTE]
  >
  >Eine strikte Ausrichtung der SPF wird für das Marketo Engage nicht unterstützt oder empfohlen.

### Dedizierte IPs und freigegebener Pool

Wenn Sie E-Mails über Marketo Engage über eine dedizierte IP-Adresse senden und keinen gebrandeten Rückgabepfad implementiert haben (oder nicht sicher sind, ob Sie diesen haben), eröffnen Sie ein Ticket beim [Adobe-Support](https://experienceleague.adobe.com/home?lang=en&amp;support-tab=home#support){target="_blank"}.

Vertrauenswürdige IPs sind ein gemeinsam genutzter Pool von IPs, die für Benutzer mit geringerem Volumen reserviert sind, die weniger als 75.000 pro Monat senden und sich nicht für eine dedizierte IP qualifizieren. Diese Benutzenden müssen auch die Anforderungen an Best Practices erfüllen.

* Wenn Sie E-Mails über Marketo Engage mit einem gemeinsamen IP-Pool senden, können Sie überprüfen, ob Sie sich für vertrauenswürdige IPs qualifizieren, indem Sie [das Programm für den vertrauenswürdigen IP-Sendebereich ](https://na-sjg.marketo.com/lp/marketoprivacydemo/Trusted-IP-Sending-Range-Program.html){target="_blank"}. Der gebrandete Rückgabepfad ist beim Senden von Marketo Engage vertrauenswürdigen IPs enthalten. Wenn Sie für dieses Programm genehmigt wurden, wenden Sie sich an den Adobe-Support, um den gebrandeten Rückgabepfad einzurichten.

* Wenn Sie monatlich mehr als 100.000 Nachrichten senden und E-Mails über Marketo Engage mit freigegebenen IPs versenden möchten, wenden Sie sich an das Adobe Account Team (Ihren Account Manager), um eine dedizierte IP-Adresse zu erwerben.

## MX-Einträge für Ihre Domain einrichten

Mit einem MX-Eintrag können Sie E-Mails an die Domain empfangen, von der Sie E-Mails senden, um Antworten und automatische Antworten zu verarbeiten. Wenn Sie von Ihrer Unternehmens-Domain aus senden, ist diese wahrscheinlich bereits konfiguriert. Andernfalls können Sie ihn für gewöhnlich so einrichten, dass er Ihrem MX-Eintrag für die Unternehmens-Domain zugeordnet wird.

## Ausgehende IP-Adressen

Eine ausgehende Verbindung wird durch Marketo Engage an einen Server im Internet in Ihrem Namen hergestellt. Ihre IT-Organisation und einige Partner/Anbieter können Zulassungslisten verwenden, um den Zugriff auf Server einzuschränken. In diesem Fall müssen Sie ihnen Marketo Engage ausgehende IP-Adressblöcke zuweisen, um sie zu ihren Zulassungsliste-hinzuzufügen.

<!-- ### Webhooks

Marketo Engage webhooks are an outbound integration mechanism. When a Smart Campaign executes a _Call Webhook_ flow action, it makes an HTTP request to an external web service. If the web service publisher uses an allowlist on the firewall of the network where the external web service is located, the publisher must add the IP address blocks listed below to their allowlist. For more information, see [Create a webhook](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/additional-integrations/create-a-webhook){target="_blank"} and [Call Webhook](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/flow-actions/call-webhook){target="_blank"} in the Marketo Engage documentation.

### CRM sync

Marketo Engage Salesforce CRM Sync and Microsoft Dynamics Sync are integration mechanisms that make outbound HTTP requests to APIs published by your CRM vendor. Ensure that your IT organization does not block any of the IP address blocks below from accessing your CRM vendor APIs. For more information, see [Add an Existing Salesforce Field to the Marketo Sync](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/salesforce-sync/sfdc-sync-details/add-an-existing-salesforce-field-to-the-marketo-sync){target="_blank"} and [Understanding the Microsoft Dynamics Sync](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/understanding-the-microsoft-dynamics-sync){target="_blank"} in the Marketo Engage documentation. -->

## Ausgehende IP-Adressblöcke

In der folgenden Liste sind alle Marketo Engage-Server aufgeführt, die ausgehende Aufrufe ausführen. Auf die Zulassungsliste setzen In diesen Listen finden Sie Informationen zum Konfigurieren von IP-Adressen, Servern, Firewalls, Zugriffssteuerungslisten, Sicherheitsgruppen oder Drittanbieterdiensten für den Empfang von ausgehenden Verbindungen von Marketo Engage.

| IP-Block (CIDR-Notation) | Individuelle IP-Adresse |
| ------------------------ | --------------------- |
| <ul><li>`94.236.119.0/26`</li><li>`103.237.104.0/22`</li><li>`130.248.172.0/24`</li><li>`130.248.173.0/24`</li><li>`130.248.244.88/29`</li><li>`185.28.196.0/22`</li><li>`192.28.144.0/20`</li><li>`192.28.160.0/19`</li><li>`199.15.212.0/22`</li></ul> | <ul><li>`13.237.155.207`</li><li>`13.55.192.247`</li><li>`18.200.201.81`</li><li>`34.247.24.245`</li><li>`35.165.244.220`</li><li>`44.235.171.179`</li><li>`52.20.211.99`</li><li>`52.64.109.86`</li><li>`54.160.246.246`</li><li>`54.212.167.17`</li><li>`54.220.138.65`</li><li>`54.237.141.197`</li><li>`130.248.168.16`</li><li>`130.248.168.17`</li></ul> |
