---
title: XDM-Feldverwaltung
description: Verwenden Sie die XDM-Feldverwaltung, um die Daten zu steuern, die Journey Optimizer B2B edition zur Verfügung stehen.
feature: Data Management, Integrations
role: User
badgeBeta: label="Beta" type="informative" tooltip="Diese Funktion befindet sich derzeit in einer eingeschränkten Beta-Version"
source-git-commit: 0497f44336cdd6bfed5bac9f6f579a97f6be585a
workflow-type: tm+mt
source-wordcount: '1070'
ht-degree: 1%

---


# XDM-Feldverwaltung

Experience-Datenmodell (XDM)-Felder sind Schemaelemente, die Daten für das [!DNL Journey Optimizer B2B Edition]-Programm bereitstellen. Verwenden Sie XDM-Felder als Filter und Einschränkungen in Journey, Einkaufsgruppen und Funktionen wie E-Mail-Personalisierung und bedingte Inhalte.

Schemata definieren Felder basierend auf standardmäßigen XDM-Klassen. Zu den standardmäßigen XDM-Klassen gehören „Individuelles Profil“, „Geschäftskonto“ und „Erlebnisereignis“. Relationale Schemata definieren auch Felder, mit denen Sie strukturierte Daten ähnlich wie herkömmliche relationale Datenbanken modellieren können.

Adobe Experience Platform (AEP)-Schemata enthalten in der Regel viele Felder in komplexen Hierarchien. Das Durchlaufen von XDM-Schemastrukturen dauert einige Zeit. Die XDM-Feldverwaltung optimiert die Feldauswahl, indem nur Felder angezeigt werden, die für jede Journey relevant sind. Administratoren steuern, welche Felder für Journey-Ersteller angezeigt werden. Admins legen die Felder auch auf „Schreibgeschützt“ oder „Bearbeitbar“ fest. Diese Maßnahmen verbessern die Effizienz beim Journey-Design.

Administratoren, die XDM verstehen und mit Dateningenieuren oder Stakeholdern der B2B-Kundendatenplattform (CDP) zusammenarbeiten, sollten die Verfahren auf dieser Seite verwenden.

