---
title: Erste Schritte mit Journey Optimizer B2B Edition
description: Als neuer Anwender in Journey Optimizer B2B Edition erfahren Sie mehr über die Schlüsselbereiche für die ersten Schritte.
exl-id: 83f8e666-0b31-4323-9902-4fdf4446424c
source-git-commit: 7103e4f6666482a72511661dfaed1392d4eb16b1
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 8%

---

# Erste Schritte mit Journey Optimizer B2B Edition

Die Funktionen und Tools, die Sie in Adobe Journey Optimizer B2B Edition einsetzen möchten, hängen von Ihrer Teamrolle ab.

Je nach Organisation können Administratoren verschiedene Arten von Benutzern definieren und ihnen je nach Berechtigung Zugriff auf bestimmte Funktionen gewähren.

>[!BEGINTABS]

>[!TAB Schnellstart für Administratoren]

Bevor Ihr Team mit der Verwendung der Adobe Journey Optimizer B2B Edition-Funktionen beginnen kann, sind einige Schritte erforderlich, um Ihre Umgebung vorzubereiten. Führen Sie diese Schritte aus, damit der Dateningenieur und Marketing-Experte mit der Adobe Journey Optimizer B2B Edition arbeiten können.

Als Systemadministrator müssen Sie sich mit Produktprofilen vertraut machen und Berechtigungen für die Sandbox-Verwaltung und Kanalkonfiguration zuweisen. Außerdem müssen Sie Sandboxes einrichten und für die verfügbaren Produktprofile verwalten. Anschließend können Sie den Produktprofilen Team-Mitglieder zuweisen. Diese Funktionen können von Produktadministratoren verwaltet werden, die Zugriff auf die Adobe Admin Console haben. [Erfahren Sie mehr über die Adobe Admin Console](https://helpx.adobe.com/de/enterprise/using/admin-console.html).

Informationen zur Zugriffsverwaltung finden Sie auf den folgenden Seiten:

1. **Erstellen Sie Sandboxes**, um Ihre Instanzen in separate, isolierte virtuelle Umgebungen zu unterteilen. [Weitere Informationen](https://experienceleague.adobe.com/en/docs/experience-platform/sandbox/home#understanding-sandboxes)

1. **Einrichten des Produktprofils**. Ein Produktprofil ist ein Satz von Einzelrechten in Adobe Experience Platform, die Benutzern den Zugriff auf bestimmte Funktionen oder Objekte in der Benutzeroberfläche ermöglichen. [Weitere Informationen](../admin/user-management.md#create-the-marketo-engage-product-profile)

1. **Richten Sie Benutzerberechtigungen ein** für Produktprofile, einschließlich Sandboxes, und gewähren Sie Zugriff auf Ihre Team-Mitglieder, indem Sie sie verschiedenen Produktprofilen zuweisen. Diese Aufgabe wird in der Admin Console ausgeführt. [Weitere Informationen](../admin/user-management.md#create-a-user-group)

1. **E-Mail-Versand konfigurieren** in Marketo Engage, wodurch Ihr Team E-Mail-Inhalte von Account-Journey senden kann. [Weitere Informationen](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/setup-steps#ensure-email-deliverability)

1. **SMS-Dienste konfigurieren**. Richten Sie einen der unterstützten Drittanbieter für SMS ein, der unabhängig Textnachrichten anbietet, und konfigurieren Sie die Kontoanmeldeinformationen in Adobe Journey Optimizer B2B Edition. [Weitere Informationen](../content/sms-authoring.md#create-a-new-api-credentials-for-an-sms-service-provider)

1. **Konfigurieren und aktivieren Sie die Verwendung von Adobe Experience Manager Assets** für Teams, die Assets als c-Cloud Service für die zentralisierte Verwaltung digitaler Assets verwenden. [Weitere Informationen](../admin/configure-aem-repositories.md)

>[!TAB Schnellstart für Marketingexperten]

Als Marketer oder _Account Journey Practitioner_ sind Sie für die Erstellung von Journey und die Erstellung von Inhalten verantwortlich. Sie können mit Adobe Journey Optimizer B2B Edition arbeiten, nachdem der Systemadministrator und der Data Engineer Ihre Umgebung vorbereitet und Ihnen Zugriff gewährt haben.

In den folgenden Abschnitten finden Sie Informationen zum Einrichten Ihrer ersten Journey, Hinzufügen von Assets und Senden von Inhalten:

1. **Fügen Sie Kontozielgruppen hinzu**. Mit der Journey Optimizer B2B Edition können Sie Kontozielgruppen durch Segmentdefinitionen direkt aus der Anwendung erstellen und in Ihren Konto-Journey nutzen. [Weitere Informationen](../audiences/account-audience-overview.md)

1. **Erstellen Sie Kaufgruppen**. Definieren Sie die Schlüsselkomponenten für die Erreichung Ihrer Geschäftsziele und erstellen Sie Kaufgruppen, die die Mitglieder für Ihre Zielkontolisten identifizieren. [Weitere Informationen](../buying-groups/buying-groups-overview.md)

1. **Erstellen und Verwalten von Assets**. Adobe Experience Manager Assets bietet ein zentrales Asset-Repository, mit dem Sie Ihre Nachrichten ausfüllen können. [Weitere Informationen](../content/assets-overview.md)

1. **Fügen Sie personalisierte und dynamische E-Mail-Vorlagen hinzu**. Nutzen Sie Personalisierungs- und dynamische Inhaltsfunktionen von Journey Optimizer B2B Edition, um Ihre Nachricht an Ihre Audience anzupassen. [Weitere Informationen](../content/email-templates.md)

1. **Design-Konto-Journey zur Bereitstellung personalisierter, kontextbezogener Erlebnisse**. Mit der Journey Optimizer B2B Edition können Sie Anwendungsfälle für die Echtzeit-Orchestrierung der Customer Journey mit Kontextdaten erstellen, die in Ereignissen oder Datenquellen gespeichert sind. Erstellen Sie mehrstufige, erweiterte Szenarien mit folgenden Funktionen:

   * Senden Sie einen einmaligen Echtzeit-Versand, der beim Empfang eines Ereignisses ausgelöst wird, oder einen Batch-Vorgang mit Adobe Experience Platform-Zielgruppen.

   * Verwenden Sie Kontextdaten aus Ereignissen, Informationen aus Adobe Experience Platform oder Daten aus API-Diensten von Drittanbietern.

   * Verwenden Sie die integrierten Kanalaktionen (E-Mail und SMS), um Nachrichten zu senden, die in Journey Optimizer B2B Edition entwickelt wurden.

   * Erstellen Sie im Journey Designer Ihre mehrstufigen Anwendungsfälle, fügen Sie Bedingungen hinzu und senden Sie personalisierte Nachrichten.

[Weitere Informationen](../journeys/journey-overview.md)

>[!ENDTABS]
