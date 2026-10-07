---
source-git-commit: 1b4d8ad802265b537eb09439cfe34b97a3e61448
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 0%
---
# GitHub-Copilot-Repository-Anweisungen

Wenn die allgemeine Anleitung in den kopierten Claude-Anweisungen mit Repository-spezifischen Konventionen oder aufgabenspezifischen Anweisungen in Konflikt steht, befolgen Sie die Repository-spezifischen oder aufgabenspezifischen Anweisungen.

## Zweck

Verwenden Sie diese Repository-Anweisungen für die Dokumentationsarbeit in diesem Repository. Halten Sie Bearbeitungen präzise, technisch genau und an Adobe Experience League-Dokumentationsstandards ausgerichtet.

## Schreiben Sie im Dokumentationsstil des Repositorys

- Eine klare, direkte und benutzerorientierte Sprache ist vorzuziehen.
- Halten Sie Sätze kurz und überschaubar.
- Eine bestimmte, verwertbare Sprache wird Marketing- oder Fülltext vorgezogen.
- Vermeiden Sie Textbausteinabschnitte wie „Verwandte Themen“, „Häufig gestellte Fragen“ oder generische Zusammenfassungsblöcke, es sei denn, sie sind ausdrücklich erforderlich.
- Verwenden Sie kontextbezogene Querverknüpfungen anstelle von Navigationsblöcken am Seitenende.
- Fügen Sie am Ende eines Artikels keine Referenzliste oder einen Abschnitt „Verwandte Themen“ hinzu. Stellen Sie verwandte Links vor, wo sie im Inhalt relevant sind, und erklären Sie, wie sich jedes Ziel auf das aktuelle Thema bezieht.
- Verwenden Sie keine räumlichen Ausdrücke wie „unten“ oder „oben“, um die Dokumentreihenfolge zu beschreiben. Verwenden Sie stattdessen „Folgendes“, „Zurück“ oder „im nächsten Abschnitt“.

## Benennungsregeln für externe Dokumentationen

- Verwenden Sie in der externen Dokumentation keine Adobe-Produktakronyme.
- Bei der ersten Erwähnung von Adobe-Produktnamen muss der vollständige Produktname verwendet werden, einschließlich ggf. &quot;Adobe&quot;.
- Verwenden Sie DNL-Tags für Produktnamen im Inhalt, z. B.:
  - [!DNL Adobe Experience Platform]
  - [!DNL Adobe Journey Optimizer B2B Edition]
  - [!DNL Experience Platform]
  - [!DNL Journey Optimizer B2B Edition]
- Ersetzen Sie reine Akronym-Verweise wie &quot;AEP&quot; und &quot;AJO B2B“ durch ihre vollständigen Produktnamen in der benutzerseitigen Dokumentation.
- Wenn ein Produkt zum ersten Mal eingeführt wird, schreiben Sie den vollständigen Namen. Spätere Erwähnungen können den kürzeren Produktnamen ohne das Akronym verwenden und das DNL-Tag beibehalten, wenn der Produktname in der Benutzeroberfläche oder im Text der Dokumente angezeigt wird.
- Wenden Sie diese Begriffe konsistent auf den Seitentitel, den ersten Absatz und alle Beschriftungen oder Querlinks an, die für Leser sichtbar sind.

## Repository-spezifische Benennungskonventionen

- Verwenden Sie &quot;Adobe Journey Optimizer B2B Edition&quot; für den Produktnamen in benutzerorientierten Dokumenten.
- Verwenden Sie &quot;Adobe Experience Platform&quot; für den Plattformnamen in Dokumenten, die für Benutzende bestimmt sind.
- Verwenden Sie den Produktnamen in seiner vollständigen Form bei der ersten Erwähnung und halten Sie dann die späteren Verweise kurz und konsistent.
- Bewahren Sie bei Datensatzverweisen die tatsächlichen Datensatznamen und IDs genau so auf, wie sie im Quellvertrag angezeigt werden, auch wenn sie veraltete Präfixe wie `AJOB2B-` enthalten.

## Anleitung für Markdown und Formatierung

- Schreiben Sie einen gültigen Markdown mit GitHub-Variante.
- Halten Sie Überschriften kurz und beschreibend.
- Verwenden Sie Tabellen nur, wenn sie den Lesern helfen, technische Details zu überprüfen.
- Verwenden Sie relative Links für repo-lokale Verweise.
- Halten Sie Code-Blöcke und Feldpfade genau und kopierbar.
- Vermeiden Sie redundante Produktverweise in Überschriften, wenn sie bereits im Seitentitel angegeben sind.

## Checkliste für die Überprüfung vor der Fertigstellung

- Stellen Sie sicher, dass in benutzerorientierten Inhalten keine Akronyme für Adobe-Produkte vorhanden sind.
- Stellen Sie sicher, dass bei der ersten Erwähnung der vollständige Produktname verwendet wird.
- Stellen Sie sicher, dass Produktnamen mit [!DNL ...] getaggt werden, sofern dies vom Repository-Stil erforderlich ist.
- Stellen Sie sicher, dass das Dokument Textbausteine und räumliche Formulierungsprobleme vermeidet.
- Sicherstellen, dass der technische Inhalt korrekt bleibt und die kontextbezogenen Querlinks erhalten bleiben.
