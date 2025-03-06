---
title: Erstellen von Fragmenten
description: Erfahren Sie, wie Sie Inhaltsfragmente erstellen, die für Ihre E-Mails und Vorlagendesigns wiederverwendet werden können, um die Effizienz zu steigern und Design- und Branding-Standards zu gewährleisten.
feature: Content
source-git-commit: 1f551b636ef347fd65aa39a809dedba8372c3ac4
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 14%

---

# Erstellen von Fragmenten

Nachdem Sie [ein Fragment erstellt haben](./fragments.md#create-fragments) verwenden Sie den Visual Editor, um die Struktur- und Inhaltskomponenten in Ihrem Fragment zu erstellen.

## Hinzufügen von Struktur und Inhalten {#design-fragment}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_fragment"
>title="Hinzufügen von Strukturkomponenten"
>abstract="Strukturkomponenten definieren das Layout des Fragments. Ziehen Sie eine **Struktur**-Komponente per Drag-and-Drop auf die Arbeitsfläche, um mit der Gestaltung Ihres Fragmentinhalts zu beginnen."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_fragment"
>title="Über Inhaltskomponenten"
>abstract="Inhaltskomponenten sind leere Platzhalter für Inhalte, mit denen Sie das Layout eines Fragments erstellen können."

{{$include /help/_includes/content-design-components.md}}

## Hinzufügen von Assets

{{$include /help/_includes/content-design-assets.md}}

## Navigieren in den Ebenen, Einstellungen und Stilen

{{$include /help/_includes/content-design-navigation.md}}

## Inhalt personalisieren

{{$include /help/_includes/content-design-personalization.md}}

## Benutzerdefinierte Felder aktivieren

Wenn ein E-Mail- oder E-Mail-Vorlagenautor das Fragment hinzufügt, ist der Fragmentinhalt standardmäßig gesperrt. Alle Änderungen am veröffentlichten Fragment werden automatisch auf alle Inhalts-Assets übertragen, in denen das Fragment verwendet wird. Wenn Sie einen Parameter für eine Komponente im Fragment als bearbeitbar festlegen, kann der E-Mail- oder Vorlagenautor einen benutzerdefinierten Feldwert angeben, der speziell für seine Anforderungen gilt. Dieses Anpassungsflag ist auf visuelle Bild-, Text- und Schaltflächen-Komponenten beschränkt.

Wenn Sie beispielsweise ein wiederverwendbares Banner mit einer anklickbaren Schaltfläche entwerfen, können Sie den URL-Parameter für die Schaltfläche als bearbeitbar festlegen. E-Mail-Autoren können dann eine URL verwenden, die spezifischer für ihre E-Mail-Kampagne ist. Mit diesen anpassbaren Feldern können Marketing-Experten Inhalte verwalten und personalisieren, ohne völlig neue Inhaltsbausteine erstellen oder die vom ursprünglichen Fragment übernommenen Aktualisierungen unterbrechen zu müssen.

1. Wählen Sie im visuellen Inhaltseditor das Bild, den Text oder das Schaltflächenelement aus, für das Sie die Anpassung aktivieren möchten.

1. Wählen Sie in den Komponentendetails auf der rechten Seite die Registerkarte **[!UICONTROL Bearbeitbare Felder]** aus.

1. Klicken Sie auf **[!UICONTROL Umschalter für die Option]** Bearbeitung aktivieren“ und legen Sie die bearbeitbaren Felder fest.

   ![Bearbeitbare Felder für eine Fragmentbildkomponente aktivieren](./assets/fragment-editable-fields-image.png){width="700" zoomable="yes"}

   Sie können die Anpassung für die angezeigten Felder aktivieren, die vom Komponententyp und den im Fragment definierten Parametern abhängen.

   Ändern Sie den Umschalter für jedes Feld, in dem Sie eine Anpassung zulassen möchten, in einen aktivierten Status.

1. Klicken Sie **[!UICONTROL Übersicht]**, um alle bearbeitbaren Felder und ihre Standardwerte zu überprüfen.

   ![Überprüfen Sie die bearbeitbaren Felder und ihre Standardwerte](./assets/fragment-editable-fields-image-overview.png){width="700" zoomable="yes"}

1. Speichern Sie Ihre Änderungen.

## Verknüpftes URL-Tracking bearbeiten

{{$include /help/_includes/content-design-links.md}}
