---
title: Erstellung von E-Mails
description: Verwenden Sie die E-Mail-Design-Tools in Journey Optimizer B2B Prime, einschließlich E-Mail-Vorlagen, Fragmenten, Personalisierung, Dunkelmodus und Validierung.
autotag-review: '2026-06-12T22:51:19.543Z'
TQID: 'https://experienceleague.adobe.com/-mtyiJ98caCTuTKaZbzYrYKiQoxolq-hMw7p5h7bNpY'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: e666e996-b2cf-4c45-8fc2-1c625212ababid: f01b5556-e951-40ba-8625-2e3001864f2bid: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: e7bdffdc-2950-4be5-8c23-84240a995090id: ff0c35fa-aa7e-4050-a37c-198fcacd09e6id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: cb3217c9fd7beb712d0c61638d143b798010d2b7
workflow-type: tm+mt
source-wordcount: 2775
ht-degree: 2%

---

# Erstellung von E-Mails

[!DNL Adobe Journey Optimizer B2B Prime] bietet der E-Mail-Design-Bereich eine visuelle Arbeitsfläche, auf der Marketing-Experten E-Mails erstellen. Die E-Mail-Design-Tools im linken und oberen Bereich (Strukturen, Inhaltskomponenten, Vorlagen, Fragmente usw.) unterstützen die Erstellung von Grund auf per Drag-and-Drop. Sie können auch mit einer Vorlage beginnen, unformatierte HTML einfügen oder Nachrichten aus wiederverwendbaren visuellen Fragmenten zusammenstellen.

>[!IMPORTANT]
>
>Informationen zum Einrichten von Subdomains, Authentifizierung, IP-Pools und E-Mail-Kanal-Konfigurationen durch Administratoren finden Sie unter [E-Mail-Zustellbarkeit und Kanalkonfiguration](../admin/configuration-email-deliverability.md).

