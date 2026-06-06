---
title: Pfade aufteilen und zusammenführen
description: Aufspalten und Zusammenführen von Journey-Pfaden zu Segmentkonten oder Personen nach Bedingungen, Einkaufsgruppen und Ereignisverlauf in Journey Optimizer B2B edition.
feature: Account Journeys
solution: Journey Optimizer B2B Edition
role: User
exl-id: 563d6a85-504d-4c70-b075-8a9a9e88bd6b
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: ff2b9b37-92e0-45fc-b853-379d44c08c89id: d00e9f03-e50b-4162-b143-0c0817c937c2
autotag-review: 2026-03-30T23:10:13.939Z
TQID: https://experienceleague.adobe.com/qTheDe4jO49z8u8ia2wGZvLg-Gbh0MrN--a0lksLPBs
source-git-commit: 7cd6c4ecfbbd3a86b4f30d1b4fe6f06655a9c4f5
workflow-type: tm+mt
source-wordcount: 2542
ht-degree: 3%

---

# Aufteilen und Zusammenführen von Pfaden {#split-paths}

Verwenden Sie Split- und Merge-Path-Knoten, um Personen oder Konten gemäß den von Ihnen definierten Bedingungen zu segmentieren. Erstellen Sie Pfade für die Audience- oder Kontenliste gemäß den Bedingungen, definieren Sie jeden Pfad mit Aktions- und Ereignisknoten für das Segment, kombinieren Sie dann die Pfade und setzen Sie das Journey fort.

