---
title: Persona-Zuordnung
description: Erfahren Sie, wie Sie Personas für Account-basiertes Marketing konfigurieren, indem Sie Personenattribute zuordnen, um optimierte Rollenvorlagen für Einkaufsgruppen zu erstellen.
feature: Setup, Buying Groups
hide: true
hidefromtoc: true
badgeBeta: label="Beta" type="informative" tooltip="Diese Funktion befindet sich derzeit in einer eingeschränkten Beta-Version"
role: Admin
source-git-commit: e301dfd5ac1421eb73e80b1d772d1b17f9ef3a1e
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 1%

---

# Persona-Zuordnung

Personas sind ein wichtiger Aspekt in einem Account-Based Marketing (ABM)-Ansatz, da sie Marketing-Experten dabei helfen, ihre Strategien an die spezifischen Bedürfnisse, Präferenzen und Schmerzpunkte von Personen in Zielkonten anzupassen. Marketing-Experten können für jede Rolle ein detailliertes Profil erstellen, einschließlich Hintergrund, Zuständigkeiten, Probleme und bevorzugter Kommunikationskanäle. Mit diesen Definitionen können Admins Personas anhand von Personenattributen in Journey Optimizer B2B edition konfigurieren, sodass Rollenvorlagen optimierte und konsistente Rollenbedingungen verwenden können, die diese Personas erfassen.

<!-- Currently there is no insight into what persona goes into what role. With buying group agent, when asked questions about, what should be the size of the buying group, what persona should be in that buying group, what role do they play, etc, then agent will analyze all the data, (opportunity data, engagement data, sales conversation, etc) and informs the user that the buying group needs 7 persona, e.g.CMO, VP of marketing, marketing leader, Marketing ops, etc. 

Then based on what agent informed, users can create a template with those personas. -->
Definition der Persona und Nutzungsbeschränkungen:

* Es können bis zu 20 Personas in der Liste „Persona _[!UICONTROL Zuordnung“ definiert]_.
* Jede Rolle kann bis zu fünf Attribute in ihre Definition aufnehmen.
* Sie können für alle definierten Personas bis zu zehn verschiedene Personenattribute verwenden.

>[!BEGINSHADEBOX]

**Anwendungsfall: Varianten der Auftragstitel**

Viele Marketing- und Verkaufsteams verwenden Jobtitel als Möglichkeit, verschiedene Rollen innerhalb eines Kontos zu identifizieren. Titel für Kontakte können jedoch inkonsistent sein und zahlreiche Varianten für ähnliche Rollen verwenden. Beim Erstellen von Vorlagen für Einkaufsgruppenrollen kann es erforderlich sein, dass Sie jede mögliche zugehörige Stellenbezeichnung für eine bestimmte Rolle definieren. Sie können diese Definitionen vereinfachen und Personen mit ähnlichen Berufsbezeichnungen unter eine abgeleitete Rolle stellen, die Sie dann in verschiedenen Rollenvorlagen für Einkaufsgruppen nutzen können.

Sie können beispielsweise eine Rolle mit dem Namen _Produktverwaltung_ konfigurieren und sie mithilfe des Attributs „Auftragstitel“ für Werte von _Produkt-Manager_, _definieren. Product Manager_, _Senior Product Manager_, _PM_, _SR. PM_, _Principal PM_ und _Principal Product Manager_. Verwenden Sie diese Rolle dann in einer Rollenvorlage, in der die Bedingung mit übereinstimmt _Persona is Product Management_. Mithilfe der konfigurierten Rolle ist die Erstellung jeder Rollenvorlage optimiert und erfordert keine komplizierte Bedingung, die mit jeder möglichen Stellenbezeichnung abgeglichen werden kann.

>[!ENDSHADEBOX]

## Zugreifen auf die konfigurierten Personas

1. Wählen Sie in der linken Navigation **[!UICONTROL Administration]** > **[!UICONTROL Konfigurationen]**.