[!DNL Journey Optimizer B2B Prime] ist jede E-Mail mit einer Aktion _[!UICONTROL E-Mail senden]_ innerhalb einer Journey verknüpft. Der vollständige Workflow vom Journey-Design bis zur E-Mail-Definition erfolgt in einem kontinuierlichen Erlebnis. Wenn Sie [ Knoten _E-Mail senden_ zu ](../marketing/person-journey-nodes.md#add-an-action-node) Personen-Journey hinzufügen, klicken Sie auf **[!UICONTROL E-Mail erstellen]**, um den Design-Prozess für E-Mail-Inhalte zu starten.

Diese Aktion startet den E-Mail-Design-Bereich, in dem Sie anhand der folgenden Optionen auswählen können, wie Sie Ihre E-Mail gestalten möchten:

* [Erstellen Sie Ihre E-Mail von Grund ](#design-your-email-from-scratch) mithilfe der visuellen Design-Oberfläche. Erstellen Sie die E-Mail-Layout-Komponente per Drag-and-Drop auf einer leeren Arbeitsfläche. Diese Methode eignet sich am besten zum Erstellen neuer Vorlagen oder einmaliger E-Mails.

* [Importieren Sie HTML](#html) in den Code-Editor oder arbeiten Sie nebeneinander mit der visuellen Arbeitsfläche.

  <!-- Full HTML import workflow with .html and .zip uploads is on the Beta roadmap. -->

* [Wählen Sie eine vorhandene ](#select-a-template) aus einer Liste integrierter oder benutzerdefinierter E-Mail-Vorlagen aus. Diese Methode eignet sich am besten für wiederholbare E-Mail-Anwendungsfälle.

<!-- * Upload a design prototype (JPG, PNG, PDF, or Figma export) and have AI Assitant convert it into a responsive HTML email. (Image to HTML (Img2HTML) -->

## E-Mail-Design-Tools

* **Top-Symbolleiste** Speichern, Zurück, Zum Code-Editor wechseln, Steuerelemente in der Vorschau anzeigen.
* **Linke Leiste:** (Spaltenlayouts), Inhalte (Text, Schaltfläche, Bild, Trennlinie, Social, HTML), Fragmente, Vorlagen, Navigationsbaum (DOM-Hierarchie der E-Mail).
* **Arbeitsfläche zentrieren:** WYSIWYG-Editor mit Desktop- und Mobile-Vorschau.
* **Rechte Leiste** Einstellungen und Stile für die aktuell ausgewählte Komponente, einschließlich Inhaltseigenschaften, Hintergrund, Rahmen, Abstand und Personalisierung.

## Best Practices für das E-Mail-Design {#design-best-practices}

Die Befolgung der Best Practices für HTML und CSS hilft bei der Sicherstellung eines konsistenten Renderings auf allen E-Mail-Clients.

| Ansatz | Leitlinien |
| -------- | -------- |
| **Empfohlen** | Statische, tabellenbasierte Layouts ・ HTML-Tabellen und verschachtelte Tabellen ・ Vorlagenbreiten von 600-800 px ・ Einfaches Inline-CSS ・ Web-sichere Schriftarten |
| **Vorsicht bei der Anwendung** | Hintergrundbilder (eingeschränkte Client-Unterstützung) ・ Benutzerdefinierte Webschriftarten (immer eine Ersatzschriftart definieren) ・ Layouts mit mehr als 800 Pixel ・ Imagemaps |
| **Vermeiden** | JavaScript, iFrames oder Flash ・ Eingebettete Audio- oder Videodateien ・ HTML-Formulare ・ Div-basierte Layouts |

>[!NOTE]
>
>E-Mail-Inhalte müssen außerdem die entsprechenden Anforderungen an die digitale Barrierefreiheit erfüllen. Strukturüberschriften sind logisch, bieten alternativen Text für alle Bilder und überprüfen den Farbkontrast sowohl im hellen als auch im dunklen Modus.

## Erstellen einer E-Mail von einer Journey {#email-from-journey}

1. Klicken Sie auf **[!UICONTROL E-Mail bearbeiten]**, um mit dem Schritt E-Mail-Konfiguration fortzufahren.
1. Wählen Sie im nächsten Bildschirm aus der Dropdown-Liste **[!UICONTROL E-Mail-Konfiguration]** eine zuvor erstellte Kanalkonfiguration aus. Es werden nur aktive Konfigurationen aufgelistet.
1. Geben Sie einen Titel für die Aktion (auf der Journey-Arbeitsfläche sichtbar) und einen internen E-Mail-Namen ein.
1. Geben Sie die Betreffzeile ein.
1. Schalten Sie optional **[!UICONTROL URL-Tracking aktivieren]** für diesen E-Mail-Knoten um.
1. Klicken Sie auf **[!UICONTROL Inhalt bearbeiten]**, um den E-Mail-Design-Bereich zu öffnen.

### Der Bildschirm Inhalt bearbeiten . {#edit-content-screen}

In diesem Bildschirm bestätigen Sie die Absenderdetails (übernommen von der Kanalkonfiguration), legen die Betreffzeile fest und öffnen den E-Mail-Design-Bereich, um den Textkörper zu erstellen. Der Preheader wird im E-Mail-Design-Bereich konfiguriert (siehe [Festlegen des Preheaders](#preheader)).

* **Absendername, Absender-E-Mail, BCC:** von der Kanalkonfiguration übernommen. Schreibgeschützt auf diesem Bildschirm.
* **Betreffzeile:** erforderlich. Personalization wird unterstützt.
* **E-Mail-Textkörper bearbeiten:** Öffnet den E-Mail-Design-Bereich.

>[!NOTE]
>
>Die E-Mail-Größe ist gemäß Best Practice des ISP auf 100 KB begrenzt. Prime warnt Sie im Editor, wenn Sie diesen Wert überschreiten. Fehler (fehlender Betreff, fehlender Text, gelöschte Kanalkonfiguration) verhindern, dass der Journey aktiviert wird, bis sie behoben sind.

## Von Grund auf gestalten {#design-from-scratch}

### Schritt für Schritt: Erstellen einer neuen E-Mail {#build-from-scratch}

1. Klicken Sie im E-Mail-Knoten Journey auf **[!UICONTROL Inhalt bearbeiten]** → **[!UICONTROL E-Mail-Textkörper]**.
1. Klicken Sie auf dem Bildschirm E-Mail erstellen auf **[!UICONTROL Von Grund auf gestalten]**.
1. Klicken Sie **[!UICONTROL Bestätigen]**, um eine leere Arbeitsfläche zu öffnen.
1. Ziehen Sie aus der linken Leiste eine **[!UICONTROL Struktur]** (1 Spalte, 1:1, 2:2, n:n Spalte) auf die Arbeitsfläche.
1. Ziehen Sie **[!UICONTROL Inhalt]**-Komponenten in die Spalten der Struktur: Text, Schaltfläche, Bild, Trennlinie, Social, HTML.
1. Klicken Sie auf eine beliebige Komponente auf der Arbeitsfläche, um sie auszuwählen. In der rechten Leiste werden die Registerkarten Einstellungen und Stile angezeigt.
1. Verwenden Sie die **[!UICONTROL Einstellungen]**, um komponentenspezifische Optionen (Textinhalt, Bildquelle, Schaltflächen-URL) zu konfigurieren.
1. Verwenden Sie die **[!UICONTROL Stile]**, um Abstand, Rahmen, Hintergrund, Schriftart und Farbe zu konfigurieren.
1. Verwenden Sie das Symbol **[!UICONTROL Navigationsbaum]** in der linken Leiste, um in einer tief verschachtelten E-Mail zwischen Komponenten zu wechseln.
1. Schalten Sie mithilfe der Symbole in der oberen Symbolleiste zwischen Desktop- und Mobile-Vorschau um.
1. Klicken Sie **[!UICONTROL Speichern]** (oder verwenden Sie das Dropdown-Menü „Speichern“, um weitere Speicheroptionen anzuzeigen).
1. Klicken Sie auf **[!UICONTROL Zurück]**, um zu den E-Mail-Eigenschaften zurückzukehren.

### Verfügbare Inhaltskomponenten {#content-components}

| Komponente | Beschreibung |
| --------- | ----------- |
| **Text** | Rich-Text mit Formatierung (fett, kursiv, Schriftgröße, Farbe, Ausrichtung, Listen, Links). |
| **Schaltfläche** | Anklickbare CTA. Unterstützt Hintergrundfarbe, Rahmen, Abstand, Mauszeigerverhalten und personalisierte URLs. |
| **Bild** | Einfügen aus Marketo Design Studio (Asset-Auswahl). Unterstützt Alt-Text, Ausrichtung, Link- und Klick-Tracking. |
| **Teiler** | Horizontales Lineal mit konfigurierbarer Dicke und Farbe. |
| **Social** | Vorformatierte Social-Media-Symbole mit Link-Konfiguration. |
| **HTML** | Rohdaten des HTML-Blocks für erweiterte Inhalte Nützlich zum Einbetten von handcodiertem Markup. |

### Strukturen und Spalten-Layouts {#structures}

Strukturen definieren das Spaltenraster der E-Mail. Zu den verfügbaren Strukturen gehören: 1 Spalte, 1:1 (zwei gleiche Spalten), 1:2 / 2:1 (asymmetrische zwei Spalten), 1:1:1 (drei gleiche Spalten) und n:n (benutzerdefinierte mehrere Spalten). Verwenden Sie Strukturen, um zu steuern, wie Inhalte auf Mobilgeräten wiederfließen - die meisten Strukturen reduzieren sich auf schmalen Bildschirmen standardmäßig auf eine Spalte.

>[!TIP]
>
>Halten Sie Ihre E-Mail-Struktur einfach. Zwei- oder dreispaltige Layouts sorgen für konsistentes Rendering auf allen E-Mail-Clients (insbesondere Outlook und Gmail). Tief verschachtelte Strukturen können unvorhersehbar gerendert werden.

### Festlegen des Preheaders {#preheader}

Der Preheader ist der Textabschnitt, der in der Vorschau des Posteingangs nach der Betreffzeile angezeigt wird. In Prime wird der Preheader auf der visuellen Arbeitsfläche im E-Mail-Design-Bereich konfiguriert - nicht auf dem Bildschirm mit den E-Mail-Eigenschaften neben der Betreffzeile.

1. Öffnen Sie die E-Mail im E-Mail-Design-Bereich.
1. Suchen Sie auf der Arbeitsfläche den Bereich Preheader oben im E-Mail-Textkörper.
1. Klicken Sie in den Textbereich des Preheaders, und geben Sie Ihre Preheader-Kopie ein.
1. Wenden Sie mithilfe der Rich-Text-Steuerelemente nach Bedarf Formatierungs- und Personalisierungs-Token an.
1. Klicken Sie auf **[!UICONTROL Speichern]**.

>[!TIP]
>
>Halten Sie den Preheader zwischen 40 und 100 Zeichen lang. Sie sollte die Betreffzeile ergänzen (nicht wiederholen) und dem Empfänger einen zusätzlichen Grund geben, die E-Mail zu öffnen.

## Arbeiten mit Vorlagen {#templates}

Vorlagen sind wiederverwendbare E-Mail-Layouts. Sie beschleunigen die E-Mail-Erstellung, erzwingen die Markenkonsistenz und erleichtern die Zusammenarbeit im Team.

### Vorlagentypen

* **Beispielvorlagen (Out-of-the-Box).** Rund 20 vorgefertigte Vorlagen für gängige Anwendungsfälle (Account-basierte Kontaktaufnahme, Ereigniseinladungen, Pflege, Produktankündigungen). Sofort für jeden Kunden verfügbar.
* **Gespeicherte Vorlagen (benutzerdefiniert).** Von Ihrem Team erstellte Vorlagen - entweder von Grund auf neu unter **[!UICONTROL Content-Management]** → **[!UICONTROL Vorlagen]** oder über eine vorhandene E-Mail mithilfe der Option „Als Vorlage speichern“ gespeichert.

### Erstellen einer E-Mail aus einer Vorlage {#create-from-template}

1. Klicken Sie im E-Mail-Knoten Journey auf **[!UICONTROL Inhalt bearbeiten]** → **[!UICONTROL E-Mail-Textkörper]**.
1. Auf dem Bildschirm E-Mail erstellen ist **[!UICONTROL Registerkarte]** Beispielvorlagen“ standardmäßig ausgewählt.
1. Durchsuchen Sie die Galerie. Verwenden Sie das Suchfeld, um nach Name oder Kategorie zu filtern.
1. Wechseln Sie zur Registerkarte **[!UICONTROL Gespeicherte Vorlagen]**, um die von Ihrem Team erstellten Vorlagen anzuzeigen.
1. Klicken Sie auf eine Vorlagenminiatur, um sie in der Vorschau anzuzeigen.
1. Klicken Sie **[!UICONTROL Diese Vorlage verwenden]**, um sie anzuwenden. Der Vorlageninhalt wird auf der Arbeitsfläche im E-Mail-Design-Bereich geöffnet.
1. Text, Bilder und Links anpassen. Die von der Vorlage geerbte Struktur kann wie eine neue E-Mail geändert werden.
1. Klicken Sie auf **[!UICONTROL Speichern]** → **[!UICONTROL Zurück]**, um zu den E-Mail-Eigenschaften zurückzukehren.

### Erstellen einer wiederverwendbaren Vorlage {#create-reusable-template}

1. Navigieren Sie zu **[!UICONTROL Content-]**→ **[!UICONTROL Vorlagen]**.
1. Klicken Sie auf **[!UICONTROL Vorlage erstellen]**.
1. Geben Sie einen Namen und eine Beschreibung ein. Wählen Sie **[!UICONTROL Kanal]** E-Mail“ aus.
1. Klicken Sie auf **[!UICONTROL Erstellen]**. Der E-Mail-Design-Bereich wird zur Bearbeitung geöffnet.
1. Erstellen Sie die Vorlage (von Grund auf neu, aus einer vorhandenen Vorlage oder durch Einfügen von HTML).
1. Aktivieren Sie optional **[!UICONTROL Governance-Einstellungen]**:
   * Struktur- und Inhaltsbearbeitung zulassen - Steuert, ob E-Mail-Autoren die Struktur der Vorlage oder nur ihren Inhalt ändern können.
   * Spezifische Komponenten sperren - Machen Sie einzelne Komponenten bei Verwendung in einer E-Mail schreibgeschützt.
1. Klicken Sie auf **[!UICONTROL Speichern]**. Die Vorlage ist jetzt für alle Benutzer im Katalog Gespeicherte Vorlagen verfügbar.

### Speichern einer E-Mail als Vorlage {#save-as-template}

1. Öffnen Sie eine vorhandene E-Mail im E-Mail-Design-Bereich.
1. Klicken Sie im Dropdown **[!UICONTROL Menü]** Speichern“ auf **[!UICONTROL Als Vorlage speichern]**.
1. Geben Sie einen Namen und eine Beschreibung ein.
1. Konfigurieren Sie optional Governance-Einstellungen.
1. Klicken Sie auf **[!UICONTROL Speichern]**.

>[!NOTE]
>
>Gespeicherte Vorlagen und ihre E-Mail-Inhalte sind unabhängig. Beim Bearbeiten einer Vorlage werden die daraus erstellten E-Mails nicht rückwirkend aktualisiert. Um Änderungen auf viele E-Mails zu übertragen, verwenden Sie visuelle Fragmente anstelle von Vorlagen.

## Visuelle Fragmente {#visual-fragments}

Ein visuelles Fragment ist ein wiederverwendbarer Inhaltsblock - eine Kopfzeile, eine Fußzeile, eine CTA, ein Haftungsausschluss, eine Reihe von Social-Media-Links -, der in viele E-Mails eingefügt werden kann. Wenn Sie ein Fragment aktualisieren, wird die Änderung automatisch auf jede E-Mail übertragen, die es verwendet. Fragmente sind die empfohlene Methode, um Markenkonsistenz zu erzwingen und Inhaltsaktualisierungen zu zentralisieren.

### Erstellen eines visuellen Fragments {#create-fragment}

1. Navigieren Sie zu **[!UICONTROL Content-]**→ **[!UICONTROL Fragments]**.
1. Klicken Sie **[!UICONTROL Fragment erstellen]**.
1. Wählen Sie **[!UICONTROL Visuelles Fragment]** als Typ aus. Geben Sie einen Namen und eine Beschreibung ein.
1. Klicken Sie auf **[!UICONTROL Erstellen]**. Der E-Mail-Design-Bereich wird zur Bearbeitung geöffnet.
1. Ziehen Sie Strukturen und Inhaltskomponenten auf die Arbeitsfläche, um das Fragment zu erstellen (z. B. eine 1-spaltige Struktur mit einem Logobild, einer Überschrift und einer Liste mit Navigations-Links).
1. (Optional) Markieren Sie Felder als **[!UICONTROL Bearbeitbar]** damit sie pro Verwendung angepasst werden können:
   * Wählen Sie eine Komponente aus und öffnen Sie dann in der rechten Leiste den Abschnitt **[!UICONTROL Bearbeitbare Felder]**.
   * Fügen Sie Felder mit Standardwerten hinzu (z. B. ein Bildquellenfeld mit einer standardmäßigen Logo-URL oder ein Textfeld mit einer standardmäßigen Überschrift).
   * E-Mail-Autoren, die das Fragment verwenden, können diese Felder überschreiben, ohne die Struktur des Fragments aufzuheben.
1. Klicken Sie auf **[!UICONTROL Speichern]**.

### Einfügen eines Fragments in eine E-Mail {#insert-fragment}

1. Öffnen Sie die E-Mail im E-Mail-Design-Bereich.
1. Klicken Sie in der linken Leiste auf **[!UICONTROL Fragmente]**.
1. Suchen Sie nach dem gewünschten Fragment.
1. Ziehen Sie das Fragment an die gewünschte Position auf die Arbeitsfläche.
1. Wenn das Fragment bearbeitbare Felder enthält, konfigurieren Sie die Werte in der rechten Leiste.
1. Klicken Sie auf **[!UICONTROL Speichern]**.

>[!TIP]
>
>Verwenden Sie Fragmente für Inhalte, die in allen E-Mails konsistent bleiben müssen - in Ihrer Kopfzeile, Ihrer legalen Fußzeile, der Symbolleiste mit Social-Media-Links, dem Abmelde-Block. Wenn die Rechtsabteilung den Haftungsausschluss aktualisiert, ändert man ein Fragment und jede E-Mail wird aktualisiert.

## Personalisierung {#personalization}

Prime verwendet die Handlebars-Syntax für die Personalisierung. Token werden zum Zeitpunkt des Versands durch Werte aus den Profildaten jedes Empfängers ersetzt.

### Wo Sie personalisieren können

* **Betreffzeile** - Häufigster Personalisierungspunkt.
* **Preheader** - auf der visuellen Arbeitsfläche festgelegt; unterstützt Profilattribut-Token.
* **E-Mail-Text** - Vornamen und andere Profilattribute, die inline eingefügt wurden.
* **Schaltflächen-URLs** — Parameter für das Anhängen pro Empfänger.

>[!NOTE]
>
>In dieser Version sind nur Profilattribute im Personalization-Editor verfügbar.

### Einfügen eines Personalisierungs-Tokens {#insert-token}

1. Klicken Sie im Bereich „E-Mail-Design“ (oder im Bildschirm mit den E-Mail-Eigenschaften für die Betreffzeile) auf das Feld, in das Sie ein Token einfügen möchten.
1. Klicken Sie auf das Personalisierungssymbol (häufig mit **[!UICONTROL Personalisierungsdialog öffnen]** oder **[!UICONTROL Ausdruck hinzufügen]**).
1. Durchsuchen Sie im Personalisierungsdialog die Schemastruktur auf der linken Seite. Profilattribute (Vorname, Nachname, E-Mail, Stellenbezeichnung und andere Profilfelder) werden aufgelistet.
1. Attribut auswählen. Prime fügt den entsprechenden Handlebars-Ausdruck ein - z. B. `{{profile.firstName}}`.
1. Fügen Sie einen Fallback-Wert hinzu, um fehlende Daten zu verarbeiten: `{{profile.firstName | default: "there"}}`.
1. Klicken Sie **[!UICONTROL Bestätigen]** oder **[!UICONTROL Einfügen]**. Der Ausdruck wird inline im Feld angezeigt.

### Häufige Personalisierungsmuster {#personalization-patterns}

Verwenden Sie Handlebars-Ausdrücke wie den folgenden (Personalisierung verwendet dieselbe Syntax, die unter [Schritt für Schritt: Einfügen eines Personalisierungs-Tokens) beschrieben ](#insert-token):

* **`{{profile.lastName}}`** - Fügen Sie den Nachnamen der Empfängerin bzw. des Empfängers ein.
* **`{{profile.jobTitle}}`** - Referenzieren Sie die Stellenbezeichnung des Empfängers in der Textkörper-Kopie.
* **`{{profile.firstName}}, ready to take the next step?`** - Kombinieren Sie Token und statischen Text inline.

Für eine Grußformel mit Vorname und einem Fallback, wenn der Wert fehlt, verwenden Sie den `default` Helper, wie in den vorherigen Personalisierungsschritten gezeigt (z. B. Vorname mit `"there"`).

### Handlebars-Helfer {#handlebars-helpers}

Über `default` hinaus enthält der Personalisierungseditor integrierte Handlebars-Helfer für bedingte Logik, Textumwandlung und Datumsformatierung. Verwenden Sie den Funktions-Browser des Editors, um verfügbare Helper zu erkunden und sie mit der richtigen Syntax einzufügen.

>[!TIP]
>
>Geben Sie im E-Mail-Design-Bereich `{{` direkt in ein beliebiges Textfeld ein, um eine Dropdown-Liste mit automatischer Inline-Vervollständigung mit verfügbaren Profilattributen zu erstellen. Es ist nicht erforderlich, das vollständige Personalisierungsdialogfeld für Schnelleinfügungen zu öffnen.

### KI-unterstützte Ausdrücke {#ai-personalization}

Der KI-Assistent im Personalisierungseditor kann Handlebars-Ausdrücke aus einer einfachen Beschreibung generieren, die Funktion eines vorhandenen Ausdrucks erklären und potenzielle Probleme identifizieren. Verwenden Sie sie, um die Erstellung von Ausdrücken zu beschleunigen, insbesondere für bedingte Logik oder Helper zur Datumsformatierung.

## Hinzufügen von Assets aus Marketo Design Studio {#marketo-assets}

Prime stellt Ihre vorhandenen Marketo Design Studio-Assets im E-Mail-Design-Bereich zur Verfügung. Sie können diese Bilder direkt über die Asset-Auswahl durchsuchen und in Ihre E-Mails einfügen.

>[!IMPORTANT]
>
>Die Asset-Verfügbarkeit in Prime basiert auf einer **Kopie** Assets aus Marketo Design Studio. Das erneute Hochladen oder Ändern von Assets in Marketo nach der ersten Kopie **nicht** in Prime angezeigt. Bild-Uploads direkt in Prime werden in dieser Version ebenfalls nicht unterstützt. Die native Verwaltung digitaler Assets in Prime - einschließlich Hochladen, Ordnernavigation, Suche und Bildbearbeitung - ist Teil des Beta-Umfangs.

### Unterstützte Dateitypen {#asset-file-types}

* **Vollständig unterstützt (in der Auswahl sichtbar, inline einbettbar):** JPG, PNG, GIF, WebP.
* **Zugänglich mit Einschränkungen:** SVG (mit einer Warnung, dass einige E-Mail-Clients SVG nicht rendern).
* **In dieser Version nicht unterstützt:** TIFF, PDF, DOCX, XLSX, PPTX, CSS, JS, HTML, TXT, Binärdateien, PSD, AI, INDD.

### Einfügen eines Bildes aus Marketo Design Studio {#insert-image}

1. Ziehen Sie im E-Mail-Design-Bereich eine Inhaltskomponente **[!UICONTROL Bild]** auf die Arbeitsfläche (oder klicken Sie auf ein vorhandenes Bild, um sie zu ersetzen).
1. Klicken Sie in der rechten Leiste auf **[!UICONTROL Marketo Engage Assets]**.
1. Die Asset-Auswahl wird geöffnet. Ordner durchsuchen oder nach Dateinamen suchen.
1. Wählen Sie das gewünschte Asset aus.
1. Klicken Sie auf **[!UICONTROL Auswählen]**. Das Bild wird aus der in Prime verfügbaren Kopie des Assets in Ihre E-Mail eingefügt.
1. Konfigurieren Sie in der rechten Leiste:
   * Alt-Text (empfohlen für Barrierefreiheit und für Clients, die Bilder standardmäßig blockieren).
   * Ausrichtung.
   * Link-Ziel - Das Bild kann angeklickt werden.
1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Dunkler Modus {#dark-mode}

Das Dark-Mode-Rendering wird über CSS- `prefers-color-scheme` Medienabfragen unterstützt. Die E-Mail-Design-Tools umfassen eine Vorschau des Dunkelmodus und Optionen zum Definieren benutzerdefinierter Stile für unterstützende E-Mail-Clients. So können Sie überprüfen, ob der Text lesbar bleibt, Logos sichtbar sind und Markenfarben einen dunklen Hintergrund aufweisen.

Ausführliche Anleitungen zur Vorschau, zur Konfiguration benutzerdefinierter Einstellungen für den Dunkelmodus, zur Unterstützung des E-Mail-Clients und zu Best Practices für Tests finden Sie unter [Dunkelmodus für E-Mail-Inhalte](./email-dark-mode.md).

## Validieren von E-Mail-Inhalten {#validation}

Bevor Ihr Journey aktiviert werden kann, muss der E-Mail-Inhalt gültig sein. Prime zeigt Warnhinweise auf Inhaltsebene in der E-Mail und auf der Journey-Arbeitsfläche an. In diesem Abschnitt werden die Warnhinweise beschrieben, die möglicherweise angezeigt werden, und wie Sie sie beheben können.

### Allgemeine Warnhinweise zu Inhalten und deren Lösung {#content-alerts}

| Warnhinweis | Bedeutung | Beheben von Problemen |
| ----- | ------------- | -------------- |
| **Betreffzeile fehlt** | Das Feld Betreffzeile ist leer. | Öffnen Sie die E-Mail und geben Sie eine Betreffzeile auf dem Bildschirm Inhalt bearbeiten ein. Personalization-Token sind zulässig, das Feld darf jedoch nicht leer sein. |
| **E-Mail-Text ist leer** | Die Arbeitsfläche im E-Mail-Design-Bereich enthält keinen Inhalt. | Klicken Sie auf **[!UICONTROL E-Mail-Text bearbeiten]**, um den E-Mail-Design-Bereich zu öffnen. Ziehen Sie mindestens eine Struktur - und eine Inhaltskomponente auf die Arbeitsfläche und klicken Sie dann auf Speichern . |
| **Kanalkonfiguration nicht ausgewählt** | Für den E-Mail-Knoten wurde keine E-Mail-Konfiguration ausgewählt. | Wählen Sie im E-Mail-Eigenschaftenbildschirm in der Dropdown-Liste **[!UICONTROL E-Mail-Konfiguration]** eine Konfiguration für den aktiven Kanal aus. |
| **Kanalkonfiguration gelöscht** | Die zuvor ausgewählte Kanalkonfiguration wurde gelöscht oder ist nicht mehr aktiv. | Öffnen Sie die E-Mail-Eigenschaften und wählen Sie eine andere aktive Kanalkonfiguration aus. Wenn keine verfügbar sind, muss ein Administrator eine erstellen oder reaktivieren. |
| **E-Mail-Größe überschreitet 100 KB** | Die Gesamtgröße der E-Mails (HTML, Inline-CSS, kodierte Inhalte) ist größer als die Obergrenze von 100 KB für Best Practices beim ISP. | Verringern der E-Mail-Größe: Ersetzen Sie große Inline-Bilder durch extern gehostete Bilder aus Marketo Design Studio, entfernen Sie nicht verwendetes Inline-CSS und vereinfachen Sie verschachtelte Strukturen. |
| **Nicht aufgelöstes Personalisierungs-Token** | Ein Handlebars-Token verweist auf ein Profilattribut ohne Fallback, und bei einigen Empfängern kann das Attribut fehlen. | Fügen Sie ein Fallback mit dem Handlebars-`default`-Helper hinzu, wie in [Personalization beschrieben](#personalization). Alternativ können Sie die Journey-Zielgruppe auf Profile beschränken, bei denen das Attribut garantiert ist. |
| **Bild nicht geladen** | Eine Bildkomponente verweist auf ein Asset, das nicht mehr verfügbar ist. | Klicken Sie auf das Bild, öffnen Sie die Asset-Auswahl und wählen Sie das Asset in Marketo Design Studio erneut aus. |

### Überprüfen und Auflösen von Warnhinweisen {#resolve-alerts}

1. Öffnen Sie die Journey mit dem E-Mail-Knoten. E-Mail-Knoten mit nicht aufgelösten Warnhinweisen werden auf der Arbeitsfläche mit einem roten Badge gekennzeichnet.
1. Klicken Sie auf den E-Mail-Knoten, um die Eigenschaftenleiste zu öffnen.
1. Lesen Sie den Abschnitt **[!UICONTROL Warnhinweise]** in der Eigenschaftenleiste. Jeder Warnhinweis ist mit dem Feld oder Bildschirm verknüpft, in dem das Problem behoben werden kann.
1. Lösen Sie die einzelnen Warnhinweise nacheinander auf, z. B. geben Sie eine fehlende Betreffzeile ein, wählen Sie eine Kanalkonfiguration aus oder öffnen Sie den E-Mail-Design-Bereich, um den Inhalt zu beheben.
1. Klicken Sie nach dem Auflösen aller Warnhinweise auf **[!UICONTROL Speichern]** im E-Mail-Knoten.
1. Bestätigen Sie, dass das rote Abzeichen auf dem E-Mail-Knoten gelöscht wird.

>[!NOTE]
>
>Warnhinweise müssen gelöscht werden, bevor die Journey fortgesetzt werden kann. Warnungen sind nicht blockierend, sollten jedoch überprüft werden (z. B. kann eine E-Mail, die ein Token ohne Fallback verwendet, bei einigen Empfängern mit leeren Werten gerendert werden).
