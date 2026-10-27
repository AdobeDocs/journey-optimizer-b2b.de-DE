---
title: Zielgruppenkenntnisse für B2B-Konten und Personen
description: Erfahren Sie mehr über Zielgruppenfähigkeiten für B2B-Konten und Personen. Erkunden Sie die Produktabsicht, identifizieren Sie Rollen, bewerten Sie die Rollenabdeckung und erstellen Sie Einkaufsgruppenvorlagen.
feature: Agentic AI, Audiences
role: User
exl-id: c1210912-66ba-4b5f-8f3b-96eb6280c926
autotag-review: '2026-06-05T16:43:42.459Z'
TQID: 'https://experienceleague.adobe.com/d7KMYbH0NpoYGnBdTCmCpzLgpGIYfNP-YIFCQUjZpIg'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: afadf741-c5fe-42cd-8013-23bb6ff2d1bc
    internal-label: Buying Groups
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
  - id: bef5003b-cad2-4f40-bdb2-a80426d52ef5
    internal-label: AI Assistant
subfeature_v2:
  - id: ff10f619-348f-47e3-99bf-3ce4c817cf2c
    internal-label: Agentic AI
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
    internal-label: Artificial intelligence
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
  - id: f8667931-f646-4dd3-af2a-b9d0cb8098ad
    internal-label: Taxonomy
source-git-commit: ce5504e7a539c38b489fddc103358029edf1cfba
workflow-type: tm+mt
source-wordcount: '1692'
ht-degree: 1%
---
# Zielgruppenkenntnisse für B2B-Konten und Personen

Verwenden Sie Zielgruppenkenntnisse für B2B in der [!DNL CX Coworker]. Erkunden Sie die Produktabsichten von Konten und Personen hinweg. Identifizieren Sie relevante Personas, bewerten Sie die Abdeckung der Einkaufsgruppe und erstellen Sie Vorlagen für die Einkaufsgruppenrolle.

* Bewerten Sie das Kontointeresse an bestimmten Produkten und vergleichen Sie Absichtstrends.
* Identifizieren Sie Personen und Rollen, die mit Produktinteressen verbunden sind.
* Überprüfen Sie die Rolle der Einkaufsgruppe und ermitteln Sie Deckungslücken.
* Generieren und Verfeinern von Vorlagen für Einkaufsgruppen-Rollen.

