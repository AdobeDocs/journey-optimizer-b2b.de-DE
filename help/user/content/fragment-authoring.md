---
title: Erstellen von Fragmenten
description: Erstellen wiederverwendbarer Inhaltsfragmente mit visuellen Design-Tools - Hinzufügen von Komponenten, Personalisierung, bedingten Inhalten und anpassbaren Feldern für E-Mails und Vorlagen in Journey Optimizer B2B edition.
feature: Fragments, Content Design Tools
role: User
exl-id: d29754cf-6721-489c-bff8-cde034456db2
autotag-review: '2026-05-27T16:13:22.974Z'
TQID: 'https://experienceleague.adobe.com/WqMj4DVOmUd3s-r-n9bSyRjXSGS8sDWMFNh5wfOiE2Y'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: e666e996-b2cf-4c45-8fc2-1c625212abab
subfeature_v2: id: e1663313-7961-4100-bea9-fa9f4edf8493
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: a09a5a04-e30b-4d55-b031-38e6f5ec86dbid: e0eb8757-182f-49f3-94a4-1587d16f5094id: f5c2a4bb-71ca-4d7e-8efd-442250e6ba48
source-git-commit: 955fac784a8f438ec2f9aaf66e9aaeefda58e2a7
workflow-type: tm+mt
source-wordcount: 391
ht-degree: 6%

---

# Erstellen von Fragmenten

Nachdem Sie [ein Fragment erstellt haben](./fragments.md#create-fragments) verwenden Sie den visuellen Design-Bereich, um die Struktur- und Inhaltskomponenten in Ihrem Fragment zu erstellen.

## Hinzufügen von Struktur und Inhalten {#design-fragment}

{{$include /help/_includes/content-design-components.md}}

## Hinzufügen von Assets

{{$include /help/_includes/content-design-assets.md}}

## Navigieren in den Ebenen, Einstellungen und Stilen

{{$include /help/_includes/content-design-navigation.md}}

## Personalisieren von Inhalten

{{$include /help/_includes/content-design-personalization.md}}

## Bedingte Inhalte

Um bedingte Inhalte hinzuzufügen, die den Inhalt auf der Grundlage von Regeln an die Zielprofile anpassen, wählen Sie eine Inhaltskomponente aus und klicken Sie auf die Schaltfläche **[!UICONTROL Bedingten Inhalt aktivieren]** in der Komponenten-Symbolleiste. Wenn das veröffentlichte Fragment in einer E-Mail-Nachricht enthalten ist, bestimmen die bedingten Regeln die Variante einer bedingten Komponente, die in der E-Mail-Nachricht gerendert wird.

Weitere Informationen finden Sie unter [_Bedingter Inhalt_](./conditional-content.md).

## Aktivieren der Fragmentanpassung

Wenn ein Autor ein Fragment zu einer [E-](./email-authoring.md#content-authoring---use-visual-fragments) oder [E-Mail-Vorlage](./email-template-authoring.md#content-authoring---use-visual-fragments) hinzufügt, ist der Fragmentinhalt standardmäßig gesperrt. Alle Änderungen am veröffentlichten Fragment werden automatisch auf alle Inhalts-Assets übertragen, in denen das Fragment verwendet wird. Wenn Sie einen Parameter für eine Komponente im Fragment als bearbeitbar festlegen, kann der E-Mail- oder Vorlagenautor einen benutzerdefinierten Feldwert angeben, der speziell für seine Anforderungen gilt. Diese Anpassungsmarkierung ist auf visuelle Bild-, Text- und Schaltflächenkomponenten beschränkt.

Wenn Sie beispielsweise ein wiederverwendbares Banner mit einer anklickbaren Schaltfläche entwerfen, können Sie den URL-Parameter für die Schaltfläche als bearbeitbar festlegen. E-Mail-Autoren können dann eine URL verwenden, die spezifischer für ihre E-Mail-Kampagne ist. Mit diesen anpassbaren Feldern können Marketing-Experten wiederverwendbare Inhalte verwalten und personalisieren, ohne völlig neue Inhaltsbausteine erstellen oder die vom ursprünglichen Fragment übernommenen Aktualisierungen unterbrechen zu müssen.

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
