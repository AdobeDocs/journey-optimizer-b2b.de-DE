---
title: Erlebnisereignisse und -felder auswählen
description: Wählen Sie Experience Platform-Ereignisse und -Felder aus, um die Echtzeit-Entscheidungsfindung in Journey auf Grundlage des Kundenverhaltens in Triggern zu ermöglichen.
feature: Setup, Integrations
role: Admin
badgeBeta: label="Beta" type="informative" tooltip="Diese Funktion befindet sich derzeit in der Beta-Version"
solution: Journey Optimizer B2B Edition, Experience Platform
exl-id: a7696d03-f4c4-4f64-8ef2-b15e59b59770
source-git-commit: 046d3648c5e482a69719d0095c297a766dd852ea
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 0%

---

# Erlebnisereignisse und -felder auswählen

Admins können bestimmte [AEP-Erlebnisereignisse](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/experienceevent){target="_blank"} und deren zugehörige Felder im Vereinigungsschema für Erlebnisereignisse auswählen. Nach der Auswahl können Benutzende Entscheidungsregeln konfigurieren, die auf diese Erlebnisereignisse lauschen, um dynamische und zielgerichtete Kampagnenaktionen zu ermöglichen, die auf nahezu in Echtzeit erfassten Ereignisdaten basieren.

