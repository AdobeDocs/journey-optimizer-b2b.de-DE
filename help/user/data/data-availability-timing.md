---
title: Datenverfügbarkeit und Synchronisierungszeitpunkt
description: Erfahren Sie, wie schnell Datenänderungen in [!DNL Journey Optimizer B2B Edition] Journey angezeigt werden und welche Timelines normal sind.
feature: Journeys, Data Management
role: User
autotag-review: '2026-10-08T18:36:33.252Z'
TQID: 'https://experienceleague.adobe.com/PA1IeRHnGWHmBtDpffzveoWIHOn99-Ctt4Y0OQb7CwE'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
    internal-label: Experience Platform
  - id: b27e5950-9033-45ac-9f86-eb22e567f615
    internal-label: Marketo Engage
feature_v2:
  - id: 095e8119-1425-57eb-9d8c-9e684f2c9771
    internal-label: Audiences
  - id: 33ca0c14-7e3b-55a1-8fd7-8a61b47da4e1
    internal-label: B2B
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
    internal-label: Journeys
  - id: a50ad69b-1331-40e9-b634-531a085a6a54
    internal-label: Identities
  - id: afadf741-c5fe-42cd-8013-23bb6ff2d1bc
    internal-label: Buying Groups
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
  - id: eec185bd-7d60-4193-ba3f-da427569936a
    internal-label: Destinations
  - id: f2da1b69-6919-4386-a5d2-9c7b5c9033db
    internal-label: Data management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
    internal-label: Data integration
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
    internal-label: Data management
source-git-commit: 827c313f032d482ac2b0a5fa8f41d6506e67b9cb
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%
---
# Datenverfügbarkeit und Synchronisierungszeitpunkt {#data-availability}

Verwenden Sie dieses Thema, um zu verstehen, wie schnell Datenänderungen in Ihren [!DNL Adobe Journey Optimizer B2B Edition] Journey angezeigt werden und welche Timelines normal sind. Wenn Sie den erwarteten Zeitpunkt kennen, können Sie Journey entsprechend entwerfen und erkennen, wann eine Verzögerung das erwartete Verhalten ist.

## Erwartete Wartezeiten

