---
title: Erstellen von E-Mail-Inhalten mit GenStudio for Performance Marketing
description: Integrieren von GenStudio for Performance Marketing mit Journey Optimizer B2B edition - Exportieren Sie HTML, erstellen Sie KI-gestützte E-Mail-Erlebnisse und importieren Sie Markeninhalte.
feature: Email Authoring, Content, Integrations
topic: Content Supply Chain
level: Intermediate
role: User
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
exl-id: 13f45e8f-9d49-4ec2-90ef-689475c629f1
source-git-commit: 79012352c3ae4e2f3d38b632b1f523d262f74f96
workflow-type: tm+mt
source-wordcount: '794'
ht-degree: 12%

---

# Erstellen von E-Mail-Inhalten mit GenStudio for Performance Marketing {#genstudio-workflow}

>[!CONTEXTUALHELP]
>id="ajo-b2b_genstudio_button"
>title="Verwenden einer mit GenStudio erstellten Vorlage"
>abstract="Nutzen Sie die Integration mit Adobe GenStudio for Performance Marketing, um eine mit KI-Technologie von Adobe erweiterte GenStudio-Vorlage zu importieren."

>[!AVAILABILITY]
>
>Die GenStudio-Integration in [!DNL Adobe Journey Optimizer B2B Edition] ist derzeit nicht für die Verwendung mit den Add-ons **Healthcare Shield** oder **Privacy and Security Shield** verfügbar.
>
>Diese Integration ist nur für den E-Mail-Kanal verfügbar.

Um die Workflow-Effizienz zu verbessern und die Markenkonsistenz zu gewährleisten, können Sie GenStudio for Performance Marketing-Erlebnisse mit der E-Mail-Orchestrierung von Adobe Journey Optimizer B2B edition kombinieren. Dieser erweiterte Workflow ermöglicht es Ihnen, die KI-gestützten Inhaltserstellungs-Tools in GenStudio zu nutzen, um die E-Mail-Kommunikation über Account Journey zu erweitern und zu maximieren.

Ein technischer Marketing-Experte, der Journey Optimizer B2B edition zum Entwickeln und Automatisieren der E-Mail-Kommunikation mit wichtigen Accounts verwendet, kann beispielsweise mit einem Performance-Marketing-Experten zusammenarbeiten, der Inhalte mithilfe von GenStudio erstellt. Mit diesem Workflow können beide zusammenarbeiten, um markeninterne Inhalte aus GenStudio in eine Journey Optimizer B2B edition-basierte Marketing-Automatisierung zu integrieren und ansprechende E-Mails zu versenden, die auf bestimmte Einkaufsgruppen abzielen und den Umsatz steigern.

>[!BEGINSHADEBOX]

## GenStudio-Funktionen zur Inhaltserstellung

