---
title: Chat-Oberfläche
description: Verwenden Sie das KI-Assistenten-Chat-Bedienfeld in Journey Optimizer B2B Prime, um Programme, Journey und Listen mit natürlicher Sprache oder dem Schrägstrich (/) zu erstellen.
badgeBeta: label="Beta" type="informative" tooltip="Diese Funktion befindet sich derzeit in einer eingeschränkten Beta-Version"
autotag-review: '2026-06-12T22:46:23.441Z'
TQID: 'https://experienceleague.adobe.com/XyBLmqv63kNBcw-Jo4hKvUKIn2la7kac7-kTbNEU5aE'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: bef5003b-cad2-4f40-bdb2-a80426d52ef5id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1fid: a30218bb-f80a-4410-8ac4-b039e99a15b4
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 29d33656b0bd05e9fdf2cbdeb1f6e89d13c3d20e
workflow-type: tm+mt
source-wordcount: 869
ht-degree: 1%

---

# Chat-Oberfläche

Das Chat-Panel ist in [!DNL Adobe Journey Optimizer B2B Prime] eingebettet. Hier können Sie mit den KI-Agenten interagieren, indem Sie sie in einfacher Sprache verwenden, um Programme und Journey zu erstellen, Personenlisten zu erstellen und zu vergleichen, Leads zu untersuchen, die Bewertung zu konfigurieren und vieles mehr.

Wählen Sie das Symbol _KI_ Assistent) im linken Navigationsbereich aus, um das Bedienfeld zu öffnen. Die Panel-Kopfzeile verfügt über vier Steuerelemente:

| Kontrollvariante | Beschreibung |
|---------|-------------|
| **Neue Konversation** | Neuen Chat starten (löscht den aktuellen Thread). |
| **Konversationsverlauf** | Öffnen Sie vergangene Unterhaltungen, damit Sie eines erneut öffnen können. |
| **Bedienfelder wechseln** | Verschieben Sie das Chat-Bedienfeld auf die andere Seite des Arbeitsbereichs. |
| **Reduzieren** | Blenden Sie das Bedienfeld aus, um dem Arbeitsbereich mehr Platz zu geben. |

Unten im Bedienfeld befindet sich das Meldungsfeld, in dem Sie Folgendes tun können:

* Fügen Sie eine Nachricht hinzu und drücken Sie **Eingabetaste** um zu senden (**Umschalt+Eingabetaste** fügt einen Zeilenumbruch ein).
* Hängen Sie eine Datei mithilfe des _Anhängen_-Symbols an (unterstützte Formate: `.txt`, `.md`, `.csv`, `.json`, `.xlsx`, `.docx`, `.pdf`). Verwenden Sie CSV- und Tabellen-Uploads, um einen Lead-Import zu starten.

## KI-Assistenten stellen

Es gibt zwei gleichermaßen gültige Arten Arbeit zu erledigen. Man muss nie das Schrägstrich-Menü benutzen.

**Natürliche Sprache** - Geben Sie Ihre Anfrage so ein, wie Sie sie einem Kollegen sagen würden:

* _„Erstellen Sie eine Begrüßungs-Journey für neue Testanmeldungen._
* _„Warum ist john@acme.com nicht auf diese Journey gekommen?“_
* _„Vergleichen Sie die Listen meiner Webinar-Teilnehmer im 3. Quartal mit den Listen der Unternehmenskonten.“_

Der Agent ordnet Ihre Formulierungen hinter den Kulissen den richtigen Kenntnissen zu und führt den entsprechenden Workflow aus.

**Das Menü mit Schrägstrich (/)** — Geben Sie `/` ein, um ein durchsuchbares Menü mit allem zu öffnen, was der Assistent tun kann. Dies ist nützlich, wenn Sie Funktionen entdecken oder direkt zu einem bekannten Workflow springen möchten.

## Der Schrägstrich (/) im Menü

Verwenden Sie eine `/` am Anfang des Meldungsfelds oder nach einem Leerzeichen, um das Menü zu öffnen. Während Sie mit der Eingabe fortfahren, filtert die Liste nach Name, Beschreibung oder ID - zum Beispiel wird `/journey` auf Journey-bezogene Befehle eingegrenzt.

