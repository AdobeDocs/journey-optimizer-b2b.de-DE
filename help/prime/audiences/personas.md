---
title: Abgeleitete Personas
description: Verwenden Sie abgeleitete Personas in Journey Optimizer B2B Prime, um Personenlisten und Journey-Pfade auszuwählen. Erfahren Sie mehr über die standardmäßigen Rollenzuordnungen und den Filter „Abgeleitete Rolle“.
badgeBeta: label="Beta" type="informative" tooltip="Diese Funktion befindet sich derzeit in einer eingeschränkten Beta-Version"
autotag-review: '2026-06-23T22:01:21.605Z'
TQID: 'https://experienceleague.adobe.com/OZ4GDkaqg9a5Aikic-m-f0MtHSpc3BO0h41fTAL1Rww'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
  - id: c3d6e661-d372-4e98-9fd9-eac771e7e4ee
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: af10a912422f1736fdc86e0609aee76f5d4daa46
workflow-type: tm+mt
source-wordcount: 650
ht-degree: 2%

---

# Abgeleitete Personas

Die Persona-Klassifizierung transformiert Kundenrohdaten in semantisches Käuferverständnis, mit dem KI Kontext generieren und personalisierte Entscheidungen über jeden Kanal und jede Journey hinweg fördern kann. Dieses einheitliche Profil bietet folgende Möglichkeiten:

* _Journey-Verzweigung_ - Aufspaltung von Routenleitern nach Rolle, Interaktionstiefe und Rolle
* _Journey-Schlichtung_ - Bestimmt, zu welchem Pflegeheim ein Lead derzeit gehört, wodurch Nachrichtenkollisionen über gleichzeitige Programme hinweg vermieden werden
* _Inhaltspersonalisierung_ - Inhalte, die rollenspezifische Erzählungen sind („für einen ausführenden Benutzer“ vs. „für einen Fachmann„)
* _Sales Qualifier Context_ - BDRs erhalten eine Zusammenfassung auf einem Bildschirm, die zeigt, „wer diese Person ist, was ihnen wichtig ist und wo sie sich auf der Kauf-Journey befinden“

## Standard-Personas {#default-ersonas}

Für die Beta-Version von Journey Optimizer B2B Prime werden die folgenden Standardpersonas entsprechend dem Auftragstitelattribut definiert:

| Persona | Stellenbezeichnungen |
| ------- | ---------- |
| [!UICONTROL CXO/EVP] | CEO, CIO, CTO, CMO, CFO, Executive Vice President of Strategy |
| [!UICONTROL SVP/VP] | SVP Marketing, VP Sales, SVP Operations, VP Product, VP IT |
| [!UICONTROL Senior Manager/Manager] | Senior Marketing Manager, IT Manager, Operations Manager, Sales Manager, HR Manager |
| [!UICONTROL Einzelner Beitragender] | Kundenbetreuer, Software-Ingenieur, Marketing-Spezialist, Customer Success-Vertreter |
| [!UICONTROL Analyst] | Business Analyst, Data Analyst, Market Research Analyst, Financial Analyst, Operations Analyst |
| [!UICONTROL Entwicklerin/Entwickler] | Frontend-Entwickler, Backend-Entwickler, Full-Stack-Entwickler, Mobile-App-Entwickler, DevOps-Ingenieur |
| [!UICONTROL Professionelles Personal] | HR Specialist, Legal Counsel, Compliance Officer, Project Manager, Procurement Specialist |
| [!UICONTROL Berater] | Unternehmensberater, IT-Berater, Business Process Consultant, Marketing Consultant |
| [!UICONTROL Sonstige] | Branchenspezialist, unabhängiger Berater, freiberuflicher Berater, Fachexperte |

>[!NOTE]
>
>In der Version zur allgemeinen Verfügbarkeit können Sie jede dieser Standardrollen entsprechend den Anforderungen Ihres Unternehmens bearbeiten. Es unterstützt auch benutzerdefinierte Persona-Definitionen und -Zuordnungen.

## Nach abgeleiteter Persona filtern {#derived-persona-filter}

