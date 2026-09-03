---
title: Verwenden von Kontolisten in Journey
description: Verwenden Sie Kontolisten in der Journey-Orchestrierung und fügen Sie in Journey Optimizer B2B edition Konten dynamisch hinzu bzw. entfernen Sie diese.
feature: Account Lists, Account Journeys
role: User
exl-id: 7cda080d-6263-4ccd-b144-432e4e78c298
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: e935834c-48b7-43d8-b754-a815196a1b05
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
autotag-review: 2026-03-27T22:29:03.719Z
TQID: https://experienceleague.adobe.com/FokJGxTj7abTN01WCcrVLDEuNLW0oI-i-8z0j-rFBO4
source-git-commit: aa6547c60d1b4c570601b5540d193eff57ec6b86
workflow-type: tm+mt
source-wordcount: 417
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

Fügen Sie innerhalb einer Konto-Journey Konten mithilfe eines [einer Aktion _-_ zu einer statischen Kontoliste &#x200B;](../journeys/action-nodes.md).

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

Entfernen Sie auf einer Konto-Journey Konten mithilfe des Knotens [Aktion ausführen _aus_ statischen &#x200B;](../journeys/action-nodes.md).

Sie haben beispielsweise einen Journey-Pfad, über den Sie eine E-Mail senden, und einige Konten führen als Antwort verschiedene Aktionen aus. Sie betrachten diese Aktivität als Qualifizierungspunkt auf der Journey. Mit dieser Qualifizierung möchten Sie sie aus einer Kontoliste entfernen. Diese Liste wird als Audience für eine andere Journey verwendet, die zusätzliche E-Mails sendet, damit Sie Ihre Qualifizierungskommunikationen nicht duplizieren.

>[!NOTE]
>
>Wenn sich ein Konto nicht in der Liste befindet, aus der es entfernt werden soll, wird die Aktion ignoriert.

1. Wählen Sie die Option _[!UICONTROL Aktion auf]_ **[!UICONTROL Konten]** aus.

1. Wählen Sie _[!UICONTROL Aktion für Konten]_ die Option **[!UICONTROL Aus Kontoliste entfernen]** aus.

   ![Wählen Sie Aus Kontenliste entfernen &#x200B;](../journeys/assets/node-action-account-remove-from-account-list.png){width="500"}

1. Wählen **[!UICONTROL unter „Live-]**-Kontoliste auswählen“ die Kontoliste aus, aus der Sie Konten entfernen möchten.

   ![Wählen Sie Aus Kontenliste entfernen &#x200B;](../journeys/assets/node-action-account-remove-from-account-list-select.png){width="500"}
