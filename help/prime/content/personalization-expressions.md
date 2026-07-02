---
title: Personalization-Editor
description: Erfahren Sie, wie Sie mit dem Personalisierungseditor in Journey Optimizer B2B Prime Profilattribut-Token in E-Mails, WhatsApp-Nachrichten, Landingpages und URL-Feldern auswählen, anordnen, anpassen und validieren können.
badgeBeta: label="Beta" type="informative" tooltip="Diese Funktion ist Teil einer eingeschränkten Beta-Version."
feature: Content Design Tools
role: User
autotag-review: '2026-06-20T00:27:51.436Z'
TQID: 'https://experienceleague.adobe.com/ctl7dFJmmm1A4HtB-g2nTx37f4-A8GTUfWhLhdIq7DM'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: e666e996-b2cf-4c45-8fc2-1c625212ababid: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1fid: bd3c685c-6c92-4a4a-becb-535cc25215de
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 205013add5060318d46a2b048bb347003c167470
workflow-type: tm+mt
source-wordcount: 1015
ht-degree: 55%

---

# Personalisierungseditor

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_personalization_editor"
>title="Über den Personalisierungseditor"
>abstract="Mit dem Personalisierungseditor können Sie Profilattribute auswählen, anordnen, anpassen und validieren, um personalisierte Inhalte zu erstellen."

Der Personalisierungseditor ist das Herzstück der Personalisierung in [!DNL Journey Optimizer B2B Prime]. Verwenden Sie sie überall dort, wo Sie dynamische Inhalte benötigen - in E-Mails, WhatsApp-Nachrichten, Landingpages und URL-Feldern.

In der Benutzeroberfläche des Personalisierungseditors können Sie Profilattribute auswählen, anordnen, anpassen und validieren, um personalisierte Inhalte zu erstellen.

![Ausdruckseditor für Personalisierung](./assets/personalization-editor.png){width="700" zoomable="yes"}