![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Übersichtsvideo ansehen](#overview-video)

Ein Knoten _Pfade aufteilen_ definiert einen oder mehrere segmentierte Pfade, die entweder auf _**- oder Personenfiltern**_. Eine Aufspaltung, die auf einem Personenfilter basiert, wird automatisch mit einem Zusammenführungspfade -Knoten geschlossen, damit alle Personen mit dem nächsten Schritt fortfahren können, ohne ihren Kontokontext zu verlieren.

>[!NOTE]
>
>Es werden maximal 25 Pfade unterstützt.

## Pfade nach Konten aufteilen {#split-paths-by-accounts}

**_(Nur Konto-Journey_**

Pfade, die nach Konten aufgeteilt sind, können sowohl Konto- als auch Personenaktionen und -ereignisse enthalten. Diese Pfade können weiter aufgeteilt werden.

_**Wie funktioniert ein aufgeteilter Pfad nach Kontenknoten**_

* Jeder Pfad, den Sie hinzufügen, enthält einen Endknoten mit der Möglichkeit, Knoten zu jedem Edge hinzuzufügen.
* Aufspaltung nach Kontoknoten kann verschachtelt werden (Sie können den Pfad wiederholt nach Konten aufteilen).
* Die Auswertung jedes Pfads erfolgt von oben nach unten. Wenn ein Konto dem ersten und zweiten Pfad entspricht, wird es nur entlang des ersten Pfads fortgesetzt.
* Zwei oder mehr Pfade können mithilfe eines Zusammenführungsknotens kombiniert werden.
* Der Knoten unterstützt die Definition eines Pfads _[!UICONTROL Andere Konten]_, in dem Sie Aktionen oder Ereignisse für Konten hinzufügen können, die nicht mit einem der definierten Segmente/Pfade übereinstimmen.

![Journey-Knoten - Pfade nach Konto aufteilen](./assets/node-split-paths-account.png){width="700" zoomable="yes"}

### Pfadbedingungen des Kontos {#account-path-filters}

| Pfadbedingungen | Beschreibung |
| --------------- | ----------- |
| [!UICONTROL Kontoattribute] | Attribute aus dem Kontoprofil, einschließlich: <li>Jahresumsatz <li>Stadt <li>Land <li>Mitarbeiterzahl <li>Branche <li>Name <li>SIC-Code <li>Status |
| [!UICONTROL Benutzerdefinierte Objekte] > hat `<custom object>` | [!BADGE Beta]{type=Informative tooltip="Beta-Funktion"} Das Konto hat keine relationalen Schemaeinträge. Sie kann auch anhand eines der ausgewählten benutzerdefinierten Objektkriterien ausgewertet werden, wie im [XDM Relational Schema) ](../admin/xdm-field-management.md#relational-schemas). (Siehe [Benutzerdefinierte Datenfilterung](#custom-data-filtering).) |
| [!UICONTROL Sonderfilter] > [!UICONTROL Konto hat eine passende Einkaufsgruppe] | Dem Konto ist mindestens eine Einkaufsgruppe zugeordnet. Sie kann für eine passende Einkaufsgruppe anhand einer oder mehrerer der folgenden Einschränkungen bewertet werden: <li>Interesse an der Lösung <li>Einkaufsgruppenphase <li>Einkaufsgruppenstatus <li>Interaktionsbewertung <li>Vollständigkeitsindex <li> Anzahl der Personen in Käufergruppenrolle |

### Fügen Sie einen aufgeteilten Pfad nach Kontenknoten hinzu

1. Navigieren Sie zur Journey-Karte.

1. Klicken Sie auf das Pluszeichen ( **+** ) auf einem Pfad und wählen Sie **[!UICONTROL Pfade aufteilen]**.

   ![Journey-Knoten hinzufügen - Aufspaltungspfade](./assets/add-node-split.png){width="300" zoomable="no"}

1. Wählen Sie in den Knoteneigenschaften auf der rechten Seite **[!UICONTROL Konten]** für die Aufspaltung aus.

1. Um eine Bedingung zu definieren, die für _[!UICONTROL Pfad 1]_ gilt, klicken Sie auf **[!UICONTROL Bedingung anwenden]**.

   ![Pfadknoten aufteilen - Bedingung hinzufügen](./assets/node-split-properties-apply-condition.png){width="500" zoomable="yes"}

1. Um den Aufspaltungspfad zu definieren, fügen Sie einen oder mehrere Filter im Bedingungseditor hinzu.

   * Ziehen Sie Filterattribute per Drag-and-Drop aus dem linken Navigationsbereich und füllen Sie die Übereinstimmungsdefinition aus.

   * Verfeinern Sie Ihre Bedingungen, indem Sie oben **[!UICONTROL die]** Filterlogik“ anwenden. Sie wählen, ob alle Filter oder nur ein beliebiger Filter übereinstimmen sollen.

     ![Pfadknoten aufteilen - Filterlogik für Bedingungskonten](./assets/node-split-conditions-accounts.png){width="700" zoomable="yes"}

   * Klicken Sie auf **[!UICONTROL Fertig]**.

1. Um weitere Pfade hinzuzufügen, klicken Sie auf **[!UICONTROL Pfad hinzufügen]** und wiederholen Sie die vorherigen Schritte, um die für diesen Pfad geltenden Bedingungen hinzuzufügen.

   Sie können auch jeden Pfad anhand dieser Bedingungen beschriften oder die Standardbeschriftungen verwenden.

1. Ordnen Sie die Pfade bei Bedarf entsprechend der Priorität neu an, die Sie für die Aufspaltung festlegen möchten.

   Die Pfadfilterung wird in der Reihenfolge von oben nach unten bewertet. Jedes Konto fährt auf dem ersten Pfad fort, der übereinstimmt.

   Klicken Sie auf die Pfeile nach oben und unten oben rechts auf jeder Pfadkarte, um sie in der Liste der Pfade nach oben oder unten zu verschieben.

   ![Pfadknoten aufteilen - Pfade neu anordnen](./assets/node-split-reorder-paths-accounts.png){width="500" zoomable="yes"}

1. Aktivieren Sie die Option **[!UICONTROL Andere Konten]**, um den Standardpfad für Konten zu definieren, die nicht mit den definierten Segmenten/Pfaden übereinstimmen.

   Wenn diese Option nicht aktiviert ist, endet das Journey für Konten, die nicht mit einem definierten Segment/Pfad innerhalb der Aufspaltung übereinstimmen.

### Gruppenfilter für Konten kaufen {#buying-group-filtering-accounts}

Sie können einen Pfad für Konten definieren, die mit Einkaufsgruppen verknüpft sind, und den Pfad mithilfe von Einkaufsgruppenkriterien filtern. Verwenden Sie den Filter **[!UICONTROL Konto hat abgeglichene Einkaufsgruppe]** um das Pfadsegment mithilfe einer abgeglichenen Einkaufsgruppe zu definieren. Dieser Filter enthält auch die Option, Konten anhand der Anzahl der zugewiesenen Rollen innerhalb einer abgeglichenen Einkaufsgruppe zu identifizieren.

Sie können beispielsweise die Bereitschaft für eine Einkaufsgruppe anhand der Tiefe (Anzahl der Personen) bewerten, die sie in verschiedenen Rollen hat, z. B. drei Entscheidungsträger und zwei Influencer. Legen Sie in diesem Fall die Bedingung fest, um Konten mit mindestens drei (3) Entscheidungsträgern und zwei (2) Einflussnehmern in einer abgeglichenen Einkaufsgruppe anzusprechen:

1. Klicken Sie **[!UICONTROL Filter hinzufügen]** und wählen Sie den Filter **[!UICONTROL Anzahl der Personen in der]** aus.

   ![Filter für Konto hinzufügen wurde mit einer Einkaufsgruppe abgeglichen und Anzahl der Personen in der Einkaufsgruppenrolle ausgewählt](./assets/node-split-account-condition-matched-buying-group-number-people-role.png){width="700" zoomable="yes"}

1. Definieren Sie den ersten Rollenparameter.

   * Legen Sie die Anzahl der Personen fest, die eine Auswertung `at least`, wobei der Wert `3` lautet.
   * Legen Sie die Rollenbewertung auf `is` fest und wählen Sie `Decision Maker` aus der Liste der Rollen aus.

1. Wiederholen Sie Schritt 1, um einen weiteren Einkaufsgruppen-Rollenparameter hinzuzufügen.

1. Definieren Sie den zweiten Rollenparameter.

   * Legen Sie die Anzahl der Personen fest, die eine Auswertung `at least`, wobei der Wert `2` lautet.
   * Legen Sie die Rollenbewertung auf `is` fest und wählen Sie `Influencer` aus der Liste der Rollen aus.

   ![Bedingungen für die Rollentiefe in der abgeglichenen Einkaufsgruppe für ein Konto](./assets/node-split-account-condition-matched-buying-group-role-depth-example.png){width="700" zoomable="yes"}

1. Klicken Sie **[!UICONTROL Fertig]**, wenn alle Bedingungen für den Pfad definiert sind.

Für die identifizierten Konten können Sie dann einen Aktionsknoten im Pfad hinzufügen, um den Status der Einkaufsgruppe oder des Kaufstadiums zu aktualisieren oder eine E-Mail mit einer Verkaufswarnung zu senden.

## Pfade nach Personen aufteilen

_(Konto- und Personen-Journey)_

Pfade, die nach Personen aufgeteilt sind, können nur Personenaktionen enthalten. Diese Pfade können nicht erneut aufgeteilt und automatisch wieder verbunden werden.

_**Wie funktioniert ein aufgeteilter Pfad nach Personenknoten**_

* Die Funktion „Aufspaltung nach Personen _Knoten funktioniert in einer Kombination aus_ und Zusammenführung. Die Pfade der Aufspaltung werden automatisch zusammengeführt, sodass alle Personen mit dem nächsten Schritt fortfahren können, ohne ihren Kontokontext zu verlieren.
* Nach Personen aufgeteilte Knoten können nicht verschachtelt werden (Sie können keinen aufgeteilten Pfad für Personen auf einem Pfad hinzufügen, der sich in diesem gruppierten Knoten befindet).
* Die Auswertung jedes Pfads erfolgt von oben nach unten. Wenn eine Person dem ersten und zweiten Pfad entspricht, fährt sie nur auf dem ersten Pfad fort.
* Der Knoten unterstützt die Verwendung von _Konto-Personen-Beziehungen_ mit denen Sie Personen nach ihrer Rolle filtern können (z. B. Auftragnehmer oder Vollzeit-Mitarbeiter), wie in der Beziehung definiert.
* Der Knoten unterstützt die Definition eines Pfads _[!UICONTROL Andere Personen]_, in dem Sie Aktionen oder Ereignisse für Personen hinzufügen können, die nicht mit einem der definierten Segmente/Pfade übereinstimmen.

![Konto-Journey-Knoten - Pfade nach Personen aufteilen](./assets/node-split-paths-people.png){width="700" zoomable="yes"}

### Personenpfadfilter {#people-path-filters}

| Filter | Beschreibung |
| ------------ | ----------- |
| [!UICONTROL Benutzerdefinierte Objekte] > hat `<custom object>` | [!BADGE Beta]{type=Informative tooltip="Beta-Funktion"} Die Person hat keine relationalen Schemaeinträge. Sie kann auch anhand eines der ausgewählten benutzerdefinierten Objektkriterien ausgewertet werden, wie im [XDM Relational Schema) ](../admin/xdm-field-management.md#relational-schemas). (Siehe [Benutzerdefinierte Datenfilterung](#custom-data-filtering)) |
| [!UICONTROL Ereignisverlauf] | Teilt Personen auf Grundlage von Erlebnisereignissen, die vor dem Journey-Eintritt aufgetreten sind. Erweitern Sie den Ordner , um alle unter „Admin[ > XDM-Ereigniskonfiguration“ konfigurierten Ereignistypen anzuzeigen](../admin/configure-aep-events.md) und wählen Sie einen aus, der als Filter hinzugefügt werden soll. Zu den Einschränkungen gehören Felder aus dem ausgewählten Ereignis, ein Lookback-Zeitfenster, das ab dem Zeitpunkt gemessen wird, zu dem die Person die Journey betritt, und eine optionale Mindestanzahl von Malen. |
| [!UICONTROL Personenattribute] | Attribute aus dem [Personenprofil](../admin/field-mapping.md#xdm-business-person-attributes), einschließlich: <li>Stadt <li>Land <li>E-Mail-Adresse <li>E-Mail-Adresse ungültig <li>E-Mail angehalten <li>Vorname <li>Abgeleitetes Bundesland/abgeleitete Region <li>Stellenbezeichnung <li>Last name <li>Mobiltelefonnummer <li>Engagement-Score einer Person <li>Telefonnummer <li>Postleitzahl <li>Bundesland |
| [!UICONTROL Sonderfilter] > [!UICONTROL Mitglied der Einkaufsgruppe] | (Veraltet) Die Person ist oder ist kein kaufendes Gruppenmitglied, das anhand eines oder mehrerer der folgenden Kriterien bewertet wird: <li>Interesse an der Lösung</li><li>Einkaufsgruppenstatus</li><li>Vollständigkeitsindex</li><li>Interaktionsbewertung</li><li>wird entfernt</li><li>Rolle</li> |
| [!UICONTROL Spezialfilter] > [!UICONTROL Mitglied der Liste] | (Veraltet) Die Person ist oder ist nicht Mitglied in einer oder mehreren [!DNL Marketo Engage]. |
| [!UICONTROL Spezialfilter] > [!UICONTROL Mitglied des Programms] | (Veraltet) Die Person ist oder ist nicht Mitglied in einem oder mehreren [!DNL Marketo Engage]. |

### Pfadbedingungen für Konto-Person

| Pfadbedingungen | Beschreibung |
| --------------- | ----------- |
| [!UICONTROL Rolle im Konto] | Der Person wird eine Rolle im Konto zugewiesen oder ihr wird keine Rolle zugewiesen. Optionale Einschränkungen: <li>Rollenname |

### Fügen Sie einen Pfad für die Aufspaltung nach Personenknoten hinzu {#add-a-split-path-by-people-node}

>[!NOTE]
>
>Wenn Sie Pfade nach Personen aufteilen, wird _Knoten „Aufspaltungspfade schließen_ automatisch eingefügt, um die Aufspaltung zu beenden. Bei einem Pfad, der nach Personen aufgeteilt ist, ist nur _Aktion ausführen_ auf Personenknoten zulässig.

1. Navigieren Sie zur Journey-Karte.

1. Klicken Sie auf das Pluszeichen ( **+** ) auf einem Pfad und wählen Sie **[!UICONTROL Pfade aufteilen]**.

   ![Journey-Knoten hinzufügen - Aufspaltungspfade](./assets/add-node-split.png){width="300" zoomable="no"}

1. Wählen Sie in den Knoteneigenschaften auf der rechten Seite **[!UICONTROL Personen]** für die Teilung aus.

1. (Nur Konto-Journey **[!UICONTROL Legen Sie die (für Bedingungen verwendeten Attribute]**.

   * Wählen Sie **[!UICONTROL Nur Personenattribute]** aus, um Bedingungen im Zusammenhang mit dem Personenprofil zu verwenden.
   * Wählen Sie **[!UICONTROL Nur Konto-Personen-Attribute]** aus, um Bedingungen im Zusammenhang mit der Rollenmitgliedschaft der Person in einem Konto zu verwenden.

1. Um eine Bedingung zu definieren, die für _[!UICONTROL Pfad 1]_ gilt, klicken Sie auf **[!UICONTROL Bedingung anwenden]**.

1. Fügen Sie im Bedingungseditor einen oder mehrere Filter hinzu, um den Aufspaltungspfad zu definieren.

   * Ziehen Sie einen beliebigen Personenfilter aus dem linken Navigationsbereich und füllen Sie die Definition der Übereinstimmung aus.

     >[!NOTE]
     >
     >Wenn Sie benutzerdefinierte Personenfelder im Kontozielgruppen-Schema in Experience Platform definiert haben, können diese Felder auch als Personenattribute in Bedingungen verwendet werden.

   * Verfeinern Sie Ihre Bedingungen, indem Sie oben **[!UICONTROL die]** Filterlogik“ anwenden. Sie wählen, ob alle Attributbedingungen oder eine beliebige Bedingung erfüllt werden sollen.

     ![Pfadknoten aufteilen - Bedingungen für Personenfilterlogik](./assets/node-split-conditions-people.png){width="700" zoomable="yes"}

   * Klicken Sie auf **[!UICONTROL Fertig]**.

1. Um weitere Pfade hinzuzufügen, klicken Sie auf **[!UICONTROL Pfad hinzufügen]** und wiederholen Sie die vorherigen Schritte, um die für diesen Pfad geltenden Bedingungen hinzuzufügen.

   Sie können auch jeden Pfad anhand dieser Bedingungen beschriften oder die Standardbeschriftungen verwenden.

1. Ordnen Sie die Pfade bei Bedarf entsprechend der Priorität neu an, die Sie für die Aufspaltung festlegen möchten.

   Die Pfadfilterung wird in der Reihenfolge von oben nach unten bewertet. Jede Person fährt auf dem ersten Pfad fort, der übereinstimmt.

   Klicken Sie auf die Pfeile nach oben und unten oben rechts auf jeder Pfadkarte, um sie in der Liste der Pfade nach oben oder unten zu verschieben.

   ![Pfadknoten aufteilen - Pfade neu anordnen](./assets/node-split-reorder-paths-people.png){width="500" zoomable="yes"}

1. Aktivieren Sie die Option **[!UICONTROL Andere Personen]**, um einen Standardpfad für Personen hinzuzufügen, die den definierten Pfaden nicht entsprechen.

   Wenn diese Option nicht aktiviert ist, bewegen sich Personen, die mit keinem definierten Segment/Pfad übereinstimmen, an der Teilung vorbei und fahren mit dem nächsten Schritt auf der Journey fort.

   Wenn Sie für jeden Pfad zur Aufteilung Ihrer Zielgruppe auf Personenebene Bedingungen definiert haben, können Sie Aktionen hinzufügen, die Sie für Personen durchführen möchten.

### Filtern des Erlebnisereignisverlaufs {#experience-event-history-filtering}

Für einen aufgeteilten Pfad nach Personen können Sie einen Pfad definieren, der auf Erlebnisereignissen basiert, die vor dem Eintritt der Person in die Journey aufgetreten sind. Erweitern Sie im Bedingungseditor den Ordner **[!UICONTROL Ereignisverlauf]**, um eine Liste aller von Ihrem Administrator konfigurierten Ereignistypen anzuzeigen. Ereignistyp auswählen, um ihn als Filterbedingung hinzuzufügen.

Das Lookback-Zeitfenster für den Ereignisverlauf wird ab dem Zeitpunkt rückwärts gemessen, zu dem die Person die Journey betritt. Beispielsweise wird in einem 30-Tage-Fenster bewertet, ob das qualifizierte Ereignis innerhalb der 30 Tage vor dem Journey-Eintrag aufgetreten ist.

Sie können den Filter mithilfe von spezifischen Einschränkungen für die Felder des ausgewählten Ereignisses weiter verfeinern. Die optionalen Einschränkungen **[!UICONTROL Mindestanzahl von]**) und **[!UICONTROL Datum der Aktivität]** werden beide innerhalb des definierten Lookback-Fensters ausgewertet. Da Ereignisverlaufsdaten mit Adobe Experience Platform synchronisiert werden, kann es zu einer kurzen Verzögerung kommen, bevor ein kürzlich aufgetretenes Ereignis für diesen Filter sichtbar wird.

>[!NOTE]
>
>Die im Ordner [!UICONTROL Ereignisverlauf] verfügbaren Ereignisse werden durch die Konfigurationen [Erlebnisereignisse und -felder) ](../admin/configure-aep-events.md).

**Beispiel:** Um Personen, die auf einen Link in einer Marketing-E-Mail geklickt haben, bevor sie die Journey aufrufen, weiterzuleiten, wählen Sie das E-Mail-Klickereignis aus dem Ordner [!UICONTROL Ereignisverlauf] aus, legen Sie das Lookback-Fenster auf den entsprechenden Zeitraum fest und wenden Sie bei Bedarf Einschränkungen auf Feldebene an (z. B. eine bestimmte Link-URL).

![Pfad nach Personenbedingung für Ereignisverlauf aufteilen](./assets/node-split-people-condition-event-history.png){width="700" zoomable="yes"}

>[!BEGINSHADEBOX „Inaktivitätsfilterung“]

Für jeden Filter _[!UICONTROL Ereignisverlauf]_ können Sie die Option **[!UICONTROL Zu Inaktivitätsfilter wechseln]** aktivieren. Diese Option ändert den Filter in eine Auswertung für eine Abwesenheit dieses Aktivitätstyps. Fügen Sie beispielsweise den Filter _[!UICONTROL Direkt-Marketing-E-Mail geöffnet]_ hinzu, um einen Pfad für Personen zu erstellen, _**eine E-Mail**_ geöffnet haben. Aktivieren Sie die Option Inaktivität und geben Sie die E-Mail-Adresse an.

![Pfad nach Inaktivitätsbedingung für Personen aufteilen](./assets/node-split-people-condition-inactivity.png){width="700" zoomable="yes"}

>[!ENDSHADEBOX]

### Filtern von Abonnements

Im Abschnitt _[!UICONTROL Spezielle Filter]_ gibt es mehrere Filter, mit denen Sie die Zugehörigkeit einer Person zu einer Einkaufsgruppe oder [!DNL Marketo Engage] Liste bewerten können.

Wenn Sie beispielsweise einen Pfad für Personen erstellen möchten, die Mitglieder einer Einkaufsgruppe sind und denen eine bestimmte Rolle zugewiesen ist, fügen Sie den Filter _[!UICONTROL Sonderfilter]_ > _[!UICONTROL Mitglied der]_) hinzu. Legen Sie für den Filter die Mitgliedschaft auf _true_ fest, wählen Sie ein _[!UICONTROL Interesse an der Lösung]_, das mit einer oder mehreren Einkaufsgruppen verknüpft ist, und legen Sie die _[!UICONTROL Rolle]_ fest, der Sie entsprechen möchten.

![Pfad nach Personen aufteilen Bedingung für den Kauf der Gruppenmitgliedschaft](./assets/node-split-people-condition-buying-group-membership.png){width="700" zoomable="yes"}

Sie können auch zusätzliche Einschränkungen für die Einkaufsgruppenmitgliedschaft einbeziehen:

* _[!UICONTROL Gruppenphase kaufen]_
* _[!UICONTROL Einkaufsgruppenstatus]_
* _[!UICONTROL Vollständigkeit]_
* _[!UICONTROL Engagement score]_
* _[!UICONTROL wird entfernt]_

>[!TIP]
>
>Um Mitglieder auszuschließen, die aus einer Einkaufsgruppe entfernt wurden, verwenden Sie die Beschränkung _[!UICONTROL Ist entfernt]_, die auf `false` gesetzt ist. Sie können entfernte Member auch explizit einbeziehen, indem Sie diese Einschränkung auf `true` festlegen.

>[!BEGINSHADEBOX &quot;Marketo Engage-Liste und Programmmitgliedschaft“]

Überprüfen Sie [!DNL Marketo Engage] _Smart-Kampagnen_ die Mitgliedschaft in Programmen, um sicherzustellen, dass Leads keine doppelten E-Mails erhalten und nicht gleichzeitig Mitglieder mehrerer E-Mail-Streams sind. In Journey Optimizer B2B können Sie als Bedingung für Ihren Aufspaltungspfad nach Personen [!DNL Marketo Engage] Listenabonnement prüfen, um doppelte Journey-Aktivitäten zu vermeiden.

Um die Listenmitgliedschaft in einer aufgeteilten Bedingung zu verwenden, erweitern Sie **[!UICONTROL Spezielle Filter]** und ziehen Sie die **[!UICONTROL Mitglied der Liste]** oder **[!UICONTROL Mitglied des Programms]** Bedingung in den Filterbereich. Vervollständigen Sie die Filterdefinition, um die Zugehörigkeit zu einer oder mehreren [!DNL Marketo Engage] zu bewerten.

![Pfad nach Personen aufteilen Bedingung für [!DNL Marketo Engage] Listenmitgliedschaft](./assets/node-split-paths-conditions-people-member-of-list.png){width="700" zoomable="yes"}
<br/>

>[!NOTE]
>
>**Einstellung von Funktionen**</br></br>
>
>In der aktuellen Journey Optimizer B2B edition-Version wird das Filtern nach Listen- oder Programmmitgliedschaften in einer Marketo Engage-Instanz nicht unterstützt.

>[!ENDSHADEBOX]

## Benutzerdefinierte Datenfilterung {#custom-data-filtering}

[!BADGE Beta]{type=Informative tooltip="Beta-Funktion"}

Sie können relationale Schemata (modellbasierte Klassen) verwenden, um Pfade nach Konto oder Personen aufzuteilen. Die benutzerdefinierten Objekte werden in _relationalen Schemata_ definiert und ein Produktadministrator kann [relationale Schemafelder konfigurieren](../admin/xdm-field-management.md#relational-schemas) in [!DNL Journey Optimizer B2B Edition]. Die ausgewählten Schemafelder sind im Bedingungseditor für die Verwendung in den Knoten _Pfad nach Konto aufteilen_ und _Pfad nach Personen aufteilen_ verfügbar.

Erweitern Sie bei **[!UICONTROL Bedingung „Pfad nach Konto]**&quot; oder **[!UICONTROL Pfad nach]** aufteilen _[!UICONTROL „Benutzerdefinierte Objekte]_. Fügen Sie die Bedingung hinzu und legen Sie den Wert auf `true` oder `false` fest. Klicken Sie **[!UICONTROL Einschränkung hinzufügen]**, um die Feldwerte zum Filtern zu verwenden.

![Beispiel für Kontobedingungen für ein benutzerdefiniertes Objekt für ein relationales Schema](./assets/node-split-paths-account-relational-schema.png){width="600" zoomable="yes"}

## Pfade zusammenführen {#merge-paths}

Fügen Sie einen _Mergepfade_-Knoten hinzu, um verschiedene _Aufspaltungspfade nach Konto_ in Ihrem Journey zu kombinieren.

1. Fügen Sie in einer Journey-Zuordnung mit einem aufgeteilten Knoten mit drei oder mehr Pfaden eine Kombination aus Aktionen und Ereignissen zu jedem Pfad hinzu.

1. Klicken Sie auf das Pluszeichen ( **+** ) für einen dieser Pfade und wählen Sie **[!UICONTROL Zusammenführen]** aus den angezeigten Optionen aus.

   ![Journey-Knoten - Zusammenführungspfade](./assets/node-plus-icon-merge-paths.png){width="400" zoomable="no"}

1. Wählen Sie in den Knoteneigenschaften „Zusammenführungspfade“ die Pfade aus, die zusammengeführt werden sollen.

   ![Journey-Knoten - Zusammenführungspfade](./assets/node-merge-select-paths.png){width="600" zoomable="yes"}

   An dieser Stelle werden die Pfade zusammengeführt, sodass Konten aus den ausgewählten Pfaden zu einem einzigen Pfad kombiniert werden, der durch den Journey weiter ausgeführt werden kann.

1. Bei Bedarf können Sie die Zusammenführung von Pfaden aufheben, indem Sie zurück zu den Knoteneigenschaften der Zusammenführungspfade navigieren und das Kontrollkästchen für alle Pfade deaktivieren, die Sie entfernen möchten.

## Übersichtsvideo {#overview-video}

>[!VIDEO](https://video.tv.adobe.com/v/3443231/?learn=on)
