---
title: Konto-Journeys
description: Erfahren Sie mehr über Konto-Journeys und darüber, wie Sie sie erstellen und verwalten können.
feature: Account Journeys
exl-id: 5c22f11f-1967-4b55-8aee-16371173c040
source-git-commit: bd6f998b610c6f3a4d7c0e1fce5db4bb72b8a1e3
workflow-type: tm+mt
source-wordcount: '1022'
ht-degree: 30%

---


# Konto-Journeys

Mit Account Journeys können Sie die Nachfragegenerierung und die Kaufgruppenqualifizierung optimieren und mehr qualifizierte Nachfrage für Ihre Akquise-, Upsell-/Crosssell- und Kundenbindungsprogramme steigern. Passen Sie Ihre Journey für jede kaufende Gruppe und jedes kaufende Gruppenmitglied an, indem Sie automatisierte Interaktionen für E-Mail, SMS, Ereignisse und mehr verwenden.

Definieren Sie eine vertriebsorientierte Interaktion, die E-Mail, SMS und mehr innerhalb der Konto-Journeys umfasst, um das eingehende Marketing mit ausgehenden Vertriebsaktivitäten für jedes Mitglied der Käufergruppe zu koordinieren.

![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Übersichtsvideo ansehen](#overview-video)

## Erste Schritte mit einer Journey

Ihre ersten Schritte mit Konto-Journeys:

1. [Erstellen einer Journey](./create-publish-journey.md#create-an-account-journey).
1. [Fügen Sie die Knoten hinzu](./create-publish-journey.md#add-a-node) und [definieren Sie den Journey Flow](./create-publish-journey.md#add-and-delete-a-path) in der Journey Map.
1. [Veröffentlichen der Journey](./create-publish-journey.md#publish-an-account-journey).

## Aufrufen und Durchsuchen von Konto-Journeys

1. Klicken Sie auf Ihrer Adobe Experience Platform-Startseite auf „Adobe Journey Optimizer B2B Edition“.

1. Klicken Sie in der linken Navigationsleiste auf **[!UICONTROL Konto-Journeys]**.

   ![Auf Konto-Journeys zugreifen](./assets/account-journey-browse.png){width="800" zoomable="yes"}

   Die angezeigte Seite „Journeys“ enthält die folgenden Spalten:

   * [!UICONTROL Name] (klicken Sie auf den Namen, um die Journey zur Bearbeitung zu öffnen)
   * [!UICONTROL Status]
   * [!UICONTROL Beschreibung]
   * [!UICONTROL Erstellt von]
   * [!UICONTROL Zuletzt aktualisiert]
   * [!UICONTROL Zuletzt aktualisiert von]
   * [!UICONTROL Veröffentlicht auf]
   * [!UICONTROL Veröffentlicht von]

Verwenden Sie das _Suche_-Tool oben, um die Journey anhand des Namens zu finden. Sie können die Liste nach (_[!UICONTROL ) sortieren]_ indem Sie auf die Spaltenüberschrift klicken.

Sie können die in der Tabelle angezeigten Spalten anpassen, indem Sie auf das Symbol _Tabelle anpassen_ ( ![Tabelle anpassen](../assets/do-not-localize/icon-column-settings.svg) ) in der oberen rechten Ecke klicken. Aktivieren oder deaktivieren Sie die Kontrollkästchen im Dialogfeld und klicken Sie auf **[!UICONTROL Übernehmen]**.

![Auswählen der Spalten, die in der Liste der Konto-Journeys angezeigt werden sollen](./assets/account-journeys-list-columns.png){width="800" zoomable="yes"}

## Anatomie einer Konto-Journey

Klicken Sie auf den Namen (als Link angezeigt) in der Liste _[!UICONTROL Konto-Journeys]_, um die Details zu überprüfen, Änderungen vorzunehmen und Maßnahmen zu ergreifen.

![Konto-Journey-Arbeitsbereich](./assets/account-journey-workspace.png){width="800" zoomable="yes"}

Die Kopfzeile jeder Account-Journey-Zuordnung enthält:

* Journey-Name
* Zugriff zum Bearbeiten des Journey-Namens (![Bearbeiten-Symbol](../assets/do-not-localize/icon-edit.svg) _Bearbeiten_-Symbol)
* Status der Journey

Der Status einer Journey kann sich je nach den von Ihnen durchgeführten Aktionen ändern. Je nach Status einer Journey stehen bestimmte Aktionen nicht rechts in der Kopfzeile zur Verfügung.

| Status | Beschreibung | Verfügbare Aktionen |
| ------ | ----------- | ----------------- |
| _**Entwurf**_ | Eine unveröffentlichte Journey, die bearbeitet werden kann. | <ul><li>[Veröffentlichen](./create-publish-journey.md#publish-an-account-journey)</li><li>Duplizieren </li><li>Löschen </li></ul> |
| _**Live**_ | Wenn eine Journey veröffentlicht wird, ändert sich der Journey-Status von „Entwurf“ zu „Live“,. In diesem Status kann sie nicht mehr bearbeitet werden. | <ul><li>Duplizieren </li><li>Für neue Eintritte schließen </li><li>Abbrechen </li></ul> |
| _**Für neue Eintritte geschlossen**_ | Der Journey-Status ändert sich von _Live_ zu _Für neue Eintritte geschlossen_, wenn Sie in der oberen Navigation auf [!UICONTROL Für neue Eintritte schließen] klicken. | <ul><li>Duplizieren </li><li>Abbrechen </li></ul> |
| _**Abgebrochen**_ | Der Journey-Status ändert sich von _Live_ oder _Für neue Eintritte geschlossen_, wenn Sie eine Journey abbrechen. Eine abgebrochene Journey kann nicht neu gestartet werden. | <ul><li>Duplizieren </li><li>Löschen </li></ul> |
| _**Beendet**_ | Wenn alle Konten in einer Journey die Journey abgeschlossen haben, ändert sich der Status von „Live“ oder „Für neue Eintritte geschlossen“ zu „Beendet“. | <ul><li>Duplizieren </li><li>Löschen </li></ul> |

## Journey verwalten

Die _Account Journey_-Liste enthält alle Journey in Ihrer Journey Optimizer B2B edition-Instanz.

### Journey abbrechen

Wenn Sie eine Live- oder geplante Journey abbrechen (stoppen), wird der Fortschritt der Konten auf der Journey sofort gestoppt, und es kann kein weiterer Journey-Eintritt erfolgen. Eine abgebrochene Journey kann nicht neu gestartet werden.

>[!IMPORTANT]
>
>Wenn die Konto-Journey auf einer anderen Journey von einem Knoten _Aktion ausführen_ mit der Aktion _Konto zu (anderer) Journey hinzufügen_ verwendet wird, blockiert das Abbrechen der Journey diese Aktion von dieser Journey.

1. Klicken Sie auf den Namen der Journey, um sie zu öffnen.

1. Klicken Sie oben rechts auf das **[!UICONTROL Mehr…]** und wählen Sie **[!UICONTROL Abbrechen]**.

   ![Klicken Sie oben rechts auf Mehr](./assets/account-journey-live-more-menu.png){width="450"}

1. Klicken Sie im Bestätigungsdialogfeld auf **[!UICONTROL Abbrechen]**.

### Für neue Eintritte schließen

Wenn Sie eine Live-Journey schließen, setzen Accounts, die sich derzeit auf der Journey befinden, ihren Pfad auf dieser Journey fort, sodass kein weiterer Journey-Eintritt möglich ist. Eine geschlossene Journey kann nicht neu gestartet werden. Sie können eine geschlossene Journey duplizieren.

>[!IMPORTANT]
>
>Wenn die Konto-Journey auf einer anderen Journey von einem Knoten _Aktion ausführen_ mit der Aktion _Konto zu (anderem) Journey hinzufügen_ verwendet wird, blockiert das Schließen auf neue Einträge diese Aktion von dieser Journey.

1. Klicken Sie auf den Namen der Journey, um sie zu öffnen.

1. Klicken Sie oben rechts auf das **[!UICONTROL Mehr…]** und wählen Sie **[!UICONTROL Für neue Einträge schließen]**.

1. Klicken Sie im Bestätigungsdialogfeld auf **[!UICONTROL Für neue Einträge schließen]**.

### Journey duplizieren

Eine Duplikataktion ähnelt einer Klonfunktion, aber eine duplizierte Journey enthält keine erstellten Journey-Inhalts-Assets. Sie können die Details für die Konto-Journey duplizieren oder einfach nur ein _Skelett_ der Fluss- und Pfadstruktur.

1. Klicken Sie auf das _Mehr_-Symbol (**…**) neben dem Journey-Namen und wählen Sie **[!UICONTROL Duplizieren]**.

   ![Klicken Sie auf das Symbol … und wählen Sie Duplizieren](./assets/account-journeys-list-more-menu.png){width="450"}

   Abhängig vom Status der Konto-Journey können Sie über die Journey-Details oder die Journey-Zuordnung auch auf die Duplikataktion zugreifen:

   * Klicken Sie bei einer Journey mit Entwurf oben rechts auf das **[!UICONTROL Mehr…]** und wählen Sie **[!UICONTROL Duplizieren]**.

   * Klicken Sie für alle anderen Journey-Status **[!UICONTROL oben]** auf „Duplizieren“.

     ![Klicken Sie oben rechts auf Duplizieren](./assets/account-journey-duplicate-button.png){width="450"}

1. Legen _im Dialogfeld Journey duplizieren_ die Werte **[!UICONTROL Name]** und **[!UICONTROL Description]** für die neue Journey fest.

   Standardmäßig verwendet das Dialogfeld den Namen der duplizierten Journey, an die __copy_ angehängt wird. Geben Sie bei Bedarf einen anderen eindeutigen Namen für die Journey ein.

   ![Dialogfeld &quot;Journey duplizieren“](./assets/account-journey-duplicate-dialog.png){width="400"}

1. Wählen Sie die Duplizierung **[!UICONTROL Typ]**:

   * **[!UICONTROL Partielle Inhaltsduplizierung]** - Verwenden Sie diesen Typ, um alles auf der Journey zu kopieren, mit Ausnahme aller erstellten E-Mails oder SMS-Nachrichten. Knoten, die auf eine Marketo Engage-E-Mail- oder -SMS-Nachricht verweisen, sind vollständig intakt.

   * **[!UICONTROL Ohne Details duplizieren]** - Verwenden Sie diesen Typ, um nur die Knotenstruktur und die Pfade zu kopieren. Alle Knoteneinstellungen und Pfadbedingungen sind nicht definiert (Standard), sodass Sie den grundlegenden Fluss mit verschiedenen Zielgruppen-, Aktionen- und Pfadsegmentierungseinstellungen wiederverwenden können. Alle _Warten_-Knoten verwenden den Standardwert von fünf Tagen.

1. Klicken Sie **[!UICONTROL Duplizieren]**.

   Die duplizierte Konto-Journey wird in der Journey-Zuordnung geöffnet, wo Sie die Details festlegen und nach Bedarf Journey-Inhalte erstellen können.

### Journey löschen

Verwenden Sie eine Löschaktion, um eine Journey dauerhaft zu löschen. Live- oder geplante Journey können nicht gelöscht werden.

1. Klicken Sie auf das _Mehr_-Symbol (**…**) neben dem Journey-Namen und wählen Sie **[!UICONTROL Löschen]**.

   Abhängig vom Status der Konto-Journey können Sie auch über die Journey-Details oder die Journey-Zuordnung auf die Löschaktion zugreifen:

   * Klicken Sie bei einer Journey mit Entwurf oben rechts auf das **[!UICONTROL Mehr…]** und wählen Sie **[!UICONTROL Löschen]**.

   * Klicken Sie bei anderen Journey-Status _wie &quot;_&quot; oder _Abgebrochen_ oben rechts auf **[!UICONTROL Löschen]**.

1. Klicken Sie im Bestätigungsdialogfeld auf **[!UICONTROL Löschen]**.

## Übersichtsvideo

>[!VIDEO](https://video.tv.adobe.com/v/3443202/?learn=on)
