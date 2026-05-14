---
title: Exportieren von Konten
description: Exportieren Sie gefilterte Kontolisten in eine CSV-Datei für Drittanbieterplattformen mit Kaufgruppen- und Interaktionswertfiltern in Journey Optimizer B2B Edition.
feature: Audiences
role: User
exl-id: 3ec8e8fd-1bc2-4efa-840f-f06520099060
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: e935834c-48b7-43d8-b754-a815196a1b05
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
autotag-review: 2026-03-30T19:51:33.392Z
TQID: https://experienceleague.adobe.com/fvkVLjO9oIF7hOuoqdSS-jU4wAvsrPnKp1fIabH-Ewk
source-git-commit: 9baf03a1ddc1733385b0398ffadde8f548c431cc
workflow-type: tm+mt
source-wordcount: 261
ht-degree: 100%

---

# Exportieren von Konten

Verwenden Sie die Funktion _Konten exportieren_, um alle Konten oder eine Reihe von Konten basierend auf von Ihnen definierten Filtern zu exportieren. Durch den Exportvorgang wird eine CSV-Datei generiert und die URL für die gespeicherte Datei wird innerhalb einer Pulse-Benachrichtigung gesendet. Mit dieser Funktion können Sie bei Bedarf Konten in Plattformen von Drittanbietern verschieben.

1. Navigieren Sie in Journey Optimizer B2B Edition in der linken Navigation zu **[!UICONTROL Konten]** > **[!UICONTROL Käufergruppen]**.

1. Wählen Sie die Registerkarte **[!UICONTROL Durchsuchen]** aus.

1. Klicken Sie oben rechts auf **[!UICONTROL Konten exportieren]**.

   ![Kontodetails bearbeiten](./assets/export-accounts.png){width="800" zoomable="yes"}

1. Definieren Sie im Dialogfeld die Parameter der zu exportierenden Kontozielgruppen.

   ![Angeben der Filterung der Kontozielgruppe](./assets/export-accounts-dialog.png){width="400"}

   Für die **[!UICONTROL Interaktionsbewertung]** ist der Operator `Between` ebenso inklusiv wie Prozentbereiche. Zum Beispiel liegen 5.1 und 5 beide _zwischen_ 5 und 6.

   Leere Filterungsparameter werden wie `Is Any` behandelt.

1. Klicken Sie auf **[!UICONTROL Konten exportieren]**, um die CSV-Datei mit den angegebenen Filtern zu generieren.

1. Wenn Sie eine Benachrichtigung über den Abschluss des Exports erhalten, klicken Sie auf den Benachrichtigungs-Link, um auf die CSV-Datei zuzugreifen.

   ![Auf die Benachrichtigung klicken, um die CSV-Datei mit der Liste der exportierten Konten herunterzuladen](./assets/export-accounts-notification.png){width="425"}

   >[!NOTE]
   >
   >Wenn Sie über ein Benachrichtigungsabonnement für E-Mail-Benachrichtigungen verfügen, das in den Voreinstellungen Ihres Adobe-Benutzerkontos eingerichtet ist, kann es sich um eine E-Mail-Benachrichtigung handeln.

   Die Anwendungsseite leitet Sie zur Registerkarte zum Durchsuchen der _Käufergruppe_ weiter, und Sie werden im Dialogfeld „Systemdatei speichern“ dazu aufgefordert, die Datei in Ihrem System zu speichern. Wenn Sie die Daten freigeben müssen, können Sie das Dateifreigabesystem Ihres Teams verwenden.
