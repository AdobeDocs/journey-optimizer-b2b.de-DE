---
title: KI-Assistenzqualifikationen
description: Überprüfen der KI-Assistentenfähigkeiten in Journey Optimizer B2B Prime - gebündelte Workflows für Programme, Journey, Zielgruppen, Bewertung, Inhalte und Sendezeitoptimierung.
badgeBeta: label="Beta" type="informative" tooltip="Diese Funktion befindet sich derzeit in einer eingeschränkten Beta-Version"
autotag-review: '2026-06-24T23:55:36.649Z'
TQID: 'https://experienceleague.adobe.com/iIi07OBWKxxa-oW-A6VrlkoTS02kmCx8kfMaCe-C-4o'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: bef5003b-cad2-4f40-bdb2-a80426d52ef5
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: ff10f619-348f-47e3-99bf-3ce4c817cf2c
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: d8f352c636ebd8980614922099701de8f755e8e4
workflow-type: tm+mt
source-wordcount: 582
ht-degree: 7%

---

# KI-Assistenzqualifikationen

Eine _Qualifikation_ ist ein gepackter Workflow, den der Agent ausführen kann - die Bausteine hinter dem `/` und den Anfragen in natürlicher Sprache. Jede Qualifikation umfasst schrittweise Anweisungen und die spezifischen Tools, die für einen Auftrag erforderlich sind (z. B. „Veröffentlichen eines Journey&quot;, „Vergleichen von zwei Personenlisten“, „Erstellen eines Bewertungsmodells„).

>[!NOTE]
>
>Jede Qualifikation wird danach klassifiziert, ob die Qualifikation den [!DNL Journey Optimizer B2B Prime]- oder [!DNL Marketo Engage] mutiert (**Write**), nur Abfragen/Analysen/Generierungen (**Read**) oder gleichrangige Abfrage- und Mutationsfunktionen aufweist (**Read+Write**).

## Programme und Planung {#programs-planning}

| SKILL | Funktion | Zugriff | Produktoberfläche | Auswirkungen/Datenfluss |
|---|---|---|---|---|
| `falco-program-creation` | End-to-End [!DNL Journey Optimizer B2B Prime] Programmerstellung - Programm, Unterordner, Token, Listen, Journey. | Schreiben | [!DNL Journey Optimizer B2B Prime] | [!DNL Journey Optimizer B2B Prime] mit Lese- und Schreibzugriff. Siehe _[Erstellen eines Programms aus einer](./program-from-brief.md)_. |
| `adapt-program` | Generieren Sie Migrationsgeschichten aus [!DNL Marketo Engage] Programmen zur [!DNL Journey Optimizer B2B Prime]. | Lesen | [!DNL Journey Optimizer B2B Prime] | Liest [!DNL Marketo Engage], schreibt [!DNL Journey Optimizer B2B Prime] |
| `folder-creation` | Erstellen Sie Organisationsordner in der Asset-Baumstruktur. | Schreiben | [!DNL Journey Optimizer B2B Prime] | Lese- und Schreibvorgänge [!DNL Journey Optimizer B2B Prime] |
| `program-creation` *(Erstellen von Programmen)* | Erstellen von Marketo-Programmen aus einer Kampagnenbeschreibung. | Schreiben | [!DNL Marketo Engage] | Lese- und Schreibvorgänge [!DNL Marketo Engage] |
| `program-planning` *(Kampagnen planen)* | Umwandeln von Briefs in Einrichtungs-/Implementierungsdokumente. | Lesen | [!DNL Marketo Engage] | Liest [!DNL Marketo Engage] |
| `program-qa` *(Programme validieren)* | Programme validieren/überprüfen (nur Regeln, Testplan oder Kurzbeschreibung). | Lesen | [!DNL Marketo Engage] | Liest [!DNL Marketo Engage] |

## Journeys {#journeys}

