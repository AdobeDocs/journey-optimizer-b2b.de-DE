---
title: Vorlagen-Content-Governance
description: 'Sperren von E-Mail-Vorlagenkomponenten für die Markenkonformität : Legen Sie Governance-Modi fest, steuern Sie die Inhaltsbearbeitung und verwalten Sie Berechtigungen für Konto-Journey-Autoren in Journey Optimizer B2B edition.'
feature: Templates, Email Authoring, Content
role: User
exl-id: 0cf852cd-491c-4478-8d5e-51fd2cc2625a
source-git-commit: 79012352c3ae4e2f3d38b632b1f523d262f74f96
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 0%

---

# Vorlagen-Content-Governance

In vielen Marketing-Organisationen gibt es Content-Experten, die E-Mail-Kampagnen entwerfen. Ein bestimmtes Design kann als Grundlage für benutzerdefinierte Account-Journey im gesamten Unternehmen verwendet werden. Um die Einhaltung genehmigter Inhaltsentwürfe sicherzustellen, können Sie Inhaltssteuerungsfunktionen zum Sperren von Vorlagenkomponenten verwenden. Wenn die Inhaltssperre in der E-Mail-Vorlage aktiviert ist, können Marketing-Experten nur die zulässigen Elemente ändern, um sie an die Inhaltsstrategie anzupassen.

Beispielsweise können Sie die Kopf- und Fußzeile sperren, die für die Kontinuität der Markenkommunikation konzipiert ist. Sie können auch die Spalte sperren, die den Haupttextabschnitt enthält, Autorinnen und Autoren jedoch erlauben, den Text so zu ändern, dass er ihren Zweck im Account-Journey-Design erfüllt.

## Aktivieren der Content Governance für die Vorlage

Nachdem Sie den visuellen Design-Bereich verwendet haben[ um die Struktur- und Inhaltskomponenten für ](./email-template-authoring.md) E-Mail-Vorlage zu erstellen, aktivieren Sie die Governance und wenden Sie bei Bedarf eine spezifische Inhaltssperrung an.

1. Greifen Sie im visuellen Entwurfsbereich mithilfe des Navigationsbaums auf die Ebenen/Container _Elemente_.

   Klicken Sie auf _Navigationsbaum_-Symbol ( ![Verknüpfungssymbol](../assets/do-not-localize/icon-navigation-tree.svg) ) links neben der Arbeitsfläche, um die Baumstruktur anzuzeigen.

1. Wählen Sie in der Baumstruktur die **[!UICONTROL &quot;]**&quot; aus.

   Das Eigenschaftenbedienfeld rechts neben der Arbeitsfläche zeigt standardmäßig die Registerkarte _[!UICONTROL Einstellungen]_ an.

1. Aktivieren Sie die **[!UICONTROL Governance]**-Option.

   ![Aktivieren der Governance für eine E-Mail-Vorlage](./assets/governance-template-enable.png){width="800" zoomable="yes"}

   Wenn diese Option aktiviert ist, ist der _[!UICONTROL Modus]_ standardmäßig **[!UICONTROL Schreibgeschützt]**. Wenn dieser Modus auf der Stammebene festgelegt ist, werden alle Elemente in der Vorlage gesperrt. In der Baumstruktur auf der linken Seite wird das _Schreibgeschützt_-Symbol ( ![Schreibgeschütztes Symbol](../assets/do-not-localize/icon-tree-lock.svg) ) neben dem Stamm und allen untergeordneten Elementen angezeigt.

1. Um eine bestimmte Inhaltssperre innerhalb der Vorlage zu aktivieren, ändern Sie **[!UICONTROL Modus]** in **[!UICONTROL Inhaltssperre]**.

   Wenn dieser Modus auf der Stammebene festgelegt ist, werden alle Elemente in der Vorlage entsperrt. In der Baumstruktur auf der linken Seite wird das Symbol _Inhaltssperrung_ ( ![Inhaltssperrsymbol](../assets/do-not-localize/icon-tree-content-lock.svg) ) neben dem Stammelement angezeigt. Wenden Sie die Inhaltssperrung nach Bedarf auf enthaltende (strukturelle) und individuelle Inhaltskomponenten an.

   Um E-Mail-Journey-Autoren das Hinzufügen von Struktur- oder Inhaltselementen zu ermöglichen, aktivieren Sie **[!UICONTROL Inhaltshinzufügen aktivieren]**. Wählen Sie die Art der Hinzufügungen aus, die Sie zulassen möchten:

   * **[!UICONTROL Struktur und Inhaltshinzufügen zulassen]** - Wählen Sie diese Option aus, wenn Sie Autorinnen und Autoren das Hinzufügen sowohl von Struktur- als auch von Inhaltselementen ermöglichen möchten.

   * **[!UICONTROL Nur Inhaltshinzufügen zulassen]** - Wählen Sie diese Option aus, wenn Sie Autoren erlauben möchten, nur Inhaltselemente hinzuzufügen.

   ![Inhaltszusätze aktivieren](./assets/governance-template-content-additions.png){width="600" zoomable="yes"}

   Wenn dieser Modus auf der Stammebene festgelegt ist, werden alle Elemente in der Vorlage gesperrt. In der Baumstruktur auf der linken Seite wird das _Schreibgeschützt_-Symbol ( ![Schreibgeschütztes Symbol](../assets/do-not-localize/icon-tree-lock.svg) ) neben dem Stamm und allen untergeordneten Elementen angezeigt.
