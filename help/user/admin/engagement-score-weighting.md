---
title: Konfigurieren der Gewichtung der Interaktionswerte
description: Erstellen Sie benutzerdefinierte Interaktionsbewertungsmodelle mit gewichteten Aktivitäten, um die Kaufgruppeninteraktion und -absicht in Journey Optimizer B2B edition genau zu messen.
feature: Setup, Engagement, Buying Groups
role: Admin
exl-id: 50d79d31-5ad8-41ed-a62b-4aa2ed9e837f
source-git-commit: 9ed2d2a36dbdaf39c107a18632d951003c86197b
workflow-type: tm+mt
source-wordcount: '892'
ht-degree: 0%

---

# Konfigurieren der benutzerdefinierten Gewichtung der Interaktionswerte

Der Interaktionswert einer Einkaufsgruppe spiegelt den Grad der Interaktion wider, indem er verschiedene Aktivitäten auswertet, die für Mitglieder der Einkaufsgruppe aufgezeichnet wurden. Mit der benutzerdefinierten Score-Gewichtung können Marketing-Operations-Teams ihre eigenen Modelle für die Gewichtung der Aktivitäten definieren, die für die Interaktion am aussagekräftigsten sind. Ein benutzerdefiniertes Scoring-Modell liefert eine genauere Darstellung Ihrer Pipeline, indem es die Verhaltensweisen priorisiert, die die Kaufabsicht in Ihrem Verkaufsprozess am genauesten signalisieren.

Als Administrator können Sie mehrere Interaktionsbewertungsmodelle für Ihre Organisation definieren, aber immer kann nur ein Modell aktiv sein. Sie definieren ein Score-Modell anhand der Gewichtung, die auf jede Interaktions-Scoring-Aktivität angewendet wird.

## Zugriff auf die Gewichtungsmodelle für Interaktionsbewertungen

1. Wählen Sie in der linken Navigation **[!UICONTROL Administration]** > **[!UICONTROL Konfigurationen]**.

