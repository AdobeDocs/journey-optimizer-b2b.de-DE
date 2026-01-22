---
title: Journey-Verwaltung
description: Optimieren Sie die Nachfragegenerierung mit Journey - Erstellen, veröffentlichen und verwalten Sie die Interaktion mit Einkaufsgruppen für E-Mail, SMS und Ereignisse in Journey Optimizer B2B edition.
feature: Account Journeys
role: User
exl-id: 5c22f11f-1967-4b55-8aee-16371173c040
source-git-commit: 6511f40329df34db665ed6f971fa20670be0ae32
workflow-type: tm+mt
source-wordcount: '1521'
ht-degree: 44%

---


# Journey-Verwaltung

In Journey Optimizer B2B edition sind Journey automatisierte, mehrstufige Account- und Lead-basierte Marketing-Pläne, die personalisierte Erlebnisse als Reaktion auf Interaktionen, Geschäftsereignisse oder geplante Kampagnen kanalübergreifend orchestrieren. Definieren Sie eine verkaufsgesteuerte Interaktion, die E-Mail, SMS und mehr umfasst, um das eingehende Marketing mit ausgehenden Verkaufsaktivitäten für jedes Mitglied der Einkaufsgruppe zu koordinieren.

Journey Optimizer B2B edition unterstützt zwei Journey-Typen:

* **Account-Journey** - Optimieren Sie die Nachfragegenerierung und die Kaufgruppenqualifizierung und steigern Sie die Nachfrage nach Ihren Akquise-, Upsell-/Crosssell- und Kundenbindungsprogrammen. Passen Sie Ihre Journeys an die individuellen Bedürfnisse jeder Käufergruppe und jedes Mitglieds einer Käufergruppe an, indem Sie automatisierte Interaktionen für E-Mails, SMS, Ereignisse und mehr verwenden. 

  ![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Übersichtsvideo zur Account-Journey ansehen](#overview-video)

* **Personen-Journey** - (Beta) Orchestrieren Sie Lead-basiertes Marketing mithilfe von Experience Platform-Zielgruppen und -Daten. Bei Personen-Journey sind Ihre Marketing-Vorgänge nicht auf Marketo Engage oder Problemumgehungen für Adobe Campaign/B2C-Toolketten angewiesen, damit sie mit B2B-Anwendungsfällen arbeiten können.

  Bei Verwendung in Kombination mit Account-Journeys und Einkaufsgruppen kann eine Personen-Journey Marketing-Fachleuten die Möglichkeit bieten, die Kauf-Journey vollständig zu orchestrieren.

  +++Aktuelle Einschränkungen für Personen-Journey

  Es gibt Einschränkungen, die bestimmte Anwendungsfälle blockieren oder Schwierigkeiten bei der Erstellung von Personen-Journey verursachen können. Viele Probleme sind das Ergebnis der ersten Implementierung des Beta-Programms, die in Zukunft angegangen werden muss.

   * Ereignisse können nicht mit Profilattributen kombiniert werden, um Zielgruppendefinitionen einzugrenzen.
   * Der Kontext des Ereignisses, das ein Profil für eine Journey qualifiziert, kann nicht für Personalisierung oder Orchestrierung verwendet werden.
   * Journey können derzeit nicht sowohl über ein Ereignis- als auch über ein Profilsegmenteinstiegskriterium verfügen.
   * Ereignis-Listener können nicht auf mehrere Ereignisse warten.
   * Warteknoten verfügen derzeit nicht über eine vollständige Suite von Optionen für die Ausstiegskriterien für den Wochentag oder die Tageszeit.
   * Der E-Mail-Editor verweist fälschlicherweise auf Funktionen und Attribute, die nur für Account-Journey verfügbar sind
   * Unterstützung für benutzerdefinierte Journey-Token (_Meine Token_) ist noch nicht verfügbar.
   * Das Hinzufügen und Entfernen von Personen-Journey-Knoten ist derzeit in keinem der Journey-Typen verfügbar.
   * Der Ereignisverlauf kann nicht für die Orchestrierung oder Personalisierung verwendet werden.
   * Zugehörige Objekte (z. B. Konto, Einkaufsgruppe, Opportunity und benutzerdefinierte Objekte) können nicht für die Orchestrierung oder Personalisierung verwendet werden.
   * Web-, SMS- und Anzeigenplattformkanäle werden derzeit nicht unterstützt.

  +++

## Erste Schritte mit einer Journey

Erste Schritte mit dem ersten Journey:

1. [Erstellen einer Journey](./create-publish-journey.md#create-a-journey).
1. [Fügen Sie die Knoten hinzu](./create-publish-journey.md#add-a-node) und [definieren Sie den Journey Flow](./create-publish-journey.md#add-and-delete-a-path) in der Journey Map.
1. [Veröffentlichen der Journey](./create-publish-journey.md#publish-a-journey).

## Zugreifen auf und Durchsuchen von Journey

>[!BEGINTABS]

>[!TAB Account Journey]

Erweitern Sie im linken Navigationsbereich die Option **[!UICONTROL Journey-]** und klicken Sie auf **[!UICONTROL Account-Journey]**.

Um die angezeigte Liste nach Namen zu filtern, geben Sie im Tool _Suchen_ oben in der Liste Text ein.

![Filtern der Liste der Konto-Journeys](./assets/account-journeys-list-search-filter.png){width="800" zoomable="yes"}

>[!TAB Personen-Journey (Beta)]

[!BADGE Beta]{type=Informative tooltip="Verfügbar als Beta-Funktion in der vereinfachten Architektur"}

Erweitern Sie im linken Navigationsbereich die Option **[!UICONTROL Journey-]** und klicken Sie auf **[!UICONTROL Personen-Journey]**.

Geben Sie oben in der Liste im _Suche_-Tool Text ein, um die angezeigte Liste nach Namen zu filtern.

![Filtern Sie die Liste der Journey](./assets/person-journeys-list-search-filter.png){width="800" zoomable="yes"}

>[!ENDTABS]

### Journey von Listenspalten

Die Listenseite Journey enthält die folgenden Spalten:

* [!UICONTROL Name] (klicken Sie auf den Namen, um die Konto-Journey zur Bearbeitung zu öffnen)
* [!UICONTROL Status]
* [!UICONTROL Erstellungsdatum]
* [!UICONTROL Erstellt von]
* [!UICONTROL Letzte Aktualisierung]
* [!UICONTROL Zuletzt aktualisiert von]
* [!UICONTROL Veröffentlicht auf]
* [!UICONTROL Veröffentlicht von]
* [!UICONTROL Startdatum]
* [!UICONTROL Enddatum]

Sie können die Liste nach _[!UICONTROL Status]_, _[!UICONTROL Erstellungsdatum]_ oder _[!UICONTROL Letzte Aktualisierung)]_, indem Sie auf die Spaltenüberschrift klicken.

Um die in der Tabelle angezeigten Spalten anzupassen (ein-/auszublenden), klicken Sie auf das Symbol _Tabelle anpassen_ (![Tabelle anpassen](../assets/do-not-localize/icon-column-settings.svg) ) in der oberen rechten Ecke. Aktivieren oder deaktivieren Sie die Kontrollkästchen im Dialogfeld und klicken Sie auf **[!UICONTROL Übernehmen]**.

![Wählen Sie die Spalten aus, die in der Liste Journey angezeigt werden sollen](./assets/account-journeys-list-columns.png){width="800" zoomable="yes"}

### Journey-Status

Der Status einer Journey kann sich entsprechend den von Ihnen durchgeführten Aktionen ändern. Je nach Status einer Journey stehen bestimmte Aktionen rechts in der Kopfzeile zur Verfügung oder nicht.

| Status | Beschreibung | Verfügbare Aktionen |
| ------ | ----------- | ----------------- |
| _**Entwurf**_ | Eine unveröffentlichte Journey, die bearbeitet werden kann. | <li>[Veröffentlichen](./create-publish-journey.md#publish-a-journey)<li>[Duplizieren](#duplicate-journey) <li>[Löschen](#delete-journey) |
| _**Live**_ | Der Journey-Status ändert sich von _Entwurf_ zu _Live_, wenn eine Journey veröffentlicht wird. In diesem Status kann sie nicht mehr bearbeitet werden. | <li>[Duplizieren](#duplicate-journey)<li>[Für neue Eintritte schließen](#close-to-new-entries) <li>[Abbrechen](#abort-journey) |
| _**Für neue Eintritte geschlossen**_ | Der Journey-Status ändert sich von _Live_ zu _Für neue Eintritte geschlossen_, wenn Sie in der oberen Navigation auf [!UICONTROL Für neue Eintritte schließen] klicken. | <li>[Duplizieren](#duplicate-journey) <li>[Abbrechen](#abort-journey) |
| _**Abgebrochen**_ | Der Journey-Status ändert sich von _Live_ oder _Für neue Eintritte geschlossen_, wenn Sie eine Journey abbrechen. Eine abgebrochene Journey kann nicht neu gestartet werden. | <li>[Duplizieren](#duplicate-journey) <li>[Löschen](#delete-journey) |
| _**Beendet**_ | Wenn alle Mitglieder der Konto- oder Personen-Zielgruppe auf einer Journey die Journey abschließen, ändert sich der Status von _Live_ oder _Geschlossen zu neuen Einträgen_ zu _Abgeschlossen_. | <li>[Duplizieren](#duplicate-journey) <li>[Löschen](#delete-journey) |

## Journey-Maps

Klicken Sie auf den Namen (als Link angezeigt) in der Liste Journey , um die Details zu überprüfen, Änderungen vorzunehmen und Maßnahmen zu ergreifen.

![Konto-Journey-Arbeitsbereich](./assets/account-journey-workspace.png){width="800" zoomable="yes"}

Die Kopfzeile jeder Journey-Zuordnung enthält:

* Journey-Name
* Tool „Bearbeiten“ für den Journey-Namen (![Symbol Bearbeiten](../assets/do-not-localize/icon-edit.svg) _Bearbeiten_-Symbol)
* [Status](#journey-status) der Journey

In der Journey-Zuordnung können Sie [Knoten hinzufügen](./create-publish-journey.md#add-a-node) und [den Journey-Fluss definieren](./create-publish-journey.md#add-and-delete-a-path).

## Journey-Aktionen

Die Journey-Listenseite enthält alle Journey von Konten oder Personen in Ihrer Journey Optimizer B2B edition-Instanz. Auf der Listenseite können Sie eine Reihe von Aktionen auf eine Journey anwenden.

### Abbrechen von Journeys

Wenn Sie eine Live- oder geplante Journey abbrechen (stoppen), stoppen Accounts oder Personen auf der Journey sofort ihren Fortschritt, und es kann kein weiterer Journey-Eintritt erfolgen. Eine abgebrochene Journey kann nicht neu gestartet werden.

>[!IMPORTANT]
>
>Wenn die Journey auf einer anderen Journey von einem &quot;_Aktion ausführen_-Knoten mit der Aktion _[!UICONTROL Konto zu (anderer) Journey hinzufügen]_ verwendet wird, blockiert das Abbrechen der Journey diese Aktion auf dieser Journey.

1. Klicken Sie auf den Namen der Journey, um sie zu öffnen.

1. Klicken Sie oben rechts auf das Menü **[!UICONTROL Mehr...]** und wählen Sie **[!UICONTROL Abbrechen]** aus.

   ![Klicken auf „Mehr“ oben rechts](./assets/account-journey-live-more-menu.png){width="450"}

1. Klicken Sie im Bestätigungsdialogfeld auf **[!UICONTROL Abbrechen]**.

### Schließen für neue Eintritte

Wenn Sie eine Live-Journey schließen, setzen die derzeit in der Journey befindlichen Konten ihren Pfad in der Journey fort und weitere Journey-Eintritte sind nicht möglich. Eine geschlossene Journey kann nicht neu gestartet werden. Sie können eine geschlossene Journey duplizieren.

>[!IMPORTANT]
>
>Wenn die Journey auf einer anderen Journey von einem &quot;_Aktion ausführen_-Knoten mit der Aktion _[!UICONTROL Konto zu (anderem) Journey hinzufügen]_ verwendet wird, blockiert das Schließen auf neue Einträge diese Aktion von dieser Journey.

1. Klicken Sie auf den Namen der Journey, um sie zu öffnen.

1. Klicken Sie oben rechts auf das Menü **[!UICONTROL Mehr...]** und wählen Sie **[!UICONTROL Für neue Eintritte schließen]** aus.

1. Klicken Sie im Bestätigungsdialogfeld auf **[!UICONTROL Für neue Einträge schließen]**.

### Duplizieren einer Journey

Die Aktion „Duplizieren“ ähnelt einer Klonfunktion, wobei eine duplizierte Journey aber keine erstellten Journey-Inhalts-Assets enthält. Sie können die Details für die Journey oder nur ein einfaches _der Fluss_ und Pfadstruktur duplizieren.

>[!NOTE]
>
>Diese Aktion ist derzeit nicht für Personen-Journey verfügbar.

1. Klicken Sie auf das Symbol _Mehr_ (**…**) neben dem Journey-Namen und wählen Sie **[!UICONTROL Duplizieren]**.

   ![Klicken auf das Symbol „…“ und Wählen der Option „Duplizieren“](./assets/account-journeys-list-more-menu.png){width="450"}

   Abhängig vom Status der Journey können Sie über die Journey-Details oder die Journey-Zuordnung auch auf die Duplikataktion zugreifen:

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

   Die duplizierte Journey wird in der Journey-Zuordnung geöffnet, wo Sie die Details festlegen und Journey-Inhalte nach Bedarf erstellen können.

### Löschen einer Journey

Verwenden Sie die Aktion „Löschen“, um eine Journey dauerhaft zu löschen. Live-Journeys oder geplante Journeys können nicht gelöscht werden.

1. Klicken Sie auf das Symbol _Mehr_ (**…**) neben dem Journey-Namen und wählen Sie **[!UICONTROL Löschen]**.

   Je nach Status der Journey können Sie auch über die Journey-Details oder die Journey-Zuordnung auf die Löschaktion zugreifen:

   * Klicken Sie bei einer Journey mit dem Status „Entwurf“ oben rechts auf **[!UICONTROL Mehr...]** und wählen Sie **[!UICONTROL Löschen]**.

   * Klicken Sie bei anderen Journeys mit anderen Status wie _Abgeschlossen_ oder _Abgebrochen_ oben rechts auf **[!UICONTROL Löschen]**.

1. Klicken Sie im Bestätigungsdialog auf **[!UICONTROL Löschen]**.

## Überprüfen des Kontofortschritts

Für eine veröffentlichte Account-Journey mit dem Status _Live_, _Geschlossen für neue Einträge_, _Abgebrochen_ oder _Abgeschlossen_ können Sie die Journey-Zuordnung öffnen, um den Kontofortschritt für die Journey-Knoten zu überprüfen. Jeder Knoten in der Map zeigt die Anzahl der Konten an, die diesen Knoten erreichen, sowie bei Live-Journeys die Anzahl der Konten, die sich aktuell an diesem Knoten befinden.

![Informationen zum Kontofortschritt an den Journey-Knoten](./assets/node-account-progression-observability.png){width="400"}

Wenn Sie den Knoten auswählen, klicken Sie auf die Zahl, um eine Liste der Konten anzuzeigen, die in den Knoten eingetreten sind oder sich derzeit an diesem Schritt der Journey befinden.

![Informationen zum Kontofortschritt an den Journey-Knoten](./assets/node-accounts-entered-list.png){width="700" zoomable="yes"}

## Übersichtsvideo zur Account-Journey {#overview-video}

>[!VIDEO](https://video.tv.adobe.com/v/3443202/?learn=on)
