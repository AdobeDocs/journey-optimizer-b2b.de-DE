---
title: Konfigurieren von Branding-Domains
description: Konfigurieren Sie Ihre Branding-Domains so, dass jede Ihrer Marken über eigene Marken-Tracking-Links verfügt.
feature: Setup, Channels
role: Admin
exl-id: ccbcbbee-a5be-46fe-bae0-ab026e5cdb72
source-git-commit: 0f34a98753b71b388c822ef4a26dbae6b4c8fb1b
workflow-type: tm+mt
source-wordcount: '1014'
ht-degree: 89%

---

# Konfigurieren von Branding-Domains

Eine Branding-Domain in Marketo Engage ist eine benutzerdefinierte Subdomain (z. B. `links.yourcompany.com`), mit der Links umgeschrieben und E-Mail-Klicks verfolgt werden können, um sicherzustellen, dass sie Ihre Marke widerspiegeln statt einer generischen Domain. Jede Branding-Domain fungiert als Klick-Tracking-Domain, um die Zustellbarkeit und das Vertrauen zu verbessern, indem Ihre E-Mail- und Landingpage-Links mit Ihrer Domain abgeglichen werden.

* Es ersetzt generische Links durch Ihr eigenes Branding in E-Mail-Hyperlinks.
* Wenn ein Lead-Konto auf einen Link klickt, wird es über diese benutzerdefinierte Domain weitergeleitet, um die Leistungsverfolgung zu ermöglichen, während es als legitim für E-Mail-Filter erscheint.
* Wenn Sie über mehrere Marken verfügen, können Sie zusätzliche Branding-Domains konfigurieren, um verschiedene Geschäftsbereiche oder Marken zu unterstützen.

>[!BEGINSHADEBOX]

**Eindeutige CNAMEs für Tracking-Links**

E-Mail-Tracking-Links müssen neu und für die angehängte Marketo Engage-Instanz eindeutig sein. Wenn Sie über CNAMEs für das Tracking von Links verfügen, die auf eine bereits vorhandene (Produktions-)Marketo Engage-Instanz verweisen, können diese nicht ohne Änderung wiederverwendet werden.

Sie können das Domain-Branding für Rückgabepfade zwischen Ihrer Marketo Engage-Produktionsinstanz und der angehängten Instanz freigeben. Dies ist jedoch eine Backend-Änderung. Öffnen Sie ein Support-Ticket und geben Sie Ihr Marketo Engage-Präfix (Munchkin ID) und Ihr neues Journey Optimizer B2B edition-Präfix (Munchkin ID) an, um das freigegebene Domain-Branding für Rückpfade anzufordern.

>[!ENDSHADEBOX]

