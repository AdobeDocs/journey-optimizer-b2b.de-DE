---
title: Web-Erlebnisdesign
description: Entwerfen von Web-Erlebnissen mit visuellen und nicht visuellen Editoren - Hinzufügen von Änderungen, Verwalten von Inhaltsaktualisierungen, Aktivieren von Klick-Tracking und Personalisieren von Inhalten in Journey Optimizer B2B edition.
feature: Content Design Tools, Channels
role: User
badgeBeta: label="Beta" type="informative" tooltip="Diese Funktion befindet sich derzeit in einer eingeschränkten Beta-Version"
source-git-commit: d01f4c14f72ebf78b10e4fc6691df42707bedb47
workflow-type: tm+mt
source-wordcount: '2333'
ht-degree: 4%

---

# Web-Erlebnisdesign

Nachdem Sie [ein Web-Erlebnis](./web-experiences.md#create-a-web-experience) erstellt haben, definieren Sie im Bereich für das Inhalts-Design die Änderungen, die Sie auf Ihre Web-Seiten anwenden möchten.

>[!BEGINSHADEBOX]

**Voraussetzungen**

Bevor Sie Web-Erlebnisse entwerfen können, stellen Sie sicher, dass die folgenden Anforderungen erfüllt sind:

* Ein Produktadministrator hat einen oder mehrere Web-Kanäle konfiguriert, um die URLs (Seiten) zu definieren, die für ein Web-Erlebnis eingeschlossen werden sollen. Weitere Informationen finden Sie unter [Webkanalkonfigurationen](../admin/configure-channels-web.md).

* Auf Ihrer Website ist [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/js-overview) (`alloy.js`) für die Besucheridentifizierung und Inhaltsbereitstellung implementiert. Adobe Experience Platform Web SDK Version 2.16 oder höher ist erforderlich.

* Sie verfügen über die erforderlichen [Berechtigungen](../admin/user-management.md#b2b-product-permissions) um Web-Erlebnisse auf einer Journey zu erstellen und zu verwalten:
   * _[!UICONTROL Kampagnen]_ > _[!UICONTROL Kampagnen verwalten]_ - Erforderlich zum Hinzufügen oder Aktualisieren eines Web-Personalisierungsaktionsknotens.
   * _[!UICONTROL Kampagnen]_ > _[!UICONTROL Kampagnen anzeigen]_ - Erforderlich zum Anzeigen von Details für Web-Personalisierungsaktionsknoten.

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>Bevor Sie ein Web-Erlebnis entwerfen, stellen Sie sicher, dass Sie die Browser-Erweiterung Adobe Experience Cloud Visual Editing Helper für Ihren Webbrowser installiert haben. Diese Erweiterung ist erforderlich, um Web-Seiten zuverlässig im Web-Erlebnis-Design-Bereich von Journey Optimizer B2B edition zu öffnen, zu erstellen und eine Vorschau davon anzuzeigen.<br/>
>
>Google Chrome und Microsoft Edge sind derzeit die einzigen Browser, die die Erweiterungs- und Authoring-Web-Erlebnisse in Journey Optimizer B2B edition unterstützen. Weitere Informationen finden Sie unter [Installieren der Visual Editing Helper-Erweiterung](./web-experiences.md#install-the-visual-editing-helper-extension).

## Web-Erlebnis-Editor

Journey Optimizer B2B edition bietet zwei Arten von Editoren zum Entwerfen von Web-Änderungen:

| Editor | Beschreibung | Am besten geeignet für |
| ------ | ----------- | -------- |
| [Visual Editor](#visual-editor) | Ein WYSIWYG-Editor (_What You See Is What You Get_), der Ihre Website anzeigt und es Ihnen ermöglicht, Elemente direkt auszuwählen und zu ändern. Dazu ist die Erweiterung [Visual Editing Helper](./web-experiences.md#install-the-visual-editing-helper-extension) in Google Chrome oder Microsoft Edge erforderlich. | Visuelle Änderungen an sichtbaren Seitenelementen wie Text, Bildern, Schaltflächen und Bannern. |
| [Nicht visueller Editor](#non-visual-editor) | Ein Code-basierter Editor zum Anwenden von Änderungen, die nicht über den visuellen Editor vorgenommen werden können. | Targeting von Elementen, die visuell schwer auszuwählen sind, Anwenden erweiterter CSS-Änderungen oder Ändern von ausgeblendeten Elementen. |

Verwenden Sie in den Web-Erlebniseigenschaften die Option **[!UICONTROL Visual Editor]**, um den Editor-Typ zu bestimmen. Aktivieren Sie die Option, um den visuellen Editor zu verwenden, oder deaktivieren Sie sie, um den nicht visuellen Editor zu verwenden.

![Visual Editor-Option aktiviert](./assets/web-experience-design-visual-editor-option.png){width="400"}

## Visueller Editor {#visual-editor}

>[!CONTEXTUALHELP]
>id="ajo-b2b_web_experience_browse"
>title="Verwenden des Durchsuchen-Modus"
>abstract="In diesem Modus können Sie zur Seite navigieren, die Sie für die ausgewählte Webkanal-Konfiguration personalisieren möchten."

Der visuelle Editor lädt die Web-Seiten in einem iFrame, in dem Sie Elemente auswählen und Änderungen direkt in der Seitenvorschau anwenden können. Führen Sie die folgenden Schritte aus, um den visuellen Editor zum Entwerfen Ihres Web-Erlebnisses zu verwenden:

1. Klicken Sie auf _[!UICONTROL Registerkarte]_ Inhalt“ auf der Seite mit den Web-Erlebnisdetails **[!UICONTROL Web-Erlebnis bearbeiten]** im rechten Bereich.

   Der visuelle Editor lädt Ihre Website basierend auf der Konfiguration des Web-Kanals.

   ![Visual Web Experience Editor](./assets/web-experience-design-visual-editor.png){width="800" zoomable="yes"}

1. Klicken Sie bei Bedarf **[!UICONTROL oben rechts auf]** Durchsuchen“ und verwenden Sie die Site-Navigationsleiste, um die spezifische Seite zu laden, die Sie ändern möchten.

   Sie können auch die Seiten-URL in das Feld oben eingeben.

   >[!NOTE]
   >
   >Stellen Sie sicher, dass die geladene Seite den in Ihrer Web-Kanal-Konfiguration definierten URL-Mustern entspricht. Klicken Sie **[!UICONTROL oben rechts auf]** Konfigurationsdetails anzeigen“, um die URL- oder Seitenabgleichregeln für die ausgewählte Webkanal-Konfiguration anzuzeigen.

   ![Durchsuchen-Modus im visuellen Editor](./assets/web-experience-design-visual-editor-browse.png){width="700" zoomable="yes"}

   <!-- If the web channel configuration is defined using page matching rules, use the left and right arrows to sequence through the matched pages -- right now these buttons don't do anything -->

   Klicken Sie **[!UICONTROL oben]** auf „Design“, um die Seite in den Design-Bereich zu laden.

1. Um zu definieren, wie die angezeigte Seite für das Web-Erlebnis geändert werden soll, können Sie:

   * [Neue Komponenten einfügen](#insert-new-components) (Trennzeichen, HTML, Bild, Überschrift, Absatz oder Link) zur Seite für das Web-Erlebnis.

   * Wählen Sie ein vorhandenes Element auf der Seite aus, z. B. ein Bild, eine Schaltfläche, einen Absatz, Text, einen Container, eine Überschrift oder einen Link, und [ändern Sie es für das Web-Erlebnis](#modify-elements).

   * [Klick-Tracking hinzufügen](#click-tracking-for-web-experiences) für Elemente, um die Interaktion zu messen und Erkenntnisse zu gewinnen.

1. Wiederholen Sie Schritt 2, um andere Seiten zu laden, die Sie in das Web-Erlebnis einbeziehen möchten, und wiederholen Sie Schritt 3, um die Seitenänderungen zu definieren.

1. [Überprüfen Sie Ihre &#x200B;](#manage-modifications) und nehmen Sie die erforderlichen Anpassungen vor.

1. Wenn Ihre Änderungen abgeschlossen sind, klicken Sie auf den linken Pfeil über dem Editor, um zu den Eigenschaften des Web-Erlebnisses zurückzukehren.

### Elemente ändern

Klicken Sie auf ein Element auf der angezeigten Seite, um es auszuwählen. Ein blauer Rahmen zeigt das ausgewählte Element an, und eine kontextuelle Symbolleiste mit Änderungsoptionen wird angezeigt.

![Element zum Ändern auswählen](./assets/web-experience-design-select-element.png){width="700" zoomable="yes"}

Die Symbolleistenoptionen hängen vom ausgewählten Komponententyp ab:

| Aktion | Beschreibung |
| ------ | ----------- |
| **[!UICONTROL Textoptionen]** | Ändern Sie die Klasse oder den Textstil des ausgewählten Elements. |
| **[!UICONTROL Bild auswählen]** | Ersetzen Sie die Bildquelle oder fügen Sie dem Element ein Bild hinzu. |
| **[!UICONTROL Link bearbeiten/Link hinzufügen]** | Ändern oder Hinzufügen einer Link-URL. |
| **[!UICONTROL Anordnen]** | Verschiebt das ausgewählte Element innerhalb der Anzeige nach vorn oder hinten. |
| **[!UICONTROL Hinzufügen von Personalisierung]** | Einfügen von Personalisierung. |
| **[!UICONTROL Klick-Tracking-Element]** | Klick-Tracking für das Element hinzufügen. |
| **[!UICONTROL Löschen]** | Das ausgewählte Element von der Seite entfernen. |

Für ein ausgewähltes Element ändern sich die Eigenschaften im rechten Bereich, um die verfügbaren Stile und Aktionen widerzuspiegeln. Klicken Sie auf ein Aktionssymbol oben im Bedienfeld, um das ausgewählte Element zu duplizieren, zu verfolgen, zu löschen oder auszublenden.

![Klicken Sie auf ein Aktionssymbol für das ausgewählte Element](./assets/web-experience-design-visual-editor-element-properties-icons.png){width="300"}

+++Textelemente

1. Ein Textelement auf der Seite auswählen.

1. Geben Sie einen neuen Textinhalt ein, oder wählen Sie eine Textzeichenfolge aus und geben Sie den Ersatztext ein.

1. (Optional) Verwenden Sie die [Textformatierungsoptionen](./content-components.md#text) z. B. fett, kursiv und Ausrichtung.

1. Klicken Sie auf eine Stelle außerhalb des Textelements, um die Änderung anzuwenden.

Weitere Informationen zu Textformatierungsoptionen für Textkomponenten finden Sie unter [Inhaltskomponenten](./content-components.md#text).

+++

+++Bildelemente

1. Wählen Sie ein Bildelement auf der Seite aus.

1. Klicken Sie auf _[!UICONTROL Symbol]_ Bild auswählen“ in der kontextuellen Symbolleiste oder im rechten Bedienfeld.

1. Suchen Sie ein Bild aus Ihrer Asset-Bibliothek und wählen Sie es aus.

1. Verwenden Sie bei [&#x200B; die Optionen für &#x200B;](./content-components.md#image) Bildstile im rechten Bedienfeld.

+++

+++Schaltflächen-Elemente

1. Wählen Sie ein Schaltflächenelement auf der Seite aus.

1. (Optional) Geben Sie einen neuen Text für die Schaltfläche ein, oder wählen Sie die Textzeichenfolge aus und geben Sie den Ersatztext ein.

   Sie können die Personalisierung verwenden, um den Schaltflächentext mithilfe von Daten aus Konto- oder Personenprofilen zu ändern.

1. Verwenden Sie bei [&#x200B; die &#x200B;](./content-components.md#button) im rechten Bedienfeld.

+++

+++ Container-Elemente

1. Wählen Sie ein Container-Element auf der Seite aus.

1. Verwenden Sie [Container-Stiloptionen](./content-components.md#container) im rechten Bedienfeld, sofern erforderlich.

+++

### Neue Komponenten einfügen

Wenn Sie im linken Navigationsbereich für den visuellen Editor im Design auf das Symbol **+** klicken, können Sie die folgenden Komponententypen zur Seite hinzufügen, um das Web-Erlebnis zu ändern:

* **[!UICONTROL Trennlinie]** - Verwenden Sie diese Komponente, um das Layout und den Inhalt Ihrer E-Mail durch eine Trennlinie zu strukturieren. Sie können Stilattribute wie Zeilenfarbe, Stil und Höhe in den Eigenschaften im rechten Bereich anpassen. Weitere Informationen finden [&#x200B; unter &#x200B;](./content-components.md#divider) in _Inhaltskomponenten_.
* **[!UICONTROL HTML]** - Verwenden Sie diese Komponente, um HTML-Code zu kopieren und in die vorhandene Struktur einzufügen. Damit können Sie kostenlose modulare HTML-Komponenten erstellen, um externe Inhalte wiederzuverwenden. HTML Weitere Informationen finden Sie unter {[}in &#x200B;](./content-components.md#html)Inhaltskomponenten _._
* **[!UICONTROL Bild]** - Verwenden Sie diese Komponente, um eine Bilddatei in die Seite einzufügen. Sie können Stilattribute wie Breite und Höhe in den Eigenschaften im rechten Bereich anpassen. Weitere Informationen finden [&#x200B; unter &#x200B;](./content-components.md#image) in _Inhaltskomponenten_.
* **[!UICONTROL Überschrift]** - Verwenden Sie diese Komponente, um Text für die Überschriftenklasse einzufügen. Sie können Stilattribute wie Textfarbe, Stil, Schriftart und Größe in den Eigenschaften im rechten Bereich anpassen. Weitere Informationen finden [&#x200B; unter &#x200B;](./content-components.md#text) in _Inhaltskomponenten_.
* **[!UICONTROL Absatz]** - Verwenden Sie diese Komponente, um ein standardmäßiges Textelement einzufügen. Sie können Stilattribute wie Textfarbe, Stil, Schriftart und Größe in den Eigenschaften im rechten Bereich anpassen. Weitere Informationen finden [&#x200B; unter &#x200B;](./content-components.md#text) in _Inhaltskomponenten_.
* **[!UICONTROL Link]** - Verwenden Sie diese Komponente, um einen freistehenden Text-Link zu einer angegebenen URL einzufügen. Sie können Stilattribute wie Textfarbe, Stil, Ausrichtung und Größe in den Eigenschaften im rechten Bereich anpassen.

Wählen Sie links einen Komponententyp aus und bewegen Sie dann den Mauszeiger über ein Element, das an der Stelle angrenzt, an der Sie es hinzufügen möchten.

![Visual Editor-Benutzeroberfläche - neue Komponente](./assets/web-experience-design-visual-editor-insert-component.png){width="800" zoomable="yes"}

Klicken Sie auf eine der angezeigten Schaltflächen, um die Komponente zu platzieren:

* ***[!UICONTROL Einfügen vor]** - Einfügen der Komponente vor dem ausgewählten Element.
* ***[!UICONTROL Einfügen nach]** - Einfügen der Komponente nach dem ausgewählten Element.

Um die Auswahl eines Komponententyps für das Einfügen aufzuheben, klicken Sie auf **[!UICONTROL ESC]** in dem kontextuellen blauen Banner, das oben auf der Seite angezeigt wird.

## Nicht visueller Editor {#non-visual-editor}

Verwenden Sie den nicht visuellen Editor, wenn Sie Änderungen vornehmen müssen, die im visuellen Editor nicht einfach zu erledigen sind. Dieser Code-basierte Ansatz bietet Ihnen präzise Kontrolle über das Targeting und die Änderung von Elementen. Führen Sie die folgenden Schritte aus, um den nicht visuellen Editor zum Entwerfen Ihres Web-Erlebnisses zu verwenden:

1. Klicken Sie auf der _[!UICONTROL „Inhalt]_ auf der Seite mit den Web-Erlebnisdetails **[!UICONTROL Bereich auf]**&#x200B;Änderung hinzufügen“.

   Der nicht visuelle Editor lädt eine Seite basierend auf der Konfiguration des Web-Kanals.

   ![Nicht visuelle Editor-Benutzeroberfläche](./assets/web-experience-design-non-visual-editor.png){width="800" zoomable="yes"}

1. Definieren Sie die erste Änderung, die Sie vornehmen möchten.

   Im linken Seitenbereich wird eine Liste der vorhandenen Änderungen angezeigt (sofern vorhanden). Klicken Sie **[!UICONTROL Hinzufügen]**, um eine neue Änderung zu definieren. Wenn keine Änderungen definiert sind, werden im Bedienfeld standardmäßig die Optionen _[!UICONTROL Änderung hinzufügen]_ verwendet.

   * Wählen Sie den **[!UICONTROL Modifizierungstyp]**:

     | Typ | Beschreibung |
     | ---- | ----------- |
     | [**[!UICONTROL CSS-Auswahl]**](#css-selector-modifications) | Targeting von Elementen mithilfe einer CSS-Auswahlzeichenfolge. |
     | [**[!UICONTROL Seite]**](#page-modifications) | Fügen Sie benutzerdefinierte HTML, CSS oder JavaScript in Elemente auf Seitenebene ein, z. B. `<head>` oder `<body>`. |

   * Konfigurieren Sie die Änderungsparameter entsprechend dem Typ:

      * **[!UICONTROL CSS-Selektor]** - Geben Sie einen gültigen CSS-Selektor ein, um bestimmte Elemente auszuwählen.
      * **[!UICONTROL Aktionstyp]** - Wählen Sie die auszuführende Aktion aus (Bearbeiten, Ausblenden, Löschen, Einfügen, Ersetzen).
      * **[!UICONTROL Inhalt]** - Geben Sie den Inhalt oder die Formatierung an, die angewendet werden soll.

1. Klicken Sie **[!UICONTROL Speichern]**, um die Änderung anzuwenden.

### Änderungen an CSS-Selektor

Änderungen an CSS-Selektoren ermöglichen es Ihnen, Elemente mithilfe der standardmäßigen CSS-Selektorsyntax präzise anzusprechen.

1. Wählen Sie **[!UICONTROL CSS]** Auswahl als Änderungstyp aus.

1. Geben Sie den Selektor in das Feld **[!UICONTROL CSS]** Elementauswahl“ ein.

<!-- This field helps you find and select the HTML elements (or nodes in the DOM tree). -->

    **Beispielselektoren:**
    
    | Selektor | Zielgruppen |
    | -------- | ------- |
    | `#hero-banner` | Element mit der ID „hero-banner“ |
    | &quot;.cta-button“ | Alle Elemente mit Klasse „cta-button“ |
    | `nav-Kopfzeile` | Links innerhalb der Navigation, innerhalb der Kopfzeile |
    | &quot;[data-offer=„premium“]&quot; | Elemente mit einem bestimmten Datenattribut |

1. Wählen Sie einen **[!UICONTROL Aktionstyp]** und geben Sie die erforderlichen Informationen/Inhalte an.

   * **[!UICONTROL Inhalt festlegen]** - Geben Sie den Text in das Feld **[!UICONTROL Inhalt]** für das Element ein, das durch den _[!UICONTROL CSS-]_ identifiziert wird.

   * **[!UICONTROL Attribut festlegen]** - Geben Sie ein Attribut an, das mit der aktuellen CSS-Auswahl verknüpft werden soll, damit das Element durch dieses Attribut identifiziert werden kann. Geben Sie einen Namen in das Feld **[!UICONTROL Attributname]** und einen Wert in das Feld **[!UICONTROL Inhalt]** ein. Wenn das Attribut bereits vorhanden ist, wird der Wert aktualisiert. Andernfalls wird ein neues Attribut mit dem angegebenen Namen und Wert hinzugefügt.

   ![Änderung der CSS-Auswahl eines nicht visuellen Editors](./assets/web-experience-design-non-visual-editor-modification-css-selector.png){width="800" zoomable="yes"}

1. (Optional) Klicken Sie auf **[!UICONTROL Personalisierung hinzufügen]** und verwenden Sie den [Personalisierungseditor](./personalization.md#personalization-editor), um eine benutzerdefinierte Personalisierung für den Inhalt zu erstellen.

### Seitenänderungen

Sie können benutzerdefinierten Code mit dem Änderungstyp Seite `<head>` hinzufügen. Das `<head>`-Element ist ein Container für Metadaten (Daten über Daten) und wird zwischen dem `<html>`-Tag und dem `<body>`-Tag platziert. In diesem Fall wartet der Code nicht darauf, dass der Hauptteil oder die Seite geladen wird, sondern er wird zu Beginn des Seitenladevorgangs ausgeführt.

Das `<head>`-Element wird häufig verwendet, um oben auf der Seite JavaScript- oder CSS-Code hinzuzufügen. Die Auswahlen für nachfolgende visuelle Aktionen hängen von den auf dieser Registerkarte hinzugefügten HTML-Elementen ab.

>[!NOTE]
>
>Benutzerdefinierter Code wird im Browser des Besuchers ausgeführt. Stellen Sie sicher, dass Ihr Code sicher und getestet ist und sich nicht negativ auf die Seitenleistung oder das Benutzererlebnis auswirkt.

1. Wählen **[!UICONTROL als Änderungstyp „Seite`<head>`]**&quot; aus.

1. Fügen Sie Ihren benutzerspezifischen Code im Feld **[!UICONTROL Inhalt]** hinzu.

   >[!CAUTION]
   >
   >Sie können nur `<script>`- und `<style>`-Elemente zum Abschnitt `<head>` hinzufügen. Das Hinzufügen `<div>` Tags und anderer Elemente kann dazu führen, dass die verbleibenden `<head>` Elemente innerhalb des `<body>` befüllt werden.

   ![Seitenkopfänderung im nicht visuellen Editor](./assets/web-experience-design-non-visual-editor-modification-page-head.png){width="800" zoomable="yes"}

1. (Optional) Klicken Sie auf **[!UICONTROL Personalisierung hinzufügen]** und verwenden Sie den [Personalisierungseditor](./personalization.md#personalization-editor), um eine benutzerdefinierte Personalisierung für den Inhalt zu erstellen.

## Verwalten von Änderungen {#manage-modifications}

>[!CONTEXTUALHELP]
>id="ajo-b2b_web_experience_modifications"
>title="Einfaches Verwalten aller Änderungen"
>abstract="Mithilfe dieses Bereichs können Sie alle für die Web-Seite definierten Anpassungen und Ergänzungen durchsuchen und verwalten."

Alle von Ihnen erstellten Änderungen werden verfolgt und können über das Bedienfeld **[!UICONTROL Änderungen]** sowohl des visuellen Editors als auch des nicht visuellen Editors verwaltet werden. Klicken Sie auf _[!UICONTROL Änderungen]_ in <!-- ( ![Modifications icon](../assets/do-not-localize/icon-web-exp-modifications.svg) ) --> linken Symbolleiste, um alle Änderungen anzuzeigen.

Jeder Änderungsdatensatz enthält:

* Das Zielelement oder die Auswahl
* Der Änderungstyp (z. B. Bearbeiten, Ausblenden oder Einfügen)
* Eine Vorschau der Änderung

![Bedienfeld Änderungen](./assets/web-experience-design-modifications-list.png){width="500" zoomable="yes"}

### Bearbeiten einer Änderung

1. Suchen Sie in _[!UICONTROL Liste]_&#x200B;Änderungen“ die Änderung, die Sie bearbeiten möchten.

1. Klicken Sie auf das _Mehr Menü_ ( **…** ) und wählen Sie **[!UICONTROL Bearbeiten]**.

1. Aktualisieren Sie die Änderungseigenschaften nach Bedarf.

1. Klicken Sie **[!UICONTROL Speichern]**, um Ihre Änderungen zu speichern.

### Löschen einer Änderung

1. Suchen Sie in _[!UICONTROL Liste]_&#x200B;Änderungen“ die Änderung, die Sie entfernen möchten.

1. Klicken Sie auf das _Mehr Menü_ ( **…** ) und wählen Sie **[!UICONTROL Änderung löschen]**.

1. Bestätigen Sie die Entfernung, wenn Sie dazu aufgefordert werden.

<!-- ### Reorder modifications

Modifications are applied in the order that they appear in the list. If you have multiple modifications that affect the same element, the order may impact the final result.

Drag and drop modifications in the list to change the order. The preview updates to reflect the new modification order. -->

## Vorschau der Änderungen

Zeigen Sie vor dem Veröffentlichen eine Vorschau des Erscheinungsbilds Ihrer Änderungen für Besucher an.

Verwenden Sie die Optionen für die Gerätevorschau oben im visuellen Editor, um Ihre Änderungen in anzuzeigen:

* Desktop
* Tablet
* Mobile

![Ändern der Gerätegröße für die Vorschau](./assets/web-experience-design-device-view.png){width="550" zoomable="yes"}

Die Vorschau wird aktualisiert, um zu zeigen, wie Änderungen auf den einzelnen Gerätegrößen gerendert werden.

Verwenden Sie die URL-Leiste, um zu verschiedenen Seiten innerhalb Ihrer Web-Kanal-Konfiguration zu navigieren. Überprüfen Sie dann, ob die Änderungen basierend auf Ihren URL-Abgleichregeln korrekt auf die Zielseiten angewendet werden.

## Klick-Tracking für Web-Erlebnisse {#web-click-tracking}

Benutzerinteraktionen mit Elementen verfolgen, um die Interaktion zu messen und Erkenntnisse zu gewinnen. Die Klick-Tracking-Daten stehen in Ihren Interaktionsberichten zur Verfügung und können verwendet werden, um die Effektivität Ihrer Änderungen am Web-Erlebnis zu messen.

Wenn Ihr Web-Erlebnis aktiviert ist (live), können Sie Berichte auch mit der Adobe Customer Journey Analytics erstellen (hierfür ist ein Produktabonnement erforderlich). Um die Überwachung Ihres Web-Erlebnisses zu verbessern, können Sie auch die Klicks auf beliebige Elemente Ihrer Website verfolgen. Mit dem Tracking können Sie die Anzahl der Klicks für dieses Element in den Web-Berichten anzeigen.

Weitere Informationen zu Customer Journey Analytics und zum Erstellen von Web-Berichten finden Sie in der [Customer Journey Analytics-Dokumentation](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-landing).

1. Wählen Sie ein Element im Web-Erlebnis-Editor aus, z. B. ein Bild oder einen Link.

1. Klicken Sie in den Elementeigenschaften oder in der kontextuellen Symbolleiste auf das Symbol _[!UICONTROL Element nachverfolgen]_.

   ![Klick-Tracking für Web-Erlebniselemente aktivieren](./assets/web-experience-design-visual-editor-click-tracking-icons.png){width="600" zoomable="yes"}

1. Öffnen Sie die Klick-Tracking-Liste im linken Bereich und ändern Sie den Wert **[!UICONTROL Nachverfolgte Aktionen]**, um diese Interaktion in Ihren Berichten zu identifizieren.

   ![Festlegen der Klick-Tracking-Kennung für das Web-Erlebnis](./assets/web-experience-design-visual-editor-click-tracking-identifier.png){width="600" zoomable="yes"}
