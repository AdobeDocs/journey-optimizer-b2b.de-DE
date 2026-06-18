---
title: Optimierung des E-Mail-Versandzeitpunkts
description: Die Sendezeitoptimierung (STO) in Adobe Journey Optimizer B2B Prime personalisiert den E-Mail-Versand für Journey von Personen. Erfahren Sie, wie Sie STO aktivieren und die Interaktion verbessern.
autotag-review: '2026-06-17T20:52:02.535Z'
TQID: 'https://experienceleague.adobe.com/wlxhS7E8DnbThm5ge-wzTkMcn-eBzFUXfw3ZGrfcRHA'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: bef5003b-cad2-4f40-bdb2-a80426d52ef5id: f01b5556-e951-40ba-8625-2e3001864f2bid: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1fid: ff0c35fa-aa7e-4050-a37c-198fcacd09e6
source-git-commit: 951d9ceaa95656952e36b6d8f238348b08c796ca
workflow-type: tm+mt
source-wordcount: 403
ht-degree: 0%

---

# Optimierung des E-Mail-Versandzeitpunkts

Verwenden Sie die Funktion „Optimierung des Versandzeitpunkts (STO)“, um den Versandzeitpunkt von E-Mails für [Personen-Journey](./person-journeys.md) zu personalisieren, indem Sie vorhersagen, wann jedes Profil am ehesten interagieren wird. Anstelle einer festen Versandzeit verwendet STO historische E-Mail-Interaktionssignale, um den Versand für jeden Empfänger zum optimalen Zeitpunkt zu planen und so die Interaktion insgesamt zu verbessern.

STO analysiert die historischen Interaktionen jedes Profils mithilfe eines großen Sprachmodells. Er sagt potenzielle Versandzeitpunkte voraus und stuft sie ein, und plant dann den Versand zum Zeitpunkt, der im Optimierungsfenster am höchsten rangiert.

<!-- Performance insights, such as usage, engagement lift, and STO vs. non-STO comparisons, are available through natural language queries in the AI Assistant. -->

>[!BEGINSHADEBOX]

Es sind viele **_zukünftige Verbesserungen_** für STO geplant:

* Globale STOP-Konfiguration im Bereich _[!UICONTROL Admin]_
* STO-Aktivierung auf Journey-Ebene
* Konfigurierbare Test-/Kontrollaufteilungen

>[!ENDSHADEBOX]

## Konfiguration {#configuration}

Sie können die Sendezeitoptimierung konfigurieren, wenn Sie [ Journey eine _[!UICONTROL Aktion durchführen]_-Knoten ](./action-nodes.md) Person hinzufügen und die Aktion **[!UICONTROL E-Mail senden]** auswählen.

1. Wählen Sie den Aktionsknoten _E-Mail senden_ Journey aus.

1. Aktivieren Sie in den Knoteneigenschaften auf der rechten Seite die Option **[!UICONTROL Sendezeitoptimierung]** .

   ![Knoten „E-Mail-Journey senden“ - Optionen zur Optimierung des Versandzeitpunkts](./assets/email-node-send-time-optimization.png){width="450" zoomable="no"}

1. Um das Fenster und die Testverteilung festzulegen, legen Sie die STO-Optionen fest:

   * **[!UICONTROL Senden innerhalb der nächsten]** - Dieser Wert bestimmt das Optimierungsfenster (in Tagen), das den Zeitraum angibt, in dem E-Mails zugestellt werden können. Ein Webinar, das beispielsweise in fünf Tagen stattfindet, kann vier oder fünf Tage dauern. STO wählt für jedes Profil in diesem Fenster die beste prognostizierte Versandzeit aus.

   * **STO / Feste Verteilung** - STO erstellt automatisch eine _Test- und Kontrollaufteilung_ um die geeigneten Profile zwischen optimierten und festen Versandzeiten zu unterteilen. Die Aufspaltung ermöglicht einen direkten Leistungsvergleich. (Es sind zukünftige Verbesserungen geplant, um benutzerdefinierte Aufspaltungsprozentsätze zuzulassen.)

   >[!NOTE]
   >
   >Profile mit einem starken Interaktionsverlauf werden gleichmäßig in Kontroll- und Testgruppen aufgeteilt, um die STO-Wirkung zu messen. Um statistisch verlässliche Ergebnisse zu gewährleisten, ist die Aufteilung zwischen STO und Nicht-STO zwischen 30 % und 70 % beschränkt. Dadurch wird verhindert, dass kleinere Kohorten die Ergebnisse verfälschen, und es werden aussagekräftige Vergleiche sichergestellt.

1. Direkt nach dem Knoten _[!UICONTROL E-Mail senden]_ [fügen Sie einen _Warten_-Knoten hinzu](./wait-nodes.md).

   Auf eine STO-aktivierte E-Mail-Aktion muss sofort ein Warteknoten folgen. Durch Hinzufügen dieses Knotens wird sichergestellt, dass Profile im Journey bleiben, bis das vollständige Optimierungsfenster gelöscht ist und alle STO-Sendungen abgeschlossen sind. Wenn Sie diesen Knoten auslassen, kennzeichnet das System die Konfiguration als ungültig.

1. Nachdem Sie den Rest der Personen-Journey abgeschlossen haben, fahren Sie mit [Veröffentlichen](./person-journeys.md#publish) fort.

## Berichtserstellung


