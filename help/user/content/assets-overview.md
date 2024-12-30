---
title: Assets
description: Erfahren Sie mehr über Asset-Management in Journey Optimizer B2B edition.
feature: Assets, Content
exl-id: f3848e65-3196-4d1f-90cf-7aa6ceeafabb
source-git-commit: 23fb478712f3c6df59e94432bdf16883e6acf70b
workflow-type: tm+mt
source-wordcount: '1034'
ht-degree: 2%

---

# Assets

In Adobe Journey Optimizer B2B edition sind Assets normalerweise die Bilder, die zum Erstellen von Journey-Inhalten verwendet werden. Sie können diese Bilder in E-Mails, E-Mail-Vorlagen und Fragmenten verwenden, die in Journey Optimizer B2B edition über einen Asset-Selektor oder eine einfache Drag-and-Drop-Oberfläche im visuellen Inhaltseditor erstellt wurden.

Adobe Journey Optimizer B2B edition bietet Marketing-Experten Zugriff auf zwei Arten von Asset-Bibliotheken: Adobe Marketo Engage Design Studio und Adobe Experience Manager Assets as a Cloud Service. Sie können nur Adobe Marketo Engage Design Studio verwenden oder beide Bibliotheken gleichzeitig konfigurieren (basierend auf der von Ihnen verwendeten AEM Assets-Lizenz).

## Asset-Management

Wenn Sie über ein Marketo Engage-Konto und Adobe Experience Manager as a -Cloud Service verfügen, haben Sie Zugriff auf die Repositorys für Marketo Engage DAM und Adobe Experience Manager Assets as a Cloud Service, wenn Ihr Benutzerkonto über die erforderlichen Berechtigungen verfügt. Diese Repositorys sind getrennt und nicht synchronisiert. Sie können Bilder aus beiden Quellen verwenden, es kann jedoch jeweils nur eines im Inhaltseditor aktiviert werden. Ein Administrator kann den Wechsel vom Marketo Engage-DAM zu Adobe Experience Manager Assets as a Cloud Service vornehmen. Das Element _[!UICONTROL Assets]_ im linken Navigationsbereich zeigt das aktuell festgelegte Repository an.

### Adobe Marketo Engage-Assets

Das Adobe Marketo Engage Design Studio Assets-Repository wird standardmäßig mit jedem Journey Optimizer B2B edition-Abonnement bereitgestellt. Das bedeutet, dass Sie Zugriff auf alle Bild-Assets haben, die unter Adobe Marketo Engage > [!UICONTROL Design Studio] > [!UICONTROL Bilder und Dateien] gespeichert sind. Sie können dieses Repository als lokale Asset-Bibliothek verwenden, einschließlich der Funktionen zum Hochladen und Herunterladen von Assets. Sie können diese Assets auch in Ihrem Journey-Inhalt verwenden.

Es gibt integrierte Leitplanken, die Bearbeitungen am Marketo Engage-Asset von Journey Optimizer B2B edition sowie Löschen- und Verschiebungsvorgänge verhindern. Diese Schutzmaßnahmen stellen sicher, dass die Quell-Assets (Marketo Engage Design Studio) beibehalten werden und gleichzeitig das nahtlose Lesen und Wiederverwenden in Journey Optimizer B2B edition ermöglicht wird.

Unterstützte Dateiformate: JPG, JPEG, GIF, PNG, EPS, SVG, RGB

### Adobe Experience Manager Assets as a Cloud Service

Zusammenführen von Marketing- und Kreativ-Workflows mithilfe von Adobe Experience Manager Assets. Sie ist nativ in Adobe Journey Optimizer B2B edition integriert, sodass Sie einfach auf Assets as a Cloud Service zugreifen können, um digitale Assets zu entdecken und zu verwenden. Es bietet Zugriff auf Ihr Assets-Repository für Assets, die Sie zum Ausfüllen Ihrer Nachrichten verwenden können.

Adobe Experience Manager Assets kann eine Verbindung zu Adobe Experience Manager Assets as a Cloud Service herstellen, um zentralisierte Asset-Arbeitsbereiche zu erstellen, die Ihr Kreativsystem erweitern und digitale Assets für die Bereitstellung von Erlebnissen zusammenführen. Adobe Experience Manager Assets as a Cloud Service bietet eine benutzerfreundliche Cloud-Lösung für effizientes Digital Asset Management und Dynamic Media-Betrieb. Es integriert nahtlos fortschrittliche Funktionen, darunter künstliche Intelligenz und maschinelles Lernen.

Weitere Informationen finden Sie in der Dokumentation zu [Adobe Experience Manager as a Cloud Service](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/assets/overview).

Über das Element **[!UICONTROL Adobe Experience Manager Assets]** im linken Navigationsbereich können Sie direkt in Adobe Journey Optimizer B2B edition auf Assets zugreifen. Sie können beim Entwerfen eines E-Mail-Inhalts auch auf Assets und Ordner zugreifen.