[Adobe GenStudio for Performance Marketing](https://business.adobe.com/de/products/genstudio-for-performance-marketing.html){target="_blank"} ist eine generative KI-First-Anwendung, mit der Marketing-Teams wirkungsvolle, personalisierte Anzeigen und E-Mails erstellen können, die den Markenstandards entsprechen und den Unternehmensrichtlinien entsprechen. Dank der KI-Technologie von Adobe bietet diese Anwendung eine umfassende Palette an Tools, die die komplexe Erstellung und Verwaltung von Inhalten vereinfachen, sodass sich Kreative darauf konzentrieren können, innovativ zu sein.

![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Erstellen von markeninternen Marketing-E-Mails](https://experienceleague.adobe.com/de/docs/genstudio-for-performance-marketing-learn/tutorials/creating-experiences/creating-on-brand-emails){target="_blank"}

Weitere Informationen zu den Funktionen von GenStudio for Performance Marketing finden Sie in der [Dokumentation](https://experienceleague.adobe.com/de/docs/genstudio-for-performance-marketing/user-guide/home){target="_blank"}

>[!ENDSHADEBOX]

## Exportieren von HTML aus Journey Optimizer B2B edition

Exportieren Sie zunächst in Journey Optimizer B2B edition HTML aus einer E-Mail, die die Richtlinien Ihrer Marke enthält.

1. Greifen Sie in Journey Optimizer B2B edition im visuellen Design auf den Inhalt Ihrer E-Mail zu.

1. Wählen Sie im Menü _[!UICONTROL Mehr …]_ oben im E-Mail-Design-Bereich **[!UICONTROL HTML exportieren]**.

   ![Klicken Sie auf Mehr und wählen Sie HTML exportieren](./assets/email-export-html.png){width="600"}

   Diese Aktion generiert eine heruntergeladene ZIP-Datei, die die HTML- und Grafikdateien enthält.

## Verwenden der exportierten HTML in GenStudio for Performance Marketing

GenStudio for Performance Marketing erkennt bestimmte Elemente innerhalb der importierten E-Mail-HTML, wenn sie mit einem erkannten Feldnamen identifiziert werden. Fügen Sie in der exportierten HTML Feldnamen mithilfe der Handlebars-Syntax hinzu, für die GenStudio for Performance Marketing einen bestimmten Inhaltstyp generieren muss.

| Feld | Inhaltstyp |
| ----------------- | ------------------------- |
| `{{pre_header}}` | Preheader |
| `{{headline}}` | Überschrift |
| `{{sub_headline}}` | Unterüberschrift |
| `{{body}}` | Haupttext |
| `{{cta}}` | Call to action (Schaltfläche) |
| `{{image}}` | Bild |
| `{{link}}` | Call to action on image |

### Erstellen der Vorlage

Verwenden Sie die HTML-Datei, um eine Vorlage in GenStudio for Performance Marketing zu erstellen.

Weitere Informationen zum Hochladen einer HTML-Vorlage in GenStudio in Adobe GenStudio for Performance Marketing finden Sie unter [Hinzufügen einer Vorlage](https://experienceleague.adobe.com/de/docs/genstudio-for-performance-marketing/user-guide/content/templates/use-templates#add-a-template) in der Dokumentation zu GenStudio for Performance Marketing.

Wenn Sie die exportierte HTML als Vorlage hochladen, überprüft GenStudio for Performance Marketing die HTML-Datei auf erkannte Felder. Verwenden Sie die Vorschau, um Ihre Vorlagenelemente zu überprüfen und sicherzustellen, dass Sie sie ordnungsgemäß mit den erkannten Feldnamen identifiziert haben.

### E-Mail-Erlebnisse generieren

Verwenden Sie in GenStudio for Performance Marketing die Vorlage , um mehrere Varianten des E-Mail-Erlebnisses zu erstellen und zu speichern.

Detaillierte Informationen zum Generieren von E-Mail-Erlebnissen mit Branding finden Sie unter [Erstellen eines E-Mail-Erlebnisses](https://experienceleague.adobe.com/de/docs/genstudio-for-performance-marketing/user-guide/create/create-email-experience) in der Dokumentation zu GenStudio for Performance Marketing.

## Hinzufügen generierter E-Mail-Erlebnisse zu Journey Optimizer B2B edition

>[!NOTE]
>
>Die GenStudio for Performance Marketing-Integration ist nur für die E-Mail-Erstellung und nicht für die Erstellung einer E-Mail-Vorlage verfügbar.

Gehen Sie wie folgt vor, um die GenStudio-E-Mail-Varianten zu verwenden, die aus der exportierten Journey Optimizer B2B edition-E-Mail-HTML-Datei erstellt wurden:

1. Fügen Sie in Journey Optimizer B2B edition [E-Mail hinzufügen](./add-email.md) mithilfe des Knotens _[!UICONTROL Aktion durchführen“]_ Konto-Journey hinzu.

   * Wählen Sie für _[!UICONTROL Ziel]_ Aktion auf“ **[!UICONTROL Personen]**.

   * Wählen Sie für _[!UICONTROL Aktion für Personen]_ die Option **[!UICONTROL E-Mail senden]**.

     ![Aktion durchführen - E-Mail senden](./assets/journey-node-send-email.png){width="700" zoomable="yes"}

   * Wählen Sie für _[!UICONTROL E-Mail]_ die Option **[!UICONTROL Neue E-Mail erstellen]** aus, um die E-Mail nativ in Journey Optimizer B2B edition zu erstellen.

1. Wählen Sie auf der _E-Mail erstellen_ die Option **[!UICONTROL HTML importieren]**.

1. Klicken Sie _[!UICONTROL Dialogfeld „E-]_ importieren“ auf **[!UICONTROL Adobe GenStudio for Performance Marketing]**.

   ![HTML aus GenStudio for Performance Marketing importieren](./assets/email-import-html-genstudio.png){width="500" zoomable="yes"}

1. Durchsuchen Sie die veröffentlichten Erlebnisse.

   Sie können die Erlebnisse nach verschiedenen Kriterien filtern, z. B _„Vorlage_ und _Erstellt von_.

   ![HTML aus GenStudio for Performance Marketing importieren](./assets/email-import-select-gen-studio-experience.png){width="600" zoomable="yes"}

1. Wählen Sie ein Erlebnis aus und klicken Sie auf **[!UICONTROL Verwenden]** um mit der Erstellung Ihres E-Mail-Inhalts zu beginnen.

   >[!NOTE]
   >
   >GenStudio-Erlebnisse, die aus einer Journey Optimizer B2B edition- oder Marketo Engage-Vorlage erstellt wurden, werden direkt in den E-Mail-Design-Bereich importiert. Erlebnisse, die ohne Journey Optimizer B2B edition-Vorlage erstellt wurden, werden in den Kompatibilitätsmodus importiert.

1. Verwenden Sie die [E-Mail-Inhalt und Personalisierungs](./email-authoring.md)Tools, um Ihre E-Mail nach Bedarf zu bearbeiten und zu speichern.

   ![HTML aus GenStudio for Performance Marketing importieren](./assets/email-imported-experience.png){width="800" zoomable="yes"}
