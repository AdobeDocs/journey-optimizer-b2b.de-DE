---
title: Audience Agent für B2B
description: Audience Agent B2B in Journey Optimizer B2B Edition verwendet Intent Analysis und Persona Mapping, um Einkaufsgruppen zu erstellen und B2B-Marketing-Workflows zu beschleunigen.
feature: Audiences, AI Assistant
role: User
source-git-commit: fa53458db4576af037dcf4b16ab1bf7b103b2fdd
workflow-type: tm+mt
source-wordcount: '3066'
ht-degree: 0%

---

# Audience Agent für B2B

Mit [Adobe Experience Platform Agent Orchestrator ](https://experienceleague.adobe.com/de/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator) ist Audience Agent B2B in Journey Optimizer B2B edition verfügbar. Die Verwendung dieses Agenten verbessert die Effizienz und Effektivität beim Erkunden und Skalieren von Zielgruppen, beschleunigt die Erstellung von Einkaufsgruppen und bietet nahtlose Workflows für die Journey-Aktivierung:

* **_Priorisieren der Zielgruppen nach Intent_**: Ziehen Sie Personas auf der Grundlage des Produktintents für verschiedene Zielgruppen in den Schluss und optimieren Sie die Kampagnenplanung, indem Sie die Zeit für die Audience-Validierung reduzieren.

* **_Nutzen von KI zur Erkennung von Einkaufsgruppen_**: Verwenden Sie KI, strukturierte, unstrukturierte Daten und einheitliche First-Party-Daten, um die Erkennung und Erstellung von Einkaufsgruppen zu optimieren.

![Audience Agent für B2B im Vollseitenmodus](./assets/audience-agent-full.png){width="700" zoomable="yes"}

>[!PREREQUISITES]
>
>Um Audience Agent für B2B zu verwenden, sind erforderliche Datendefinitionen und Zuordnungen vorhanden:<br/>
>
>* [Intent-Datentaxonomie/Zuordnung](../admin/intent-data.md)
>* [XDM-Feldtaxonomie/-zuordnung](#xdm-data-prerequisites)

## Audience Agent für B2B-Funktionen

| Bereich | Funktion | Geschäftswert |
| ---- | ------------ | -------------- |
| Absichtsanalyse | <li> Messen Sie die Stärke der Kontoabsicht (z. B. niedrig, mittel und hoch) für bestimmte Produkte. <li>Vergleichen Sie die Trends der Produktzinsen im Zeitverlauf (z. B. die Top-Produkte der letzten _n_ Tage). <li>Identifizieren Sie Konten, die aktiv Interesse an bestimmten Produkten zeigen. <li>Interaktionsmuster, die Kontoaktivität mit persönlicher Abdeckung kombinieren. | <li>Hilft Teams, sich zum richtigen Zeitpunkt auf die richtigen Accounts zu konzentrieren. <li>Verbessert die Pipeline-Qualität, indem Konten mit echten Kaufsignalen priorisiert werden. <li>Ermöglicht proaktive Interaktion, bevor Mitbewerber handeln. |
| Persona-Zuordnung | <li>Erkennen und ordnen Sie die wichtigsten Personas nach Produktabsicht. <li>Identifizieren Sie Personen, die am Kauf eines oder mehrerer Produkte beteiligt sind. <li>Ordnen Sie Rollen (z _B._, _Entscheidungsträger_ und _Influencer_ mit einer Begründung zu. <li>Überprüfen, warum eine bestimmte Person als Champion gilt. | <li>Stellt sicher, dass das Vertriebsteam die wahren Entscheidungsträger und Einflussnehmer einbindet. <li>Geringerer Aufwand bei Kontakten mit geringen Auswirkungen. <li>Steigert die Gewinnraten durch Abstimmung der Reichweite auf die Kaufkraftdynamik. |
| Einkaufsgruppenbewertung | <li>Bewerten Sie die Größe der Einkaufsgruppe (z. B. Gruppen mit mehr als _n_ Mitgliedern). <li>Messen Sie die persönliche Abdeckung aller Konten (z. B. unter _x_%). <li>Verfolgen Sie Rollenverteilungs- und Abdeckungslücken in Einkaufsgruppen. <li>Markieren Sie Konten mit Champions, die in den letzten Angeboten identifiziert wurden. | <li>Zeigt Abdeckungslücken, die Abschlüsse blockieren könnten. <li>Stärkt Multithreading-Strategien durch Sicherstellung einer vollständigen Rollendarstellung. <li>Verbessert die Verfolgung der Angebotsstatus durch Interaktionseinblicke auf Gruppenebene. |

## Beispiele für Eingabeaufforderungen

Diese Eingabeaufforderungsbeispiele zeigen einige Möglichkeiten auf, wie Sie den Agenten verwenden können:

* Trend-Fenster anzeigen: Früheste und letzte Aktualisierung für die Kontoproduktzielsetzung pro Produkt.
* Listen Sie `<product>` Einkaufsgruppen mit Produktabsicht und Bewertungen auf.
* Listen Sie `<product>` Personas und Rollen mit ihren Opportunity-Metriken auf (Erfolgsrate, Mitgliedschaftsrate, Anzahl).
* Wie ist die durchschnittliche Abdeckung von Account-Personas bei Accounts in `<industry>` für `<product>`?
* Welche Accounts haben eine geringe Absicht für ein Produkt, haben aber immer noch offene Möglichkeiten (die es wert sind, gepflegt zu werden)?
* Welche Accounts haben diese Woche neue Absichtssignale für `<account_name>` hinzugefügt?

## Konzepte

| Konzept | Erklärung |
| ------- | ----------- |
| Zielgruppenerkennung | Hinter den Kulissen untersucht der Agent Absichtssignale von Erstanbietern, die auf zwei Dingen basieren: Wie stark Leute mit Ihrer Marke interagieren und welche Arten von Personas sie repräsentieren. Die Analyse blickt auf die letzten 18 Monate der Aktivität zurück, um die Produktabsichten für alle Personen im Konto zu erkennen, insbesondere in der Zeit, die zum Abschluss einer Opportunity führte. Diese Analyse hilft dem Agenten, die Personas hervorzuheben, die den Deal am wahrscheinlichsten beeinflussen.<br/><br/>Manchmal haben Konten nicht alle Opportunity-Daten in perfekter Form, was jedoch in Ordnung ist, und der Agent kann die Produktabsicht weiterhin rein aus Interaktionsmustern erkennen. |
| Persona | Personas stellen die Arten von Personen dar, die mit einem Konto interagieren. Der Agent erstellt die Informationen anhand der Stellenbezeichnung, der Funktion und der Dienstaltersstufe und normalisiert diese Informationen, sodass sie in verschiedenen Konten konsistent sind. Auf diese Weise können Sie schnell erkennen, ob Sie Entscheidungsträger, Influencer oder Support-Rollen erreichen, anstatt sich in unübersichtlichen Titeln zu verlieren. Personas helfen Ihnen zu verstehen, wer Interesse zeigt, nicht nur, wie viel Interesse es gibt. <br/><br/> Wenn der Agent Personas Kaufgruppenrollen zuordnet, verwendet er den Typ der identifizierten Persona, basierend auf ihrer Stellenbezeichnung, Funktion, Dienstalter und jedem anderen Attribut, das Sie hinzufügen möchten, und ordnet sie den Rollen zu, die sie am wahrscheinlichsten bei einer Kaufentscheidung spielen, z. B. _Entscheidungsträger_, _Influencer_ oder _Champion_. Diese Rollen sind für das jeweilige Produkt relevant, sodass Sie sehen können, wer für diese Opportunity am wichtigsten ist. Der Agent zeigt auch die Abdeckung für jede Rolle an, sodass Sie schnell verstehen können, welche Rollen gut vertreten sind und wo Lücken in Ihrer Interaktionsstrategie vorhanden sein können. |
| Einkaufsgruppenrollen zuordnen | Nachdem Rollen Rollen zugeordnet wurden, fügen Sie sie zu einer Einkaufsgruppe zusammen. Stellen Sie sich das gesamte Team innerhalb des Accounts vor, das den Kauf am ehesten beeinflussen oder entscheiden wird. Jede Rolle (z _B._, _Influencer_ oder _Champion_) fügt ein Bild hinzu, sodass Sie einen klaren Überblick über das gesamte Komitee haben, das den Deal vorantreibt. <br/><br/> Wenn Sie Personen Einkaufsgruppenrollen zuordnen, nehmen Sie die Art der identifizierten Rolle, basierend auf ihrer Position, Funktion, dem Dienstalter und jedem anderen Attribut, das Sie hinzufügen möchten, und ordnen Sie sie der Rolle zu, die sie am wahrscheinlichsten bei einer Kaufentscheidung spielen, z. B. _Entscheidungsträger_, _Influencer_ oder _Champion_. Diese Rollen sind für das jeweilige Produkt relevant, sodass Sie sehen können, wer für diese Opportunity am wichtigsten ist. Der Agent zeigt die Abdeckung für jede Rolle an, sodass Sie schnell verstehen können, welche Rollen gut vertreten sind und wo Lücken in Ihrer Interaktionsstrategie bestehen können. |
| Käufergruppen | Einkaufsgruppen ermöglichen es Marketing-Experten, die wahre Komplexität von Einkaufsausschüssen zu verwalten, nicht isolierte Leads oder Accounts. Adobe Journey Optimizer B2B edition bietet die Tools (KI-gesteuerte Einblicke, rollenbasierte Journey und Vollständigkeitsverfolgung), um Struktur, Personalisierung und analytische Klarheit in diesen Prozess zu bringen, was dazu führt, dass Marketing und Vertrieb enger an den Umsatzergebnissen ausgerichtet werden.<br/><br/>Beim Erstellen einer Einkaufsgruppe geht es in Wirklichkeit darum, drei Schlüsselelemente zusammenzuführen: die richtige Zielgruppe, den Produktkontext und die Rollen der Einkaufsgruppe. Im Folgenden finden Sie eine schrittweise Vorschau der Funktionsweise: <ol><li>**Zielgruppe identifizieren** <ul><li>Zunächst deckt der Agent die Konten auf, die für Ihr Produkt am relevantesten sind. Diese Entdeckung umfasst Konten, die bereits Zinsen zeigen, und Konten mit Potenzial.<li>Innerhalb dieser Accounts werden die Personen (Ihre Schlüsselpersonen) identifiziert, die die Kaufentscheidung beeinflussen oder Teil der Kaufentscheidung sein könnten.<li>Es wählt aus den darzustellenden Konten eine Kontoliste oder eine Kontozielgruppe aus.</ul><li>**Betrachten Sie den Produktkontext**<ul><li>Als Nächstes wird das Produkt oder die Lösung betrachtet, auf das bzw. die Sie sich konzentrieren, um sicherzustellen, dass die identifizierten Personen tatsächlich für das relevant sind, was Sie verkaufen oder bewerben möchten.<li>Es hilft auch, auf Lücken in der Abdeckung hinzuweisen (vielleicht fehlen bestimmte Rollen für das Produkt), damit Sie wissen, worauf Sie sich konzentrieren müssen.</ul> <li>**Ordnen Sie Personen kaufenden Gruppenrollen zu** <ul><li>Schließlich ordnet der Agent diese Personas bestimmten Rollen in der Einkaufsgruppe zu, z. B. Entscheidungsträgern, Influencern und Champions.<li>Basierend auf dieser Zuordnung kann der Agent eine Einkaufsgruppenkomposition für Sie empfehlen, die Sie überprüfen, anpassen oder bestätigen können.</ul> </ol> Wenn diese drei Komponenten zusammenkommen, wird Ihre Einkaufsgruppe erstellt, die alle Details, Rollen und Einblicke der Mitglieder enthält. |
| Gruppen in einer Journey kaufen | Innerhalb eines Journey kann eine Einkaufsgruppe als zentrale Organisationseinheit verwendet werden, was es den Marketing-Experten ermöglicht, Erlebnisse zu entwerfen, die sich an die Dynamik der Gruppe anpassen, anstatt die Mitglieder isoliert zu behandeln. Sie können beispielsweise die gesamte Gruppe mit koordiniertem Messaging ansprechen und gleichzeitig rollenspezifische Inhalte auf Entscheidungsträger, Influencer oder Endbenutzer zuschneiden. Wenn Absichtssignale und Interaktionsdaten in fließen, können die Journey auf der Grundlage der Gruppenbereitschaft Verzweigungen erstellen, Warnhinweise für den Vertrieb aufdecken, wenn wichtige Rollen interagieren, oder automatisch Trigger-Nurture-Schritte ausführen, wenn wichtige Rollen fehlen. Dieser Fluss stellt sicher, dass jeder Touchpoint (von E-Mails über Account-basierte Anzeigen bis hin zu Vertriebsmaßnahmen) zusammenarbeitet, um die Gruppe bei ihrem Kaufprozess voranzubringen, wodurch der Konsens beschleunigt und die Reibung auf dem Weg zum Kauf verringert wird. |
| Journey in Journey Optimizer B2B edition | Eine Journey kann mit oder ohne eine Einkaufsgruppe erstellt werden, aber der Grad der Präzision und Wirkung ändert sich erheblich:<ul><li>**Ohne eine Einkaufsgruppe** basieren Journey normalerweise auf Accounts. Marketing-Experten können weiterhin Signale wie Absicht, Verhalten oder Produktinteresse verwenden, um den Trigger zu fördern, und die Reichweite zu steigern. Diese Methode funktioniert für einfachere Bewegungen oder wenn Sie nur begrenzte Daten über ein Konto haben. Es besteht jedoch die Gefahr, die breitere Palette der Stakeholder zu übersehen, die den Deal beeinflussen, was die Konversionsrate verlangsamen oder Interaktionslücken verursachen kann.<li>**Mit einer Einkaufsgruppe** werden die Journey um die gesamte Gruppe der an einer Kaufentscheidung beteiligten Rollen orchestriert. Sie können die Schritte an Meilensteinen auf Gruppenebene ausrichten (z. B. wenn der Ausschuss einen Vollständigkeitswert erreicht oder kollektive Interaktion anzeigt) und gleichzeitig Touchpoints für jede Rolle personalisieren. Mit dieser Methode können Sie eine koordinierte Multithread-Interaktion entwerfen: Ein Entscheidungsträger erhält möglicherweise strategische ROI-Inhalte, während Einflussnehmer detaillierte Produkteinblicke erhalten, und der Verkauf wird benachrichtigt, wenn kritische Rollen interagieren. Durch die Zuordnung sowohl des individuellen als auch des kollektiven Journey können Marketer und Verkäufer die Konsensbildung beschleunigen und Chancen effizienter voranbringen. </ul> |
| Opportunity-Daten zur Erkennung von Persona verwenden | Um Ihnen einen möglichst genauen Überblick darüber zu geben, wer interagiert und wo seine Interessen liegen, nähert sich der Agent dem Persona-Ranking und der Produktabsicht gemäß den folgenden Kriterien: <ul><li>Best-Case-Szenario: Wenn Sie Daten wie _Opportunity-_, _Opportunity-Abschlussdatum_ und eine klare _Zuordnung von Opportunity zu Produkt_ bereitstellen können, kann der Agent Personas sicher nach Produkt ordnen.<li>Dieses Ranking bietet ein präzises Verständnis von Interaktion und Interesse im gesamten Konto. </ul>Der Agent weiß jedoch, dass die Daten nicht immer vollständig sind, was in Ordnung ist. Es enthält intelligente Fallbacks, um die Dinge in Bewegung zu halten:<ul><li>Der Agent analysiert das Volumen der Aktivitäten und gibt den jüngsten Aktivitäten mehr Gewicht, indem er den Zeitverfall verwendet.<li>Mit dieser Gewichtung kann der Agent Personas differenzieren und ordnen, auch ohne vollständige Opportunity-Daten. </ul>Wenn es um die Verknüpfung von Opportunities mit Produkten geht, sieht der Agent wie folgt aus:<ul><li>_Ideal_: Sie stellen die Zuordnungstabelle bereit oder helfen dem Agenten bei ihrer Erstellung.<li>_Wenn nicht verfügbar_: Der Agent verwendet Fuzzy Matching, um die Punkte zu verbinden.<li>_Keine Verknüpfung_: Der Agent leitet die Produktabsicht auf der Grundlage der letzten Aktivitäten vor dem Abschlussdatum ab.</ul>Dieser mehrschichtige Ansatz stellt sicher, dass der Agent auch dann noch aussagekräftige Einblicke liefern kann, wenn die Daten nicht perfekt sind. |
| Opportunity-Analyse | Der Agent untersucht historische Opportunity-Daten, um zu verstehen, welche Faktoren am stärksten einen Gewinn vorhersagen. Dazu verwendet er drei Kerndimensionen:<ol><li>Erfolgsquote: Zeigt an, wie oft Angebote erfolgreich abgeschlossen werden, wenn bestimmte Rollen beteiligt sind. Wenn Konten mit einem bestimmten Persona-Muster (z. B. ein technischer Bewerter oder ein Entscheidungsträger auf VP-Ebene) häufiger konvertieren, gewichtet das Modell dieses Muster höher. Diese Informationen sind ein Prozentsatz der Gesamtchancen, z. B. abgeschlossene oder gewonnene Opportunitys.<li>Mitgliedschaftsrate: Misst, wie oft ein Personentyp in verschiedenen Opportunities für ein bestimmtes Produkt angezeigt wird. Wenn bestimmte Rollen durchgängig in erfolgreichen Angeboten erscheinen, deutet dies darauf hin, dass sie eine entscheidende Rolle im Kaufprozess spielen.<li>Personaler Einfluss: Quantifiziert, wie viel eine bestimmte Rolle zum Ergebnis beiträgt, nicht nur, ob sie vorhanden ist, sondern auch, wie ihre Interaktion oder Aktivitätsstufe mit Gewinnen korreliert.</ol>Gemeinsam helfen diese Signale zu entscheiden, welche Personas die stärksten Auswirkungen auf Kaufergebnisse haben, auch wenn die Opportunity-Daten unvollständig sind. Im Laufe der Zeit kann das System so wirkungsvolle Personas und Muster erkennen, die den Geschäftserfolg am ehesten vorhersagen können und dann die Account-Absicht, die Persona-Zuordnung und die Kaufempfehlungen der Gruppe beeinflussen. |
| Absicht | Wenn jemand eine Web-Seite besucht oder auf einen E-Mail-Link klickt, der sich auf ein Produkt bezieht, ist dies ein Signal, dass er interessiert ist, und das wird als _bezeichnetIntent_.<br/><br/>Der Agent beginnt mit einer Taxonomie, die im Grunde eine Liste der Produkte des Kunden und der Schlüsselwörter ist, die sie beschreiben. Diese Informationen helfen dem Agenten zu verstehen, worum es bei jedem Inhalt oder jeder Interaktion geht.<br/><br/>Als Nächstes verwendet der Agent diese Taxonomie, um Besucheraktivitäten zu kennzeichnen, z. B. welche Schlüsselwörter oder Produkte ihre Aktionen betreffen.<br/><br/>Anschließend untersucht der Agent, wie stark jemand interagiert, z. B. wie viele Seiten er besucht oder wie oft er interagiert. Anhand dieser Informationen wird der individuelle Intent Score für bestimmte Keywords, Produkte oder Produktkategorien berechnet. Sie fasst jeden Intent-Score in _Hoch_, _Medium_ oder _Niedrig_ Intent zusammen, um die Interessenstärke anzugeben. (Geringe Absicht: `<=0.2`, Medium-Absicht: `0.2 < score <= 0.6`, Hohe Absicht: `0.6 < score <= 1`)<br/><br/>Schließlich kombiniert der Agent die Absichtsbewertungen aller Personen aus demselben Unternehmen (Account), um die allgemeine Absicht auf Kontoebene anzuzeigen, die zeigt, welche Produkte oder Themen das Unternehmen am meisten interessiert zu sein scheint. |
| Rollen, die eine Einkaufsgruppe beeinflussen | Jede Einkaufsgruppe besteht aus Rollen, die unterschiedlich zur Kaufentscheidung beitragen, z. B _„Entscheidungsträger_, _Influencer_, _Champion_ und _Endbenutzer_. Jede Rolle hat unterschiedliche Auswirkungen.<br/><br/>Entscheidungsträger haben den größten Einfluss und kontrollieren in der Regel Budgetgenehmigungen. Influencer formen Evaluierung und Recommendations. Champions tragen dazu bei, einen internen Konsens herzustellen, während Endbenutzer die Eignung des Produkts überprüfen.<br/><br/>Der Agent zeigt Ihnen diese Rollen und hilft Ihnen zu verstehen, wer die Kaufentscheidung bestimmt, wo Ihre Interaktion am stärksten ist und wo Lücken in der Abdeckung bestehen könnten. Diese Informationen ermöglichen es Ihnen, sich auf die Rollen zu konzentrieren, die für dieses Produkt am wichtigsten sind. |
| Personen- oder Rollenabdeckung | Für jedes Produkt gibt es in der Regel eine Reihe von Schlüsselrollen und Rollen, von denen bekannt ist, dass sie den Kauf beeinflussen (_N_ Rollen).<br/><br/>Für jedes Konto berechnet der Agent die Abdeckung, indem er überprüft, wie viele dieser _N_-Rollen von mindestens einer Person in diesem Konto repräsentiert werden.<br/><br/>Wenn alle _N_-Rollen vorhanden sind, wird das Konto vollständig abgedeckt. Wenn nur einige Rollen dargestellt werden, ist die Abdeckung teilweise.<br/><br/>Einfach ausgedrückt: Die Rollen- und Personenabdeckung misst, wie vollständig Ihre Einkaufsgruppe für ein Produkt ist, je nachdem, ob alle wichtigen Entscheidungsträger, Einflussnehmer und Champions einbezogen werden. |

## Voraussetzungen für XDM-Daten

Audience Agent bietet Einblicke in Konten, die die First-Party-Absicht für -Produkte zeigen, und berechnet Persona und Rollen basierend auf den definierten Daten. Stellen Sie sicher, dass die folgenden vorausgesetzten Daten für die Verwendung von Audience Agent-Funktionen konfiguriert sind:

### XDM-Feldzuordnung

<table>
  <tbody>
    <tr>
      <th>XDM-Feld</th>
      <th>Entität</th>
      <th>Geschäftsdefinition</th>
      <th>Weitere Details</th>
    </tr>
    <tr>
      <td>
        <p>
          <span>b2b.accountKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>Profile</span>
        </p>
      </td>
      <td>Account-ID, die in Joins zu Opportunity-, Ereignis- und Intent-Daten verwendet wird</td>
      <td rowspan="2">Opportunity-Analyse<br/>Account-Exploration<br/>
        <br/>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>b2b.personKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>Profile</span>
        </p>
      </td>
      <td>Personenkennung, die bei Joins verwendet wird, die Ereignisdaten mit Profildaten beinhalten</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>extendedWorkDetails.department</span>
        </p>
      </td>
      <td>
        <p>
          <span>  Profile</span>
        </p>
      </td>
      <td>Job-Abteilung des Profils/der Person</td>
      <td rowspan="5">
        <p>
          <br/>
        </p>
        <p>Persona-Zuordnung</p>
      </td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>extendedWorkDetails.jobTitle</span>
        </p>
      </td>
      <td>
        <p>
          <span>  Profile</span>
        </p>
      </td>
      <td>Berufsbezeichnung des Profils/der Person, das/die in der Rollenberechnung verwendet wird</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>person.name.firstName</span>
        </p>
      </td>
      <td>
        <p>
          <span >Profile</span>
        </p>
      </td>
      <td>Vorname der Person, der von Audience Agent zur Anzeige von Namen in der Benutzeroberfläche verwendet wird, wenn ein Kriterium erfüllt ist</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>person.name.fullName</span>
        </p>
      </td>
      <td>
        <p>
          <span> Profile</span>
        </p>
      </td>
      <td>Vollständiger Name der Person, der von Audience Agent zur Anzeige von Namen in der Benutzeroberfläche verwendet wird, wenn ein Kriterium erfüllt ist</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>person.name.lastName</span>
        </p>
      </td>
      <td>
        <p>
          <span> Profile</span>
        </p>
      </td>
      <td>Nachname der Person, von Audience Agent zur Anzeige von Namen in der Benutzeroberfläche verwendet, wenn ein Kriterium erfüllt ist</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span> Konten</span>
        </p>
      </td>
      <td>Account-ID, die in Joins zu Opportunity-, Ereignis- und Intent-Daten verwendet wird</td>
      <td>Opportunity-Analyse<br/>Account-Exploration</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountName</span>
        </p>
      </td>
      <td>
        <p>
          <span>Konten</span>
        </p>
      </td>
      <td>Name des Kontos, das von Audience Agent verwendet wird, um in der Benutzeroberfläche anzuzeigen, wenn ein Kriterium in der Benutzerabfrage erfüllt ist</td>
      <td rowspan="4">
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>Account Exploration</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountDescription</span>
        </p>
      </td>
      <td>
        <p>
          <span>Konten</span>
        </p>
      </td>
      <td>Beschreibung des Kontos/Unternehmens, das von Audience Agent verwendet wird, um einen Filter auf Konten basierend auf der Benutzerabfrage in der Benutzeroberfläche anzuwenden </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountOrganization.industry</span>
        </p>
      </td>
      <td>
        <p>
          <span>  Konten </span>
        </p>
      </td>
      <td>Von Audience Agent verwendete Konto-/Unternehmensbranche, um Kontofilter basierend auf Benutzerabfragen in der Benutzeroberfläche anzuwenden </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountBillingAddress.region</span>
        </p>
      </td>
      <td>
        <p>
          <span>  Konten </span>
        </p>
      </td>
      <td>Rechnungsadresse des Kontos/Unternehmens, das von Audience Agent verwendet wird, um Kontofilter basierend auf Benutzerabfragen in der Benutzeroberfläche anzuwenden </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>Opportunity</span>
        </p>
      </td>
      <td>Account-ID, die in Joins zu Opportunity-, Ereignis- und Intent-Daten verwendet wird</td>
      <td rowspan="2">
        <p>Opportunity Analysis<br/>Account Exploration</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>unityKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>Opportunity</span>
        </p>
      </td>
      <td>Opportunity-Kennung, die in Verknüpfungen zu Account-Daten verwendet wird</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>unityName</span>
        </p>
      </td>
      <td>
        <p>
          <span> Opportunity</span>
        </p>
      </td>
      <td>Name der von Audience Agent verwendeten Opportunity </td>
      <td rowspan="5">
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>Opportunity-Analyse</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>isWon</span>
        </p>
      </td>
      <td>
        <p>
          <span>Opportunity</span>
        </p>
      </td>
      <td>Ob die Opportunity gewonnen ist (binär)</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>OpportunityDescription</span>
        </p>
      </td>
      <td>
        <p>
          <span>Opportunity</span>
        </p>
      </td>
      <td>Beschreibung der von Audience Agent verwendeten Opportunity </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>OpportunityAmount</span>
        </p>
      </td>
      <td>
        <p>
          <span>Opportunity</span>
        </p>
      </td>
      <td>An Opportunity beteiligter Betrag von $</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>unityType</span>
        </p>
      </td>
      <td>
        <p>
          <span>Opportunity</span>
        </p>
      </td>
      <td>Opportunity-Typ</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>unityStage</span>
        </p>
      </td>
      <td>
        <p>
          <span> Opportunity</span>
        </p>
      </td>
      <td>Stufe der Opportunity (geschlossene, gewonnene oder verlorene oder irgendeine der Zwischenstufen) </td>
      <td rowspan="4">
        <p>Opportunity-Analyse<br/>Account-Exploration</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>actualCloseDate</span>
        </p>
      </td>
      <td>
        <p>
          <span>Opportunity</span>
        </p>
      </td>
      <td>Tatsächliches Abschlussdatum der Opportunity</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>expectedCloseDate</span>
        </p>
      </td>
      <td>
        <p>
          <span> Opportunity</span>
        </p>
      </td>
      <td>Voraussichtliches Abschlussdatum der Opportunity</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>extSourceSystemAudit.createdDate</span>
        </p>
      </td>
      <td>
        <p>
          <span>Opportunity</span>
        </p>
      </td>
      <td>Erstellungsdatum für diese Opportunity</td>
    </tr>
  </tbody>
</table>

### Taxonomiedaten

Audience Agent nutzt die in Journey Optimizer B2B edition erkannte First-Party-Absicht:

1. Intent Computation erfordert Taxonomiedaten (Kundenprodukte und entsprechende Keywords) von Kunden > Taxonomie
1. Taxonomiedaten werden zur Kennzeichnung von Ereignisdaten (Asset-Kennzeichnung) verwendet. Diese Daten bieten Einblicke darüber, welche Keywords und Produkte Besucherinnen und Besucher basierend auf ihren Ereignisdaten > Asset-Kennzeichnung interessieren 
1. Bezeichnete Assets (Ereignisdaten) werden mit dem Verhalten der Besucher (Anzahl der besuchten Seiten) kombiniert, um eine Besucherabsicht auf Keyword-, Produkt- und Produktkategorieebene → die Absichtsberechnung zu bestimmen
1. Absichtsbewertungen auf Besucherprofilebene werden auf Kontoebene aggregiert, um die Kontoabsicht in einem bestimmten Keyword, einer bestimmten Produkt- und Produktkategorie > Absichtskonto-Aggregation zu bestimmen

Zusätzlich zu „Konfigurieren der [-Taxonomie“ sind die folgenden Felder ](../admin/intent-data.md):

<table>
  <tbody>
    <tr>
      <th>XDM-Feld</th>
      <th>Entität</th>
      <th>Geschäftsdefinition</th>
    </tr>
    <tr>
      <th>
        <br/>
      </th>
      <th>
        <br/>
      </th>
      <td>Personenprofil</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>_acp_system_metadata.primaryIdentity.namespace.code<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Profil</span>
        </p>
      </td>
      <td>Hilft bei der Identifizierung einer Person (E-Mail- oder B2B_Person-Kennung)</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>_acp_system_metadata.primaryIdentity.id
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Profil</span>
        </p>
      </td>
      <td>namespace_id</td>
    </tr>
    <tr>
      <td>
        <ul>
          <li>Schlüsselwort_ID</li>
          <li>Schlüsselwort_name</li>
          <li>product_id</li>
          <li>product_name</li>
          <li>product_category_id</li>
          <li>product_category_name</li>
        </ul>
      </td>
      <td>
        <p>
          <br/>
        </p>
      </td>
      <td>Wird als Taxonomie zum Kennzeichnen von Assets verwendet (Erlebnisereignisse wie angeklickte E-Mails, besuchte Web-Seiten)</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>Zeitstempel</span>
        </p>
      </td>
      <td>
        <p>
          <span>Erlebnisereignis</span>
        </p>
      </td>
      <td>Wird für die Zeit zum Aufstocken und inkrementellen Ausführen verwendet</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>eventType</span>
        </p>
      </td>
      <td>
        <p>
          <span>Erlebnisereignis</span>
        </p>
      </td>
      <td>Ermitteln Sie den Ereignistyp, da der Agent nur vier Ereignisse verarbeitet (<span>directMarketing.emailClicked, directMarketing.emailOpened, directMarketing.emailUnsubscribed, web.webpagedetails.pageViews)</span>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingName</span>
        </p>
      </td>
      <td>
        <p>
          <span>Erlebnisereignis</span>
        </p>
      </td>
      <td>Nur zur Referenz-/Buchhaltung; Informationen zum Kampagnennamen</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingKey.sourceID</span>
        </p>
      </td>
      <td>
        <p>
          <span>Erlebnisereignis</span>
        </p>
      </td>
      <td>Nur zur Referenz-/Buchhaltung; Informationen zur Quell-ID, an die die E-Mail gerichtet ist</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingKey.sourceInstanceID<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Erlebnisereignis</span>
        </p>
      </td>
      <td>Nur zur Referenz-/Buchhaltung; Informationen zur Quellinstanz, an die die E-Mail gerichtet ist</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingKey.sourceKey<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Erlebnisereignis</span>
        </p>
      </td>
      <td>Dient zum Abrufen des E-Mail-Inhalts aus dem Marketo Engage-Rechenzentrum. Er besteht aus (SourceID@SourceInsatceID.SourceType)</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingKey.sourceType<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Erlebnisereignis</span>
        </p>
      </td>
      <td>Nur für Referenz-/Buchführung; Informationen über die Art der Quelle oder woher die Quelle stammt </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Erlebnisereignis</span>
        </p>
      </td>
      <td>Informationen über die Quelle, an die die E-Mail gesendet wird</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.name<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Erlebnisereignis</span>
        </p>
      </td>
      <td>Tatsächliche URL zum Abrufen von Inhalten</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.queryParameters</span>
        </p>
      </td>
      <td>
        <p>
          <span>Erlebnisereignis</span>
        </p>
      </td>
      <td>Zusätzlicher Abfrageparameter für die URL zum Abrufen zielgerichteter Inhalte </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.isPersonalizedURL</span>
        </p>
      </td>
      <td>
        <p>
          <span>Erlebnisereignis</span>
        </p>
      </td>
      <td>Nur für Referenz-/Buchhaltung</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.sourceID<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Erlebnisereignis</span>
        </p>
      </td>
      <td>Nur zur Referenz-/Buchhaltung; Informationen zur Quell-ID, an die die E-Mail gerichtet ist</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.sourceInstanceID<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Erlebnisereignis</span>
        </p>
      </td>
      <td>Nur zur Referenz-/Buchhaltung; Informationen zur Quellinstanz, an die die E-Mail gerichtet war</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.sourceKey<br/>
          </span>
        </p>
      </td>
      <td>
        <span>Erlebnisereignis</span>
      </td>
      <td>Nur zur Referenz/Buchführung; es besteht aus (SourceID@SourceInsatceID.SourceType)</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.sourceType</span>
        </p>
      </td>
      <td>
        <span>Erlebnisereignis</span>
      </td>
      <td>Nur für Referenz-/Buchführung; Informationen über die Art der Quelle oder woher die Quelle stammt</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.URL</span>
        </p>
      </td>
      <td>
        <span>Erlebnisereignis</span>
      </td>
      <td>Wird zum Abrufen der tatsächlichen URL verwendet, wenn web.webPageDetails.name nicht über diese verfügt.</td>
    </tr>
  </tbody>
</table>
