---
title: Übersicht über Adobe Journey Optimizer B2B edition
description: Entdecken Sie die wichtigsten Funktionen, Anwendungsfälle und Architekturen von Adobe Journey Optimizer B2B Edition.
exl-id: fdfbafdf-826f-44e9-bbb6-5e729d0e18ef
source-git-commit: 5ca03b12fd459c64b245ad95e60a382c355922f9
workflow-type: tm+mt
source-wordcount: '811'
ht-degree: 5%

---

# Übersicht über Adobe Journey Optimizer B2B edition

Mit Adobe Journey Optimizer B2B Edition können Sie Konto- und Käufergruppen-Journeys mithilfe integrierter generativer KI und branchenführender Automatisierung koordinieren, um die Nachfrage nach spezifischen Angeboten mithilfe Marketing-qualifizierter Käufergruppen zu maximieren.

## Customer Journeys mit Einkaufsgruppen

Beim Vergleich Adobe Systems Journey Optimizer B2B Edition mit Marketo Engage und Adobe Systems Journey Optimizer-Standard besteht der Hauptunterschied darin, dass Konto Journeys Konten und nicht Personen durch die Journey bewegen. Eine Person, die mit einem Konto in Verbindung gebracht wird, hat in der Regel eine nichtlineare Progression, die auf dem Fortschritt der Konto durch die Journey basiert, nicht auf ihren Kontakt Handlungen. Wenn sich ein Konto Instanz in einer frühen Phase des Kaufs Journey befindet, können sich die gesendeten Informationen auf allgemeine Lösungsfunktionen oder -merkmale beziehen. Im weiteren Verlauf der Kaufprozess könnte die Inhalte stärker auf bestimmte Angebote oder andere Artikel ausgerichtet sein, die auf den Abschluss eines Verkaufs ausgerichtet sind. Nachdem die Lösung gekauft wurde, können sich die Informationen erneut ändern, um Anleitungen, Best Practices oder Informationen über bevorstehende Veranstaltungen oder Inhalte über zusätzliche Upsells bereitzustellen. Selbst wenn ein Kontakt nicht mit der frühen Phase Inhalte interagiert hat, möchten Sie ihn dennoch in die aktuelle Phase bringen, nicht basierend auf seinen eigenen Handlungen, sondern auf der Grundlage der Handlungen der anderen Personen in seiner Konto oder kaufen Gruppe.

## Allgemeine Architektur

Adobe Systems Journey Optimizer B2B Edition verwendet _Account Audiences_ und _People Audiences_ von Adobe Experience Platform, um eine Konto Journey zu betreiben, die in Marketo Engage ausgeführt wird. Experience Platform ist immer die wahre Quelle für diese Daten, aber die Ausführung und Verarbeitung der Account-Journey erfolgt innerhalb der B2B-Marketing-Infrastruktur von Marketo Engage. Der Orchestrierung bringt Daten nahezu in Echtzeit über den vorhandenen Marketo Engage zurück Experience Platform - Adobe Systems Real-Zeit CDP B2B Edition-Quellkonnektor, der Datenänderungen von Marketo Engage auf Experience Platform streamt.

![Hochrangige Datenarchitektur](./assets/high-level-data-architecture.png){width="500" zoomable="yes"}

>[!NOTE]
>
>Überprüfen Sie Ihre Lizenzberechtigungen und die entsprechende [Produktbeschreibung](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} auf Leistungs-Leitplanken und statische Einschränkungen.

### Abonnementmodell

Ein Journey Optimizer B2B Edition-Mitgliedschaft wird durch ein Paar Experience Platform (AEP)-Sandboxes mit einem Marketo Engage _Munchkin-Mitgliedschaft_ definiert. Es ist nicht möglich, dass eine einzelne Marketo Engage Mitgliedschaft mit mehr als einer AEP-Sandbox gekoppelt wird. Wenn Sie sich nicht dafür entscheiden, eine vorhandene Marketo Engage Mitgliedschaft mit Journey Optimizer B2B Edition zu koppeln, wird Ihnen eine neue, leere Marketo Engage Mitgliedschaft für die Verwendung mit Journey Optimizer B2B Edition bereitgestellt.

Der Zweck der Experience Platform in diesem Setup besteht darin, eine einheitliche Ansicht für die Daten aus den Marketo Engage Instanzen (und allen angehängten CRM Systemen) bereitzustellen und dann mithilfe einer Konto Journey auf die vereinheitlichten Daten reagieren zu können.

### Vorgänge für Konto Journey

Account-Journeys werden in Journey Optimizer B2B Edition erstellt und in der Marketo Engage Instanz gespeichert, die mit dem Mitgliedschaft verknüpft ist. Obwohl es in der Marketo Engage Data Geschäft gespeichert ist, ist es im Marketo Engage UI nicht sichtbar und kann immer nur in Journey Optimizer B2B Edition verwendet werden.

Eine Konto Journey beginnt immer mit der Auswahl einer Konto Segment, die als Konto Zielgruppe für die Journey verwendet werden soll. Die Auswahl der Zielgruppe verwendet die Standardkomponente Experience Platform Zielgruppe Selektor. Marketingexperten können die Account-Journey dann implementieren, indem sie die Pfade des Journey nach ihren eigenen Kriterien aufteilen, z. B. Kontokriterien, Personenkriterien oder Kaufgruppenkriterien. In jeder Verzweigung können Aktionen zur Implementierung der Journey durchgeführt werden, z. B. das Senden einer E-Mail oder das Warten auf ein Ereignis.

Nachdem die Konto-Journey erstellt wurde, muss sie veröffentlicht werden. Zum Zeitpunkt der Veröffentlichung wird die Account-Journey validiert und in eine Reihe von Marketo Engage-Kampagnen konvertiert, die das Journey-Erlebnis implementieren. Data Integration Services werden kontaktiert, um den Datenfluss zu starten, der wiederum die Journey-Vorgänge des Kontos startet. Der erste Schritt besteht darin, die Segmente für die Personen des Kontos zu erstellen.

### Datenfluss

Journey Optimizer B2B Edition verwendet die Real-Zeit CDP Konto Segmentierung für die Definition und Ausführung von Konto Segmenten und zugehörigen Konto Personensegmenten, die für Journeys erforderlich sind. Während ein veröffentlichtes Journey ausgeführt wird, können sich Daten zu den Personen und Konten ändern, und es werden Daten zu den Personen gesammelt, die mit dem Journey interagieren. Journey Optimizer B2B Edition verlässt sich auf den Marketo Engage Source Connector für Real-Zeit CDP B2B Edition, um Datenänderungen zurück an die Experience Platform Sandbox zu leiten, die die Quelle der Wahrheit ist.  Diese Daten werden nahezu in Echtzeit an AEP übermittelt.

Nur die vorhandenen Datentypen, die vom Marketo Engage Quell-Connector unterstützt werden (Accounts, People und Opportunities), fließen zurück in die Real-Zeit CDP. Das bedeutet, dass der Kauf Gruppe Daten nicht an AEP fließt und sich stattdessen in der Marketo Engage Instanz befindet, die von der Journey Optimizer B2B Edition Mitgliedschaft verwendet wird.
