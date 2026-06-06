---
title: Konto-Zielgruppenknoten
description: Konfigurieren Sie Konto-Zielgruppenknoten mit Konto-Zielgruppen oder Kontolisten, um Journey-Einstiegspunkte für die zielgerichtete Orchestrierung in Journey Optimizer B2B edition zu definieren.
feature: Account Journeys, Audiences, Account Lists
role: User
exl-id: 288ac5a8-79ed-4654-8ac1-83da2af04f2c
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: beb5f4be-cec3-471a-9db6-831a77dd3ac9id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
subfeature_v2: id: c31bc6c7-76bc-467b-80c0-7315a4e3f6be
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: ff2b9b37-92e0-45fc-b853-379d44c08c89
autotag-review: '2026-04-29T23:21:59.633Z'
source-git-commit: 7cd6c4ecfbbd3a86b4f30d1b4fe6f06655a9c4f5
workflow-type: tm+mt
source-wordcount: 277
ht-degree: 4%

---


# Account Audience Journey Nodes

Der Zielgruppenknoten Konto gibt an, welche Konten in die Journey eintreten. Wenn Sie [Konto-Journey erstellen](./create-publish-journey.md#create-a-journey) beginnt die Journey immer mit einem Konto-Zielgruppenknoten, der die Eingabe definiert.

Verwenden Sie eine der folgenden Eingabeoptionen für diesen Journey-Knoten:

* **[Konto-Zielgruppe](../audiences/account-audience-overview.md)** - Die Konto-Zielgruppe stellt die grundlegende Zielgruppe dar, die mit dem Segmentierungs-Service von Experience Platform synchronisiert wird.
* **[Kontoliste](../accounts/account-lists.md)** - Die Kontoliste ist eine Sammlung benannter Konten, die Sie für die zielgerichtete Journey-Orchestrierung verwenden. Eine Kontenliste zielt auf benannte Konten ab, die definierte Kriterien verwenden, z. B. Branche, Standort oder Unternehmensgröße.

## Festlegen der Zielgruppe für den Konto-Zielgruppenknoten

1. Klicken Sie auf **[!UICONTROL Knoten]** Konto-Zielgruppe“. Diese Aktion zeigt die Knoteneigenschaften im rechten Bedienfeld an.

   ![Konto-Zielgruppen-Journey-Knoten](./assets/account-journey-account-audience-node.png){width="700" zoomable="yes"}

1. Eingabetyp für Konten auswählen, die auf die Journey zugreifen:

   * **[!UICONTROL Konto-Zielgruppe]**

     Wählen Sie die Option Konto-Zielgruppe . Klicken Sie dann auf **[!UICONTROL Konto-Zielgruppe hinzufügen]**.

     Wählen Sie _[!UICONTROL Dialogfeld]_ Zielgruppe hinzufügen“ ein zuvor erstelltes Zielgruppensegment aus. Klicken Sie dann auf **[!UICONTROL Zielgruppe hinzufügen]**.

     ![Wählen Sie ein Zielgruppensegment für den Knoten aus](./assets/node-audience-add-dialog.png){width="700" zoomable="yes"}

   * **[!UICONTROL Kontoliste]**

     Wählen Sie die Option Kontoliste aus. Klicken Sie **[!UICONTROL Kontoliste hinzufügen]**.

     Wählen _[!UICONTROL im Dialogfeld]_ Live-Kontoliste auswählen“ eine veröffentlichte Kontoliste aus. Klicken Sie dann auf **[!UICONTROL Speichern]**.

     ![Live-Kontoliste für den Knoten auswählen](./assets/account-journey-account-audience-select-account-list.png){width="700" zoomable="yes"}

     Weitere Informationen zum Erstellen und Veröffentlichen von Kontolisten finden Sie unter [Kontolisten](../accounts/account-lists.md).

## Erstellen eines Zielgruppensegments

1. Wählen Sie in der linken Navigation **[!UICONTROL Konten]** > **[!UICONTROL Zielgruppen]** aus.

1. Klicken **[!UICONTROL oben]** auf „Zielgruppe erstellen“.

   ![Erstellen eines Zielgruppensegments](./assets/audiences-list-create.png){width="800" zoomable="yes"}

1. Führen Sie die Schritte im [Handbuch zum Segmentierungs-Service](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/types/account-audiences){target="_blank"} aus.