| SKILL | Funktion | Zugriff | Produkt | Backend (Datenfluss) |
|---|---|---|---|---|
| `journey-creation` | Erstellen und bearbeiten Sie Journey aus natürlicher Sprache. | Schreiben | [!DNL Journey Optimizer B2B Prime] | Lese- und Schreibvorgänge [!DNL Journey Optimizer B2B Prime] |
| `journey-edit-dates` | Ändern des Start-/Enddatums einer Journey ohne Veröffentlichung. | Schreiben | [!DNL Journey Optimizer B2B Prime] | Lese- und Schreibvorgänge [!DNL Journey Optimizer B2B Prime] |
| `journey-publish` | Personen-Journey veröffentlichen/starten/planen. | Schreiben | [!DNL Journey Optimizer B2B Prime] | Lese- und Schreibvorgänge [!DNL Journey Optimizer B2B Prime] |
| `journey-stop` | Abbrechen, schließen, stoppen, stoppen oder Journey töten. | Schreiben | [!DNL Journey Optimizer B2B Prime] | Lese- und Schreibvorgänge [!DNL Journey Optimizer B2B Prime] |
| `journey-reentry` | Erneuten Eintrag konfigurieren: Zulassen/Verweigern, Abklingzeit, Max. Einträge. | Schreiben | [!DNL Journey Optimizer B2B Prime] | Lese- und Schreibvorgänge [!DNL Journey Optimizer B2B Prime] |
| `journey-trafficcontrol` | Führen Sie eine Traffic-Steuerungssimulation aus, die das Profil-Routing anzeigt. | Lesen | [!DNL Journey Optimizer B2B Prime] | Liest [!DNL Journey Optimizer B2B Prime] (Simulation) |
| `journey-observability` | Debug/Überwachung des Fortschritts - Pfade, Timing, Aufspaltungen, Verzögerungen, Verweildauer. | Lesen | [!DNL Journey Optimizer B2B Prime] | Liest [!DNL Journey Optimizer B2B Prime] + [!DNL Marketo Engage] (statische Listenüberprüfung) |

## Zielgruppen und Personen {#audiences-people}

| SKILL | Funktion | Zugriff | Produkt | Backend (Datenfluss) |
|---|---|---|---|---|
| `audience-creation` | Passen Sie eine [!DNL Marketo Engage] SmartList an, erstellen Sie eine Personenliste oder fügen Sie Regeln hinzu bzw. aktualisieren Sie sie. | Schreiben | [!DNL Journey Optimizer B2B Prime] | Liest [!DNL Marketo Engage] + liest/schreibt [!DNL Journey Optimizer B2B Prime].  Siehe _[Erstellen von Zielgruppen für Programme](./audience-creation.md)_. |
| `people-list-comparison` | Vergleichen Sie zwei Personenlisten und zeigen Sie sich überschneidende Elemente an. | Lesen | [!DNL Journey Optimizer B2B Prime] | Liest [!DNL Journey Optimizer B2B Prime] |
| `import-leads` | Überprüfen Sie die CSV-Datenqualität und übertragen Sie Importe auf [!DNL Marketo Engage]. | Lese- und Schreibzugriff | Beide | Lese- und Schreibvorgänge [!DNL Marketo Engage] |
| `lead-investigation` *(Leads untersuchen)* | Untersuchen der Aktivität, Bewertung, Qualifizierung und des Lebenszyklus eines Leads. | Lesen | [!DNL Marketo Engage] | Liest [!DNL Marketo Engage] |

## Inhalt und Kanäle {#content-channels}

| SKILL | Funktion | Zugriff | Produkt | Backend (Datenfluss) |
|---|---|---|---|---|
| `content-personalization` | Vorlagen durchsuchen/in der Vorschau anzeigen und Inhalte bearbeiten/Varianten erzeugen. | Lese- und Schreibzugriff | [!DNL Journey Optimizer B2B Prime] | Lese- und Schreibvorgänge [!DNL Journey Optimizer B2B Prime] |
| `asset-tokens` | Vollständiges CRUD-Token für Programme/Ordner/Journey. | Lese- und Schreibzugriff | [!DNL Journey Optimizer B2B Prime] | Lese- und Schreibvorgänge [!DNL Journey Optimizer B2B Prime] |
| `fcs-channels` | Kanalsuchen und CRUD + Publish/Stopp/Delete. | Lese- und Schreibzugriff | [!DNL Journey Optimizer B2B Prime] | Lese- und Schreibvorgänge [!DNL Journey Optimizer B2B Prime] |

