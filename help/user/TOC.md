---
user-guide-title: Dokumentation zu Journey Optimizer B2B Edition
user-guide-description: Erfahren Sie mehr über Adobe Journey Optimizer B2B Edition und darüber, wie Sie sie zum Orchestrieren von Konto- und Käufergruppen-Journeys mithilfe der integrierten generativen KI und branchenführender Automatisierung verwenden können.
source-git-commit: f80f0ac96f730833473e0a3e17035dac0fb5f3ce
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 96%

---


# Benutzerhandbuch für Journey Optimizer B2B Edition {#user}

+ [Dokumentation zu Adobe Journey Optimizer B2B Edition](guide-overview.md)
+ [Versionshinweise](./release-notes/release-notes.md)
+ Erste Schritte {#get-started}
   + [Journey Optimizer B2B Edition – Überblick](about-journey-optimizer-b2b-edition.md)
   + [Anmelde- und Startseite](home-page.md)
   + [Anleitung zum Onboarding](./start/get-started.md)
   + [Tracking- und E-Mail-Protokolle](./start/email-protocols.md)
+ KI-Assistent {#ai-assistant}
   + [Überblick](./ai-assistant/ai-assistant-overview.md)
   + [Aktivieren des Zugriffs auf den KI-Assistenten](./ai-assistant/enable-ai-assistant-access.md)
   + [Anleitung zu Fragen](./ai-assistant/question-guidance.md)
   + [Verwenden des KI-Assistenten](./ai-assistant/use-ai-assistant.md)
   + Agentinnen bzw. Agenten {#ai-agents}
      + [Audience Agent](./agents/audience-agent-b2b.md)
      + [Journey Build Agent](./agents/journey-agent.md)
      + [Verkaufskennzeichner](./agents/sales-qualifier.md)
+ Konto-Journeys {#account-journeys}
   + [Überblick](./journeys/journey-overview.md)
   + [Erstellen und Veröffentlichen einer Journey](./journeys/create-publish-journey.md)
   + [Journey-Knoten](./journeys/journey-nodes.md)
   + Journey-Knoten {#journey-nodes}
      + [Kontozielgruppe](./journeys/account-audience-nodes.md)
      + [Durchführen einer Aktion](./journeys/action-nodes.md)
      + [Auf ein Ereignis lauschen](./journeys/listen-for-event-nodes.md)
      + [Aufteilen und Zusammenführen von Pfaden](./journeys/split-merge-paths-nodes.md)
      + [Warten](./journeys/wait-nodes.md)
   + [Journey-Details](./journeys/journey-details.md)
+ Journey-Inhalt {#journey-content}
   + E-Mail-Kanal {#email-channel}
      + [Hinzufügen einer E-Mail](./content/add-email.md)
      + [E-Mail-Erstellung](./content/email-authoring.md)
      + [KI-Assistent für E-Mail-Erstellung](./content/ai-assistant-emails.md)
      + [GenStudio-Workflows](./content/genstudio-email-workflow.md)
      + [Dunkler Modus für E-Mail-Design](./content/email-dark-mode.md)
      + [Geregelte Vorlagen](./content/email-authoring-governance.md)
      + [E-Mail mit Verkaufshinweis](./content/sales-alert-email.md)
   + [Benutzerdefinierte Personalisierungs-Token](./content/personalization-my-tokens.md)
   + [SMS-Erstellung](./content/sms-authoring.md)
+ Konten {#accounts}
   + [Zielgruppen](./audiences/account-audience-overview.md)
   + Käufergruppen {#buying-groups}
      + [Überblick](./buying-groups/buying-groups-overview.md)
      + [Lösungsinteressen](./buying-groups/solution-interests.md)
      + [Rollenvorlagen](./buying-groups/buying-groups-role-templates.md)
      + [Standard- und benutzerdefinierte Rollen](./buying-groups/default-custom-roles.md)
      + Käufergruppenbewertung {#scoring}
         + [Interaktionswerte](./buying-groups/engagement-scores.md)
         + [Vollständigkeitswerte](./buying-groups/completeness-scores.md)
      + [Käufergruppenphasen](./buying-groups/buying-group-stages.md)
      + [Erstellen von Käufergruppen](./buying-groups/buying-groups-create.md)
      + [Exportieren von Konten](./audiences/account-list-export.md)
      + [Auf LinkedIn-Konto abgestimmte Zielgruppen](./data/linkedin-account-matched-audiences.md)
      + [Käufergruppenfilter in Marketo Engage](./buying-groups/marketo-engage-smart-list-buying-group-filters.md)
      + [In-CRM-Einblicke](./buying-groups/incrm-insights.md)
   + Kontolisten {#account-lists}
      + [Überblick](./accounts/account-lists.md)
      + [Verwendung in Journeys und Programmen](./accounts/account-lists-journeys.md)
   + [XDM-Felder](./data/field-mapping.md)
   + Vertriebserlebnis {#sales-experience}
      + [Kontodetails](./accounts/account-details.md)
      + [Käufergruppendetails](./buying-groups/buying-group-details.md)
      + [Personendetails](./accounts/person-details.md)
      + [CRM-Verknüpfung](./accounts/crm-linking.md)
+ Content-Management {#content-management}
   + E-Mails {#emails}
      + [Arbeiten mit E-Mail-Inhalten](./content/emails-list.md)
      + [Gestalten barrierefreier Inhalte](./content/email-accessible-content.md)
      + Vorschau und Validierung {#preview}
         + [Simulieren von Inhalten](./content/email-simulate-content.md)
         + [Testen des E-Mail-Renderings](./content/email-test-rendering.md)
         + [Spam-Bericht](./content/email-spam-report.md)
      + [E-Mail-Zusammenarbeit](./content/email-collaboration-tools.md)
   + Assets {#assets}
      + [Überblick](./content/assets-overview.md)
      + Interne Assets {#internal-dam}
         + [Arbeiten mit internen Assets](./content/internal-image-assets.md)
         + [Bearbeiten von Bildern mit Adobe Express](./content/image-edit-adobe-express.md)
      + [Experience Manager – Bild-Assets](./content/aem-assets.md)
   + Vorlagen {#templates}
      + [Content-Governance](./content/template-content-governance.md)
      + E-Mail-Vorlagen {#email-templates}
         + [Überblick](./content/email-templates.md)
         + [Erstellung von E-Mail-Vorlagen](./content/email-template-authoring.md)
         + [Konvertieren eines Bilds in eine Vorlage](./content/email-template-image-convert.md)
      + Landingpage-Vorlagen (Beta) {#landing-page-templates}
         + [Überblick](./content/landing-page-templates.md)
         + [Landingpage-Vorlagen-Design](./content/landing-page-template-design.md)
   + Fragmente {#visual-fragments}
      + [Überblick](./content/fragments.md)
      + [Erstellen von Fragmenten](./content/fragment-authoring.md)
   + Formulare (Beta) {#forms}
      + [Überblick](./content/forms.md)
      + [Formular-Design](./content/form-design.md)
   + Landingpages (Beta) {#landing-pages}
      + [Übersicht](./content/landing-pages.md)
      + [Landingpage-Design](./content/landing-page-design.md)
   + Tools für das Design von Inhalten {#content-design}
      + [Strukturkomponenten](./content/structure-components.md)
      + [Inhaltskomponenten](./content/content-components.md)
      + [Benutzerdefiniertes CSS](./content/design-custom-css.md)
   + Marken (Beta) {#brands}
      + [Überblick](./content/brands-overview.md)
      + [Verwalten und Erstellen](./content/brands-manage-create.md)
      + [Markenausrichtung](./content/brand-alignment.md)
   + [Markenthemen](./content/brand-themes.md)
   + [Bedingte Inhalte](./content/conditional-content.md)
   + Personalisierung {#personalization}
      + [Überblick](./content/personalization.md)
      + [Personalisierungssyntax](./content/personalization-syntax.md)
      + [Liste der Hilfsfunktionen](./content/personalization-helper-functions.md)
+ Erkenntnis-Dashboards {#dashboards}
   + [Intelligentes Dashboard](./dashboards/intelligent-dashboard.md)
   + [Überblick über die Interaktionen](./dashboards/engagement-dashboard.md)
   + [Überblick über Käufergruppen](./dashboards/buying-groups-dashboard.md)
   + [Überblick über Konto-Journeys](./dashboards/journeys-dashboard.md)
+ Administration {#admin}
   + [Governance](./admin/governance.md)
   + [Persona-Mapping](./admin/persona-mapping.md)
   + [Benutzerverwaltung](./admin/user-management.md)
   + Kanäle {#channels}
      + [E-Mail-Konfigurationen](./admin/configure-channels-emails.md)
      + [SMS-Konfigurationen](./admin/configure-channels-sms.md)
      + [Landingpage-Einstellungen](./admin/landing-page-settings.md)
      + [Konfigurieren von Datenströmen für die Ereignissammlung](./data/aep-event-collection.md)
   + Konfigurationen  {#configurations}
      + [AEM Assets-Repositorys](./admin/configure-aem-repositories.md)
      + [AEP-Ereignisdefinitionen](./admin/configure-aep-events.md)
      + [Absichtsdaten](./admin/intent-data.md)
      + [Gewichtung der Interaktionsbewertung](./admin/engagement-score-weighting.md)
   + [Vereinfachte Architektureinrichtung](simplified-architecture.md)