>[!PREREQUISITES]
>
>Bevor Sie Zielgruppen-Fähigkeiten für B2B-Konten und Personen verwenden, konfigurieren Sie die folgenden Datendefinitionen und -zuordnungen:
>
>* [Intent-Datentaxonomie und -Zuordnung](../admin/intent-data.md)
>* [XDM-Feldzuordnung](#xdm-data-prerequisites)

Klicken Sie auf _[!DNL Coworker]_ ( ![Fragen [!DNL Coworker]](../assets/do-not-localize/icon-ask-coworker.svg) ) oben in der Anwendung, um die [!DNL Coworker] Anwendung zu öffnen. Geben Sie in der Chat-Oberfläche Ihre Aufforderung in natürlicher Sprache ein.

![Zielgruppen-Eingabeaufforderung in [!DNL CX Coworker]](./assets/audience-skills-prompt.png){width="800" zoomable="yes"}

## Zielgruppen-Kompetenz-Fokusbereiche

Verwenden Sie Zielgruppen-Fokusbereiche, um die Account-Absicht zu untersuchen, Personen und Rollen zu verstehen und Kaufgruppenvorlagen vorzubereiten.

| Focus | Aufgaben |
| ----- | ----- |
| Kontoabsicht | Bewerten Sie die Kontoabsicht für bestimmte Produkte mithilfe einer niedrigen, mittleren und hohen Absichtsebene. Vergleichen Sie die Entwicklung der Produktzinsen im Zeitverlauf und ermitteln Sie Konten, die Interesse an bestimmten Produkten zeigen. Überprüfen Sie die Interaktionsmuster zusammen mit der persönlichen Abdeckung. |
| Personen und Rollen | Personas in einem oder mehreren Produkten nach Produktabsicht identifizieren und ordnen Überprüfen Sie Opportunity-Metriken, einschließlich Gewinnrate, Mitgliedschaftsrate und Anzahl. Ordnen Sie Rollen wie _Champion_, _Entscheidungsträger_ und _Influencer_ zu und überprüfen Sie Erklärungen für Rollenzuweisungen. |
| Abdeckung der Einkaufsgruppe | Bewerten Sie die Größe der Einkaufsgruppe und die persönliche Abdeckung aller Konten. Überprüfen Sie die Rollenverteilung und identifizieren Sie fehlende Rollen oder Personas. Finden Sie Konten mit Champions, die in den letzten Angeboten identifiziert wurden. |
| Einkaufsgruppenvorlagen | Generieren von Rollenvorlagen für Einkaufsgruppen für bestimmte Produkte und Überprüfen empfohlener Rollenzuordnungen. Verfeinern von Vorlagen durch Einschließen oder Ausschließen von Rollen und Personas. Validieren Sie die erforderlichen Rollen, bevor Sie Einkaufsgruppen erstellen. |

## Einschränkungen

Zielgruppeneinblicke hängen von der konfigurierten Intent-Taxonomie, den XDM-Feldzuordnungen und den Erlebnisereignisdaten ab. Unvollständige Opportunity-Daten, fehlende oder veraltete Taxonomien oder fehlende Profil- und Kontokennungen können die Zuverlässigkeit von insight beeinträchtigen.

Die Absichtsberechnung verwendet nur diese Erlebnisereignisse: `directMarketing.emailClicked`, `directMarketing.emailOpened`, `directMarketing.emailUnsubscribed` und `web.webpagedetails.pageViews`.

## Beispiele für Prompts

Geben Sie die folgenden Eingabeaufforderungen in der [!DNL CX Coworker] ein, um die Kontoabsicht zu untersuchen, Personen und Rollen zu verstehen und Kaufgruppenvorlagen vorzubereiten.

### Kontoabsicht

Erkunden Sie das Kontointeresse an Produkten und überprüfen Sie die Änderungen in der Absicht.

* Trend-Fenster anzeigen: Früheste und neueste Aktualisierungen für die Kontoproduktzielsetzung pro Produkt.
* Welche Accounts haben eine geringe Absicht für ein Produkt, haben aber immer noch offene Möglichkeiten (die es wert sind, gepflegt zu werden)?
* Welche neuen Absichtssignale wurden diese Woche für `<account_name>` aufgezeichnet?

### Personen und Rollen

Identifizieren Sie die mit dem Produktinteresse verknüpften Personen und überprüfen Sie die empfohlenen Einkaufsgruppenrollen.

* Anzeigen der mit `<product>` verknüpften Rollen
* Zeigen Sie mir die Empfehlung der Rollenzuordnung zu Persona-Zuordnung für `<product>`.
* Listen Sie `<product>` Personas und Rollen mit ihren Opportunity-Metriken auf (Erfolgsrate, Mitgliedschaftsrate, Anzahl).

### Einkaufsgruppen und Vorlagen

Überprüfen Sie die Einkaufsgruppenabsicht und -abdeckung und generieren oder verfeinern Sie dann Vorlagen.

* Listen Sie `<product>` Einkaufsgruppen mit Produktabsicht und Bewertungen auf.
* Wie ist die durchschnittliche Abdeckung von Account-Personas bei Accounts in `<industry>` für `<product>`?
* Erstellen Sie eine Einkaufsgruppenvorlage für `<product>`.
* Erstellen Sie eine Einkaufsgruppenvorlage für `<product>` ohne `<persona>` und entfernen Sie die Rolle `<role>` .

## Konzepte

Verwenden Sie diese Konzepte, um Kontoabsicht, persönliches Ranking und Kaufgruppenempfehlungen zu interpretieren.

| Konzept | Erklärung |
| ------- | ----------- |
| Zielgruppenerkennung | Analysieren Sie First-Party-Interaktionssignale von Personen in einem -Konto, um Produktinteressen und relevante Personas zu identifizieren. In der Analyse werden die vorherigen 18 Monate der Aktivität berücksichtigt, einschließlich der Aktivität vor Abschluss der Opportunity. Interaktionsmuster können auf eine Produktabsicht hinweisen, wenn die Opportunity-Daten unvollständig sind. Fehlende Daten können jedoch die Zuverlässigkeit von insight beeinträchtigen. |
| Persona | Personas gruppieren Personen nach normalisierter Stellenbezeichnung, Funktion und Dienstalter. Verwenden Sie Personas, um zu verstehen, wer mit einem Account interagiert, einschließlich Entscheidungsträgern, Influencern und Support-Rollen. |
| Einkaufsgruppenrollen zuordnen | Ordnen Sie den produktspezifischen Einkaufsgruppenrollen Personas basierend auf Auftragstitel, Funktion, Dienstalter und konfigurierten Attributen zu. Diese Rollen repräsentieren die Personen innerhalb eines Accounts, die einen Kauf beeinflussen oder entscheiden. Überprüfen Sie die Abdeckung, um fehlende Rollen zu identifizieren. |
| Opportunity-Daten für persönliches Ranking | Das Opportunity-Stadium, das Abschlussdatum und die Zuordnung von Opportunity zu Produkt unterstützen das persönliche Ranking für jedes Produkt. Wenn Opportunity-Daten unvollständig sind, verwendet das Ranking das Aktivitätsvolumen und den Zeitverfall, um der letzten Aktivität mehr Gewicht zu verleihen.<br/><br/>Produktverknüpfung verwendet eine bereitgestellte oder generierte Tabelle für die Zuordnung von Opportunity zu Produkt, sofern verfügbar. Andernfalls verknüpft der Fuzzy Matching Opportunities mit Produkten. Wenn keine Verknüpfung verfügbar ist, wird die Produktabsicht aus der letzten Aktivität vor dem Opportunity-Abschlussdatum abgeleitet. Durch diese Fallback-Methoden werden die Zuverlässigkeitsbeschränkungen unvollständiger Daten nicht beseitigt. |
| Opportunity-Analyse | Die historische Opportunity-Analyse verwendet drei Dimensionen, um die mit den Kaufergebnissen verbundenen Persönlichkeitsmuster zu identifizieren:<ul><li>Erfolgsquote: Misst, wie oft Gelegenheiten gewonnen werden, wenn bestimmte Rollen beteiligt sind. Persönliche Muster, die mit höheren Gewinnraten verbunden sind, erhalten mehr Gewicht.</li><li>Mitgliedschaftsrate: Misst, wie oft eine Rolle in Opportunities für ein bestimmtes Produkt angezeigt wird.</li><li>Persönlicher Einfluss: Misst, wie die persönliche Interaktion oder Aktivität mit Gewinnen korreliert, und geht darüber hinaus, ob die Rolle vorhanden ist.</li></ul>Diese Signale geben Aufschluss über die Kontoabsicht, die persönliche Zuordnung und die Kaufempfehlungen der Gruppe. |
| Absicht | Die Absicht zeigt das Produktinteresse durch Interaktion an, z. B. Web-Seitenbesuche oder E-Mail-Link-Klicks. Die Produkttaxonomie verbindet Interaktionsaktivitäten mit Schlüsselwörtern, Produkten und Produktkategorien. Interaktionstiefe und -frequenz bestimmen individuelle Absichtswerte für jedes Keyword, Produkt oder jede Produktkategorie.<br/><br/>Scores zeigen die Interessensstärke: Niedriger Intent: `<=0.2`, Medium Intent: `0.2 < score <= 0.6`, hoher Intent: `0.6 < score <= 1`.<br/><br/>Die individuellen Intent-Scores werden für alle Personen im selben Konto aggregiert, um den Account-Intent zu bestimmen. |
| Rollen, die eine Einkaufsgruppe beeinflussen | Die Rolle der Einkaufsgruppe stellt verschiedene Beiträge zu einer Kaufentscheidung dar. _Entscheidungsträger_ steuern normalerweise Budgetgenehmigungen. _Influencer_ Formauswertung und Empfehlungen. _Champions_ erzielen einen internen Konsens. _Endbenutzer_ Überprüfen Sie die Produktpassung.<br/><br/>Prüfen Sie die Rollenzuweisungen und -abdeckung, um zu verstehen, wer die Entscheidung beeinflusst und wo weiterhin Interaktionslücken bestehen. |
| Personen- oder Rollenabdeckung | Die Abdeckung misst, wie viele erwartete Rollen oder Personas mindestens einen Vertreter in einem Konto haben. Bei einem Produkt mit _N_ erwarteten Rollen oder Rollen bedeutet die vollständige Abdeckung, dass alle _N_ dargestellt werden. Teilweise Abdeckung bedeutet, dass einige fehlen. Nutzen Sie die Abdeckung, um die Vollständigkeit der Einkaufsgruppe zu bewerten und Lücken zu identifizieren. |

## Voraussetzungen für XDM-Daten

Konfigurieren Sie die folgenden XDM-Feldzuordnungen, um die Analyse der Kontoabsicht, die Identifikation von Personen und die Zuordnung der Einkaufsgruppenrolle zu unterstützen.

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
      <td>Zeigt den Vornamen der Person in Ergebnissen an, die Ihrer Abfrage entsprechen.</td>
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
      <td>Zeigt den vollständigen Namen der Person in Ergebnissen an, die Ihrer Abfrage entsprechen.</td>
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
      <td>Zeigt den Nachnamen der Person in Ergebnissen an, die Ihrer Abfrage entsprechen.</td>
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
      <td>Zeigt den Kontonamen in den Ergebnissen an, die Ihrer Abfrage entsprechen.</td>
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
      <td>Unterstützt die Kontofilterung nach Kontobeschreibung auf der Grundlage Ihrer Abfrage.</td>
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
      <td>Unterstützt die Filterung von Konten nach Branchen basierend auf Ihrer Abfrage.</td>
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
      <td>Unterstützt die Kontofilterung nach Abrechnungsadressenregion basierend auf Ihrer Abfrage.</td>
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
      <td>In der Opportunity-Analyse verwendeter Opportunity-Name.</td>
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
      <td>In der Opportunity-Analyse verwendete Opportunity-Beschreibung.</td>
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

Zielgruppen-Fähigkeiten verwenden First-Party-Intent-Daten aus [!DNL Adobe Journey Optimizer B2B Edition]. Die Absichtsberechnung verbindet die Produkttaxonomie mit der Interaktionsaktivität und aggregiert die individuellen Bewertungen auf Kontoebene.

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
      <td>Identifiziert den Ereignistyp. Die Absichtsberechnung verwendet nur <code>directMarketing.emailClicked</code>, <code>directMarketing.emailOpened</code>, <code>directMarketing.emailUnsubscribed</code> und <code>web.webpagedetails.pageViews</code>.
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
      <td>Dient zum Abrufen des E-Mail-Inhalts aus dem [!DNL Adobe Marketo Engage] Rechenzentrum. Sie umfasst (SourceID@SourceInstanceID.SourceType).</td>
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
