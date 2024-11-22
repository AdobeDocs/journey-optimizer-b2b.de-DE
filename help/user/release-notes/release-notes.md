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

Journey Optimizer B2B edition basiert nativ auf [!DNL Adobe Experience Platform] und übernimmt die neuesten Innovationen und Verbesserungen. Weitere Informationen zu diesen Änderungen finden Sie unter [Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/release-notes/latest){target="_blank"}.

Informationen zu Berechtigungen, Leistungsgarantien und Einschränkungen finden Sie in der [Produktbeschreibung](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} .

## Versionshinweise für Oktober 2024 {#Oct-2024}

**Veröffentlichungsdatum**: 29. Oktober 2024

Diese Version umfasst die folgenden neuen Funktionen und Erweiterungen:

| Typ | Element | Beschreibung |
| ---- | ---- | ----------- |
| Neue Funktion | Bedingter Inhalt in E-Mail-Vorlagen | Personalisieren Sie Ihren E-Mail-Inhalt auf der Basis des Empfängerverhaltens und der Profilmerkmale - sowohl auf Konto- als auch auf Lead-Ebene. <p>Wenn Sie eine E-Mail für Ihre Konto-Journey im E-Mail-Designer erstellen, verwenden Sie Bedingungsregeln, um mehrere Varianten für jede Inhaltskomponente zu definieren. <a href="../content/conditional-content.md">Weitere Informationen</a> |
| Neue Funktion | Benutzeraktionen für die Aktionen _Zu Liste hinzufügen_ und _Aus Liste entfernen_ in Journey | Personalisieren Sie Ihren E-Mail-Inhalt auf der Basis des Empfängerverhaltens und der Profilmerkmale - sowohl auf Konto- als auch auf Lead-Ebene. <a href="../journeys/journey-nodes.md#action-nodes">Weitere Informationen</a> |
| Neue Funktion | Content Governance und Komponentensperrung | Um die Einhaltung genehmigter Inhaltsentwürfe sicherzustellen, verwenden Sie Content Governance-Funktionen, um Inhaltskomponenten für E-Mail-Vorlagen zu sperren. Wenn Content Governance in der E-Mail-Vorlage aktiviert ist, können Marketer nur die zulässigen Elemente ändern, um sie an der Inhaltsstrategie auszurichten. <a href="../content/template-content-governance.md">Weitere Informationen</a> |
| Neue Funktion | Käufergruppenphasen | Wenn Sie ein benutzerdefiniertes Testmodell für Einkaufsgruppen definieren und veröffentlichen, können Sie den Fortschritt von Einkaufsgruppen über die Lebenszyklusphasen von Einkaufsgruppen verfolgen. Verwenden Sie diese Schritte, um die nächsten besten Aktionen für den Kauf von Gruppenmitgliedern zu ermitteln. Sie konfigurieren die Übergangsregeln und Journey-Knoten, die die Schrittfortschritt- und Trigger-Aktionen basierend auf Änderungen bestimmen. <a href="../buying-groups/buying-group-stages.md">Weitere Informationen</a> |
| Verbesserung | Neue native E-Mail-Vorlagen | Die Beispielvorlagenbibliothek enthält jetzt zusätzliche E-Mail-Vorlagen, die für B2B-Marketer entwickelt wurden. Verwenden Sie diese Beispielvorlagen als Ausgangspunkt und fügen Sie Ihr eigenes Branding und Ihre eigenen Nachrichten hinzu. <a href="../content/email-templates.md#select-a-design-template">Weitere Informationen</a> |
| Verbesserung | Benutzerdefinierte Felder als Personenattribute | Wenn Sie benutzerdefinierte Personenfelder im Konto-Zielgruppenschema in Experience Platform definiert haben, können diese Felder auch als Personenattribute in Bedingungen verwendet werden. Verwenden Sie diese benutzerdefinierten Attribute in: <li>Benutzervorlagen <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Mehr erfahren</a></li><li>Geteilte Pfade nach Personen, Journey-Knoten <a href="../journeys/journey-nodes.md#add-a-split-path-by-people-node">Mehr erfahren</a></li> |
| Verbesserung | E-Mail-Kanaleinstellungen | E-Mail-Einstellungen sind jetzt in der Benutzeroberfläche von Journey Optimizer B2B edition sichtbar. Sie können die aktuellen Konfigurationen schnell überprüfen und Administratoren können auf _[!UICONTROL Einstellungen bearbeiten]_ klicken, um direkt zu den Einstellungen im Marketo Engage zu wechseln und sie entsprechend den Anforderungen Ihres Unternehmens zu aktualisieren. <a href="../admin/configure-channels-emails.md">Weitere Informationen</a> |

## Versionshinweise für September 2024 {#Sept-2024}

**Veröffentlichungsdatum**: 7. Oktober 2024

