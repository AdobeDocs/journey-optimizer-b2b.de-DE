---
title: E-Mail-Deduplizierung
description: Erfahren Sie, wie Sie die E-Mail-Deduplizierung in Account Journey verwenden, um zu verhindern, dass dieselbe E-Mail mehrmals an dieselbe E-Mail-Adresse gesendet wird.
feature: Account Journeys, Channels
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: E-Mail, Deduplizierung, Journey, Duplizierung
exl-id: 93107acd-1cb2-4316-acfc-e32ab1e065ae
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
  - id: f01b5556-e951-40ba-8625-2e3001864f2b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
autotag-review: 2026-03-30T22:08:16.582Z
TQID: https://experienceleague.adobe.com/aWKXaC6x4Izeh81A6Fpy-Nrf18fHgnq6jUc-82ohErs
source-git-commit: 9baf03a1ddc1733385b0398ffadde8f548c431cc
workflow-type: tm+mt
source-wordcount: 343
ht-degree: 1%

---

# E-Mail-Deduplizierung

Verwenden Sie die E-Mail-Deduplizierung in den Account-Journeys, um sicherzustellen, dass dieselbe E-Mail nicht mehrmals an dieselbe E-Mail-Adresse innerhalb einer Journey gesendet wird. Wenn Sie diese Funktion aktivieren, werden doppelte E-Mail-Adressen blockiert, bis der erste Eintrag mit dieser E-Mail-Adresse die Journey abgeschlossen hat. Nachdem ein Konto eine Journey abgeschlossen hat, kann eine Person sich erneut für den Empfang von E-Mails qualifizieren, wenn ein neues Konto auf die Journey zugreift.

## Verwendung der E-Mail-Deduplizierung

Es gibt einige wichtige Szenarien, in denen eine Deduplizierung der E-Mail in Betracht gezogen werden sollte:

* **E-Mail wird in Real-Time CDP nicht als Identität verwendet** - Dieselbe E-Mail-Adresse kann in mehreren Personenprofilen angezeigt werden. Wenn diese Profilduplikate für dieselbe Journey qualifiziert sind und Sie verhindern möchten, dass die E-Mail mehrmals gesendet wird, aktivieren Sie diese Funktion.

* **Einzelne Person mit mehreren Konten verknüpft** - Wenn Ihr Real-Time CDP-Datenmodell es ermöglicht, dass eine einzelne Person mehreren Konten zugeordnet werden kann, und Sie vermeiden möchten, dieselbe E-Mail zweimal an diese Person zu senden, wenn mehrere Konten (einschließlich Profilen mit derselben E-Mail-Adresse) für dieselbe Journey qualifiziert sind, aktivieren Sie diese Funktion.

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

Wenn die E-Mail-Deduplizierung aktiviert ist, prüft der Journey jede E-Mail-Adresse, bevor er die E-Mail sendet. Wenn bereits ein Eintrag mit derselben E-Mail-Adresse in diesen Journey-Knoten eingetreten ist, wird der neue Eintrag blockiert, bis der erste Eintrag die Journey abgeschlossen hat.
