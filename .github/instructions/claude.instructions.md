---
applyTo: "**/*.md"
source-git-commit: d36cfd513df3d363a7bd74b5e09b774426e50b9b
workflow-type: tm+mt
source-wordcount: '5166'
ht-degree: 1%
---

# Adobe Experience League-Dokumentation: Claude Code-Anweisungen

Sie unterstützen einen technischen Autor im Adobe Experience League Public Documentation Repo (`journey-optimizer-b2b.en`). Jedes Inhaltselement, das Sie entwerfen, bearbeiten oder überprüfen, MUSS allen unten stehenden Regeln entsprechen. Wenn Sie bezüglich der Terminologie Zweifel haben, sehen Sie sich die referenzierten Wikis mit dem Confluence MCP-Tool (`mcp__adobe-wiki-confluence`) an.

&#x200B;---

## &#x200B;1. Stimme, Ton und Stil

### Benutzerfokussiertes Schreiben

Zentrieren Sie den Benutzer, nicht die Funktion. Schreiben Sie, was der Benutzer tun **&#x200B;**, nicht, was die Funktion tut.

- Verwenden Sie die zweite Person („Sie„) und die imperative Stimmung für Anweisungen.
- Verwenden Sie „Sie“, wenn Sie mit der Zielgruppe über sich selbst sprechen, nicht über „Benutzer“. „Benutzer“ ist akzeptabel, wenn auf eine Rolle verwiesen wird (z. B. ein Administrator oder eine Administratorin, der oder die Benutzer verwaltet).
- VERMEIDEN Sie „Feature X ermöglicht es Ihnen,…“ oder „Feature X ermöglicht es Ihnen,…“. Benutzende als Subjekt verwenden oder Imperative Stimmung verwenden.
  - Schlecht: „Die Server-API kann auf Servern verwendet werden.“
  - Gut: „Verwenden Sie die Server-API auf Servern.“
  - Schlecht: „Berechnete Felder ermöglichen die Erstellung von Werten…“
  - Gut: „Verwenden Sie berechnete Felder, um Werte zu erstellen…“
- Achten Sie auf das „Sie können.“ Es ist angebracht, kann aber übermäßig verwendet werden, wodurch sich wiederholende oder wortgewaltige Sätze entstehen.
- Verwenden Sie „Auswählen“, um Optionen aus einer Liste auszuwählen oder Text hervorzuheben. „Klick“ nur für explizite Mausaktionen verwenden. Vermeiden Sie die Benennung des Steuerelementtyps (Schaltfläche, Link), es sei denn, dies ist für die Eindeutigkeit erforderlich.
- Verwenden Sie „Öffnen“ / „Schließen“ für Anwendungen und große Fenster oder Bedienfelder.
- Verwenden Sie „Leave“, um eine Site oder ein Erlebnis zu verlassen (z. B. „Leave Report Builder„).
- Verwenden Sie für die Navigation „Gehe zu“ oder „Navigieren zu“.
- Verwenden Sie „Video abspielen“, nicht „Video ansehen“. Nicht alle sehen zu.
- Verwenden Sie „Anzeigen“, „Anzeigen“ oder „Zu allen wechseln“, nicht „Alle anzeigen“. Nicht jeder sieht es.
- Verwenden Sie „Anmelden“ / „Abmelden“, nicht „Anmelden“ / „Abmelden“.
- Vermeiden Sie „um zu helfen“. Verwenden Sie stattdessen „to“.
- Vermeiden Sie „Utilize“. Verwenden Sie stattdessen „Verwenden“.
- Vermeide vage Adjektive wie „schnell“ oder „einfach“. Genauer gesagt: „Dieser Vorgang dauert in der Regel 5 Minuten.“
- Schwache Adverbien vermeiden: sehr, extrem, unglaublich.

### Satz- und Absatzstruktur

- Ziel ≤20 Wörter pro Satz (Authoring-Handbuch sagt ≤35 max). Einen Gedanken pro Satz.
- Absätze: max. 125 Wörter, idealerweise ≤100. Maximal 4 bis 5 Sätze. Keine Mauern aus Text.
- Aktiv-Formulierungen verwenden. Vermeiden Sie passive Konstruktionen und Nominalisierungen (verwenden Sie z. B. „create“ und nicht „creation„).
- Verwenden Sie eine einfache Objekt-Verb-Objekt-Struktur.
- Vermeiden Sie falsche Motive („Es ist…“, „Es gibt…„).
- Verwenden Sie dasselbe Wort konsistent. Keine Synonyme drehen.
- Kein Humor, kein Slang, kein Jargon und keine kulturspezifischen Beispiele (müssen gut lokalisiert werden).
- Verwenden Sie das Komma „Oxford“ in Listen mit drei oder mehr Elementen.
- Schreiben Sie ganze Zahlen von null bis neun aus; verwenden Sie Ziffern für 10 und darüber.
- Keine Semikolons. Stattdessen einen Punkt und einen neuen Satz verwenden.

### Scannbarkeit

- Leser sollten den Artikelbereich nur anhand von Titel, Überschriften und Beschriftungen erfassen.
- Max. 2 bis 5 Unterabschnitte pro Abschnitt.
- Target 7 Schritte pro Aufgabe; 10 ist das praktische Maximum. Unterteilen Sie längere Vorgänge in Teilaufgaben.
- Max. 8 Elemente pro Aufzählungsliste.
- Verwenden Sie Tabellen, wenn sie die Überprüfung von Begriffsdefinitionslisten erleichtern.
- Der Inhalt sollte bei einem Lesbarkeitstest (nach dem Entfernen von Eigennamen und Titeln) unter Stufe 10 liegen.

### Schreiben für KI-Erkennung

KI-Assistenten und Suchwerkzeuge tauchen zunehmend in generierten Antworten auf Experience League-Inhalte auf.

- Legen Sie Schlüsselbegriffe (Produktnamen, Funktionsnamen, Aufgaben) in Textkörper- und Link-Text fest, nicht nur in Bildern oder komplexen Tabellen. KI-Systeme basieren auf lesbarem Text.
- Schreiben Sie klare, in sich abgeschlossene Überschriften und erste Absätze. KI-Werkzeuge extrahieren diese häufig isoliert; sie müssen ohne den sie umgebenden Kontext sinnvoll sein.
- Halten Sie Sätze kurz und direkt. Präzise Prosa ist für KI einfacher zu parsen und genau zu zitieren.
- Verwenden Sie strukturierte Formate (nummerierte Schritte, kurze Aufzählungszeichen, Überschriften im Definitionsstil) für Verfahren und Vergleiche. Die Struktur der KI hilft, die richtige Antwort zu finden.
- Schließen Sie bei der ersten Verwendung Synonyme oder alternative Begriffe (z. B. „ECID (Experience Cloud ID)„) ein, um den Abruf für verschiedene Abfrageausdrücke zu verbessern.
- Stellen Sie sicher, dass Metadatenfelder (Titel, Beschreibung, Feature Tags) vollständig und korrekt sind.

&#x200B;---

## &#x200B;2. Markdown-Syntax in Adobe (Experience League)

### Frontmatter (für jede Datei erforderlich)

```yaml
---
title: Title Case Title Here
description: Learn how to... or Learn about... (150-160 chars, sentence case).
---
```

Zusätzliche optionale Felder, die in diesem Repository verwendet werden: `solution`, `type`, `role`, `exl-id`. Übereinstimmung mit dem Muster vorhandener Dateien.

**WICHTIG:** Fügen Sie beim Erstellen einer neuen Seite KEINE `exl-id` hinzu. Er wird zum Zeitpunkt der Veröffentlichung automatisch generiert. Nur `exl-id` Felder, die bereits auf bestehenden Seiten vorhanden sind, sollten beibehalten werden.

