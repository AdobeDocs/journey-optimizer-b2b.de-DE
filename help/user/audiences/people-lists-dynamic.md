---
title: Dynamische Personenlisten
description: Definieren Sie Mitgliedschaftsregeln und duplizieren Sie dynamische Personenlisten in Journey Optimizer B2B Edition.
feature: Audiences
role: User
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: ff2b9b37-92e0-45fc-b853-379d44c08c89
    internal-label: Audience segmentation
source-git-commit: 734966636b6d2addf014905431fa755f6fe92ee6
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 2%
---

# Dynamische Personenlisten

Eine dynamische [Personenliste](./people-lists.md) ist eine Sammlung von Personenprofilen, die durch Regeln (Filter) definiert wird. Die Zugehörigkeit zu einer dynamischen Liste wird mithilfe einfacher Filter definiert, die auf Personenattribute und -aktivitäten verweisen. Die Mitgliedschaft wird automatisch beibehalten, da Profile gemäß der Filterlogik qualifiziert und disqualifiziert werden.

Sie können keine einzelnen Personen zu einer dynamischen Liste hinzufügen oder daraus entfernen. Um die Mitgliedschaft in der Liste zu ändern, aktualisieren Sie die Regeln. Wenn Sie die Mitgliedschaft manuell oder über eine Journey verwalten müssen, verwenden Sie stattdessen eine [statische Liste](./people-lists-static.md).

## Festlegen von Mitgliedschaftsregeln {#set-membership-rules}

>[!NOTE]
>
>Eine dynamische Liste ohne Regeln hat keine Mitglieder. Fügen Sie mindestens einen Filter hinzu, um die Liste zu füllen.

1. Öffnen Sie die dynamische Liste und wählen Sie die Registerkarte **[!UICONTROL Regeln]** aus.

1. Klicken Sie **[!UICONTROL Regeln bearbeiten]**.

   ![Zugriffsregeln zum Erstellen einer dynamischen Personenliste](./assets/people-list-dynamic-rules-edit.png){width="700" zoomable="yes"}

1. Definieren _[!UICONTROL im Dialogfeld „Regeln]_&quot; die Regeln für das Qualifizieren von Profilen, indem Sie Filter aus dem linken Bereich ziehen.

   Profile für die Liste qualifizieren, indem eine beliebige Kombination aus Folgendem verwendet wird:

   * Aktivitätsverlauf
   * [!DNL Experience Platform] Personenfelder
   * Benutzerdefinierte Felder
   * Absichtsdaten
   * Personenattribute
   * Spezielle Filter, z. B. Journey-Mitgliedschaft

   Klicken Sie für jeden hinzugefügten Filter auf **[!UICONTROL Beschränkungen hinzufügen]**, um die entsprechenden Kriterien zu verfeinern. Passen Sie Ihre Bedingungen durch Anwendung der **[!UICONTROL Filterlogik]** oben an. Sie können festlegen, dass alle Bedingungen, alle Bedingungen erfüllt werden, oder eine erweiterte Logik definieren.

   ![Filter mit Einschränkungen hinzufügen, um die dynamische Liste zu füllen](./assets/people-list-dynamic-rules-edit-filter.png){width="700" zoomable="yes"}

1. Klicken Sie **[!UICONTROL Fertig]**, um Ihre Änderungen zu speichern.

   Auf der Registerkarte **[!UICONTROL Regeln]** werden die Filter und die Filterlogik für die Liste angezeigt, und auf der Registerkarte **[!UICONTROL Mitglieder]** wird die aktualisierte Mitgliedschaft aktualisiert. Um die aktuellsten Zielgruppenqualifikationen zu finden, verwenden Sie **[!UICONTROL Mitglieder aktualisieren]** im Menü **[!UICONTROL Mehr]**.

1. Wählen Sie die **[!UICONTROL Mitglieder]** aus.

   Qualifizierende Mitglieder werden nach kurzer Verzögerung in der Liste angezeigt.

   ![Generierte Mitglieder für eine dynamische Personenliste](./assets/people-list-dynamic-members.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Um die Listenregeln jederzeit zu ändern, können Sie diese Schritte wiederholen. Die Mitgliedschaftsliste wird basierend auf den gespeicherten Filtern aktualisiert.

<!--

## Duplicate a dynamic list {#duplicate-dynamic-list}

Duplicating a dynamic list replicates its membership filtering so that you can reuse it in a different context.

1. In the _[!UICONTROL Dynamic lists]_ tab, click the _More menu_ ( **...** ) icon next to the list and choose **[!UICONTROL Duplicate]**.

1. Enter a unique **[!UICONTROL Name]** (required) and a **[!UICONTROL Description]** (optional).

   By default, the dialog appends `_copy` to the name of the originating list. Enter a different unique name as needed.

   ![Duplicate list dialog](./assets/people-list-duplicate-dialog.png){width="375"}

1. Click **[!UICONTROL Duplicate]**.
-->
