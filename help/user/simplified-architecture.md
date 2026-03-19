---
title: Vereinfachte Architektureinrichtung
description: Richten Sie Journey Optimizer B2B edition auf der vereinfachten Architektur ein. Konfigurieren Sie XDM-Schemata, E-Mail-/SMS-Kanäle, Marketo Engage-Journey-Aktionen und Benutzende.
feature: Setup, Administration
role: Admin, Data Engineer
exl-id: 81232976-09d6-4e10-a034-5c193a63b7df
source-git-commit: 38d1794ed30a34dbb34dfaec2d3088bc3a4680ac
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 17%

---

# Vereinfachte Architektureinrichtung

Adobe Journey Optimizer B2B Edition ist jetzt in einer vereinfachten Architektur verfügbar. Mit dieser Architektur befinden sich Journey Optimizer B2B edition und Marketo Engage nicht mehr auf demselben System und in demselben Datenspeicher. Journey Optimizer B2B Edition empfängt Daten nur von Adobe Experience Platform. Sie ist jedoch weiterhin auf Marketo Engage-Berechtigungen und einige Backend-Funktionen wie E-Mail-Versand angewiesen, um das System bereitzustellen und zu konfigurieren.

Die vereinfachte Architektur ist die Grundlage, auf der neue Funktionen in Journey Optimizer B2B edition freigeschaltet werden:

* **Vereinheitlichen und skalieren Sie Ihre Daten auf einfache Weise:** Die neue Plattform unterstützt komplexe Datenmodelle, einschließlich benutzerdefinierter Objekte, Einkaufsgruppen und Kontoereignisse.

* **Mehrere Adobe Marketo Engage-Instanzen verbinden:** Verwalten und Vereinheitlichen von Daten aus mehreren Marketo Engage-Umgebungen an einem Ort.

* **Schützt Ihre Daten:** Erweiterte Datenschutz- und Sicherheitsfunktionen zum Schutz Ihrer Kundendaten. (_in Kürze verfügbar_)

* **Für die Zukunft entwickelt:** Mit diesem Upgrade sind Sie bereit für kontinuierliche Verbesserungen und Innovationen.

Verwenden Sie für Umgebungen, die für diese Architektur bereitgestellt werden, die folgenden Konfigurationsrichtlinien.

Verwenden Sie diese Checkliste, um die Einrichtung von Journey Optimizer B2B edition auf der vereinfachten Architektur abzuschließen.

## &#x200B;1. Generieren von B2B-Namespaces und -Schemata

<table>
<thead>
<tr>
<th colspan="2">Aufgabe</th>
<th>Details und Anweisungen</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Einrichten der Umgebung:</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>Laden Sie den Namespace und das Dienstprogramm zur automatischen Schemaerstellung von GitHub herunter.</td>
<td><a href="./data/namespaces-schemas.md#set-up-the-auto-generation-utility">Weitere Informationen</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>Sammeln Sie Experience Platform-API-Anmeldeinformationen und erforderliche Kopfzeilen.</td>
<td><a href="https://experienceleague.adobe.com/de/docs/experience-platform/landing/platform-apis/api-guide">Weitere Informationen</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>Wenden Sie Umgebungswerte auf Ihre Postman-Umgebung an.</td>
<td><a href="./data/namespaces-schemas.md#environment-values">Weitere Informationen</a></td>
</tr>
<tr>
<td colspan="2"><strong>Skripte ausführen:</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>Führen Sie das <em>Namespaces und Schemata</em> in Postman aus und bestätigen Sie, dass Namespaces und Schemata erstellt wurden.</td>
<td><a href="./data/namespaces-schemas.md#run-the-scripts">Weitere Informationen</a></td>
</tr>
</tbody>
</table>

## &#x200B;2. XDM-Felder und -Ereignisse konfigurieren

<table>
<thead>
<tr>
<th colspan="2">Aufgabe</th>
<th>Details und Anweisungen</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Standard-XDM-Klassen</strong>: Richten Sie Klassen für XDM Individual Profile und XDM Business Account ein.</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>Wählen Sie verwaltete Felder aus, die für Journey, Einkaufsgruppen und E-Mail-Personalisierung verfügbar gemacht werden sollen.</td>
<td><a href="./admin/xdm-field-management.md#standard-classes">Weitere Informationen</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>Bearbeitbare Felder für Schemata.</td>
<td><a href="./admin/xdm-field-management.md#updatable-fields">Weitere Informationen</a></td>
</tr>
<tr>
<td colspan="2"><strong>Relationale Schemata</strong>: Wählen Sie die relationale XDM-Klasse aus (benutzerdefiniertes Konto: Viele-zu-eins-Objekt).</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>Stellen Sie sicher, dass Schemata über die erforderlichen Konfigurationswerte verfügen.</td>
<td><a href="./admin/xdm-field-management.md#relational-schemas">Weitere Informationen</a></td>
</tr>
<tr>
<td colspan="2"><strong>Ereignisse</strong>: Konfigurieren von Ereignistypen und -feldern in Experience Platform.</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>Konfigurieren Sie jeden Experience Platform-Ereignistyp mit Feldern, die in Journey-Entscheidungs-/Aufspaltungspfaden unterstützt werden sollen.</td>
<td><a href="./admin/configure-aep-events.md">Weitere Informationen</a></td>
</tr>
</tbody>
</table>

