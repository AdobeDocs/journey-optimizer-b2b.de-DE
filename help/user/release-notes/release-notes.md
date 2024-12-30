---
title: Versionshinweise
description: Neueste Versionshinweise für Adobe Journey Optimizer B2B Edition
exl-id: 7d3f1c26-d8a6-4065-a70f-5b30cb975dc8
source-git-commit: 18a9f073f5c898d01c075611c6808d192d71dbc7
workflow-type: tm+mt
source-wordcount: '895'
ht-degree: 10%

---

# Versionshinweise zu Journey Optimizer B2B edition

Adobe Journey Optimizer B2B edition bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen.

Journey Optimizer B2B edition basiert nativ auf [!DNL Adobe Experience Platform] und profitiert von den neuesten Innovationen und Verbesserungen von Platform. Weitere Informationen zu diesen Änderungen finden Sie unter [Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/release-notes/latest){target="_blank"}.

Lesen Sie die [Produktbeschreibung](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"}, um Informationen über Berechtigungen, Leistungsschutzmechanismen und Einschränkungen zu erhalten.

## Versionshinweise für Oktober 2024 {#Oct-2024}

**Veröffentlichungsdatum:**. Oktober 2024

Diese Version umfasst die folgenden neuen Funktionen und Verbesserungen:

| Typ | Element | Beschreibung |
| ---- | ---- | ----------- |
| Neue Funktion | Bedingte Inhalte in E-Mail-Vorlagen | Personalisieren Sie Ihren E-Mail-Inhalt basierend auf dem Verhalten und den Profilmerkmalen der Empfänger - sowohl auf Konto- als auch auf Lead-Ebene. <p>Verwenden Sie beim Erstellen einer E-Mail für Ihr Konto-Journey im E-Mail-Designer bedingte Regeln, um mehrere Varianten für Inhaltskomponenten zu definieren. <a href="../content/conditional-content.md">Weitere Informationen</a> |
| Neue Funktion | _Zu Liste hinzufügen_ und _Aus Liste entfernen_ Personalaktionen in Journey | Personalisieren Sie Ihren E-Mail-Inhalt basierend auf dem Verhalten und den Profilmerkmalen der Empfänger - sowohl auf Konto- als auch auf Lead-Ebene. <a href="../journeys/journey-nodes.md#action-nodes">Weitere Informationen</a> |
| Neue Funktion | Content Governance und Komponentensperrung | Um die Einhaltung genehmigter Inhaltsentwürfe sicherzustellen, verwenden Sie Content-Governance-Funktionen zum Sperren von Inhaltskomponenten für E-Mail-Vorlagen. Wenn die Content Governance in der E-Mail-Vorlage aktiviert ist, können Marketing-Experten nur die zulässigen Elemente ändern, um sie an die Inhaltsstrategie anzupassen. <a href="../content/template-content-governance.md">Weitere Informationen</a> |
| Neue Funktion | Käufergruppenphasen | Wenn Sie ein benutzerdefiniertes Einkaufsgruppen-Staging-Modell definieren und veröffentlichen, können Sie den Fortschritt der Einkaufsgruppe über die Lebenszyklusphasen der Einkaufsgruppe verfolgen. Verwenden Sie diese Schritte, um die nächste beste Aktion für Käufergruppenmitglieder zu ermitteln. Sie konfigurieren die Übergangsregeln und Journey-Knoten, die den Staging-Fortschritt und die Trigger-Aktionen basierend auf Änderungen bestimmen. <a href="../buying-groups/buying-group-stages.md">Weitere Informationen</a> |
| Verbesserung | Neue vordefinierte E-Mail-Vorlagen | Die Bibliothek mit Beispielvorlagen enthält jetzt zusätzliche E-Mail-Vorlagen, die für B2B-Marketing-Fachleute entwickelt wurden. Verwenden Sie diese Beispielvorlagen als Ausgangspunkt und fügen Sie Ihr eigenes Branding und Messaging hinzu. <a href="../content/email-templates.md#select-a-design-template">Weitere Informationen</a> |
| Verbesserung | Benutzerdefinierte Felder als Personenattribute | Wenn Sie benutzerdefinierte Personenfelder im Konto-Zielgruppenschema auf Experience Platform definiert haben, sind diese Felder auch verfügbar, um als Personenattribute in Bedingungen zu verwenden. Verwenden Sie diese benutzerdefinierten Attribute in: <li>Rollenvorlagen <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Weitere Informationen</a></li><li>Pfade nach Personen-Journey-Knoten aufteilen <a href="../journeys/journey-nodes.md#add-a-split-path-by-people-node">Weitere Informationen</a></li> |
| Verbesserung | E-Mail-Kanaleinstellungen | E-Mail-Einstellungen sind jetzt in der Benutzeroberfläche von Journey Optimizer B2B edition sichtbar. Sie können die aktuellen Konfigurationen schnell überprüfen und Administratoren können auf _[!UICONTROL Einstellungen bearbeiten]_ klicken, um direkt zu den Einstellungen in Marketo Engage zu wechseln und sie entsprechend den Anforderungen Ihres Unternehmens zu aktualisieren. <a href="../admin/configure-channels-emails.md">Weitere Informationen</a> |

## Versionshinweise für September 2024 {#Sept-2024}

**Veröffentlichungsdatum:**. Oktober 2024

Diese Version umfasst die folgenden neuen Funktionen und Verbesserungen:

| Typ | Element | Beschreibung |
| ---- | ---- | ----------- |
| Verbesserung | Zentrale Asset-Bibliothek | Mit der erweiterten _Central Assets Library_ können Sie alle Bild-Assets in Ihrer Marketo Engage-Instanz in allen Design Studio-Arbeitsbereichen verwenden. Es gibt integrierte Leitplanken, die Bearbeitungen an den Marketo Engage-Assets von Journey Optimizer B2B edition sowie Lösch- und Verschiebungsvorgänge verhindern. Diese Schutzmaßnahmen stellen sicher, dass die Quell-Assets (Marketo Engage Design Studio) beibehalten werden und gleichzeitig das nahtlose Lesen und Wiederverwenden in Journey Optimizer B2B edition ermöglicht wird.<p>Für Assets, die ausschließlich zur Verwendung in Journey Optimizer B2B edition vorgesehen sind, bietet ein bestimmter Arbeitsbereich sämtliche Asset-Management-Funktionen. <a href="../content/marketo-engage-design-studio.md">Weitere Informationen</a> |
| Neue Funktion | Kürzlich aufgerufene Assets | Die Startseite in der Journey Optimizer B2B edition-App enthält jetzt den Abschnitt _[!UICONTROL Kürzlich aufgerufen]_ mit einer Liste der zuletzt aufgerufenen Assets für den Marketing- oder Administrator. Mit dieser Liste können Sie direkt zu dem Asset gehen, an dem Sie kürzlich gearbeitet haben, ohne durch eine Reihe von Asset-Seiten zu navigieren oder zu suchen. <p>Die Liste enthält zusätzliche Informationen zur Änderung, sodass Sie entscheiden können, welches der Assets weiter geändert werden muss. Bei E-Mail-Assets wird die Konto-Journey angezeigt, auf der das E-Mail-Asset verwendet wird. <a href="../home-page.md">Weitere Informationen</a> |
| Verbesserung | Journey-geteilter Knoten - Pfade neu anordnen | Bei aufgeteilten Pfadknoten wird die Pfadfilterung in der Reihenfolge von oben nach unten ausgewertet. Jede Person oder jedes Konto fährt auf dem ersten Pfad fort, der übereinstimmt. Sie können die Reihenfolge der definierten Pfade ändern, indem Sie auf die Pfeile nach oben und unten oben rechts auf jeder Pfadkarte klicken, um sie in der Liste nach oben oder unten zu verschieben. <a href="../journeys/journey-nodes.md#split-paths">Weitere Informationen</a> |
| Verbesserung | Journey-Aufspaltungsknoten - Zusätzliche Bedingungsattribute für den Aktivitätsverlauf | Wenn Sie Bedingungen verwenden, um die Pfadfilterung für einen aufgeteilten Knoten nach Personen zu definieren, gibt es zwei zusätzliche Attribute: _Geöffnete E-_ und _Bereitgestellte E-Mail_. Diese Ergänzungen bieten mehr Flexibilität beim Filtern von Personen im Journey anhand von E-Mail-Aktivitäten. <a href="../journeys/journey-nodes.md#split-paths">Weitere Informationen</a> |

## Versionshinweise für August 2024 {#Aug-2024}

**Veröffentlichungsdatum:**. August 2024

Diese Version umfasst die folgenden neuen Funktionen und Verbesserungen:

| Typ | Element | Beschreibung |
| ---- | ---- | ----------- |
| Neue Funktion | Vom linkedIn-Konto abgeglichene Zielgruppen | Generieren von LinkedIn-Anzeigen-Zielgruppen durch Zielgruppen mit Konto-Matched, damit Sie leere Rollen in Ihren Einkaufsgruppen ausfüllen können. Durch die Definition eines Satzes von Einkaufsgruppenfiltern können Sie eine von LinkedIn übereinstimmende Zielgruppe verwalten, um Interessenten anzusprechen, die Ihren Einkaufsgruppenparametern entsprechen. <p>Diese Funktion nutzt Experience Platform-Ziele, um einige Aspekte der Integration zu verwalten. <a href="../data/linkedin-account-matched-audiences.md">Weitere Informationen</a> |
| Verbesserung | Statuslebenszyklus für visuelle Inhaltsfragmente | Visuelle Fragmente werden jetzt mithilfe eines Status-Lebenszyklus verwaltet. Der Fragmentstatus bestimmt seine Verfügbarkeit zur Verwendung in einer E-Mail oder E-Mail-Vorlage und die Änderungen, die Sie daran vornehmen können. <p>Dieser erweiterte Workflow erleichtert die Verwaltung wiederverwendeter Inhalte entsprechend Ihrem Werbe- und Kommunikationskalender. <a href="../content/fragments.md#fragment-status-and-lifecycle">Weitere Informationen</a> |
