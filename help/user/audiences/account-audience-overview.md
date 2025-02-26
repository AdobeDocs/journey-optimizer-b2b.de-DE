---
title: Konto-Zielgruppen
description: Erfahren Sie mehr über Account-Zielgruppen und wie sie Account-basierte Journey aktivieren.
exl-id: f9ba690f-bab2-4c31-9000-f0be1342c8b3
source-git-commit: b6b26d9cb79926577ed7fc4ed50c094986796505
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 2%

---

# Konto-Zielgruppen

Eine Zielgruppe ist eine Gruppe von Personen, die ähnliche Verhaltensweisen und/oder Merkmale aufweisen. Journey Optimizer B2B edition verwendet die Kontosegmentierungsfunktionen von Adobe Real-Time Customer Data Platform B2B- und B2P-Editionen. Mit der Kontosegmentierung können Benutzer Account-Zielgruppen generieren, indem sie Daten aus jeder B2B-Entität im System nutzen. Diese Account-Zielgruppen dienen als Eingaben für die Account-Journey von Journey Optimizer B2B edition und erleichtern die nahtlose Aktivierung und Personalisierung.

Weitere Informationen zu Konto-Zielgruppen und deren Definition finden Sie in der Dokumentation zum [Adobe Experience Platform Segmentation Service](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/types/account-audiences).

## Workflow für Konto-Zielgruppe

Sie können sich Journey Optimizer B2B edition als Experience Platform-Ziel (AEP) vorstellen, das nicht im Zielkatalog angezeigt wird. Aktivieren Sie Konto-Zielgruppen für Journey Optimizer B2B edition mithilfe der folgenden Schritte:

1. Erstellen Sie Schemata für Ihre Daten in AEP.
1. Nehmen Sie Ihre Daten in AEP auf.
1. Erstellen Sie ein Kontosegment, um Ihre Daten auszuwerten.
1. Aktivieren Sie die ausgewerteten Daten für Journey Optimizer B2B edition.

In Journey Optimizer B2B edition werden Account-Zielgruppen als Eingabe für Account-basierte Journey verwendet, sodass Sie die Personen in diesen Accounts ansprechen können. Beispielsweise können Sie Account-Zielgruppen verwenden, um Datensätze aller Konten abzurufen, die keine Kontaktinformationen für Personen mit dem Titel Chief Operating Officer (COO) oder Chief Marketing Officer (CMO) haben.

Mit Journey Optimizer B2B edition können Sie Adobe Experience Platform (AEP)-Konto-Zielgruppen direkt über die linke Navigationsleiste erstellen und sie in Ihre Account-Journey integrieren.

![Zugriff auf Konto-Zielgruppen](./assets/account-audiences-browse.png){width="800" zoomable="yes"}

## Konto-Zielgruppe erstellen

Definieren Sie die Konto-Zielgruppe, indem Sie eine Kontosegmentierung erstellen. Sie haben die Möglichkeit, die Kontosegmentierung direkt in der Journey Optimizer B2B edition-Anwendung zu erstellen oder die [Segment Builder-Benutzeroberfläche) ](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder). Im Folgenden finden Sie die Schritte, die Sie zum Erstellen einer Kontosegmentierung in Journey Optimizer B2B edition verwenden können.

1. Wählen Sie in der linken Navigation **[!UICONTROL Konten]** > **[!UICONTROL Zielgruppen]** aus.

1. Klicken **[!UICONTROL oben]** auf „Zielgruppe erstellen“.

1. Erstellen Sie die Segmentdefinition.

   Die Kontoattribute und Zielgruppen werden in der linken Navigationsleiste angezeigt. Auf der Registerkarte _[!UICONTROL Attribute]_ können Sie sowohl von Platform erstellte als auch benutzerdefinierte Attribute hinzufügen. Ziehen Sie jedes Attribut, um die Logik für das Segment zu erstellen.

   >[!TIP]
   >
   >Beachten Sie beim Erstellen einer Konto-Zielgruppe, dass Ereignisse unter _[!UICONTROL Personen]_ aufgeführt werden, da diese Attribute mit Personen verknüpft sind.<br/>
   >
   >Auf der Registerkarte _[!UICONTROL Zielgruppen]_ können Sie zuvor erstellte personenbasierte Zielgruppen hinzufügen, auf die Sie bei der Erstellung Ihrer eigenen Konto-Zielgruppe aufbauen können.

   Im folgenden Beispiel wird eine mit `Country Code`, `Revenue Amount` und `Market segment` erstellte Zielgruppe definiert. Die englischsprachige Abfrage lautet: „I want all accounts in the US who are in the Finance Segment their Revenue above $1M.“

   ![Beispiel für Account Audience Segment Builder](./assets/audience-segment-builder-US-finance-1M.png){width="700" zoomable="yes"}
   <br/>

   >[!IMPORTANT]
   >
   >Das `Account Name` für Kontoeinträge muss einen Wert enthalten, der in die Journey des Kontos aufgenommen werden soll. Wenn dieses Attribut leer (null) ist, wird der Kontodatensatz ausgeschlossen.<br/>
   >Um sicherzustellen, dass nur Konten mit einem nicht leeren Kontonamen enthalten sind, fügen Sie das Attribut **[!UICONTROL Kontoname]** hinzu und wählen Sie _[!UICONTROL vorhanden]_ als Übereinstimmungsbedingung aus<br/>
   >![Das Attribut „Kontoname“ ist vorhanden](./assets/audience-segment-builder-account-name-exists.png){width="600"}
   ><br/>Wenn Sie ein benutzerdefiniertes Attribut als Kontonamen verwenden, verwenden Sie den benutzerdefinierten Attributnamen anstelle von _[!UICONTROL Kontoname]_.

1. Klicken **[!UICONTROL oben]** auf „Speichern und schließen“.

Um Ihre Konto-Zielgruppe für Journey Optimizer B2B edition zu aktivieren, müssen Sie [sie zu einer Konto-Journey hinzufügen](../journeys/journey-overview.md#add-the-account-audience-for-your-journey) und [die Journey veröffentlichen](../journeys/journey-overview.md).
