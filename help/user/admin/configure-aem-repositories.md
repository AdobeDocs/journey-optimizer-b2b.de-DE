---
title: Konfigurieren von Experience Manager-Asset-Repositorys
description: Erfahren Sie, wie Sie eine Verbindung zu Experience Manager Assets-Repositorys konfigurieren, um Inhalte in Journey Optimizer B2B Edition zu erstellen.
feature: Assets, Integrations
source-git-commit: 3d3f0e4d6e62aa7126e915cfd5b54151d1bf9186
workflow-type: tm+mt
source-wordcount: '766'
ht-degree: 0%

---

# Konfigurieren von Experience Manager-Asset-Repositorys

Adobe Journey Optimizer B2B Edition ist mit Adobe Experience Manager Assets as a Cloud Service integriert und ermöglicht so mehr als nur die Verwendung von Assets wie E-Mails innerhalb einer Konto-Journey. Sie sorgt für Transparenz durch den Austausch von Informationen mit Experience Manager Assets. Konfigurieren Sie die Verbindung zu Adobe Experience Assets, um diese Funktion zu aktivieren.

Adobe Experience Manager Cloud Manager ist in Programme unterteilt. Jedes Programm verfügt über mehrere Umgebungen und Repositorys ([Mehr erfahren](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/using-cloud-manager/programs/program-types)). Wenn Sie Adobe Experience Manager Assets in Adobe Journey Optimizer B2B Edition konfigurieren, richten Sie Verbindungen zu jedem Repository ein, das Sie für den Zugriff auf digitale Assets verwenden möchten.

## Voraussetzungen

