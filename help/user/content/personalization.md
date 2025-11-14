---
title: Personalisierung von Inhalten
description: Personalisieren von B2B-E-Mails mit Konto-, Personen- und System-Token in Journey Optimizer B2B edition. Erfahren Sie, wie Sie den Personalisierungseditor und die Syntax verwenden.
feature: Personalization, Content Design Tools, Email Authoring
topic: Personalization
role: User, Developer
level: Intermediate
keywords: Ausdruck, Editor, Start, Personalisierung
source-git-commit: fee5bddcce11b3035da6ab93b18bcc7006b4b554
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 1%

---

# Personalisierung von Inhalten {#add-personalization}

>[!CONTEXTUALHELP]
>id="aj-b2b_personalization"
>title="Personalisieren von Inhaltserlebnissen"
>abstract="Verwenden Sie **Adobe Journey Optimizer B2B edition**, um Ihre Nachrichten für jeden einzelnen Empfänger anzupassen, indem Sie die vorhandenen Daten und Informationen nutzen. Dabei kann es sich um den Vornamen, die Branche, den Titel und mehr handeln."

[!DNL Adobe Journey Optimizer B2B Edition] Personalisierungsfunktionen ermöglichen es Ihnen, Ihre E-Mail-Nachrichten an jeden einzelnen Empfänger anhand der vorhandenen Daten anzupassen. Dabei kann es sich um den Vornamen, die Branche, den Titel und mehr handeln.

Mit dem _Personalisierungseditor_ können Sie alle Daten auswählen, anordnen, anpassen und validieren, um eine benutzerdefinierte Personalisierung für Ihre Inhalte zu erstellen. Verwenden Sie verschiedene Tools, z. B. Hilfsfunktionen, um Nachrichten anzupassen. Der Editor verwendet eine Inline-Personalisierungssyntax, die auf _Handlebars_ basiert. Dabei werden Ausdrücke mit Inhalten erstellt, die von geschweiften Klammern `{{}}` eingeschlossen sind.

Bei der Verarbeitung der Nachricht ersetzt Journey Optimizer B2B edition den Ausdruck durch die im Adobe Experience Platform-Datensatz enthaltenen Daten und die Werte des lokalen Systems. Beispielsweise wird `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` dynamisch zu `Hello John Doe`.

Mit dieser Syntax können Sie Nachrichten über mehrere Felder hinweg personalisieren, einschließlich E-Mail-Betreffzeilen, Nachrichtentexten und Absenderinformationen.

## Personalization-Token

In [!DNL Journey Optimizer B2B Edition] können Sie Ihren dynamischen E-Mail-Inhalt mithilfe von Personalisierungs-Token erstellen:

* **Konto-Token** - Diese Token basieren auf den Kontoattributen, z _B. „Kontoname_, _Branche_ und _Anzahl der Mitarbeiter_. Verwenden Sie diese Token, um Attributdaten auszufüllen, die vom Schema **_XDM Business Account Details_** verwaltet werden, das in Adobe Experience Platform definiert ist.

* **Personen**-Token: Diese Token basieren auf den Attributen von Geschäftspersonen, wie _Vorname_, _Stellenbezeichnung_ und _Firmenname_. Verwenden Sie diese Token, um Attributdaten auszufüllen, die vom Schema **_XDM-Geschäftspersonendetails_** verwaltet werden, das in Adobe Experience Platform definiert ist.

* **System-**: Diese Token basieren auf den Systemfeldwerten, z. B. _Datum_, _Uhrzeit_ und _Abmelde-Link_.

* **Meine Token** (wenn für die Journey definiert) - Die [benutzerdefinierten Token, die für die Journey definiert sind](./personalization-my-tokens.md) in denen sich die E-Mail befindet.

>[!NOTE]
>
>Weitere Informationen zu den XDM-Schemata finden Sie in der Dokumentation zum [Adobe Experience Platform-Datenmodell (XDM)](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/home){target="_blank"}.

## Personalisierungseditor

