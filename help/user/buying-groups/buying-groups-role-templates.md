---
title: Einkaufsgruppen-Rollenvorlagen
description: Erstellen Sie Rollenvorlagen mit bedingter automatischer Zuweisung, um Entscheidungsträger und Stakeholder für Einkaufsgruppen in Journey Optimizer B2B edition zu identifizieren.
feature: Buying Groups
role: User
exl-id: 9206356e-e9cf-486c-8982-c7d893222413
source-git-commit: bd6dff55621943dc349b47b99f24afefe5b9a514
workflow-type: tm+mt
source-wordcount: '1329'
ht-degree: 6%

---

# Vorlagen für Käufergruppenrollen

In einem B2B-Markt werden Kaufentscheidungen in der Regel von mehreren Personen getroffen. Diese Personen nehmen entsprechend ihrer Rolle in der Organisation am Entscheidungsprozess teil. Erstellen Sie Rollenvorlagen für Einkaufsgruppen, die eine Gruppe von Rollendefinitionen entsprechend jedem Produktangebotstyp oder Account-Anwendungsfall enthalten.

![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Übersichtsvideo ansehen](#overview-video)

## Zugreifen auf und Durchsuchen von Rollenvorlagen

1. Klicken Sie in der linken Navigation auf **[!UICONTROL Gruppen kaufen]**.

1. Wählen Sie auf _[!UICONTROL Seite]_ die Registerkarte **[!UICONTROL Rollenvorlagen]** aus.

   ![Registerkarte Rollenvorlagen](assets/roles-templates-tab.png){width="800" zoomable="yes"}

   Die Registerkarte bietet eine Bestandsliste aller vorhandenen Rollenvorlagen und zeigt die folgenden Informationen im Spaltenformat an:

   * [!UICONTROL Name]
   * [!UICONTROL Status]
   * [!UICONTROL Erstellungsdatum]
   * [!UICONTROL Erstellt von]
   * [!UICONTROL Letzte Aktualisierung]
   * [!UICONTROL Zuletzt aktualisiert von]
   * [!UICONTROL Veröffentlicht auf]
   * [!UICONTROL Veröffentlicht von]

   Die Liste ist standardmäßig nach der _[!UICONTROL Letzte Aktualisierung]_ sortiert. Alle Rollenvorlagen haben den Status `Draft` oder `Live`.

1. Um die Liste nach Namen zu filtern, verwenden Sie das Suchfeld oben in der Liste.

   Geben Sie die ersten Zeichen des Namens ein, um die angezeigte Liste auf die entsprechenden Elemente zu reduzieren.

   ![Rollenvorlagen filtern nach Suchzeichenfolge](assets/roles-templates-search.png){width="700" zoomable="yes"}

## Erstellen einer Rollenvorlage

1. Klicken Sie auf _[!UICONTROL Registerkarte]_ Rollenvorlagen **[!UICONTROL oben rechts auf]** Vorlage erstellen“.

1. Geben Sie in das Dialogfeld einen eindeutigen **[!UICONTROL Namen]** (erforderlich) und **[!UICONTROL Beschreibung]** (optional) für die Vorlage ein.

   ![Dialogfeld „Rollenvorlage erstellen“](assets/roles-template-create-dialog.png){width="400"}

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

### Vorlagenrollen hinzufügen

Nachdem Sie die Vorlage erstellt haben, wird sie im Arbeitsbereich geöffnet, und Sie werden aufgefordert, die Rollen hinzuzufügen. Standardmäßig wird die erste Rollenkarte angezeigt.

Jede Rolle, die Sie für die Vorlage definieren, verwendet einen Satz von Filtern oder _Bedingungen_, um die der Rolle zugewiesenen Mitglieder zu bestimmen. Verwenden Sie die folgenden Filtertypen, um die Bedingungen für eine Rolle zu definieren:

| Typ | Bedingung |
| ---- | --------- |
| Personenattribute | <li>E-Mail-Adresse <li>E-Mail-Adresse ungültig <li>E-Mail angehalten <li>Faxnummer <li>Vorname <li>Abgeleitetes Bundesland/abgeleitete Region <li>Stellenbezeichnung <li>Last name <li>Zweiter Vorname <li>Mobiltelefonnummer <li>Engagement-Score einer Person <li>Telefonnummer <li>Postleitzahl <li>Land <li>Abbestellt <li>Grund für Abmeldung |
| Spezielle Filter | <li>Mitglied der Liste <li>Mitglied des Programms |
| Absichtsdaten | <li>Kategoriebedingung <li>Produktzweck <li>Keyword Intent<br/>[Erfahren Sie mehr über Intent-Daten](../admin/intent-data.md) |

1. Definieren Sie für die erste Rollenkarte die Rolleneigenschaften.

   * Wählen Sie die **[!UICONTROL Einkaufsgruppenrolle]** aus der Liste aus.

     Es gibt sechs Standardrollen: `Decision Maker`, `Influencer`, `Practitioner`, `Executive Steering Committee`, `Champion` und `Other`. Die Liste enthält auch alle [benutzerdefinierten Rollen), die in der Liste _Rollen_ definiert &#x200B;](./default-custom-roles.md#custom-roles).

     ![Liste der Gruppenrollen kaufen](./assets/roles-template-create-roles-list.png){width="700" zoomable="yes"}

   * Legen Sie die **[!UICONTROL Gewichtung]** für die Rolle fest, die zur Berechnung des Interaktionswerts verwendet wird.

     Der Wert für jede Option wird in einen Prozentsatz für die Score-Berechnung umgerechnet: [!UICONTROL Trivial] = 20, [!UICONTROL Minor] = 40, [!UICONTROL Normal] = 60, [!UICONTROL Important] = 80 und [!UICONTROL Vital] = 100.

     Beispiel: Eine Rollenvorlage mit Rollen, die „Wichtig“, „Normal“ und „Wichtig“ verwenden, wird dann in „100/240“, „80/240“ und „60/240“ konvertiert.

   * **[!UICONTROL Bedingungen für automatische Zuweisung hinzufügen]** - Aktivieren Sie dieses Kontrollkästchen, um Bedingungen für die automatische Zuweisung von Mitgliedern zur Einkaufsgruppe hinzuzufügen, die der Bedingung entsprechen. Wenn das Kontrollkästchen nicht aktiviert ist, ist das Hinzufügen von Bedingungen NICHT erforderlich.

   * **[!UICONTROL Erforderlich für Vollständigkeitsbewertung]** - Aktivieren Sie dieses Kontrollkästchen für die Rolle, wenn es eine Anforderung für die Berechnung eines Vollständigkeitswerts sein soll.

1. Klicken Sie **[!UICONTROL Bedingung hinzufügen]** und definieren Sie die bedingte Regel für die Rolle.

   * Erweitern Sie _[!UICONTROL Dialogfeld]_ Bedingung“ die Liste der **[!UICONTROL Personenattribute]** und suchen Sie ein Attribut, das Sie für die Rolle verwenden möchten. Ziehen Sie ihn nach rechts und legen Sie ihn im Filterbereich ab.

     ![Rollenvorlage fügt Bedingung zum Ziehen hinzu](assets/roles-template-role-attribute.png){width="700" zoomable="yes"}

     >[!NOTE]
     >
     >Wenn Sie benutzerdefinierte Personenfelder im Konto-Zielgruppenschema in Experience Platform definiert haben, sind diese Felder auch verfügbar, um als Personenattribute in Bedingungen zu verwenden.

   * Verwenden Sie das -Attribut, um mithilfe eines oder mehrerer Werte einen übereinstimmenden Filter zu erstellen.

     Im folgenden Beispiel wird das Attribut Auftragstitel verwendet, um eine Übereinstimmung für den Entscheidungsträger zu identifizieren. Jeder Wert für Titel, der mit `Director` oder `Sr Director` beginnt, wird für die Bedingung als „true“ ausgewertet.

     ![Beispiel für Rollenvorlagenbedingungen unter Verwendung des Auftragstitels](assets/roles-template-condition-example-job-title.png){width="700" zoomable="yes"}

   * Fügen Sie bei Bedarf ein weiteres Attribut und eine weitere Bedingung hinzu, um die Kriterien für eine Übereinstimmung mit der Rolle weiter zu verfeinern.

   * Klicken Sie auf **[!UICONTROL Fertig]**.

1. Klicken Sie für jede zusätzliche Rolle, die Sie in die Vorlage aufnehmen möchten, auf **[!UICONTROL Weitere Rolle hinzufügen]** und wiederholen Sie die Schritte 1 und 2, um die Rolle zu definieren.

   ![Rollenvorlage mit mehreren definierten Rollen](assets/roles-template-multiple-roles.png){width="700" zoomable="yes"}

>[!BEGINSHADEBOX &quot;Marketo Engage List Membership“]

Überprüfen Sie in Marketo Engage _Smart_ Kampagnen) die Programmmitgliedschaft, um sicherzustellen, dass Leads keine doppelten E-Mails erhalten und nicht gleichzeitig Mitglieder mehrerer E-Mail-Streams sind. In Journey Optimizer B2B können Sie die Marketo Engage-Listenmitgliedschaft als Bedingung für Ihre Rollenvorlage überprüfen, um doppelte Käufe von Gruppenmitgliedschaft und Journey-Aktivitäten zu vermeiden.

