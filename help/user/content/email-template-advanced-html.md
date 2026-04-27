---
title: Erweiterter HTML-Modus für das Design von E-Mail-Vorlagen
description: Verwenden Sie den erweiterten HTML-Modus, um die unformatierte HTML-Quelle Ihres Inhalts Ihrer E-Mail-Vorlage direkt im E-Mail-Design-Bereich in Journey Optimizer B2B Edition anzuzeigen und zu bearbeiten.
feature: Email Authoring, Templates, Content Design Tools
level: Experienced
role: User
exl-id: 92af078b-29b4-4507-ae43-55dc4dd4b748
source-git-commit: a99560d6f32222f8912c7711ff1913777a1161b6
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 0%

---

# Erweiterter HTML-Modus für das Design von E-Mail-Vorlagen

_Erweiterter HTML-Modus_ bietet eine Ansicht, mit der erfahrene Benutzende den Rohcode für den Inhalt von E-Mail-Vorlagen direkt anzeigen und bearbeiten können. Dieser Modus ist ideal, wenn Sie anspruchsvolle Ausdrücke wie bedingte Logik direkt in die Quelle einfügen möchten. Sie ist auch für strukturelle Anpassungen nützlich, die über das hinausgehen, was die visuellen Entwurfswerkzeuge verfügbar machen.

<!-- 
We don't have the code editor at this point 
>[!NOTE]
>
>_Advanced HTML mode_ is different from the code editor option that is available when you start a new design. The code editor does not allow you to change to the visual design space. With _advanced HTML mode_, you can toggle back and forth between the HTML source view and the visual design view at any time. 
-->

>[!AVAILABILITY]
>
>Diese Funktion ist derzeit _Eingeschränkte Verfügbarkeit_ und steht nicht allen Benutzern zur Verfügung.

## Wichtige Einschränkungen

Bevor Sie den erweiterten HTML-Modus für das [Erstellen von E-Mail-Vorlagen](./email-template-authoring.md) verwenden, stellen Sie sicher, dass Sie die folgenden Einschränkungen verstehen:

* **Keine Validierung** - Der HTML-Editor führt keine Syntaxüberprüfung oder Layout-Überprüfung durch. Überprüfen Sie Ihren Code sorgfältig, bevor Sie ihn speichern.

* **Inhaltsaktualisierungen** - Künftige Systemänderungen können Änderungen am Standard-Markup im erweiterten HTML-Modus beeinträchtigen oder überschreiben. Überprüfen Sie Ihren Inhalt nach Produktaktualisierungen, um sicherzustellen, dass er wie erwartet gerendert wird.

* **Eingeschränkter Support** - Adobe kann keine Rendering-Probleme oder Inhaltsfehler beheben, die aus benutzerdefinierten Code-Änderungen im erweiterten HTML-Modus resultieren.

* **Vorschaubeschränkungen** - Die Inhaltssimulation (Vorschau mit Profilen) ist nur in der Desktop-Ansicht verfügbar, nicht direkt in der HTML-Quellansicht.

### Zugriff auf den erweiterten HTML-Modus

Der erweiterte HTML-Modus ist über die Symbolleiste oben im visuellen Design-Bereich aufrufbar, wenn Sie eine E-Mail-Vorlage auf die Arbeitsfläche geladen haben.

1. Öffnen oder [Erstellen einer E-Mail](./email-templates.md#create-an-email-template)Vorlage und öffnen Sie den Design-Bereich, um den Inhalt zu bearbeiten.

1. Klicken Sie in der Symbolleiste auf das Symbol _[!UICONTROL HTML]_ ( ![HTML](../assets/do-not-localize/icon-code.svg) ).

   ![Klicken Sie auf das HTML-Symbol in der Symbolleiste Design-Bereich für E-Mail-Vorlagen](./assets/email-template-advanced-html-mode-toolbar.png){width="750" zoomable="yes"}

   Wenn Sie den erweiterten HTML-Modus zum ersten Mal öffnen (oder ein Monat oder mehr verstrichen ist), wird eine Warnmeldung angezeigt. Überprüfen Sie die Informationen und klicken Sie auf **[!UICONTROL OK]**, um fortzufahren.

   ![Überprüfen Sie die Warnung Erweiterter HTML-Modus und klicken Sie auf OK , um fortzufahren](./assets/email-template-html-mode-warning.png){width="500"}

   Die Arbeitsfläche des Designs wechselt zur HTML-Quellansicht.

1. Überprüfen Sie den Code und fügen Sie die gewünschten Änderungen zum E-Mail-Inhalt hinzu.

   Im _erweiterten HTML_ Modus haben Sie direkten Zugriff auf den vollständigen HTML-Quellinhalt Ihrer E-Mail-Vorlage:

   * Anzeigen und Ändern eines beliebigen Teils des unformatierten HTML-Markups.
   * Fügen Sie erweiterte [Personalisierungsausdrücke](./personalization.md) direkt in die Quelle ein.
   * Fügen Sie [bedingte Inhalte](./conditional-content.md) Logik mithilfe der Ausdruckssyntax hinzu.
   * Fügen Sie benutzerdefinierte HTML-Attribute, Tracking-Tags oder anderes Markup hinzu, das nicht über die Steuerelemente des visuellen Editors verfügbar ist.

   ![Erweiterter HTML-Modus mit unformatierter HTML-Quelle des E-Mail-Inhalts](./assets/email-template-advanced-html-mode.png){width="800" zoomable="yes"}

   >[!IMPORTANT]
   >
   >Achten Sie darauf, den richtigen HTML- und CSS-Code einzugeben. Adobe bietet keine Syntaxvalidierung oder Unterstützung für benutzerdefinierten Code.

   Inhaltssimulation und -speicherung sind im erweiterten HTML-Modus aus Kompatibilitätsgründen nicht verfügbar. Sie können zur Desktop-Ansicht zurückkehren, um eine Vorschau Ihres Inhalts anzuzeigen und die Vorlage zu speichern. Alle vorgenommenen Änderungen bleiben beim Wechseln zwischen der HTML-Quellansicht und der visuellen Entwurfsansicht erhalten.

   Wenn Sie im erweiterten HTML-Modus oben **auf**&#x200B;[!UICONTROL &#x200B; Speichern &#x200B;]&#x200B;**oder** Speichern und schließen klicken, werden Sie in einem Warndialogfeld darüber informiert, dass Sie den erweiterten HTML-Modus beenden müssen, bevor Sie die Vorlage speichern und den Design-Bereich verlassen.

   ![Das Dialogfeld „Warnhinweise“ für das Speichern ist im erweiterten HTML-Modus deaktiviert](./assets/email-template-advanced-html-save-disabled-alert.png){width="500"}

1. Klicken Sie auf das Symbol _[!UICONTROL Desktop]_ ( ![Desktop-Symbol](../assets/do-not-localize/icon-desktop-spectrum-1.svg) ) in der Symbolleiste, um vom erweiterten HTML-Modus (der HTML-Quellansicht) zur Arbeitsfläche für das visuelle Design zu wechseln.

   Ihre Bearbeitungen bleiben beim Wechseln der Ansichten erhalten.
