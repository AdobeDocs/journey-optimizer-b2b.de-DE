---
title: Personenlisten in Journey verwenden
description: Verwenden Sie Personenlisten, um Personen dynamisch hinzuzufügen oder zu entfernen und Journey-Pfade nach Listenmitgliedschaft in Journey Optimizer B2B Edition aufzuteilen.
feature: Audiences, Person Journeys, Account Journeys
role: User
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
    internal-label: Journeys
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
    internal-label: Customer journeys
source-git-commit: d713d57bddf2ac6f8cf7e7a7d163281f607d729c
workflow-type: tm+mt
source-wordcount: '829'
ht-degree: 0%
---

# Personenlisten in Journey verwenden

Es gibt mehrere Möglichkeiten, „Personenlisten[ in Ihre Account-Journey](./people-lists.md) und Personen-Journey zu integrieren:

* **Beibehalten einer statischen Liste von einer Journey** - Verwenden Sie in einem _Aktion durchführen_-Knoten die _[!UICONTROL Zu Personenliste hinzufügen]_ oder _[!UICONTROL Aus Personenliste entfernen]_, um die Mitgliedschaft in einer statischen Personenliste zu aktualisieren, wenn Personen die Journey durchlaufen.
* **Personen basierend auf Listenmitgliedschaft routen** - Verwenden Sie im Knoten _Pfade aufteilen_ den Filter _[!UICONTROL Personenmitglied der statischen Personenliste]_ oder _[!UICONTROL Personenmitglied der dynamischen Personenliste]_, um einen Pfad für Personen zu erstellen, die Mitglieder einer Liste sind (oder nicht).

Sie können beispielsweise eine Ausschlussliste mit Team-Mitgliedern und Partnern erstellen und diese Liste verwenden, um diese Personen von einem Pflegepfad auszuschließen. Alternativ können Sie Personen zu einer statischen Liste hinzufügen, wenn sie einen Qualifizierungspunkt auf einer Journey erreichen, und diese Liste dann verwenden, um Personen auf einer anderen Journey zu verzweigen.

## Aktionsknoten ausführen - Zu Personenliste hinzufügen {#add-to-people-list}

**_Nur statische Personenlisten_**

