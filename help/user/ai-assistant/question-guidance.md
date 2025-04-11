---
title: Fragebögen für KI-Assistenten
description: Platzhalter
feature: AI Assistant
level: Beginner
exl-id: 65541246-7f4f-442f-8293-df036ea1c4ac
source-git-commit: f09f3f5b7d4419ead5308e4c5be3b518b4e16ff5
workflow-type: tm+mt
source-wordcount: '871'
ht-degree: 1%

---

# Anleitung für KI-Assistenten in Journey Optimizer B2B edition

Sehen Sie sich die folgenden Beispielfragen für die Abfrage des KI-Assistenten in Journey Optimizer B2B edition an. Diese Informationen enthalten auch Tipps zum Formulieren Ihrer Fragen, um vom KI-Assistenten optimale Antworten zu erhalten.

## Zielbezogene Fragen

Die folgenden Beispielfragen werden nach Zielen gruppiert, die Sie mit dem KI-Assistenten erreichen können:

| Zielvorgabe | Beschreibung | Beispiel |
| --- | --- | --- |
| Lernkonzepte und fortlaufende Workflows | Als Anfänger können Sie den KI-Assistenten verwenden, um Real-Time CDP- und Adobe Journey Optimizer B2B edition-Konzepte zu erlernen und sich mit Produkten und Funktionen vertraut zu machen, die Ihnen nicht bekannt sind. <br>Als erfahrener Benutzer können Sie den KI-Assistenten verwenden, um einen Randfall zu lösen, der Ihren Workflow blockieren könnte. | <li>Erzählen Sie mir einige Anwendungsfälle für Real-Time CDP. <li>Erklären Sie mir das Konzept der Einkaufsgruppe. |
| Fehlerbehebung | Verwenden Sie den KI-Assistenten, um zu erfahren, wie Sie grundlegende Fehler debuggen, auf die Sie in Ihrem Workflow stoßen können. | <li>Was bedeutet dieser Fehler &lt;ERROR_MESSAGE>? <li>Warum kann ich die Zielgruppe mit dem Namen &quot;…“ nicht löschen? |
| Sandbox-Hygiene | Verwenden Sie den KI-Assistenten, um Duplikate oder nicht verwendete Objekte zu identifizieren, damit Sie Ihre Sandbox effizient verwalten können. | <li>Können Sie mir ähnliche Konto-Zielgruppen zeigen? <li>Gibt es Schemata, denen kein Datensatz zugeordnet ist? |
| Wertanalyse | Verwenden Sie den KI-Assistenten, um Ihre am häufigsten verwendeten Datenobjekte zu identifizieren und Leistungsindikatoren zu bewerten oder die wertvollsten Datenobjekte zu finden. | <li>Wie viele Konten befinden sich in unserer Segmentdefinition &quot;…“? <li>Wann wurden Zielgruppen für das Experience Cloud-Zielgruppen-Ziel aktiviert? |
| Suche | Verwenden Sie den KI-Assistenten, um unterstützte Experience Platform- und Adobe Journey Optimizer-B2B edition-Objekte zu finden, z. B. Kontozielgruppen, Datensätze, Ziele, Schemata, Quellen, Account-Journey, Einkaufsgruppenvorlagen und Lösungsinteressen | <li>Listen Sie die Zielgruppen auf, die „Luma“ im Namen enthalten und in den Account-Journey verwendet wurden. <li>Welche Attribute enthalten das XDM-Schema „Luma: Custom Actions“? |
| Wirkungsanalyse | Verwenden Sie den KI-Assistenten, um Datenobjekte zu identifizieren, die in bestimmten Workflows verwendet wurden, damit Sie die Auswirkungen von Änderungen bewerten können. | <li>Welche Konto-Zielgruppen verwenden `workEmail.address` im Schema „B2B-Person“? <li>In welchen Datensätzen sind die … `jobTitle` gespeichert? |

## Formulieren von Fragen

Sie müssen Ihre Fragen an den KI-Assistenten mit Klarheit und Kontext formulieren, um eine möglichst präzise Antwort zu erhalten. Eine Anleitung dazu, wie Sie im Kontext eine klare Frage stellen, finden Sie in der folgenden Liste von Tipps:

* Geben Sie Ihre Aufgabe und/oder Frage kurz an.
* Vermeiden Sie mehrdeutige Sprache oder eine übermäßig komplexe Syntax, um das Verständnis zu erleichtern.
* Geben Sie einen relevanten Kontext zu Ihrer Aufgabe und/oder Frage an, da der Kontext dazu beitragen kann, dass der KI-Assistent relevantere Antworten generiert.