<!-- ![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Watch the video overview](#overview-video) -->
Die Verwendung von AEP-Erlebnisereignissen in Journey ist ein zweistufiger Prozess:

1. AEP Ein Administrator ([ Erlebnisereignisse und -felder) ](#add-an-event) den Journey Optimizer B2B edition-Konfigurationen.

2. Auf einer Journey fügt der Marketing-Experte einen _Lauschen auf ein_) hinzu und [wählt ein Erlebnisereignis aus](../journeys/listen-for-event-nodes.md#listen-for-an-experience-event).

   * Wählt das im Knoten zu verwendende Ereignis aus.
   * Wählt die als Einschränkung zu verwendenden Felder aus.

>[!BEGINSHADEBOX]

## Richtlinien und Einschränkungen

Beachten Sie bei der Auswahl von Ereignissen zur Erreichung Ihrer Unternehmensziele Folgendes:

* Sie können bis zu 50 Ereignisse und bis zu 100 Felder pro Ereignis auswählen.

* Journey können Erlebnisereignisse überwachen, die über Experience Platform-Streaming-Funktionen aufgenommen werden, z. B. Web-SDK oder HTTP-API.

* Sie können Erlebnisereignisse für Entscheidungszwecke in einem Journey verwenden, sie werden jedoch nicht beibehalten. Daher können Sie keinen historischen Datensatz mit Erlebnisereignissen in Journey Optimizer B2B edition nutzen.

* Wenn Sie ein Erlebnisereignis verwenden und die Journey veröffentlichen, können Sie weitere Felder hinzufügen, zuvor ausgewählte Felder jedoch nicht entfernen.

* Sie können auf ein Erlebnisereignis in mehreren Journey verweisen oder ein Erlebnisereignis mehrmals auf derselben Journey verwenden.

>[!ENDSHADEBOX]

## Verwalten von Erlebnisereignissen

1. Wählen Sie in der linken Navigation **[!UICONTROL Administration]** > **[!UICONTROL Konfigurationen]**.

1. Klicken Sie **[!UICONTROL Zwischenbereich auf]** XDM-Klassen“ und anschließend auf die Registerkarte **[!UICONTROL Ereignisse]**, um die Liste der verfügbaren Ereignisse anzuzeigen.

   ![Zugriff auf die ausgewählten Erlebnisereignisse](./assets/configurations-xdm-classes-events.png){width="800" zoomable="yes"}

   Die Tabelle wird nach der Spalte _[!UICONTROL Letzte Aktualisierung]_ sortiert, wobei die zuletzt aktualisierten Ereignisse standardmäßig oben stehen.

   Auf dieser Seite können Sie Ereignisse [Auswählen](#add-an-event) und [Bearbeiten](#edit-an-event) zur Verwendung in Journey auswählen.

   Um auf die Details für ein ausgewähltes Ereignis zuzugreifen, klicken Sie auf den Ereignisnamen.

### Filtern der Ereignisliste

Geben Sie Text in das _[!UICONTROL Suchen]_-Feld ein, um die angezeigten Ereignisse nach einer Übereinstimmung mit dem Ereignisnamen zu filtern.

![Filtern Sie die Liste der ausgewählten Ereignisse nach Namen](./assets/configurations-xdm-classes-events-search.png){width="600" zoomable="yes"}

### Ereignis hinzufügen

Um ein Erlebnisereignis für den Knoten _Lauschen auf ein Ereignis_ auf einer Journey verfügbar zu machen, wählen Sie das Ereignis und die unterstützten Felder aus.

>[!NOTE]
>
>In der Beta-Version können Sie keine Ereignisse aus der Liste entfernen. Stellen Sie sicher, dass jedes Ereignis, das Sie hinzufügen, für Ihre Organisation vorgesehen ist.

1. Klicken **[!UICONTROL oben]** auf „Erlebnisereignis auswählen“.

   Die Seite mit den Ereignisdetails wird angezeigt. Auf dieser Seite können Sie den Ereignistyp und die Felder auswählen.

   ![Ereignisdetails für ein neues Ereignis](./assets/configurations-xdm-classes-events-select-new.png){width="700" zoomable="yes"}

1. Wählen Sie den Ereignistyp.

   * Klicken Sie **[!UICONTROL Ereignistyp auswählen]**.

   * Wählen Sie im Dialogfeld den Ereignistyp aus.

     Filtern Sie _[!UICONTROL angezeigte Liste mithilfe]_ Felds „Suche“ nach Namen. Mit dem Schieberegler **[!UICONTROL Nur ausgewählte Felder anzeigen]** können Sie die aktuellen Auswahlen überprüfen.

     ![Dialogfeld „Ereignistyp auswählen“](./assets/configurations-xdm-classes-select-event-type-dialog.png){width="450" zoomable="yes"}

   * Klicken Sie auf **[!UICONTROL Auswählen]**.

1. Wählen Sie ein oder mehrere Felder für den Ereignistyp aus.

   * Klicken Sie **[!UICONTROL Felder auswählen]**.

   * Wählen Sie im Dialogfeld die Felder aus, die Sie als Einschränkungen für übereinstimmende Ereignisse verwenden möchten.

     Filtern Sie _[!UICONTROL angezeigte Liste mithilfe]_ Felds „Suche“ nach Namen. Mit dem Schieberegler **[!UICONTROL Nur ausgewählte Felder anzeigen]** können Sie die aktuellen Auswahlen überprüfen.

     ![Dialogfeld „Felder auswählen“](./assets/configurations-xdm-classes-select-fields-dialog.png){width="450" zoomable="yes"}

   * Klicken Sie auf **[!UICONTROL Auswählen]**.

1. Klicken Sie auf der Seite mit den Ereignisdetails auf **[!UICONTROL Speichern]**.

Das gespeicherte Ereignis wird in der Liste auf der Registerkarte _[!UICONTROL Ereignisse]_ angezeigt.

### Ereignis bearbeiten

Bearbeiten Sie die Ereignisdetails, um die Felder zu ändern.

1. Klicken Sie auf den Ereignisnamen oder auf das Symbol _Mehr Menü_ ( **…** ) und wählen Sie **[!UICONTROL Bearbeiten]**.

   ![Klicken Sie auf das Menüsymbol Mehr ](./assets/configurations-xdm-classes-events-more-menu.png){width="500" zoomable="yes"}

1. Klicken Sie **[!UICONTROL Felder bearbeiten]**, um im Dialogfeld „Felder _[!UICONTROL &quot; weitere Felder hinzuzufügen oder]_ Auswahl zu entfernen.

1. Klicken Sie **[!UICONTROL Auswählen]**, um Ihre Auswahl zu speichern.

### Ereignis entfernen

>[!NOTE]
>
>In der Beta-Version dieser Funktion können Sie kein Ereignis aus der Liste der ausgewählten Ereignisse entfernen. Für die GA-Version ist eine Entfernung von Ereignissen geplant.

<!-- ## Overview video

>[!VIDEO](https://video.tv.adobe.com/v/3448637/?learn=on) -->