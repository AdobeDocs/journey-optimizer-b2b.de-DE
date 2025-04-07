---
title: Versionshinweise
description: Neueste Versionshinweise für Adobe Journey Optimizer B2B Edition
exl-id: 7d3f1c26-d8a6-4065-a70f-5b30cb975dc8
source-git-commit: dd93531d76ecb025451f0015eedd9ccce0986cb8
workflow-type: tm+mt
source-wordcount: '1816'
ht-degree: 9%

---

# Versionshinweise zu Journey Optimizer B2B edition

Adobe Journey Optimizer B2B edition bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen.

Journey Optimizer B2B edition basiert nativ auf [!DNL Adobe Experience Platform] und profitiert von den neuesten Innovationen und Verbesserungen von Platform. Weitere Informationen zu diesen Änderungen finden Sie unter [Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/release-notes/latest){target="_blank"}.

Lesen Sie die [Produktbeschreibung](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"}, um Informationen über Berechtigungen, Leistungsschutzmechanismen und Einschränkungen zu erhalten.

## Versionshinweise für 2025.3

**Veröffentlichungsdatum**: Mittwoch, 1. April 2025

Diese Version umfasst die folgenden neuen Funktionen und Verbesserungen:

| Typ | Element | Beschreibung |
| ---- | ---- | ----------- |
| Neue Funktion | Kontolisten | Sie können jetzt eine statische oder dynamische Kontenliste erstellen, um benannte Konten nach Ihren definierten Kriterien wie Branche, Standort oder Größe des Unternehmens auszuwählen. <a href="../accounts/account-lists.md">Weitere Informationen</a> |
| Neue Funktion | Meine Token für Account Journey | Sie können jetzt einen Satz benutzerdefinierter Token mit Werten definieren, die für die Konto-Journey spezifisch sind. Dieser Satz benutzerdefinierter Token wird als &quot;_Token“_. Jedes dieser benutzerdefinierten Token dient zur Personalisierung beim Verfassen von Journey-E-Mails. |
| Neue Funktion | Einkaufsgruppenstufen löschen | Sie können das Modell der Einkaufsgruppenstufen löschen, wenn es sich im Status Entwurf oder Veröffentlicht befindet. Wenn sie veröffentlicht (live) ist, können Sie sie nur löschen, wenn sie nicht mit einer Interessenslösung verbunden ist. <a href="../buying-groups/buying-group-stages.md#delete-the-buying-group-stages-model">Weitere Informationen</a> |
| Verbesserung | Journey-Knotenanzahl | Verbesserte Sichtbarkeit der Anzahl der Journey-Mitglieder auf Knotenebene. Verwenden Sie diese Informationen, um den Kontofortschritt auf einer Journey zu überprüfen. |

## Versionshinweise für 2025.2

**Veröffentlichungsdatum:**. März 2025

Diese Version umfasst die folgenden neuen Funktionen und Verbesserungen:

| Typ | Element | Beschreibung |
| ---- | ---- | ----------- |
| Neue Funktion | Anpassbare Felder - Inhaltsfragmente | Als Inhaltsfragment-Designer können Sie einen Parameter für eine Komponente im Fragment als bearbeitbar festlegen. Auf diese Weise kann der E-Mail- oder Vorlagenautor einen benutzerdefinierten Feldwert angeben, der speziell für seine Anforderungen gilt. Dieses Anpassungsflag ist auf visuelle Bild-, Text- und Schaltflächen-Komponenten beschränkt. <a href="../content/fragment-authoring.md#enable-custom-fields">Weitere Informationen</a> |
| Neue Funktion | Integrierte B2B-Rollen und -Produktberechtigungen | Experience Platform enthält jetzt eine Reihe integrierter (standardmäßiger) Rollen, mit denen Sie den Zugriff auf die B2B-Produktfunktionen verwalten können. <a href="../admin/user-management.md#b2b-built-in-roles">Weitere Informationen</a> <br/>Administratoren können jetzt benutzerdefinierte Rollen in Adobe Experience Platform definieren, um Journey Optimizer B2B edition-Produktberechtigungen einzuschließen.  <a href="../admin/user-management.md#b2b-product-permissions">Weitere Informationen</a> |
| Neue Funktion | Journey-Duplikatstypen | Wenn Sie eine Konto-Journey duplizieren, können Sie Knotendetails einbeziehen, mit Ausnahme von E-Mails und SMS-Nachrichten, die in Journey Optimizer B2B edition erstellt wurden. Als Alternative können Sie eine Skelettkopie der Struktur- und Pfadflüsse erstellen, ohne Knotendetails und Einstellungen. <a href="../journeys/journey-overview.md#duplicate-journey">Weitere Informationen</a> |
| Verbesserung | Vier zusätzliche Beispiel-E-Mail-Vorlagen | Die Beispiel-E-Mail-Vorlagen-Bibliothek enthält jetzt vier SecurFinancial-Vorlagen als Beispiele für die Wiederaufnahme von Interaktionen, Informationen, Pflege und Feedback-Inhalte |

## Versionshinweise für 2025.1 {#Jan-2025}

**Veröffentlichungsdatum:**. Februar 2025

Diese Version umfasst die folgenden neuen Funktionen und Verbesserungen:

| Typ | Element | Beschreibung |
| ---- | ---- | ----------- |
| Neue Funktion | Erlebnisereignisweiterleitung | Admins können auf Adobe Experience Platform (AEP) basierende Ereignisdefinitionen konfigurieren. Diese Konfigurationen ermöglichen es Marketing-Experten, Account-Journey zu erstellen, die auf AEP Experience Events reagieren.  <a href="../admin/configure-aep-events.md">Weitere Informationen</a> |
| Neue Funktion | Paid Media-Ziele | Bekannte Personen für Paid-Media-Kampagnen von einer Account-Journey qualifizieren, damit sie auf Werbeplattformen wie LinkedIn weiter eingebunden werden können. Verwenden Sie einen aufgeteilten Pfadknoten in einer Account-Journey, um Account-Zielgruppen basierend auf bestimmten Verhaltensweisen zu segmentieren und Accounts zu identifizieren, die zusätzliche Interaktionen rechtfertigen. Fügen Sie dann Personen aus diesen Konten über Real-Time CDP zu einer externen Kundenzielgruppe zu einem unterstützten Paid-Media-Ziel hinzu. <a href="../journeys/action-nodes.md#journey-optimizer-b2b-actions">Weitere Informationen</a> |
| Neue Funktion | Intelligentes Dashboard | Sehen Sie sich den Fortschritt von Einkaufsgruppen über ihre Account-Journey an, einschließlich KI-generierter Einblicke, um eine intelligentere Analyse und eine genauere Account-Priorisierung zu erhalten. <a href="../dashboards/intelligent-dashboard.md">Weitere Informationen</a> |
| Neue Funktion | Einkaufsgruppe und Kontodetails | Sehen Sie sich Einblicke auf der Einkaufs- und Kontoebene an, um mehr Kontext- und historische Daten zu erhalten, wenn Sie mit der Interaktion mit einem Kunden beginnen.<p>Zu den Details der Einkaufsgruppe gehören alle erkannten First-Party-Absichten. <a href="../buying-groups/buying-group-details.md">Weitere Informationen</a><p>Die Accounts mit den Kontodetails zeigen den beobachteten Anstieg der Interaktionsabsicht, sodass Sie den Vertrieb auf Accounts hinweisen können, die für eine kundenspezifische, verkaufsorientierte Interaktion bereit sind.  <a href="../accounts/account-details.md">Weitere Informationen</a> |
| Neue Funktion | Übersicht über die Journey | Wenn Sie auf Account-Journey zugreifen, bietet die Registerkarte Übersicht eine umfassende Übersicht über Ihre aktiven Account-Journey mit detaillierten Account-Fortschrittsanzeigen, in denen Kreis- und Balkendiagramme verwendet werden, die Abschlüsse und Interaktionsaktivitäten kategorisieren und quantifizieren.  <a href="../dashboards/journeys-dashboard.md">Weitere Informationen</a> |
| Neue Funktion | Adobe Express-Bildbearbeitung | Schnellaktionen in Adobe Express ermöglichen Ihnen einfache Bearbeitungen (z. B. Zuschneiden und Ändern der Größe) von Bildern, um das Erscheinungsbild Ihres Inhalts zu verbessern. <a href="../content/image-edit-adobe-express.md#quick-actions-in-adobe-express">Weitere Informationen</a>  <p>Für einen umfassenderen Satz an Design-Tools ermöglicht diese Integration eine vollständige Adobe Express-Lizenz in Journey Optimizer B2B edition. Mit diesem Setup wird die gesamte Adobe Express-Benutzeroberfläche im lokalen Asset-Arbeitsbereich verfügbar. <a href="../content/image-edit-adobe-express.md#adobe-express-enterprise-license">Weitere Informationen</a> |
| Neue Funktion | Absichtsfilter für den Kauf von Gruppenrollen | Wenn Sie Ihre Absichtsschlüsselwörter übermitteln, sagt das Absichtserkennungsmodell basierend auf der Aktivität eines Leads eine Lösung/ein Produkt von Interesse mit ausreichend hoher Zuverlässigkeit voraus. <a href="../admin/intent-data.md">Weitere Informationen</a> <p>Diese Absichtsdaten stehen für die Definition der Bedingungen für die Einkaufsgruppenrolle zur Verfügung <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Weitere Informationen</a> |
| Verbesserung | Marketo Engage-Ereignisunterstützung in Journey | Der _Lauschen auf Ereignis_-Journey-Knoten unterstützt jetzt zwei Marketo Engage-Ereignisse auf Benutzerebene: _Besucht die_ und _Formular ausfüllt_. <a href="../journeys/listen-for-event-nodes.md#listen-for-marketo-engage-event">Weitere Informationen</a> |
| Verbesserung | Kaufen von Gruppenfiltern für Marketo Engage-Smart-Listen | Anzeigen und Erstellen von Smart Lists mit Einkaufsgruppenfiltern in Marketo Engage. Mit diesen hinzugefügten Filtern können Sie kaufmännische Gruppenmitglieder über Marketo Engage-Kampagnen und -Programme hinweg von den Account-Journey in Journey Optimizer B2B edition unterdrücken und einbeziehen. <a href="../buying-groups/marketo-engage-smart-list-buying-group-filters.md">Weitere Informationen</a> |
| Verbesserung | Marketo Engage-Listenmitgliedschaftsfilter für Journey und Rollen | Überprüfen Sie in Journey Optimizer B2B die Marketo Engage-Listenmitgliedschaft als Bedingung für einen _Aufspaltungspfad nach Personen_-Knoten, um doppelte Journey-Aktivitäten zu vermeiden. <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">Weitere Informationen</a> <p> Verwenden Sie für Vorlagen für Gruppenrollen die Listenmitgliedschaft als Rollenbedingung. <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Weitere Informationen</a> |
| Verbesserung | Dashboard für Interaktionsübersicht | Dieses Dashboard wird aktualisiert, um eine umfassende Ansicht der Interaktion zu bieten. Es zeigt Echtzeit-Metriken von Konto- und individuellen Interaktionen durch Momentaufnahmen-Kreisdiagramme und Trend-aufschlussreiche Liniendiagramme im Zeitverlauf. <a href="../dashboards/engagement-dashboard.md">Weitere Informationen</a> |


## Versionshinweise für Oktober 2024 {#Oct-2024}

**Veröffentlichungsdatum:**. Oktober 2024

Diese Version umfasst die folgenden neuen Funktionen und Verbesserungen:

| Typ | Element | Beschreibung |
| ---- | ---- | ----------- |
| Neue Funktion | Bedingte Inhalte in E-Mail-Vorlagen | Personalisieren Sie Ihren E-Mail-Inhalt basierend auf dem Verhalten und den Profilmerkmalen der Empfänger - sowohl auf Konto- als auch auf Lead-Ebene. <p>Verwenden Sie beim Erstellen einer E-Mail für Ihr Account-Journey im visuellen Design-Bereich der E-Mail bedingte Regeln, um mehrere Varianten für Inhaltskomponenten zu definieren. <a href="../content/conditional-content.md">Weitere Informationen</a> |
| Neue Funktion | _Zu Liste hinzufügen_ und _Aus Liste entfernen_ Personalaktionen in Journey | Personalisieren Sie Ihren E-Mail-Inhalt basierend auf dem Verhalten und den Profilmerkmalen der Empfänger - sowohl auf Konto- als auch auf Lead-Ebene. <a href="../journeys/action-nodes.md">Weitere Informationen</a> |
| Neue Funktion | Content Governance und Komponentensperrung | Um die Einhaltung genehmigter Inhaltsentwürfe sicherzustellen, verwenden Sie Content-Governance-Funktionen zum Sperren von Inhaltskomponenten für E-Mail-Vorlagen. Wenn die Content Governance in der E-Mail-Vorlage aktiviert ist, können Marketing-Experten nur die zulässigen Elemente ändern, um sie an die Inhaltsstrategie anzupassen. <a href="../content/template-content-governance.md">Weitere Informationen</a> |
| Neue Funktion | Käufergruppenphasen | Wenn Sie ein benutzerdefiniertes Einkaufsgruppen-Staging-Modell definieren und veröffentlichen, können Sie den Fortschritt der Einkaufsgruppe über die Lebenszyklusphasen der Einkaufsgruppe verfolgen. Verwenden Sie diese Schritte, um die nächste beste Aktion für Käufergruppenmitglieder zu ermitteln. Sie konfigurieren die Übergangsregeln und Journey-Knoten, die den Staging-Fortschritt und die Trigger-Aktionen basierend auf Änderungen bestimmen. <a href="../buying-groups/buying-group-stages.md">Weitere Informationen</a> |
| Verbesserung | Neue vordefinierte E-Mail-Vorlagen | Die Bibliothek mit Beispielvorlagen enthält jetzt zusätzliche E-Mail-Vorlagen, die für B2B-Marketing-Fachleute entwickelt wurden. Verwenden Sie diese Beispielvorlagen als Ausgangspunkt und fügen Sie Ihr eigenes Branding und Messaging hinzu. <a href="../content/email-templates.md#select-a-design-template">Weitere Informationen</a> |
| Verbesserung | Benutzerdefinierte Felder als Personenattribute | Wenn Sie benutzerdefinierte Personenfelder im Konto-Zielgruppenschema in Experience Platform definiert haben, sind diese Felder auch verfügbar, um als Personenattribute in Bedingungen zu verwenden. Verwenden Sie diese benutzerdefinierten Attribute in: <li>Rollenvorlagen <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Weitere Informationen</a></li><li>Pfade nach Personen-Journey-Knoten aufteilen <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">Weitere Informationen</a></li> |
| Verbesserung | E-Mail-Kanaleinstellungen | E-Mail-Einstellungen sind jetzt in der Benutzeroberfläche von Journey Optimizer B2B edition sichtbar. Sie können die aktuellen Konfigurationen schnell überprüfen. Administratoren können dann auf _[!UICONTROL Einstellungen bearbeiten]_ klicken, um direkt zu den Einstellungen in Marketo Engage zu wechseln und sie entsprechend den Anforderungen Ihres Unternehmens zu aktualisieren. <a href="../admin/configure-channels-emails.md">Weitere Informationen</a> |

## Versionshinweise für September 2024 {#Sept-2024}

**Veröffentlichungsdatum:**. Oktober 2024

Diese Version umfasst die folgenden neuen Funktionen und Verbesserungen:

| Typ | Element | Beschreibung |
| ---- | ---- | ----------- |
| Verbesserung | Zentrale Asset-Bibliothek | Mit der erweiterten _Central Assets Library_ können Sie alle Bild-Assets in Ihrer Marketo Engage-Instanz in allen Design Studio-Arbeitsbereichen verwenden. Es gibt integrierte Leitplanken, die Änderungen an den Marketo Engage-Assets von Journey Optimizer B2B edition sowie Löschen- und Verschiebungsvorgänge verhindern. Diese Schutzmaßnahmen stellen sicher, dass die Quell-Assets (Marketo Engage Design Studio) beibehalten werden und gleichzeitig das nahtlose Lesen und Wiederverwenden in Journey Optimizer B2B edition ermöglicht wird.<p>Für Assets, die ausschließlich zur Verwendung in Journey Optimizer B2B edition vorgesehen sind, bietet ein bestimmter Arbeitsbereich sämtliche Asset-Management-Funktionen. <a href="../content/marketo-engage-design-studio.md">Weitere Informationen</a> |
| Neue Funktion | Kürzlich aufgerufene Assets | Die Startseite in der Journey Optimizer B2B edition-App enthält jetzt den Abschnitt _[!UICONTROL Kürzlich aufgerufen]_ mit einer Liste der zuletzt aufgerufenen Assets für den Marketing- oder Administrator. Mit dieser Liste können Sie direkt zu dem Asset gehen, an dem Sie kürzlich gearbeitet haben, ohne durch eine Reihe von Asset-Seiten zu navigieren oder zu suchen. <p>Die Liste enthält zusätzliche Informationen zur Änderung, sodass Sie entscheiden können, welches der Assets weiter geändert werden muss. Bei E-Mail-Assets wird die Konto-Journey angezeigt, auf der das E-Mail-Asset verwendet wird. <a href="../home-page.md">Weitere Informationen</a> |
| Verbesserung | Journey-geteilter Knoten - Pfade neu anordnen | Bei aufgeteilten Pfadknoten wird die Pfadfilterung in der Reihenfolge von oben nach unten ausgewertet. Jede Person oder jedes Konto fährt auf dem ersten Pfad fort, der übereinstimmt. Sie können die Reihenfolge der definierten Pfade ändern, indem Sie auf die Pfeile nach oben und unten oben rechts auf jeder Pfadkarte klicken, um sie in der Liste nach oben oder unten zu verschieben. <a href="../journeys/split-merge-paths-nodes.md#split-paths">Weitere Informationen</a> |
| Verbesserung | Journey-Aufspaltungsknoten - Zusätzliche Bedingungsattribute für den Aktivitätsverlauf | Wenn Sie Bedingungen verwenden, um die Pfadfilterung für einen aufgeteilten Knoten nach Personen zu definieren, gibt es zwei zusätzliche Attribute: _Geöffnete E-_ und _Bereitgestellte E-Mail_. Diese Ergänzungen bieten mehr Flexibilität beim Filtern von Personen im Journey anhand von E-Mail-Aktivitäten. <a href="../journeys/journey-nodes.md#split-paths">Weitere Informationen</a> |

## Versionshinweise für August 2024 {#Aug-2024}

**Veröffentlichungsdatum:**. August 2024

Diese Version umfasst die folgenden neuen Funktionen und Verbesserungen:

| Typ | Element | Beschreibung |
| ---- | ---- | ----------- |
| Neue Funktion | Zugeordnete Zielgruppen des LinkedIn-Kontos | Generieren Sie LinkedIn-Anzeigen-Zielgruppen durch Zielgruppen mit Konto-Matched, damit Sie leere Rollen in Ihren Einkaufsgruppen ausfüllen können. Durch die Definition eines Satzes von Einkaufsgruppenfiltern können Sie eine LinkedIn Matched Audience verwalten, um Interessenten anzusprechen, die Ihren Einkaufsgruppenparametern entsprechen. <p>Diese Funktion nutzt Experience Platform-Ziele, um einige Aspekte der Integration zu verwalten. <a href="../data/linkedin-account-matched-audiences.md">Weitere Informationen</a> |
| Verbesserung | Statuslebenszyklus für visuelle Inhaltsfragmente | Visuelle Fragmente werden jetzt mithilfe eines Status-Lebenszyklus verwaltet. Der Fragmentstatus bestimmt seine Verfügbarkeit zur Verwendung in einer E-Mail oder E-Mail-Vorlage und die Änderungen, die Sie daran vornehmen können. <p>Dieser erweiterte Workflow erleichtert die Verwaltung wiederverwendeter Inhalte entsprechend Ihrem Werbe- und Kommunikationskalender. <a href="../content/fragments.md#fragment-status-and-lifecycle">Weitere Informationen</a> |
