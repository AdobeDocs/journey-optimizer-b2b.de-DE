---
title: Sales Alert-E-Mail
description: Erfahren Sie, wie Sie eine E-Mail mit automatisiertem Verkaufswarnhinweis in Ihre Journey einschließen.
feature: Email Authoring, Content
exl-id: 01bffbce-6c73-483a-8731-de4e5569cf61
source-git-commit: 33bd8f68ae581d974fc52f94df6f2249d9493325
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 3%

---

# Warnungen-E-Mail für Vertrieb

Eine _E-Mail mit einer Verkaufswarnung_ signalisiert die Übergabe von Einkaufsgruppen an den Verkauf. Die E-Mail enthält eine Zusammenfassung der Einkaufsgruppe und Informationen über die Mitglieder der Einkaufsgruppe und ihre Aktivitäten.

Als Marketing-Experte können Sie einen E-Mail-Knoten für Verkaufswarnungen in Ihren Journey konfigurieren, um Ihr Verkaufsteam über den Abschluss der Journey für bestimmte Einkaufsgruppen zu informieren. Innerhalb des Knotens können Sie die E-Mail-Adressen des Verkaufsteams oder einen Verteilungsalias angeben, der eine Reihe von Konten erreicht.

## E-Mail-Inhalt

+++E-Mail mit Beispielverkaufswarnung
![Beispiel einer E-Mail mit einem Verkaufswarnhinweis unter Verwendung der Standardvorlage](./assets/sales-alert-email-example.png){width="500" zoomable="yes"}

+++

| Abschnitt | Name | Beschreibung |
| - | ---- | ----------- |
| Gruppeninformationen kaufen | Name der Gruppe kaufen | Anzeigename für die Kaufgruppe. |
|   | Kontoname | Name des Kontos. |
|   | Engagement-Bewertung | Interaktionsbewertung der Einkaufsgruppe basierend auf aktiven Interaktionsaktivitäten in den letzten 30 Tagen. |
|   | Vollständigkeitsbewertung | Vollständigkeitsbewertung der Einkaufsgruppe. |
|   | Lösungsinteresse | Lösungsinteresse in Verbindung mit der Einkaufsgruppe&quot; |
|   | Status | Status der Einkaufsgruppe. |
| Gruppenhervorhebungen kaufen | Topbeteiligte Mitglieder | Topbeteiligte Mitglieder der Einkaufsgruppe durch Kauf der Interaktionsbewertung und Rolle der Gruppenmitglieder. |
|   | Thema von Interesse | Die häufigsten Suchbegriffe, die bei der Interaktion mit Inhalten auftreten, basieren auf E-Mails, Downloads, Chat, PDF-Review, Aktivitätszusammenfassung und Webinar-Fragen. |
|   | Fehlende Rollen | Obligatorische Rollen in der Vorlage, fehlen jedoch in der Gruppe &quot;Einkauf&quot;. |
| Zusammenfassung der Gruppe kaufen | Aktivitätszusammenfassung (basierend auf generativer KI) | KI generierte Zusammenfassung der Einkaufsgruppe basierend auf den Aktivitäten der Mitglieder. Die Aktivitäten der letzten 30 Tage werden berücksichtigt. |
|   | Wichtige interessante Momente | Jüngste interessante Momente im Zusammenhang mit den Mitgliedern der Einkaufsgruppe. |
| Mitglieder | Liste von vier Buying Members | Details der vier wichtigsten Mitglieder der Einkaufsgruppe nach Interaktionsbewertung und Rolle. |
| Jedes Mitglied einer Einkaufsgruppe | Name des Mitglieds | Name des Mitglieds der Einkaufsgruppe. |
|   | Titel | Titel des Mitglieds der Einkaufsgruppe. |
|   | Role | Die Rolle &quot;Buying group&quot;des Mitglieds. |
|   | Engagement-Bewertung | Interaktionsbewertung der Gruppenmitglieder. Das Ergebnis basiert auf aktiven Interaktionsaktivitäten der letzten 30 Tage. |
|   | Letzter interessanter Moment | Der neueste interessanteste Moment bezogen sich auf das Mitglied. |
|   | Letzte Aktivitäten | Die letzten beiden Aktivitäten bezogen sich auf das Mitglied der Gruppe. |
|   | E-Mail-ID | E-Mail-ID des Käufergruppenmitglieds. |
|   | Telefonnummer | Telefonnummer des Mitglieds der Einkaufsgruppe. |

## Hinzufügen einer E-Mail-Aktion mit Verkaufswarnungen in einer Konto-Journey

Sie können E-Mail-Sendungen zu Verkaufswarnungen auf einer Konto-Journey einrichten, wenn Sie einen Knoten vom Typ _[!UICONTROL Aktion durchführen]_ hinzufügen und folgende Schritte ausführen:

1. Wählen Sie für das Ziel _[!UICONTROL Aktion für]_ die Option **[!UICONTROL Konto]**.

1. Wählen Sie für _[!UICONTROL Aktion für Konten]_ die Option **[!UICONTROL Warnung zum Verkauf senden]**.

1. Wählen Sie für **[!UICONTROL Lösungsinteresse auswählen]** das Lösungsinteresse für den generierten E-Mail-Inhalt aus.

1. Geben Sie für &quot;**[!UICONTROL E-Mail senden an]**&quot;jede E-Mail-Adresse oder jeden Alias ein, die/den Sie für den Versand einbeziehen möchten.

   ![Neues E-Mail-Dialogfeld erstellen](assets/sales-alert-email-journey-node.png){width="600" zoomable="yes"}

   Nach der Veröffentlichung der Konto-Journey wird die Verkaufswarnung entsprechend diesen Parametern bereitgestellt.
