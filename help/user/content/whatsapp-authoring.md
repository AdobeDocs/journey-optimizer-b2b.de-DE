---
title: WhatsApp-Authoring
description: Erstellen Sie WhatsApp-Nachrichten für Account-Journey mithilfe genehmigter Meta-Vorlagen, Personalisierungs-Token und Versandeinstellungen in Journey Optimizer B2B edition.
feature: Content, Channels, Account Journeys
role: User
exl-id: 36c7e377-1f51-4d68-9e00-c6ce994e9909
autotag-review: '2026-05-27T16:19:44.490Z'
TQID: 'https://experienceleague.adobe.com/B368ny2Y9BSzsE7CClVIbVr-5Kha5d2pTiNiDGCwML4'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: beb5f4be-cec3-471a-9db6-831a77dd3ac9id: f01b5556-e951-40ba-8625-2e3001864f2b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: d90cafcd84266a177523fc6d716ebfa8bf999d89
workflow-type: tm+mt
source-wordcount: 828
ht-degree: 20%

---

# WhatsApp-Authoring

Verwenden Sie Adobe Journey Optimizer B2B edition, um WhatsApp-Nachrichten an Kontomitglieder auf ihren Mobilgeräten zu senden. Sie können Nachrichten mithilfe genehmigter Meta-Nachrichtenvorlagen im WhatsApp-Editor erstellen, personalisieren und in der Vorschau anzeigen. <!-- Test your WhatsApp messages before publishing the account journey to ensure your intended rendering, accurate personalization, and proper configuration of all settings. -->

Bevor Sie WhatsApp-Nachrichten für Account-Journey erstellen, stellen Sie sicher, dass Sie den erforderlichen [WhatsApp-Kanal) ](../admin/configure-channels-whatsapp.md) den Einstellungen _[!UICONTROL Administrator]_ konfiguriert haben.


>[!NOTE]
>
>In _B2B edition_ nur WhatsApp-Nachrichtenelemente unterstützt.

+++ Unterstützte Nachrichtenelemente und Aktionsaufruf-Optionen

Die folgenden Nachrichtentypen werden in WhatsApp unterstützt:

| Nachrichtenelement | Beschreibung |
| - | - |
| Kopfzeilen | Optionaler Text, der über dem Nachrichtentext angezeigt wird. |
| Text | Unterstützt dynamische Inhalte durch Parameter. |
| Bilder (JPEG, PNG) | Müssen im 8-Bit-RGB- oder -RGBA-Format vorliegen und kleiner als 5 MB sein. |
| Videos | Muss 3GPP oder MP4 sein, unter 16 MB und von URL gehostet. |
| Audio | Nur für Antwortnachrichten verfügbar. Muss im AAC-, AMR-, MP3-, MP4 Audio- oder OGG-Format vorliegen, über eine URL gehostet werden und kleiner als 16 MB sein. |
| Dokumente | Muss unter 100 MB groß sein, auf einer URL gehostet werden und eines der folgenden Formate aufweisen: `.txt`, `.xls`/`.xlsx`, `.doc`/`.docx`, `.ppt`/`.pptx` oder `.pdf`. |
| Textkörper | Unterstützt dynamische Inhalte durch Parameter. |
| Fußzeilentext | Unterstützt dynamische Inhalte durch Parameter. |

Für Ihre WhatsApp-Nachrichten stehen die folgenden call-to-action-Optionen zur Verfügung:

| Call to action | Beschreibung |
| - | - |
| Besuchen einer Website | Es ist nur eine Schaltfläche zulässig, einschließlich Variablenparametern. |
| Anruf über WhatsApp | Stellt eine Schaltfläche bereit, mit der ein WhatsApp-Chat mit der angegebenen Telefonnummer direkt von der Nachricht aus geöffnet wird. |
| Anrufen einer Telefonnummer | Stellt eine Schaltfläche bereit, mit der ein Telefonanruf an die angegebene Nummer gestartet wird, wenn die Benutzenden darauf tippen. |

+++

## Hinzufügen einer WhatsApp-Aktion auf einer Konto-Journey

>[!IMPORTANT]
>
>**Einverständnisverwaltung per WhatsApp**: Gemäß den Richtlinien und geltenden Vorschriften von Meta dürfen alle WhatsApp-Marketing-Nachrichten nur an Empfänger gesendet werden, die sich für den Erhalt von Nachrichten entschieden haben. Empfänger von WhatsApp können sich jederzeit per Opt-out-Keyword abmelden. Opt-out-Antworten werden automatisch berücksichtigt und die entsprechenden Profile werden aus zukünftigen Marketing-Nachrichten-Audiences entfernt. Einzelheiten dazu, wie die Einverständnisvoreinstellungen von WhatsApp zum Zeitpunkt des Versands ausgewertet werden, finden Sie unter [Einverständnisvoreinstellungen](./channels-consent-preferences.md).

Sie können WhatsApp-Nachrichtenversand auf einer Konto-Journey einrichten, wenn Sie [einen Knoten _[!UICONTROL Aktion durchführen]_ hinzufügen ](../journeys/action-nodes.md) Folgendes tun:

1. Wählen Sie für _[!UICONTROL Ziel]_ Aktion auf“ **[!UICONTROL Personen]**.

