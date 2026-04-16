---
title: Warteknoten
description: Verwenden Sie Warteknoten, um den Journey-Fortschritt anzuhalten und den Beendigungszeitpunkt nach Dauer, Datum oder erweiterten Tag- und Zeiteinstellungen zu steuern.
feature: Account Journeys, Person Journeys
role: User
exl-id: fecab788-4e8e-490a-bcca-bc3ab43411d9
source-git-commit: 944d2616fa21e7f8d2f8c439eaa2f5e529dacb84
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 0%

---

# Warteknoten

Verwenden Sie _Knoten_ Warten“, wenn Sie den Journey-Fortschritt für eine bestimmte Dauer anhalten möchten, bevor Sie mit dem nächsten Schritt fortfahren.

Es gibt zwei Möglichkeiten, die Wartezeit zu definieren:

* Ein bestimmtes Datum, an dem Sie zum nächsten Knoten auf der Journey wechseln möchten
* Eine relative Dauer (Anzahl der Minuten, Stunden, Tage, Wochen oder Monate)

## Warteknoten hinzufügen

1. Navigieren Sie zur Journey-Karte.

1. Klicken Sie auf das Pluszeichen ( **+** ) in einem Pfad und wählen Sie **[!UICONTROL Warten]** aus.

   ![Journey-Knoten hinzufügen - warten](./assets/add-node-wait.png){width="440"}

1. Legen Sie in den Knoteneigenschaften auf der rechten Seite den **[!UICONTROL Typ]** der Wartezeit fest, bevor die Journey zum nächsten Knoten im Pfad fortgesetzt wird.

   * **[!UICONTROL Dauer]** - Definiert eine bestimmte Anzahl von Tagen, Stunden oder Minuten, die zwischen dem Eintritt und dem Austritt des Warteknotens vergehen sollen.
   * **[!UICONTROL Datum]** - Geben Sie ein bestimmtes Datum und eine bestimmte Uhrzeit für den Ausgang an.

   ![Journey-Knoten - Warten](./assets/node-wait.png){width="500"}

## Erweiterte Warteeinstellungen

Aktivieren Sie die Option **[!UICONTROL Muss enden am]**, um einen _erweiterten_&quot; zu konfigurieren und sicherzustellen, dass Ihre Nachrichten Personen und Kontomitglieder zum optimalen Zeitpunkt erreichen. Mit dieser Konfiguration können Sie genau steuern, wann eine Person oder ein Konto einen Warteschritt beendet und zum nächsten Knoten auf der Journey übergeht. Anstatt eine feste Anzahl von Stunden oder Tagen von der Ein- bis zur Ausreise zu definieren, können Sie Aktionen so planen, dass sie zu bestimmten Zeiten und an bestimmten Wochentagen stattfinden.

Mit einem _erweiterten Warteschritt_ definieren Sie **_wann_** die Person oder das Konto beenden soll, nicht nur, wie lange sie warten soll.

![Journey-Knoten - erweiterter Warteschritt](./assets/node-wait-advanced.png){width="500"}

### Wartetypen

| Wartetyp | Beschreibung | Konfiguration |
| --------- | ----------- | ------------- |
| **Bestimmte Tageszeit** | Anhalten bis zu einem bestimmten Zeitpunkt (z. B. 9:00 h) | Uhrzeit (Stunde und Minute) einstellen. Beendet den Vorgang beim nächsten Vorkommen dieser Zeit (für die ausgewählte Zeitzone). |
| **Bestimmter Wochentag** | Halten Sie bis zu einem bestimmten Tag (z. B. Dienstag) | Einen Wochentag auswählen. Wenn keine Uhrzeit angegeben ist, erfolgt der Austritt um Mitternacht (für die ausgewählte Zeitzone) am nächsten übereinstimmenden Tag. |
| **Tagesbereich oder Kombination** | Anhalten bis zu einem beliebigen Tag innerhalb eines Bereichs (z. B. Montag bis Freitag) oder an einem der angegebenen Tage | Zieltage auswählen. Wenn keine Uhrzeit angegeben ist, erfolgt der Austritt um Mitternacht (für die ausgewählte Zeitzone) am nächsten übereinstimmenden Tag. |
| **Zeit + Tag-Kombination** | Kombinieren Sie beide für eine präzise Planung (z. B. Dienstag um 10 :00 Uhr) | Wählen Sie Ihre Zieltage und legen Sie die Zielzeit fest. Beendet am nächsten Tag/zur nächsten Uhrzeit (für die ausgewählte Zeitzone). |

### Häufige Szenarien

Die folgenden Szenarien veranschaulichen, wie Sie typische Szenarien auf Ihre Warteknotenkonfiguration anwenden können:

+++E-Mail-Ankunft während der Geschäftszeiten

**Szenario:** vermarkten Sie an B2B-Kunden, die E-Mails bei der Arbeit lesen. Sie möchten, dass alle E-Mails während der Geschäftszeiten eintreffen.

**Lösung:** Konfigurieren Sie Ihren Warteschritt, um Leads um :00 Uhr an Wochentagen (Montag bis Freitag) freizugeben. Unabhängig davon, wann ein Lead den Warteknoten betritt, erhält er Ihre E-Mail während der Geschäftszeiten.

+++

+++Konsistente Sendezeiten für dynamische Zielgruppen

**Szenario:** Ihre Zielgruppe ändert sich täglich, wenn neue Konten oder Leads qualifiziert werden. Sie möchten, dass alle Leads die erste E-Mail gleichzeitig erhalten, unabhängig davon, wann sie sich qualifiziert haben.

**Lösung:** Sie den Warteschritt so, dass er zu einem bestimmten Zeitpunkt (z. B. 10 :00) endet. Alle Leads, ob um Mitternacht oder Mittag qualifiziert, verlassen den Warteschritt gemeinsam um 10 :00 Uhr.

+++

+++SLA-konforme Folgeaufgaben

**Szenario:** Ihr Vertriebsteam verfügt über eine zweitägige SLA, um für Marketing qualifizierte Account-Leads nachzuverfolgen. Wochenenden zählen nicht.

**Lösung:** Konfigurieren Sie den Warteschritt, um Leads nur an Werktagen freizugeben. Ein am Freitag qualifizierter Lead wird zur Nachverfolgung am Montag oder Dienstag weitergeleitet, nicht über das Wochenende.

+++

### Beispiele für Ein- und Austritte

| Wartekonfiguration | Konto-/Lead-Eintritte | Konto-/Lead-Ausstiege |
| ------------------ | ------------------- | ------------------ |
| 9:0000, jeden Tag | Montag 11:00 h | Dienstag 9:00 h |
| 9:0000, jeden Tag | Montag 7:00 h | Montag 9:00 h |
| Dienstag, keine Zeit festgelegt | Freitag 15:0000 Uhr | Dienstag 12:00 h |
| 10:00 h, Montag-Freitag | Samstag 14 :00 | Montag 10:00 h |
| 10:00 h, Montag-Freitag | Mittwoch 8:00 h | Mittwoch :00 Uhr |
