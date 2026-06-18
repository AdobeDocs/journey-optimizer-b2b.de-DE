---
title: E-Mail-Zustellbarkeit und Kanalkonfiguration
description: Konfigurieren Sie die Zuweisung von Subdomains, DMARC, SPF, DKIM, IP-Pools und E-Mail-Kanalkonfigurationen für Journey Optimizer B2B Prime.
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
source-git-commit: 0e90250101eef0572af0382cc7d24bca727d2b75
workflow-type: tm+mt
source-wordcount: 3095
ht-degree: 1%

---

# E-Mail-Zustellbarkeit und Kanalkonfiguration

Die folgenden Informationen richten sich an Administratoren, die die Versandinfrastruktur so konfigurieren, dass Marketing-Experten und E-Mail-Autoren unterstützt werden. Es beschreibt Zustellbarkeitsfunktionen, Rollen und Berechtigungen und beschreibt, wie Subdomains, Authentifizierung, IP-Pools und Kanalkonfigurationen konfiguriert werden.

Detaillierte Informationen zum Erstellen von E-Mails und Verfassen von E-Mail-Inhalten im E-Mail-Design-Bereich finden Sie unter [E-Mail-Authoring](../content/email-authoring.md).

## Schlüsselkonzepte {#key-concepts}

Überprüfen Sie vor dem Konfigurieren von E-Mails die folgenden Konzepte, die für die Zustellbarkeitsfunktionen des E-Mail-Kanals gelten:

| Konzept | Was es in [!DNL Journey Optimizer B2B Edition] Prime bedeutet |
| ------- | ---------------------- |
| **_Kanalkonfiguration_** | Ein wiederverwendbarer Satz von E-Mail-Sendeeinstellungen - einschließlich Absenderidentität, Antwortadresse, Subdomain, IP-Pool, E-Mail-Typ (Marketing oder Transaktion) und Tracking -, die Sie an E-Mail-Aktionen in Journey anhängen. Sie können mehrere benannte Kanalkonfigurationen für verschiedene Marken, Geschäftseinheiten oder Versandtypen haben. |
| **_Subdomain_** | Ein delegierter Teil Ihrer Versand-Domain (z. B. `mail.contoso.com`), der zum Senden von E-Mails über Prime verwendet wird. Subdomains isolieren Ihre B2B-Marketing-Reputation von Unternehmens- oder Transaktions-E-Mails. |
| **_IP-Pool_** | Eine Gruppe von IP-Adressen, die mit einer oder mehreren Subdomains verknüpft sind. Prime unterstützt in dieser Version einen gemeinsamen IP-Pool, der von Adobe verwaltet wird. Dedizierte IP-Pools sind in der GA-Roadmap enthalten. |

## Rollen und Berechtigungen {#roles-permissions}

[!DNL Journey Optimizer B2B Edition] Prime verwendet die rollenbasierte Zugriffssteuerung (RBAC) für E-Mail-Funktionen. Berechtigungen werden in Adobe Admin Console (IMS) verwaltet und bei der Anmeldung synchronisiert. Produktadministratoren weisen Produktprofilen granulare Berechtigungen zu und hängen diese Produktprofile dann an Benutzer an.

Der Zugriff auf E-Mail-Funktionen in [!DNL Journey Optimizer B2B Edition] Prime wird von zwei Ebenen gesteuert:

1. **Feature Flag (LD).** Eine LaunchDarkly-Markierung steuert, ob die gesamte Funktion für Ihre Organisation aktiviert ist. E-Mail-Erstellung und Zustellbarkeit werden von `dx_ajo_btob_channel_foundation` bewertet. Ohne dieses Flag wird die Funktion unabhängig von Berechtigungen ausgeblendet.
2. **Funktionale Berechtigung.** Eine Berechtigung auf Benutzerebene, die steuert, ob ein bestimmter Benutzer in einer Funktion lesen oder schreiben kann.

Die meisten E-Mail-Funktionen folgen einem `view-*`- (Lese-) und `manage-*`- (Schreib-)Muster. Ein Benutzer benötigt die Leseberechtigung, um eine Funktion in der Navigation zu sehen, und die Schreibberechtigung zum Erstellen, Bearbeiten oder Löschen innerhalb der Funktion.

