---
title: Öffnungs-Tracking für E-Mails verwalten
description: Deaktivieren Sie das E-Mail-Öffnungs-Tracking für eine einzelne E-Mail oder erfassen Sie die Tracking-Voreinstellungen einer Person und verwenden Sie einen aufgeteilten Pfad, um Tracking- und Nicht-Tracking-E-Mail-Varianten zu senden.
feature: Account Journeys, Channels
topic: Content Management
role: User
level: Beginner, Intermediate
autotag-review: '2026-07-08T00:02:50.497Z'
TQID: 'https://experienceleague.adobe.com/LIutoajlpVQTeJP2y4i0Wv7H-WqGj-c-LVsOGfin384'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: d6e625c1-468f-4d73-9f32-fd1edb87f96bid: e666e996-b2cf-4c45-8fc2-1c625212ababid: f01b5556-e951-40ba-8625-2e3001864f2b
subfeature_v2: id: ff0c35fa-aa7e-4050-a37c-198fcacd09e6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: 884e430e7dadd400a132ec261b146ebbb27f0909
workflow-type: tm+mt
source-wordcount: 712
ht-degree: 0%

---

# Öffnungs-Tracking für E-Mails verwalten

Ihre Organisation ist für die Festlegung Ihrer eigenen Compliance-Verpflichtungen gemäß den geltenden Richtlinien und Gesetzen zur Rechtsprechung verantwortlich, Sie können jedoch die folgenden [!DNL Journey Optimizer B2B Edition]-Funktionen verwenden, um Ihre Compliance-Bemühungen zu unterstützen.

Sie können das Öffnungs-Tracking für eine einzelne E-Mail deaktivieren oder die Tracking-Voreinstellungen jeder Person in Adobe Experience Platform erfassen und einen aufgeteilten Pfad verwenden, um Personen zu Tracking- und Nicht-Tracking-E-Mail-Varianten zu leiten.

## Tracking für einzelne E-Mail deaktivieren {#disable-tracking-single-email}

Verwenden Sie diese Option, wenn Sie möchten, dass eine bestimmte E-Mail nie eine offene Aktivität meldet, unabhängig davon, wer sie erhält.

1. Öffnen Sie in den Eigenschaften des Journey-Knotens auf der rechten Seite die E-Mail.

