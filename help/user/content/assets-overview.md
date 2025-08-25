---
title: Assets
description: Erfahren Sie mehr über das Asset-Management in Journey Optimizer B2B Edition.
feature: Assets, Content
role: User
exl-id: f3848e65-3196-4d1f-90cf-7aa6ceeafabb
source-git-commit: ea2093b03ba89f9e8d3f0db60b65cb143603c217
workflow-type: tm+mt
source-wordcount: '871'
ht-degree: 48%

---

# Assets

In der [!DNL Adobe Journey Optimizer B2B Edition] sind Assets normalerweise die Bilder, die beim Entwerfen von Inhalten zur Unterstützung von Account-Journey verwendet werden. Sie können diese Bilder in E-Mails, E-Mail-Vorlagen und Fragmenten über einen Asset-Wähler oder eine einfache Drag-and-Drop-Oberfläche im visuellen Design-Bereich verwenden.

[!DNL Journey Optimizer B2B Edition] bietet Marketing-Experten Zugriff auf zwei Arten von Asset-Bibliotheken: [!DNL Adobe Marketo Engage] [!DNL Design Studio] und [!DNL Adobe Experience Manager Assets as a Cloud Service]. Sie können nur Adobe Marketo Engage Design Studio verwenden oder beide Bibliotheken gleichzeitig konfigurieren (basierend auf der von Ihnen verwendeten [!DNL Experience Manager Assets]).

## Asset-Management

Wenn Sie über [!DNL Adobe Experience Manager as a Cloud Services] verfügen, haben Sie Zugriff auf die Repositorys für [!DNL Marketo Engage Design Studio] und [!DNL Adobe Experience Manager Assets as a Cloud Service], wenn Ihr Benutzerkonto über die erforderlichen Berechtigungen verfügt. Diese Repositorys sind getrennt und nicht synchronisiert. Sie können Bilder aus beiden Quellen verwenden.

### Adobe Marketo Engage-Assets

Das [!DNL Adobe Marketo Engage Design Studio] Assets-Repository wird standardmäßig mit jedem [!DNL Journey Optimizer B2B Edition]-Abonnement bereitgestellt. Das bedeutet, dass Sie Zugriff auf alle in [!DNL Adobe Marketo Engage] gespeicherten Bild-Assets haben ([!UICONTROL Design Studio] > [!UICONTROL Bilder und Dateien]). Sie können dieses Repository als lokale Asset-Bibliothek verwenden, also auch die Funktionen zum Hoch- und Herunterladen von Assets. Sie können diese Assets auch in Ihren Journey-Inhalten einsetzen.

Es gibt integrierte Leitplanken, die verhindern, dass Änderungen an den [!DNL Marketo Engage] Assets [!DNL Journey Optimizer B2B Edition] werden und Vorgänge zum Löschen und Verschieben ausgeführt werden können. Diese Schutzmaßnahmen stellen sicher, dass die Quell-Assets (Marketo Engage Design Studio) beibehalten werden und gleichzeitig das nahtlose Lesen und Wiederverwenden in [!DNL Journey Optimizer B2B Edition] ermöglicht wird.

Folgende Dateiformate werden unterstützt: JPG, JPEG, GIF, PNG, EPS, SVG und RGB.

### Adobe Experience Manager Assets as a Cloud Service

Zusammenführen von Marketing- und Kreativ-Workflows mithilfe von [!DNL Adobe Experience Manager Assets]. Sie ist nativ in [!DNL Journey Optimizer B2B Edition] integriert, sodass Sie einfach auf Assets as a Cloud Service zugreifen können, um digitale Assets zu finden und zu verwenden. Sie bietet Zugriff auf Ihr Repository für Assets, die Sie für Ihre Nachrichten verwenden können.

[!DNL Adobe Journey Optimizer B2B Edition] können eine Verbindung zu [!DNL Adobe Experience Manager Assets as a Cloud Service] herstellen, um zentralisiertes Asset-Management zu erhalten, das Ihr Kreativsystem erweitert und digitale Assets für die Bereitstellung von Erlebnissen zusammenfasst. [!DNL Adobe Experience Manager Assets as a Cloud Service] bietet eine benutzerfreundliche Cloud-Lösung für effizientes Digital Asset Management und Dynamic Media-Vorgänge. Es integriert nahtlos fortschrittliche Funktionen, darunter künstliche Intelligenz und maschinelles Lernen.

Weitere Informationen finden Sie in der Dokumentation zu [Adobe Experience Manager Assets as a Cloud Service](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/assets/overview){target="_blank"}.

{{aem-assets-licensing-note}}

Greifen Sie über das Element [!DNL Adobe Experience Manager Assets]Experience Manager Assets[!DNL Journey Optimizer B2B Edition] im linken Navigationsbereich des Inhaltsdesigns direkt in **[!UICONTROL auf]** zu. Sie können auf Assets und Ordner auch beim Entwerfen von E-Mails, E-Mail-Vorlagen und visuellen Fragmentinhalten zugreifen.

Derzeit können in Adobe Journey Optimizer B2B Edition nur Bilder aus Adobe Experience Manager Assets verwendet werden.

