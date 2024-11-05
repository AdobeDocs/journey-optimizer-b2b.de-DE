---
title: Vorlagen-Content-Governance
description: Erfahren Sie, wie Sie Inhaltselemente in Ihren E-Mail-Vorlagen sperren können, damit Sie steuern können, wie sie zur Verwendung in Konto-Journey verändert werden können.
feature: Email Authoring, Content
source-git-commit: 44413c763ca57d04b83ba78df0ae846142180ec3
workflow-type: tm+mt
source-wordcount: '763'
ht-degree: 0%

---

# Verwaltung von Vorlageninhalten

In vielen Marketingorganisationen entwerfen Inhaltsexperten E-Mail-Kampagnen. Ein bestimmtes Design kann als Grundlage für benutzerdefinierte Konto-Journey im gesamten Unternehmen verwendet werden. Um die Einhaltung genehmigter Inhaltsentwürfe sicherzustellen, können Sie mithilfe der Inhaltsverwaltungsfunktionen Vorlagenkomponenten sperren. Wenn die Inhaltssperrung in der E-Mail-Vorlage aktiviert ist, können Marketer nur die zulässigen Elemente ändern, um sie an der Inhaltsstrategie auszurichten.

Sie können beispielsweise die Kopf- und Fußzeile sperren, die für die Kontinuität der Markenkommunikation konzipiert ist. Sie können auch die Spalte sperren, die den Hauptteilabschnitt enthält, aber Autoren die Möglichkeit geben, den Journey-Text so zu ändern, dass er dem Zweck des Kontos entspricht.

## Aktivieren der Inhaltsverwaltung für die Vorlage

Nachdem Sie den visuellen Designer zum [Erstellen der Struktur- und Inhaltskomponenten](./email-template-authoring.md) für Ihre E-Mail-Vorlage verwendet haben, aktivieren Sie Governance und wenden Sie bei Bedarf spezifische Inhaltssperren an.

1. Greifen Sie im Visual Designer mithilfe des _Navigationsbaums_ auf die Ebenen/Container und Elemente zu.

   Klicken Sie auf das Symbol _Navigationsbaum_ ( ![Verknüpfungssymbol](../assets/do-not-localize/icon-navigation-tree.svg) ) links neben der Arbeitsfläche, um den Baum anzuzeigen.

1. Wählen Sie in der Struktur die Stammkomponente **[!UICONTROL Hauptteil]** aus.

   Im Eigenschaftenbereich rechts neben der Arbeitsfläche wird standardmäßig die Registerkarte _[!UICONTROL Einstellungen]_ angezeigt.

1. Aktivieren Sie die Option **[!UICONTROL Governance]** .

   ![Aktivieren der Governance für eine E-Mail-Vorlage](./assets/governance-template-enable.png){width="800" zoomable="yes"}

   Wenn diese Option aktiviert ist, ist der standardmäßige _[!UICONTROL Modus]_ **[!UICONTROL Schreibgeschützt]**. Wenn dieser Modus auf der Stammebene festgelegt ist, werden alle Elemente in der Vorlage gesperrt. In der Baumstruktur auf der linken Seite wird das Symbol _Schreibgeschützt_ ( ![Schreibgeschütztes Symbol](../assets/do-not-localize/icon-tree-lock.svg) ) neben dem Stamm und allen untergeordneten Elementen angezeigt.

1. Um bestimmte Inhalte innerhalb der Vorlage zu sperren, ändern Sie den **[!UICONTROL Modus]** in **[!UICONTROL Inhaltssperrung]**.

   Wenn dieser Modus auf der Stammebene festgelegt ist, werden alle Elemente in der Vorlage entsperrt. In der Baumstruktur auf der linken Seite wird das Symbol _Inhaltssperrung_ ( ![Symbol für Inhaltssperrung](../assets/do-not-localize/icon-tree-content-lock.svg) ) neben dem Stammelement angezeigt. Wenden Sie bei Bedarf die Inhaltssperrung auf die enthaltenen (strukturellen) und individuellen Inhaltskomponenten an.

   Aktivieren Sie die Option **[!UICONTROL Content-Addition aktivieren]**, damit Journey-E-Mail-Autoren Struktur- oder Inhaltselemente hinzufügen können. Wählen Sie die Art der Ergänzungen aus, die Sie zulassen möchten:

   * **[!UICONTROL Hinzufügen von Struktur und Inhalt zulassen]** - Wählen Sie diese Option, wenn Sie Autoren erlauben möchten, sowohl Struktur- als auch Inhaltselemente hinzuzufügen.

   * **[!UICONTROL Nur Inhaltsangebot zulassen]** - Wählen Sie diese Option, wenn Sie zulassen möchten, dass Autoren nur Inhaltselemente hinzufügen können.

   ![Aktivieren von Inhaltszusätzen](./assets/governance-template-content-additions.png){width="600" zoomable="yes"}

   Wenn dieser Modus auf der Stammebene festgelegt ist, werden alle Elemente in der Vorlage gesperrt. In der Baumstruktur auf der linken Seite wird das Symbol _Schreibgeschützt_ ( ![Schreibgeschütztes Symbol](../assets/do-not-localize/icon-tree-lock.svg) ) neben dem Stamm und allen untergeordneten Elementen angezeigt.