* Generieren Sie Service-Anmeldeinformationen für die gewünschte Umgebung auf der AEM Headless Developer Console ([Weitere Informationen](https://experienceleague.adobe.com/en/docs/experience-manager-learn/getting-started-with-aem-headless/authentication/service-credentials#generate-service-credentials)).
* Verarbeiten Sie die Zertifikate, die für die Verbindung benötigt werden. Als Best Practice sollten Sie sicherstellen, dass die Zertifikate mindestens sechs Monate vor Ablauf des Zertifikats verbleiben. Die Zertifikate laufen alle 365 Tage ab.
* Adobe Journey Optimizer B2B Edition unterstützt den gleichzeitigen Zugriff auf eine digitale Asset-Management-Quelle. Stellen Sie sicher, dass die erforderlichen Assets in Adobe Experience Manager verfügbar sind, bevor Sie wechseln.

>[!IMPORTANT]
>
>Die Anmeldedaten für den Dienst sind beschädigt und enthalten einen privaten Schlüssel. Diese Anmeldeinformationen müssen gemäß den IT- und Sicherheitsrichtlinien Ihres Unternehmens gespeichert, verwaltet und aufgerufen werden.

## Repository-Verbindung hinzufügen

1. Wählen Sie im linken Navigationsbereich **[!UICONTROL Administration]** > **[!UICONTROL Konfiguration]**.

1. Klicken Sie im Zwischenbereich auf **[!UICONTROL Assets]** .

   ![Zugriff auf den Assets-Konfigurationsraum](./assets/configuration-assets-aem.png){width="700" zoomable="yes"}

<!--   The default digital asset management option is configured as `Adobe Marketo Engage`.
-->
Von hier aus können Sie die Verbindungen zu jedem AEM Umgebungs-Repository einzeln konfigurieren.

1. Klicken Sie im Feld _[!UICONTROL Adobe Experience Manager Assets]_ auf den Pfeil neben **[!UICONTROL Repository konfigurieren]** und wählen Sie das Repository aus.

   ![Wählen Sie ein AEM Assets-Repository](./assets/configure-assets-aem-choose-respository.png){width="500"}

1. Klicken Sie auf **[!UICONTROL Zertifikat hinzufügen]** und verwenden Sie die Dialogfeldwerkzeuge, um die Datei hochzuladen.

   Sie können eine JSON-Datei hochladen, indem Sie sie in das Dialogfeld ziehen oder auf den Link klicken, um eine Datei auf Ihrem System zu suchen und auszuwählen (stellen Sie sicher, dass es sich bei der Datei um einen gültigen JSON-Typ handelt).

   ![Laden Sie die JSON-Zertifikatdatei hoch](./assets/configuration-assets-aem-upload-cert.png){width="500"}

   Nach dem Hochladen wird das Zertifikat unten angezeigt.

   >[!NOTE]
   >
   >Wenn eine ungültige Datei verwendet wird, wird im Dialogfeld unten ein Fehler angezeigt.

   Klicken Sie auf **[!UICONTROL Hinzufügen]** , um das Zertifikat abzuschließen.

1. Klicken Sie auf den Pfeil &quot;Zurück&quot;(↓), um zur Hauptkonfigurationsseite zurückzukehren.

   Das konfigurierte Repository wird in der Tabelle unter dem Auswahlbereich angezeigt. Sie können ein anderes Repository hinzufügen, indem Sie die Schritte 3 bis 4 wiederholen.

   ![Überprüfen Sie die konfigurierten AEM Asset-Repositorys](./assets/configuration-assets-aem-repositories.png){width="600" zoomable="yes"}

Wenn Sie die Konfiguration der Repositorys abgeschlossen haben, können Teammitglieder die Adobe Experience Manager Assets bei der Inhaltserstellung auswählen.

>[!NOTE]
>
>Adobe Journey Optimizer B2B Edition unterstützt den Zugriff auf eine digitale Asset-Management-Quelle bei der Inhaltserstellung. 

## Zertifikat ersetzen

Zertifikate laufen alle 365 Tage ab dem Erstellungsdatum ab. Ersetzen Sie sie vor ihrem Ablauf, um sicherzustellen, dass Ihr Team weiterhin auf Assets zugreifen kann.

>[!NOTE]
>
>Adobe Journey Optimizer B2B Edition kommuniziert mit Experience Manager-Assets, um Nutzungsinformationen zu erhalten. Die Verbindung muss aktiv bleiben, um eine zuverlässige Datensynchronisierung der Nutzung zu gewährleisten und Datendiskrepanzen zu vermeiden. Admin-Benutzer werden über die In-App-Benachrichtigungen darüber benachrichtigt, dass Zertifikate ablaufen. Sie können auch die Ablaufdaten im Assets-Unterabschnitt - Digital Asset Management im Admin-Bereich feststellen.

1. Suchen Sie auf der Seite Digital Asset Management die Liste der konfigurierten Repositorys.

1. Klicken Sie auf das gewünschte Repository, um das Zertifikat zu ersetzen.

1. Klicken Sie auf das Symbol mit den Auslassungspunkten (**...**) für die Zertifikatdatei, um die Optionen für Aktionen darauf anzuzeigen.

   ![Zugriff auf das Optionsmenü für das AEM Asset-Repository-Zertifikat](./assets/configuration-assets-aem-repo-menu.png){width="600" zoomable="yes"}

1. Wählen Sie **[!UICONTROL Ersetzen]** aus, um das Dialogfeld für den Datei-Upload zu öffnen.

1. Laden Sie eine Datei hoch, indem Sie sie entweder in das Dialogfeld ziehen oder den Link verwenden. Stellen Sie sicher, dass die Datei vom JSON-Typ ist.

   ![Laden Sie die JSON-Datei des AEM Assets-Repository-Zertifikats-Assets hoch](./assets/configuration-assets-aem-upload-replacement-cert.png){width="500"}

1. Klicken Sie auf **[!UICONTROL Ersetzen]** , um den Upload zu bestätigen.

## Zertifikat anzeigen

Sie können die JSON-Zertifikatdatei anzeigen, die mit der Repository-Verbindung verknüpft ist.

1. Suchen Sie auf der Seite Digital Asset Management die Liste der konfigurierten Repositorys.

1. Klicken Sie auf das verbundene Repository.

1. Klicken Sie auf das Symbol mit den Auslassungspunkten (**...**) für die Zertifikatdatei, um die Optionen für Aktionen darauf anzuzeigen.

1. Wählen Sie **[!UICONTROL Ansicht]** aus.

   ![Anzeigen der JSON-Zertifikatdatei für ein verbundenes AEM Asset-Repository](./assets/configuration-assets-aem-view-cert.png){width="600"}

1. Klicken Sie auf **[!UICONTROL Schließen]** , um zur Seite Repository konfigurieren zurückzukehren.

## Repository-Verbindung löschen

Durch das Löschen eines Repositorys wird der Benutzerzugriff auf die Experience Manager Assets-Umgebung in Journey Optimizer B2B Edition entfernt.

1. Suchen Sie auf der Seite _[!UICONTROL Digital Asset Management]_ die Liste der konfigurierten Asset-Repositorys.

1. Klicken Sie auf den gewünschten Repository-Namen, um die Verbindung zu bearbeiten.

1. Klicken Sie auf das Symbol mit den Auslassungspunkten (**...**) für die Zertifikatdatei, um die Optionen für Aktionen darauf anzuzeigen.

1. Wählen Sie **[!UICONTROL Löschen]** aus.

1. Klicken Sie im Bestätigungsdialogfeld auf **[!UICONTROL Löschen]**.
<!--

## Switch back to Adobe Marketo Engage Assets

Select Adobe Marketo Engage digital asset management in the Assets section.

After the confirmation, the Adobe Marketo Engage assets library is available for users.
-->
