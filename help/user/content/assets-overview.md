---
title: Assets
description: Erfahren Sie mehr über die Asset-Verwaltung in Journey Optimizer B2B edition.
feature: Assets, Content
exl-id: f3848e65-3196-4d1f-90cf-7aa6ceeafabb
source-git-commit: 23fb478712f3c6df59e94432bdf16883e6acf70b
workflow-type: tm+mt
source-wordcount: '1034'
ht-degree: 2%

---

# Assets

In Adobe Journey Optimizer B2B edition sind Assets normalerweise die Bilder, die zum Erstellen Ihres Journey-Inhalts verwendet werden. Sie können diese Bilder in E-Mails, E-Mail-Vorlagen und Fragmenten verwenden, die in Journey Optimizer B2B edition erstellt wurden. Verwenden Sie dazu einen Asset-Selektor oder eine einfache Drag &amp; Drop-Benutzeroberfläche im Visual Content Editor.

Adobe Journey Optimizer B2B edition bietet Marketing-Experten Zugriff auf zwei Arten von Asset-Bibliotheken: Adobe Marketo Engage Design Studio und Adobe Experience Manager Assets as a Cloud Service. Sie dürfen nur Adobe Marketo Engage Design Studio oder beide gleichzeitig konfigurierten Bibliotheken verwenden (basierend auf Ihrer AEM Assets-Lizenz).

## Asset-Management

Wenn Sie über ein Marketo Engage-Konto und Adobe Experience Manager as a Cloud Service verfügen, haben Sie Zugriff auf die Repositorys für Marketo Engage DAM und Adobe Experience Manager Assets as a Cloud Service, wenn Ihr Benutzerkonto über die erforderlichen Berechtigungen verfügt. Diese Repositorys sind getrennt und nicht synchronisiert. Sie können Bilder aus beiden Quellen verwenden, jedoch kann jeweils nur eines im Inhaltseditor aktiviert werden. Ein Administrator kann den Wechsel vom Marketo Engage-DAM zu Adobe Experience Manager Assets as a Cloud Service vornehmen. Das Element _[!UICONTROL Assets]_ im linken Navigationsbereich zeigt das derzeit eingerichtete Repository an.

### Adobe Marketo Engage-Assets

Das Asset-Repository von Adobe Marketo Engage Design Studio wird standardmäßig bei jedem Journey Optimizer B2B edition-Abonnement bereitgestellt. Dies bedeutet, dass Sie Zugriff auf alle Bild-Assets haben, die in Adobe Marketo Engage > [!UICONTROL Design Studio] > [!UICONTROL Bilder und Dateien] gespeichert sind. Sie können dieses Repository als Ihre lokale Asset-Bibliothek verwenden, einschließlich der Funktionen zum Hochladen und Herunterladen von Assets. Sie können diese Assets auch in Ihrem Journey-Inhalt verwenden.

Es gibt integrierte Limits, die Bearbeitungen von Marketo Engage-Assets aus Journey Optimizer B2B edition sowie Löschvorgänge und Verschiebungen verhindern. Diese Schutzmaßnahmen stellen sicher, dass die Quell-Assets (Marketo Engage Design Studio) beibehalten werden, während eine nahtlose Lese- und Wiederverwendung in Journey Optimizer B2B edition ermöglicht wird.

Unterstützte Dateiformate: JPG, JPEG, GIF, PNG, EPS, SVG, RGB

### Adobe Experience Manager Assets as a Cloud Service

Marketing- und Kreativ-Workflows mit Adobe Experience Manager Assets zusammenführen Es ist nativ in Adobe Journey Optimizer B2B edition integriert, sodass Sie mühelos auf Assets as a Cloud Service zugreifen können, um digitale Assets zu finden und zu verwenden. Es bietet Zugriff auf Ihr Assets-Repository für Assets, mit denen Sie Ihre Nachrichten ausfüllen können.

Adobe Experience Manager Assets kann für zentrale Asset-Arbeitsbereiche, die Ihr Kreativsystem erweitern und digitale Assets für die Bereitstellung von Erlebnissen vereinheitlichen, eine Verbindung zu Adobe Experience Manager Assets as a Cloud Service herstellen. Adobe Experience Manager Assets as a Cloud Service bietet eine benutzerfreundliche Cloud-Lösung für effiziente Digital Asset Management- und Dynamic Media-Vorgänge. Es integriert nahtlos fortschrittliche Funktionen, darunter künstliche Intelligenz und maschinelles Lernen.

Weitere Informationen finden Sie in der Dokumentation zu [Adobe Experience Manager as a Cloud Service](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/assets/overview) .

Der Zugriff auf Adobe Experience Manager Assets erfolgt direkt in Adobe Journey Optimizer B2B edition über das Element **[!UICONTROL Assets]** im linken Navigationsbereich. Sie können beim Entwerfen eines E-Mail-Inhalts auch auf Assets und Ordner zugreifen.

