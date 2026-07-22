---
title: Verkaufskennzeichner
description: Automatisieren Sie die B2B-Qualifizierung und Kontaktaufnahme mit dem Sales Qualifier. Es bietet KI-gestützte Forschung, E-Mail-Erstellung, CRM-Integration und KI-Ausgangs-Workflows für BDRs.
feature: Agentic AI, Sales Insights, Account Journeys
role: User
exl-id: cc590444-41df-44fe-830b-92241718ee81
autotag-review: '2026-06-05T16:42:16.451Z'
TQID: 'https://experienceleague.adobe.com/VNgs0cTpjCTG7JpFjFErnVMmRtR-gmw-iRRHZanZDUs'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
  - id: fc1ff3b2-6614-41ad-a113-de48597598fd
  - id: f979fe0e-02fe-4599-b492-7b3df1d4e7dc
subfeature_v2:
  - id: fe583b80-65a2-48c2-b4e1-9ea8fbac0a8a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: a5145b53d6b5c9462392f7c540a81b7d85abdd7b
workflow-type: tm+mt
source-wordcount: 6084
ht-degree: 1%

---

# Verkaufskennzeichner

Sales Qualifier ist eine KI-gesteuerte Anwendung, die Sie mit Adobe Journey Optimizer B2B edition verwenden können. Es implementiert die Account Qualification Agent und optimiert die Workflows für Business Development Representatives (BDRs). Sales Qualifier automatisiert Workflows für die Qualifizierung von Interessenten, Kontaktaufnahme und Käuferinteraktion über verschiedene Kanäle hinweg. Dies reduziert die manuelle BDR-Belastung und beschleunigt die Pipeline-Geschwindigkeit für B2B-Unternehmen.

BDRs können den Browser und die E-Mail-Plug-ins verwenden, um Business Intelligence direkt in CRMs oder Outlook aufzurufen. Im folgenden Video werden der Sales Qualifier und Account Qualification Agent kurz vorgestellt.

>[!VIDEO](https://video.tv.adobe.com/v/3476570?captions=ger)

## Programm-Startseite

Der Verkaufsqualifizierer ist in [!UICONTROL Journey Optimizer B2B edition] enthalten, aber es handelt sich um eine separate App innerhalb der Adobe Experience Platform.

![Startbildschirm des Sales Qualifier](./assets/home-screen.png){width="800" zoomable="yes"}

### Account Qualification Agent

Die Account Qualification Agent (AQA) bildet den Kern des Sales Qualifier. Die AQA verwendet KI, um Ihre Konten zu lesen und festzustellen, welche für den nächsten Schritt bereit sind. Es unterstützt Sie bei der Recherche, beim Erstellen von E-Mails und beim CRM-informierten Kontext, wenn Ihr Unternehmen eine Verbindung zum CRM hergestellt hat.

<!--
## Edit the left navigation bar

At the bottom left of the application, click the _Edit_ ( ![Edit icon](../assets/do-not-localize/icon-edit.svg) ) icon to control which elements are visible in the left navigation. You can also drag and drop them to reorder as you want.
-->

### Grundlegende Verwendung des Agenten

Adobe AI-Agenten verwenden _Abfragen in natürlicher Sprache_ was bedeutet, dass sie in der Textaufforderung dieselbe Sprache verwenden wie bei einem Gespräch mit einer Person. Je detaillierter Sie sind, desto besser sind die Ergebnisse.

Mit natürlicher Sprache können Sie den Agenten bitten:

* `Tell me the latest financial results of Bodea`
* `Tell me more about hiring at TechNova`
* `Tell me about the new AI features in Bodea LumaSecure4`

Iterieren Sie Ihre ausgehenden Workflows, indem Sie Ihre Eingabeaufforderungen verfeinern, um die benötigten Ergebnisse zu erhalten. Beispiel:

* _Entwerfen einer Folge-E-Mail aus dem Kontext wie Einkommensaufrufe oder Berichte._ Bis zu 120 Wörter. Betreffzeile: Fesselnd, mit einem Schlüsselthema. Einführung: Beginnen Sie mit einem direkten Zitat aus Kontextquellen. Hauptteil: Verbinden Sie sich mit Problembereichen und Wertangeboten. CTA: Schließen Sie eine kurze Aufforderung zur weiteren Untersuchung ein.

* _Das Ziel dieser E-Mail ist es, ein Gespräch zu beginnen und Glaubwürdigkeit aufzubauen._ Entwerfen Sie eine E-Mail unter 120 Wörtern, die einen beratenden und einfühlsamen Ton hat. Vermeiden Sie einen allzu vertrauten Ansatz oder Vertriebsansatz und verwenden Sie nicht die Ausdrücke „Ich hoffe, es geht Ihnen gut“, „nur einchecken“ oder „Bitte“.

### Produktzugriff und Benutzergruppen

Der Zugriff auf Funktionen des Verkaufsqualifizierers wird über zwei Benutzergruppen in Adobe Admin Console verwaltet. Produktadministratoren müssen die Gruppen während des Onboardings einrichten, bevor Benutzer auf die Anwendung zugreifen können.

#### Sales Qualifier-Benutzer

Benutzer müssen Mitglieder der Benutzergruppe `Sales Qualifier` sein, um auf die Anwendung „Sales Qualifier“ zugreifen zu können.

1. Erstellen Sie in Adobe Admin Console eine Benutzergruppe mit dem Namen `Sales Qualifier`.
1. Weisen Sie der **das AEP-Profil** Standardproduktion - Alle Zugriffsrechte) zu.
1. Fügen Sie Benutzer hinzu, die Zugriff auf den Sales Qualifier benötigen.

#### Sales Qualifier-Administratoren