**Titel-Metadatenregeln:**

- Title Case (nur in Experience League platzieren, die Title Case verwenden).
- Maximal 60 Zeichen (Englisch). Das System hängt `| Adobe Experience Platform` automatisch an. Berücksichtigen Sie dies als Länge.
- Fügen Sie KEINEN Pipe- oder Produktnamen hinzu. Sie wird automatisch hinzugefügt.
- Stellen Sie sich diese als SEO-Version Ihres Seitennamens vor (wonach Benutzer suchen).
- Konzeptname: Substantivsatz (z. B. „Seitenansichtsbericht„).
- Aufgabentitel: Verbphrase (z. B. „Erstellen eines Segments für Seitenansichten„).
- Akronyme werden von Marketing für die meisten Verwendungszwecke nicht genehmigt, aber eine begrenzte Verwendung ist für SEO-, Inhaltsverzeichniseinträge, Beschreibungsmetadaten und Überschriften akzeptabel, bei denen die Länge ein Problem darstellt.

**Beschreibung der Metadatenregeln:**

- Urteilsfall. Idealerweise 150 bis 160 Zeichen, max. 160 Zeichen.
- Ein bis zwei kurze Sätze. Der erste Satz fasst zusammen, der zweite ist ein call to action.
- Beginnen Sie die Konzeptbeschreibungen mit „Mehr erfahren über…“ oder „Verstehen…“.
- Beginnen Sie die Aufgabenbeschreibungen mit „Erfahren Sie, wie Sie…“ Oder ein Verbum des Imperativs.
- Beginnen Sie NICHT mit dem Produktnamen. Beginnen Sie mit einem Verb für SEO.
- Kopieren Sie NICHT den ersten Absatz wörtlich (anderer Zweck).
- Wenn ein Metadatenfeld mit einem `[!DNL]`- oder &grave;&grave;-Tag beginnt, setzen Sie den gesamten Feldwert in Anführungszeichen oder die Validierung schlägt fehl.

### Überschriften

- `#` = H1 (Artikeltitel, einer pro Seite). `##` = H2-Hauptabschnitte. `###` = H3, usw.
- Überschriftenebenen NICHT überspringen (z. B. nicht von H2 nach H4 springen).
- Ziel ≤5 Wörter. Maximal 69 Zeichen (Englisch).
- Leerzeile vor UND nach jeder Überschrift.
- Auf jede Überschrift muss mindestens ein Satz des Haupttextteils folgen. Stapeln Sie NIEMALS zwei Überschriften oder platzieren Sie eine Anmerkung, Liste oder Tabelle direkt unter einer Überschrift, ohne zuerst einen Absatz einzufügen.
- Benutzerdefinierte Anker-IDs: `## Section title {#section-id}` (Kleinbuchstaben, mit Bindestrich, keine Punkte).
- Vermeiden Sie Ankernamen, die mit JavaScript/CSS in Konflikt stehen: Suche, Ergebnisse, Inhalt, Kopfzeile, Fußzeile, Navigation, Seitenleiste, Paginierung usw.
- Platzieren Sie KEINE Abzeichen oder Markdown-Elemente innerhalb des Überschriftentextes.
- Verwenden Sie KEINE einzelnen abstrakten Wörter wie „Überblick“ oder „Einführung“ allein. Beschreiben Sie immer, worum es in der Übersicht oder Einführung geht.
- H1s NICHT nummerieren. Verwenden Sie für -Tutorials „Schritt 1: …“ in Unterüberschriften statt nummerierten Ankern.
- Groß-/Kleinschreibung für alle Überschriften (Eigennamen und Benutzeroberflächenelemente ausgenommen).
- Konzeptüberschriften: Substantive und Substantivsätze (z. B. „Überblick über die Segmentierung„).
- Aufgabenüberschriften: Imperative Verben (z. B. „Zielgruppen-Workflow erstellen„). Vermeiden Sie Gerundien (-ing-Formulare).
- Vermeiden Sie es, Verben mit -ment oder -ion zu vereinheitlichen (verwenden Sie „Erstellen einer Roadmap“ und nicht „Erstellung einer Roadmap„).
- Überschriftenstruktur in Abschnitten parallel halten.
- Keine doppelten Anker-IDs für Überschriften in einem Dokument.
- Wenn eine Überschrift Ziffern enthält, geben Sie eine explizite Überschriften-ID an, die nicht mit einer Zahl beginnt (z. B. `## Release notes for 2016 {#release-notes-2016}`).

### Links

- Interne Querverweise: Stamm-relative Pfade, die mit `/help/` beginnen: `[link text](/help/path/to/file.md)`
- Deep-Links zu Ankern: `[text](/help/path/to/file.md#anchor-id)`
- Externe Links (außerhalb dieses Repositorys): absolute `https://`-URLs. Diese werden automatisch in einer neuen Registerkarte geöffnet.
- Explizit in neuer Registerkarte öffnen: `{target="_blank"}` anhängen (für Querleitungs-Links verwenden).
- Referenzlinks (im `[1]: url` Stil): funktionieren nur mit absoluten URLs.
- Fügen Sie dieselbe Datei NICHT mehrmals in einem Inhaltsverzeichnis hinzu.
- Vermeiden Sie rohe URLs im Textkörper. Verwenden Sie immer beschreibenden Link-Text.
- Verwenden Sie niemals „hier klicken“ oder „Link“ als Link-Text. Die Sprachausgabe zeigt Links außerhalb des Kontexts an und kann mehrere „Hier klicken“-Instanzen nicht unterscheiden.
- Der Link-Text muss das Ziel für sich klar machen.
- Für „Weitere Informationen“-Querverweislisten verwenden Sie eine `More help on this topic` Unterüberschrift mit einer Aufzählungsliste.

### Bilder

- Syntax: `![alt text](path/to/image.png)`
- Größe ändern: `{width="300"}` oder `{width="50%"}`
- Ausrichten: `{align="center"}` oder `{align="right"}`
- Zoombar: `{zoomable="yes"}`
- Modale Anzeige: `{modal="regular"}`. Nicht mit einem Link kombinieren.
- Empfohlene Breite: 640 bis 2000 px. Maximale Dateigröße: 5 MB empfohlen; 100 MB Hard-Limit. Max. 100 Bilder pro Artikel.
- Bilder werden in einen `assets/` Unterordner relativ zur Markdown-Datei verschoben.
- Bilder, die NICHT lokalisiert werden dürfen, werden in einen `do-not-localize/` Unterordner verschoben.
- Erfassen Sie Screenshots immer mit dem **Light**-Design in der Experience Cloud-Produktoberfläche, nicht mit dem Dunklen Design.
- Zeigen Sie KEINE Kundendaten in Screenshots an.
- Dokumentieren Sie KEINE Schnittstellen von Drittanbietern in Screenshots. Stattdessen einen Link zur eigenen Dokumentation des Drittanbieters.
- Verwenden Sie KEINE Screenshots, nur um den Fortschritt durch Bildschirme zu verfolgen oder offensichtliche UI-Elemente anzuzeigen.
- Illustrationen von leicht identifizierbaren Symbolen nicht öfter als einmal pro Artikel enthalten.
- Verwenden Sie KEINE Bilder von Code. Verwenden Sie stattdessen Codeblöcke.
- Verwenden Sie KEINE Farbe allein, um Informationen zu vermitteln (für farbenblinde Benutzer nicht zugänglich).
- Verwenden Sie KEINE animierten Grafiken, die mehr als dreimal pro Sekunde blinken (Anfallsrisiko).
- Stellen Sie sicher, dass die Bilder einen guten Kontrast haben und klar sind.
- Richtlinien für die Größe von Screenshot-Pixeln: max. 2.000 Pixel für große, 672 Pixel für mittlere, 300 Pixel für kleine und 30-35 Pixel für Symbole.
- Für Beschriftungen: Verwenden Sie rote HEX-#EB1000, Linienstärke 3 Pixel, Eckenradius 8 Pixel.

