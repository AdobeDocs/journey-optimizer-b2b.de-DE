---
title: Personendetails
description: Anzeigen von Personeneinblicken mit KI-generierten Zusammenfassungen, Interaktionswerten, Aktivitäts-Tracking und Absichtserkennung für Kauf-Gruppenmitglieder in Journey Optimizer B2B Edition.
feature: Account Insights
role: User
exl-id: 401d7107-fd20-471e-9adf-a64c590b0080
autotag-review: 2026-03-27T22:21:27.328Z
TQID: 'https://experienceleague.adobe.com/EVVkq83oIwQy2BWI-0z0YA8uBCnvw6Wz2GI7O2c-jE0'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: afadf741-c5fe-42cd-8013-23bb6ff2d1bc
    internal-label: Buying Groups
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
  - id: f979fe0e-02fe-4599-b492-7b3df1d4e7dc
    internal-label: Intelligent Insights
subfeature_v2:
  - id: aa03b4f9-8230-4f55-8705-d4fda6d64f2b
    internal-label: Account insights
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 21fbce544faf291ad01a3301a9981add95442097
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 7%
---
# Personendetails

Wenn Sie an einer beliebigen Stelle in Journey Optimizer B2B Edition auf einen Personennamen klicken, wird die Seite mit den Personendetails angezeigt. Diese Seite enthält nützliche Informationen über die Person, die mit einem Konto oder einer Einkaufsgruppe verknüpft ist, einschließlich einer Zusammenfassung der Highlight- und Intent-Daten zur generativen KI (falls konfiguriert). <!-- There are also [actions](#person-actions) that you can execute for the person. -->

![Seite „Personendetails“](./assets/person-details-page.png){width="800" zoomable="yes"}

Sie können auf diese Seite zugreifen, indem Sie auf einen Namen klicken[ der im Intelligenten Dashboard ](../dashboards/intelligent-dashboard.md), auf [Seite mit den Kaufgruppendetails](../buying-groups/buying-group-details.md) oder auf [Kontodetailseite](./account-details.md).

Die Seite „Personendetails“ besteht aus den folgenden vier Abschnitten:

## Personenübersicht

![Personenübersicht](./assets/details-page-account-overview.png){zoomable="yes"}

Der Abschnitt „Personenübersicht“ oben auf der Seite enthält die folgenden Informationen:

* Name
* Titel
* E-Mail
* Telefonnummer
* Interaktionsbewertung
* Zusammenfassung

## Aktivitäten

In diesem Abschnitt finden Sie eine Liste der letzten E-Mail-, Web-, Formular- und interessanten Momente, die mit der Person verbunden sind (bis zu 20). Die Elemente werden als Aktivitätstyp mit Datum und Uhrzeit aufgelistet.

![Aktivitäten - Personendetails](./assets/person-details-activities.png){width="700" zoomable="yes"}

## Gruppen auf der Basis des Interaktionswerts kaufen

Dieser Abschnitt enthält Einkaufsgruppen, in denen die Person Mitglied ist und nach dem Interaktionswert sortiert ist. Jede Karte enthält die folgenden Informationen zur Einkaufsgruppe:

* Name - Klicken Sie auf den Namen, um die [Einkaufsgruppendetails“ ](../buying-groups/buying-group-details.md) öffnen.
* Interaktionsbewertung
* Vollständigkeitsbewertung
* Phase
* Mitglieder

![Gruppen basierend auf Interaktion kaufen - Personendetails](./assets/person-details-buying-groups-engagement.png){width="700" zoomable="yes"}

## Absichtsdaten

In Journey Optimizer B2B Edition sagt das Modell der Absichtserkennung eine Lösung/ein Produkt von Interesse mit ausreichend hoher Zuverlässigkeit basierend auf der Aktivität einer Person voraus. Außerdem werden die Aktivitäten anderer Account-Co-Mitglieder sowie getaggte Inhalte genutzt. Die Absicht einer Person kann als die Wahrscheinlichkeit interpretiert werden, dass sie Interesse an einem Produkt hat.

{{intent-data-note}}

![Absichtsdaten - Personendetails](./assets/intent-data-panel.png){width="700" zoomable="yes"}

* Absichtsebenen
* Arten von Intent-Signalen - Schlüsselwörter, Produkt und Lösung

<!-- ## Person actions -->
