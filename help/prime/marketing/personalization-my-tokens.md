---
title: Benutzerdefinierte Token für Personalization
description: Erstellen und verwalten Sie benutzerdefinierte „Meine Token“ für die dynamische Personalisierung Ihrer Marketing-Artefakte - definieren Sie Text- und Zahlenvariablen für Programme in Journey Optimizer B2B Prime.
badgeBeta: label="Beta" type="informative" tooltip="Diese Funktion befindet sich derzeit in einer eingeschränkten Beta-Version"
autotag-review: '2026-06-23T15:59:01.024Z'
TQID: 'https://experienceleague.adobe.com/Pd79Nz-7texCFpD9Oq-UAHkfBodklt961aJcsTwsJPI'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: aed878b8-11d0-487c-828b-d23b2051ec37id: e666e996-b2cf-4c45-8fc2-1c625212abab
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1fid: bd3c685c-6c92-4a4a-becb-535cc25215de
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: ad5a67d291ffef797bb93f8b06f1bd8657efb67f
workflow-type: tm+mt
source-wordcount: 627
ht-degree: 5%

---

# Benutzerdefinierte Token für die Personalisierung

Die Inhaltspersonalisierung verwendet Token als Platzhalter oder Variablen, die beim Generieren des Inhaltsartefakts aufgefüllt werden. Standard-Personalisierungs-Token sind für E-Mails, Landingpages, Fragmente und Vorlagen verfügbar. Sie können auch einen Satz benutzerdefinierter Token mit Werten definieren, die für das Programm oder den Ordner spezifisch sind. Dieser Satz benutzerdefinierter Token wird als _Meine Token_ bezeichnet. Alle diese benutzerdefinierten Token dienen der Personalisierung.

Wenn Sie einer E-Mail ein benutzerdefiniertes Token hinzufügen, wird es als `{{my.TokenName}}` angezeigt. Beispielsweise könnten Sie `{{my.EventDate}}` oder `{{my.WebinarSpeaker}}` Token erstellen, um E-Mail-Inhalte im Zusammenhang mit kommenden Webinaren zu verwalten.

Zusätzlich zu _Meine Token_ die spezifisch für das Programm oder den Ordner sind, können Sie jedes der standardmäßigen (integrierten) Token für die Personalisierung verwenden.

## Zugriffstoken

1. Erweitern Sie in der linken Navigation **[!UICONTROL Marketing-Verwaltung]**.

1. Wählen Sie rechts in der **[!UICONTROL Marketing]**-Ressourcenliste **[!UICONTROL Programme]** aus.

1. Wenn Sie die Baumstruktur ändern, wählen Sie das Programm oder den Ordner aus, um die Details im mittleren Arbeitsbereich zu öffnen.

1. Klicken Sie auf die **[!UICONTROL Token]**.

   ![Registerkarte Token im ausgewählten Programm](./assets/program-tokens-tab.png){width="800" zoomable="yes"}

   Auf der Registerkarte werden alle benutzerdefinierten Token angezeigt, die im Ordner oder Programm definiert sind, sowie alle für übergeordnete Ordner oder Programme definierten.

### Tokentypen {#my-tokens}

Die _Meine Token_ sind benutzerdefinierte Variablen, die Sie für ein Programm oder einen Ordner erstellen oder ändern. Dieser benutzerdefinierte Token-Satz unterstützt die folgenden Token-Typen:

| Token-Typ | Beschreibung |
| ---------- | ----------- |
| Text | Dieser Typ enthält eine standardmäßige Textzeichenfolge. Die Größenbeschränkung für Text-Token beträgt 524.288 Zeichen (UTF-8) oder 2 MB. |
| Datum | Dieser Typ enthält einen Datumswert. Das Datum wird als Monat-Tag-Jahr angezeigt (z. B. 09-23-2026). |
| Datum und Uhrzeit | Dieser Typ enthält einen Datums- und Uhrzeitwert. |
| Zahl | Dieser Typ enthält einen ganzzahligen Standardwert. |
| E-Mail | Dieser Typ enthält eine gültige E-Mail-Adresse. |
| Ergebnis | Verwenden Sie dieses Token, um die Punktzahl für einen Journey-Aktionsknoten zu ändern. |
| Boolesch | Dieser Typ enthält den booleschen Standardwert true oder false. |
| RTF | Dieser Typ enthält formatierten Text. |