Um die Listenmitgliedschaft als Rollenbedingung zu verwenden, erweitern Sie **[!UICONTROL Spezielle Filter]** und ziehen Sie die **[!UICONTROL Mitglied der Liste]** Bedingung in den Filterbereich. Schließen Sie dann die Filterdefinition ab, um die Zugehörigkeit zu einer oder mehreren Marketo Engage-Listen zu bewerten.

![Vorlagenbedingung für Rollen für Marketo Engage-Listenmitgliedschaft](assets/roles-template-conditions-member-of-list.png){width="700" zoomable="yes"}
<br/>

>[!NOTE]
>
>**Einstellung von Funktionen**</br></br>
>
>Mit der [vereinfachten Architektur](../simplified-architecture.md) für Journey Optimizer B2B edition wird das Filtern nach Listen- oder Programmmitgliedschaften in einer Marketo Engage-Instanz nicht unterstützt.

>[!ENDSHADEBOX]

Ihre Änderungen werden automatisch im Status _Entwurf_ gespeichert. Wenn Sie die Rollenvorlage nicht veröffentlichen möchten, klicken Sie auf den Pfeil nach links (zurück) oben auf der Seite und kehren Sie zur Liste _[!UICONTROL Rollenvorlagen]_ zurück.

### Ändern der Vollständigkeitsbewertungseinstellungen

