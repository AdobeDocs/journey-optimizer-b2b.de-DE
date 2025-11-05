---
title: Vollständigkeits-Scores für Einkaufsgruppen
description: Berechnen Sie die Vollständigkeit der Einkaufsgruppe mithilfe von rollenbasierten Schwellenwerten, anpassbaren Mitgliedsanforderungen und Vollständigkeitseinstellungen in Journey Optimizer B2B edition.
feature: Buying Groups
role: User
source-git-commit: 1ebc27a709e1b82029c22950897505f3945a507f
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 4%

---


# Vollständigkeitswerte {#completeness-scores}

>[!CONTEXTUALHELP]
>id="ajo-b2b_buying_group_completeness_score"
>title="Vollständigkeitsbewertung"
>abstract="Die Vollständigkeitswerte spiegeln wider, wie gut die Mitgliedschaft in der Einkaufsgruppe für eine verkaufsbereite Einkaufsgruppe abgestimmt ist."

Ein Vollständigkeitswert ist ein Prozentsatz, der angibt, wie gut eine Einkaufsgruppe mit den erforderlichen Mitgliedern in ihren definierten Rollen gefüllt ist. Diese Bewertungen basieren auf den Schwellenwerten für Rollenmitglieder, die Sie in der Rollenvorlage konfigurieren, und der tatsächlichen Anzahl der Mitglieder, die jeder Rolle in der Einkaufsgruppe zugewiesen wurden. Die resultierenden Bewertungen helfen Marketing-Experten, die Verkaufsbereitschaft zu bewerten und Lücken in der Zusammensetzung der Einkaufsgruppe zu identifizieren. Die Score-Berechnung erfolgt automatisch, wenn sich die Kauf-Gruppenmitgliedschaft ändert.

![Vollständigkeitswerte für die Einkaufsgruppe](./assets/buying-group-details-page-completeness-scores.png){width="800" zoomable="yes"}

Es gibt zwei Arten von Vollständigkeitsbewertungen:

* **Bewertung der Vollständigkeit der Einkaufsgruppe** - Der Wert für die Vollständigkeit der Einkaufsgruppe entspricht einem Prozentsatz zwischen 0 % und 100 % und stellt die Gesamtvollständigkeit der Einkaufsgruppe auf der Grundlage von Berechnungen der Vollständigkeit auf Rollenebene dar.

  Der Vollständigkeitswert für die Einkaufsgruppe wird auf der Seite [Einkaufsgruppendetails](./buying-group-details.md) angezeigt. Diese Punktzahl bietet einen Überblick darüber, ob die Einkaufsgruppe über die erforderlichen Stakeholder für Vertriebsaktivitäten verfügt.

* **Funktions-Vollständigkeitsbewertung** - Der Funktions-Vollständigkeitswert ist ein Prozentsatz für jede einzelne Funktion innerhalb einer Einkaufsgruppe, basierend auf der Anzahl der dieser Funktion zugewiesenen Mitglieder.

  Die Rollenvollständigkeitsbewertung für jede Rolle wird auf der Detailseite für Einkaufsgruppen angezeigt, wenn Sie Rollen bearbeiten und die Vollständigkeitseinstellungen anpassen. Anhand dieser Bewertungen können Sie ermitteln, welche Rollen zusätzliche Mitglieder benötigen, um den Schwellenwert für verkaufsbereite Produkte zu erreichen.

  Auf der Detailseite werden die ersten beiden Rollenvollständigkeitsbewertungen mit einem n_+-Link für alle zusätzlichen Rollen angezeigt. Klicken Sie auf den Link, um die zusätzlichen Rollenvollständigkeitswerte anzuzeigen.

Die Vollständigkeitswerte spiegeln den aktuellen Status der kaufenden Gruppenmitgliedschaft wider und werden automatisch aktualisiert, wenn Mitglieder hinzugefügt oder entfernt werden. Die angezeigten Werte werden als ganze Prozentsätze angezeigt (z. B. wird ein Wert von 66,67 % als 67 % angezeigt).

## Bewerten der Verkaufsbereitschaft