Der Personalisierungseditor ist in jedem Kontext verfügbar, in dem Sie die Personalisierung in E-Mail-Inhalten definieren müssen. Im Editor können Sie alle Daten auswählen, anordnen, anpassen und validieren, um eine benutzerdefinierte Personalisierung für Ihre Inhalte zu erstellen.

>[!NOTE]
>
>Die folgenden Informationen für den Personalisierungseditor spiegeln die Änderungen wider, die für Journey Optimizer B2B edition-Umgebungen verfügbar sind, die auf der [vereinfachten Architektur“ bereitgestellt &#x200B;](../simplified-architecture.md).

Fügen Sie Personalisierung in einem beliebigen Feld oder einer beliebigen Inhaltskomponente hinzu, indem Sie auf das Symbol _Personalisierung hinzufügen_ (![Personalisierungssymbol hinzufügen](../../assets/do-not-localize/icon-personalization-field.svg) klicken.

![Personalization-Editor](./assets/personalization-editor.png){width="800" zoomable="yes"}

Um ein Personalisierungs-Token oder eine Hilfsfunktion zu verwenden, suchen Sie es im linken Navigationsbereich und klicken Sie auf **+**, um es bzw. sie dem Ausdruck hinzuzufügen.

Klicken Sie auf das Symbol _Mehr_ ( **…** ) (neben dem Symbol _Hinzufügen_ ( **+** ), um weitere Details zu jedem Attribut anzuzeigen und Ihre am häufigsten verwendeten Attribute zu den _Favoriten_ hinzuzufügen. Zu Favoriten hinzugefügte Attribute sind über das Menü **[!UICONTROL Favoriten]** im linken Navigationsbereich des Editors zugänglich.

![Personalization-Editor - Menü „Mehr Token“](./assets/personalization-editor-token-more-menu.png){width="800" zoomable="yes"}

<!-- >>[!NOTE]
>
>By default, the attributes list shows only populated attributes. To display all attributes, click the _Settings_ icon above the search field and toggle off the **[!UICONTROL Show only populated attributes]** option.
-->
Sie können auch eine standardmäßige Fallback-Textzeichenfolge definieren, die angezeigt wird, wenn ein Profilattribut vom Typ Zeichenfolge leer ist. Klicken Sie auf das Symbol _Mehr_ ( **…** ) für das Attribut und wählen Sie **[!UICONTROL Einfügen mit Fallback-Text]**. Geben Sie den Text ein, der angezeigt werden soll, wenn der Wert des Attributs für ein Profil leer ist, und klicken Sie dann auf **[!UICONTROL Hinzufügen]**.

Es empfiehlt sich, den Ausdruck zu validieren, bevor Sie ihn in den Inhalt einfügen. Klicken **[!UICONTROL unten]** Editor auf „Validieren“, um Ihre Syntax zu überprüfen und sicherzustellen, dass keine Fehler auftreten.

![Vom Personalization-Editor validierter Code](./assets/personalization-editor-validated.png){width="500"}

Wenn der Ausdruck vollständig und fehlerfrei ist, klicken Sie auf **[!UICONTROL Speichern]**.

<!-- ## Personalization experimentation {#playground}

**[!DNL Adobe Journey Optimizer]** includes an interactive tool designed to help you learn and experiment with personalization capabilities.

This playground provides a simulated environment to write and test personalization code using sample data without requiring live datasets. You can leverage predefined code samples, edit dummy profile payloads, and preview the output of your personalization code in real-time. 

![personalization playground](assets/playground.png)

➡️ [Access the personalization playground](https://experienceleague.adobe.com/de/apps/journey-optimizer/ajo-personalization){target="_blank"} 

## How-to videos{#video-perso}

Learn how to use contextual event information from a journey to personalize a message.

>[!VIDEO](https://video.tv.adobe.com/v/3448148?captions=ger&quality=12)

Learn how to add profile-based personalization to a message and how to use audience membership as a pre-condition to a personalization block.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)

Learn how to leverage the personalization editor playground to write and test personalization code using sample data.

>[!VIDEO](https://video.tv.adobe.com/v/3475961?captions=ger&quality=12) -->