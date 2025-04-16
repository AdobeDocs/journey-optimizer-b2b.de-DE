---
title: Assets
description: Erfahren Sie mehr über das Asset-Management in Journey Optimizer B2B Edition.
feature: Assets, Content
exl-id: f3848e65-3196-4d1f-90cf-7aa6ceeafabb
source-git-commit: 728d5316cfdeee92bd4f67277d299bbec2773a4f
workflow-type: ht
source-wordcount: '981'
ht-degree: 100%

---

# Assets

In Adobe Journey Optimizer B2B Edition sind Assets normalerweise die Bilder, die beim Gestalten von Inhalten für Account-Journeys verwendet werden. Sie können diese Bilder in E-Mails, E-Mail-Vorlagen und Fragmenten über einen Asset-Wähler oder eine einfache Drag-and-Drop-Oberfläche im visuellen Content-Editor nutzen.

Adobe Journey Optimizer B2B Edition bietet Marketing-Fachleuten Zugriff auf zwei Arten von Asset-Bibliotheken: Adobe Marketo Engage Design Studio und Adobe Experience Manager Assets as a Cloud Service. Sie können entweder ausschließlich Adobe Marketo Engage Design Studio oder gleichzeitig beide konfigurierten Bibliotheken verwenden (je nach der von Ihnen verwendeten AEM Assets-Lizenz).

## Asset-Management

Wenn Sie über ein Abonnement für Adobe Experience Manager as a Cloud Service verfügen, haben Sie Zugriff auf die Repositorys für Marketo Engage Design Studio und Adobe Experience Manager Assets as a Cloud Service, sofern Ihr Benutzerkonto über die erforderlichen Berechtigungen verfügt. Diese Repositorys sind getrennt und nicht synchronisiert. Sie können Bilder aus beiden Quellen verwenden.

### Adobe Marketo Engage-Assets

Das Assets-Repository von Adobe Marketo Engage Design Studio wird standardmäßig mit jedem Journey Optimizer B2B Edition-Abonnement bereitgestellt. Das bedeutet, dass Sie Zugriff auf alle in Adobe Marketo Engage gespeicherten Bild-Assets haben ([!UICONTROL Design-Studio] > [!UICONTROL Bilder und Dateien]). Sie können dieses Repository als lokale Asset-Bibliothek verwenden, also auch die Funktionen zum Hoch- und Herunterladen von Assets. Sie können diese Assets auch in Ihren Journey-Inhalten einsetzen.

Es gibt integrierte Schutzmechnismen, die Änderungen an den Marketo Engage-Assets von Journey Optimizer B2B Edition sowie Lösch- und Verschiebevorgänge verhindern. Diese Schutzmaßnahmen stellen sicher, dass die Quell-Assets (Marketo Engage Design Studio) beibehalten werden und gleichzeitig ein nahtloses Lesen und Wiederverwenden in Journey Optimizer B2B Edition möglich ist.

Folgende Dateiformate werden unterstützt: JPG, JPEG, GIF, PNG, EPS, SVG und RGB.

### Adobe Experience Manager Assets as a Cloud Service

Mithilfe von Adobe Experience Manager Assets können Sie Marketing- und Kreativ-Workflows zusammenführen. Diese Lösung ist nativ mit Adobe Journey Optimizer B2B Edition integriert, sodass Sie einfach auf Assets as a Cloud Service zugreifen können, um digitale Assets zu entdecken und zu verwenden. Sie bietet Zugriff auf Ihr Repository für Assets, die Sie für Ihre Nachrichten verwenden können.

Adobe Journey Optimizer B2B Edition kann eine Verbindung zu Adobe Experience Manager Assets as a Cloud Service herstellen und so ein zentrales Asset-Management ermöglichen, das Ihr Kreativsystem erweitert und digitale Assets für die Bereitstellung von Erlebnissen vereinheitlicht. Adobe Experience Manager Assets as a Cloud Service bietet eine benutzerfreundliche Cloud-Lösung für effiziente Digital Asset Management- und Dynamic Media-Vorgänge. Es integriert nahtlos fortschrittliche Funktionen, darunter künstliche Intelligenz und maschinelles Lernen.

Weitere Informationen finden Sie in der Dokumentation zu [Adobe Experience Manager Assets as a Cloud Service](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/assets/overview).

{{aem-assets-licensing-note}}

Um Adobe Experience Manager Assets direkt in Journey Optimizer B2B Edition aufzurufen, wählen Sie das Element **[!UICONTROL Experience Manager Assets]** im linken Navigationsbereich für das Content-Design aus. Sie können auf Assets und Ordner auch beim Entwerfen von E-Mails, E-Mail-Vorlagen und visuellen Fragmentinhalten zugreifen.

Derzeit können in Adobe Journey Optimizer B2B Edition nur Bilder aus Adobe Experience Manager Assets verwendet werden.

## Verwenden von Assets für die Inhaltserstellung