>[!NOTE]
>
>AEM Assets as a Cloud Service und Dynamic Media-Lizenzen sind Voraussetzung für diese Integration.<br/>
>Abhängig von Ihrem Vertrag und Ihrer Konfiguration können Sie über den Assets-Abschnitt im linken Menü direkt von Adobe Journey Optimizer B2B edition auf Adobe Experience Manager Assets as a Cloud Service zugreifen. Sie können beim Entwerfen eines E-Mail-Inhalts auch auf Assets und Ordner zugreifen.

Derzeit können Sie nur Bilder von Adobe Experience Manager Assets in Adobe Journey Optimizer B2B edition verwenden.

## Verwenden von Assets für die Inhaltserstellung

Verwenden Sie Assets beim Erstellen von E-Mails, E-Mail-Vorlagen und visuellen Fragmenten. Die Benutzeroberfläche des visuellen Inhaltseditors bietet Zugriff auf die Bilder in Ihren verbundenen Asset-Repositorys.

### Asset-Quelle auswählen

Wenn Sie über ein Abonnement für Experience Manager Assets as a Cloud Service und das standardmäßige Adobe Marketo Engage Design Studio verfügen, können Sie Bild-Assets aus beiden Quellen auswählen. Wählen Sie dazu bei der Erstellung einer neuen E-Mail, E-Mail-Vorlage oder eines visuellen Fragments die Bildquelle aus. Sie können auch die Bildquelle auswählen, wenn Sie den Inhalt bearbeiten. Die Auswahl gilt nur für das Bearbeitungserlebnis, und Sie können die Bildquelle ändern, um bei Bedarf auf Assets aus einer anderen Bibliothek zuzugreifen.

_**Erstellen einer Inhaltsressource**_ - Zum Auswählen einer Bildquelle beim Erstellen einer E-Mail, einer E-Mail-Vorlage oder eines Fragments legen Sie die **[!UICONTROL Bildquelle]** im Dialogfeld fest.

_**Bearbeiten einer Inhaltsressource**_ **[!UICONTROL - Verwenden Sie die Einstellung „Bildquelle“ im Bedienfeld auf der rechten]**, um eine Bild-Asset-Quelle in der visuellen Vorschau auszuwählen.

### Hinzufügen von Assets zu Inhalten

Sie können je nach ausgewählter Bild-Asset-Quelle ein Bild-Asset hinzufügen, während Sie Ihre Inhalte erstellen.

>[!BEGINTABS]

>[!TAB Hinzufügen von Marketo Engage-Bild-Assets]

Sie können Marketo Engage-Assets mit einer der folgenden Methoden hinzufügen:

* Fügen Sie ein Strukturelement hinzu und ziehen Sie dann Assets aus dem linken Navigationsbereich in die visuelle Arbeitsfläche.
* Fügen Sie ein Strukturelement hinzu und ziehen Sie dann den Inhaltstyp _Bild_ in die Struktur. In den Eigenschafteneinstellungen auf der rechten Seite gibt es zwei Möglichkeiten, das Bild anzugeben:
   * Klicken Sie auf **[!UICONTROL Durchsuchen]**, um den Asset-Wähler zu öffnen, in dem Sie ein Bild aus der Asset-Bibliothek von Adobe Marketo Engage Design Studio auswählen können.
   * Klicken Sie **[!UICONTROL Medien importieren]**, um ein Asset aus Ihrem lokalen System zu importieren. Das importierte Asset wird im Assets-Stammordner Ihrer Adobe Marketo Engage Design Studio-Bibliothek gespeichert.

Weitere Informationen [ Sie unter „Verwenden von ](./marketo-engage-design-studio.md#use-assets-in-your-content) in Ihren Inhalten“.

Um das Bild zu ändern, können Sie die Quell-URL für das Bild in den Eigenschaften auf der rechten Seite aktualisieren.

>[!TAB Hinzufügen von Experience Manager Assets-Bildern]

1. Ziehen Sie beim Verfassen Ihres E-Mail-Inhalts in Email Designer ein Bildelement auf die Arbeitsfläche.

   Die Eigenschaften auf der rechten Seite spiegeln die Auswahl der Bildelemente wider.

1. Klicken Sie auf **[!UICONTROL Asset auswählen]**, um den Experience Manager-Asset-Wähler zu öffnen.

   Hier können Sie Ihr gewünschtes Inhalts-Asset suchen, filtern und darauf zugreifen, um es zu Ihrem Marketing-Asset hinzuzufügen. Auf dieser Seite finden Sie weitere Informationen zur Verwendung des -Selektors.

   >[!NOTE]
   >
   >Wenn mehr als ein Repository konfiguriert ist, können Sie den Repository-Umschalter auf dem Asset-Wähler verwenden

1. Wählen Sie das gewünschte Asset aus, das in die E-Mail eingefügt werden soll.

>[!ENDTABS]
