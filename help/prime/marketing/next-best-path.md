---
title: Nächster bester Pfadknoten
description: Verwenden Sie den nächstbesten Pfadknoten in Journey Optimizer B2B Prime für KI-gesteuertes Journey-Routing mit Eingabeaufforderungen in natürlicher Sprache, Pfadsimulation, Konfidenzwerten und Live-Pfadergebnissen für die Aufspaltung.
badgeBeta: label="Beta" type="informative" tooltip="Diese Funktion befindet sich derzeit in einer eingeschränkten Beta-Version"
source-git-commit: 2f19137465c71f2292d37bea5786533b1df6e286
workflow-type: tm+mt
source-wordcount: '2205'
ht-degree: 0%

---

# Nächster bester Pfadknoten

In Journey Optimizer B2B Prime bringt der Knoten *Nächster bester Pfad* die KI-gesteuerte Split Path-Entscheidungsfindung direkt in die Journey-Arbeitsfläche. Anstatt Filterbedingungen auf einem [Split-Pfade](./split-merge-paths-nodes.md)-Knoten zu konfigurieren, beschreiben Sie Ihre Absicht in natürlicher Sprache und lassen Sie das System den relevantesten Pfad für jede Person bestimmen.

Beim B2B-Kauf mag ein Profil wie eine Art Käufer erscheinen, aber ihr Verhalten, ihre firmografischen Daten und ihr Interaktionskontext offenbaren eine differenziertere Geschichte. Der nächstbeste Pfadknoten bewertet diesen Kontext, um eine intelligente Routing-Entscheidung zu treffen, während Sie alle KI-Empfehlungen vor der Aktivierung des Journey überprüfen, ändern oder überschreiben können.

## Pfadentscheidung {#path-decisioning}

Von der Absicht zur Aktivierung sind drei Schritte erforderlich.

* **Schritt 1: Pfade definieren** - Fügen Sie einen Knoten des Typs Nächster bester Pfad zu Ihrem Journey hinzu, benennen Sie jeden Pfad und schreiben Sie eine Eingabeaufforderung in natürlicher Sprache, die beschreibt, wer den Pfad abschreiten soll. Sie können Pfade jederzeit hinzufügen oder entfernen.

* **Schritt 2: Simulieren** — Wählen Sie eine Beispielzielgruppe aus und führen Sie eine Simulation aus. Sie sehen Profilanzahl pro Pfad, Konfidenzwerte und die KI-Argumentation, damit Sie die Logik vor der Aktivierung überprüfen können.

  >[!NOTE]
  >
  >Die Simulation wird nur für Beispieldaten ausgeführt und beeinflusst nie die Live-Journey-Ausführung.

* **Schritt 3: Aktivieren** - Veröffentlichen Sie die Journey für Ihre echte Audience. Die KI bewertet jede Person zur Laufzeit, weist den Pfad mit der besten Anpassung in Echtzeit zu und ein standardmäßiges Fallback stellt sicher, dass niemand in eine Sackgasse gerät.

### KI-Entscheidungseingaben {#ai-decisioning-inputs}

Wenn eine Person den Knoten erreicht, ruft das System Profilkontext ab, wendet Einschränkungen an und wählt mithilfe eines LLM den am besten geeigneten Pfad aus. Die KI bewertet jede Person anhand einer Kombination der folgenden Eingaben:

* **Interaktionsverlauf** - E-Mail-Öffnungen, Link-Klicks, Web-Seitenbesuche und andere Verhaltenssignale von aktuellen und vorherigen Journey
* **Echtzeit-Signale** - Ereignisse mit hohen Absichten wie Formularausfüllungen und Preise für Seitenbesuche
* **Profilattribute** - Demografie, Stellenbezeichnung, Rolle und firmografische Daten
* **Kontoattribute** - Mit dem Konto der Person verknüpfte firmografische und technografische Daten

### KI-Kontextbildung {#ai-context-building}

Unter der Grundlage der Routing-Entscheidung erstellt die KI für jedes Profil eine abgeleitete Ebene. Sie kombiniert demografische und firmografische Daten, Kontodetails und Verhaltenssignale (wie persönliche Details, Problemabsicht und Produktabsicht) zu einer kontextuellen Zusammenfassung für diese Person. Unter Verwendung dieses angereicherten Kontexts kann die KI jede Person zum optimalen Pfad führen und sowohl einen Konfidenzwert als auch die Logik hinter jeder Entscheidung in natürlicher Sprache bereitstellen.

