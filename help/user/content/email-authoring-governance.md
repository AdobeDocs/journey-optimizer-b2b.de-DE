---
title: Aus einer verwalteten Vorlage erstellen
description: 'Verfassen von E-Mails aus verwalteten Vorlagen mit gesperrtem Inhalt : Identifizieren Sie bearbeitbare Bereiche und arbeiten Sie innerhalb der Governance-Beschränkungen in Journey Optimizer B2B edition.'
feature: Email Authoring, Content
role: User
exl-id: 1af996a6-a010-4899-96e9-bad76f93865c
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: e666e996-b2cf-4c45-8fc2-1c625212abab
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: f5c2a4bb-71ca-4d7e-8efd-442250e6ba48
autotag-review: 2026-03-30T22:35:16.900Z
TQID: https://experienceleague.adobe.com/iwVl-dwU9oGG0rHQ9-J3EO5r3B778jQCe6XK742ArEo
source-git-commit: 2c6aafd07cf033df8801621f7e5275dbeeb2768e
workflow-type: tm+mt
source-wordcount: 273
ht-degree: 1%

---

# Aus einer verwalteten Vorlage erstellen

Content-Designer können beim Erstellen von E[Mail _Vorlagen die_ Governance“ ](./template-content-governance.md). Mit Governance-Funktionen können sie die Teile des Designs festlegen, die bei Verwendung auf einer Account-Journey nicht geändert werden können. Wenn Sie [gespeicherte Vorlage auswählen](./email-authoring.md#select-a-template) um eine E-Mail zu erstellen, lädt der visuelle Design-Bereich die Vorlage, damit Sie sie als Grundlage für Ihre E-Mail verwenden können.

Wenn für die Vorlage die Governance aktiviert ist, wird im Bereich Eigenschaften auf der rechten Seite ein Warnhinweis angezeigt. Wählen Sie **[!UICONTROL Bearbeitbare Bereiche hervorheben]** oben auf der Arbeitsfläche aus, um zu sehen, welche Komponenten und Inhaltselemente für die Verwendung auf Ihrem Journey bearbeitbar sind.

![Bearbeitbare Bereiche in einer verwalteten Vorlage anzeigen](./assets/email-designer-governed-highlight.png){width="800" zoomable="yes"}

Sie können die gesperrten oder bearbeitbaren Elemente auch mithilfe des _Navigationsbaums“_. Klicken Sie auf _Navigationsbaum_-Symbol ( ![Verknüpfungssymbol](../assets/do-not-localize/icon-navigation-tree.svg) ) links neben der Arbeitsfläche, um die Baumstruktur anzuzeigen.

![Bearbeitbare Bereiche in einer verwalteten Vorlage anzeigen](./assets/email-designer-governed-tree.png){width="600" zoomable="yes"}

Die Symbole geben die angewendeten Einstellungen zum Sperren von Inhalten an.

| Symbol | Name | Beschreibung |
|------|------|-------------|
| ![Schreibgeschütztes Symbol](../assets/do-not-localize/icon-tree-lock.svg) | Schreibgeschützt | Die Komponente ist gesperrt und kann nicht bearbeitet werden. Wenn sie auf der Stammebene (_[!UICONTROL body]_) angewendet werden, sind alle untergeordneten Komponenten gesperrt und können nicht bearbeitet werden. |
| ![Symbol für Inhaltsbearbeitung](../assets/do-not-localize/icon-tree-content-lock.svg) | Inhaltssperre | Die Inhaltssperre wird auf Komponentenebene angewendet. |
| ![Bearbeitbares Symbol](../assets/do-not-localize/icon-edit.svg) | Bearbeitbar | Die Komponente kann vollständig bearbeitet werden. Sie können das Element jedoch möglicherweise nicht löschen. |
| ![Symbol für Inhaltsbearbeitung](../assets/do-not-localize/icon-tree-edit-text.svg) | Bearbeitbar - nur Inhalt | Komponente und Stil sind statisch, aber Sie können den Inhalt (z. B. Text oder Bild) ändern. |
