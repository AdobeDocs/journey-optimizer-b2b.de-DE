---
title: Verwenden von Kontolisten in Journey
description: Verwenden Sie Kontolisten in der Journey-Orchestrierung und fügen Sie Konten in Journey Optimizer B2B Edition dynamisch hinzu bzw. entfernen Sie sie.
feature: Account Lists, Account Journeys
role: User
exl-id: 7cda080d-6263-4ccd-b144-432e4e78c298
autotag-review: 2026-03-27T22:29:03.719Z
TQID: 'https://experienceleague.adobe.com/FokJGxTj7abTN01WCcrVLDEuNLW0oI-i-8z0j-rFBO4'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: e935834c-48b7-43d8-b754-a815196a1b05
    internal-label: Account lists
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
    internal-label: Journeys
subfeature_v2:
  - id: c31bc6c7-76bc-467b-80c0-7315a4e3f6be
    internal-label: Account Journeys
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
    internal-label: Customer journeys
source-git-commit: d713d57bddf2ac6f8cf7e7a7d163281f607d729c
workflow-type: tm+mt
source-wordcount: '914'
ht-degree: 0%
---
# Verwenden von Kontolisten in Journey

Es gibt mehrere Möglichkeiten, Live (veröffentlichte)-Account-Listen in die Account-Journey zu integrieren.

## Konto-Zielgruppenknoten

Alle Account-Journey beginnen mit einem [_Account-Zielgruppe_-Knoten](../journeys/account-audience-nodes.md). Wenn Sie diesen Knoten so einstellen, dass er eine Kontenliste verwendet, durchlaufen die Mitgliederkonten die Journey, sobald sie live (veröffentlicht) geschaltet wird.

1. Wählen Sie die Option **[!UICONTROL Kontoliste]** für den _Kontozielgruppe_ Startknoten aus.

   ![Option „Kontoliste auswählen“ für den Konto-Zielgruppen-Knoten](../journeys/assets/node-audience-account-list.png){width="500"}

1. Klicken Sie **[!UICONTROL Kontoliste hinzufügen]**.

1. Aktivieren Sie das Kontrollkästchen für die Kontoliste und klicken Sie auf **[!UICONTROL Speichern]**.

   ![Option „Kontoliste auswählen“ für den Konto-Zielgruppen-Knoten](../journeys/assets/node-audience-account-list-select-dialog.png){width="600" zoomable="yes"}

## Aktionsknoten ausführen - Zum Konto hinzufügen

**_Nur statische Kontolisten_**

Fügen Sie innerhalb einer Konto-Journey Konten mithilfe eines [einer Aktion _-_ zu einer statischen Kontoliste ](../journeys/action-nodes.md).

Sie haben beispielsweise einen Journey-Pfad, über den Sie eine E-Mail senden, und einige Konten führen als Antwort verschiedene Aktionen aus. Sie betrachten diese Aktivität als Qualifizierungspunkt auf der Journey. Mit der Qualifizierung können Sie sie zu einer Kontenliste hinzufügen, die als Zielgruppe für eine andere Journey mit einem anderen Fluss für qualifizierte Konten verwendet wird.

>[!NOTE]
>
>Wenn sich zum Zeitpunkt der Ausführung des Knotens bereits ein Konto in der Liste befindet, wird die Aktion ignoriert.

1. Wählen Sie die Option _[!UICONTROL Aktion auf]_ **[!UICONTROL Konten]** aus.

1. Wählen Sie _[!UICONTROL Aktion für Konten]_ die Option **[!UICONTROL Zur Kontoliste hinzufügen]** aus.

   ![Wählen Sie Zur Kontoliste hinzufügen aus](../journeys/assets/node-action-account-add-to-account-list.png){width="500"}

1. Wählen **[!UICONTROL unter „Live-]**-Kontoliste auswählen“ die Kontoliste aus, der Sie Konten hinzufügen möchten.

   ![Wählen Sie Zur Kontoliste hinzufügen aus](../journeys/assets/node-action-account-add-to-account-list-select.png){width="500"}

