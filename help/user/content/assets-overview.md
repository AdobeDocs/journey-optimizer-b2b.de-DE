---
title: Assets
description: Erfahren Sie mehr über die Asset-Verwaltung in Journey Optimizer B2B Edition.
feature: Assets, Content
exl-id: f3848e65-3196-4d1f-90cf-7aa6ceeafabb
source-git-commit: dcd8ab2820d60654e8970944054142fc296ed54f
workflow-type: tm+mt
source-wordcount: '963'
ht-degree: 0%

---

# Assets

Assets sind in der Regel die Bilder, die zum Erstellen Ihres Journey-Inhalts in Adobe Journey Optimizer B2B Edition verwendet werden. Sie können diese Bilder in E-Mails, E-Mail-Vorlagen und Fragmenten verwenden, die in Journey Optimizer B2B Edition erstellt wurden. Verwenden Sie dazu einen Asset-Selektor oder eine einfache Drag &amp; Drop-Benutzeroberfläche im Visual Content Editor.

Adobe Journey Optimizer B2B Edition bietet Marketing-Experten Zugriff auf zwei Arten von Asset-Bibliotheken: Adobe Marketo Engage Design Studio und Adobe Experience Manager Assets as a Cloud Service. Sie dürfen nur Adobe Marketo Engage Design Studio oder beide gleichzeitig konfigurierten Bibliotheken verwenden (basierend auf Ihrer AEM Assets-Lizenz).

## Asset-Management

Wenn Sie über ein Marketo Engage-Konto und Adobe Experience Manager as a Cloud Service verfügen, haben Sie Zugriff auf die Repositorys für Marketo Engage DAM und Adobe Experience Manager Assets as a Cloud Service, wenn Ihr Benutzerkonto über die erforderlichen Berechtigungen verfügt. Diese Repositorys sind separat und nicht synchronisiert. Sie können Bilder aus beiden Quellen verwenden, jedoch kann jeweils nur eines im Inhaltseditor aktiviert werden. Ein Administrator kann den Wechsel vom Marketo Engage-DAM zu Adobe Experience Manager Assets as a Cloud Service vornehmen. Das Element _[!UICONTROL Assets]_ im linken Navigationsbereich zeigt das derzeit eingerichtete Repository an.

### Adobe Marketo Engage Design Studio

Das Asset-Repository von Adobe Marketo Engage Design Studio wird standardmäßig bei jedem Journey Optimizer B2B Edition-Abonnement bereitgestellt. Dies bedeutet, dass Sie Zugriff auf alle Bild-Assets haben, die in Adobe Marketo Engage > Design Studio > Bilder und Dateien gespeichert sind. Sie können dieses Repository als Ihre lokale Asset-Bibliothek verwenden, einschließlich der Funktionen zum Hochladen, Löschen und Herunterladen von Assets. Sie können diese Assets auch in Ihrem Journey-Inhalt verwenden.

Unterstützte Dateiformate: JPG, JPEG, GIF, PNG, EPS, SVG, RGB

### Adobe Experience Manager Assets as a Cloud Service

Marketing- und Kreativ-Workflows mit Adobe Experience Manager Assets zusammenführen Es ist nativ in Adobe Journey Optimizer B2B Edition integriert, sodass Sie einfach auf Assets as a Cloud Service zugreifen können, um digitale Assets zu finden und zu verwenden. Es bietet Zugriff auf Ihr Assets-Repository für Assets, mit denen Sie Ihre Nachrichten ausfüllen können.

Adobe Experience Manager Assets kann für zentrale Asset-Arbeitsbereiche, die Ihr Kreativsystem erweitern und digitale Assets für die Bereitstellung von Erlebnissen vereinheitlichen, eine Verbindung zu Adobe Experience Manager Assets as a Cloud Service herstellen. Adobe Experience Manager Assets as a Cloud Service bietet eine benutzerfreundliche Cloud-Lösung für effiziente Digital Asset Management- und Dynamic Media-Vorgänge. Es umfasst nahtlos erweiterte Funktionen, darunter künstliche Intelligenz und maschinelles Lernen.