Die folgenden Tabellen enthalten einige Best Practices, die Sie bei der Verwendung des KI-Assistenten befolgen können:

| tun | Beispiel |
| --- | --- |
| <li>Geben Sie das Objekt oder die Informationen an, die Sie abrufen oder analysieren möchten. <li>Versuchen Sie, Ihre Datenobjektnamen in Anführungszeichen zu setzen. <li>Wenn Sie nur einen Teil des Objektnamens kennen, können Sie diesen auch in der Frage angeben. | <li>Welche Datensätze verwenden das Schema „B2B-Konto“? <li>Anzeigen der aktivierten Zielgruppen, die „Konto“ im Namen haben Sortieren Sie sie nach der Anzahl der Mitglieder. |
| <li>Vermeiden Sie Mehrdeutigkeiten und verwenden Sie eine klare Sprache. <li>Verwenden Sie eine präzise Terminologie, um eine klarere Abfrage zu ermöglichen. <li>Wenn Sie Fragen zu Adobe Experience Platform und Adobe Journey Optimizer B2B edition stellen, versuchen Sie, eine Experience Platform- oder Adobe Journey Optimizer B2B edition-spezifische Terminologie zu verwenden, um die Relevanz der Antworten zu verbessern. | <li>Wie viele Mitglieder habe ich in „My Account Audience“? <li>Wie viele Account-Journey verwenden die Account-Zielgruppe „My Account Audience“? |
| <li>Geben Sie den Kontext an oder geben Sie ein Kriterium zum Filtern Ihrer Ergebnisse an. <li>Verwenden Sie in den Fragen ein Filterkriterium, um die Datenmenge in der Antwort zu begrenzen. | <li>Account-Zielgruppen anzeigen, die nicht aktiviert wurden, vor mehr als 6 Monaten erstellt wurden und noch nie geändert wurden. <li>In den letzten 7 Tagen veröffentlichte Account-Journey anzeigen mit einer Account-Zielgruppe mit mehr als 1000 Mitgliedern |

| Tu das nicht | Beispiel |
| --- | --- |
| Verwende eine vage oder mehrdeutige Sprache. | <li>Geben Sie mir Informationen zu Datensätzen. <li>Was macht Journey X? <li>Wie viele Benutzer habe ich in „ACME Audience“? <li>Segmente anzeigen. <li>Attribute auflisten. |
| Unvollständige Anfragen stellen. | <li>„Luma - Treueprogramm-Datensatz“ |
| Annahme von Wissen ohne Kontext. | <li>Zielgruppen in den letzten 6 Monaten. <li>Erstellen Sie eine Abfrage für mich. <li>Erstellen einer Journey für mich |
| Formulieren Sie übermäßig komplexe Abfragen. | <li>Bieten Sie eine umfassende Analyse der Datenherkunft für alle Objekte und deren Abhängigkeiten. |
| Kriterien oder Parameter auslassen. | <li>Anzeigen von Datensätzen |

## Beispiele für nicht unterstützte Fragen

Die folgende Liste enthält Beispiele für Fragen, die der KI-Assistent in Journey Optimizer B2B edition derzeit nicht unterstützt:

* Welche Konto-Zielgruppen verwenden das Feld workEmail.address der Feldergruppe … in ihrer Bedingung? 
* Zeigen Sie mir die Anzahl der aktiven Journey mit Account-Zielgruppen von mehr als 10.000, 5.000-10.000, 1.000-5.000 und weniger als 1.000 in einem Verteilungsbild
* Wer hat das letzte Update auf Account Journey X gemacht?
* Wie viele aktive Journey fügen Mitglieder der Einkaufsgruppe für Solution Interest x hinzu?
* Welche aktiven Journey fügen Mitglieder der Einkaufsgruppe für Solution Interest x hinzu?
* Welcher Titel ist der häufigste Entscheidungsträger bei Käufergruppenvorlagen?
* Wer sind die Entscheidungsträger für den Kauf von Gruppenvorlagen x?

## Nächste Schritte

Informationen zur Verwendung der Funktionen des KI-Assistenten während Ihrer Workflows finden Sie unter [Verwenden des KI-Assistenten in Journey Optimizer B2B edition](./use-ai-assistant.md).