Standardmäßig wird die Vollständigkeit für eine Rolle als ein der Rolle zugewiesenes Mitglied definiert. Wenn Sie die Vollständigkeit der Einkaufsgruppe als Indikator für die Verkaufsbereitschaft oder den <!-- journey decisioning coming later--> verwenden möchten, können Sie diese Einstellungen verwenden, um die Punktzahl an die Anzahl der Mitglieder pro Rolle anzupassen, die zum Schließen einer Opportunity erforderlich sind.

Wenn Sie beispielsweise ein Geschäft für Ihre Lösung _X_ abschließen möchten, müssen mehrere Marketing-Entscheidungsträger identifiziert und einbezogen werden, da mehrere Marketing-Teams in einem Unternehmen die Lösung verwenden würden. In diesem Fall möchten Sie den Schwellenwert erhöhen, um eine _vollständige_ Einkaufsgruppe zu berechnen, indem Sie mindestens zwei Marketing-Entscheidungsträger benötigen.

Unter [Vollständigkeitswerte](./completeness-scores.md) finden Sie detaillierte Informationen zur Bewertung und Berechnung der Vollständigkeit.

1. Klicken Sie oben rechts auf der Seite mit der Rollenvorlage auf **[!UICONTROL Vollständigkeitsbewertungseinstellungen]**.

   ![Schaltfläche „Rollenvorlage - Vollständigkeit der Bewertungseinstellungen“](./assets/buying-group-details-edit-roles-completeness-settings.png){width="700" zoomable="yes"}

