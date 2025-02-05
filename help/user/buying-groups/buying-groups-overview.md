---
title: Einkaufsgruppen
description: Erfahren Sie, wie Einkaufsgruppen in Journey Optimizer B2B edition die Marketing-Effektivität steigern können, indem sie Mitglieder für Ihre Kontolisten identifizieren und auswählen.
feature: Buying Groups
exl-id: ddcd7b62-6a76-4f5e-b6d3-a20944ca8332
source-git-commit: e2059726fbb7541dbe0e7ab9be4cd82f37f26cf8
workflow-type: tm+mt
source-wordcount: '1259'
ht-degree: 6%

---


# Käufergruppen

Für B2B-Vertriebs- und Marketing-Aktivitäten sind Accounts der Schlüssel zu jeder Strategie. Jedem Konto ist eine Gruppe von Personen zugeordnet, und diese Personen können Mitarbeiter des Kontos oder Auftragnehmer sein, die mit dem Konto arbeiten. Konten sind hierarchisch, und verschiedene Produkte können auf verschiedenen Ebenen in der Hierarchie verkauft werden. Beispielsweise kann Adobe Experience Platform auf Unternehmensebene an ein Konto der obersten Ebene verkauft werden, während Adobe Photoshop an ein Konto verkauft werden kann, das einen Geschäftsbereich oder eine Abteilung innerhalb eines Unternehmens repräsentiert, z. B. eine Design-Abteilung innerhalb eines größeren Unternehmens.

![Diagramm zu Kontorollen](assets/account-roles-diagram.png){width="800"}

Innerhalb des Kontos könnte es eine Untergruppe von Personen geben, die die &quot;_&quot;_. Dies sind die Personen, die letztendlich die Kaufentscheidung treffen. Sie benötigen daher besondere Aufmerksamkeit vom Marketing-Experten und möglicherweise andere Informationen als die anderen Personen, die mit dem Account in Verbindung stehen. Einkaufsgruppen können für verschiedene Produktlinien oder Angebote eine unterschiedliche Personengruppe umfassen. Beispielsweise kann ein Cybersicherheitsprodukt in der Regel die Genehmigung eines Kaufs durch einen Chief Information Officer oder Chief Security Officer und einen Mitarbeiter der Rechtsabteilung erfordern, aber ein Produkt zur Fehlersuche kann in der Regel einen VP of Engineering und einen IT-Director als Mitglieder der kaufenden Gruppe haben.

