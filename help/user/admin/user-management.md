---
title: Benutzerverwaltung
description: Erfahren Sie, wie Sie Journey Optimizer B2B Edition-Produktprofilen Teammitglieder zuweisen.
feature: Setup
roles: Admin
source-git-commit: dcd8ab2820d60654e8970944054142fc296ed54f
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 1%

---

# Benutzerverwaltung

Nachdem die Bereitstellung abgeschlossen und die Sandboxes gebunden sind, führen Sie die folgenden Schritte aus, um Ihrem Team und Ihren Benutzern Zugriff auf die Adobe Journey Optimizer B2B Edition zu gewähren.

1. [Erstellen Sie ein Marketo Engage-Produktprofil](#marketo-engage-profile) in der Admin Console (nur neue Marketo Engage-Instanz).
1. [Erstellen Sie eine Benutzergruppe](#create-user-group) in der Admin Console.
1. [Erstellen Sie eine Rolle ](#create-role) in den AEP-Berechtigungen.
1. [Benutzer hinzufügen](#add-users) in der Admin Console.

Als Administrator können Sie diese Aufgaben in der Adobe Admin Console erledigen, einem zentralen Ort für die Verwaltung und Verwaltung Ihrer Adobe-Produktlizenzen und -Benutzer. In der Admin Console können Sie Benutzer an einem Ort erstellen und verwalten und nicht in Ihren einzelnen Lösungen. Weitere Informationen zu Funktionen und Funktionen finden Sie auf der Seite [Admin Console - Übersicht](https://helpx.adobe.com/de/enterprise/using/admin-console.html) .

## Zugriff auf die Admin Console

Bevor Sie die Admin Console zum Verwalten von Benutzern in Ihrem Team verwenden können, müssen Sie sicherstellen, dass Sie auf die Admin Console zugreifen und über die entsprechenden Berechtigungen verfügen können.

1. Als Systemadministrator sollten Sie im Rahmen des Onboarding-Prozesses mehrere E-Mails von Adobe erhalten.

   Suchen Sie nach der Begrüßungs-E-Mail mit Informationen zum Organisationsnamen, auf den Sie Zugriff erhalten haben.

1. Klicken Sie in Ihrer Begrüßungs-E-Mail auf den Link **[!UICONTROL Erste Schritte]** , um zur Admin Console zu navigieren.

   Wenn Sie die E-Mail nicht finden können, öffnen Sie einen Browser direkt auf der Admin Console unter [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Melden Sie sich mit Ihrer Adobe ID an.

   Nach erfolgreicher Anmeldung wird die Übersichtsseite der Adobe Admin Console angezeigt.

1. Wenn Sie Zugriff auf mehrere Organisationen haben, stellen Sie sicher, dass Sie sich bei der richtigen Organisation angemeldet haben.

   Um Ihre Organisation zu ändern, klicken Sie oben rechts auf den Namen der Organisation und wählen Sie die Organisation aus, auf die Sie Zugriff benötigen.

1. Wählen Sie auf der Karte Benutzer die Option Administratoren , um zu überprüfen, ob Sie Systemadministrator sind.

1. Suchen Sie nach Ihrer Adobe ID-E-Mail-, Benutzernamen-, Vor- oder Nachnamen.

   * Wenn Ihr Zugriff korrekt konfiguriert ist, gibt die Suche Ihren Datensatz zurück.

   * Wenn der Wert in der Spalte **[!UICONTROL ADMIN ROLE]** den Wert `System` anzeigt, wissen Sie, dass Sie (oder der angezeigte Benutzer) ein Systemadministrator sind.

## Marketo Engage-Produktprofil erstellen {#marketo-engage-profile}

Wenn Sie Benutzern Zugriff auf eine Adobe-Lösung gewähren, möchten Sie ihnen nicht unbedingt uneingeschränkten Zugriff gewähren. Produktprofile ermöglichen es jeder Lösung, über eigene Benutzerberechtigungen zu verfügen. Verwenden Sie die Admin Console, um Produktprofile zuzuweisen.

>[!NOTE]
>
>Diese Schritte können nur von einem Admin Console-Systemadministrator oder Marketo Engage-Produktadministrator ausgeführt werden.

1. Melden Sie sich bei [https://adminconsole.adobe.com](https://adminconsole.adobe.com) an.

1. Wählen Sie Produkte > Marketo Engage.

1. Klicken Sie auf Neues Profil und geben Sie einen Produktprofilnamen ein, z. B. _Standardbenutzer_.

1. Klicken Sie auf Weiter > Speichern

## Benutzergruppe erstellen {#create-user-group}

Eine Benutzergruppe ist eine Sammlung von Benutzern, denen ein freigegebener Berechtigungssatz gewährt wird. Sie können Benutzer zu Ihrer Benutzergruppe hinzufügen oder daraus entfernen. Die Gruppenberechtigungen bleiben unverändert, während sich die Benutzer innerhalb der Gruppe ändern.

>[!NOTE]
>
>Diese Schritte können nur von einem Admin Console-Systemadministrator durchgeführt werden.

1. Melden Sie sich bei [https://adminconsole.adobe.com](https://adminconsole.adobe.com) an.

1. Wählen Sie **[!UICONTROL Benutzer]** > **[!UICONTROL Benutzergruppen]** > **[!UICONTROL Neue Benutzergruppe]** aus.

1. Geben Sie einen Namen für die Benutzergruppe ein, z. B. _Standardbenutzer_ und klicken Sie auf **[!UICONTROL Speichern]**.

1. Klicken Sie auf die soeben erstellte Benutzergruppe.

1. Klicken Sie auf **[!UICONTROL Zugewiesene Produktprofile]** > **[!UICONTROL Profil zuweisen]**.

1. Wählen Sie die folgenden Produkte aus:
   * [!UICONTROL Marketo Engage - Standardbenutzer]
   * [!UICONTROL Adobe Experience Platform - AEP-Default-All-Users]
   * [!UICONTROL Adobe Experience Platform-Datenerfassung - Standard]
   * [!UICONTROL Datenerfassung - Zugriff auf alle ]

1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Rollen in AEP-Berechtigungen erstellen {#create-role}

Berechtigungen sind Einzelrechte, mit denen Sie die einem Produktprofil zugewiesenen Berechtigungen definieren können. Jede Berechtigung wird im Rahmen einer Funktion erfasst, z. B. Journey oder Einkaufsgruppen, die die verschiedenen Funktionen oder Objekte in Journey Optimizer B2B Edition repräsentiert.

_Berechtigungen_ ist der Bereich von Adobe Experience Platform, in dem Administratoren Benutzerrollen und Zugriffsrichtlinien definieren können, um Zugriffsberechtigungen für Funktionen und Objekte in einer Produktanwendung zu verwalten. In dieser App können Sie Rollen erstellen und verwalten sowie die gewünschten Ressourcenberechtigungen für diese Rollen zuweisen. Mit Berechtigungen können Sie auch die Bezeichnungen, Sandboxes und Benutzer verwalten, die einer bestimmten Rolle zugeordnet sind.

>[!NOTE]
>
>Um die folgenden Schritte durchzuführen, müssen Sie Produktadministrator für Adobe Experience Platform sein.

1. Wechseln Sie zu [experience.adobe.com](https://experience.adobe.com/).

1. Wählen Sie **[!UICONTROL Berechtigungen]** aus.

   >[!NOTE]
   >
   >Wenn Sie die Berechtigungen nicht sehen, müssen Sie möglicherweise auf Alle anzeigen klicken und sie in den verfügbaren Anwendungen auswählen.

1. Wählen Sie **[!UICONTROL Rollen]** im linken Navigationsbereich und dann **[!UICONTROL Rolle erstellen]** aus.

1. Geben Sie im Dialogfeld _[!UICONTROL Neue Rolle erstellen]_ einen Namen für die Rolle ein, z. B. _Standardbenutzer_, und eine Beschreibung (optional).

1. Klicken Sie auf **[!UICONTROL Bestätigen]**.

1. Wählen Sie Ihre Sandboxes aus.

1. Fügen Sie die Profilberechtigungen hinzu:

   * Suchen Sie links in der Liste _[!UICONTROL Ressourcen]_ das Element **[!UICONTROL Profilverwaltung]** und klicken Sie auf das Pluszeichen (**+**), um das Attribut hinzuzufügen.

   * Fügen Sie für das -Attribut die folgenden Berechtigungen hinzu:
      * [!UICONTROL Anzeigen von Segmenten]
      * [!UICONTROL Segmente verwalten]
      * [!UICONTROL Profile anzeigen]
      * [!UICONTROL Profile verwalten]
      * [!UICONTROL B2B-Profil anzeigen]
      * [!UICONTROL B2B-Profil verwalten]

1. Klicken Sie oben rechts auf **[!UICONTROL Speichern]** .

1. Wählen Sie **[!UICONTROL Benutzergruppen]** > **[!UICONTROL Gruppen hinzufügen]** aus.

1. Aktivieren Sie das Kontrollkästchen neben der Benutzergruppe, die Sie zuvor in der Admin Console erstellt haben.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Hinzufügen von Benutzern zur Admin Console

>[!NOTE]
>
>Diese Schritte können nur von einem Admin Console-Systemadministrator oder einem Produktadministrator durchgeführt werden.

1. Wechseln Sie zu [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Klicken Sie auf **[!UICONTROL Benutzer hinzufügen]**.

1. Fügen Sie jeden Benutzer hinzu:

   * Geben Sie die E-Mail-Adresse, den Vor- und Nachnamen des Benutzers ein.
   * Klicken Sie auf [!UICONTROL Benutzergruppen].
   * Wählen Sie die zuvor erstellte Benutzergruppe aus.

1. Klicken Sie auf **[!UICONTROL Anwenden]**.

1. Klicken Sie auf **[!UICONTROL Speichern]**.
