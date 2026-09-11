---
title: Absichtswerte
description: Erfahren Sie, wie Journey Optimizer B2B edition die Absichtswerte aus der Interaktion mit Personen und der Inhaltsrelevanz berechnet und wie sich die Werte zu Konten summieren.
feature: Dashboards, Intent, Intelligent Insights
role: User
autotag-review: '2026-09-11T14:56:32.307Z'
TQID: 'https://experienceleague.adobe.com/ajtUdNKafSoE1BC08imOpyflpDeAsXaQ3tdlbeYT6NU'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: f979fe0e-02fe-4599-b492-7b3df1d4e7dc
subfeature_v2:
  - id: e388c29d-df1e-4b47-ad27-1b14ae45776e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
source-git-commit: 2da5c7bbbadde4bbb5df82a81398ecb970165da2
workflow-type: tm+mt
source-wordcount: 1445
ht-degree: 0%

---


# Absichtswerte {#intent-scores}

Ein Intent Score misst, wie interessiert eine Person oder ein Konto an einem Keyword, einem Produkt oder einer Produktkategorie ist. Adobe Journey Optimizer B2B edition berechnet den Score anhand von maschinellem Lernen, das die Ähnlichkeit der Bedeutung misst, und nicht anhand manueller Regeln oder eines Festpunktsystems. Jeder Score wird von 0 auf 1 normalisiert, wobei höhere Zahlen eine stärkere Absicht anzeigen.