![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Video ansehen - Übersicht](#overview-video)

## Schlüsselkomponenten

Sie können die Marketing-Effektivität steigern, indem Sie in Journey Optimizer B2B edition Einkaufsgruppen einrichten, die fehlende Mitglieder für Ihre Zielkontenlisten identifizieren. Diese Gruppen basieren auf den Lösungen, für die Ihre Vertriebsteams verantwortlich sind. Bevor Sie und Ihr Marketing-Team mit der Erstellung Ihrer Einkaufsgruppen beginnen, stellen Sie sicher, dass Sie die Schlüsselkomponenten definiert haben. Diese Komponenten sind für die Erreichung Ihrer Geschäftsziele von entscheidender Bedeutung.

| Komponente | Zweck |
| --------- | ------- |
| Lösungsinteresse | Diese Komponente bietet die Antwort auf: <ul><li>Was verkaufen Sie als Marketing-Organisation?</li><li>Welches Produkt oder welche Kollektion von Produkten möchten Sie verkaufen?</li></ul>  **_Beispiel:_** Crossselling New Product X to existing customers |
| Konto-Zielgruppe | Diese Komponente bietet die Antwort auf: <ul><li>An wen verkaufen Sie?</li><li>Auf welche Liste von Konten zielen Sie ab?</li></ul> **_Beispiel:_** Kontosegment, das durch Konten mit Produkt Y mit einem Umsatz von mehr als 1 Million definiert wird |
| Rollenvorlagen für Einkaufsgruppen | Diese Komponente bietet die Antwort auf: <ul><li>Auf welche Rollen zielen Sie ab?</li><li>Welcher Regelsatz wird verwendet, um zu bestimmen, wem die Rollen der Einkaufsgruppe zugewiesen sind?</li></ul>  **_Beispiel:_** Weisen Sie der Rolle Entscheidungsträger eine Person mit CMO-Titel zu |
| Käufergruppenphasen | (Optional) Diese Komponente bietet die Antwort auf: Wie verfolgt die kaufende Gruppe den Erfolg oder Misserfolg? |

## Einkaufsgruppen-Workflow

1. Erstellen Sie Einkaufsgruppen.

   Optionen:
   * Verwenden [Lösungsinteressen](./solution-interests.md) und [Rollenvorlage](./buying-groups-role-templates.md)
   * Import von Drittanbietern verwenden
   * Generieren aus KI/ML

1. Identifizieren Sie fehlende Personen.

   Analysieren Sie die Einkaufsgruppe mithilfe von Filtern.

   **_Beispiel_** Die Rolle des Entscheidungsträgers fehlt und der Vollständigkeitswert ist &lt; 50

1. Füllen Sie die Definitionen der Einkaufsgruppen aus.
<!--
   * Acquire missing people
   * Send to LinkedIn Destination
   * Enrich with Zoominfo -->

1. Verwendung auf einer Konto-Journey über das zugehörige Lösungsinteresse.

## Einkaufsgruppen und Komponenten anzeigen

Erweitern Sie in der linken Navigation **[!UICONTROL Konten]** und klicken Sie auf **[!UICONTROL Gruppen kaufen]**.

Die _[!UICONTROL Einkaufsgruppen]_ ist in Registerkarten unterteilt:

| Tab | Beschreibung |
| --- | ----------- |
| [!UICONTROL Übersicht] | Diese Registerkarte ist die Standardeinstellung und zeigt das Dashboard [Einkaufsgruppen](../dashboards/buying-groups-dashboard.md) an. |
| [!UICONTROL Durchsuchen] | Diese Registerkarte unterstützt die folgenden Aktivitäten: <ul><li>Liste der vorhandenen Einkaufsgruppen anzeigen. </li><li>Suchen Sie nach dem Namen der kaufenden Gruppe. </li><li>Filtern nach Lösungsinteresse. </li><li>Aufschlüsselung zu Details der Einkaufsgruppe. </li><li>Erstellen Sie eine Einkaufsgruppe. Eine Einkaufsgruppe löschen.</li></ul> |
| [!UICONTROL Lösungsinteressen] | Diese Registerkarte unterstützt die folgenden Aktivitäten: <ul><li>Liste der vorhandenen Einkaufsgruppen anzeigen. </li><li>Suchen Sie nach dem Namen der kaufenden Gruppe. </li><li>Zugreifen auf und Bearbeiten von Lösungsinteresseneigenschaften. </li><li>Erstellen Sie eine Interessenslösung. </li><li>Löschen Sie ein Lösungsinteresse. </li><li>Anzeigen und Löschen von Einkaufsgruppenvorgängen. </li></ul> |
| [!UICONTROL Rollenvorlagen] | Diese Registerkarte unterstützt die folgenden Aktivitäten: <ul><li>Anzeigen der Liste der vorhandenen Rollenvorlagen. </li><li>Nach Namen der Rollenvorlage suchen. </li><li>Zugreifen auf und Bearbeiten von Eigenschaften und Bedingungen von Rollenvorlagen. </li><li>Erstellen Sie eine Rollenvorlage. </li><li>Löschen einer Rollenvorlage. </li></ul> |
| [!UICONTROL Stadien] | Diese Registerkarte unterstützt die folgenden Aktivitäten: <ul><li>Zeigen Sie das Modell der vorhandenen Einkaufsgruppen-Stadien an. </li><li>Zugreifen auf und Bearbeiten des Entwurfs des Modells für Einkaufsgruppenschritte. </li><li>Erstellen Sie das Modell für Einkaufsgruppenstufen. </li></ul> |

## Suche und Filter für Einkaufsgruppen

Auf der _[!UICONTROL Durchsuchen]_ können Sie die Liste der Einkaufsgruppen anzeigen. Sie können nach Namen suchen und die Liste nach Lösungsinteressen filtern.

![Einkaufsgruppe Seite durchsuchen](assets/buying-groups-browse.png){width="800" zoomable="yes"}

## Details der Einkaufsgruppe

Um auf Details für eine Einkaufsgruppe zuzugreifen, klicken Sie auf den Namen der Einkaufsgruppe auf der Registerkarte _[!UICONTROL Durchsuchen]_. [Weitere Informationen](./buying-group-details.md)

![Details der Einkaufsgruppe](assets/buying-group-details.png){width="600" zoomable="yes"}

### Vollständigkeitsbewertung der Einkaufsgruppe

Mit dem Vollständigkeitswert wird bestimmt, ob die Einkaufsgruppe vollständig ist, d. h., dass ihr die richtigen Mitglieder zugewiesen sind und sie auf einer Account-Journey verwendet werden kann. Dieser Wert ist ein Prozentsatz, der auf der Anzahl der Rollen innerhalb der Einkaufsgruppe und der Anzahl der Rollen basiert, die mit mindestens einem Lead zugewiesen werden.

Wenn beispielsweise eine Einkaufsgruppe vier Funktionen hat und drei der vier Funktionen mindestens einem Lead zugewiesen sind, ist die Einkaufsgruppe zu 75 % abgeschlossen.

Der Vollständigkeitswert für die Einkaufsgruppe wird jedes Mal neu berechnet, wenn eine Einkaufsgruppe erstellt oder aktualisiert wird.

### Interaktionsbewertung der Käufergruppe

Der Interaktionswert für eine Einkaufsgruppe ist eine Zahl, die die Interaktion der Mitglieder einer Einkaufsgruppe auf der Grundlage der von ihnen durchgeführten Aktivitäten bestimmt. Zur Berechnung der Punktzahl wird jede eingehende Aktivität verwendet, die von den Mitgliedern der Einkaufsgruppe in den letzten 30 Tagen ausgeführt wurde.

Es gibt eine tägliche Häufigkeitsbegrenzung von 20 pro Aktivität. Wenn ein Mitglied einer Einkaufsgruppe dieselbe Aktivität mehr als 20 Mal am Tag ausführt, ist die Anzahl der Aktivitäten auf 20 begrenzt und nicht höher.

Die angezeigte Punktzahl ist gerundet. Beispielsweise wird ein Wert von 75,89999 als 76 angezeigt.

#### Gewichtung

Benutzerinnen und Benutzer können jeder Rolle in _Rollenvorlage &quot;_&quot; zuweisen, um einer Rolle unterschiedliche Gewichtungen für die Berechnung des Interaktionswerts zuzuweisen.

![Legen Sie in der Rollenvorlage die Gewichtung für jede Rolle fest](./assets/roles-templates-weighting.png){width="700" zoomable="yes"}

Jede Gewichtungsstufe wird in einen Wert umgewandelt, der für die Berechnung des Interaktionswerts verwendet wird:

* [!UICONTROL Trivial] = 20
* [!UICONTROL Gering] = 40
* [!UICONTROL Normal] = 60
* [!UICONTROL Wichtig] = 80
* [!UICONTROL Vital] = 100

Eine Rollenvorlage mit drei Rollen, gewichtet mit _[!UICONTROL Wichtig]_, _[!UICONTROL Wichtig]_ und _[!UICONTROL Normal]_, konvertiert in die folgenden gewichteten Prozentsätze:

| Role | Gewichtung | Systemwert | Wertberechnung | Prozentsatz |
|-------------- |--------- |------------- |------------------ |---------- |
|               |          |              |                   |           |
| Entscheidungsträger | lebenswichtig | 100 | 100/240 | 41,67 % |
| Beeinflusser | Wichtig | 80 | 80/240 | 33,33 % |
| Praktiker | Normal | 60 | 60/240 | 25 % |
|               | Gesamt | 240 |                   |           |

#### Berechnungsbeispiel

Das folgende Beispiel veranschaulicht die Berechnung des Interaktionswerts mithilfe des beschriebenen Prozentsatzes der Rollengewichtung, der Anzahl der eingehenden Aktivitäten für jedes Mitglied der Einkaufsgruppe und einer täglichen Begrenzung von 20 Zählern für jedes Ereignis (wenn es mehrmals aufgetreten ist).

| Role | Mitglied | Typ der Aktivität | Zählung gestern | Zählung heute | Kalkulation | Gesamtergebnis |
|-------------- |--------- |-------------|-----------------|-------------|------|-----------|
|               |          |             |                 |             |      |           |
| Entscheidungsträger | Adam | Besuchte Website | 37 | 15 | 20 + 15 | 35 |
|               |          | Angeklickte E-Mail | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Mark | Besuchte Website | 5 | 3 | 5 + 3 | 8 |
|               |          | Angeklickte E-Mail | 1 | 1 | 1 + 1 | 2 |
|               |          | Heruntergeladene Kneipe | 3 | 2 | 3 + 2 | 5 |
| **Gesamtpunktzahl der Entscheidungsträger** |         |             |                 |             |      | **£** |
|               |          |             |                 |             |      |           |
| Beeinflusser | John | Besuchte Website | 19 | 9 | 19 + 9 | 28 |
| **Influencers-Gesamtpunktzahl** |         |             |                 |             |      | **28** |
|               |          |             |                 |             |      |           |
| Praktiker | Bob | Angeklickte E-Mail | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Paul | Angeklickte E-Mail | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Calvin | Angeklickte E-Mail | 1 | 1 | 1 + 1 | 2 |
|               |          | Besuchte Website | 1 | 7 | 1 + 7 | 8 |
|               |          | Heruntergeladene Kneipe | 1 | 2 | 1 + 2 | 3 |
| **Gesamtpunktzahl der Praktizierenden** |         |             |                 |             |      | **17** |

Der endgültige Engagement-Score wird durch Anwendung der Gewichtung für jeden Rollenwert berechnet:

| Role | Gesamtergebnis der Funktion | Rollengewichtung % | Score X Gewichtung % |
|-------------- |---------------- |------------- |---------------- |
| Entscheidungsträger | 52 | 41,67 % | 21,67 |
| Influencers | 28 | 33,33 % | 9,33 |
| Praktizierende | 17 | 25 % | 4,25 |
| **Endgültiger Interaktionswert** |                |             | **,25** |

## Übersichtsvideo

>[!VIDEO](https://video.tv.adobe.com/v/3433078/?learn=on)
