---
title: Versionshinweise zu Journey Optimizer B2B Edition
description: Die neuesten Funktionen und Verbesserungen in Adobe Journey Optimizer B2B Edition.
role: User, Admin
exl-id: 7d3f1c26-d8a6-4065-a70f-5b30cb975dc8
source-git-commit: dfd426f6d658a9340c531231e7180cbc215b65f9
workflow-type: tm+mt
source-wordcount: '2552'
ht-degree: 85%

---

# Versionshinweise zu Journey Optimizer B2B Edition

Adobe Journey Optimizer B2B Edition bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. 

Journey Optimizer B2B Edition setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von dessen neuesten Innovationen und Verbesserungen. Weitere Informationen zu diesen Änderungen finden Sie in den [Versionshinweisen zu Adobe Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/release-notes/latest){target="_blank"}.

Lesen Sie die [Produktbeschreibung](https://helpx.adobe.com/de/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"}, um Informationen über Berechtigungen, Leitlinien für die Leistung und Einschränkungen zu erhalten.
<!-- hold for 2025.8 release 

| Feature | Landing pages | You can now create and publish landing pages in Journey Optimizer B2B Edition to support your journeys and programs. _(Previously a Beta program feature.)_ [Learn more](../content/landing-pages.md) |
| Feature | Forms | You can now create and publish re-usable form components to enable data submission from landing pages that are created and published in Journey Optimizer B2B Edition. _(Previously a Beta program feature.)_ [Learn more](../content/forms.md) |

-->

## Versionshinweise für 2025.6

**Bereitstellungsdatum**: Mittwoch, 15. Juli 2025

Diese Version umfasst die folgenden neuen Funktionen und Verbesserungen:

| Typ | Element | Beschreibung |
| ---- | ---- | ----------- |
| Funktion | Integration mit GenStudio for Performance Marketing | (Eingeschränkte Verfügbarkeit) E-Mail-Erlebnisse in GenStudio for Performance Marketing können jetzt mit Journey Optimizer B2B Edition integriert werden, um die Marketing-Effizienz zu steigern und die Markenkonsistenz zu gewährleisten. Diese Integration kombiniert die KI-gestützte Inhaltserstellung von GenStudio mit den erweiterten Orchestrierungsfunktionen in Journey Optimizer B2B Edition. [Weitere Informationen](../content/genstudio-email-workflow.md) |
| Funktion | Spam-Erkennungsberichte | Um Spam-Filter zu vermeiden und sicherzustellen, dass Nachrichten an Zielgruppen-Posteingänge gesendet werden, können Sie _Spam-Bericht_ direkt im E-Mail-Design-Bereich erstellen. [Weitere Informationen](../content/email-spam-report.md) |
| Funktion | Seite „Personendetails“ | Sie können jetzt auf den Namen einer Person klicken, wenn er (als Hyperlink) im Intelligenten Dashboard, auf der Seite mit den Einkaufsgruppendetails und auf der Seite mit den Kontodetails angezeigt wird. Diese Aktion öffnet die Seite mit den zugehörigen Personendetails, auf der Informationen zum Kontakt, zu seiner Aktivität und zu den aktivsten Einkaufsgruppen angezeigt werden. [Weitere Informationen](../accounts/person-details.md) |
| Funktion | Konto- und Einkaufsgruppenaktionen | Ergreifen Sie Aktionen direkt auf den Seiten „Kontodetails“ und „Einkaufsgruppendetails“, um rechtzeitig und vorsätzlich mit Ihnen zu interagieren. <li>Verwenden Sie die Aktion _E-Mail senden_, um eine genehmigte Marketo Engage-E-Mail an ausgewählte Kontokontakte oder Mitglieder der Einkaufsgruppe zu senden. [Weitere Informationen](../accounts/account-details.md#send-emails) <li>Zu den Aktionen in den Details der Einkaufsgruppe gehören auch _Neues Mitglied zuweisen_, _Mitglied entfernen_ und _Rolle bearbeiten_. [Weitere Informationen](../buying-groups/buying-group-details.md#members-tab) |
| Funktion | In-CRM-Zugriff auf Detailseiten | Sie können jetzt direkte Links zu Journey Optimizer B2B edition-Detailseiten für Konten, Kontakte und Leads in Ihrem CRM-Tool (Customer Relationship Management) konfigurieren, z. B. Salesforce oder Microsoft Dynamics. [Weitere Informationen](../accounts/crm-linking.md) |
| Funktion | Benutzerdefinierte CSS-Unterstützung für das Content-Design | Sie können jetzt Ihr eigenes benutzerdefiniertes CSS hinzufügen, wenn Sie E-Mail- und Landingpage-Inhalte im Design-Bereich erstellen. [Weitere Informationen](../content/design-custom-css.md) |
| Funktion | Konfiguration der Intent-Schlüsselwortzuordnung | Um das Modell zur Absichtserkennung zu aktivieren und zu verwalten, können Sie jetzt eine Tabelle hochladen, um eine Absichtsdaten-Mapping-Kategorie zu definieren. [Weitere Informationen](../admin/intent-data.md) |
| Verbesserung | Inhalt aus E-Mail-Zusammenfassung simulieren | Sie können jetzt über die E _Mail-Zusammenfassung (Details und Eigenschaften) auf die Tools_ Inhalt simulieren) zugreifen, wenn Sie eine E-Mail über die E-Mail-Liste öffnen. Dieser Zugriff ergänzt den E-Mail-Design-Bereich. [Weitere Informationen](../content/email-simulate-content.md#display-the-email-preview) |
| Verbesserung | Anzeige der Gesamtzahl für die Liste der Rollenvorlagen | Die _[!UICONTROL Rollenvorlagen]_ Listenseite wird um die Gesamtanzahl neben der Suchleiste erweitert. |

<!-- The following capabilities are currently available only for a set of program participants (Beta):

**Brand Kit with AI Assistant** - Maintain brand consistency across email assets by storing and managing brand assets. Add assets, such as colors, fonts, logos, themes, visual content, and compliance guidelines, and use them for your generative AI content creation. -->

## Versionshinweise für 2025.5

**Bereitstellungsdatum**: 3. Juni 2025

Diese Version umfasst die folgenden neuen Funktionen und Verbesserungen:

| Typ | Element | Beschreibung |
| ---- | ---- | ----------- |
| Funktion | E-Mail-Tests mit Litmus | Mit einem [Litmus Enterprise-Konto](https://www.litmus.com/email-testing){target="_blank"} können Sie jetzt das E-Mail-Rendering in gängigen E-Mail-Clients von Journey Optimizer B2B edition aus in der Vorschau anzeigen. Durch diese Integration können Sie sicherstellen, dass Ihr E-Mail-Inhalt in jedem E-Mail-Posteingang gut aussieht und wie vorgesehen funktioniert. [Weitere Informationen](../content/email-test-rendering.md) |
| Verbesserung | E-Mail duplizieren | Beim Hinzufügen einer E-Mail für einen Journey-Knoten können Sie jetzt eine vorhandene E-Mail duplizieren. Ändern Sie die Einstellung oder den Inhalt für die duplizierte E-Mail oder lassen Sie sie intakt.  [Weitere Informationen](../content/add-email.md#add-an-email-to-your-journey) |
| Verbesserung | Handlebar-Token-Format für E-Mail | Personalisierungs-Token für E-Mail-Inhalte verwenden jetzt ein aktualisiertes Format, das vollständig mit Handlebar-Scripting kompatibel ist. Dieses Format verwendet _Binnenmajuskel-Schreibweise_ oder Unterstriche, wobei Leerzeichen eliminiert werden. [Weitere Informationen](../content/email-authoring.md#content-authoring---personalization) |
| Verbesserung | Anzeige der Gesamtzahl der Listen | Die Listenseiten für _[!UICONTROL Lösungsinteressen]_ und _[!UICONTROL Konto-Journeys]_ werden durch die Anzeige der Gesamtanzahl neben der Suchleiste erweitert. |

## Versionshinweise für 2025.4

**Bereitstellungsdatum**: 29. April 2025

Diese Version umfasst die folgenden neuen Funktionen und Verbesserungen:

| Typ | Element | Beschreibung |
| ---- | ---- | ----------- |
| Funktion | Kontolisten | Sie können nun eine statische oder dynamische Kontoliste erstellen, um benannte Konten anhand der von Ihnen definierten Kriterien wie Branche, Standort oder Größe des Unternehmens auszuwählen. <a href="../accounts/account-lists.md">Weitere Informationen</a> |
| Funktion | Journey-Orchestrierung der Kontoliste | Verwenden Sie den Knoten „Journey-Aktion“, um Konten für statische Kontolisten hinzuzufügen und zu entfernen. <a href="../accounts/account-lists-journeys.md#take-an-action-node---add-to-account">Weitere Informationen</a> |
| Verbesserung | Filtern der Journey-Mitgliedschaft in Marketo Engage | Verwenden Sie Kontolisten in Adobe Journey Optimizer B2B Edition für die Journey-Zielgruppe und verwenden Sie dann den Filter _Mitglied einer Kontoliste_ in intelligenten Listen in Marketo Engage. <a href="../accounts/account-lists-journeys.md#marketo-engage-program---member-of-account-list">Weitere Informationen</a> |
| Funktion | Inaktivitätsfilter | Orchestrieren Sie Journeys auf der Grundlage von Inaktivität innerhalb von Marketo Engage-Kampagnen und -Programmen, einschließlich E-Mail-Inaktivität, interessanten Momenten, Änderungen des Datenwerts und besuchten Web-Seiten. <a href="../journeys/split-merge-paths-nodes.md#activity-filtering">Weitere Informationen</a> |
| Verbesserung | Filter für besuchte Web-Seiten | Orchestrieren Sie Journeys basierend auf der Aktivität für besuchte Web-Seiten, die mit Marketo Engage-Kampagnen und -Programmen verknüpft sind. <a href="../journeys/split-merge-paths-nodes.md#people-path-conditions">Weitere Informationen</a> |
| Verbesserung | E-Mail-Liste | Zeigen Sie eine globale Liste der aktiven E-Mails und der E-Mail-Entwürfe an, um sie in den zugehörigen Konto-Journeys zu suchen, zu überprüfen und zu aktualisieren. <a href="../content/emails-list.md">Weitere Informationen</a> |

## Versionshinweise für 2025.3

**Bereitstellungsdatum**: 1. April 2025

Diese Version umfasst die folgenden neuen Funktionen und Verbesserungen:

| Typ | Element | Beschreibung |
| ---- | ---- | ----------- |
| Funktion | Duplizieren von Konto-Journeys | Für Konto-Journeys ist jetzt eine Aktion zum Duplizieren verfügbar. Sie können die Details für die Konto-Journey duplizieren oder einfach nur eine simple Basis der Fluss- und Pfadstruktur duplizieren. <a href="../journeys/journey-overview.md#duplicate-journey">Weitere Informationen</a> |
| Funktion | Meine Token für Konto-Journeys | Sie können jetzt einen Satz benutzerdefinierter Token mit Werten definieren, die für die Konto-Journey spezifisch sind. Dieser Satz benutzerdefinierter Token wird unter _Meine Token_ zusammengefasst. Jedes dieser benutzerdefinierten Token dient bei der Erstellung von Journey-E-Mails zur Personalisierung. <a href="../content/personalization-my-tokens.md">Weitere Informationen</a> |
| Funktion | Löschen von Käufergruppenphasen | Sie können das Modell der Käufergruppenphasen löschen, wenn es sich im Status „Entwurf“ oder „Veröffentlicht“ befindet. Falls es veröffentlicht (live) ist, können Sie es nur löschen, wenn es nicht mit einem Lösungsinteresse verbunden ist. <a href="../buying-groups/buying-group-stages.md#delete-the-buying-group-stages-model">Weitere Informationen</a> |
| Verbesserung | Journey-Knotenanzahl | Verbesserte Sichtbarkeit der Anzahl der veröffentlichten Journey-Zugehörigkeiten auf Knotenebene. In der _Journey Map_ zeigen Knoten die _[!UICONTROL Gesamtzahl der eingetretenen Konten]_ an. Wenn Sie einen Knoten auswählen und dafür eine Aktion ausführen, umfassen die Details auf der rechten Seite auch die _[!UICONTROL Konten, für die noch keine Aktion ausgeführt wurde]_. Zu den Details für Knoten vom Typ _Auf ein Ereignis lauschen_ gehören _[!UICONTROL Konten bei diesem Schritt]_. Verwenden Sie diese Informationen, um den Kontofortschritt in Ihren Live-Journeys sowie abgeschlossenen und abgebrochenen Journeys zu überprüfen. |

## Versionshinweise für 2025.2

**Bereitstellungsdatum**: 11. März 2025

Diese Version umfasst die folgenden neuen Funktionen und Verbesserungen:

| Typ | Element | Beschreibung |
| ---- | ---- | ----------- |
| Funktion | Anpassbare Felder – Inhaltsfragmente | Während Sie visuelle Fragmente designen, können Sie Parameter für eine Komponente im Fragment als bearbeitbar festlegen. Diese Funktion ermöglicht es der Autorin bzw. dem Autor der E-Mail oder Vorlage, einen benutzerdefinierten Feldwert anzugeben, der speziell für ihre bzw. seine Anforderungen gilt. Diese Anpassungsmarkierung ist auf visuelle Bild-, Text- und Schaltflächenkomponenten beschränkt. <a href="../content/fragment-authoring.md#enable-fragment-customization">Weitere Informationen</a> |
| Funktion | Journey-Duplizierungstypen | Wenn Sie eine Konto-Journey duplizieren, können Sie Knotendetails einbeziehen, mit Ausnahme von in Journey Optimizer B2B Edition erstellten E-Mails und SMS-Nachrichten. Als Alternative können Sie eine Basiskopie der Struktur- und Pfadflüsse erstellen (ohne Knotendetails und Einstellungen). <a href="../journeys/journey-overview.md#duplicate-journey">Weitere Informationen</a> |
| Verbesserung | Vier zusätzliche Beispielvorlagen für E-Mails | Die Bibliothek mit Beispielvorlagen für E-Mails enthält jetzt vier SecurFinancial-Vorlagen als Beispiele für die Wiederaufnahme von Interaktionen, Informieren, Pflegen und Feedback-Inhalte |

<!-- | Feature | B2B built-in roles and product permissions | Experience Platform now includes a set of built-in (default) roles that you can use to manage access to the B2B product capabilities. <a href="../admin/user-management.md#b2b-built-in-roles">Learn more</a> <br/>Administrators can now define custom roles in Adobe Experience Platform to include Journey Optimizer B2B Edition product permissions.  <a href="../admin/user-management.md#b2b-product-permissions">Learn more</a> | -->

## Versionshinweise für 2025.1 {#Jan-2025}

**Bereitstellungsdatum**: 6. Februar 2025

Diese Version umfasst die folgenden neuen Funktionen und Verbesserungen:

| Typ | Element | Beschreibung |
| ---- | ---- | ----------- |
| Funktion | Weiterleitung von Erlebnisereignissen | Admins können die auf Adobe Experience Platform (AEP) basierenden Ereignisdefinitionen konfigurieren. Mit diesen Konfigurationen können Marketing-Fachleute Konto-Journeys erstellen, die auf Erlebnisereignissen aus AEP reagieren. <a href="../admin/configure-aep-events.md">Weitere Informationen</a> |
| Funktion | Paid Media-Ziele | Qualifizieren Sie bekannte Personen für Paid Media-Kampagnen von einer Konto-Journey aus, damit Sie auf Werbeplattformen wie LinkedIn weiter mit ihnen interagieren können. Verwenden Sie einen Knoten vom Typ „Pfad aufteilen“ in einer Konto-Journey, um Konto-Zielgruppen basierend auf bestimmten Verhaltensweisen zu segmentieren und Konten zu identifizieren, die zusätzliche Interaktionen gewährleisten. Fügen Sie dann Personen aus diesen Konten über Real-Time CDP zu einer externen Kundenzielgruppe für ein unterstütztes Paid Media-Ziel hinzu. <a href="../journeys/action-nodes.md#journey-optimizer-b2b-actions">Weitere Informationen</a> |
| Funktion | Intelligentes Dashboard | Sehen Sie sich den Fortschritt von Käufergruppen durch ihre Konto-Journey an, einschließlich KI-generierter Erkenntnisse, um eine intelligentere Analyse und eine genauere Priorisierung von Konten zu erhalten. <a href="../dashboards/intelligent-dashboard.md">Weitere Informationen</a> |
| Funktion | Details zu Käufergruppen und Konten | Sehen Sie sich Erkenntnisse auf der Käufergruppen- und Kontoebene an, um zu Beginn der Interaktion mit einer Kundin oder einem Kunden mehr Kontext- und historische Daten zu erhalten.<p>Zu den Details der Käufergruppe gehören alle erkannten First-Party-Intent-Daten. <a href="../buying-groups/buying-group-details.md">Weitere Informationen</a><p>Die Konten mit den Kontodetails zeigen den beobachteten Anstieg der Interaktionsabsicht, sodass Sie Ihren Vertrieb auf Konten hinweisen können, die für eine kundenspezifische, verkaufsorientierte Interaktion bereit sind.  <a href="../accounts/account-details.md">Weitere Informationen</a> |
| Funktion | Journey-Überblick | Wenn Sie auf Konto-Journeys zugreifen, bietet die Registerkarte „Überblick“ eine umfassende Übersicht über Ihre aktiven Konto-Journeys mit detaillierten Fortschrittsanzeigen zu Konten, in denen Abschlüsse und Interaktionsaktivitäten anhand von Kreis- und Balkendiagrammen kategorisiert und quantifiziert werden.  <a href="../dashboards/journeys-dashboard.md">Weitere Informationen</a> |
| Funktion | Bildbearbeitung in Adobe Express | Schnellaktionen in Adobe Express ermöglichen Ihnen einfache Bearbeitungen (z. B. Zuschneiden und Ändern der Größe) von Bildern, um das Erscheinungsbild Ihrer Inhalte zu verbessern. <a href="../content/image-edit-adobe-express.md#quick-actions-in-adobe-express">Weitere Informationen</a>  <p>Für einen umfassenderen Satz an Design-Tools ermöglicht diese Integration eine Adobe Express-Volllizenz in Journey Optimizer B2B Edition. Mit dieser Einrichtung wird die gesamte Adobe Express-Benutzeroberfläche im lokalen Asset-Arbeitsbereich verfügbar. <a href="../content/image-edit-adobe-express.md#adobe-express-enterprise-license">Weitere Informationen</a> |
| Funktion | Absichtsfilter für Käufergruppenrollen | Wenn Sie Ihre Absichtsschlüsselwörter übermitteln, sagt das Absichtserkennungsmodell eine Lösung/ein Produkt von Interesse basierend auf der Aktivität eines Leads mit ausreichend hoher Zuverlässigkeit voraus. <a href="../admin/intent-data.md">Weitere Informationen</a> <p>Diese Absichtsdaten stehen für die Definition der Bedingungen für die Käufergruppenrolle zur Verfügung <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Weitere Informationen</a> |
| Verbesserung | Marketo Engage-Ereignisunterstützung in Journeys | Der Journey-Knoten _Auf Ereignis lauschen_ unterstützt jetzt zwei Marketo Engage-Ereignisse auf Personenebene: _Besucht Webseite_ und _Füllt Formular aus_. <a href="../journeys/listen-for-event-nodes.md#listen-for-marketo-engage-event">Weitere Informationen</a> |
| Verbesserung | Käufergruppenfilter für intelligente Listen in Marketo Engage | Sie können in Marketo Engage intelligente Listen mit Käufergruppenfiltern anzeigen und erstellen. Mit diesen hinzugefügten Filtern können Sie Mitglieder von Käufergruppen in allen Marketo Engage-Kampagnen und -Programmen über die Konto-Journeys in Journey Optimizer B2B Edition unterdrücken und einbeziehen. <a href="../buying-groups/marketo-engage-smart-list-buying-group-filters.md">Weitere Informationen</a> |
| Verbesserung | Mitgliedschaftsfilter für Marketo Engage-Listen für Journeys und Rollen | Aktivieren Sie die Marketo Engage-Listenmitgliedschaft in Journey Optimizer B2B als Bedingung für einen Knoten _Pfad nach Personen aufteilen_, um doppelte Journey-Aktivitäten zu vermeiden. <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">Weitere Informationen</a> <p> Verwenden Sie die Listenmitgliedschaft als Rollenbedingung für Rollenvorlagen für Käufergruppen. <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Weitere Informationen</a> |
| Verbesserung | Dashboard für den Überblick über die Interaktion | Dieses Dashboard wurde aktualisiert, um eine umfassende Interaktionsansicht zu bieten. Es zeigt Echtzeitmetriken der Interaktionen von Konten und Einzelpersonen durch Kreisdiagramme von Momentaufnahmen und Liniendiagramme, die Trends aufzeigen, im Zeitverlauf an. <a href="../dashboards/engagement-dashboard.md">Weitere Informationen</a> |

## Versionen 2024

Erweitern Sie die folgenden Listen, um die Funktionen und Verbesserungen aus der 2024 veröffentlichen Version von Journey Optimizer B2B Edition anzuzeigen.

+++Versionshinweise für Oktober 2024

**Bereitstellungsdatum**: 29. Oktober 2024

Diese Version umfasst die folgenden neuen Funktionen und Verbesserungen:

| Typ | Element | Beschreibung |
| ---- | ---- | ----------- |
| Funktion | Sperren von bedingten Inhalten in E-Mail-Vorlagen | Personalisieren Sie Ihre E-Mail-Inhalte basierend auf dem Verhalten und den Profilmerkmalen der Empfängerinnen und Empfänger – sowohl auf Konto- als auch auf Lead-Ebene. <p>Verwenden Sie bedingte Regeln beim Erstellen einer E-Mail für Ihre Konto-Journey im visuellen Design-Bereich der E-Mail, um mehrere Varianten für Inhaltskomponenten zu definieren. <a href="../content/conditional-content.md">Weitere Informationen</a> |
| Funktion | Personenaktionen _Zu Liste hinzufügen_ und _Aus Liste entfernen_ | Personalisieren Sie Ihre E-Mail-Inhalte basierend auf dem Verhalten und den Profilmerkmalen der Empfängerinnen und Empfänger – sowohl auf Konto- als auch auf Lead-Ebene. <a href="../journeys/action-nodes.md">Weitere Informationen</a> |
| Funktion | Content-Governance und Komponentensperrung | Um die Einhaltung genehmigter Inhaltsentwürfe sicherzustellen, verwenden Sie Content-Governance-Funktionen, um Inhaltskomponenten für E-Mail-Vorlagen zu sperren. Wenn die Content-Governance in der E-Mail-Vorlage aktiviert ist, können Marketing-Fachleute nur die zulässigen Elemente ändern, um sie an die Inhaltsstrategie anzupassen. <a href="../content/template-content-governance.md">Weitere Informationen</a> |
| Funktion | Käufergruppenphasen | Wenn Sie ein benutzerdefiniertes Käufergruppenphasenmodell definieren und veröffentlichen, können Sie den Fortschritt der Käufergruppe über die Lebenszyklusphasen der Käufergruppe hinweg verfolgen. Verwenden Sie diese Phasen, um die nächsten optimalen Aktionen für Käufergruppenmitglieder zu ermitteln. Sie konfigurieren die Übergangsregeln und Journey-Knoten, die den Fortschritt in der Phase festlegen und Aktionen basierend auf Änderungen auslösen. <a href="../buying-groups/buying-group-stages.md">Weitere Informationen</a> |
| Verbesserung | Neue vordefinierte E-Mail-Vorlagen | Die Bibliothek mit Beispielvorlagen enthält jetzt zusätzliche E-Mail-Vorlagen, die für B2B-Marketing-Fachleute entwickelt wurden. Verwenden Sie diese Beispielvorlagen als Ausgangspunkt und fügen Sie Ihr eigenes Branding und Ihr eigene Botschaft hinzu. <a href="../content/email-templates.md#select-a-design-template">Weitere Informationen</a> |
| Verbesserung | Benutzerdefinierte Felder als Personenattribute | Wenn Sie benutzerdefinierte Personenfelder im Konto-Zielgruppenschema in Experience Platform definiert haben, können diese Felder auch als Personenattribute in Bedingungen verwendet werden. Verwenden Sie diese benutzerdefinierten Attribute in: <li>Rollenvorlagen <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Weitere Informationen</a></li><li>Journey-Knoten vom Typ „Pfade nach Personen aufteilen“ <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">Weitere Informationen</a></li> |
| Verbesserung | Einstellungen für den E-Mail-Kanal | E-Mail-Einstellungen sind jetzt in der Benutzeroberfläche von Journey Optimizer B2B Edition sichtbar. Sie können die aktuellen Konfigurationen schnell überprüfen. Admins können dann auf _[!UICONTROL Einstellungen bearbeiten]_ klicken, um direkt zu den Einstellungen in Marketo Engage zu wechseln und sie entsprechend den Anforderungen Ihrer Organisation zu aktualisieren. <a href="../admin/configure-channels-emails.md">Weitere Informationen</a> |

+++

+++Versionshinweise für September 2024

**Bereitstellungsdatum**: 7. Oktober 2024

Diese Version umfasst die folgenden neuen Funktionen und Verbesserungen:

| Typ | Element | Beschreibung |
| ---- | ---- | ----------- |
| Verbesserung | Zentrale Asset-Bibliothek | Mit der erweiterten _zentralen Assets-Bibliothek_ können Sie alle Bild-Assets in Ihrer Marketo Engage-Instanz in allen Design Studio-Arbeitsbereichen verwenden. Es gibt integrierte Schutzmechnismen, die Änderungen an den Marketo Engage-Assets von Journey Optimizer B2B Edition sowie Lösch- und Verschiebevorgänge verhindern. Diese Schutzmaßnahmen stellen sicher, dass die Quell-Assets (Marketo Engage Design Studio) beibehalten werden und gleichzeitig ein nahtloses Lesen und Wiederverwenden in Journey Optimizer B2B Edition möglich ist.<p>Für Assets, die ausschließlich zur Verwendung in Journey Optimizer B2B Edition vorgesehen sind, werden sämtliche Asset-Management-Funktionen in einem spezifischen Arbeitsbereich bereitgestellt. <a href="../content/marketo-engage-design-studio.md">Weitere Informationen</a> |
| Funktion | Zuletzt aufgerufene Assets | Die Startseite in der Journey Optimizer B2B Edition-Anwendung enthält jetzt den Abschnitt _[!UICONTROL Zuletzt aufgerufen]_ mit einer Liste der zuletzt aufgerufenen Assets für die Marketing-Fachkraft oder die Admins. Mit dieser Liste gelangen Sie direkt zu dem Asset, an dem Sie kürzlich gearbeitet haben, ohne erst durch eine Reihe von Asset-Seiten navigieren oder danach suchen zu müssen. <p>Die Liste enthält zusätzliche Informationen zu der Änderung, sodass Sie entscheiden können, welches der Assets weiter geändert werden muss. Bei E-Mail-Assets wird die Konto-Journey angezeigt, in der das E-Mail-Asset verwendet wird. <a href="../home-page.md">Weitere Informationen</a> |
| Verbesserung | Journey-Knoten vom Typ „Aufteilen“ – Neues Anordnen von Pfaden | Bei Knoten vom Typ „Pfad aufteilen“ wird die Pfadfilterung in der Reihenfolge von oben nach unten ausgewertet. Jede Person oder jedes Konto fährt auf dem ersten Pfad fort, der passt. Sie können die Reihenfolge der definierten Pfade ändern, indem Sie oben rechts auf jeder Pfadkarte auf die Pfeile nach oben und unten klicken, um die Pfade in der Liste nach oben oder unten zu verschieben. <a href="../journeys/split-merge-paths-nodes.md#split-paths">Weitere Informationen</a> |
| Verbesserung | Journey-Knoten vom Typ „Aufteilen“ – Zusätzliche Bedingungsattribute für den Aktivitätsverlauf | Wenn Sie Bedingungen verwenden, um die Pfadfilterung für einen Knoten vom Typ „Aufteilen“ nach Personen zu definieren, gibt es zwei zusätzliche Attribute: _Hat E-Mail geöffnet_ und _War übermittelte E-Mail_. Diese Ergänzungen bieten mehr Flexibilität beim Filtern von Personen in der Journey basierend auf E-Mail-Aktivitäten. <a href="../journeys/journey-nodes.md#split-paths">Weitere Informationen</a> |

+++

+++Versionshinweise für August 2024

**Bereitstellungsdatum**: 29. August 2024

Diese Version umfasst die folgenden neuen Funktionen und Verbesserungen:

| Typ | Element | Beschreibung |
| ---- | ---- | ----------- |
| Funktion | LinkedIn Account Matched Audiences | Generieren Sie LinkedIn-Anzeigezielgruppen über Account Matched Audiences, damit Sie leere Rollen in Ihren Käufergruppen ausfüllen können. Durch die Definition eines Satzes von Käufergruppenfiltern können Sie eine LinkedIn Matched Audience verwalten, um Interessenten anzusprechen, die Ihren Käufergruppenparametern entsprechen. <p>Diese Funktion nutzt Experience Platform-Ziele, um einige Aspekte der Integration zu verwalten. <a href="../data/linkedin-account-matched-audiences.md">Weitere Informationen</a> |
| Verbesserung | Statuslebenszyklus für visuelle Inhaltsfragmente | Visuelle Fragmente werden jetzt mithilfe eines Statuslebenszyklus verwaltet. Der Fragmentstatus bestimmt seine Verfügbarkeit zur Verwendung in einer E-Mail oder E-Mail-Vorlage und die Änderungen, die Sie daran vornehmen können. <p>Dieser erweiterte Workflow erleichtert es Ihnen, wiederverwendete Inhalte entsprechend Ihrem Werbe- und Kommunikationskalender zu verwalten. <a href="../content/fragments.md#fragment-status-and-lifecycle">Weitere Informationen</a> |

+++
