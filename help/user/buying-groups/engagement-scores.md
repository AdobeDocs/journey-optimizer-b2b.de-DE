---
title: Interaktionswerte für Einkaufsgruppen
description: Verfolgen Sie die Werte für Einkaufsgruppen- und Personeninteraktionen mit gewichteten Aktivitäten und rollenbasierten Berechnungen in Journey Optimizer B2B edition.
feature: Buying Groups, Engagement
role: User
exl-id: 424d9598-92dd-42de-8447-3c7cebc71a73
source-git-commit: 9ed2d2a36dbdaf39c107a18632d951003c86197b
workflow-type: tm+mt
source-wordcount: '1251'
ht-degree: 29%

---

# Interaktionsbewertungen {#engagement-scores}

>[!CONTEXTUALHELP]
>id="ajo-b2b_buying_group_engagement_score"
>title="Interaktionsbewertung"
>abstract="Interaktionsbewertungen bestimmen den Grad der Interaktion für Käufergruppenmitglieder."

Ein Interaktionswert ist eine Zahl, die den Grad der Interaktion der Mitglieder einer Einkaufsgruppe angibt. Diese Bewertungen basieren auf den Aktivitäten der Mitglieder der Einkaufsgruppe, gewichteten Aktionen und gewichteten Rollen. Die resultierenden Bewertungen werden innerhalb eines Mandanten (einer Instanz) normalisiert, um einen konsistenten Vergleich zu ermöglichen und umsetzbare Einblicke zu ermöglichen. Die Berechnung des Punktwerts beginnt, sobald Sie die Einkaufsgruppe erstellen. Das Journey Optimizer B2B edition-Daten-Hub-System berechnet die Bewertungen täglich und lädt sie mithilfe des Aufnahme-Service in das MySQL-System des Multi-Level Marketing (MLM) hoch.

Es gibt zwei Arten von Interaktionswerten:

* **Score für Gruppeninteraktionen** - Der Score für Gruppeninteraktionen in Käufen ist ein normalisierter Score zwischen 0 und 100 und basiert auf dem auf Personenebene berechneten Interaktionswert.

  Der Interaktionswert der kaufenden Gruppe wird auf der Seite [Kaufgruppendetails](./buying-group-details.md) angezeigt. Sie können auch die aktivsten Einkaufsgruppen im intelligenten Dashboard anzeigen.

  ![Die aktivsten Einkaufsgruppen](./assets/person-engagement-score-attribute-filtering.png){width="700" zoomable="yes"}

