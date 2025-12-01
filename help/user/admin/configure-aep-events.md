---
title: Erlebnisereignisse und -felder auswählen
description: Wählen Sie Experience Platform-Ereignisse und -Felder aus, um die Echtzeit-Entscheidungsfindung in Journey auf Grundlage des Kundenverhaltens in Triggern zu ermöglichen.
feature: Setup, Integrations
role: Admin
badgeBeta: label="Beta" type="informative" tooltip="Diese Funktion befindet sich derzeit in der Beta-Version"
solution: Journey Optimizer B2B Edition, Experience Platform
exl-id: a7696d03-f4c4-4f64-8ef2-b15e59b59770
source-git-commit: 5f3d7bb8eb72c48409273de43b03114d273cb80c
workflow-type: tm+mt
source-wordcount: '1463'
ht-degree: 10%

---

# Erlebnisereignisse und -felder auswählen

Admins können bestimmte [AEP-Erlebnisereignisse](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/classes/experienceevent){target="_blank"} und deren zugehörige Felder im Vereinigungsschema für Erlebnisereignisse auswählen. Nach der Auswahl können Benutzende Entscheidungsregeln konfigurieren, die auf diese Erlebnisereignisse lauschen, um dynamische und zielgerichtete Kampagnenaktionen zu ermöglichen, die auf nahezu in Echtzeit erfassten Ereignisdaten basieren.