## Aktionsknoten ausführen - Aus Konto entfernen

**_Nur statische Kontolisten_**

Entfernen Sie auf einer Konto-Journey Konten mithilfe des Knotens [Aktion ausführen _aus_ statischen ](../journeys/action-nodes.md).

Sie haben beispielsweise einen Journey-Pfad, über den Sie eine E-Mail senden, und einige Konten führen als Antwort verschiedene Aktionen aus. Sie betrachten diese Aktivität als Qualifizierungspunkt auf der Journey. Mit dieser Qualifizierung möchten Sie sie aus einer Kontoliste entfernen. Diese Liste wird als Audience für eine andere Journey verwendet, die zusätzliche E-Mails sendet, damit Sie Ihre Qualifizierungskommunikationen nicht duplizieren.

>[!NOTE]
>
>Wenn sich ein Konto nicht in der Liste befindet, aus der es entfernt werden soll, wird die Aktion ignoriert.

1. Wählen Sie die Option _[!UICONTROL Aktion auf]_ **[!UICONTROL Konten]** aus.

1. Wählen Sie _[!UICONTROL Aktion für Konten]_ die Option **[!UICONTROL Aus Kontoliste entfernen]** aus.

   ![Wählen Sie Aus Kontenliste entfernen ](../journeys/assets/node-action-account-remove-from-account-list.png){width="500"}

1. Wählen **[!UICONTROL unter „Live-]**-Kontoliste auswählen“ die Kontoliste aus, aus der Sie Konten entfernen möchten.

   ![Wählen Sie Aus Kontenliste entfernen ](../journeys/assets/node-action-account-remove-from-account-list-select.png){width="500"}

## Knoten „Pfade aufteilen“ - Kontomitglied der Kontoliste {#split-paths-account-member-of-account-list}

**_Nur Konto-Journey_**

Verwenden Sie den _[!UICONTROL Kontomitglied der Kontenliste]_ Filter in einem [_Aufspaltungspfade_-Knoten](../journeys/split-merge-paths-nodes.md#add-a-split-path-by-account-node) der nach Konten aufgeteilt wird. Das Konto ist oder ist nicht Mitglied in mindestens einer der ausgewählten Kontolisten. Um Konten in die Listen aufzunehmen, legen Sie die Mitgliedschaft auf `true` fest oder legen Sie sie auf `false` fest, um sie auszuschließen.

Um Konten auf einer Blockierungsliste auszuschließen, fügen Sie den Filter _[!UICONTROL Kontomitglied der]_) hinzu, legen Sie die Mitgliedschaft auf `false` fest und wählen Sie die Liste aus.

1. Navigieren Sie zur Journey-Karte.

1. Klicken Sie auf das Pluszeichen ( **+** ) auf einem Pfad und wählen Sie **[!UICONTROL Pfade aufteilen]**.

1. Wählen Sie in den Knoteneigenschaften auf der rechten Seite **[!UICONTROL Konten]** für die Aufspaltung aus.

1. Um eine Bedingung für _[!UICONTROL Pfad 1) zu definieren]_ klicken Sie auf **[!UICONTROL Bedingung anwenden]**.

1. Definieren Sie den Filter für die Kontoliste.

   * Erweitern Sie im Bedingungseditor den Ordner _[!UICONTROL Spezielle Filter]_ und ziehen Sie den **[!UICONTROL Kontomitglied der Kontenliste]** in den Bedingungsarbeitsbereich.

   * Um Konten in die Listen aufzunehmen, legen Sie die Mitgliedschaft auf `true` fest oder legen Sie sie auf `false` fest, um sie auszuschließen.

   * Eine oder mehrere Kontenlisten auswählen.

   ![Editor für Bedingungen für aufgeteilte Pfade mit Kontomitglied des Kontolistenfilters](./assets/account-lists-journeys-split-path-account-filter.png){width="700" zoomable="yes"}

   Sie können den Filter für die Kontolistenmitgliedschaft mit anderen Kontofiltern kombinieren und auswählen, ob alle Bedingungen oder eine beliebige Bedingung erfüllt werden sollen. Verfeinern Sie Ihre Bedingungen, indem Sie oben **[!UICONTROL die]** Filterlogik“ anwenden.

