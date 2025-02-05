---
title: Erste Schritte mit Journey Optimizer B2B edition
description: Als neue Benutzerin bzw. neuer Benutzer von Journey Optimizer B2B Edition erfahren Sie mehr über die Schlüsselbereiche für die ersten Schritte.
exl-id: 83f8e666-0b31-4323-9902-4fdf4446424c
source-git-commit: b403ff764c002796953956379e33fec6eb8c0611
workflow-type: tm+mt
source-wordcount: '664'
ht-degree: 10%

---

# Erste Schritte mit Journey Optimizer B2B edition

Welche Funktionen und Tools Sie in Adobe Journey Optimizer B2B edition angehen möchten, hängt von Ihrer Rolle in Ihrem Team ab.

Abhängig von Ihrem Unternehmen können Admins verschiedene Typen von Benutzenden definieren und ihnen je nach deren Berechtigungen Zugriff auf bestimmte Funktionen gewähren.

>[!TIP]
>
>Überprüfen Sie außerdem Ihre Lizenzberechtigungen und die entsprechende [Produktbeschreibung](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} auf Leistungs-Leitplanken und statische Einschränkungen.

>[!BEGINTABS]

>[!TAB Administrator-Schnellstart]

Bevor Ihr Team mit der Verwendung der Funktionen von Adobe Journey Optimizer B2B edition beginnen kann, sind mehrere Schritte erforderlich, um Ihre Umgebung vorzubereiten. Führen Sie diese Schritte aus, damit Datentechniker und Marketing-Fachleute mit Adobe Journey Optimizer B2B edition arbeiten können.

Als Systemadministrator müssen Sie Produktprofile verstehen und Berechtigungen für die Sandbox-Administration und Kanalkonfiguration zuweisen. Außerdem müssen Sie Sandboxes einrichten und für die verfügbaren Produktprofile verwalten. Anschließend können Sie den Produktprofilen Team-Mitglieder zuweisen. Diese Funktionen können von Produktadministratoren verwaltet werden, die Zugriff auf die Adobe Admin Console haben. [Erfahren Sie mehr über die Adobe Admin Console](https://helpx.adobe.com/de/enterprise/using/admin-console.html).

Informationen zur Zugriffsverwaltung finden Sie auf den folgenden Seiten:

1. **Erstellen Sie Sandboxes**, um Ihre Instanzen in separate, isolierte virtuelle Umgebungen zu unterteilen. [Weitere Informationen](https://experienceleague.adobe.com/en/docs/experience-platform/sandbox/home#understanding-sandboxes)

1. **Einrichten des Produktprofils**. Ein Produktprofil ist eine Reihe von Einzelrechten in Adobe Experience Platform, die Benutzenden den Zugriff auf bestimmte Funktionen oder Objekte in der Benutzeroberfläche ermöglichen. [Weitere Informationen](../admin/user-management.md#create-the-marketo-engage-product-profile)

1. **Richten Sie Benutzerberechtigungen** Produktprofile, einschließlich Sandboxes, ein und gewähren Sie Ihren Team-Mitgliedern Zugriff, indem Sie sie verschiedenen Produktprofilen zuweisen. Diese Aufgabe wird in der Admin Console ausgeführt. [Weitere Informationen](../admin/user-management.md#create-a-user-group)

1. **Konfigurieren Sie den E** Mail-Versand in Marketo Engage, damit Ihr Team E-Mail-Inhalte von den Account-Journey senden kann. [Weitere Informationen](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/setup-steps#ensure-email-deliverability)

1. **Konfigurieren von SMS-Services**. Richten Sie einen der unterstützten SMS-Drittanbieter ein, der Textnachrichten-Services unabhängig anbietet, und konfigurieren Sie die Kontoanmeldeinformationen in Adobe Journey Optimizer B2B edition. [Weitere Informationen](../admin/configure-channels-sms.md)

1. **Konfigurieren und Aktivieren der Verwendung von Adobe Experience Manager Assets** für Teams, die Assets as a Cloud Service für die zentralisierte Verwaltung digitaler Assets verwenden. [Weitere Informationen](../admin/configure-aem-repositories.md)

1. **Einrichten von Adobe Experience Platform (AEP)-Erlebnisereignisdefinitionen** für Teams, die für die Erstellung von Account-Journey verantwortlich sind und auf AEP-Erlebnisereignisse warten. [Weitere Informationen](../admin/configure-aep-events.md)

>[!TAB Marketer-Schnellstart]

Als Marketing-Experte oder _Account Journey Practitioner_ sind Sie für die Gestaltung von Journey und die Erstellung von Inhalten verantwortlich. Sie können mit Adobe Journey Optimizer B2B edition arbeiten, nachdem der Systemadministrator und der Datentechniker Ihre Umgebung vorbereitet und Ihnen Zugriff gewährt haben.

In den folgenden Abschnitten erfahren Sie, wie Sie Ihre erste Journey einrichten, Assets hinzufügen und Inhalte senden:

1. **Konto-Zielgruppen hinzufügen**. Mit Journey Optimizer B2B edition können Sie Account-Zielgruppen über Segmentdefinitionen direkt im Programm erstellen und diese in Ihren Account-Journey nutzen. [Weitere Informationen](../audiences/account-audience-overview.md)

1. **Einkaufsgruppen erstellen**. Definieren Sie die wichtigsten Komponenten, um Ihre Geschäftsziele zu erreichen, und erstellen Sie Einkaufsgruppen, die die Mitglieder für Ihre Target-Kontolisten identifizieren. [Weitere Informationen](../buying-groups/buying-groups-overview.md)

1. **Erstellen und Verwalten von Assets**. Adobe Experience Manager Assets bietet ein zentrales Repository mit Assets, die Sie Ihren Nachrichten hinzufügen können. [Weitere Informationen](../content/assets-overview.md)

1. **Personalisierte und dynamische E-Mail-Vorlagen hinzufügen**. Nutzen Sie die Personalisierungs- und Dynamic Content-Funktionen von Journey Optimizer B2B edition, um Ihre Nachricht an Ihre Audience anzupassen. [Weitere Informationen](../content/email-templates.md)

1. **Entwerfen Sie Account-Journey für personalisierte, kontextuelle Erlebnisse**. Mit Journey Optimizer B2B edition können Sie Anwendungsfälle für die Echtzeit-Orchestrierung erstellen und dabei kontextuelle Daten nutzen, die in Ereignissen oder Datenquellen gespeichert sind. Entwerfen Sie mehrstufige, erweiterte Szenarien mit den folgenden Funktionen:

   * Führen Sie einen unitären Versand in Echtzeit aus, ausgelöst durch den Empfang eines Ereignisses, oder im Batch unter Verwendung von Adobe Experience Platform-Zielgruppen.

   * Verwenden Sie kontextuelle Daten aus Ereignissen, Informationen aus Adobe Experience Platform oder Daten aus API-Services von Drittanbietern.

   * Verwenden Sie die integrierten Kanalaktionen (E-Mail und SMS) zum Senden von in Journey Optimizer B2B edition entworfenen Nachrichten.

   * Erstellen Sie im Journey-Designer Ihre mehrstufigen Anwendungsfälle, fügen Sie Bedingungen hinzu und senden Sie personalisierte Nachrichten.

[Weitere Informationen](../journeys/journey-overview.md)

>[!ENDTABS]
