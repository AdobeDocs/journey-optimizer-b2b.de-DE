---
title: Zielgruppen-Journey-Knoten für Person
description: Platzhalterseite für Personen-Journey.
autotag-review: '2026-06-16T21:21:01.614Z'
TQID: 'https://experienceleague.adobe.com/pk1NGg3M67oRieuCOZFdaguKl2bVkiZyEPVnJDTUBJs'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: ba367494-9862-4596-bd6f-299c7e10a46b
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: b7cb8c2a43b8a562e55923d709f518b8f1d74b2a
workflow-type: tm+mt
source-wordcount: 212
ht-degree: 0%

---

# Zielgruppenknoten Person

Der _Personen-Zielgruppe_-Knoten gibt an, welche Personenprofile in die Journey eintreten. Wenn Sie [Personen-Journey erstellen](./person-journeys.md) beginnt die Journey immer mit einem Personen-Zielgruppenknoten, der die Eingabe definiert. Der Knoten „Zielgruppe“ kann einen von zwei Arten von Zielgruppeneingaben aufweisen: eine statische Personenliste oder eine dynamische Personenliste.

Wenn die Personenliste, die Sie für den Personen-Journey benötigen, nicht bereits vorhanden ist, erstellen [die Personenliste](../audiences/audience-management.md#create-a-people-list) und konfigurieren Sie dann den Zielgruppenknoten Person .

## Festlegen der Zielgruppe für den Zielgruppenknoten „Person“

1. Klicken Sie auf **[!UICONTROL Knoten]** Zielgruppe“.

   Diese Aktion zeigt die Knoteneigenschaften rechts an.

   <!-- ![Person audience journey node](./assets/person-journey-person-audience-node.png){width="700" zoomable="yes"} -->

1. Verwenden Sie im Bedienfeld Knoteneigenschaften auf der rechten Seite eine der folgenden Eingabeoptionen für den Knoten „Zielgruppen-Journey für Personen“:

   * **[!UICONTROL Dynamische Liste]** - Verwenden Sie eine dynamische, regelbasierte Personenliste. Die Listenregeln werden zur Journey-Laufzeit ausgewertet, um Mitglieder der Journey zu qualifizieren. Personen, die sich zu einem späteren Zeitpunkt für die dynamische Liste disqualifizieren, werden nicht von der Journey entfernt.

   * **[!UICONTROL Statische Liste]** - Verwenden Sie eine statische Liste von Personen als Mitglied Ihres Journey. Die aktuelle Listenmitgliedschaft wird zur Journey-Laufzeit ausgewertet, um Mitglieder für die Journey zu qualifizieren. Personen, die später aus der statischen Liste entfernt werden, werden nicht von der Journey entfernt.