Weitere Informationen finden Sie in der Dokumentation zu [Adobe Experience Manager as a Cloud Service](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/assets/overview) .

Der Zugriff auf Adobe Experience Manager Assets erfolgt direkt in Adobe Journey Optimizer B2B Edition über das Element **[!UICONTROL Assets]** im linken Navigationsbereich. Sie können beim Entwerfen eines E-Mail-Inhalts auch auf Assets und Ordner zugreifen.

>[!NOTE]
>
>Für diese Integration sind AEM Assets als Cloud Service- und Dynamic Media-Lizenzen erforderlich.<br/>
>Je nach Vertrag und Konfiguration können Sie über das linke Menü Assets direkt von Adobe Journey Optimizer B2B Edition aus auf Adobe Experience Manager Assets as a Cloud Service zugreifen. Sie können beim Entwerfen eines E-Mail-Inhalts auch auf Assets und Ordner zugreifen.

Derzeit können Sie nur Bilder aus Adobe Experience Manager Assets in Adobe Journey Optimizer B2B Edition verwenden.

## Verwenden von Assets für die Inhaltserstellung

Verwenden Sie Assets beim Erstellen von E-Mails, E-Mail-Vorlagen und visuellen Fragmenten. Die Benutzeroberfläche des Visual Content Editors bietet Zugriff auf die Bilder in Ihren verbundenen Asset-Repositorys.

### Auswählen einer Asset-Quelle

Wenn Sie über ein Abonnement von Experience Manager Assets as a Cloud Service sowie die standardmäßige Adobe Marketo Engage Design Studio verfügen, können Sie Bild-Assets aus beiden Quellen auswählen. Dazu müssen Sie die Bildquelle zum Zeitpunkt der Erstellung für eine neue E-Mail, eine E-Mail-Vorlage oder ein neues visuelles Fragment auswählen. Sie können auch die Bildquelle auswählen, wenn Sie den Inhalt bearbeiten. Die Auswahl gilt nur für das Bearbeitungserlebnis. Sie können die Bildquelle ändern, um bei Bedarf auf Assets aus einer anderen Bibliothek zuzugreifen.

E-Mails erstellen

Bearbeiten einer E-Mail: Um eine Bild-Asset-Quelle im Visual Editor auszuwählen, verwenden Sie die Auswahl **[!UICONTROL Bildquelle auswählen]** oben auf der Arbeitsfläche.

### Hinzufügen von Assets zu Inhalten

Sie können je nach ausgewählter Bild-Asset-Quelle beim Erstellen Ihres Inhalts ein Bild-Asset hinzufügen.

>[!BEGINTABS]

>[!TAB Marketo Engage Design Studio-Bild-Assets hinzufügen]

Sie können Marketo Engage Design Studio-Assets mit einer der folgenden Methoden hinzufügen:

* Fügen Sie ein Strukturelement hinzu und ziehen Sie dann Assets aus der linken Navigation in die visuelle Arbeitsfläche.
* Fügen Sie ein Strukturelement hinzu und ziehen Sie dann den Inhaltstyp _image_ in die Struktur. In den Eigenschaften auf der rechten Seite gibt es zwei Möglichkeiten, das Bild anzugeben:
   * Klicken Sie auf **[!UICONTROL Durchsuchen]** , um die Asset-Auswahl zu öffnen, in der Sie ein Bild aus der Adobe Marketo Engage Design Studio-Asset-Bibliothek auswählen können.
   * Klicken Sie auf **[!UICONTROL Medien importieren]** , um ein Asset aus Ihrem lokalen System zu importieren. Das importierte Asset wird im Stammordner von Assets Ihrer Adobe Marketo Engage Design Studio-Bibliothek gespeichert.

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
