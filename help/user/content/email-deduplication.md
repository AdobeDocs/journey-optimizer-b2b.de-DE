---
title: E-Mail-Deduplizierung
description: Erfahren Sie, wie Sie die E-Mail-Deduplizierung in Account Journey verwenden, um zu verhindern, dass dieselbe E-Mail mehrmals an dieselbe E-Mail-Adresse gesendet wird.
feature: Account Journeys, Channels
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: E-Mail, Deduplizierung, Journey, Duplizierung
exl-id: 93107acd-1cb2-4316-acfc-e32ab1e065ae
autotag-review: 2026-03-30T22:08:16.582Z
TQID: 'https://experienceleague.adobe.com/aWKXaC6x4Izeh81A6Fpy-Nrf18fHgnq6jUc-82ohErs'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
    internal-label: Journeys
  - id: f01b5556-e951-40ba-8625-2e3001864f2b
    internal-label: Communication channels
  - id: d77af7eb-afc3-53f3-a50c-dabc0d05ecfd
    internal-label: Channels
subfeature_v2:
  - id: c31bc6c7-76bc-467b-80c0-7315a4e3f6be
    internal-label: Account Journeys
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: 21fbce544faf291ad01a3301a9981add95442097
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 1%
---
# E-Mail-Deduplizierung

Um sicherzustellen, dass dieselbe E-Mail nicht mehrmals an dieselbe E-Mail-Adresse innerhalb einer Journey gesendet wird, verwenden Sie die E-Mail-Deduplizierung in den Account Journey. Wenn Sie diese Funktion aktivieren, werden doppelte E-Mail-Adressen blockiert, bis der erste Eintrag mit dieser E-Mail-Adresse die Journey abgeschlossen hat. Nachdem ein Konto eine Journey abgeschlossen hat, kann eine Person sich erneut für den Empfang von E-Mails qualifizieren, wenn ein neues Konto auf die Journey zugreift.

## Verwendung der E-Mail-Deduplizierung

Für die Aktivierung der E-Mail-Deduplizierung sind folgende Schlüsselszenarien zu berücksichtigen:

* **E-Mail wird in Real-Time CDP nicht als Identität verwendet** - Dieselbe E-Mail-Adresse kann in mehreren Personenprofilen angezeigt werden. Wenn diese Profilduplikate für dieselbe Journey qualifiziert sind und Sie verhindern möchten, dass die E-Mail mehrmals gesendet wird, aktivieren Sie diese Funktion.

* **Einzelne Person mit mehreren Konten verknüpft** - Wenn Ihr [!DNL Real-Time CDP]-Datenmodell eine einzelne Person mit mehreren Konten verknüpft, aktivieren Sie diese Funktion, um zu vermeiden, dass dieselbe E-Mail zweimal gesendet wird, wenn mehrere Profile mit derselben E-Mail-Adresse für dieselbe Journey qualifiziert sind.

>[!NOTE]
>
>Die Deduplizierung von E-Mails erfolgt auf Journey-Ebene. Wenn sich eine Person mit derselben E-Mail-Adresse für verschiedene Journey qualifiziert, kann sie dennoch E-Mails von jeder Journey erhalten.

## E-Mail-Deduplizierung für einen Journey aktivieren

So aktivieren Sie die E-Mail-Deduplizierung für eine Konto-Journey:

1. Konto-Journey öffnen.

1. Klicken Sie **[!UICONTROL Mehr]** (**…**) In der oberen rechten Ecke des Arbeitsbereichs Journey.

   ![Journey-Arbeitsbereich mit erweitertem Menü „Mehr“ mit Option „E-Mail-Deduplizierung“](./assets/email-deduplication-more-menu.png){width="450"}

1. Wählen Sie **[!UICONTROL E-Mail-Deduplizierung]**.

1. Aktivieren Sie im Dialogfeld das Kontrollkästchen **[!UICONTROL E-Mail-Deduplizierung]**.

   ![Dialogfeld „E-Mail-Deduplizierung“ mit aktiviertem Umschalter](./assets/email-deduplication-dialog.png){width="400"}

1. Klicken Sie auf **[!UICONTROL Speichern]**.

Wenn die E-Mail-Deduplizierung aktiviert ist, prüft der Journey jede E-Mail-Adresse, bevor er die E-Mail sendet. Wenn bereits ein Eintrag mit derselben E-Mail-Adresse in diesen Journey-Knoten eingetreten ist, wird der neue Eintrag blockiert, bis der erste Eintrag den Journey beendet.
