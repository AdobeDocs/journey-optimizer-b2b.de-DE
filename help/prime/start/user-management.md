---
title: Benutzerzugriff und Berechtigungen
description: 'Verwalten des Benutzerzugriffs in der Adobe Admin Console: Erstellen Sie Benutzergruppen, weisen Sie Produktprofile zu und legen Sie rollenbasierte Berechtigungen für Journey Optimizer B2B edition Prime fest.'
source-git-commit: f1449f734b5d93dc9bd4d7b4c1292a50cbc338b7
workflow-type: tm+mt
source-wordcount: '1719'
ht-degree: 70%

---

# Benutzerzugriff und Berechtigungen

Nachdem die Bereitstellung abgeschlossen und Sandboxes gebunden sind, führen Sie die folgenden Schritte aus, um Ihrem Team und Ihren Benutzenden Zugriff auf Adobe Journey Optimizer B2B edition zu gewähren.

1. [Erstellen eines Adobe Journey Optimizer B2B edition-Produktprofils](#create-profile) in der Admin Console (nur einmaliges/erstes Setup).
1. [Hinzufügen einer Benutzergruppe](#add-user-group) in der Admin Console.
1. [Bearbeiten von integrierten Rollen](#edit-role-permissions) oder [Erstellen einer benutzerdefinierten Rolle](#create-a-custom-role) mit Berechtigungen für Journey Optimizer B2B edition in Adobe Experience Platform.
1. [Hinzufügen von &#x200B;](#add-users-to-a-role) oder [Gruppen](#add-user-groups-to-a-role) zu Rollen in Adobe Experience Platform.

## Produktprofil konfigurieren {#config-profile}

Als Admin können Sie diese Aufgaben in der Adobe Admin Console ausführen, die ein zentraler Ort für die Verwaltung Ihrer Adobe-Produktlizenzen und Benutzenden ist. In der Admin Console können Sie Benutzende an einem zentralen Ort anstatt in Ihren individuellen Lösungen erstellen und verwalten. Weitere Informationen zu den Funktionen und Leistungsmerkmalen von finden Sie auf der Seite Übersicht über Admin Console [&#128279;](https://helpx.adobe.com/de/enterprise/using/admin-console.html).

### Die Admin Console aufrufen {#admin-console}

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

   ![Übersicht über Admin Console - auf Administratoren klicken](./assets/admin-console-overview-administrators.png){width="800" zoomable="yes"}

1. Suchen Sie durch Eingabe Ihrer Adobe ID-E-Mail-Adresse, Ihres Benutzernamens, Vor- oder Nachnamens.

   * Wenn Ihr Zugriff richtig konfiguriert ist, gibt die Suche Ihren Datensatz zurück.

   * Wenn in der Spalte **[!UICONTROL ADMINISTRATORROLLE]** der Wert &quot;`System`&quot; angezeigt wird, bedeutet dies, dass Sie (oder die angezeigte Person) System-Admin sind.

### Erstellen des Adobe Journey Optimizer B2B edition-Produktprofils {#create-profile}

Wenn Sie Benutzenden Zugriff auf eine Adobe-Lösung gewähren, möchten Sie ihnen nicht unbedingt uneingeschränkten Zugriff gewähren. Produktprofile ermöglichen es jeder Lösung, über eigene Benutzerberechtigungen zu verfügen. Verwenden Sie die Admin Console, um Produktprofile zuzuweisen.

Weitere Informationen zur Verwendung von Produktprofilen für Benutzerberechtigungen finden Sie unter [_Verwalten von Produktprofilen für Unternehmensbenutzer_](https://helpx.adobe.com/de/enterprise/using/manage-product-profiles.html){target="_blank"} in der Dokumentation zu Admin Console.

![Anforderungen an die Administratorrolle](../../assets/do-not-localize/icon-admin-user.svg){width="30"} Ein Systemadministrator oder Adobe Journey Optimizer B2B edition-Produktadministrator kann die folgenden Schritte unter [https://adminconsole.adobe.com](https://adminconsole.adobe.com) ausführen.

1. Wählen Sie die Registerkarte **[!UICONTROL Produkte]** aus.

1. Öffnen Sie die Adobe Journey Optimizer B2B edition-Instanz, der Sie das Profil hinzufügen möchten, und klicken Sie auf **[!UICONTROL Neues Profil]**.

   ![Experience Platform - Produktprofile für Benutzergruppe](./assets/admin-console-product-profiles.png){width="600" zoomable="yes"}

1. Geben Sie einen Produktprofilnamen ein, z. B. _B2B-Benutzer_.

1. Klicken Sie **[!UICONTROL Weiter]** und dann **[!UICONTROL Speichern]**.

### Hinzufügen einer Benutzergruppe {#add-user-group}

Eine Benutzergruppe ist eine Sammlung von Benutzern, denen ein gemeinsamer Berechtigungssatz gewährt wird. Sie können Benutzer in Ihrer Benutzergruppe hinzufügen oder entfernen. Die Gruppenberechtigungen bleiben unverändert, während die Benutzer innerhalb der Gruppe wechseln.

Weitere Informationen dazu, wie Benutzergruppen zum Verwalten von Berechtigungen verwendet werden, finden Sie unter [Verwalten von Benutzergruppen](https://helpx.adobe.com/de/enterprise/using/user-groups.html){target="_blank"} in der Dokumentation zu Admin Console.

![Anforderungen an die Administratorrolle](../../assets/do-not-localize/icon-admin-user.svg){width="30"} Ein Systemadministrator kann die folgenden Schritte unter [https://adminconsole.adobe.com](https://adminconsole.adobe.com) ausführen.

1. Wählen Sie die **[!UICONTROL Benutzer]** aus.

1. Wählen **[!UICONTROL Benutzergruppen]** im linken Navigationsbereich aus.

1. Klicken **[!UICONTROL oben]** auf „Neue Benutzergruppe“.

1. Geben Sie einen Namen für die Benutzergruppe ein, z. B. _B2B-Journey-Benutzer_ und klicken Sie auf **[!UICONTROL Speichern]**.

   ![Admin Console - Benutzergruppe hinzufügen](./assets/admin-console-new-user-group.png){width="600" zoomable="yes"}

### Produktprofil zuweisen {#assign-profile}

![Anforderungen an die Administratorrolle](../../assets/do-not-localize/icon-admin-user.svg){width="30"} Ein Produktadministrator kann die folgenden Schritte unter [https://adminconsole.adobe.com](https://adminconsole.adobe.com) ausführen.

1. Klicken Sie auf die von Ihnen erstellte Benutzergruppe.

1. Wählen Sie die Registerkarte **[!UICONTROL Zugewiesene Produktprofile]** und klicken Sie auf **[!UICONTROL Profil zuweisen]**.

1. Klicken Sie auf **+** und fügen Sie jede Instanz der folgenden Produkte hinzu:

   * [!UICONTROL Adobe Journey Optimizer B2B edition - Benutzerprofil]
   * [!UICONTROL Adobe Experience Platform - AEP-default-all-users]
   * [!UICONTROL Adobe Experience Platform-Datenerfassung - Standardzugriff auf die Datenerfassung für alle]
   * [!UICONTROL Adobe Experience Platform - Standardzugriff auf alle Produktionsumgebungen]

   ![Admin Console - Produktprofile für Benutzergruppen](./assets/admin-console-product-profiles.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Speichern]**.

### Benutzer zur neuen Gruppe hinzufügen {#add-users}

Informationen zur Benutzerverwaltung finden Sie unter [_Adobe Admin Console-Benutzer_](https://helpx.adobe.com/de/enterprise/using/users.html){target="_blank"} in der Dokumentation zu Admin Console.

![Anforderungen an die Administratorrolle](../../assets/do-not-localize/icon-admin-user.svg){width="30"} Ein System- oder Produktadministrator kann die folgenden Schritte unter [https://adminconsole.adobe.com](https://adminconsole.adobe.com) ausführen. Ein Produktadministrator kann nur Benutzer hinzufügen, die bereits in seiner Organisation vorhanden sind.

1. Wenn die Benutzer noch nicht Mitglieder Ihrer Organisation sind, fügen Sie jeden Benutzer hinzu:

   * Klicken _[!UICONTROL unter &quot;]_&quot; auf **[!UICONTROL Benutzer hinzufügen]**.

   * Geben Sie die E-Mail-Adresse des Benutzers ein und klicken Sie auf **[!UICONTROL Als neuen Benutzer hinzufügen]**.

     ![Admin Console - Benutzerprofil für die neue Gruppe hinzufügen](./assets/admin-console-user-group-add-users.png){width="600" zoomable="yes"}

   * Geben Sie den Vor- und Nachnamen ein und klicken Sie dann auf **[!UICONTROL Speichern]**.

1. Fügen Sie jeder Benutzer der Gruppe hinzu:

   * Klicken Sie auf den Benutzernamen.

   * Scrollen Sie auf der Seite mit den Benutzerdetails zu **[!UICONTROL Benutzergruppen]**.

   * Klicken Sie links auf _Mehr_ ( **…** ) und wählen Sie **[!UICONTROL Benutzergruppen bearbeiten]**.

   * Klicken Sie auf _Hinzufügen_ ( **+** ) unter **[!UICONTROL Benutzergruppen]**.

     ![Admin Console - Benutzergruppe für Benutzer auswählen](./assets/admin-console-user-edit-user-groups.png){width="600" zoomable="yes"}

   * Wählen Sie die zuvor erstellte Benutzergruppe aus und klicken Sie auf **[!UICONTROL Anwenden]**.

   * Klicken **[!UICONTROL auf &quot;]**&quot; für die Benutzeränderungen.

## Zuweisen von Produktberechtigungen {#assign-product-permissions}

Berechtigungen sind Einzelrechte, mit denen Sie die einem Produktprofil zugewiesenen Berechtigungen definieren können. Jede Berechtigung wird unter einer Funktion gruppiert, z. B. Journey oder Einkaufsgruppen, die Funktionen in [!DNL Journey Optimizer B2B Prime] darstellen.

Im _Berechtigungen_ von Adobe Experience Platform können Admins Benutzerrollen und Zugriffsrichtlinien definieren, um Zugriffsberechtigungen für Funktionen und Objekte innerhalb einer Produktanwendung zu verwalten. In dieser App können Sie Rollen erstellen und verwalten sowie die gewünschten Ressourcenberechtigungen für diese Rollen zuweisen. Mit Berechtigungen können Sie auch die Sandboxes und die Benutzer verwalten, die einer bestimmten Rolle zugeordnet sind.

Weitere Informationen zu Rollenberechtigungen in Experience Platform finden Sie unter [Verwalten von Berechtigungen für eine Rolle](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/permissions){target="_blank"} in der Dokumentation zu Experience Platform.

1. Navigieren Sie zu [experience.adobe.com](https://experience.adobe.com/).

1. Wählen Sie im Bedienfeld _[!UICONTROL Schnellzugriff]_ die Option **[!UICONTROL Berechtigungen]** aus.

   >[!NOTE]
   >
   >Wenn „Berechtigungen _[!UICONTROL nicht angezeigt wird]_ müssen Sie möglicherweise auf **[!UICONTROL Alle anzeigen]** klicken und diese aus den verfügbaren Programmen auswählen.

   ![Experience Platform - Zugriffsberechtigungen](./assets/aep-permissions.png){width="700" zoomable="yes"}

<!--

### B2B product permissions {#b2b-product-permissions}

The following permissions govern access to Journey Optimizer B2B Edition capabilities:

| Category | Description | Permissions |
| -------- | ----------- | ---------- |
| B2B Account Lists | Configure, manage, view, and publish permissions for B2B account lists. These permissions include actions such as add, remove, import, and delete accounts from account lists. | <li>Manage B2B Account Lists |
| B2B Admin Configurations | Configure, manage, and view permissions for B2B administrative configurations. These permissions include digital asset management connections, asset repositories, and events. | <li>Manage B2B Admin Configurations |
| B2B Assets | Configure, manage, and view permissions for B2B assets. These permissions include emails, SMS, landing pages, fragments, templates, and images. | <li>Manage B2B Assets <li>Manage B2B Templates <li>Manage B2B Fragments <li>Manage B2B Emails |
| B2B Buying Groups | Configure, manage, and view permissions for B2B buying groups. These permissions include solution interests, roles templates, and buying group status. | <li>Manage B2B Buying Groups <li>Manage B2B Solution Interests <li>Manage B2B Role Templates <li>Manage B2B Stages <li>View B2B Buying Groups |
| B2B Channel Configurations | Configure, manage, and view permissions for B2B channel configurations. These permissions include settings for communication limits, API credentials, and security settings. | <li>Manage B2B Channels Configurations |
| B2B Dashboards | Configure and view permissions for B2B dashboards. These permissions include account engagement, buying group stages, surging accounts, and contact coverage. | <li>View B2B Engagement Dashboard |
| B2B Journeys | Configure, manage, view, and publish permissions for B2B journeys. These permissions include account and person actions, event listeners, and split paths. | <li>Manage B2B Account Journeys |
| Journey Optimizer Rules | Access and configure frequency rules (communication limits). These permissions should be limited to product administrators. | <li>View Frequency Rules <li>Manage Frequency Rules |

### B2B built-in roles {#b2b-built-in-roles}

When your organization has the Journey Optimizer B2B Edition product provisioned, Experience Platform includes a set of built-in (default) roles that you can use to manage access to the product capabilities:

| Role | Permissions |
| ---- | ----------- |
| B2B Journey Manager | <li>Manage B2B Journeys <li>Manage B2B Buying Groups <li>Manage B2B Account Lists <li>View B2B Engagement Dashboard <li>View B2B Insights Dashboard |
| B2B Channel Manager | <li>Manage B2B Assets <li>Manage B2B Templates <li>Manage B2B Fragments |
| B2B System Administrator | <li>Manage B2B Channels Configurations <li>Manage B2B Admin Configurations |
| B2B Sales User | <li>View B2B Engagement Dashboard <li>View B2B Buying Groups <li>Access In-CRM Insights |

-->

### Rollenberechtigungen bearbeiten {#edit-role-permissions}

Für integrierte oder benutzerdefinierte Rollen können Sie sich jederzeit entscheiden, Berechtigungen hinzuzufügen oder zu löschen. Wenn Sie eine standardmäßige oder benutzerdefinierte Rolle ändern, wirkt sich dies auf jeden Benutzer aus, der dieser Rolle zugewiesen ist.

Im folgenden Beispiel möchten Sie Berechtigungen im Zusammenhang mit der B2B-Journey-Ressource für Benutzer hinzufügen, die der Rolle B2B-Kanal-Manager zugewiesen sind. Durch diese Änderung können Benutzende für diese Rolle auch Account-Journey verwalten.

>[!NOTE]
>
>Ein Admin Console-Systemadministrator kann die folgenden Schritte ausführen.

_So ändern Sie die Berechtigungen für eine Rolle :_

1. Wählen **[!UICONTROL Rollen]** im linken Navigationsbereich aus.

1. Klicken Sie auf den **_B2B-Kanal_** Manager-Rollennamen.

1. Klicken Sie auf der Detailseite oben **[!UICONTROL auf]** Bearbeiten“.

   ![Experience Platform - Rolle bearbeiten](../../user/admin/assets/aep-permissions-role-edit.png){width="700" zoomable="yes"}

   Im Rolleneditor wird im Menü _[!UICONTROL Ressourcen]_ die Liste der Ressourcen angezeigt, die für die Produkte Experience Cloud - Plattformgestützte Anwendungen gelten.

   Sie können im Suchwerkzeug _B2B_ eingeben, um die Liste nach den B2B-Produktberechtigungen zu filtern.

1. Klicken Sie auf _Hinzufügen_-Symbol (**+**) für die Ressource B2B-Journey .

   ![Experience Platform - B2B-Journey-Ressource zur Rolle des Kanal-Managers hinzugefügt](./assets/aep-permissions-b2b-list.png){width="700" zoomable="yes"}

1. Wählen Sie auf der _[!UICONTROL B2B-Journey]_ Berechtigungskarte **[!UICONTROL B2B-Konto-Journey verwalten]** aus.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

   <!-- ![Experience Platform - B2B Journeys permissions saved for Channel Manager role](../../user/admin/assets/aep-permissions-role-edit-b2b-journeys-done.png){width="700" zoomable="yes"} -->

1. Klicken Sie **[!UICONTROL Schließen]**, um zur Detailseite zurückzukehren.

### Benutzer zu einer Rolle hinzufügen {#add-users-to-a-role}

![Anforderungen an die Administratorrolle](../../assets/do-not-localize/icon-admin-user.svg){width="30"} Ein Systemadministrator oder AEP-Produktadministrator kann die folgenden Schritte ausführen.

1. Öffnen Sie die Rollendetails und wählen Sie die Registerkarte **[!UICONTROL Benutzer]** aus.

   Auf dieser Registerkarte wird eine Liste aller Benutzer angezeigt, die der Rolle zugewiesen wurden.

1. Klicken Sie **[!UICONTROL Benutzer hinzufügen]**.

   ![Experience Platform - Fügen Sie Benutzer zur Rolle hinzu](../../user/admin/assets/aep-permissions-role-add-users.png){width="700" zoomable="yes"}

1. Suchen Sie im _[!UICONTROL Benutzer hinzufügen]_ die Benutzer, die Sie der Rolle hinzufügen möchten, und wählen Sie sie aus.

   * Sie können das Suchwerkzeug verwenden, um die Benutzerliste zu filtern.

   * Aktivieren Sie das Kontrollkästchen für jeden Benutzer.

   ![Experience Platform - Dialogfeld „Benutzer hinzufügen“](../../user/admin/assets/aep-permissions-role-add-users-dialog.png){width="600" zoomable="yes"}

1. Klicken Sie **[!UICONTROL Speichern]**, wenn Sie alle Benutzenden ausgewählt haben, die Sie hinzufügen möchten.

### Hinzufügen von Benutzergruppen zu einer Rolle {#add-user-groups-to-a-role}

Informationen zur Benutzerverwaltung finden Sie unter [_Adobe Admin Console-Benutzer_](https://helpx.adobe.com/de/enterprise/using/users.html){target="_blank"} in der Dokumentation zu Admin Console.

![Anforderungen an die Administratorrolle](../../assets/do-not-localize/icon-admin-user.svg){width="30"} Ein Systemadministrator oder AEP-Produktadministrator kann die folgenden Schritte ausführen.

1. Öffnen Sie die Rollendetails und wählen Sie die Registerkarte **[!UICONTROL Benutzergruppen]** aus.

   Auf dieser Registerkarte wird eine Liste aller Benutzergruppen angezeigt, die der Rolle zugewiesen sind.

1. Klicken Sie **[!UICONTROL Gruppen hinzufügen]**.

   ![Experience Platform - Fügen Sie der Rolle Gruppen hinzu](../../user/admin/assets/aep-permissions-role-add-groups.png){width="700" zoomable="yes"}

1. Suchen Sie im _[!UICONTROL Gruppen hinzufügen]_ die Gruppen, die Sie der Rolle hinzufügen möchten, und wählen Sie sie aus.

   * Sie können das Suchwerkzeug verwenden, um die Liste der Benutzergruppen zu filtern.

   * Aktivieren Sie das Kontrollkästchen für jede Benutzergruppe.

   ![Experience Platform - Dialogfeld „Gruppen hinzufügen“](../../user/admin/assets/aep-permissions-role-add-groups-dialog.png){width="600" zoomable="yes"}

1. Klicken Sie **[!UICONTROL Speichern]**, wenn Sie alle Gruppen ausgewählt haben, die Sie hinzufügen möchten.

### Erstellen einer benutzerdefinierten Rolle {#create-a-custom-role}

![Anforderungen an die Administratorrolle](../../assets/do-not-localize/icon-admin-user.svg){width="30"} Ein Systemadministrator oder AEP-Produktadministrator kann die folgenden Schritte ausführen.

1. Wählen Sie **[!UICONTROL linken Navigationsbereich die Option]** Rollen“ und dann **[!UICONTROL Rolle erstellen]** aus.

1. Geben _[!UICONTROL im Dialogfeld Neue Rolle erstellen]_ einen Namen für die Rolle ein, z. B. _B2B-Marketer_ und eine Beschreibung (optional).

1. Klicken Sie auf **[!UICONTROL Bestätigen]**.

1. Wählen Sie Ihre Sandboxes aus.

   ![Experience Platform - Fügen Sie Sandboxes für die neue Rolle hinzu](../../user/admin/assets/aep-permissions-role-sandboxes.png){width="700" zoomable="yes"}

1. B2B-Produktberechtigungen hinzufügen:

   <!-- To determine which product capabilities that you want for the role, refer to the list of [B2B product permissions](#b2b-product-permissions). -->

   Suchen Sie in der _[!UICONTROL Ressourcen]_-Liste auf der linken Seite die B2B-Elemente und klicken Sie auf das _Hinzufügen_-Symbol (**+**), um jedes Attribut hinzuzufügen, das Sie für die Rolle aktivieren möchten.

   Sie können im Suchwerkzeug _B2B_ eingeben, um die Liste nach den B2B-Produktberechtigungen zu filtern.

   ![Experience Platform - B2B-Berechtigungen](./assets/aep-permissions-b2b-list.png){width="700" zoomable="yes"}

1. Klicken **[!UICONTROL oben]** auf „Speichern“.

1. Gehen Sie zu den Rollendetails und wählen Sie die Registerkarte **[!UICONTROL Benutzergruppen]** aus.

1. Klicken Sie **[!UICONTROL Gruppen hinzufügen]**.

   ![Experience Platform - Benutzergruppe für die benutzerdefinierte Rolle auswählen](../../user/admin/assets/aep-permissions-role-add-groups.png){width="700" zoomable="yes"}

1. Aktivieren Sie das Kontrollkästchen neben der Benutzergruppe, die Sie zuvor in der Admin Console erstellt haben.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

Ihre benutzerdefinierte Rolle ist konfiguriert, und Benutzerinnen und Benutzer in der zugewiesenen Gruppe können jetzt auf die von Ihnen ausgewählten Journey Optimizer B2B edition-Funktionen zugreifen.