### Alternativtext

Alternativtext wird von Google indiziert und von Sprachausgaben gelesen. Schreibe es immer vorsichtig.

- Beschreiben Sie, was das Bild zeigt, nicht nur den Namen des Bildschirms.
- Vollständige Sätze mit korrekter Grammatik und Interpunktion verwenden.
- Binden Sie relevanten Text aus dem Bild ein.
- Verwenden Sie vollständige Wörter, keine Abkürzungen. Bildschirmlesehilfen schreiben Abkürzungen aus.
- Nicht mit „Dieses Bild zeigt…“ beginnen. Beschreiben Sie den Inhalt einfach direkt.
- Alt-Text wird normalerweise nicht für rein dekorative Bilder benötigt, sondern im Zweifelsfall bereitgestellt.

| Guter Alternativtext | vermeiden |
|---|---|
| Screenshot des Audience Builders mit ausgewählten geografischen und altersbezogenen demografischen Filtern. | Audience Builder |
| Wählen Sie eine Erweiterung im Erweiterungskatalog aus. | Erweiterungsbibliothek |

### Videos

- Syntax: `>[!VIDEO](https://video.tv.adobe.com/v/xxxxx/?quality=12&learn=on)`
- Fügen Sie am Ende aller Video-URLs `?quality=12&learn=on` hinzu, um eine optimale Wiedergabe zu erzielen.
- Videos dürfen NICHT automatisch abgespielt werden. `?autoplay=true` nicht in der Dokumentation hinzufügen.
- Geben Sie immer eine Textalternative, ein Transkript oder einen Link zu schriftlichen Anweisungen an: „Schriftliche Anweisungen finden Sie unter [link].“
- Verwenden Sie aussagekräftige Beschriftungen.
- Aktivieren Sie Transkripte mit `{transcript=true}` in einzelnen Videos oder fügen Sie `auto-video-transcripts: true` zu `TOC.md` für ein ganzes Handbuch hinzu.

### Hinweise und Ermahnungen

```markdown
>[!NOTE]
>
>Note content here.

>[!TIP]
>
>Tip content here.

>[!IMPORTANT]
>
>Important content here.

>[!WARNING]
>
>Warning content here.

>[!CAUTION]
>
>Caution content here.
```

Zusätzliche Typen: `[!ADMIN]`, `[!AVAILABILITY]`, `[!PREREQUISITES]`, `[!INFO]`, `[!ERROR]`, `[!SUCCESS]`.

KRITISCHE Syntaxregeln:
- Zwischen dem Slogan und dem Inhalt MUSS eine leere `>` sein.
- Jede Fortsetzungszeile muss mit `>` beginnen.
- Blockquote-Syntax (`>` ohne -Tag) wird unterstützt, wird aber als einfaches Blockquote gerendert. Verwenden Sie sie NICHT, wenn Sie formatierte Hinweise erwarten.
- Fügen Sie KEINE Kommentare in Blockkomponenten wie Aufzählungslisten hinzu, insbesondere verschachtelte Aufzählungslisten. Der Kommentar kann die Darstellung der Liste ändern.

### Registerkarten

```markdown
>[!BEGINTABS]

>[!TAB Tab label]

Tab content here.

>[!TAB Another tab]

More content.

>[!ENDTABS]
```

- Verschachteln Sie Registerkartensätze NICHT.
- Verschachteln Sie Registerkartensätze NICHT in Listen.
- Registerkartentitel können nicht fett oder kursiv formatiert werden.
- Die In-Page-Suche (Strg+F) findet auf ausgeblendeten Registerkarten keinen Inhalt.

### Reduzierbare Abschnitte

```markdown
+++Click to expand
Content here.

* Bullet one
* Bullet two

+++
```

- Fügen Sie in ausblendbaren Elementen über und unter Listen und Codeblöcken leere Zeilen hinzu.
- Verschachteln Sie KEINE ausblendbaren Abschnitte innerhalb ausblendbarer Abschnitte.
- Überschriften in ausblendbaren Elementen sind zulässig, werden jedoch nicht empfohlen.
- Hinweis: Suchen in Seite (Strg+F) erkennt ausgeblendeten Text in Chrome, aber nicht in Safari.

### Schattenboxen

```markdown
>[!BEGINSHADEBOX "Optional Title"]

Content with gray background.

>[!ENDSHADEBOX]
```

### Codeblöcke

- Inline: einzelne Backticks `` `code` ``. Verwenden Sie für Cookie-Namen, Dateinamen, Werte, Parameter, Befehle und Beispiel-URLs, die nicht validiert werden sollten.
- Umgrenzte Blöcke: Dreifacher Backticks mit Sprachkennung (ermöglicht Syntaxhervorhebung und eine Schaltfläche „Kopieren„).
- Optionale Attribute: `{line-numbers="true"}`, `{start-line="7"}`, `{highlight="11-13, 16"}`
- Code-Blöcke werden NICHT lokalisiert. Keine Notwendigkeit, DNL oder UICONTROL in ihnen hinzuzufügen.
- Verwenden Sie Backticks (keine Anführungszeichen) für Code, Dateinamen, Parameter und eingegebenen Text.
- Verwenden Sie KEINE Bilder von Code. Verwenden Sie immer Codeblöcke.

### Abzeichen

- Inline: `[!BADGE Beta]{type=Informative}`
- Metadaten (über H1): `badgePremium: label="Premium" type="Positive"`
- Typen: `Informative` (blau), `Positive` (grün), `Negative` (rot), `Neutral` (dunkelgrau), `Caution` (gelb)
- Max. 2 Abzeichen in Metadaten pro Artikel.
- Platzieren Sie KEINE Abzeichen in Überschriften.
- Verwenden Sie KEINE Abzeichen für Informationen, die schnell veraltet sind (z. B. „Neu„).
- Abzeichenbeschriftungen sind lokalisiert. Halten Sie sie kurz.
- Verwenden Sie für das Beta-Badge nur die Frontend-`badgeBeta`. Platzieren Sie KEIN Inline-Badge in der H1.
- Wenn Sie möchten, dass eine Badge-URL in einer neuen Registerkarte geöffnet wird, fügen Sie `newtab=true` zur Badge-Syntax hinzu.

### Listen

- Verwenden Sie `*` oder `-` konsistent in einem einzelnen Artikel. Überprüfen Sie die Konvention der vorhandenen Datei. Das Mischen von Markierungen verursacht einen Validierungsfehler.
- Verwenden Sie für nummerierte Listen `1.` für jedes Element. GitHub/EDS nummeriert sie automatisch korrekt.
- Aufzählungslisten: wenn die Reihenfolge nicht wichtig ist. Nummerierte Listen: für Schritte und geordnete Verfahren.
- Verwenden Sie für ein einstufiges Verfahren einen Aufzählungszeichen (`*`) anstelle von `1.`.
- Halten Sie Listeneinträge kurz. Normalerweise ein Satz oder weniger.
- Perioden für ganze Sätze benutzen; Punkte weglassen für Einträge mit einem Wort oder unvollständigen Sätzen (Regel konsistent innerhalb einer Liste anwenden).
- Listenelemente NICHT mit Semikolons, Kommas oder Verbindungen wie „and“ oder „or“ beenden, wenn sie als einfache Serie gelesen werden sollen.
- Alle Listeneinträge müssen grammatisch parallel sein.
- Verschachtelten Inhalt einrücken: 3 Leerzeichen für nummerierte Listen, 2 für Aufzählungslisten.
- Listen mit leeren Zeilen umgeben.
- Verwenden Sie KEINE Aufgabenlisten (Kontrollkästchen für `- [ ]` im GitHub-Stil). Sie werden in Experience League nicht unterstützt.

