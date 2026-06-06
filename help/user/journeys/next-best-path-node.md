---
title: Nächster bester Pfadknoten
description: Verwenden Sie KI-gestützte Entscheidungsfindung , um Personen auf der Grundlage von Eingabeaufforderungen in natürlicher Sprache, Verhaltensdaten und Echtzeit-Profilkontext in Journey Optimizer B2B edition auf den relevantesten Journey-Pfad zu leiten.
feature: Account Journeys, AI Assistant
role: User
autotag-review: '2026-05-20T18:52:08.227Z'
TQID: 'https://experienceleague.adobe.com/idPaG-ZNnNwJjN8yVC3Ay1FZ2XPgtQgrSMNIus4fReI'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
subfeature_v2:
  - id: ba367494-9862-4596-bd6f-299c7e10a46b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: c4147b6e-073b-4d3c-9ab1-d60f2f4434ef
source-git-commit: 7cd6c4ecfbbd3a86b4f30d1b4fe6f06655a9c4f5
workflow-type: tm+mt
source-wordcount: 1912
ht-degree: 0%

---

# Nächster bester Pfadknoten

Der Knoten _Nächster bester Pfad_ bringt die KI-gesteuerte Split-Path-Entscheidung direkt in die Journey-Arbeitsfläche. Anstatt Filterbedingungen auf einem [Split-Pfade](./split-merge-paths-nodes.md)-Knoten zu konfigurieren, beschreiben Sie Ihre Absicht in natürlicher Sprache und lassen Sie das System den relevantesten Pfad für jede Person bestimmen.

>[!NOTE]
>
>Die nächstbesten Pfadknoten sind nur in Personen-Journey verfügbar. Sie werden in Account-Journey nicht unterstützt.

Beim B2B-Kauf mag ein Profil wie eine Art Käufer erscheinen, aber ihr Verhalten, ihre firmografischen Daten und ihr Interaktionskontext offenbaren eine differenziertere Geschichte. Der nächstbeste Pfadknoten bewertet diesen Kontext, um eine intelligente Routing-Entscheidung zu treffen, während Sie alle KI-Empfehlungen vor der Aktivierung des Journey überprüfen, ändern oder überschreiben können.

Die KI bewertet jede Person anhand Ihrer definierten Pfadaufforderungen mithilfe einer Kombination von Eingaben:

* **Interaktionsverlauf** - E-Mail-Öffnungen, Link-Klicks, Web-Seitenbesuche und andere Verhaltenssignale von aktuellen und vorherigen Journey
* **Echtzeit-Signale** - Ereignisse mit hohen Absichten wie Formularausfüllungen und Preise für Seitenbesuche
* **Profilattribute** - Demografie, Stellenbezeichnung, Rolle und firmografische Daten
* **Kontoattribute** - Mit dem Konto der Person verknüpfte firmografische und technografische Daten

Wenn eine Person den Knoten erreicht, ruft das System Profilkontext ab, wendet Einschränkungen an und wählt mithilfe eines LLM den am besten geeigneten Pfad aus. Jede Entscheidung wird mit einem Konfidenzwert und einer Argumentation in natürlicher Sprache für Transparenz und Beobachtbarkeit protokolliert.

Wenn kein Pfad eine starke Übereinstimmung aufweist oder die Eingabeaufforderung auf Daten verweist, die für ein Profil nicht verfügbar sind, wird die Person zum standardmäßigen Fallback-Pfad weitergeleitet.

## Hinzufügen eines Knotens mit dem nächsten besten Pfad {#add-next-best-path-node}

1. Öffnen Sie die Personen-Journey und navigieren Sie zur Journey-Karte.

1. Klicken Sie auf das Pluszeichen ( **+** ) auf einem Pfad und wählen Sie **[!UICONTROL Nächster bester Pfad]**.

   ![Journey-Knoten hinzufügen - nächster optimaler Pfad](./assets/add-node-next-best-path.png){width="350" zoomable="no"}

   Der Knoten wird der Arbeitsfläche hinzugefügt und das Bedienfeld für die Konfiguration der KI-Teilung wird auf der rechten Seite angezeigt. Sie beginnt mit einem Pfad und dem Standardpfad _Andere Personen_ zum Routing von Personen, die sich für keinen der definierten Pfade qualifizieren.

   ![Nächster bester Pfadknoten](./assets/node-next-best-path-new.png){width="500"}

