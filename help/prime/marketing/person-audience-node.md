---
title: Zielgruppen-Journey-Knoten für Person
description: Konfigurieren Sie den Zielgruppenknoten Person in Journey Optimizer B2B, um mithilfe von dynamischen Personenlisten oder ereignisbasierten Zielgruppen anzugeben, welche Profile auf eine Journey zugreifen.
badgeBeta: label="Beta" type="informative" tooltip="Diese Funktion befindet sich derzeit in einer eingeschränkten Beta-Version"
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
source-git-commit: 6227b7f64baf307e3778e73bcceabb140ab65fb8
workflow-type: tm+mt
source-wordcount: 225
ht-degree: 4%

---

# Zielgruppenknoten Person

Der _Personen-Zielgruppe_-Knoten gibt an, welche Personenprofile in die Journey eintreten. Wenn Sie [Personen-Journey erstellen](./person-journeys.md) beginnt die Journey immer mit einem Personen-Zielgruppenknoten, der die Eingabe definiert. Der Zielgruppenknoten Person kann einen von zwei Zielgruppen-Eingabetypen aufweisen: eine Liste dynamischer Personen oder einen Ereignis-Trigger.

Wenn die dynamische Personenliste, die Sie für den Personen-Journey benötigen, nicht bereits vorhanden ist, erstellen [&#x200B; die Personenliste &#x200B;](../audiences/people-lists.md#create-a-people-list) konfigurieren Sie dann den Zielgruppenknoten Person .

_So konfigurieren Sie die Journey-Zielgruppe :_

1. Klicken Sie auf **[!UICONTROL Knoten]** Zielgruppe“.

   Diese Aktion zeigt die Knoteneigenschaften rechts an.

   ![Zielgruppen-Journey-Knoten für Person](./assets/person-audience-node-properties.png){width="500" zoomable="yes"}

1. Verwenden Sie eine der folgenden Zielgruppen-Konfigurationsoptionen für die Zielgruppe der Person:

   * **[!UICONTROL Dynamische Liste]** - Verwenden Sie eine dynamische, regelbasierte Personenliste. Die Listenregeln werden zur Journey-Laufzeit ausgewertet, um Mitglieder der Journey zu qualifizieren. Personen, die sich zu einem späteren Zeitpunkt für die dynamische Liste disqualifizieren, werden nicht von der Journey entfernt. Siehe _[Dynamische](../audiences/people-lists.md#dynamic-lists)_.

   * **[!UICONTROL Ereigniszielgruppe]** - Verwenden Sie eine Ereigniszielgruppe, um die Journey-Zielgruppe basierend auf qualifizierten Ereignissen zu definieren. Definieren Sie Zielgruppenmitglieder mithilfe der Personenprofilfilterung und des Trigger-Journey-Eintrags mithilfe von Ereigniskriterien. Siehe _[Ereignisbasierte Zielgruppen](../audiences/event-based-audiences.md)_.