Jede Entscheidung wird mit einem Konfidenzwert und einer Argumentation in natürlicher Sprache für Transparenz und Beobachtbarkeit protokolliert.

Wenn kein Pfad eine starke Übereinstimmung aufweist oder die Eingabeaufforderung auf Daten verweist, die für ein Profil nicht verfügbar sind, wird die Person zum standardmäßigen Fallback-Pfad weitergeleitet.

## Hinzufügen eines Knotens mit dem nächsten besten Pfad {#add-node}

1. Öffnen Sie die Personen-Journey und navigieren Sie zur Journey-Karte.

1. Klicken Sie auf das Pluszeichen ( **+** ) auf einem Pfad und wählen Sie **Nächster bester Pfad**.

   Der Knoten wird der Arbeitsfläche hinzugefügt und das Bedienfeld für die Konfiguration einer KI-Teilung wird auf der rechten Seite geöffnet. Sie beginnt mit einem Pfad und dem Standardpfad *Andere Personen* zum Routing von Personen, die sich für keinen der definierten Pfade qualifizieren.

## Konfigurieren von Pfaden {#configure-paths}

Definieren Sie für jeden Pfad einen Namen und eine Eingabeaufforderung in natürlicher Sprache, die beschreibt, wer dort weitergeleitet werden soll. Die Benutzeroberfläche für Filterbedingungen wird durch die Eingabeaufforderung vollständig ersetzt. Es gibt keine Attributbedingungen, die konfiguriert werden müssen.

1. Klicken Sie **Pfad hinzufügen** für jeden zusätzlichen Pfad, den Sie einbeziehen möchten.

   Um einen Pfad zu entfernen, klicken Sie auf das *Löschen*-Symbol auf der Pfadkarte.

1. Für jede Pfadkarte im rechten Bedienfeld:

   * Geben Sie einen **Titel** ein, der die Zielgruppe oder Absicht für dieses Segment widerspiegelt.

   * Geben Sie eine **Eingabeaufforderung** in natürlicher Sprache ein, die beschreibt, wer zu diesem Pfad gehört. Konzentration auf Absicht und Ergebnis, nicht auf bestimmte Attributwerte.

     **Beispiel fordert zu einer Aufteilung auf drei Pfade auf:**

      * *Pfad 1 - Personalverantwortliche:* Identifizieren Sie Personen in Personalführungsrollen, die am ehesten mit dem Talent-Management und Mitarbeitererlebnisinhalten interagieren.
      * *Pfad 2 - Technische Gutachter:* Identifizieren Sie technische Stakeholder, die mit größter Wahrscheinlichkeit mit Produktarchitektur, Integrationen und Implementierungs-Content interagieren.
      * *Pfad 3 - Entscheidungsträger in Unternehmen:* Ermitteln Sie die Stakeholder, die am ehesten mit ROI, Geschäftsergebnissen und Fallstudieninhalten zu tun haben.

1. Ordnen Sie die Pfade bei Bedarf neu an, um die Prioritätsreihenfolge für den Abgleich festzulegen.

   Die Pfadfilterung wird in der Reihenfolge von oben nach unten bewertet. Jede Person fährt auf dem ersten Pfad fort, der übereinstimmt. Klicken Sie auf die Pfeile nach oben und unten oben rechts auf jeder Pfadkarte, um sie in der Liste nach oben oder unten zu verschieben.

1. Überprüfen Sie den Standardpfad (der letzte in der Pfadliste) und ändern Sie bei Bedarf die Bezeichnung.

   Der Standardpfad wird verwendet, wenn die KI keine Person einem definierten Pfad zuweisen kann oder wenn die relevanten Daten nicht verfügbar sind. Wenn eine Eingabeaufforderung auf Daten verweist, die für ein bestimmtes Profil nicht im Datensatz vorhanden sind, leitet das System dieses Profil an den Standardpfad weiter und markiert die Datenlücke.

>[!BEGINSHADEBOX]

**Human-in-the-loop-Steuerung**

KI-Empfehlungen sind unverbindlich. Vor der Aktivierung der Journey haben Sie folgende Möglichkeiten:

* Bearbeiten Sie eine Pfadaufforderung, um die Routing-Logik zu verfeinern.
* Pfade hinzufügen, entfernen oder neu anordnen.
* Überschreiben von KI-Vorschlägen bei Bedarf mit benutzerdefinierten Bedingungen.

KI-gesteuerte Pfadzuweisungen werden erst wirksam, wenn Sie die Journey veröffentlichen.

>[!ENDSHADEBOX]

## Beispiele nach Anwendungsfall auffordern {#prompt-examples}