### Authoring-Berechtigungen für E-Mails {#email-authoring-permissions}

| Fähigkeit | Berechtigung | Was es erlaubt |
| ---------- | ---------- | -------------- |
| **E-Mails anzeigen** | `view-b2b-emails` | E-Mail-Liste anzeigen, E-Mails öffnen, Inhalt anzeigen (schreibgeschützt). |
| **E-Mails erstellen/bearbeiten/löschen** | `manage-b2b-emails` | Alle Lesezugriffe sowie E-Mails erstellen, bearbeiten, duplizieren und löschen. Erforderlich zum Erstellen von E-Mail-Inhalten auf einer Journey. |
| **Vorlagen anzeigen** | `view-b2b-templates` | Durchsuchen und Anzeigen einer Vorschau von Vorlagen im Vorlagenkatalog (schreibgeschützt). |
| **Erstellen/Bearbeiten/Löschen von Vorlagen** | `manage-b2b-templates` | Lesezugriff sowie Erstellen, Bearbeiten und Löschen gespeicherter Vorlagen. |
| **Anzeigen von Fragmenten** | `view-b2b-fragments` | Durchsuchen und Vorschau von visuellen Fragmenten (schreibgeschützt). |
| **Erstellen/Bearbeiten von Fragmenten** | `manage-b2b-fragments` | Alle Lesezugriffe sowie das Erstellen und Bearbeiten visueller Fragmente. |
| **Veröffentlichen von Fragmenten** | `publish-b2b-fragments` | Veröffentlichen Sie ein Fragment, damit es für E-Mail-Autoren im gesamten Unternehmen verfügbar ist. |
| **Verwalten freigegebener Assets und Bibliothekselemente** | `manage-b2b-library-items` | Verwalten Sie die zugrunde liegende freigegebene Bibliothek, die von Vorlagen, Fragmenten und E-Mails verwendet wird. Wird häufig zusammen mit den Verwaltungsberechtigungen für Vorlagen/Fragmente gewährt. |
| **Verwalten von Nutzungskennzeichnungen** | `manage-b2b-delete-usage-labels` | Verwalten von Datennutzungskennzeichnungen (DULE), die zur Governance an Bibliothekselemente angehängt sind. |
| **Pakete verwalten** | `manage-b2b-packages` | Bündeln Sie Vorlagen, Fragmente und E-Mails und verschieben Sie sie zwischen Sandboxes. |
| **Anzeigen von Assets (Marketo Design Studio-Assets in Prime)** | `view-b2b-assets` | Durchsuchen Sie die Asset-Auswahl und zeigen Sie eine Vorschau von Bildern an. Schreibgeschützt. |
| **Verwalten von Assets** | `manage-b2b-assets` | Alle Lesezugriffe sowie zukünftige Asset-Management-Aktionen (Beta-Umfang). |
| **Exportieren von Nachrichtendaten** | `manage-b2b-message-export` | Exportieren Sie Nachrichtendaten und Berichte auf E-Mail-Ebene. |

Innerhalb einer Personen-Journey ist für die **E-Mail senden** Aktion `manage-b2b-person-journeys` erforderlich (um die Aktion hinzuzufügen und die Journey zu aktivieren). Benutzende, die nur über E-Mail-Berechtigungen verfügen, können Inhalte erstellen, aber keine E-Mail zu einer Journey hinzufügen.

### E-Mail-Zustellbarkeitsberechtigungen {#email-deliverability-permissions}

Zustellbarkeitsfunktionen (Subdomains, DMARC, IP-Pools, Unterdrückungslisten, Zulassungslisten, IP-Aufwärmpläne und Seed-Listen) sind Konfigurationen auf Admin-Ebene. Sie unterliegen zwei Berechtigungen, die den gesamten Bereich **[!UICONTROL Kanäle]** > **[!UICONTROL E-Mail-Einstellungen]** abdecken:

| Fähigkeit | Berechtigung | Was es erlaubt |
| ---------- | ---------- | -------------- |
| **E-Mail-Einstellungen anzeigen** | `view-b2b-email-settings` | Anzeigen von Subdomains, PTR-Einträgen, IP-Pools, Unterdrückungsliste, Zulassungsliste, IP-Aufwärmplänen und Seed-Listen (schreibgeschützt). |
| **E-Mail-Einstellungen verwalten** | `manage-b2b-email-settings` | Alle Lesezugriffe plus Delegieren von Subdomains, Konfigurieren von DMARC, Verwalten von Unterdrückungs- und Zulassungslisten, Verwalten von IP-Aufwärmplänen und Testadressenlisten. |

Einige Unterfunktionen in E-Mail-Einstellungen werden durch zusätzliche LaunchDarkly-Flags - Unterdrückungsliste (`enable-suppression`), Zulassungsliste (`enable-allow-list`), Testadressenlisten (`enable-seedlist-ui`) - kategorisiert. Wenn in Ihrer Organisation keine Unterfunktion angezeigt wird, wenden Sie sich an den Adobe-Support, um zu erfahren, ob die Markierung aktiviert ist.

### Kanalkonfigurationsberechtigungen {#channel-configuration-permissions}

Kanalkonfigurationen befinden sich unter **[!UICONTROL Kanäle]** → **[!UICONTROL Allgemeine Einstellungen]**. Sie verknüpfen Zustellbarkeits-Primitive (Subdomain, IP-Pool, Absenderidentität) mit einem wiederverwendbaren Objekt, auf das Journey-Autorinnen und -Autoren verweisen. Sie unterliegen einer einzigen Berechtigung:

| Fähigkeit | Berechtigung | Was es erlaubt |
| ---------- | ---------- | -------------- |
| **Kanalkonfigurationen verwalten** | `manage-b2b-channels-configurations` | Anzeigen, Erstellen, Bearbeiten und Löschen von E-Mail-Kanal-Konfigurationen. |

## Übersicht über die E-Mail-Zustellbarkeit {#deliverability-overview}

Die E-Mail-Zustellbarkeit in [!DNL Journey Optimizer B2B Edition] Prime umfasst eine Reihe von Infrastruktur- und Authentifizierungskonfigurationen, mit denen E-Mail-Nachrichten den Posteingang der Empfänger und nicht den Spam-Ordner erreichen und nicht von ISPs (Internet Service Providern) blockiert werden.

Sie verwendet die folgenden Bausteine, die von einem Administrator konfiguriert werden, in der Regel in der folgenden Reihenfolge:

1. Delegieren Sie eine oder mehrere Subdomains an Adobe.
1. Konfigurieren Sie DMARC-, SPF- und DKIM-Einträge für jede Subdomain.
1. Bestätigen Sie den IP-Pool, der E-Mails für Ihre Subdomain senden wird.
1. Erstellen Sie eine oder mehrere E-Mail-Kanal-Konfigurationen, die eine Subdomain, einen IP-Pool und eine Absenderidentität verbinden.
1. Verwenden Sie diese Kanalkonfigurationen beim Journey von E-Mail-Aktionen.

>[!TIP]
>
>Behandeln Sie die Einrichtung der Zustellbarkeit als einmalige Administratoraktivität pro Geschäftseinheit oder Marke. Nach der Konfiguration müssen Marketer und E-Mail-Autoren nicht erneut darauf zugreifen.

## Delegieren von Subdomains {#subdomain-delegation}

Die Subdomain-Delegierung teilt dem Internet mit, dass Adobe berechtigt ist, E-Mails im Namen einer bestimmten Subdomain (z. B. `mail.contoso.com`) Ihrer Domain zu senden. Durch das Delegieren einer dedizierten Subdomain - und nicht Ihrer Root-Domain - wird Ihre Unternehmens-E-Mail geschützt und eine

* **Reputationsisolierung.** Marketing-Sendungen werden getrennt von Unternehmens-E-Mails aufbewahrt. Wenn die Marketing-Reputation nachlässt, sind Ihre Transaktions- und Unternehmens-E-Mails nicht betroffen.
* **Schnelleres IP-Aufwärmen.** Dedizierte Subdomains helfen bei ISPs, eine positive Reputation bei Absendern schneller aufzubauen.
* **Moderne Authentifizierung.** SPF, DKIM und DMARC können sauber pro Subdomain eingerichtet werden, ohne dass andere E-Mail-Flüsse beeinträchtigt werden.
* **Compliance.** Hilft bei der Erfüllung der Massenabsenderanforderungen von Gmail, Yahoo und anderen wichtigen ISPs.

