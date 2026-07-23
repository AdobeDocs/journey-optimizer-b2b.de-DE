---
title: KI-Entscheidung
description: Machen Sie sich mit der KI-Entscheidungsfindung in Journey Optimizer B2B Prime vertraut, der Intelligenzschicht hinter der Journey-Traffic-Steuerung, dem nächstbesten Pfad, der Sendezeitoptimierung und anderen Funktionen, die statische Regeln durch ergebnisgesteuerte Automatisierung ersetzen.
autotag-review: '2026-07-23T00:13:49.629Z'
TQID: 'https://experienceleague.adobe.com/vAu9C6Erjr-0TIJ18jQnR209Ed2xfLl9P3Nq2fPTs9c'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: aed878b8-11d0-487c-828b-d23b2051ec37id: bef5003b-cad2-4f40-bdb2-a80426d52ef5
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1fid: c3d6e661-d372-4e98-9fd9-eac771e7e4eeid: ff10f619-348f-47e3-99bf-3ce4c817cf2c
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 120afb1109e550fc65c2fc5a01680f2d7d2e2345
workflow-type: tm+mt
source-wordcount: 814
ht-degree: 2%

---


# KI-Entscheidung

KI-Entscheidungsfindung ist die Intelligenzebene hinter Adobe Journey Optimizer B2B Prime. Anstatt jede Verzweigung als statische Regel vorab zu erstellen, bewertet KI-Entscheidungsfindung kontinuierlich den Kontext eines Profils, einschließlich Journey-Mitgliedschaft, Interaktionsverlauf, Absichtsbewertungen und Echtzeitverhalten, um die nächstbeste Aktion oder den nächsten besten Pfad für diese Person zu ermitteln.

Diese kontinuierliche Auswertung bewegt die Orchestrierung von statischen Regeln hin zu einer ergebnisorientierten Automatisierung: Statt jede Bedingung im Voraus zu definieren, beschreiben Sie das gewünschte Ergebnis, und das System bestimmt, wie Sie für jede Person dorthin gelangen.

## Funktionen {#capabilities}

KI-Entscheidungsfindung besteht aus den folgenden Funktionen:

