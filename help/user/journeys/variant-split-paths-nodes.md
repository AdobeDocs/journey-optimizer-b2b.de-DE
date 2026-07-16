---
title: Aufspaltungspfade für Varianten
description: Erfahren Sie, wie Sie mit Pfadknoten für die Variantenaufteilung Konten nach dem Zufallsprinzip über mehrere Journey-Pfade mithilfe der prozentualen Zuordnung in Journey Optimizer B2B edition verteilen können.
feature: Account Journeys
solution: Journey Optimizer B2B Edition
role: User
badgeBeta: label="Beta" type="informative" tooltip="Diese Funktion befindet sich derzeit in einer eingeschränkten Beta-Version"
autotag-review: '2026-07-06T23:50:12.985Z'
TQID: 'https://experienceleague.adobe.com/42lSbF7J-yEzFYbFFhs2sSQ4j4NfRtENlIz-R-HcPx8'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
subfeature_v2:
  - id: c31bc6c7-76bc-467b-80c0-7315a4e3f6be
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 11e6c1954e3a99f3da6fc0967038d1c316991d07
workflow-type: tm+mt
source-wordcount: 1439
ht-degree: 2%

---

# Pfade für aufgeteilte Varianten

Verwenden Sie einen _Pfade mit Variantenaufteilung_, um Konten nach dem Zufallsprinzip auf zwei oder mehr Journey-Pfade basierend auf der von Ihnen definierten prozentualen Zuordnung zu verteilen. Dieser Knoten ist nützlich, um verschiedene Messaging-, Timing- oder Interaktionstaktiken in allen Segmenten Ihrer Konto-Audience zu testen, ohne bedingte Regeln anzuwenden. Sie ist nicht für kontrollierte A/B-Experimente geeignet, die eine konsistente Zuweisung pro Konto erfordern.

