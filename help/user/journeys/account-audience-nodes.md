---
title: Konto-Zielgruppenknoten
description: Erfahren Sie mehr über den Knotentyp Konto-Zielgruppe , den Sie zum Definieren der Eingabe für die Journey Ihres Kontos in Journey Optimizer B2B edition verwenden können.
feature: Account Journeys
exl-id: 288ac5a8-79ed-4654-8ac1-83da2af04f2c
source-git-commit: 5ed7e58b7a069c8b436d0d2f7b338072259768be
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 5%

---

# Account Audience Journey Nodes

Der Zielgruppenknoten Konto definiert die Eingabekonten für die Journey. Wenn Sie [Konto-Journey erstellen](./journey-overview.md#create-an-account-journey) beginnt diese immer mit einem _Konto-Zielgruppe_-Knoten, der die Eingabe für die Journey definiert.

Es gibt zwei Arten von Eingaben, die Sie für diesen Knoten verwenden können:

* **[Konto-Zielgruppe](../audiences/account-audience-overview.md)** - Dies ist die grundlegende Zielgruppe, die mit dem Experience Platform-Segmentierungs-Service synchronisiert wird.
* **[Kontoliste](../accounts/account-lists.md)** - Dies ist eine Sammlung benannter Konten, die Sie für die zielgerichtete Journey-Orchestrierung verwenden können. Eine Kontenliste zielt auf benannte Konten nach den definierten Kriterien ab, z. B. Branche, Standort oder Größe des Unternehmens.

_So legen Sie die Zielgruppe für den Knoten fest:_

1. Klicken Sie auf **[!UICONTROL Knoten]** Konto-Zielgruppe), um die Knoteneigenschaften auf der rechten Seite anzuzeigen.

   ![Konto-Zielgruppenknoten](./assets/account-journey-account-audience-node.png){width="700" zoomable="yes"}

1. Wählen Sie den Eingabetyp für die Konten, die in die Journey eingehen sollen:

   * **[!UICONTROL Konto-Zielgruppe]**

     Wählen Sie diesen Typ aus und klicken Sie dann auf **[!UICONTROL Konto-Zielgruppe hinzufügen]**.

     Wählen _[!UICONTROL Dialogfeld „Zielgruppe hinzufügen]_ ein zuvor erstelltes Zielgruppensegment aus und klicken Sie auf **[!UICONTROL Zielgruppe hinzufügen]**.

     ![Wählen Sie ein Zielgruppensegment für den Knoten aus](./assets/node-audience-add-dialog.png){width="700" zoomable="yes"}

   * **[!UICONTROL Kontoliste]**

     Wählen Sie diesen Typ aus und klicken Sie dann auf **[!UICONTROL Kontoliste hinzufügen]**.

     Wählen _[!UICONTROL im Dialogfeld „Live-]_ auswählen“ eine zuvor veröffentlichte Kontoliste aus und klicken Sie auf **[!UICONTROL Speichern]**.

     ![Live-Kontoliste für den Knoten auswählen](./assets/account-journey-account-audience-select-account-list.png){width="700" zoomable="yes"}

     Unter [Kontolisten](../accounts/account-lists.md) finden Sie detaillierte Informationen zum Erstellen und Veröffentlichen von Kontolisten.

_So erstellen Sie ein Zielgruppensegment:_

1. Wählen Sie in der linken Navigation **[!UICONTROL Konten]** > **[!UICONTROL Zielgruppen]** aus.

1. Klicken Sie oben rechts auf **[!UICONTROL Zielgruppe erstellen]**.

   ![Erstellen eines Zielgruppensegments](./assets/audiences-list-create.png){width="800" zoomable="yes"}

1. Führen Sie die im [Handbuch zum Segmentierungs-Service](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/ui/account-audiences){target="_blank"} beschriebenen Schritte aus.
