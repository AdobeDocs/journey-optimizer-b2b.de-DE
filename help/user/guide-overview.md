---
title: Dokumentation zu Adobe Journey Optimizer B2B Edition
description: 'Vollständige Dokumentation für Journey Optimizer B2B Edition: Erkunden Sie die verfügbaren Ressourcen für das Onboarding, die Erstellung von Käufergruppen, die Einrichtung von Konto-Journeys und die Verwaltung von Content.'
exl-id: 3d7b6c82-95c3-4d89-b3dc-7fd5b0aef615
autotag-review: 2026-03-27T22:18:45.397Z
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: f467931a-9b22-4ca8-869f-adfbd64061ce
    internal-label: Onboarding
TQID: https://experienceleague.adobe.com/BK-uFYGIZyqRNy4Gx-vJB-oy3q8zpjERIoJwBvgofUY
source-git-commit: ce5504e7a539c38b489fddc103358029edf1cfba
workflow-type: tm+mt
source-wordcount: '1123'
ht-degree: 26%
---
# Dokumentation zu Adobe Journey Optimizer B2B Edition

[!DNL Adobe Journey Optimizer B2B Edition] ist eine erstklassige Anwendung, mit der Marketing- und Vertriebsteams Account-basierte Erlebnisse orchestrieren und Einkaufsgruppen für bestimmte Produkte über den gesamten Kundenlebenszyklus hinweg qualifizieren können. Es verwendet KI, um Einkaufsgruppen innerhalb von Zielkonten anzusprechen und zu qualifizieren, sodass Ihre Teams eine Pipeline mit höherer Qualität generieren und bessere Akquise-, Expansions- und Aufbewahrungsstrategien entwerfen können. Darüber hinaus ermöglicht es gemeinsame Einblicke durch Vertriebs- und Marketing-Teams.

Diese Dokumentation enthält Informationen zur Verwaltung der Anwendung. Es wurde für Marketing-Experten, Vertreter der Geschäftsentwicklung, Datenanalysten und operative Administratoren entwickelt.

## Neue Funktionen

Sehen Sie sich dieses Sampling der neuesten Ergänzungen und Verbesserungen in der [!DNL Journey Optimizer B2B Edition]-Anwendung und -Dokumentation an.

>[!BEGINTABS]

>[!TAB Personen-Journey ]

Orchestrieren Sie Lead-basiertes Marketing mit Personen-Journeys, die [!DNL Adobe Experience Platform] Zielgruppen und Daten verwenden, um einzelne Personen zu interagieren. Personen-Journey unterstützen jetzt _Abhören eines Ereignisses_, externe Aktionen und externe Aufspaltungsknoten sowie den erneuten Eintritt von Journey. Verwenden Sie sie zusammen mit Account Journey und Buying Groups, um die vollständige Buying Journey zu orchestrieren.

[!BADGE Weitere Informationen]{type=Informative url="/help/user/journeys/journeys-overview.md" tooltip="Informationen zu Personen-Journey"}

>[!TAB Aufspaltungspfade der Variante]

Testen Sie Varianten innerhalb eines Accounts oder Personen-Journey, indem Sie basierend auf von Ihnen definierten Prozentsätzen Konten oder Personen unterschiedlichen Journey-Pfaden zuweisen. In Personen-Journey ist die Zuordnung deterministisch, sodass jede Person immer denselben Weg verfolgt, was gesteuerte Experimente unterstützt.

[!BADGE Weitere Informationen]{type=Informative url="/help/user/journeys/variant-split-paths-nodes.md" tooltip="Informationen zu Aufspaltungspfaden für Varianten"}

>[!TAB WhatsApp-Kanal]

Wenn Entwickelnde und Produktadministratoren eine Integration mit einem Meta Business Manager-Konto konfigurieren, können Marketing-Experten WhatsApp-Nachrichten mithilfe der Meta Cloud-API als Inhaltskanal in Account-Journey aufnehmen. WhatsApp verbindet E-Mail und SMS als verfügbaren Kanal für die direkte Bereitstellung von Journey-Inhalten an Account-Mitglieder.

[!BADGE Weitere Informationen]{type=Informative url="/help/user/admin/configure-channels-whatsapp.md" tooltip="Informationen zum WhatsApp-Kanal"}

>[!TAB Generative KI-Modelle]

E-Mail-Designer können jetzt aus standardmäßigen [!DNL Firefly], benutzerdefinierten [!DNL Firefly], die für markenspezifische Assets trainiert wurden, und genehmigten Bildmodellen von Drittanbietern auswählen, wenn sie Bilder für E-Mail-Inhalte generieren. Diese Auswahl gibt Teams die Kontrolle darüber, welches Modell zu ihrem spezifischen Design-Szenario passt, von allgemeinen Inhaltsanforderungen bis hin zu markenspezifischen oder spezialisierten Anwendungsfällen.

[!BADGE Weitere Informationen]{type=Informative url="/help/user/content/generative-ai-models.md" tooltip="Erfahren Sie mehr über die Auswahl des Modells für generative KI"}

>[!TAB Versandzeitoptimierung]

