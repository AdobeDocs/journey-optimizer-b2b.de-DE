---
title: Mitarbeiter in Adobe Journey Optimizer B2B Edition
description: Erfahren Sie, wie Sie mit CX Enterprise Coworker Konto- und Personen-Journey suchen, erstellen und konfigurieren, Vorschauentwürfe überprüfen und die Journey-Erstellung genehmigen können.
feature: Account Journeys, Person Journeys, Agentic AI
role: User
level: Beginner
autotag-review: '2026-11-24T23:47:29.469Z'
TQID: 'https://experienceleague.adobe.com/gkizS-MB6qEMoG1pMqD3tSCBtcEuv-m-GMD5H6Z4JsY'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: 9b63d357-750f-5558-9208-62fc8a356785
    internal-label: Approval
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
    internal-label: Journeys
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
  - id: c2f21a5c-bae4-56c6-97e3-2fc9a0e6c120
    internal-label: Use Cases
subfeature_v2:
  - id: ba367494-9862-4596-bd6f-299c7e10a46b
    internal-label: Person Journeys
  - id: c31bc6c7-76bc-467b-80c0-7315a4e3f6be
    internal-label: Account Journeys
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 81b4844bc7b333baaa2218639a542fefd512102f
workflow-type: tm+mt
source-wordcount: '780'
ht-degree: 2%
---

# [!DNL CX Enterprise Coworker] in [!DNL Adobe Journey Optimizer B2B Edition] {#coworker-overview}

Verwenden Sie [!DNL Adobe CX Enterprise Coworker] Chat, um Aufgaben in [!DNL Adobe Journey Optimizer B2B Edition] abzuschließen. Beschreiben Sie ein Ziel in einfacher Sprache. [!DNL Coworker] plant die Arbeit, führt sie aus, validiert die Ergebnisse und legt die Arbeit zur Genehmigung vor.

Suchen Sie bestehende Konto- und Personen-Journey, erstellen Sie neue Journey-Entwürfe oder aktualisieren Sie gespeicherte Entwürfe. [!DNL Coworker] verwandelt Ihren Brief in ein validiertes Journey-Diagramm und zeigt eine Vorschau an, bevor Sie den Entwurf erstellen. Sie müssen die Vorschau explizit genehmigen, bevor [!DNL Coworker] die Journey erstellt.