>[!NOTE]
>[Relationale Schemata](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/relational#) stehen als eingeschränkte Verfügbarkeitsversion zur [!DNL Journey Optimizer B2B Edition] zur Verfügung. Data Mirror und relationale Schemata stehen Lizenzinhabern von Journey Optimizer Orchestered Campaign zur Verfügung. Relationale Schemata sind auch als eingeschränkte Version für Customer Journey Analytics-Benutzende verfügbar, abhängig von Ihrer Lizenz und der Aktivierung von Funktionen. Wenden Sie sich an den Adobe-Support, um Zugang zu erhalten.

## Zugriff auf XDM-Klassen

1. Wählen Sie in der linken Navigation **[!UICONTROL Administration]** > **[!UICONTROL Konfiguration]** aus.

1. Klicken Sie **[!UICONTROL Zwischenbereich auf]** XDM-Klassen“.

   * Verwenden Sie die Registerkarten **[!UICONTROL Standard]** und **[!UICONTROL Relational]**, um neue Felder hinzuzufügen und sie in Journey Optimizer B2B edition verfügbar zu machen.

   * Verwenden Sie die **Ereignisse**, um [bestimmte AEP Experience Events und ihre zugehörigen Felder auszuwählen](./configure-aep-events.md) die für das Journey von Ereignisknoten verwendet werden sollen.

## Feldauswahl

>[!IMPORTANT]
>
>Sie können Ihre Feldauswahl jederzeit aktualisieren, indem Sie neue Felder auswählen oder die Auswahl von Feldern aufheben, die Sie nicht mehr benötigen. Wenn Sie eine Journey mit diesem Schema veröffentlichen, sperren Sie die Schemastruktur. Das Löschen oder Umbenennen des Schemas, das Hinzufügen neuer Felder oder das Ändern von Feldtypen wird nicht unterstützt und kann zu Journey-Fehlern führen.

Verwenden Sie die folgende Richtlinie für die Auswahl von Feldern:

* Sie können neue Felder erst hinzufügen, nachdem ein Schema aktiv auf einer Journey verwendet wurde.
* Das Löschen, Umbenennen oder Ändern von Feldtypen kann zu Problemen mit der Journey-Funktionalität führen. Seien Sie beim Bearbeiten von Schemata vorsichtig.
* Umbenennen oder löschen Sie keine Schemata und ändern Sie keine Schlüssel in relationalen Schemata.

### Standardklassen

Auf der Registerkarte _[!UICONTROL Standard]_ können Sie _verwaltete Felder_ und _aktualisierbare Felder_ für die Standardklassen bearbeiten:

* Verwaltete Felder werden in Journeys, Einkaufsgruppen und Personalisierungsfunktionen angezeigt.
* Aktualisierbare Felder dienen als Einschränkungen für die Journey-Knoten _Kontoprofil aktualisieren_ und _Personenprofil aktualisieren_.

![Registerkarte „Standardklassen“ mit XDM-Klassenkonfiguration](assets/xdm-standard.png){width="600" zoomable="yes"}

Die Liste umfasst zwei Klassen:

* **[!UICONTROL Individuelles XDM-Profil]**
* **[!UICONTROL XDM Business-Konto]**

Zu den angezeigten Klasseninformationen gehören:

* Anzahl der verwalteten Felder
* Anzahl der aktualisierbaren Felder
* Zeitpunkt der letzten Aktualisierung

Um Felder aus dem Vereinigungsschema für Standard-XDM-Klassen auszuwählen, klicken Sie auf den Klassennamen, um das Auswahldialogfeld _Verwaltete Felder_ zu öffnen, oder klicken Sie auf das Symbol _Mehr_ ( **…** ), um zwischen _[!UICONTROL Verwaltete Felder]_ und _[!UICONTROL Aktualisierbare Felder]_ wählen.

![Klicken Sie auf das Menüsymbol Mehr , um zwischen verwalteten Feldern und aktualisierbaren Feldern zu wählen](./assets/xdm-classes-standard-more-menu.png){width="550" zoomable="yes"}

>[!NOTE]
>
>Ein Feld muss zunächst _verwaltet“_ kann dann _aktualisierbar_ werden. Die _aktualisierbaren Felder_ die Sie auswählen, müssen in Ihrem vom Benutzer bereitgestellten Schema vorhanden sein. Ihr Schema enthält möglicherweise keine erforderlichen Felder, mit Ausnahme der systemdefinierten.

#### Verwaltete Felder

Bei Auswahl von **[!UICONTROL Verwaltete Felder]** werden im Dialogfeld _Felder auswählen_ alle konfigurierbaren Felder aufgelistet.

1. Wählen Sie bis zu 100 Felder für jede XDM-Klasse aus.

   Filtern Sie _[!UICONTROL angezeigte Liste mithilfe]_ Felds „Suche“ nach Namen. Mit dem Schieberegler **[!UICONTROL Nur ausgewählte Felder anzeigen]** können Sie die aktuellen Auswahlen überprüfen.

   ![Dialogfeld zur Auswahl verwalteter Felder für standardmäßige XDM-Klassen mit konfigurierbaren Feldoptionen](assets/xdm-standard-managed-fields.png){width="450" zoomable="yes"}

1. Klicken Sie **[!UICONTROL Speichern]**, um Ihre Auswahl zu bestätigen.

#### Aktualisierbare Felder

Bevor Sie aktualisierbare Felder konfigurieren, müssen sie sich in einem benutzerdefinierten Datensatz befinden. Eine exemplarische Vorgehensweise des benutzerdefinierten Datensatz-Workflows finden Sie unter [Erstellen von Datensätzen und Aufnehmen von Daten](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/data-management/create-datasets-and-ingest-data#){target="_blank"} und verwenden Sie die Option **[!UICONTROL Erstellen eines Datensatzes aus einem Schema]**. Mit diesem Datensatz werden aktualisierbare Felder isoliert. Alle aktualisierbaren Felder müssen sich in diesem Datensatz befinden.

Erstellen Sie einen Datensatz für ein individuelles Profil und einen anderen für ein Geschäftskonto. Wählen Sie während des Konfigurationsprozesses jeden neuen Datensatz aus:

1. Wählen **[!UICONTROL unter]** die neue Datenquelle aus, die Sie erstellt haben.
1. Felder aus dem ausgewählten Datensatz auswählen.

   ![Dialogfeld zur Auswahl aktualisierbarer Felder aus Datensätzen in der XDM-Schemakonfiguration](./assets/xdm-select-updateable.png){width="450" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Speichern]**, um Ihre Änderungen anzuwenden.

### Relationale Schemata

Mit relationalen Schemata können Sie benutzerdefinierte Datenklassen erstellen. Mit Zugriff auf mehrere Datensätze können Sie Klassen erstellen, die speziell auf Ihre Datenanforderungen zugeschnitten sind. Verwenden Sie relationale Schemata für Geschäftsentitäten wie Käufe, Lizenzen und Ereignisregistrierungen beim Journey von Entscheidungen und bei der E-Mail-Personalisierung. Pro Schema können bis zu 50 Schemata und bis zu 100 Felder ausgewählt werden.

Weitere Informationen darüber, wie die ausgewählten Felder für die erweiterte E-Mail-Personalisierung verwendet werden, finden Sie unter [Inhaltspersonalisierung](../content/personalization.md#custom-datasets).

>[!NOTE]
>
>Diese Funktion unterstützt derzeit kontobezogene Anwendungsfälle für benutzerdefinierte Objekte, wobei in Zukunft weitere vordefinierte Anwendungsfälle für Objekte unterstützt werden sollen.

Sie können relationale Schemata mit dem Schema-Editor erstellen (navigieren Sie **[!UICONTROL Daten-Management]** > **[!UICONTROL Schemata]** in der linken Navigationsleiste).

Beim Erstellen eines Schemas zur Verwendung mit [!DNL Journey Optimizer B2B Edition] sind die folgenden Konfigurationswerte erforderlich:

* Verhalten: Datensatz
* Segmentierung: Aktiviert
* Beziehungstyp: Viele-zu-eins
* Referenzschema: B2B-Konto
* Erforderliche Felder: Primärer Schlüssel, Fremdschlüssel und Versionsdeskriptor
* Zugeordneter Datensatz: Definiert und dem Schema zugeordnet

So wählen Sie relationale Schemafelder zur Verwendung in [!DNL Journey Optimizer B2B Edition] aus:

1. Wählen Sie die Registerkarte **[!UICONTROL Relational]** aus, um Ihre Schemata anzuzeigen.

   ![Registerkarte „Relationale Schemata“ im Schema-Editor mit Feldern zu Geschäftsentitäten für Adobe Journey Optimizer B2B edition](assets/xdm-relational.png){width="600" zoomable="yes"}

1. Klicken Sie **[!UICONTROL Relationales XDM-Schema auswählen]**.

   >[!NOTE]
   >
   >In dieser Beta-Funktionsversion werden nur _Viele-zu-eins-benutzerdefinierte Objekte_ Konto“ unterstützt.

1. Wählen Sie ein relationales Schema aus und klicken Sie auf **[!UICONTROL Weiter]**.

   >[!NOTE]
   >
   >In dieser Beta-Funktionsversion können Sie ein Schema nicht aus der Liste entfernen, nachdem Sie es ausgewählt haben.

   ![Wählen Sie im Dialogfeld ein relationales Schema aus](./assets/xdm-classes-relational-select-schema-dialog.png){width="500" zoomable="yes"}

1. Geben Sie einen Namespace ein oder verwenden Sie den standardmäßigen Namespace. Klicken Sie auf **[!UICONTROL Weiter]**.

   Sie können den Namespace nur einmal festlegen und diese Aktion nicht rückgängig machen.

   ![Der Standard-Namespace im Dialogfeld Namespace erstellen &#x200B;](./assets/xdm-classes-relational-create-namespace.png){width="400" zoomable="yes"}

1. Überprüfen Sie die Felder des relationalen Schemas.

   Klicken Sie auf das Symbol _Info_ ![Info](../assets/do-not-localize/icon-info-light.svg), um die Feldmetadaten anzuzeigen.

1. Auswahl der Felder, die für Journey und Personalisierung aktiviert werden sollen.

   Die Plattform wählt automatisch die folgenden erforderlichen Felder aus:

   * Fremdschlüssel
   * Primärschlüssel
   * Versionsdeskriptor

   Filtern Sie _[!UICONTROL angezeigte Liste mithilfe]_ Felds „Suche“ nach Namen. Mit dem Schieberegler **[!UICONTROL Nur ausgewählte Felder anzeigen]** können Sie die aktuellen Auswahlen überprüfen.

   ![Wählen Sie im Dialogfeld Felder für das relationale Schema aus](./assets/xdm-classes-relational-select-schema-fields.png){width="500" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Speichern]**.
