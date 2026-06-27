---
title: Erstellen benutzerdefinierter Bewertungsmodelle
description: Erstellen, Anzeigen und Veröffentlichen benutzerdefinierter Lead-Bewertungsmodelle in Journey Optimizer B2B Prime mithilfe der Scoring Studio-Kenntnisse in der Chat-Oberfläche des KI-Assistenten.
badgeBeta: label="Beta" type="informative" tooltip="Diese Funktion befindet sich derzeit in einer eingeschränkten Beta-Version"
autotag-review: '2026-06-25T21:20:26.754Z'
TQID: 'https://experienceleague.adobe.com/-D5EaJ-3GQ5iwaE6hChscZGEdflKmZ3tdp6VUNuPjWk'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: bef5003b-cad2-4f40-bdb2-a80426d52ef5id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: ff10f619-348f-47e3-99bf-3ce4c817cf2cid: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: d8f352c636ebd8980614922099701de8f755e8e4
workflow-type: tm+mt
source-wordcount: 489
ht-degree: 2%

---

# Erstellen benutzerdefinierter Bewertungsmodelle

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_scoring_studio"
>title="Scoring-Studio"
>abstract="Verwenden Sie die Scoring Studio-Kenntnisse zum Erstellen, Konfigurieren und Veröffentlichen benutzerdefinierter Lead-Scoring-Modelle über die Chat-Oberfläche des KI-Assistenten."

Die [_Scoring Studio_-](./skills.md#scoring-signals) in [!DNL Adobe Journey Optimizer B2B Prime] bietet eine KI-native Lead-Scoring-Lösung, mit der Sie Lead-Scoring-Modelle erstellen, konfigurieren und veröffentlichen können. Das Studio kombiniert einen agentengesteuerten Workflow mit einer visuellen Benutzeroberfläche. Sie können Bewertungsmodelle durch natürliche Spracheingaben in der [KI-Assistenten-Chat-Oberfläche ](./chat-interface.md) durch direkte Interaktion mit den Benutzeroberflächen-Steuerelementen erstellen.

* **Kenntnisse** - `scoring-studio`
* **Aufruf** - Verwenden Sie einen Schrägstrich, um Scoring Studio zu öffnen. Beispiel: _„Open Scoring Studio.“_
* **Lese-/Schreibvorgänge an** - [!DNL Journey Optimizer B2B Prime] Scoring-Service; liest [!DNL Marketo Engage] Lead-Felder und Aktivitätstypen

Beim Launch ruft der KI-Assistent automatisch relevanten Kontext ab - einschließlich Aktivitätstypen, Lead-Feldern, Personenlisten und vorhandenen Bewertungslisten -, um seine Vorschläge in Ihren Daten zu begründen.

![Scoring Studio in der Benutzeroberfläche des KI-Assistenten gestartet](./assets/scoring-studio.png){width="700" zoomable="yes"}

## Scoring-Modell erstellen {#create-model}

Wenn Sie Scoring Studio öffnen, schlägt der KI-Assistent ein relevantes Beispiel für ein Scoring-Modell vor, das mit einer statischen Liste und einer Reihe von bewerteten Aktivitäten vorausgefüllt ist. Sie können diesen vorgeschlagenen Ausgangspunkt annehmen oder Ihre eigene Aufforderung angeben, um ein benutzerdefiniertes Modell zu definieren.

### Vorschau des Modells {#preview-model}

Nachdem Sie eine Eingabeaufforderung eingegeben haben, generiert der KI-Assistent eine Modellvorschau, bevor Sie Änderungen vornehmen. Die Vorschauoberflächen:

* Verwendete Scoring-Dimensionen
* Bewertete Attribute und Aktivitäten
* Statische Listen oder Smart-Listen, die als Segmente angewendet werden
* Eine Zusammenfassung des Modellziels, des Zielsegments und der primären Signale

Sie können die Vorschau überprüfen und wählen, ob Sie das Modell basierend darauf erstellen möchten, oder den Chat vor der Fertigstellung weiter verfeinern.

### Modellstruktur {#model-structure}

Das erstellte Modell ist in _Dimensionen_ und _Signale_ organisiert. Sie können jedes Signal über das Bedienfeld „Eigenschaft“ in der Benutzeroberfläche konfigurieren:

* **Signaltyp** — Aktivitäts- oder attributbasiert
* **Aktivität oder Attribut** - Das spezifische Element, das bewertet werden soll
* **Signalparameter** — Einstellbare Einstellungen für das Signal

Sie können Modelle vollständig über den Agenten in natürlicher Sprache erstellen und konfigurieren oder direkt mit den Benutzeroberflächen-Steuerelementen interagieren.

## Scoring-Modell veröffentlichen {#publish-model}

Weisen Sie nach Fertigstellung Ihres Modells den Agenten an, es zu veröffentlichen. Der Veröffentlichungsprozess verarbeitet automatisch Folgendes:

| Schritt | Was passiert? |
|---|---|
| **Regelkompilierung** | Alle Bewertungsregeln werden kompiliert und validiert |
| **Erstellen von Score-Aufgaben** | Eine geplante Bewertungsaufgabe wird erstellt und für die tägliche Ausführung konfiguriert |

Nach der Veröffentlichung haben Sie auch die Möglichkeit, einen manuellen Trigger auszuführen, um Scores sofort zu verarbeiten.

## Scoring-Ergebnisse anzeigen {#view-results}

Nach Abschluss eines Scoring-Durchgangs werden die Bewertungen über den Lead-Importprozess zurück in [!DNL Marketo Engage] geschrieben. Nach Abschluss des Imports können die aktualisierten Scores direkt in [!DNL Marketo Engage] überprüft werden.

Nach jedem Durchlauf können Sie eine Ergebniszusammenfassung anzeigen, die Folgendes anzeigt:

* Wie viele Personen wurden bewertet?
* Die individuelle Punktzahl ändert sich pro Person

Ein Administratorprotokoll ist für die Überprüfung zusätzlicher Ausführungsdetails verfügbar.
