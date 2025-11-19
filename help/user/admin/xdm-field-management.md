---
title: XDM-Feldverwaltung
description: Verwenden Sie die XDM-Feldverwaltung, um die Daten zu steuern, die Journey Optimizer B2B edition zur Verfügung stehen.
feature: Data Management, Integrations
role: User
badgeBeta: label="Beta" type="informative" tooltip="Diese Funktion befindet sich derzeit in einer eingeschränkten Beta-Version"
source-git-commit: de7f5620556a48fe6f12ed1c70e925e11ec770f1
workflow-type: tm+mt
source-wordcount: '1027'
ht-degree: 2%

---


# XDM-Feldverwaltung

Experience-Datenmodell (XDM)-Felder sind Schemaelemente, die Daten für das [!DNL Journey Optimizer B2B Edition]-Programm bereitstellen. Sie verwenden XDM-Felder als Filter und Einschränkungen in Journey, Einkaufsgruppen und Funktionen wie E-Mail-Personalisierung und bedingte Inhalte.

Schemata definieren Felder basierend auf standardmäßigen XDM-Klassen. Zu den standardmäßigen XDM-Klassen gehören „Individuelles Profil“, „Geschäftskonto“ und „Erlebnisereignis“. Relationale Schemata definieren auch Felder, mit denen Sie strukturierte Daten ähnlich wie herkömmliche relationale Datenbanken modellieren können.

Adobe Experience Platform (AEP)-Schemata enthalten in der Regel viele Felder in komplexen Hierarchien. Das Durchlaufen von XDM-Schemastrukturen dauert einige Zeit. Die XDM-Feldverwaltung optimiert die Feldauswahl, indem nur Felder angezeigt werden, die für jede Journey relevant sind. Administratoren steuern, welche Felder für Journey-Ersteller angezeigt werden. Admins legen die Felder auch auf „Schreibgeschützt“ oder „Bearbeitbar“ fest. Diese Maßnahmen verbessern die Effizienz beim Journey-Design.

Administratoren, die XDM verstehen und mit Dateningenieuren oder Stakeholdern der B2B-Kundendatenplattform (CDP) für die Datenmodellierung zusammenarbeiten, befolgen die Verfahren in diesem Handbuch.