Verwenden Sie Assets beim Erstellen von E-Mails, E-Mail-Vorlagen und visuellen Fragmenten. Der visuelle Content-Editor bietet Zugriff auf die Bilder in Ihren verbundenen Asset-Repositorys. Wenn Sie über ein Abonnement für Experience Manager Assets as a Cloud Service und die Standardversion von Adobe Marketo Engage Design Studio verfügen, können Sie Bild-Assets aus beiden Quellen auswählen. Sie können auch ein Bild-Asset hochladen, wodurch es im Journey Optimizer B2B Edition-Arbeitsbereich des verbundenen Marketo Engage Design Studio-Repositorys platziert wird.

Sie können die Bildquelle auswählen, wenn Sie die Einstellungen für eine Bildkomponente bearbeiten oder direkt auf der Arbeitsfläche Änderungen vornehmen.

* **_Einstellungen der Bildkomponente_**: Wenn Sie eine Bildkomponente im visuellen Designer ausgewählt haben, können Sie die Einstellungen im rechten Panel anzeigen und bearbeiten. Um die in der Komponente angezeigte Bilddatei hinzuzufügen oder zu ändern, wählen Sie den Quelltyp und dann eine Bilddatei aus.

  ![Bearbeiten der Einstellungen der Bildkomponente im rechten Panel](./assets/content-assets-image-settings.png){width="350"}

* **_Leere Komponente_**: Wenn Sie eine Bildkomponente im visuellen Designer hinzufügen, ist sie leer und bietet einen einfachen Zugriff, um eine Quelle und eine Bilddatei auszuwählen.

  ![Auswählen einer Quelle, um eine Bilddatei für die leere Bildkomponente festzulegen](./assets/content-assets-image-component-empty.png){width="500"}

* **_Bildkomponenten-Symbolleiste_**: Wenn Sie eine Bildkomponente im visuellen Designer ausgewählt haben, bietet die Symbolleiste einen einfachen Zugriff, um eine Quelle und die Bilddatei auszuwählen.

  ![Auswählen einer Quelle und einer Bilddatei für die Bildkomponente mithilfe der Symbolleiste](./assets/content-assets-image-toolbar-settings.png){width="500"}

Sie können ein Bild-Asset hinzufügen, während Sie Inhalte erstellen, je nach Quelle des Bild-Assets.

>[!BEGINTABS]

>[!TAB Marketo Engage Assets]

Klicken Sie auf **[!UICONTROL Marketo Engage Assets]**, um den Asset-Wähler zu öffnen. Dort können Sie ein Bild aus einem Marketo Engage-Arbeitsbereich oder dem Journey Optimizer B2B Edition-Arbeitsbereich auswählen.

![Auswählen eines Bild-Assets aus dem Arbeitsbereich](./assets/content-assets-image-me-selected.png){width="700" zoomable="yes"}

Sie können die Suche und Filter verwenden, um das gewünschte Bild-Asset zu finden. Wählen Sie das Asset aus und klicken Sie auf **[!UICONTROL Auswählen]**, um es für die Bildkomponente zu verwenden.

Detaillierte Informationen zur Verwendung von Bild-Assets finden Sie unter [Verwenden von Assets in Ihren Inhalten](./marketo-engage-design-studio.md#use-assets-in-your-content).

>[!TAB Experience Manager Assets]

Klicken Sie auf **[!UICONTROL Experience Manager Assets]**, um den Asset-Wähler zu öffnen. Dort können Sie ein Bild aus dem Experience Manager Assets-Repository auswählen.

![Auswählen eines Bild-Assets aus dem AEM Assets-Repository ](./assets/content-assets-image-aem-selected.png){width="700" zoomable="yes"}

Sie können die Suche und Filter verwenden, um das gewünschte Bild-Asset zu finden. Wählen Sie das Asset aus und klicken Sie auf **[!UICONTROL Auswählen]**, um es für die Bildkomponente zu verwenden.

Detaillierte Informationen zur Verwendung von Bilddateien aus Experience Manager Assets finden Sie unter [Zugreifen auf AEM Assets-Bilder](./aem-assets.md#access-aem-assets-images).

>[!TAB Medien importieren]

Klicken Sie auf **[!UICONTROL Medien importieren]**, um eine Bilddatei auszuwählen und sie als Asset zu importieren, das für Journey Optimizer B2B Edition-Inhalte verwendet werden kann.

![Auswählen einer eigenen Bilddatei, die als Asset importiert werden soll](./assets/content-assets-image-import-file-selected.png){width="500" zoomable="yes"}

Nachdem Sie die Datei per Drag-and-Drop verschoben oder aus Ihrem Dateisystem ausgewählt haben, klicken Sie auf **[!UICONTROL Importieren]**. Das importierte Asset wird im Journey Optimizer B2B Edition-Arbeitsbereich des Adobe Marketo Engage Design Studio-Repositorys gespeichert.

>[!ENDTABS]