<!-- ![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Watch the video overview](#overview-video) -->
Die Verwendung von AEP-Erlebnisereignissen in Journey ist ein zweistufiger Prozess:

1. AEP Ein Administrator ([&#x200B; Erlebnisereignisse und -felder) &#x200B;](#add-an-event) den Journey Optimizer B2B edition-Konfigurationen.

2. Auf einer Journey fügt der Marketing-Experte einen _Lauschen auf ein_) hinzu und [wählt ein Erlebnisereignis aus](../journeys/listen-for-event-nodes.md#listen-for-an-experience-event).

   * Wählt das im Knoten zu verwendende Ereignis aus.
   * Wählt die als Einschränkung zu verwendenden Felder aus.

>[!BEGINSHADEBOX]

## Richtlinien und Einschränkungen

Beachten Sie bei der Auswahl von Ereignissen zur Erreichung Ihrer Unternehmensziele Folgendes:

* Sie können bis zu 50 Ereignisse und bis zu 100 Felder pro Ereignis auswählen.

* Journey können Erlebnisereignisse überwachen, die über Experience Platform-Streaming-Funktionen aufgenommen werden, z. B. Web-SDK oder HTTP-API.

* Sie können Erlebnisereignisse für Entscheidungszwecke in einem Journey verwenden, sie werden jedoch nicht beibehalten. Daher können Sie keinen historischen Datensatz mit Erlebnisereignissen in Journey Optimizer B2B edition nutzen.

* Wenn Sie ein Erlebnisereignis verwenden und die Journey veröffentlichen, können Sie weitere Felder hinzufügen, zuvor ausgewählte Felder jedoch nicht entfernen.

* Sie können auf ein Erlebnisereignis in mehreren Journey verweisen oder ein Erlebnisereignis mehrmals auf derselben Journey verwenden.

>[!ENDSHADEBOX]

## Verwalten von Erlebnisereignissen

1. Wählen Sie in der linken Navigation **[!UICONTROL Administration]** > **[!UICONTROL Konfigurationen]**.

1. Klicken Sie **[!UICONTROL Zwischenbereich auf]** XDM-Klassen“ und anschließend auf die Registerkarte **[!UICONTROL Ereignisse]**, um die Liste der verfügbaren Ereignisse anzuzeigen.

   ![Zugriff auf die ausgewählten Erlebnisereignisse](./assets/configurations-xdm-classes-events.png){width="800" zoomable="yes"}

   Die Tabelle wird nach der Spalte _[!UICONTROL Letzte Aktualisierung]_ sortiert, wobei die zuletzt aktualisierten Ereignisse standardmäßig oben stehen.

   Auf dieser Seite können Sie Ereignisse [Auswählen](#add-an-event) und [Bearbeiten](#edit-an-event) zur Verwendung in Journey auswählen.

   Um auf die Details für ein ausgewähltes Ereignis zuzugreifen, klicken Sie auf den Ereignisnamen.

### Filtern der Ereignisliste

Geben Sie Text in das _[!UICONTROL Suchen]_-Feld ein, um die angezeigten Ereignisse nach einer Übereinstimmung mit dem Ereignisnamen zu filtern.

![Filtern Sie die Liste der ausgewählten Ereignisse nach Namen](./assets/configurations-xdm-classes-events-search.png){width="600" zoomable="yes"}

### Ereignis hinzufügen

Um ein Erlebnisereignis für den Knoten _Lauschen auf ein Ereignis_ auf einer Journey verfügbar zu machen, wählen Sie das Ereignis und die unterstützten Felder aus.

>[!NOTE]
>
>In der Beta-Version können Sie keine Ereignisse aus der Liste entfernen. Stellen Sie sicher, dass jedes Ereignis, das Sie hinzufügen, eines ist, das Ihr Unternehmen verwenden möchte.

1. Klicken **[!UICONTROL oben]** auf „Erlebnisereignis auswählen“.

   Die Seite mit den Ereignisdetails wird angezeigt. Auf dieser Seite können Sie den Ereignistyp und die Felder auswählen.

   ![Ereignisdetails für ein neues Ereignis](./assets/configurations-xdm-classes-events-select-new.png){width="700" zoomable="yes"}

1. Wählen Sie den Ereignistyp.

   * Klicken Sie **[!UICONTROL Ereignistyp auswählen]**.

   * Wählen Sie im Dialogfeld den Ereignistyp aus.

     Filtern Sie _[!UICONTROL angezeigte Liste mithilfe]_ Felds „Suche“ nach Namen. Mit dem Schieberegler **[!UICONTROL Nur ausgewählte Felder anzeigen]** können Sie die aktuellen Auswahlen überprüfen.

     ![Dialogfeld „Ereignistyp auswählen“](./assets/configurations-xdm-classes-select-event-type-dialog.png){width="450" zoomable="yes"}

   * Klicken Sie auf **[!UICONTROL Auswählen]**.

1. Wählen Sie ein oder mehrere Felder für den Ereignistyp aus.

   * Klicken Sie **[!UICONTROL Felder auswählen]**.

   * Wählen Sie im Dialogfeld die Felder aus, die Sie als Einschränkungen für übereinstimmende Ereignisse verwenden möchten.

     Filtern Sie _[!UICONTROL angezeigte Liste mithilfe]_ Felds „Suche“ nach Namen. Mit dem Schieberegler **[!UICONTROL Nur ausgewählte Felder anzeigen]** können Sie die aktuellen Auswahlen überprüfen.

     ![Dialogfeld „Felder auswählen“](./assets/configurations-xdm-classes-select-fields-dialog.png){width="450" zoomable="yes"}

   * Klicken Sie auf **[!UICONTROL Auswählen]**.

1. Klicken Sie auf der Seite mit den Ereignisdetails auf **[!UICONTROL Speichern]**.

Das gespeicherte Ereignis wird in der Liste auf der Registerkarte _[!UICONTROL Ereignisse]_ angezeigt.

### Ereignis bearbeiten

Bearbeiten Sie die Ereignisdetails, um die Felder zu ändern.

1. Klicken Sie auf den Ereignisnamen oder auf das Symbol _Mehr Menü_ ( **…** ) und wählen Sie **[!UICONTROL Bearbeiten]**.

   ![Klicken Sie auf das Menüsymbol Mehr &#x200B;](./assets/configurations-xdm-classes-events-more-menu.png){width="500" zoomable="yes"}

1. Klicken Sie **[!UICONTROL Felder bearbeiten]**, um im Dialogfeld „Felder _[!UICONTROL &quot; weitere Felder hinzuzufügen oder]_ Auswahl zu entfernen.

1. Klicken Sie **[!UICONTROL Auswählen]**, um Ihre Auswahl zu speichern.

### Ereignis entfernen

>[!NOTE]
>
>In der Beta-Version dieser Funktion können Sie kein Ereignis aus der Liste der ausgewählten Ereignisse entfernen. Für die GA-Version ist eine Entfernung von Ereignissen geplant.

## Ereignisse und Felder

[!DNL Journey Optimizer B2B Edition] werden bestimmte Aktivitäten auf Personenebene als Erlebnisereignisse [!DNL Experience Platform]. Diese Ereignisse werden in einem Systemdatensatz gespeichert, der das XDM-Erlebnisereignisschema verwendet und Journey-spezifische Feldergruppen enthält. Sie können diese Ereignisse in [!UICONTROL Journey Optimizer B2B edition] wie jedes andere Erlebnisereignis verwenden.

Jedes Ereignis zeigt einen definierten Satz von Feldern, die in Journey-Knoten (_eines Ereignisses)_ werden können (Ereignisentscheidung). Überprüfen Sie die verfügbaren Ereignistypen und ihre Felder, um zu bestimmen, welches Ereignis und welche Felder in diesen Journey-Knoten verwendet werden sollen:

### E-Mail gesendet

Dieses Ereignis verfolgt, wann eine Marketing-E-Mail an eine Person gesendet wurde.

Ereignistyp: `directMarketing.emailSent`

+++Felder

| Feld | Feldtyp |
| ----- | ---------- |
| Kennung | `_id` |
| Ereignistyp | `eventType` |
| Zeitstempel | `timestamp` |
| Personen-ID | `personID` |
| Personen-Quell-ID | `personKey.sourceID` |
| Quelltyp der Person | `personKey.sourceType` |
| ID der Quellinstanz der Person | `personKey.sourceInstanceID` |
| Ursprungsschlüssel der Person | `personKey.sourceKey` |
| E-Mail-Quell-ID | `directMarketing.emailSent.mailingKey.sourceID` |
| E-Mail-Quelltyp | `directMarketing.emailSent.mailingKey.sourceType` |
| E-Mail-Quellinstanz-ID | `directMarketing.emailSent.mailingKey.sourceInstanceID ` |
| E-Mail-Quellschlüssel | `directMailing.emailSent.mailingKey.sourceKey` |
| Mailing-Name | `directMarketing.emailSent.mailingName` |
| Journey-ID | `_experience.journeyOrchestration.stepEvents.journeyID` |
| Knoten-ID | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### E-Mail übermittelt

Dieses Ereignis verfolgt, wann eine E-Mail erfolgreich an den E-Mail-Service einer Person zugestellt wurde.

Ereignistyp: `directMarketing.emailDelivered `

+++Felder

| Feld | Feldtyp |
| ----- | ---------- |
| Kennung | `_id` |
| Ereignistyp | `eventType` |
| Zeitstempel | `timestamp` |
| Personen-ID | `personID` |
| Personen-Quell-ID | `personKey.sourceID` |
| Quelltyp der Person | `personKey.sourceType` |
| ID der Quellinstanz der Person | `personKey.sourceInstanceID` |
| Ursprungsschlüssel der Person | `personKey.sourceKey` |
| Mailingquellen-ID | `directMarketing.mailingKey.sourceID` |
| Quelltyp der E-Mail | `directMarketing.mailingKey.sourceType` |
| Quellinstanz-ID wird gesendet | `directMarketing.mailingKey.sourceInstanceID` |
| Quellschlüssel der E-Mail-Adresse | `directMarketing.mailingKey.sourceKey` |
| Mailing-Name | `directMarketing.mailingName` |
| Journey-ID | `_experience.journeyOrchestration.stepEvents.journeyID` |
| Knoten-ID | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### E-Mail geöffnet

Dieses Ereignis verfolgt, wann eine Person eine Marketing-E-Mail geöffnet hat.

Ereignistyp: `directMarketing.emailOpened`

+++Felder

| Feld | Feldtyp |
| ----- | ---------- |
| Kennung | `_id` |
| Ereignistyp | `eventType` |
| Zeitstempel | `timestamp` |
| Personen-ID | `personID` |
| Personen-Quell-ID | `personKey.sourceID` |
| Quelltyp der Person | `personKey.sourceType` |
| ID der Quellinstanz der Person | `personKey.sourceInstanceID` |
| Ursprungsschlüssel der Person | `personKey.sourceKey` |
| Mailingquellen-ID | `directMarketing.mailingKey.sourceID` |
| Quelltyp der E-Mail | `directMarketing.mailingKey.sourceType` |
| Quellinstanz-ID wird gesendet | `directMarketing.mailingKey.sourceInstanceID` |
| Quellschlüssel der E-Mail-Adresse | `directMarketing.mailingKey.sourceKey` |
| Mailing-Name | `directMarketing.mailingName` |
| Ist ein mobiles Gerät | `device.isMobileDevice` |
| Gerätemodell | `device.model` |
| Benutzeragent | `environment.browserDetails.userAgent` |
| Betriebssystem | `environment.operatingSystem` |
| Journey-ID | `_experience.journeyOrchestration.stepEvents.journeyID` |
| Knoten-ID | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### E-Mail angeklickt

Dieses Ereignis verfolgt, wann eine Person auf einen Link in einer Marketing-E-Mail geklickt hat.

Ereignistyp: `directMarketing.emailClicked`

+++Felder

| Feld | Feldtyp |
| ----- | ---------- |
| Kennung | `_id` |
| Ereignistyp | `eventType` |
| Zeitstempel | `timestamp` |
| Personen-ID | `personID` |
| Personen-Quell-ID | `personKey.sourceID` |
| Quelltyp der Person | `personKey.sourceType` |
| ID der Quellinstanz der Person | `personKey.sourceInstanceID` |
| Ursprungsschlüssel der Person | `personKey.sourceKey` |
| Mailingquellen-ID | `directMarketing.mailingKey.sourceID` |
| Quelltyp der E-Mail | `directMarketing.mailingKey.sourceType` |
| Quellinstanz-ID wird gesendet | `directMarketing.mailingKey.sourceInstanceID` |
| Quellschlüssel der E-Mail-Adresse | `directMarketing.mailingKey.sourceKey` |
| Mailing-Name | `directMarketing.mailingName` |
| Link-URL | `directMarketing.linkURL` |
| Ist ein mobiles Gerät | `device.isMobileDevice` |
| Modell | `device.model` |
| Benutzeragent | `environment.browserDetails.userAgent` |
| Betriebssystem | `environment.operatingSystem` |
| Journey-ID | `_experience.journeyOrchestration.stepEvents.journeyID` |
| Knoten-ID | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### E-Mail aufgrund eines Bounce-Ereignisses unzustellbar

Dieses Ereignis verfolgt, wann eine E-Mail an eine Person gebounct hat.

Ereignistyp: `directMarketing.emailBounced`

+++Felder

| Feld | Feldtyp |
| ----- | ---------- |
| Kennung | `_id` |
| Ereignistyp | `eventType` |
| Zeitstempel | `timestamp` |
| Personen-ID | `personID` |
| Personen-Quell-ID | `personKey.sourceID` |
| Quelltyp der Person | `personKey.sourceType` |
| ID der Quellinstanz der Person | `personKey.sourceInstanceID` |
| Ursprungsschlüssel der Person | `personKey.sourceKey` |
| Mailingquellen-ID | `directMarketing.mailingKey.sourceID` |
| Quelltyp der E-Mail | `directMarketing.mailingKey.sourceType` |
| Quellinstanz-ID wird gesendet | `directMarketing.mailingKey.sourceInstanceID` |
| Quellschlüssel der E-Mail-Adresse | `directMarketing.mailingKey.sourceKey` |
| Mailing-Name | `directMarketing.mailingName` |
| E-Mail | `directMarketing.email` |
| E-Mail-Bounce-Code | `directMarketing.emailBouncedCode` |
| E-Mail-Bounce-Details | `directMarketing.emailBouncedDetails` |
| Journey-ID | `_experience.journeyOrchestration.stepEvents.journeyID` |
| Knoten-ID | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### E-Mail nicht zugestellt (Soft Bounce)

Dieses Ereignis verfolgt, wann eine E-Mail an eine Person Softbounce erzeugt.

Ereignistyp: `directMarketing.emailBouncedSoft`

+++Felder

| Feld | Feldtyp |
| ----- | ---------- |
| Kennung | `_id` |
| Ereignistyp | `eventType` |
| Zeitstempel | `timestamp` |
| Personen-ID | `personID` |
| Personen-Quell-ID | `personKey.sourceID` |
| Quelltyp der Person | `personKey.sourceType` |
| ID der Quellinstanz der Person | `personKey.sourceInstanceID` |
| Ursprungsschlüssel der Person | `personKey.sourceKey` |
| Mailingquellen-ID | `directMarketing.mailingKey.sourceID` |
| Quelltyp der E-Mail | `directMarketing.mailingKey.sourceType` |
| Quellinstanz-ID wird gesendet | `directMarketing.mailingKey.sourceInstanceID` |
| Quellschlüssel der E-Mail-Adresse | `directMarketing.mailingKey.sourceKey` |
| Mailing-Name | `directMarketing.mailingName` |
| E-Mail | `directMarketing.email` |
| E-Mail-Bounce-Code | `directMarketing.emailBouncedCode` |
| E-Mail-Bounce-Details | `directMarketing.emailBouncedDetails` |
| Journey-ID | `_experience.journeyOrchestration.stepEvents.journeyID` |
| Knoten-ID | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### E-Mail abbestellt

Dieses Ereignis verfolgt, wann eine Person sich von einer Marketing-E-Mail abgemeldet hat.

Ereignistyp: `directMarketing.emailUnsubscribed `

+++Felder

| Feld | Feldtyp |
| ----- | ---------- |
| Kennung | `_id` |
| Ereignistyp | `eventType` |
| Zeitstempel | `timestamp` |
| Personen-ID | `personID` |
| Personen-Quell-ID | `personKey.sourceID` |
| Quelltyp der Person | `personKey.sourceType` |
| ID der Quellinstanz der Person | `personKey.sourceInstanceID` |
| Ursprungsschlüssel der Person | `personKey.sourceKey` |
| Mailingquellen-ID | `directMarketing.mailingKey.sourceID` |
| Quelltyp der E-Mail | `directMarketing.mailingKey.sourceType` |
| Quellinstanz-ID wird gesendet | `directMarketing.mailingKey.sourceInstanceID` |
| Quellschlüssel der E-Mail-Adresse | `directMarketing.mailingKey.sourceKey` |
| Mailing-Name | `directMarketing.mailingName` |
| Journey-ID | `_experience.journeyOrchestration.stepEvents.journeyID` |
| Knoten-ID | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### Seitenbesuch

Dieser Ereignistyp ist die Standardmethode zum Markieren des Treffers als Seitenansicht.

Ereignistyp: `web.webpagedetails.pageViews`

+++Felder

| Feld | Feldtyp |
| ----- | ---------- |
| Kennung | `_id` |
| Ereignistyp | `eventType` |
| Zeitstempel | `timestamp` |
| Personen-ID | `personID` |
| Personen-Quell-ID | `personKey.sourceID` |
| Quelltyp der Person | `personKey.sourceType` |
| ID der Quellinstanz der Person | `personKey.sourceInstanceID` |
| Ursprungsschlüssel der Person | `personKey.sourceKey` |
| Quellkennung der Webseite | `web.webPageDetails.webPageKey.sourceID` |
| Quelltyp der Web-Seite | `web.webPageDetails.webPageKey.sourceType` |
| Quellinstanz-ID der Web-Seite | `web.webPageDetails.webPageKey.sourceInstanceID` |
| Quellschlüssel der Webseite | `web.webPageDetails.webPageKey.sourceKey` |
| Name der Web-Seite | `web.webPageDetails.name` |
| Web-Seiten-URL | `web.webPageDetails.URL` |
| Web-Seiten-Abfrageparameter | `web.webPageDetails.queryParameters` |
| Webseiten-ID | `web.webPageDetails.webPageID` |
| Benutzeragent | `environment.browserDetails.userAgent` |
| Referrer-URL | `web.webReferrer.URL` |

+++

### Formular ausgefüllt

Dieses Ereignis verfolgt, wann eine Person ein Formular auf einer Web-Seite ausgefüllt hat.

Ereignistyp: `web.formFilledOut`

+++Felder

| Feld | Feldtyp |
| ----- | ---------- |
| Kennung | `_id` |
| Ereignistyp | `eventType` |
| Zeitstempel | `timestamp` |
| Personen-ID | `personID` |
| Personen-Quell-ID | `personKey.sourceID` |
| Quelltyp der Person | `personKey.sourceType` |
| ID der Quellinstanz der Person | `personKey.sourceInstanceID` |
| Ursprungsschlüssel der Person | `personKey.sourceKey` |
| Quellkennung des Webformulars | `web.fillOutForm.webFormKey.sourceID` |
| Quelltyp des Web-Formulars | `web.fillOutForm.webFormKey.sourceType` |
| Quellinstanz-ID des Web-Formulars | `web.fillOutForm.webFormKey.sourceInstanceID` |
| Quellschlüssel des Web-Formulars | `web.fillOutForm.webFormKey.sourceKey` |
| Web-Formular-ID | `web.fillOutForm.webFormID` |
| Name des Web-Formulars | `web.fillOutForm.webFormName` |
| Web-Seiten-Abfrageparameter | `web.webPageDetails.queryParameters` |
| Webseiten-ID | `web.webPageDetails.webPageID` |
| Benutzeragent | `environment.browserDetails.userAgent` |
| Referrer-URL | `web.webReferrer.URL` |

+++

### Weblink angeklickt

Das Ereignis signalisiert, dass die Web-SDK automatisch einen Link-Klick aufgezeichnet hat.

Ereignistyp: `web.webinteraction.linkClicks`

+++Felder

| Feld | Feldtyp |
| ----- | ---------- |
| Kennung | `_id` |
| Ereignistyp | `eventType` |
| Zeitstempel | `timestamp` |
| Personen-ID | `personID` |
| Personen-Quell-ID | `personKey.sourceID` |
| Quelltyp der Person | `personKey.sourceType` |
| ID der Quellinstanz der Person | `personKey.sourceInstanceID` |
| Ursprungsschlüssel der Person | `personKey.sourceKey` |
| Quell-ID der Web-Interaktion | `web.webInteraction.webInteractionKey.sourceID` |
| Quelltyp für Web-Interaktion | `web.webInteraction.webInteractionKey.sourceType` |
| Quellinstanz-ID für Web-Interaktion | `web.webInteraction.webInteractionKey.sourceInstanceID` |
| Quellschlüssel der Web-Interaktion | `web.webInteraction.webInteractionKey.sourceKey` |
| Webinteraktions-Link-ID | `web.webInteraction.linkID` |
| Web Interaction Link URL | `web.webInteraction.linkURL` |
| Web-Seiten-Abfrageparameter | `web.webPageDetails.queryParameters` |
| Webseiten-ID | `web.webPageDetails.webPageID` |
| Benutzeragent | `environment.browserDetails.userAgent` |
| Referrer-URL | `web.webReferrer.URL` |

+++

### Interessanter Moment

Dieses Ereignis verfolgt, wann ein interessanter Moment für eine Person aufgezeichnet wurde.

Ereignistyp: `leadOperation.interestingMoment `

+++Felder

| Feld | Feldtyp |
| ----- | ---------- |
| Kennung | `_id` |
| Ereignistyp | `eventType` |
| Zeitstempel | `timestamp` |
| Personen-ID | `personID` |
| Personen-Quell-ID | `personKey.sourceID` |
| Quelltyp der Person | `personKey.sourceType` |
| ID der Quellinstanz der Person | `personKey.sourceInstanceID` |
| Ursprungsschlüssel der Person | `personKey.sourceKey` |
| Datum des Augenblicks | `leadOperation.interestingMoment.date` |
| Momentenbeschreibung | `leadOperation.interestingMoment.description` |
| Momentquelle | `leadOperation.interestingMoment.source` |
| Momenttyp | `leadOperation.interestingMoment.type` |
| Journey-ID | `_experience.journeyOrchestration.stepEvents.journeyID` |
| Knoten-ID | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

<!-- ## Overview video

>[!VIDEO](https://video.tv.adobe.com/v/3448692/?captions=ger&learn=on) -->