>[!NOTE]
>[Relationale Schemata](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/relational#) sind in begrenztem Umfang für die [!DNL Journey Optimizer B2B Edition] verfügbar. Data Mirror und relationale Schemata stehen Lizenzinhabern von Journey Optimizer Orchestered Campaign zur Verfügung. Relationale Schemata sind auch als eingeschränkte Version für Customer Journey Analytics-Benutzende verfügbar, abhängig von Ihrer Lizenz und der Aktivierung von Funktionen. Wenden Sie sich an den Adobe-Support, um Zugang zu erhalten.

## Zugriff auf XDM-Klassen

Um den Bereich für die XDM-Feldverwaltung zu öffnen, navigieren Sie zu **Konfigurationen** > SETUP > **XDM-Klassen**.

* Sie können neue Felder erst hinzufügen, nachdem ein Schema aktiv auf einer Journey verwendet wurde.
* Das Löschen, Umbenennen oder Ändern von Feldtypen kann zu Problemen mit der Journey-Funktionalität führen. Seien Sie beim Bearbeiten von Schemata vorsichtig.
* Umbenennen oder löschen Sie keine Schemata und ändern Sie keine Schlüssel in relationalen Schemata.

>[!IMPORTANT]
>Sie können Ihre Feldauswahl jederzeit aktualisieren, indem Sie neue Felder auswählen oder die Auswahl von Feldern aufheben, die Sie nicht mehr benötigen. Nachdem Sie eine Journey mit diesem Schema veröffentlicht haben, sperren Sie die Schemastruktur. Das Löschen oder Umbenennen des Schemas, das Hinzufügen neuer Felder oder das Ändern von Feldtypen wird nicht unterstützt und kann zu Journey-Fehlern führen.

## Standardklassen

Auf der Registerkarte Standardklassen können Sie &quot;_Felder“_ „Aktualisierbare _&quot;_.

* Verwaltete Felder werden in Journeys, Einkaufsgruppen und Personalisierungsfunktionen angezeigt.
* Aktualisierbare Felder dienen als Einschränkungen für die Journey-Knoten _Kontoprofil aktualisieren_ und _Personenprofil aktualisieren_.

![Registerkarte „Standardklassen“ mit verwalteten und aktualisierbaren Feldern für die XDM-Klassenkonfiguration](assets/xdm-standard.png){width="600" zoomable="yes"}

Führen Sie die folgenden Schritte aus, um Felder aus dem Vereinigungsschema für standardmäßige XDM-Klassen auszuwählen:

1. Navigieren Sie **Administration** > **Konfigurationen** > **XDM-Klassen**.
1. Öffnen Sie die Registerkarte **Standard**. Wählen Sie eine der folgenden Klassen:

   * XDM-Profil für Einzelpersonen
   * XDM-Geschäftskonto

Die Tabelle zeigt Informationen an, darunter:

* Anzahl der verwalteten Felder
* Anzahl der aktualisierbaren Felder
* Zeitpunkt der letzten Aktualisierung

Klicken Sie auf den Klassennamen, um das Auswahldialogfeld _Verwaltete Felder_ zu öffnen.

![Dialogfeld zur Auswahl verwalteter Felder für standardmäßige XDM-Klassen mit konfigurierbaren Feldoptionen](assets/xdm-standard-managed-fields.png){width="600" zoomable="yes"}

1. Klicken Sie auf das Menü **…**, um zwischen _[!UICONTROL verwalteten Feldern]_ und _[!UICONTROL aktualisierbaren Feldern“]_. Im Dialogfeld werden alle konfigurierbaren Felder aufgelistet.
1. Wählen Sie bis zu 100 Felder für jede XDM-Klasse aus.
1. Klicken Sie **[!UICONTROL Speichern]**, um Ihre Auswahl zu bestätigen.

Verwenden Sie den Filter [!UICONTROL Nur ausgewählte Felder anzeigen], um nur aktive Felder anzuzeigen.

Für _Aktualisierbare Felder_ rufen Sie ein separates Dialogfeld auf, in dem Sie Felder aus anderen Datenquellen auswählen können:

1. Wählen Sie in der Dropdown-Liste Datensätze die Datenquelle aus, die Sie konfigurieren möchten.
1. Felder aus dem ausgewählten Datensatz bearbeiten.
1. Klicken Sie auf **[!UICONTROL Speichern]**, um die Änderungen anzuwenden.

![Dialogfeld zur Auswahl aktualisierbarer Felder aus Datensätzen in der XDM-Schemakonfiguration](assets/xdm-select-updateable.png){width="600" zoomable="yes"}

Das Feld muss zunächst _verwaltet“_ kann dann _aktualisierbar_ werden. Die _aktualisierbaren Felder_ die Sie auswählen, müssen in Ihrem vom Benutzer bereitgestellten Schema vorhanden sein.

## Relationale Schemata

Mit relationalen Schemata können Sie benutzerdefinierte Datenklassen erstellen. Mit Zugriff auf mehrere Datensätze können Sie Klassen erstellen, die speziell auf Ihre Datenanforderungen zugeschnitten sind.
Verwenden Sie relationale Schemata für Geschäftsentitäten wie Käufe, Lizenzen und Ereignisregistrierungen beim Journey von Entscheidungen und bei der E-Mail-Personalisierung. Pro Schema können bis zu 50 Schemata und bis zu 100 Felder ausgewählt werden.

![Registerkarte „Relationale Schemata“ im Schema-Editor mit Feldern zu Geschäftsentitäten für Adobe Journey Optimizer](assets/xdm-relational.png)

>[!NOTE]
>Diese Funktion unterstützt derzeit kontenbezogene Anwendungsfälle für benutzerdefinierte Objekte, wobei in Zukunft weitere vordefinierte Anwendungsfälle für Objekte unterstützt werden sollen.

Erstellen Sie relationale Schemata mit dem Schema-Editor unter **Daten-Management** > **Schemata**.

Diese Konfigurationswerte müssen beim Erstellen eines Schemas zur Verwendung mit [!DNL Journey Optimizer B2B Edition] eingeschlossen werden:

* Verhalten: Datensatz
* Segmentierung: Aktiviert
* Beziehungstyp: Viele-zu-eins
* Referenzschema: B2B-Konto
* Erforderliche Felder: Primärer Schlüssel, Fremdschlüssel und Versionsdeskriptor
* Zugeordneter Datensatz: Definiert und dem Schema zugeordnet

### Erstellen eines relationalen Schemas

Führen Sie die folgenden Schritte aus, um Felder zur Verwendung in [!DNL Journey Optimizer B2B Edition] auszuwählen:

1. Navigieren Sie **Administration** > **Konfigurationen** > **XDM-Klassen**.
1. Öffnen Sie die Registerkarte **Relational**, um Ihre Schemata anzuzeigen.
1. Klicken Sie **[!UICONTROL Relationales XDM-Schema auswählen]**.

   * In der Beta-Version werden nur _Viele-zu-eins-benutzerdefinierte_) unterstützt.

