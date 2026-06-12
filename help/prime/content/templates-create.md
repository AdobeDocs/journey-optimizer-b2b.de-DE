---
title: E-Mail-Vorlagen erstellen
description: Erfahren Sie, wie Sie E-Mail-Vorlagen in Journey Optimizer B2B Prime erstellen - von Grund auf neu entwerfen, eine E-Mail von einer Journey als Vorlage speichern oder ein Design-Bild in eine E-Mail-Vorlage konvertieren.
badgeBeta: label="Beta" type="informative" tooltip="Diese Funktion ist Teil einer eingeschränkten Beta-Version."
source-git-commit: 2f19137465c71f2292d37bea5786533b1df6e286
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 1%

---


# E-Mail-Vorlagen erstellen

Sie haben drei Möglichkeiten, um eine E-Mail-Vorlage in [!DNL Journey Optimizer B2B Edition Prime] zu erstellen:

* **Von Grund auf gestalten** - Erstellen Sie eine neue Vorlage in der Vorlagenbibliothek mithilfe des visuellen E-Mail-Design-Bereichs.
* **Von einer Journey-E-Mail speichern** - Speichern Sie eine E-Mail, die Sie auf einer Journey verfasst haben, als wiederverwendbare Vorlage.
* **Bild konvertieren** - Laden Sie ein Designbild hoch und verwenden Sie generative KI, um es in eine bearbeitbare E-Mail-Vorlage zu konvertieren.

>[!NOTE]
>
>In dieser Beta-Version werden nur E-Mail-Vorlagen unterstützt.

## Erstellen einer neuen Vorlage {#design-from-scratch}

