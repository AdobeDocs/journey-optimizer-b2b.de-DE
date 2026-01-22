---
title: Kontodetails
description: Account Insights mit KI-Zusammenfassungen, Absichtserkennung, Kontaktabdeckungsanalyse und E-Mail-Nachrichten in Journey Optimizer B2B edition anzeigen.
feature: Account Insights
role: User
exl-id: 12be33de-0a43-43d9-90b8-fe4411a50599
source-git-commit: 2a676f3cbeb43616a75fa3fa6eb9106230b9fb40
workflow-type: tm+mt
source-wordcount: '639'
ht-degree: 6%

---

# Kontodetails

Wenn Sie in Journey Optimizer B2B edition von einer beliebigen Stelle auf einen Kontonamen klicken _wird die_ „Kontodetails“ angezeigt. Auf dieser Seite finden Sie nützliche Informationen zum -Konto, einschließlich der Zusammenfassungen der generativen KI. Es gibt auch [Aktionen](#account-actions) die Sie für Kontakte ausführen können, die mit dem Konto verknüpft sind.

![Zugriff auf Kontodetails](./assets/account-details.png){width="700" zoomable="yes"}

Verwenden Sie die **[!UICONTROL Übersicht]**, um Informationen über das Konto zu überprüfen, und die **[!UICONTROL Kontakte]**, um auf eine Liste der Kontokontakte zuzugreifen.

## Registerkarte [!UICONTROL Übersicht]

Die Seite mit den Kontodetails besteht aus drei primären Abschnitten:

### Kontoübersicht

![Kontoübersicht](./assets/details-page-account-overview.png){zoomable="yes"}

Der Abschnitt Kontoübersicht enthält die folgenden Kontoinformationen:

* Kontoname
* Anzahl der Personen im Konto
* Branche
* Offene Chancen
* Die drei neuesten Account-Journey, in denen das Account derzeit verwendet wird (klicken Sie auf den Journey-Namen, um die [Journey-Übersicht zu öffnen](../journeys/journeys-overview.md))
* Generative KI-Zusammenfassung des Kontos, die Informationen zu den aktivsten Einkaufsgruppen enthält.

### Absichtsdaten

In Journey Optimizer B2B edition prognostiziert das Absichtserkennungsmodell basierend auf der Kontokontaktaktivität eine Lösung/ein Produkt von Interesse mit ausreichend hoher Konfidenz. Die Absicht von Account-Kontakten kann als die Wahrscheinlichkeit interpretiert werden, dass ein Interesse an einem Produkt besteht.

{{intent-data-note}}

![Intent-Daten - Kontodetails](./assets/intent-data-panel.png){width="700" zoomable="yes"}

* Absichtsebenen
* Arten von Intent-Signalen - Schlüsselwörter, Produkt und Lösung


### Kontaktabdeckung

![Konto-Kontaktabdeckung](./assets/details-page-contact-coverage.png){width="800" zoomable="yes"}

Im Abschnitt _[!UICONTROL Kontaktabdeckung]_ wird die Anzahl der Kontakte aus dem Konto mit einer bestimmten Rolle angezeigt, die mit einem Lösungsinteresse verbunden ist. Die Zuweisung von Rollen und Lösungsinteressen basiert auf der Vorlage „Einkaufsgruppenrollen“. Klicken Sie auf eine Zelle, um die folgenden Details anzuzeigen:

* Beschreibung, im folgenden Format: _x Personen haben meine Rolle für ein Lösungsinteresse_
* Spalten
* Name
* Konto
* Stellenbezeichnung
* Käufergruppe
* Engagement-Score einer Person
* Letzte Aktivität
* Details

Klicken Sie oben links auf _Filter_-Symbol ![Filtersymbol](../assets/do-not-localize/icon-filter.svg) ), um die Datenanzeige mit einem der folgenden Attribute zu filtern:

* Lösungsinteresse
* Zeitraum

### Kontaktüberschneidung