### Token-Verschachtelung

Wenn Sie ein Token in einem Programm oder Ordner erstellen, ist es für Verweise durch andere untergeordnete Objekte verfügbar.

* Lokales Token - Das Token wird im selben Programm oder Ordner definiert.
* Vererbtes Token - Das Token wird in einem übergeordneten Programm oder Ordner definiert und liegt eine oder mehrere Ebenen über dem aktuellen Programm oder Ordner.
* Überschriebenes Token - Das Token wird in einem übergeordneten Programm oder Ordner definiert, aber im aktuellen Programm oder Ordner wird ein anderer Wert definiert. Der Token-Status ändert sich in _Überschrieben_ und alle untergeordneten Ordner, Programme und Marketing-Artefakte übernehmen den neuen Wert.

![Token-Typen und Vererbung](./assets/program-tokens-inherited-overridden.png){width="600" zoomable="yes"}

### Erstellen eines Tokens

1. Klicken Sie auf der _[!UICONTROL Token]_-Registerkarte auf **[!UICONTROL Erstellen]**.

1. Geben Sie im Dialogfeld den **[!UICONTROL Namen]** für das Token ein.

   ![Geben Sie einen Namen und einen Wert für das Text-Token ein](./assets/token-create-dialog.png){width="400"}

   Sie können im Token-Namen keine Leerzeichen oder Sonderzeichen verwenden. Sie können _Binnenmajuskel-Schreibweise_ wie `EventType` verwenden, um einen Namen mit mehreren Wörtern zu verwenden, der leicht zu identifizieren ist.

1. Wählen Sie den **[!UICONTROL Typ]** für das Token.

1. Legen Sie den **[!UICONTROL Wert]** für das Token fest.

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

### Token bearbeiten

Sie können den Wert für jedes der definierten „Meine Token“ bearbeiten. Überschreiben Sie so den Wert für ein geerbtes Token.

<!-- (How does this affect live person journeys? ) -->

1. Klicken Sie auf _[!UICONTROL Token]_ auf das Symbol _Bearbeiten_ neben dem Token-Namen.

1. Ändern Sie im Feld den Wert nach Bedarf.

   ![Ändern Sie den Namen und den Wert für das Token](../../user/content/assets/my-tokens-edit-text-token-dialog.png){width="400"}

1. Klicken Sie auf das _Speichern_-Symbol.

### Token löschen

Sie können ein benutzerdefiniertes Token aus der Liste löschen, wenn es derzeit nicht zum Journey von E-Mail-Inhalten verwendet wird.

1. Klicken Sie auf _[!UICONTROL Token]_ auf das Symbol _Löschen_ neben dem Token-Namen.

1. Klicken Sie im Bestätigungsdialog auf **[!UICONTROL Löschen]**.

<!--

## Use custom tokens in your content

When you are authoring email content for your programs, you can use any of the tokens from the _My Tokens_ list when you use the personalization tools in the visual design space.

1. Select the text component and click the _Add personalization_ ( ![Add personalization icon](../../assets/do-not-localize/icon-personalization-field.svg) ) icon in the toolbar.

   ![Click the Add personalization icon](../../user/content/assets/email-personalize-text.png){width="600"}

   This action opens the _Edit Personalization_ dialog. The dialog includes a _[!UICONTROL My tokens]_ folder in the _[!UICONTROL Personalization Tokens]_ library if there are custom tokens defined for the account journey.

1. To add one of your custom tokens to the blank space, expand the **[!UICONTROL My tokens]** folder, then click **+** or **...**.

   You can add any additional static text as needed.

   ![Construct personalized text using My tokens](../../user/content/assets/personalization-edit-dialog-my-tokens.png){width="700" zoomable="yes"}

1. Click **[!UICONTROL Save]**.

-->