| Datentyp | Typische Verfügbarkeit |
| --- | --- |
| [Zielgruppenzugehörigkeit](#daily-refresh) | Bis zu 24 Stunden (Tageszyklus) |
| [Änderungen an Konto- und Personenbeziehungen](#daily-refresh) | Bis zu 24 Stunden (Tageszyklus) |
| [Daten von [!DNL Experience Platform] bis [!DNL Journey Optimizer B2B Edition]](#platform-sync) | Bis zu 30 Minuten (nahezu in Echtzeit) |
| [Daten von [!DNL Journey Optimizer B2B Edition] bis [!DNL Experience Platform]](#platform-sync) | Bis zu vier Stunden (Mikrochargen) |
| [Aktivitätsereignisse wie Klicks und Öffnungen](#activity-and-actions) | Bis zu vier Stunden |
| [[!DNL Marketo Engage] Liste hinzufügen oder entfernen](#activity-and-actions) | Innerhalb von 30 Minuten (nahezu in Echtzeit) |
| [Von Journey Optimizer B2B Edition generierte Ereignisse](#activity-and-actions) | Nur in Batch-Zielgruppen verwendbar |
| [LinkedIn-Zielgruppenpopulation](#linkedin-timing) | Selber Tag bis 36-40 Stunden (im schlimmsten Fall) |

## Zielgruppen- und Beziehungsdaten {#daily-refresh}

[!DNL Journey Optimizer B2B Edition] bewertet die Zugehörigkeit zu Konto und Zielgruppe einer Person einmal täglich, ausgelöst durch eine Batch-Auftragsplanung. Das Ergebnis:

* Accounts oder Personen, die sich neu für eine Zielgruppe qualifizieren, können innerhalb von 24 Stunden nach dem Qualifizieren eine Journey betreten.
* Änderungen an Zielgruppenkriterien werden im nächsten täglichen Bewertungszyklus wirksam.
* Wenn sich ein Konto heute für eine Zielgruppe qualifiziert hat, aber noch nicht auf die Journey gelangt ist, warten Sie, bis der nächste tägliche Zyklus abgeschlossen ist, bevor Sie eine Untersuchung durchführen.
* Wenn sich die Kontoverknüpfung einer Person ändert, z. B. wenn ein Kontakt zu einem anderen Konto wechselt, wird die Aktualisierung der Beziehung innerhalb von 24 Stunden durch den täglichen Synchronisierungszyklus propagiert. Journey, die von der Kontomitgliedschaft abhängig sind, spiegeln die aktualisierte Beziehung nach dem nächsten täglichen Zyklus wider. Es sind keine Maßnahmen erforderlich.

>[!TIP]
>
>Entwerfen Sie Journey mit dem Verständnis, dass die Zielgruppenzugehörigkeit täglich aktualisiert wird, nicht in Echtzeit. Wenn Sie nahezu in Echtzeit antworten müssen, verwenden Sie [ereignisbasierte Trigger &#x200B;](../journeys/listen-for-event-nodes.md) anstelle der zielgruppenbasierten Eingabe.

## Datensynchronisation mit [!DNL Experience Platform] {#platform-sync}

[!DNL Experience Platform] ist der primäre Datenspeicher für Accounts, Personen und Opportunities und [!DNL Journey Optimizer B2B Edition] besitzt Journey, Einkaufsgruppen und Einkaufsgruppenrollen. [Weitere Informationen zur Architektur](../about-journey-optimizer-b2b-edition.md#high-level-architecture).

Die Daten bewegen sich in unterschiedlichen Abständen zwischen den beiden Systemen in jeder Richtung:

* **[!DNL Experience Platform]zu[!DNL Journey Optimizer B2B Edition]** - Die Datensynchronisation erfolgt nahezu in Echtzeit und kann bis zu 30 Minuten dauern.
* **[!DNL Journey Optimizer B2B Edition]bis[!DNL Experience Platform]** - Datensynchronisation in Mikrostapeln und kann bis zu 4 Stunden dauern.

## Aktivitätsereignisse und Journey-Aktionen {#activity-and-actions}

Der Zeitpunkt für Aktivitätsdaten und Journey-Aktionen hängt davon ab, wie die Daten zwischen den Systemen verschoben werden:

* **Aktivitätsdaten** - Es kann etwa vier Stunden dauern, bis Personenaktivitätsdatensätze wie E-Mail-Öffnungen, Link-Klicks und Formularausfüllungen in [!DNL Journey Optimizer B2B Edition] angezeigt werden. Diese Zeitplanung gilt für Batch-Aktivitätsdaten. [!DNL Experience Platform] Experience Event-Trigger verwenden Streaming-Daten und können nahezu in Echtzeit reagieren.
* **[!DNL Marketo Engage]Aktionen** - Journey-Aktionen, die [!DNL Marketo Engage] aufrufen, sind nahezu in Echtzeit, da es sich um API-Aufrufe handelt. Wenn beispielsweise ein Journey-Schritt eine Person zu einer [!DNL Marketo] hinzufügt oder daraus entfernt, wird die Aktion in der Regel innerhalb von 30 Minuten abgeschlossen. [Weitere Informationen zu Journey-Aktionen](../journeys/action-nodes.md).
* **Aktionen, die[!DNL Experience Platform]** durchlaufen - Jede Aktion, die an [!DNL Experience Platform] ersten zurückgibt, wird in Batches verarbeitet, sodass sie dem Batch-Timing und nicht nahezu dem Echtzeit-Timing unterliegt.
* **Von[!DNL Journey Optimizer B2B Edition]** generierte Ereignisse - Ereignisse, die [!DNL Journey Optimizer B2B Edition] in [!DNL Experience Platform] generiert, können nur in Batch-Zielgruppen verwendet werden.

## [!DNL LinkedIn] von Zielgruppenzielen {#linkedin-timing}

Wenn Ihr Journey eine [!DNL LinkedIn] Zielaktion enthält, erwarten Sie nach der Veröffentlichung der Journey die folgende Zeitleiste.

| Szenario | Erwartete Wartezeit |
| --- | --- |
| Zum Zeitpunkt der Veröffentlichung der Journey waren bereits Konten in der Zielgruppe | Selber Tag, wenn die Verarbeitung vor Mitternacht Ortszeit abgeschlossen ist |
| Die Konten kamen an, nachdem die Journey veröffentlicht wurde | Bis zu 24 Stunden |
| Konten sind nach dem ersten täglichen Synchronisierungsfenster eingegangen | Bis zu 36-40 Stunden |

[!DNL LinkedIn] Zielgruppengröße werden möglicherweise nicht sofort aktualisiert. Diese Verzögerung ist eine erwartete Verzögerung bei der [!DNL Experience Platform] der Verarbeitung und Bereitstellung der Zielgruppendatei an [!DNL LinkedIn]. Wenn die Zielgruppengröße nach 48 Stunden immer noch 0 ist, untersuchen Sie. [Erfahren Sie mehr über abgeglichene Zielgruppen mit LinkedIn-Konto](./linkedin-account-matched-audiences.md).