## &#x200B;3. Tracking und E-Mail-Zustellbarkeit konfigurieren

Um E-Mails von [!DNL Journey Optimizer B2B Edition] über die vereinfachte Architektur zu senden, konfigurieren Sie das E-Mail-Tracking und die Zustellbarkeit in der angehängten [!DNL Marketo Engage]-Produktionsinstanz und in der [!DNL Journey Optimizer B2B Edition]-App.

<table>
<thead>
<tr>
<th colspan="2">Aufgabe</th>
<th>Details und Anweisungen</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Ersteinrichtung</strong> für die angeschlossene Marketo Engage-Instanz</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>Neuen CNAME für Tracking-Links in DNS-Einträgen konfigurieren</td>
<td><a href="./start/email-protocols.md#create-dns-records-for-landing-pages-and-email">Weitere Informationen</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>Konfigurieren von Branding-Domains für die angehängte Marketo Engage-Instanz</td>
<td><a href="./start/branding-domains.md">Weitere Informationen</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>Konfigurieren von DKIM und SPF für die angeschlossene Marketo Engage-Instanz</td>
<td><a href="./start/email-protocols.md#set-up-spf-and-dkim">Weitere Informationen</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>Einrichten von DMARC</td>
<td><a href="./start/email-protocols.md#set-up-dmarc">Weitere Informationen</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>Einrichten von MX-Einträgen für Ihre Domain</td>
<td><a href="./start/email-protocols.md#set-up-mx-records-for-your-domain">Weitere Informationen</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>Hinzufügen ausgehender IP-Adressen zu Zulassungslisten</td>
<td><a href="./start/email-protocols.md#outbound-ip-addresses">Weitere Informationen</a></td>
</tr>
<tr>
<td colspan="2"><strong>E-Mail-Setup</strong> für die angehängte Marketo Engage-Instanz</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>Konfigurieren von <em>Von E-Mail</em> und <em>Von Beschriftung</em> (optional)</td>
<td><a href="./start/email-setup.md#from-email-and-label">Weitere Informationen</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>Konfigurieren von <em>HTML abmelden</em> und <em>Text zum Abmelden</em></td>
<td><a href="./start/email-setup.md#unsubscribe-messaging">Weitere Informationen</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>Konfigurieren <em>Als Webseite anzeigen HTML</em> und <em>Als Webseite anzeigen Text</em></td>
<td><a href="./start/email-setup.md#view-as-web-page">Weitere Informationen</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>Konfigurieren Sie <em>Beschränkungen für benutzerdefinierte Objektabrufe</em></td>
<td><a href="./start/email-setup.md#custom-object-retrieval-limits">Weitere Informationen</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>Konfigurieren von <em>benutzerdefinierten Kopfzeilenoptionen</em></td>
<td><a href="./start/email-setup.md#custom-header-options">Weitere Informationen</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>Konfigurieren der <em>Bot-Aktivität</em> Filterung</td>
<td><a href="./start/email-setup.md#filter-email-bots">Weitere Informationen</a></td>
</tr>
<tr>
<td colspan="2"><strong>E-Mail-Kanalkonfiguration</strong> für Journey Optimizer B2B edition</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>Konfigurieren von <em>Kommunikationsbeschränkungen</em> in Journey Optimizer B2B edition</td>
<td><a href="./admin/configure-channels-emails.md#communication-limits">Weitere Informationen</a></td>
</tr>
</tbody>
</table>

<!-- TBD for later 

<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox"/></td>
<td>Configure <em>Email CC Settings</em></td>
<td>[Learn more](TBD)</td>
</tr>

<tr>
<td colspan="2"><strong>Additional configurations</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox"/></td>
<td>Configure <em>Location Settings</em> for the attached Marketo Engage instance</td>
<td>< [Learn more](TBD)</td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox"/></td>
<td>Define and configure which Binding Groups / IPs to move over</td>
<td>[Learn more](TBD)</td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox"/></td>
<td>Test Email Send</td>
<td>[Learn more](TBD)</td>
</tr>
-->

