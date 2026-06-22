---
title: Hinzufügen von benutzerdefiniertem CSS für Inhalte
description: Hinzufügen von benutzerdefiniertem CSS zu E-Mails und Landingpages für erweiterte Formatierung und präzise Designkontrolle über die Standardkomponenten in Journey Optimizer B2B Prime hinaus.
feature: Content Design Tools, Email Authoring, Landing Pages
role: User
badgeBeta: label="Beta" type="informative" tooltip="Diese Funktion ist Teil einer eingeschränkten Beta-Version."
autotag-review: '2026-06-19T22:00:56.704Z'
TQID: 'https://experienceleague.adobe.com/z0vACEVhY2WZcSgeO3Kbx7ceSNsf4Se3DZut36xnN4E'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: e666e996-b2cf-4c45-8fc2-1c625212ababid: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: e7bdffdc-2950-4be5-8c23-84240a995090id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: c9ba0bd460bf68ea46c2641b8044f23c9656334b
workflow-type: tm+mt
source-wordcount: 567
ht-degree: 9%

---


Sie können Ihr eigenes benutzerdefiniertes CSS direkt im E-Mail- oder Landingpage-Design-Bereich hinzufügen. Verwenden Sie benutzerdefiniertes CSS, um erweiterte und spezifische Stile anzuwenden, um die Flexibilität und Kontrolle über das Erscheinungsbild Ihrer Inhalte zu erhöhen.

Das benutzerdefinierte CSS wird innerhalb eines `<style>`-Tags mit dem `data-name="global-custom"`-Attribut an den `<head>`-Abschnitt angehängt. Diese Struktur stellt sicher, dass die benutzerdefinierten Stile global auf den Inhalt angewendet werden.

+++ Beispielimplementierung

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="content-version" content="3.3.31">
    <meta name="x-apple-disable-message-reformatting">
    <meta name="viewport" content="width=device-width,initial-scale=1.0">
    <style data-name="default" type="text/css">
      td { padding: 0; }
      th { font-weight: normal; }
    </style>
    <style data-name="grid" type="text/css">
      .acr-grid-table { width: 100%; }
    </style>
    <style data-name="acr-theme" type="text/css" data-theme="default" data-variant="0">
      body { margin: 0; font-family: Arial; }
    </style>
    <style data-name="media-default-max-width-500px" type="text/css">
      @media screen and (max-width: 500px) {
        body { width: 100% !important; }
      }
    </style>
    <style data-name="global-custom" type="text/css">
      /* Add you custom CSS here */
    </style>
  </head>
  <body>
    <!-- Minimal content -->
  </body>
</html>
```

+++

>[!NOTE]
>
>Das benutzerdefinierte CSS wird für eine ausgewählte Komponente im Bedienfeld _[!UICONTROL Stile]_ nicht angezeigt oder validiert. Sie ist völlig unabhängig und kann nur durch die Option [!UICONTROL Benutzerdefiniertes CSS hinzufügen] auf der Ebene der Hauptteilkomponente geändert werden.

## Hinzufügen von benutzerdefiniertem CSS

1. Wenn mindestens eine Inhaltskomponente auf der Arbeitsfläche hinzugefügt wurde, wählen Sie die **[!UICONTROL Hauptteil]** in der linken Navigationsleiste aus.

1. Wählen Sie auf _rechten Seite die_ „Stile“ und klicken Sie auf **[!UICONTROL Benutzerdefiniertes CSS hinzufügen]**.

   ![Zugriff auf Textkörperstile](../../user/content/assets/email-body-styles.png){width="800" zoomable="yes"}

   >[!NOTE]
   >
   >Die Schaltfläche _[!UICONTROL Benutzerdefiniertes CSS hinzufügen]_ ist nur verfügbar, wenn die Komponente _[!UICONTROL Hauptteil]_ ausgewählt ist. Sie können jedoch benutzerdefinierte CSS-Stile auf alle darin enthaltenen Komponenten anwenden.

   Der _[!UICONTROL Benutzerdefinierte CSS hinzufügen]_ Popup-Editor wird mit Platzhalter-Code-Kommentaren angezeigt.

1. Geben Sie Ihren CSS-Code im Editor ein.

   Stellen Sie sicher, dass das benutzerdefinierte CSS gültig ist und der richtigen Syntax folgt. Wenn die eingegebene CSS-Datei ungültig ist, wird eine Fehlermeldung angezeigt und die CSS-Datei kann nicht gespeichert werden. Weitere Informationen finden Sie unter [CSS-Gültigkeit](#css-validity).

   ![Benutzerdefiniertes CSS im Editor eingeben](../../user/content/assets/content-design-add-custom-css.png){width="450"}

1. Klicken Sie **[!UICONTROL Speichern]**, um das benutzerdefinierte CSS zu speichern.

   Das benutzerdefinierte Stylesheet wird auf den vorhandenen Inhalt angewendet. Sie können überprüfen, ob Ihr benutzerdefiniertes CSS Ihren Anforderungen entspricht. Informationen zum Vornehmen von Änderungen und Anpassen der Stylesheet-Anwendung finden Sie unter [Fehlerbehebung](#troubleshooting).

   ![Benutzerdefiniertes CSS auf Inhalte angewendet](../../user/content/assets/email-body-custom-css-applied.png){width="600" zoomable="yes"}

## CSS-Gültigkeit {#css-validity}

>[!CAUTION]
>
>Benutzende sind für die Sicherheit ihres benutzerdefinierten CSS verantwortlich. Stellen Sie sicher, dass durch Ihr CSS keine Sicherheitslücken entstehen und dass es nicht mit den vorhandenen Inhalten in Konflikt steht.
>
>Vermeiden Sie die Verwendung von CSS, das unbeabsichtigt das Layout oder die Funktionalität des Inhalts beeinträchtigen könnte.

+++ Beispiele für gültiges CSS

```css
.acr-component[data-component-id="form"] {
  display: flex;
  justify-content: center;
  background: none;
}

