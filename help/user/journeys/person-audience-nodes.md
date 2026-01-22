---
title: Personen-Zielgruppenknoten
description: Konfigurieren Sie Personen-Zielgruppenknoten mit segmentbasierten oder ereignisbasierten Zielgruppen, um Einstiegspunkte für den Personen-Journey für die zielgerichtete Orchestrierung in Journey Optimizer B2B edition zu definieren.
feature: Audiences
role: User
badgeBeta: label="Beta" type="informative" tooltip="Diese Funktion befindet sich derzeit in einer eingeschränkten Beta-Version"
source-git-commit: f5170767a6df14874fab5de203264a5a5e3e245a
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 0%

---

# Personen-Zielgruppen-Journey-Knoten

Der _Personen-Zielgruppe_-Knoten gibt an, welche Personenprofile in die Journey eintreten. Wenn Sie [Personen-Journey erstellen](./create-publish-journey.md#create-a-journey) beginnt die Journey immer mit einem Personen-Zielgruppenknoten, der die Eingabe definiert. Der Zielgruppenknoten Person kann einen von zwei Zielgruppen-Eingabetypen aufweisen: CDP-Segmente oder ereignisbasierte Zugehörigkeit. Segmentbasierte und ereignisbasierte Zielgruppendefinitionen können nicht kombiniert werden.

Verwenden Sie eine der folgenden Eingabeoptionen für den Knoten „Zielgruppen-Journey für Personen“:

* **Profilzielgruppe** - Verwenden Sie in einer CDP definierte Segmentzielgruppen. Alle Profile, die sich für die Zielgruppe qualifizieren, werden der Journey als Mitglieder hinzugefügt. Neu für das Segment qualifizierte Profile werden während der täglichen (Profil[Aufnahme) -Aufgaben &#x200B;](#profile-ingestion) Journey hinzugefügt. Wenn sich ein Profil nicht mehr für das Segment qualifiziert, wird es **_nicht_** von der Journey entfernt.

* **Ereigniszielgruppe** - Verwenden Sie qualifizierende Ereignisse, um die Zielgruppe zu definieren. Diese Ereignisse werden in der Knotenkonfiguration definiert und müssen [XDM-Ereignisse verwenden, die in den Administrationseinstellungen konfiguriert sind](../admin/configure-aep-events.md). Bis zu 10 Ereignisse werden für die ereignisbasierte Zielgruppenzugehörigkeit unterstützt. Ein Profil qualifiziert sich sofort für das Journey, nachdem das erste passende Ereignis eintritt, das sein Profil eingeht.

  >[!NOTE]
  >
  >Ereignisse können nicht mit Profilattributen kombiniert werden, um Zielgruppendefinitionen einzugrenzen. Verbesserungen in Bezug auf diese Einschränkung sind für zukünftige Versionen geplant.

## Profilaufnahme

In Journey Optimizer B2B edition verwaltet eine nächtliche Zielgruppen-Erfassungsaufgabe Profile mit Experience Platform. Während ereignisbasierte Personenprofile Journey-Profile qualifizieren können, die nicht Teil einer Profil- oder Account-Zielgruppe sind, die von Journey Optimizer B2B edition aufgenommen/verwendet wird, führt dies zu aufgenommenen Profilen, die veraltet bleiben, es sei denn, sie sind Teil einer Zielgruppe, die von einer Person auf Journey, Account-Journey oder einer Einkaufsgruppe verwendet wird. Wenn ein Profil aufgenommen und später zu einer Zielgruppe hinzugefügt wird, wird eine Profilzuordnung durchgeführt und das Profil bleibt mit Experience Platform synchronisiert. Verbesserungen an dieser Profildaten-Synchronisierung sind für zukünftige Versionen geplant.

Ein neu erstelltes Profil, das von einer ereignisbasierten Personen-Journey aufgenommen wurde, verfügt zum Zeitpunkt der Aufnahme möglicherweise nicht über die aktualisierten Profilinformationen. Wenn beispielsweise ein Profil über ein Formularausfüllereignis erstellt wird und eine Person Journey diese Daten vom qualifizierten Formularausfüllereignis erfasst, werden die im Formular übermittelten Daten möglicherweise noch nicht mit dem Profil synchronisiert, wenn die Journey sie aufgenommen hat. Das Ergebnis könnten unvollständige Daten für die Personalisierung sein (z. B. in E-Mail-Inhalten). Verbesserungen an dieser Profilereignisdaten-Synchronisierung sind für zukünftige Versionen geplant.

Ereignisbasierte Personenprofile, die noch anonym sind/keine E-Mail-Adressen aufweisen und nur ECIDs enthalten, können durch Journey-Ereignisse qualifiziert werden. Dies geschieht am häufigsten, wenn Sie eine Qualifizierungslogik für Web-Seitenaktivitäten haben. Eine zu breite ereignisbasierte Zielgruppenlogik könnte dazu führen, dass die Instanz die 40-Millionen-Profilbegrenzung erreicht, wenn zu viele Profile qualifiziert sind. Beschränken Sie den möglichen Umfang Ihrer Audience, um dieses Szenario zu verhindern.

>[!IMPORTANT]
>
>Während des aktuellen Beta-Programms ist die ideale Verwendung von Personen-Journey, um nur Profile zu qualifizieren, an die Sie auch in Account-Journeys und Einkaufsgruppendefinitionen denken. Dadurch wird sichergestellt, dass ein vollständiges Profil mit Experience Platform synchronisiert bleibt.

## Festlegen der Zielgruppe für den Zielgruppenknoten „Person“

1. Klicken Sie auf **[!UICONTROL Knoten]** Zielgruppe“.

   Diese Aktion zeigt die Knoteneigenschaften rechts an.

   ![Zielgruppen-Journey-Knoten für Person](./assets/person-journey-person-audience-node.png){width="700" zoomable="yes"}

1. Wählen Sie den Eingabetyp für Personen, die die Journey betreten:

   * **[!UICONTROL Profil-Zielgruppe]**

     Wählen Sie die Option _[!UICONTROL Profil-Zielgruppe]_ aus. Klicken Sie dann auf **[!UICONTROL Profil-Audience hinzufügen]**.

     Wählen Sie _[!UICONTROL Dialogfeld]_ Zielgruppe hinzufügen“ ein zuvor erstelltes Zielgruppensegment aus. Klicken Sie dann auf **[!UICONTROL Zielgruppe hinzufügen]**.

     ![Wählen Sie eine Profilzielgruppe für den Knoten aus](./assets/node-person-audience-add-audience-dialog.png){width="700" zoomable="yes"}

   * **[!UICONTROL Ereigniszielgruppe]**

     Wählen Sie die Option _[!UICONTROL Ereigniszielgruppe]_ aus. Klicken Sie dann auf **[!UICONTROL Ereigniskriterien hinzufügen]**.

     Fügen Sie _[!UICONTROL Dialogfeld Ereigniskriterien bearbeiten]_ ein oder mehrere Ereignisse hinzu, die Sie für die Qualifizierung von Zielgruppenmitgliedern verwenden möchten. Klicken Sie für jedes Ereignis, das Sie hinzufügen, auf **[!UICONTROL Begrenzung hinzufügen]**, um ein Ereignisattribut für eine Übereinstimmung auszuwählen. Legen Sie die Auswertung fest, die Sie für eine Übereinstimmung verwenden möchten. Sie können dem Ereignis mehrere Einschränkungen hinzufügen.

     ![Ereignisse hinzufügen und Kriterien zum Qualifizieren eines Personenprofils erfüllen](./assets/node-person-audience-edit-event-criteria-dialog.png){width="700" zoomable="yes"}

     Wenn die Ereigniskriterien definiert sind, klicken Sie auf **[!UICONTROL Speichern]**.

     Weitere Informationen zur Konfiguration für Journey-unterstützte Ereignisse finden Sie unter [Verwalten von Erlebnisereignissen](../admin/configure-aep-events.md#manage-experience-events).
