---
title: Aktivieren von Marketo Engage zur Unterstützung von Journey-Aktionen
description: Aktivieren Sie Marketo Engage-Verbindungen, um Journey-Aktionen zu unterstützen, damit Marketer Kampagnen zwischen Marketo Engage und Journey Optimizer B2B edition koordinieren können.
feature: Integrations, Audiences, Buying Groups
role: User, Admin
source-git-commit: 9b77570ddb9b416251f38db51a57507a935a526a
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 1%

---


# Aktivieren von Marketo Engage-Instanzen zur Unterstützung von Aktionen

Marketo Engage-Aktionen sind _personenbasierte_ Aktionen, mit denen Sie Ihre _Account-basierte_ Marketing-Orchestrierung zwischen Journey Optimizer B2B edition und Ihren _Lead-basierten_ Marketing-Maßnahmen in Marketo Engage koordinieren können. Verwenden Sie diese Aktionen, um die Mitgliedschaft in statischen Listen zu orchestrieren und Personen in Kampagnen zu platzieren.

Um Marketo Engage-Journey-Aktionen zu verwenden, erstellt ein Administrator zunächst einen [benutzerdefinierten Service](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/rest/custom-services){target="_blank"} in Marketo Engage, der die für die Authentifizierung erforderlichen Anmeldeinformationen bereitstellt. Anschließend verwendet ein Produktadministrator für Journey Optimizer B2B edition die Anmeldeinformationen, um eine Verbindung zu Marketo Engage herzustellen. Journey Optimizer B2B edition-Benutzer können dann auf die Verbindung verweisen, um Marketo Engage-Aktionen in <!-- person and -->Account-Journey zu konfigurieren, z. B. Personen zu Marketo Engage-Listen hinzuzufügen oder daraus zu entfernen oder sie zu Anfragekampagnen hinzuzufügen.

## Konfigurieren einer Marketo Engage-Verbindung {#external-marketo-configure}

>[!CONTEXTUALHELP]
>id="ajo-b2b_marketo-configure-connections"
>title="Externe Marketo Engage-Verbindungen"
>abstract="Produktadministratoren können Verbindungen zu externen Marketo Engage-Instanzen konfigurieren, wodurch sie für Journey-Aktionen verfügbar sind."

Führen Sie die folgenden Schritte aus, um eine externe Marketo Engage-Instanz für die Verwendung mit Journey-Aktionen zu konfigurieren.

### Erstellen des benutzerdefinierten Marketo Engage-Service

1. Melden Sie sich bei Marketo Engage als Administrator an und [&#x200B; Sie einen benutzerdefinierten Service &#x200B;](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/additional-integrations/create-a-custom-service-for-use-with-rest-api){target="_blank"}.
1. Kopieren Sie die folgenden Werte, die für die Journey Optimizer B2B edition-Verbindung verwendet werden sollen:

   * Munchkin-ID
   * Client-ID
   * Client-Geheimnis

Die Sichtbarkeit von Marketo Engage Workspace für Assets wie Listen und Kampagnen wird durch die [Rollenberechtigungen, die im benutzerdefinierten Service zugewiesen sind“ &#x200B;](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/rest/custom-services#permission-list){target="_blank"}. Marketer können dieselbe Verbindung mehrmals innerhalb einer Journey und verschiedene Marketo Engage-Verbindungen innerhalb derselben Journey verwenden.

### Integration hinzufügen

![Integrationsdetails hinzufügen](assets/integration-connection-details.png){width="800" zoomable="yes"}

1. Navigieren Sie in Journey Optimizer B2B edition zu **[!UICONTROL Administration]** > **[!UICONTROL Konfigurationen]**.
1. Wählen Sie auf der Registerkarte **[!UICONTROL Integrationen]** aus.
1. Klicken Sie **[!UICONTROL Verbindung erstellen]**.
1. Geben Sie **[!UICONTROL Name]** (erforderlich) und **[!UICONTROL Beschreibung]** (optional) ein.
1. Wählen Sie die Aktualisierungsrichtlinie aus, die zum Anwenden einer Aktion auf einen passenden Personendatensatz verwendet wird.

   Wenn eine Aktion für die verbundene Marketo Engage-Instanz ausgeführt wird, bestimmt die ausgewählte _Aktualisierungsrichtlinie_ die Personendatensätze in Marketo Engage, um auszuwählen, ob mehrere Kennungen im einheitlichen Personenprofil vorhanden sind.

   * **[!UICONTROL Aktualisieren aller übereinstimmenden Datensätze]**
   * **[!UICONTROL Nur den ältesten übereinstimmenden Datensatz aktualisieren]**
   * **[!UICONTROL Nur den neuesten übereinstimmenden Datensatz aktualisieren]**

   >[!NOTE]
   >
   >Personen durchlaufen die Journey unabhängig von einer Übereinstimmung, es sei denn, es tritt ein Fehler auf.

1. Geben Sie die Munchkin-ID, die Client-ID und den geheimen Client-Schlüssel für den Service ein, der in der externen Marketo Engage-Instanz erstellt wurde.
1. Klicken Sie **[!UICONTROL Mit Marketo verbinden]**.
1. Klicken Sie auf **[!UICONTROL Erstellen]**.

## Verbindung in einer Journey-Aktion verwenden

Wenn ein Marketer eine Marketo Engage-Aktion auf einer Journey verwendet, kann er den Knoten mithilfe des Verbindungsnamens konfigurieren.

Nach abgeschlossener Integration sind Marketo Engage-Aktionen unter **Aktionen auf:** in den Knoteneigenschaften verfügbar.

![Marketo-Aktionsliste](assets/marketo-actions-list.png){width="800" zoomable="yes"}