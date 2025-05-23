---
title: Käufergruppen
description: Erfahren Sie, wie Käufergruppen in Journey Optimizer B2B Edition die Effektivität des Marketings durch das Identifizieren und Targeting von Mitgliedern für Ihre Kontolisten steigern können.
feature: Buying Groups
role: User
exl-id: ddcd7b62-6a76-4f5e-b6d3-a20944ca8332
source-git-commit: d1130841ed3c560208bc93c53a54169f9b0b94aa
workflow-type: ht
source-wordcount: '1778'
ht-degree: 100%

---


# Käufergruppen

Bei B2B-Vertriebs- und Marketing-Aktivitäten sind Konten wichtig für jede Strategie. Jedem Konto ist eine Gruppe von Personen zugeordnet, und diese Personen können Mitarbeitende des Kontos oder Auftragnehmer sein, die mit dem Konto arbeiten. Konten sind hierarchisch, und verschiedene Produkte können auf verschiedenen Ebenen in der Hierarchie verkauft werden. Adobe Experience Platform kann beispielsweise auf Unternehmensebene an einn Konto der obersten Ebene verkauft werden. Adobe Photoshop wird möglicherweise an ein Konto verkauft, das einen Geschäftsbereich oder eine Abteilung innerhalb eines Unternehmens repräsentiert, z. B. eine Design-Abteilung innerhalb eines größeren Unternehmens.

![Diagramm zu Kontorollen](assets/account-roles-diagram.png){width="800"}

Innerhalb des Kontos könnte es eine Untergruppe von Personen geben, die die _Käufergruppe_ umfassen. Dies sind die Personen, die letztendlich die Kaufentscheidung treffen. Sie benötigen daher besondere Aufmerksamkeit von der Marketing-Fachkraft und ihnen müssen möglicherweise andere Informationen bereitgestellt werden als anderen Personen, die dem Konto zugeordnet sind. Käufergruppen können unterschiedliche Personengruppen für verschiedene Produktlinien oder Angebote umfassen. Beispielsweise ist für ein Cybersicherheitsprodukt in der Regel die Kaufgenehmigung durch einen Chief Information Officer oder Chief Security Officer und einen Vertreter der Rechtsabteilung erforderlich, aber ein Produkt zur Fehlersuche kann in der Regel einen VP of Engineering und einen IT Director als Mitglieder der Käufergruppe haben.

