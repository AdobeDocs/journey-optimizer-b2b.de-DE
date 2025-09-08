---
title: Käufergruppen
description: Verstärken Sie das Account-Based-Marketing mit Einkaufsgruppen, um wichtige Entscheidungsträger zu identifizieren, Interaktionsbewertungen zu verfolgen und Zielkonten in Journey Optimizer B2B edition zu finden.
feature: Buying Groups
role: User
exl-id: ddcd7b62-6a76-4f5e-b6d3-a20944ca8332
source-git-commit: 6f141e08066097c3b5e991e27b6177148fad1fff
workflow-type: tm+mt
source-wordcount: '1194'
ht-degree: 73%

---


# Käufergruppen

Bei B2B-Vertriebs- und Marketing-Aktivitäten sind Konten wichtig für jede Strategie. Jedem Konto ist eine Gruppe von Personen zugeordnet, und diese Personen können Mitarbeitende des Kontos oder Auftragnehmer sein, die mit dem Konto arbeiten. Konten sind hierarchisch, und verschiedene Produkte können auf verschiedenen Ebenen in der Hierarchie verkauft werden. Adobe Experience Platform kann beispielsweise auf Unternehmensebene an einn Konto der obersten Ebene verkauft werden. Adobe Photoshop wird möglicherweise an ein Konto verkauft, das einen Geschäftsbereich oder eine Abteilung innerhalb eines Unternehmens repräsentiert, z. B. eine Design-Abteilung innerhalb eines größeren Unternehmens.

![Diagramm zu Kontorollen](assets/account-roles-diagram.png){width="800"}

Innerhalb des Kontos könnte es eine Teilmenge von Personen geben, die die _Käufergruppe_ umfassen. Dies sind die Personen, die letztendlich die Kaufentscheidung treffen. Sie benötigen daher besondere Aufmerksamkeit von der Marketing-Fachkraft und ihnen müssen möglicherweise andere Informationen bereitgestellt werden als anderen Personen, die dem Konto zugeordnet sind. Käufergruppen können unterschiedliche Personengruppen für verschiedene Produktlinien oder Angebote umfassen. Beispielsweise muss der Kauf eines Cyber-Sicherheitsprodukts in der Regel durch die oder den Chief Information Officer oder Chief Security Officer sowie eine Vertreterin oder einen Vertreter der Rechtsabteilung genehmigt werden. Bei einem Produkt zur Fehlersuche kann die Käufergruppe typischerweise die oder den VP of Engineering und die oder den IT Director umfassen.