1. Wählen Sie ein relationales Schema aus und klicken Sie auf **[!UICONTROL Weiter]**.

   * In der Beta-Version können Sie ein Schema nicht mehr aus der Liste entfernen, nachdem Sie es ausgewählt haben.

1. Geben Sie einen Namespace ein oder verwenden Sie den standardmäßigen Namespace. Klicken Sie auf **[!UICONTROL Weiter]**.

   * Sie können den Namespace nur einmal festlegen und diese Aktion nicht rückgängig machen.

1. Überprüfen Sie die Felder des relationalen Schemas. Klicken Sie auf das Symbol ![Info](../assets/do-not-localize/icon-info-light.svg) [!UICONTROL Info], um die Feldmetadaten anzuzeigen.
1. Auswahl der Felder, die für Journey und Personalisierung aktiviert werden sollen. Die Plattform wählt automatisch die folgenden erforderlichen Felder aus:

   * Fremdschlüssel
   * Primärschlüssel
   * Versionsdeskriptor

1. Verwenden Sie den Regler [!UICONTROL Nur ausgewählte Felder anzeigen], um eine Vorschau Ihrer Auswahlen anzuzeigen.
1. Filtern Sie Felder mithilfe der Suchleiste nach Namen.
1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Ereignisse

Verwenden Sie Erlebnisereignisse und die zugehörigen Felder beim Journey von Entscheidungen. Sie können bis zu 50 Ereignisse und bis zu 100 Felder pro Ereignis auswählen.

![Registerkarte „Ereignisse“ mit Auswahl- und Schemafeldern für Erlebnisereignisse für Journey und Personalisierung](assets/xdm-events.png){width="700" zoomable="yes"}

Klicken Sie auf einen Ereignisnamen, um Details anzuzeigen und die konfigurierten Felder zu bearbeiten.

Führen Sie die folgenden Schritte aus, um Erlebnisereignisse und Schemafelder auszuwählen:

1. Navigieren Sie **Administration** > **Konfigurationen** > **XDM-Klassen**.
1. Öffnen Sie die Registerkarte **Ereignisse**.
1. Um Felder für ein Ereignis auszuwählen, klicken Sie auf **[!UICONTROL Erlebnisereignis auswählen]**.
1. Klicken Sie auf der Detailseite auf **[!UICONTROL Ereignistyp auswählen]**.
1. Wählen Sie in der Liste Ereignis Ihr Ereignis aus.
1. Klicken Sie **[!UICONTROL Auswählen]**, um das Dialogfeld zu schließen.

   * In der Beta-Version können Sie ausgewählte Ereignisse nicht entfernen.

1. Klicken Sie **[!UICONTROL Felder auswählen]**.
1. Verwenden Sie den [!UICONTROL Nur ausgewählte Felder anzeigen], um Ihre aktuellen Auswahlen anzuzeigen.
1. Auswahl der in [!DNL Journey Optimizer B2B Edition] zu verwendenden Felder. Klicken Sie **[!UICONTROL Auswählen]**, um das Dialogfeld zu schließen.
1. Klicken Sie auf [!UICONTROL Speichern].