## Scoring und Signale {#scoring-signals}

| SKILL | Funktion | Zugriff | Produkt | Backend (Datenfluss) |
|---|---|---|---|---|
| `scoring-studio` | Bewertungsmodelle auflisten/abrufen und erstellen/veröffentlichen. | Lese- und Schreibzugriff | [!DNL Journey Optimizer B2B Prime] | Liest und schreibt [!DNL Journey Optimizer B2B Prime] (Scoring-Service); liest [!DNL Marketo Engage] Lead-Felder/Aktivitätstypen. Siehe _[Erstellen benutzerdefinierter Bewertungsmodelle](./lead-scoring-model.md)_. |
| `engagementconfiguration` | Interaktionskonfiguration anzeigen und Gewichtungen bearbeiten/aktualisieren. | Lese- und Schreibzugriff | [!DNL Journey Optimizer B2B Prime] | Lese- und Schreibvorgänge [!DNL Journey Optimizer B2B Prime] |
| `intentconfiguration` | Absichtskonfiguration anzeigen und Gewichtung festlegen/aktualisieren. | Lese- und Schreibzugriff | [!DNL Journey Optimizer B2B Prime] | Lese- und Schreibvorgänge [!DNL Journey Optimizer B2B Prime] |
| `intent-query` | Abfrage und Erläuterung der Absichtsergebnisse nach Person/Segment/Liste. | Lesen | [!DNL Journey Optimizer B2B Prime] | Liest [!DNL Journey Optimizer B2B Prime] |

## Versandzeitoptimierung {#sto}

| SKILL | Funktion | Zugriff | Produkt | Backend (Datenfluss) |
|---|---|---|---|---|
| `send-time-optimization` | Überprüfen Sie den STO-Status und aktivieren/deaktivieren Sie ihn auf einem E-Mail-Knoten. | Lese- und Schreibzugriff | [!DNL Journey Optimizer B2B Prime] | Lese- und Schreibvorgänge [!DNL Journey Optimizer B2B Prime] |
| `send-time-report` | Abrufen/Anzeigen des STO-Leistungsberichts. | Lesen | [!DNL Journey Optimizer B2B Prime] | Liest [!DNL Journey Optimizer B2B Prime] |

## Kenntnisse {#knowledge}

| SKILL | Funktion | Zugriff | Produkt | Backend (Datenfluss) |
|---|---|---|---|---|
| `product-knowledge` | Beantworten Sie Anleitungen/Konzeptfragen in [!DNL Journey Optimizer B2B Prime] Dokumentation zu Experience League. | Lesen | Beide | Liest externe Dokumente - keine Produktdaten |

## Cross-Backend {#cross-backend}

Diese Fähigkeiten umfassen mehr als ein Backend:

- **`adapt-program`** — `gather_program_assets` liest [!DNL Marketo Engage] (`get_program`, `get_smart_campaign`, `list_emails`) und schreibt dann über `falcomcp_create_journey` — klassisches Backend.
- **`audience-creation`** - liest [!DNL Marketo Engage] Smart Lists (`get_smart_list`/`get_smart_campaign`) und schreibt dann [!DNL Journey Optimizer B2B Prime] Personenlisten.
- **`journey-observability`** - [!DNL Journey Optimizer B2B Prime] Lesevorgänge und ein `check_lead_in_marketo_static_list` [!DNL Marketo Engage].
- **`scoring-studio`** - liest [!DNL Marketo Engage] Lead-Felder/Aktivitätstypen zusammen mit [!DNL Journey Optimizer B2B Prime] Scoring-Service.

Alle `falco-mcp_*`- und Journey/Token/Scoring/STO/FCS-Tools treffen auf [!DNL Journey Optimizer B2B Prime] Services; CSV/Programm/Lead-Tools auf [!DNL Marketo Engage].
