---
title: Assets
description: Verwalten von Bild-Assets aus Journey Optimizer B2B edition für E-Mails, Vorlagen und visuelle Fragmente.
feature: Assets, Content
role: User
badge: label="Beta" type="Informative"
autotag-review: '2026-06-18T20:11:57.611Z'
TQID: 'https://experienceleague.adobe.com/Xsl4zqpk4xqXuOS85Z5U08tnbv8GWm3FXdqsegPCBI4'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: e666e996-b2cf-4c45-8fc2-1c625212ababid: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: c8402946-ff35-44c5-ab98-74c1bba0975fid: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 85f61c8fa8eda07dfe8ea1e83f3c261c9159976f
workflow-type: tm+mt
source-wordcount: 495
ht-degree: 3%

---

# Assets

In der [!DNL Adobe Journey Optimizer B2B Prime] sind Assets normalerweise die Bilder, die beim Entwerfen von Inhalten zur Unterstützung von Journey verwendet werden. Sie können diese Bilder in Ihren E-Mails, E-Mail-Vorlagen und visuellen Fragmenten über den Asset-Wähler oder eine einfache Drag-and-Drop-Oberfläche im visuellen Design-Bereich verwenden.

Folgende Dateiformate werden unterstützt: JPG, JPEG, GIF, PNG, EPS, SVG und RGB.


>>
Der Import von Assets aus externen Systemen wie dem Marketo Engage-DAM und der Zugriff auf eine vorausgefüllte Asset-Bibliothek sind noch nicht verfügbar. Künftige Versionen werden voraussichtlich Asset-Importe aus vorhandenen Systemen, Ordnerunterstützung und erweiterte Asset-Management-Funktionen umfassen.

<!-- You can [edit these assets using Adobe Express](./image-edit-adobe-express.md), and move them into folders to organize them for use across your emails, templates, and fragments. -->

Die **Assets**-Bibliothek bietet Zugriff auf das zentrale Repository zum Speichern und Verwalten von Bildern und anderen Kreativ-Assets. Es enthält KI-gestützte Funktionen, die automatisch Metadaten generieren und die Suche in natürlicher Sprache ermöglichen.

Erweitern Sie in der linken Navigationsleiste **[!UICONTROL Content-Management]** und wählen Sie **[!UICONTROL Assets]**.

>[!NOTE]
>
>In dieser Beta-Version können Sie Bilder und Assets aus einer einmaligen Kopie Ihrer Marketo Engage-Asset-Bibliothek direkt auf der E-Mail-Arbeitsfläche auswählen. Sie können auch zusätzliche Bild-Assets aus der _[!UICONTROL Assets]_-Bibliothek oder dem Inhaltsdesign-Bereich hochladen. Diese hochgeladenen Assets sind nur für die Verwendung in der [!DNL Adobe Journey Optimizer B2B Prime] verfügbar.

![Assets-Bibliothek](./assets/dam-asset-library-list-view.png){width="800" zoomable="yes"}

>[!BEGINSHADEBOX]

Wenn Sie das erste Mal auf die Bibliothek _[!UICONTROL Assets]_ zugreifen, lesen Sie die _[!UICONTROL Nutzungsbedingungen für Generative AI]_ und klicken Sie auf **[!UICONTROL Zustimmen und fortfahren]**.

![Assets-Bibliothek](./assets/dam-asset-library-gen-ai-agree.png){width="500"}

>[!ENDSHADEBOX]

Die -Bibliothek unterstützt zwei Layout-Optionen:

* **[!UICONTROL List]** - Klicken Sie auf das Symbol _Listenansicht_ ( ![Listenansichtssymbol](../../assets/do-not-localize/icon-falco-list-view.svg) ), um Assets in einer sortierbaren Tabelle mit Metadatenspalten anzuzeigen.
* **[!UICONTROL Galerie]** - Klicken Sie auf das Symbol _Galerieansicht_ ( ![Galerieansichtssymbol](../../assets/do-not-localize/icon-falco-gallery-view.svg) ), um Assets als visuelles Miniaturraster anzuzeigen.

## Nach Assets suchen {#find-assets}

Verwenden Sie das Feld _[!UICONTROL Suche]_, um Assets zu finden, indem Sie beschreiben, was Sie in natürlicher Sprache benötigen. Suchergebnisse basieren auf KI-generierten Metadaten, sodass Sie nicht auf die Suche nach Dateinamen beschränkt sind.

**Beispiele:**

* `team members`
* `nature`
* `exercise`

![Ausgewähltes Bild aus Suchergebnissen in der Assets-Bibliothek](./assets/dam-asset-library-select-image.png){width="700" zoomable="yes"}

## Asset-Details anzeigen {#view-details}

Wählen Sie ein Asset aus, um seine Detailansicht zu öffnen. In der Detailansicht werden eine KI-generierte Beschreibung, Tags und Keywords sowie zusätzliche Metadatenfelder angezeigt. Diese Informationen werden beim Hochladen des Assets automatisch generiert.

Wählen Sie ein Asset in der Listen- oder Galerieansicht aus, um seine Detailansicht auf der rechten Seite zu öffnen. Wählen Sie die Registerkarte KI-Metadaten aus, um die von der KI generierte Beschreibung, die Tags und die Metadaten anzuzeigen.

![Ausgewähltes Bild aus Suchergebnissen in der Assets-Bibliothek](./assets/dam-asset-library-select-image-metadata.png){width="700" zoomable="yes"}

## Hochladen eines Assets {#upload}

1. Klicken **[!UICONTROL oben]** auf „Hochladen“.

1. Ziehen Sie im Dialogfeld eine Datei per Drag-and-Drop aus Ihrem lokalen System.

   ![Laden Sie ein Bild-Asset hoch](./assets/dam-upload-assets-dialog.png){width="450"}

   Alternativ können Sie auf **[!UICONTROL Datei auf Ihrem Computer auswählen]** klicken, um Ihr lokales Dateisystem zum Suchen und Auswählen der Datei zu verwenden.

1. Klicken Sie **[!UICONTROL Datei hochladen]**, um zu bestätigen und die Datei in das Repository hochzuladen.

Nach Abschluss des Uploads generiert das System automatisch eine Beschreibung, weist Tags und Keywords zu und extrahiert visuelle Attribute wie Betreff und Einstellung. Es ist kein manuelles Tagging erforderlich. Das neue Bild wird mit dem Status _[!UICONTROL VERARBEITUNG“ angezeigt]_ bis dieser Vorgang abgeschlossen ist.

![Neues Bild-Asset im Verarbeitungsstatus](./assets/dam-asset-library-upload-processing.png){width="700" zoomable="yes"}