1. Ändern Sie im Dialogfeld den Wert **[!UICONTROL Mitglieder erforderlich]** für jede definierte Rolle nach Bedarf.

   Sie können den Wert eingeben oder auf **&plus;** oder **−** klicken, um den Wert zu erhöhen oder zu verringern.

   ![Schaltfläche „Rollenvorlage - Vollständigkeit der Bewertungseinstellungen“](./assets/buying-group-details-edit-roles-completeness-settings-dialog.png){width="450"}

1. Klicken Sie auf **[!UICONTROL Speichern]**.

### Veröffentlichen der Rollenvorlage

Wenn die Vorlage einsatzbereit ist, klicken Sie oben **[!UICONTROL auf]** Veröffentlichen“.

Durch das Veröffentlichen der Vorlage wird der Status auf _Live_ gesetzt und für die Verknüpfung mit einer interessanten Lösung verfügbar gemacht. Es muss mindestens eine definierte Rolle vorhanden sein, um die Rollenvorlage zu veröffentlichen.

## Bearbeiten einer Vorlage für Aufgabenentwürfe

Wenn sich eine Rollenvorlage im Status _Entwurf_ befindet, können Sie die definierten Rollen weiter bearbeiten. Alle von Ihnen vorgenommenen Änderungen werden automatisch gespeichert.

Ändern Sie alle Einstellungen in der Kopfzeile der Rollenkarte, einschließlich der Rolle der Einkaufsgruppe, der Gewichtung, der automatischen Zuweisung und der Vollständigkeitsbewertung.

![Eigenschaften der Einkaufsgruppenrolle ändern](./assets/roles-template-role-properties.png){width="600"}

### Bedingungen für eine Rolle ändern

Um die Bedingungs-/Filterlogik für eine der Rollen zu ändern, klicken Sie auf _Bearbeiten_ ( ![Bearbeiten-Symbol](../assets/do-not-localize/icon-edit.svg) ) oben rechts in der Rollenkarte. Diese Aktion öffnet den Arbeitsbereich _[!UICONTROL Bedingungen]_ in dem Sie einen vorhandenen Filter ändern, einen Filter hinzufügen oder entfernen oder die Filterlogik ändern können.

### Löschen einer Rollenkarte

Wenn Sie eine Rolle aus der Vorlage entfernen möchten, klicken Sie auf das Symbol _Löschen_ ( ![Löschsymbol](../assets/do-not-localize/icon-delete.svg) ) in der Rollenkarte.

### Festlegen der Priorität für Rollen

Sie können die Rollen in der Vorlage neu anordnen, wodurch die Priorität für die Zuweisung von Leads zu einer Rolle festgelegt wird. Rechts neben jeder **[!UICONTROL wird ein Controller]** Priorität“ angezeigt. Klicken Sie auf den _Nach_ oder _Nach-unten_ Pfeil auf der rechten Seite, um die Rollenkarte nach oben oder unten zu verschieben.

![Rollenpriorität ändern](./assets/roles-template-role-priority.png){width="700"}

## Löschen einer Rollenvorlage

Sie können eine Rollenvorlage löschen, wenn sie sich im Status _Entwurf_ befindet.

1. Wählen Sie die Rollenvorlage aus der Liste aus, um sie zu öffnen.

1. Klicken **[!UICONTROL oben]** auf „Löschen“.

   ![Rollenpriorität ändern](./assets/roles-template-delete.png){width="700"}

1. Klicken Sie im Dialogfeld zur Bestätigung **[!UICONTROL Löschen]**.

## Übersichtsvideo

>[!VIDEO](https://video.tv.adobe.com/v/3453310/?captions=ger&learn=on)