| Fähigkeit | Was er entscheidet |
|---|---|
| [Traffic-Steuerung für Journey](../marketing/journey-traffic-control.md) | Auf welcher Journey eine Person gerade sein sollte. Wenn sich eine Person für mehr als einen Journey qualifiziert, werden sie von der Journey-Traffic-Steuerung in dem Moment neu geleitet, in dem sich ihr Profil oder ihr Verhalten ändert, anstatt sie auf einem Pfad zu belassen, der nicht mehr passt. |
| [Nächster bester Pfad](../marketing/next-best-path.md) | Der am besten geeignete Pfad für eine Person innerhalb eines Journey. Anstatt die Filterbedingungen fest zu kodieren, beschreiben Sie die Absicht in natürlicher Sprache, und das System leitet jede Person zum richtigen Zeitpunkt zum Pfad, der am besten passt. |
| [Versandzeitoptimierung](../marketing/email-send-time-optimization.md) | Das beste Versandfenster für jeden Empfänger basierend auf historischer Interaktion und nicht auf einem festen Zeitplan für alle. |
| Kontextueller Inhalt | Automatisch aus einer Inhaltsbeschreibung generierte personalisierte E-Mail-Varianten zur Verwendung als einzelnes personalisiertes E-Mail-Asset in Journeys. _In Kürze verfügbar._ |
| [Brand Concierge](https://experienceleague.adobe.com/de/docs/brand-concierge/content/home){target="_blank"} | Gesprächsweiterleitung und -reaktion in Echtzeit, z. B. Chat und Live-Unterstützung. Brand Concierge erfordert zusätzliche Produktberechtigungen. |

Einige dieser Funktionen lösen verschiedene Probleme innerhalb derselben Journey. Die Journey-Traffic-Steuerung entscheidet, welche Journey Priorität erhält, wenn mehrere Journey um die gleichzeitige Kontaktaufnahme mit derselben Person konkurrieren. Die anderen Funktionen entscheiden, was geschieht, nachdem eine Person bereits auf einer Journey ist.

## Pfade aufteilen und nächstbesten Pfad {#split-paths-next-best-path}

[Aufspaltungspfade](../marketing/split-merge-paths-nodes.md) ermöglichen es Ihnen, Journey-Verzweigungen mit expliziten Filterbedingungen zu definieren: Wenn ein Score über einem Schwellenwert liegt, senden Sie eine Person einen Pfad nach unten, andernfalls einen anderen. Diese regelbasierte Logik ist präzise und vollständig überprüfbar, aber jede neue Bedingung erfordert eine neue Verzweigung.

Der [Nächster bester Pfad](../marketing/next-best-path.md)-Knoten wendet die KI-Entscheidungsfindung auf dasselbe Problem an. Anstelle eines festen Schwellenwerts bewertet das Modell Interaktion, Persönlichkeit, Produktinteresse und das funnel-Stadium gemeinsam, sagt das beste Ergebnis für jede Person voraus und wählt automatisch den optimalen Pfad aus.

## Dateneingaben {#data-inputs}

KI-Entscheidungen basieren auf den folgenden Datenkategorien:

| Kategorie | Beispiele |
|---|---|
| Demografisch und firmografisch | Stellenbezeichnung, Branche und Unternehmensgröße |
| psychographisch | Lead-Bewertung, Dringlichkeit und Priorität |
| Interaktion | Bewertung, Ebene, Trend, letzte Aktivität und Kanal |
| Absicht | Produkt- oder Keyword-Absicht, gruppiert in hohe, mittlere oder niedrige Behälter |
| Persona | Rolle in Abschluss, Stellenbezeichnung und Rolle |

## Auswertungskadenz {#evaluation-cadence}

Die KI-Entscheidungsfindung verwendet zwei verschiedene Auswertungszeitpläne. Das zugrunde liegende Profil für eine Person wird auf Basis eines nächtlichen Batches neu berechnet. Die Entscheidung selbst wird bei jeder Interaktion in Echtzeit angewendet, wobei das neueste Nachtprofil verwendet wird. Der kontinuierliche Teil der KI-Entscheidung beschreibt also den Entscheidungszeitpunkt, nicht die Aktualisierungsrate des Profils.

## Leitplanken und Regeln {#guardrails-rules}

Regeln betreffen nur Bedingungen, die jemand explizit aufgeschrieben hat. Wenn die Realität außerhalb dieses Baums liegt, z. B. eine hybride Rolle oder eine Signalkombination, die niemand vorhergesehen hatte, tun Regeln nichts, bis jemand einen neuen Zweig hinzufügt. Die KI-Entscheidungsfindung bewertet jede Person kontinuierlich und gibt stattdessen eine vertrauensbasierte beste Aktion aus. Daher verarbeitet sie Kombinationen, auf die niemand explizit programmiert ist, und verbessert sich, da mehr Ergebnisse angezeigt werden, was eine Regel nie tut.

Die Regeln sind erklärbar und werden sofort für Audits verwendet, während KI-Entscheidungen eher auf Vertrauen als auf Determinismus basieren. Aus diesem Grund bleiben Regeln das bessere Instrument, wenn:

* Eine harte Compliance-Grenze darf niemals überschritten werden, z. B. die Unterdrückung von ausgeschlossenen Kontakten.
* Es gibt noch nicht genug Volumen oder Historie, aus dem ein Modell lernen kann.
* Jede Entscheidung muss auf Anfrage vollständig erklärbar sein.

Die meisten ausgereiften Setups laufen beide zusammen: Regeln als Leitplanken und KI-Entscheidungsfindung, die alles dazwischen handhabt.

## Vorteile {#benefits}

* Weniger manuelle Journey-Komplexität, weniger Regelzweige zu pflegen.
* Relevantere Erlebnisse, ohne Hunderte von Regeln zu erstellen.
* Höhere Qualifizierungseffizienz.
* Schnellere Identifizierung der nächstbesten Interaktion für jedes Profil.

>[!BEGINSHADEBOX]

**Zukünftiger Umfang: Konto- und Einkaufsgruppenkontext**

Derzeit nicht in Journey Optimizer B2B Prime verfügbar. Die KI-Entscheidungsfindung soll über das individuelle Profil hinaus auf Folgendes ausgedehnt werden:

* Kontokontext - Signale auf Unternehmens- und Kontoebene als Entscheidungseingabe.
* Kaufgruppensignale - Rolle bei Abschluss, Status von Entscheidungsträgern oder Fachleuten und Interaktion, aggregiert über alle an einer Kaufentscheidung beteiligten Personen.
* Journey-Orchestrierung auf Kontoebene - Routing- und Inhaltsentscheidungen, die für das Konto oder die Einkaufsgruppe als Einheit getroffen werden, wobei die Journey-Traffic-Steuerung die verschiedenen beteiligten Personen koordiniert.

>[!ENDSHADEBOX]
