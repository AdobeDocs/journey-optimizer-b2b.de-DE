---
title: Setup
description: Führen Sie die anfänglichen Einrichtungsaufgaben für Ihre Journey Optimizer B2B-Prime-Instanz aus, einschließlich der Konfiguration des Benutzerzugriffs und der Infrastruktur zur E-Mail-Zustellbarkeit.
autotag-review: '2026-06-12T23:06:52.179Z'
TQID: 'https://experienceleague.adobe.com/D8qXM-F4anA8IVYmdlaclUoxgTwqQptN36xYFpsuvHY'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: d6e625c1-468f-4d73-9f32-fd1edb87f96b
  - id: f467931a-9b22-4ca8-869f-adfbd64061ce
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
  - id: f6df9def-cdf7-4728-9ec8-3f65716828c7
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: 0e90250101eef0572af0382cc7d24bca727d2b75
workflow-type: tm+mt
source-wordcount: 190
ht-degree: 55%

---

# Einrichten

Führen Sie diese Aufgaben aus, um die Funktionalität in Ihrer bereitgestellten Journey B2B-Prime-Instanz zu aktivieren.

## Benutzerzugriff aktivieren

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
<td><a href="./user-management.md#create-profile">Weitere Informationen</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>Hinzufügen einer Benutzergruppe für das Profil</td>
<td><a href="./user-management.md#add-user-group">Weitere Informationen</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>B2B-Benutzerrollen konfigurieren</td>
<td><a href="./user-management.md#edit-roles-for-product-permissions">Weitere Informationen</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>Hinzufügen von Benutzenden oder Gruppen zu den Rollen</td>
<td><a href="./user-management.md#add-users-to-a-role">Weitere Informationen</a></td>
</tr>
</tbody>
</table>

## Zustellbarkeit von E-Mails

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
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>Delegieren einer Subdomain an Adobe</td>
<td><a href="./admin/configuration-email-deliverability.md#delegate-fully-delegated">Vollständig delegiert</a> oder <a href="./admin/configuration-email-deliverability.md#delegate-cname">CNAME</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>Konfigurieren von DMARC für die Subdomain</td>
<td><a href="./admin/configuration-email-deliverability.md#configure-dmarc">Weitere Informationen</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>IP-Pool überprüfen und zuweisen</td>
<td><a href="./admin/configuration-email-deliverability.md#review-ip-pool">Weitere Informationen</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kontrollkästchen"/></td>
<td>Erstellen einer E-Mail-Kanal-Konfiguration</td>
<td><a href="./admin/configuration-email-deliverability.md#create-email-channel-configuration">Weitere Informationen</a></td>
</tr>
</tbody>
</table>
<!-- -->

