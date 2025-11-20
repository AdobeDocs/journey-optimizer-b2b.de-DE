---
title: Assets
description: Verwalten von Bild-Assets aus Journey Optimizer B2B edition und AEM Assets für E-Mails, Vorlagen und Fragmente.
feature: Assets, Content
role: User
exl-id: f3848e65-3196-4d1f-90cf-7aa6ceeafabb
source-git-commit: 1c5a08b293db9287d03b103d794cc17a1c186af0
workflow-type: tm+mt
source-wordcount: '852'
ht-degree: 60%

---

# Assets

In [!DNL Adobe Journey Optimizer B2B Edition] sind Assets normalerweise die Bilder, die beim Gestalten von Inhalten für Konto-Journeys verwendet werden. Sie können diese Bilder in Ihren E-Mails, E-Mail-Vorlagen und Fragmenten über den Asset-Wähler oder eine einfache Drag-and-Drop-Oberfläche im visuellen Design-Bereich verwenden.

[!DNL Journey Optimizer B2B Edition] bietet Designern und Marketern Zugriff auf zwei Arten von Asset-Bibliotheken: ein internes [!DNL Journey Optimizer B2B Edition] Asset-Repository und [!DNL Adobe Experience Manager Assets as a Cloud Service]. Sie können nur das integrierte Repository verwenden oder beide Bibliothekstypen gleichzeitig verwenden (je nach vorhandener [!DNL Experience Manager Assets]).

## Asset-Management

Wenn Sie über [!DNL Adobe Experience Manager as a Cloud Services] verfügen und es als Asset-Quelle in [!DNL Journey Optimizer B2B Edition] konfiguriert ist, haben Sie Zugriff auf beide Repository-Typen, wenn Ihr Benutzerkonto über die erforderlichen Berechtigungen verfügt. Diese Repositorys sind getrennt und nicht synchronisiert. Sie können Bilder aus beiden Quellen verwenden.

### Interne Assets

Das interne Asset-Repository wird standardmäßig bei jedem [!DNL Journey Optimizer B2B Edition]-Abonnement bereitgestellt. Das bedeutet, dass Sie Zugriff auf alle Bild-Assets haben, die im verbundenen [!DNL Adobe Marketo Engage]-Asset-Dateisystem gespeichert sind. Sie können dieses Repository als lokale Asset-Bibliothek verwenden, also auch die Funktionen zum Hoch- und Herunterladen von Assets. Sie können diese Assets auch in Ihren Journey-Inhalten einsetzen.

Sie können [diese Assets mit Adobe Express bearbeiten](./image-edit-adobe-express.md) und sie in Ordner verschieben, um sie für die Verwendung in Ihren E-Mails, Vorlagen und Fragmenten zu organisieren.

Folgende Dateiformate werden unterstützt: JPG, JPEG, GIF, PNG, EPS, SVG und RGB.

### Adobe Experience Manager Assets as a Cloud Service

Zusammenführen von Marketing- und Kreativ-Workflows mithilfe von [!DNL Adobe Experience Manager Assets]. Diese Lösung ist nativ mit [!DNL Journey Optimizer B2B Edition] integriert, sodass Sie einfach auf Assets as a Cloud Service zugreifen können, um digitale Assets zu entdecken und zu verwenden. Sie bietet Zugriff auf Ihr Repository für Assets, das Sie für Ihre Nachrichten verwenden können.

[!DNL Adobe Journey Optimizer B2B Edition] kann mit [!DNL Adobe Experience Manager Assets as a Cloud Service] verbunden werden, um eine zentralisierte Asset-Verwaltung zu ermöglichen, die Ihr Kreativsystem erweitert und digitale Assets für die Bereitstellung von Erlebnissen vereinheitlicht. [!DNL Adobe Experience Manager Assets as a Cloud Service] bietet eine benutzerfreundliche Cloud-Lösung für effiziente Vorgänge im Bereich Digital Asset Management und Dynamic Media. Es integriert nahtlos fortschrittliche Funktionen, darunter künstliche Intelligenz und maschinelles Lernen.

Weitere Informationen finden Sie in der Dokumentation zu [Adobe Experience Manager Assets as a Cloud Service](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/assets/overview){target="_blank"}.

{{aem-assets-licensing-note}}

Greifen Sie über das Element **[!UICONTROL Experience Manager Assets]** im linken Navigationsbereich des Inhalts-Designs direkt in [!DNL Journey Optimizer B2B Edition] auf [!DNL Adobe Experience Manager Assets] zu. Sie können auf Assets und Ordner auch beim Entwerfen von E-Mails, E-Mail-Vorlagen und visuellen Fragmentinhalten zugreifen.

Derzeit können in Adobe Journey Optimizer B2B Edition nur Bilder aus Adobe Experience Manager Assets verwendet werden.

