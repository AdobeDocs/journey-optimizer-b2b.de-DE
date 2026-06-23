---
title: Programmtypen
description: Erstellen und verwalten Sie Programmtypen, die Attribute und Mitgliedsstatusflüsse für Programme in Journey Optimizer B2B Prime definieren.
badgeBeta: label="Beta" type="informative" tooltip="Diese Funktion befindet sich derzeit in einer eingeschränkten Beta-Version"
autotag-review: '2026-06-23T19:10:36.949Z'
TQID: 'https://experienceleague.adobe.com/gDNLfcAICFtF7M-cB1zJjLih5kL6nUlpYA5zb1aQJv0'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: aed878b8-11d0-487c-828b-d23b2051ec37id: d6e625c1-468f-4d73-9f32-fd1edb87f96b
subfeature_v2: id: f6df9def-cdf7-4728-9ec8-3f65716828c7id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ad5a67d291ffef797bb93f8b06f1bd8657efb67f
workflow-type: tm+mt
source-wordcount: 401
ht-degree: 2%

---

# Programmtypen

Programmtypen definieren wichtige Aspekte von [Programmen](../marketing/programs.md) und deren Mitgliedern und unterscheiden verschiedene Arten von Marketing-Programmen voneinander. Jeder Programmtyp definiert die folgenden Eigenschaften, die für Programme mithilfe des Programmtyps übernommen werden:

* **Attribute** - Die Attribute beschreiben die wichtigen Aspekte des Programmtyps, wie Ereignisdaten und Standortattribute.

* **Programmstatusfluss** - Jeder Status wird einem Schritt im Programmtyp zugewiesen (z. B. 1, 2 oder 3). Mitglieder eines Programms können nur von einem Status mit derselben Schrittnummer (z. B. von _Nicht angezeigt_ zu _Teilgenommen_) oder zu einem Status mit einer höheren Schrittnummer (z. B. von _Eingeladen_ zu _Registriert_) wechseln.

  Programmstatus schließen sich gegenseitig aus und sind linear, sodass eine Person nur einen Statuswert pro Programm haben kann. Überlegen Sie beim Entwerfen von Status, zwischen welchen Status Sie wechseln möchten. Wenn beispielsweise jemand nicht zu einem Webinar erschienen ist, aber die Möglichkeit hat, später bei Bedarf teilzunehmen, sollte er entweder dieselbe Statusnummer erhalten oder bei Bedarf eine höhere Statusnummer erhalten, damit ein Programmmitglied zu dieser wechseln kann.

>[!NOTE]
>
>Wenn ein Programmtyp von mindestens einem Programm verwendet wird, kann er nicht bearbeitet werden.

_So definieren Sie einen benutzerdefinierten Programmtyp :_

1. Erweitern Sie in der linken [!DNL Adobe Journey Optimizer B2B Prime]-Navigation **[!UICONTROL Administration]** und wählen Sie **[!UICONTROL Programmtypen]**.

   ![Zugriff auf die Liste der Programmtypen](./assets/program-types-list.png){width="800" zoomable="yes"}

1. Klicken **[!UICONTROL oben]** auf „Typ erstellen“.

1. Geben Sie einen eindeutigen **[!UICONTROL Name]** (erforderlich) und **[!UICONTROL Beschreibung]** (optional) ein.

   ![Programmtyp erstellen](./assets/program-type-create.png){width="600" zoomable="yes"}

   >[!TIP]
   >
   >Das Einschließen einer Beschreibung ist eine Best Practice und macht Ihre Programmtypbibliothek leichter zu verwalten.

1. Klicken Sie **[!UICONTROL Typ erstellen]**.

1. Fügen Sie **[!UICONTROL Programmtyp]** Attribute“ hinzu.

   Für jedes Attribut, das Sie hinzufügen möchten:

   * Klicken Sie **[!UICONTROL Attribut hinzufügen]**.
   * Wählen Sie den **[!UICONTROL API-]** aus und geben Sie den **[!UICONTROL Anzeigenamen]** ein.
   * Klicken Sie auf **[!UICONTROL Speichern]**.

   ![Attribute vom Typ Programm](./assets/program-type-attributes.png){width="600" zoomable="yes"}

1. Definieren Sie die Schritte für **[!UICONTROL Programmstatus]**.

   Definieren Sie jeden Schritt, den Sie in den Fluss aufnehmen möchten:

   * Klicken Sie **[!UICONTROL Schritt hinzufügen]**.
   * Geben Sie einen Statusnamen ein.
   * (Optional) Klicken Sie **[!UICONTROL Status hinzufügen]** und geben Sie einen zusätzlichen Statusnamen ein, der in den Schritt aufgenommen werden soll.

   Aktivieren Sie das **[!UICONTROL Als Erfolg]** markieren) für jeden Schritt, den Sie als erfolgreiche Programmausführung verfolgen möchten.

   ![Programmtypstatus](./assets/program-type-statuses.png){width="600" zoomable="yes"}

1. Klicken Sie **[!UICONTROL Fertig]**, um Ihre Änderungen zu speichern und zur Liste Programmtypen zurückzukehren.