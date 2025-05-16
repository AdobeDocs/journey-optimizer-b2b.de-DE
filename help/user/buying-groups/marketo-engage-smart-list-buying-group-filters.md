---
title: Kaufen von Gruppenfiltern in Market Engage
description: Erfahren Sie mehr über den Erwerb der Gruppenmitgliedschaft zum Definieren von Filtern in Marketo Engage Smart Lists.
feature: Buying Groups, Integrations
role: User
exl-id: b137e787-808e-4d36-8e8b-a1c7b999f8a2
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 1%

---

# Käufergruppenfilter in Marketo Engage

Als Marketing-Experte können Sie Kampagnen in Marketo Engage für Personen unterdrücken, die Teil von Einkaufsgruppen in Journey Optimizer B2B edition sind. Sie können die Lead-Scoring-Workflows in Marketo Engage auch anhand von Informationen zu den Leads informieren, die mit Einkaufsgruppen verbunden sind. Beispiel:

* Ist dieser Lead Teil einer Einkaufsgruppe?
* Ist die Einkaufsgruppe vollständig und engagiert?

Wenn diese Bedingungen erfüllt sind, können Sie den Lead höher bewerten. Andernfalls können Sie ihn nicht als Marketing-qualifizierten Lead (MQL) markieren.

In Ihrer Marketo Engage-Instanz, die mit Journey Optimizer B2B edition verbunden ist, können Sie den Filter _[!UICONTROL Mitglied der Kaufgruppe]_ in Ihren Smart Lists verwenden, um diese Leads entsprechend Ihrer Kampagnenstrategie zu identifizieren.

1. Nachdem Sie [Smart-Liste in Marketo Engage erstellen](https://experienceleague.adobe.com/de/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/creating-a-smart-list/create-a-smart-list){target="_blank"} wählen Sie die Registerkarte **[!UICONTROL Smart-Liste]** aus, um den Filter-Editor zu öffnen.

1. Scrollen Sie in der Filterliste auf der rechten Seite in der Liste nach unten und erweitern Sie den Ordner **[!UICONTROL Spezielle Filter]**.

1. Klicken Sie auf den **[!UICONTROL Mitglied der Einkaufsgruppe]** und ziehen Sie ihn in den Bereich für die Filterdefinition.

   ![Fügen Sie den Filter Mitglied der Einkaufsgruppe zur Smart List hinzu](./assets/me-member-of-buying-group-filter-add.png){width="700" zoomable="yes"}

1. Setzen Sie die Option _[!UICONTROL Mitglied der Einkaufsgruppe]_ auf **[!UICONTROL true]** oder **[!UICONTROL false]**.

   Diese Einschränkung ist für die Definition erforderlich.

1. (Optional) Fügen Sie dem Filter weitere Einkaufsgruppeneinschränkungen hinzu, je nachdem, wie Sie Leads für die Smart-Liste identifizieren möchten.

   * Klicken **[!UICONTROL oben rechts]** der Filterkarte auf „Beschränkung hinzufügen“.

     ![Andere Einschränkung auswählen](./assets/me-member-of-buying-group-filter-add-constraint.png){width="700" zoomable="yes"}

   * Wählen Sie die Begrenzung aus, die Sie hinzufügen möchten, z. B _„Vollständigkeitswert_ oder _Lösungsinteresse_.

   * Legen Sie die Auswertung fest, die Sie für eine Übereinstimmung verwenden möchten. Für einen Score können Sie eine exakte Übereinstimmung oder einen Bereich oberhalb oder unterhalb der eingegebenen Zahl verwenden.

     Für ein diskretes Element, z. B. die in Journey Optimizer B2B edition definierten Lösungsinteressen, können Sie ein oder mehrere Elemente für die Liste auswählen.

     ![Wählen Sie einen Wert für die Einschränkung aus der Liste aus](./assets/me-member-of-buying-group-filter-constraint-list.png){width="600" zoomable="yes"}

     Wählen Sie die erste Option aus und klicken Sie erneut auf die Auswahl, um das Dialogfeld _[!UICONTROL Auswahl mehrerer Werte]_ zu öffnen.

     ![Wählen Sie mehrere Werte für die Begrenzung aus](./assets/me-member-of-buying-group-filter-constraint-multiple-value.png){width="500" zoomable="yes"}

     Verschieben Sie die verbleibenden Elemente nach rechts und klicken Sie auf **[!UICONTROL OK]**, wenn Sie eine Liste der Elemente haben, die Sie für die Begrenzung verwenden möchten.

   * Wiederholen Sie diese Aktionen, um beliebig viele Einschränkungen hinzuzufügen.

   ![Mitglied des Käufergruppenfilters mit mehreren Einschränkungen](./assets/me-member-of-buying-group-filter-constraints-complete.png){width="600" zoomable="yes"}
