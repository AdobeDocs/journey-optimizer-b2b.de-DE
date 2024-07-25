---
title: Arbeiten mit Experience Manager Assets
description: Erfahren Sie, wie Sie beim Bearbeiten von Inhalten in Adobe Journey Optimizer B2B Edition Bild-Assets aus einem verbundenen AEM Assets-Repository verwenden können.
feature: Assets, Content
exl-id: c6864981-209c-4123-8d3f-24deb07026a0
source-git-commit: 7103e4f6666482a72511661dfaed1392d4eb16b1
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 1%

---

# Arbeiten mit Experience Manager-Assets

Wenn Adobe Experience Manager Assets as a Cloud Service in Adobe Journey Optimizer B2B Edition integriert ist, können Sie digitale Assets einfach entdecken und aufrufen, um sie in Ihren Marketinginhalten zu verwenden. Während Sie Ihren Inhalt erstellen, können Sie über das Element _[!UICONTROL Assets]_ im linken Navigationsbereich auf die Assets zugreifen und E-Mail-Journey-Inhalte für ein Konto erstellen. Sie können Assets auch direkt von Adobe Journey Optimizer B2B Edition in das angeschlossene AEM Assets as a Cloud Service-Repository hochladen.

>[!NOTE]
>
>Derzeit werden in Adobe Journey Optimizer B2B Edition nur Bild-Assets aus Adobe Experience Manager Assets unterstützt. Änderungen an den Assets müssen über das zentrale Adobe Experience Manager Assets-Repository vorgenommen werden. [Weitere Informationen](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/manage-digital-assets)

Wenn Sie diese digitalen Assets verwenden, werden die neuesten Änderungen in Assets as a Cloud Service über verknüpfte Verweise automatisch in Live-E-Mail-Kampagnen übernommen. Wenn Bilder in Adobe Experience Manager Assets as a Cloud Service gelöscht werden, werden die Bilder in den E-Mails mit einem fehlerhaften Verweis angezeigt. Wenn Assets geändert oder gelöscht werden, die derzeit in Konto-Journey verwendet werden, werden die Journey-Autoren über die Bildänderungen und die Liste der Journey benachrichtigt, die das Bild verwenden. Alle Änderungen an den Assets müssen im zentralen Repository von Adobe Experience Manager Assets vorgenommen werden.

## AEM Assets als Bildquelle verwenden

Wenn Ihre Umgebung über eine oder mehrere [Assets-Repository-Verbindungen](../admin/configure-aem-repositories.md) verfügt, können Sie AEM Assets als Quelle für Assets festlegen, wenn Sie Details für eine E-Mail, eine E-Mail-Vorlage oder ein visuelles Fragment erstellen oder anzeigen.

* Wenn Sie einen neuen Inhalt erstellen, wählen Sie `AEM Assets` als Element **[!UICONTROL Image Source]** im Dialogfeld.

  ![Wählen Sie AEM Assets als Bildquelle im Dialogfeld &quot;Erstellen&quot;aus](./assets/create-dialog-aem-assets.png){width="400"}

* Wenn Sie eine vorhandene Inhaltsressource öffnen, wählen Sie im Bereich _[!UICONTROL Hauptteil]_ rechts die Option &quot;`AEM Assets`&quot;.

  ![Wählen Sie AEM Assets als Bildquelle in den Eigenschaften aus](./assets/content-source-aem-assets.png){width="700" zoomable="yes"}

## Zugreifen auf Assets für die Bearbeitung

