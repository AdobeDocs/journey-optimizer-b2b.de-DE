---
title: Ereignisbasierte Zielgruppen
description: Verwenden Sie ereignisbasierte Zielgruppen in Journey Optimizer B2B Prime, um auf der Grundlage von Marketo Engage-Aktivitäten nahezu in Echtzeit einen Trigger-Personen-Journey-Eintrag zu erstellen.
badgeBeta: label="Beta" type="informative" tooltip="Diese Funktion befindet sich derzeit in einer eingeschränkten Beta-Version"
autotag-review: '2026-06-25T17:59:01.953Z'
TQID: 'https://experienceleague.adobe.com/04J58rjKw0hCoTOeYheZIPaX-YR8GwP-k6-Wn3XCetU'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
subfeature_v2:
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 263e15040990a48475ffdd2b0b25d1cb557d5abf
workflow-type: tm+mt
source-wordcount: 332
ht-degree: 3%

---

# Ereignisbasierte Zielgruppen

Mit _ereignisbasierten Zielgruppen_ können Sie [!DNL Adobe Journey Optimizer B2B Prime] Zielgruppenmitglieder nahezu in Echtzeit zu einer Live-[Personen-Journey](../marketing/person-journeys.md) hinzufügen, wenn eine [!DNL Marketo Engage] stattfindet. Sie konfigurieren ereignisbasierte Zielgruppen auf dem Zielgruppenknoten der Journey-Arbeitsfläche:

* Wählen Sie eine oder mehrere [!DNL Marketo Engage] Aktivitäten (Standard oder benutzerdefiniert) als qualifizierende Ereignisse aus.
* Fügen Sie optional Personenprofilfilter hinzu (z. B. Branche, Region oder Lebenszyklusphase), um einzugrenzen, welche Personen eintreten können.
* Definieren Sie optional Aktivitätsattribut-Einschränkungen (z. B. ein bestimmtes Formular, eine bestimmte URL oder ein bestimmtes Programm), um einzugrenzen, welche Vorkommen jeder Aktivität qualifiziert sind.

Wenn eine qualifizierte Aktivität für einen Lead [!DNL Marketo Engage] angemeldet und in [!DNL Adobe Journey Optimizer B2B Prime] repliziert wird, wertet das System den entsprechenden Personendatensatz anhand Ihrer konfigurierten Filter und Begrenzungen aus. Wenn die Bedingungen erfüllt sind, gelangt die Person sofort über den Zielgruppenknoten auf die Journey.

_So definieren Sie eine ereignisbasierte Zielgruppe für eine Personen-Journey :_

1. Wählen Sie den [_Zielgruppe Person_-Knoten](../marketing/person-audience-node.md).

1. Wählen Sie rechts in den Knoteneigenschaften als Eintragstyp **[!UICONTROL Ereigniszielgruppe]** aus.

   ![Knoten „Zielgruppen-Journey für Personen“ auf „Ereignisbasierte Zielgruppe“ festgelegt](./assets/event-based-audience-node.png){width="400"}

1. Klicken Sie **[!UICONTROL Ereigniskriterien hinzufügen]**.

1. Fügen Sie _[!UICONTROL Dialogfeld Ereigniskriterien bearbeiten]_ eine oder mehrere [!DNL Marketo Engage] Aktivitäten als qualifizierte Ereignisse hinzu, z. B.:

   * _Teilnahme am Webinar_
   * _E-Mail wird zugestellt_
   * _Klicks auf Link in E-Mail_

   >[!NOTE]
   >
   >Sie können auch benutzerdefinierte Aktivitäten auswählen, die in der zugehörigen [!DNL Marketo Engage]-Instanz definiert sind.

   Legen Sie für jede Aktivität den passenden Operator und die entsprechenden Werte fest.

   ![Aktivitäts-Trigger für eine ereignisbasierte Zielgruppe](./assets/event-based-audience-triggers.png){width="700" zoomable="yes"}

   Eine Person qualifiziert sich für die Journey, wenn eine dieser konfigurierten Aktivitäten für diesen Lead protokolliert wird.

1. (Optional) Um eine Ereignis- und Filterkombination für die Zielgruppen-Qualifizierung zu verwenden, fügen Sie Filter auf Personenebene hinzu.

   * Wählen Sie die **[!UICONTROL Filter]** aus.
   * Ziehen Sie jeden Filter und legen Sie die entsprechenden Kriterien fest.

   ![Personenfilter für eine ereignisbasierte Zielgruppe](./assets/event-based-audience-filters.png){width="700" zoomable="yes"}

   Wenn Sie Filter hinzufügen, muss die Person mindestens eine konfigurierte Aktivitätsbedingung und die konfigurierten Filter erfüllen.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