Adobe Journey Optimizer B2B edition bietet Marketing-Experten Tools, mit denen sichergestellt wird, dass Einkaufsgruppen mit echten Entscheidungsprozessen übereinstimmen. Sie können vollständige Einkaufsgruppen mithilfe anpassbarer Schwellenwerte für Mitglieder der Funktion definieren, die die Vertriebsmethode Ihres Unternehmens widerspiegeln. Indem Sie für jede Rolle Mindest- und Höchstmitgliedsanforderungen festlegen, legen Sie klare Kriterien dafür fest, was eine verkaufsbereite Einkaufsgruppe darstellt.

Die Bewertung der Vollständigkeit der Einkaufsgruppe liefert ein genaues Maß für die Verkaufsbereitschaft der Gruppe. Um beispielsweise eine Gelegenheit für eine bestimmte Lösung zu erhalten, benötigen Sie möglicherweise mindestens zwei Entscheidungsträger, einen Influencer und mindestens einen Anwender. Die Berechnung des Vollständigkeitswerts berücksichtigt jede dieser rollenspezifischen Anforderungen und bietet einen Überblick über die Bereitschaft der gesamten Einkaufsgruppe.

## Journey-Effektivität messen

Die Vollständigkeit der Einkaufsgruppe dient als wichtiger Leistungsindikator (KPI) für die Journey-Effektivität. Das Ziel einer bestimmten Journey kann darin bestehen, die Vollständigkeit der Einkaufsgruppe um einen bestimmten Prozentsatz zu erhöhen oder einen Mindestschwellenwert zu erreichen, bevor verkaufsfertige Warnhinweise ausgelöst werden.

In einem großen Unternehmen können Sie möglicherweise eine Person pro Rolle identifizieren. Möglicherweise ist diese Person jedoch nicht der richtige Ansprechpartner für den Verkauf, oder Sie benötigen mehrere Ansprechpartner in kritischen Rollen. Beispielsweise kann ein großes Unternehmen über mehrere IT-Entscheidungsträger verfügen, die über Abteilungen oder Geschäftsbereiche verteilt sind. Die Identifizierung eines Entscheidungsträgers reicht für einen komplexen Unternehmensumsatz möglicherweise nicht aus.

Nachdem Sie die Vollständigkeit der aktuellen Einkaufsgruppe analysiert haben, können Sie die erforderliche Anzahl von Kontakten für jede Rolle in der Rollenvorlage anpassen. Mit diesen Anpassungen können Sie Ihre Einkaufsgruppenstrategie auf der Grundlage von realen Mustern und Verkaufsergebnissen anpassen.

<!-- ## Analyze audiences for journey optimization

Marketers can view the starting buying group completeness score of target account audiences to find the best performance indicators for a solution. This visibility enables marketers to:

* Determine if they need to adjust the completeness score requirements for each role to make journeys more effective.
* Identify which buying groups are closest to sales-ready status and prioritize them for acceleration campaigns.
* Segment buying groups by completeness score ranges and create tailored nurture strategies for different maturity levels.

>[!BEGINSHADEBOX]