## Verwenden von Assets für die Inhaltserstellung

Verwenden Sie Assets beim Erstellen von E-Mails, E-Mail-Vorlagen und visuellen Fragmenten. Der visuelle Content-Editor bietet Zugriff auf die Bilder in Ihren verbundenen Asset-Repositorys. Wenn Sie auch über ein Abonnement für Experience Manager Assets as a Cloud Service verfügen, können Sie Bild-Assets aus beiden Quellen auswählen. Sie können auch ein Bild-Asset hochladen, wodurch es im internen Assets-Repository abgelegt wird.

Sie können die Bildquelle auswählen, wenn Sie die Einstellungen für eine Bildkomponente bearbeiten oder direkt auf der Arbeitsfläche Änderungen vornehmen.

* **_Einstellungen der Bildkomponente_** - Wenn Sie eine Bildkomponente auf der Arbeitsfläche ausgewählt haben, können Sie die Einstellungen im rechten Bedienfeld anzeigen und bearbeiten. Um die in der Komponente angezeigte Bilddatei hinzuzufügen oder zu ändern, wählen Sie den Quelltyp und dann eine Bilddatei aus.

  ![Bearbeiten der Einstellungen der Bildkomponente im rechten Panel](./assets/content-assets-image-settings.png){width="350"}

* **_Leere Komponente_** - Wenn Sie eine Bildkomponente zur Arbeitsfläche hinzufügen, ist sie leer und bietet einfachen Zugriff zum Auswählen einer Quelle und einer Bilddatei.

  ![Auswählen einer Quelle, um eine Bilddatei für die leere Bildkomponente festzulegen](./assets/content-assets-image-component-empty.png){width="500"}

* **_Bildkomponenten-Symbolleiste_** - Wenn Sie eine Bildkomponente auf der Arbeitsfläche ausgewählt haben, bietet die Symbolleiste einfachen Zugriff, um eine Quelle und die Bilddatei auszuwählen.

  ![Auswählen einer Quelle und einer Bilddatei für die Bildkomponente mithilfe der Symbolleiste](./assets/content-assets-image-toolbar-settings.png){width="500"}

Sie können ein Bild-Asset hinzufügen, während Sie Inhalte erstellen, je nach Quelle des Bild-Assets. Sie können ein Bild-Asset auch in den Hintergrundeinstellungen für eine Strukturkomponente auswählen.

>[!BEGINTABS]

>[!TAB Asset auswählen]

Klicken Sie auf **[!UICONTROL Asset auswählen]**, um den Asset-Wähler zu öffnen, in dem Sie ein Bild aus dem Journey Optimizer B2B edition Asset-Repository auswählen können.

![Bild-Asset auswählen](./assets/content-assets-internal-image-selected.png){width="700" zoomable="yes"}

Sie können die Suche und Filter verwenden, um das gewünschte Bild-Asset zu finden. Wählen Sie das Asset aus und klicken Sie auf **[!UICONTROL Auswählen]**, um es für die Bildkomponente zu verwenden.

Weitere Informationen zur Verwendung interner Bild-Assets finden Sie unter [Verwenden von Assets in Ihren Inhalten](./internal-image-assets.md#use-assets-in-your-content).

>[!TAB Experience Manager Assets]

Klicken Sie auf **[!UICONTROL Experience Manager Assets]**, um den Asset-Wähler zu öffnen. Dort können Sie ein Bild aus dem Experience Manager Assets-Repository auswählen.

![Auswählen eines Bild-Assets aus dem AEM Assets-Repository &#x200B;](./assets/content-assets-image-aem-selected.png){width="700" zoomable="yes"}

Sie können die Suche und Filter verwenden, um das gewünschte Bild-Asset zu finden. Wählen Sie das Asset aus und klicken Sie auf **[!UICONTROL Auswählen]**, um es für die Bildkomponente zu verwenden.

Weitere Informationen zur Verwendung von Bilddateien aus [!DNL Experience Manager Assets] finden Sie unter [Zugreifen auf AEM Assets-Bilder](./aem-assets.md#access-aem-assets-images).

>[!TAB Medien importieren]

Klicken Sie auf **[!UICONTROL Medien importieren]**, um eine Bilddatei auszuwählen und sie als Asset zu importieren, das für Journey Optimizer B2B Edition-Inhalte verwendet werden kann.

![Auswählen einer eigenen Bilddatei, die als Asset importiert werden soll](./assets/content-assets-image-import-file-selected.png){width="450" zoomable="yes"}

Nachdem Sie die Datei per Drag-and-Drop verschoben oder aus Ihrem Dateisystem ausgewählt haben, klicken Sie auf **[!UICONTROL Importieren]**. Das importierte Asset wird im [!DNL Journey Optimizer B2B Edition] Asset-Repository gespeichert.

>[!ENDTABS]
