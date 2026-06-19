---
title: Checkliste einrichten
description: Führen Sie die anfänglichen Einrichtungsaufgaben für Ihre Journey Optimizer B2B-Prime-Instanz aus, einschließlich der Konfiguration des Benutzerzugriffs und der Infrastruktur zur E-Mail-Zustellbarkeit.
autotag-review: '2026-06-12T23:06:52.179Z'
TQID: 'https://experienceleague.adobe.com/D8qXM-F4anA8IVYmdlaclUoxgTwqQptN36xYFpsuvHY'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: d6e625c1-468f-4d73-9f32-fd1edb87f96bid: f467931a-9b22-4ca8-869f-adfbd64061ceid: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1fid: f6df9def-cdf7-4728-9ec8-3f65716828c7
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: de83abd4ca48e2dfda8a1900f7c8074232bb9d8e
workflow-type: tm+mt
source-wordcount: 218
ht-degree: 11%

---

# Checkliste einrichten

Führen Sie diese Aufgaben aus, um die Funktionalität in Ihrer bereitgestellten [!DNL Journey Optimizer B2B Prime]-Instanz zu aktivieren.

## Benutzerzugriff aktivieren {#enable-user-access}

Wenn die Bereitstellung abgeschlossen und Sandboxes gebunden sind, konfigurieren Sie [!DNL Journey Optimizer B2B Edition] Zugriff für Ihr Team und Ihre Benutzer.

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
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox für Aufgabe"/></td>
<td>Erstellen eines Journey Optimizer B2B edition-Produktprofils in der Admin Console (nur einmaliges/erstmaliges Setup)</td>
<td><a href="./user-management.md#create-profile">Profil erstellen</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox für Aufgabe"/></td>
<td>Hinzufügen einer Benutzergruppe in der Admin Console</td>
<td><a href="./user-management.md#add-user-group">Benutzergruppe hinzufügen</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox für Aufgabe"/></td>
<td>Bearbeiten von integrierten Rollen oder Erstellen einer benutzerdefinierten Rolle mit Produktberechtigungen</td>
<td><a href="./user-management.md#edit-role-permissions">Rollen bearbeiten</a> <br/> <a href="./user-management.md#create-a-custom-role">Benutzerdefinierte Rolle erstellen</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox für Aufgabe"/></td>
<td>Hinzufügen von Benutzenden oder Gruppen zu Rollen in Adobe Experience Platform</td>
<td><a href="./user-management.md#add-users-to-a-role">Benutzer hinzufügen</a> <br/><a href="./user-management.md#add-user-groups-to-a-role">Gruppen hinzufügen</a></td>
</tr>
</tbody>
</table>

## Zustellbarkeit von E-Mails {#email-deliverability}

Bevor Marketer E-Mails von Journey-Benutzern senden können, müssen Sie die Versandinfrastruktur für Ihr Unternehmen konfigurieren, einschließlich Subdomain-Zuweisung, E-Mail-Authentifizierung und Kanaleinstellungen.

<table>
<thead>
<tr>
<th colspan="2">Aufgabe</th>
<th>Details und Anweisungen</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Konfigurieren der E-Mail-Zustellbarkeit und Kanaleinstellungen</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox für Aufgabe"/></td>
<td>Delegieren einer Subdomain an Adobe (vollständig delegiert oder CNAME)</td>
<td><a href="./admin/configuration-email-deliverability.md#delegate-fully-delegated">Vollständig delegiert</a> <br/> <a href="./admin/configuration-email-deliverability.md#delegate-cname">CNAME</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox für Aufgabe"/></td>
<td>Konfigurieren von DMARC für die Subdomain</td>
<td><a href="./admin/configuration-email-deliverability.md#configure-dmarc">Konfigurieren von DMARC</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox für Aufgabe"/></td>
<td>IP-Pool überprüfen und zuweisen</td>
<td><a href="./admin/configuration-email-deliverability.md#review-ip-pool">IP-Pool überprüfen</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox für Aufgabe"/></td>
<td>Erstellen einer E-Mail-Kanal-Konfiguration</td>
<td><a href="./admin/configuration-email-deliverability.md#create-email-channel-configuration">Konfigurieren des E-Mail-Kanals</a></td>
</tr>
</tbody>
