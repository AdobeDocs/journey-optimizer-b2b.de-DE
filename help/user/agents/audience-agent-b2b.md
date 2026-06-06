---
title: Audience Agent B2B
description: Audience Agent B2B in Journey Optimizer B2B edition verwendet Intent Analysis und Persona Mapping, um Einkaufsgruppen zu erstellen und B2B-Marketing-Workflows zu beschleunigen.
feature: Agentic AI, Audiences
role: User
exl-id: c1210912-66ba-4b5f-8f3b-96eb6280c926
autotag-review: '2026-06-05T16:43:42.459Z'
TQID: 'https://experienceleague.adobe.com/d7KMYbH0NpoYGnBdTCmCpzLgpGIYfNP-YIFCQUjZpIg'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: afadf741-c5fe-42cd-8013-23bb6ff2d1bc
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
  - id: bef5003b-cad2-4f40-bdb2-a80426d52ef5
subfeature_v2:
  - id: ff10f619-348f-47e3-99bf-3ce4c817cf2c
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: f8667931-f646-4dd3-af2a-b9d0cb8098ad
source-git-commit: b43117c1e47f698d62b29f56b4713ac776c497a0
workflow-type: tm+mt
source-wordcount: 2500
ht-degree: 2%

---

# Audience Agent B2B