>[!PREREQUISITES]
>
>Bevor Sie eine Domain in der Benutzeroberfläche bearbeiten oder hinzufügen, müssen Sie über einen [zugeordneten CNAME zu einer von Adobe bereitgestellten Marketo Engage-Domain](https://experienceleague.adobe.com/de/docs/marketo/using/getting-started/initial-setup/setup-steps#customize-your-landing-page-urls-with-a-cname){target="_blank"} verfügen.
>
>Beim Hinzufügen einer Domain sucht das System nach bereits vorhandenen SSLs, die möglicherweise zuvor manuell erstellt wurden. Wenn diese Validierung auftritt, erstellen Sie Ihre Domain, ohne die SSL-Erstellung auszuwählen, und verbinden Sie sie dann als separates Verfahren.

## Zugriff auf Branding-Domains in Marketo Engage

1. Wechseln Sie zum Bereich **[!UICONTROL Admin]** in Ihrer Marketo Engage-Instanz und wählen Sie **[!UICONTROL E-Mail]** aus.

1. Scrollen Sie nach unten zum Bedienfeld **[!UICONTROL Branding-Domains]** .

   ![Bedienfeld „Branding-Domains“ in „Admin“ unter „E-Mail“ mit der Standard-Domain](./assets/me-admin-email-branding-domains.png){width="700" zoomable="yes"}

   In der Liste wird die Standard-Domain für die Marketo Engage-Instanz angezeigt.

## Standard-Branding-Domain bearbeiten

Der erste Schritt bei der Arbeit mit Branding-Domains besteht darin, die in Ihrer Marketo Engage-Instanz definierte Standard-Branding-Domain zu bearbeiten.

>[!NOTE]
>
>Sie können keine zusätzliche Branding-Domain definieren, bevor Sie die generische Standard-Domain bearbeitet haben.

1. Wählen Sie im Bedienfeld _[!UICONTROL Branding]_ Domains“ die generische Domain aus und klicken Sie oben **[!UICONTROL Bearbeiten]**.

   ![Bedienfeld „Branding-Domains“ mit ausgewählter generischer Domain](./assets/me-admin-email-branding-domains-edit-default.png){width="500"}

1. Geben _[!UICONTROL im Dialogfeld Branding-Domain bearbeiten]_ den Namen Ihrer Standard-Domain in das Feld **[!UICONTROL Domain]** ein.

   ![Dialogfeld „Branding-Domain bearbeiten“](./assets/me-admin-email-branding-domains-edit-default-name.png){width="400"}

1. Wenn Sie mehrere Arbeitsbereiche für Ihre Marketo Engage-Instanz definiert haben, klicken Sie auf **[!UICONTROL Weiter]**.

   Wählen Sie jeden der Arbeitsbereiche aus, auf den Sie die aktualisierte primäre Domain anwenden möchten.

   ![Dialogfeld „Branding-Domain bearbeiten“ mit Workspace-Auswahl für primäre Domain](./assets/me-admin-email-branding-domains-edit-default-workspaces.png){width="400"}

1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Definieren einer zusätzlichen Domain

Nachdem Sie die Standard-Domain bearbeitet haben, können Sie eine weitere Branding-Domain hinzufügen, um mehrere Marken in Ihrer Journey Optimizer B2B Edition-Umgebung zu unterstützen, wobei jede über eigene Branding-Tracking-Links verfügt. Beim Hinzufügen einer Domain stehen die folgenden Optionen zur Verfügung:

>* _Primäre Domain festlegen_: Wählen Sie diese als primäre Domain für den Arbeitsbereich aus. Wenn Sie diese Option auswählen, werden alle vorhandenen nicht gesendeten E-Mails auf die standardmäßige primäre Domain eingestellt und alle neu erstellten E-Mails werden automatisch auf diese primäre Domain eingestellt. Marketer können bei Bedarf eine alternative Branding-Domain auswählen.
>
>* _SSL-Zertifikat generieren_: Erstellen Sie eine Secure Sockets Layer (SSL) mit der Erstellung der Domain. Die erste Tracking-Domain startet eine einmalige Einrichtung der Infrastruktur, die einige Stunden dauern kann. Das System sendet nach Abschluss eine Benachrichtigung.

_Domain hinzufügen :_

1. Klicken Sie _[!UICONTROL Bedienfeld]_ Branding-Domains **[!UICONTROL oben]** „Hinzufügen“.

   ![Bedienfeld „Branding-Domains“ mit der Schaltfläche „Hinzufügen“ oben](assets/me-admin-email-branding-domains-add.png){width="500"}

1. Geben Sie im Dialogfeld _[!UICONTROL Neue Branding]_ Domain) im Feld **[!UICONTROL Domain]** den Namen der Branding-Domain ein.