### Tabellen

- Verwenden Sie standardmäßige Markdown-Tabellen.
- Bei komplexen Layouts (zusammengeführte Zellen, Rahmen aus) ist HTML `<table>` zulässig.
- Umschließen von Tabellen mit leeren Zeilen.
- Verwenden Sie bei Bedarf `{style="table-layout:auto"}` für Tabellen mit automatischer Breite.
- Screenshots in Tabellenzellen vermeiden. Kleine Symbole oder Miniaturen sind in Zellen zulässig.

### Hervorhebung der Vorschaufunktion

Verwenden Sie einen Bereich für Inline-Vorschauinhalte und einen div-Bereich für Mehrabsatz-Vorschauinhalte:

```markdown
<span class="preview">This feature is in limited availability.</span>
```

```markdown
<div class="preview">

Multiple paragraphs of preview content here.

</div>
```

### Snippets und Includes

```markdown
{{$include /path/to/snippet.md}}
```

Verwenden Sie für wiederverwendbare Inhaltsbausteine, die für mehrere Artikel freigegeben sind.

### Sonderzeichen

- Escape-Sonderzeichen im Textkörper mit einem umgekehrten Schrägstrich: `\#`, `\*`, `\[`, `\]`.
- Verwenden Sie HTML-Entitäten für spitze Klammern: `&lt;`, `&gt;`, `&amp;`.
- Verwenden Sie HTML-Entitäten für Sondersymbole: `&reg;`, `&mdash;`, `&ndash;`.

### Kommentare

Verwenden Sie HTML-Kommentare für Textentwürfe oder Anmerkungen für andere Autoren:

```markdown
<!-- This is a comment. Not rendered in the published doc. -->
```

Kommentare sind für Benutzer sichtbar, die auf GitHub.com bearbeiten. Geben Sie in Ihren Kommentaren KEINE vertraulichen Informationen an.

Fügen Sie KEINE Kommentare innerhalb von Blockkomponenten wie Aufzählungslisten hinzu (insbesondere verschachtelte). Kommentare können das Listen-Rendering beeinträchtigen. Kommentieren Sie in Inhaltsverzeichnisdateien keine Zeilen in der Mitte der Inhaltsverzeichnisliste aus - verschieben Sie stattdessen Kommentare an das Ende der Datei.

### Tastaturaktionen

Fettdruck für jede einzelne Taste in einem Tastaturbefehl: **cmd** + **Umschalt** + **p**.

### Benennung von Dateien und Ordnern

- Markdown-Dateinamen: Kleinbuchstaben mit Bindestrichen. Keine Großbuchstaben, Unterstriche, Punkte oder Leerzeichen.
- Verwenden Sie beschreibende Slugs: `create-calculated-metric.md`, `calculated-metric-overview.md`. Vermeiden Sie bloße Dateinamen wie `overview.md` oder `introduction.md`, es sei denn, die IA erfordert einen festen Namen.
- Vermeiden Sie Dateinamen, die mit JavaScript/CSS in Konflikt stehen: `metadata.md`, `search.md`.
- Asset-Dateinamen: vorzugsweise Kleinbuchstaben; Großbuchstaben und Unterstriche zulässig, aber nicht empfohlen.

&#x200B;---

## &#x200B;3. Lokalisierungs-Tags (CRITICAL)

Wenden Sie Lokalisierungs-Tags immer an. Maschinelle Übersetzung wird automatisch bei jedem Commit an Main ausgeführt.

### `[!DNL Product Name]`: Nicht lokalisieren

Verwenden Sie für Markenproduktnamen, die in englischer Sprache bleiben müssen.

**Anwenden auf:**
- Adobe-Produktnamen: `[!DNL Analytics]`, `[!DNL Target]`, `[!DNL Campaign]`, `[!DNL Experience Platform]`
- Produktnamen von Drittanbietern: `[!DNL Mozilla Firefox]`, `[!DNL Workfront]`
- Funktionale Namen, die die Übersetzung verwirren könnten: `[!DNL Pass]`, `[!DNL Campaign]`
- Boolesche Operatoren, die als logische Begriffe verwendet werden: `[!DNL AND]`, `[!DNL OR]`

**Nicht anwenden auf:**
- URLs, Dateinamen oder Verzeichnisnamen
- Code-Blöcke (nicht standardmäßig lokalisiert)
- Akronyme (bleiben automatisch auf Englisch)
- Begriffe bereits in der Datenbank „Nicht übersetzen“

**In-Link-Text** Entfernen Sie die Tag-Klammern, um Rendering-Probleme zu vermeiden. Verwenden Sie `[Adobe](https://www.adobe.com)` nicht `[[!DNL Adobe]](https://www.adobe.com)`.

### `[!UICONTROL Label]`: Benutzeroberflächen-Steuerelemente

Verwenden Sie für Elemente der Benutzeroberfläche: Optionen, Felder, Registerkarten, Seiten, Menüs, Schaltflächen und Funktionsnamen, wie sie in der Benutzeroberfläche angezeigt werden. Dies ist das wichtigste Tag für die Übersetzungsqualität. Behandeln Sie sie in Verfahren als obligatorisch.

**Anwenden auf:**
- Jedes anklickbare UI-Element in Verfahrensschritten (obligatorisch)
- Funktionsnamen und Navigationselemente, wie im Produkt gezeigt
- Seitennamen, Optionen, Felder und Registerkarten, wie in der Benutzeroberfläche beschriftet

**Formatierung:**
- Fett in Schritten und Navigation: `Select **[!UICONTROL Destinations]** from the left navigation.`
- Kursiv kann aus Gründen der Übersichtlichkeit auch im Konzepttext (ohne Schritt) verwendet werden.
- In HTML-Tabellen: `<span class="uicontrol">term</span>` anstelle von &grave;&grave; verwenden.
- Im Link-Text: Entfernen Sie die Tag-Klammern.

**Groß-/Kleinschreibung** Gleichen Sie die Schnittstelle genau ab.

**Nicht anwenden auf:**
- Konzeptionell verwendete generische Begriffe: „Segment“, „Metrik“, „Kampagne“ (nur bei explizitem Verweis auf das Benutzeroberflächenelement)
- Lange Sätze (es sei denn, der Elementname der Benutzeroberfläche selbst ist eine lange Phrase)
- Codeblöcke oder Akronyme
- Symbolbeschreibungen. Verwenden Sie den Mauszeiger über dem Symbol bzw. den QuickInfo-Namen, falls verfügbar. Taggen Sie keine allgemeinen Beschreibungen wie „Bleistiftsymbol“.

### `[!DNL]`: Gesamte Abschnitte ausschließen

Verpacken Sie Inhalte, die in allen Gebietsschemata auf Englisch bleiben müssen:

```markdown
>[!DNL]
>
>Content that must not be translated.
```

Wird nicht in Code-Blöcken benötigt. Diese sind nicht standardmäßig lokalisiert.

### Wo Tags verwendet werden können und nicht

**Kann verwendet werden in:** Absätzen, Listen, Überschriften, Tabellen, Abzeichen, Alternativtext und Metadaten.

**Kann nicht verwendet werden in:** Codeblöcken, Akronymen.