>[!IMPORTANT]
>
>Ein Administrator muss Benutzer, die Zugriff auf Assets benötigen, den Assets-Produktprofilen für Endanwender oder/und Assets-Benutzer hinzufügen. [Weitere Informationen](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/security/ims-support#managing-products-and-user-access-in-admin-console)

Klicken Sie im Visual Content Editor auf das Symbol _Asset-Wähler_ in der linken Seitenleiste. Dadurch wird der Tool-Bereich in eine Liste der verfügbaren Assets im ausgewählten Repository geändert.

![Klicken Sie auf das Assets-Auswahlsymbol, um auf die Bild-Assets zuzugreifen](./assets/content-assets-selector-aem-assets.png){width="700" zoomable="yes"}

Wenn mehrere Repositorys verbunden sind, klicken Sie auf den Menüpfeil für **[!UICONTROL Repository]**, um das Repository auszuwählen, das Sie verwenden möchten.

![Wählen Sie ein AEM Assets-Repository, um auf die Bild-Assets zuzugreifen](./assets/content-assets-selector-aem-repo.png){width="700" zoomable="yes"}

Es gibt mehrere Methoden zum Hinzufügen eines Bild-Assets zur visuellen Arbeitsfläche:

* Ziehen Sie eine Miniaturansicht per Drag-and-Drop aus der linken Navigation.

  ![Wählen Sie ein AEM Assets-Repository, um auf die Bild-Assets zuzugreifen](./assets/content-drag-drop-image-aem-assets.png){width="700" zoomable="yes"}

* Fügen Sie der Arbeitsfläche eine Bildkomponente hinzu und klicken Sie auf **[!UICONTROL Durchsuchen]** , um das Dialogfeld _[!UICONTROL Assets auswählen]_ zu öffnen.

  Im Dialogfeld können Sie ein Bild aus dem ausgewählten Repository auswählen.

  Es stehen mehrere Tools zur Verfügung, mit denen Sie das benötigte Asset finden können.

  ![Verwenden Sie das Tool im Dialogfeld &quot;Assets auswählen&quot;, um ein Bild-Asset zu suchen und auszuwählen](./assets/content-select-assets-dialog-aem.png){width="700" zoomable="yes"}

   * Ändern Sie das **[!UICONTROL Repository]** oben rechts.

   * Klicken Sie oben rechts auf **[!UICONTROL Assets verwalten]** , um das Assets-Repository in einer anderen Browser-Registerkarte zu öffnen und AEM Assets-Verwaltungstools zu verwenden.

   * Klicken Sie oben rechts auf den Selektor _Ansichtstyp_ , um die Anzeige in **[!UICONTROL Listenansicht]**, **[!UICONTROL Rasteransicht]**, **[!UICONTROL Galerie-Ansicht]** oder **[!UICONTROL Wasserfallansicht]** zu ändern.

   * Klicken Sie auf das Symbol _Sortierreihenfolge_ , um die Sortierreihenfolge zwischen auf- und absteigender Reihenfolge zu ändern.

   * Klicken Sie auf den Menüpfeil **[!UICONTROL Nach]** sortieren , um die Sortierkriterien in **[!UICONTROL Name]**, **[!UICONTROL Größe]** oder **[!UICONTROL Geändert]** zu ändern.

   * Klicken Sie oben links auf das Symbol _Filter_ , um die angezeigten Elemente nach Ihren Kriterien zu filtern.

   * Geben Sie Text in das Suchfeld ein, um die angezeigten Elemente nach einer Übereinstimmung mit dem Asset-Namen zu filtern.

  ![Verwenden Sie die Filter und das Suchfeld, um das Asset zu finden](./assets/content-select-assets-dialog-aem-filter.png){width="700" zoomable="yes"}

<!-- 
## Upload assets

To import files to Assets as a Cloud Service, you first need to browse or create the folder to be used for storage. You can then import an asset and add it to your email content. After assets are uploaded, you can [use the image assets as you author content](./assets-overview.md#add-assets-to-your-content).

1. While authoring your content in the email designer, drag an image element into the canvas. 

   The properties on the right reflect the image element selection. 

1. Click **[!UICONTROL Import media]** to open the _[!UICONTROL Upload image]_ dialog.

1. If your file system is open to your image file, drag and drop the file on the box in the dialog.

   ![Upload image file to Assets repository](./assets/email-designer-image-upload.png){width="700" zoomable="yes"}

   You can also click the **[!UICONTROL Select a file from your computer]** link and use your file system to locate and select the image file. Click Open and the image file is displayed in the box.

1. Click **[!UICONTROL Import]**.

-->
