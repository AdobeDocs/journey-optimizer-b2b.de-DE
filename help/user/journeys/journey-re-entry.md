---
title: Journey-Wiedereintritt
description: Legen Sie fest, wann und wie oft Konten dieselbe Konto-Journey erneut betreten können.
feature: Account Journeys
role: User
level: Intermediate
exl-id: e5153125-6d5b-4835-bd19-c9b7ce67e46a
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
subfeature_v2: id: c31bc6c7-76bc-467b-80c0-7315a4e3f6be
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: d00e9f03-e50b-4162-b143-0c0817c937c2
autotag-review: '2026-04-29T23:21:59.633Z'
source-git-commit: bb44a295784fbdeab2583cf7c759b15c0808d7d5
workflow-type: tm+mt
source-wordcount: 419
ht-degree: 9%

---

# Journey-Wiedereintritt

_Nur Konto-Journey_

Wenn Sie die erneute Eingabe für eine Konto-Journey aktivieren, können Sie festlegen, wann und wie oft ein Konto dieselbe Journey erneut eingeben kann. Verwenden Sie die Wiedereinstiegseinstellungen, um Kriterien, Beschränkungen und Wartezeiten festzulegen, damit die Konten sich kontrolliert für die Journey qualifizieren.

Ein Konto kann sich für eine Journey erneut qualifizieren, wenn die folgenden Elemente zutreffen:

* Das Konto befindet sich innerhalb der Anzahl der zulässigen erneuten Einträge für die Journey.
* Das Konto hat den Wartezeitschwellenwert erreicht (die Mindestwartezeit, bevor eine erneute Qualifizierung erfolgt).
* Das Konto befindet sich derzeit nicht auf der Journey.

## Erneuter Eintrag für eine Konto-Journey aktivieren

Sie können die Wiedereinstiegseinstellungen aktivieren und die Wiedereinstiegseinstellungen ändern, wenn sich die Journey im Status _Entwurf_ befindet.

1. Öffnen Sie die Journey des Kontoentwurfs.

1. Klicken Sie oben rechts auf **[!UICONTROL Mehr…]** und wählen Sie **[!UICONTROL Wiedereintritt]**.

   ![Klicken auf „Mehr“ oben rechts](./assets/account-journey-draft-more-menu.png){width="450"}

1. Schalten Sie im Dialogfeld für den erneuten ]_von_[!UICONTROL  Journey die Option **[!UICONTROL Erneuten Eintrag aktivieren]** um.

   Wenn die Funktion aktiviert ist, werden die Optionen für Timing, Verzögerung und Grenzwerte angezeigt.

   ![Dialogfeld zum erneuten Eingeben von Journey mit aktivierter Funktion](./assets/journey-re-entry-dialog-enabled.png){width="450"}

1. Wählen **[!UICONTROL für die Zeitplanung]** erneuten Eintritt die Art der Wartezeit:

   * **[!UICONTROL Warten ab Ende der Journey]** - Die Wartezeit beginnt, wenn das Konto beendet wird oder die Journey abschließt. Zum Beispiel: „30 Tage, nachdem das Konto die Journey abgeschlossen hat, kann es erneut eintreten.“

   * **[!UICONTROL Warten ab dem Start des Journey]** - Die Wartezeit basiert darauf, wann das Konto zum ersten Mal auf die Journey zugegriffen hat. Zum Beispiel: „30 Tage nach dem Start des Kontos für die Journey können sie erneut eingeben.“

1. Legen Sie die **[!UICONTROL Wiedereinstiegsverzögerung]** fest, d. h. die Wartezeit in Stunden oder Tagen.

   Diese Einstellung legt fest, wie lange ein Konto nach dem Beenden oder Starten der Journey warten muss, bevor es erneut eintreten kann.

1. Legen Sie die **[!UICONTROL Eintrittsbeschränkung]** fest, um festzulegen, wie oft ein Konto maximal auf die Journey zugreifen darf.

   Wenn ein Konto das Limit erreicht, ist es nicht mehr für die Eingabe qualifiziert, bis das Limit zurückgesetzt oder die Journey mit einem neuen Limit erneut veröffentlicht wurde.

   Dieser Grenzwert gilt pro Konto für diese Journey.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Account Progress and Activity

Bei veröffentlichten Account-Journey zeigt die Journey-Zuordnung [Account-Fortschritt](./journeys-overview.md#review-account-progression) für die Journey-Knoten an. Jeder Knoten in der Map zeigt die Anzahl der Konten an, die diesen Knoten erreichen, sowie bei Live-Journeys die Anzahl der Konten, die sich aktuell an diesem Knoten befinden. Jedes Mal, wenn ein Konto eine Journey erneut betritt, zählt es als eigenständiger Eintrag.

<!-- 
You can see how many times accounts have entered the journey. ?? 

When you drill in to [account details](../accounts/account-details.md), the account activity shows each time the account entered the journey. It includes explicit activity and a recurrence count so that you can see re-entries clearly.
-->
