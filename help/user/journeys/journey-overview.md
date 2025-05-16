---
title: Konto-Journeys
description: Erfahren Sie mehr über Konto-Journeys und darüber, wie Sie sie erstellen und verwalten können.
feature: Account Journeys
role: User
exl-id: 5c22f11f-1967-4b55-8aee-16371173c040
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '1009'
ht-degree: 100%

---


# Konto-Journeys

Mit Konto-Journeys können Sie die Nachfragegenerierung sowie die Qualifizierung von Käufergruppen optimieren und die qualifizierte Nachfrage für Ihre Akquise-, Upsell-/Crosssell- und Kundenbindungsprogramme steigern. Passen Sie Ihre Journeys an die individuellen Bedürfnisse jeder Käufergruppe und jedes Mitglieds einer Käufergruppe an, indem Sie automatisierte Interaktionen für E-Mails, SMS, Ereignisse und mehr verwenden. 

Definieren Sie eine vertriebsorientierte Interaktion, die E-Mail, SMS und mehr innerhalb der Konto-Journeys umfasst, um das eingehende Marketing mit ausgehenden Vertriebsaktivitäten für jedes Mitglied der Käufergruppe zu koordinieren.

![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Übersichtsvideo ansehen](#overview-video)

## Erste Schritte mit einer Journey

Ihre ersten Schritte mit Konto-Journeys:

1. [Erstellen einer Journey](./create-publish-journey.md#create-an-account-journey).
1. [Fügen Sie die Knoten hinzu](./create-publish-journey.md#add-a-node) und [definieren Sie den Journey Flow](./create-publish-journey.md#add-and-delete-a-path) in der Journey Map.
1. [Veröffentlichen der Journey](./create-publish-journey.md#publish-an-account-journey).

## Aufrufen und Durchsuchen von Konto-Journeys

Klicken Sie in der linken Navigationsleiste auf **[!UICONTROL Konto-Journeys]**.

![Auf Konto-Journeys zugreifen](./assets/account-journey-browse.png){width="800" zoomable="yes"}

Die angezeigte Seite „Journeys“ enthält die folgenden Spalten:

* [!UICONTROL Name] (klicken Sie auf den Namen, um die Konto-Journey zur Bearbeitung zu öffnen)
* [!UICONTROL Status]
* [!UICONTROL Beschreibung]
* [!UICONTROL Erstellt von]
* [!UICONTROL Zuletzt aktualisiert]
* [!UICONTROL Zuletzt aktualisiert von]
* [!UICONTROL Veröffentlicht auf]
* [!UICONTROL Veröffentlicht von]

Verwenden Sie oben das Tool _Suchen_, um nach der Journey anhand ihres Namens zu suchen. Sie können die Liste nach _[!UICONTROL Status]_ sortieren, indem Sie auf die Spaltenüberschrift klicken.

Sie können die in der Tabelle angezeigten Spalten anpassen, indem Sie oben rechts auf das Symbol _Tabelle anpassen_ ( ![Tabelle anpassen](../assets/do-not-localize/icon-column-settings.svg) ) klicken. Aktivieren oder deaktivieren Sie die Kontrollkästchen im Dialogfeld und klicken Sie auf **[!UICONTROL Übernehmen]**.

![Auswählen der Spalten, die in der Liste der Konto-Journeys angezeigt werden sollen](./assets/account-journeys-list-columns.png){width="800" zoomable="yes"}

## Anatomie einer Konto-Journey

Klicken Sie auf den Namen (als Link angezeigt) in der Liste _[!UICONTROL Konto-Journeys]_, um die Details zu überprüfen, Änderungen vorzunehmen und Maßnahmen zu ergreifen.

![Konto-Journey-Arbeitsbereich](./assets/account-journey-workspace.png){width="800" zoomable="yes"}

Die Kopfzeile jeder Journey Map eines Kontos enthält:

* Journey-Name
* Zugriff zum Bearbeiten des Journey-Namens (Symbol ![Bearbeiten-Symbol](../assets/do-not-localize/icon-edit.svg) _Bearbeiten_)
* Status der Journey

Der Status einer Journey kann sich entsprechend den von Ihnen durchgeführten Aktionen ändern. Je nach Status einer Journey stehen bestimmte Aktionen rechts in der Kopfzeile zur Verfügung oder nicht.

| Status | Beschreibung | Verfügbare Aktionen |
| ------ | ----------- | ----------------- |
| _**Entwurf**_ | Eine unveröffentlichte Journey, die bearbeitet werden kann. | <ul><li>[Veröffentlichen](./create-publish-journey.md#publish-an-account-journey)</li><li>Duplizieren </li><li>Löschen </li></ul> |
| _**Live**_ | Wenn eine Journey veröffentlicht wird, ändert sich der Journey-Status von „Entwurf“ zu „Live“,. In diesem Status kann sie nicht mehr bearbeitet werden. | <ul><li>Duplizieren </li><li>Schließen für neue Eintritte </li><li>Abbrechen </li></ul> |
| _**Für neue Eintritte geschlossen**_ | Der Journey-Status ändert sich von _Live_ zu _Für neue Eintritte geschlossen_, wenn Sie in der oberen Navigation auf [!UICONTROL Für neue Eintritte schließen] klicken. | <ul><li>Duplizieren </li><li>Abbrechen </li></ul> |
| _**Abgebrochen**_ | Der Journey-Status ändert sich von _Live_ oder _Für neue Eintritte geschlossen_, wenn Sie eine Journey abbrechen. Eine abgebrochene Journey kann nicht neu gestartet werden. | <ul><li>Duplizieren </li><li>Löschen </li></ul> |
| _**Beendet**_ | Wenn alle Konten in einer Journey die Journey abgeschlossen haben, ändert sich der Status von „Live“ oder „Für neue Eintritte geschlossen“ zu „Beendet“. | <ul><li>Duplizieren </li><li>Löschen </li></ul> |

## Verwalten von Journeys

Die Liste _Konto-Journeys_ enthält alle Journeys in Ihrer Journey Optimizer B2B Edition-Instanz.

### Abbrechen von Journeys

Wenn Sie eine Live-Journey oder geplante Journey abbrechen (stoppen), wird der Journey-Fortschritt der Konten sofort gestoppt und es kann kein weiterer Journey-Eintritt erfolgen. Eine abgebrochene Journey kann nicht neu gestartet werden.

>[!IMPORTANT]
>
>Wenn die Konto-Journey in einer anderen Journey von einem Knoten _Aktion durchführen_ mit der Aktion _Konto zu (anderer) Journey hinzufügen_ verwendet wird, wird durch den Journey-Abbruch diese Aktion von dieser Journey geblockt.

1. Klicken Sie auf den Namen der Journey, um sie zu öffnen.

1. Klicken Sie oben rechts auf das Menü **[!UICONTROL Mehr...]** und wählen Sie **[!UICONTROL Abbrechen]** aus.

   ![Klicken auf „Mehr“ oben rechts](./assets/account-journey-live-more-menu.png){width="450"}

1. Klicken Sie im Bestätigungsdialogfeld auf **[!UICONTROL Abbrechen]**.

### Schließen für neue Eintritte

Wenn Sie eine Live-Journey schließen, setzen die derzeit in der Journey befindlichen Konten ihren Pfad in der Journey fort und weitere Journey-Eintritte sind nicht möglich. Eine geschlossene Journey kann nicht neu gestartet werden. Sie können eine geschlossene Journey duplizieren.

>[!IMPORTANT]
>
>Wenn die Konto-Journey in einer anderen Journey von einem Knoten _Aktion durchführen_ mit der Aktion _Konto zu (anderer) Journey hinzufügen_ verwendet wird, wird durch das Schließen für neue Eintritte diese Aktion von dieser Journey geblockt.

1. Klicken Sie auf den Namen der Journey, um sie zu öffnen.

1. Klicken Sie oben rechts auf das Menü **[!UICONTROL Mehr...]** und wählen Sie **[!UICONTROL Für neue Eintritte schließen]** aus.

1. Klicken Sie im Bestätigungsdialogfeld auf **[!UICONTROL Für neue Einträge schließen]**.

### Duplizieren von Journeys

Die Aktion „Duplizieren“ ähnelt einer Klonfunktion, wobei eine duplizierte Journey aber keine erstellten Journey-Inhalts-Assets enthält. Sie können die Details für die Konto-Journey duplizieren oder einfach nur eine simple _Basis_ der Fluss- und Pfadstruktur.

1. Klicken Sie auf das Symbol _Mehr_ (**…**) neben dem Journey-Namen und wählen Sie **[!UICONTROL Duplizieren]**.

   ![Klicken auf das Symbol „…“ und Wählen der Option „Duplizieren“](./assets/account-journeys-list-more-menu.png){width="450"}

   Abhängig vom Status der Konto-Journey können Sie über die Journey-Details oder die Journey Map auch auf die Aktion „Duplizieren“ zugreifen:

   * Klicken Sie bei einer Journey mit dem Status „Entwurf“ oben rechts auf **[!UICONTROL Mehr...]** und wählen Sie **[!UICONTROL Duplizieren]**.

   * Klicken Sie bei Journeys mit anderen Status oben rechts auf **[!UICONTROL Duplizieren]**.

     ![Klicken auf „Duplizieren“ oben rechts](./assets/account-journey-duplicate-button.png){width="450"}

1. Legen Sie im Dialogfeld _Journey duplizieren_ den **[!UICONTROL Namen]** und die **[!UICONTROL Beschreibung]** für die neue Journey fest.

   Standardmäßig verwendet das Dialogfeld den Namen der duplizierten Journey, an den __Kopie_ angehängt wird. Geben Sie bei Bedarf einen anderen eindeutigen Namen für die Journey ein.

   ![Dialogfeld „Journey duplizieren“](./assets/account-journey-duplicate-dialog.png){width="400"}

1. Wählen Sie den **[!UICONTROL Typ]** der Duplizierung:

   * **[!UICONTROL Duplizierung von Teilinhalten]**: Verwenden Sie diesen Typ, um alles in der Journey zu kopieren, ausgenommen alle erstellten E-Mails bzw. SMS-Nachrichten. Knoten, die auf eine Marketo Engage-E-Mail oder -SMS verweisen, sind vollständig intakt.

   * **[!UICONTROL Ohne Details duplizieren]**: Verwenden Sie diesen Typ, um nur die Knotenstruktur und Pfade zu kopieren. Alle Knoteneinstellungen und Pfadbedingungen sind nicht definiert (Standard), sodass Sie den grundlegenden Fluss mit unterschiedlichen Einstellungen für Zielgruppen, Aktionen und Pfadsegmentierungen wiederverwenden können. Alle Knoten vom Typ _Warten_ verwenden den Standardwert von fünf Tagen.

1. Klicken Sie auf **[!UICONTROL Duplizieren]**.

   Die duplizierte Konto-Journey wird in der Journey Map geöffnet. Hier können Sie nach Bedarf die Details festlegen und Journey-Inhalte erstellen.

### Löschen von Journeys

Verwenden Sie die Aktion „Löschen“, um eine Journey dauerhaft zu löschen. Live-Journeys oder geplante Journeys können nicht gelöscht werden.

1. Klicken Sie auf das Symbol _Mehr_ (**…**) neben dem Journey-Namen und wählen Sie **[!UICONTROL Löschen]**.

   Abhängig vom Status der Konto-Journey können Sie über die Journey-Details oder die Journey Map auch auf die Aktion „Löschen“ zugreifen:

   * Klicken Sie bei einer Journey mit dem Status „Entwurf“ oben rechts auf **[!UICONTROL Mehr...]** und wählen Sie **[!UICONTROL Löschen]**.

   * Klicken Sie bei anderen Journeys mit anderen Status wie _Abgeschlossen_ oder _Abgebrochen_ oben rechts auf **[!UICONTROL Löschen]**.

1. Klicken Sie im Bestätigungsdialog auf **[!UICONTROL Löschen]**.

## Übersichtsvideo

>[!VIDEO](https://video.tv.adobe.com/v/3443216/?learn=on&captions=ger)