1. Klicken Sie **[!UICONTROL Zwischenbereich auf]** Persona-Zuordnung“, um die Liste der Personas anzuzeigen.

   ![Zugriff auf die konfigurierten Personas](./assets/configuration-engagement-scoring-list.png){width="800" zoomable="yes"}

   Auf dieser Seite können Sie [erstellen](#create-an-engagement-score-model), [bearbeiten](#change-the-engagement-weighting-settings) oder [löschen](#delete-a-persona).

   Die Persona-Zuordnungsliste. ist als Tabelle organisiert und zeigt oben die zuletzt aktualisierten Personas an (sortiert nach &quot;_[!UICONTROL Aktualisierung]_). Sie können die angezeigte Tabelle anpassen, indem Sie auf das Symbol _Spalteneinstellungen_ ( ![Spalteneinstellungen](../assets/do-not-localize/icon-column-settings.svg) ) in der oberen rechten Ecke klicken und die Kontrollkästchen für die Spalten aktivieren oder deaktivieren.

![Spalten für die Anzeige in der Persona-Zuordnungsliste](./assets/configuration-engagement-scoring-list-columns.png){width="300"}

1. Um auf die Details einer Rolle zuzugreifen, klicken Sie auf den Namen.

### Standard-Personas

Die _Persona-Zuordnung_ enthält fünf standardmäßige Personas, die anhand des Attributs für die Auftragstitel definiert werden. Sie können jede dieser Standardpersonas entsprechend den Anforderungen Ihres Unternehmens bearbeiten:

| Persona | Stellenbezeichnungen |
| ------- | ---------- |
| CXO / EVP - CXO / Executive Vice President | CEO, CIO, CTO, CMO, CFO, Executive Vice President of Strategy |
| SVP / VP - Senior Vice President / Vice President | SVP Marketing, VP Sales, SVP Operations, VP Product, VP IT |
| Senior Director / Director - Senior Director / Director | Director of Engineering, Senior Director of Product, Director of Finance, Director of Customer Success |
| Senior Manager/Manager - Senior Manager/Manager | Senior Marketing Manager, IT Manager, Operations Manager, Sales Manager, HR Manager |
| Einzelner Mitwirkender - Einzelner Mitwirkender | Kundenbetreuer, Software-Ingenieur, Marketing-Spezialist, Customer Success-Vertreter |
| Analyst - Analyst | Business Analyst, Data Analyst, Market Research Analyst, Financial Analyst, Operations Analyst |
| Entwickler - Entwickler | Frontend-Entwickler, Backend-Entwickler, Full-Stack-Entwickler, Mobile-App-Entwickler, DevOps-Ingenieur |
| Professionelles Personal - Professionelles Personal | HR Specialist, Legal Counsel, Compliance Officer, Project Manager, Procurement Specialist |
| Berater - Berater | Unternehmensberater, IT-Berater, Business Process Consultant, Marketing Consultant |
| Andere - Andere | Branchenspezialist, unabhängiger Berater, freiberuflicher Berater, Fachexperte |

### Filtern von Listen

Verwenden Sie die Such- und Filter-Tools, um die gewünschte Rolle zu finden:

* Geben Sie eine Textzeichenfolge in die Suchleiste ein, um Personas nach Namen abzugleichen.

  ![Filtern Sie die angezeigten Ereignisdefinitionen](./assets/configuration-events-defs-list-filtered.png){width="700" zoomable="yes"}

* Klicken Sie oben links auf _Filter_-Symbol ![Filtersymbol](../assets/do-not-localize/icon-filter.svg) ), um die angezeigte Liste mithilfe eines der folgenden Attribute zu filtern:

   * ?
   * ?

## Persona erstellen

1. Wählen Sie in der linken Navigation **[!UICONTROL Administration]** > **[!UICONTROL Konfiguration]** aus.

1. Klicken Sie **[!UICONTROL Zwischenbereich auf]** Persona-Zuordnung“.

1. Klicken Sie **[!UICONTROL Persona erstellen]**.

1. Geben Sie einen eindeutigen **[!UICONTROL Namen]** und **[!UICONTROL Beschreibung]** (optional) für die Rolle ein.

1. Wählen Sie die Attribute aus, die für die Zuordnung der Rolle verwendet werden sollen.

   * Klicken Sie **[!UICONTROL Personenattribute auswählen]**.

   * Aktivieren _[!UICONTROL im Dialogfeld &quot;]_ auswählen“ das Kontrollkästchen für jedes Attribut, das Sie zuordnen möchten (maximal fünf).

     Sie können die angezeigte Tabelle anpassen, indem Sie auf das Symbol _Spalteneinstellungen_ ( ![Spalteneinstellungen](../assets/do-not-localize/icon-column-settings.svg) ) in der oberen rechten Ecke klicken.

     Um die Attributliste nach Namen zu filtern, geben Sie eine Textzeichenfolge in die Suchleiste ein. Sie können auch auf das Symbol _Filter_ ( ![Filtersymbol](../assets/do-not-localize/icon-filter.svg) ) oben links klicken, um die angezeigte Liste nach Typ, _Standard_ oder _Benutzerdefiniert_ zu filtern.

   * Klicken Sie auf **[!UICONTROL Speichern]**.

     Die ausgewählten Attribute werden im Abschnitt &quot;_[!UICONTROL -Attribute]_ ausgefüllt.

1. Geben Sie für jedes Attribut die kommagetrennten Werte ein, denen Sie für das Attribut entsprechen möchten.

   Anstelle eines Werts können Sie auch eine Eingabeaufforderung hinzufügen, mit der eine Übereinstimmung identifiziert werden kann. Sie können beispielsweise Folgendes eingeben

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

## Persona bearbeiten

1. Um auf die Details der Rolle zuzugreifen, klicken Sie auf den Namen.


## Persona löschen

Wenn Sie eine Rolle löschen, wird sie aus der Liste _Persona-Zuordnung_ entfernt und ist nicht mehr für die Verwendung in Rollenvorlagen verfügbar.

1. Suchen Sie auf _[!UICONTROL Seite]_ Persona-Zuordnung“ die Persona, die Sie löschen möchten.

1. Klicken Sie neben dem Namen auf das Symbol mit den Auslassungspunkten (**…**) für und wählen Sie **[!UICONTROL Löschen]**.

1. Klicken Sie im Bestätigungsdialog auf **[!UICONTROL Löschen]**.
