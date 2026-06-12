---
title: Sperren von Inhalten für E-Mail-Vorlagen
description: Verwenden Sie Governance-Einstellungen in Journey Optimizer B2B Prime, um Inhalte in E-Mail-Vorlagen auf Struktur- oder Komponentenebene zu sperren und so zu steuern, welche E-Mail-Autoren bearbeiten können.
badgeBeta: label="Beta" type="informative" tooltip="Diese Funktion ist Teil einer eingeschränkten Beta-Version."
source-git-commit: 2f19137465c71f2292d37bea5786533b1df6e286
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---


# Sperren von Inhalten für E-Mail-Vorlagen

Mit der Inhaltssperrung können Vorlagenautoren Governance-Regeln definieren, die einschränken, welche Teile einer E-Mail-Vorlage geändert werden können, wenn die Vorlage auf einer Journey verwendet wird. Dies hilft Marken- und Compliance-Teams, wichtige Design-Elemente wie Kopfzeilen, Logos und rechtliche Inhalte zu schützen und es Marketing-Teams zu ermöglichen, die Nachricht innerhalb der genehmigten Struktur anzupassen.

>[!NOTE]
>
>Das Sperren von Inhalten ist eine Funktion der Governance auf Editor-Ebene. Es steuert, was Autorinnen und Autoren im E-Mail-Design-Bereich bearbeiten können, verhindert jedoch nicht die über die API vorgenommenen Änderungen.

Nur Benutzer mit der Berechtigung **[!UICONTROL Inhaltsvorlagen verwalten]** können Governance-Einstellungen konfigurieren.

## Governance-Modi {#modes}

Wenn Sie die Governance für eine Vorlage aktivieren, wählen Sie einen von zwei Modi aus:

| Modus | Beschreibung |
| ---- | ----------- |
| **[!UICONTROL Inhaltssperrung]** | Bestimmte Strukturen oder Komponenten selektiv sperren. Entsperrte Bereiche bleiben von Autoren bearbeitbar. |
| **[!UICONTROL Schreibgeschützt]** | Die gesamte Vorlage sperren. Autoren können sie auf eine E-Mail anwenden, aber keinen Teil ihres Inhalts ändern. |

## Governance aktivieren {#enable}

1. Öffnen Sie die Vorlage im E-Mail-Design-Bereich.
1. Klicken Sie in der rechten Leiste auf die Komponente **[!UICONTROL Hauptteil]**, um sie auszuwählen.
1. Schalten Sie auf **[!UICONTROL Governance]** um.
1. Wählen Sie aus der Dropdown-Liste Modus **[!UICONTROL Inhaltssperrung]** oder **[!UICONTROL Schreibgeschützt]** aus.

Wenn Sie **[!UICONTROL Inhaltssperrung]** ausgewählt haben, fahren Sie mit dem Sperren einzelner Elemente fort.

### Sperren einer Struktur {#lock-structure}

1. Wählen Sie auf der Arbeitsfläche die Struktur (Spaltenlayout) aus, die Sie schützen möchten.
1. Aktivieren Sie in der rechten Leiste den Umschalter **[!UICONTROL Struktur sperren]**.

Alle Inhalte, die in einer gesperrten Struktur verschachtelt sind, werden automatisch gesperrt. Damit eine bestimmte Komponente innerhalb einer gesperrten Struktur bearbeitbar bleibt, wählen Sie die Komponente aus und aktivieren Sie **[!UICONTROL Bearbeitbar]** in der rechten Leiste.

### Sperren einer Komponente {#lock-component}

Innerhalb einer bearbeitbaren Struktur können Sie einzelne Inhaltskomponenten sperren.

1. Wählen Sie die Komponente auf der Arbeitsfläche aus.
1. Aktivieren Sie in der rechten Leiste den Umschalter **[!UICONTROL Inhalt sperren]**.

### Hinzufügen von Inhalten zulassen {#allow-additions}

Bei Verwendung **[!UICONTROL Modus „Inhaltssperrung]** können Sie Autoren ermöglichen, der Vorlage neuen Inhalt hinzuzufügen, während gesperrte Elemente geschützt bleiben:

1. Aktivieren **[!UICONTROL Hinzufügen von Inhalten zulassen]**.
1. Wählen Sie aus, ob Autoren sowohl Strukturen als auch Inhaltskomponenten oder nur Inhaltskomponenten hinzufügen können.

## Gesperrte Elemente identifizieren {#identify}

Der **[!UICONTROL Navigationsbaum]** in der linken Leiste zeigt Schloss- und Stiftsymbole, die Autoren dabei helfen, schnell zu identifizieren, was sie ändern können und was nicht:

* Ein **Sperrsymbol** zeigt ein gesperrtes Element an.
* Ein **Bleistiftsymbol** zeigt ein Element an, das bearbeitet werden kann.

Gesperrte Elemente werden auf der Arbeitsfläche visuell angezeigt, wenn ein Autor die Vorlage öffnet.

## Aspekte

Governance-Einstellungen werden mit der Vorlage gespeichert. Jede E-Mail, die aus einer verwalteten Vorlage erstellt wird, übernimmt die Sperrkonfiguration zum Zeitpunkt der Anwendung. Die Aktualisierung der Governance-Einstellungen einer Vorlage hat keine Auswirkungen auf die zuvor damit erstellten E-Mails.
