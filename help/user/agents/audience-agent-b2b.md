---
title: Audience Agent B2B
description: Audience Agent B2B in Journey Optimizer B2B Edition verwendet Intent Analysis und Persona Mapping, um Einkaufsgruppen zu erstellen und B2B-Marketing-Workflows zu beschleunigen.
feature: Audiences, AI Assistant
role: User
source-git-commit: 7f1c1533c226a2626978ada221c7026bc3d1432b
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Audience Agent B2B

Mit [Adobe Experience Platform Agent Orchestrator &#x200B;](https://experienceleague.adobe.com/de/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator) ist Audience Agent B2B in Journey Optimizer B2B edition verfügbar. Die Verwendung dieses Agenten verbessert die Effizienz und Effektivität beim Erkunden und Skalieren von Zielgruppen, beschleunigt die Erstellung von Einkaufsgruppen und bietet nahtlose Workflows für die Journey-Aktivierung:

* **_Priorisieren der Zielgruppen nach Absicht_** - Ziehen Sie Personas auf der Grundlage des Produktinhalts für verschiedene Zielgruppen heran und optimieren Sie die Kampagnenplanung, indem Sie die Zeit für die Audience-Validierung reduzieren.

* **_Nutzen von KI zur Erkennung von Einkaufsgruppen_** - Verwenden Sie KI, strukturierte, unstrukturierte Daten und einheitliche First-Party-Daten, um die Erkennung und Erstellung von Einkaufsgruppen zu optimieren.

![Audience Agent B2B im Vollseitenmodus](./assets/audience-agent-full.png){width="700" zoomable="yes"}

## Audience Agent-Funktionen

| Bereich | Funktion | Geschäftswert |
| ---- | ------------ | -------------- |
| Absichtsanalyse | <li> Messen Sie die Stärke der Kontoabsicht (z. B. niedrig, mittel und hoch) für bestimmte Produkte. <li>Vergleichen Sie die Trends der Produktzinsen im Zeitverlauf (z. B. die Top-Produkte der letzten _n_ Tage). <li>Identifizieren Sie Konten, die aktiv Interesse an bestimmten Produkten zeigen. <li>Interaktionsmuster, die Kontoaktivität mit persönlicher Abdeckung kombinieren. | <li>Hilft Teams, sich zum richtigen Zeitpunkt auf die richtigen Accounts zu konzentrieren. <li>Verbessert die Pipeline-Qualität, indem Konten mit echten Kaufsignalen priorisiert werden. <li>Ermöglicht proaktive Interaktion, bevor Mitbewerber handeln. |
| Persona-Zuordnung | <li>Erkennen und Sortieren von Top-Personas nach Produktabsicht. <li>Identifizieren Sie Personen, die am Kauf eines oder mehrerer Produkte beteiligt sind. <li>Ordnen Sie Rollen (Champion, Entscheidungsträger, Influencer usw.) mit einer Begründung zu. <li>Überprüfen, warum eine bestimmte Person als Champion gilt. | <li>Stellt sicher, dass der Vertrieb die wahren Entscheidungsträger und Influencer anspricht. <li>Geringerer Aufwand bei Kontakten mit geringen Auswirkungen. <li>Steigert die Gewinnraten durch Abstimmung der Reichweite auf die Kaufkraftdynamik. |
| Einkaufsgruppenbewertung | <li>Bewerten Sie die Größe der Einkaufsgruppe (z. B. Gruppen mit mehr als n Mitgliedern). <li>Messen der persönlichen Abdeckung aller Konten (z. B. unter x %). <li>Verfolgen Sie Rollenverteilungs- und Abdeckungslücken in Einkaufsgruppen. <li>Markieren Sie Konten mit Champions, die in den letzten Angeboten identifiziert wurden. | <li>Zeigt Abdeckungslücken, die Abschlüsse blockieren könnten. <li>Stärkt Multithreading-Strategien durch Sicherstellung einer vollständigen Rollendarstellung. <li>Verbessert die Verfolgung der Angebotsstatus durch Interaktionseinblicke auf Gruppenebene. |

## Beispiele für Eingabeaufforderungen

In diesen Beispielen werden einige Möglichkeiten der Verwendung des Agenten demonstriert:

* Trend-Fenster anzeigen: Früheste und letzte Aktualisierung für die Kontoproduktzielsetzung pro Produkt.
* Listen Sie `<product>` Einkaufsgruppen mit Produktabsicht und Bewertungen auf.
* Listen Sie `<product>` Personas und Rollen mit ihren Opportunity-Metriken auf (Erfolgsrate, Mitgliedschaftsrate, Anzahl).
* Wie ist die durchschnittliche Abdeckung von Account-Personas bei Accounts in `<industry>` für `<product>`?
* Welche Accounts haben eine geringe Absicht für ein Produkt, haben aber immer noch offene Möglichkeiten (die es wert sind, gepflegt zu werden)?
* Welche Accounts haben diese Woche neue Absichtssignale für `<account_name>` hinzugefügt?