1. Klicken Sie auf **[!UICONTROL Fertig]**.

Fahren Sie mit der Konfiguration des Knotens „Aufspaltungspfad“ fort, wie in [Aufspaltungspfad nach Kontenknoten hinzufügen“ ](../journeys/split-merge-paths-nodes.md#add-a-split-path-by-account-node).

## Knoten „Pfade aufteilen“ - Person Mitglied der Kontenliste {#split-paths-member-of-account-list}

**_Nur Journey_**

Verwenden Sie die Mitgliedschaftsfilter für die Kontoliste in einem [_Aufspaltungs-Pfade_-Knoten](../journeys/split-merge-paths-nodes.md) einer Personen-Journey, um Personen basierend darauf, ob ihr Konto Mitglied einer Kontoliste ist, weiterzuleiten. Zwei Filter sind verfügbar:

| Filter | Beschreibung |
| ------ | ----------- |
| [!UICONTROL Person Mitglied der dynamischen Kontoliste] | Das Konto der Person ist oder ist nicht Mitglied in einer oder mehreren dynamischen Kontolisten. |
| [!UICONTROL Person Mitglied der statischen Kontoliste] | Das Konto der Person ist oder ist nicht Mitglied in einer oder mehreren statischen Kontolisten. |

Um Personen in auf die Blockierungsliste gesetzt Konten aus einem Pflegepfad auszuschließen, fügen Sie den Filter _[!UICONTROL Person Mitglied der statischen]_ Konto-Liste“ hinzu, legen Sie den Operator auf `is not` fest und wählen Sie die Liste aus.

1. Navigieren Sie zur Journey-Karte.

1. Klicken Sie auf das Pluszeichen ( **+** ) auf einem Pfad und wählen Sie **[!UICONTROL Pfade aufteilen]**.

1. Um eine Bedingung für _[!UICONTROL Pfad 1) zu definieren]_ klicken Sie auf **[!UICONTROL Bedingung anwenden]**.

1. Definieren des Kontolistenfilters

   * Erweitern Sie im Bedingungseditor den Ordner _[!UICONTROL Spezielle Filter]_ und ziehen Sie den Filter **[!UICONTROL Person Mitglied der dynamischen]** Konto oder **[!UICONTROL Person Mitglied der statischen]** Konto in den Arbeitsbereich Bedingungen .

   * Um Personen aufzunehmen, deren Konto in der Liste enthalten ist, legen Sie den Operator auf `is` fest, oder legen Sie ihn auf `is not` fest, um sie auszuschließen.

   * Eine oder mehrere Kontenlisten auswählen.

     ![Editor für Bedingungen für aufgeteilte Pfade mit Personen-Abonnenten von Kontolistenfiltern](./assets/account-lists-journeys-split-path-person-member-account-filter.png){width="700" zoomable="yes"}

   Sie können Filter für die Kontolistenmitgliedschaft mit Filtern für andere Personen kombinieren und festlegen, dass alle Bedingungen oder jede beliebige Bedingung erfüllt werden. Verfeinern Sie Ihre Bedingungen, indem Sie oben **[!UICONTROL die]** Filterlogik“ anwenden.

1. Klicken Sie auf **[!UICONTROL Fertig]**.

Fahren Sie mit der Konfiguration des Knotens „Aufspaltungspfad“ fort, wie in [Aufspaltungspfad nach Personenknoten hinzufügen“ ](../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node).