Verwenden Sie **/**, um durch Einträge zu navigieren **(** oder **Tabulator** auszuwählen und **Esc**, um sie zu schließen. Sie können auch direkt auf einen Eintrag klicken.

Menüeinträge sind in beschriftete Abschnitte unterteilt:

| Abschnitt | Enthält |
|---------|----------|
| **untersuchen** | Diagnostische, schreibgeschützte Suchen (z. B. Lead-Ermittlung, Absichtsabfragen). |
| **Validieren** | QA- und Audit-Workflows |
| **Build** | Erstellungs-Workflows (Programme, Journey, Listen, Bewertung). |
| **Importieren** | CSV-Leadimport. |
| **Sonstige** | Alles, was nicht in die oben genannten Kategorien fällt. |

Im Menü werden auch **Connectoren** (z. B. _Marketo durchsuchen_ und ein Auswahldialogfeld geöffnet) und **Navigationskürzel** aufgeführt, die zu einem Arbeitsbereichsbildschirm springen.

### Menüelement auswählen

Wenn Sie eine Qualifikation oder einen Agenten aus dem Menü auswählen, wird eine Starteraufforderung in das Meldungsfeld eingefügt, die Sie bearbeiten können - sie wird **automatisch**. Wenn Sie beispielsweise _Kampagnen planen_ in &quot;_&quot; auswählen, wird ein neues Marketo-Programm für [Kampagnenname“ ]. Ich lade die Zusammenfassung hoch.“_ Füllen Sie die Platzhalter in Klammern aus und drücken Sie **Eingabetaste** um zu senden.

Connectoren öffnen ein modales Fenster, anstatt Text einzufügen. Über Navigationsbefehle gelangen Sie direkt zu diesem Bildschirm im Arbeitsbereich.

>[!NOTE]
>
>Einige Befehle werden ausgegraut angezeigt und als _In Kürze verfügbar_ gekennzeichnet. Diese werden durch Feature Flags eingegrenzt und sind noch nicht für Ihr Konto aktiv. Die Auswahl eines Flags bewirkt nichts. Welche Funktionen verfügbar sind, hängt davon ab, welche für Sie aktiviert sind.

## Kenntnisse

Eine Qualifikation ist ein gepackter Workflow, den der Agent ausführen kann - die Bausteine hinter dem `/` und den Anforderungen in natürlicher Sprache. Jede Qualifikation umfasst schrittweise Anweisungen und die spezifischen Tools, die für einen Auftrag erforderlich sind (z. B. „Veröffentlichen eines Journey&quot;, „Vergleichen von zwei Personenlisten“, „Erstellen eines Bewertungsmodells„).

Wichtige Informationen zu Kenntnissen über Fähigkeiten:

* **Kenntnisse beziehen sich auf das Produkt.** In AJO B2B Prime sehen Sie AJO B2B-Kenntnisse (Journey, Personenlisten, Punktzahl, Kanäle, Sendezeitoptimierung usw.). Einige wenige Kenntnisse sind nur Marketo und ein paar arbeiten in beiden Produkten (Leadimport, Produktwissen). Sie sehen nur Fähigkeiten, die für Ihren aktuellen Standort relevant sind.
* **Sie müssen sich die Namen von Kenntnissen nicht merken.** Beschreiben Sie Ihr Ziel, und der Agent wählt die passende Qualifikation aus. Das `/` ist eine schnellere, auffindbare Verknüpfung zu denselben Workflows.
* **Manche Fähigkeiten lesen nur; andere ändern Dinge.** Investigative Fähigkeiten und Berichtsfähigkeiten (z. B. Lead-Ermittlung, Absichtsabfrage, Sendezeitbericht) lesen nur Daten. Erstellen und konfigurieren Sie Fertigkeiten (z. B. Journey-Erstellung, Bewertung), um Daten zu erstellen oder zu ändern.

## Folgenachrichten

Nachdem der Assistent geantwortet hat, wird oft eine Reihe klickbarer Nachfragen angezeigt, die auf das zugeschnitten sind, was Sie gerade getan haben. So könnte er beispielsweise nach dem Erstellen einer Journey _„Diese Journey veröffentlichen“_ oder _„Warteschritt hinzufügen“_. Klicken Sie auf eins, um ohne Eingabe fortzufahren. Hierbei handelt es sich lediglich um Vorschläge. Stattdessen können Sie auch Ihre eigene nächste Nachricht eingeben.

## Tipps

* **Verwenden Sie Kennungen.** Geben Sie bei der Untersuchung oder Bearbeitung die E-Mail-Adresse, den Personennamen, den Journey-Namen oder den Listennamen an, damit der Agent das richtige Asset bearbeiten kann.
* **Verwenden Sie `/` zum Erkunden.** Wenn Sie sich nicht sicher sind, was der Assistent tun kann, öffnen Sie das Menü `/` und überspringen Sie die Kategorien.
* **Bearbeiten Sie die Starteraufforderung.** Durch Auswahl einer Qualifikation erhalten Sie eine Vorlage - ersetzen Sie die `[bracketed]` Platzhalter vor dem Versand.
* **Zuerst für Importe hochladen.** Für einen Lead-Import fügen Sie zuerst die CSV-Datei hinzu und beschreiben Sie dann, was Sie damit tun möchten.
* **Beginnen Sie eine neue Konversation** wenn Sie zu einer nicht verwandten Aufgabe wechseln, sodass sich ein früherer Kontext nicht auf die neue Anfrage auswirkt.