Die folgenden Beispiele zeigen, wie effektive Pfadaufforderungen in gängigen B2B-Marketing-Anwendungsfällen geschrieben werden. Verwenden Sie sie als Ausgangspunkte und passen Sie die Sprache an Ihren Journey-Kontext und Ihre Zielgruppendaten an.

+++Aktive Forschungs- und Kaufsignale

**Path 1 - Aktive Produktforscher**
*Identifizieren Sie Personen, die aktiv an CRM-Software forschen. Suchen Sie nach wiederholten Produktseitenbesuchen, Interaktionen mit Vergleichsinhalten, häufigen Rückkehrbesuchen und erhöhten Absichtssignalen von Drittanbietern in den letzten 30 Tagen.*

**Pfad 2 - Preisvergleichsverhalten**
*Ermitteln Sie Benutzer, die in den letzten 14 Tagen mehrmals Preis- oder Planvergleichsseiten angezeigt haben, insbesondere diejenigen, die zwischen Preis- und Funktionsdokumentationsseiten wechseln.*

**Pfad 3 - Hohe Absicht, keine Konversion**
*Identifizieren Sie Besucherinnen und Besucher, die in den letzten 21 Tagen mit Produktdemos, Preisseiten oder Integrationsdokumenten interagiert, aber kein Formular gesendet oder konvertiert haben.*

**Pfad 4 - zögerliches Checkout-Verhalten**
*Identifizieren Sie Benutzer, die den Checkout- oder Demobuchungsfluss gestartet, aber nicht abgeschlossen haben und mindestens einmal danach ohne Konvertierung zurückgekehrt sind.*

+++

+++Abwanderungs- und Kundenbindungsrisiko

**Pfad 1 - Risikosignale für Abwanderung**
*Identifizieren Sie Kunden mit Anzeichen einer Abwanderung, die auf einer rückläufigen Produktnutzung, einer reduzierten Anmeldefrequenz, Support-Ticket-Spitzen und einer verringerten Marketing-Interaktion in den letzten 60 Tagen basieren.*

**Pfad 2 - Trennung von Power-Benutzern**
*Ermitteln Sie zuvor engagierte Benutzende, deren Interaktionsgeschwindigkeit in den letzten 30 Tagen im Vergleich zu ihrer historischen Baseline signifikant gesunken ist.*

+++

+++Bildung und Evaluierungslücken

**Pfad 1 - Recherche zur Preisreihenfolge**
*Identifizieren Sie Benutzer, die ein eBook heruntergeladen und dann innerhalb von 7 Tagen die Preisseite besucht haben, aber keine Demo angefordert haben.*

**Pfad 2 - Webinar ohne Follow-up**
*Personen identifizieren, die an einem Webinar teilgenommen und anschließend zu den Produktseiten zurückgekehrt sind, aber noch nie eine Demo gebucht oder den Vertrieb kontaktiert haben.*

**Pfad 3 - Vergleichsgestützte Auswertung**
*Ermitteln Sie Besucherinnen und Besucher, die einen Artikel zum Vergleich mit Mitbewerbern angesehen und dann innerhalb von 14 Tagen die Dokumentation zu Integration oder Migration besucht haben.*

+++

+++E-Mail-Interaktionssequenzen

**Pfad 1 - Wird ohne Klicks geöffnet**
*Identifizieren Sie Leads, die innerhalb von 30 Tagen drei oder mehr Marketing-E-Mails geöffnet, aber nie auf die Website geklickt haben.*

**Pfad 2 - Angeklickt, aber keine vertiefte Interaktion**
*Identifizieren Sie Benutzer, die von einer E-Mail zu einer Produktseite geklickt haben, aber keine zusätzlichen Seiten erkundet haben oder innerhalb von 7 Tagen zurückkehrten.*

+++

+++Test- und Konversionsmuster

**Path 1 - Schnelle Konverter**
*Ermitteln Sie Kunden, die innerhalb von 30 Tagen nach Beginn einer Testversion ein Upgrade durchgeführt haben und während des Testzeitraums ein hohes Maß an Interaktionen mit dem Produkt zeigten.*

**Pfad 2 - Benutzer der Testversion angehalten**
*Ermitteln Sie Testbenutzer, die sich während der ersten Woche angemeldet haben, danach jedoch nur minimale Aktivität gezeigt haben und vor Ablauf der Testversion nicht konvertiert haben.*

+++

+++Multi-Channel-Käufer