## Konfigurieren von Pfaden {#configure-paths}

Definieren Sie für jeden Pfad einen Namen und eine Eingabeaufforderung in natürlicher Sprache, die beschreibt, wer dort weitergeleitet werden soll. Die Benutzeroberfläche für Filterbedingungen wird durch die Eingabeaufforderung vollständig ersetzt. Es gibt keine Attributbedingungen, die konfiguriert werden müssen.

1. Klicken Sie **[!UICONTROL Pfad hinzufügen]** für jeden zusätzlichen Pfad, den Sie für den Knoten einschließen möchten.

   Um einen Pfad zu entfernen, klicken Sie auf das Symbol _Löschen_ ( ![Löschsymbol](../assets/do-not-localize/icon-delete-outline.svg) ) auf der Pfadkarte.

1. Für jede Pfadkarte im rechten Bedienfeld:

   * Geben Sie einen **[!UICONTROL Titel]** ein, der die Zielgruppe oder Absicht für dieses Segment widerspiegelt.

   * Geben Sie eine **[!UICONTROL Eingabeaufforderung]** in natürlicher Sprache ein, die beschreibt, wer zu diesem Pfad gehört. Konzentration auf Absicht und Ergebnis, nicht auf bestimmte Attributwerte.

     <!-- To get prompt ideas, click **[!UICONTROL Suggest prompts]**. The system provides several example prompts tailored to the path context that you can use as-is or adapt. -->

     ![Nächster bester Pfadknoten - Beispielpfade](./assets/node-next-best-path-new.png){width="500"}

     **Beispiel fordert zu einer Aufteilung auf drei Pfade auf:**

      * _Path 1 - HR Leaders :_Identifizieren Sie Personen in HR-Führungsrollen, die am ehesten mit dem Talent-Management und Mitarbeitererlebnisinhalten zu tun haben.
      * _Path 2 - Technische Gutachter :_Identifizieren Sie technische Stakeholder, die mit größter Wahrscheinlichkeit mit Produktarchitektur, Integrationen und Implementierungs-Content interagieren.
      * _Path 3 - Entscheidungsträger aus dem :_: Ermitteln Sie die Stakeholder aus dem Unternehmen, die am ehesten mit ROI, Geschäftsergebnissen und Fallstudieninhalten zu tun haben.

1. Ordnen Sie die Pfade bei Bedarf neu an, um die Prioritätsreihenfolge für den Abgleich festzulegen.

   Die Pfadfilterung wird in der Reihenfolge von oben nach unten bewertet. Jede Person fährt auf dem ersten Pfad fort, der übereinstimmt.

   Klicken Sie auf die Pfeile nach oben und unten oben rechts auf jeder Pfadkarte, um sie in der Liste der Pfade nach oben oder unten zu verschieben.

   ![Nächster bester Pfadknoten - Pfade neu anordnen](./assets/node-next-best-path-reorder-paths.png){width="500"}

1. Überprüfen Sie den Standardpfad (der letzte in der Pfadliste) und ändern Sie bei Bedarf die Bezeichnung.

   Der Standardpfad wird verwendet, wenn die KI keine Person einem definierten Pfad zuweisen kann oder wenn die relevanten Daten nicht verfügbar sind. Wenn eine Eingabeaufforderung auf Daten verweist, die für ein bestimmtes Profil nicht im Datensatz vorhanden sind, leitet das System dieses Profil an den Standardpfad weiter und markiert die Datenlücke.

### Human-in-the-Loop-Steuerung {#human-in-the-loop}

KI-Empfehlungen sind unverbindlich. Vor der Aktivierung der Journey haben Sie folgende Möglichkeiten:

* Bearbeiten Sie eine Pfadaufforderung, um die Routing-Logik zu verfeinern.
* Pfade hinzufügen, entfernen oder neu anordnen.
* Überschreiben von KI-Vorschlägen bei Bedarf mit benutzerdefinierten Bedingungen.

KI-gesteuerte Pfadzuweisungen werden erst wirksam, wenn Sie die Journey veröffentlichen.

## Beispiele nach Anwendungsfall auffordern {#examples}

Die folgenden Beispiele zeigen, wie effektive Pfadaufforderungen in gängigen B2B-Marketing-Anwendungsfällen geschrieben werden. Verwenden Sie sie als Ausgangspunkte und passen Sie die Sprache an Ihren Journey-Kontext und Ihre Zielgruppendaten an.