![Video-Symbol](../../assets/do-not-localize/icon-video.svg){width="30"} [Video-Übersicht ansehen](#overview-video)

## Wichtige Komponenten

Sie können die Marketing-Effektivität steigern, indem Sie in Journey Optimizer B2B edition Einkaufsgruppen einrichten, die Mitglieder für Ihre Target-Kontolisten für die Lösungen identifizieren, für die Ihre Vertriebsteams verantwortlich sind. Bevor Sie und Ihr Marketing-Team mit der Erstellung Ihrer Käufergruppen beginnen, stellen Sie sicher, dass Sie die wichtigen Komponenten definiert haben. Diese Komponenten sind für die Erreichung Ihrer Geschäftsziele von entscheidender Bedeutung.

| Komponente | Zweck |
| --------- | ------- |
| Lösungsinteresse | Diese Komponente bietet die Antwort auf: <ul><li>Was verkaufen Sie als Marketing-Organisation?</li><li>Welches Produkt oder welche Produktkollektion möchten Sie verkaufen?</li></ul>  **Beispiel::_** Crossselling des neuen Produkts X an Bestandskundschaft |
| Kontozielgruppe | Diese Komponente bietet die Antwort auf: <ul><li>An wen verkaufen Sie?</li><li>Auf welche Kontoliste zielen Sie ab?</li></ul> **Beispiel::_** Kontosegment, das durch Konten mit Produkt Y und einem Umsatz von mehr als 1 Million definiert wird |
| Vorlagen für Käufergruppenrollen | Diese Komponente bietet die Antwort auf: <ul><li>Auf welche Rollen zielen Sie ab?</li><li>Welcher Regelsatz wird verwendet, um zu bestimmen, wer welchen Käufergruppenrollen zugewiesen wird?</li></ul>  **Beispiel::_** Zuweisen einer Person mit CMO-Titel zur Entscheidungsträger-Rolle |
| Käufergruppenphasen | (Optional) Diese Komponente bietet die Antwort auf die Frage: Wie stark ist die Käufergruppe auf Erfolg oder Misserfolg ausgerichtet? |

## Mitgliederzuweisung

Es gibt drei Möglichkeiten, wie Mitglieder einer Käufergruppe zugewiesen oder aus dieser entfernt werden. In der folgenden Liste werden diese Methoden zum Hinzufügen und Entfernen in der Reihenfolge ihrer Priorität beschrieben. Die oberste Methode hat die höchste Priorität und kann durch eine niedrigere nicht überschrieben werden.

1. **_Manuelle Aktion:_** Manuelle Aktion zum Hinzufügen oder Entfernen eines Mitglieds, die von Benutzenden aus dem Vertrieb für die Käufergruppe ausgeführt wird
2. **_Journey-Aktion:_** Journey-[Aktionsknoten für die Käufergruppenmitgliedschaft](../journeys/action-nodes.md#add-a-people-based-action) (_Der Käufergruppe zuweisen_ oder _Aus der Käufergruppe entfernen_)
3. **_Systemaufträge:_** Käufergruppen-[Erstellung](../buying-groups/buying-groups-create.md#buying-group-creation-jobs) und Wartungsaufträge.

Um zu vermeiden, dass eine Mitgliedschaftszuweisung in einer Einkaufsgruppe fälschlicherweise überschrieben wird, ist diese Liste in der Rangfolge aufgeführt, die im System befolgt wird, um eine genaue Mitgliedschaftszuweisung sicherzustellen. Wenn Benutzende aus dem Vertrieb beispielsweise der Käfergruppe manuell ein Mitglied hinzufügen, möchten sie nicht, dass dies durch einen Wartungsauftrag geändert wird. Durch Verwendung der Prioritätsrangfolge werden folgende Szenarien erzwungen:

* Wenn ein(e) Benutzende(r) ein Mitglied manuell einer Einkaufsgruppe zuweist und ihm ein Wartungsauftrag für die Einkaufsgruppe folgt, durch den dasselbe Mitglied aus der Einkaufsgruppe entfernt wird, **der Wartungsauftrag dieses** nicht entfernen und kann die manuelle Zuweisung nicht überschreiben.
* Wenn ein(e) Benutzende(r) ein Mitglied manuell einer Einkaufsgruppe zuweist und auf diesen ein ausgelöster Journey-Knoten folgt, der dasselbe Mitglied aus der Einkaufsgruppe entfernt, wird dieses Mitglied durch die Knotenaktion **nicht entfernt** und die manuelle Zuweisung kann nicht überschrieben werden.
* Wenn ein ausgelöster Journey-Aktionsknoten ein Mitglied zu einer Einkaufsgruppe hinzufügt und auf ihn ein Wartungsauftrag für eine Einkaufsgruppe folgt, der dasselbe Mitglied aus der Einkaufsgruppe entfernt, entfernt der Wartungsauftrag **dieses** nicht und kann die Journey-Aktionszuweisung nicht überschreiben.

## Käufergruppen-Workflow

1. Erstellen Sie Käufergruppen.

   * Definieren Sie [Lösungsinteresse](./solution-interests.md) und [Rollenvorlage](./buying-groups-role-templates.md)
   * [Erstellen Sie die Käufergruppe](./buying-groups-create.md#create-buying-groups) und weisen Sie [Käufergruppenphasen](./buying-group-stages.md) zu.

1. Identifizieren Sie fehlende Personen nach Vollständigkeit.

   Analysieren Sie die Käufergruppe mithilfe von Filtern.

   **_Beispiel:_** Die Entscheidungsträger-Rolle fehlt und die Vollständigkeitsbewertung ist &lt; 50

1. Vervollständigen Sie die Definitionen der Käufergruppen.
<!--
   * Acquire missing people
   * Send to LinkedIn Destination
   * Enrich with Zoominfo -->

1. Fügen Sie Ihren Konto-Journeys Käufergruppenaktionen hinzu.

## Anzeigen von Käufergruppen und Komponenten

Erweitern Sie in der linken Navigation **[!UICONTROL Konten]** und klicken Sie auf **[!UICONTROL Käufergruppen]**.

Die Seite _[!UICONTROL Käufergruppen]_ ist in Registerkarten unterteilt:

| Tab | Beschreibung |
| --- | ----------- |
| [!UICONTROL Übersicht] | Diese Registerkarte ist die Standardeinstellung und zeigt das [Käufergruppen-Dashboard](../dashboards/buying-groups-dashboard.md) an. |
| [!UICONTROL Durchsuchen] | Diese Registerkarte unterstützt die folgenden Aktivitäten: <ul><li>Liste der vorhandenen Käufergruppen anzeigen. </li><li>Nach dem Namen der Käufergruppe suchen. </li><li>Nach Lösungsinteresse filtern. </li><li>Details zur Käufergruppe aufschlüsseln. </li><li>Erstellen sie eine Käufergruppe. </li></ul> |
| [!UICONTROL Lösungsinteressen] | Diese Registerkarte unterstützt die folgenden Aktivitäten: <ul><li>Liste der vorhandenen Käufergruppen anzeigen. </li><li>Nach dem Namen der Käufergruppe suchen. </li><li>Auf Lösungsinteresseneigenschaften zugreifen und diese bearbeiten. </li><li>Lösungsinteresse erstellen. </li><li>Lösungsinteresse löschen. </li><li>Käufergruppenaufträge anzeigen und löschen. </li></ul> |
| [!UICONTROL Rollenvorlagen] | Diese Registerkarte unterstützt die folgenden Aktivitäten: <ul><li>Liste der vorhandenen Rollenvorlagen anzeigen. </li><li>Nach dem Namen der Rollenvorlage suchen. </li><li>Auf die Eigenschaften und Bedingungen von Rollenvorlagen zugreifen und diese bearbeiten. </li><li>Eine Rollenvorlage erstellen. </li><li>Eine Rollenvorlage löschen. </li></ul> |
| [!UICONTROL Stadien] | Diese Registerkarte unterstützt die folgenden Aktivitäten: <ul><li>Modell der vorhandenen Käufergruppenphasen anzeigen. </li><li>Auf den Modellentwurf der Käufergruppenphasen zugreifen und diesen bearbeiten. </li><li>Das Modell für Käufergruppenphasen erstellen. </li></ul> |

## Suchen nach und Filtern von Käufergruppen

Verwenden Sie die Registerkarte _[!UICONTROL Durchsuchen]_, um auf die Liste der Käufergruppen zuzugreifen. Sie können nach Name suchen und die Liste nach Lösungsinteressen filtern.

![Seite zum Durchsuchen der Käufergruppe](assets/buying-groups-browse.png){width="800" zoomable="yes"}

## Käufergruppendetails

Um auf die Details einer Käufergruppe zuzugreifen, klicken Sie auf der Registerkarte _[!UICONTROL Durchsuchen]_ auf den Namen der Käufergruppe. [Weitere Informationen](./buying-group-details.md)

![Details zur Käufergruppe](assets/buying-group-details.png){width="600" zoomable="yes"}

### Vollständigkeitswert der Käufergruppe

Mit dem Vollständigkeitswert wird bestimmt, ob die Einkaufsgruppe über die richtigen Mitglieder verfügt, die den Rollen zugewiesen sind, und für die Verwendung auf einer Account-Journey bereit ist. Dieser Wert ist ein Prozentsatz, der auf der Anzahl der Rollen innerhalb der Käufergruppe und der Anzahl der Rollen basiert, die mit mindestens einem Lead zugewiesen werden.

Wenn eine Käufergruppe beispielsweise vier Rollen umfasst und drei der vier Rollen mindestens einem Lead zugewiesen sind, ist die Käufergruppe zu 75 % vollständig.

Jedes Mal, wenn eine Käufergruppe erstellt oder aktualisiert wird, wird der Vollständigkeitswert für der Käufergruppe neu berechnet.

### Interaktionsbewertung der Käufergruppe {#engagement-score}

Der Interaktionswert basiert auf den Aktivitäten der kaufenden Gruppenmitglieder, den gewichteten Aktionen und den gewichteten Rollen. Die resultierende Bewertung wird innerhalb des Mandanten/der Instanz normalisiert, um einen konsistenten Vergleich zu ermöglichen und umsetzbare Einblicke zu ermöglichen.

Die Berechnung des anfänglichen Interaktionswerts beginnt, sobald Sie die Einkaufsgruppe erstellen, und wird täglich neu berechnet.

Unter [Interaktionswerte](./engagement-scores.md) finden Sie detaillierte Informationen zu Aktivitäten und Berechnungen des Interaktionswerts.

## Übersichtsvideo

>[!VIDEO](https://video.tv.adobe.com/v/3452948/?learn=on&captions=ger)
