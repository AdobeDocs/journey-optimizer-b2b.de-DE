---
title: Konto-Journeys
description: Erfahren Sie mehr über Account Journey und wie Sie sie erstellen und verwalten können.
feature: Account Journeys
exl-id: 5c22f11f-1967-4b55-8aee-16371173c040
source-git-commit: d03e0e2d8070916d38bb956adff8dea3f3873aad
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 4%

---


# Account Journey

Erstellen und führen Sie Journey aus, die für jede kaufende Gruppe und jedes kaufende Gruppenmitglied maßgeschneidert sind, indem Sie automatisierte Interaktionen für E-Mail, SMS, Ereignisse und mehr verwenden. Mit Account Journey können Sie die Nachfragegenerierung und die Kaufgruppenqualifizierung optimieren und mehr qualifizierte Nachfrage für Ihre Akquise-, Upsell-/Crosssell- und Kundenbindungsprogramme steigern.

Definieren Sie eine verkaufsgesteuerte Interaktion, die E-Mail, SMS und mehr innerhalb der Account-Journey umfasst, um das eingehende Marketing mit ausgehenden Verkaufsaktivitäten für jedes Mitglied der Einkaufsgruppe zu koordinieren.

![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Übersichtsvideo ansehen](#overview-video)

## Zugreifen auf und Durchsuchen von Account-Journey

1. Klicken Sie auf Ihrer Adobe Experience Platform-Startseite auf Adobe Journey Optimizer B2B edition.

1. Klicken Sie im linken Navigationsbereich auf **[!UICONTROL Account Journey]**.

   ![Zugriff auf Account Journey](./assets/account-journey-browse.png){width="800" zoomable="yes"}

   Die angezeigte Seite Journey enthält die folgenden Spalten:

   * [!UICONTROL Name] (auf den Namen klicken, um die Konto-Journey zur Bearbeitung zu öffnen)
   * [!UICONTROL Status]
   * [!UICONTROL Beschreibung]
   * [!UICONTROL Erstellt von]
   * [!UICONTROL Zuletzt aktualisiert um]
   * [!UICONTROL Zuletzt aktualisiert von]
   * [!UICONTROL Veröffentlicht am]
   * [!UICONTROL Veröffentlicht von]

Diese Tabelle bietet die Möglichkeit, nach Namen und „Erstellt von“ zu suchen. Die Sortierung ist derzeit nicht verfügbar.

Sie können die angezeigte Tabelle anpassen, indem Sie auf das Symbol _Spalten_ in der oberen rechten Ecke klicken und die Kontrollkästchen aktivieren oder deaktivieren.

![Wählen Sie die Spalten aus, die in der Liste der Konto-Journey angezeigt werden sollen](./assets/account-journeys-list-columns.png){width="800" zoomable="yes"}

## Anatomie einer Account-Journey

Klicken Sie auf den Namen (als Link angezeigt) in der Liste _[!UICONTROL Account-Journey]_, um die Details zu überprüfen, Änderungen vorzunehmen und Maßnahmen zu ergreifen.

![Konto-Journey-Arbeitsbereich](./assets/account-journey-workspace.png){width="800" zoomable="yes"}

Die Editor-Kopfzeile jeder Account-Journey enthält:

* Journey-Name
* Möglichkeit, den Namen zu bearbeiten (_Bearbeiten_-Symbol)
* Status der Journey

Die folgenden Aktionen sind in der Kopfzeile verfügbar:

* **Veröffentlichen** - Sie können eine Journey veröffentlichen, wenn keine Blocker-Fehler vorliegen. Nach der Veröffentlichung ändert sich der Journey-Status in _Live_. Wenn die Journey Fehler aufweist, ist die Schaltfläche mit folgenden Inhaltsinformationen abgeblendet: `Resolve errors before publishing`.
* **Duplizieren** - Diese Aktion ähnelt einer Klonfunktion, aber die duplizierte Journey enthält keine Assets.
* **Für neue Einträge schließen** - Wenn Sie eine Journey schließen, setzen Konten, die sich derzeit auf der Journey befinden, ihren Pfad auf der Journey fort, sodass kein weiterer Journey-Eintritt möglich ist. Ein geschlossener Journey kann nicht neu gestartet werden. Sie können eine geschlossene Journey duplizieren.
* **Abbruch** - Wenn Sie eine Journey stoppen, stoppen Konten auf der Journey sofort ihren Fortschritt und es kann kein weiterer Journey-Eintritt erfolgen. Ein gestoppter Journey kann nicht neu gestartet werden. Wenn Sie neue Eintritte blockieren, ohne den Fortschritt der Benutzer zu stoppen, sollten Sie stattdessen die Journey schließen.
* **Löschen** - Durch diese Aktion wird die Journey dauerhaft gelöscht.

Der Status einer Journey ändert sich je nach den von Ihnen durchgeführten Aktionen. Je nach Status einer Journey sind bestimmte Aktionen in der Kopfzeile nicht verfügbar.

| Status | Beschreibung | Verfügbare Aktionen |
| ------ | ----------- | ----------------- |
| _**Entwurf**_ | Eine unveröffentlichte Journey, die bearbeitbar ist. | <ul><li>Veröffentlichen Sie</li><li>Doppelt </li><li>Löschen </li></ul> |
| _**Live**_ | Der Journey-Status ändert sich von Entwurf zu Live, wenn eine Journey veröffentlicht wird. In diesem Zustand ist er nicht mehr bearbeitbar. | <ul><li>Doppelt </li><li>Für neue Einträge schließen </li><li>Abbrechen </li></ul> |
| _**Für neue Einträge geschlossen**_ | Der Journey-Status ändert sich von _Live_ zu _Geschlossen zu neuen Einträgen_ wenn Sie im oberen Navigationsbereich auf [!UICONTROL Für neue Einträge schließen] klicken. | <ul><li>Doppelt </li><li>Abbrechen </li></ul> |
| _**abgebrochen**_ | Der Journey-Status ändert sich von _Live_ oder _Geschlossen zu neuen_, wenn Sie eine Journey abbrechen. Eine abgebrochene Journey kann nicht neu gestartet werden. | <ul><li>Doppelt </li><li>Löschen </li></ul> |
| _**BEENDET**_ | Wenn alle Konten auf einer Journey die Journey abgeschlossen haben, ändert sich der Status von Live oder Geschlossen zu Neue Einträge zu Beendet. | <ul><li>Doppelt </li><li>Löschen </li></ul> |

## Erste Schritte mit einer Journey

Erste Schritte mit den Account-Journey:

1. [Erstellen einer Journey](./create-publish-journey.md#create-an-account-journey)
1. [Fügen Sie die Knoten hinzu](./create-publish-journey.md#add-a-node) und [definieren Sie den Journey-](./create-publish-journey.md#add-and-delete-a-path)) in der Journey-Zuordnung.
1. [Veröffentlichen Sie die Journey](./create-publish-journey.md#publish-an-account-journey).

## Übersichtsvideo

>[!VIDEO](https://video.tv.adobe.com/v/3443202/?learn=on)
