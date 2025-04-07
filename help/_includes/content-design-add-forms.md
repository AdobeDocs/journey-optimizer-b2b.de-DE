---
title: Inhaltserstellung - Formulare hinzufügen
description: Wiederverwendbarer Abschnitt zum Hinzufügen von Formularen in Landingpages und Vorlagen
source-git-commit: 97d8e5b366e8786e517c18828236f95304f3f3be
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 0%

---

# Inhaltserstellung - Formulare hinzufügen

Ein Formular ist eine wiederverwendbare Komponente, die von mehreren Landingpages und Landingpage-Vorlagen in Adobe Journey Optimizer B2B edition referenziert werden kann. Es handelt sich dabei um einen Block von Feldern und eine Senden-Schaltfläche, die vorab erstellt und schnell eingefügt werden können, um den Seitenentwurf schneller und konsistenter zu machen.

Im folgenden Beispiel werden Schritte zum Hinzufügen eines Formulars während des Designs Ihrer Seite beschrieben.

1. Ziehen Sie **[!UICONTROL Abschnitt]** Inhalte“ das Element **[!UICONTROL Formular]** und legen Sie es in einer Strukturkomponente im Seitendesign-Bereich ab.

   ![Ziehen Sie eine Formular -Komponente in den visuellen Design-Bereich](../assets/content-design-shared/content-design-add-form.png){width="600"}

   >[!TIP]
   >
   >Um das Formular so hinzuzufügen, dass es das gesamte horizontale Layout in der E-Mail einnimmt, fügen Sie eine 1:1-Spaltenstruktur hinzu und ziehen Sie das Formular dann per Drag-and-Drop hinein.

1. Klicken Sie auf das _Formular_-Symbol in der Komponenten-Symbolleiste oder verwenden Sie die Eigenschaften **[!UICONTROL Formular einbetten]** rechts, um das veröffentlichte Formular auszuwählen.

   ![Wählen Sie das veröffentlichte Formular aus](../assets/content-design-shared/content-design-add-form-properties.png){width="600"}

1. Wenn Sie den standardmäßigen **[!UICONTROL Follow-up-Typ]** für das Formular überschreiben möchten, ändern Sie die Einstellung entsprechend den Anforderungen für Ihre Seite oder Vorlage.

   Dies wird auch als &quot;_-Seite“_ das Formular bezeichnet. Diese Einstellung bestimmt, was passiert, wenn ein Besucher das Formular sendet:

   * **[!UICONTROL Auf Seite bleiben]** - Wählen Sie diese Option, um den Besucher beim Senden des Formulars auf der gleichen Seite zu belassen.

   * **[!UICONTROL Landingpage]** - Wählen Sie diese Option, um eine beliebige Journey Optimizer B2B edition- oder Marketo Engage-Landingpage als Folgemaßnahme auszuwählen.

   * **[!UICONTROL Externe URL]** - Wählen Sie diese Option aus, um eine beliebige URL als Folgeseite anzugeben. Nachdem der Besucher das Formular gesendet hat, lädt der Browser die vorgesehene URL.

     >[!TIP]
     >
     >Wenn Sie das Formular zum Herunterladen einer Datei verwenden möchten, können Sie eine URL für die gehostete Datei angeben. Mit dieser Konfiguration fungiert die Senden-Schaltfläche als Download-Schaltfläche.

   ![Ändern der Folgeeinstellung](../assets/content-design-shared/content-design-add-form-follow-up.png){width="280"}

1. Wenn Sie die Anzeige des Formulars nach Gerätetyp beschränken möchten, ändern Sie die Einstellung **[!UICONTROL Anzeigeoptionen]**:

   * **[!UICONTROL Nur auf Desktop-Geräten anzeigen]**
   * **[!UICONTROL Nur auf Mobilgeräten anzeigen]**
   * **[!UICONTROL Auf allen Geräten anzeigen]** (Standard)

1. Wählen Sie bei Bedarf die **[!UICONTROL Stile]** im rechten Bereich aus, um die Formularränder innerhalb der Seite festzulegen.