1. (Optional) Aktivieren Sie das Kontrollkästchen **[!UICONTROL SSL-Zertifikat generieren]**, um automatisch eine SSL für die Domain zu generieren.

   ![Dialogfeld „Neue Branding-Domain“](assets/me-admin-email-branding-domains-add-name.png){width="400"}

   Bei Bedarf und nach Verfügbarkeit können Sie auch das Kontrollkästchen _Primäre Domain erstellen_ aktivieren.

   >[!NOTE]
   >
   >**_Benutzerdefinierte SSL_**: Wenn Sie eine benutzerdefinierte SSL benötigen, können Sie ein [Support-Ticket](https://experienceleague.adobe.com/de/support){target="_blank"} senden. Aktivieren Sie nicht das Kontrollkästchen für die SSL-Erstellung.

1. Wenn Sie mehrere Arbeitsbereiche für Ihre Marketo Engage-Instanz definiert haben, klicken Sie auf **[!UICONTROL Weiter]**.

   Wählen Sie bei Bedarf jeden der Arbeitsbereiche aus, auf die Sie die neue Domain als primäre Domain anwenden möchten.

   ![Dialogfeld „Neue Branding-Domain“ mit Workspace-Auswahl zum Anwenden der primären Domain](assets/me-admin-email-branding-domains-add-workspaces.png){width="400"}

1. Klicken Sie auf **[!UICONTROL Speichern]**.

## SSLs für bestehende Branding-Domains bearbeiten

Führen Sie diese Schritte aus, um SSL für Ihre bestehenden Domains zu aktivieren.

1. Wählen Sie im Bereich _[!UICONTROL Admin]_ die Option **[!UICONTROL E-Mail]** aus.

1. Wählen Sie im Bedienfeld _[!UICONTROL Branding]_ Domains“ die Zeile Domain aus und klicken Sie auf **[!UICONTROL SSL hinzufügen]**.

   ![Bedienfeld „Branding-Domains“ mit „SSL hinzufügen“ oben](./assets/me-admin-email-branding-domain-add-ssl.png){width="500"}

1. Klicken Sie im Dialogfeld auf &quot;**[!UICONTROL &quot;]**.

   ![Bestätigungsdialogfeld für SSL-Zertifikat generieren](./assets/me-admin-email-branding-domain-generate-ssl-cert-confirm.png){width="400"}

## Fehlermeldungen

| Fehler | Details |
| ----- | ------- |
| `Domain already exists.` | Eine Domain mit demselben Namen ist bereits vorhanden. |
| `Domain is not mapped to the default domain.` | Die benutzerdefinierte Domain wird nicht korrekt der Standard-Domain zugeordnet. Überprüfen Sie die Einstellungen für die Domain-Zuordnung und stellen Sie sicher, dass die DNS-Konfiguration auf die richtige Standard-Domain verweist. |
| `SSL certificates could not be issued due to unsupported CAA records. Request your IT to update your CAA records.` | Die CAA-Einträge sind nicht aktuell. Für Benutzer, die von Adobe verwaltete SSL-Zertifikate verwenden, müssen CAA-Einträge auf vom Anbieter empfohlene Zertifikate aktualisiert werden. |
| `SSL certificate has already been issued.` | Für diese benutzerdefinierte Domain ist bereits ein SSL-Zertifikat vorhanden. Es sind keine weiteren Maßnahmen erforderlich, es sei denn, das Zertifikat ist abgelaufen oder muss erneut ausgestellt werden. |
| `The default domain was not found. Please contact Support for assistance.` | Beim Suchen der Standard-Domain ist ein Problem aufgetreten. Adobe-Support kontaktieren, um Trigger zu untersuchen. |
| `Unexpected error encountered while creating a domain. Please contact Support for assistance.` | Es ist ein unerwarteter Fehler aufgetreten. Sammeln Sie Protokolle und Fehlerdetails und eskalieren Sie das Problem an den Adobe-Support. |

## Löschen einer Branding-Domain

>[!NOTE]
>
>Wenn Sie die primäre Branding-Domain (in einem oder mehreren Arbeitsbereichen) löschen möchten, müssen Sie zunächst eine andere Branding-Domain auswählen, die als primäre Domain für jeden Arbeitsbereich fungieren soll.
>
>Beim Löschen einer Domain **_nicht_** das SSL-Zertifikat gelöscht. Diese Schutzmaßnahme verhindert Benutzerfehler, die dazu führen, dass eine Website ohne SSL-Zertifikate ist. Wenn Sie die SSL-Zertifikate entfernen möchten, wenden Sie sich an den Adobe-Support.

Wählen Sie im Bedienfeld _[!UICONTROL Branding]_ Domains“ die Domain aus und klicken Sie oben **[!UICONTROL Löschen]**.