### Aktive Forschungs- und Kaufsignale {#active-research}

+++Pfad 1 - Aktive Produktforscher

_Identifizieren Sie Personen, die aktiv an CRM-Software forschen. Suchen Sie nach wiederholten Produktseitenbesuchen, Interaktionen mit Vergleichsinhalten, häufigen Rückkehrbesuchen und erhöhten Absichtssignalen von Drittanbietern in den letzten 30 Tagen._

+++

+++Pfad 2: Preisvergleichsverhalten

_Ermitteln Sie Benutzer, die in den letzten 14 Tagen mehrmals Preis- oder Planvergleichsseiten angezeigt haben, insbesondere diejenigen, die zwischen Preis- und Funktionsdokumentationsseiten wechseln._

+++

+++Pfad 3: Hohe Absicht, keine Konversion

_Identifizieren Sie Besucherinnen und Besucher, die in den letzten 21 Tagen mit Produktdemos, Preisseiten oder Integrationsdokumenten interagiert, aber kein Formular gesendet oder konvertiert haben._

+++

+++Pfad 4: Zögerliches Checkout-Verhalten

_Identifizieren Sie Benutzer, die den Checkout- oder Demobuchungsfluss gestartet, aber nicht abgeschlossen haben und mindestens einmal danach ohne Konvertierung zurückgekehrt sind._

+++

### Abwanderungs- und Kundenbindungsrisiko {#churn-retention}

+++Pfad 1: Risikosignale für Abwanderung

_Identifizieren Sie Kunden mit Anzeichen einer Abwanderung, die auf einer rückläufigen Produktnutzung, einer reduzierten Anmeldefrequenz, Support-Ticket-Spitzen und einer verringerten Marketing-Interaktion in den letzten 60 Tagen basieren._

+++

+++Pfad 2: Trennung der Hauptanwender

_Ermitteln Sie zuvor engagierte Benutzende, deren Interaktionsgeschwindigkeit in den letzten 30 Tagen im Vergleich zu ihrer historischen Baseline signifikant gesunken ist._

+++

### Bildung und Evaluierungslücken {#education-evaluation}

+++Pfad 1: Recherche zur Preisreihenfolge

_Identifizieren Sie Benutzer, die ein eBook heruntergeladen und dann innerhalb von 7 Tagen die Preisseite besucht haben, aber keine Demo angefordert haben._

+++

+++Pfad 2: Webinar ohne Follow-up

_Personen identifizieren, die an einem Webinar teilgenommen und anschließend zu den Produktseiten zurückgekehrt sind, aber noch nie eine Demo gebucht oder den Vertrieb kontaktiert haben._

+++

+++Pfad 3: vergleichsgesteuerte Auswertung

_Ermitteln Sie Besucherinnen und Besucher, die einen Artikel zum Vergleich mit Mitbewerbern angesehen und dann innerhalb von 14 Tagen die Dokumentation zu Integration oder Migration besucht haben._

+++

### E-Mail-Interaktionssequenzen {#email-engagement}

+++Pfad 1: Wird ohne Klicks geöffnet

_Identifizieren Sie Leads, die innerhalb von 30 Tagen drei oder mehr Marketing-E-Mails geöffnet, aber nie auf die Website geklickt haben._

+++

+++Pfad 2 - Angeklickt, aber keine eingehendere Interaktion

_Identifizieren Sie Benutzer, die von einer E-Mail zu einer Produktseite geklickt haben, aber keine zusätzlichen Seiten erkundet haben oder innerhalb von 7 Tagen zurückkehrten._

+++

### Test- und Konversionsmuster {#trial-conversion}

+++Pfad 1: Schnelle Konverter

_Ermitteln Sie Kunden, die innerhalb von 30 Tagen nach Beginn einer Testversion ein Upgrade durchgeführt haben und während des Testzeitraums ein hohes Maß an Interaktionen mit dem Produkt zeigten._

+++

+++Pfad 2: Benutzer der Testversion stoppen

_Ermitteln Sie Testbenutzer, die sich während der ersten Woche angemeldet haben, danach jedoch nur minimale Aktivität gezeigt haben und vor Ablauf der Testversion nicht konvertiert haben._

+++