**Pfad 1: Konvergenz von Werbung und organischer Produktion**
*Identifizieren Sie Benutzer, die zuerst über bezahlte Anzeigen interagiert und später innerhalb von 14 Tagen über direkte oder organische Kanäle zurückgegeben haben.*

**Pfad 2 - Ereignis-zu-Produkt-Evaluierung**
*Ermitteln Sie Konten, die an einer persönlichen oder virtuellen Veranstaltung teilgenommen haben, und steigerten Sie danach das Verhalten bei der Produktforschung innerhalb von 30 Tagen.*

**Path 3 - Social-to-Site-Forscher**
*Identifizieren Sie Benutzer, die mit Social-Media-Inhalten interagiert haben und später Seiten mit hohen Absichten wie Preise oder Demobuchung besucht haben.*

+++

+++Regionale Kaufsignale

**Pfad 1 - Anstieg in einer bestimmten Region**
*Ermitteln Sie Konten in Nordamerika, die in den letzten 30 Tagen eine erhöhte Produktforschungsaktivität und erhöhte Absichtserklärungen von Drittanbietern im Vergleich zu ihren historischen Ausgangswerten aufwiesen.*

**Pfad 2 - Dynamik in Schwellenländern**
*Ermitteln Sie Konten in APAC, bei denen die Interaktionsgeschwindigkeit in den letzten 14 Tagen erheblich gestiegen ist, auch wenn das gesamte Interaktionsvolumen immer noch moderat ist.*

**Pfad 3 - Regionsspezifisches Unternehmensinteresse**
*Ermitteln Sie Konten im Unternehmensbereich in EMEA, die in den letzten 21 Tagen Compliance-, Datenresidenz- oder Sicherheitsdokumentationen durchgeführt haben.*

**Pfad 4 - Unterwandertes Gebiet**
*Identifizieren Sie Konten mit hoher Anpassungsfähigkeit in zugewiesenen Verkaufsgebieten, die Absichtssignale gezeigt haben, aber noch nicht mit dem Verkauf Kontakt aufgenommen haben.*

+++

+++Zielgruppen-Targeting für Webinare

**Path 1 - HR-Leiter, die an KI interessiert sind**
*Identifizieren Sie Personen, die in den letzten 30 Tagen Interaktionen auf HR-Sites (shrm.org, hbr.org/topic/human-resource-management) hatten und sich für Journey Optimizer interessierten, die wahrscheinlich an einem Webinar zum Thema „KI im HR-Betrieb“ teilnehmen werden. Sie hätten auch ein gewisses Interesse an KI-Produkten zeigen sollen.*

**Path 2 - Finanzexperten, die sich für KI interessieren**
*Identifizieren Sie Personen, die in den letzten 30 Tagen auf Finanzwebsites (wsj.com/finance, investopedia.com) Interaktionen mit Marketo hatten und an einem Webinar zum Thema „KI in der Finanzplanung“ teilnehmen dürften. Sie hätten auch ein gewisses Interesse an KI-Produkten zeigen sollen.*

**Pfad 3 - An KI interessierte Risiko- und Forschungspersonen**
*Identifizieren Sie Personen, die in den letzten 30 Tagen an GenStudio interessiert waren und an einem Webinar zum Thema „KI im Risikomanagement“ teilnehmen werden, auf Risiko-/Forschungswebsites (mckinsey.com/capabilities/risk-and-resilience, forrester.com/research). Sie hätten auch ein gewisses Interesse an KI-Produkten zeigen sollen.*

+++

+++Verhaltens-Timing-Signale

**Pfad 1 - Nachmittagsforscher**
*Identifizieren Sie Benutzer, die außerhalb der normalen Geschäftszeiten in ihrer lokalen Zeitzone wiederholt mit Produkt- und Preisseiten interagieren.*

**Pfad 2 - Komprimiertes Forschungsfenster**
*Ermitteln Sie Konten mit ungewöhnlich hoher Interaktionsdichte innerhalb eines kurzen 72-Stunden-Fensters in mehreren Produktbereichen.*

**Pfad 3 - Aktivitätsspitze zum Quartalsende**
*Identifizieren Sie Konten mit einem Anstieg der Aktivität in der Auswertungsphase in den letzten 30 Tagen des Geschäftsquartals.*

+++

## Simulieren der Entscheidungsfindung vor der Veröffentlichung {#simulate}

Verwenden Sie eine Simulation, um zu testen, wie die KI Ihre Eingabeaufforderungen vor der Live-Schaltung der Journey gegenüber einer echten Zielgruppe auswertet. Die Simulation ist nur verfügbar, wenn sich die Journey im Status *Entwurf* befindet, und hat keine Auswirkungen auf veröffentlichte Journey.