1. Navigieren Sie **[!UICONTROL Content-Management]** > **[!UICONTROL Vorlagen]**.
1. Klicken Sie auf **[!UICONTROL Vorlage erstellen]**.
1. Geben Sie einen **[!UICONTROL Vorlagennamen“]** optional &quot;**[!UICONTROL &quot;]**.
1. Optional können Sie Tags hinzufügen, um die Vorlage zu kategorisieren.
1. Klicken Sie **[!UICONTROL Erstellen]**, um den E-Mail-Design-Bereich zu öffnen.
1. Entwerfen Sie das E-Mail-Layout mit Strukturen und Inhaltskomponenten. Eine vollständige Übersicht der verfügbaren Tools finden Sie unter [E-Mail-Authoring](email-authoring.md).
1. Optional können Sie [Inhaltssperre](template-content-locking.md) konfigurieren, um zu beschränken, welche Teile der Vorlagen von Vorlagenautoren bearbeitet werden können, wenn sie auf einer Journey verwendet werden.
1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Speichern einer Journey-E-Mail als Vorlage {#save-as-template}

Wenn Sie eine E-Mail auf einer Journey entwerfen, die Sie wiederverwenden möchten, speichern Sie sie direkt im E-Mail-Design-Bereich in der Vorlagenbibliothek.

1. Öffnen Sie im E-Mail-Design das **[!UICONTROL Speichern]** Dropdown-Menü oben im Editor.
1. Wählen **[!UICONTROL Als Inhaltsvorlage speichern]**.
1. Geben Sie einen **[!UICONTROL Vorlagennamen“]** optional &quot;**[!UICONTROL &quot;]**.
1. Fügen Sie optional Tags hinzu und konfigurieren Sie [Inhaltssperrung](template-content-locking.md).
1. Klicken Sie auf **[!UICONTROL Speichern]**.

Die ursprüngliche Journey-E-Mail ist nicht betroffen. Die gespeicherte Vorlage ist in der Vorlagenbibliothek für alle Benutzer in der Sandbox verfügbar.

## Konvertieren eines Bildes in eine Vorlage {#image-to-template}

[!DNL Journey Optimizer B2B Edition Prime] können ein statisches Bild - z. B. ein Mockup aus Figma oder Photoshop - mithilfe von generativer KI in eine bearbeitbare E-Mail-Vorlage konvertieren. Dadurch entfällt die Notwendigkeit, Layouts aus Design-Dateien manuell neu zu erstellen.

### Anforderungen

Bevor Sie beginnen:

* Ihr Unternehmen muss das Generative AI-Addendum mit Adobe unterzeichnet haben.
* Sie müssen über die Berechtigung **[!UICONTROL Inhalt generieren]** zusätzlich zu **[!UICONTROL Inhaltsvorlagen verwalten]** verfügen.
* Die Bilddatei muss den folgenden Spezifikationen entsprechen:
   * Format: JPEG (.jpg, .jpeg) oder PNG (.png)
   * Maximale Dateigröße: 10 MB
   * Empfohlene Breite: 600-800 Pixel
   * Klare, hochwertige Bilder mit lesbarem Text und ausgeprägten visuellen Elementen

>[!IMPORTANT]
>
>Das Bild darf keine personenbezogenen oder vertraulichen Daten enthalten.

### Konvertieren eines Bildes

1. Navigieren Sie **[!UICONTROL Content-Management]** > **[!UICONTROL Vorlagen]**.
1. Klicken Sie **[!UICONTROL der Kopfzeile auf]** Bild in Vorlage konvertieren“.
1. Geben Sie einen **[!UICONTROL Vorlagennamen“]** optional &quot;**[!UICONTROL &quot;]**.
1. Wählen Sie optional ein **[!UICONTROL Markendesign]**, um die Farben, Schriftarten und Abstände Ihrer Marke auf die generierte Ausgabe anzuwenden.
1. Laden Sie das Bild per Drag-and-Drop oder im Datei-Browser hoch.
1. Vergewissern Sie sich, dass das Bild keine personenbezogenen Daten enthält.
1. Lesen und akzeptieren Sie die Adobe Generative AI-Benutzerrichtlinien (nur beim ersten Mal).
1. Klicken Sie **[!UICONTROL Konvertieren]**.

   Die Konvertierung wird in der Regel innerhalb von fünf Minuten abgeschlossen. Komplexe oder große Bilder können bis zu zehn Minuten dauern. Sie können die Seite verlassen. Der Vorgang wird im Hintergrund fortgesetzt.

1. Wenn die Konvertierung abgeschlossen ist, klicken Sie auf den Namen der Vorlage, um die generierten Inhalte in der Vorschau anzuzeigen und zu bearbeiten.

>[!NOTE]
>
>Das Ergebnis wird nicht automatisch angezeigt. Aktualisieren Sie die Seite oder kehren Sie zur Vorlagenbibliothek zurück, um die fertige Vorlage anzuzeigen.

### Nach Konvertierung bearbeiten

Die konvertierte Vorlage wird im E-Mail-Design-Bereich als vollständig bearbeitbare E-Mail geöffnet. Verwenden Sie die standardmäßigen Design-Tools für Folgendes:

* Bearbeiten von Text und Hinzufügen [Personalisierungs](email-authoring.md#personalization)Token.
* Bilder aktualisieren oder ersetzen und Links hinzufügen.
* Farben, Schriftarten und Abstände anpassen.
* Hinzufügen, Entfernen oder Neuanordnen von Inhaltskomponenten.
* Konfigurieren Sie [Inhaltssperrung](template-content-locking.md).

>[!IMPORTANT]
>
>Die generative KI erzeugt statische HTML basierend auf dem visuellen Bild. Überprüfen Sie den gesamten Text auf Genauigkeit und fügen Sie nach der Konvertierung Personalisierung, dynamische Inhalte und Tracking manuell hinzu.

Die konvertierte Vorlage wird nach Abschluss der Konvertierung automatisch in der Vorlagenbibliothek gespeichert.

### Tipps für optimale Ergebnisse

Verwenden Sie die folgenden Richtlinien, um die besten Ergebnisse aus der Konvertierung von Bildern in Vorlagen zu erzielen:

**Vor der Konvertierung:**

* Verwenden Sie die Version mit der höchsten Auflösung Ihrer Design-Datei.
* Entwerfen Sie mit standardmäßigen E-Mail-Breiten (600-800 Pixel) und fügen Sie das vollständige Layout - Kopf- und Fußzeile - in ein einziges Bild ein.
* Achten Sie auf einen ausreichenden Kontrast zwischen Text und Hintergrund und verwenden Sie lesbare Schriftgrößen.

**Design für genaue Konvertierung:**

* Verwenden Sie einfache, gut strukturierte Layouts mit klarer Trennung zwischen Abschnitten.
* Folgen Sie standardmäßigen E-Mail-Mustern - Kopfzeile, Hauptteil, Aktionsaufrufe, Fußzeile - anstelle von komplexen mehrschichtigen Designs.
* Halten Sie visuelle Elemente getrennt, damit die KI Strukturgrenzen korrekt identifizieren kann.

**Nach der Konvertierung:**

* Testen des Renderings auf E-Mail-Clients und Geräten, bevor die Vorlage auf einer Journey verwendet wird.
* Überprüfen Sie die Ausrichtung anhand von Markenfarben, Schriftarten und Stilrichtlinien.
* Überprüfen und verbessern Sie die Barrierefreiheit, einschließlich Bild-Alt-Text.
