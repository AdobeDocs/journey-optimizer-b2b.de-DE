---
title: Benutzerverwaltung
description: Erfahren Sie, wie Sie Team-Mitglieder Journey Optimizer B2B edition-Produktprofilen zuweisen.
feature: Setup, Permissions
roles: Admin
exl-id: ddbdc6a5-49bc-46cd-8d9b-1d37223dffe2
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '1879'
ht-degree: 2%

---

# Benutzerverwaltung

Nachdem die Bereitstellung abgeschlossen und Sandboxes gebunden sind, führen Sie die folgenden Schritte aus, um Ihrem Team und Ihren Benutzenden Zugriff auf Adobe Journey Optimizer B2B edition zu gewähren.

1. [Erstellen eines Marketo Engage-Produktprofils](#marketo-engage-profile) in der Admin Console (nur neue Marketo Engage-Instanz).
1. [Erstellen einer Benutzergruppe](#create-user-group) in der Admin Console.
1. [Bearbeiten von integrierten Rollen](#edit-roles) oder [Erstellen einer benutzerdefinierten Rolle](#create-a-custom-role) mit Berechtigungen für Journey Optimizer B2B edition.
1. [Benutzer](#add-users) oder &quot;[&quot; ](#add-user-groups-to-a-role) Rollen hinzufügen.

Als Admin können Sie diese Aufgaben in der Adobe Admin Console ausführen, die ein zentraler Ort für die Verwaltung Ihrer Adobe-Produktlizenzen und Benutzenden ist. In der Admin Console können Sie Benutzende an einem zentralen Ort anstatt in Ihren individuellen Lösungen erstellen und verwalten. Weitere Informationen zu den Funktionen und ](https://helpx.adobe.com/de/enterprise/using/admin-console.html) finden Sie auf der Seite [Übersicht über Admin Console .

## Die Admin Console aufrufen

Bevor Sie die Admin Console zum Verwalten von Benutzenden in Ihrem Team verwenden können, müssen Sie sicherstellen, dass Sie auf die Admin Console zugreifen können und über die entsprechenden Berechtigungen verfügen.

1. Als System-Admin sollten Sie im Rahmen des Onboarding-Prozesses mehrere E-Mails von Adobe erhalten.

   Suchen Sie nach der Begrüßungs-E-Mail mit Informationen zum Namen der Organisation, auf die Sie Zugriff erhalten haben.

1. Klicken Sie auf **[!UICONTROL Link]** Erste Schritte“ in Ihrer Begrüßungs-E-Mail, um zur Admin Console zu navigieren.

   Wenn Sie die E-Mail nicht finden können, öffnen Sie einen Browser unter [https://adminconsole.adobe.com](https://adminconsole.adobe.com) direkt zur Admin Console.

1. Melden Sie sich mit Ihrer Adobe ID an.

   Nach erfolgreicher Anmeldung sehen Sie die _Übersicht_ der Adobe Admin Console.

1. Wenn Sie Zugriff auf mehrere Organisationen haben, stellen Sie sicher, dass Sie sich bei der richtigen Organisation angemeldet haben.

   Um Ihre Organisation zu ändern, klicken Sie oben rechts auf den Organisationsnamen und wählen Sie die Organisation aus, auf die Sie Zugriff benötigen.

1. Wählen Sie **[!UICONTROL Administratoren]** auf der Karte _[!UICONTROL Benutzer]_ aus, um zu überprüfen, ob Sie ein Systemadministrator sind.

   ![Übersicht über Admin Console - auf Administratoren klicken](./assets/admin-console-overview-administrators.png){width="700" zoomable="yes"}

1. Suchen Sie durch Eingabe Ihrer Adobe ID-E-Mail-Adresse, Ihres Benutzernamens, Vor- oder Nachnamens.

   * Wenn Ihr Zugriff richtig konfiguriert ist, gibt die Suche Ihren Datensatz zurück.

   * Wenn in der Spalte **[!UICONTROL ADMINISTRATORROLLE]** der Wert &quot;`System`&quot; angezeigt wird, bedeutet dies, dass Sie (oder die angezeigte Person) System-Admin sind.

## Marketo Engage-Produktprofil erstellen {#marketo-engage-profile}

Wenn Sie Benutzenden Zugriff auf eine Adobe-Lösung gewähren, möchten Sie ihnen nicht unbedingt uneingeschränkten Zugriff gewähren. Produktprofile ermöglichen es jeder Lösung, über eigene Benutzerberechtigungen zu verfügen. Verwenden Sie die Admin Console, um Produktprofile zuzuweisen.

Weitere Informationen zur Verwendung von Produktprofilen für Benutzerberechtigungen finden Sie unter [Verwalten von Produktprofilen für Unternehmensbenutzer](https://helpx.adobe.com/de/enterprise/using/manage-product-profiles.html){target="_blank"} in der Dokumentation zu Admin Console.
<!--
>[!BEGINSHADEBOX]

When you add a user to the Marketo Engage product profile, they are subsequently added to the _Standard User_ role within the Default workspace of the Marketo Engage subscription. This role grants them all _Standard User_ permissions for Marketo Engage in that workspace. Currently, all Journey Optimizer B2B Edition users are required to be Marketo Engage users. A Marketo Engage administrator can restrict access by updating the permissions for the _Standard User_ role or by moving the user to a different Marketo Engage user role with more restrictive permissions.

For more information about managing these permissions within Marketo Engage, see [Managing User Roles and Permissions](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/users-and-roles/managing-user-roles-and-permissions){target="_blank"} in the Marketo Engage documentation.

>[!ENDSHADEBOX]-->

![Anforderungen an die Administratorrolle](../../assets/do-not-localize/icon-admin-user.svg){width="30"} Ein Systemadministrator oder Marketo Engage-Produktadministrator kann die folgenden Schritte ausführen.

1. Anmelden bei [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Wählen Sie die Registerkarte **[!UICONTROL Produkte]** aus.

1. Öffnen Sie die Marketo Engage-Instanz, der Sie das Profil hinzufügen möchten, und klicken Sie auf **[!UICONTROL Neues Profil]**.

   ![Admin Console - Marketo Engage-Instanz - Neues Profil](./assets/admin-console-marketo-engage-instance-new-profile.png){width="700" zoomable="yes"}

1. Geben Sie einen Produktprofilnamen ein, z. B _„Standardbenutzer_.

1. Klicken Sie **Weiter** und dann **Speichern**.

## Erstellen einer Benutzergruppe {#create-user-group}

Eine Benutzergruppe ist eine Sammlung von Benutzern, denen ein gemeinsamer Berechtigungssatz gewährt wird. Sie können Benutzer in Ihrer Benutzergruppe hinzufügen oder entfernen. Die Gruppenberechtigungen bleiben unverändert, während die Benutzer innerhalb der Gruppe wechseln.

Weitere Informationen dazu, wie Benutzergruppen zum Verwalten von Berechtigungen verwendet werden, finden Sie unter [Verwalten von Benutzergruppen](https://helpx.adobe.com/de/enterprise/using/user-groups.html){target="_blank"} in der Dokumentation zu Admin Console.

![Anforderungen an die Administratorrolle](../../assets/do-not-localize/icon-admin-user.svg){width="30"} Ein Systemadministrator kann die folgenden Schritte ausführen.

1. Anmelden bei [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Wählen Sie die **[!UICONTROL Benutzer]** aus.

1. Wählen **[!UICONTROL Benutzergruppen]** im linken Navigationsbereich aus.

1. Klicken **[!UICONTROL oben]** auf „Neue Benutzergruppe“.

1. Geben Sie einen Namen für die Benutzergruppe ein, z. B. _Standardbenutzer_ und klicken Sie auf **[!UICONTROL Speichern]**.

1. Klicken Sie auf die soeben erstellte Benutzergruppe.

1. Wählen Sie die Registerkarte **[!UICONTROL Zugewiesene Produktprofile]** und klicken Sie auf **[!UICONTROL Profil zuweisen]**.

1. Klicken Sie auf **+** und fügen Sie jede Instanz der folgenden Produkte hinzu:

   * [!UICONTROL Marketo Engage]
   * [!UICONTROL Adobe Experience Platform - AEP-default-all-users]
   * [!UICONTROL Adobe Experience Platform – Datenerfassung]
   * [!UICONTROL Zugriff auf alle Datenerfassungs-]

   ![Admin Console - Benutzergruppe - Produkte hinzufügen](./assets/admin-console-user-group-add-products.png){width="700" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Benutzer zu einer Gruppe hinzufügen

Informationen zur Benutzerverwaltung finden Sie unter [Admin Console-Benutzer](https://helpx.adobe.com/de/enterprise/using/user-groups.html) in der Dokumentation zu Admin Console.

![Anforderungen an die Administratorrolle](../../assets/do-not-localize/icon-admin-user.svg){width="30"} Ein System- oder Produktadministrator kann die folgenden Schritte ausführen. Ein Produktadministrator kann nur Benutzer hinzufügen, die bereits in seiner Organisation vorhanden sind.

1. Navigieren Sie zu [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Klicken _[!UICONTROL unter &quot;]_&quot; auf **[!UICONTROL Benutzer hinzufügen]**.

1. Fügen Sie jeden Benutzer hinzu:

   * Geben Sie die E-Mail-Adresse, den Vornamen und den Nachnamen des Benutzers ein.

     ![Experience Platform - Fügen Sie Profile für die neue Rolle hinzu](./assets/admin-console-add-users.png){width="600" zoomable="yes"}

   * Klicken Sie **[!UICONTROL „Benutzergruppen]** auf **+**.

   * Wählen Sie die zuvor erstellte Benutzergruppe aus.

   * Klicken Sie auf **[!UICONTROL Übernehmen]**.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Rollen für Produktberechtigungen bearbeiten {#edit-roles}

Berechtigungen sind Einzelrechte, mit denen Sie die einem Produktprofil zugewiesenen Berechtigungen definieren können. Jede Berechtigung wird unter einer Funktion erfasst, z. B. Journey oder Einkaufsgruppen, die die verschiedenen Funktionen oder Objekte in Journey Optimizer B2B edition darstellt.

Im _Berechtigungen_ von Adobe Experience Platform können Admins Benutzerrollen und Zugriffsrichtlinien definieren, um Zugriffsberechtigungen für Funktionen und Objekte innerhalb einer Produktanwendung zu verwalten. In dieser App können Sie Rollen erstellen und verwalten sowie die gewünschten Ressourcenberechtigungen für diese Rollen zuweisen. Mit Berechtigungen können Sie auch die Sandboxes und die Benutzer verwalten, die einer bestimmten Rolle zugeordnet sind.

Weitere Informationen zu Rollenberechtigungen in Experience Platform finden Sie unter [Verwalten von Berechtigungen für eine Rolle](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/permissions){target="_blank"} in der Dokumentation zu Experience Platform.

### B2B-Produktberechtigungen

Die folgenden Berechtigungen regeln den Zugriff auf Funktionen von Journey Optimizer B2B edition:

| Kategorie | Beschreibung | Berechtigungen |
| -------- | ----------- | ---------- |
| B2B-Kontolisten | Berechtigungen für B2B-Kontolisten konfigurieren, verwalten, anzeigen und veröffentlichen. Zu diesen Berechtigungen gehören Aktionen wie das Hinzufügen, Entfernen, Importieren und Löschen von Konten aus Kontolisten. | <li>Verwalten von B2B-Kontolisten |
| B2B-Administratorkonfigurationen | Konfigurieren, Verwalten und Anzeigen von Berechtigungen für B2B-Administrationskonfigurationen. Zu diesen Berechtigungen gehören Verbindungen für Digital Asset Management, Asset-Repositorys und Ereignisse. | <li>Verwalten von B2B-Admin-Konfigurationen |
| B2B-Assets | Konfigurieren, Verwalten und Anzeigen von Berechtigungen für B2B-Assets. Zu diesen Berechtigungen gehören E-Mails, SMS, Landingpages, Fragmente, Vorlagen und Bilder. | <li>Verwalten von B2B-Assets <li>B2B-Vorlagen verwalten <li>Verwalten von B2B-Fragmenten |
| B2B-Einkaufsgruppen | Konfigurieren, Verwalten und Anzeigen von Berechtigungen für B2B-Einkaufsgruppen. Zu diesen Berechtigungen gehören Lösungsinteressen, Rollenvorlagen und der Kaufgruppenstatus. | <li>Verwalten von B2B-Einkaufsgruppen |
| B2B-Kanal-Konfigurationen | Konfigurieren, Verwalten und Anzeigen von Berechtigungen für B2B-Kanal-Konfigurationen. Zu diesen Berechtigungen gehören Einstellungen für Kommunikationsbeschränkungen, API-Anmeldeinformationen und Sicherheitseinstellungen. | <li>Verwalten von B2B-Kanal-Konfigurationen |
| B2B-Dashboards | Konfigurieren und Anzeigen von Berechtigungen für B2B-Dashboards. Zu diesen Berechtigungen gehören die Kontointeraktion, der Einkauf von Gruppenphasen, steigende Konten und die Kontaktabdeckung. | <li>B2B-Dashboards verwalten |
| B2B-Journey | Konfigurieren, Verwalten, Anzeigen und Veröffentlichen von Berechtigungen für B2B-Journey. Zu diesen Berechtigungen gehören Konto- und Personenaktionen, Ereignis-Listener und Aufspaltungspfade | <li>B2B-Journey verwalten |

### Integrierte B2B-Rollen

Wenn Ihr Unternehmen Journey Optimizer B2B edition bereitgestellt hat, verfügt Experience Platform über eine Reihe integrierter (standardmäßiger) Rollen, mit denen Sie den Zugriff auf die Produktfunktionen verwalten können:

| Rolle | Berechtigungen |
| ---- | ----------- |
| B2B Journey Manager | <li>B2B-Journey verwalten <li>Verwalten von B2B-Einkaufsgruppen <li>Verwalten von B2B-Kontolisten <li>Dashboard für B2B-Interaktionen anzeigen <li>Dashboard für B2B-Insights anzeigen |
| B2B-Kanal-Manager | <li>Verwalten von B2B-Assets <li>B2B-Vorlagen verwalten <li>Verwalten von B2B-Fragmenten |
| B2B-Systemadministrator | <li>Verwalten von B2B-Kanal-Konfigurationen <li>Verwalten von B2B-Admin-Konfigurationen |
| B2B-Verkaufsbenutzer | <li>Dashboard für B2B-Interaktionen anzeigen |

### Rollenberechtigungen bearbeiten

Für integrierte oder benutzerdefinierte Rollen können Sie sich jederzeit entscheiden, Berechtigungen hinzuzufügen oder zu löschen. Wenn Sie eine standardmäßige oder benutzerdefinierte Rolle ändern, wirkt sich dies auf jeden Benutzer aus, der dieser Rolle zugewiesen ist.

Im folgenden Beispiel möchten Sie Berechtigungen im Zusammenhang mit der B2B-Journey-Ressource für Benutzer hinzufügen, die der Rolle B2B-Kanal-Manager zugewiesen sind. Durch diese Änderung können Benutzende für diese Rolle auch Account-Journey verwalten.

>[!NOTE]
>
>Ein Admin Console-Systemadministrator kann die folgenden Schritte ausführen.

_So ändern Sie die Berechtigungen für eine Rolle:_

1. Navigieren Sie zu [experience.adobe.com](https://experience.adobe.com/).

1. Wählen Sie im Bedienfeld _[!UICONTROL Schnellzugriff]_ die Option **[!UICONTROL Berechtigungen]** aus.

   >[!NOTE]
   >
   >Wenn „Berechtigungen _[!UICONTROL nicht angezeigt wird]_ müssen Sie möglicherweise auf **[!UICONTROL Alle anzeigen]** klicken und diese aus den verfügbaren Programmen auswählen.

   ![Experience Platform - Zugriffsberechtigungen](./assets/aep-permissions.png){width="700" zoomable="yes"}

1. Wählen **[!UICONTROL Rollen]** im linken Navigationsbereich aus.

1. Klicken Sie auf den **_B2B-Kanal_** Manager-Rollennamen.

1. Klicken Sie auf der Detailseite oben **[!UICONTROL auf]** Bearbeiten“.

   ![Experience Platform - Rolle bearbeiten](./assets/aep-permissions-role-edit.png){width="700" zoomable="yes"}

   Im Rolleneditor wird im Menü _[!UICONTROL Ressourcen]_ die Liste der Ressourcen angezeigt, die für die Produkte Experience Cloud - Plattformgestützte Anwendungen gelten.

   Sie können im Suchwerkzeug _B2B_ eingeben, um die Liste nach den B2B-Produktberechtigungen zu filtern.

1. Klicken Sie auf _Hinzufügen_-Symbol (**+**) für die Ressource B2B-Journey .

   ![Experience Platform - Rolle bearbeiten](./assets/aep-permissions-role-edit-b2b-journeys-add.png){width="700" zoomable="yes"}

1. Wählen Sie auf der _[!UICONTROL B2B-Journey]_ Berechtigungskarte **[!UICONTROL B2B-Konto-Journey verwalten]** aus.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

   ![Experience Platform - Rolle bearbeiten](./assets/aep-permissions-role-edit-b2b-journeys-done.png){width="700" zoomable="yes"}

1. Klicken Sie **[!UICONTROL Schließen]**, um zur Detailseite zurückzukehren.

### Benutzer zu einer Rolle hinzufügen

![Anforderungen an die Administratorrolle](../../assets/do-not-localize/icon-admin-user.svg){width="30"} Ein Systemadministrator oder AEP-Produktadministrator kann die folgenden Schritte ausführen.

1. Öffnen Sie die Rollendetails und wählen Sie die Registerkarte **[!UICONTROL Benutzer]** aus.

   Auf dieser Registerkarte wird eine Liste aller Benutzer angezeigt, die der Rolle zugewiesen wurden.

1. Klicken Sie **[!UICONTROL Benutzer hinzufügen]**.

   ![Experience Platform - Fügen Sie Benutzer zur Rolle hinzu](./assets/aep-permissions-role-add-users.png){width="700" zoomable="yes"}

1. Suchen Sie im _[!UICONTROL Benutzer hinzufügen]_ die Benutzer, die Sie der Rolle hinzufügen möchten, und wählen Sie sie aus.

   * Sie können das Suchwerkzeug verwenden, um die Benutzerliste zu filtern.

   * Aktivieren Sie das Kontrollkästchen für jeden Benutzer.

   ![Experience Platform - Dialogfeld „Benutzer hinzufügen“](./assets/aep-permissions-role-add-users-dialog.png){width="600" zoomable="yes"}

1. Klicken Sie **[!UICONTROL Speichern]**, wenn Sie alle Benutzenden ausgewählt haben, die Sie hinzufügen möchten.

### Hinzufügen von Benutzergruppen zu einer Rolle

Informationen zur Benutzerverwaltung finden Sie unter [Admin Console-Benutzer](https://helpx.adobe.com/de/enterprise/using/user-groups.html) in der Dokumentation zu Admin Console.

![Anforderungen an die Administratorrolle](../../assets/do-not-localize/icon-admin-user.svg){width="30"} Ein Systemadministrator oder AEP-Produktadministrator kann die folgenden Schritte ausführen.

1. Öffnen Sie die Rollendetails und wählen Sie die Registerkarte **[!UICONTROL Benutzergruppen]** aus.

   Auf dieser Registerkarte wird eine Liste aller Benutzergruppen angezeigt, die der Rolle zugewiesen sind.

1. Klicken Sie **[!UICONTROL Gruppen hinzufügen]**.

   ![Experience Platform - Fügen Sie Benutzer zur Rolle hinzu](./assets/aep-permissions-role-add-groups.png){width="700" zoomable="yes"}

1. Suchen Sie im _[!UICONTROL Gruppen hinzufügen]_ die Gruppen, die Sie der Rolle hinzufügen möchten, und wählen Sie sie aus.

   * Sie können das Suchwerkzeug verwenden, um die Liste der Benutzergruppen zu filtern.

   * Aktivieren Sie das Kontrollkästchen für jede Benutzergruppe.

   ![Experience Platform - Dialogfeld „Gruppen hinzufügen“](./assets/aep-permissions-role-add-groups-dialog.png){width="600" zoomable="yes"}

1. Klicken Sie **[!UICONTROL Speichern]**, wenn Sie alle Benutzenden ausgewählt haben, die Sie hinzufügen möchten.

## Erstellen einer benutzerdefinierten Rolle

![Anforderungen an die Administratorrolle](../../assets/do-not-localize/icon-admin-user.svg){width="30"} Ein Systemadministrator oder AEP-Produktadministrator kann die folgenden Schritte ausführen.

1. Wählen Sie **[!UICONTROL linken Navigationsbereich die Option]** Rollen“ und dann **[!UICONTROL Rolle erstellen]** aus.

1. Geben _[!UICONTROL im Dialogfeld Neue Rolle erstellen]_ einen Namen für die Rolle ein, z. B. _B2B-Marketer_ und eine Beschreibung (optional).

1. Klicken Sie auf **[!UICONTROL Bestätigen]**.

1. Wählen Sie Ihre Sandboxes aus.

   ![Experience Platform - Fügen Sie Sandboxes für die neue Rolle hinzu](./assets/aep-permissions-role-sandboxes.png){width="700" zoomable="yes"}

1. Fügen Sie die Profilberechtigungen hinzu:

   * Suchen Sie in _[!UICONTROL Liste]_ Ressourcen“ auf der linken Seite das Element **[!UICONTROL Profilverwaltung]** und klicken Sie auf das Symbol _Hinzufügen_ (**+**), um das Attribut hinzuzufügen.

   * Fügen Sie für das -Attribut die folgenden Berechtigungen hinzu:
      * [!UICONTROL Segmente anzeigen]
      * [!UICONTROL Segmente verwalten]
      * [!UICONTROL Profile anzeigen]
      * [!UICONTROL Profile verwalten]
      * [!UICONTROL B2B-Profil anzeigen]
      * [!UICONTROL Verwalten des B2B-Profils]

   ![Experience Platform - Fügen Sie Profile für die neue Rolle hinzu](./assets/aep-permissions-role-profiles.png){width="700" zoomable="yes"}

1. B2B-Produktberechtigungen hinzufügen:

   Anhand der Liste der B2B[Produktberechtigungen können Sie ](#b2b-product-permissions), welche Produktfunktionen Sie für die Rolle benötigen.

   Suchen Sie in der _[!UICONTROL Ressourcen]_-Liste auf der linken Seite die **[!UICONTROL B2B]**-Elemente und klicken Sie auf das _Hinzufügen_-Symbol (**+**), um jedes Attribut hinzuzufügen, das Sie für die Rolle aktivieren möchten.

   Sie können im Suchwerkzeug _B2B_ eingeben, um die Liste nach den B2B-Produktberechtigungen zu filtern.

1. Klicken **[!UICONTROL oben]** auf „Speichern“.

1. Gehen Sie zu den Rollendetails und wählen Sie die Registerkarte **[!UICONTROL Benutzergruppen]** aus.

1. Klicken Sie **[!UICONTROL Gruppen hinzufügen]**.

   ![Experience Platform - Fügen Sie Profile für die neue Rolle hinzu](./assets/aep-permissions-role-add-groups.png){width="700" zoomable="yes"}

1. Aktivieren Sie das Kontrollkästchen neben der Benutzergruppe, die Sie zuvor in der Admin Console erstellt haben.

1. Klicken Sie auf **[!UICONTROL Speichern]**.