<!-- 

   
- ![Link icon](../assets/do-not-localize/icon-navigation-tree.svg)
- ![Read only icon](../assets/do-not-localize/icon-tree-lock.svg)
- ![Content edit icon](../assets/do-not-localize/icon-tree-content-lock.svg)
- ![Content edit icon](../assets/do-not-localize/icon-tree-edit-text.svg)
- ![Edit element](../assets/do-not-localize/icon-edit.svg) -->

## Anwenden von Sperren auf eine Struktur

Planen Sie mithilfe des strukturellen Vererbungsmodells das Layout und die Struktur Ihrer E-Mail-Vorlage entsprechend der Governance, die Sie anwenden möchten. Verwenden Sie die Strukturkomponenten als Container, um Elemente so zu gruppieren, dass sie leicht als gesperrt oder bearbeitbar gekennzeichnet werden können. Wenn der E-Mail-Vorlagenentwurf eingerichtet ist, überprüfen Sie die Struktur und wenden Sie Sperrfunktionen entsprechend Ihrem Plan an.

Wenn Sie einen Sperrtyp auf der Strukturebene anwenden, wird eine Standardeinstellung für die untergeordneten Komponenten bereitgestellt. Sie können dann bei Bedarf eine bestimmte Sperreinstellung auf Spalten- oder Inhaltselementebene anwenden.

1. Klicken Sie auf _Navigationsbaum_-Symbol ( ![Verknüpfungssymbol](../assets/do-not-localize/icon-navigation-tree.svg) ) links neben der Arbeitsfläche, um die Baumstruktur anzuzeigen.

1. Wählen Sie die Struktur im Baum aus.

   Das Eigenschaftenbedienfeld rechts neben der Arbeitsfläche zeigt standardmäßig die Registerkarte _[!UICONTROL Einstellungen]_ an.

1. Legen Sie den **[!UICONTROL Sperrtyp]** fest:

   * **[!UICONTROL Gesperrt]** - Mit dieser Einstellung sind alle untergeordneten Komponenten standardmäßig gesperrt. In der Baumstruktur auf der linken Seite wird das _Schreibgeschützt_-Symbol ( ![Schreibgeschütztes Symbol](../assets/do-not-localize/icon-tree-lock.svg) ) neben allen untergeordneten Komponenten angezeigt.

   * **[!UICONTROL Bearbeitbar]** - Mit dieser Einstellung können alle untergeordneten Komponenten standardmäßig bearbeitet werden. In der Baumstruktur auf der linken Seite werden keine Symbole neben den untergeordneten Komponenten angezeigt.

   ![Wenden Sie Inhaltssperren auf eine Strukturkomponente an](./assets/governance-template-structure-locking.png){width="800" zoomable="yes"}

## Festlegen der Sperrung für eine untergeordnete Komponente

1. Wählen Sie die Komponente im Navigationsbaum aus.

   Das Eigenschaftenbedienfeld rechts neben der Arbeitsfläche zeigt standardmäßig die Registerkarte _[!UICONTROL Einstellungen]_ an.

1. Aktivieren Sie **[!UICONTROL Option „Spezifische Sperre verwenden]**.

1. Wählen Sie die Art der anzuwendenden Governance:

   * **[!UICONTROL Bearbeitbar]** - Ermöglicht die vollständige redaktionelle Kontrolle der Komponente beim E-Mail-Authoring.
   * **[!UICONTROL Nur bearbeitbare Inhalte]** - Ermöglicht E-Mail-Autoren das Ändern des Inhalts, aber nicht der Komponente selbst.
   * **[!UICONTROL Gesperrt]** - Verhindert Änderungen an der Komponente während des E-Mail-Authorings.

     Bei gesperrten Komponenten können Sie das Entfernen der Komponente während der E-Mail-Bearbeitung zulassen, indem Sie die Option **[!UICONTROL Löschen zulassen]** aktivieren.

   ![Wenden Sie die Inhaltssperre auf eine untergeordnete Komponente an](./assets/governance-template-component-locking.png){width="800" zoomable="yes"}