![Kontokontaktüberschneidung](./assets/details-page-contact-overlap.png){width="800" zoomable="yes"}

Im Abschnitt _[!UICONTROL Kontaktüberschneidung]_ werden Kontakte aus dem Konto angezeigt, die zu mehr als einer Einkaufsgruppe gehören, da sie mit mehreren Lösungsinteressen verknüpft sind. Diese Informationen werden in Form einer Tabelle mit den folgenden Spalten bereitgestellt:

* Name
* Stellenbezeichnung
* Konto
* Lösungsinteresse

Klicken Sie auf _Information_ ( ![Informationssymbol](../assets/do-not-localize/icon-info.svg) ) neben dem Kontaktnamen, um eine Tabelle mit den folgenden Details anzuzeigen:

* Einkaufsgruppe (klicken Sie auf den Namen, um die [Einkaufsgruppendetails) &#x200B;](../buying-groups/buying-group-details.md) öffnen
* Rolle
* Lösungsinteresse
* Produktabsicht (falls [&#x200B; konfiguriert](../admin/intent-data.md))
* Produkt

Klicken Sie oben links auf _Filter_-Symbol ![Filtersymbol](../assets/do-not-localize/icon-filter.svg) ), um die Datenanzeige mit einem der folgenden Attribute zu filtern:

* Lösungsinteresse
* Rollen

## Registerkarte [!UICONTROL Kontakte]

Wählen Sie die **[!UICONTROL Kontakte]**, um eine Liste aller mit dem Account verbundenen Personen anzuzeigen, die mit Experience Platform synchronisiert werden. Jeder aufgeführte Kontakt enthält den Namen, die E-Mail-Adresse und den Interaktionswert.

![Kontodetails - Registerkarte „Kontakte“](./assets/account-details-contacts-tab.png){width="700" zoomable="yes"}

## E-Mail senden

Sie können eine von einem Marketing-Experten genehmigte E-Mail an einen oder mehrere ausgewählte Kontakte (bis zu 50 gleichzeitig) oder an alle Kontakte für das Konto senden. Die Liste der verfügbaren E-Mails ist auf genehmigte E-Mails aus der verbundenen Marketo Engage-Instanz beschränkt.

>[!BEGINTABS]

>[!TAB Alle Kontokontakte]

1. Klicken Sie auf der _[!UICONTROL Übersicht]_ oben rechts auf **[!UICONTROL E-Mail]**.

   ![Kontodetails - E-Mail auswählen](../accounts/assets/account-details-send-email.png){width="700" zoomable="yes"}

1. Wählen _[!UICONTROL Dialogfeld „E]_ Mail senden“ den Marketo Engage-Arbeitsbereich aus und aktivieren Sie dann das Kontrollkästchen für die zu sendende E-Mail.

   ![Wählen Sie eine E-Mail aus, die an kaufende Gruppenmitglieder gesendet werden soll](../accounts/assets/account-details-send-email-dialog.png){width="700" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Senden]**.

>[!TAB Ausgewählte Kontakte]

1. Aktivieren Sie auf _[!UICONTROL Registerkarte]_ die Kontrollkästchen der Kontakte, die Sie die E-Mail erhalten möchten.

1. Klicken Sie oben rechts oder in der Auswahlleiste unten auf **[!UICONTROL E-Mail senden]**.

   ![Registerkarte „Mitglieder“ - E-Mail senden](../accounts/assets/account-details-send-email-selections.png){width="700" zoomable="yes"}

1. Wählen _[!UICONTROL Dialogfeld „E]_ Mail senden“ den Marketo Engage-Arbeitsbereich aus und aktivieren Sie dann das Kontrollkästchen für die zu sendende E-Mail.

   ![Wählen Sie eine E-Mail aus, die an kaufende Gruppenmitglieder gesendet werden soll](../accounts/assets/account-details-send-email-dialog.png){width="700" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Senden]**.

>[!ENDTABS]
