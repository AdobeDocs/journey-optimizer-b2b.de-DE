---
title: Externe Zielgruppen [!DNL Adobe Target]
description: Aktivieren Sie externe Zielgruppen für  [!DNL Adobe Target] über Account-Journey. Personalisieren Sie B2B-Web-Erlebnisse und sorgen Sie für plattformübergreifende Konsistenz.
feature: Integrations, Audiences, Account Journeys
role: User, Admin
source-git-commit: 598546c62cb2d567f19b26f7f760aa43e4dd0bc9
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 1%

---

# Externe Zielgruppen [!DNL Adobe Target]

Sie können Erlebnisse für externe Zielgruppen in [!DNL Adobe Target] über Account Journey aktivieren und personalisieren. Verwenden Sie diese Integration, um eine erweiterte und maßgeschneiderte Personalisierung zu erzielen, die die Interaktion erhöht, und um die plattformübergreifende Konsistenz über [!DNL Target] und [!DNL Journey Optimizer B2B Edition] hinweg aufrechtzuerhalten. Diese Konsistenz stellt sicher, dass Teams Web-Kanäle für Einkaufsgruppen im gesamten B2B-Käufer-Journey abstimmen und personalisieren.

Es handelt sich um einen zweistufigen Workflow zur Aktivierung einer externen Zielgruppe über Adobe Target:

1. [Hinzufügen zur externen Kundenzielgruppe](#add-to-customer-external-audience-from-a-journey) von einer Journey.
2. [Aktivieren Sie die externe Zielgruppe](#activate-the-external-audience-to-target-as-a-destination) um als Ziel in Experience Platform zu [!DNL Target].

## Hinzufügen von Daten von einer Journey zur externen Zielgruppe des Kunden

Fügen Sie in Ihrem Journey [Knoten _Aktion ausführen_ hinzu](../journeys/action-nodes.md) um die Aktion _[!UICONTROL Hinzufügen zur externen Kundenzielgruppe]_ auszuführen. Aktionen sind in der Regel das, was infolge eines Triggers geschehen soll, z. B. eines Ereignisses oder einer vorherigen Aktion. Der Journey führt die Aktion aus, wenn ein passendes Konto mit Personenprofilen den Knoten erreicht.

>[!NOTE]
>
>Wenn ein qualifizierendes Konto mit Personenprofilen den Knoten _Zu externer Kundenzielgruppe hinzufügen_ in einer veröffentlichten Journey erreicht, kann es bis zu 48 Stunden dauern, bis diese Profile in der externen Zielgruppe ausgefüllt sind.

1. Wenn der Knoten _Aktion ausführen_ auf der Arbeitsfläche &quot;Journey&quot; ausgewählt ist, wählen Sie die Option _[!UICONTROL Aktion für]_ **[!UICONTROL Personen]**.

1. Wählen Sie für _[!UICONTROL Aktion für Personen]_ die Option **[!UICONTROL Zu externer Kundenzielgruppe hinzufügen]**.

   ![Journey-Knoten - Eine Aktion für Personen durchführen - Zu externer Kundenzielgruppe hinzufügen](./assets/node-add-external-audience.png){width="550" zoomable="yes"}

1. Legen Sie in den Knoteneigenschaften auf der rechten Seite die externe Zielgruppe fest.

   * Wenn bereits mindestens eine externe Zielgruppe erstellt wurde, können Sie **[!UICONTROL Vorhandene auswählen]** und [die Zielgruppe auswählen, die Sie verwenden möchten](#choose-an-external-audience).

   * Wenn Sie eine Zielgruppe [&#x200B; möchten, &#x200B;](#create-an-external-audience) Sie für den Knoten verwenden möchten, wählen Sie **[!UICONTROL Neu erstellen]**.

### Erstellen einer externen Zielgruppe

1. Nachdem Sie die Option **[!UICONTROL Neu erstellen]** in den Knoteneigenschaften ausgewählt haben, klicken Sie auf **[!UICONTROL Externe Kundenzielgruppe erstellen]**.

   ![Aktion für Personen durchführen - zur externen Zielgruppe hinzufügen - neue Option erstellen](./assets/node-add-external-audience-create-new-option.png){width="400"}

1. Geben Sie im Dialogfeld einen **[!UICONTROL Namen]** (erforderlich) und **[!UICONTROL Beschreibung]** (optional) für die neue Zielgruppe ein.

   ![Dialogfeld „Externe Zielgruppe erstellen“](./assets/create-external-customer-audience-dialog.png){width="400"}

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

   Das System erstellt die neue Zielgruppe und zeigt eine Bestätigungsmeldung an. Anschließend können Sie sie als vorhandene Zielgruppe für die Knotenaktion verwenden.

### Externe Zielgruppe auswählen

1. Nachdem Sie die Option **[!UICONTROL Vorhandene auswählen]** in den Knoteneigenschaften ausgewählt haben, klicken Sie auf **[!UICONTROL Externe Kundenzielgruppe auswählen]**.

   ![Eine Aktion für Personen durchführen - zur externen Kundenzielgruppe hinzufügen - Vorhandene Option auswählen](./assets/node-add-external-audience-select-existing-option.png){width="300"}

1. Wählen _[!UICONTROL im Dialogfeld]_ Zielgruppe hinzufügen“ die Zielgruppe aus, die Sie verwenden möchten.

   Sie können Text in das Feld _Suche_ eingeben, um die angezeigten Elemente nach übereinstimmenden Zielgruppennamen zu filtern.

   ![Eine Aktion für Personen durchführen - Zu externer Kunden-Zielgruppe hinzufügen - Dialogfeld „Zielgruppe hinzufügen“](./assets/add-audience-dialog.png){width="700" zoomable="yes"}

1. Klicken Sie **[!UICONTROL Zielgruppe hinzufügen]**.

## Aktivieren der externen Zielgruppe für Target als Ziel

Für die Aktivierung der externen Zielgruppe für Adobe Target müssen Sie [!DNL Adobe Target] als Ziel in [!DNL Real-time Customer Data Platform (RTCDP)] konfiguriert haben. Weitere Informationen zu dieser Konfiguration finden Sie in der Dokumentation zu [RTCDP](https://experienceleague.adobe.com/de/docs/platform-learn/tutorials/destinations/target/configure-the-target-destination){target="_blank"}.

>[!IMPORTANT]
>
>Bei der Aktivierung über einen Journey muss Ihre Implementierung von RTCDP eine E-Mail-Adresse als Identität verwenden.

Der Aktivierungsprozess erfordert, dass Sie [!DNL Adobe Target] als externe Zielgruppe oder externes Ziel hinzufügen. Erstellen Sie zunächst eine [!DNL Target] Zielgruppe im Audience Builder. Sie können auch eine Platzhalter-Zielgruppe erstellen und die Funktion für externe Zielgruppen hinzufügen.

>[!BEGINSHADEBOX]

![AEP-Berechtigungssymbol](../../assets/do-not-localize/icon_permissions-outline.svg) Für diese Schritte sind die folgenden Berechtigungen für die zugewiesene Benutzerrolle erforderlich:

* **[!UICONTROL Experience Platform]** - Für die Ressource _[!UICONTROL Ziele]_: `Activate Destinations`, `Manage and Activate Dataset Destination` und `View Destination`
* **[!DNL Target]** – `Approver`

>[!ENDSHADEBOX]

1. Navigieren Sie in Experience Platform **[!UICONTROL Verbindungen]** > **[!UICONTROL Ziele]** im linken Navigationsbereich.

1. Wählen Sie die Registerkarte **[!UICONTROL Durchsuchen]** aus.

1. Suchen Sie die Zielverbindung, die Sie zum Aktivieren Ihrer Segmente verwenden möchten, klicken Sie auf das Symbol _Mehr Menü_ ( **…** ) neben dem Namen und wählen Sie **[!UICONTROL Zielgruppen aktivieren]**.

   Geben Sie Text in das Feld _[!UICONTROL Suchen]_ ein, um die angezeigten Ziele nach einer Übereinstimmung nach Namen zu filtern.

   ![Experience Platform - Ziele - Target-Ziele durchsuchen - Menü „Mehr“](./assets/aep-destinations-activate-target-audience.png){width="800" zoomable="yes"}

1. Wählen Sie in _[!UICONTROL Liste &quot;]_ Zielgruppen“ Ihre externe Zielgruppe aus und klicken Sie auf **[!UICONTROL Weiter]**.

   ![Experience Platform - Ziele - Target-Ziele durchsuchen - Menü „Mehr“](./assets/aep-destinations-activate-target-audience-available-audiences.png){width="700" zoomable="yes"}

1. Nehmen Sie eine beliebige zusätzliche Feldzuordnung zum Ziel vor (optional) und klicken Sie auf **[!UICONTROL Weiter]**.

1. Überprüfen Sie die neuen Zielgruppenparameter und klicken Sie auf **[!UICONTROL Beenden]**.

   ![Experience Platform - Ziele - Ziel aktivieren - Überprüfen](./assets/aep-destinations-activate-target-audience-review.png){width="700" zoomable="yes"}

Nach der Aktivierung können Sie die Zielgruppe in [Adobe Target-Zielgruppen](https://experienceleague.adobe.com/de/docs/target/using/audiences/create-audiences/audiences#use-list){target="_blank"} sehen und in Adobe Target-Aktivitäten verwenden.

