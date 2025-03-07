---
title: Aktion ausführen
description: Erfahren Sie mehr über den Knotentyp Aktion ausführen , den Sie zur Orchestrierung Ihrer Account-Journey in Journey Optimizer B2B edition verwenden können.
feature: Account Journeys
exl-id: 167cb627-96ee-42a8-8657-bb8040bb4bfe
source-git-commit: 632eee973730f527ea0314c6affe5a49a72e3945
workflow-type: tm+mt
source-wordcount: '1200'
ht-degree: 1%

---

# Aktion ausführen

Auf Ihrer Konto-Journey können Sie einen Knoten _[!UICONTROL Aktion ausführen]_ hinzufügen, um eine Aktion auszuführen, z. B. eine E-Mail senden, einen Punktewert ändern, einer Einkaufsgruppe zuweisen usw. Aktionen sind in der Regel das, was infolge eines Triggers geschehen soll, z. B. eines Ereignisses oder einer vorherigen Aktion.

![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Übersichtsvideo ansehen](#overview-video)

## Kontoaktionen

Verwenden Sie eine Aktion für Konten, wenn Sie eine Änderung auf alle Personen anwenden möchten, die Teil von Konten im Knotenpfad sind.

### Aktionen und Einschränkungen {#account-action-constraints}

| Aktion | Begrenzungen |
| ------ | ----------- |
| [!UICONTROL Datenwert der Kontoänderung] | Attribut/<br/> Wert auswählen |
| [!UICONTROL Interessanter Moment des Kontos] | Typ (E-Mail, Meilenstein oder Web)<br/>Beschreibung (optional) |
| [!UICONTROL Konto zu (anderem) Journey hinzufügen] | Live-Konto-Journey auswählen |
| [!UICONTROL Zur Kontoliste hinzufügen] | Live-Liste statischer Konten auswählen |
| [!UICONTROL Konto von Journey entfernen] | Live-Konto-Journey auswählen |
| [!UICONTROL Aus der Kontenliste entfernen] | Live-Liste statischer Konten auswählen |
| [!UICONTROL Verkaufswarnung senden] | Lösungsinteresse auswählen<br/> E-Mail senden an |
| [!UICONTROL Phase der Einkaufsgruppe aktualisieren] | Lösungsinteresse auswählen<br/>Einkaufsgruppenstufe auswählen |
| [!UICONTROL Status der Einkaufsgruppe aktualisieren] | Lösungsinteresse/<br/> auswählen (erforderlich, max. 50 Zeichen) |

### Hinzufügen einer kontobasierten Aktion

1. Navigieren Sie zum Journey-Editor.

1. Klicken Sie auf das Pluszeichen ( **+** ) auf einem Pfad und wählen Sie **[!UICONTROL Aktion ausführen]**.

   ![Journey-Knoten hinzufügen - eine Aktion ausführen](./assets/add-node-action.png){width="400"}

1. Wählen Sie in den Knoteneigenschaften auf der rechten Seite **[!UICONTROL Konten]** für die Aktion aus.

1. Wählen Sie eine Aktion aus der Liste aus und legen Sie beliebige Werte für die Aktion fest.

   ![Journey-Knoten - Aktion für ein Konto durchführen](./assets/node-take-action-account.png){width="700" zoomable="yes"}

## Personenaktionen

Verwenden Sie eine Aktion für Personen, wenn Sie eine Änderung auf alle Personen im Knotenpfad anwenden möchten. Dieser Knotentyp kann im Aufspaltungspfad nach Personen oder im Aufspaltungspfad nach Konten verwendet werden.

### Aktionen und Einschränkungen {#people-action-constraints}

| Kontext | Aktion | Begrenzungen |
| ------- | ------ | ----------- |
| [Journey Optimizer B2B](#journey-optimizer-b2b-actions) | [!UICONTROL Hinzufügen zur externen Kundenzielgruppe] | Externe Kundenzielgruppe auswählen |
| | [!UICONTROL Der Einkaufsgruppe zuweisen] | Lösungsinteresse auswählen<br/>Rolle auswählen |
| | [!UICONTROL Ändern des Datenwerts] | Personenattribut auswählen<br/>neuen Wert festlegen |
| | [!UICONTROL Punktzahl ändern] | Score-Name<br/>Änderung des Score |
| | [!UICONTROL Interessanter Moment der Person] | type<br/>description |
| | [!UICONTROL Aus Einkaufsgruppe entfernen] | Interesse an der Lösung auswählen |
| | [!UICONTROL E-Mail senden] | Neue E-Mail erstellen<br/>E-Mail aus Marketo Engage auswählen |
| | [!UICONTROL SMS senden] | SMS erstellen |
| [Marketo Engage](#marketo-engage-actions) | [!UICONTROL Zu Liste hinzufügen] | Marketo Engage workspace<br/>list name auswählen |
| | [!UICONTROL Zur Marketo Engage-Anfragekampagne hinzufügen] | Marketo Engage Workspace auswählen<br/>Kampagne anfordern auswählen |
| | [!UICONTROL Ändern der Personenpartition in Marketo Engage] | Neue Partition |
| | [!UICONTROL Aus Liste entfernen] | Marketo Engage workspace<br/>list name auswählen |

### Hinzufügen einer personenbasierten Aktion

1. Navigieren Sie zum Journey-Editor.

1. Klicken Sie auf das Pluszeichen ( **+** ) auf einem Pfad und wählen Sie **[!UICONTROL Aktion ausführen]**.

1. Wählen Sie in den Knoteneigenschaften auf der rechten Seite **[!UICONTROL Personen]** für die Aktion aus.

1. Wählen Sie eine Aktion aus der Liste aus und legen Sie beliebige Werte für die Aktion fest.

![Journey-Knoten - Eine Aktion auf Personen durchführen](./assets/node-take-action-people.png){width="700" zoomable="yes"}

### Journey Optimizer B2B-Aktionen

Die personenbasierten Aktionen von Journey Optimizer B2B dienen der Verwaltung der Kommunikation über die konfigurierten Kanäle und der Kategorisierung von Personen in Ihren Einkaufsgruppen und Konten. Der Journey wendet die Aktion an, wenn ein qualifizierendes Konto mit Personenprofilen den Knoten erreicht.

+++[!UICONTROL Hinzufügen zur externen Kundenzielgruppe]

Verwenden Sie diese Aktion, um Personen zu einer externen Zielgruppe zu pushen, die über einen bezahlten Medienkanal aktiviert werden kann, um Mitglieder von Einkaufsgruppen weiter anzusprechen. Diese Aktion wird über Real-Time CDP B2B/P Edition ausgeführt.

>[!NOTE]
>
>Wenn ein qualifizierendes Konto mit Personenprofilen den Knoten _Zu externer Kundenzielgruppe hinzufügen_ in einer veröffentlichten Journey erreicht, kann es bis zu 48 Stunden dauern, bis diese Profile in der externen Zielgruppe ausgefüllt sind.

![Aktion durchführen - Hinzufügen zu einer externen Kundenzielgruppe](./assets/node-action-add-to-external-audience-options.png){width="300"}

Wenn Sie diese personenbasierte Aktion auswählen, können Sie eine neue externe Zielgruppe erstellen oder aus einer vorhandenen externen Zielgruppe auswählen. Bei bestehenden Zielgruppen können Sie aus externen Kundenzielgruppen wählen, die nur in Journey Optimizer B2B edition erstellt wurden. Wenn Sie eine Zielgruppe erstellen und für diese Journey-Aktion verwenden, stellen Sie sicher, dass Sie eine Verbindung mit dem Ziel herstellen. Weitere Informationen finden Sie unter [Erstellen einer neuen Zielverbindung](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/connect-destination){target="_blank"} und [Aktivierung - Übersicht](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activation-overview#activate-audiences-from-the-destinations-catalog){target="_blank"} in der Dokumentation zu Experience Platform.

![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Videoübersicht über die Orchestrierung bezahlter Medien ansehen](../data/linkedin-account-matched-audiences.md#orchestrate-paid-media-engagement)

_So erstellen Sie eine externe Zielgruppe:_

1. Wählen Sie **[!UICONTROL Neu erstellen]**.

1. Klicken Sie **[!UICONTROL Externe Kundenzielgruppe erstellen]**.

1. Geben Sie **[!UICONTROL Name]** (erforderlich) und **[!UICONTROL Beschreibung]** (optional) für die neue externe Zielgruppe ein.

   ![Hinzufügen zur externen Kundenzielgruppe - Zielgruppe erstellen](./assets/node-action-add-to-external-create-new.png){width="300"}

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

   Das System erstellt die neue Zielgruppe und zeigt eine Bestätigungsmeldung an. Anschließend können Sie sie als vorhandene Zielgruppe für die Knotenaktion verwenden.

_So verwenden Sie eine vorhandene Zielgruppe:_

1. Klicken Sie **[!UICONTROL Externe Kundenzielgruppe auswählen]**.

1. Wählen Sie im Dialogfeld die Zielgruppe aus, die Sie verwenden möchten.

   ![Hinzufügen zur externen Kundenzielgruppe - Zielgruppe hinzufügen](./assets/node-action-add-to-external-audience-select.png){width="700" zoomable="yes"}

1. Klicken Sie **[!UICONTROL Zielgruppe hinzufügen]**.

+++

+++[!UICONTROL Der Einkaufsgruppe zuweisen]

Verwenden Sie diese Aktion, um Personenprofile basierend auf einem ausgewählten [ und einer ausgewählten Rolle ](../buying-groups/buying-groups-overview.md) einer Kaufgruppe hinzuzufügen.

![Aktion ausführen - Zu Einkaufsgruppe hinzufügen](./assets/node-action-add-to-buying-group.png){width="300"}

+++

+++[!UICONTROL Ändern des Datenwerts]

Verwenden Sie diese Aktion, um den Wert eines „Personenprofilattributs[ zu ](../data/field-mapping.md#xdm-business-person-attributes). Wählen Sie das Attribut aus und legen Sie dann den neuen Wert fest.

![Aktion ausführen - Datenwert ändern](./assets/node-action-change-data-value.png){width="300"}

+++

+++[!UICONTROL Punktzahl ändern]

Verwenden Sie diese Aktion, um die Punktzahl der Person in Marketo Engage zu ändern. [Weitere Informationen](https://experienceleague.adobe.com/en/docs/marketo-learn/tutorials/lead-and-data-management/lead-scoring-learn){target="_blank"}

![Aktion ausführen - Punktzahl ändern](./assets/node-action-change-score.png){width="300"}

+++

+++[!UICONTROL Interessanter Moment der Person]

Verwenden Sie diese Aktion, um einen interessanten Moment für Personenprofile zu protokollieren. Wählen Sie einen Typ aus (E-Mail, Meilenstein oder Web) und fügen Sie eine Beschreibung hinzu (optional).

![Aktion durchführen - interessante Person-Momente](./assets/node-action-person-interesting-moment.png){width="300"}

+++

+++[!UICONTROL Aus Einkaufsgruppe entfernen]

Verwenden Sie diese Aktion, um Personenprofile aus einer [Einkaufsgruppe“ ](../buying-groups/buying-groups-overview.md) Grundlage eines ausgewählten Lösungsinteresses zu entfernen.

![Aktion ausführen - Zu Einkaufsgruppe hinzufügen](./assets/node-action-remove-from-buying-group.png){width="300"}

+++

+++[!UICONTROL E-Mail senden]

Verwenden Sie diese Aktion, um eine E-Mail zu senden. Sie können E-Mail-Nachrichten im visuellen Designer erstellen, personalisieren und in der Vorschau anzeigen (siehe [E-Mail-Authoring](../content/email-authoring.md)). Sie können auch eine (E[Mail von Marketo Engage aus) ](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/general/creating-an-email/create-an-email){target="_blank"}. Wählen Sie den Marketo Engage-Arbeitsbereich und dann die zu sendende E-Mail aus.

![Aktion durchführen - E-Mail senden](./assets/node-action-send-email-from-marketo.png){width="300"}

+++

+++[!UICONTROL SMS senden]

Verwenden Sie diese Aktion, um eine SMS-Nachricht zu senden. Sie können SMS-Nachrichten im visuellen Designer erstellen, personalisieren und in der Vorschau anzeigen (siehe [SMS-Authoring](../content/sms-authoring.md)).

![Aktion ausführen - SMS senden](./assets/node-action-send-sms.png){width="300"}

+++

### Marketo Engage-Aktionen

Die personenbasierten Marketo Engage-Angebote sind so konzipiert, dass sie Ihre kontobasierte Marketing-Orchestrierung in Journey Optimizer B2B edition mit Ihren Lead-basierten Marketing-Maßnahmen in Marketo Engage koordinieren. Verwenden Sie diese Aktionen, um Listen-Mitgliedschaften, Personenpartitionen und Anfragekampagnen zu orchestrieren.

+++[!UICONTROL Zu Liste hinzufügen]

Mit dieser Aktion können Sie Personen aus einer [Smart List](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/understanding-smart-lists){target="_blank"} in Marketo Engage entfernen.

Wählen Sie zunächst den Arbeitsbereich in der verbundenen Marketo Engage-Instanz aus. Wählen Sie anschließend den Listennamen aus.

![Aktion ausführen - Zu Liste hinzufügen](./assets/node-action-add-to-list-options.png){width="300"}

+++

+++[!UICONTROL Zur Marketo-Anfragekampagne hinzufügen]

Verwenden Sie diese Aktion, um Personenprofile zu einer [Anfragekampagne](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/flow-actions/request-campaign){target="_blank"} in Marketo Engage hinzuzufügen.

Wählen Sie zunächst den Arbeitsbereich in der verbundenen Marketo Engage-Instanz aus. Wählen Sie als Nächstes den Namen der Anfragekampagne aus.

![Aktion ausführen - Zur Marketo-Anfragekampagne hinzufügen](./assets/node-action-add-to-request-campaign-options.png){width="300"}

+++

+++[!UICONTROL Ändern der Personenpartition in Marketo Engage]

Verwenden Sie diese Aktion, um die [Personenpartition](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/workspaces-and-person-partitions/understanding-workspaces-and-person-partitions#person-partitions){target="_blank"} in Marketo Engage zu ändern.

![Aktion durchführen - Personenpartition in Marketo Engage ändern](./assets/node-action-change-people-partition-options.png){width="300"}

+++

+++[!UICONTROL Aus Liste entfernen]

Mit dieser Aktion können Sie Personen aus einer [Smart List](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/understanding-smart-lists){target="_blank"} in Marketo Engage entfernen. Wählen Sie zunächst den Arbeitsbereich in der verbundenen Marketo Engage-Instanz aus. Wählen Sie anschließend den Listennamen aus.

![Aktion ausführen - Aus Liste entfernen](./assets/node-action-remove-from-list-options.png){width="300"}

Wenn das Personenprofil nicht Mitglied der Smart-Liste war, wird die Aktion ignoriert.

+++

## Übersichtsvideo

>[!VIDEO](https://video.tv.adobe.com/v/3443207/?learn=on)