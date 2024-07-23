---
title: Übersicht über Adobe Journey Optimizer B2B Edition
description: Entdecken Sie die wichtigsten Funktionen, Anwendungsfälle und Architekturen von Adobe Journey Optimizer B2B Edition.
source-git-commit: b9fc31ed31cf05370f1370510d966b8151e14695
workflow-type: tm+mt
source-wordcount: '805'
ht-degree: 0%

---

# Übersicht über Adobe Journey Optimizer B2B Edition

Mit der Adobe Journey Optimizer B2B Edition können Sie Konto- und Einkaufsgruppen-Journey mithilfe integrierter generativer KI und branchenführender Automatisierung koordinieren, um die Nachfrage nach spezifischen Angeboten mithilfe marketingqualifizierter Einkaufsgruppen zu maximieren.

## Journey mit Einkaufsgruppen

Beim Vergleich von Adobe Journey Optimizer B2B Edition mit Marketo Engage und Adobe Journey Optimizer Standard besteht der Hauptunterschied darin, dass Journey Konten durch die Journey verschieben, nicht durch Personen. Eine Person, die mit einem Konto verknüpft ist, weist höchstwahrscheinlich eine nicht lineare Progression auf, die auf dem Fortschritt des Kontos durch die Journey basiert und nicht auf ihren individuellen Aktionen basiert. Wenn sich beispielsweise ein Konto in einer frühen Phase der Journey befindet, können die gesendeten Informationen allgemeine Lösungsfunktionen betreffen. Im weiteren Verlauf des Kaufprozesses kann der Inhalt zielgerichteter auf bestimmte Angebote oder andere Artikel ausgerichtet werden, die auf das Schließen eines Verkaufs ausgerichtet sind. Nach dem Kauf der Lösung ändern sich die Informationen möglicherweise erneut, um Anleitungen, Best Practices oder Informationen über bevorstehende Ereignisse oder Inhalte über zusätzliche Upsells bereitzustellen. Selbst wenn eine Person nicht mit dem Inhalt der frühen Phase interagiert hat, möchten Sie sie dennoch in die aktuelle Phase eintreten, nicht auf der Grundlage ihres eigenen Handelns, sondern auf der Grundlage des Handelns der anderen Personen in ihrem Konto oder ihrer Einkaufsgruppe.

## Umfangreiche Architektur

Adobe Journey Optimizer B2B Edition verwendet _Kontozielgruppen_ und die _Zielgruppen des Kontos_ aus Adobe Experience Platform, um eine Journey für das Konto zu ermöglichen, die innerhalb von Marketo Engage ausgeführt wird. Experience Platform ist immer die &quot;Source of Truth&quot; für diese Daten, aber die gesamte Ausführung und Verarbeitung der Konto-Journey erfolgt innerhalb der Marketo Engage-B2B-Marketinginfrastruktur. Die Orchestrierung bringt Daten nahezu in Echtzeit durch den bestehenden Marketo Engage - Adobe Real-Time CDP B2B Edition Quell-Connector auf Experience Platform zurück, der Datenänderungen von Marketo Engage an Experience Platform überträgt.

![Datenarchitektur auf hoher Ebene](./assets/high-level-data-architecture.png){width="600" zoomable="yes"}

### Abonnementmodell

Ein Journey Optimizer B2B Edition-Abonnement wird durch ein Paar von Experience Platform-Sandboxes (AEP) mit einem Marketo Engage _munchkin_-Abonnement definiert. Es ist nicht möglich, ein einzelnes Marketo Engage-Abonnement mit mehr als einer AEP-Sandbox zu verbinden. Wenn Sie sich nicht für ein bestehendes Marketo Engage-Abonnement mit Journey Optimizer B2B Edition entscheiden oder derzeit kein Marketo Engage verwenden, erhalten Sie ein neues, leeres Marketo Engage-Abonnement für die Verwendung mit Journey Optimizer B2B Edition.

Mit der Experience Platform in dieser Einrichtung soll eine einheitliche Sicht auf die Daten der Marketo Engage-Instanzen (und angehängter CRM-Systeme) gewährleistet und anschließend mithilfe einer Konto-Journey auf die einheitlichen Daten reagiert werden können.

### Journey-Vorgänge für Konten

Journey werden in Journey Optimizer B2B Edition erstellt und in der mit dem Abonnement verknüpften Marketo Engage-Instanz gespeichert. Obwohl sie im Marketo Engage-Datenspeicher gespeichert ist, ist sie nicht in der Marketo Engage-Benutzeroberfläche sichtbar und kann nur von Journey Optimizer B2B Edition aus verwendet werden.

Eine Journey beginnt immer mit der Auswahl eines Kontosegments, das als Kontenzielgruppe für die Journey verwendet werden soll. Die Auswahl der Audience verwendet die standardmäßige Experience Platform-Audience-Selektor-Komponente. Marketingexperten können dann die Konto-Journey implementieren, indem sie die Pfade der Journey nach ihren eigenen Kriterien aufteilen, zu denen Kontokriterien, Personenkriterien oder Einkaufsgruppenkriterien gehören können. Auf jeder Verzweigung können Aktionen zur Implementierung der Journey durchgeführt werden, z. B. das Senden einer E-Mail oder das Warten auf das Eintreten eines Ereignisses.

Nachdem die Journey erstellt wurde, muss sie veröffentlicht werden. Zum Zeitpunkt der Veröffentlichung wird die Journey des Kontos validiert und in eine Reihe von Marketo Engage-Kampagnen konvertiert, die das Journey-Erlebnis implementieren. Data Integration Services werden kontaktiert, um den Datenfluss zu starten, der wiederum den Journey-Vorgang für das Konto startet. Der erste Schritt besteht darin, die Segmente für die Personen des Kontos zu erstellen.

### Datenfluss

Journey Optimizer B2B Edition verwendet die Real-Time CDP-Kontosegmentierung zum Definieren und Ausführen von Kontosegmenten und zugehörigen Kontopersonensegmenten, die für Journey erforderlich sind. Während eine veröffentlichte Journey ausgeführt wird, können sich Daten über die Personen und Konten ändern und Daten über die Personen erfasst werden, die mit der Journey interagieren. Journey Optimizer B2B Edition nutzt den Marketo Engage-Quell-Connector für Real-Time CDP B2B Edition, um Datenänderungen zurück in die Experience Platform-Sandbox zu leiten, die die &quot;Source of Truth&quot; ist.  Diese Daten werden fast in Echtzeit an AEP übermittelt.

Nur die vom Marketo Engage-Quell-Connector unterstützten Datentypen (Konten, Personen und Möglichkeiten) fließen zurück in Real-Time CDP. Das bedeutet, dass die Daten der gekauften Gruppe nicht an AEP fließen und stattdessen in der Marketo Engage-Instanz gespeichert sind, die von der Journey Optimizer B2B Edition-Anmeldung verwendet wird.