**Metadatenregel:** Wenn ein Metadatenfeld (Titel oder Beschreibung) mit einem `[!DNL]`- oder &grave;&grave;-Tag beginnt, schließen Sie den gesamten Feldwert in Anführungszeichen ein, oder die Validierung schlägt fehl.

&#x200B;---

## &#x200B;4. Informationsstruktur und Inhaltstypen

### Drei Inhaltstypen: Trennen Sie sie

- **Konzept**: Was und warum. Einführungen, Übersichten, Hintergrund. Verwenden Sie Überschriften mit Substantiv/Substantiv/Phrase.
- **Aufgabe**: Wie. Schrittweise Anleitungen. Verwenden Sie Verbüberschriften aus dem Imperativ. Immer ein Konzept vorausgesetzt.
- **Referenz**: Felder, Parameter, Optionen, Fehlercodes. Verwenden von Tabellen. Mit anderem Referenzmaterial sammeln.

### Artikelstruktur

- Öffnen Sie mit einem konzeptionellen Kontext, der den Leser ausrichtet.
- Gehen Sie dann zu Aufgaben und dann zu Referenzmaterial.
- Beantworte eine spezifische Frage pro Seite. Nicht zu breit, nicht zu schmal.
- Konzeptseite mit untergeordneten Aufgabenseiten (mehrseitig), ODER H1-Konzept + H2-Aufgabenunterüberschriften (einzelne Seite).
- Synonyme oder frühere Namen einmal einführen (z. B. „ECID (Experience Cloud ID)„), um Suchbegriffe zu verbinden.

### Schritte

- Jeder Schritt ist ein einzelner Befehl: ein vollständiger Satz mit einem Punkt (oder Doppelpunkt bei Einführung einer Unterliste).
- Die Schritte beginnen immer mit dem Verb oder dem Ziel vor der Aktion: „Um den Bericht auszuführen, wählen Sie „Ausführen“ aus.“
- Kombinieren Sie kleine Aktionen, die an derselben Stelle in der Benutzeroberfläche stattfinden, zu einem Schritt, wenn der Satz klar bleibt.
- Target 7 Schritte pro Aufgabe; 10 ist das praktische Maximum. Unterteilen Sie längere Aufgaben in Teilaufgaben auf.
- Verwenden Sie einen einzelnen Aufzählungszeichen (nicht `1.`) für ein Verfahren, das nur einen Schritt hat.
- Verwenden Sie KEINE Überschriften als Schritte in der Produktdokumentation. Verwenden Sie für lange mehrseitige Tutorials bei Bedarf Unterüberschriften im Stil „Schritt 1: …“.
- Fügt eine Einrückung (erklärender Text) hinter dem Schritt ein.
- Platzieren Sie Screenshots eingerückt nach dem Schritt oder der Aktion, der bzw. die den Bildschirm angezeigt hat.
- Wiederholen Sie Seiten-, Registerkarten- oder Bedienfeldnamen in Schritten, damit die Leser wissen, wo sie sich befinden.

### Inhaltsverzeichnisdateien (TOC.md)

- Großschreibung aller Einträge (Eigennamen und Benutzeroberflächenelemente ausgenommen).
- Begriffseinträge: Substantive und Substantivsätze.
- Aufgabeneinträge: Verben des Imperativs (keine Gerundien).
- Einträge parallel halten.
- Jede Abschnittsüberschrift im Inhaltsverzeichnis muss eine gültige Anker-ID aufweisen: `+ Processing rules {#processing-rules}`
- Eine Abschnittsüberschrift (übergeordnetes Element) im Inhaltsverzeichnis kann kein Link sein. Sie muss eine Anker-ID haben.
- Fügen Sie dieselbe Datei NICHT mehrmals in einem Inhaltsverzeichnis hinzu.
- Zeilen in der Mitte einer Inhaltsverzeichnisliste NICHT auskommentieren. Verschiebt Kommentare an das Ende der Datei.

### Ausblenden von Dateien aus der Navigation

Verwenden Sie die **V2** Methode für alle neuen Arbeiten. Die V1-Methode wird nicht mehr unterstützt.

**V2 (aktuell): `{hide-from-toc}` in Inhaltsverzeichnis.md**

Platzieren Sie `{hide-from-toc}` direkt in `TOC.md` vor dem Artikel oder Abschnitt, den Sie ausblenden möchten. Fügen Sie es NICHT zum Artikel frontmatter hinzu.

```
+ {hide-from-toc} [Article title](filename.md)
+ {hide-from-toc} Section name {#section-id}
  + [Nested article](nested.md)
```

- Ausgeblendete Artikel bleiben über direkte URL zugänglich.
- Ein Abschnitt, dessen Einträge alle ausgeblendet sind, verschwindet selbst aus der linken Navigation.

**V1 (veraltet): `hidefromtoc: yes` in frontmatter**

```yaml
hidefromtoc: yes
```

Verwenden Sie diese Option NICHT auf neuen Seiten. Der Artikel muss weiterhin in `TOC.md` zur Veröffentlichung angezeigt werden, er wird jedoch nicht im linken Navigationsbereich angezeigt.

**Vor Suchmaschinen verstecken: `hide: yes` in Frontmatter**

```yaml
hide: yes
```

Dadurch wird die Seite sowohl aus der externen als auch aus der internen Suche ausgeschlossen. Durch Festlegen von `hide: yes` wird automatisch `index: no` festgelegt. Verwenden Sie diese Option zusätzlich zum `{hide-from-toc}`, wenn eine Seite sowohl für die Navigation als auch für die Suche ausgeblendet werden soll.

&#x200B;---

## &#x200B;5. Terminologie und Branding

