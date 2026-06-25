---
title: Konfiguration der E-Mail-Zustellbarkeit
description: Konfigurieren Sie die Zuweisung von Subdomains, DMARC, SPF, DKIM und IP-Pools für Journey Optimizer B2B Prime.
badgeBeta: label="Beta" type="informative" tooltip="Diese Funktion ist Teil einer eingeschränkten Beta-Version."
autotag-review: '2026-06-12T22:43:42.799Z'
TQID: 'https://experienceleague.adobe.com/RKZSQkjSRvHixOm2faRT5D-yB00IykXfPO06vvIUQ6k'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: d6e625c1-468f-4d73-9f32-fd1edb87f96b
  - id: f01b5556-e951-40ba-8625-2e3001864f2b
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
  - id: ff0c35fa-aa7e-4050-a37c-198fcacd09e6
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: 9eb18693341e5a194cb3c4922e2af760f6b0130c
workflow-type: tm+mt
source-wordcount: 1918
ht-degree: 1%

---

# Zustellbarkeit von E-Mails

Die folgenden Informationen richten sich an Administratoren, die die Versandinfrastruktur so konfigurieren, dass Marketing-Experten und Ersteller von E-Mail-Inhalten unterstützt werden. Es beschreibt Zustellbarkeitsfunktionen und beschreibt, wie Subdomains, Authentifizierung und IP-Pools konfiguriert werden. Weitere Informationen zu E-Mail-Kanälen finden Sie unter den folgenden Themen:

* Konfigurieren von E-Mail-Kanälen [Konfiguration des E-Mail-Kanals](../admin/email-channel-configuration.md)
* E-Mails erstellen - [E-Mails an Journey senden](../marketing/email-channel.md)
* Entwerfen von E-Mail-Inhalten - [Erstellen von E-Mail-Inhalten](../content/email-authoring.md).

Die E-Mail-Zustellbarkeit in [!DNL Journey Optimizer B2B Prime] umfasst eine Reihe von Infrastruktur- und Authentifizierungskonfigurationen, mit denen E-Mail-Nachrichten den Posteingang der Empfänger und nicht den Spam-Ordner erreichen und nicht von ISPs (Internet Service Providern) blockiert werden.

Sie verwendet die folgenden Bausteine, die von einem Administrator konfiguriert werden, in der Regel in der folgenden Reihenfolge:

1. [Delegieren einer oder mehrerer Subdomains](#subdomain-delegation) an Adobe.
1. [Konfigurieren Sie DMARC-, SPF- und DKIM](#dmarc-spf-dkim)Einträge für jede Subdomain.
1. [Bestätigen Sie den IP-Pool](#ip-pools) der zum Senden von E-Mails für Ihre Subdomain verwendet wird.
1. [Erstellen Sie eine oder mehrere E-Mail](../admin/email-channel-configuration.md#create-email-channel-configuration)Kanalkonfigurationen, die eine Subdomain, einen IP-Pool und eine Absenderidentität verbinden.

![Einrichtung der E-Mail-Zustellbarkeit für Journey Optimizer B2B Prime](./assets/email-deliverability-diagram.svg){width="450" zoomable="yes"}

>[!TIP]
>
>Zustellbarkeit und Kanaleinrichtung als einmalige Administratoraktivität behandeln. Nach der Konfiguration müssen Marketer und E-Mail-Autoren nicht erneut darauf zugreifen.

## Aktuelle Einschränkungen {#limitations}

* **Methode der benutzerdefinierten Delegierung** für die Subdomain-Delegierung ist noch nicht verfügbar. Verwenden Sie „Vollständig delegiert“ oder CNAME. Benutzerdefinierte Delegierung ist für allgemeine Verfügbarkeit vorgesehen.
* **Dedizierte IP-Pools** sind bei Beta nicht verfügbar. Der freigegebene IP-Pool ist die einzige Option. Dedizierte IPs werden bei GA ausgeliefert, einschließlich IP-Aufwärmplanung und PTR-Eintragsverwaltung.

## Schlüsselkonzepte {#key-concepts}

Überprüfen Sie vor dem Konfigurieren von E-Mails die folgenden Konzepte, die für die Zustellbarkeitsfunktionen des E-Mail-Kanals gelten:

| Konzept | Was es in [!DNL Journey Optimizer B2B Prime] bedeutet |
| ------- | ---------------------- |
| **_Subdomain_** | Ein delegierter Teil Ihrer Versand-Domain (z. B. `mail.contoso.com`), der zum Senden von E-Mails über Prime verwendet wird. Subdomains isolieren Ihre B2B-Marketing-Reputation von Unternehmens- oder Transaktions-E-Mails. |
| **_IP-Pool_** | Eine Gruppe von IP-Adressen, die mit einer oder mehreren Subdomains verknüpft sind. Prime unterstützt in dieser Version einen gemeinsamen IP-Pool, der von Adobe verwaltet wird. Dedizierte IP-Pools sind in der GA-Roadmap enthalten. |
| **_Kanalkonfiguration_** | Ein wiederverwendbarer Satz von E-Mail-Sendeeinstellungen (Absenderidentität, Antwortadresse, Subdomain, IP-Pool, E-Mail-Typ und Tracking), die Sie an E-Mail-Aktionen in Journey anhängen. Sie können mehrere benannte Kanalkonfigurationen für verschiedene Marken, Geschäftseinheiten oder Versandtypen haben. |

<!--

## Roles and permissions {#roles-permissions}

[!DNL Journey Optimizer B2B Prime] uses role-based access control (RBAC) for email features. Permissions are managed in the Adobe Admin Console (IMS) and synced at login. Product administrators assign granular permissions to product profiles, and then attach those product profiles to users.

Access to email functionality in [!DNL Journey Optimizer B2B Prime] is gated by two layers:

1. **Feature flag (LD).** A LaunchDarkly flag controls whether the entire feature is turned on for your organization. Email authoring and deliverability are gated by `dx_ajo_btob_channel_foundation`. Without this flag, the feature is hidden regardless of permissions.
2. **Functional permission.** A user-level permission that controls whether a specific user can read or write within a feature.

Most email features follow a `view-*` (read) and `manage-*` (write) pattern. A user needs the read permission to see a feature in the navigation, and the write permission to create, edit, or delete within it.

### Email authoring permissions {#email-authoring-permissions}

| Capability | Permission | What it allows |
| ---------- | ---------- | -------------- |
| **View emails** | `view-b2b-emails` | View the email list, open emails, view content (read-only). |
| **Create / edit / delete emails** | `manage-b2b-emails` | All read access plus create, edit, duplicate, and delete emails. Required to author email content within a journey. |
| **View templates** | `view-b2b-templates` | Browse and preview templates in the Templates gallery (read-only). |
| **Create / edit / delete templates** | `manage-b2b-templates` | All read access plus create, edit, and delete saved templates. |
| **View fragments** | `view-b2b-fragments` | Browse and preview visual fragments (read-only). |
| **Create / edit fragments** | `manage-b2b-fragments` | All read access plus create and edit visual fragments. |
| **Publish fragments** | `publish-b2b-fragments` | Publish a fragment so it becomes available to email authors across the organization. |
| **Manage shared assets and library items** | `manage-b2b-library-items` | Manage the underlying shared library used by templates, fragments, and emails. Often granted alongside the template/fragment manage permissions. |
| **Manage usage labels** | `manage-b2b-delete-usage-labels` | Manage data usage labels (DULE) attached to library items for governance. |
| **Manage packages** | `manage-b2b-packages` | Bundle and move templates, fragments, and emails between sandboxes. |
| **View assets (Marketo Design Studio assets in Prime)** | `view-b2b-assets` | Browse the asset picker and preview images. Read-only. |
| **Manage assets** | `manage-b2b-assets` | All read access plus future asset-management actions (Beta scope). |
| **Export message data** | `manage-b2b-message-export` | Export email-level message data and reports. |

Within a person journey, the **Send email** action requires `manage-b2b-person-journeys` (to add the action and activate the journey). A user with only email permissions can author content but cannot add an email to a journey.

### Email deliverability permissions {#email-deliverability-permissions}

Deliverability features (subdomains, DMARC, IP pools, suppression lists, allowed lists, IP warmup plans, and seed lists) are administrator-level configuration. They are governed by two permissions covering the entire **[!UICONTROL Channels]** > **[!UICONTROL Email settings]** area:

| Capability | Permission | What it allows |
| ---------- | ---------- | -------------- |
| **View email settings** | `view-b2b-email-settings` | View subdomains, PTR records, IP pools, suppression list, allowed list, IP warmup plans, and seed lists (read-only). |
| **Manage email settings** | `manage-b2b-email-settings` | All read access plus delegate subdomains, configure DMARC, manage suppression and allowed lists, manage IP warmup plans and seed lists. |

Some sub-features within Email settings are gated by additional LaunchDarkly flags — Suppression list (`enable-suppression`), Allowed list (`enable-allow-list`), Seed lists (`enable-seedlist-ui`). If a sub-feature is not visible in your organization, check with your Adobe representative on flag enablement.

### Channel configuration permissions {#channel-configuration-permissions}

Channel configurations sit under **[!UICONTROL Channels]** → **[!UICONTROL General settings]**. They tie deliverability primitives (subdomain, IP pool, sender identity) to a reusable object that journey authors reference. They are governed by a single permission:

| Capability | Permission | What it allows |
| ---------- | ---------- | -------------- |
| **Manage channel configurations** | `manage-b2b-channels-configurations` | View, create, edit, and delete email channel configurations. |

-->

## Delegieren von Subdomains {#subdomain-delegation}

Die Subdomain-Delegierung teilt dem Internet mit, dass Adobe berechtigt ist, E-Mails im Namen einer bestimmten Subdomain (z. B. `mail.contoso.com`) Ihrer Domain zu senden. Das Delegieren einer dedizierten Subdomain - und nicht Ihrer Stammdomain - schützt Ihre Unternehmens-E-Mails und bietet die folgenden Vorteile:

* **Reputationsisolierung.** Marketing-Sendungen werden getrennt von Unternehmens-E-Mails aufbewahrt. Wenn die Marketing-Reputation nachlässt, sind Ihre Transaktions- und Unternehmens-E-Mails nicht betroffen.
* **Schnelleres IP-Aufwärmen.** Dedizierte Subdomains helfen bei ISPs, eine positive Reputation bei Absendern schneller aufzubauen.
* **Moderne Authentifizierung.** SPF, DKIM und DMARC können sauber pro Subdomain eingerichtet werden, ohne dass andere E-Mail-Flüsse beeinträchtigt werden.
* **Compliance.** Hilft bei der Erfüllung der Massenabsenderanforderungen von Gmail, Yahoo und anderen wichtigen ISPs.

>[!NOTE]
>
>Jede Subdomain in Prime kann nur von einem Adobe-Produkt verwendet werden. Es ist nicht möglich, dieselbe Versand-Subdomain zwischen Prime und einem anderen Produkt wie Adobe Marketo Engage oder Adobe Campaign freizugeben. Es müssen unterschiedliche Subdomains verwendet werden.

### Unterstützte Methoden {#supported-methods}

Prime unterstützt in dieser Beta-Version zwei der drei Methoden zur Zuweisung von Subdomains. Die dritte Methode (benutzerdefinierte Delegierung) steht auf dem Plan.

| Methode | Verwendungszeitpunkt | Worum es geht |
| ------ | ----------- | ---------------- |
| **Vollständig delegiert** | Empfohlen | Delegieren Sie die vollständige DNS-Berechtigung für die Subdomain an Adobe. Adobe erstellt und verwaltet MX-, SPF-, DKIM-, DMARC-, A- und CNAME-Einträge. Niedrigster Betriebsaufwand. Adobe übernimmt DNS-Änderungen für Sie. |
| **CNAME** | Für eingeschränkte Richtlinien | Legen Sie die DNS-Autorität fest und erstellen Sie CNAME-Einträge, die auf von Adobe verwaltete Einträge verweisen. Verwenden Sie dies, wenn die DNS-Richtlinie Ihrer Organisation keine vollständige Delegierung zulässt. Sie sind für die Pflege der DNS-Einträge verantwortlich. |
| **Benutzerdefinierte Delegierung** | Fahrplan (GA) | Vollständige Eigentümerschaft an DNS- und SSL-Zertifikaten behalten. Bietet maximale Kontrolle, einschließlich der Möglichkeit, eigene Zertifikate zu verwenden. Dies ist für die GA-Version vorgesehen. |

### Subdomain delegieren (Methode „Vollständig delegiert„) {#delegate-fully-delegated}

>[!PREREQUISITES]
>
>* Festlegen einer Benennungskonvention für Subdomains (z. B. `mail.contoso.com` für Marketing, `alerts.contoso.com` für Transaktionen)
>* Vergewissern Sie sich bei Ihrem IT-/DNS-Team, dass es die Subdomain (NS-Einträge) an Adobe delegieren kann.
>* Erstellen Sie die neue Subdomain in Ihrem DNS-Anbieter und warten Sie dann 24-48 Stunden auf die DNS-Verbreitung, bevor Sie sie an Adobe delegieren.
>* Vergewissern Sie sich, dass Sie in Prime über die Administratorrolle verfügen.

1. Erweitern Sie in der linken [!DNL Adobe Journey Optimizer B2B Prime]-Navigation **[!UICONTROL Administration]** und wählen Sie **[!UICONTROL Kanäle]** aus.
1. Erweitern Sie im Bedienfeld **[!UICONTROL E-Mail-Einstellungen]** und wählen Sie **[!UICONTROL Subdomains]**.
1. Klicken Sie auf **[!UICONTROL Subdomain einrichten]**.
1. Geben Sie den vollständigen Namen der Subdomain ein (z. B. `mail.contoso.com`).
1. Wählen Sie **[!UICONTROL Vollständig delegiert]** als Delegierungsmethode aus.
1. Konfigurieren Sie DMARC für die Subdomain (siehe [DMARC, SPF und DKIM](#dmarc-spf-dkim)).

   Richten Sie mindestens einen DMARC-Datensatz mit einer Startrichtlinie von `none` ein, damit Sie Berichte überwachen können, ohne den Versand zu beeinträchtigen.

1. Überprüfen Sie die Liste der zu verwaltenden DNS-Einträge für Adobe.

   Dazu gehören normalerweise MX-, SPF-, DKIM-, DMARC-, A- und CNAME-Datensätze (für Tracking- und Mirrorseiten-URLs).

1. DNS-Einträge als CSV-Datei über die Schaltfläche **[!UICONTROL Einträge herunterladen]** herunterladen. Geben Sie diese Datei für Ihr DNS-Team frei.

1. Ihr DNS-Team fügt die NS-Einträge in Ihrer Domain-Hosting-Lösung hinzu, die die Subdomain an Adobe delegieren.

1. Nachdem Ihr DNS-Team bestätigt hat, dass die Einträge vorhanden sind, kehren Sie zu [!DNL Journey Optimizer B2B Prime] zurück und aktivieren Sie das Kontrollkästchen, um zu bestätigen, dass Sie die erforderlichen Einträge auf der Hosting-Site erstellt haben.

1. Klicken Sie **[!UICONTROL Senden]**, um eine Reihe von Validierungsprüfungen (Vorab-Validierung, MX, SPF, DKIM, DMARC, FBL-Registrierung) einzuleiten.

1. Warten Sie, bis der Status der Subdomain auf **[!UICONTROL Erfolg]** geändert wird.

   Dies dauert in der Regel einige Minuten, sobald die DNS-Verbreitung abgeschlossen ist.

>[!NOTE]
>
>Wenn die Validierung fehlschlägt, ändert sich der Status in **[!UICONTROL Fehlgeschlagen]** und [!DNL Journey Optimizer B2B Prime] wird der Grund angezeigt (z. B. NS-Eintrag nicht gefunden, MX-Eintrag fehlt oder DMARC falsch konfiguriert). Beheben Sie das zugrunde liegende DNS-Problem und wiederholen Sie dann die Übermittlung.

### Delegieren einer Subdomain (CNAME-Methode) {#delegate-cname}

Verwenden Sie diese Methode nur, wenn die DNS-Richtlinie Ihrer Organisation die vollständige Delegierung verbietet. Mit CNAME verwalten Sie DNS-Einträge auf Ihrer Seite.

1. Erweitern Sie in der linken [!DNL Adobe Journey Optimizer B2B Prime]-Navigation **[!UICONTROL Administration]** und wählen Sie **[!UICONTROL Kanäle]** aus.
1. Erweitern Sie im Bedienfeld **[!UICONTROL E-Mail-Einstellungen]** und wählen Sie **[!UICONTROL Subdomains]**.
1. Klicken Sie auf **[!UICONTROL Subdomain einrichten]**.
1. Geben Sie den vollständigen Namen der Subdomain ein.
1. Wählen Sie **[!UICONTROL CNAME]** als Delegierungsmethode aus.
1. Konfigurieren Sie DMARC für die Subdomain ([DMARC, SPF und DKIM](#dmarc-spf-dkim)).
1. Überprüfen Sie die Liste der zu generierenden CNAME-Einträge. Diese verweisen die Komponenten Ihrer Subdomain auf von Adobe verwaltete Einträge.
1. Einträge als CSV herunterladen und für Ihr DNS-Team freigeben
1. Ihr DNS-Team fügt jeden CNAME-Eintrag zu Ihrer DNS-Hosting-Lösung hinzu.
1. Wenn Datensätze vorhanden und übertragen sind, kehren Sie zum [!DNL Adobe Journey Optimizer B2B Prime] zurück und bestätigen Sie den Vorgang.
1. Klicken Sie auf **[!UICONTROL Senden]**.
1. Warten Sie, bis der Status &quot;**[!UICONTROL &quot;]**.

>[!IMPORTANT]
>
>Mit CNAME kann Adobe Ihnen nicht dabei helfen, das DNS für die Subdomain zu ändern, zu verwalten oder Fehler zu beheben. Zukünftige Änderungen, z. B. das Hinzufügen eines neuen CNAME für eine Funktionsaktualisierung, müssen von Ihrem DNS-Team vorgenommen werden.

### Leitplanken für Subdomains {#subdomain-guardrails}

* **Standardlimit:** 10 Subdomains pro Organisation. Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, wenn Sie mehr benötigen (bis zu 100 je nach Vertrag).
* **DNS-Übertragung:** Sie 24 bis 48 Stunden, bis sich Änderungen global ausbreiten. Die Validierung kann fehlschlagen, einfach weil das DNS noch nicht propagiert wurde.
* **Wiederverwendung von Subdomains:** Eine Subdomain, die bereits von einem anderen Adobe-Produkt (Marketo Engage, Adobe Campaign) verwendet wird, kann in Prime nicht wiederverwendet werden.

## DMARC, SPF und DKIM {#dmarc-spf-dkim}

DMARC, SPF und DKIM sind E-Mail-Authentifizierungsstandards. Gemeinsam weisen sie den empfangenden E-Mail-Servern nach, dass Ihre Nachricht im Namen Ihrer Domain gesendet und nicht gefälscht wurde. Moderne ISPs - Gmail, Yahoo, Microsoft - verlangen diese Standards für Massenversender.

| Eintrag | steht für | Zweck |
| ------ | ---------- | ------- |
| **SPF** | Sender Policy Framework | Listet die Mail-Server-IPs auf, die zum Senden von E-Mails von Ihrer Domain zugelassen sind. Empfangs-Server lehnen E-Mails von IPs ab, die nicht auf dieser Liste stehen. Adobe erstellt und verwaltet den SPF-Eintrag automatisch, wenn Sie eine Subdomain delegieren (vollständig delegiert). |
| **DKIM** | DomainKeys Identified Mail (mit DomainKeys identifizierte E-Mail) | Eine jeder ausgehenden E-Mail hinzugefügte kryptografische Signatur. Der empfangende Server überprüft die Signatur anhand eines öffentlichen Schlüssels, der im DNS veröffentlicht wurde. Adobe generiert während der Subdomain-Delegierung automatisch DKIM-Schlüssel und DNS-Einträge. |
| **DMARC** | Domain-basierte Nachrichtenauthentifizierung, Reporting und Konformität | teilt den empfangenden Servern mit, was zu tun ist, wenn SPF oder DKIM fehlschlägt - und liefert Berichte über die Authentifizierungsergebnisse. DMARC verfügt über drei Richtlinienmodi: Keine, Quarantäne und Ablehnen. |

### DMARC-Richtlinienmodi {#dmarc-policy-modes}

| Richtlinie | Aktion | Verwendungszeitpunkt |
| ------ | ------ | ----------- |
| `none` | Überwachen | Der Empfangs-Server tut nichts, wenn DMARC fehlschlägt, sendet aber dennoch einen Bericht. Verwenden Sie diese Option, wenn Sie eine Subdomain zum ersten Mal delegieren, um zu bestätigen, dass die Authentifizierung funktioniert, ohne Nachrichtenverlust zu riskieren. |
| `quarantine` | Quarantäne | Der empfangende Server platziert fehlerhafte Nachrichten im Ordner „Spam/Junk“. |
| `reject` | Ablehnen | Der empfangende Server lehnt Nachrichten ab, bei denen die Authentifizierung fehlschlägt (Bounces). Striktester Modus. Empfohlen, sobald Sie sich auf Ihre Authentifizierungseinstellungen verlassen können. |

### Konfigurieren von DMARC {#configure-dmarc}

DMARC ist zum Zeitpunkt der Subdomain-Delegierung konfiguriert, Sie können DMARC jedoch auch für eine bereits delegierte Subdomain hinzufügen oder aktualisieren.

1. Erweitern Sie in der linken [!DNL Adobe Journey Optimizer B2B Prime]-Navigation **[!UICONTROL Administration]** und wählen Sie **[!UICONTROL Kanäle]** aus.

1. Erweitern Sie im Bedienfeld **[!UICONTROL E-Mail-Einstellungen]** und wählen Sie **[!UICONTROL Subdomains]**.

1. Suchen Sie in der Liste der Subdomains Ihre Subdomain und überprüfen Sie die Spalte DMARC-Eintrag .

   Wenn ein Datensatz fehlt, wird ein Warnhinweis angezeigt.

1. Öffnen Sie die Subdomain und scrollen Sie zum Abschnitt DMARC-Eintrag .

   * Wenn in der übergeordneten Domain bereits ein DMARC-Eintrag vorhanden ist, ruft [!DNL Journey Optimizer B2B Prime] die Werte automatisch ab. Sie können sie beibehalten oder überschreiben.
   * Wenn kein Datensatz vorhanden ist, wählen Sie **[!UICONTROL Mit Adobe verwalten]** und Adobe erstellt und hostet den DMARC-Datensatz.

1. Legen Sie die Richtlinie fest: `none`, `quarantine` oder `reject`. Beginnen Sie mit `none`, es sei denn, Sie haben bereits eine ausgereifte DMARC-Haltung in Ihrer übergeordneten Domain.

1. (Optional) Konfigurieren Sie zusätzliche DMARC-Tags (`sp` für die Subdomain-Richtlinie, `pct` für Prozentsatz, `rua` und `ruf` für Berichtsadressen).

1. Wenn Sie die vollständige Delegierung verwenden, klicken Sie auf **[!UICONTROL Speichern]**.

   Adobe wendet den Datensatz automatisch an. Wenn Sie CNAME verwenden, kopieren Sie den DNS-Eintrag und lassen Sie ihn von Ihrem DNS-Team hinzufügen. Bestätigen Sie ihn dann in [!DNL Journey Optimizer B2B Prime].

1. Warten Sie bis zu 48 Stunden für die DNS-Übertragung und stellen Sie dann sicher, dass die DMARC-Statusanzeige auf der Subdomain-Seite grün/intakt ist.

>[!TIP]
>
>Beginnen Sie mit der `policy=none` der Überwachung von Authentifizierungsberichten, dem Fortschritt bei der `quarantine` und schließlich mit der `reject`, sobald Ihre Berichte eine fehlerfreie Ausrichtung von SPF und DKIM aufweisen. Ein direkter Wechsel zu `reject` ohne Überwachung kann dazu führen, dass legitime E-Mails abgelehnt werden.

## IP-Pools {#ip-pools}

Ein IP-Pool ist eine benannte Gruppe von IP-Adressen, die zum Senden Ihrer E-Mail verwendet werden. IP-Pools sind für die Reputation des Absenders wichtig: Jeder Pool hat bei ISPs eine eigene Reputation, sodass ein Problem mit einem Pool (z. B. ein Marketing-Burst, der Trigger von Spam-Beschwerden veranlasst) einen anderen Pool nicht kontaminiert (z. B. Transaktionsbestätigungen).

### Pooltypen {#pool-types}

| Pooltyp | Verfügbarkeit | Beschreibung |
| --------- | ------------ | ----------- |
| **Freigegebener IP-Pool** | Verfügbar unter Beta | Ein Pool von IP-Adressen, die von Adobe verwaltet und von vielen Kunden gemeinsam genutzt werden. Die Reputation wird von Adobe im gesamten Pool aufrechterhalten. Ideal für Kunden mit geringem bis mittlerem E-Mail-Volumen, die keine IP-Aufwärmung verwalten möchten. |
| **Dedizierter IP-Pool** | Fahrplan (GA) | Eine oder mehrere IP-Adressen, die ausschließlich Ihrer Organisation zugewiesen sind. Du bist der Besitzer des Rufes. Empfohlen für Absender mit hohem Versandvolumen. Umfasst IP-Aufwärmplanung und Verwaltung von PTR-Einträgen. |

### IP-Pool überprüfen und zuweisen {#review-ip-pool}

In dieser Version sind IP-Pools für Ihre Organisation vorab bereitgestellt. Beim Erstellen einer E-Mail-Kanal-Konfiguration weisen Sie einen IP-Pool zu.

1. Erweitern Sie in der linken [!DNL Adobe Journey Optimizer B2B Prime]-Navigation **[!UICONTROL Administration]** und wählen Sie **[!UICONTROL Kanäle]** aus.
1. Erweitern Sie im Bedienfeld **[!UICONTROL E-Mail-Einstellungen]** und wählen Sie **[!UICONTROL IP-Pools]**.
1. Vergewissern Sie sich, dass für Ihre Organisation **[!UICONTROL IP-Pool mit dem Status]** Aktiv“ verfügbar ist.
1. Bewegen Sie den Mauszeiger über den Pool, um die IP-Adressen und ihre PTR-Einträge (Reverse DNS) anzuzeigen.
1. Wenn Ihr Unternehmen über mehrere Geschäftseinheiten oder Marken verfügt, planen Sie vor der Erstellung der Kanalkonfigurationen, wie Sie IP-Pools (z. B. Marketing-Pool vs. Webinar-Pool) verwenden werden.

>[!IMPORTANT]
>
>Mischen Sie keinen Marketing- und Transaktions-Traffic auf demselben IP-Pool, selbst wenn der freigegebene Pool verfügbar ist. Die Einstellung E-Mail-Typ in der Kanalkonfiguration (Marketing vs. Transaktion) bestimmt das Unterdrückungsverhalten, aber Ihre Kanalkonfigurationen sollten weiterhin nach Möglichkeit unterschiedliche Pools verwenden.

<!--

### Frequently asked questions {#faq}

| Question | Answer |
| -------- | ------ |
| **Can I reuse the subdomain I already use in Marketo Engage?** | No. A subdomain can only be associated with one Adobe product at a time. Create a new subdomain (for example, mail2.contoso.com) for Prime. |
| **Why does my channel configuration show Failed?** | The most common reasons are: MX record validation failed (your subdomain DNS isn't fully configured); DMARC misalignment; or an IP pool that is in Processing and has never been associated with the selected subdomain. Open the configuration to see the specific reason. |
| **What happens if a personalization token has no value at send time?** | If you defined a fallback with the Handlebars `default` helper, the fallback is used. If not, the token resolves to an empty string. Prime warns you when a token has no fallback and the underlying attribute is not guaranteed by the audience definition. |
| **Can I personalize using account-level attributes?** | Not in this release. Personalization in Prime today supports profile attributes only. |
| **What's the maximum email size?** | 100 KB is the recommended best-practice cap for inbox rendering. Prime warns you in the editor if you exceed it. |
| **Can I migrate existing Marketo email templates into Prime?** | A guided self-serve migration tool — including Velocity-to-Handlebars conversion — is delivered at GA. In this release, you can manually rebuild templates or paste raw HTML. |
| **Will my updates to Marketo assets show up in Prime?** | No. Asset availability in Prime is based on a one-time copy from Marketo Design Studio. Re-uploaded or modified Marketo assets are not reflected in Prime today. Native asset upload and management within Prime is on the Beta roadmap. |

## Glossary {#glossary}

| Term | Definition |
| ---- | ---------- |
| **DKIM** | DomainKeys Identified Mail — cryptographic email signature. |
| **DMARC** | Domain-based Message Authentication, Reporting & Conformance. |
| **FBL** | Feedback Loop — a service ISPs offer to receive spam-complaint reports back to senders. |
| **Handlebars** | JavaScript templating language used in Prime for personalization expressions. |
| **IP pool** | Group of IP addresses used to send email. |
| **MX record** | Mail Exchange DNS record — directs incoming mail to the correct mail servers. |
| **NS record** | Name Server DNS record — used to delegate a subdomain. |
| **PTR record** | Pointer record — reverse DNS that maps an IP address back to a hostname. |
| **RBAC** | Role-Based Access Control. |
| **SPF** | Sender Policy Framework — DNS record listing authorized sending IPs. |
| **Subdomain delegation** | Granting Adobe authority over a portion of your domain (a subdomain) for sending email. |

-->