>[!NOTE]
>
>In dieser Beta-Version sind im Personalisierungseditor nur Profilattribute verfügbar. Personalisierung auf Kontoebene und Daten über benutzerdefinierte Objekte sind nicht verfügbar. Siehe [Aktuelle Einschränkungen](../marketing/email-channel.md#limitations).

Sie können Personalisierung in jedem Feld mit dem Symbol _Personalisieren_ ( ![Personalisierungssymbol](../../user/assets/do-not-localize/icon-personalize.svg) ) hinzufügen. Erweitern Sie die folgenden Abschnitte für weitere Details.

+++E-Mails und WhatsApp-Nachrichten

In [E](./email-authoring.md#personalize-content)Mails und [WhatsApp-Nachrichten](./whatsapp-authoring.md#personalize-message-content) kann die Personalisierung an verschiedenen Stellen hinzugefügt werden, wie z. B. im Feld **[!UICONTROL Betreffzeile]** in einer E-Mail oder mit dynamischen Parametern in einer genehmigten WhatsApp-Vorlage.

Sie können sie auch in anderen Bereichen Ihres Inhalts hinzufügen, einschließlich E-Mail-Text, Preheadern und Schaltflächen-URLs.

+++

+++Inhaltsdesign-Bereich

Beim Bearbeiten visueller Inhalte können Sie die meisten Textelemente mithilfe des Symbols in der kontextuellen Symbolleiste personalisieren.

<!-- ![](assets/perso_insert.png) -->

+++

+++URLs

[!DNL Journey Optimizer B2B Prime] können Sie auch **URLs** in Ihren Nachrichten personalisieren. Personalisierte URLs führen Empfangende je nach den Profilattributen zu bestimmten Seiten einer Website oder zu einer personalisierten Microsite.

<!-- ![](assets/perso-url.png){width="50%"} -->

>[!NOTE]
>
>Die Personalisierung von URLs ist für diese Link-Typen verfügbar: **Externer Link**, **Abmelde-Link** und **Ausschluss**.

+++

+++E-Mail-Konfiguration

Beim Erstellen einer [E-Mail](../admin/email-channel-configuration.md)Kanalkonfiguration können Sie personalisierte Werte für Subdomains, Header und URL-Tracking-Parameter definieren.

+++

## Hinzufügen von Personalisierung {#add}

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_perso_editor_autocomplete"
>title="Automatisches Vervollständigen"
>abstract="Wenn diese Option über den Umschalter aktivieret ist, kann das System den Code während der Eingabe automatisch vervollständigen und Vorschläge unterbreiten. Diese Funktion ist nur für HTML- und Textformate verfügbar und unterstützt Profilattribute. Wenn die Option über den Umschalter deaktiviert wird, ermöglicht der Editor stattdessen die automatische Vervollständigung von nativem HTML-Code."

Im zentralen Arbeitsbereich erstellen Sie Ihre Personalisierungssyntax. Um ein Attribut zur Personalisierung Ihrer Nachricht zu verwenden, suchen Sie es im linken Navigationsbereich und klicken Sie auf die Schaltfläche `+`, um es zum Ausdruck hinzuzufügen.

<!-- ![](assets/personalization-add-attribute.png) -->

Über das Menü mit den Auslassungspunkten neben dem Symbol `+` können Sie weitere Details für jedes Attribut abrufen und Ihre am häufigsten verwendeten Attribute zu den Favoriten hinzufügen. Zu Favoriten hinzugefügte Attribute sind über das Menü **[!UICONTROL Favoriten]** im Navigationsbereich zugänglich.

>[!NOTE]
>
>Im Bereich „Attribute“ werden standardmäßig nur ausgefüllte Attribute angezeigt. Um alle Attribute anzuzeigen, wählen Sie die Schaltfläche **[!UICONTROL Einstellungen]** im Attributbereich und schalten Sie die Option **[!UICONTROL Nur ausgefüllte Attribute anzeigen]** aus.

Darüber hinaus können Sie einen standardmäßigen Fallback-Text definieren, der angezeigt wird, wenn ein Profilattribut vom Typ Zeichenfolge leer ist. Klicken Sie dazu auf die Schaltfläche mit den Auslassungspunkten neben dem Attribut und wählen Sie **[!UICONTROL Einfügen mit Fallback-Text]**. Schreiben Sie den Text, der standardmäßig angezeigt werden soll, wenn der Wert des Attributs für ein Profil leer ist, und klicken Sie dann auf **[!UICONTROL Hinzufügen]**.

<!-- ![](assets/attribute-details.png) -->

Sie können beispielsweise jeden Empfänger mit dem Vornamen begrüßen, indem Sie `{{profile.firstName}}` mit einem Fallback versehen, wenn der Wert fehlt: `{{profile.firstName | default: "there"}}`.

## Optionen für die Ausdrucksbearbeitung {#options}

Der zentrale Arbeitsbereich bietet verschiedene Tools, mit denen Sie Ihren Personalisierungsausdruck schreiben können.

<!-- ![](assets/perso-workspace.png) -->

Verfügbare Optionen sind:

1. **[!UICONTROL Suchen]**/**[!UICONTROL Suchen und Ersetzen]**: Durchsuchen Sie Ihren Ausdruck und ersetzen Sie automatisch Teile des Codes.
1. **[!UICONTROL Rückgängig machen]**/**[!UICONTROL Wiederholen]**: Machen Sie den letzten Vorgang rückgängig oder wiederholen Sie ihn.
1. **[!UICONTROL Automatisch vervollständigen]**: Vervollständigt Code automatisch während der Eingabe und unterbreitet Vorschläge. Diese Funktion ist nur für HTML- und Textformate verfügbar und unterstützt Profilattribute. Wenn die Option über den Umschalter deaktiviert wird, ermöglicht der Editor stattdessen die automatische Vervollständigung von nativem HTML-Code.

   <!-- ![](assets/perso-complete.png){width="70%" align="center" zoomable="yes"} -->

1. **[!UICONTROL HTML]**/**[!UICONTROL JSON]**/**[!UICONTROL Text]**: Identifizieren Sie das Format Ihres Codes. Dadurch kann das System die Funktion zur Validierung und automatischen Vervollständigung basierend auf der ausgewählten Sprache anpassen.
1. **[!UICONTROL Validieren]**: Überprüfen Sie die Syntax Ihres Ausdrucks.
1. **[!UICONTROL Schriftgrad]**: Passt den Schriftgrad für den Content im Editor an, um die Lesbarkeit zu verbessern.
1. **[!UICONTROL Zeilenumbruch]**: Aktiviert oder deaktiviert den Zeilenumbruch, sodass lange Ausdrücke in einer einzelnen Zeile angezeigt oder im Editor umgebrochen werden können. Zu den Optionen gehören:
   * **Aus** (Standard): Kein Zeilenumbruch. Lange Zeilen gehen über die Ansicht des Editors hinaus und erfordern einen horizontalen Bildlauf.
   * **Ein**: Passt Zeilen mit Umbrüchen an die Breite des Editors an.
   * **Zeilenumbruch-Spalte** - Bettet Zeilen ein, wenn eine Zeile 80 Zeichen erreicht.
   * **Begrenzt**: Fügt Zeilenumbrüche angepasst an die Editor-Breite oder bei Erreichen von 80 Zeichen ein, je nachdem, welcher Wert kleiner ist.
1. **[!UICONTROL Pillen]**: Attribute werden als kompakte „Pillen“ angezeigt, um die Lesbarkeit zu verbessern, indem lange Attributpfade ausgeblendet werden. Klicken Sie auf ein Attribut, um dessen vollständigen Pfad anzuzeigen.

   >[!NOTE]
   >
   >Diese Option ist nur für Profilattribute verfügbar.

Im Navigationsbereich stehen zusätzliche Funktionen zur Verfügung, mit denen Sie Ihren Personalisierungsausdruck erstellen können.

<!-- ![](assets/perso-features.png) -->

* **[!UICONTROL Hilfsfunktionen]**: Listet alle Hilfsfunktionen auf, die für die Durchführung von Datenoperationen wie Berechnungen, Datenformatierungen oder -konvertierungen, Bedingungen und die Bearbeitung von Daten im Rahmen der Personalisierung verfügbar sind.

* **[!UICONTROL Favoriten]**: Attribute, die Sie den Favoriten hinzugefügt haben, werden in dieser Liste angezeigt. Auf diese Weise können Sie schnell auf Ihre am häufigsten verwendeten Elemente zugreifen. Um ein Attribut zu Ihren Favoriten hinzuzufügen, klicken Sie auf das Menü mit den Auslassungspunkten und wählen Sie **[!UICONTROL Zu Favoriten hinzufügen]** aus.

Der KI-Assistent kann Handlebars-Ausdrücke aus Beschreibungen in einfacher Sprache generieren, vorhandene Ausdrücke erklären und potenzielle Probleme identifizieren.

Wenn Ihr Personalisierungsausdruck fertig ist, klicken Sie auf **[!UICONTROL Bestätigen]** oder **[!UICONTROL Einfügen]** um ihn zu Ihrem Inhalt hinzuzufügen.

## Mechanismen der Validierung {#validation-mechanisms}

Die Validierung Ihres Ausdrucks wird automatisch ausgeführt, wenn Sie auf **[!UICONTROL Bestätigen]** oder **[!UICONTROL Einfügen]** klicken, um den Editor zu schließen. Sie können auch auf **[!UICONTROL Validieren]** klicken, um Ihre Personalisierungssyntax vor dem Schließen zu überprüfen.

Informationen zu Inhaltswarnhinweisen, die die Journey-Aktivierung blockieren, finden Sie unter [Validieren von E-Mail-Inhalten](./email-authoring.md#validation).

Erweitern Sie den folgenden Abschnitt, um häufige Fehler bei der Validierung der Personalisierung anzuzeigen.

+++Häufige Fehler

* **Pfad „XYZ“ nicht gefunden**

Dieser Fehler tritt auf, wenn Sie auf ein Feld verweisen, das nicht im Schema definiert ist.

In diesem Fall **firstName1** nicht als Attribut im Profilschema definiert:

```handlebars
{{profile.firstName1}}
```

* **Typ für Variable „XYZ“ stimmt nicht überein. Array erwartet, Zeichenfolge gefunden.**

Dieser Fehler tritt auf, wenn Sie versuchen, über eine Zeichenfolge statt über ein Array zu iterieren.

In diesem Fall **jobTitle** eine Zeichenfolge, kein Array:

```handlebars
{{#each profile.jobTitle as |item|}}
  {{item}}
{{/each}}
```

* **Ungültige Handlebars-Syntax.`'[XYZ}}'`** gefunden

Dieser Fehler tritt auf, wenn eine ungültige Handlebars-Syntax verwendet wird.

```handlebars
{{[profile.firstName}}
```

+++
