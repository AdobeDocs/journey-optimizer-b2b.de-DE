---
title: Erstellen von Fragmenten
description: Erstellen wiederverwendbarer Inhaltsfragmente mit visuellen Design-Tools - Hinzufügen von Struktur, Assets, Personalisierung, bedingten Inhalten und Linktracking-URLs für E-Mails und Vorlagen in Journey Optimizer B2B Prime.
badgeBeta: label="Beta" type="informative" tooltip="Diese Funktion ist Teil einer eingeschränkten Beta-Version."
autotag-review: '2026-07-13T16:38:09.506Z'
TQID: 'https://experienceleague.adobe.com/Zn5L6Bc3x8SuGyjOPDdTWI-oxrrhk06a2f8ZvX2SN4s'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: aed878b8-11d0-487c-828b-d23b2051ec37id: e666e996-b2cf-4c45-8fc2-1c625212abab
subfeature_v2: id: e1663313-7961-4100-bea9-fa9f4edf8493id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 5206ed7bc0ce24e65700da28b023d76c68cb6419
workflow-type: tm+mt
source-wordcount: 215
ht-degree: 4%

---

# Erstellen von Fragmenten

Nachdem Sie [ein Fragment erstellt haben](./fragments.md#create-fragments) verwenden Sie den visuellen Design-Bereich, um die Struktur- und Inhaltskomponenten in Ihrem Fragment zu erstellen.

## Hinzufügen von Struktur und Inhalten {#design-fragment}

{{$include /help/_includes/content-design-components-prime.md}}

## Hinzufügen von Assets {#add-assets}

Wählen Sie im visuellen Design-Bereich das Symbol _Assets_ ( ![Assets-Symbol](../../assets/do-not-localize/icon-assets-me.svg) ) in der linken Navigationsleiste aus, um Bild-Assets in der [!DNL Journey Optimizer B2B Prime] Asset-Bibliothek zu suchen und auszuwählen.

Anweisungen zum Auswählen, Ersetzen oder Hochladen von Bild-Assets finden Sie unter [Verwenden von Assets für die Inhaltserstellung](./digital-asset-management.md#assets-authoring).

## Navigieren in den Ebenen, Einstellungen und Stilen {#navigate-layers-settings-styles}

{{$include /help/_includes/content-design-navigation.md}}

## Personalisieren von Inhalten {#personalize-content}

[!DNL Journey Optimizer B2B Prime] verwendet die Handlebars-Syntax für die Personalisierung. Token werden zum Zeitpunkt des Versands durch Werte aus den Profildaten jedes Empfängers ersetzt.

_Personalisierung hinzufügen :_

1. Wählen Sie die Textkomponente aus und klicken Sie auf das Symbol _Personalisierung hinzufügen_ ( ![Personalisierungssymbol](../../user/assets/do-not-localize/icon-personalize.svg) ) in der Symbolleiste.
1. Durchsuchen Sie im Personalisierungsdialog die Schemastruktur auf der linken Seite und wählen Sie ein Profilattribut aus. Der Editor fügt den entsprechenden Handlebars-Ausdruck ein, z. B. `{{profile.firstName}}`.
1. Fügen Sie bei Bedarf einen Fallback-Wert hinzu, um fehlende Daten zu verarbeiten - z. B. `{{profile.firstName | default: "there"}}`.
1. Klicken Sie **[!UICONTROL Bestätigen]** oder **[!UICONTROL Einfügen]**. Der Ausdruck wird inline im Feld angezeigt.

Weitere Informationen zu den Tools und der Syntax des Ausdruckseditors finden Sie unter [Personalization-Editor](./personalization-expressions.md).

## Verknüpftes URL-Tracking bearbeiten {#edit-linked-url-tracking}

{{$include /help/_includes/content-design-links.md}}
