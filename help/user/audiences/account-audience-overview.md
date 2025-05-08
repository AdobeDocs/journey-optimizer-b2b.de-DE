---
title: Konto-Zielgruppen
description: Erfahren Sie mehr über Kontozielgruppen und darüber, wie sie Account-basierte Journeys aktivieren.
exl-id: f9ba690f-bab2-4c31-9000-f0be1342c8b3
source-git-commit: 9031191ead88652df95137a122f379b0ae2516a7
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 100%

---

# Konto-Zielgruppen

Eine Zielgruppe ist eine Gruppe von Personen, die ähnliche Verhaltensweisen und/oder Merkmale aufweisen. Journey Optimizer B2B Edition verwendet die Kontosegmentierungsfunktionen der B2B- und B2P-Editionen von Adobe Real-Time Customer Data Platform. Mit der Kontosegmentierung können Benutzende Kontozielgruppen generieren, indem sie Daten aus jeder B2B-Entität im System nutzen. Diese Kontozielgruppen dienen als Eingaben für die Konto-Journeys von Journey Optimizer B2B Edition und erleichtern die Fähigkeit zur nahtlosen Aktivierung und Personalisierung.

Weitere Informationen zu Kontozielgruppen und deren Definition finden Sie in der [Dokumentation zum Segmentierungs-Service von Adobe Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/types/account-audiences){target="_blank"}.

## Kontozielgruppen-Workflow

Sie können sich Journey Optimizer B2B Edition als ein Experience Platform(AEP)-Ziel vorstellen, das nicht im Zielkatalog angezeigt wird. Aktivieren Sie Kontozielgruppen für Journey Optimizer B2B Edition mithilfe der folgenden Schritte:

1. Erstellen von Schemata für Ihre Daten in AEP.
1. Aufnehmen Ihrer Daten in AEP.
1. Erstellen eines Kontosegments zur Auswertung Ihrer Daten.
1. Aktivieren der ausgewerteten Daten für Journey Optimizer B2B Edition.

In Journey Optimizer B2B Edition werden Kontozielgruppen als Eingabe für kontobasierte Journeys verwendet, sodass Sie die Personen in diesen Konten ansprechen können. Sie können beispielsweise Kontozielgruppen verwenden, um Datensätze aller Konten abzurufen, die keine Kontaktinformationen für Personen mit dem Titel Chief Operating Officer (COO) oder Chief Marketing Officer (CMO) haben.

Mit Journey Optimizer B2B Edition können Sie Adobe Experience Platform(AEP)-Kontozielgruppen direkt über die linke Navigationsleiste erstellen und sie in Ihre Konto-Journeys integrieren.

![Auf Kontozielgruppen zugreifen](./assets/account-audiences-browse.png){width="800" zoomable="yes"}

## Erstellen einer Kontozielgruppe

Definieren Sie die Kontozielgruppe, indem Sie eine Kontosegmentierung erstellen. Sie können die Kontosegmentierung direkt in der Journey Optimizer B2B Edition-Anwendung erstellen oder die [Benutzeroberfläche von Segment Builder](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/ui/segment-builder){target="_blank"} verwenden. Im Folgenden finden Sie die Schritte, die Sie zum Erstellen einer Kontosegmentierung in Journey Optimizer B2B Edition verwenden können.

1. Wählen Sie in der linken Navigation **[!UICONTROL Konten]** > **[!UICONTROL Zielgruppen]** aus.

1. Klicken Sie oben rechts auf **[!UICONTROL Zielgruppe erstellen]**.

1. Erstellen Sie die Segmentdefinition.

   Die Kontoattribute und Zielgruppen werden in der linken Navigationsleiste angezeigt. Auf der Registerkarte _[!UICONTROL Attribute]_ können Sie sowohl von Platform erstellte als auch benutzerdefinierte Attribute hinzufügen. Ziehen Sie jedes Attribut, um die Logik für das Segment zu erstellen.

   >[!TIP]
   >
   >Beachten Sie beim Erstellen einer Kontozielgruppe, dass Ereignisse unter _[!UICONTROL Personen]_ aufgeführt werden, da diese Attribute mit Personen verknüpft sind.<br/>
   >
   >Auf der Registerkarte _[!UICONTROL Zielgruppen]_ können Sie zuvor erstellte personenbasierte Zielgruppen hinzufügen, auf die Sie bei der Erstellung Ihrer eigenen Kontozielgruppe aufbauen können.

   Im folgenden Beispiel wird eine mit `Country Code`, `Revenue Amount` und `Market segment` erstellte Zielgruppe definiert. Die englischsprachige Abfrage lautet: „I want all accounts in the US who are in the Finance Segment whose revenue exceeds $1M.“

   ![Beispiel für Kontozielgruppensegment-Builder](./assets/audience-segment-builder-US-finance-1M.png){width="700" zoomable="yes"}
   <br/>

   >[!IMPORTANT]
   >
   >Das Attribut `Account Name` für Kontodatensätze muss einen Wert enthalten, der in Konto-Journeys aufgenommen werden soll. Wenn dieses Attribut leer (null) ist, wird der Kontodatensatz ausgeschlossen.<br/>
   >Um sicherzustellen, dass nur Konten mit einem nicht leeren Kontonamen enthalten sind, fügen Sie das Attribut **[!UICONTROL Kontoname]** hinzu und wählen Sie _[!UICONTROL Vorhanden]_ als Übereinstimmungsbedingung aus.<br/>
   >![Das Attribut „Kontoname“ ist vorhanden](./assets/audience-segment-builder-account-name-exists.png){width="600"}
   ><br/>Wenn Sie ein benutzerdefiniertes Attribut als Kontonamen verwenden, verwenden Sie den Namen des benutzerdefinierten Attributs anstelle von _[!UICONTROL Kontoname]_.

1. Klicken Sie oben rechts auf **[!UICONTROL Speichern und schließen]**.

Um Ihre Kontozielgruppe für Journey Optimizer B2B Edition zu aktivieren, müssen Sie [sie zu einer Konto-Journey hinzufügen](../journeys/journey-overview.md#add-the-account-audience-for-your-journey) und [die Journey veröffentlichen](../journeys/journey-overview.md).