### Simulation ausführen {#run-simulation}

1. Wählen Sie den nächstbesten Pfadknoten aus und klicken Sie oben *rechten Bedienfeld auf* Simulieren“.

1. Wählen Sie im Dialogfeld die Zielgruppe aus, die für die Simulation verwendet werden soll:

   * **[!UICONTROL Ursprüngliche Personenlisten]** - Verwenden Sie die Zielgruppe aus dem Zielgruppenknoten. Geben Sie eine Stichprobengröße an, wenn die vollständige Zielgruppe den Simulationsschwellenwert überschreitet.
   * **[!UICONTROL Dynamische und statische Listen]** - Verwenden Sie eine statische oder dynamische Marketo Engage-Liste.
   * **[!UICONTROL Testdatensätze]** - Verwenden von von KI vorgeschlagenen Testprofilen.

   >[!NOTE]
   >
   >* Wenn die ausgewählte Zielgruppe den Schwellenwert für die Simulation überschreitet, führt das System die Simulation an einem 100-Profil-Beispiel aus. Ein Indikator in der Benutzeroberfläche zeigt an, dass die Ergebnisse Beispielbasiert sind.
   >* Wenn die ausgewählte Zielgruppe noch nicht materialisiert wurde, wird die Simulation blockiert. Eine Inline-Warnung weist Sie an, die Zielgruppe zuerst zu materialisieren.

1. Klicken Sie **[!UICONTROL Simulieren]**.

### Überprüfen der Simulationsergebnisse {#review-results}

Nach der Ausführung der Simulation zeigt das rechte Bedienfeld die Verteilung der Profile auf die einzelnen Pfade und die KI-Überlegungen hinter diesen Zuweisungen an:

| Ergebnis | Beschreibung |
|---|---|
| **Profile** | Die Anzahl der an den Pfad weitergeleiteten Profile. |
| **Aufspaltung** | Der Prozentsatz der an den Pfad weitergeleiteten Profile. |
| **Konfidenz** | Die KI-Vertrauensstufe für die Pfadzuweisung. Konfidenz spiegelt die Aktualität der Daten, die Signalstärke und -konsistenz sowie den historischen Erfolg ähnlicher Routing-Muster wider. |
| **Eingabeaufforderung** | Die Aufforderung, die für den Pfad ausgewertet wurde. |
| **KI-Argumentation** | Eine Erklärung in natürlicher Sprache, warum Profile diesem Pfad gemeinsam zugewiesen wurden. |

>[!NOTE]
>
>Wenn Daten verfügbar sind oder der Umfang eine Entscheidung einschränkt, enthalten die Ergebnisse Informationen über die Einschränkung. Wenn beispielsweise ein erforderliches Attribut im Datensatz nicht vorhanden ist, enthalten die Ergebnisse einen expliziten Indikator, der erklärt, wie sich die fehlenden Daten auf die Ergebnisse ausgewirkt haben.

Verwenden Sie die Ergebnisse, um Eingabeaufforderungen zu verfeinern und zu bestätigen, dass das Routing Ihr beabsichtigtes Ergebnis widerspiegelt. Sie können Pfadaufforderungen ändern und die Simulation so oft wie nötig vor der Veröffentlichung erneut ausführen.

## Veröffentlichen und Überwachen der Journey {#publish-monitor}

Nach Validierung der Simulationsergebnisse:

1. Verbinden Sie die Zielgruppe mit dem Journey-Einstiegsknoten.

2. [Veröffentlichen der Journey](./journeys-overview.md).

Nach der Live-Schaltung des Journey wird der nächstbeste Pfadknoten zur Ausführungszeit ausgeführt. Wenn jede Person den Knoten erreicht, bewertet die KI sie in Echtzeit anhand der neuesten Signale und leitet sie zum relevantesten Pfad.

Öffnen Sie für eine veröffentlichte Journey die Journey-Zuordnung und wählen Sie den nächstbesten Pfadknoten aus, um den Abschnitt **_[!UICONTROL Live-]_**&quot; im rechten Bedienfeld anzuzeigen. Live-Ergebnisse zeigen:

* Die prozentuale Verteilung der Profile über jeden Pfad
* Der Konfidenzwert für jede Pfadzuweisung
* Argumentation auf Pfad- und Profilebene mit erweiterbaren Details für einzelne Profile

Live-Ergebnisse sind auch in der Journey-Konsole und über die Journey-Beobachtungsfunktion im KI-Hub verfügbar.