1. Klicken Sie **[!UICONTROL Zwischenbereich auf]** Engagement Score-Gewichtung“, um die Liste der Scoring-Modelle anzuzeigen.

   Auf dieser Seite können Sie [Interaktionsbewertungsmodelle erstellen (duplizieren](#create-an-engagement-score-model), [aktivieren](#activate-a-score-model) und [bearbeiten](#change-the-engagement-weighting-settings).

   ![Zugriff auf die konfigurierten Ereignisdefinitionen](./assets/configuration-engagement-scoring-list.png){width="800" zoomable="yes"}

   Die Tabelle zeigt die zuletzt aktualisierten Modelle oben an (sortiert nach _[!UICONTROL Zuletzt aktualisiert]_) und bietet die Möglichkeit, nach _[!UICONTROL Name]_ zu suchen.

   Sie können die angezeigte Tabelle anpassen, indem Sie auf das Symbol _Spalteneinstellungen_ ( ![Spalteneinstellungen](../assets/do-not-localize/icon-column-settings.svg) ) in der oberen rechten Ecke klicken und die Kontrollkästchen für die Spalten aktivieren oder deaktivieren.

   ![Spalten für die Anzeige in der Liste der Interaktionsbewertungen](./assets/configuration-engagement-scoring-list-columns.png){width="300"}

1. Um auf die Details für ein Interaktionsbewertungsmodell zuzugreifen, klicken Sie auf den Namen.

### Standard-Bewertungsmodell

Das System erstellt ein anfängliches Interaktionsbewertungsmodell mit dem Namen _Aktivitätsgewichtungsmodell 1_, das das aktive Modell ist, bis Sie Ihr eigenes benutzerdefiniertes Modell erstellen und aktivieren. Wenn Sie Ihr benutzerdefiniertes Modell aktivieren, ändert sich das Standardmodell in den Status _Archiviert_. Sie können sie duplizieren, wenn Sie zum standardmäßigen Interaktionsbewertungsmodell zurückkehren oder sie als Ausgangspunkt für ein anderes benutzerdefiniertes Modell verwenden möchten.

![Gewichtungsmodell für den Standardinteraktionswert](./assets/configuration-engagement-scoring-model-default.png){width="600" zoomable="yes"}

### Löschen eines Entwurfsmodells

Sie können ein Entwurfs-Interaktionsbewertungsmodell löschen, wenn Sie es in Zukunft nicht aktivieren möchten. Klicken Sie auf das _Mehr_ Menü (***…***) neben dem Namen des Entwurfs-Bewertungsmodells in der Liste und wählen Sie **[!UICONTROL Löschen]**.

![Löschen des Entwurfs-Bewertungsmodells](./assets/configuration-engagement-scoring-model-more-delete.png){width="350"}

Klicken Sie im Bestätigungsdialog auf **[!UICONTROL Löschen]**.

## Erstellen eines benutzerdefinierten Interaktions-Bewertungsmodells

Um ein benutzerdefiniertes Interaktionsbewertungsmodell zu erstellen, duplizieren Sie das Standardmodell oder ein anderes bereits erstelltes benutzerdefiniertes Modell. Sie können das aktuelle _Aktiv_-Modell, ein _Entwurf_-Modell oder ein _Archiviert_-Modell duplizieren. Bearbeiten Sie dann das doppelte Modell entsprechend Ihren Anforderungen.

1. Klicken Sie auf den Modellnamen, um die Seite mit den Modelldetails zu öffnen, und klicken **[!UICONTROL oben]** auf „Duplizieren“.

   ![Duplizieren Sie das aktive Modell](./assets/configuration-engagement-scoring-model-duplicate.png){width="600" zoomable="yes"}

   Sie können auch auf das Symbol _Mehr Menü_ (***…***) neben dem Namen des Bewertungsmodells in der Liste klicken und **[!UICONTROL Duplizieren]** auswählen.

   ![Verwenden Sie das Menü Mehr , um das aktive Modell zu duplizieren](./assets/configuration-engagement-scoring-model-more-duplicate.png){width="325"}

1. Geben _im Dialogfeld &quot;_&quot; einen eindeutigen Namen für das duplizierte Modell ein und klicken Sie auf **[!UICONTROL Duplizieren]**.

   ![Bestätigen Sie, um das Bewertungsmodell zu duplizieren](./assets/configuration-engagement-scoring-model-duplicate-dialog.png){width="500"}

   Das duplizierte Modell wird in der Liste mit dem Status _Entwurf_ angezeigt. Klicken Sie auf den Namen, um die Details des Bewertungsmodells zu öffnen und Ihre Änderungen vorzunehmen.

### Ändern der Einstellungen für die Interaktionsgewichtung

Die Gewichtungseinstellungen definieren die Bänder, die Sie jeder Aktivität im Modell zuweisen können. Sie können die Bands ändern, um die Strategien Ihres Unternehmens zur Bewertung der Interaktion widerzuspiegeln. Sie können beispielsweise die _&quot;_&quot; auf einen Wert von 65 anpassen, wenn Sie den normalen Aktivitäten einen höheren Wert zuweisen möchten. Sie können auch ein Gewichtungsband hinzufügen, das Aktivitäten erfasst, die zwischen &quot;_&quot;_ &quot;_&quot;_. In diesem Fall können Sie ein Band hinzufügen und es mit &quot;_&quot;_ und einen Gewichtungsbandwert von 75 zuweisen.

1. Klicken Sie auf der Detailseite des Score **[!UICONTROL Modells oben auf]** Einstellungen für Interaktionsgewichtung“.

   ![Zugriff auf Einstellungen für die Interaktionsgewichtung](./assets/configuration-engagement-scoring-model-weight-settings-button.png){width="600" zoomable="yes"}

1. Passen Sie für jedes Gewichtsband den Namen oder die Werte Ihren Anforderungen entsprechend an:

   * Ändern Sie den Namen im Feld _[!UICONTROL Gewichtungsband]_.
   * Einen neuen Wert eingeben. Sie können auch auf **&amp;plus;** oder **−** klicken, um den Wert zu erhöhen oder zu verringern.

   ![Einstellungen für die Interaktionsgewichtung](./assets/configuration-engagement-scoring-model-weight-settings.png){width="500"}

1. Fügen Sie bei Bedarf ein weiteres Gewichtsband hinzu:

   Klicken Sie unten **[!UICONTROL der Liste auf]**+ Gewichtungsband hinzufügen . Durch diese Aktion wird ein leeres Gewichtungsband am Ende der Liste eingefügt.

   Geben Sie den Namen ein und legen Sie den Wert für das Band fest. Stellen Sie sicher, dass Sie einen eindeutigen Namen und Wert verwenden.

1. Entfernen Sie gegebenenfalls ein Gewichtungsband, und klicken Sie auf das Symbol _Löschen_ ( ![Löschsymbol](../assets/do-not-localize/icon-delete-outline.svg) ) für die Zeile „Gewichtungsband“.

1. Wenn Ihre Änderungen abgeschlossen sind, klicken Sie auf **[!UICONTROL Speichern]**.

### Ändern der Aktivitätsgewichtung

Jedes Score-Modell enthält die vollständige Liste der unterstützten Interaktionsbewertungsaktivitäten:

{{engagement-activities}}

Legen Sie für jede Aktivität in der Liste den Wert fest, den Sie jeder Aktivitätsinstanz zuweisen möchten. Klicken Sie im Feld **[!UICONTROL Gewichtung]** auf den Abwärtspfeil und wählen Sie das in den Einstellungen für die Interaktionsgewichtung definierte Gewichtungsband aus.

![Festlegen der Aktivitätsgewichtung](./assets/configuration-engagement-scoring-model-set-activity-weighting.png){width="500"}

Wenn bei der Berechnung des Interaktionswerts keine Aktivität verwendet werden soll, legen Sie für die Gewichtung einen Wert von null (0) fest.

Ihre Änderungen werden automatisch gespeichert.

## Score-Modell aktivieren

Wenn Sie ein Entwurfsbewertungsmodell aktivieren, ersetzt es das derzeit aktive Modell. Das aktuell aktive Modell wird automatisch archiviert.

1. Öffnen Sie ein Bewertungsmodell für einen Entwurf, um die Detailseite anzuzeigen.

1. Klicken Sie **[!UICONTROL Aktivieren]**.

1. Klicken Sie im Bestätigungsdialogfeld auf **[!UICONTROL Aktivieren]**.

   ![Zugriff auf die konfigurierten Ereignisdefinitionen](./assets/configuration-engagement-scoring-activate-dialog.png){width="400"}