Diese Version umfasst die folgenden neuen Funktionen und Erweiterungen:

| Typ | Element | Beschreibung |
| ---- | ---- | ----------- |
| Verbesserung | Central Assets-Bibliothek | Mit der erweiterten Bibliothek _für zentrale Assets_ können Sie alle Bild-Assets in Ihrer Marketo Engage-Instanz über Design Studio-Arbeitsbereiche hinweg verwenden. Es gibt integrierte Limits, die Bearbeitungen von Marketo Engage-Assets aus Journey Optimizer B2B edition sowie Löschvorgänge und Verschiebevorgänge verhindern. Diese Schutzmaßnahmen stellen sicher, dass die Quell-Assets (Marketo Engage Design Studio) beibehalten werden, während eine nahtlose Lese- und Wiederverwendung in Journey Optimizer B2B edition ermöglicht wird.<p>Für Assets, die ausschließlich in Journey Optimizer B2B edition verwendet werden, bietet ein bestimmter Arbeitsbereich vollständige Asset-Management-Funktionen. <a href="../content/marketo-engage-design-studio.md">Weitere Informationen</a> |
| Neue Funktion | Zuletzt aufgerufene Assets | Die Startseite im Journey Optimizer B2B edition-Programm enthält jetzt den Abschnitt &quot;_[!UICONTROL Kürzlich aufgerufen]_&quot;, der eine Liste der zuletzt aufgerufenen Assets für Marketing-Experten oder Administratoren enthält. Sie können diese Liste verwenden, um direkt zu dem Asset zu gelangen, an dem Sie kürzlich gearbeitet haben, ohne durch eine Reihe von Asset-Seiten zu navigieren und zu suchen. <p>Die Liste enthält zusätzliche Informationen zur Änderung, sodass Sie die Entscheidung darüber treffen können, welche der Assets ab der letzten Sitzung weiter geändert werden muss. Bei E-Mail-Assets wird die Journey des Kontos angezeigt, in dem das E-Mail-Asset verwendet wird. <a href="../home-page.md">Weitere Informationen</a> |
| Verbesserung | Journey split node - reorder paths | In geteilten Pfadknoten wird die Pfadfilterung in der Reihenfolge von oben nach unten ausgewertet. Jede Person oder jedes Konto wird auf dem ersten Pfad weitergeführt, der mit übereinstimmt. Sie können die definierten Pfade neu anordnen, indem Sie oben rechts auf jeder Pfadkarte auf die Pfeile nach oben und unten klicken, um sie in der Liste nach oben oder unten zu verschieben. <a href="../journeys/journey-nodes.md#split-paths">Weitere Informationen</a> |
| Verbesserung | Journey split node - Zusätzliche Bedingungsattribute für den Aktivitätsverlauf | Bei der Verwendung von Bedingungen zum Definieren des Pfadfilters für einen geteilten Knoten durch Personen gibt es zwei zusätzliche Attribute: _Geöffnete E-Mail_ und _Wurde E-Mail gesendet_. Diese Ergänzungen bieten eine größere Flexibilität beim Filtern von Personen im Journey anhand von E-Mail-Aktivitäten. <a href="../journeys/journey-nodes.md#split-paths">Weitere Informationen</a> |

## Versionshinweise für August 2024 {#Aug-2024}

**Veröffentlichungsdatum**: 29. August 2024

Diese Version umfasst die folgenden neuen Funktionen und Erweiterungen:

| Typ | Element | Beschreibung |
| ---- | ---- | ----------- |
| Neue Funktion | LinkedIn-Konto-Matched Audiences | Generieren Sie LinkedIn-Anzeigenzielgruppen über kontengerechte Zielgruppen, damit Sie leere Rollen in Ihren Einkaufsgruppen ausfüllen können. Durch Definition eines Satzes von Einkaufsgruppenfiltern können Sie eine mit LinkedIn übereinstimmende Zielgruppe beibehalten, um potenzielle Kunden auszuwählen, die mit Ihren Kundengruppenparametern übereinstimmen. <p>Diese Funktion nutzt Experience Platform-Ziele , um einige Aspekte der Integration zu verwalten. <a href="../data/linkedin-account-matched-audiences.md">Weitere Informationen</a> |
| Verbesserung | Status-Lebenszyklus für visuelle Inhaltsfragmente | Visuelle Fragmente werden jetzt mit einem Statuslebenszyklus verwaltet. Der Fragmentstatus bestimmt seine Verfügbarkeit für die Verwendung in einer E-Mail- oder E-Mail-Vorlage sowie die Änderungen, die Sie daran vornehmen können. <p>Dieser erweiterte Workflow erleichtert die Verwaltung wiederverwendeter Inhalte entsprechend Ihrem Werbe- und Kommunikationskalender. <a href="../content/fragments.md#fragment-status-and-lifecycle">Weitere Informationen</a> |
