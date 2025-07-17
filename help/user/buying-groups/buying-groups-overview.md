---
title: Käufergruppen
description: Erfahren Sie, wie Käufergruppen in Journey Optimizer B2B Edition die Effektivität des Marketings durch das Identifizieren und Targeting von Mitgliedern für Ihre Kontolisten steigern können.
feature: Buying Groups
role: User
exl-id: ddcd7b62-6a76-4f5e-b6d3-a20944ca8332
source-git-commit: 92916a9d018084dd10681cbe9e9e54a5970c3c94
workflow-type: tm+mt
source-wordcount: '2151'
ht-degree: 57%

---


# Käufergruppen

Bei B2B-Vertriebs- und Marketing-Aktivitäten sind Konten wichtig für jede Strategie. Jedem Konto ist eine Gruppe von Personen zugeordnet, und diese Personen können Mitarbeitende des Kontos oder Auftragnehmer sein, die mit dem Konto arbeiten. Konten sind hierarchisch, und verschiedene Produkte können auf verschiedenen Ebenen in der Hierarchie verkauft werden. Adobe Experience Platform kann beispielsweise auf Unternehmensebene an einn Konto der obersten Ebene verkauft werden. Adobe Photoshop wird möglicherweise an ein Konto verkauft, das einen Geschäftsbereich oder eine Abteilung innerhalb eines Unternehmens repräsentiert, z. B. eine Design-Abteilung innerhalb eines größeren Unternehmens.

![Diagramm zu Kontorollen](assets/account-roles-diagram.png){width="800"}

Innerhalb des Kontos könnte es eine Teilmenge von Personen geben, die die _Käufergruppe_ umfassen. Dies sind die Personen, die letztendlich die Kaufentscheidung treffen. Sie benötigen daher besondere Aufmerksamkeit von der Marketing-Fachkraft und ihnen müssen möglicherweise andere Informationen bereitgestellt werden als anderen Personen, die dem Konto zugeordnet sind. Käufergruppen können unterschiedliche Personengruppen für verschiedene Produktlinien oder Angebote umfassen. Beispielsweise kann für ein Cybersicherheitsprodukt in der Regel ein Chief Information Officer oder ein Chief Security Officer sowie ein Vertreter der Rechtsabteilung erforderlich sein, um einen Kauf zu genehmigen. Ein Produkt zur Fehlersuche kann in der Regel einen VP of Engineering und einen IT Director als Mitglieder der kaufenden Gruppe haben.

