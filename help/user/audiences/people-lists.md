---
title: Personenlisten
description: Erfahren Sie mehr über Personenlisten und wie Sie sie in Journey Optimizer B2B Edition durchsuchen, anzeigen, bearbeiten, löschen und verwenden können.
feature: Audiences
role: User
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: ff2b9b37-92e0-45fc-b853-379d44c08c89
    internal-label: Audience segmentation
source-git-commit: d713d57bddf2ac6f8cf7e7a7d163281f607d729c
workflow-type: tm+mt
source-wordcount: '880'
ht-degree: 1%
---

# Personenlisten

[!DNL Journey Optimizer B2B Edition] ist eine Personenliste eine benannte Sammlung von Personenprofilen, die Sie in Ihren Journey wiederverwenden können. Anstatt in jeder Journey denselben Filtersatz neu zu erstellen, definieren Sie die Personengruppe einmal und verweisen Sie dort, wo Sie ihn benötigen. Verwenden Sie beispielsweise eine Personenliste, um interne Mitarbeiter oder Bestandskunden von einer Nurture-Journey auszuschließen oder um Personen zu verfolgen, die einen Schritt auf einer Journey abgeschlossen haben, damit eine andere Journey darauf reagieren kann.

Es gibt zwei Arten von Personenlisten:

* **[!UICONTROL Static]** - Die Mitgliedschaft ändert sich nur, wenn Sie Personen explizit hinzufügen oder entfernen. Sie können Personen hinzufügen, indem Sie einen Filtersatz anwenden, um die Liste auf der Grundlage der aktuellen Personendaten zu füllen, oder Personen über ein Konto oder eine Personen-Journey hinzufügen und entfernen. Siehe [Statische Personenlisten](./people-lists-static.md).
* **[!UICONTROL Dynamisch]** - Sie definieren einen Regelsatz (Filter) zum automatischen Kuratieren der Liste. Die Liste wird dynamisch aktualisiert, wenn Personen für die Regeldefinition qualifiziert oder disqualifiziert werden. Siehe [Dynamische Personenlisten](./people-lists-dynamic.md).

Sie können [Personenlisten in Account-Journey und Personen-Journey verwenden](./people-lists-journeys.md) um Pfade auf Grundlage der Listenmitgliedschaft aufzuteilen und Personen zu statischen Listen hinzuzufügen oder daraus zu entfernen.

>[!NOTE]
>
>Personenlisten enthalten Personenprofile, die bereits synchronisiert und in [!DNL Journey Optimizer B2B Edition] verfügbar sind. Profile werden bei der Auswertung der Liste nicht direkt aus [!DNL Adobe Experience Platform] Audiences gelesen.

## Aufrufen und Durchsuchen von Personenlisten {#access-browse}

Über die linke Navigationsleiste können Sie auf Personenlisten zugreifen, um Listenmitgliedschaften anzuzeigen, zu erstellen und zu verwalten.

