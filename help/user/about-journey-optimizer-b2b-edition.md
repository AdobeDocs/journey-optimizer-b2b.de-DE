---
title: Übersicht über Adobe Journey Optimizer B2B edition
description: Entdecken Sie die wichtigsten Funktionen, Anwendungsfälle und Architekturen von Adobe Journey Optimizer B2B Edition.
exl-id: fdfbafdf-826f-44e9-bbb6-5e729d0e18ef
source-git-commit: 5ca03b12fd459c64b245ad95e60a382c355922f9
workflow-type: tm+mt
source-wordcount: '817'
ht-degree: 5%

---

# Übersicht über Adobe Journey Optimizer B2B edition

Mit Adobe Journey Optimizer B2B Edition können Sie Konto- und Käufergruppen-Journeys mithilfe integrierter generativer KI und branchenführender Automatisierung koordinieren, um die Nachfrage nach spezifischen Angeboten mithilfe Marketing-qualifizierter Käufergruppen zu maximieren.

## Account-Journey bei Einkaufsgruppen

Beim Vergleich von Adobe Journey Optimizer B2B edition mit Marketo Engage und Adobe Journey Optimizer Standard besteht der Hauptunterschied darin, dass Account-Journeys Konten über den Journey verschieben, nicht über Personen. Eine Person, die einem Account zugeordnet ist, weist in der Regel einen nicht-linearen Verlauf auf, der auf dem Fortschritt des Accounts durch den Journey basiert, nicht auf seinen individuellen Aktionen. Wenn sich beispielsweise ein Account in einer frühen Phase des Kauf-Journey befindet, können die gesendeten Informationen allgemeine Lösungsfunktionen oder -funktionen betreffen. Im weiteren Verlauf des Kaufprozesses können die Inhalte zielgerichteter auf bestimmte Angebote oder andere Artikel ausgerichtet werden, die auf den Abschluss eines Verkaufs abzielen. Nach dem Kauf der Lösung ändern sich die Informationen möglicherweise erneut, um Anleitungen, Best Practices oder Informationen über bevorstehende Ereignisse oder mit Inhalten zu zusätzlichen Upsells bereitzustellen. Selbst wenn eine Person mit dem Inhalt der Frühphase nicht interagiert hat, möchten Sie sie dennoch in die aktuelle Phase führen, wobei dies nicht auf ihren eigenen Aktionen basiert, sondern auf den Aktionen der anderen Personen innerhalb ihres Kontos oder ihrer Einkaufsgruppe.

## Hochrangige Architektur

Adobe Journey Optimizer B2B edition verwendet _Account-Zielgruppen_ und _People-Zielgruppen_ von Adobe Experience Platform, um eine Account-Journey zu betreiben, die innerhalb von Marketo Engage ausgeführt wird. Experience Platform ist immer die wahre Quelle für diese Daten, aber die Ausführung und Verarbeitung der Account-Journey erfolgt innerhalb der B2B-Marketing-Infrastruktur von Marketo Engage. Durch die Orchestrierung werden Daten nahezu in Echtzeit über den vorhandenen Quell-Connector von Marketo Engage - Adobe Real-Time CDP B2B edition an Experience Platform zurückgegeben, der Datenänderungen von Marketo Engage an Experience Platform streamt.

![Hochrangige Datenarchitektur](./assets/high-level-data-architecture.png){width="500" zoomable="yes"}{width=„500“ zoomable=„yes“}

>[!NOTE]
>
>Überprüfen Sie Ihre Lizenzberechtigungen und die entsprechende [Produktbeschreibung](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"}{target=„_blank“} auf Leistungs-Schutzmechanismen und statische Einschränkungen.

### Abonnementmodell

Ein Journey Optimizer B2B edition-Abonnement wird durch ein Paar Experience Platform (AEP)-Sandboxes mit einem Marketo Engage _Munchkin_-Abonnement definiert. Es ist nicht möglich, ein einzelnes Marketo Engage-Abonnement mit mehr als einer AEP-Sandbox zu kombinieren. Wenn Sie sich nicht dafür entscheiden, ein bestehendes Marketo Engage-Abonnement mit Journey Optimizer B2B edition zu paaren, erhalten Sie ein neues, leeres Marketo Engage-Abonnement zur Verwendung mit Journey Optimizer B2B edition.

Experience Platform soll bei dieser Einrichtung eine einheitliche Ansicht der Daten aus den Marketo Engage-Instanzen (und allen angeschlossenen CRM-Systemen) bieten und dann mithilfe einer Account-Journey auf die einheitlichen Daten reagieren können.

### Account Journey Operations

Account-Journey werden in Journey Optimizer B2B edition erstellt und in der Marketo Engage-Instanz gespeichert, die mit dem Abonnement verknüpft ist. Obwohl sie im Marketo Engage-Datenspeicher gespeichert ist, ist sie nicht in der Marketo Engage-Benutzeroberfläche sichtbar und nur von Journey Optimizer B2B edition aus verwendbar.

Eine Account-Journey beginnt immer mit der Auswahl eines Account-Segments, das als Account-Audience für die Journey verwendet werden soll. Die Auswahl der Audience erfolgt über die standardmäßige Experience Platform-Audience-Selektor -Komponente. Marketingexperten können die Account-Journey dann implementieren, indem sie die Pfade des Journey nach ihren eigenen Kriterien aufteilen, z. B. Kontokriterien, Personenkriterien oder Kaufgruppenkriterien. In jeder Verzweigung können Aktionen zur Implementierung der Journey durchgeführt werden, z. B. das Senden einer E-Mail oder das Warten auf ein Ereignis.

Nachdem die Konto-Journey erstellt wurde, muss sie veröffentlicht werden. Zum Zeitpunkt der Veröffentlichung wird die Account-Journey validiert und in eine Reihe von Marketo Engage-Kampagnen konvertiert, die das Journey-Erlebnis implementieren. Data Integration Services werden kontaktiert, um den Datenfluss zu starten, der wiederum die Journey-Vorgänge des Kontos startet. Der erste Schritt besteht darin, die Segmente für die Personen des Kontos zu erstellen.

### Datenfluss

Journey Optimizer B2B edition verwendet die Real-Time CDP-Kontosegmentierung sowohl zum Definieren als auch zum Ausführen von Kontosegmenten und zugehörigen Kontopersonensegmenten, die von Journey benötigt werden. Wenn eine veröffentlichte Journey läuft, können sich Daten über Personen und Konten ändern, und es werden Daten über die Personen erfasst, die mit der Journey interagieren. Journey Optimizer B2B edition nutzt den Marketo Engage-Quell-Connector für Real-Time CDP B2B edition, um Datenänderungen zurück an die Experience Platform-Sandbox zu übertragen, die die wahre Quelle ist.  Diese Daten werden nahezu in Echtzeit an AEP übermittelt.

Nur die vorhandenen Datentypen, die vom Marketo Engage-Quell-Connector unterstützt werden (Konten, Personen und Opportunities), fließen zurück in Real-Time CDP. Das bedeutet, dass gekaufte Gruppendaten nicht an AEP übermittelt werden, sondern sich in der Marketo Engage-Instanz befinden, die vom Journey Optimizer B2B edition-Abonnement verwendet wird.
