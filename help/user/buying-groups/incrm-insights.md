---
title: In-CRM-Einblicke
description: Rufen Sie Journey Optimizer B2B edition-Einkaufsgruppen direkt in Salesforce auf. Mitglieder des Vertriebsteams können Interaktionsdaten anzeigen und Verkaufschancen mit In-CRM-Insights identifizieren.
feature: Sales Insights, Buying Groups
role: User
source-git-commit: de7f5620556a48fe6f12ed1c70e925e11ec770f1
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---


# In-CRM-Einblicke

In-CRM Insights ist ein Web-basiertes Programm, das in Salesforce integriert wird und Ihnen Zugriff auf Ihre Journey Optimizer B2B edition-Einkaufsgruppen direkt in Salesforce bietet. So können Sie Möglichkeiten für ein höheres Interaktions- und Verkaufspotenzial erkennen.

Die Insights-Anwendung in CRM ist im Paket [Marketo Sales Insights verfügbar](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/marketo-sales-insight/msi-for-salesforce/installation/install-marketo-sales-insight-package-in-salesforce-appexchange).

## Berechtigungen

Um auf das Programm zugreifen zu können, müssen Benutzer über eine Mitgliedschaft in einer Rolle mit der Berechtigung **Sales Insights:View Sales Insights** verfügen.

Wenn Sie eine Benutzergruppe auf InCRM-Insights beschränken möchten, verwenden Sie die folgenden Richtlinien, um eine benutzerdefinierte Rolle speziell für InCRM-Insights zu erstellen:

* Erstellen Sie eine benutzerdefinierte Rolle nur mit dem Berechtigungssatz **Sales Insights:View Sales Insights** .
* Neue Benutzergruppe erstellen, ohne Produktprofile hinzuzufügen.
* Erstellen Sie eine weitere Benutzergruppe und fügen Sie ein AEP-Produktprofil hinzu oder fügen Sie der soeben erstellten Benutzergruppe ein vorhandenes AEP-Profil hinzu.
* Weisen Sie die neuen Benutzergruppen der neuen Rolle zu und fügen Sie neue Benutzer zu den neuen Benutzergruppen hinzu.

## Verwenden von CRM-internen Einblicken

Die In-CRM-Insights-Anwendung ist in Salesforce über den App-Starter verfügbar.

1. Klicken Sie auf den App-Starter in Salesforce.
1. Wählen Sie aus oder suchen Sie nach `Journey Optimizer B2B Edition`.
1. Melden Sie sich auf der angezeigten Registerkarte mit Ihren Adobe-Anmeldeinformationen an.
1. Wählen Sie eine Sandbox aus, die Ihre Account-Journey hostet.

Ihre Einkaufsgruppen werden geladen und sind verfügbar. Daten sind durch In-CRM-Insights schreibgeschützt.

>[!NOTE]
>
>Für den Zugriff auf In-CRM[Einblicke ist eine Mitgliedschaft in der &#x200B;](../admin/user-management.md#b2b-built-in-roles)B2B-Verkaufsbenutzer“ erforderlich.

Nachdem Sie eine Einkaufsgruppe ausgewählt haben, können Sie die [Gruppendetails](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/accounts/sales-experience/buying-group-details#) wie in Journey Optimizer B2B edition durchsuchen.