1. Aktivieren Sie in den E-Mail-Eigenschaften das Kontrollkästchen **[!UICONTROL Öffnungs-Tracking deaktivieren]**.

   ![Öffnungs-Tracking für E-Mails deaktivieren](./assets/email-tracking-disable-all.png){width="500" zoomable="yes"}

   Siehe [Definieren der E-Mail](./add-email.md#define-the-email-settings)Einstellungen, um die vollständige Liste der E-Mail-Eigenschaften aufzurufen.

## Personen nach Tracking-Voreinstellungen segmentieren {#segment-people-tracking-preference}

Wenn Sie möchten, dass jede Person auswählen kann, ob ihre E-Mail-Öffnungen verfolgt werden, erfassen Sie diese Voreinstellung als Personenattribut in Adobe Experience Platform (AEP). Sie können dieses Feld in einem [Landingpage-Formular](./forms.md) verwenden, damit Ihre Kontakte das Tracking der E-Mail-Öffnungen deaktivieren können. Anschließend können Sie den Knoten _Split-Pfade_ in Ihren Journey verwenden, um Personen, die das Tracking nicht fortsetzen, zu verschiedenen E-Mail-Varianten weiterzuleiten. Auf diese Weise können Sie ein individuelles Opt-out berücksichtigen, ohne das Öffnungs-Tracking für alle zu deaktivieren.

Der Workflow besteht aus drei Teilen:

1. [Benutzerdefiniertes Feld für die Tracking-Voreinstellung hinzufügen](#add-custom-field-tracking-preference) in AEP und Senden einer Opt-out-Kommunikation mit einem Formular-Link.
1. [Fügen Sie einen Aufspaltungspfad für das Tracking-Opt-out ](#add-split-path-tracking) der Journey hinzu.
1. [Konfigurieren Sie Tracking- und Nicht-Tracking-E-](#configure-tracking-and-non-tracking-email-variants) für jeden Pfad.

### Benutzerdefiniertes Feld für Tracking-Voreinstellungen hinzufügen {#add-custom-field-tracking-preference}

>[!NOTE]
>
>Das Hinzufügen und Zuordnen benutzerdefinierter XDM-Felder ist eine Adobe Experience Platform-Verwaltungsaufgabe. Wenden Sie sich an Ihren AEP-Administrator oder Ihr Data Engineering-Team, um diesen Schritt abzuschließen.

1. Öffnen Sie in AEP das Schema, das für Ihr B2B-Personenprofil verwendet wird (z. B. _B2B-Person_).

1. Suchen oder erstellen Sie unter der Mandanten-ID eine Feldergruppe für die Felder der Einverständnisverwaltung Ihres Unternehmens (z. B. `consents`).

1. Fügen Sie der Feldergruppe ein Feld hinzu, z. B. ein boolesches Feld mit dem Namen `emailTracking`, um anzugeben, ob die Person dem Öffnungs-Tracking zugestimmt hat.

1. Geben Sie den Feldnamen und den Anzeigenamen ein, legen Sie den Typ fest, weisen Sie ihn der Feldergruppe zu und klicken Sie auf **[!UICONTROL Anwenden]**.

1. Klicken Sie **[!UICONTROL Speichern]**, um die Schemaänderungen zu speichern.

   ![Feld „emailTracking“ zur Feldergruppe &quot;AEP-Schema-Einverständnis“ hinzufügen](./assets/email-tracking-xdm-field-aep-schema.png){width="800" zoomable="yes"}

1. Stellen Sie das Feld in [!DNL Journey Optimizer B2B Edition] zur Verfügung, indem Sie es als _verwaltetes Feld_ für die Klasse [!UICONTROL XDM Individual Profile] in der [XDM-Feldverwaltung](../admin/xdm-field-management.md#managed-fields).

   ![Wählen Sie emailTracking als verwaltetes Feld in der XDM-Feldverwaltung aus](./assets/email-tracking-xdm-field-select.png){width="450"}

   Dadurch wird das Feld als Bedingung in aufgeteilten Pfadknoten verfügbar.

### Aufspaltungspfad für Tracking-Opt-out hinzufügen {#add-split-path-tracking}

Fügen Sie Ihrem Journey [_Aufspaltungspfade nach Personen_ Knoten](../journeys/split-merge-paths-nodes.md#split-paths-by-people) hinzu und definieren Sie einen Pfad für jeden Tracking-Voreinstellungswert.

1. Fügen Sie den Knoten **[!UICONTROL Pfade aufteilen]** hinzu und wählen Sie **[!UICONTROL Personen]** für die Aufspaltung aus.

1. Wenden Sie für den ersten Pfad eine Bedingung mithilfe Ihres benutzerdefinierten Tracking-Präferenzfelds an (z. B. `emailTracking` ist `true`), um Personen zu identifizieren, die das Öffnungs-Tracking zulassen.

   ![Bedingung für aufgeteilten Pfad - E-Mail-Tracking-Feld als wahr hinzufügen](./assets/email-tracking-condition-true.png){width="700" zoomable="yes"}

1. Fügen Sie einen zweiten Pfad hinzu und wenden Sie die umgekehrte Bedingung (`emailTracking` ist `false`) an, um Personen zu identifizieren, die sich gegen das Tracking entschieden haben.

   Allgemeine Schritte zum Hinzufügen von Pfaden, Anwenden von Bedingungen und Neuanordnen von Pfaden finden Sie unter [Hinzufügen eines Pfads, der nach Personen-Knoten aufgeteilt ist](../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node).

   ![Pfad nach Personen aufteilen - E-Mail-Tracking mit und ohne Bedingungen](./assets/email-tracking-split-paths.png){width="500" zoomable="yes"}

### Konfigurieren von Tracking- und Nicht-Tracking-E-Mail-Varianten {#configure-tracking-and-non-tracking-email-variants}

Fügen Sie jedem Pfad [_[!UICONTROL  Aktionsknoten ]_E-Mail senden](./add-email.md) hinzu, damit jede Person die E-Mail-Variante erhält, die ihrer Tracking-Voreinstellung entspricht.

1. Fügen Sie im Pfad mit aktiviertem Tracking die Aktion **[!UICONTROL E-Mail senden]** hinzu und wählen oder erstellen Sie die E-Mail wie gewohnt, wobei **[!UICONTROL Tracking deaktivieren]** in den E-Mail-Eigenschaften deaktiviert bleibt.

1. Fügen Sie im Abmeldepfad die Aktion **[!UICONTROL E-Mail senden]** mit derselben oder einer duplizierten E-Mail hinzu und aktivieren Sie dann das Kontrollkästchen **[!UICONTROL Öffnungs-Tracking deaktivieren]** in den E-Mail-Eigenschaften auf der rechten Seite.

   ![E-Mail zum Tracking außerhalb des Pfads - Öffnungs-Tracking deaktivieren](./assets/email-tracking-disable.png){width="600" zoomable="yes"}

1. [Veröffentlichen der Journey](../journeys/create-publish-journey.md#publish-a-journey).

   Personen werden automatisch an die E-Mail-Variante weitergeleitet, die dem Wert ihres Tracking-Präferenzfelds entspricht, und alle Aktualisierungen, die sie an ihren Präferenzen vornehmen, werden widergespiegelt, wenn sie das nächste Mal die Journey betreten.