Journey Optimizer B2B Prime leitet für jeden Personendatensatz eine Rolle ab, indem die Attribute des Datensatzes mit den definierten Rollen verglichen werden. Sie können das abgeleitete Ergebnis - die _abgeleitete Persona_ - als Filter verwenden, wenn Sie die Audience für eine Personenliste definieren oder eine Personen-Journey segmentieren.

Der _[!UICONTROL Abgeleitete Persona]_-Filter wird im Filterbedienfeld unter der Kategorie **[!UICONTROL Personenattribute]** angezeigt.

### Personenlisten {#people-lists}

Wenn Sie Mitglieder zu einer [statischen Personenliste](./people-lists.md#static-list) hinzufügen oder daraus entfernen oder wenn Sie die Mitgliedschaftsregeln für eine [dynamische Personenliste](./people-lists.md#dynamic-lists) definieren, können Sie nach abgeleiteter Persona filtern, um alle Personen anzusprechen, deren Attribute einer bestimmten konfigurierten Persona entsprechen.

![Abgeleitete Rollenfilterung für eine Personenliste](./assets/derived-persona-filter-people-list.png){width="750" zoomable="yes"}

**Statische Liste - Mitglieder hinzufügen**

1. Öffnen Sie die statische Liste und klicken Sie **[!UICONTROL oben]** auf „Personen hinzufügen“.

1. Erweitern Sie im Filterdialogfeld **[!UICONTROL Personenattribute]** und ziehen Sie **[!UICONTROL Abgeleitete Persona]** auf die Arbeitsfläche.

1. Wählen Sie in der Filterbedingung **[!UICONTROL ist]** und wählen Sie eine oder mehrere Rollen aus der Liste aus.

1. Klicken Sie **[!UICONTROL Fertig]**, um den Filter anzuwenden und passende Personen für die Liste zu qualifizieren.

**Dynamische Liste - Festlegen von Mitgliedschaftsregeln**

1. Öffnen Sie die dynamische Liste und wählen Sie die Registerkarte **[!UICONTROL Regeln]** aus.

1. Klicken Sie **[!UICONTROL Regeln bearbeiten]**.

1. Erweitern Sie im Filterdialogfeld **[!UICONTROL Personenattribute]** und ziehen Sie **[!UICONTROL Abgeleitete Persona]** auf die Arbeitsfläche.

1. Wählen Sie in der Filterbedingung **[!UICONTROL ist]** und wählen Sie eine oder mehrere Rollen aus der Liste aus.

1. Klicken Sie **[!UICONTROL Fertig]**, um die Regel zu speichern.

   Die Mitgliedschaft wird automatisch aktualisiert, wenn Personendatensätze anhand der Regel ausgewertet werden.

### Personen-Journey {#person-journeys}

Wenn Sie die Segmentierung für eine Personen-Journey in einem [_Aufspaltungs-_-Knoten](../marketing/split-merge-paths-nodes.md) konfigurieren, können Sie eine abgeleitete Rolle als Personenprofilfilter verwenden, um zu steuern, welche Personen in den Journey-Pfad eintreten.

![Abgeleitete Rollenfilterung für eine Bedingung eines aufgeteilten Pfads](./assets/derived-persona-filter-split-path.png){width="750" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Arbeitsfläche Journey auf]** Knoten „Pfade aufteilen“.

1. Klicken Sie im Bedienfeld Knoteneigenschaften rechts auf **[!UICONTROL Bedingung anwenden]** oder **[!UICONTROL Bedingung bearbeiten]** für einen Pfad.

1. Erweitern Sie im Filterdialogfeld **[!UICONTROL Personenattribute]** und ziehen Sie **[!UICONTROL Abgeleitete Persona]** auf die Arbeitsfläche.

1. Wählen Sie in der Filterbedingung **[!UICONTROL ist]** und wählen Sie eine oder mehrere Rollen aus der Liste aus.

1. Klicken Sie **[!UICONTROL Fertig]**, um den Filter für den Pfad zu speichern.