>[!AVAILABILITY]
>
>Die folgenden Produktberechtigungen steuern den Zugriff auf Personenlisten:
>
>* [!UICONTROL B2B-Personenlisten verwalten] - Anzeigen, Erstellen, Bearbeiten und Löschen von Personenlisten.
>* [!UICONTROL B2B-Personenlisten anzeigen] - Personenlisten und ihre Mitglieder anzeigen (schreibgeschützt).
>
>Informationen zum Zuweisen von Berechtigungen finden Sie unter [Benutzerzugriff und Berechtigungen](../admin/user-management.md#b2b-product-permissions).

* Erweitern Sie in der linken Navigation **[!UICONTROL Konten]** und wählen Sie **[!UICONTROL Personenlisten]** aus.

* Wählen Sie **[!UICONTROL Dynamische Listen]** oder **[!UICONTROL Statische Listen]** aus, um zwischen den beiden Listentypen zu wechseln.

* Geben Sie oben in der Liste im Feld _Suche_ Text ein, um die angezeigte Liste nach Namen zu filtern.

  ![Zugriff auf Personenlisten zur Verwaltung von Zielgruppen auf Personenebene](./assets/people-lists-browse-search.png){width="800" zoomable="yes"}

* Klicken Sie auf _Spalteneinstellungen_ ( ![Spalteneinstellungssymbol](../assets/do-not-localize/icon-column-settings-new.svg) ) oben rechts, um die angezeigten Spalten auszuwählen oder zu löschen.

* Um die Breite einer Spalte zu ändern, ziehen Sie die Trennlinie zwischen den Spaltenüberschriften.

Jede Registerkarte enthält die Spalten **[!UICONTROL Name]**, **[!UICONTROL Zuletzt aktualisiert]**, **[!UICONTROL Aktualisiert von]**, **[!UICONTROL Erstellt am]** und **[!UICONTROL Erstellt von]**. Klicken Sie auf den Namen der Personenliste, um deren Details anzuzeigen.

Auf dieser Seite haben Sie außerdem folgende Möglichkeiten:

* Erstellen Sie neue dynamische und statische Listen.
* Öffnet eine Liste und [prüft die aktuellen Mitglieder](#view-list-members).
* Klicken Sie auf das _Mehr Aktionen_-Symbol ( **…** ) für eine Liste und wählen Sie [Bearbeiten](#edit-list-properties) oder [Löschen](#delete-people-list) aus.

## Erstellen einer Personenliste {#create-people-list}

1. Klicken **[!UICONTROL oben rechts]** der Seite &quot;_[!UICONTROL &quot; auf „Liste]_&quot;.

   ![Dialogfeld „Personenliste erstellen“](./assets/people-list-create-dialog.png){width="450"}

1. Geben Sie einen **[!UICONTROL Namen]** (erforderlich) und einen **[!UICONTROL Beschreibung]** (optional) für die Liste ein.

   Der Name kann bis zu 180 Zeichen lang sein und muss in Listen desselben Typs eindeutig sein. Die Beschreibung kann bis zu 2.000 Zeichen lang sein.

1. Wählen Sie die Liste **[!UICONTROL Typ]**:

   * [**[!UICONTROL Statisch]**](./people-lists-static.md) - Qualifizierungsfilter bestimmen die Mitgliedschaft, wenn Sie sie auf die Liste anwenden. Die Mitgliedschaft wird nur aktualisiert, wenn Sie Personen manuell hinzufügen oder wenn eine Journey sie hinzufügt oder entfernt.
   * [**[!UICONTROL Dynamisch]**](./people-lists-dynamic.md) - Qualifizierungsfilter bestimmen die Mitgliedschaft dynamisch. Die Mitgliedschaft wird automatisch aktualisiert.

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

   Die neue Personenliste wird auf ihrer Detailseite geöffnet und der Filter-Editor wird geöffnet, sodass Sie die Personen für die Liste definieren können. Um Personen zu einer statischen Liste hinzuzufügen, wenden Sie einen oder mehrere Filter an. Definieren Sie für eine dynamische Liste die Regeln für die Listenmitgliedschaft.

## Listenmitglieder anzeigen {#view-list-members}

Auf der Detailseite für eine Personenliste zeigt die Liste **[!UICONTROL Mitglieder]** die Personen in der Liste an. Die Gesamtzahl der Personen in der Liste wird oben in der Tabelle angezeigt.

Die Tabelle „Mitglieder“ enthält die folgenden Spalten:

* **[!UICONTROL Name]**
* **[!UICONTROL E-Mail-Adresse]**
* **[!UICONTROL Stellenbezeichnung]**
* **[!UICONTROL Firma]**
* **[!UICONTROL Abo storniert]**
* **[!UICONTROL Erstellt am]**
* **[!UICONTROL Zuletzt geändert]**

Standardmäßig sortiert das System die Mitglieder nach **[!UICONTROL Zuletzt geändert]** wobei die zuletzt geänderten Personen zuerst angezeigt werden. Sie können auch nach **[!UICONTROL Name]**, **[!UICONTROL E-Mail-]** oder **[!UICONTROL Erstellt am]** sortieren.

* Um ein bestimmtes Mitglied zu finden, verwenden Sie das Feld _Suche_. Sie können nach Vorname, E-Mail-Adresse oder Firma suchen.
* Um die anzuzeigenden Spalten auszuwählen, klicken Sie auf das Symbol _Spalteneinstellungen_ und aktivieren oder deaktivieren Sie die Kontrollkästchen. Die _[!UICONTROL Name]_ wird immer angezeigt.
* Um die neueste Mitgliedschaft anzuzeigen, wählen Sie im Menü _[!UICONTROL Mehr]_ die Option **[!UICONTROL Mitglieder aktualisieren]**.
* Um weitere Informationen zu einer Person anzuzeigen, klicken Sie auf den Namen der Person, um die Seite [Personendetails](../accounts/person-details.md) zu öffnen, auf der Sie die Zusammenfassung und die letzten Aktivitäten dieser Person anzeigen können.

## Eigenschaften der Personenliste bearbeiten {#edit-list-properties}

Sie können den Namen und die Beschreibung für eine statische oder dynamische Personenliste ändern.

1. Öffnen Sie _[!UICONTROL Dialogfeld]_ Liste bearbeiten“ mit einer der folgenden Methoden:

   * Klicken Sie auf _[!UICONTROL Seite &quot;]_&quot; auf das Symbol _Mehr Aktionen_ ( **…** ) für die Liste und wählen Sie **[!UICONTROL Bearbeiten]**.
   * Klicken Sie auf der Detailseite für die Liste auf **[!UICONTROL Eigenschaften der Liste bearbeiten]**.

1. Aktualisieren Sie **[!UICONTROL Name]** oder **[!UICONTROL Beschreibung]**.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Personenliste löschen {#delete-people-list}

>[!IMPORTANT]
>
>Das Löschen einer Personenliste ist dauerhaft und kann nicht rückgängig gemacht werden. Sie können eine Personenliste, die von einer aktiven Journey verwendet wird, nicht löschen.

1. Löschen Sie die Liste mithilfe einer der folgenden Methoden:

   * Klicken Sie auf _[!UICONTROL Seite &quot;]_&quot; auf das Symbol _Mehr Aktionen_ ( **…** ) neben dem Listennamen und wählen Sie **[!UICONTROL Löschen]**.
   * Klicken Sie auf der Detailseite für die Liste auf **[!UICONTROL Liste]**.

1. Klicken Sie im Bestätigungsdialog auf **[!UICONTROL Löschen]**.