## Verwenden von Assets für die Inhaltserstellung

Verwenden Sie Assets beim Erstellen von E-Mails, E-Mail-Vorlagen und visuellen Fragmenten. Der visuelle Content-Editor bietet Zugriff auf die Bilder in Ihren verbundenen Asset-Repositorys. Wenn Sie über ein Abonnement für Experience Manager Assets as a Cloud Service und die Standardversion von Adobe Marketo Engage Design Studio verfügen, können Sie Bild-Assets aus beiden Quellen auswählen. Sie können auch ein Bild-Asset hochladen, wodurch es im [!DNL Journey Optimizer B2B Edition] Arbeitsbereich des verbundenen [!DNL Marketo Engage Design Studio]-Repositorys platziert wird.

Sie können die Bildquelle auswählen, wenn Sie die Einstellungen für eine Bildkomponente oder direkt auf der Arbeitsfläche bearbeiten:

* **_Einstellungen der Bildkomponente_** - Wenn Sie eine Bildkomponente im visuellen Design-Bereich ausgewählt haben, können Sie die Einstellungen im rechten Bedienfeld anzeigen und bearbeiten. Um die in der Komponente angezeigte Bilddatei hinzuzufügen oder zu ändern, wählen Sie den Quelltyp und dann eine Bilddatei aus.

  ![Bearbeiten der Einstellungen der Bildkomponente im rechten Panel](./assets/content-assets-image-settings.png){width="350"}

* **_Leere Komponente_** - Wenn Sie eine Bildkomponente im visuellen Design hinzufügen, ist sie leer und bietet einfachen Zugriff, um eine Quelle auszuwählen und eine Bilddatei auszuwählen.

  ![Auswählen einer Quelle, um eine Bilddatei für die leere Bildkomponente festzulegen](./assets/content-assets-image-component-empty.png){width="500"}

* **_Bildkomponenten-Symbolleiste_** - Wenn Sie eine Bildkomponente im visuellen Design-Bereich ausgewählt haben, bietet die Symbolleiste einfachen Zugriff, um eine Quelle und die Bilddatei auszuwählen.

  ![Auswählen einer Quelle und einer Bilddatei für die Bildkomponente mithilfe der Symbolleiste](./assets/content-assets-image-toolbar-settings.png){width="500"}

Sie können ein Bild-Asset hinzufügen, während Sie Ihre Inhalte erstellen, je nach Quelle des Bild-Assets. Sie können auch ein Bild-Asset in den Hintergrundeinstellungen für eine Strukturkomponente auswählen.

>[!BEGINTABS]

>[!TAB Marketo Engage Assets]

Klicken Sie auf **[!UICONTROL Marketo Engage Assets]**, um den Asset-Wähler zu öffnen, in dem Sie ein Bild aus einem [!DNL Marketo Engage] oder dem Journey Optimizer B2B edition-Arbeitsbereich auswählen können.

![Auswählen eines Bild-Assets aus dem Arbeitsbereich](./assets/content-assets-image-me-selected.png){width="700" zoomable="yes"}

Sie können die Suche und Filter verwenden, um das gewünschte Bild-Asset zu finden. Wählen Sie das Asset aus und klicken Sie auf **[!UICONTROL Auswählen]**, um es für die Bildkomponente zu verwenden.

Weitere Informationen zur Verwendung [!DNL Marketo Engage] Bild-Assets finden Sie unter [Verwenden von Assets in Ihrem Inhalt](./marketo-engage-design-studio.md#use-assets-in-your-content).

>[!TAB Experience Manager Assets]

Klicken Sie auf **[!UICONTROL Experience Manager Assets]**, um den Asset-Wähler zu öffnen. Dort können Sie ein Bild aus dem Experience Manager Assets-Repository auswählen.

![Auswählen eines Bild-Assets aus dem AEM Assets-Repository ](./assets/content-assets-image-aem-selected.png){width="700" zoomable="yes"}

Sie können die Suche und Filter verwenden, um das gewünschte Bild-Asset zu finden. Wählen Sie das Asset aus und klicken Sie auf **[!UICONTROL Auswählen]**, um es für die Bildkomponente zu verwenden.

Weitere Informationen zur Verwendung von Bilddateien aus [!DNL Experience Manager Assets] finden Sie unter [Zugriff auf AEM Assets-Bilder](./aem-assets.md#access-aem-assets-images).

>[!TAB Medien importieren]

Klicken Sie auf **[!UICONTROL Medien importieren]**, um eine Bilddatei auszuwählen und sie als Asset zu importieren, das für Journey Optimizer B2B Edition-Inhalte verwendet werden kann.

![Auswählen einer eigenen Bilddatei, die als Asset importiert werden soll](./assets/content-assets-image-import-file-selected.png){width="500" zoomable="yes"}

Nachdem Sie die Datei per Drag-and-Drop verschoben oder aus Ihrem Dateisystem ausgewählt haben, klicken Sie auf **[!UICONTROL Importieren]**. Das importierte Asset wird im Arbeitsbereich [!DNL Journey Optimizer B2B Edition] des [!DNL Adobe Marketo Engage Design Studio]-Repositorys gespeichert.

>[!ENDTABS]