![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Videoüberblick ansehen](#overview-video)

## Wichtige Komponenten

Sie können die Marketing-Effektivität steigern, indem Sie in Journey Optimizer B2B edition Einkaufsgruppen einrichten, die Mitglieder für Ihre Target-Kontolisten basierend auf den Lösungen identifizieren, für die Ihre Vertriebsteams verantwortlich sind. Bevor Sie und Ihr Marketing-Team mit der Erstellung Ihrer Einkaufsgruppen beginnen, stellen Sie sicher, dass Sie die Schlüsselkomponenten definiert haben. Diese Komponenten sind für die Erreichung Ihrer Geschäftsziele von entscheidender Bedeutung.

| Komponente | Zweck |
| --------- | ------- |
| Lösungsinteresse | Diese Komponente bietet die Antwort auf: <ul><li>Was verkaufen Sie als Marketing-Organisation?</li><li>Welches Produkt oder welche Produktkollektion möchten Sie verkaufen?</li></ul>  **_Example:_** Crossselling new Product X to existing customers |
| Kontozielgruppe | Diese Komponente bietet die Antwort auf: <ul><li>An wen verkaufen Sie?</li><li>Auf welche Kontoliste zielen Sie ab?</li></ul> **_Example:_** Kontensegment, das durch Konten mit Produkt Y mit einem Umsatz über 1 Million definiert ist |
| Vorlagen für Käufergruppenrollen | Diese Komponente bietet die Antwort auf: <ul><li>Auf welche Rollen zielen Sie ab?</li><li>Welcher Regelsatz wird verwendet, um zu bestimmen, wer welchen Käufergruppenrollen zugewiesen wird?</li></ul>  **_Example:_** Weisen Sie der Rolle Entscheidungsträger eine Person mit CMO-Titel zu |
| Käufergruppenphasen | (Optional) Diese Komponente bietet die Antwort auf die Frage: Wie stark ist die Käufergruppe auf Erfolg oder Misserfolg ausgerichtet? |

## Mitgliederzuweisung

Es gibt drei Möglichkeiten, wie Mitglieder einer Einkaufsgruppe zugewiesen oder aus dieser entfernt werden. In der folgenden Liste werden diese Methoden zum Hinzufügen und Entfernen in der Reihenfolge ihrer Priorität beschrieben. Die oberste Methode hat die höchste Priorität und eine niedrigere kann sie nicht überschreiben.

1. **_Manuelle Aktion_** - Eine manuelle Aktion zum Hinzufügen eines Mitglieds oder zum Entfernen eines Mitglieds, die von einem Verkaufsbenutzer für die Einkaufsgruppe ausgeführt wird
2. **_Journey-Aktion_** - Journey [Aktionsknoten für den Erwerb der Gruppenmitgliedschaft](../journeys/action-nodes.md#add-a-people-based-action) (_Der Einkaufsgruppe zuweisen_ oder _Aus der Einkaufsgruppe entfernen_)
3. **_Systemaufträge_** - Kauf von [- ](../buying-groups/buying-groups-create.md#buying-group-creation-jobs) Wartungsaufträgen.

Um sicherzustellen, dass die Mitgliederzuweisung in einer Einkaufsgruppe nicht falsch überschrieben wird, ist diese Liste in der Reihenfolge der Rangfolge, die im System befolgt wird, um eine genaue Mitgliederzuweisung sicherzustellen. Wenn ein Verkaufsbenutzer beispielsweise manuell ein Mitglied zur Einkaufsgruppe hinzufügt, möchte er nicht, dass ein Wartungsauftrag diese Hinzufügung ändert. Unter Verwendung der Rangfolge der Priorität werden die folgenden Szenarien erzwungen:

* Wenn ein(e) Benutzende(r) ein Mitglied manuell einer Einkaufsgruppe zuweist und anschließend ein Wartungsauftrag für die Einkaufsgruppe ausgeführt wird, bei dem dasselbe Mitglied aus der Einkaufsgruppe entfernt wird, **der Wartungsauftrag dieses** nicht entfernen und kann die manuelle Zuweisung nicht überschreiben.
* Wenn ein(e) Benutzende(r) ein Mitglied manuell einer Einkaufsgruppe zuweist und anschließend ein ausgelöster Journey-Knoten auftritt, der dasselbe Mitglied aus der Einkaufsgruppe entfernt, wird dieses Mitglied durch die Knotenaktion **nicht entfernt** und die manuelle Zuweisung kann nicht überschrieben werden.
* Wenn ein ausgelöster Journey-Aktionsknoten ein Mitglied zu einer Einkaufsgruppe hinzufügt und darauf ein Wartungsauftrag für eine Einkaufsgruppe folgt, der dasselbe Mitglied aus der Einkaufsgruppe entfernt, entfernt der Wartungsauftrag **dieses Mitglied nicht** und kann die Journey-Aktionszuweisung nicht überschreiben.

## Käufergruppen-Workflow

1. Erstellen Sie Käufergruppen.

   * Definieren Sie [Lösungsinteresse](./solution-interests.md) und [Rollenvorlage](./buying-groups-role-templates.md)
   * [Erstellen Sie die Käufergruppe](./buying-groups-create.md#create-buying-groups) und weisen Sie [Käufergruppenphasen](./buying-group-stages.md) zu.

1. Identifizieren Sie fehlende Personen anhand der Vollständigkeit.

   Analysieren Sie die Käufergruppe mithilfe von Filtern.

   **_:_**: Die Rolle des Entscheidungsträgers fehlt und der Vollständigkeitswert ist &lt; 50

1. Vervollständigen Sie die Definitionen der Käufergruppen.
<!--
   * Acquire missing people
   * Send to LinkedIn Destination
   * Enrich with Zoominfo -->

1. Fügen Sie Ihren Account-Journey Kauf-Gruppenaktionen hinzu.

## Anzeigen von Käufergruppen und Komponenten

Erweitern Sie in der linken Navigation **[!UICONTROL Konten]** und klicken Sie auf **[!UICONTROL Käufergruppen]**.

Die Seite _[!UICONTROL Käufergruppen]_ ist in Registerkarten unterteilt:

| Tab | Beschreibung |
| --- | ----------- |
| [!UICONTROL Übersicht] | Diese Registerkarte ist die Standardeinstellung und zeigt das [Käufergruppen-Dashboard](../dashboards/buying-groups-dashboard.md) an. |
| [!UICONTROL Durchsuchen] | Diese Registerkarte unterstützt die folgenden Aktivitäten: <ul><li>Liste der vorhandenen Käufergruppen anzeigen. </li><li>Suchen Sie nach dem Namen der Einkaufsgruppe. </li><li>Nach Lösungsinteresse filtern. </li><li>Details zur Käufergruppe aufschlüsseln. </li><li>Erstellen sie eine Käufergruppe. </li></ul> |
| [!UICONTROL Lösungsinteressen] | Diese Registerkarte unterstützt die folgenden Aktivitäten: <ul><li>Liste der vorhandenen Käufergruppen anzeigen. </li><li>Suchen Sie nach dem Namen der Einkaufsgruppe. </li><li>Auf Lösungsinteresseneigenschaften zugreifen und diese bearbeiten. </li><li>Lösungsinteresse erstellen. </li><li>Lösungsinteresse löschen. </li><li>Käufergruppenaufträge anzeigen und löschen. </li></ul> |
| [!UICONTROL Rollenvorlagen] | Diese Registerkarte unterstützt die folgenden Aktivitäten: <ul><li>Liste der vorhandenen Rollenvorlagen anzeigen. </li><li>Nach dem Namen der Rollenvorlage suchen. </li><li>Auf die Eigenschaften und Bedingungen von Rollenvorlagen zugreifen und diese bearbeiten. </li><li>Eine Rollenvorlage erstellen. </li><li>Eine Rollenvorlage löschen. </li></ul> |
| [!UICONTROL Stadien] | Diese Registerkarte unterstützt die folgenden Aktivitäten: <ul><li>Modell der vorhandenen Käufergruppenphasen anzeigen. </li><li>Auf den Modellentwurf der Käufergruppenphasen zugreifen und diesen bearbeiten. </li><li>Das Modell für Käufergruppenphasen erstellen. </li></ul> |

## Suchen nach und Filtern von Käufergruppen

Verwenden Sie die Registerkarte _[!UICONTROL Durchsuchen]_, um auf die Liste der Käufergruppen zuzugreifen. Sie können nach Name suchen und die Liste nach Lösungsinteressen filtern.

![Seite zum Durchsuchen der Käufergruppe](assets/buying-groups-browse.png){width="800" zoomable="yes"}

## Details zu Käufergruppen

Um auf die Details einer Käufergruppe zuzugreifen, klicken Sie auf der Registerkarte _[!UICONTROL Durchsuchen]_ auf den Namen der Käufergruppe. [Weitere Informationen](./buying-group-details.md)

![Details zur Käufergruppe](assets/buying-group-details.png){width="600" zoomable="yes"}

### Vollständigkeitswert der Käufergruppe

Mit dem Vollständigkeitswert wird bestimmt, ob die Käufergruppe vollständig ist, d. h., dass den Rollen die richtigen Mitglieder zugewiesen sind und sie in einer Konto-Journey verwendet werden kann. Dieser Wert ist ein Prozentsatz, der auf der Anzahl der Rollen innerhalb der Käufergruppe und der Anzahl der Rollen basiert, die mit mindestens einem Lead zugewiesen werden.

Wenn eine Käufergruppe beispielsweise vier Rollen umfasst und drei der vier Rollen mindestens einem Lead zugewiesen sind, ist die Käufergruppe zu 75 % vollständig.

Jedes Mal, wenn eine Käufergruppe erstellt oder aktualisiert wird, wird der Vollständigkeitswert für der Käufergruppe neu berechnet.

### Interaktionsbewertung der Käufergruppe

Die Interaktionsbewertung einer Käufergruppe ist eine Zahl, anhand der die Interaktion der Mitglieder einer Käufergruppe basierend auf den von ihnen durchgeführten Aktivitäten ermittelt wird.

* Die Berechnung der Interaktionsbewertung beginnt, sobald die Käufergruppe generiert wurde.
* Zur Berechnung der Bewertung wird jede eingehende Aktivität verwendet, die von den Mitgliedern der Käufergruppe in den letzten 30 Tagen ausgeführt wurde.
* Mit dem 30-Tage-Fenster und dem Ablaufen von Aktivitäten könnte die Bewertung sinken.
* Es gibt eine tägliche Frequenzlimitierung von 20 pro Aktivität. Wenn ein Mitglied einer Käufergruppe also dieselbe Aktivität mehr als 20 Mal am Tag ausführt, wird die Anzahl der Aktivitäten auf 20 begrenzt und nicht höher.
* Die angezeigte Bewertung ist gerundet. Beispielsweise wird eine Bewertung von 75,89999 als 76 angezeigt.

+++Für die Bewertung verwendete Aktivitäten

>[!BEGINSHADEBOX]

| Aktivitätsname | Beschreibung | Interaktionstyp | Maximale tägliche Frequenzlimitierung | Aktivitätsgewichtung |
| --- | --- | --- | --- | --- |
| [!UICONTROL Web-Seite besuchen] | Ein Mitglied besucht eine Webseite | Web | 20 | 40 |
| [!UICONTROL Formular ausfüllen] | Ein Mitglied füllt ein Formular auf einer Web-Seite aus und sendet es. | Web | 20 | 40 |
| [!UICONTROL Link klicken] | Ein Mitglied klickt auf einen Link auf einer Webseite | Web | 20 | 40 |
| [!UICONTROL E-Mail öffnen] | Ein Mitglied öffnet eine E-Mail | E-Mail | 20 | 30 |
| [!UICONTROL E-Mail klicken] | Ein Mitglied klickt auf einen Link in einer E-Mail | E-Mail | 20 | 30 |
| [!UICONTROL Verkaufs-E-Mail öffnen] | Ein Mitglied öffnet eine Verkaufs-E-Mail | E-Mail | 20 | 30 |
| [!UICONTROL Verkaufs-E-Mail klicken] | Ein Mitglied klickt auf einen Link in einer Verkaufs-E-Mail | E-Mail | 20 | 30 |
| [!UICONTROL Interessanter Moment] | Ein Mitglied hat einen interessanten Moment | Kuratiert | 20 | 60 |
| [!UICONTROL Tippen Sie auf Push-Benachrichtigung] | Ein Mitglied erhält eine Push-Benachrichtigung | Mobile | 20 | 30 |
| [!UICONTROL Mobile-App-Aktivität] | Ein Mitglied führt eine Aktivität in einer mobilen App aus | Mobile | 20 | 30 |
| [!UICONTROL Mobile-App-Sitzung] | Ein Mitglied ist in einer App-Sitzung aktiv | Mobile | 20 | 30 |
| [!UICONTROL Facebook-Lead-Anzeigen-Formular ausfüllen] | Ein Mitglied füllt ein Lead-Anzeigen-Formular auf einer Facebook-Seite aus und sendet es. | Social | 20 | 30 |
| [!UICONTROL Klicken Sie auf RTP Call to action] | Ein Mitglied klickt auf eine personalisierte call to action | Web | 20 | 60 |
| [!UICONTROL In-App-Nachricht anzeigen] | Ein Mitglied sieht sich eine In-App-Nachricht an | Mobile | 20 | 30 |
| [!UICONTROL Tippen Sie auf In-App-Nachricht] | Ein Mitglied tippt auf eine In-App-Nachricht | Mobile | 20 | 30 |
| [!UICONTROL SMS abonnieren] | Abonnierte SMS-Nachrichten | SMS | 20 | 90 |
| [!UICONTROL Antwort auf Verkaufs-E-Mail] | Ein Mitglied antwortet auf eine Verkaufs-E-Mail | E-Mail | 20 | 30 |
| [!UICONTROL Interagiert mit einem Dialog] | Ein Mitglied greift auf ein Dynamic Chat-Dialogfeld zu | Chat | 20 | 90 |
| [!UICONTROL Interagiert mit einem Dokument im Dialogfeld] | Ein Mitglied interagiert in einem Dynamic Chat-Dialogfeld mit einem Dokument | Chat | 20 | 90 |
| [!UICONTROL Geplante Besprechung im Dialogfeld] | Ein Mitglied plant einen Termin in einem Dynamic Chat-Dialogfeld | Chat | 20 | 90 |
| [!UICONTROL Dialogziel erreicht] | Ein Mitglied erreicht ein Ziel in einem Dynamic Chat-Dialogfeld |  | 20 | 90 |
| [!UICONTROL Beantwortet eine Umfrage im Webinar] | Teilnehmer antwortet auf eine Umfrage in einem Webinar-Ereignis | Chat | 20 | 90 |
| [!UICONTROL Call to action im Webinar angeklickt] | Ein Teilnehmer klickt auf einen call-to-action-Link in einem Webinar-Ereignis | Anruf | 20 | 30 |
| [!UICONTROL Asset-Downloads im Webinar] | Ein Mitglied lädt eine Datei/ein Asset in einem Webinar-Ereignis herunter | Ereignis | 20 | 60 |
| [!UICONTROL Stellt Fragen im Webinar] | Ein Mitglied stellt in einer Webinar-Veranstaltung Fragen. | Ereignis | 20 | 60 |
| [!UICONTROL Hat an der Veranstaltung teilgenommen] | Ein Mitglied hat an einer Veranstaltung teilgenommen | Ereignis | 20 | 60 |
| [!UICONTROL Interagiert mit einem Agenten im Dialog] | Ein Mitglied tritt mit einem Agenten in einem Dynamic Chat-Dialogfeld in Kontakt | Chat | 20 | 90 |
| [!UICONTROL Link im Chat im Dialogfeld angeklickt] | Ein Mitglied klickt in einem Dynamic Chat-Dialogfeld auf einen Link | Chat | 20 | 90 |
| [!UICONTROL Interagiert mit einem Gesprächsfluss] | Ein Mitglied tritt mit einem Dynamic Chat-Gesprächsfluss in Kontakt | Chat | 20 | 90 |
| [!UICONTROL Geplante Besprechung im Gesprächsfluss] | Ein Mitglied plant einen Termin in einem Dynamic Chat-Gesprächsfluss | Chat | 20 | 90 |
| [!UICONTROL Ziel des Gesprächsflusses erreicht] | Ein Mitglied erreicht ein Ziel in einem Dynamic Chat-Gesprächsfluss | Chat | 20 | 90 |
| [!UICONTROL Interagiert mit einem Dokument im Konversationsfluss] | Ein Mitglied interagiert mit einem Dokument in einem Dynamic Chat-Gesprächsfluss | Chat | 20 | 90 |
| [!UICONTROL Interagiert mit einem Agenten im Gesprächsfluss] | Ein Mitglied interagiert mit einem Agenten in einem Dynamic Chat-Gesprächsfluss | Chat | 20 | 90 |
| [!UICONTROL Link im Chat im Gesprächsfluss angeklickt] | Ein Mitglied klickt auf einen Link in einem Dynamic Chat-Gesprächsfluss | Chat | 20 | 90 |
| [!UICONTROL Link in SMS V2 klicken] | Ein Mitglied klickt auf einen Link in einer SMS-Nachricht | SMS | 20 | 90 |


>[!ENDSHADEBOX]

>[!NOTE]
>
>Aktivitäten für die Interaktionsbewertung werden im Marketo Engage-[Aktivitätsprotokoll für eine Person](https://experienceleague.adobe.com/de/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/managing-people-in-smart-lists/locate-the-activity-log-for-a-person){target="_blank"} dokumentiert.

+++

#### Gewichtung

Benutzerinnen und Benutzer können jeder Rolle in der Rollenvorlage eine _Gewichtung_ zuweisen, um einer Rolle unterschiedliche Gewichtungen für die Berechnung der Interaktionsbewertung zu geben.

![Eine Gewichtung für jede Rolle in der Rollenvorlage festlegen](./assets/roles-templates-weighting.png){width="700" zoomable="yes"}

Jede Gewichtungsstufe wird in einen Wert umgewandelt, der für die Berechnung der Interaktionsbewertung verwendet wird:

* [!UICONTROL Trivial] = 20
* [!UICONTROL Geringfügig] = 40
* [!UICONTROL Normal] = 60
* [!UICONTROL Wichtig] = 80
* [!UICONTROL Entscheidend] = 100

Eine Rollenvorlage mit drei Rollen, die als _[!UICONTROL Entscheidend]_, _[!UICONTROL Wichtig]_ und _[!UICONTROL Normal]_ gewichtet sind und in die folgenden gewichteten Prozentsätze konvertiert werden:

| Rolle | Gewichtung | Systemwert | Wertberechnung | Prozentsatz |
|-------------- |--------- |------------- |------------------ |---------- |
|               |          |              |                   |           |
| Entscheidungsträger | Entscheidend | 100 | 100/240 | 41,67 % |
| Influencer | Wichtig | 80 | 80/240 | 33,33 % |
| Praktizierende | Normal | 60 | 60/240 | 25 % |
|               | Gesamt | 240 |                   |           |

#### Beispiel einer Berechnung

Das folgende Beispiel veranschaulicht die Berechnung der Interaktionsbewertung mithilfe des beschriebenen Prozentsatzes der Rollengewichtung, der Anzahl der eingehenden Aktivitäten für jedes Mitglied der Käufergruppe und einer täglichen Begrenzung auf eine Anzahl von 20 für jedes Ereignis (falls es mehrmals aufgetreten ist).

| Rolle | Mitglied | Typ der Aktivität | Zählung gestern | Zählung heute | Berechnung | Gesamtbewertung |
|-------------- |--------- |-------------|-----------------|-------------|------|-----------|
|               |          |             |                 |             |      |           |
| Entscheidungsträger | Adam | Besuchte Website | 37 | 15 | 20 + 15 | 35 |
|               |          | Angeklickte E-Mail | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Mark | Besuchte Website | 5 | 3 | 5 + 3 | 8 |
|               |          | Angeklickte E-Mail | 1 | 1 | 1 + 1 | 2 |
|               |          | Heruntergeladene Veröffentlichung | 3 | 2 | 3 + 2 | 5 |
| **Gesamtpunktzahl der Entscheidungsträger** |         |             |                 |             |      | **52** |
|               |          |             |                 |             |      |           |
| Influencer | John | Besuchte Website | 19 | 9 | 19 + 9 | 28 |
| **Gesamtpunktzahl der Influencer** |         |             |                 |             |      | **28** |
|               |          |             |                 |             |      |           |
| Praktizierende | Bob | Angeklickte E-Mail | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Paul | Angeklickte E-Mail | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Calvin | Angeklickte E-Mail | 1 | 1 | 1 + 1 | 2 |
|               |          | Besuchte Website | 1 | 7 | 1 + 7 | 8 |
|               |          | Heruntergeladene Veröffentlichung | 1 | 2 | 1 + 2 | 3 |
| **Gesamtpunktzahl der Praktizierenden** |         |             |                 |             |      | **17** |

Die endgültige Interaktionsbewertung wird durch Anwenden der Gewichtung für jeden Rollenwert berechnet:

| Rolle | Gesamtbewertung der Rolle | Rollengewichtung % | Bewertung x Gewichtung % |
|-------------- |---------------- |------------- |---------------- |
| Entscheidungsträger | 52 | 41,67 % | 21,67 |
| Influencer | 28 | 33,33 % | 9,33 |
| Praktizierende | 17 | 25 % | 4,25 |
| **Endgültige Interaktionsbewertung** |                |             | **35,25** |

## Übersichtsvideo

>[!VIDEO](https://video.tv.adobe.com/v/3452948/?learn=on&captions=ger)
