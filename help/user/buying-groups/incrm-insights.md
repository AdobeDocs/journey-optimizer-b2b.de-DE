---
title: In-CRM-Einblicke
description: Greifen Sie auf Journey Optimizer B2B edition-Einkaufsgruppen direkt in CRMs zu. Mitglieder des Vertriebsteams können Interaktionsdaten anzeigen und Verkaufschancen mit In-CRM-Insights identifizieren.
feature: Sales Insights, Buying Groups
role: User
exl-id: c55a1fce-2ddc-481b-9f60-5e67a4bf9633
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: afadf741-c5fe-42cd-8013-23bb6ff2d1bc
  - id: fc1ff3b2-6614-41ad-a113-de48597598fd
  - id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
subfeature_v2:
  - id: fe583b80-65a2-48c2-b4e1-9ea8fbac0a8a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
autotag-review: '2026-03-30T21:40:22.011Z'
source-git-commit: ff337a5f215daee1ea6dbe8d6b643087ac3324e2
workflow-type: tm+mt
source-wordcount: 483
ht-degree: 2%

---

# In-CRM-Einblicke

[!DNL In-CRM Insights] ist ein Web-basiertes Programm, das in Salesforce und Microsoft Dynamics 365 integriert ist und Ihnen Zugriff auf [!DNL Journey Optimizer B2B Edition] Einkaufsgruppen direkt in Ihrem CRM bietet. Es führt Vertriebsdatenquellen zusammen und erleichtert so die Identifizierung von Möglichkeiten für mehr Interaktion und Verkaufspotenzial.

## Installation

Der Installationsprozess umfasst Folgendes:

* Einrichten von Benutzerberechtigungen und Gruppen
* Installieren des Softwarepakets
* Anmeldung über Ihr CRM

### Berechtigungen festlegen

Benutzer, die die Software installieren, müssen über Berechtigungen zum Installieren von Salesforce-Paketen verfügen.

Um auf das Programm zugreifen zu können, müssen Benutzer über eine Mitgliedschaft in einer Rolle mit der Berechtigung **Sales Insights:View Sales Insights** verfügen.

Wenn Sie Benutzerinnen und Benutzer auf [!DNL In-CRM Insights] beschränken möchten:

1. Erstellen Sie eine [benutzerdefinierte Rolle](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/accounts/buying-groups/default-custom-roles#create-a-custom-role) und weisen Sie ihr die Berechtigung **Verkaufseinblicke: Verkaufseinblicke anzeigen** zu.
1. Erstellen Sie eine neue [Benutzergruppe](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/user-management#create-user-group).
1. Fügen Sie der Gruppe ein Experience Platform-Produktprofil hinzu.

### Installieren des Pakets

Um das In-CRM-Insights-Paket zu installieren, führen Sie die Schritte für Salesforce oder Microsoft Dynamics aus.

#### Salesforce

1. Laden Sie das [In-CRM Insights-Installationspaket) &#x200B;](https://experience.adobe.com/solutions/OneAdobe-sales-workflow-optimizer-sales-insight-ui/install/sales-insight?crm=salesforce).
1. Nach der Anmeldung werden Sie zur Seite für die Paketinstallation weitergeleitet.
1. Wählen Sie die Option **[!UICONTROL Für alle Benutzer installieren]** und klicken Sie auf **[!UICONTROL Installieren]**.

   ![Installieren des In-CRM Insights-Pakets](assets/incrm-install-sf.png){width=500}

1. Genehmigen Sie den Zugriff von Drittanbietern im Dialogfeld und klicken Sie dann auf **[!UICONTROL Weiter]**.
1. Klicken Sie nach Abschluss der Installation auf **[!UICONTROL Fertig]**.

   Sie wird jetzt auf der Seite **Installierte Pakete** und **Journey Optimizer B2B edition** wird im App-Starter aufgeführt.

   ![In-CRM-Insights in Salesforce eingerichtet](assets/in-crm-install-sf-done.png){width=800 zoomable="yes"}

#### MS Dynamics

1. Laden Sie das [In-CRM Insights-Installationspaket) &#x200B;](https://experience.adobe.com/solutions/OneAdobe-sales-workflow-optimizer-sales-insight-ui/install/sales-insight?crm=dynamics).
1. Gehen Sie zum [Power Apps-Portal](https://make.powerapps.com/){target=_blank}.
1. Wählen Sie nach der Anmeldung die Umgebung für das Paket aus und navigieren Sie dann **Menü links zu** Lösungen“.
1. Klicken Sie **[!UICONTROL Lösung importieren]**.
1. Navigieren Sie zum Installationspaket, laden Sie es hoch und klicken Sie dann auf **[!UICONTROL Weiter]**.
1. Überprüfen Sie die Paketdetails und klicken Sie auf **[!UICONTROL Weiter]**.
1. Überprüfen _unter &quot;_&quot;, ob der Wert auf `prod` festgelegt ist (ändern Sie den Wert nicht), und klicken Sie auf **[!UICONTROL Importieren]**.
1. Nach Abschluss der Installation wird **[!UICONTROL Journey Optimizer B2B edition]** > **[!UICONTROL Einkaufsgruppen]** in der linken Navigationsleiste angezeigt.

   ![In-CRM-Insights in Microsoft Dynamics verfügbar](assets/incrm-ms-install-done.png){width=800 zoomable="yes"}

## Anzeigen Ihrer Einkaufsgruppen

Befolgen Sie die Anweisungen, um sich bei Ihrem Adobe-Konto anzumelden. Ihre Einkaufsgruppen werden geladen und können angezeigt werden.

Nachdem Sie eine Einkaufsgruppe ausgewählt haben, können Sie die [Gruppendetails“ &#x200B;](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/accounts/sales-experience/buying-group-details#). Dies entspricht den in Journey Optimizer B2B edition angezeigten Daten und Erkenntnissen, die Daten sind jedoch über [!DNL In-CRM Insights] schreibgeschützt.