.acr-Form {
  width: 100%;
  padding: 20px 100px;
  border-spacing: 0px 8px;
  box-sizing: border-box;
  margin: 0;
}

.acr-Form .spectrum-FieldLabel {
  width: 20%;
}

.acr-Form.spectrum-Form--labelsAbove .spectrum-FieldLabel,
.acr-Form [data-form-item="checkbox"] .spectrum-FieldLabel {
  width: auto;
}

.acr-Form .spectrum-Textfield {
  width: 100%;
}

#acr-form-error,
#acr-form-confirmation {
  width: 100%;
  padding: var(--spectrum-global-dimension-static-size-500);
  display: flex;
  align-items: center;
  flex-direction: column;
  justify-content: center;
  gap: var(--spectrum-global-dimension-static-size-200);
}

.spectrum-Form-item.is-required .spectrum-FieldLabel:after{
  content: '*';
  font-size: 1.25rem;
  margin-left: 5px;
  position: absolute;
}

/* Error field placeholder */
.spectrum-HelpText {
  display: none !important;
}

.spectrum-HelpText.is-invalid,
.is-invalid ~ .spectrum-HelpText {
  display: flex !important;
}
```

```css
@media only screen and (min-width: 600px) {
  .acr-paragraph-1 {
    width: 100% !important;
  }
}
```

+++

+++ Beispiele für ungültiges CSS

Die Verwendung von `<style>`-Tags wird nicht akzeptiert:

```html
<style type="text/css">
  .acr-Form {
    width: 100%;
    padding: 20px 100px;
    border-spacing: 0px 8px;
    box-sizing: border-box;
    margin: 0;
  }
</style>
```

Ungültige Syntax wie fehlende Klammern wird nicht akzeptiert:

```css
body {
  background: red;
```

+++

## CSS in importierten Inhalten {#imported-content}

Wenn Sie benutzerdefiniertes CSS mit Inhalten verwenden möchten, die in den Design-Bereich für E-Mails oder Landingpages importiert wurden, sollten Sie Folgendes beachten:

* Wenn Sie externe HTML-Inhalte einschließlich CSS importieren, werden diese im [!UICONTROL Kompatibilitätsmodus] aufgefüllt und der Abschnitt [!UICONTROL CSS-]&quot; ist nicht verfügbar.

* Wenn Sie Inhalte importieren, die ursprünglich im Design-Bereich der E-Mail oder Landingpage mit der Option [!UICONTROL Benutzerdefiniertes CSS hinzufügen] erstellt wurden, ist die angewendete CSS-Datei von derselben Option aus sichtbar und bearbeitbar.

## Fehlerbehebung {#troubleshooting}

Wenn Ihr benutzerdefiniertes CSS nicht wie erwartet angewendet wird, verwenden Sie die Browser-Entwickler-Tools, um den Inhalt zu überprüfen und sicherzustellen, dass Ihr CSS auf die richtigen Selektoren abzielt. Beachten Sie beim Überprüfen des Stilcodes Folgendes:

* Überprüfen Sie, ob Ihr CSS gültig und frei von Syntaxfehlern (z. B. fehlende Klammern, falsche Eigenschaftsnamen) ist.

* Vergewissern Sie sich, dass Ihre CSS-Datei dem `<style>`-Tag mit dem `data-name="global-custom"` hinzugefügt wurde.

* Überprüfen Sie, ob für das Stil-Tag des `global-custom` das Attribut auf „true“ festgelegt `data-disabled`, z. B.:

  `<style data-name="global-custom" type="text/css" data-disabled="true"> body: { color: red; } </style>`

* Vergewissern Sie sich, dass Ihr CSS nicht an einer beliebigen Stelle im Inhalt überschrieben wird, z. B. beim Anwenden von Inline-Stilen.

* Fügen Sie Ihren -Deklarationen `!important` hinzu, um sicherzustellen, dass sie Vorrang haben, z. B.:

  ```
  .acr-Form {
  background: red !important;
  }
  ```
