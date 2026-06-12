---
title: Zielgruppen-Management
description: Platzhalterseite für Zielgruppen.
autotag-review: '2026-06-12T22:47:10.727Z'
TQID: 'https://experienceleague.adobe.com/KWT9-Lr6358MQ0sLQyKAlb4SLERnBl-QQL7Cj1iXCZM'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: beb5f4be-cec3-471a-9db6-831a77dd3ac9id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: cb3217c9fd7beb712d0c61638d143b798010d2b7
workflow-type: tm+mt
source-wordcount: 442
ht-degree: 4%

---

# Zielgruppen-Management

Wie können Audiences in AJO B2B Prime gespielt werden?

Klicken Sie im rechten Navigationsbereich im Marketing **[!UICONTROL Management-Hub auf]** Personenlisten“.

![Zugreifen auf Personenlisten zur Verwaltung Ihrer Zielgruppen](./assets/people-lists.png){width="800" zoomable="yes"}

Es gibt zwei Registerkarten für die Seite, auf denen Sie (dynamische Listen **[!UICONTROL und (statische Listen]** anzeigen **[!UICONTROL verwalten]**. Klicken Sie auf die Registerkarte, um die Listenansicht zwischen den einzelnen Typen zu wechseln.

Auf dieser Seite haben Sie folgende Möglichkeiten:

* Erstellen neuer dynamischer und statischer Listen
* Nach bestehenden Listen suchen
* Asset-Informationen anzeigen
* Auf Listen zugreifen, um ihre Mitgliedschaft zu überprüfen

<!--
## Audience Hub

The AI Audience Hub is a centralized, AI-driven starting point for all audience-related capabilities across AJO B2B. It is designed to accelerate first-time user success while progressively unlocking advanced intelligence, insights, and control for returning and power users.

The Hub acts as:

* A guided starting point for discovering, creating, and refining person lists, account lists, and buying groups

* A visibility layer for audience health, coverage, overlap, engagement patterns, and AI-driven insights

* A control center for audience governance, optimization, reuse, and readiness for activation across journeys and sales workflows

### High level structure

Prompt-based starting point - Quick Start prompts and freeform input to help users discover, create, or optimize audiences.

1. AI insights feed - Surfaces key audience signals such as overlap, gaps, saturation risk, and optimization opportunities.

1. Adaptive audience library - A personalized view of people lists, account lists, and buying groups that adapts based on usage, relevance, and activation.

1. Optimization and arbitration nudges - Guides users to refine, split, or reuse audiences before activation.

1. Audience visibility and reporting - High-level insight into audience health, engagement patterns, and usage across active journeys.


### Empty and Error States (High-Level)

No audiences / no data - Show Quick Start prompts to help first-time users create or import person lists

Low data or incomplete audience - Explain what's missing (e.g., insufficient contacts, missing persona coverage, or low engagement data) and suggest next steps.

AI insights unavailable - Provide a graceful fallback with a clear explanation, so users understand why insights aren't shown and what actions they can take manually.
-->

## Erstellen einer Personenliste


Erstellen einer neuen dynamischen oder statischen Liste:

1. Klicken **oben rechts** der Seite &quot;_[!UICONTROL &quot; auf „Liste]_&quot;.
1. Wählen Sie ein Programm als **[!UICONTROL Übergeordnetes Element]** für die Liste aus.
1. Geben Sie die Liste als **[!UICONTROL Name]** und **[!UICONTROL Beschreibung]** (optional) ein.
1. Wählen Sie dann Liste **[!UICONTROL Typ]**:

   * **[!UICONTROL Statisch]** - Die Mitgliedschaft wird durch qualifizierte Filter bestimmt, die beim Erstellen der Liste ausgewertet werden. Die Listenmitgliedschaft wird nur aktualisiert, wenn Datensätze manuell qualifiziert oder disqualifiziert werden.
***[!UICONTROL Dynamisch]** - Die Mitgliedschaft wird durch qualifizierte Filter dynamisch bestimmt. Die Mitgliedschaft in der Liste wird automatisch aktualisiert.

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

>[!NOTE]
>
>„Löschen“ und „Duplizieren“ werden derzeit für Personenlisten in dieser Beta-Version nicht unterstützt.

## Statische Listen

Die statische Mitgliedschaft in Listen wird durch einfache Filter definiert, die auf Personenattribute und Aktivitäten verweisen. Die Mitgliedschaft ändert sich nur, wenn Sie Mitglieder manuell qualifizieren oder disqualifizieren.

### Mitglieder hinzufügen

1. Öffnen Sie die statische Liste und klicken Sie **[!UICONTROL oben]** auf „Personen hinzufügen“.

1. Definieren Sie im Dialogfeld die Regeln für die Qualifizierung Ihrer Leads, indem Sie Filter von links ziehen und ablegen.

   Sie können Personen nach einer beliebigen Kombination aus folgenden Kriterien filtern:

   * Aktivitätsverlauf
   * Unternehmensattribute
   * Personenattribute
   * Spezielle Filter wie Journey-Mitgliedschaft

1. Klicken Sie auf „Fertig“, um **[!UICONTROL Änderungen]** speichern.

1. Wählen Sie die **[!UICONTROL Mitglieder]** aus.

   Nach kurzer Zeit werden qualifizierte Mitglieder in der Liste aufgeführt.

### Mitglieder entfernen

1. Öffnen Sie die statische Liste und klicken Sie **[!UICONTROL oben]** auf „Personen entfernen“.

1. Fügen Sie im Dialogfeld die Filter hinzu, um Mitglieder zu finden, die Sie nicht qualifizieren möchten.

1. Klicken Sie auf „Fertig“, um **[!UICONTROL Änderungen]** speichern.

1. Wählen Sie die **[!UICONTROL Mitglieder]** aus.

   Nach kurzer Zeit verlassen disqualifizierte Mitglieder die Liste.

## Dynamische Listen

Die Zugehörigkeit zu einer dynamischen Liste wird mithilfe einfacher Filter definiert, die auf Personenattribute und Aktivitäten verweisen. Die Mitgliedschaft wird automatisch aufrechterhalten, indem Leads entsprechend der Filterlogik qualifiziert und disqualifiziert werden.

### Definieren der Mitgliedschaftslogik

1. Öffnen Sie die statische Liste und wählen Sie die Registerkarte Regeln aus.

1. Klicken Sie auf Regeln bearbeiten .

1. Definieren Sie im Dialogfeld die Regeln für die Qualifizierung Ihrer Leads, indem Sie Filter von links ziehen und ablegen.

   Sie können Leads für die Liste qualifizieren, indem Sie eine beliebige Kombination aus Folgendem verwenden:

   * Aktivitätsverlauf
   * Unternehmensattribute
   * Personenattribute
   * Spezielle Filter wie Journey-Mitgliedschaft

1. Klicken Sie auf „Fertig“, um **[!UICONTROL Änderungen]** speichern.

1. Wählen Sie die **[!UICONTROL Mitglieder]** aus.

   Nach kurzer Zeit werden qualifizierte Mitglieder in der Liste aufgeführt.

Klicken Sie auf den Namen einer Person in der Liste, um die Detailseite für das Lead-Profil zu öffnen, auf der die Zusammenfassung und die letzten Aktivitäten angezeigt werden.