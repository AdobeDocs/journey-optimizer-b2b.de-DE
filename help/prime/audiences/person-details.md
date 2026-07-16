---
title: Personendetails
description: Zeigen Sie die KI-generierte Persona, die Interaktion und die Absichtszusammenfassung einer Person, den Aktivitätsverlauf, die Profilattribute und die Unternehmensdetails einer Person an und stellen Sie Fragen an den KI-Assistenten zum Datensatz in Journey Optimizer B2B Prime.
badgeBeta: label="Beta" type="informative" tooltip="Diese Funktion befindet sich derzeit in einer eingeschränkten Beta-Version"
autotag-review: '2026-07-15T18:38:26.025Z'
TQID: 'https://experienceleague.adobe.com/pPq1KsFRDCjVUB5yYXeEXa1HFrIzF7etLI-vLHe-mE4'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
subfeature_v2:
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 4c7c9b6044716d0014ea2b0dda86aa69c762ca30
workflow-type: tm+mt
source-wordcount: 710
ht-degree: 9%

---


# Personendetails

Wenn Sie [!DNL Adobe Journey Optimizer B2B Prime] auf der Registerkarte _[!UICONTROL Mitglieder]_ einer (Personenliste[&#128279;](./people-lists.md) auf den Namen einer Person klicken,  die Seite mit den Personendetails mit einer konsolidierten Ansicht dieser Person geöffnet. Diese Seite bietet:

* Eine von KI generierte Rolle, Interaktion und Absichtserklärung
* Vollständiger Aktivitätsverlauf
* Profil- und Firmenattribute
* Die Chat-Oberfläche des KI-Assistenten beantwortet Fragen zur Person.

## Personendetails öffnen {#open-person-details}

1. Erweitern Sie in der linken Navigation **[!UICONTROL Marketing-Verwaltung]**.

1. Wählen Sie rechts in der **[!UICONTROL Marketing]**-Ressourcenliste **[!UICONTROL Personenlisten]** aus.

1. Öffnen Sie eine dynamische oder statische Liste.

1. Klicken Sie auf **[!UICONTROL Name]** einer Person in der Liste.

   ![Liste statischer Personen - Registerkarte „Mitglieder“](./assets/people-list-members-tab.png){width="600" zoomable="yes"}

Die Seite mit Personendetails wird mit drei Registerkarten geöffnet **[!UICONTROL „Übersicht]**, **[!UICONTROL Attribute]** und **[!UICONTROL Unternehmen]**.

## Seitenkopf {#page-header}

In der Kopfzeile wird der Name der Person als Seitentitel zusammen mit einer Schnellansichts-Kontaktleiste angezeigt:

* Stellenbezeichnung
* Unternehmen
* E-Mail-Adresse
* Telefonnummer

Klicken Sie **[!UICONTROL Zurück]**, um zur Ursprungsliste zurückzukehren.

## Registerkarte „Überblick“ {#overview-tab}

Die **[!UICONTROL Übersicht]** enthält die Karten mit der Lead-Zusammenfassung und die Zeitleiste der Aktivität.

![Personendetails - Registerkarte „Übersicht“](./assets/people-list-person-details-overview-tab.png){width="700" zoomable="yes"}

### Lead-Zusammenfassung {#lead-summary}

Drei Karten geben eine KI-generierte Bewertung der Person ab:

| Karte | Inhalt |
|---|---|
| **[!UICONTROL Persona]** | Die [abgeleitete &#x200B;](./personas.md) für die Person sowie eine kurze Erzählung, die ihre Rolle, ihr Unternehmen und ihre Branche beschreibt. Klicken Sie auf das Infosymbol, um weitere Details anzuzeigen. |
| **[!UICONTROL Interaktion]** | Der [Interaktionswert für Personen](./engagement-scores.md) der Trend (z. B _„steigend_) und die Ebene (_niedrig_, _Medium_, _hoch_). |
| **[!UICONTROL Intent]** | Erkannte Kaufabsicht oder _Keine erkannt_ mit kontextueller Anleitung und einem Link, der Ihnen hilft, die Produktabsicht zu erhöhen. |

### Aktivitäten {#activities}

Unter der Lead-Zusammenfassung **[!UICONTROL das Bedienfeld]** Aktivitäten“ den vollständigen Interaktionsverlauf der Person nach Datum gruppiert. Jede Datumgruppe ist erweiterbar und ausblendbar, und jede Zeile zeigt einen Zeitstempel, ein Aktivitätstyp-Tag (z. B. _[!UICONTROL Datenwert ändern]_, _[!UICONTROL Zu Liste hinzufügen]_, _[!UICONTROL Person zum Journey hinzufügen]_ oder _[!UICONTROL Journey-Knotenübergang]_) und eine unmissverständliche Beschreibung der Geschehnisse. Gegebenenfalls enthält die Beschreibung einen Link wie **[!UICONTROL Liste anzeigen]** oder **[!UICONTROL Journey anzeigen]**, um zum zugehörigen Objekt zu springen.

Verwenden Sie die Bedienfeld-Steuerelemente, um mit der Zeitleiste zu arbeiten:

* **Aktivitätstyp** - Filtern Sie die Zeitleiste nach einem bestimmten Aktivitätstyp, z. B. E-Mail-Sendungen, Webinar-Interaktionen oder Listen- und Journey-Änderungen.
* **Datumsbereich** - Begrenzt die Zeitleiste mithilfe des Calendar-Steuerelements auf einen bestimmten Datumsbereich.
* **[!UICONTROL Export]** - Exportieren Sie die sichtbaren Aktivitätsdaten.
* **[!UICONTROL Alle reduzieren]/[!UICONTROL Alle erweitern]** - Schaltet jede Datumsgruppierung ein oder aus, die gleichzeitig geöffnet oder geschlossen ist.

## Registerkarte „Attribute“ {#attributes-tab}

![Personendetails - Registerkarte „Attribute“](./assets/people-list-person-details-attributes-tab.png){width="700" zoomable="yes"}

Auf **[!UICONTROL Registerkarte]** Attribute“ werden die gespeicherten Profilfelder der Person als Titel-/Werteliste angezeigt:

* Vorname
* Zweiter Vorname
* Last name
* E-Mail
* Titel
* Telefon
* Adresse
* Stadt
* Bundesland
* Land
* Unternehmen
* Erstellt
* Zuletzt aktualisiert

## Registerkarte „Unternehmen“ {#company-tab}

![Personendetails - Registerkarte „Unternehmen“](./assets/people-list-person-details-company-tab.png){width="700" zoomable="yes"}

Auf **[!UICONTROL Registerkarte]** Unternehmen“ werden firmografische Daten angezeigt, die mit dem Unternehmen der Person verknüpft sind:

* Unternehmen
* Branche
* Jahresumsatz
* Abrechnungsstraße
* Rechnungsort
* Abrechnungsstatus
* Postleitzahl der Rechnung
* Rechnungsland

Felder ohne verfügbare Daten werden als Bindestriche angezeigt.

## Fragen des KI-Assistenten nach einer Person {#ask-ai-assistant}

Öffnen Sie das Symbol **[!UICONTROL KI]** Assistent-Bedienfeld“ oben auf der Seite, um Hilfe zum aktuellen Personendatensatz zu erhalten. Das Bedienfeld wird für diese Person geöffnet - ein Chip unterhalb des Nachrichten-Threads (z. B. _person: [person name]_) bestätigt, welcher Datensatz Ihre Eingabeaufforderungen als Ziel hat.

![Personendetails - KI-Assistent](./assets/people-list-person-details-ai-assistant.png){width="700" zoomable="yes"}

### Mit vorgeschlagener Eingabeaufforderung starten {#suggested-prompts}

Wenn Sie das Bedienfeld über eine Seite mit Personendetails öffnen, begrüßt Sie der KI-Assistent mit einer kontextuellen Begrüßungsnachricht und vorgeschlagenen Standardaufforderungen, z. B.:

* _Helfen Sie mir, den [Personennamen“ zu]_
* _Erzählen Sie mir [ Persona ]Personennamen_
* _Zusammenfassen [ Interaktionsaktivität ]Personennamens_

Klicken Sie auf eine vorgeschlagene Eingabeaufforderung oder geben Sie Ihre eigene Frage in das Eingabefeld am unteren Rand des Bedienfelds ein.

### Überprüfen der Antwort {#review-response}

Wenn Sie eine Eingabeaufforderung auswählen, wird ein mehrstufiger [Qualifikation](../agents/skills.md) ausgeführt, der als sequenzielle Statusschritte angezeigt wird (z. B. _Person nach ID_ und _Person-Story abrufen_), während der KI-Assistent die Antwort zusammenstellt. Die Antwort ist eine strukturierte Zusammenfassung, die Profildetails, den Interaktionsverlauf und die E-Mail-Leistung der Person enthalten kann.

Verwenden Sie das Steuerelement „Daumen hoch“/„Daumen runter“, um die Antwort zu bewerten. Wie bei allen Ausgaben des KI-Assistenten sollten Sie die Antwort überprüfen, bevor Sie sie verwenden. Weitere Informationen finden Sie in den [Benutzerrichtlinien für die generative KI von Adobe](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}.