### Multi-Channel-Käufer {#multi-channel}

+++Pfad 1: Konvergenz von Werbung und organischer Produktion

_Identifizieren Sie Benutzer, die zuerst über bezahlte Anzeigen interagiert und später innerhalb von 14 Tagen über direkte oder organische Kanäle zurückgegeben haben._

+++

+++Pfad 2 - Ereignis-zu-Produkt-Evaluierung

_Ermitteln Sie Konten, die an einer persönlichen oder virtuellen Veranstaltung teilgenommen haben, und steigerten Sie danach das Verhalten bei der Produktforschung innerhalb von 30 Tagen._

+++

+++Pfad 3: Social-to-Site-Forscher

_Identifizieren Sie Benutzer, die mit Social-Media-Inhalten interagiert haben und später Seiten mit hohen Absichten wie Preise oder Demobuchung besucht haben._

+++

### Regionale Kaufsignale {#regional-buying}

+++Pfad 1: Anstieg in einer bestimmten Region

_Ermitteln Sie Konten in Nordamerika, die in den letzten 30 Tagen eine erhöhte Produktforschungsaktivität und erhöhte Absichtserklärungen von Drittanbietern im Vergleich zu ihren historischen Ausgangswerten aufwiesen._

+++

+++Pfad 2: Dynamik in Schwellenländern

_Ermitteln Sie Konten in APAC, bei denen die Interaktionsgeschwindigkeit in den letzten 14 Tagen erheblich gestiegen ist, auch wenn das gesamte Interaktionsvolumen immer noch moderat ist._

+++

+++Pfad 3: Regionsspezifisches Unternehmensinteresse

_Ermitteln Sie Konten im Unternehmensbereich in EMEA, die in den letzten 21 Tagen Compliance-, Datenresidenz- oder Sicherheitsdokumentationen durchgeführt haben._

+++

+++Pfad 4 - Unterwandertes Gebiet

_Identifizieren Sie Konten mit hoher Anpassungsfähigkeit in zugewiesenen Verkaufsgebieten, die Absichtssignale gezeigt haben, aber noch nicht mit dem Verkauf Kontakt aufgenommen haben._

+++

### Verhaltens-Timing-Signale {#behavioral-timing}

+++Pfad 1: Nachmittagsforscher

_Identifizieren Sie Benutzer, die außerhalb der normalen Geschäftszeiten in ihrer lokalen Zeitzone wiederholt mit Produkt- und Preisseiten interagieren._

+++

+++Pfad 2: Komprimiertes Forschungsfenster

_Ermitteln Sie Konten mit ungewöhnlich hoher Interaktionsdichte innerhalb eines kurzen 72-Stunden-Fensters in mehreren Produktbereichen._

+++

+++Pfad 3: Aktivitätsspitze zum Quartalsende

_Identifizieren Sie Konten mit einem Anstieg der Aktivität in der Auswertungsphase in den letzten 30 Tagen des Geschäftsquartals._

+++

## Simulieren der Entscheidungsfindung vor der Veröffentlichung {#simulate}

Verwenden Sie eine Simulation, um zu testen, wie die KI Ihre Eingabeaufforderungen vor der Live-Schaltung der Journey gegenüber einer echten Zielgruppe auswertet. Sie ist nur verfügbar, wenn sich die Journey im Status _Entwurf_ befindet, und hat keine Auswirkungen auf veröffentlichte Journey. Verwenden Sie sie, um die Routing-Logik zu validieren und Vertrauen in die KI-Empfehlungen aufzubauen.

### Simulation ausführen {#run-simulation}

