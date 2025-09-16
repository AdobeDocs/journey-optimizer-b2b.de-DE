---
title: Adobe Journey Optimizer B2B Edition – Überblick
description: 'Erfahren Sie mehr über Adobe Journey Optimizer B2B Edition: Orchestrieren Sie Konto-Journeys mit Käufergruppen, KI-Erkenntnisse und Experience Platform-Integration für B2B-Marketing.'
exl-id: fdfbafdf-826f-44e9-bbb6-5e729d0e18ef
source-git-commit: d3247a48ff1fbda54c559fa03580865da7252935
workflow-type: ht
source-wordcount: '819'
ht-degree: 100%

---

# Adobe Journey Optimizer B2B Edition – Überblick

Mit Adobe Journey Optimizer B2B Edition können Sie Konto- und Käufergruppen-Journeys mithilfe der integrierten generativen KI und einer branchenführenden Automatisierung koordinieren, um die Nachfrage nach spezifischen Angeboten mithilfe Marketing-qualifizierter Käufergruppen zu maximieren.

## Konto-Journeys mit Käufergruppen

Beim Vergleich von Adobe Journey Optimizer B2B Edition mit Marketo Engage und Adobe Journey Optimizer Standard besteht der Hauptunterschied darin, dass bei Konto-Journeys Konten und nicht Personen die Journey durchlaufen. Eine Person, die einem Konto zugeordnet ist, weist in der Regel einen nicht-linearen Verlauf auf, der auf dem Fortschreiten des Kontos durch die Journey basiert, und nicht auf ihren individuellen Aktionen. Befindet sich ein Konto beispielsweise in einer frühen Phase der Kauf-Journey, können die gesendeten Informationen allgemeine Lösungsfunktionen betreffen. Im weiteren Verlauf des Kaufprozesses können die Inhalte stärker zielgerichtet auf bestimmte Angebote oder andere Artikel ausgerichtet werden, die auf den Abschluss eines Verkaufs abzielen. Nach dem Kauf der Lösung ändern sich die Informationen möglicherweise erneut, um Anleitungen, Best Practices oder Informationen zu bevorstehenden Ereignissen oder Inhalte zu zusätzlichen Upsells bereitzustellen. Selbst wenn eine Person nicht mit dem Inhalt der frühen Phase interagiert hat, liegt es dennoch in Ihrem Interesse, sie in die aktuelle Phase zu führen. Dies basiert jedoch nicht auf ihren eigenen Aktionen, sondern auf den Aktionen der anderen Personen innerhalb ihres Kontos oder ihrer Käufergruppe.

## Allgemeine Architektur

Adobe Journey Optimizer B2B Edition verwendet _Kontozielgruppen_ und _Personenzielgruppen_ aus Adobe Experience Platform, um eine Konto-Journey anzutreiben, die innerhalb von Marketo Engage ausgeführt wird. Experience Platform ist immer die wahre Datenquelle, aber die Ausführung und Verarbeitung der Konto-Journey erfolgt innerhalb der B2B-Marketing-Infrastruktur von Marketo Engage. Durch die Orchestrierung werden Daten nahezu in Echtzeit über den vorhandenen Quell-Connector von Marketo Engage – Adobe Real-Time CDP B2B Edition an Experience Platform zurückgegeben, der Datenänderungen von Marketo Engage an Experience Platform streamt.

![Allgemeine Datenarchitektur](./assets/high-level-data-architecture.png){width="500" zoomable="yes"}

>[!NOTE]
>
>Überprüfen Sie Ihre Lizenzberechtigungen und die entsprechende [Produktbeschreibung](https://helpx.adobe.com/de/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} auf Leitlinien für die Leistung und statische Einschränkungen.

### Abonnementmodell

Ein Journey Optimizer B2B Edition-Abonnement wird durch ein Paar von Experience Platform(AEP)-Sandboxes mit einem Marketo Engage _Munchkin_-Abonnement definiert. Es ist nicht möglich, ein einzelnes Marketo Engage-Abonnement mit mehr als einer AEP-Sandbox zu kombinieren. Wenn Sie dagegen entscheiden, ein bestehendes Marketo Engage-Abonnement mit Journey Optimizer B2B Edition zu kombinieren, erhalten Sie ein neues, leeres Marketo Engage-Abonnement zur Verwendung mit Journey Optimizer B2B Edition.

Experience Platform soll bei dieser Einrichtung eine einheitliche Ansicht der Daten aus den Marketo Engage-Instanzen (und allen angeschlossenen CRM-Systemen) bieten und dann mithilfe einer Konto-Journey auf die einheitlichen Daten reagieren können.

### Vorgänge in der Konto-Journey

Konto-Journeys werden in Journey Optimizer B2B Edition erstellt und in der Marketo Engage-Instanz gespeichert, die mit dem Abonnement verknüpft ist. Obwohl sie im Marketo Engage-Datenspeicher gespeichert ist, ist sie nicht in der Marketo Engage-Benutzeroberfläche sichtbar und kann nur über Journey Optimizer B2B Edition verwendet werden.

Eine Konto-Journey beginnt immer mit der Auswahl eines Kontosegments, das als Kontozielgruppe für die Journey verwendet werden soll. Die Auswahl der Zielgruppe erfolgt über die standardmäßige Zielgruppenauswahlkomponente in Experience Platform. Anschließend können Marketing-Fachleute die Konto-Journey implementieren, indem sie die Pfade der Journey nach ihren eigenen Kriterien aufteilen (z. B. Kontokriterien, Personenkriterien oder Käufergruppenkriterien). In jeder Verzweigung können Aktionen zur Implementierung der Journey durchgeführt werden, z. B. das Senden einer E-Mail oder das Warten auf ein Ereignis.

Nachdem die Konto-Journey erstellt wurde, muss sie veröffentlicht werden. Zum Zeitpunkt der Veröffentlichung wird die Konto-Journey validiert und in eine Reihe von Marketo Engage-Kampagnen konvertiert, die das Journey-Erlebnis implementieren. Data Integration Services werden kontaktiert, um den Datenfluss zu starten, der wiederum die Vorgänge der Konto-Journey startet. Der erste Schritt besteht darin, die Segmente für die Personen des Kontos zu erstellen.

### Datenfluss

Journey Optimizer B2B Edition verwendet die Real-Time CDP-Kontosegmentierung zum Definieren sowie zum Ausführen von Kontosegmenten und zugehörigen Kontopersonensegmenten, die für Journeys erforderlich sind. Wenn eine veröffentlichte Journey ausgeführt wird, können sich Daten über Personen und Konten ändern, und es werden Daten über die Personen erfasst, die mit der Journey interagieren. Journey Optimizer B2B Edition nutzt den Quell-Connector von Marketo Engage für Real-Time CDP B2B Edition, um Datenänderungen zurück an die Experience Platform-Sandbox zu übertragen, die die Datenquelle ist.  Diese Daten werden nahezu in Echtzeit an AEP übermittelt.

Nur die vorhandenen Datentypen, die vom Quell-Connector von Marketo Engage unterstützt werden (Konten, Personen und Opportunitys), fließen zurück in Real-Time CDP. Das bedeutet, dass Daten zu Käufergruppen nicht an AEP übermittelt werden, sondern sich in der Marketo Engage-Instanz befinden, die vom Journey Optimizer B2B Edition-Abonnement verwendet wird.
