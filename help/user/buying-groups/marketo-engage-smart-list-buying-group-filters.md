---
title: Kaufen von Gruppenfiltern in Marketo Engage
description: Filtern Sie Leads, indem Sie Gruppenmitgliedschaften in Marketo Engage Smart Lists mit Einschränkungen wie Vollständigkeitsbewertung erwerben, um Kampagnen zu optimieren und die Lead-Bewertung zu optimieren.
feature: Buying Groups, Integrations
role: User
exl-id: b137e787-808e-4d36-8e8b-a1c7b999f8a2
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
  - id: b27e5950-9033-45ac-9f86-eb22e567f615
feature_v2:
  - id: afadf741-c5fe-42cd-8013-23bb6ff2d1bc
  - id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
autotag-review: 2026-03-30T21:39:24.495Z
TQID: https://experienceleague.adobe.com/HGixvYgQPYt-yMoavl8qFwpujaAW5Ejh1Yb1-Pkc8Z8
source-git-commit: 9baf03a1ddc1733385b0398ffadde8f548c431cc
workflow-type: tm+mt
source-wordcount: 562
ht-degree: 1%

---

# Käufergruppenfilter in Marketo Engage

>[!IMPORTANT]
>
>**Einstellung von Funktionen**</br></br>
>
>In Journey Optimizer B2B edition sind die Einkaufsgruppenfilter nicht mehr in einer verbundenen Marketo Engage-Instanz verfügbar.</br></br>
>
>Alternativ können Sie für jede gewünschte Lösung eine statische Liste erstellen und dann [die Aktion _Zu Marketo-Liste hinzufügen_ von einem Journey-](../journeys/action-nodes.md#marketo-engage-actions) aus verwenden. Durch diese Aktion werden kaufende Gruppenmitglieder zu einer bestimmten statischen Liste in einer verbundenen Marketo Engage-Instanz hinzugefügt. Verwenden Sie dann die lösungsorientierte statische Liste für einen Smart-Listen-Filter.

Als Marketing-Experte können Sie Kampagnen in Marketo Engage für Personen unterdrücken, die Teil von Einkaufsgruppen in Journey Optimizer B2B edition sind. Sie können die Lead-Scoring-Workflows in Marketo Engage auch anhand von Informationen zu den Leads informieren, die mit Einkaufsgruppen verbunden sind. Beispiel:

* Ist dieser Lead Teil einer Einkaufsgruppe?
* Ist die Einkaufsgruppe vollständig und engagiert?

Wenn diese Bedingungen erfüllt sind, können Sie den Lead mit dem höheren Wert bewerten. Andernfalls können Sie ihn nicht als Marketing-qualifizierten Lead (MQL) markieren.

In Ihrer Marketo Engage-Instanz, die mit Journey Optimizer B2B edition verbunden ist, können Sie den Filter _[!UICONTROL Mitglied der Kaufgruppe]_ in Ihren Smart Lists verwenden, um diese Leads entsprechend Ihrer Kampagnenstrategie zu identifizieren.

1. Nachdem Sie [Smart-Liste in Marketo Engage erstellen](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/creating-a-smart-list/create-a-smart-list){target="_blank"} wählen Sie die Registerkarte **[!UICONTROL Smart-Liste]** aus, um den Filter-Editor zu öffnen.

1. Scrollen Sie in der Filterliste auf der rechten Seite in der Liste nach unten und erweitern Sie den Ordner **[!UICONTROL Spezielle Filter]**.

1. Klicken Sie auf den **[!UICONTROL Mitglied der Einkaufsgruppe]** und ziehen Sie ihn in den Bereich für die Filterdefinition.

   ![Fügen Sie den Filter Mitglied der Einkaufsgruppe zur Smart List hinzu](./assets/me-member-of-buying-group-filter-add.png){width="700" zoomable="yes"}

1. Setzen Sie die Option _[!UICONTROL Mitglied der Einkaufsgruppe]_ auf **[!UICONTROL true]** oder **[!UICONTROL false]**.

   Diese Einschränkung ist für die Definition erforderlich.

1. (Optional) Fügen Sie dem Filter weitere Einkaufsgruppeneinschränkungen hinzu, je nachdem, wie Sie Leads für die Smart-Liste identifizieren möchten.

   * Klicken **[!UICONTROL oben rechts]** der Filterkarte auf „Beschränkung hinzufügen“.

     ![Andere Einschränkung auswählen](./assets/me-member-of-buying-group-filter-add-constraint.png){width="700" zoomable="yes"}

   * Wählen Sie die Begrenzung aus, die Sie hinzufügen möchten, z. B _„Vollständigkeitswert_ oder _Lösungsinteresse_.

   * Legen Sie die Auswertung fest, die Sie für eine Übereinstimmung verwenden möchten.

     Für einen Score können Sie eine exakte Übereinstimmung oder einen Bereich oberhalb oder unterhalb der eingegebenen Zahl verwenden.

     Um Mitglieder auszuschließen, die aus einer Einkaufsgruppe entfernt wurden, verwenden Sie die Beschränkung _[!UICONTROL Ist entfernt]_, die auf `false` gesetzt ist. Sie können entfernte Mitglieder auch explizit in die Smart-Liste einbeziehen, indem Sie diese Einschränkung auf `true` festlegen.

     Für ein diskretes Element, z. B. die in Journey Optimizer B2B edition definierten Lösungsinteressen, können Sie ein oder mehrere Elemente für die Liste auswählen.

     ![Wählen Sie einen Wert für die Einschränkung aus der Liste aus](./assets/me-member-of-buying-group-filter-constraint-list.png){width="600" zoomable="yes"}

     Wählen Sie die erste Option aus und klicken Sie erneut auf die Auswahl, um das Dialogfeld _[!UICONTROL Auswahl mehrerer Werte]_ zu öffnen.

     ![Wählen Sie mehrere Werte für die Begrenzung aus](./assets/me-member-of-buying-group-filter-constraint-multiple-value.png){width="500" zoomable="yes"}

     Verschieben Sie die verbleibenden Elemente nach rechts und klicken Sie auf **[!UICONTROL OK]**, wenn Sie eine Liste der Elemente haben, die Sie für die Begrenzung verwenden möchten.

   * Wiederholen Sie diese Aktionen, um beliebig viele Einschränkungen hinzuzufügen.

   ![Mitglied des Käufergruppenfilters mit mehreren Einschränkungen](./assets/me-member-of-buying-group-filter-constraints-complete.png){width="600" zoomable="yes"}