>[!AVAILABILITY]
>
>Der Knoten „Pfade für die Variantenaufspaltung“ ist derzeit für ausgewählte Kundinnen und Kunden als eingeschränkte Beta-Version (nur für **_-Journey_** verfügbar. Der Support für Personen-Journey ist für eine künftige Version geplant. Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, um Zugriff zu erhalten.

## Vergleich mit aufgeteilten Pfaden {#compare-split-paths}

Sowohl _[Split-Pfade](./split-merge-paths-nodes.md)_ als _Variant-Split-Pfade_ unterteilen Konten in mehrere Journey-Verzweigungen, sie verwenden jedoch unterschiedliche Mechanismen:

| Aspekt | Pfade aufteilen | Pfade für aufgeteilte Varianten |
| -------- | ----------- | ------------------- |
| **Zuweisungslogik** | _Regelbasiert_ - Jedes Konto wird anhand definierter Bedingungen ausgewertet, und es wird entlang des ersten Pfads fortgefahren, mit dem es übereinstimmt. | _Prozentbasierte zufällige Zuweisung_ - Konten werden entsprechend konfigurierten Prozentsätzen ohne Filterbedingungen auf verschiedene Pfade verteilt. |
| **Determinismus** | _Deterministisch_ - Ein Konto folgt immer demselben Pfad, solange es dieselben Bedingungen erfüllt. | Nicht deterministisch - dasselbe Konto kann bei der Wiedereinreise unterschiedlichen Wegen folgen. |
| **Anwendungsfall** | Segmentieren nach bekannten Konto- oder Einkaufsgruppenattributen; Bewertung nach Priorität. | Verteilen Sie nach dem Zufallsprinzip Konten für Tests, Messaging, Timing oder Taktiken über Ihre Kontozielgruppe. |
| **Pfad für andere Konten** | _Unterstützt_ - Konten, die mit keinem definierten Pfad übereinstimmen, können an einen Standardpfad weitergeleitet werden. | _Nicht zutreffend_ - Jedes Konto ist einem der definierten Pfade zugewiesen. |

## Aufspaltung nach Konto {#split-by-account}

Wenn ein Konto einen Knoten mit aufgeteilten Pfaden für Varianten erreicht, weist der Knoten ihn basierend auf konfigurierten Prozentsätzen genau einem Pfad zu. Die Zuweisung verwendet einen kontingentbasierten Algorithmus, der verfolgt, wie viele Konten jedem Pfad zugewiesen wurden, und sich im Laufe der Zeit anpasst, um die konfigurierten Verhältnisse beizubehalten.

* Jedes Konto ist genau einem Pfad zugewiesen.
* Die Zuweisung erfolgt nach dem Zufallsprinzip und auf Basis von Kontingenten. Der Algorithmus passt die Zuweisungen dynamisch an die konfigurierten Prozentsätze in der Gesamtpopulation an.
* Der Knoten unterstützt 2 bis 20 Pfade. Jeder Pfad hat einen konfigurierbaren Namen und einen ganzzahligen Prozentsatz von 1 bis 99. Die Summe aller Pfadprozentsätze muss genau 100 % betragen.

>[!IMPORTANT]
>
>**Quotenbasierter Algorithmus: nicht deterministisch**
>
>Der Verteilungsalgorithmus verwendet eine auf Kontingenten basierende zufällige Zuweisung. Dieser Algorithmus ist **_nicht deterministisch_**: Dasselbe Konto kann jedes Mal einem anderen Pfad zugewiesen werden, wenn es auf die Journey gelangt oder erneut eintritt. Die Pfadzuweisung hängt vom aktuellen Kontingent-Status zum Zeitpunkt der Bewertung ab, nicht von einer festen Kontoeigenschaft. Unter [Einschränkungen](#limitations) finden Sie Einzelheiten zu den Anwendungsfällen, auf die sich dies auswirkt.

### Verteilungsalgorithmus {#distribution-algorithm}

Der Knoten für die Pfade der Variantenaufspaltung verwendet einen **_kontingentbasierten Algorithmus_** zufällige Zuweisung“. Wenn ein Konto den Knoten erreicht, wertet das System die vorhandenen Kontozuweisungen für jeden Pfad aus und leitet das Konto an den Pfad weiter, der am weitesten unter seinem konfigurierten Kontingent liegt. Es gibt zwei wichtige Eigenschaften für den Algorithmus:

* Die Verteilung verfolgt die konfigurierten Prozentsätze auf allen Kontovolumina genau. Da der Algorithmus die Anzahl der Kontingente aktiv beibehält, variiert die tatsächliche Verteilung nur um höchstens ein Konto pro Pfad. Dies ist auf eine Rundung zurückzuführen, bei der sich die Gesamtwerte nicht gleichmäßig teilen.
* Der Algorithmus verwendet eine pessimistische Sperre während der Kontingentauswertung, um Zuweisungen zu serialisieren, was eine genaue Zählungsverfolgung bei gleichzeitiger Ausführung sicherstellt.

### Einschränkungen {#limitations}

Überprüfen Sie diese Einschränkungen, bevor Sie Variantenaufspaltungspfade in Ihren Journey verwenden.

>[!CAUTION]
>
>**Pfadzuweisung ist nicht deterministisch.**
>
>Der kontingentbasierte Algorithmus garantiert nicht, dass dasselbe Konto immer demselben Pfad folgt. Wenn ein Konto existiert und die Journey erneut betritt, kann es je nach Kontingent-Status zum Zeitpunkt der erneuten Eingabe einem anderen Pfad zugewiesen werden. Verwenden Sie keine Pfade mit Variantenaufteilung für Anwendungsfälle, die eine konsistente Zuweisung von Pfaden pro Konto über Journey-Instanzen hinweg erfordern.

| Einschränkung | Beschreibung |
| ---------- | ----------- |
| **Nicht geeignet für kontrollierte Experimente** | Da die Pfadzuweisung nicht deterministisch ist, sind Variantenaufspaltungspfade **nicht geeignet** für A/B-Experimente oder Attributionsszenarien, bei denen ein bestimmtes Konto durchgängig dieselbe Behandlung erhält. Anwendungsfälle, die von der Konsistenz pro Konto abhängen, z. B. die Messung der Reaktionsraten oder die Zuweisung von Ergebnissen zu einem bestimmten Erlebnis, können zu unzuverlässigen Ergebnissen führen. |
| **Geringfügige Rundungsabweichung** | Wenn die Gesamtzahl der Konten nicht gleichmäßig durch die konfigurierten Prozentsätze teilbar ist, kann die Verteilung um höchstens ein Konto pro Pfad verschoben werden. Dies ist ein erwartetes Rundungsverhalten und kein Fehler. |
| **Pfadzuweisung ist nicht idempotent** | Beim erneuten Eingeben der Journey kann es zu einer unterschiedlichen Pfadzuweisung für dasselbe Konto kommen. Wenn Ihr Journey-Design davon ausgeht, dass ein Konto immer demselben Pfad nach dem Aufspaltungsknoten folgt, gilt diese Annahme nicht. |
| **Nur Konto-Journey** | Pfade für die Variantenaufspaltung werden nur in Account-Journey unterstützt. Personen-Journey werden derzeit nicht unterstützt. |
| **Keine bedingte Filterung** | Im Gegensatz _Aufspaltungspfade_ gelten für Pfade mit Variantenaufspaltung keine Bedingungen. Jedes Konto, das den Knoten erreicht, wird einem Pfad zugewiesen. |

## Aufspaltung nach Personen {#split-by-people}

Auf einer Konto-Journey können Sie auch einen Variantenverteilungs-Pfadknoten verwenden, um die _Personen innerhalb von Konten_ nach dem Zufallsprinzip auf prozentuale Pfade zu verteilen. Dieser Aufspaltungstyp ist nützlich, wenn Sie verschiedene Inhalte oder Erlebnisse auf Personenebene testen möchten, da Konten weiterhin den Journey durchlaufen. Die Variantenaufspaltung nach Personenknoten funktioniert mit den folgenden Leitplanken:

* Der Knoten fungiert als _gruppierter Knoten_ wobei es sich um eine Kombination aus Aufspaltung und Zusammenführung handelt. Die aufgeteilten Pfade werden automatisch an einem entsprechenden Zusammenführungsknoten geschlossen, sodass alle Personen fortfahren können, ohne ihren Kontokontext zu verlieren.
* Jede Person im Konto wird basierend auf den konfigurierten Prozentsätzen genau einem Pfad zugewiesen.
* Für Personen gilt derselbe kontingentbasierte Algorithmus, der für Konten verwendet wird. Die Pfadzuweisung ist nicht deterministisch, und dieselbe Person kann beim erneuten Eintritt einem anderen Pfad folgen.
* Innerhalb _[!UICONTROL Pfade werden nur Knoten]_ Aktion ausführen) für Personen unterstützt. Die Pfade können nicht weiter aufgeteilt werden.

>[!BEGINSHADEBOX „Verteilungsverhalten über Personen hinweg“]

Personen innerhalb eines Kontos werden als Batch verarbeitet. Die jedem Pfad zugewiesene Zahl wird als `floor(percentage / 100 × people_in_account)` berechnet, und der **zuletzt konfigurierte Pfad empfängt alle verbleibenden Personen**. Das bedeutet:

* Wenn ein Konto eine ungerade Anzahl von Personen enthält, empfängt der letzte Pfad eine weitere Person als frühere Pfade.
* Bei Konten mit einer einzelnen Person wird diese Person unabhängig von den konfigurierten Prozentsätzen immer dem ersten Pfad zugewiesen.
* Bei Accounts mit sehr wenigen Personen (weniger als 10) kann die Verteilung pro Account deutlich von den konfigurierten Prozentsätzen abweichen. Die Verteilung nähert sich den konfigurierten Verhältnissen an, wenn sie über viele Konten hinweg gemessen wird.

>[!NOTE]
>
>Dieses Rundungsverhalten gilt pro Konto-Batch, nicht für alle Konten auf der Journey. Der letzte Pfad empfängt systematisch etwas mehr Personen als konfiguriert, wenn die Kontogrößen ungerade sind. Dieses Verhalten ist normal.

>[!ENDSHADEBOX]

## Hinzufügen eines Knotens mit aufgeteilten Pfaden für Varianten {#add-variant-split-paths-node}

1. Navigieren Sie zur Journey-Karte.

1. Klicken Sie auf das Pluszeichen ( **+** ) auf einem Pfad und wählen Sie **[!UICONTROL Variantenaufspaltungspfade]** aus.

   ![Journey-Knoten hinzufügen - Aufspaltungspfade von Varianten](./assets/node-variant-split-paths-add.png){width="300" zoomable="no"}

   Der hinzugefügte Knoten verfügt über zwei Pfade zum Starten.

1. Wählen Sie in den Knoteneigenschaften auf der rechten Seite entweder **[!UICONTROL Konten]** oder **[!UICONTROL Personen]** für die Aufspaltung aus.

   Wenn Sie den Typ _[!UICONTROL Personen]_ verwenden, wird automatisch ein Knoten _Variante-Aufspaltungspfade schließen_ eingefügt, um die gruppierte Aufspaltung zu schließen.

   ![Journey-Arbeitsfläche - Variante aufgeteilt nach Personen mit automatisch eingefügtem Schließen-Knoten](./assets/node-variant-split-paths-people-canvas.png){width="700" zoomable="yes"}

1. Überprüfen oder aktualisieren Sie die **[!UICONTROL Beschriftung]** für jeden Pfad.

   Pfadbeschriftungen werden als Kantenbeschriftungen auf der Journey-Arbeitsfläche angezeigt und helfen bei der Unterscheidung von Pfaden in Journey-Analysen.

   ![Knotenpfad für Variantenaufteilung - Pfadnamenkonfiguration](./assets/node-variant-split-paths-names.png){width="600" zoomable="yes"}

1. Legen Sie **[!UICONTROL Prozentsatz]** für jeden Pfad fest.

   Werte müssen ganze Zahlen von 1 bis 99 sein.

   ![Knotenpfad für Variantenaufteilung - Konfiguration des Pfadprozentsatzes](./assets/node-variant-split-paths-config.png){width="500" zoomable="yes"}

   Der Indikator „Laufende Gesamtsumme“ zeigt die Summe aller Pfadprozentsätze an. Der Gesamtwert muss genau 100 % betragen, bevor Sie die Journey veröffentlichen können. Ein Fehlerstatus wird angezeigt, wenn die Gesamtsumme nicht 100 % beträgt.

   ![Knoten mit Variantenaufspaltung - Validierungsfehler, wenn die Gesamtsumme nicht 100 % beträgt](./assets/node-variant-split-paths-validation-error.png){width="500" zoomable="yes"}

   Um die Prozentsätze gleichmäßig auf alle Pfade zu verteilen, klicken Sie auf **[!UICONTROL Gleichmäßig verteilen]**. Das System berechnet die gleichen Anteile und passt jede Rundung an, um sicherzustellen, dass die Summe 100% entspricht.

1. Um zusätzliche Pfade zu definieren, klicken **[!UICONTROL für jeden]** auf „Pfad hinzufügen“.

   Der Knoten unterstützt bis zu 20 Pfade. Wenn Sie weitere Pfade hinzufügen, passen Sie den _[!UICONTROL Prozentsatz]_ so an, dass die Gesamtsumme 100 % beträgt.

   Sie können einen Pfad entfernen, indem Sie auf das Symbol _Löschen_ ( ![Löschsymbol](../assets/do-not-localize/icon-delete-outline.svg) ) auf der Pfadkarte klicken. Ein Pfad kann nur entfernt werden, wenn mindestens zwei Pfade verbleiben.

### Validierungsregeln {#validation-rules}

Die folgenden Regeln gelten für die Konfiguration von Pfaden für die Variantenaufspaltung. Verletzungen blockieren die Veröffentlichung von Journey.

| Regel | Anforderung |
| ---- | ----------- |
| Mindestpfade | 2 |
| Maximale Anzahl an Pfaden | 20 |
| Prozentsatz pro Pfad | Ganze Zahl von 1 bis 99 |
| Gesamtprozentsatz | Muss genau 100 % entsprechen |