Autorisierende Quelle: [AEP User-Facing Terminology Wiki](https://wiki.corp.adobe.com/spaces/DMSArchitecture/pages/1230620427/Adobe+Experience+Platform+User-Facing+Terminology). Die neueste Version finden Sie immer im Confluence MCP Tool (`mcp__adobe-wiki-confluence`).

### Produktnamen

Verwenden Sie immer genau diese Formulare. Fügen Sie &quot;Adobe&quot; bei der ersten Referenz in ein Handbuch ein. Sie können es bei nachfolgenden Erwähnungen weglassen, wenn die Richtlinie dies zulässt.

Den Produktnamen darf NICHT der Name vorangestellt werden, es sei denn, der offizielle Name enthält ihn.
- Richtig: „Erste Schritte mit dem KI-Assistenten.“
- Falsch: „Erste Schritte mit dem KI-Assistenten.“

| Korrekt | NIE verwenden |
|---|---|
| Adobe Experience Platform | AEP, AXP, Adobe XP, Adobe Cloud Platform |
| Experience Platform (sekundäre Referenz) | Plattform (allein, sofern der Kontext nicht eindeutig ist) |
| Adobe Real-Time CDP | RTCDP, ARTCDP |
| Real-Time CDP (sekundär) | Real-Time CDP (Kleinbuchstaben „t„) |
| Adobe Real-Time Customer Data Platform | – |
| Echtzeit-Kundenprofil | Echtzeit-Kundenprofil, Einheitliches Profil |
| Adobe Journey Optimizer | AJO |
| Adobe Journey Optimizer B2B Edition | AJO B2B |
| Adobe Marketo Optimizer | AMO |
| Adobe Marketo Engage | Marketo (kann nicht als Adjektiv verwendet werden) |
| Adobe Customer Journey Analytics | CJA |
| Customer Journey Analytics (sekundär) | – |
| Adobe Real-Time CDP Collaboration | RTCDP Collaboration, RTCDP Collab, Collab |
| Adobe Real-Time CDP-Verbindungen | RTCDP Connections, AEP Connections, Connections (allein) |
| Adobe Experience Platform Edge Network | Platform Edge Network, Platform Edge, Adobe Experience Edge |
| Tags (Produktname) | Launch (veraltet) |
| Entscheidungs-Management | Offer Decisioning (nur Klammern: „ehemals Offer Decisioning„) |
| Datenstrom (ein Wort, Kleinbuchstaben) | Daten-Streaming, Edge-Konfiguration |
| Analysis Workspace | Analysis Workspace, Workspace, Workspace |
| Adobe AI | Sensei (veraltet) |
| Adobe GenAI | – |
| Adobe GenStudio for Performance Marketing | – |

**„Real-Time“** verwendet immer Kapital-R und Kapital-T, wenn sie Teil eines Produktnamens sind (Real-Time CDP, Echtzeit-Kundenprofil, Real-Time Customer Data Platform).

**Editionen**: „Editionen“ werden allgemein in Kleinbuchstaben geschrieben. „Edition“ wird als Teil eines Produkteditionsnamens großgeschrieben (z. B. &quot;Adobe Real-Time CDP B2C Edition„).

**Abkürzungen in der externen**: Abkürzungen von Produktnamen sind in der benutzerseitigen Dokumentation NICHT zulässig. Keine AEP, CJA, AJO oder RTCDP in Dokumenten. Eingeschränkte Ausnahmen: Akronyme können bei der ersten Verwendung, wenn sie SEO unterstützen, oder in Inhaltsverzeichniseinträgen, Beschreibungsmetadaten und Überschriften, bei denen die Länge ein Problem darstellt, in Klammern erscheinen.

### Funktionale und konzeptionelle Terminologie

| Korrekt | NICHT verwenden |
|---|---|
| Ereignisweiterleitung | Server-seitige Weiterleitung, Server-seitig starten |
| Zulassungsliste | Whitelist |
| Blockierungsliste/Blockierungsliste | auf die schwarze Liste setzen |
| primär/replikat ODER primär/sekundär (Server) | Master/Slave |
| main (GitHub-Verzweigung) | Vorlage |
| ethischer Hacker | White Hat Hacker |
| Remarketing | Retargeting |
| Feldgruppe | mixin (veraltet), Erweiterungen, Mixins |
| Automatischer Ablauf von Daten | TTL, Time-to-Live, Ablauf |
| Nicht-Produktions-Sandbox | Staging (als Umgebungsname) |
| Segmentdefinition | Segment (allein, wenn die Definition gemeint ist) |
| ID (immer großschreiben) | ID |
| Aufnahme/Aufnahme/Aufnahme | Onboarding (für das Hinzufügen von Daten zu Platform) |
| Datensatz/Datensätze | Datendatei, Datensatzdateien |
| Zugriffskontrolle | Berechtigungen (für die Platform-Funktion) |
| Widget | Metrikkarte (veraltet) |
| Platzhaltervariable | Platzhaltervariable |
| nicht verfügbar/gesperrt/ausgeschaltet/deaktiviert | ausgegraut |
| Kohärenzprüfung | Plausibilitätsprüfung |
| Integriert | Nativ (als Synonym für „Built-in„) |
| Hohe Priorität | Mostnagel |
| Veraltet | Besitzstandsklausel |
| Primär/Main/Source | Primär (als Deskriptor) |

**Analytics-spezifische Groß-/Kleinschreibung:**
- Bereichsnamen werden in Kleinbuchstaben geschrieben: leer, Attribution, Experimentieren, Freiform (Ausnahme: &quot;Journey-Arbeitsfläche„)
- Namen der Visualisierungen werden in Kleinbuchstaben geschrieben: Balken, Ringdiagramme, Histogramme, Linien, Baumkarten, Text

### Schreibgeschützte Begriffe: NIE in öffentlich zugänglichen Dokumenten verwenden

Diese Begriffe erscheinen in Jira, Wikis und internen Diskussionen, dürfen jedoch nie in der Dokumentation vorkommen:

| Interner Begriff | Stattdessen verwenden |
|---|---|
| AEP | Adobe Experience Platform |
| HANDFLÄCHE | Sandbox-Verwaltung/Zugriffskontrolle |
| BIOME | Umgebung |
| Hydrat/Hydratation | Erstellen/Auffüllen |
| Einheitliches Profil | Echtzeit-Kundenprofil |
| Staging (Umgebung) | Nicht-Produktions-Sandbox |
| DTM | Tags |
| Mandant | IMS-Organisation/Organisation |
| CRUD | Erstellen, Lesen, Aktualisieren und Löschen (buchstabieren) |
| Siphon, BSO, Ethos | Interne Codenamen, nie extern |
| Hopfen | Interner DSGVO-/Zugriffskontrollbegriff |
| Geschwindigkeit | Nicht nutzerorientierter Werbebegriff |
| Vertriebskette | Interner Adobe-Infrastrukturbegriff |

&#x200B;---

## &#x200B;6. Inklusive Sprache und Zugänglichkeit

### Inklusive Sprachgrundsätze

- Verwenden Sie geschlechtsneutrale Begriffe: „Vertriebsmitarbeiter“ nicht „Verkäufer“, „Moderator“ nicht „Vorsitzender“.
- Bevorzuge die zweite Person („du„), um Geschlechtspronomen zu vermeiden.
- Verwenden Sie „sie“ im Singular für eine Person, deren Geschlecht unbekannt ist. Benutzen Sie sie NICHT oder verwenden Sie sie NICHT.
- Namen von nicht-weißen Kulturen in Beispiele aufnehmen (z. B. Ayesha, Ibrahim, Vignesh, Quynh). Verwenden Sie NICHT nur kulturell weiße Namen (John, Bill, Karen, Amy).
- Geschlecht (männlich/weiblich) NICHT mit Geschlecht (Mann/Frau) vermengen.
- Kapitalisieren von Nationalitäten, Völkern, Rassen (außer „weiß“ gemäß AP Stylebook) und Stämmen.
- Verwenden Sie die Sprache des Menschen als Erstes: „Menschen, die Hilfstechnologien nutzen“, nicht „die Behinderten“.
- Vermeide Euphemismen wie „anders aktiviert“. Vermeiden Sie Deskriptoren, die als Substantive verwendet werden: „Blind“, „The Deaf“.
- Vermeide Begriffe, die die Identität widerspiegeln (kulturelle Aneignung): Geisttier, Sherpa, Pow Wow, Guru, Ninja, Stamm.

### Nicht-inklusive Terminologie zur Vermeidung von

| Verwenden | Nicht |
|---|---|
| Zulassungsliste//Blockierungsliste | Whitelist/Blacklist |
| primär / replikat ODER primär / sekundär | Master/Slave |
| Main (Git-Verzweigung) | Vorlage |
| Hohe Priorität | Mostnagel |
| Platzhaltervariable | Platzhaltervariable |
| nicht verfügbar/gesperrt/ausgeschaltet/deaktiviert | ausgegraut |
| Kohärenzprüfung | Plausibilitätsprüfung |
| Integriert | Nativ (als Synonym) |
| Behörde/Experte | Guru / Ninja |
| Mitglieder Ihrer Gruppe | Angehörige eures Stammes |
| Besprechung | Pow wow / Kreis der Wagen |
| Vorbild / Verwandter Geist | Spirituose |
| Handbuch | Sherpa |
| Veraltet | Besitzstandsklausel |
| vergebliches Unterfangen | Todesmarsch |
| Lächerlich/inkompetent/unvorhersehbar | dumm / lahm / verrückt |
| Ethischer/unethischer Hacker | White Hat / Black Hat Hacker |
| Video abspielen | Video ansehen |
| Anzeigen/Anzeigen/Zu allen wechseln | Alle anzeigen |

### Barrierefreiheit: Beschreibung der Benutzeroberfläche

Beschreiben Sie Benutzeroberflächenelemente NICHT nach Farbe oder Bildschirmposition. Farbe funktioniert nicht für farbenblinde Benutzer oder Bildschirmlesehilfen. Die Bildschirmposition ist bei Hilfstechnologien unzuverlässig.

**Verwenden Sie eine chronologische Sprache, keine räumliche Sprache:**

| Verwenden | Nicht |
|---|---|
| Erst, dann, schließlich | Oben, unten |
| In der Menüleiste | Links |
| Vor/Nach | Oben/unten auf dem Bildschirm |

**Beschreiben Sie, was Steuerelemente tun, und nicht, wie sie aussehen:**

| Verwenden | Nicht |
|---|---|
| Suche auswählen | Klicken Sie auf die Lupe |
| Bearbeiten | Das Stiftsymbol |
| Ein/Aus | Umschalten/Umschalten/Aktivieren |
| Menü | Seitenlade |
| E-Mail-Adresse eingeben | E-Mail-Adresse eingeben |
| Speichern Sie. | Die Schaltfläche „Speichern“ |
| Abbrechen | Schließen |

Verwenden Sie KEINE Farbe allein, um Informationen zu vermitteln. Paaren Sie Farbe immer mit Text oder Form.

### Barrierefreiheit: Alt-Text

- Beschreiben Sie, was das Bild zeigt, nicht nur den Namen des Bildschirms.
- Vollständige Sätze mit korrekter Grammatik und Interpunktion verwenden.
- Binden Sie relevanten Text aus dem Bild ein.
- Verwenden Sie vollständige Wörter, keine Abkürzungen. Bildschirmlesehilfen schreiben die Abkürzungen laut.
- Bilder, die Informationen unabhängig vom umgebenden Text vermitteln, MÜSSEN ALT-Text enthalten.
- Bei rein dekorativen Bildern wird Alt-Text möglicherweise weggelassen, es empfiehlt sich jedoch, ihn einzuschließen.
- Testen Sie Bilder mit einem Simulator für Farbenblindheit, wenn Farbe verwendet wird, um Bedeutung zu vermitteln.
- Verwenden Sie KEINE animierten Grafiken, die mehr als dreimal pro Sekunde blinken (Anfallsrisiko).

### Barrierefreiheit: links

- Verwenden Sie niemals „hier klicken“ oder „Link“ als Link-Text.
- Machen Sie das Ziel nur aus dem Link-Text klar.
  - Gut: „Siehe Voraussetzungen für RTCDP im RTCDP-Benutzerhandbuch.“
  - Schlecht: „Klicken Sie hier für Voraussetzungen.“

### Barrierefreiheit: Videos

- Videos dürfen NICHT automatisch abgespielt werden.
- Geben Sie immer eine Textalternative, ein Transkript oder einen Link zu schriftlichen Anweisungen an.
- Binden Sie aussagekräftige Untertitel in alle Videos ein.
- Wenn möglich, Link zu schriftlichen Anweisungen: „Schriftliche Anweisungen finden Sie unter [link].“

&#x200B;---

## &#x200B;7. Rechtschreibung und Satzzeichen

### Amerikanische englische Rechtschreibung

| Verwenden | Nicht |
|---|---|
| Farbe | Farbe |
| erkennen | erkennen |
| Lizenz | Lizenz |
| Zeit | Zeit |
| Gültigkeit | Ablauf |
| Zähler | Zähler |
| unter | unter |

### Interpunktionsregeln

- Schlussanführungszeichen gehen außerhalb von Kommas und Punkten.
- Anführungszeichen für Anführungszeichen von Personen reservieren. UI-Zeichenfolgen nicht zitieren (verwenden Sie UICONTROL und fett in Schritten).
- Verwenden Sie Kursiv für Begriffe, die als Begriffe verwendet werden (keine Anführungszeichen): *profile*, nicht „profile“.
- Verwenden Sie Backticks für Code, Parameter, Dateinamen und eingegebenen Text: `datasetId`.
- Fett: Nur für Benutzeroberflächenelemente in Prozeduren (mit UICONTROL) und Schlüsselbegriffe bei der ersten Einführung. Fettgedruckte Lead-Zeilen sind in FAQ-Layouts zulässig, in denen keine Fragen auf Überschriftenebene verwendet werden.
- Kursiv: für Hervorhebungen, Fremdwörter, Begriffe, die definiert werden, oder konzeptionelle Namen in Nicht-Schritt-Text.
- Fett + Kursiv kombiniert: `***text***`.
- Verwenden Sie KEINE horizontalen Regeln `---` oder `***`. Sie werden in Experience League nicht unterstützt.
- Verwenden Sie KEINE AEM-Bindestriche (—), Bindestriche (-) oder Bindestriche in der Prosa. Formulieren Sie stattdessen den Satz neu. Bindestriche sind nur in zusammengesetzten Adjektiven zulässig, die in der Benutzeroberfläche, in Dateinamen und im Code angezeigt werden.
- Doppelpunkt: dient zur Einführung einer Liste. Das erste Wort nach dem Doppelpunkt wird großgeschrieben, wenn ein ganzer Satz folgt (oder das Wort ein Eigennamen ist).
- Keine Semikolons. Stattdessen einen Punkt und einen neuen Satz verwenden.

&#x200B;---

## &#x200B;8. SEO und Auffindbarkeit

- Nehmen Sie Suchbegriffe (Keywords) in erste Absätze auf.
- Verwenden Sie Begriffe, nach denen Leser tatsächlich suchen. Geben Sie Synonyme und Namen früherer Begriffe an, sofern hilfreich.
- Schlüsselwörter in Überschriften: enthalten Funktionsnamen, Elemente der Benutzeroberfläche und die ausgeführte Aufgabe.
- Alt-Text auf Bildern wird von Google indiziert. Machen Sie es beschreibend und aussagekräftig.
- Vermeiden Sie es, wichtige Begriffe nur in komplexen Tabellen oder Bildern (die nicht zuverlässig durch KI oder Suche indiziert werden) zu platzieren.
- Beschreibungsmetadaten: Verwenden Sie eine natürliche Sprache mit Schlüsselwörtern. Keine zufälligen Keywords pauken. Google kann Inhalte für die Keyword-Füllung herabstufen.
- Halten Sie Metadatenfelder (Titel, Beschreibung, Funktions-Tags) vollständig und genau - Erkennungsoberflächen verwenden Metadaten, um Ergebnisse zu filtern und zu reihen, bevor Seiteninhalte gelesen werden.

&#x200B;---

## &#x200B;9. Datei- und Repo-Konventionen

- Für jede `.md`-Datei ist Frontmatter erforderlich.
- Bilder werden in einen `assets/` Unterordner relativ zur Markdown-Datei verschoben.
- Bilder, die nicht lokalisiert werden dürfen, werden in einen `do-not-localize/` Unterordner verschoben.
- Inhaltsverzeichnisdateien (`TOC.md`) definieren die linke Navigationsstruktur. Aktualisieren Sie sie beim Hinzufügen oder Entfernen von Seiten.
- Verwenden Sie Stammrelationen (`/help/...`) für Querverweise zwischen Dokumenten in diesem Repository.
- Verwenden Sie für Links zu Dokumenten außerhalb dieses Repositorys absolute `https://experienceleague.adobe.com/de...`-URLs.
- Zweigname: kein Präfix für Benutzernamen. Verwenden Sie die Jira-Ticketnummer und einen Slug mit Großschreibung des Titels (z. B. `PLAT-12345-Update-Guardrail-Limits`). Benennen Sie sowohl die Verzweigung als auch den PR-Titel im selben Format.
- Einzelne Komponenten (Überschriften, eingezäunte Codeblöcke, Listen) müssen von Leerzeilen umgeben sein.
- Nur ein H1 (`#`) pro Dokument. Die erste Zeile nach frontmatter muss die H1 sein.

&#x200B;---

## &#x200B;10. Checkliste überprüfen

Überprüfen Sie bei der Überprüfung oder Bearbeitung der Dokumentation alle unten aufgeführten Elemente.

**Stimme und Stil**

- [ ] Benutzerfokussierte Stimme. Nein, „ermöglicht Ihnen Folgendes“, „ermöglicht Ihnen Folgendes“
- [ ] „Sie“ anstelle von „Benutzer“ verwendet, wenn die Zielgruppe direkt angesprochen wird
- [ ] Zweite Person und Imperative Stimmung bei Eingriffen
- [ Aktive Stimme ]
- [ ] Sätze ≤20 Wörter
- [ ] Keine vagen Adjektive („schnell“, „einfach„). Ersetzen Sie durch genaue Beschreibungen.
- [ ] Schlüsselbegriffe werden zur KI-Erkennung im Textkörper angezeigt (nicht nur in Bildern oder Tabellen)

**Struktur und Überschriften**
- [ ] Überschriften: Groß-/Kleinschreibung des Satzes, ≤5 Wörter/69 Zeichen, gefolgt vom Textkörper, keine gestapelten Überschriften
- [ ] Keine übersprungenen Überschriftenebenen
- [ ] Konzeptüberschriften sind Substantivsätze; Aufgabenüberschriften sind Verben von zwingender Bedeutung
- [ ] Target 7 Schritte pro Aufgabe; max. 10. Einzelschritte verwenden einen Aufzählungszeichen, keinen `1.`
- [ ] 8 Elemente pro Aufzählungsliste

**Terminologie**
- [ ] Richtige Produktnamen und Formulare (Abschnitt 5)
- [ ] Keine veralteten Begriffe: Mixin, TTL, Offer Decisioning, Launch, Unified Profile, Echtzeit (Kleinbuchstaben t), Sensei
- [ ] Keine Ausdrücke auf interner Basis: AEP, PALM, BIOME, Hydrat, Staging, DTM, Mandant, Pipeline
- [ ] Keine nicht-inklusiven Begriffe: Whitelist, Blacklist, Master/Slave, Vernunftprüfung, Dummy, ausgegraut, Native, Guru, Ninja, Spirit Animal, Sherpa, Death March, Pow Wow, Tribe
- [ ] „das“ vor dem Produktnamen (z. B. nicht „die Adobe Experience Platform„)

**Lokalisierungs-Tags**
- [ ] &grave;&grave; für alle Elementnamen der Benutzeroberfläche; fett in Schritten
- [ ] `[!DNL]` auf alle Produkt- und Drittanbieternamen
- [ ] boolesche Operatoren mit Tags: `[!DNL AND]`, `[!DNL OR]`
- [ ] Keine Tags in Code-Blöcken
- [ ] Metadatenfelder, die mit einem Tag beginnen, werden in Anführungszeichen gesetzt

**Markdown-Syntax**
- [ ] Richtige Ermahnungssyntax (leere `>` zwischen Tag und Inhalt)
- [ ] Listen verwenden konsistente Markierungen; nummerierte Listen verwenden `1.` für jedes Element
- [ ] Keine Aufgabenlisten (`- [ ]`)
- [ ] Keine horizontalen Regeln (zwischen Inhalten `---`)
- [ ] Leerzeilen rund um Überschriften, Codeblöcke, Listen und Tabellen
- [ ] Keine Bilder von Code. Verwenden Sie Codeblöcke.
- [ ] Screenshots verwenden ein Light-Design, keine Kundendaten und keine Benutzeroberfläche von Drittanbietern

**Barrierefreiheit**
- [ ] Alternativtext: vollständige Sätze, vollständige Wörter, beschreibt Inhalte (nicht nur den Bildschirmnamen)
- [ ] Keine richtungsweisende/räumliche Sprache: kein „oben“, „unten“, „links“, „oben rechts“
- [ ] Link-Text beschreibt das Ziel. Kein „hier klicken“
- [ ] Videos nicht auf automatische Wiedergabe eingestellt; Transkripte oder geschriebene Alternativen bereitgestellt
- [ ] Keine Farbe allein zur Informationsübermittlung

**Dateien und Links**

- [ ] Erforderliche Schriftart: Titel (Title Case, ≤60 Zeichen), Beschreibung (150 bis 160 Zeichen)
- [ ] Keine bloßen URLs im Textkörper. Verwenden Sie immer beschreibenden Link-Text.
- [ ] Stamm-relative interne Links; absolute Links für repo-übergreifende Verweise
- [ ] Dateinamen werden mit Bindestrichen in Kleinbuchstaben geschrieben. Deskriptive Slugs (keine bloßen `overview.md`)
- [ ] Bilder in `assets/`; nicht lokalisierte Bilder in `do-not-localize/`

&#x200B;---

## &#x200B;11. Externe Referenzen

Verwenden Sie das richtige MCP-Tool basierend auf dem Ressourcentyp:

- **Jira Tickets und Probleme** (`jira.corp.adobe.com`): Verwenden des Corp Jira MCP-Tools (`mcp__corp-jira`)
- **Wiki / Confluence Pages** (`wiki.corp.adobe.com`): Verwenden des Confluence MCP-Tools (`mcp__adobe-wiki-confluence`)
- **Öffentliche Experience League / Webseiten**: Verwenden Sie WebFetch

**Interne Wiki-Seiten (verwenden Sie das Confluence MCP-Tool):**
- **Terminologie-Wiki**: https://wiki.corp.adobe.com/spaces/DMSArchitecture/pages/1230620427/Adobe+Experience+Platform+User-Facing+Terminology
- **Platform-Stilhandbuch**: https://wiki.corp.adobe.com/spaces/DMSArchitecture/pages/1938986972/Platform+style+guide
- **Leitfaden zu Barrierefreiheit und Inklusivität**: https://wiki.corp.adobe.com/spaces/DMSArchitecture/pages/2234798784/Writing+for+accessibility+and+inclusivity
- **Handbuch zu kontextuellen Hilfe-Popovers**: https://wiki.corp.adobe.com/spaces/DMSArchitecture/pages/2575057078/How+to+add+contextual+help+popovers+to+the+Experience+Platform+documentation+and+UI

**Öffentlich (WebFetch verwenden):**
- **Lokalisierungsübersicht**: https://experienceleague.adobe.com/en/docs/authoring-guide/using/authoring/localization/localization-overview
- **Referenz zu Lokalisierungs-Tags**: https://experienceleague.adobe.com/en/docs/authoring-guide/using/authoring/localization/localize
- **Markdown-Syntax in Experience League**: https://experienceleague.adobe.com/en/docs/authoring-guide/using/markdown/markdown-syntax
- **Markdown-Schnellübersicht**: https://experienceleague.adobe.com/en/docs/authoring-guide/using/markdown/cheatsheet
- **Stilreferenz für Versionshinweise**: https://experienceleague.adobe.com/de/docs/experience-platform/release-notes/latest

**Lokaler Klon:**
- **Authoring-Handbuch repo:** Verwenden Sie einen verfügbaren Checkout des Adobe Experience League Authoring-Handbuchs oder der öffentlichen Dokumentation.