![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Videoüberblick ansehen](#overview-video)

## Wichtige Komponenten

Sie können die Effektivität des Marketings steigern, indem Sie Käufergruppen in Journey Optimizer B2B Edition einrichten, die fehlende Mitglieder für Ihre Zielkontenlisten identifizieren. Diese Gruppen basieren auf den Lösungen, für deren Vertrieb Ihre Vertriebs-Teams verantwortlich sind. Bevor Sie und Ihr Marketing-Team mit der Erstellung Ihrer Käufergruppen beginnen, stellen Sie sicher, dass Sie die wichtigen Komponenten definiert haben. Diese Komponenten sind für die Erreichung Ihrer Geschäftsziele von entscheidender Bedeutung.

| Komponente | Zweck |
| --------- | ------- |
| Lösungsinteresse | Diese Komponente bietet die Antwort auf: <ul><li>Was verkaufen Sie als Marketing-Organisation?</li><li>Welches Produkt oder welche Produktkollektion möchten Sie verkaufen?</li></ul>  **_Beispiel:_** Crossselling des neuen Produktes X an Bestandskundschaft |
| Kontozielgruppe | Diese Komponente bietet die Antwort auf: <ul><li>An wen verkaufen Sie?</li><li>Auf welche Kontoliste zielen Sie ab?</li></ul> **_Beispiel:_** Kontosegment, das durch Konten mit Produkt Y und einem Umsatz von mehr als 1 Million definiert wird. |
| Vorlagen für Käufergruppenrollen | Diese Komponente bietet die Antwort auf: <ul><li>Auf welche Rollen zielen Sie ab?</li><li>Welcher Regelsatz wird verwendet, um zu bestimmen, wer welchen Käufergruppenrollen zugewiesen wird?</li></ul>  **_Beispiel:_** Weisen Sie eine Person mit CMO-Titel der Rolle „Entscheidungsträger“ zu. |
| Käufergruppenphasen | (Optional) Diese Komponente bietet die Antwort auf die Frage: Wie stark ist die Käufergruppe auf Erfolg oder Misserfolg ausgerichtet? |

## Käufergruppen-Workflow

1. Erstellen Sie Käufergruppen.

   * Definieren Sie [Lösungsinteresse](./solution-interests.md) und [Rollenvorlage](./buying-groups-role-templates.md)
   * [Erstellen Sie die Käufergruppe](./buying-groups-create.md#create-buying-groups) und weisen Sie [Käufergruppenphasen](./buying-group-stages.md) zu.

1. Identifizieren Sie fehlende Personen.

   Analysieren Sie die Käufergruppe mithilfe von Filtern.

   **_Beispiel_** Die Rolle „Entscheidungsträger“ fehlt und der Vollständigkeitswert ist &lt; 50

1. Vervollständigen Sie die Definitionen der Käufergruppen.
<!--
   * Acquire missing people
   * Send to LinkedIn Destination
   * Enrich with Zoominfo -->

1. Verwenden Sie die Käufergruppe Ihrer Konto-Journeys.

## Anzeigen von Käufergruppen und Komponenten

Erweitern Sie in der linken Navigation **[!UICONTROL Konten]** und klicken Sie auf **[!UICONTROL Käufergruppen]**.

Die Seite _[!UICONTROL Käufergruppen]_ ist in Registerkarten unterteilt:

| Tab | Beschreibung |
| --- | ----------- |
| [!UICONTROL Übersicht] | Diese Registerkarte ist die Standardeinstellung und zeigt das [Käufergruppen-Dashboard](../dashboards/buying-groups-dashboard.md) an. |
| [!UICONTROL Durchsuchen] | Diese Registerkarte unterstützt die folgenden Aktivitäten: <ul><li>Liste der vorhandenen Käufergruppen anzeigen. </li><li>Nach dem Namen der Käufergruppe suchen. </li><li>Nach Lösungsinteresse filtern. </li><li>Details zur Käufergruppe aufschlüsseln. </li><li>Erstellen sie eine Käufergruppe. </li></ul> |
| [!UICONTROL Lösungsinteressen] | Diese Registerkarte unterstützt die folgenden Aktivitäten: <ul><li>Liste der vorhandenen Käufergruppen anzeigen. </li><li>Nach dem Namen der Käufergruppe suchen. </li><li>Auf Lösungsinteresseneigenschaften zugreifen und diese bearbeiten. </li><li>Lösungsinteresse erstellen. </li><li>Lösungsinteresse löschen. </li><li>Käufergruppenaufträge anzeigen und löschen. </li></ul> |
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

| Aktivitätsname | Beschreibung | Interaktionstyp | Maximale tägliche Frequenzlimitierung | Aktivitätsgewichtung |
| --- | --- | --- | --- | --- |
| Für Ereignis registrieren | Registriert sich für ein Ereignis, das mit einer Kampagne verbunden ist | Ereignis | 20 | 60 |
| An Ereignis teilnehmen | Nimmt an einem Kampagnenereignis teil | Ereignis | 20 | 90 |
| E-Mail öffnen | Öffnet eine E-Mail | E-Mail | 20 | 30 |
| Auf E-Mail klicken | Klickt auf einen Link in einer E-Mail | E-Mail | 20 | 30 |
| Verkaufs-E-Mail öffnen | Öffnet eine Verkaufs-E-Mail | E-Mail | 20 | 30 |
| Auf Verkaufs-E-Mail klicken | Klickt auf einen Link in einer Verkaufs-E-Mail | E-Mail | 20 | 30 |
| Interessanter Moment | Erlebt einen interessanten Moment | Kuratiert | 20 | 60 |
| Push-Benachrichtigung antippen | Empfängt eine Push-Benachrichtigung | Mobile | 20 | 30 |
| Aktivität einer Mobile App | Führt eine Aktivität in einer Mobile App durch | Mobile | 20 | 30 |
| Sitzung einer Mobile App | Ist in einer Mobile-App-Sitzung aktiv | Mobile | 20 | 30 |
| Facebook-Lead-Ads-Formular ausfüllen | Füllt ein Formular für Lead-Anzeigen auf einer Facebook-Seite aus und sendet es ab. | Social | 20 | 30 |
| RTP-Handlungsaufforderung anklicken | Klickt auf eine personalisierte Handlungsaufforderung | Web | 20 | 60 |
| In-App-Nachricht anzeigen | Zeigt eine In-App-Nachricht an | Mobile | 20 | 30 |
| In-App-Nachricht antippen | Tippt auf eine In-App-Nachricht  | Mobile | 20 | 30 |
| SMS abonnieren | Abonniert SMS-Nachrichten | SMS | 20 | 90 |
| Auf Verkaufs-E-Mail antworten | Antwortet auf eine Verkaufs-E-Mail | E-Mail | 20 | 30 |
| Hatte eine Interaktion mit einem Dialog | Interagiert mit einem Dynamic Chat-Dialog | Chat | 20 | 90 |
| Hatte eine Interaktion mit Dokument in Dialog | Interagiert mit einem Dokument in einem Dynamic Chat-Dialog | Chat | 20 | 90 |
| Arrangierte ein Meeting in Dialog | Plant einen Termin in einem Dynamic Chat-Dialog | Chat | 20 | 90 |
| Dialogziel erreicht | Erreicht ein Ziel in einem Dynamic Chat-Dialog |  | 20 | 90 |
| Antwortete auf eine Umfrage in Webinar | Antwortet auf eine Umfrage in einem Webinar-Ereignis | Chat | 20 | 90 |
| Handlungsaufforderung im Webinar angeklickt | Klickt auf einen Link mit Handlungsaufruf in einem Webinar-Ereignis | Anruf | 20 | 30 |
| Asset-Downloads im Webinar | Lädt in einem Webinar-Ereignis eine Datei/ein Asset herunter | Ereignis | 20 | 60 |
| Stellt Fragen im Webinar | Stellt Fragen in einem Webinar-Ereignis | Ereignis | 20 | 60 |
| Nahm am Event teil | Nahm am Event teil | Ereignis | 20 | 60 |
| Hatte eine Interaktion mit einem Support-Mitarbeitenden per Dialog | Interagiert mit einem Agenten in einem Dynamic Chat-Dialog | Chat | 20 | 90 |
| Klickte auf Link im Chat in Dialog | Klickt auf einen Link in einem Dynamic Chat-Dialog | Chat | 20 | 90 |
| Hatte eine Interaktion mit einem Konversationsschema | Interagiert mit einem Dynamic Chat-Konversationsfluss | Chat | 20 | 90 |
| Arrangierte ein Meeting in Konversationsschema | Plant einen Termin in einem Dynamic Chat-Konversationsfluss | Chat | 20 | 90 |
| Ziel des Konversationsschemas erreicht | Erreicht ein Ziel in einem Dynamic Chat-Konversationsfluss | Chat | 20 | 90 |
| Hatte eine Interaktion mit Dokument in Konversationsschema | Interagiert mit einem Dokument in einem Dynamic Chat-Konversationsfluss | Chat | 20 | 90 |
| Hatte eine Interaktion mit Mitarbeitenden in Konversationsschema | Interagiert mit einem Agenten in einem Dynamic Chat-Konversationsfluss | Chat | 20 | 90 |
| Klickte auf Link im Chat in Konversationsschema | Klickt auf einen Link in einem Dynamic Chat-Konversationsfluss | Chat | 20 | 90 |
| Link in SMS anklicken V2 | Klickt auf einen Link in einer SMS-Nachricht | SMS | 20 | 90 |

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