1. Wählen Sie für _[!UICONTROL Aktion für Personen]_ die Option **[!UICONTROL WhatsApp senden]** aus.

   ![Aktion durchführen - WhatsApp senden](./assets/whatsapp-journey-node.png){width="500" zoomable="yes"}

## Erstellen der WhatsApp-Nachricht

1. Klicken Sie unten im Bedienfeld _[!UICONTROL Aktion ausführen]_ auf **[!UICONTROL WhatsApp erstellen]**.

1. Geben Sie im Dialogfeld einen eindeutigen **[!UICONTROL Namen]** (erforderlich) und **[!UICONTROL Beschreibung]** (optional) für die WhatsApp-Nachricht ein.

   ![Dialogfeld „Neue WhatsApp-Nachricht erstellen“](./assets/whatsapp-create-dialog.png){width="400"}

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

   Der _WhatsApp-Design-Bereich_ wird geöffnet, in dem Sie die WhatsApp-Aktionen definieren und den Inhalt für den Nachrichtenversand erstellen können.

### Auswählen der Aktionskonfiguration

1. Wählen _im WhatsApp-_ die Registerkarte **[!UICONTROL Aktionen]** aus.

1. Wählen Sie für **[!UICONTROL WhatsApp]** Konfiguration die [Konfiguration](../admin/configure-channels-whatsapp.md#create-channel-configuration) aus, die die Marketing-Aktionen und die Einstellungen für den Nachrichtenversand für Ihre Anforderungen unterstützt.

   ![Erstellen einer WhatsApp - Registerkarte „Aktionen“](./assets/whatsapp-create-actions-tab.png){width="700" zoomable="yes"}

1. Klicken Sie **[!UICONTROL Inhalt bearbeiten]**, um mit den Nachrichtenparametern und dem Text fortzufahren.

### Nachrichtenvorlage auswählen

WhatsApp-Nachrichten werden mit vorab genehmigten Nachrichtenvorlagen von Ihrem Meta WhatsApp Business-Konto gesendet. **Vorlagen müssen von Meta überprüft und genehmigt werden** bevor Sie sie in Journey Optimizer B2B edition verwenden können. Wenden Sie sich an Ihren [!DNL Meta Business Manager]-Kontoadministrator, um Vorlagen zu verwalten und zur Genehmigung einzureichen.

1. Wählen **[!UICONTROL für „Vorlagenkategorie]**&quot; eine der folgenden Optionen:

   * Marketing
   * Dienstprogramm
   * Authentifizierung

1. Wählen **[!UICONTROL unter „WhatsApp-]** auswählen“ eine genehmigte Vorlage für die Konfiguration des Geschäftskontos aus.

   Der Vorlageninhalt wird im Nachrichten-Editor geladen und zeigt die Vorlagenstruktur und alle für die Personalisierung verfügbaren Variablenfelder an.

   ![Ausgewählte WhatsApp-Nachrichtenvorlage mit im Vorschaufenster geladener Nachricht](./assets/whatsapp-create-select-template.png){width="700" zoomable="yes"}

   Das System organisiert Vorlagen nach Kategorie (_Marketing_, _Dienstprogramm_ und _Authentifizierung_) und Status. Nur **_genehmigte_** Vorlagen sind zur Auswahl verfügbar. Weitere Informationen zum Erstellen von WhatsApp-Vorlagen finden Sie unter [_Erstellen von Nachrichtenvorlagen für Ihr WhatsApp Business-Konto_](https://www.facebook.com/business/help/2055875911147364?id=2129163877102343) in der Dokumentation zu Meta.

### Bild-URL

Wenn Ihre Vorlage Bilder enthält, verwenden Sie das Feld **[!UICONTROL Bild-URL]**, um Medien-URLs hinzuzufügen, um alle Platzhalter in Ihrer Vorlage zu ersetzen. Die Vorlagenmedien von Meta sind nur Platzhalter. Damit Bilder, Audio oder Video korrekt angezeigt werden, müssen Sie externe URLs aus Adobe Experience Manager oder anderen Quellen verwenden.

### Nachrichteninhalt personalisieren

Genehmigte WhatsApp-Vorlagen können variable Platzhalter enthalten, die Sie mithilfe von Profildaten oder dynamischen Werten definieren.

Klicken Sie für jedes in der Vorlage angezeigte Variablenfeld auf das _Personalisieren_-Symbol ( ![Personalisieren-Symbol](../assets/do-not-localize/icon-personalize.svg) ) neben dem Feld.

![Variablen in der WhatsApp-Vorlage](./assets/whatsapp-create-variables.png){width="700" zoomable="yes"}

Das Dialogfeld bietet Zugriff auf die Konto-Token, Personen-Token und System-Token. Sowohl standardmäßige als auch benutzerdefinierte Token sind enthalten. Sie können die _Suche_ verwenden, um das benötigte Token zu finden, oder durch die Ordnerstruktur navigieren, um eines der Token zu finden und auszuwählen.

Ausführliche Informationen zur Verwendung von Token für die Personalisierung finden Sie unter [Inhaltspersonalisierung](./personalization.md).

Wenn Ihre Personalisierungs-Token definiert sind, klicken Sie auf **[!UICONTROL Speichern]**, um Änderungen zu speichern und zum Hauptarbeitsbereich der WhatsApp-Nachricht zurückzukehren.