Für Aktionsknoten _E-Mail senden_ in Personen-Journeys können Sie jetzt die Sendezeitoptimierung verwenden, um den Zeitpunkt des E-Mail-Versands zu personalisieren. Das System sagt voraus, wann jede Person mit der größten Wahrscheinlichkeit interagiert, und plant den Versand entsprechend, anstatt ihn an alle Empfänger gleichzeitig zu senden.

[!BADGE Weitere Informationen]{type=Informative url="/help/user/content/email-send-time-optimization.md" tooltip="Informationen zur Optimierung des Versandzeitpunkts"}

>[!TAB Erneute Eingabe von Journey]

Sie können jetzt Konten oder Personen über ein Konto oder Personen-Journey mehrmals senden. Der Wiedereinstieg betrifft mehrere Szenarien, z. B. die Neubewertung von Qualifikationskriterien und wiederverwendbare Nurture-Workflows. Verwenden Sie die Einstellungen für den erneuten Eintritt, um Kriterien, Beschränkungen und Wartezeiten festzulegen, damit sich Accounts oder Personen kontrolliert für den Journey qualifizieren.

[!BADGE Weitere Informationen]{type=Informative url="/help/user/journeys/journey-re-entry.md" tooltip="Informationen zum erneuten Eintreten von Journey"}

>[!ENDTABS]

## Exploring starten {#section-explore}

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=de)

Neueste Versionshinweise

Bleiben Sie mit den neuesten Versionshinweisen, neuen Funktionen und Verbesserungen in [!DNL Adobe Journey Optimizer B2B Edition] auf dem Laufenden.

[Versionshinweise anzeigen](./release-notes/release-notes.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=de)

Erste Schritte

Lesen Sie die [!DNL Journey Optimizer B2B Edition] Onboarding-Anleitung für Admins und Marketing-Fachleute.

[Administratoren](./setup-ultimate.md)
[Benutzer](./start/get-started.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=de)

Verwalten von Daten

Aktivieren Sie die XDM-Schemata und -Felder, die Sie in [!DNL Adobe Journey Optimizer B2B Edition] verwenden möchten, und erfahren Sie, wie die Daten in [!DNL Adobe Experience Platform] funktionieren.

[XDM-Feldverwaltung anzeigen](./admin/xdm-field-management.md)
[Exportierte Datensätze](./data/aep-exported-datasets.md)
[Datensatzabfragen](./data/aep-query-examples.md)
[Datenverfügbarkeit und Synchronisierungszeitpunkt](./data/data-availability-timing.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=de)

Kommunikationskanäle

Konfigurieren und verwalten Sie E-Mail, SMS, WhatsApp und andere Kanäle für personalisierte Kundeninteraktionen.

[E-Mail-Kanal konfigurieren](./admin/configure-channels-emails.md)
[SMS-Kanal konfigurieren](./admin/configure-channels-sms.md)
[Konfigurieren des WhatsApp-Kanals](./admin/configure-channels-whatsapp.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=de)

Erstellen einer Journey

Entwerfen, orchestrieren, verwalten und optimieren Sie personalisierte Account- und Personen-Journey.

[Erkunden Sie Journeys](./journeys/journeys-overview.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/users.svg?lang=de)

Einkaufsgruppen verstehen

Detaillierte Anleitungen zum Erstellen, Verwalten und Optimieren von Einkaufsgruppen für eine effektive Zielgruppenbestimmung.

[Informationen zu Einkaufsgruppen](./buying-groups/buying-groups-overview.md)
:::

::::