>[!NOTE]
>
>Jede Subdomain in Prime kann nur von einem Adobe-Produkt verwendet werden. Es ist nicht möglich, dieselbe Versand-Subdomain zwischen Prime und einem anderen Produkt wie Adobe Marketo Engage oder Adobe Campaign freizugeben. Es müssen unterschiedliche Subdomains verwendet werden.

### Unterstützte Methoden

Prime unterstützt zwei der drei Methoden zur Delegierung von Subdomains bei Alpha. Die dritte Methode (benutzerdefinierte Delegierung) steht auf dem Plan.

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

1. [!DNL Adobe Journey Optimizer B2B Edition] Prime navigieren Sie zu **[!UICONTROL Administration]** → **[!UICONTROL Kanäle]** → **[!UICONTROL E-Mail]** → **[!UICONTROL Subdomains]**.
1. Klicken Sie auf **[!UICONTROL Subdomain einrichten]**.
1. Geben Sie den vollständigen Namen der Subdomain ein (z. B. `mail.contoso.com`).
1. Wählen Sie **[!UICONTROL Vollständig delegiert]** als Delegierungsmethode aus.
1. Konfigurieren Sie DMARC für die Subdomain (siehe [DMARC, SPF und DKIM](#dmarc-spf-dkim)).

   Richten Sie mindestens einen DMARC-Datensatz mit einer Startrichtlinie von `none` ein, damit Sie Berichte überwachen können, ohne den Versand zu beeinträchtigen.

1. Überprüfen Sie die Liste der zu verwaltenden DNS-Einträge für Adobe.

   Dazu gehören normalerweise MX-, SPF-, DKIM-, DMARC-, A- und CNAME-Datensätze (für Tracking- und Mirrorseiten-URLs).

1. DNS-Einträge als CSV-Datei über die Schaltfläche **[!UICONTROL Einträge herunterladen]** herunterladen. Geben Sie diese Datei für Ihr DNS-Team frei.

1. Ihr DNS-Team fügt die NS-Einträge in Ihrer Domain-Hosting-Lösung hinzu, die die Subdomain an Adobe delegieren.

1. Nachdem Ihr DNS-Team bestätigt hat, dass die Einträge vorhanden sind, kehren Sie zu [!DNL Journey Optimizer B2B Edition] Prime zurück und aktivieren Sie das Kontrollkästchen, um zu bestätigen, dass Sie die erforderlichen Einträge auf der Hosting-Site erstellt haben.

1. Klicken Sie **[!UICONTROL Senden]**, um eine Reihe von Validierungsprüfungen (Vorab-Validierung, MX, SPF, DKIM, DMARC, FBL-Registrierung) einzuleiten.

1. Warten Sie, bis der Status der Subdomain auf **[!UICONTROL Erfolg]** geändert wird.

   Dies dauert in der Regel einige Minuten, sobald die DNS-Verbreitung abgeschlossen ist.

>[!NOTE]
>
>Wenn die Validierung fehlschlägt, ändert sich der Status in **[!UICONTROL Fehlgeschlagen]** und [!DNL Journey Optimizer B2B Edition] Prime zeigt den Grund an (z. B. NS-Eintrag nicht gefunden, MX-Eintrag fehlt oder DMARC falsch konfiguriert). Beheben Sie das zugrunde liegende DNS-Problem und wiederholen Sie dann die Übermittlung.

### Delegieren einer Subdomain (CNAME-Methode) {#delegate-cname}

Verwenden Sie diese Methode nur, wenn die DNS-Richtlinie Ihrer Organisation die vollständige Delegierung verbietet. Mit CNAME verwalten Sie DNS-Einträge auf Ihrer Seite.

1. Navigieren Sie in [!DNL Adobe Journey Optimizer B2B Edition] Prime zu **[!UICONTROL Administration]** → **[!UICONTROL Kanäle]** → **[!UICONTROL E-Mail]** → **[!UICONTROL Subdomains]**.
1. Klicken Sie auf **[!UICONTROL Subdomain einrichten]**.
1. Geben Sie den vollständigen Namen der Subdomain ein.
1. Wählen Sie **[!UICONTROL CNAME]** als Delegierungsmethode aus.
1. Konfigurieren Sie DMARC für die Subdomain ([DMARC, SPF und DKIM](#dmarc-spf-dkim)).
1. Überprüfen Sie die Liste der von Prime generierten CNAME-Einträge - diese verweisen die Komponenten Ihrer Subdomain auf von Adobe verwaltete Einträge.
1. Einträge als CSV herunterladen und für Ihr DNS-Team freigeben
1. Ihr DNS-Team fügt jeden CNAME-Eintrag zu Ihrer DNS-Hosting-Lösung hinzu.
1. Sobald die Datensätze eingerichtet und weitergegeben sind, kehren Sie zu Prime zurück und bestätigen Sie den Vorgang. Klicken Sie auf **[!UICONTROL Senden]**.
1. Warten Sie, bis der Status &quot;**[!UICONTROL &quot;]**.

>[!IMPORTANT]
>
>Mit CNAME kann Adobe Ihnen nicht dabei helfen, das DNS für die Subdomain zu ändern, zu verwalten oder Fehler zu beheben. Zukünftige Änderungen - z. B. das Hinzufügen eines neuen CNAME für eine Funktionsaktualisierung - müssen von Ihrem DNS-Team vorgenommen werden.

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

### DMARC-Richtlinienmodi

| Richtlinie | Aktion | Verwendungszeitpunkt |
| ------ | ------ | ----------- |
| `none` | Überwachen | Der Empfangs-Server tut nichts, wenn DMARC fehlschlägt, sendet aber dennoch einen Bericht. Verwenden Sie diese Option, wenn Sie eine Subdomain zum ersten Mal delegieren, um zu bestätigen, dass die Authentifizierung funktioniert, ohne Nachrichtenverlust zu riskieren. |
| `quarantine` | Quarantäne | Der empfangende Server platziert fehlerhafte Nachrichten im Ordner „Spam/Junk“. |
| `reject` | Ablehnen | Der empfangende Server lehnt Nachrichten ab, bei denen die Authentifizierung fehlschlägt (Bounces). Striktester Modus. Empfohlen, sobald Sie sich auf Ihre Authentifizierungseinstellungen verlassen können. |

### Konfigurieren von DMARC {#configure-dmarc}

DMARC ist zum Zeitpunkt der Subdomain-Delegierung konfiguriert, Sie können DMARC jedoch auch für eine bereits delegierte Subdomain hinzufügen oder aktualisieren.

1. Navigieren Sie zu **[!UICONTROL Administration]** → **[!UICONTROL Kanäle]** → → **[!UICONTROL E-Mail-Einstellungen]** **[!UICONTROL Subdomains]**.

1. Suchen Sie in der Liste der Subdomains Ihre Subdomain und überprüfen Sie die Spalte DMARC-Eintrag .

   Wenn ein Datensatz fehlt, wird ein Warnhinweis angezeigt.

1. Öffnen Sie die Subdomain und scrollen Sie zum Abschnitt DMARC-Eintrag .

   * Wenn in der übergeordneten Domain bereits ein DMARC-Eintrag vorhanden ist, ruft [!DNL Journey Optimizer B2B Edition] Prime die Werte automatisch ab. Sie können sie beibehalten oder überschreiben.
   * Wenn kein Datensatz vorhanden ist, wählen Sie **[!UICONTROL Mit Adobe verwalten]** und Adobe erstellt und hostet den DMARC-Datensatz.

1. Legen Sie die Richtlinie fest: `none`, `quarantine` oder `reject`. Beginnen Sie mit `none`, es sei denn, Sie haben bereits eine ausgereifte DMARC-Haltung in Ihrer übergeordneten Domain.

1. (Optional) Konfigurieren Sie zusätzliche DMARC-Tags (`sp` für die Subdomain-Richtlinie, `pct` für Prozentsatz, `rua` und `ruf` für Berichtsadressen).

1. Wenn Sie die vollständige Delegierung verwenden, klicken Sie auf **[!UICONTROL Speichern]**.

   Adobe wendet den Datensatz automatisch an. Wenn Sie CNAME verwenden, kopieren Sie den DNS-Eintrag und lassen Sie ihn von Ihrem DNS-Team hinzufügen. Bestätigen Sie ihn dann in [!DNL Journey Optimizer B2B Edition] Prime.

1. Warten Sie bis zu 48 Stunden für die DNS-Übertragung und stellen Sie dann sicher, dass die DMARC-Statusanzeige auf der Subdomain-Seite grün/intakt ist.

>[!TIP]
>
>Beginnen Sie mit der `policy=none` der Überwachung von Authentifizierungsberichten, dem Fortschritt bei der `quarantine` und schließlich mit der `reject`, sobald Ihre Berichte eine fehlerfreie Ausrichtung von SPF und DKIM aufweisen. Ein direkter Wechsel zu `reject` ohne Überwachung kann dazu führen, dass legitime E-Mails abgelehnt werden.

## IP-Pools {#ip-pools}

Ein IP-Pool ist eine benannte Gruppe von IP-Adressen, die zum Senden Ihrer E-Mail verwendet werden. IP-Pools sind für die Reputation des Absenders wichtig: Jeder Pool hat bei ISPs eine eigene Reputation, sodass ein Problem mit einem Pool (z. B. ein Marketing-Burst, der Trigger von Spam-Beschwerden veranlasst) einen anderen Pool nicht kontaminiert (z. B. Transaktionsbestätigungen).

### Pooltypen

| Pooltyp | Verfügbarkeit | Beschreibung |
| --------- | ------------ | ----------- |
| **Freigegebener IP-Pool** | Verfügbar unter Alpha | Ein Pool von IP-Adressen, die von Adobe verwaltet und von vielen Kunden gemeinsam genutzt werden. Die Reputation wird von Adobe im gesamten Pool aufrechterhalten. Ideal für Kunden mit geringem bis mittlerem E-Mail-Volumen, die keine IP-Aufwärmung verwalten möchten. |
| **Dedizierter IP-Pool** | Fahrplan (GA) | Eine oder mehrere IP-Adressen, die ausschließlich Ihrer Organisation zugewiesen sind. Du bist der Besitzer des Rufes. Empfohlen für Absender mit hohem Versandvolumen. Umfasst IP-Aufwärmplanung und Verwaltung von PTR-Einträgen. |

### IP-Pool überprüfen und zuweisen {#review-ip-pool}

In dieser Version sind IP-Pools für Ihre Organisation vorab bereitgestellt. Beim Erstellen einer E-Mail-Kanal-Konfiguration weisen Sie einen IP-Pool zu.

1. Navigieren Sie zu **[!UICONTROL Administration]** → **[!UICONTROL Kanäle]** → → **[!UICONTROL E-Mail]** **[!UICONTROL IP-Pools]**.
1. Vergewissern Sie sich, dass für Ihre Organisation **[!UICONTROL IP-Pool mit dem Status]** Aktiv“ verfügbar ist.
1. Bewegen Sie den Mauszeiger über den Pool, um die IP-Adressen und ihre PTR-Einträge (Reverse DNS) anzuzeigen.
1. Wenn Ihr Unternehmen über mehrere Geschäftseinheiten oder Marken verfügt, planen Sie vor der Erstellung der Kanalkonfigurationen, wie Sie IP-Pools (z. B. Marketing-Pool vs. Webinar-Pool) verwenden werden.

>[!IMPORTANT]
>
>Mischen Sie keinen Marketing- und Transaktions-Traffic auf demselben IP-Pool, selbst wenn der freigegebene Pool verfügbar ist. Die Einstellung E-Mail-Typ in der Kanalkonfiguration (Marketing vs. Transaktion) bestimmt das Unterdrückungsverhalten, aber Ihre Kanalkonfigurationen sollten weiterhin nach Möglichkeit unterschiedliche Pools verwenden.

## E-Mail-Kanalkonfigurationen {#email-channel-configurations}

Eine Kanalkonfiguration ist das zentrale Objekt, das Ihre Absenderidentität, Subdomain, Ihren IP-Pool und Ihre Tracking-Einstellungen miteinander verknüpft. E-Mail-Aktionen in Journey verweisen auf eine Kanalkonfiguration, um zu erfahren, wie die Nachricht gesendet werden soll:

* **channel:** email.
* **E-Mail-Typ** Marketing oder Transaktion. Diese Einstellung bestimmt, ob Unterdrückungsregeln angewendet werden (Marketing wendet sie an; Transaktionsnachrichten umgehen standardmäßig die Unterdrückung von Spam-Beschwerden für rechtmäßige Transaktionsnachrichten).
* **Kopfzeilenparameter:** von Name, von E-Mail, Antwort-an-Name, Antwort-an-E-Mail, Fehler-E-Mail.
* **Subdomain:** Die delegierte Subdomain, die zum Senden verwendet wird. Die Absender-E-Mail muss diese Subdomain verwenden.
* **IP-Pool:** Der IP-Pool, der zum Versand der Nachricht verwendet wird.
* **URL-Tracking** Aktivieren oder Deaktivieren des Klick- und Öffnungs-Trackings; Konfigurieren der Tracking-Domain.
* **Tags:** Tags für Organisation und Suche.

### Erstellen einer E-Mail-Kanal-Konfiguration {#create-email-channel-configuration}

>[!PREREQUISITES]
>
>* Mindestens eine Subdomain muss delegiert und aktiv sein.
>* Ihrem Unternehmen muss mindestens ein IP-Pool zugewiesen sein.
>* Sie benötigen die Administratorrolle.

1. Navigieren Sie zu **[!UICONTROL Kanäle]** → **[!UICONTROL Allgemeine Einstellungen]** → **[!UICONTROL Kanalkonfigurationen]**.
1. Klicken Sie **[!UICONTROL Kanalkonfiguration erstellen]**.
1. Geben Sie einen Namen (z. B. „Contoso B2B Marketing — North America„) und eine optionale Beschreibung ein.
1. Wählen Sie den Kanal **[!UICONTROL E-Mail]** aus.
1. Wählen Sie optional Tags aus, um die Konfiguration zu kategorisieren.
1. Wählen Sie im Abschnitt **[!UICONTROL E]** Mail-Typ“ die Option „Marketing“ oder „Transaktion“.
1. Wählen Sie im **[!UICONTROL Subdomain]** eine zuvor delegierte Subdomain aus.
1. Wählen Sie **[!UICONTROL Abschnitt „IP]** Pool“ einen aktiven IP-Pool aus. Sie können den Mauszeiger über die IPs bewegen, um PTR-Einträge anzuzeigen.
1. Konfigurieren Sie die **[!UICONTROL Kopfzeilenparameter]**:
   * Absendername (z. B. „Contoso Marketing„)
   * Aus E-Mail - Muss die ausgewählte Subdomain verwenden (z. B. `marketing@mail.contoso.com`).
   * Name der Antwortadresse und E-Mail-Adresse der Antwortadresse — standardmäßig Von , wenn leer.
   * Fehler-E-Mail - Adresse, die Nicht-Versand-Benachrichtigungen erhält.
1. Aktivieren Sie **[!UICONTROL URL-Tracking]** und wählen Sie die Tracking-Domain aus.
1. Klicken Sie auf **[!UICONTROL Senden]**.
1. Prime führt die Validierung durch: Subdomain-Status, MX-Eintrag, SPF/DKIM/DMARC-Ausrichtung, IP-Pool-Bereitschaft, FBL-Registrierung. Die Konfiguration durchläuft die → „Entwurf → Verarbeitung aktiv“.

>[!NOTE]
>
>Wenn die Validierung fehlschlägt, wechselt die Konfiguration in den Status **[!UICONTROL Fehlgeschlagen]**. Öffnen Sie die Konfiguration, um die Fehlerursache anzuzeigen. Häufige Ursachen sind Fehler bei der Validierung von MX-Datensätzen, IPs im Pool, die nicht mit der Konfiguration übereinstimmen, oder eine Fehlausrichtung von DMARC. Auflösen und erneut übermitteln.

### Bearbeiten oder Löschen einer Kanalkonfiguration {#edit-channel-configuration}

Sie können Kanalkonfigurationen nach der Erstellung bearbeiten, jedoch mit einer wichtigen Einschränkung:

* **Kanal kann nicht geändert werden.** Eine Konfiguration ist an ihren Kanal gebunden.

Wenn Sie eine Konfiguration bearbeiten, die verwendet wird:

* **Für veröffentlichte Journey**: Die Änderung wird bei der nächsten Wiederholung oder bei der nächsten Ausführung angewendet. Die Ausführungen während des Fluges werden mit den vorherigen Einstellungen fortgesetzt.
* **Bei Transaktions- oder Echtzeitnachrichten:** Änderungen werden innerhalb von etwa fünf Minuten weitergegeben.

Um eine Konfiguration zu löschen, entfernen oder aktualisieren Sie zunächst jede E-Mail-Aktion, die auf sie verweist. [!DNL Journey Optimizer B2B Edition] Prime löscht keine Konfiguration, die derzeit von einer aktiven Journey verwendet wird.

### Konfigurationen mit mehreren Kanälen {#multiple-channel-configurations}

Die meisten B2B-Unternehmen verwenden mehrere Kanalkonfigurationen, um Marken, Regionen oder Versandtypen zu trennen. Häufige Muster:

* Eine separate Marketing-Konfiguration pro Geschäftseinheit (z. B. *BU-A Marketing*, *BU-B Marketing*).
* Eine dedizierte Transaktionskonfiguration mit E-Mail-Typ = Transaktionsnachricht für Produkt- oder Vertragsbenachrichtigungen.
* Regionsspezifische Konfigurationen mithilfe regionsspezifischer Subdomains (z. B. `mail.eu.contoso.com`, `mail.us.contoso.com`) zur Abstimmung mit regionalen ISPs und zur Einhaltung der Vorschriften.

>[!TIP]
>
>Benennen Sie Ihre Konfigurationen mit einer klaren, strukturierten Konvention - z. B.: *[Marke] - [Region] - [Typ]*. Dies wird wichtig, sobald Sie ein Dutzend oder mehr Konfigurationen haben.

### Bekannte Einschränkungen {#known-limitations}

* **Methode der benutzerdefinierten Delegierung** für die Subdomain-Delegierung ist noch nicht verfügbar. Verwenden Sie „Vollständig delegiert“ oder CNAME. Benutzerdefinierte Delegierung ist für allgemeine Verfügbarkeit vorgesehen.
* **Dedizierte IP-Pools** sind bei Alpha nicht verfügbar. Der freigegebene IP-Pool ist die einzige Option. Dedizierte IPs werden bei GA ausgeliefert, einschließlich IP-Aufwärmplanung und PTR-Eintragsverwaltung.
* Der HTML-Import von **per HTML- oder ZIP-Upload** ist bei Alpha beschränkt. Der vollständige HTML-Import - einschließlich Code-Editor und visueller Arbeitsfläche mit doppelter Ansicht, Validierung und Inline-CSS-Auto-Konvertierung - wird in Beta ausgeliefert.
* **Nativer Bild-Upload und DAM in Prime** (Hochladen, Organisieren, Bearbeiten) steht auf der Beta-Roadmap. Verwenden von Marketo Design Studio-Assets in dieser Version. Erneute Uploads in Marketo werden in Prime nicht angezeigt.
* **Testprofile, Inhalt simulieren und Testversand durchführen** sind in dieser Version nicht verfügbar. Litmus-Rendering- und SpamAssassin-basierte Spam-Berichte stehen auf der Beta-Roadmap.
* **Personalisierung auf Kontoebene und benutzerdefinierte Objektdaten** sind in dieser Version nicht verfügbar. Verwenden von Profilattributen.
* **Automatisierte Migration von Velocity zu Handlebars** bestehender Marketo-Vorlagen wird über GA ausgeliefert.
* **Kommentare und Zusammenarbeit bei E** Mails (Inline-Kommentare, @mentions, Workflow für die Überprüfung von Anfragen) werden in der Fast-Follow-up-Version bereitgestellt.
* Integrationen mit **AEM Assets, AEM-Inhaltsfragmenten und Adobe Express** stehen auf dem Plan „Schnelle Nachverfolgung“.

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
<!-- -->