* **Interaktionswert für eine Person** - Der Interaktionswert für eine Person basiert auf den Aktivitäten eines einzelnen kaufenden Gruppenmitglieds.

  Der Interaktionswert der Person für jedes kaufende Gruppenmitglied wird auf der Seite mit den Details zur kaufenden Gruppe [_[!UICONTROL Registerkarte &#x200B;]_&#x200B;Mitglieder) ](./buying-group-details.md#buying-group-members). Diese Bewertungen werden auch auf Seiten und in Dashboards angezeigt, die hochmotivierte Mitglieder und sich überschneidende Kontaktinformationen enthalten.

  ![Die engagiertesten Mitglieder der Einkaufsgruppe](./assets/top-engaged-buying-group-members.png){width="550" zoomable="yes"}

>[!BEGINSHADEBOX]

Der Personeninteraktionswert ist ein Attribut, das zum Filtern in [Rollenvorlagen](./buying-groups-role-templates.md#add-the-template-roles) und [Journey-Knoten, die nach Personen aufgeteilt werden können, ](../journeys/split-merge-paths-nodes.md#people-path-conditions).

![Zugriff auf die konfigurierten Ereignisdefinitionen](./assets/most-engaged-buying-groups.png){width="550" zoomable="yes"}

>[!ENDSHADEBOX]

Zur Berechnung der Scores wird jede Interaktionsgewichtete Aktivität verwendet, die von den Mitgliedern der Einkaufsgruppe in den letzten 30 Tagen durchgeführt wurde. Im 30-Tage-Fenster laufen die Aktivitätsereignisse ab und die Scores können nach unten verschoben werden (Score-Zerfall). Die angezeigten Werte werden gerundet (z. B. wird ein Wert von 75,89999 als 76 angezeigt).

## Für die Interaktionsbewertung verwendete Aktivitäten

Buying Group Scoring ist nicht _ausgelöste_. Es handelt sich um einen täglichen Prozess, der die Aktivität aller Mitglieder der Einkaufsgruppe auswertet und die Punktzahl neu berechnet. Aktivitäten verwenden _Gewichtungen_ um die Bewertung der Einkaufsgruppe gemäß dem aktiven Gewichtungsmodell zu informieren, das bestimmt, wie jede Aktivität gewichtet wird.

Es gibt eine tägliche Frequenzbegrenzung von 20 pro Aktivität. Wenn ein Mitglied einer Einkaufsgruppe dieselbe Aktivität mehr als 20 Mal an einem Tag ausführt, wird die Anzahl für die Aktivität auf 20 begrenzt.

| Aktivitätsname | Beschreibung | Interaktionstyp | Maximale tägliche Frequenzlimitierung | Standardmäßige Aktivitätsgewichtung des Modells |
|---------------|-------------|-----------------|---------------------------|-------------------------------|
| An Ereignis teilnehmen | Ein Mitglied nimmt an einem Event teil | Ereignis | 20 | 60 |
| E-Mail angeklickt | Ein Mitglied klickt auf einen Link in einer E-Mail | E-Mail | 20 | 30 |
| E-Mail geöffnet | Ein Mitglied öffnet eine E-Mail | E-Mail | 20 | 30 |
| Formular ausgefüllt | Ein Mitglied füllt ein Formular auf einer Web-Seite aus und sendet es ab | Web | 20 | 40 |
| Interessanter Moment | Ein Mitglied hat einen interessanten Moment | Kuratiert | 20 | 60 |
| Link-Klicks | Ein Mitglied klickt auf einen Link auf einer Web-Seite | Web | 20 | 40 |
| Seitenansichten | Ein Mitglied zeigt eine Web-Seite an | Web | 20 | 40 |
| Für Ereignis registrieren | Ein für ein Ereignis registriertes Mitglied | Ereignis | 20 | 60 |

<!-- old list

| Activity name | Description | Engagement type | Max daily frequency count | Activity weight |
| --- | --- | --- | --- | --- |
| [!UICONTROL Visit Webpage]| A member visits a web page | Web | 20 | 40 |
| [!UICONTROL Fill Out Form]| A member fills and submits a form on a web page | Web | 20 | 40 |
| [!UICONTROL Click Link] | A member clicks a link on a web page | Web | 20 | 40 |
| [!UICONTROL Open Email] | A member opens an email | Email | 20 | 30 |
| [!UICONTROL Click Email] | A member clicks a link in an email | Email | 20 | 30 |
| [!UICONTROL Open Sales Email] | A member opens a sales email | Email | 20 | 30 |
| [!UICONTROL Click Sales Email] | A member clicks a link in a sales email | Email | 20 | 30 |
| [!UICONTROL Interesting Moment] | A member has an interesting moment | Curated | 20 | 60 |
| [!UICONTROL Tap Push Notification] | A member receives a push notification | Mobile | 20 | 30 |
| [!UICONTROL Mobile App Activity] | A member performs an activity on a mobile app | Mobile | 20 | 30 |
| [!UICONTROL Mobile App Session] | A member is active on a mobile app session | Mobile | 20 | 30 |
| [!UICONTROL Fill Out Facebook Lead Ads Form] | A member fills and submits a Lead Ads form on a Facebook page | Social | 20 | 30 |
| [!UICONTROL Click RTP Call to Action] | A member clicks a personalized call to action | Web | 20 | 60 |
| [!UICONTROL View In-App Message] | A member views an in-app message | Mobile | 20 | 30 |
| [!UICONTROL Tap In-App Message] | A member taps an in-app message | Mobile | 20 | 30 |
| [!UICONTROL Subscribe SMS] | A member subscribes to SMS communications | SMS | 20 | 90 |
| [!UICONTROL Reply to Sales Email] | A member replies to a sales email | Email | 20 | 30 |
| [!UICONTROL Engaged with a Dialogue] | A member engages with a Dynamic Chat dialogue | Chat | 20 | 90 |
| [!UICONTROL Interacted with Document in Dialogue] | A member interacts with a document in a Dynamic Chat dialogue | Chat | 20 | 90 |
| [!UICONTROL Scheduled Meeting in Dialogue] | A member schedules an appointment in a Dynamic Chat dialogue | Chat | 20 | 90 |
| [!UICONTROL Reached Dialogue Goal] | A member reaches a goal in a Dynamic Chat dialogue |  |20 | 90 |
| [!UICONTROL Responded to a poll in webinar] | A member responds to a poll in a webinar event | Chat | 20 | 90 |
| [!UICONTROL Call to action clicked in webinar] | A member clicks a call-to-action link in a webinar event | Call | 20 | 30 |
| [!UICONTROL Asset downloads in webinar] | A member downloads a file/asset in a webinar event | Event | 20 | 60 |
| [!UICONTROL Asks questions in webinar] | A member asks questions in a webinar event | Event | 20 | 60 |
| [!UICONTROL Has attended event] | A member attended an event | Event | 20 | 60 |
| [!UICONTROL Engaged with an Agent in Dialogue] | A member engages with an agent in a Dynamic Chat dialogue | Chat | 20 | 90 |
| [!UICONTROL Clicked Link in Chat in Dialogue] | A member clicks a link in a Dynamic Chat dialogue | Chat | 20 | 90 |
| [!UICONTROL Engaged with a Conversational Flow] | A member engages with a Dynamic Chat conversational flow | Chat | 20 | 90 |
| [!UICONTROL Scheduled Meeting in Conversational Flow] | A member schedules an appointment in a Dynamic Chat conversational flow | Chat | 20 | 90 |
| [!UICONTROL Reached Conversational Flow Goal] | A member reaches a goal in a Dynamic Chat conversational flow | Chat | 20 | 90 |
| [!UICONTROL Interacted with Document in Conversational Flow] | A member interacts with a document in a Dynamic Chat conversational flow | Chat | 20 | 90 |
| [!UICONTROL Engaged with an Agent in Conversational Flow] | A member engages with an Agent in a Dynamic Chat conversational flow | Chat | 20 | 90 |
| [!UICONTROL Clicked Link in Chat in Conversational Flow] | A member clicks a link in a Dynamic Chat conversational flow | Chat | 20 | 90 |
| [!UICONTROL Click Link in SMS V2] | A member clicks a link in an SMS message | SMS | 20 | 90 | -->

>[!NOTE]
>
>Aktivitäten mit dem Interaktionswert werden im Aktivitätsprotokoll von Marketo Engage für eine Person aufgezeichnet. Sie können auf dieses Protokoll in der verbundenen Marketo Engage-Instanz zugreifen. Weitere Informationen finden Sie unter [Suchen des Aktivitätsprotokolls für eine Person](https://experienceleague.adobe.com/de/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/managing-people-in-smart-lists/locate-the-activity-log-for-a-person){target="_blank"} in der Dokumentation zu Marketo Engage.

## Rollengewichtung der Vorlage {#engagement-score-weighting}

>[!CONTEXTUALHELP]
>id="ajo-b2b_buying_group_engagement_score_weighting"
>title="Rollengewichtung der Interaktionsbewertung"
>abstract="Verwenden Sie eine Rollengewichtung, um die Berechnung der Interaktionsbewertung anzupassen."

Benutzerinnen und Benutzer können jeder _in der_ Rollenvorlage“ eine [Gewichtung](./buying-groups-role-templates.md) zuweisen, um einer Rolle unterschiedliche Gewichtungen zuzuweisen.

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

## Score-Berechnungsbeispiel

Das folgende Beispiel veranschaulicht die Berechnung des Interaktionswerts. Es verwendet den angegebenen Rollengewichtungsprozentsatz, die Anzahl der eingehenden Aktivitäten für jedes kaufende Gruppenmitglied und eine tägliche Obergrenze von 20 für jedes Ereignisereignis.

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

## Bewertungslogik

Zusätzlich zu der im Berechnungsbeispiel beschriebenen Berechnungslogik gibt es eine erheblich komplexe Normalisierung der Bewertungen, die im System erfolgt, und zwar für alle Personen, Einkaufsgruppen und Konten in Ihrer Instanz. Ein Engagement-Score für eine Einkaufsgruppe weist eine Abhängigkeit von den Interaktionswerten der Person auf, gemäß der folgenden geordneten Logik:

### Logik zur Berechnung des Punktwerts für die Personeninteraktion

1. Identifizieren Sie alle _Interaktionsgewichteten_ Aktivitätstypen mit zugehörigem Gewicht und täglichem Kontingent, z. B. Website-Besuche, E-Mail-Klicks und Webinar-Teilnahme.

1. Identifizieren Sie alle _(Interaktionsgewichtete)_, die innerhalb des Lookback-Fensters der Aktivität ausgeführt werden, das derzeit auf 30 Tage hartcodiert ist.

1. Normalisieren Sie die Gewichtungen der Aktivitätstypen für alle in _1 identifizierten_ Interaktionsgewichtungen) und ignorieren Sie diejenigen, die nicht innerhalb des Lookback-Fensters aufgetreten sind.

   Dieser Schritt nutzt _Min-Max-Normalisierung_ und reduziert erheblich die künstliche Verwässerung der Aktivitätstypgewichtung für einen Mandanten, der die meisten von ihnen nicht nutzt.

1. Wenden Sie die tägliche Kontingentfilterung pro Person und Aktivitätstyp an.

   Dieser Schritt minimiert das Auftreten sehr großer Ausreißer, indem er verhindert, dass Aktivitäten mit niedrigerem Wert/hohem Volumen die Scores verzerren.

1. Berechnen Sie den unformatierten Engagement-Score einer Person, indem Sie die tägliche Aktivität pro Aktivitätstyp addieren, sie mit der zugehörigen Gewichtung multiplizieren und dann die Ergebnisse für alle Tage des Lookback-Fensters addieren.

1. Verwenden Sie eine _Leistungstransformation_ (Quadratwurzel) Transformation, um die Varianz zu stabilisieren, indem Sie mögliche Ausreißer reduzieren.

   Diese Transformationen helfen, Verzerrungen zu reduzieren und Muster in den Daten linearer zu gestalten.

1. Wenden Sie eine zusätzliche _Skalierte Normalisierungs_ Transformation an, um sicherzustellen, dass die Bewertungen den gesamten Bereich von 0 bis 100 nutzen.

### Logik zur Berechnung des Bewertungswerts der Einkaufsgruppeninteraktion

1. Wenden Sie auf jedes Mitglied der Einkaufsgruppe eine normalisierte Gewichtung nach Rolle an, entsprechend der in der Rollenvorlage konfigurierten Gewichtung.

1. Normalisieren Sie die Gewichtung der Einkaufsgruppenrolle für jede Einkaufsgruppe.

   Durch diese Normalisierung wird eine unnötige Verwässerung des Rollengewichts vermieden, wenn eine Einkaufsgruppe nicht alle Rollen verwendet.

1. Aggregieren Sie alle Werte für die Interaktion mit Personen für Käufergruppen-Mitglieder, indem Sie die Interaktionswerte der Person mit der normalisierten Rollengewichtung der Person multiplizieren und addieren Sie sie.

1. Wenden Sie eine _Power Transformation_-Transformation (Quadratwurzel) an, um die Varianz zu stabilisieren, indem Sie mögliche Ausreißer reduzieren, insbesondere für sehr große Einkaufsgruppen.

1. Wenden Sie eine zusätzliche _Skalierte Normalisierungs_ Transformation an, um sicherzustellen, dass die Bewertungen den gesamten Bereich von 0 bis 100 nutzen.