The buying group completeness score is available to use for filtering in [journey split-path-by-account nodes](../journeys/split-merge-paths-nodes.md#account-path-filters) and for audience segmentation. Role completeness can be used to create personalized content that addresses specific gaps in buying group composition.

>[!ENDSHADEBOX] -->

## Berechnung der Rollenvollständigkeit {#role-completeness-calculation}

>[!CONTEXTUALHELP]
>id="ajo-b2b_buying_group_role_completeness_calculation"
>title="Berechnung der Rollenvollständigkeit"
>abstract="Die Rollenvollständigkeitswerte werden als Prozentsatz basierend auf der Anzahl der Mitglieder berechnet, die einer Rolle zugewiesen wurden."

Journey Optimizer B2B edition berechnet den Vollständigkeitswert für jede einzelne Einkaufsgruppenrolle als Prozentsatz. Stützen Sie diese Bewertung auf die Anzahl der Mitglieder, die der Rolle zugewiesen sind, im Vergleich zu [der in der Rollenvorlage erforderlichen Anzahl](./buying-groups-role-templates.md#change-the-completeness-score-settings) für die Fertigstellung.

Die Berechnung der Rollenvollständigkeit ist ein linearer Prozentsatz zwischen null und dem angegebenen Schwellenwert (Mitglieder erforderlich):

* Wenn die Anzahl der zugewiesenen Mitglieder &quot;**&quot;**, ist die Vollständigkeit der Rolle **0%**.
* Wenn die Anzahl der zugewiesenen Mitglieder **am oder über dem Schwellenwert** liegt, beträgt die Vollständigkeit der Rolle **100%**.
* Liegt die Anzahl der zugewiesenen Mitglieder **zwischen einem und dem Schwellenwert** wird die Vollständigkeit proportional berechnet.

### Formel zur Rollenvollständigkeit

Der Prozentwert der Rollenvollständigkeit wird anhand der folgenden Formel berechnet:

```text
Role Completeness % = ((Assigned Members - Threshold) / (Threshold)) × 100
```

Dabei gilt:

* `Assigned Members` = Aktuelle Anzahl der Mitglieder in der Funktion
* `Threshold` = Erforderlicher Wert für Mitglieder in der Rollenvorlage festgelegt

### Beispiele für die Rollenvollständigkeit

Die folgenden Beispiele veranschaulichen Rollenvollständigkeitsberechnungen mit verschiedenen Schwellenwertkonfigurationen:

| Rolle | Mitglieder erforderlich | Zugewiesene Mitglieder | Berechnung | Vollständigkeit der Rolle |
|------|------------------|------------------|-------------|-------------------|
| Entscheidungsträger | 3 | 0 | Keine | 0 % |
|  |  | 1 | 1/3 × 100 | 33 % |
|  |  | 2 | 2/3 × 100 | 66 Prozent |
|  |  | 3 | Bei Schwellenwert | 100 % |
|  |  | 4 | Über Schwellenwert | 100 % |
| Influencer | 5 | 0 | Keine | 0 % |
|  |   | 1 | 1/5 × 100 | 20 % |
|  |   | 2 | 2/5 × 100 | 40 % |
|  |   | 3 | 3/5 × 100 | 60 % |
|  |   | 4 | 4/5 × 100 | 80 % |
|  |   | 5 | Bei Schwellenwert | 100 % |
|  |   | 6 | Über Schwellenwert | 100 % |

## Berechnung der Vollständigkeit der Einkaufsgruppe {#buying-group-completeness-calculation}

Der Vollständigkeitswert für die Einkaufsgruppe aggregiert die individuellen Rollenvollständigkeitswerte. Diese Berechnung bietet eine ganzheitliche Sicht der Bereitschaft für eine Einkaufsgruppe für alle definierten Rollen.

### Vollständigkeitsformel für die Einkaufsgruppe

Der Prozentsatz der Vollständigkeit der Einkaufsgruppe wird anhand der folgenden Formel berechnet:

```text
Buying Group Completeness % = Σ(Role Completeness %) / Number of defined roles
```

Dabei gilt:

* `Role Completeness %` = Prozentsatz der Vollständigkeit der einzelnen Rollen (0-100 %)
* `Σ` = Summe aller Funktionen in der Einkaufsgruppe

<!--

## Use completeness scores in journeys

Use buying group completeness scores and role-level completeness scores to optimize your account journeys and personalize engagement strategies.

### Split paths by completeness

Use completeness thresholds in [journey split-path-by-account nodes](../journeys/split-merge-paths-nodes.md#account-path-filters) to route buying groups through different journey paths based on their readiness. For example:

* **High completeness path** (≥70%) - Buying groups that are nearly sales-ready can be routed to sales teams or receive call-to-action campaigns
* **Medium completeness path** (40-69%) - Buying groups in active development receive nurture campaigns focused on filling specific role gaps
* **Low completeness path** (<40%) - Newly formed buying groups receive awareness and education content to build initial engagement

### Trigger actions based on completeness milestones

Set up journey events that trigger specific actions when buying groups reach completeness milestones. FOr example:

* Alert sales teams when a buying group reaches 70% completeness.
* Send a _stakeholder alignment_ campaign when completeness increases by 20% or more within a defined timeframe.
* Trigger an automated assessment when a buying group stalls at the same completeness level for an extended period.

By leveraging completeness scores throughout the journey, you create more targeted, efficient campaigns that align with the actual composition and maturity of your buying groups.

-->