Fügen Sie innerhalb eines Accounts oder einer Personen-Journey Personen mithilfe des Knotens [Aktion ausführen _zu_ Personenliste ](../journeys/action-nodes.md#people-actions).

Betrachten Sie beispielsweise einen Journey-Pfad, über den Sie eine E-Mail senden und sich einige Personen für ein Webinar registrieren. Sie betrachten diese Antwort als Qualifizierungspunkt auf der Journey. Nach der Qualifizierung sollten Sie diese Personen zu einer statischen Personenliste hinzufügen, die eine andere Journey verwendet, um qualifizierte Personen in einen anderen Pfad aufzuteilen.

>[!NOTE]
>
>Wenn sich eine Person bereits in der Liste befindet, wenn der Knoten ausgeführt wird, wird die Aktion ignoriert.

1. Navigieren Sie zur Journey-Karte.

1. Klicken Sie auf das Pluszeichen ( **+** ) auf einem Pfad und wählen Sie **[!UICONTROL Aktion ausführen]**.

1. (Nur Konto-Journey _[!UICONTROL Wählen Sie die Option Aktion für]_ **[!UICONTROL Personen]** aus.

1. Wählen Sie _[!UICONTROL Aktion für Personen]_ die Option **[!UICONTROL Zu Personenliste hinzufügen]**.

1. Wählen **[!UICONTROL unter „Statische Personenliste]**&quot; die Personenliste aus, der Sie Personen hinzufügen möchten.

   ![Wählen Sie Zu Personenliste hinzufügen aus](../journeys/assets/node-action-add-to-people-list.png){width="300"}

## Aktionsknoten ausführen - Aus Personenliste entfernen {#remove-from-people-list}

**_Nur statische Personenlisten_**

Entfernen Sie in einem Konto oder einer Personen-Journey Personen mithilfe des Knotens [Aktion ausführen _aus_ Liste ](../journeys/action-nodes.md#people-actions).

Wenn eine Person beispielsweise konvertiert hat, möchten Sie sie aus einer statischen Liste entfernen. Diese Liste wird verwendet, um Personen auf einen Pflegepfad zu leiten, damit sie keine Pflegekommunikation mehr erhalten.

>[!NOTE]
>
>Wenn sich eine Person nicht in der Liste befindet, aus der sie entfernt werden soll, wird die Aktion ignoriert.

1. Navigieren Sie zur Journey-Karte.

1. Klicken Sie auf das Pluszeichen ( **+** ) auf einem Pfad und wählen Sie **[!UICONTROL Aktion ausführen]**.

1. (Nur Konto-Journey _[!UICONTROL Wählen Sie die Option Aktion für]_ **[!UICONTROL Personen]** aus.

1. Wählen Sie _[!UICONTROL Aktion für Personen]_ die Option **[!UICONTROL Aus Benutzerliste entfernen]**.

1. Wählen **[!UICONTROL unter „Statische Personenliste]**&quot; die Personenliste aus, aus der Sie Personen entfernen möchten.

   ![Wählen Sie „Aus Personenliste entfernen“](../journeys/assets/node-action-remove-from-people-list.png){width="300"}

## Knoten „Pfade aufteilen“ - Liste „Mitglied von Personen“ {#split-paths-by-list-membership}

**_Konto- und Personen-Journey_**

Verwenden Sie die Mitgliedschaftsfilter der Personenliste in einem [_Aufspaltungspfade_-Knoten](../journeys/split-merge-paths-nodes.md) um Personen auf Grundlage dessen, ob sie Mitglieder einer Personenliste sind, weiterzuleiten. Zwei Filter sind verfügbar:

| Filter | Beschreibung |
| ------ | ----------- |
| [!UICONTROL Person Mitglied der dynamischen Liste „Personen“] | Die Person ist oder ist nicht Mitglied in einer oder mehreren dynamischen Personenlisten. Die Mitgliedschaft spiegelt die aktuellen Regeln der Liste wider. |
| [!UICONTROL Person Mitglied der statischen Personenliste] | Die Person ist oder ist nicht Mitglied in einer oder mehreren statischen Personenlisten. |

Diese Filter sind in beiden Journey-Typen verfügbar:

* **Personen-Journey** - In einem _Aufspaltungs-Pfaden_-Knoten.
* **Account-Journey** - In einem _Split-Pfade_-Knoten, der nach &quot;_[!UICONTROL &quot;]_.

Um Team-Mitglieder und Partner aus einem Pflegepfad auszuschließen, fügen Sie den Filter _[!UICONTROL Person Mitglied der statischen Personenliste]_ hinzu, legen Sie den Operator auf `is not` fest und wählen Sie die Liste aus.

1. Navigieren Sie zur Journey-Karte.

1. Klicken Sie auf das Pluszeichen ( **+** ) auf einem Pfad und wählen Sie **[!UICONTROL Pfade aufteilen]**.

   ![Journey-Knoten hinzufügen - Aufspaltungspfade](../journeys/assets/add-node-split.png){width="300" zoomable="no"}

1. (Nur Konto-Journey) Legen Sie den Knoten für die Bedingungen für Personen fest.

   * Wählen Sie in den Knoteneigenschaften auf der rechten Seite **[!UICONTROL Personen]** für die Teilung aus.

   * Legen Sie **[!UICONTROL Attribute, die für Bedingungen verwendet werden]** auf **[!UICONTROL Nur Personenattribute]** fest.

   ![Account Journey - Split Path Node - Personenattribute](../journeys/assets/node-split-path-account-journey-people-attributes.png){width="300" zoomable="no"}

1. Um eine Bedingung für _[!UICONTROL Pfad 1) zu definieren]_ klicken Sie auf **[!UICONTROL Bedingung anwenden]**.

1. Erweitern Sie im Bedingungseditor den Ordner _[!UICONTROL Spezielle Filter]_ und ziehen Sie den Filter **[!UICONTROL Person Mitglied der dynamischen]** Personen oder **[!UICONTROL Person Mitglied der statischen]** auf den Arbeitsbereich Bedingungen .

   ![Editor für Bedingungen für aufgeteilte Pfade mit Personen-Listenfiltern für Mitglieder](../accounts/assets/account-lists-person-journeys-split-path-filter.png){width="700" zoomable="yes"}

1. Um Listenmitglieder einzuschließen, setzen Sie die Mitgliedschaft auf `is`.

   Um sie auszuschließen, legen Sie `is not` fest.

1. Wählen Sie die auszuwertende Personenliste aus.

   Geben Sie Text in das Feld ein, um die verfügbaren Listen zu filtern. Es stehen nur benutzerdefinierte Personenlisten zur Auswahl.

1. Verfeinern Sie Ihre Bedingungen, indem Sie oben **[!UICONTROL die]** Filterlogik“ anwenden.

   Sie können Filter für die Listenmitgliedschaft mit Filtern für andere Personen kombinieren und auswählen, ob alle Bedingungen oder eine beliebige Bedingung erfüllt werden sollen.

1. Klicken Sie auf **[!UICONTROL Fertig]**.

Fahren Sie mit der Konfiguration des Knotens „Aufspaltungspfade“ fort, wie in [_Hinzufügen eines Aufspaltungspfads nach Personenknoten_](../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node) beschrieben. Weitere Informationen zu Mitgliedschaftsfiltern finden Sie unter [_Mitgliedschaftsfilter_](../journeys/split-merge-paths-nodes.md#membership-filtering).