>[!NOTE]
>
>Für diese Integration sind AEM Assets als Cloud Service- und Dynamic Media-Lizenzen erforderlich.<br/>
>Abhängig von Ihrem Vertrag und Ihrer Konfiguration können Sie über das linke Menü &quot;Assets&quot;direkt von Adobe Journey Optimizer B2B edition aus auf Adobe Experience Manager Assets as a Cloud Service zugreifen. Sie können beim Entwerfen eines E-Mail-Inhalts auch auf Assets und Ordner zugreifen.

Derzeit können Sie nur Bilder aus Adobe Experience Manager Assets in Adobe Journey Optimizer B2B edition verwenden.

## Verwenden von Assets für die Inhaltserstellung

Verwenden Sie Assets beim Erstellen von E-Mails, E-Mail-Vorlagen und visuellen Fragmenten. Die Benutzeroberfläche des Visual Content Editors bietet Zugriff auf die Bilder in Ihren verbundenen Asset-Repositorys.

### Auswählen einer Asset-Quelle

Wenn Sie über ein Abonnement für Experience Manager Assets as a Cloud Service sowie die standardmäßige Adobe Marketo Engage Design Studio verfügen, können Sie Bild-Assets aus beiden Quellen auswählen. Dazu müssen Sie die Bildquelle zum Zeitpunkt der Erstellung für eine neue E-Mail, eine E-Mail-Vorlage oder ein neues visuelles Fragment auswählen. Sie können auch die Bildquelle auswählen, wenn Sie den Inhalt bearbeiten. Die Auswahl gilt nur für das Bearbeitungserlebnis. Sie können die Bildquelle ändern, um bei Bedarf auf Assets aus einer anderen Bibliothek zuzugreifen.

_**Erstellen einer Inhaltsressource**_ - Wenn Sie beim Erstellen einer E-Mail, einer E-Mail-Vorlage oder eines Fragments eine Bildquelle auswählen möchten, legen Sie die **[!UICONTROL Bildquelle]** im Dialogfeld fest.

_**Bearbeiten einer Inhaltsressource**_ - Um eine Bild-Asset-Quelle in der visuellen Vorschau auszuwählen, verwenden Sie die Einstellung **[!UICONTROL Bildquelle]** im Bereich auf der rechten Seite.

### Hinzufügen von Assets zu Inhalten

Sie können je nach ausgewählter Bild-Asset-Quelle beim Erstellen Ihres Inhalts ein Bild-Asset hinzufügen.

>[!BEGINTABS]

>[!TAB Hinzufügen von Marketo Engage-Bild-Assets]

Sie können Marketo Engage-Assets mit einer der folgenden Methoden hinzufügen:

* Fügen Sie ein Strukturelement hinzu und ziehen Sie dann Assets aus der linken Navigation in die visuelle Arbeitsfläche.
* Fügen Sie ein Strukturelement hinzu und ziehen Sie dann den Inhaltstyp _image_ in die Struktur. In den Eigenschaften auf der rechten Seite gibt es zwei Möglichkeiten, das Bild anzugeben:
   * Klicken Sie auf **[!UICONTROL Durchsuchen]** , um die Asset-Auswahl zu öffnen, in der Sie ein Bild aus der Adobe Marketo Engage Design Studio-Asset-Bibliothek auswählen können.
   * Klicken Sie auf **[!UICONTROL Medien importieren]** , um ein Asset aus Ihrem lokalen System zu importieren. Das importierte Asset wird im Stammordner von Assets Ihrer Adobe Marketo Engage Design Studio-Bibliothek gespeichert.

Weitere Informationen finden Sie unter [Verwenden von Assets in Ihrem Inhalt](./marketo-engage-design-studio.md#use-assets-in-your-content) .

Um das Bild zu ändern, können Sie die Quell-URL für das Bild in den Eigenschaften auf der rechten Seite aktualisieren.

>[!TAB Hinzufügen von Experience Manager Assets-Bildern]

1. Ziehen Sie beim Bearbeiten Ihres E-Mail-Inhalts im E-Mail-Designer ein Bildelement auf die Arbeitsfläche.

   Die Eigenschaften auf der rechten Seite spiegeln die Auswahl des Bildelements wider.

1. Klicken Sie auf &quot;**[!UICONTROL Select an asset]**&quot;, um die Experience Manager-Asset-Auswahl zu öffnen.

   Hier können Sie Ihr gewünschtes Inhalts-Asset durchsuchen, filtern und aufrufen, um es zu Ihrem Marketing-Asset hinzuzufügen. Weitere Informationen zur Verwendung des Selektors finden Sie auf dieser Seite .

   >[!NOTE]
   >
   >Wenn mehr als ein Repository konfiguriert ist, können Sie den Repository-Umschalter in der Asset-Auswahl verwenden

1. Wählen Sie das gewünschte Asset aus, das in die E-Mail eingefügt werden soll.

>[!ENDTABS]
