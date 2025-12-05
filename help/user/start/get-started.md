---
title: Anleitung zum Onboarding für Admins und Marketing-Fachleute
description: 'Onboarding-Handbuch für Admins und Marketing-Fachleute: Einrichten von Sandboxes, Konfigurieren von Kanälen, Erstellen von Käufergruppen und Entwerfen von Konto-Journey in Journey Optimizer B2B Edition.'
role: Admin, User
level: Beginner
exl-id: 83f8e666-0b31-4323-9902-4fdf4446424c
source-git-commit: 32b36690e76a4920a87bdd6c2fff85158c22d0e7
workflow-type: tm+mt
source-wordcount: '739'
ht-degree: 93%

---

# Anleitung zum Onboarding

Welche Funktionen und Tools Sie in Adobe Journey Optimizer B2B Edition verwenden, hängt von Ihrer Rolle in Ihrem Team ab. Abhängig von Ihrer Organisation können Admins verschiedene Typen von Benutzenden definieren und ihnen je nach deren Berechtigungen Zugriff auf bestimmte Funktionen gewähren.

>[!TIP]
>
>Überprüfen Sie Ihre Lizenzberechtigungen und die entsprechende [Produktbeschreibung](https://helpx.adobe.com/de/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} auf Leitlinien für die Leistung und statische Einschränkungen.

>[!BEGINTABS]

>[!TAB Admin]

Bevor Ihr Team die Funktionen von Adobe Journey Optimizer B2B Edition verwenden kann, sind mehrere Schritte erforderlich, um Ihre Umgebung vorzubereiten. Führen Sie diese Schritte aus, damit Data Engineering und Marketing mit Adobe Journey Optimizer B2B Edition arbeiten können.

Als Systemadmin müssen Sie Produktprofile verstehen und Berechtigungen für die Sandbox-Administration und Kanalkonfiguration zuweisen. Außerdem müssen Sie Sandboxes einrichten und entsprechend den verfügbaren Produktprofilen verwalten. Anschließend können Sie den Produktprofilen Team-Mitglieder zuweisen. Produktadmins mit Zugriff auf die Adobe Admin Console können diese Funktionen verwalten. [Erfahren Sie mehr über die Adobe Admin Console](https://helpx.adobe.com/de/enterprise/using/admin-console.html).

Informationen zur Zugriffsverwaltung finden Sie auf den folgenden Seiten:

1. **Erstellen Sie Sandboxes**, um Ihre Instanzen in separate, isolierte virtuelle Umgebungen zu unterteilen. [Weitere Informationen](https://experienceleague.adobe.com/de/docs/experience-platform/sandbox/home#understanding-sandboxes){target="_blank"}

1. **Arbeiten Sie mit Ihrem Data Engineering zusammen**, um Ihre B2B-Zielgruppe und Profilaktivierung zu planen und zu implementieren. Überprüfen Sie die veröffentlichten Blueprints und befolgen Sie die Richtlinien entsprechend Ihren Anforderungen. [Weitere Informationen](https://experienceleague.adobe.com/de/docs/blueprints-learn/architecture/b2b-activation/overview){target="_blank"}

1. **Planen und implementieren Sie die Marketo Engage** Integrationen, um benutzerdefinierte Schemata, die Aufnahme von Profilen und Konten und die Orchestrierung personalisierter Journey für Einkaufsgruppen einzubinden. [Weitere Informationen](https://experienceleague.adobe.com/de/docs/blueprints-learn/architecture/b2b-activation/b2b-journeys-with-marketo){target="_blank"}

1. **Richten Sie das Produktprofil ein**. Bei einem Produktprofil handelt es sich um eine Reihe von Einzelberechtigungen in Adobe Experience Platform, die Benutzenden den Zugriff auf bestimmte Funktionen oder Objekte in der Benutzeroberfläche ermöglichen. [Weitere Informationen](../admin/user-management.md#create-the-marketo-engage-product-profile)

1. **Richten Sie Benutzerberechtigungen für Produktprofile ein**, einschließlich Sandboxes, und gewähren Sie Ihren Team-Mitgliedern Zugriff, indem Sie sie verschiedenen Produktprofilen zuweisen. Diese Aufgabe wird in der Admin Console durchgeführt. [Weitere Informationen](../admin/user-management.md#create-a-user-group)

1. **Konfigurieren von XDM-Klassen und -**, um die Daten zu steuern, die für die Journey-Orchestrierung und die Inhaltspersonalisierung in Journey Optimizer B2B edition verfügbar sind. [Weitere Informationen](../admin/xdm-field-management.md)

1. **Konfigurieren Sie den E-Mail-Versand** in Marketo Engage, damit Ihr Team E-Mail-Inhalte von Konto-Journeys senden kann. [Weitere Informationen](../admin/configure-channels-emails.md){target="_blank"}

1. **Konfigurieren Sie SMS-Dienste**. Richten Sie einen der unterstützten SMS-Drittanbieter ein, der Textnachrichten-Dienste unabhängig anbietet, und konfigurieren Sie die Kontoanmeldeinformationen in Adobe Journey Optimizer B2B Edition. [Weitere Informationen](../admin/configure-channels-sms.md)

1. **Konfigurieren und aktivieren Sie die Verwendung von Adobe Experience Manager Assets** für Teams, die Assets as a Cloud Service zur zentralen Verwaltung digitaler Assets einsetzen. [Weitere Informationen](../admin/configure-aem-repositories.md)

1. **Richten Sie Erlebnisereignis-Definitionen für Adobe Experience Platform (AEP) ein**, und zwar für Teams, die für die Erstellung von Konto-Journeys zuständig sind, die auf AEP-Erlebnisereignisse lauschen. [Weitere Informationen](../admin/configure-aep-events.md)

>[!TAB Marketing-Fachkraft]

Als Marketing-Fachkraft oder als _Person, die Konto-Journeys nutzt_, sind Sie für die Gestaltung von Journeys und die Erstellung von Inhalten verantwortlich. Sie können mit Adobe Journey Optimizer B2B Edition arbeiten, nachdem die Systemadministration und das Data Engineering Ihre Umgebung vorbereitet und Ihnen Zugriff gewährt haben.

Anhand der folgenden Abschnitte können Sie Ihre erste Journey einrichten, Assets hinzufügen und Inhalte senden:

1. **Fügen Sie Kontozielgruppen hinzu**. Mit Journey Optimizer B2B Edition können Sie Kontozielgruppen durch Segmentdefinitionen direkt über die Anwendung erstellen und in Ihren Konto-Journeys nutzen. [Weitere Informationen](../audiences/account-audience-overview.md)

1. **Erstellen Sie Käufergruppen**. Definieren Sie die wichtigsten Komponenten, um Ihre Geschäftsziele zu erreichen, und erstellen Sie Käufergruppen, die die Mitglieder für Ihre Zielkontolisten identifizieren. [Weitere Informationen](../buying-groups/buying-groups-overview.md)

1. **Erstellen und verwalten Sie Assets**. Adobe Experience Manager Assets bietet ein zentrales Repository mit Assets, die Sie für Ihre Nachrichten verwenden können. [Weitere Informationen](../content/assets-overview.md)

1. **Fügen Sie personalisierte und dynamische E-Mail-Vorlagen hinzu**. Nutzen Sie die Journey Optimizer B2B Editio-Funktionen für Personalisierung und dynamische Inhalte, um Nachrichten an Ihre Zielgruppen anzupassen. [Weitere Informationen](../content/email-templates.md)

1. **Entwerfen Sie Konto-Journeys, um personalisierte, kontextuelle Erlebnisse bereitzustellen**. Mit Journey Optimizer B2B Edition können Sie anhand von in Ereignissen oder Datenquellen gespeicherten kontextuellen Daten Echtzeit-Orchestrierungsfälle erstellen. Erstellen Sie mehrstufige fortgeschrittene Szenarien mit den folgenden Funktionen:

   * Führen Sie einen unitären Versand in Echtzeit aus, ausgelöst durch den Empfang eines Ereignisses, oder als Batch unter Verwendung von Adobe Experience Platform-Zielgruppen.

   * Nutzen Sie kontextuelle Daten aus Ereignissen, Informationen aus Adobe Experience Platform oder Daten aus API-Services von Drittanbietern.

   * Verwenden Sie die integrierten Kanalaktionen (E-Mail und SMS) zum Senden von in Journey Optimizer B2B Edition entworfenen Nachrichten.

   * Erstellen Sie in der Journey Map mehrstufigen Anwendungsfälle, fügen Sie Bedingungen hinzu und senden Sie personalisierte Nachrichten.

[Weitere Informationen](../journeys/journey-overview.md)

>[!ENDTABS]