## &#x200B;4. Konfigurieren zusätzlicher Inhaltskanäle

Um Marketingexperten dabei zu unterstützen, andere Kanäle in ihre Journey aufzunehmen, konfigurieren Sie zusätzliche Kanäle.

<table>
<thead>
<tr>
<th colspan="2">Aufgabe</th>
<th>Details und Anweisungen</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>SMS</strong>-Kanalkonfiguration für Journey Optimizer B2B edition.</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>Konfigurieren Sie jedes SMS-Konto, das Sie unterstützen möchten.</td>
<td><a href="./admin/configure-channels-sms.md">Weitere Informationen</a></td>
</tr>
<tr>
<td colspan="2"><strong>Landingpages</strong> (Beta)-Kanalkonfiguration für Journey Optimizer B2B edition</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>Füllen Sie die Einstellungen der Landingpage aus, um Marketing-Experten zu unterstützen, die diese Seiten erstellen und veröffentlichen</td>
<td><a href="./admin/landing-page-settings.md">Weitere Informationen</a></td>
</tr>
<tr>
<td colspan="2"><strong>Web</strong> (Beta)-Kanalkonfiguration für Journey Optimizer B2B edition</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>Konfigurieren Sie Ihre Business-Website zur Unterstützung der Adobe Experience Platform Web SDK.</td>
<td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/js-overview">Weitere Informationen</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>Fügen Sie Web-Eigenschaften über eine URL hinzu, über die der Inhalt bereitgestellt wird.</td>
<td><a href="./admin/configure-channels-web.md">Weitere Informationen</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>Weisen Sie Web-Erlebnisautoren an, die Browser-Erweiterung Adobe Experience Cloud Visual Editing Helper zu installieren.</td>
<td><a href="./content/web-experiences.md#install-the-visual-editing-helper-extension">Weitere Informationen</a></td>
</tr>
</tbody>
</table>

## &#x200B;5. Marketo Engage-Instanz verbinden, um Journey-Aktionen zu unterstützen (optional)

Wenn Sie planen, die Journey Optimizer B2B edition-Funktionen durch Kampagnen und Programme in Marketo Engage zu ergänzen, richten Sie die Unterstützung für Marketo Engage-Aktionen ein. Diese Aktionen ermöglichen es Ihren Marketing-Teams _ihr (Account-basiertes_ Marketing in Journey Optimizer B2B edition und _Lead-basiertes_ Marketing in Marketo Engage zu koordinieren.

<table>
<thead>
<tr>
<th colspan="2">Aufgabe</th>
<th>Details und Anweisungen</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Für jede Marketo Engage-Instanz</strong> um Journey-Aktionen zu unterstützen</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>Erstellen des benutzerdefinierten Marketo Engage-Service</td>
<td><a href="./admin/marketo-actions-connect.md#create-the-marketo-engage-custom-service">Weitere Informationen</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>Hinzufügen der Integration in Journey Optimizer B2B edition</td>
<td><a href="./admin/marketo-actions-connect.md#add-the-integration">Weitere Informationen</a></td>
</tr>
</tbody>
</table>

## &#x200B;6. Benutzerzugriff aktivieren

Wenn die Bereitstellung abgeschlossen ist, Sandboxes gebunden und die anfänglichen Einrichtungsaufgaben abgeschlossen sind, konfigurieren Sie den Zugriff auf Journey Optimizer B2B edition und Marketo Engage für Ihr Team und Ihre Benutzerinnen und Benutzer.

<table>
<thead>
<tr>
<th colspan="2">Aufgabe</th>
<th>Details und Anweisungen</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Produktzugriff und Berechtigungen für </strong> bereitstellen</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>Erstellen eines Marketo Engage-Produktprofils in der Adobe Admin Console (nur neue Marketo Engage-Instanz)</td>
<td><a href="./admin/user-management.md#create-the-marketo-engage-product-profile">Weitere Informationen</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>Hinzufügen einer Benutzergruppe für das Profil</td>
<td><a href="./admin/user-management.md#add-a-user-group-for-the-profile">Weitere Informationen</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>B2B-Benutzerrollen konfigurieren</td>
<td><a href="./admin/user-management.md#b2b-built-in-roles">Weitere Informationen</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>Hinzufügen von Benutzenden oder Gruppen zu den Rollen</td>
<td><a href="./admin/user-management.md#add-users-to-a-role">Weitere Informationen</a></td>
</tr>
</tbody>
</table>