1. Wählen Sie den nächstbesten Pfadknoten aus und klicken Sie oben _rechten Bedienfeld auf_ Simulieren![&#x200B; ((](../../assets/do-not-localize/icon-simulate-outline.svg)) ).

   ![Nächster bester Pfad - Klicken Sie auf das Symbol „Simulieren“](./assets/node-next-best-path-simulate-select.png){width="500"}

1. Wählen Sie im Dialogfeld die Zielgruppe aus, die für die Simulation verwendet werden soll:

   * **[!UICONTROL Ursprüngliche Personenlisten]** - Verwenden Sie die Zielgruppe aus dem Zielgruppenknoten. Geben Sie eine Stichprobengröße an, wenn die vollständige Zielgruppe den Simulationsschwellenwert überschreitet.
   * **[!UICONTROL Dynamische und statische Listen]** - Verwenden Sie eine [!DNL Marketo Engage] statische oder dynamische Liste.
   * **[!UICONTROL Testdatensätze]** - Verwenden von von KI vorgeschlagenen Testprofilen.

   ![Nächster bester Pfad - Simulieren - Zielgruppe wählen](./assets/node-next-best-path-simulate-dialog.png){width="300"}

   >[!NOTE]
   >
   >Wenn die ausgewählte Zielgruppe den Schwellenwert für die Simulation überschreitet, führt das System die Simulation an einem 100-Profil-Beispiel aus. Ein Indikator in der Benutzeroberfläche zeigt an, dass die Ergebnisse Beispielbasiert sind.
   >
   >Wenn die ausgewählte Zielgruppe noch nicht materialisiert wurde, wird die Simulation blockiert. Eine Inline-Warnung weist Sie an, die Zielgruppe zuerst zu materialisieren.

1. Klicken Sie **[!UICONTROL Simulieren]**.

### Überprüfen der Simulationsergebnisse {#review-simulation-results}

Nach den Simulationsausführungen zeigt das rechte Bedienfeld an, wie die Profile auf die einzelnen Pfade verteilt wurden, und beschreibt die KI-Logik hinter diesen Zuweisungen:

| Ergebnis | Beschreibung |
| ------ | ----------- |
| **Profile** | Die Anzahl der an den Pfad weitergeleiteten Profile. |
| **Aufspaltung** | Der Prozentsatz der an den Pfad weitergeleiteten Profile. |
| **Konfidenz** | Die KI-Vertrauensstufe für die Pfadzuweisung. Konfidenz spiegelt die Aktualität der Daten, die Signalstärke und -konsistenz sowie den historischen Erfolg ähnlicher Routing-Muster wider. |
| **Eingabeaufforderung** | Die Aufforderung, die für den Pfad ausgewertet wurde. |
| **KI-Argumentation** | Eine Erklärung in natürlicher Sprache, warum Profile diesem Pfad gemeinsam zugewiesen wurden. |

![Nächster bester Pfad - Simulieren - Ergebnisse für Pfad](./assets/node-next-best-path-simulate-path-result.png){width="400"}

>[!NOTE]
>
>Wenn Daten verfügbar sind oder der Umfang eine Entscheidung einschränkt, enthalten die Ergebnisse Informationen über die Einschränkung. Wenn beispielsweise ein erforderliches Attribut im Datensatz nicht vorhanden ist, enthalten die Ergebnisse einen expliziten Indikator, der erklärt, wie sich die fehlenden Daten auf die Ergebnisse ausgewirkt haben.

Verwenden Sie die Ergebnisse, um Eingabeaufforderungen zu verfeinern und zu bestätigen, dass das Routing Ihr beabsichtigtes Ergebnis widerspiegelt. Sie können Pfadaufforderungen ändern und die Simulation so oft wie nötig vor der Veröffentlichung erneut ausführen.

## Veröffentlichen und Überwachen der Journey {#publish-and-monitor}

Nach Validierung der Simulationsergebnisse:

1. Verbinden Sie die Zielgruppe mit dem Journey-Einstiegsknoten.

1. [Veröffentlichen der Journey](./create-publish-journey.md#publish-a-journey).

Nach der Live-Schaltung des Journey wird der nächstbeste Pfadknoten zur Ausführungszeit ausgeführt. Wenn jede Person den Knoten erreicht, bewertet die KI sie in Echtzeit anhand der neuesten Signale und leitet sie zum relevantesten Pfad.

Öffnen Sie für eine veröffentlichte Journey die Journey-Zuordnung und wählen Sie den nächstbesten Pfadknoten aus, um den Abschnitt **[!UICONTROL Live-]**&quot; im rechten Bedienfeld anzuzeigen. Live-Ergebnisse zeigen:

* Die prozentuale Verteilung der Profile über jeden Pfad
* Der Konfidenzwert für jede Pfadzuweisung
* Argumentation auf Pfad- und Profilebene mit erweiterbaren Details für einzelne Profile

Live-Ergebnisse sind auch in der Journey-Konsole und über die [Journey-Beobachtungsfunktion](../agents/journey-agent.md#journey-observability-skill) im KI-Hub verfügbar.
