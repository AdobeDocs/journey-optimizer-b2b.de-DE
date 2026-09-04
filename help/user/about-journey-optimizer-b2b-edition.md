---
title: Adobe Journey Optimizer B2B Edition – Überblick
description: 'Erfahren Sie mehr über Adobe Journey Optimizer B2B Edition: Orchestrieren Sie Konto-Journeys mit Käufergruppen, nutzen Sie KI-Erkenntnisse und die Integration mit Adobe Experience Platform für B2B-Marketing.'
exl-id: fdfbafdf-826f-44e9-bbb6-5e729d0e18ef
autotag-review: 2026-04-29T23:21:13.339Z
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: f467931a-9b22-4ca8-869f-adfbd64061ce
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
TQID: https://experienceleague.adobe.com/L58cK4MP-S-8U9fFiXU2qZn4HCieNzjoOaSRCLkyanI
source-git-commit: 8d2fc3ebc7df1674ac9af441679228a9e19d8d5a
workflow-type: tm+mt
source-wordcount: 739
ht-degree: 15%

---

# Adobe Journey Optimizer B2B Edition – Überblick

Mit Adobe Journey Optimizer B2B edition können Sie Personen- und Account-Journey mithilfe integrierter generativer KI und branchenführender Automatisierung koordinieren, um die Nachfrage nach bestimmten Angeboten mithilfe von Marketing-qualifizierten Einkaufsgruppen zu maximieren.

## Konto-Journeys mit Käufergruppen

Beim Vergleich von Konto-Journeys mit den Journey-Funktionen in Marketo Engage und der Standardversion von Adobe Journey Optimizer besteht der Hauptunterschied darin, dass sich bei Konto-Journeys Konten durch die Journey bewegen, nicht Personen. Eine Person, die einem Konto zugeordnet ist, weist in der Regel einen nicht-linearen Verlauf auf, der auf dem Fortschreiten des Kontos durch die Journey basiert, und nicht auf ihren individuellen Aktionen. Wenn sich beispielsweise ein Account in einer frühen Phase des Kauf-Journey befindet, werden in der Regel Informationen zu allgemeinen Lösungsmöglichkeiten oder -funktionen gesendet. Im weiteren Verlauf des Kaufprozesses werden die Inhalte zielgerichteter auf bestimmte Angebote oder andere Artikel ausgerichtet, die auf den Abschluss eines Verkaufs abzielen. Nach dem Kauf der Lösung ändern sich die Informationen erneut, um Anleitungen, Best Practices, Informationen über bevorstehende Ereignisse oder Inhalte über zusätzliche Upsells bereitzustellen. Selbst wenn eine Person nicht mit Inhalten der frühen Phase interagiert hat, können Sie sie basierend auf den Aktionen anderer in ihrem Konto oder ihrer Einkaufsgruppe in die aktuelle Phase weiterleiten.

## Allgemeine Architektur

Adobe Journey Optimizer B2B edition basiert auf Adobe Experience Platform, einschließlich Real-Time CDP B2B. Journey Optimizer B2B edition und Marketo Engage werden auf separaten Systemen mit jeweils einem eigenen Datenspeicher ausgeführt. Experience Platform ist der primäre Datenspeicher und die maßgebliche Quelle für Accounts, Personen und Opportunities. Journey Optimizer B2B edition besitzt die Journey Ihres Kontos, kauft Gruppen und kauft Gruppenrollen.

Eine dedizierte Marketo Engage-Instanz unterstützt jedes Journey Optimizer B2B edition-Abonnement. Diese Instanz speichert keine Journey, Zielgruppen oder Einkaufsgruppen Ihres Kontos. Stattdessen werden Berechtigungen und Backend-Services wie E-Mail-Versand, Absenderkonfiguration und Branding-Domains bereitgestellt.

Um Journey-Aktionen zu unterstützen, können Sie auch eine oder mehrere Ihrer bestehenden Marketo Engage-Instanzen verbinden, einschließlich Ihrer Produktionsinstanz. Mit Journey-Aktionen können Marketing-Fachleute Account-basierte Journey in Journey Optimizer B2B edition mit Lead-basierten Kampagnen in Marketo Engage koordinieren, z. B. das Hinzufügen von Personen zu einer Liste oder eine Anfragekampagne. [Weitere Informationen zum Verbinden von Marketo Engage-Instanzen](./admin/marketo-actions-connect.md).

![Hochrangige Datenarchitektur, die die mit Adobe Experience Platform verbundene Journey Optimizer B2B edition als Datenquelle für Konto- und Personen-Zielgruppen, eine dedizierte Marketo Engage-Instanz, die Berechtigungen und Backend-Services bereitstellt, und eine optionale Marketo Engage-Produktionsinstanz zeigt, die zum Ausführen von Journey-Aktionen verwendet wird.](./assets/high-level-data-architecture.png){zoomable="yes"}

>[!NOTE]
>
>Überprüfen Sie Ihre Lizenzberechtigungen und die entsprechende [Produktbeschreibung](https://helpx.adobe.com/de/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} auf Leistungs-Leitplanken und statische Einschränkungen.

### Abonnementmodell

Eine Experience Platform-Sandbox gepaart mit einer dedizierten Marketo Engage-Instanz definiert ein Journey Optimizer B2B edition-Abonnement. Diese dedizierte Instanz ist von Ihrer Marketo Engage-Produktionsinstanz getrennt und dient der Unterstützung von Berechtigungen und Backend-Services, anstatt Account-Journey-Daten zu speichern. [Weitere Informationen zum Setup](./setup-ultimate.md).

Experience Platform bietet eine einheitliche Datenansicht Ihrer verbundenen Marketo Engage-Instanzen und CRM-Systeme. Verwenden Sie diese einheitlichen Daten, um Ihre Journey zu erstellen und auszuführen.

### Journey-Vorgänge

Journey Optimizer B2B edition erstellt, speichert und führt Ihre Account-Journey aus. Account-Journey werden nicht in Marketo Engage angezeigt und können nur in Journey Optimizer B2B edition verwendet werden.

Eine Journey beginnt immer mit einer Audience, die Leads oder Accounts und ihre Mitarbeiter für die Journey qualifiziert. Wählen Sie diese Zielgruppe mit dem standardmäßigen Experience Platform-Zielgruppenselektor aus. Marketing-Experten implementieren den Journey, indem sie Pfade mithilfe von Konto-, Personen- oder Einkaufsgruppenkriterien aufteilen. Auf jedem Pfad senden Aktionen Nachrichten oder warten auf das Auftreten eines Ereignisses.

Nachdem Sie eine Konto-Journey erstellt haben, veröffentlichen Sie sie, um die Journey live zu schalten. Qualifizierende Accounts gelangen innerhalb von 24 Stunden auf eine veröffentlichte Journey.

### Datenfluss

Journey Optimizer B2B edition fungiert als Adobe Real-Time CDP B2B edition-Ziel. Verwenden Sie die Real-Time CDP-Kontosegmentierung, um die Konto-Zielgruppen und Personen-Zielgruppen, die Konten und Personen für eine Journey qualifizieren, zu erstellen und zu bewerten. Wenn Sie eine Journey veröffentlichen, aktiviert Journey Optimizer B2B edition die qualifizierten Zielgruppen aus Experience Platform.

Einkaufsgruppen, Einkaufsgruppenrollen und Kaufgruppenbewertungen werden in Journey Optimizer B2B edition erstellt und gespeichert. [Erfahren Sie mehr über Einkaufsgruppen](./buying-groups/buying-groups-overview.md).