Die Inhaltsrelevanz wird etwa alle 12 Stunden aktualisiert, und die Intent-Scores werden täglich neu berechnet. Scores aggregieren sich von Keyword zu Produkt und von Person zu Konto. Absichtsbewertungen werden im gesamten [Intelligent Dashboard](../dashboards/intelligent-dashboard.md) und auf den [Kontodetails](../accounts/account-details.md), [_Einkaufsgruppendetails_, &#x200B;](../buying-groups/buying-group-details.md) und [Personendetails](../accounts/person-details.md) angezeigt.

![Intent-Datenvisualisierung](../data/assets/intent-data-visualization.png){width="700" zoomable="yes"}

In den folgenden Abschnitten werden die Kernkonzepte hinter der Absichtsermittlung, der kontinuierliche Prozess, der die Bewertungen aktuell hält, die Berechnungslogik hinter jedem Score und die Einstellungen, die Sie konfigurieren können, erläutert.

## Kernkonzepte {#core-concepts}

Die Absichtserkennung misst, wie genau eine Person mit Ihren Produkten und Schlüsselwörtern interagiert, und gewichtet diese Ähnlichkeit dann danach, wie viel die Person interagiert hat. Dieses Modell besteht aus drei Entitäten.

| Entität | Beschreibung |
|--------|--------------|
| Person | Die Person, die mit Ihren Inhalten interagiert, indem sie E-Mails öffnet, Web-Seiten besucht und mit der Zeit interagiert. |
| Inhalt | Die E-Mails und Webseiten, mit denen eine Person interagiert. Andere Formate wie Webinare und Kampagnen werden im Laufe der Zeit hinzugefügt. |
| Taxonomie | Ihre Struktur von Schlüsselwörtern, Produkten und Produktkategorien, die die Interessen repräsentieren, die Sie messen möchten. |

### Standardtaxonomie und Aktualisierungen {#taxonomy}

Ihre Taxonomie, die Keywords, Produkte und Kategorien, an denen die Absicht gemessen wird, können ohne erforderliche Einrichtung verwendet werden.

Sie können Taxonomiezuordnungen jederzeit auf der Seite „Absichtszuordnung _[!UICONTROL überprüfen und]_. Siehe [Absichtsdaten](../admin/intent-data.md) für den Einrichtungsprozess der Taxonomie.

### Inhaltsrelevanz {#content-relevance}

Journey Optimizer B2B edition übersetzt Inhalte und Taxonomien in eine mathematische Darstellung ihrer Bedeutung und verwendet dann ein Ähnlichkeitsmodell, um zu messen, wie genau sie übereinstimmen. Inhalte, die einem Keyword oder Produkt sehr ähnlich sind, erhalten eine hohe Relevanz. Nicht verwandte Inhalte erhalten eine niedrige Bewertung.

Das Ähnlichkeitsmodell ist auf allgemeine Sprache vortrainiert, sodass keine kundenspezifischen Schulungen erforderlich sind, um zu beginnen.

## Bewertungsprozess {#scoring-process}

Ein kontinuierlicher Prozess wandelt rohe Interaktionen in eine Absichtsbewertung um. Jede Stufe baut auf dem auf, was die vorherige Stufe produziert hat.

![Flussdiagramm mit fünf Scoring-Phasen: Interaktionserfassung, Inhaltsextraktion, Relevanzbewertung, tägliche Intent-Berechnung und Score-Bereitstellung.](./assets/intent-scores-pipeline.svg){width="700"}

### Interaktionsaufnahme {#engagement-capture}

Jeder aussagekräftige Touchpoint, den eine Person hat, wird so erfasst, wie er passiert, und mit den betroffenen Inhalten verknüpft.

* Seitenbesuche, E-Mail-Öffnungen und -Klicks, Formularübermittlungen und ähnliche Aktivitäten werden als Interaktionsereignisse aufgezeichnet.
* Jedes einzelne Inhaltselement wird ebenfalls notiert, sodass es im nächsten Schritt analysiert werden kann.
* **Aktualisierungskadenz** - Fortlaufend, wenn eine Interaktion stattfindet.

### Inhaltsextraktion {#content-extraction}

Bevor Inhalte nach Relevanz bewertet werden können, extrahiert Journey Optimizer B2B edition den Text und liest ihn.

* Für jedes neue Inhaltselement extrahiert das System den zugrunde liegenden Text, unabhängig davon, ob er sich auf einer Web-Seite oder in einer E-Mail befindet.
* Einige Aktivitätstypen, z. B. Formularausfüllungen, enthalten bereits eigene beschreibende Inhalte und überspringen diesen Schritt.
* Inhalte, die nicht abgerufen werden können, z. B. ein fehlerhafter oder entfernter Link, werden protokolliert und in Zukunft ausgeschlossen.
* **Aktualisierungskadenz** - Wenn neue Inhalte erkannt werden.

### Relevanzbewertung {#relevance-scoring}

Jedes Asset wird anhand Ihrer Taxonomie gemessen, unabhängig davon, wer damit in Kontakt stand.

* Jede E-Mail und Web-Seite wird mithilfe des Ähnlichkeitsmodells analysiert und mit Ihren Keywords, Produkten und Kategorien verglichen.
* Das Ergebnis ist ein Relevanzwert zwischen 0 und 1 für dieses Asset für jedes zugehörige Keyword oder Produkt.
* **Aktualisierungskadenz** - Alle 12 Stunden.

### Berechnung der täglichen Absicht {#daily-intent-calculation}

Interaktion und Inhaltsrelevanz werden zu einem täglichen Intent-Score pro Person, pro Keyword oder Produkt kombiniert.

* Jeder Aktivitätstyp hat eine konfigurierbare Gewichtung. Beispielsweise kann eine Formularübermittlung weit mehr zählen als eine Seitenansicht.
* Jüngste Aktivitäten sind wichtiger als ältere Aktivitäten, daher begünstigen Scores das, was jemand diese Woche getan hat, im Vergleich zu dem, was er vor einem Monat getan hat.
* Ein Konfidenzmaßstab spiegelt wider, wie konsistent die Interaktion einer Person war, nicht nur das Volumen.
* **Aktualisierungskadenz** - Täglich.

### Versand bewerten {#score-delivery}

Tägliche Scores aggregieren, eine Absichtsebene erhalten und an Ihr Dashboard gesendet werden.

* Jeder Wert hat die Absichtsebene Hoch, Medium oder Niedrig.
* Die Bewertungen sind mit dem richtigen Konto verknüpft, sodass Vertriebs- und Marketing-Teams sowohl die Absichten auf Personenebene als auch auf Kontoebene sehen können.
* Nur Personen, deren Absichtsebene sich geändert hat, werden aktualisiert, sodass das Dashboard die neueste bedeutsame Änderung widerspiegelt.
* **Aktualisierungskadenz** - Täglich.

## Berechnungslogik der Bewertung {#score-calculation-logic}

Die Berechnung besteht aus fünf Ebenen, die jeweils mehr Kontext zu den Rohdaten zu Relevanz und Interaktion hinzufügen.

### Inhaltsrelevanz für ein Thema {#relevance-to-topic}

Jedes Inhaltselement und jedes Thema, also ein Keyword, ein Produkt oder eine Kategorie, wird in eine mathematische Darstellung seiner Bedeutung übersetzt. Inhalte mit einer ähnlichen Bedeutung wie ein Thema liegen in dieser Darstellung näher beieinander. Relevanz ist ein Maß für die Nähe in der Bedeutung, keine exakte Wortübereinstimmung.

### Tägliche Interaktionsgewichtung {#engagement-weighting}

Die Punktzahl einer Person an einem bestimmten Tag ist ein gewichteter Durchschnitt der Relevanz von allem, mit dem sie interagiert hat. Aktivitäten mit höherem Wert zählen für mehr.

>[!BEGINSHADEBOX „example“]

Eine Person interagiert an einem Tag mit drei Inhalten. Seitenansichten haben die Gewichtung eins, und Formularübermittlungen haben die Gewichtung fünf.

Da die Übermittlung eines einzelnen Formulars fünf Mal so viel zählt wie eine Seitenansicht, wirkt sich dies erheblich auf die tägliche Bewertung aus, auch wenn insgesamt drei Elemente verwendet wurden.

Ihr resultierender Tageswert für dieses Thema liegt bei etwa 0,70 auf einer Skala von 0 bis 1.

>[!ENDSHADEBOX]

### Neuheitszerfall {#recency-decay}

Der Wert einer Person spiegelt eine Mischung aus den letzten Tagen wider, wobei die jüngste Aktivität viel stärker gewichtet wird als die ältere Aktivität. Nach etwa einer Woche hat ältere Aktivität nur minimale Auswirkungen, sodass der Score immer das aktuelle Interesse widerspiegelt. In der Praxis wiegt ein Besuch heute schwerer als ein Besuch von gestern, was schwerer wiegt als ein Besuch vor zehn Tagen.

### Normalisierung und Absichtsebenen bewerten {#normalization-intent-levels}

Jeder angepasste Wert wird im Verhältnis zu anderen Personen in Ihrer Instanz auf einer konsistenten Skala von 0 bis 1 platziert und dann in eine Absichtsebene zusammengefasst.

| Endergebnis | Absichtsstufe |
|-------------|--------------|
| Über 0,6 | Hoch |
| 0,2 bis 0,6 | Medium |
| Unter 0,2 | Niedrig |

### Score-Aggregation {#score-aggregation}

Die individuellen Bewertungen werden aggregiert, sodass Sie die Absicht auf der Ebene überprüfen können, die für eine Entscheidung wichtig ist, nicht nur auf der detailliertesten Ebene.

* **Keyword zu Produkt** - Scores, die auf Keyword-Ebene berechnet werden, aggregieren, um Interesse an einem Produkt zu zeigen und nicht nur an einem einzelnen Suchbegriff.
* **Person zu Konto** - Ein Kontowert aggregiert alle Bewertungen seiner Personen, sodass Sie sehen können, wenn eine ganze Einkaufsgruppe ihre Absicht zeigt.

![Diagramm mit der Aggregation von Keyword-Scores zu Produkt-Scores und von Personen-Scores zu Konto-Scores.](./assets/intent-scores-aggregation.svg){width="500"}

Verwenden Sie die Ansicht auf Produktebene , um zu sehen, welche Produkte insgesamt an Interesse zunehmen, und nicht, welche einzelnen Keywords sich im Trend befinden. Verwenden Sie die Ansicht auf Kontoebene, um zu sehen, wann eine ganze Einkaufsgruppe gemeinsam ein erhöhtes Interesse zeigt, anstatt auf eine einzelne engagierte Person zu reagieren.

## Konfigurierbare Einstellungen {#configurable-settings}

Die meiste Scoring-Logik ist darauf ausgelegt, die Ergebnisse im Zeitverlauf zuverlässig und vergleichbar zu halten. Ein Produktadministrator kann zwei Einstellungen an Ihre Anforderungen anpassen:

* **Aktivitätsgewichte** - Erhöhen Sie die Gewichtung von hochwertigen Aktivitäten wie einer Demoanfrage oder einem Seitenbesuch, um eine größere Wirkung auf die Absichtsergebnisse zu erzielen. Um eine Aktivität vollständig auszuschließen, setzen Sie ihre Gewichtung auf null, was für Aktionen wie Abmeldungen nützlich ist, die nicht zur Absicht beitragen. Die Aktivitätsgewichte für die Absichtsberechnung verwenden dasselbe Gewichtungsmodell, das auch zu den [&#x200B; (Interaktionsbewertungen](../buying-groups/engagement-scores.md) führt. Informationen [_Ändern der Aktivitätsgewichtung finden_](../admin/engagement-score-weighting.md) unter „Konfigurieren der“.

* **Taxonomiezuordnungen** - Die Schlüsselwörter, Produkte und Kategorien, auf denen die Bewertung basiert, können verwendet werden. Überprüfen und aktualisieren Sie sie jederzeit auf der Seite _[!UICONTROL Intent Mapping]_. Siehe [_Absichtsdaten_](../admin/intent-data.md) für den Einrichtungsprozess.

Alles andere, einschließlich der Schwellenwerte für Inhaltsrelevanz, Aktivitätsverfall und _Hoch_, _Medium_ und _Niedrig_, wird so korrigiert, dass die Bewertungen im Laufe der Zeit konsistent und vergleichbar bleiben.

## Scoring-Grundsätze {#scoring-principles}

Beachten Sie die folgenden Prinzipien, wenn Sie Absichtswerte überprüfen und bearbeiten.

### Modellgesteuerte Bewertung {#model-driven}

Es gibt keine Punktzuweisungen oder Schlüsselwortregeln, die gepflegt werden müssen. Das Modell erfährt Relevanz direkt aus Ihrem Inhalt und Ihrer Taxonomie, wodurch die Bewertung konsistent bleibt, wenn Ihre Inhaltsbibliothek wächst und sich ändert, ohne dass eine laufende Konfiguration erforderlich ist.

### Relative Bewertung {#relative-scoring}

Ein Score gibt an, wo eine Person oder ein Konto heute zu Ihren anderen Kontakten gehört, und das System berechnet ihn täglich basierend auf der aktuellen Population neu. Punktzahlen verwenden, um Personen und Konten innerhalb Ihrer eigenen Instanz zu vergleichen, anstatt als feste, universelle Zahl. Die Bewertungen sind von einem Unternehmen zum anderen nicht direkt vergleichbar.

### Aktualität der Daten {#data-freshness}

Die Inhaltsrelevanz wird etwa alle 12 Stunden aktualisiert, wenn neue Inhalte angezeigt werden. Die Absichtswerte werden einmal pro Tag neu berechnet, sodass das Dashboard jeden Morgen die Aktivität des Vortages widerspiegelt.
