---
title: Autor aus einer konfigurierten Vorlage
description: Erfahren Sie, wie Sie E-Mail-Authoring mit einer verwalteten Vorlage verwenden, die gesperrte Inhaltskomponenten enthält.
feature: Email Authoring, Content
source-git-commit: d7e2b7673b0a6709d2841893d87617e580b62298
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 1%

---

# Autor aus einer verwalteten Vorlage

Inhaltsentwickler können beim Erstellen von E-Mail-Vorlagen die [Governance (_Inhaltssperrung_)](./template-content-governance.md) aktivieren. Mit Governance-Funktionen können die Designteile bestimmt werden, die bei Verwendung in einer Konto-Journey nicht geändert werden können. Wenn Sie [eine gespeicherte Vorlage auswählen](./email-authoring.md#select-a-template), um eine E-Mail zu erstellen, lädt der visuelle Designer die Vorlage, damit Sie sie als Grundlage für Ihre E-Mail verwenden können.

Wenn für die Vorlage Governance aktiviert ist, wird im Eigenschaftenbedienfeld auf der rechten Seite ein Warnhinweis angezeigt. Sie können oben auf der Arbeitsfläche die Option **[!UICONTROL Bearbeitbare Bereiche markieren]** aktivieren, um zu sehen, welche Komponenten und Inhaltselemente für die Verwendung in Ihrer Journey bearbeitbar sind.

![Bearbeitbare Bereiche in einer verwalteten Vorlage anzeigen](./assets/email-designer-governed-highlight.png){width="800" zoomable="yes"}

Sie können die gesperrten oder bearbeitbaren Elemente auch mithilfe des _Navigationsbaums_ bestimmen. Klicken Sie auf das Symbol _Navigationsbaum_ ( ![Verknüpfungssymbol](../assets/do-not-localize/icon-navigation-tree.svg) ) links neben der Arbeitsfläche, um den Baum anzuzeigen.

![Bearbeitbare Bereiche in einer verwalteten Vorlage anzeigen](./assets/email-designer-governed-tree.png){width="600" zoomable="yes"}

Die Symbole geben die angewendeten Einstellungen für die Inhaltssperrung an.

| Symbol | Name | Beschreibung |
|------|------|-------------|
| ![Schreibgeschütztes Symbol](../assets/do-not-localize/icon-tree-lock.svg) | Schreibgeschützt | Die Komponente ist gesperrt und kann nicht bearbeitet werden. Wenn sie auf die Stammebene (_[!UICONTROL Hauptteil]_) angewendet werden, sind alle untergeordneten Komponenten gesperrt und können nicht bearbeitet werden. |
| ![Symbol zur Inhaltsbearbeitung](../assets/do-not-localize/icon-tree-content-lock.svg) | Inhaltssperre | Die Inhaltssperrung wird auf Komponentenebene angewendet. |
| ![Symbol &quot;Bearbeitbar&quot;](../assets/do-not-localize/icon-edit.svg) | Bearbeitbar | Die Komponente kann vollständig bearbeitet werden. Möglicherweise können Sie das Element jedoch nicht löschen. |
| ![Symbol zur Inhaltsbearbeitung](../assets/do-not-localize/icon-tree-edit-text.svg) | Bearbeitbar - nur Inhalt | Die Komponente und der Stil sind statisch, Sie können jedoch den Inhalt ändern (z. B. Text oder Bild). |
