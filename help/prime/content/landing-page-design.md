---
title: Landingpage-Design
description: Entwerfen von Landingpages mit visuellen Tools - Hinzufügen von Inhaltskomponenten, Formularen, benutzerdefiniertem CSS, Personalisierung und Gerätevorschau für Personen-Journey in Journey Optimizer B2B Prime.
badgeBeta: label="Beta" type="informative" tooltip="Diese Funktion ist Teil einer eingeschränkten Beta-Version."
feature: Landing Pages, Content Design Tools
role: User
autotag-review: '2026-07-08T20:36:05.221Z'
TQID: 'https://experienceleague.adobe.com/M8OA0CPihuuX5h9J-ZrGJOPHkHLwatX5VhBa8co4r4Y'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
  - id: e666e996-b2cf-4c45-8fc2-1c625212abab
subfeature_v2:
  - id: a96755d6-1f54-4f3f-a971-d31f83705ab7
  - id: e7bdffdc-2950-4be5-8c23-84240a995090
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 75a4fec07c880f52ac1e8981b5f4416a2f69afe9
workflow-type: tm+mt
source-wordcount: 568
ht-degree: 2%

---

# Landingpage-Design

Nachdem Sie [Landingpage erstellt haben](./landing-pages-create-publish.md#create-landing-page) verwenden Sie den visuellen Design-Bereich, um die Struktur- und Inhaltskomponenten in Ihrer Seite zu erstellen.

## Hinzufügen von Struktur und Inhalten {#structure-content-landing-page}

{{$include /help/_includes/content-design-components-prime.md}}

### Hinzufügen von benutzerdefiniertem CSS {#add-custom-css}

Sie können Ihr eigenes benutzerdefiniertes CSS direkt im Design-Bereich der Landingpage hinzufügen. Verwenden Sie benutzerdefiniertes CSS, um erweiterte und spezifische Stile anzuwenden, um die Flexibilität und Kontrolle über das Erscheinungsbild Ihrer Inhalte zu erhöhen. Es empfiehlt sich, diese Formatierung auf höchster Ebene hinzuzufügen, bevor Sie Komponenten wie Bilder, Schaltflächen und Text einbeziehen.

Wählen Sie bei mindestens einer Inhaltskomponente auf der Arbeitsfläche die Komponente **[!UICONTROL Hauptteil]** in der linken Navigationsstruktur aus, um auf den benutzerdefinierten CSS-Editor zuzugreifen.

![Zugriff auf Textkörperstile](../../user/content/assets/landing-page-body-styles-css.png){width="800" zoomable="yes"}

Anweisungen[&#x200B; Syntaxregeln und Fehlerbehebung finden Sie unter „Hinzufügen von benutzerdefiniertem &#x200B;](./design-custom-css.md) für Ihre Inhalte“.

### Hinzufügen von Assets {#add-assets}

Wählen Sie im visuellen Design-Bereich das Symbol _Assets_ ( ![Assets-Symbol](../../assets/do-not-localize/icon-assets-me.svg) ) in der linken Navigationsleiste aus, um Bild-Assets in der [!DNL Journey Optimizer B2B Prime] Asset-Bibliothek zu suchen und auszuwählen.

Anweisungen zum Auswählen, Ersetzen oder Hochladen von Bild-Assets finden Sie unter [Verwenden von Assets für die Inhaltserstellung](./digital-asset-management.md#assets-authoring).

### Formulare hinzufügen {#add-forms}

{{$include /help/_includes/content-design-add-forms.md}}

### Navigieren in den Ebenen, Einstellungen und Stilen {#navigate-layers-settings-styles}

{{$include /help/_includes/content-design-navigation.md}}

### Personalisieren von Inhalten {#personalize-content}

[!DNL Journey Optimizer B2B Prime] verwendet die Handlebars-Syntax für die Personalisierung. Token werden bei der Anzeige der Landingpage durch Werte aus den Profildaten der einzelnen Besucher ersetzt.

_Personalisierung hinzufügen :_

1. Wählen Sie die Textkomponente aus und klicken Sie auf das Symbol _Personalisierung hinzufügen_ ( ![Personalisierungssymbol](../../user/assets/do-not-localize/icon-personalize.svg) ) in der Symbolleiste.
1. Durchsuchen Sie im Personalisierungsdialog die Schemastruktur auf der linken Seite und wählen Sie ein Attribut aus. Der Editor fügt den entsprechenden Handlebars-Ausdruck ein.
1. Fügen Sie bei Bedarf einen Fallback-Wert hinzu, um fehlende Daten zu verarbeiten.
1. Klicken Sie **[!UICONTROL Bestätigen]** oder **[!UICONTROL Einfügen]**. Der Ausdruck wird inline im Feld angezeigt.

Weitere Informationen zu den Tools und der Syntax des Ausdruckseditors finden Sie unter [Personalization-Editor](./personalization-expressions.md).

### Verknüpftes URL-Tracking bearbeiten {#linked-url-tracking}

{{$include /help/_includes/content-design-links.md}}

![Klicken Sie auf das Symbol Bearbeiten , um auf das Linktracking zuzugreifen](../../user/content/assets/landing-page-link-tracking.png){width="400"}

Verwenden Sie den **[!UICONTROL Tracking-Typ]**, um das Tracking für den Link zu steuern:

* **[!UICONTROL Verfolgt]** - Aktiviert das Tracking der Link-URL.
* **[!UICONTROL Nie]** - Das Tracking der Link-URL wird nie aktiviert.

### Speichern Sie Ihre Arbeit {#save-your-work}

Klicken Sie **[!UICONTROL auf]**, um den Entwurf der Landingpage zu speichern.

Sie können die Entwurfsseite weiterhin bearbeiten. Wenn Sie bereit sind, die Seite anzuzeigen und für die Verknüpfung in einer E-Mail oder SMS-Nachricht verfügbar zu machen, können Sie die Seite veröffentlichen.

### Optionen anzeigen {#view-options}

Nutzen Sie die Ansicht- und Inhaltsvalidierungsoptionen, die im visuellen Design-Bereich verfügbar sind.

* Vergrößern/Verkleinern des Inhalts in allen vordefinierten Zoom-Optionen.

* Wechseln der Anzeige von Inhalten zwischen Desktop, Mobilgerät oder Nur-Text-/Nur-Text-Ansicht.
   * Klicken Sie auf das _Anzeigen_-Symbol für die geräteübergreifende Inhaltsvorschau.
   * Wählen Sie eines der standardmäßigen Geräte aus oder geben Sie benutzerdefinierte Dimensionen ein, um eine Vorschau des Inhalts anzuzeigen.

### Mehr Optionen {#more-options}

Im Menü _[!UICONTROL Mehr …]_ oben im visuellen Design-Bereich können Sie die folgenden Aktionen ausführen:

![Klicken Sie auf Mehr , um auf Landingpage-Aktionen zuzugreifen](../../user/content/assets/landing-page-designer-more-menu.png){width="500"}

* **[!UICONTROL Landingpage zurücksetzen]** - Klicken Sie auf diese Option, um die visuelle Design-Arbeitsfläche zu leeren und die Erstellung Ihres Seiteninhalts neu zu starten.
* **[!UICONTROL Design ändern]** - Kehren Sie zur Startseite von _[!UICONTROL Erstellen]_ primären Landingpage“ zurück. Dort können Sie eine andere Vorlage auswählen, um den Design-Prozess neu zu starten, oder die Seite von Grund auf auf auf einer leeren Arbeitsfläche entwerfen.
* **[!UICONTROL HTML exportieren]** - Laden Sie den Inhalt auf der visuellen Arbeitsfläche in HTML im Format herunter, das als ZIP-Datei verpackt ist.
