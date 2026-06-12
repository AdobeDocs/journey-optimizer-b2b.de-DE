---
title: Aktivieren von Marketo Engage zur Unterstützung von Journey-Aktionen
description: Aktivieren Sie Marketo Engage-Verbindungen, um Journey-Aktionen zu unterstützen, damit Marketer Kampagnen zwischen Marketo Engage und Journey Optimizer B2B edition koordinieren können.
feature: Setup, Integrations
role: Admin
exl-id: e324a11b-1025-4850-865f-ef8886a6b2bb
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
  - id: d6e625c1-468f-4d73-9f32-fd1edb87f96b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
autotag-review: 2026-03-27T22:48:47.183Z
TQID: https://experienceleague.adobe.com/nM-Jxcj7wekzRks2xCqshOdlY7W8K0WKCXtWCNSb388
source-git-commit: 55446fa98f494b367f9f84abccebc70f59381f26
workflow-type: tm+mt
source-wordcount: 540
ht-degree: 71%

---

# Aktivieren von Marketo Engage-Verbindungen zur Unterstützung von Aktionen

Marketo Engage-Aktionen sind _personenbasierte_ Aktionen, mit denen Sie Ihre _Account-basierte_ Marketing-Orchestrierung zwischen Journey Optimizer B2B edition und Ihren _Lead-basierten_ Marketing-Maßnahmen in Marketo Engage koordinieren können. Verwenden Sie diese Aktionen, um die Mitgliedschaft in statischen Listen zu orchestrieren und Personen in Kampagnen zu platzieren.

Um Marketo Engage-Journey-Aktionen zu verwenden, erstellt ein Administrator zunächst einen [benutzerdefinierten Service](https://experienceleague.adobe.com/de/docs/marketo-developer/marketo/rest/custom-services){target="_blank"} in Marketo Engage, der die für die Authentifizierung erforderlichen Anmeldeinformationen bereitstellt. Anschließend verwendet ein Produktadministrator für Journey Optimizer B2B edition die Anmeldeinformationen, um eine Verbindung zu Marketo Engage herzustellen. Benutzerinnen und Benutzer von Journey Optimizer B2B edition können dann auf die Verbindung verweisen, um Marketo Engage-Aktionen in Personen- und Account-Journey zu konfigurieren:

* [!UICONTROL Zu Marketo-Liste hinzufügen]
* [!UICONTROL Aus Marketo-Liste entfernen]
* [!UICONTROL Zu Marketo-Anfragekampagne hinzufügen]

## Konfigurieren einer Marketo Engage-Verbindung {#external-marketo-configure}

>[!CONTEXTUALHELP]
>id="ajo-b2b_marketo-configure-connections"
>title="Externe Marketo Engage-Verbindungen"
>abstract="Produkt-Admins können Verbindungen zu externen Marketo Engage-Instanzen konfigurieren, wodurch diese für Journey-Aktionen verfügbar werden."

Führen Sie die folgenden Schritte aus, um eine externe Marketo Engage-Instanz für die Verwendung mit Journey-Aktionen zu konfigurieren.

### Erstellen des benutzerdefinierten Marketo Engage-Service

1. Melden Sie sich bei Marketo Engage als Administrator an und [&#x200B; Sie einen benutzerdefinierten Service &#x200B;](https://experienceleague.adobe.com/de/docs/marketo/using/product-docs/administration/additional-integrations/create-a-custom-service-for-use-with-rest-api){target="_blank"}.
1. Kopieren Sie die folgenden Werte, die für die Journey Optimizer B2B edition-Verbindung verwendet werden sollen:

   * Munchkin-ID
   * Client-ID
   * Client-Geheimnis

Die [Rollenberechtigungen, die im benutzerdefinierten Service zugewiesen &#x200B;](https://experienceleague.adobe.com/de/docs/marketo-developer/marketo/rest/custom-services#permission-list){target="_blank"}, steuern die Sichtbarkeit von Marketo Engage Workspace für Assets wie Listen und Kampagnen. Marketer können dieselbe Verbindung mehrmals innerhalb einer Journey und verschiedene Marketo Engage-Verbindungen innerhalb derselben Journey verwenden.

### Integration hinzufügen

![Integrationsdetails hinzufügen](assets/integration-connection-details.png){width="800" zoomable="yes"}

1. Navigieren Sie in Journey Optimizer B2B edition zu **[!UICONTROL Administration]** > **[!UICONTROL Konfigurationen]**.
1. Wählen Sie die **[!UICONTROL Integrationen]** aus.
1. Klicken Sie **[!UICONTROL Verbindung erstellen]**.
1. Geben Sie **[!UICONTROL Name]** (erforderlich) und **[!UICONTROL Beschreibung]** (optional) ein.
1. Wählen Sie die Aktualisierungsrichtlinie aus, die zum Anwenden einer Aktion auf einen entsprechenden Personendatensatz verwendet wird.

   Wenn eine Aktion für die verbundene Marketo Engage-Instanz ausgeführt wird, bestimmt die ausgewählte _Aktualisierungsrichtlinie_ die Personendatensätze in Marketo Engage, um auszuwählen, ob mehrere Kennungen im einheitlichen Personenprofil vorhanden sind.

   * **[!UICONTROL Aktualisieren aller übereinstimmenden Datensätze]**
   * **[!UICONTROL Nur den ältesten übereinstimmenden Datensatz aktualisieren]**
   * **[!UICONTROL Nur den neuesten übereinstimmenden Datensatz aktualisieren]**

   >[!NOTE]
   >
   >Eine Person/ein Lead durchläuft die Journey unabhängig von einer Übereinstimmung, es sei denn, ein Fehler tritt auf. Eine Journey-Aktion erstellt in Marketo Engage keinen neuen Personendatensatz, wenn kein übereinstimmender Datensatz vorhanden ist.

1. Geben Sie die Munchkin-ID, die Client-ID und den geheimen Client-Schlüssel für den Service ein, der in der externen Marketo Engage-Instanz erstellt wurde.
1. Klicken Sie **[!UICONTROL Mit Marketo verbinden]**.
1. Klicken Sie auf **[!UICONTROL Erstellen]**.

## Verbindung in einer Journey-Aktion verwenden

Wenn ein Marketer eine Marketo Engage-Aktion auf einer Journey verwendet, konfiguriert er den Knoten mithilfe des Verbindungsnamens.

>[!NOTE]
>
>Von einer Journey ausgeführte Marketo Engage-Aktionen gelten nicht für die REST-API-Beschränkungen für die verbundene Marketo Engage-Instanz.

Nach abgeschlossener Integration sind Marketo Engage-Aktionen unter **_Actions in den:_** verfügbar.

![Marketo-Aktionsliste](assets/marketo-actions-list.png){width="800" zoomable="yes"}