<!-- 

   
- ![Link icon](../assets/do-not-localize/icon-navigation-tree.svg)
- ![Read only icon](../assets/do-not-localize/icon-tree-lock.svg)
- ![Content edit icon](../assets/do-not-localize/icon-tree-content-lock.svg)
- ![Content edit icon](../assets/do-not-localize/icon-tree-edit-text.svg)
- ![Edit element](../assets/do-not-localize/icon-edit.svg) -->

## Anwenden von Sperren auf eine Struktur

Planen Sie mithilfe des strukturellen Vererbungsmodells das Layout und die Struktur Ihrer E-Mail-Vorlage entsprechend der gewünschten Governance. Verwenden Sie die Strukturkomponenten als Container, um Elemente so zu gruppieren, dass sie einfach als gesperrt oder bearbeitbar gekennzeichnet werden können. Wenn der E-Mail-Vorlagenentwurf eingerichtet ist, überprüfen Sie die Struktur und wenden Sie die Sperrfunktionen gemäß Ihrem Plan an.

Wenn Sie einen Sperrtyp auf Strukturebene anwenden, erhalten Sie eine Standardeinstellung für die untergeordneten Komponenten. Anschließend können Sie bei Bedarf eine bestimmte Sperreinstellung auf Spalten- oder Inhaltselementebene anwenden.

1. Klicken Sie auf das Symbol _Navigationsbaum_ ( ![Verknüpfungssymbol](../assets/do-not-localize/icon-navigation-tree.svg) ) links neben der Arbeitsfläche, um den Baum anzuzeigen.

1. Wählen Sie die Struktur im Baum aus.

   Im Eigenschaftenbereich rechts neben der Arbeitsfläche wird standardmäßig die Registerkarte _[!UICONTROL Einstellungen]_ angezeigt.

1. Legen Sie den **[!UICONTROL Sperrtyp]** fest:

   * **[!UICONTROL Gesperrt]** - Mit dieser Einstellung sind alle untergeordneten Komponenten standardmäßig gesperrt. In der Baumstruktur auf der linken Seite wird das Symbol _Schreibgeschützt_ ( ![Schreibgeschütztes Symbol](../assets/do-not-localize/icon-tree-lock.svg) ) neben allen untergeordneten Komponenten angezeigt.

   * **[!UICONTROL Bearbeitbar]** - Mit dieser Einstellung sind alle untergeordneten Komponenten standardmäßig bearbeitbar. In der Baumstruktur auf der linken Seite werden neben den untergeordneten Komponenten keine Symbole angezeigt.

   ![Anwenden der Inhaltssperrung auf eine Strukturkomponente](./assets/governance-template-structure-locking.png){width="800" zoomable="yes"}

## Festlegen der Sperrung für eine untergeordnete Komponente

1. Wählen Sie die Komponente im Baum aus.

   Im Eigenschaftenbereich rechts neben der Arbeitsfläche wird standardmäßig die Registerkarte _[!UICONTROL Einstellungen]_ angezeigt.

1. Aktivieren Sie die Option **[!UICONTROL Spezifisches Sperren verwenden]** .

1. Wählen Sie den anzuwendenden Governance-Typ aus:

   * **[!UICONTROL Bearbeitbar]** - Ermöglicht die vollständige redaktionelle Kontrolle der Komponente beim E-Mail-Authoring.
   * **[!UICONTROL Nur bearbeitbarer Inhalt]** - Ermöglicht es E-Mail-Autoren, den Inhalt zu ändern, nicht jedoch die Komponente selbst.
   * **[!UICONTROL Gesperrt]** - Verhindert alle Änderungen an der Komponente während des E-Mail-Authoring.

     Bei gesperrten Komponenten können Sie das Entfernen der Komponente während des E-Mail-Authoring zulassen, indem Sie die Option **[!UICONTROL Löschen zulassen]** aktivieren.

   ![Anwenden der Inhaltssperrung auf eine untergeordnete Komponente](./assets/governance-template-component-locking.png){width="800" zoomable="yes"}