<!--
:::
![icon](https://cdn.experienceleague.adobe.com/icons/image.svg?lang=de)

Design Content

Learn how to author and manage content for personalized customer experiences orchestrated through journeys.

[Explore Content Components](./content/content-components.md)
::: 
-->

## Demo zum Überblick

Entdecken Sie die Komponenten einer Käufergruppe und erfahren Sie mehr über die Grundlagen des Aufbaus einer Konto-Journey.

>[!VIDEO](https://video.tv.adobe.com/v/3432054?quality=12)

## Dokumentation anzeigen

<table style="table-layout:auto">
  <tr style="border: 0;">
    <td>
      <img src="../assets/do-not-localize/icon-quick-start.svg" width="35px" alt="Erste Schritte"><br/>
      <strong>Erste Schritte</strong><br/><a href="home-page.md">Anmeldung und Startseite</a><br/><a href="./start/get-started.md">Onboarding-Anleitung</a> <br/><a href="./ai-coworker/ai-overview.md">KI-Funktionen</a>
    </td>
    <td>
      <img src="../assets/do-not-localize/icon_audience.svg" width="35px" alt="Käufergruppen"><br/>
<strong>Käufergruppen</strong><br/><a href="./buying-groups/buying-groups-overview.md">Überblick über Käufergruppen</a><br/><a href="./buying-groups/buying-groups-role-templates.md">Rollenvorlagen</a><br/><a href="./buying-groups/solution-interests.md">Lösungsinteressen</a><br/><a href="./buying-groups/buying-groups-create.md">Käufergruppen erstellen</a>
    </td>
    <td>
      <img src="../assets/do-not-localize/icon-paths.svg" width="35px" alt="Konto-Journeys"><br/>
      <strong>Konto-Journeys</strong><br/><a href="./journeys/journeys-overview.md">Übersicht über Journeys</a><br/><a href="./journeys/create-publish-journey.md#create-a-journey">Erstellen einer Konto-Journey</a><br/><a href="./journeys/journey-nodes.md">Journey-Knoten</a>
    </td>
  </tr>
  <tr style="border: 0;">
    <td>
      <img src="../assets/do-not-localize/icon-campaign.svg" width="35px" alt="Journey-Inhalt"><br/>
      <strong>Journey-Inhalt</strong><br/><a href="./content/add-email.md">E-Mail-Kanal</a><br/><a href="./content/generate-content-emails.md">E-Mail-Inhalt generieren</a><br/><a href="./content/genstudio-email-workflow.md">GenStudio-E-Mail-Erlebnisse</a><br/><a href="./content/sms-authoring.md">SMS-Kanal</a>
    </td>
        <td>
      <img src="../assets/do-not-localize/icon_assets.svg" width="35px" alt="Content-Management"><br/>
      <strong>Content-Management</strong><br/><a href="./content/assets-overview.md">Übersicht über Assets</a><br/><a href="./content/email-templates.md">E-Mail-Vorlagen</a><br/><a href="./content/fragments.md">Visuelle Fragmente</a><br/><a href="./content/conditional-content.md">Bedingter Inhalt</a><br/><a href="./content/brand-themes.md">Markenthemen</a>
    </td>
    <td>
      <img src="../assets/do-not-localize/icon-offer.svg" width="35px" alt="Erkenntnisse und Dashboards"><br/>
      <strong>Insights</strong><br/><a href="./dashboards/intelligent-dashboard.md">Intelligent Dashboard</a><br/><a href="./dashboards/engagement-dashboard.md">Interaktions-Dashboard</a><br/><a href="./dashboards/buying-groups-dashboard.md">Gruppen-Dashboard kaufen</a><br/><a href="./dashboards/journeys-dashboard.md">Journey-Dashboard</a><br/><a href="./buying-groups/incrm-insights.md">In-CRM-Insights</a>
    </td>

</tr>
</table>

>[!BEGINSHADEBOX]

## [!DNL Marketo Qualifier]

[!DNL Adobe Marketo Qualifier] ist eine KI-gesteuerte Anwendung, die Sie mit [!DNL Journey Optimizer B2B Edition] verwenden können. Es implementiert die Kontenqualifikation und optimiert die Workflows für Business Development Representatives (BDRs). [!DNL Marketo Qualifier] automatisiert Workflows für die Qualifizierung von Interessenten, Kontaktaufnahme und Käuferinteraktion kanalübergreifend. Dies reduziert die manuelle BDR-Belastung und beschleunigt die Pipeline-Geschwindigkeit für B2B-Unternehmen.

Weitere Informationen finden Sie in der Dokumentation zu [Marketo Qualifier](https://experienceleague.adobe.com/de/docs/marketo-qualifier/using/home){target="_blank"}.

>[!ENDSHADEBOX]

## Zusätzliche Ressourcen

<table style="table-layout:fixed">
<tr><td><strong>Adobe Journey Optimizer B2B Edition</strong><br/>
<a href="https://experienceleague.adobe.com/de/docs/journey-optimizer-b2b-learn/tutorials/overview" target="_blank">Videos und Tutorials</a> - <a href="https://helpx.adobe.com/de/legal/product-descriptions/adobe-journey-optimizer-b2b.html" target="_blank">Produktbeschreibung</a> <!-- - <a href="https://www.adobe.com/content/dam/cc/en/security/pdfs/AJO_SecurityOverview.pdf" target="_blank">Security overview (PDF)</a> - <a href="https://developer.adobe.com/journey-optimizer-apis/" target="_blank">APIs reference</a> - <a href="https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=de" target="_blank">Journey Optimizer Schema Dictionary</a> -->
</td>
<td><strong>Adobe Experience Platform</strong><br/>
<a href="https://experienceleague.adobe.com/de/docs/experience-platform/landing/home" target="_blank">Dokumentation</a> - <a href="https://business.adobe.com/de/products/experience-platform/documentation-and-developer-resources.html" target="_blank">Entwicklerressourcen</a>
</td></tr>
<tr><td><strong>Adobe Real-Time Customer Data Platform</strong><br/>
<a href="https://experienceleague.adobe.com/de/docs/experience-platform/rtcdp/home" target="_blank">Dokumentation</a> - <a href="https://experienceleague.adobe.com/de/docs/platform-learn/getting-started-for-data-architects-and-data-engineers/overview" target="_blank">Entwickler-Tutorials</a>
</td><td><strong>Adobe Marketo Engage</strong><br/>
<a href="https://experienceleague.adobe.com/de/docs/marketo/using/home" target="_blank">Benutzerdokumentation</a> - <a href="https://experienceleague.adobe.com/de/docs/marketo-developer/marketo/home" target="_blank">Entwicklerdokumentation</a>
</td>
</tr></table>