[!DNL Coworker] respektiert die vorhandenen [Produktberechtigungen](../admin/user-management.md#b2b-product-permissions) Ihres Unternehmens. Sie können nur Aktionen ausführen, zu denen Sie bereits berechtigt sind. Administratoren steuern, wann Sie Schreibzugriff haben. Informationen zu Zugriffsanforderungen finden Sie unter [Aktivieren des KI-Zugriffs](../ai-coworker/enable-ai-access.md).

[!DNL Coworker] funktioniert im gesamten Adobe-Ökosystem, nicht nur in [!DNL Journey Optimizer B2B Edition]. Die erweiterten Funktionen finden Sie in der Übersicht über den [Adobe CX Enterprise Coworker-Chat](https://experienceleague.adobe.com/de/docs/coworker/content/chat/overview){target="_blank"}. Anweisungen zum Öffnen der App und zum Starten von Konversationen finden Sie im [Handbuch zur -Benutzeroberfläche](https://experienceleague.adobe.com/de/docs/coworker/content/chat/ui-guide){target="_blank"}.

## Journey-Kenntnisse {#skills}

Verwenden Sie diese drei Kenntnisse, um Journey zu untersuchen, Journey-Diagramme zu erstellen und Knoten zu konfigurieren. Qualifikationskennungen sind exakte technische Namen.

| Skill | Was es Ihnen hilft zu tun | Außerhalb des Bereichs der Kenntnisse |
| --- | --- | --- |
| `journey-lookup-ajob2b` | Auflisten, Zählen, Suchen und Erklären von Account- und Personen-Journey. Überprüfen Sie Knoten, Einstellungen für den erneuten Eintritt und die Aktivitäten, Attribute oder Ereignis-Zielgruppe, die eine Journey verwendet. Diese Fertigkeit ändert die Journey nicht. | Journey erstellen oder ändern, Regeln konfigurieren, Nachrichten kopieren, Einkaufsgruppenvorlagen verwalten, veröffentlichen oder löschen. |
| `journey-creation-ajob2b` | Verwandeln Sie eine Kurzbeschreibung in eine Journey. Wählen Sie den Journey-Typ aus, lösen Sie die Zielgruppe in ihre [!DNL Adobe Experience Platform] Zielgruppen-ID auf, validieren Sie das Diagramm und zeigen Sie eine Vorschau an. Erstellen Sie den Entwurf nach expliziter Genehmigung. Bearbeiten Sie das Diagramm eines gespeicherten Entwurfs und nehmen Sie die Einstellungen für den erneuten Eintritt vor. | Vorhandene Journey nachschlagen, Regeln konfigurieren, Nachrichtenkopien erstellen, Einkaufsgruppenvorlagen verwalten, Zielgruppen entdecken, veröffentlichen oder löschen. |
| `journey-rules-ajob2b` | Konfigurieren Sie Bedingungen, Aktionen, Ereignisse und die dynamische Audience-Liste auf einem gespeicherten Journey auf nicht konfigurierten Knoten. | Ändern Sie das Diagramm, suchen Sie nach Journey, verfassen Sie E-Mails oder SMS-Kopien, entdecken Sie Zielgruppen oder veröffentlichen Sie. |

Weitere Hinweise zur Eingabeaufforderung finden Sie unter [Journey-Kenntnisse für B2B](./journey-skills.md). Informationen zum Arbeiten mit Konto- und Personen-Zielgruppen finden Sie unter [Zielgruppenkenntnisse für B2B-Konten und Personen](./audience-skills-b2b.md).

## Beispielhafte Anwendungsfälle {#use-cases}

Verwenden Sie separate Anfragen, um einen Entwurf zu erstellen, die zugehörigen Knoten zu konfigurieren und die vorhandenen Journey zu überprüfen.

### Konto-Journey erstellen {#build-account-journey}

Erstellen Sie aus einer Zusammenfassung eine Account Nurture-Journey und konfigurieren Sie dann deren Knoten.

Beispiel-Eingabeaufforderung: _Erstellen Sie eine Konto-Journey für die Zielgruppe der Enterprise Target-Konten, die eine Begrüßungs-E-Mail sendet, drei Tage wartet und dann eine E-Mail mit einer Fallstudie sendet._

1. Beschreiben Sie die Zielgruppe und den Journey-Ablauf im [!DNL Coworker] Chat.
1. Überprüfen Sie das validierte Journey-Diagramm und die Vorschau. [!DNL Coworker] löst die benannte Zielgruppe in die [!DNL Experience Platform] Zielgruppen-ID auf.
1. Die Vorschau muss ausdrücklich genehmigt werden. [!DNL Coworker] erstellt den Entwurf und gibt die zugehörige Relation zurück.
1. Bitten Sie [!DNL Coworker], die nicht konfigurierten Knoten des Entwurfs zu konfigurieren.
1. Öffnen Sie den Entwurf in [!DNL Journey Optimizer B2B Edition] , um eine Nachrichtenkopie hinzuzufügen und die Journey zu überprüfen.

Das Ergebnis ist eine Entwurfs-Journey, keine veröffentlichte Journey. Führen Sie die Schritte zur Überprüfung und Veröffentlichung von [Journey](../journeys/create-publish-journey.md) in der Anwendung aus.

### Journey überprüfen und aktualisieren {#inspect-update-journeys}

Überprüfen Sie Ihr Journey-Inventar und verfeinern Sie dann die Aufspaltungsbedingungen und die Wiedereinstiegseinstellungen eines gespeicherten Entwurfs.

Beispiel-Lookup-Eingabeaufforderung: _Wie viele Account-Journey sind live? Anzeigen, wo auf Journey 14251 Konten warten._

1. Fragen Sie [!DNL Coworker] nach der Anzahl der Journey nach Status, oder suchen Sie eine Journey nach Name oder ID.
1. Überprüfen Sie die Journey-Details und die Kontoanzahl auf jedem Knoten.
1. Identifizieren Sie den gespeicherten Entwurf, den Sie aktualisieren möchten.
1. Bitten Sie [!DNL Coworker], die Aufspaltungsbedingung zu konfigurieren. Beispiel: _Stellen Sie für den Entwurf von Journey-14252 sicher, dass die Verzweigung mit hoher Absicht einen Seitenbesuch zu Preisen erfordert._
1. Anfordern der Wiedereintrittsänderung. Beispiel: _Bei Entwurfs-Journey-14252 30 Tage lang verhindern, dass Konten erneut erfasst werden._

Änderungen werden auf den gespeicherten Entwurf angewendet. Die Veröffentlichung ist ein separater Schritt. Konfigurationsdetails finden Sie unter [Aufspaltungs- und Zusammenführungspfade](../journeys/split-merge-paths-nodes.md) und [Neueingabe von Journey](../journeys/journey-re-entry.md).

## MCP-Tools {#mcp-tools}

[!DNL Coworker] verwendet die folgenden MCP-Tools (Model Context Protocol) zum Journey von Aufgaben. Lesetools Überprüfen Sie vorhandene Informationen, das Überprüfungstool validiert ein Diagramm und Schreib-Tools ändern Journey-Einstellungen oder Entwürfe.

| Tool | Unterstützte Aktion | Typ |
| --- | --- | --- |
| `list_account_journeys` | Gibt eine paginierte Liste der Konto-Journeys zurück. | Lesen |
| `list_person_journeys` | Gibt eine paginierte Liste von Journey-Personen zurück. | Lesen |
| `count_account_journeys` | Journey des Kontos nach Bundesland zählen. | Lesen |
| `count_person_journeys` | Journey der Person nach Bundesland zählen. | Lesen |
| `get_journey` | Lesen von Journey-Knoten und Wiedereinstiegseinstellungen. | Lesen |
| `get_journey_rules` | Lesen Sie die Konfigurationsziele eines nicht konfigurierten Journey-Knotens. | Lesen |
| `get_journey_node_catalog` | Gibt `ruleset_types` zurück, die gültige Eingaben für Regeldaten sind. | Lesen |
| `validate_journey_graph` | Validieren eines erstellten Entwurfsdiagramms. | nachprüfen |
| `create_journey` | Vorschau der Journey mit `confirm=false`. Erstellen Sie nach der expliziten Genehmigung den Entwurf und geben Sie den Link zurück. | Schreiben |
| `update_journey` | Ändern des Diagramms einer gespeicherten Entwurfs-Journey. | Schreiben |
| `set_journey_reentry` | Ändern Sie die Wiedereinstiegseinstellungen. | Schreiben |
| `set_journey_split_conditions` | Festlegen von Bedingungen für die Verzweigung aufteilen | Schreiben |
| `apply_journey_rules` | Wenden Sie `rule_data` für Bedingungen, Aktionen, Ereignisse und die Audience der dynamischen Liste auf eine Journey an. | Schreiben |