Administratoren, die [CRM-Verbindungen](#integrations-and-crm), das [Wissenscenter](#knowledge-center) und globale E-Mail-Opt-out-Einstellungen konfigurieren, müssen auch Mitglieder der `Sales Qualifier Admins`-Benutzergruppe sein.

1. Erstellen Sie in Adobe Admin Console eine Benutzergruppe mit dem Namen `Sales Qualifier Admins`.
1. Fügen Sie die Administratoren sowohl der `Sales Qualifier`- als auch der `Sales Qualifier Admins` hinzu.

Die Mitgliedschaft in beiden Gruppen macht **[!UICONTROL Admin-Einstellungen]** im linken Navigationsbereich unter **[!UICONTROL Administration]** sichtbar. Standardbenutzer können die konfigurierten Felder, Filter und das Playbook verwenden, und die konfigurierte Opt-out-Fußzeile wird auf ihre ausgehenden E-Mails angewendet. Sie können diese Einstellungen nicht ändern.

>[!NOTE]
>
>Die Namen der Benutzergruppen müssen genau mit denen übereinstimmen, die in den vorherigen Schritten gezeigt wurden.

## Prospects

Wählen **[!UICONTROL im]** Navigationsbereich die Option „Interessenten“ aus, um eine Liste der Leads anzuzeigen, auf die Sie zugreifen können. Die Liste bietet eine schnelle Übersicht mit Informationen wie Lead-Status und letzte Aktivität.

![Tabelle mit Interessenten, in der der Lead-Status und die letzte Aktivität für das Interessenten-Management angezeigt werden](./assets/prospects.png){width="800" zoomable="yes"}

### Interessentenliste erstellen

In der Liste potenzieller Kunden werden Personen aus mehreren Quellen zusammengefasst:

* **Interessenten aus CRM** - Wenn Sie ein CRM verbinden, werden automatisch Leads importiert, die dem verbundenen Benutzer gehören. Siehe [Integrationen und CRM](#integrations-and-crm).
* **Importierte Interessenten** - Importieren Sie eine Lead-Liste aus einer CSV-Datei.
* **Manuell hinzugefügte Interessenten** - Fügen Sie eine einzelne Person direkt in der App hinzu.

So fügen Sie potenzielle Kunden hinzu, die nicht aus Ihrem CRM stammen:

1. Wählen Sie auf **[!UICONTROL Seite]** Interessenten“ **[!UICONTROL Interessenten hinzufügen]** aus.
1. Wählen Sie **[!UICONTROL CSV importieren]** oder **[!UICONTROL Manuell hinzufügen]**.

   * Laden Sie für einen CSV-Import die Datei hoch und ordnen Sie ihre Spalten Interessentenfeldern zu.
   * Um eine Person manuell hinzuzufügen, geben Sie deren Details in das Formular ein.

1. Wählen Sie **[!UICONTROL Speichern]** aus.

### Prospects filtern und suchen

Wählen Sie das Symbol _Filter_ ![Filter](../../assets/do-not-localize/icon_filter-outline.svg) aus, um die Liste einzugrenzen. Sie können nach folgenden Kriterien filtern:

* Lead-Status
* Interaktionsbewertung
* Von Marketing markierte interessante Momente
* Stern- und Flammenbewertung
* Zugeordnete Angebote

Administratoren können auch zugeordnete CRM-Felder als Filter verfügbar machen. In **[!UICONTROL Admin-Einstellungen]** aktivieren sie **[!UICONTROL Filterbar]** für die Felder, die die Kundenvertreter verwenden, um Interessenten zu finden. Siehe [Zuordnen von CRM-Feldern](#map-crm-fields-inbound-mapping).

### Details des potenziellen Kunden überprüfen

Interessenten auswählen, um ihr Profil zu öffnen. Überprüfen Sie die wichtigen Signale, bevor Sie sich melden:

* **Aktivitätsliste** - Eine chronologische Liste der Aktivitäten des Interessenten mit einer **KI-Aktivitätsübersicht** oben, die das relevanteste Verhalten der letzten Zeit hervorhebt.
* **Zeitleisten-Ansicht** - Eine visuelle Zeitleiste der Interaktion über alle Kanäle hinweg.
* **Angezeigte Inhalte** - Öffnen Sie den tatsächlichen Inhalt, den ein Interessent angesehen hat, z. B. eine Web-Seite oder ein Asset, direkt aus einer Aktivität heraus.

## Konten

Wählen Sie **[!UICONTROL linken Navigationsbereich]** Konten“ aus, um mit den Konten zu arbeiten, an die Sie verkaufen. Der Sales Qualifier vereint firmografische Details, die Pipeline und die Interaktion, sodass Sie die Kontaktaufnahme auf Kontoebene priorisieren können.

Die Kontoübersicht fasst wichtige Faktoren wie Umsatz, Branche, Unternehmensgröße und Hauptsitz zusammen. Neben diesen Details wird jedes Konto angezeigt:

* **Offene Opportunitys** - Die mit dem Account verbundenen offenen Opportunitys, die von Ihrem verbundenen CRM bezogen werden, damit Sie die Kontaktaufnahme mit der aktiven Pipeline abstimmen können.
* **Top-Engagierte Mitglieder** - Die Kontakte auf dem Konto mit der neuesten Interaktion, sodass Sie wissen, wer in der Einkaufsgruppe Vorrang haben soll.
* **CRM-Eingaben** - Kontofelder, Opportunities und Besitzerinformationen werden von Ihrem verbundenen CRM angezeigt. Siehe [Integrationen und CRM](#integrations-and-crm), wie diese Daten zugeordnet werden.

### Detaillierte Einblicke in Konten

Um einen tiefen Einblick zu erhalten, eröffnen Sie ein Konto. Die Account Qualification Agent (AQA) priorisiert die Signale, die für die Verkaufsstrategie Ihres Unternehmens am relevantesten sind, damit Sie schnell verstehen können, wo sich das Konto befindet, und entscheiden können, was als Nächstes zu tun ist.

## Ausgehende Workflows

>[!NOTE]
>
>Ausgehende Workflows, die von Produktadministratoren erstellt wurden, werden für alle Benutzenden in Ihrer Organisation freigegeben.

Ein _ausgehender Workflow_ ist die Struktur, die der Verkaufsqualifizierer verwendet, um eine zielgesteuerte Kadenz auszuführen. Sie definieren ein Kontaktziel und Zielgruppenkriterien, und die KI schlägt eine Multi-Touch-Kadenz vor und schreibt für jeden Interessenten personalisierten E-Mail-Inhalt. Sie überprüfen und genehmigen jede E-Mail, bevor die Registrierung die Kadenz aktiviert, sodass Nachrichten nur während des konfigurierten Fensters gesendet werden.

Ein ausgehender Workflow verbindet vier Elemente:

* **Ziel** - Das Ergebnis, das Sie aus der Öffentlichkeitsarbeit erwarten (z. B. die Buchung eines Discovery-Anrufs oder die Registrierung eines Fahrevents).
* **Zielgruppenfilter** - Bedingungen, die bestimmen, welche potenziellen Kunden infrage kommen.
* **Kadenz der Touchpoints** - Die geordnete Sequenz von Schritten, jeweils an einem geplanten Tag. Touchpoints können **E-**, **Telefonanrufe** oder **LinkedInMails** sein.
* **Personalisierter E-Mail** Inhalt: Für jeden E-Mail-Touchpoint entwirft die KI Inhalte mithilfe des Interessentenprofils, des Kontokontexts, des Interaktionsverlaufs und der neuesten Nachrichten.

Das Ziel bestimmt alles nachgelagerte: Die KI verwendet es, um Zielgruppenfilter vorzuschlagen, die Kadenz zu entwerfen, Touchpoint-Eingabeaufforderungen zu entwerfen und die Personalisierung für jede generierte E-Mail zu gestalten.

![Registerkarte „Übersicht über ausgehende Workflows“](./assets/outbound-workflow-overview.png){width="800" zoomable="yes"}

### Schlüsselkonzepte

| Konzept | Beschreibung |
| --- | --- |
| **Workflow** | Eine wiederverwendbare ausgehende Aktivität, die durch ein Ziel, Zielgruppenbestimmungsfilter, Kadenz und Einstellungen definiert ist. |
| **Ziel** | Was die Öffentlichkeitsarbeit leisten sollte. |
| **Touchpoint** | Ein Schritt in der Kadenz (E-Mail, Telefonanruf oder LinkedInMail), geplant relativ zur Registrierung. |
| **Touchpoint-Eingabeaufforderung** | Anweisungen, die die KI beim Generieren von E-Mail-Textkörper und -Betreff für einen Interessenten befolgt - Ton, Länge, Fokus und call to action. |
| **Kadenz** | Die vollständige Sequenz von Touchpoints: wie viele, in welcher Reihenfolge und an welchen Tagen. |
| **Zielgruppenbestimmungsfilter** | Eine Bedingung, die den Workflow auf eine Untergruppe von potenziellen Kunden beschränkt. |
| **Entwurf** | Eine generierte E-Mail, die zur Überprüfung bereit, aber noch nicht genehmigt ist. |
| **Argumentation** | Die Erklärung der KI, wie sie eine bestimmte E-Mail geschrieben hat (welche Signale und Datenquellen sie verwendet hat). |
| **Enrollment** | Entwürfe eines Interessenten validieren , wodurch die Kadenz und die Warteschlangen der E-Mails aktiviert werden, die während des Versandfensters des Workflows gesendet werden sollen. |

In den folgenden Abschnitten wird der gesamte Lebenszyklus beschrieben: Erstellen eines Workflows im Assistenten, Überprüfen generierter E-Mails, Genehmigen von potenziellen Kunden und Verwalten von Workflows im Zeitverlauf.

### Erstellen eines ausgehenden Workflows

Der Workflow-Assistent umfasst fünf Schritte: **Ziel**, **Targeting**, **Touchpoints generieren**, **Einstellungen** und **Interessenten hinzufügen**. Jeder Schritt baut auf dem letzten auf; Ihr anfängliches Ziel formt jede nachfolgende Entscheidung.

1. Wählen Sie in der linken Navigation **[!UICONTROL Ausgehender Workflow]** aus.

1. Klicken **[!UICONTROL auf der Registerkarte]** Durchsuchen“ auf **[!UICONTROL + Workflow erstellen]** in der oberen rechten Ecke.

#### Schritt 1: Definieren Sie Ihr Ziel

Das Ziel ist der wichtigste Input: Es teilt der KI mit, wie der Erfolg aussieht, und verankert Targeting, Kadenz und E-Mail-Generierung.

1. Wählen Sie **[!UICONTROL Von Grund auf neu]**, um Ihr eigenes Ziel zu schreiben, oder **[!UICONTROL Von Vorlage starten]**, um eine gespeicherte Vorlage zu verwenden.

   ![Ausgehende Workflows von Grund auf neu erstellen](./assets/outbound-workflow-create-start-from-scratch.png){width="700" zoomable="yes"}

1. Wählen Sie eines der **[!UICONTROL empfohlenen Ziele]** als Ausgangspunkt oder geben Sie Ihr eigenes Ziel ein.

1. Klicken Sie **[!UICONTROL Weiter: Zielgruppenbestimmung]**.

Ziele funktionieren am besten, wenn sie ein **konkretes Ergebnis** und nicht nur ein Thema angeben. Um der KI mehr Möglichkeiten zur Arbeit zu geben, verwenden Sie ein Ziel wie `Book a 15-minute discovery call with marketing leaders evaluating campaign automation` anstelle von `Promote campaign automation`.

#### Schritt 2: Zielgruppenbestimmungsfilter konfigurieren

Zielgruppenbestimmungsfilter definieren, welche potenziellen Kunden infrage kommen. Wenn Sie später Interessenten hinzufügen, werden nur die Interessenten in der Auswahlliste angezeigt, die diesen Filtern entsprechen.

1. Klicken Sie auf den Abwärtspfeil, um die Liste **[!UICONTROL Filter hinzufügen]** anzuzeigen und einen anzuwendenden Filter auszuwählen.

   ![Erstellen von ausgehenden Workflow-Zielgruppenfiltern](./assets/outbound-workflow-create-targeting-filter-list.png){width="700" zoomable="yes"}

1. Legen Sie Werte für den Filter fest.

1. Fügen Sie weitere Filter hinzu, wenn Sie die Zielgruppe eingrenzen möchten.

   ![Ausgehenden Workflow erstellen - Zielgruppenbestimmung hat Filter mit Werten hinzugefügt](./assets/outbound-workflow-create-targeting-filters-values.png){width="600" zoomable="yes"}

1. Klicken Sie **[!UICONTROL Weiter: Touchpoints generieren]**.

#### Schritt 3: Erstellen und Überprüfen von Touchpoints

Nachdem das Targeting festgelegt wurde, erstellt die KI **_Kadenz_**: Sie analysiert Ihr Ziel und die Zielgruppenbestimmung, definiert die Touchpoint-Sequenz und schreibt für jeden Schritt eine **_Touchpoint_** Eingabeaufforderung. Es wird eine mehrstufige Kadenz für jeden Touchpoint an einem bestimmten Tag angezeigt. Die Kadenz kann E-Mail-, Telefonanruf- und LinkedInMail-Schritte mischen.

![Vom ausgehenden Workflow generierte Touchpoint-Kadenz und Eingabeaufforderungen](./assets/outbound-workflow-create-touchpoints.png){width="700" zoomable="yes"}

Um die Eingabeaufforderung zu lesen, erweitern Sie einen E-Mail-Touchpoint. Diese Anweisung leitet die KI beim Schreiben der E-Mail jedes Interessenten an, einschließlich Ton, Länge, Fokus und _call to action_.

**Kadenz neu erzeugen**

Wenn die Kadenz nicht das ist, was Sie möchten, klicken Sie auf **[!UICONTROL Regenerieren]** und geben Sie eine Verfeinerungsanweisung ein. Beispiel:

* `Make it 3 touchpoints across 2 weeks`
* `Lead with an executive briefing offer in the first email`
* `Add a nurture touch focused on a relevant case study`

Die KI schreibt die gesamte Kadenz auf der Grundlage Ihrer Anweisungen um.

Um einen einzelnen E-Mail-Touchpoint anzupassen, ohne die gesamte Kadenz zu regenerieren, bearbeiten Sie den Aufforderungstext direkt in seinem Textbereich.

**Verwenden Sie ein Playbook in Ihren Eingabeaufforderungen**

Wenn Ihr Unternehmen im [Wissenscenter](#knowledge-center) ein Playbook erstellt hat, können Sie die KI anweisen, beim Schreiben von E-Mails daraus zu schöpfen. Benennen Sie in der Eingabeaufforderung das Dokument und den Kontext, den die KI verwenden soll, z. B. `Use the ABC positioning guide from the Knowledge Center and focus on the security value proposition`. Die generierten E-Mails spiegeln dann die Nachricht in diesem Playbook wider.

Wenn die Kadenz und die Eingabeaufforderungen nach rechts aussehen, klicken Sie auf **[!UICONTROL Weiter: Einstellungen]**.

Verfeinern von Touchpoint-Eingabeaufforderungen vor der Generierung pro Interessent: Diese Eingabeaufforderungen sind die Kernanweisungen, die die KI später für jeden Interessenten verwendet. Die hier verbrachte Zeit kann für alle generierten E-Mails skaliert werden.

#### Schritt 4: Workflow-Einstellungen konfigurieren

Der **Einstellungen** steuert, wie der Workflow ausgeführt wird.

![Einstellungen für ausgehende Workflows](./assets/outbound-workflow-create-settings.png){width="700" zoomable="yes"}

1. Überprüfen Sie den **[!UICONTROL Workflow-Namen]** und ändern Sie ihn, wenn Sie eine klarere Beschriftung wünschen.
1. Bestätigen **[!UICONTROL unter „Max. potenzielle]** pro Workflow“ die Obergrenze für die Anzahl der potenziellen Kunden, die der Workflow gleichzeitig verwalten kann.
1. Legen Sie das **[!UICONTROL Sendefenster]** für die Stunden fest, die ausgehende E-Mails senden dürfen.
1. Aktivieren Sie **[!UICONTROL Wochenenden überspringen]**, um jeden Touchpoint, der auf ein Wochenende fällt, auf den nächsten Werktag zu verschieben.
1. Um Follow-up-Touchpoints automatisch zu stoppen, sobald ein Interessent ein Meeting bucht, aktivieren Sie **[!UICONTROL Meeting-Buchungspause]**.
1. Bestätigen Sie, dass **[!UICONTROL Zeitzone]** mit Ihrer Audience übereinstimmt.
1. Klicken Sie **[!UICONTROL Speichern und Interessenten hinzufügen]**.

Die Opt-out-Fußzeile wird global von einem Administrator konfiguriert und gilt unabhängig von den Workflow-Einstellungen für ausgehende E-Mails. Siehe [Globale Abmeldesynchronisierung](#global-opt-out-sync).

#### Schritt 5: Interessenten hinzufügen und E-Mail-Generierung starten

Beim Speichern wird die Perspektivauswahl-Ansicht geöffnet, die bereits nach dem Targeting für Schritt 2 gefiltert wurde.

![Ausgehender Workflow - Interessenten hinzufügen](./assets/outbound-workflow-create-add-prospects.png){width="700" zoomable="yes"}

1. Überprüfen Sie die Liste.

   Die Zeilen enthalten normalerweise den Namen des Interessenten, das Konto, die E-Mail-Adresse, die Stellenbezeichnung, den Interaktionsstatus und den Status des Interessenten.

1. Filter hier anpassen, wenn Sie die Liste erweitern oder eingrenzen müssen.
1. Wählen Sie Interessenten mithilfe der Kontrollkästchen aus.
1. Klicken Sie auf **[!UICONTROL Weiter: Touchpoints überprüfen]**, um mit der Erstellung **E** Mails für einzelne Interessenten zu beginnen.

Die KI generiert personalisierte E-Mails für jeden ausgewählten Interessenten **jeden E-Mail-Touchpoint** an der Kadenz. Telefon- und LinkedInMail-Touchpoints bleiben als geplante Schritte in der Kadenz. Die Generierung kann im Hintergrund ausgeführt werden. Verwenden Sie **[!UICONTROL Bei Fertigstellung benachrichtigen]** wenn Sie andere Arbeiten fortsetzen möchten, während diese abgeschlossen sind.

Für jeden Interessenten kombiniert die KI jede Touchpoint-Eingabeaufforderung mit Interessenten-spezifischen Daten (Person, Konto, Interaktionsverlauf, aktuelle Nachrichten), um Betreffzeile und Text zu erstellen.

### Überprüfen und Verfeinern generierter E-Mails

Nach Abschluss der Generierung zeigt die Workflow-Detailansicht ein Banner zur Überprüfung von Entwürfen an. Eine Überprüfung ist erforderlich, und es wird nichts gesendet, bis Sie Ihre Genehmigung erteilen.

![Ausgehende Workflow-Prüfungsgenerierte E-Mails](./assets/outbound-workflow-create-review-generated-emails.png){width="700" zoomable="yes"}

1. Klicken Sie in der Workflow-Detailansicht **[!UICONTROL Banner auf]** Entwürfe überprüfen“.
1. Der Schritt **[!UICONTROL Touchpoints überprüfen]** umfasst zwei Registerkarten:
   * **[!UICONTROL Bereit für Überprüfung]** - E-Mails, deren Generierung abgeschlossen ist.
   * **[!UICONTROL Generating]** - E-Mails werden noch geschrieben.
1. Klicken Sie in der Liste der Interessenten auf der linken Seite auf einen Namen, um die Kontaktpunkte dieses Interessenten auf der rechten Seite zu laden.
1. Verwenden Sie den Pfeil (**>**) auf einem Touchpoint, um die gesamte Betreffzeile und den gesamten Textkörper zu erweitern und zu lesen.

#### Lesen der KI-Argumentation

Für jede generierte E **[!UICONTROL Mail wird in &quot;]**&quot; erläutert, wie die KI diese Nachricht erstellt hat, einschließlich Signalen, Attributen und Quellen, die den Inhalt und call to action geprägt haben. Überprüfen Sie diese Informationen und validieren Sie die Personalisierung, bevor Sie sie genehmigen.

![KI-Argumentation für ausgehende Workflows generierte E-Mails](./assets/outbound-workflow-create-review-generated-email-reasoning.png){width="600" zoomable="yes"}

#### E-Mails direkt bearbeiten

Für kleine Bearbeitungen (Formulierung, Ton, ein einziger Satz):

1. Klicken Sie auf dem erweiterten Touchpoint auf das Symbol _Bearbeiten_, um den Editor zu öffnen.
1. Bearbeiten Sie die Betreffzeile oder den Text.
1. Klicken Sie auf **[!UICONTROL Speichern]**.

#### E-Mails mit KI verfeinern

Für größere Änderungen (Umstrukturierung, Verlagerung, Hervorhebung oder Umgestaltung der Nachricht) verwenden Sie **[!UICONTROL Mit KI generieren]**. Der KI-Agent schreibt die E-Mail neu, wobei der Personalisierungskontext beibehalten wird.

1. Klicken Sie im E-Mail-Editor auf **[!UICONTROL Mit KI generieren]**.

   ![Verfeinerung ausgehender Workflows mit KI](./assets/outbound-workflow-create-review-generated-email-edit-regenerate.png){width="600" zoomable="yes"}

1. Geben Sie eine klare Anweisung ein, z. B.:
   * `Make it shorter and more direct. Keep it under 100 words.`
   * `Focus more on the prospect's role and how the solution helps them specifically.`
   * `Change the call-to-action to suggest a 15-minute introductory call instead.`
1. Überprüfen Sie die Revision und passen Sie sie bei Bedarf manuell an.
1. Klicken Sie auf **[!UICONTROL Speichern]**.

>[!TIP]
>
>Direkte Bearbeitungen passen zu Text und Ton. Verwenden Sie _[!UICONTROL Mit KI generieren]_ um die E-Mail von Grund auf neu zu schreiben.

### Interessenten genehmigen und registrieren

Validierung aktiviert die Kadenz für einen Interessenten. Bis zur Genehmigung und Registrierung eines potenziellen Kunden sendet das System keine E-Mails an ihn.

1. Wählen Sie in der linken Liste die Interessenten aus, deren E-Mails Sie geprüft haben und senden möchten.
1. Klicken Sie **[!UICONTROL Interessenten genehmigen und registrieren]** (unten rechts).

![Ausgehender Workflow - Interessenten auswählen und genehmigen](./assets/outbound-workflow-create-approve-enroll-prospects.png){width="700" zoomable="yes"}

Genehmigte E-Mails werden während des Workflows **Sendefenster** in der konfigurierten **Zeitzone** an jedem geplanten Touchpoint-Tag relativ zur Registrierung gesendet. Interessenten, die Sie nicht genehmigen, verbleiben in **[!UICONTROL Bereit für Überprüfung]** bis Sie handeln. Nach der Genehmigung wird der Workflow entsprechend der von Ihnen definierten Kadenz ausgeführt.

### Verwalten vorhandener Workflows

Auf der Seite _[!UICONTROL Ausgehender Workflow]_ werden auf der Registerkarte **[!UICONTROL Durchsuchen]** alle Workflows aufgelistet. Jede Karte zeigt das Ziel, konfigurierte Touchpoints und Leistungsmetriken. Verwenden Sie diese Ansicht, um aktive Workflows zu überwachen, zu Entwürfen zurückzukehren, die noch überprüft werden müssen, oder einen Workflow zu öffnen, um weitere Interessenten hinzuzufügen.

### Best Practices für ausgehende Workflows

* **Investieren Sie in das Ziel.** Nachgelagertes Targeting, Kadenz und E-Mails werden alle zum Ziel zurückverfolgt. Konkrete, ergebnisorientierte Ziele übertreffen vage Ziele.
* **Touchpoint-Eingabeaufforderungen vor der Generierung pro Interessent abschließen.** Nach der Massengenerierung werden Änderungen normalerweise jeweils nur von einem Interessenten vorgenommen.
* **Verwenden von Argumentation als Qualitätsprüfung.** Wenn das falsche Signal hervorgehoben wird - oder ein offensichtliches Signal fehlt - bearbeiten Sie die E-Mail oder besuchen Sie die Touchpoint-Eingabeaufforderung erneut und regenerieren Sie die Kadenz.
* **Passen Sie das Bearbeitungswerkzeug an die Änderung an.** Direkte Bearbeitungen für Wortlaut und Ton; **[!UICONTROL Mit KI generieren]** für Umstrukturierung oder Reframing.
* **Genehmigen Sie nur, was Sie geprüft haben.** Erweitern Sie Touchpoints, lesen Sie den Inhalt und verfeinern Sie ihn vor der Registrierung nach Bedarf.

### Globale Abmeldesynchronisierung

Admins können an jede ausgehende E-Mail eine Light-Touch-Fußzeile zur Abmeldung anhängen, die den vorab genehmigten [!DNL Marketo] verwendet. Wenn ein Interessent den Ausschluss-Link auswählt, unterdrückt der Verkaufskennzeichner den Interessenten dauerhaft von weiteren E-Mails und synchronisiert den Ausschluss-Status wieder mit dem verbundenen CRM. Siehe [Konfigurieren einer globalen E-Mail-Abmeldung](#configure-global-email-opt-out).

## E-Mail-Postausgang

Im Bedienfeld E-Mail-Postausgang werden alle automatisierten E-Mails aufgelistet, die Sie gesendet haben.

<!--
## Meeting bookings

This panel displays all meetings set up through automation.

## Chat inbox

This panel displays all your chat threads.

![Panel showing chat threads with contact and thread summaries for sales automation](assets/chat-inbox.png)

You can interact with clients, and see summaries for the contact and the thread so that you can quickly know where you are in the thread.

-->

## Aufgaben

Der Bereich _Aufgaben_ im Sales Qualifier bietet BDRs (Business Development Representatives) einen speziellen Raum zur Verwaltung und Verarbeitung ihrer ausgehenden Workflow-Aktionen. Die ausgehende Workflow-Engine generiert automatisch Aufgaben, die die spezifischen Aktionen darstellen, die ein BDR bei jedem Interessenten durchführen muss - Telefonanrufe, LinkedInMails und E-Mail-Überprüfungen.

Bei der Aufgabenverwaltung handelt es sich um **Verarbeitungswarteschlange** nicht um eine Aufgabenliste. Sie können eine Aufgabe öffnen, eine Aktion ausführen, sie als abgeschlossen markieren und mit der nächsten fortfahren - und das alles, ohne die Seite zu verlassen.

Wählen Sie **[!UICONTROL Aufgaben]** in der linken Navigationsleiste aus, um die vollständige Aufgabenseite zu öffnen. Diese Seite ist der primäre Arbeitsbereich für die Bearbeitung von Aufgaben nach und nach.

![Aufgabenseite mit Aufgabenwarteschlange und Detailbereich](./assets/tasks.png){width="800" zoomable="yes"}

<!--
**Homepage feed** - The homepage displays a running feed of your most urgent tasks, with overdue items at the top followed by today's tasks. Each item in the feed has an "Open" button that takes you directly to that task in the Tasks page with the detail panel already loaded.
-->

### Aufgabentypen

Alle Aufgaben sind an ausgehende Workflow-Schritte gebunden. Es gibt drei Typen:

**Telefonanruf** - Wird erstellt, wenn eine Kadenz einen Telefonanrufschritt erreicht. Das Aufgabenbedienfeld zeigt vom Agenten generierte Tonpunkte und ein Feld Inline-Notizen zur Erfassung von Anrufnotizen an.

**LinkedInMail** - Wird erstellt, wenn eine Kadenz einen LinkedInMail-Schritt erreicht. Das Aufgabenbedienfeld zeigt eine von KI generierte Betreffzeile und einen Nachrichtentext an, die Sie kopieren und außerhalb des Produkts versenden können.

**E-Mail-Überprüfung** - Wird erstellt, sobald das System die Generierung personalisierter E-Mails für einen in einem Workflow registrierten potenziellen Kunden abgeschlossen hat. Sie überprüfen und genehmigen die E-Mails, bevor der Ausgang für diesen potenziellen Kunden beginnt. Jeder Interessent erhält eine separate E-Mail-Prüfungsaufgabe. Wenn Sie zehn Interessenten für einen Workflow registrieren, werden nach Abschluss der Generierung bis zu 10 E-Mail-Prüfungsaufgaben angezeigt.

### Aufgabenverwaltung

Die Seite Aufgaben ist in zwei Bereiche unterteilt:

* **Links - Aufgabenliste:** Ihre Aufgabenwarteschlange, sortiert und gefiltert nach den ausgewählten Ansichts- und Sortiereinstellungen.
* **Rechts - Aufgabenarbeitsbereich:** Details für die ausgewählte Aufgabe, einschließlich Informationen für Interessenten, Workflow-Kontext, aufgabenspezifische Inhalte und Aktionssteuerelemente.

Wenn Sie eine Aufgabe im linken Bereich auswählen, werden deren Details in den rechten Bereich geladen, ohne die Seite zu verlassen.

#### Warteschlangensteuerung

Das Arbeitsfenster enthält Steuerelemente **Weiter** und **Zurück**, um Ihre Aufgabenwarteschlange nacheinander zu durchlaufen. Die Warteschlange berücksichtigt alle Sortier- und Filtereinstellungen, die Sie auf die Liste anwenden. Wenn Sie also überfällige Telefonanrufaufgaben nach Fälligkeitsdatum sortiert durcharbeiten, durchlaufen _Weiter_ und _Zurück_ genau dieses Set.

Wenn Sie eine Aufgabe als abgeschlossen markieren, wird das Bedienfeld automatisch zur nächsten Aufgabe in der Warteschlange weitergeleitet.

#### Hinweise

Für Telefonanrufe und LinkedInMail-Aufgaben steht im Arbeitsbereich ein Feld Inline-Notizen zur Verfügung. Notizen werden automatisch gespeichert, wenn Sie auf „Abwesend“ klicken, damit sie beim Navigieren zu einer anderen Aufgabe nicht verloren gehen, bevor Sie die aktuelle Aufgabe als abgeschlossen markieren.

#### Aufgabenaktionen

Verwenden Sie die folgenden Aktionen, um Ihre Aufgaben zu verwalten:

* **[!UICONTROL Als abgeschlossen markieren]** - Die primäre Aktion. Verwenden Sie diese Aktion, nachdem Sie die Aufgabe ausgeführt haben - den Aufruf durchgeführt, die InMail gesendet oder die E-Mails überprüft und genehmigt haben. Nach Abschluss wird die Aufgabe als **Abgeschlossen“ aufgezeichnet** die Warteschlange wird automatisch fortgesetzt.

* **[!UICONTROL Touchpoint überspringen]** - verfügbar über das Menü „Überlauf“ im Arbeitsbereich. Verwenden Sie diese Option, wenn Sie diesen Schritt nicht abschließen können, der Interessent jedoch eine gültige Zielgruppe im Workflow bleibt.
  * Der Interessent geht in der Kadenz zum nächsten Schritt über. Zukünftige Aufgaben werden weiterhin planmäßig generiert.
  * Wählen Sie einen Grund aus: *Ungültige Kontaktinformationen*, *Fehlerhaftes Timing*, *Inhalt nicht relevant* oder *Sonstiges* (mit einem Freitext-Feld).
  * Der Aufgabenstatus wird auf **Übersprungen** festgelegt und mit dem Grund und dem Zeitstempel protokolliert.
  * Wenn dies der letzte Schritt im Workflow war, endet die Ausführung des Workflows des Interessenten. Die Aufgabe wird weiterhin als Übersprungen (nicht entfernt) protokolliert.

* **[!UICONTROL Aus Workflow entfernen]** - verfügbar über das Menü „Überlauf“ im Arbeitsbereich. Verwenden Sie diese Option, wenn der Interessent nicht mehr zu diesem Workflow gehört.

  Wenn Sie einen Interessenten aus einem Workflow entfernen:
  * Alle ausstehenden und zukünftigen Aufgaben für diesen potenziellen Kunden innerhalb dieses Workflows werden abgebrochen.
  * Der Registrierungsstatus des Interessenten ändert sich in **Von BDR entfernt**.
  * Wählen Sie einen Grund aus: *linke Firma*, *Duplizieren*, *Falsche Anpassung*, *Bereits konvertiert* oder *Sonstige* (mit einem Textfeld).
  * Ein Bestätigungsdialogfeld wird angezeigt: *„Diese Aktion löscht alle verbleibenden Touchpoints für [Interessent] in [Workflow-Name]. Fortfahren?“*
  * Der Aufgabenstatus wird auf &quot;**&quot;**. Alle abgebrochenen gleichrangigen Aufgaben sind ebenfalls mit **Entfernen** gekennzeichnet.

>[!NOTE]
>
>Ursachendaten für Überspringen und Entfernen informieren Analytics, einschließlich Kanalüberspringungsraten, Workflow-Entfernungsraten und Hauptgründen. Dies trägt zur Verbesserung der Workflow-Qualität bei und fließt in die Leistungsanalyse im Laufe der Zeit ein.

**Automatisches Überspringen**

Stagnierende LinkedInMail- und Telefonanruftasks werden automatisch übersprungen, wenn sie für zwei Tage unvollständig bleiben. Durch das automatische Überspringen bleibt ein potenzieller Kunde in der Kadenz, ohne die Ausführung zu stoppen, und die E-Mail-Timeline wird nicht beeinflusst. Geplante E-Mail-Touchpoints werden weiterhin wie geplant gesendet.

### Aufgabenstatus

Jede Aufgabe durchläuft die folgenden Status:

| Status | Beschreibung |
|---|---|
| **Ausstehend** | Erstellt, aber der vorherige Workflow-Schritt wurde noch nicht abgeschlossen. Nicht in der Aufgabenliste sichtbar. |
| **Künftig** | Der vorherige Schritt ist abgeschlossen, das Fälligkeitsdatum liegt jedoch in der Zukunft. Sichtbar und umsetzbar - Sie können sie frühzeitig abschließen, wenn der richtige Zeitpunkt gekommen ist. |
| **Öffnen** | Heute fällig. Sichtbar und umsetzbar. |
| **Überfällig** | Überfällig am, noch nicht abgeschlossen. Sichtbar, ausführbar und visuell gekennzeichnet. |
| **Abgeschlossen** | Sie haben ausgeführt und die Aufgabe als abgeschlossen markiert. |
| **Übersprungen** | Sie haben diesen Touchpoint übersprungen. Der Interessent kommt im Workflow voran. |
| **entfernt** | Sie haben den potenziellen Kunden aus dem Workflow entfernt. Alle gleichrangigen Aufgaben werden abgebrochen. |
| **Abgebrochen** | System wurde aufgrund einer Workflow-Änderung oder Entfernung eines Interessenten abgebrochen. |

### Listenansichten

Verwenden Sie die Registerkarten oben in der Aufgabenliste, um zwischen Ansichten zu wechseln:

* **Heute** *(Standard)* - Heute fällige Aufgaben, die noch nicht abgeschlossen wurden.

* **Überfällig** - Aufgaben, deren Fälligkeitsdatum überschritten wurde und noch offen sind. Befassen Sie sich zuerst mit diesen Aufgaben.

* **Kommend** - Aufgaben mit einem zukünftigen Fälligkeitsdatum, bei denen der vorherige Workflow-Schritt bereits abgeschlossen wurde. Diese Aufgaben sind frühzeitig sichtbar, sodass Sie im Voraus planen oder früher handeln können, wenn der Zeitpunkt richtig ist (z. B. wenn Sie bereits einen Anruf mit einem Interessenten haben). Das geplante Fälligkeitsdatum wird angezeigt, damit Sie den gewünschten Zeitpunkt kennen.

* **Abgeschlossen** - Ein Datensatz mit Aufgaben, die Sie abgeschlossen, übersprungen oder entfernt haben. Nützlich für Überprüfungs- und Auditzwecke.

### Filtern und Suchen

Es gibt mehrere Möglichkeiten, die Aufgabenliste zu filtern:

* Filtern Sie mithilfe einer Mehrfachauswahlliste nach Aufgabentyp. Wenn Sie mehrere Typen auswählen, werden Aufgaben angezeigt *die mit* ausgewählten Typen übereinstimmen (z **B. Telefonanruf** E-Mail-Überprüfung).

* Nach Aufgabenstatus filtern. Wenn Sie mehrere Status auswählen, werden Aufgaben angezeigt, die einem der ausgewählten Status entsprechen.

* Filtern Sie mithilfe der **-Logik gruppenübergreifend**. Beispielsweise zeigt `Type = Phone Call and Status = Overdue` nur überfällige Aufrufaufgaben an.

Verwenden Sie die Suchleiste, um Aufgaben nach Interessentenname, Firmenname oder Interaktionsname zu suchen. Die Suche gilt zusammen mit allen aktiven Filtern. Nur Textübereinstimmung - Exakte Teilübereinstimmung, keine Ungefährsuche.

### Sortieren

Verwenden Sie das Steuerelement **Sortieren nach**, um festzulegen, wie die Aufgabenliste sortiert werden soll. Die Sortierung bestimmt auch die Reihenfolge, in der sich der nächste und der vorherige Durchlauf durch die Warteschlange bewegen.

| Sortieroption | Verhalten |
|---|---|
| **Fälligkeitsdatum (aufsteigend)** *(Standard)* | Ältestes Fälligkeitsdatum zuerst. Überfällige Aufgaben werden vor den heutigen Aufgaben angezeigt. |
| **Fälligkeitsdatum (absteigend)** | Spätestes Fälligkeitsdatum zuerst. |
| **Erstellungsdatum (neueste)** | Zuletzt erstellte Aufgaben zuerst. |
| **Erstellungsdatum (ältestes)** | Die ältesten erstellten Aufgaben zuerst. |
| **Aufgabentyp** | Gruppiert nach Typ in der richtigen Reihenfolge: Telefonanruf → LinkedInMail → E-Mail-Überprüfung. Innerhalb jeder Gruppe, sortiert nach Fälligkeitsdatum aufsteigend. |

### Überfällige Aufgaben

Eine Aufgabe ist am Tag nach ihrem Fälligkeitsdatum überfällig, wenn sie nicht abgeschlossen wurde. Überfällige Aufgaben:

* In der Ansicht **Überfällig** und oben im Homepage-Feed anzeigen.
* Werden in der Aufgabenliste visuell mit einem „Überfällig“-Badge gekennzeichnet.
* Vollständig umsetzbar bleiben - Sie können sie abschließen, überspringen oder entfernen.

### Anstehende Aufgaben

Anstehende Aufgaben werden erstellt, sobald ein Interessent einen Workflow-Schritt abgeschlossen hat, selbst wenn der nächste Fälligkeitsdatum für den Schritt noch in der Zukunft liegt. Durch diese Sichtbarkeit erhalten Sie einen frühzeitigen Einblick in insight in Ihre Pipeline, sodass Sie im Voraus planen oder frühzeitig handeln können, wenn die Gelegenheit auftritt.

Anstehende Aufgaben zeigen ihr geplantes Fälligkeitsdatum an, sodass Sie immer wissen, wann sie gelöst werden sollen. Die frühzeitige Durchführung einer anstehenden Aufgabe wird vollständig unterstützt - die Workflow-Engine zeichnet das tatsächliche Abschlussdatum auf und treibt den potenziellen Kunden normal voran.

### Aufgabenabschluss

Die Aufgabenfertigstellung ist nicht auf die Seite „Aufgaben“ beschränkt.

**Ansicht „Interessent interagieren“:** Touchpoint-Vorschauen auf der Seite eines interagierenden Interessenten enthalten eine Aktion _Als abgeschlossen markieren_ neben einer Inhaltsvorschau und einem optionalen Feld Notizen . Wenn Sie hier eine Aufgabe abschließen, wird ihr Status auf der Seite Aufgaben sofort aktualisiert. Diese Ansicht ändert nichts am automatischen Vorverlagerungsverhalten - es ist eine Ansichts- und Aktionsfläche, keine Warteschlangen-Verarbeitungsfläche.

**Salesforce (CRM-Plug-in):** Das Sales Qualifier-Plug-in in Salesforce zeigt den Aufgabenstatus (bevorstehende, ausstehende, abgeschlossene, überfällige, übersprungene) in der Karte für ausgehende Workflows an. In der aktuellen Version ist die CRM-Karte **schreibgeschützt** - Sie können den Aufgabenstatus sehen, müssen jedoch Aufgaben im Verkaufsqualifizierer abschließen.

### Leere Zustände

* **Heute ohne Aufgaben:** Sie sehen eine _Sie sind heute alle eingeholt_ Nachricht. Wenn anstehende Aufgaben vorhanden sind, wird eine Eingabeaufforderung angezeigt als _Sie haben [N] anstehende Aufgaben - Anstehende Aufgaben anzeigen_.
* **Überfällige Aufgaben vorhanden:** Sie werden aufgefordert, überfällige Aufgaben zuerst anzugehen.

## Buchung eines Meetings

Der Sales Qualifier wandelt engagierte Konversationen in gebuchte Meetings um, ohne den ausgehenden Fluss zu verlassen. Wenn Sie Ihren Kalender verbinden, generiert Sales Qualifier einen persönlichen Buchungslink, über den Interessenten Zeit mit Ihnen planen können.

* **Buchungslinks** - Konfigurieren Sie Ihre Kalenderverbindung und -verfügbarkeit in [Profileinstellungen](#profile-settings). Ihr Buchungs-Link kann Ihrer E-Mail-Signatur hinzugefügt werden, damit er in ausgehenden E-Mails angezeigt wird.
* **Automatische Einfügung in einer Kadenz** - Sales Qualifier fügt Ihren Buchungslink an geeigneten Stellen in einer Kadenz ein, sodass die Einladung zu einem Treffen angezeigt wird, wenn es am relevantesten ist. Sie können die Platzierung manuell überschreiben.
* **Buchungspause** - Wenn ein potenzieller Kunde ein Meeting bucht, **[!UICONTROL Buchungspause für das Meeting]** weitere Folgemaßnahmen automatisch gestoppt. Siehe [Konfigurieren von Workflow-Einstellungen](#step-4-configure-workflow-settings).

Verfolgen Sie Buchungsergebnisse im Abschnitt [Performance](#performance) .

## Knowledge Center

Das _[!UICONTROL Knowledge Center]_ ermöglicht Account Qualification Agent (AQA) Zugriff auf Ihre eigenen Vertriebsmaterialien, sodass der Sales Qualifier Recherchen, Qualifikationserkenntnisse und Öffentlichkeitsarbeit generieren kann, die widerspiegeln, wie Ihr Unternehmen verkauft. Das Erstellen und Verwalten des Playbooks ist eine Administratoraufgabe.

![Wissenszentrum](./assets/integrations-knowledge-center.png){width="700" zoomable="yes"}

### Verkaufsmaterial hochladen

1. Erweitern Sie in der linken Navigation **[!UICONTROL Administration]** und wählen Sie **[!UICONTROL Admin-Einstellungen]** aus.
1. Wählen Sie **[!UICONTROL Wissenszentrum]** unter **[!UICONTROL Integrationen]** aus.
1. Legen Sie die **[!UICONTROL Firmenname]** und **[!UICONTROL Firmen-URL]** fest, die Sales Qualifier verwendet, um Ihr Unternehmen zu durchsuchen und E-Mails zu entwerfen.
1. Laden Sie Vertriebsmitteilungen, ideale Kundenprofile (ICPs), Positionierungsleitfäden und anderes Vertriebsmaterial im PDF-, PPTX- oder DOCX-Format hoch.

Jedes hochgeladene Dokument zeigt seinen Verarbeitungsstatus an, z **[!UICONTROL B. &quot;]**&quot; und den Zeitpunkt der letzten Aktualisierung.

### Playbook erstellen

Nachdem Sie Ihre Dokumente hochgeladen haben, wählen Sie **[!UICONTROL Playbook erstellen]** aus, um sie in ein Playbook umzuwandeln.

>[!NOTE]
>
>Die Verarbeitung eines Playbooks dauert etwa 24 Stunden, bevor es einsatzbereit ist.

Wenn das Playbook fertig ist, dient es sowohl der Öffentlichkeitsarbeit als auch der Unterstützung:

* **Ausgehende E-Mail-Eingabeaufforderungen** - Referenzieren Sie das Playbook beim Generieren von E-Mails, indem Sie das Dokument und den Kontext in Ihrer Eingabeaufforderung benennen. Siehe [Erstellen und Überprüfen von Touchpoints](#step-3-generate-and-review-touchpoints).
* **Konversationeller Vertriebsassistent** - Um aus dem Playbook zu ziehen, richten Sie den Assistenten auf das Knowledge Center. Siehe [Konversationeller Vertriebsassistent](#conversational-sales-assistant).

## Dialogfähiger Vertriebsassistent

Der Conversational Sales Assistant ist ein Chat-Erlebnis, bei dem Sie Fragen in natürlicher Sprache stellen und Antworten in Ihrem Vertriebskontext erhalten. Der Assistent nutzt folgende Funktionen:

* Ihre interne Wissensdatenbank, einschließlich aller [Wissenscenter](#knowledge-center) Playbooks
* CRM-Signale von Ihrem verbundenen CRM
* [!DNL Marketo] Aktivitäts- und Interaktionsdaten
* Web-Recherche

Verwenden Sie den Assistenten, um sich vor der Kontaktaufnahme vorzubereiten, z. B. um die Kontopositionierung im Vorfeld eines Meetings aufzubauen. Um aus einem erstellten Playbook zu ziehen, richten Sie in Ihrer Frage den Assistenten auf das Knowledge Center. Beispiel: `From the Knowledge Center, help me position our security solution for ABC Corp ahead of tomorrow's call.`

## Leistung

Im Abschnitt **[!UICONTROL Performance]** wird angezeigt, wie sich der ausgehende Datenverkehr entwickelt, sodass Sie sehen können, was funktioniert und wo Anpassungen vorgenommen werden müssen.

### E-Mail-Leistung

Überprüfen Sie das Volumen und die Effektivität Ihrer ausgehenden E-Mail:

* E-Mails gesendet
* Öffnungsrate
* Klickrate
* Antwortquote

Der Sales Qualifier identifiziert Abwesenheitsantworten und Bounces mit ihren entsprechenden Status, sodass Sie sie von Interessentenengagements unterscheiden können.

### Meeting-Buchungsleistung

Die Statuskarten für die Besprechungsbuchung fassen zusammen, wo sich Ihre gebuchten Besprechungen befinden. Filtern Sie die Karten so, dass sie sich auf die Meetings und Status konzentrieren, die Sie überprüfen möchten.

## Integrationen und CRM

Bei Integrationen stellt Sales Qualifier eine Verbindung zu Ihrem CRM her, sodass die Account Qualification Agent (AQA)- und Outbound-Workflows eine konsistente Ansicht von Leads, Konten, Kontakten, Aktivitäten und Eigentümern in Salesforce oder Microsoft Dynamics 365 gemeinsam haben. Der Verkaufskennzeichner liest CRM-Verkaufsdaten und -aktivitäten, um Erkenntnisse zu bereichern, und kann protokollierte Outreach-Aktivitäten und den Opt-out-Status zurückschreiben. Andernfalls werden Ihre CRM-Datensätze über diese Verbindung nicht geändert.

CRM-Verbindungen, Zuordnung eingehender Felder und Aktivitätssynchronisierung werden von einem Administrator unter **[!UICONTROL Administration]** > **[!UICONTROL Admin-Einstellungen]** > **[!UICONTROL CRM-Verbindungen]** konfiguriert. Standardbenutzer verwenden die konfigurierten CRM-Daten und -Filter, können diese Einstellungen jedoch nicht ändern.

### CRM MCP und das eingebettete Plug-in

Der Sales Qualifier arbeitet auf mehr als eine Weise mit Ihrem CRM zusammen:

* **Abfragen von CRM-Daten über das CRM-MCP** - Account Qualification Agent fragt Live-CRM-Daten über das CRM-MCP ab, sodass Antworten und Einblicke den aktuellen Status Ihrer Datensätze widerspiegeln.
* **Eingebettetes Plug-in** - Das eingebettete CRM-Plug-in zeigt [!DNL Marketo Sales Insights] (MSI)-Kerneinblicke zusammen mit den neuen Agentendaten direkt in Ihrem CRM. Fügen Sie über das Plug-in mit einem Klick einen Interessenten zum Verkaufsqualifizierer hinzu.
* **Aktivitätssynchronisierung** - Wenn ein Administrator die **[!UICONTROL Aktivitätssynchronisierung]** aktiviert, werden Outreach-Aktivitäten wieder mit dem CRM synchronisiert, damit die Vertriebsmitarbeiter die Aktivität „Verkaufsqualifizierer“ in den bereits verwendeten Tools sehen.

>[!IMPORTANT]
>
>Der Zugriff auf **[!UICONTROL Admin]** Einstellungen erfordert die Mitgliedschaft in den Benutzergruppen `Sales Qualifier` und `Sales Qualifier Admins`.

### CRM-Zugriffsbereich

Der Sales Qualifier liest die erforderlichen CRM-Entitäten und kann nur einen definierten Datensatz zurückschreiben. Zu den typischen gelesenen Entitäten gehören Benutzer, Kontakte, Besitzerzuordnungen, Leads, Konten, Chancen und Aktivitäten. Writeback ist auf protokollierte Outreach-Aktivitäten und den Opt-out-Status beschränkt. Ihr CRM-Administrator bereitet den API-Zugriff in Salesforce oder Dynamics vor. Anschließend verbinden Sie den Verkaufsqualifizierer, ordnen eingehende Felder zu und wählen aus, ob Aktivitäten in der App synchronisiert werden sollen.

>[!NOTE]
>
>Die folgenden Schritte zur Anmeldung beschreiben den Lesezugriff auf CRM-Objekte. Wenn Sie Aktivitätssynchronisierung oder Opt-out-Writeback aktivieren, wenden Sie sich an Ihren CRM-Administrator, um ihm den entsprechenden für Ihre CRM-Konfiguration erforderlichen Schreibzugriff zu gewähren.

### Vorbereiten der Anmeldeinformationen in Ihrem CRM

Arbeiten Sie mit Ihrem CRM-Administrator zusammen, bevor Sie den Sales Qualifier verbinden. Im Folgenden wird zusammengefasst, was normalerweise in jedem System erstellt wird.

#### Microsoft Dynamics 365 (Dataverse/Power-Plattform)

1. Registrieren Sie in Azure Active Directory eine Anwendung (**[!UICONTROL App-Registrierungen]**).

   Notieren Sie sich **Client-ID** und **Mandanten-ID** und erstellen Sie ein **Client-Geheimnis**.

1. Öffnen Sie im **[!UICONTROL Power Platform Admin Center]** Ihre Umgebung und gehen Sie zu **[!UICONTROL Einstellungen]** > **[!UICONTROL Benutzer + Berechtigungen]** > **[!UICONTROL Anwendungsbenutzer]**.

1. Erstellen Sie einen Programmbenutzer, der mit dieser Azure AD-App verknüpft ist.

1. Weisen Sie eine Sicherheitsrolle zu, die **(**) Zugriff auf die Entitäten gewährt, die für den Sales Qualifier erforderlich sind, z. B. Leads, Kontakte, Konten, Chancen und Aktivitäten.

   Die App erfordert eine Sicherheitsrolle mit Lesezugriff auf Lesedaten.

**Informationen zum Verbinden von Dynamics:**

* Client-ID
* Client-Geheimnis
* Mandantenkennung
* Dynamics-Instanz-URL (Organisations-URL)

#### Salesforce

Erstellen Sie in Salesforce [eine externe Client](https://help.salesforce.com/s/articleView?id=xcloud.create_a_local_external_client_app.htm&type=5)App oder eine _verbundene App_) mit aktivierten OAuth-Bereichen, die API-Zugriff auf Identitäten und Daten ermöglichen und den Sicherheitsstandards Ihrer Organisation entsprechen. Der integrierende Benutzer muss Lesezugriff auf Objekte wie Leads, Konten, Kontakte, Aufgaben, Ereignisse und Chancen haben. Für administrative Aufgaben ist es oft erforderlich, dass Benutzende mit **[!UICONTROL Verbundene Apps verwalten]** (neben anderen Berechtigungen) nach der Erstellung einen Kundenschlüssel und ein Kundengeheimnis anzeigen.

>[!PREREQUISITES]
>
>Um eine externe Client-Anwendung zu erstellen, sollte ein Produktadministrator sicherstellen, dass Folgendes aktiviert ist (über Profil oder Berechtigungssatz):
>
>* Programm anpassen
>* Setup und Konfiguration anzeigen
>* Alle Daten ändern
>* Verbundene Apps verwalten (wichtig)
>
>   Wenn _Verbundene Apps verwalten_ nicht aktiviert ist, können Sie die Client-ID und das Client-Geheimnis nach dem Erstellen der externen Client-App nicht mehr anzeigen.

Wenn Sie die externe Client-App erstellen, aktivieren Sie OAuth und geben Sie Berechtigungen. Aktivieren Sie außerdem die folgenden Client-Anmeldeinformationen:

* Zugriff auf den Identity URL-Service (ID, Profil, E-Mail, Adresse, Telefon)
* Benutzerdaten über APIs verwalten (API)
* Zugriff auf eindeutige Benutzerkennung (openid)

Nachdem Sie die App erstellt haben, aktivieren Sie den Fluss der Client-Anmeldeinformationen erneut und verwenden Sie Kontakt-E-Mail als Benutzernamen.  Wenn die Client-Anmeldeinformationen aktiviert sind, konfigurieren Sie einen Benutzer für _Ausführen als_.

Stellen Sie sicher, dass der konfigurierte Benutzer Lesezugriff auf die folgenden Objekte hat:

* Leads
* Konten
* Kontakte
* Aufgaben
* Ereignisse
* Opportunity
* OpportunityContactRoles
* OpportunityLineItems

**Informationen, die beim Verbinden von Salesforce in Sales Qualifier bereitzustellen sind:**

* Client-ID (Verbraucherschlüssel)
* Client-Geheimnis (Consumer Secret)
* Callback-URL (wie in der verbundenen App konfiguriert)
* Salesforce-Instanz-URL

>[!IMPORTANT]
>
>Senden Sie keine Kundengeheimnisse per E-Mail. Verwenden Sie den genehmigten sicheren Kanal Ihres Unternehmens, um Anmeldeinformationen mit denjenigen zu teilen, die sie im Sales Qualifier eingeben.

### Verbindung zu Ihrem CRM herstellen

1. Melden Sie sich bei Sales Qualifier an und bestätigen Sie, dass die richtige Sandbox oder Umgebung ausgewählt ist.

1. Erweitern Sie in der linken Navigation **[!UICONTROL Administration]** und wählen Sie **[!UICONTROL Admin-Einstellungen]** aus.

1. Wählen Sie **[!UICONTROL CRM-Verbindungen]** unter **[!UICONTROL Integrationen]** aus.

   Auf der Seite werden Karten für Salesforce und Microsoft Dynamics angezeigt. Eine inaktive Verbindung wird angezeigt **[!UICONTROL Verbinden]**. Eine konfigurierte Verbindung zeigt **[!UICONTROL Verbunden]** und eine **[!UICONTROL Verwalten]**-Aktion an.

   ![Admin-Einstellungen CRM-Verbindungen mit Salesforce- und Dynamics-Verbindungskarten](./assets/integrations-crm-connections.png){width="800" zoomable="yes"}

1. Klicken Sie **[!UICONTROL das]** CRM-System auf „Verbinden“.

1. Geben Sie die Client-ID, Geheimnisse, Mandanten- oder Callback-Werte und **Instanz-URL** von Ihrem CRM-Administrator ein.

1. Bestätigen Sie nach erfolgreicher Verbindung, dass auf der Karte &quot;**[!UICONTROL &quot;]**.

### Richtlinien für Instanz-URLs

Die **Instanz-URL** muss die umgebungsbasierte URL sein, die Ihr CRM für die API- und Integrationskonfiguration verwendet - kein reiner Hostname, der nur die Benutzeroberfläche hat.

**Salesforce**

1. Melden Sie sich an und notieren Sie sich _Subdomain Ihrer Organisation_ Meine Domain) in der Adressleiste des Browsers (der `{{mydomain}}`).

1. Verwenden Sie für den Verkaufsqualifizierer die kanonische Form: `https://{{mydomain}}.my.salesforce.com` .

   Verwenden **nicht** eine `lightning.force.com` URL als Instanz-URL.

**Microsoft Dynamics 365**

1. Öffnen Sie Ihr CRM im Browser und kopieren Sie die Basis-URL aus der Adressleiste.

   Sie liegt normalerweise in der Form `https://{{org}}.crm.dynamics.com` vor.

### CRM-Felder zuordnen (eingehende Zuordnung)

Nachdem das CRM verbunden ist, wählen Sie **[!UICONTROL Verwalten]** für die Verbindung aus und öffnen Sie **[!UICONTROL Eingehende Zuordnung]**. Inbound mapping steuert, welche CRM-Felder der Sales Qualifier in das Programm einzieht.

1. Wählen Sie eine Objektgruppe aus: **[!UICONTROL Kontakt]**, **[!UICONTROL Interessent]** oder **[!UICONTROL Konto]**.
1. Wählen **[!UICONTROL Abschnitt hinzufügen]** und geben Sie einen Abschnittsnamen und eine optionale Beschreibung ein.
1. Fügen Sie die CRM-Felder zum Abschnitt hinzu.

   Jede Feldzeile zeigt ihren **[!UICONTROL Anzeigenamen]**, **[!UICONTROL Feldname]** und **[!UICONTROL Datentyp]** an.

1. Aktivieren **[!UICONTROL Filterbar]** für jedes Feld, das als Filter in der Liste **[!UICONTROL Interessenten“ verfügbar]** soll.
1. Zeigen Sie eine Vorschau der Zuordnung an und speichern Sie sie.

Zugeordnete Felder werden in den entsprechenden Bereichen des Verkaufsqualifizierers angezeigt:

* Die Felder Interessent und Kontakt werden auf der Registerkarte **[!UICONTROL Person]** für Interessenten angezeigt.
* Kontofelder werden in der Kontoansicht angezeigt.
* Opportunity-bezogene Felder werden in den Opportunity-Bereichen des Account-Erlebnisses angezeigt.

### Aktivitätssynchronisierung konfigurieren (ausgehende Zuordnung)

1. Wählen Sie **[!UICONTROL CRM-Verbindungen]** die Option **[!UICONTROL Verwalten]** für das verbundene CRM aus.
1. Öffnen Sie **[!UICONTROL Ausgehende Zuordnung]**.
1. Aktivieren Sie **[!UICONTROL Aktivitätssynchronisierung]** um die Outreach-Aktivitäten des Verkaufsqualifizierers wieder mit dem CRM zu synchronisieren.

Wenn die Aktivitätssynchronisierung deaktiviert ist, kann der Vertriebsqualifizierer weiterhin eingehende CRM-Daten verwenden, schreibt jedoch keine Outreach-Aktivitäten zurück in das CRM.

### Konfigurieren des globalen E-Mail-Opt-outs

1. Erweitern Sie in der linken Navigation **[!UICONTROL Administration]** und wählen Sie **[!UICONTROL Admin-Einstellungen]** aus.
1. Wählen Sie **[!UICONTROL E-Mail]** Einstellungen unter **[!UICONTROL Compliance]** aus.
1. Aktivieren Sie **[!UICONTROL Ausschluss-Link in jeder E-Mail einschließen]** um eine Fußzeile zur Abmeldung an ausgehende E-Mails anzuhängen.
1. Geben **[!UICONTROL in der Opt]** out-Nachrichtenvorlage den Fußzeilentext ein. Schließen Sie das `{{opt_out_link}}`-Token ein, in dem der anklickbare Abmelde-Link angezeigt werden soll.
1. Speichern Sie die Einstellungen.

Wenn ein Interessent den Link auswählt, unterdrückt der Verkaufsqualifizierer den Interessenten dauerhaft von weiteren E-Mails. Der Opt-out-Status synchronisiert sich auch wieder mit dem verbundenen CRM.

### Referenz: Beispiel-API-Parameter

Ihr CRM-Team kann diese Beispiele verwenden, um zu bestätigen, dass der Lesezugriff die erwarteten Lead-Felder zurückgibt.

**Dynamics (Auszug im OData-Stil)**

```text
$select=fullname,_ownerid_value,leadid,emailaddress1,jobtitle,statuscode,createdon,modifiedon,statecode
$filter=_ownerid_value eq '<crmUserId>' [AND additional filters]
$expand=Lead_ActivityPointers(...),parentaccountid(...)
$orderby=modifiedon desc
```

**Salesforce (SOQL-Auszug)**

```sql
SELECT Id, Salutation, FirstName, LastName, Name, Title, Company, Email,
  LeadSource, Status, OwnerId, LastModifiedDate, LastActivityDate, CreatedDate,
  (SELECT Id, Subject, ActivityDate, Status FROM Tasks ORDER BY ActivityDate DESC LIMIT 1),
  (SELECT Id, Subject, ActivityDateTime FROM Events ORDER BY ActivityDateTime DESC LIMIT 1)
FROM Lead
WHERE OwnerId = '<crmUserId>' AND IsDeleted = false
ORDER BY LastModifiedDate DESC
```

## Profileinstellungen

Die Profileinstellungen geben Informationen über sich selbst an, einschließlich persönlicher Daten, E-Mail, Kalender und Chat-Verfügbarkeit.

### E-Mail-Einstellungen

Richten Sie auf **[!UICONTROL Registerkarte]** E-Mail-Einstellungen“ Ihre E-Mail-Verbindungen ein.

![Registerkarte E-Mail-Einstellungen mit E-Mail-Verbindungsoptionen und E-Mail-Signaturkonfiguration](assets/email-settings.png)

* **[!UICONTROL E-Mail-]**: Klicken Sie auf **[!UICONTROL Verbinden]** und folgen Sie dem Anmeldeverfahren für Microsoft.

* **[!UICONTROL E-Mail-]**: Konfigurieren der E-Mail-Signatur, die in automatisch generierten E-Mails verwendet wird. Fügen Sie [&#x200B; Link &quot;](#meeting-booking)&quot; zur Signatur hinzu, damit potenzielle Kunden Zeit mit Ihnen planen können.

### Kalenderkonfiguration

Legen Sie auf **[!UICONTROL Registerkarte]** Kalenderkonfiguration“ Ihre Zeitzone und Verfügbarkeit fest.

<!-- 
![Calendar settings tab showing time zone and availability options](assets/calendar-settings.png)
-->

* **[!UICONTROL Kalenderverbindung]** - Klicken Sie auf **[!UICONTROL Verbinden]** und folgen Sie dem Anmeldeverfahren für Microsoft, um Ihren Kalender zu integrieren.

* **[!UICONTROL Besprechungsbestätigungs-E-Mail]** - Wenn ein Kunde ein Meeting mit Ihnen bestätigt, erhält er die Bestätigungs-E-Mail als Antwort. Verwenden Sie diese Einstellungen, um den Betreff und Text der E-Mail zu definieren.

* **[!UICONTROL Voreinstellungen]** - Legen Sie die standardmäßige Länge der Besprechung und die Zeit zwischen aufeinander folgenden Besprechungen fest.

Wenn Sie den Kalender trennen:

* Aktive Buchungs-Links sind effektiv deaktiviert.
* Die Buchungsseite zeigt einen freundlichen, vorübergehend nicht verfügbaren Status an.
* Beim erneuten Verbinden werden die Einstellungen beibehalten.

### Kalenderverfügbarkeit

Die Verfügbarkeit Ihres Kalenders in Sales Qualifier basiert auf zwei Eingaben:

* Ihr verbundener Arbeitskalender (Outlook oder Gmail)
* Ihre konfigurierte Verfügbarkeit + Zeitschlitzregeln in _Kalendereinstellungen_.

Der Verkaufskennzeichner liest den Frei/Belegt-Status aus dem verbundenen Kalender, nicht den vollständigen Ereignisinhalt, und verwendet diesen zusammen mit den konfigurierten Regeln, um zu entscheiden, welche Buchungs-Slots ein potenzieller Kunde sehen kann.

Sie können Folgendes konfigurieren:

* Arbeitszeit nach Wochentag
* Mehrere Blöcke pro Tag (Beispiel: 9:00-12:00 und 1:00-5:00)
* Ihre Zeitzone
* Meeting-Dauer
* Puffer vor/nach Besprechungen
* Mindestkündigungsfrist
* Buchungsfenster

<!-- 
### Chat settings

In the **[!UICONTROL Chat settings]** tab, set your Timezone Live chat availability.

![Chat settings tab for configuring timezone and live chat availability](assets/chat-settings.png)

## Representative management

The _[!UICONTROL Representative management]_ panel displays the defined representatives and their calendar status.

## Meeting performance

This panel presents analytics around your completed meetings.
-->

<!--
 SHPHR-24341 remove section
## Set up the Chrome plugin

The AI Assistant Chrome plugin is available on the [Google Store](https://chromewebstore.google.com/detail/ai-assistant/hancbabllcmckehonngbdkhilocpdfji?authuser=0&hl=en).

When the plugin is installed in Chrome, the Adobe logo appears on the middle right when you are on an integrated site:

* Adobe web applications
* Salesforce
* Outlook
* Microsoft Dynamics and web applications
* Google applications 
-->
