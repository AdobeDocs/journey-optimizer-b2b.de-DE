---
title: E-Mail-Rendering testen
description: Erfahren Sie, wie Sie Ihr Litmus-Konto nutzen können, um das Rendering für E-Mails in Journey Optimizer B2B edition zu testen.
feature: Email Authoring, Integrations
level: Intermediate
role: User
exl-id: 26d87a56-6bd1-4d4a-8090-71f5b0a7e9f8
source-git-commit: dbb1c0d57f3d0b9818dc284047bda9562cfb40f6
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 3%

---

# Testen des E-Mail-Renderings mit Litmus

Zum Testen Ihrer E-Mails können Sie ein [Litmus](https://www.litmus.com/email-testing){target="_blank"} Enterprise-Konto von Journey Optimizer B2B edition nutzen. Mit dieser Integration können Sie das E-Mail-Rendering in gängigen E-Mail-Clients in der Vorschau anzeigen. Mit diesem Tool können Sie sicherstellen, dass Ihr E-Mail-Inhalt in jedem Posteingang gut aussieht und wie vorgesehen funktioniert.

>[!NOTE]
>
>Diese Integration ist nur für Litmus Enterprise-Konten verfügbar. Weitere Informationen finden Sie auf der Seite [Lösung auf der Litmus-Website](https://www.litmus.com/solutions/esp/adobe-journey-optimizer){target="_blank"}.

1. Wenn Ihr E-Mail-Design fertig ist und getestet werden kann, klicken **[!UICONTROL im E-]**-Design auf „Inhalt simulieren“.

1. Klicken Sie **[!UICONTROL oben]** auf „E-Mail rendern“.

   ![Schaltfläche „E-Mail rendern](./assets/email-simulate-render-button.png){width="700" zoomable="yes"}

   Wenn Sie noch keine Verbindung zu Ihrem Litmus -Konto über Journey Optimizer B2B edition hergestellt haben, bietet die angezeigte Seite eine Option zum Starten eines Testkontos oder zum Herstellen einer Verbindung zu Ihrem bestehenden Konto.

1. Klicken **[!UICONTROL oben rechts auf „Litmus-]** verbinden“ oder verwenden Sie den Link auf der Seite.

   ![Verbinden Sie Ihr Litmus-Konto](./assets/email-simulate-render-litmus-connect.png){width="700" zoomable="yes"}

1. Geben Sie Ihre Litmus-Kontoanmeldeinformationen ein und klicken Sie auf **[!UICONTROL Anmelden]**.

1. Klicken Sie **[!UICONTROL Verbinden]**, um die Verbindung zwischen Litmus und Journey Optimizer B2B edition zu bestätigen und den E-Mail-Inhalt zum Rendern zu senden.

   >[!IMPORTANT]
   >
   >Wenn Sie Ihr Litmus-Konto mit Journey Optimizer B2B edition verbinden, stimmen Sie zu, dass Testmeldungen an Litmus gesendet werden. Diese Inhalte werden dann in Litmus und nicht in Adobe verwaltet. Daher gilt für diese E-Mails die Litmus-Richtlinie zur Datenaufbewahrung, einschließlich der Personalisierungsdaten, die in die Testnachrichten aufgenommen werden können.

1. Klicken Sie **[!UICONTROL oben rechts auf]** Test ausführen), um E-Mail-Vorschauen zu generieren.

   ![Führen Sie einen Litmus-Rendering-Test aus](./assets/email-simulate-render-litmus-run-test.png){width="700" zoomable="yes"}

1. Prüfen Sie Ihren E-Mail-Inhalt auf gängigen Clients für Desktop, mobile Geräte und Web.

   Klicken Sie auf die angezeigte Miniaturansicht, um die Details für einen der gerenderten Client-Tests anzuzeigen.

   ![Litmus-E-Mail-Vorschau](./assets/email-simulate-render-litmus-previews.png){width="700" zoomable="yes"}

1. Wenn Sie mit der Überprüfung fertig sind, klicken Sie oben links auf den Rückwärtspfeil ![Filtersymbol ein- oder ausblenden](../../assets/do-not-localize/icon_back-arrow.svg), um zur Seite „Inhalt simulieren“ zurückzukehren.

   Sie können ein anderes Profil auswählen und einen weiteren Rendering-Test durchführen oder zum E-Mail-Design-Bereich zurückkehren, um die erforderlichen Anpassungen auf der Grundlage Ihrer Überprüfung vorzunehmen.
