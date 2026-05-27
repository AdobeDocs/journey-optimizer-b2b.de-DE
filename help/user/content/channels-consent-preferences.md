---
title: Einverständnis mit Kanalnachrichten
description: Erfahren Sie, wie Journey Optimizer B2B edition die Einstellungen für das Einverständnis des AEP-XDM-Profils liest und das Opt-in- und Opt-out-Verfahren zum Zeitpunkt des Nachrichtenversands für E-Mail-, SMS- und WhatsApp-Kanäle durchsetzt.
feature: Setup, Channels
role: Admin, User
autotag-review: '2026-05-19T16:18:37.228Z'
TQID: 'https://experienceleague.adobe.com/-c0dJnpfiIcj0B5gViyEQ7E1Ws0BwP864OLF003rOjw'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: f01b5556-e951-40ba-8625-2e3001864f2b
subfeature_v2: id: ff0c35fa-aa7e-4050-a37c-198fcacd09e6id: a22f05f6-0fcf-40c0-a70e-e13a3db185f7
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 8226114f1a34adf85437579ef17a50b80ccfa596
workflow-type: tm+mt
source-wordcount: 424
ht-degree: 2%

---

# Einverständnis mit Kanal-Messaging

Adobe Journey Optimizer B2B edition liest die in den XDM-Profilen von Adobe Experience Platform gespeicherten Einverständnisvoreinstellungen pro Person und erzwingt diese zum Zeitpunkt des Nachrichtenversands als Teil der [ der App](../admin/governance.md). Personen, die sich gegen einen Kanal entschieden haben, werden vom Versand ausgeschlossen, bevor Inhalte vom Kanal oder nachgelagerten Messaging-Anbieter gesendet werden.

In den folgenden Abschnitten wird beschrieben, wie Journey Optimizer B2B edition das Einverständnis zum Zeitpunkt des Nachrichtenversands für jeden unterstützten Kanal auswertet.

## E-Mail {#email}

Journey Optimizer B2B edition bewertet das folgende XDM-Attribut für das E-Mail-Einverständnis beim Senden von Nachrichten über den [E-Mail-Kanal](../admin/configure-channels-emails.md):

| XDM-Attribut | `y` | `n` | Kein Wert |
| --- | --- | --- | --- |
| `consents.marketing.email.val` | Opt-in | Opt-out | Opt-in |

Beachten Sie die folgenden Überlegungen für das Einverständnis per E-Mail:

* Personen, die sich global von E-Mails abgemeldet haben, können E-Mails erhalten, die als betriebsbereit markiert sind.
* Voreinstellungen auf Abonnementebene werden nicht unterstützt.

Informationen zur Abmeldeaktivität für gesendete E-Mails finden Sie im [E-Mail-Leistungsbericht](../dashboards/email-performance-dashboard.md).

## SMS {#sms}

Journey Optimizer B2B edition bewertet die folgenden XDM-Attribute für das SMS-Einverständnis beim Senden von Nachrichten über den [SMS-Kanal](../admin/configure-channels-sms.md):

| XDM-Attribut | `y` | `n` | Kein Wert |
| --- | --- | --- | --- |
| `consents.marketing.sms.val` | Opt-in | Opt-out | Opt-out |
| `consents.marketing.subscriptions.<senderID>` | Opt-in | Opt-out | Opt-out |
| `consents.marketing.sms.subscriptions.<senderId>.subscribers.<phoneNumber>` | Opt-in | Opt-out | Opt-out |

Beachten Sie die folgenden Überlegungen für das SMS-Einverständnis:

* Wenn ein Lead-(Personen-)Datensatz von der SMS abgemeldet wird, wird der Datensatz vollständig ausgeschlossen und nicht an nachgelagerte SMS-Anbieter weitergeleitet.
* Sofern verfügbar, wird das Einverständnis auf Abonnementebene ausgewertet. Die globale Abmeldung wird als Fallback verwendet, wenn die Zustimmung auf Abonnementebene nicht verfügbar ist.
* Personen, die sich vom SMS-Versand abgemeldet haben, können weiterhin Nachrichten erhalten, die als betriebsbereit gekennzeichnet sind.
* Wenn mehrere Lead-Datensätze dieselbe Telefonnummer haben, haben sie denselben Opt-in- oder Opt-out-Status.

## WhatsApp {#whatsapp}

Journey Optimizer B2B edition wertet die folgenden XDM-Attribute für das WhatsApp-Einverständnis aus, wenn Nachrichten über einen konfigurierten [WhatsApp-Kanal“ gesendet ](../admin/configure-channels-whatsapp.md):

| XDM-Attribut | `y` | `n` | Kein Wert |
| --- | --- | --- | --- |
| `consents.marketing.whatsApp.val` | Opt-in | Opt-out | Opt-out |
| `consents.idSpecific.Phone.<number>.marketing.whatsApp.val` | Opt-in | Opt-out | Opt-out |

Beachten Sie die folgenden Überlegungen für das Einverständnis mit WhatsApp:

* Wenn der globale WhatsApp-Attributwert (`consents.marketing.whatsApp.val`) vorhanden ist, wird er zur Einverständnisbewertung verwendet.
* Wenn der globale Attributwert nicht vorhanden ist, aber ein absenderspezifischer Eintrag vorhanden ist, wird der absenderspezifische Eintrag zur Einverständnisbewertung verwendet.
* Wenn für keines der Attribute ein Wert vorhanden ist, wird die Person als Opt-out behandelt.

## Nicht unterstützt {#not-supported}

Die folgenden einverständnisbezogenen Funktionen werden derzeit in Journey Optimizer B2B edition nicht unterstützt:

* AEP-Einverständnisrichtlinien
* Marketing-Attribute (`consents.marketing.preferred`)
