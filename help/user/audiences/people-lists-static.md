---
title: Listen mit statischen Personen
description: Mitglieder für statische Personenlisten in Journey Optimizer B2B Edition hinzufügen und entfernen.
feature: Audiences
role: User
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: ff2b9b37-92e0-45fc-b853-379d44c08c89
    internal-label: Audience segmentation
source-git-commit: d713d57bddf2ac6f8cf7e7a7d163281f607d729c
workflow-type: tm+mt
source-wordcount: '462'
ht-degree: 2%
---

# Listen statischer Personen

Eine statische [Personenliste](./people-lists.md) ist eine Sammlung von Personenprofilen, deren Mitgliedschaft sich nur ändert, wenn Sie Personen hinzufügen oder entfernen. Einfache Filter, die auf Personenattribute und Aktivitäten verweisen, definieren die statische Listenmitgliedschaft. Die Mitgliedschaft ändert sich nur, wenn Sie Mitglieder hinzufügen oder entfernen. Sie haben folgende Möglichkeiten:

* [Personen hinzufügen](#static-list-add-members) durch Anwenden eines Filtersatzes, der einmal ausgewertet wird, wenn Sie ihn anwenden.
* Fügen Sie Personen über ein Konto oder eine Personen-Journey hinzu oder entfernen Sie sie mithilfe der Aktionen [!UICONTROL Zu Personenliste hinzufügen] und [!UICONTROL Aus Benutzerliste entfernen]. (Siehe [Verwenden von Personenlisten in Journey](./people-lists-journeys.md))
<!-- * [Activate the list to a destination](#static-list-activate) to sync its membership downstream. -->

>[!NOTE]
>
>Statische Listenfilterdefinitionen werden nur einmal angewendet, wenn Sie Mitglieder zur Liste hinzufügen. Der definierte Filter ist danach nicht mehr verfügbar. Wenn Sie eine konsistente Zielgruppendefinition mithilfe von Filtern beibehalten möchten, verwenden Sie stattdessen eine [dynamische Liste](./people-lists-dynamic.md).

## Mitglieder hinzufügen {#static-list-add-members}

>[!NOTE]
>
>Wenn eine statische Liste leer beginnen soll, wenden Sie keine Filter an. Eine leere statische Liste ist hilfreich, wenn Sie Mitglieder über Journey hinzufügen möchten.

1. Öffnen Sie die statische Liste und klicken Sie **[!UICONTROL oben]** auf „Personen hinzufügen“.

   ![Personen zu einer statischen Personenliste hinzufügen](./assets/people-list-static-add-people.png){width="700" zoomable="yes"}

1. Definieren _[!UICONTROL im Dialogfeld „Personen]_&quot; die Regeln für das Qualifizieren von Profilen, indem Sie Filter aus dem linken Bereich ziehen.

   Profile mit einer beliebigen Kombination aus folgenden Optionen filtern:

   * Aktivitätsverlauf
   * Experience Platform-aktivierte Personenfelder
   * Benutzerdefinierte Felder
   * Absichtsdaten
   * Personenattribute
   * Spezielle Filter, z. B. Journey-Mitgliedschaft

   Die Filter sind in Kategorieordnern verschachtelt. Erweitern Sie jeden Ordner und scrollen Sie durch die verfügbaren Filter oder verwenden Sie das _Suchen_-Feld oben, um den benötigten Filter zu finden. Für jeden Filter, den Sie hinzufügen:

   * Ziehen Sie den Filter aus dem linken Bereich in den Bereich für die Filterdefinition.
   * Füllen Sie die Definition für die Übereinstimmungsbewertung aus.
   * Klicken Sie **[!UICONTROL Beschränkungen hinzufügen]**, um die entsprechenden Kriterien zu verfeinern.

   Passen Sie Ihre Bedingungen durch Anwendung der **[!UICONTROL Filterlogik]** oben an. Sie können festlegen, dass alle Bedingungen, alle Bedingungen erfüllt werden, oder eine erweiterte Logik definieren.

   ![Filter mit Einschränkungen hinzufügen, um Personen zur statischen Liste hinzuzufügen](./assets/people-list-static-add-people-filters.png){width="800" zoomable="yes"}

1. Klicken Sie **[!UICONTROL Fertig]**, um Ihre Änderungen zu speichern.

   Das System verarbeitet die Anfrage und zeigt eine Bestätigungsmeldung an, wenn Personen hinzugefügt werden. Die Verarbeitungszeit hängt von der Anzahl der auszuwertenden Personen und den von Ihnen ausgewählten Filterkriterien ab. Wenn die Liste weiter gefüllt wird, verwenden Sie **[!UICONTROL Mitglieder aktualisieren]** im Menü _[!UICONTROL Mehr]_, um die Liste zu aktualisieren.

   Qualifizierende Mitglieder werden nach kurzer Verzögerung in der Liste angezeigt. Der Filtersatz wird einmal ausgewertet, sodass Personen, die später mit den Filtern übereinstimmen, nicht automatisch hinzugefügt werden. Sie können diesen Vorgang jederzeit wiederholen, um der Liste weitere Personen hinzuzufügen.

   ![Mitglieder für eine statische Personenliste](./assets/people-list-static-members.png){width="700" zoomable="yes"}

## Mitglieder entfernen {#static-list-remove-members}

Sie können Personen mithilfe der Aktion „Aus Personenliste entfernen“ automatisch über einen Journey [!UICONTROL &#x200B; aus einer &#x200B;] entfernen. (Siehe [Verwenden von Personenlisten in Journey](./people-lists-journeys.md))

<!--
TODO: Restore this section when the activate to a destination function is released.

## Activate to a destination {#static-list-activate}

Activating a static people list sends its membership to a connected destination, with ongoing sync instead of a one-time export. This is useful for paid media targeting, suppression, and downstream orchestration.

* The static list acts as a container for the people.
* The activation sends and syncs that membership to a destination.
* People added to the list later are propagated automatically.
* People removed later are deactivated automatically.

>[!PREREQUISITES]
>
>You must have one or more configured destinations for your [!DNL Journey Optimizer B2B Edition] sandbox before you can activate a static list to a destination. See [Destinations](./destinations.md).

1. Select the **[!UICONTROL Static lists]** tab.

1. Locate the static list that you want to activate, click the _More menu_ ( **...** ) icon next to the list, and choose **[!UICONTROL Activate to destination]**.

   ![Access the More menu for a static people list](./assets/people-lists-static-more-menu.png){width="450"}

   You can also open the static list and use the **[!UICONTROL More]** menu at the top right.

1. Select the check box for the configured destination connection.

   ![Configured destinations available for activation](./assets/people-list-activate-destination-select.png){width="600" zoomable="yes"}

1. Click **[!UICONTROL Save]**.

1. In the _[!UICONTROL Activate list to destination]_ dialog, click **[!UICONTROL Activate]** to confirm.

When activation completes, a confirmation message appears and the destination shows as **[!UICONTROL Active]** on the **[!UICONTROL Destinations]** tab of the list. You can activate a static list to more than one destination at a time. Membership syncs to all of them.

To review the destinations that a static list is activated to, open the list and select the **[!UICONTROL Destinations]** tab.

### Deactivate a destination {#deactivate-destination}

Remove a destination connection from a static list when you no longer want its membership synced downstream.

1. Open the static list and select the **[!UICONTROL Destinations]** tab.

1. Use the row action to remove the destination that you want to disconnect.

1. Confirm in the _[!UICONTROL Deactivate destination]_ dialog.

Deactivating removes the destination from the list. The people in the list are also removed from the connected destination audience.

-->
