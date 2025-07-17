---
title: Details der Einkaufsgruppe
description: Erfahren Sie mehr über den Zugriff auf detaillierte Informationen und Zusammenfassungen der generativen KI für Einkaufsgruppen in Journey Optimizer B2B edition.
feature: Buying Groups, Intelligent Insights
role: User
exl-id: f14301dc-d605-4ed2-8867-6a49675019de
source-git-commit: 65c7bdcc998c604125442fbd0a65c2f8ebd3255d
workflow-type: tm+mt
source-wordcount: '779'
ht-degree: 4%

---

# Details zu Käufergruppen

Wenn Sie in Journey Optimizer B2B edition von einer beliebigen Stelle auf einen Einkaufsgruppennamen klicken, werden die Details der Einkaufsgruppe angezeigt. Diese Übersicht enthält nützliche Informationen zur Einkaufsgruppe, einschließlich der Zusammenfassungen zur generativen KI. Es gibt auch [Aktionen](#buying-group-actions) die Sie für Kontakte ausführen können, die mit dem Konto verknüpft sind.

![Auf Details der Einkaufsgruppe zugreifen](./assets/buying-group-details.png){width="800" zoomable="yes"}

Verwenden Sie die **[!UICONTROL Übersicht]**, um Informationen über das Konto zu überprüfen, und die Registerkarte **[!UICONTROL Mitglieder]**, um auf eine Liste der Mitglieder der Einkaufsgruppe zuzugreifen.

## Registerkarte „Überblick“

Die Registerkarte Übersicht besteht aus drei Hauptabschnitten:

### Zusammenfassung der Einkaufsgruppe

![Zusammenfassung der Einkaufsgruppe](./assets/details-page-buying-group-overview.png){zoomable="yes"}

Der Abschnitt Zusammenfassung der Einkaufsgruppe enthält die folgenden Informationen zur Einkaufsgruppe:

* Käufergruppenname
* Kontoname (klicken Sie auf den Namen, um die [Kontodetails](../accounts/account-details.md) zu öffnen
* Anzahl der Mitglieder in der Einkaufsgruppe
* Interaktionsbewertung
* Vollständigkeitsbewertung
* Aktuelle Einkaufsgruppenphase
* Rollenvorlage (auf den Namen klicken, um die [Rollenvorlage) ](buying-groups-role-templates.md#access-and-browse-role-templates).
* Datum der letzten Änderung/Aktualisierung
* Generative KI-Zusammenfassung der Einkaufsgruppe

### Kontoübersicht

![Einkaufsgruppenkonto - Übersicht](./assets/details-page-buying-group-account-overview.png){zoomable="yes"}

Der Abschnitt Kontoübersicht enthält die folgenden Kontoinformationen:

* Kontoname (auf den Namen klicken, um die Kontodetails zu öffnen)
* Anzahl der Personen im Konto
* Branche
* Offene Chancen
* Die letzten drei Konto-Journey, in denen das Konto derzeit verwendet wird (klicken Sie auf den Namen, um die Journey-Details zu öffnen)
* Generative KI-Zusammenfassung des Kontos

### Absichtsdaten

In Journey Optimizer B2B edition prognostiziert das Modell der Absichtserkennung eine Lösung/ein Produkt von Interesse mit ausreichend hoher Zuverlässigkeit, basierend auf der Aktivität der kaufenden Gruppenmitglieder. Die Absicht, Gruppenmitglieder zu kaufen, kann als die Wahrscheinlichkeit interpretiert werden, dass sie Interesse an einem Produkt haben.

{{intent-data-note}}

![Absichtsdaten - Details der Einkaufsgruppe](../accounts/assets/intent-data-panel.png){width="700" zoomable="yes"}

* Absichtsebenen
* Arten von Intent-Signalen - Schlüsselwörter, Produkt und Lösung

### Käufergruppenmitglieder

![Käufliche Gruppenmitglieder](./assets/details-page-buying-group-members.png){width="800" zoomable="yes"}

Der Abschnitt _[!UICONTROL Käufliche Gruppenmitglieder]_ zeigt zwei Zeilen, die Käufliche Gruppenmitglieder hervorheben:

* **[!UICONTROL Entscheidungsträger]** - Die drei wichtigsten Entscheidungsträger basierend auf der Bewertung der Interaktion mit Personen
* **[!UICONTROL Am häufigsten engagierte Mitglieder]** - Andere am häufigsten engagierte Mitglieder auf der Grundlage des Personeninteraktionswerts

Jede Mitgliedskarte enthält die folgenden Details:

* Name
* Titel
* Rolle
* Bewertung der Lead-Interaktion

Klicken Sie **[!UICONTROL Details anzeigen]**, um auf die folgenden Mitgliedsinformationen zuzugreifen:

* Generative KI-Zusammenfassung
* Letzter interessanter Moment
* Zuletzt durchgeführte Aktivitäten (zwei)
* Andere Einkaufsgruppen, in denen der Lead Mitglied ist (begrenzt auf drei Einkaufsgruppen basierend auf der zuletzt hinzugefügten).
* E-Mail-Adresse
* Telefonnummer

![Weitere Details für ein Mitglied einer Einkaufsgruppe anzeigen](./assets/details-page-buying-group-members-view-details.png){width="600" zoomable="yes"}

## Mitglieder-Registerkarte

Wählen Sie die **[!UICONTROL Mitglieder]**, um eine Liste aller Mitglieder der Einkaufsgruppe anzuzeigen. Jede Mitgliederliste enthält den Namen, die Funktion, die Stellenbezeichnung, die E-Mail-Adresse, die Telefonnummer und die Quelle.

![Registerkarte „Mitglieder“ - Details der Einkaufsgruppe](./assets/buying-group-details-members-tab.png){width="700" zoomable="yes"}

Es gibt mehrere Aktionen, die Sie über die Registerkarte _Mitglieder_ ausführen können:

### Neues Mitglied zuweisen

Einem Konto können eine oder mehrere Einkaufsgruppen zugeordnet sein. Einkaufsgruppenmitglieder sind in der Regel eine Untergruppe von Kontakten aus dem Konto. Sie können der Einkaufsgruppe manuell einen beliebigen Kontakt aus dem zugehörigen Konto hinzufügen.

1. Klicken **[!UICONTROL oben]** auf „Neues Mitglied zuweisen“.

1. Wählen _[!UICONTROL im Dialogfeld &quot;]_ zuweisen“ die Leads aus, die Sie der Einkaufsgruppe hinzufügen möchten, und klicken Sie auf **[!UICONTROL Weiter]**.

   ![Registerkarte „Mitglieder“ - Neue Mitglieder zuweisen](./assets/buying-group-details-assign-member.png){width="700" zoomable="yes"}

1. Wählen _[!UICONTROL im Dialogfeld „Neue]_ bearbeiten“ die Rolle aus, die jedem der neuen Mitglieder zugewiesen werden soll.

   ![Registerkarte „Mitglieder“ - Neue Mitgliederrolle zuweisen](./assets/buying-group-details-assign-member-edit-role.png){width="700" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Speichern]**.

### Mitglied entfernen

Sie können ein oder mehrere ausgewählte Mitglieder (bis zu 50 gleichzeitig) aus der Einkaufsgruppe entfernen.

1. Aktivieren Sie die Kontrollkästchen der Mitglieder, die Sie entfernen möchten.

1. Klicken Sie unten in der Auswahlleiste auf **[!UICONTROL Mitglieder entfernen]**.

   ![Registerkarte „Mitglieder“ - Mitglieder entfernen](./assets/buying-group-details-remove-selected.png){width="700" zoomable="yes"}

1. Klicken Sie im Bestätigungsdialogfeld auf **[!UICONTROL Entfernen]**.

### Rolle bearbeiten

Sie können die Rolle für ein oder mehrere ausgewählte Mitglieder (bis zu 50 gleichzeitig) der Einkaufsgruppe ändern.

1. Aktivieren Sie die Kontrollkästchen der Mitglieder, deren Rollen geändert werden sollen.

1. Klicken Sie unten in der Auswahlleiste auf **[!UICONTROL Rollen bearbeiten]**.

   ![Registerkarte „Mitglieder“ - Rollen bearbeiten](./assets/buying-group-details-edit-roles.png){width="700" zoomable="yes"}

1. Wählen _[!UICONTROL im Dialogfeld &quot;]_ bearbeiten“ die Rolle aus, die den einzelnen Mitgliedern zugewiesen werden soll.

   ![Mitgliederrollen bearbeiten - Rollen auswählen](./assets/buying-group-details-edit-roles-choose-roles.png){width="700" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Speichern]**.

### E-Mail senden

Sie können eine von einem Marketer genehmigte E-Mail an ein oder mehrere ausgewählte Mitglieder (bis zu 50 gleichzeitig) einer Einkaufsgruppe senden. Die Liste der verfügbaren E-Mails ist auf genehmigte E-Mails aus der verbundenen Marketo Engage-Instanz beschränkt.

1. Aktivieren Sie die Kontrollkästchen der Mitglieder, die Sie die E-Mail erhalten möchten.

1. Klicken Sie oben rechts oder in der Auswahlleiste unten auf **[!UICONTROL E-Mail senden]**.

   ![Registerkarte „Mitglieder“ - E-Mail senden](./assets/buying-group-details-send-email.png){width="700" zoomable="yes"}

1. Wählen _[!UICONTROL Dialogfeld „E]_ Mail senden“ den Marketo Engage-Arbeitsbereich aus und aktivieren Sie dann das Kontrollkästchen für die zu sendende E-Mail.

   ![Wählen Sie eine E-Mail aus, die an kaufende Gruppenmitglieder gesendet werden soll](../accounts/assets/account-details-send-email-dialog.png){width="700" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Senden]**.