Mit [Adobe Experience Platform Agent Orchestrator &#x200B;](https://experienceleague.adobe.com/de/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator) ist Audience Agent B2B in Journey Optimizer B2B edition verfügbar. Die Verwendung dieses Agenten verbessert die Effizienz und Effektivität beim Erkunden und Skalieren von Zielgruppen, beschleunigt die Erstellung von Einkaufsgruppen und bietet nahtlose Workflows für die Journey-Aktivierung:

* **_Priorisieren der Zielgruppen nach Intent_**: Ziehen Sie Personas auf der Grundlage des Produktintents für verschiedene Zielgruppen in den Schluss und optimieren Sie die Kampagnenplanung, indem Sie die Zeit für die Audience-Validierung reduzieren.

* **_Nutzen von KI zur Erkennung und Erstellung von Einkaufsgruppen_**: Verwenden Sie KI, strukturierte, unstrukturierte Daten und einheitliche First-Party-Daten, um die Erkennung und Erstellung von Einkaufsgruppen zu optimieren.

![Audience Agent B2B im Vollseitenmodus](./assets/audience-agent-full.png){width="700" zoomable="yes"}

>[!PREREQUISITES]
>
>Für die Verwendung von Audience Agent B2B sind erforderliche Datendefinitionen und Zuordnungen vorhanden:<br/>
>
>* [Intent-Datentaxonomie/Zuordnung](../admin/intent-data.md)
>* [XDM-Feldtaxonomie/-zuordnung](#xdm-data-prerequisites)

## Audience Agent B2B-Funktionen

| Bereich | Funktion | Geschäftswert |
| ---- | ------------ | -------------- |
| Absichtsanalyse | <li> Messen Sie die Stärke der Kontoabsicht (z. B. niedrig, mittel und hoch) für bestimmte Produkte. <li>Vergleichen Sie die Trends der Produktzinsen im Zeitverlauf (z. B. die Top-Produkte der letzten _n_ Tage). <li>Identifizieren Sie Konten, die aktiv Interesse an bestimmten Produkten zeigen. <li>Interaktionsmuster, die Kontoaktivität mit persönlicher Abdeckung kombinieren. | <li>Hilft Teams, sich zum richtigen Zeitpunkt auf die richtigen Accounts zu konzentrieren. <li>Verbessert die Pipeline-Qualität, indem Konten mit echten Kaufsignalen priorisiert werden. <li>Ermöglicht proaktive Interaktion, bevor Mitbewerber handeln. |
| Persona-Mapping | <li>Erkennen und ordnen Sie die wichtigsten Personas nach Produktabsicht. <li>Identifizieren Sie Personen, die am Kauf eines oder mehrerer Produkte beteiligt sind. <li>Ordnen Sie Rollen (z _B._, _Entscheidungsträger_ und _Influencer_ mit einer Begründung zu. <li>Überprüfen, warum eine bestimmte Person als Champion gilt. | <li>Stellt sicher, dass das Vertriebsteam die wahren Entscheidungsträger und Einflussnehmer einbindet. <li>Geringerer Aufwand bei Kontakten mit geringen Auswirkungen. <li>Steigert die Gewinnraten durch Abstimmung der Reichweite auf die Kaufkraftdynamik. |
| Einkaufsgruppenbewertung | <li>Bewerten Sie die Größe der Einkaufsgruppe (z. B. Gruppen mit mehr als _n_ Mitgliedern). <li>Messen Sie die persönliche Abdeckung aller Konten (z. B. unter _x_%). <li>Verfolgen Sie Rollenverteilungs- und Abdeckungslücken in Einkaufsgruppen. <li>Markieren Sie Konten mit Champions, die in den letzten Angeboten identifiziert wurden. | <li>Zeigt Abdeckungslücken, die Abschlüsse blockieren könnten. <li>Stärkt Multithreading-Strategien durch Sicherstellung einer vollständigen Rollendarstellung. <li>Verbessert die Verfolgung der Angebotsstatus durch Interaktionseinblicke auf Gruppenebene. |
| Erstellung und Verwertbarkeit von Einkaufsgruppen | <li>Auf beobachteten Rollen- und Rollenmustern basierende Rollen-zu-Rollen-Zuordnungen empfehlen. <li>Generieren Sie eine Vorlage für die Einkaufsgruppenrolle für ein bestimmtes Produkt. <li>Unterstützen Sie die Anpassung von Vorlagen, indem Sie bestimmte Rollen und Personas ein- oder ausschließen. <li>Überprüfen Sie, ob die erforderlichen Rollen definiert sind, bevor Sie Einkaufsgruppen erstellen. | <li>Reduziert manuellen Aufwand und Risiko unvollständiger Einkaufsgruppenvorlagen. <li>Stellt sicher, dass die Rollenabdeckung vor der Erstellung validiert wird, wodurch das Risiko von Abdeckungslücken verringert wird. <li>Wandelt Analyseeinblicke in sofortige, operative nächste Schritte um. |

## Einschränkungen

Audience Agent B2B hängt von der konfigurierten Intent-Taxonomie, den XDM-Feldzuordnungen und Erlebnisereignisdaten ab. Einblicke sind weniger zuverlässig, wenn Opportunity-Daten unvollständig sind, die Intent-Taxonomie fehlt oder veraltet ist oder die erforderlichen Profil- und Account-IDs nicht zugeordnet sind. Für die Absichtsberechnung verarbeitet der Agent nur diese Erlebnisereignisse: `directMarketing.emailClicked`, `directMarketing.emailOpened`, `directMarketing.emailUnsubscribed` und `web.webpagedetails.pageViews`.

## Beispiele für Prompts

Diese Eingabeaufforderungsbeispiele zeigen einige der Möglichkeiten auf, wie Sie den Agenten verwenden können:

* Trend-Fenster anzeigen: Früheste und neueste Aktualisierungen für die Kontoproduktzielsetzung pro Produkt.
* Listen Sie `<product>` Einkaufsgruppen mit Produktabsicht und Bewertungen auf.
* Listen Sie `<product>` Personas und Rollen mit ihren Opportunity-Metriken auf (Erfolgsrate, Mitgliedschaftsrate, Anzahl).
* Wie ist die durchschnittliche Abdeckung von Account-Personas bei Accounts in `<industry>` für `<product>`?
* Welche Accounts haben eine geringe Absicht für ein Produkt, haben aber immer noch offene Möglichkeiten (die es wert sind, gepflegt zu werden)?
* Welche Accounts haben diese Woche neue Absichtssignale für `<account_name>` hinzugefügt?
* Anzeigen der mit `<product>` verknüpften Rollen
* Zeigen Sie mir die Empfehlung der Rollenzuordnung zu Persona-Zuordnung für `<product>`.
* Erstellen Sie eine Einkaufsgruppenvorlage für `<product>`.
* Erstellen Sie eine Einkaufsgruppenvorlage für `<product>` ohne `<persona>` und entfernen Sie die Rolle `<role>` .

## Konzepte

| Konzept | Erklärung |
| ------- | ----------- |
| Zielgruppenerkennung | Hinter den Kulissen untersucht der Agent Absichtssignale von Erstanbietern, die auf zwei Dingen basieren: Wie stark Leute mit Ihrer Marke interagieren und welche Arten von Personas sie repräsentieren. Die Analyse blickt auf die letzten 18 Monate der Aktivität zurück, um die Produktabsichten für alle Personen im Konto zu erkennen, insbesondere in der Zeit, die zum Abschluss einer Opportunity führte. Diese Analyse hilft dem Agenten, die Personas hervorzuheben, die den Deal am wahrscheinlichsten beeinflussen.<br/><br/>Manchmal haben Konten nicht alle Opportunity-Daten in perfekter Form, was jedoch in Ordnung ist, und der Agent kann die Produktabsicht weiterhin rein aus Interaktionsmustern erkennen. |
| Persona | Personas stellen die Arten von Personen dar, die mit einem Konto interagieren. Der Agent erstellt sie, indem er sich die Stellenbezeichnung, die Funktion und die Dienstaltersstufe ansieht und diese Informationen dann normalisiert, sodass sie in verschiedenen Konten konsistent sind. Auf diese Weise können Sie schnell erkennen, ob Sie Entscheidungsträger, Influencer oder Support-Rollen erreichen, anstatt sich in unübersichtlichen Titeln zu verlieren. Personas helfen Ihnen zu verstehen, wer Interesse zeigt, nicht nur, wie viel Interesse es gibt. |
| Einkaufsgruppenrollen zuordnen | Nachdem Rollen Rollen zugeordnet wurden, fügen Sie sie zu einer Einkaufsgruppe zusammen - dem gesamten Team innerhalb des Kontos, das den Kauf am wahrscheinlichsten beeinflusst oder entscheidet. Jede Rolle (z _B._, _Influencer_ oder _Champion_) fügt ein Bild hinzu, damit Sie einen klaren Überblick über das Komitee haben, das den Deal vorantreibt.<br/><br/>Der Agent ordnet jede identifizierte Rolle der Rolle zu, die sie am wahrscheinlichsten für ein bestimmtes Produkt spielen, basierend auf der Stellenbezeichnung, der Funktion, dem Dienstalter und anderen von Ihnen konfigurierten Attributen. Es wird auch die Abdeckung für jede Rolle angezeigt, damit Sie sehen können, welche Rollen gut repräsentiert sind und wo Lücken in Ihrer Interaktionsstrategie verbleiben. |
| Opportunity-Daten zur Erkennung von Persona verwenden | Um Ihnen einen möglichst genauen Überblick darüber zu geben, wer interagiert und wo seine Interessen liegen, nähert sich der Agent dem Persona-Ranking und der Produktabsicht gemäß den folgenden Kriterien: <ul><li>Best-Case-Szenario: Wenn Sie Daten wie _Opportunity-_, _Opportunity-Abschlussdatum_ und eine klare _Zuordnung von Opportunity zu Produkt_ bereitstellen können, kann der Agent Personas sicher nach Produkt ordnen.<li>Dieses Ranking bietet ein präzises Verständnis von Interaktion und Interesse im gesamten Konto. </ul>Der Agent weiß jedoch, dass die Daten nicht immer vollständig sind, was in Ordnung ist. Es enthält intelligente Fallbacks, um die Dinge in Bewegung zu halten:<ul><li>Der Agent analysiert das Volumen der Aktivitäten und gibt den jüngsten Aktivitäten mehr Gewicht, indem er den Zeitverfall verwendet.<li>Mit dieser Gewichtung kann der Agent Personas differenzieren und ordnen, auch ohne vollständige Opportunity-Daten. </ul>Wenn es um die Verknüpfung von Opportunities mit Produkten geht, sieht der Agent wie folgt aus:<ul><li>_Ideal_: Sie stellen die Zuordnungstabelle bereit oder helfen dem Agenten bei ihrer Erstellung.<li>_Wenn nicht verfügbar_: Der Agent verwendet Fuzzy Matching, um die Punkte zu verbinden.<li>_Keine Verknüpfung_: Der Agent leitet die Produktabsicht auf der Grundlage der letzten Aktivitäten vor dem Abschlussdatum ab.</ul>Dieser mehrschichtige Ansatz stellt sicher, dass der Agent auch dann noch aussagekräftige Einblicke liefern kann, wenn die Daten nicht perfekt sind. |
| Opportunity-Analyse | Der Agent untersucht historische Opportunity-Daten, um zu verstehen, welche Faktoren am stärksten einen Gewinn vorhersagen. Dazu verwendet er drei Kerndimensionen:<ol><li>Erfolgsquote: Zeigt an, wie oft Angebote erfolgreich abgeschlossen werden, wenn bestimmte Rollen beteiligt sind. Wenn Konten mit einem bestimmten Persona-Muster (z. B. ein technischer Bewerter oder ein Entscheidungsträger auf VP-Ebene) häufiger konvertieren, gewichtet das Modell dieses Muster höher. Diese Informationen sind ein Prozentsatz der Gesamtchancen, z. B. abgeschlossene oder gewonnene Opportunitys.<li>Mitgliedschaftsrate: Misst, wie oft ein Personentyp in verschiedenen Opportunities für ein bestimmtes Produkt angezeigt wird. Wenn bestimmte Rollen durchgängig in erfolgreichen Angeboten erscheinen, deutet dies darauf hin, dass sie eine entscheidende Rolle im Kaufprozess spielen.<li>Personaler Einfluss: Quantifiziert, wie viel eine bestimmte Rolle zum Ergebnis beiträgt, nicht nur, ob sie vorhanden ist, sondern auch, wie ihre Interaktion oder Aktivitätsstufe mit Gewinnen korreliert.</ol>Gemeinsam helfen diese Signale zu entscheiden, welche Personas die stärksten Auswirkungen auf Kaufergebnisse haben, auch wenn die Opportunity-Daten unvollständig sind. Im Laufe der Zeit kann das System so wirkungsvolle Personas und Muster erkennen, die den Geschäftserfolg am ehesten vorhersagen können und dann die Account-Absicht, die Persona-Zuordnung und die Kaufempfehlungen der Gruppe beeinflussen. |
| Absicht | Wenn jemand eine Web-Seite besucht oder auf einen E-Mail-Link klickt, der sich auf ein Produkt bezieht, ist dies ein Signal, dass er interessiert ist, und das wird als _bezeichnetIntent_.<br/><br/>Der Agent beginnt mit einer Taxonomie, die im Grunde eine Liste der Produkte des Kunden und der Schlüsselwörter ist, die sie beschreiben. Diese Informationen helfen dem Agenten zu verstehen, worum es bei jedem Inhalt oder jeder Interaktion geht.<br/><br/>Anschließend verwendet der Agent diese Taxonomie, um Besucheraktivitäten zu kennzeichnen, z. B. welche Schlüsselwörter oder Produkte ihre Aktionen betreffen.<br/><br/>Anschließend untersucht der Agent, wie stark jemand interagiert, z. B. wie viele Seiten er besucht oder wie oft er interagiert. Anhand dieser Informationen wird der individuelle Intent Score für bestimmte Keywords, Produkte oder Produktkategorien berechnet. Sie fasst jeden Intent-Score in _Hoch_, _Medium_ oder _Niedrig_ Intent zusammen, um die Interessenstärke anzugeben. (Geringe Absicht: `<=0.2`, Medium-Absicht: `0.2 < score <= 0.6`, Hohe Absicht: `0.6 < score <= 1`)<br/><br/>Schließlich kombiniert der Agent die Absichtsbewertungen aller Personen aus demselben Unternehmen (Account), um die allgemeine Absicht auf Kontoebene anzuzeigen, die zeigt, welche Produkte oder Themen das Unternehmen am meisten interessiert zu sein scheint. |
| Rollen, die eine Einkaufsgruppe beeinflussen | Jede Einkaufsgruppe besteht aus Rollen, die unterschiedlich zur Kaufentscheidung beitragen, z. B _„Entscheidungsträger_, _Influencer_, _Champion_ und _Endbenutzer_. Jede Rolle hat unterschiedliche Auswirkungen.<br/><br/>Entscheidungsträger haben den größten Einfluss und kontrollieren in der Regel Budgetgenehmigungen. Influencer formen Evaluierung und Recommendations. Champions tragen dazu bei, einen internen Konsens herzustellen, während Endbenutzer die Eignung des Produkts überprüfen.<br/><br/>Der Agent zeigt Ihnen diese Rollen und hilft Ihnen zu verstehen, wer die Kaufentscheidung bestimmt, wo Ihre Interaktion am stärksten ist und wo Lücken in der Abdeckung bestehen könnten. Diese Informationen ermöglichen es Ihnen, sich auf die Rollen zu konzentrieren, die für dieses Produkt am wichtigsten sind. |
| Personen- oder Rollenabdeckung | Für jedes Produkt gibt es in der Regel eine Reihe von Schlüsselrollen und Rollen, von denen bekannt ist, dass sie den Kauf beeinflussen (_N_ Rollen oder Rollen).<br/><br/>Für jedes Konto berechnet der Agent die Abdeckung, indem er überprüft, wie viele dieser _N_-Rollen von mindestens einer Person innerhalb dieses Kontos repräsentiert werden.<br/><br/>Wenn alle _N_-Rollen vorhanden sind, wird das Konto vollständig abgedeckt. Wenn nur einige Rollen dargestellt werden, ist die Abdeckung teilweise.<br/><br/>Einfach ausgedrückt: Die Rollen- und Personenabdeckung misst, wie vollständig Ihre Einkaufsgruppe für ein Produkt ist, je nachdem, ob alle wichtigen Entscheidungsträger, Einflussnehmer und Champions einbezogen werden. |

## Voraussetzungen für XDM-Daten

Audience Agent bietet Einblicke in Konten, die die First-Party-Absicht für -Produkte zeigen, und berechnet Personas und Rollen basierend auf den definierten Daten. Stellen Sie sicher, dass die folgenden vorausgesetzten Daten für die Verwendung von Audience Agent-Funktionen konfiguriert sind:

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
          <span> Profile</span>
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
          <span> Profile</span>
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
          <span> Konten</span>
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
          <span> Konten</span>
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

Zusätzlich zu „Konfigurieren der [-Taxonomie“ sind die folgenden Felder &#x200B;](../admin/intent-data.md):

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
      <td>Nur zur Referenz/Buchhaltung; Informationen zum Kampagnennamen</td>
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
      <td>Nur zu Referenz-/Buchhaltungszwecken; Informationen zur Quell-ID, an die die E-Mail gerichtet ist</td>
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
      <td>Nur zu Referenz-/Buchhaltungszwecken; Informationen zur Quellinstanz, an die die E-Mail gerichtet ist</td>
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
      <td>Dient zum Abrufen des E-Mail-Inhalts aus dem Marketo Engage-Rechenzentrum. Er besteht aus (SourceID@SourceInstanceID.SourceType)</td>
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
      <td>Nur zur Referenz/Buchführung; Informationen über die Art der Quelle oder woher die Quelle stammt </td>
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
      <td>Informationen zur Herkunft der Quelle für den Web-Seitenbesuch</td>
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
      <td>Nur für Referenz/Buchhaltung</td>
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
      <td>Nur zu Referenz-/Buchhaltungszwecken; Informationen zur Quell-ID, an die die E-Mail gerichtet ist</td>
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
      <td>Nur zu Referenz-/Buchhaltungszwecken; Informationen zur Quellinstanz, an die die E-Mail gerichtet war</td>
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
      <td>Nur zur Referenz/Buchhaltung; es besteht aus (SourceID@SourceInstanceID.SourceType)</td>
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
      <td>Nur zur Referenz/Buchführung; Informationen über die Art der Quelle oder woher die Quelle stammt</td>
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
