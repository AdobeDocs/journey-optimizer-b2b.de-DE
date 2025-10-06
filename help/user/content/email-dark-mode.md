---
title: Dunkler Modus für E-Mail-Inhalte
description: Erfahren Sie mehr über das Design von E-Mails im Dunkelmodus in Journey Optimizer B2B edition. Vorschau des Renderings, Anpassen von Einstellungen, Sicherstellung der Barrierefreiheit und Testen über E-Mail-Clients hinweg.
feature: Email Authoring
topic: Content Management
hidefromtoc: true
role: User
level: Beginner, Intermediate
keywords: Dunkler Modus, E-Mail, Farbe, Design
source-git-commit: 9cb77da73778c313392af1c42632d6b9e7e92f3b
workflow-type: tm+mt
source-wordcount: '1600'
ht-degree: 19%

---

# Dunkler Modus für E-Mail-Inhalte {#dark-mode}

>[!CONTEXTUALHELP]
>id="ajo-b2b_dark_mode"
>title="Wechseln zum dunklen Modus"
>abstract="Wechseln Sie in den dunklen Modus, um eine Vorschau des Renderings anzuzeigen und bestimmte benutzerdefinierte Einstellungen vorzunehmen. <br>Das endgültige Rendering hängt vom E-Mail-Client der Empfängerinnen und Empfänger ab. Beachten Sie, dass nicht alle E-Mail-Clients den benutzerdefinierten dunklen Modus unterstützen."

>[!CONTEXTUALHELP]
>id="ajo-b2b_dark_mode_preview"
>title="Wechseln zum dunklen Modus"
>abstract="Wechseln Sie zum dunklen Modus, um eine Vorschau des Renderings auf unterstützenden E-Mail-Clients anzuzeigen. <br>Das endgültige Rendering hängt vom E-Mail-Client der Empfängerinnen und Empfänger ab. Beachten Sie, dass nicht alle E-Mail-Clients den dunklen Modus unterstützen."

_Dunkler Modus_ ermöglicht es einem unterstützenden E-Mail-Client oder einer unterstützenden App, E-Mails mit dunkleren Hintergründen und helleren Farben für Text, Schaltflächen und andere visuelle Elemente anzuzeigen. Diese Art von Display reduziert die Belastung der Augen, spart Akkulaufzeit und verbessert die Lesbarkeit in schwach beleuchteten Umgebungen für ein angenehmeres Betrachtungserlebnis. Aufgrund des wachsenden Trends bei den wichtigsten Betriebssystemen und Apps ist es jetzt eine wichtige Überlegung im modernen E-Mail-Design, sicherzustellen, dass Inhalte für alle Benutzer lesbar und visuell ansprechend bleiben.

![Konzeptdiagramm für Hell- und Dunkelmodus, in dem das Rendern von Inhalten sowohl in hellen als auch in dunklen Designs angezeigt wird](../assets/do-not-localize/light-dark-mode.svg){width="50%"}

Wenn Sie [E-Mail](./email-authoring.md)Inhalt erstellen) im visuellen [!DNL Journey Optimizer B2B Edition]-Design-Bereich wechseln Sie zur Ansicht _&#x200B;**[!UICONTROL Dunkelmodus]**&#x200B;_. In dieser Ansicht können Sie auch spezifische benutzerdefinierte Einstellungen für unterstützende E-Mail-Clients definieren, wenn deren Dunkelmodus aktiviert ist.

## Überlegungen zum E-Mail-Client

Die Art und Weise, wie verschiedene E-Mail-Clients und Apps den Dunkelmodus anwenden, ist sehr unterschiedlich. Daher sollten Sie die Erwartungen an das Rendering im Dunkelmodus mit Vorsicht überlegen. Bevor Sie den Dunkelmodus im E-Mail-Design-Bereich verwenden, sollten Sie die folgenden Anwendungsfälle für E-Mail-Clients berücksichtigen:
<!--
* Check out the list of [email clients supporting dark mode](https://www.caniemail.com/search/?s=dark){target="_blank"}

* Learn more on Dark mode in this [Litmus blog post](https://www.litmus.com/blog/the-ultimate-guide-to-dark-mode-for-email-marketers){target="_blank"}
-->

+++Clients, die den Dunkelmodus nicht unterstützen

Einige E-Mail-Clients unterstützen diese Funktion überhaupt nicht, z. B.:

* [!DNL Yahoo! Mail]
* [!DNL AOL]

Wenn Sie benutzerdefinierte Einstellungen für den Dunkelmodus im E-Mail-Design definieren, können diese E-Mail-Clients keinen Dark-Mode-Rendering anzeigen. <!--Regardless of whether the interface is in light or dark mode, your email will render the same.-->

+++

+++Clients, die ihre eigene Dunkelmodus-{#default-support} anwenden

Einige E-Mail-Clients wenden ihren eigenen standardmäßigen Dunkelmodus systematisch auf alle empfangenen E-Mails an. Sie passen Farben, Hintergründe, Bilder und andere Elemente automatisch an die Einstellungen für den Dunkelmodus an. Externe Einstellungen sind nicht möglich. Zu diesen Clients gehören:

* Gmail (Desktop-Webmail, iOS, Android™, mobile Webmail)
* Outlook Windows
* Outlook Windows Mail

<!--It is important to note that less than 25% of email clients offer customization options for dark mode. Clients such as Gmail implement their own dark mode rendering, which is not subject to external modification.-->
In diesem Fall überschreiben die Client-Einstellungen für den Dunkelmodus die benutzerdefinierten Einstellungen für den Dunkelmodus, die Sie in [!DNL Journey Optimizer B2B Edition] definieren

+++

+++Clients, die den benutzerdefinierten Dunkelmodus unterstützen

Viele der beliebtesten E-Mail-Clients bieten die Option, den benutzerdefinierten Dunkelmodus mit der `@media (prefers-color-scheme: dark)`-Abfrage zu rendern, was die Methode ist, die von den [!DNL Journey Optimizer B2B Edition] E-Mail-Stilen verwendet wird. Diese Kundenliste umfasst:

* Apple Mail für macOS
* Apple Mail für iOS
* Outlook macOS
* Outlook.com
* Outlook iOS
* Outlook Android™

In diesem Fall werden die spezifischen Einstellungen gerendert, die Sie im [!DNL Journey Optimizer B2B Edition] definieren. Je nach E-Mail-Client können jedoch einige Einschränkungen gelten. Einige Clients (z. B. Apple Mail 16 (macOS 13)) generieren beispielsweise keinen Dunkelmodus, wenn im E-Mail-Inhalt Bilder vorhanden sind.

Um optimale Ergebnisse zu erzielen, testen Sie Ihren Inhalt mit den E-Mail-Clients, auf die Sie abzielen. Um eine Simulation anzuzeigen, die dem Endergebnis für jeden Client so nahe kommt wie möglich, verwenden Sie die Integration [Litmus Email Test Rendering](./email-test-rendering.md) im E-Mail-Design-Bereich.

+++

## Design für den Dunkelmodus

Wenn Sie Ihre E-Mail-Inhalte für den Dunkelmodus in [!DNL Journey Optimizer B2B Edition] gestalten, bietet der visuelle Design-Bereich zwei Arten von Tools:

* Verwenden Sie die [Vorschaufunktion](#preview-default-dark-mode), um das standardmäßige Dark-Mode-Rendering für die meisten unterstützenden E-Mail-Clients zu überprüfen.

* Wenn Sie die Standardeinstellungen unterstützender E-Mail-Clients überschreiben möchten, definieren und wenden Sie benutzerdefinierte Einstellungen für den Dunkelmodus auf Ihren E-Mail-Inhalt an. [Weitere Informationen](#define-custom-dark-mode)

### Vorschau des standardmäßigen dunklen Modus {#preview-dark-mode}

<!-- Should work with templates and themes, NOT for LP and fragments - but TBC with eng. 
>[!NOTE]
>
>Currently you may not be able to switch to dark mode if you select an [email template](use-email-templates.md) or if you apply a [theme](apply-email-themes.md).-->

1. Öffnen Sie den E-Mail-Inhalt im E-Mail-Design-Bereich.

   Oben rechts auf der Arbeitsfläche gibt es einen Hell-Dunkel-Selektor, der die Inhaltsanzeige zwischen Hell- (Standard) und Dunkelmodus umschaltet.

   ![E-Mail-Design-Arbeitsfläche mit der Auswahl des Lichtmodus in der oberen rechten Ecke](./assets/email-color-mode-light-selector.png){width="700" zoomable="yes"}

1. Ändern Sie den Selektor in _Dunkelmodus_ ( ![Dunkelmodus-Symbol](../assets/do-not-localize/icon-content-dark-mode.svg) ).

   Auf der Arbeitsfläche wird der Inhalt mit der standardmäßigen Vorschau des dunklen Modus angezeigt.x

   Standardmäßig wendet die Dunkelmodusvorschau das `full color invert` Farbschema auf alle Elemente außer Bildern und Symbolen an. Dieses Farbschema erkennt Bereiche mit hellen und dunklen Elementen und invertiert sie. Helle Hintergründe werden dunkel und dunkler Text wird hell, oder dunkle Hintergründe werden hell und heller Text wird dunkel.

   ![E-Mail-Design-Arbeitsfläche mit der Auswahl für den Dunkelmodus und den im Dunkelmodus angezeigten E-Mail-Inhalten](./assets/email-color-mode-dark-selector.png){width="700" zoomable="yes"}

>[!CAUTION]
>
>Das endgültige Rendering kann je nach E-Mail-Client des Empfängers variieren. Um für jeden E-Mail-Client eine Simulation anzuzeigen, die dem Endergebnis möglichst nahe kommt, verwenden Sie die Integration [Litmus E-Mail-Rendering testen](./email-test-rendering.md).

### Definieren benutzerdefinierter Einstellungen für den Dunkelmodus {#custom-dark-mode}

>[!CONTEXTUALHELP]
>id="ajo-b2b_dark_mode_image"
>title="Verwenden eines bestimmten Bildes für den dunklen Modus"
>abstract="Sie können ein anderes Bild auswählen, das angezeigt werden soll, wenn der Dunkelmodus aktiviert ist. <br>Das Hinzufügen eines bestimmten Bildes für den Dunkelmodus garantiert nicht, dass es in allen E-Mail-Clients korrekt gerendert wird. Beachten Sie, dass nicht alle E-Mail-Clients den benutzerdefinierten dunklen Modus unterstützen."

Nach dem Wechsel in den dunklen Modus können Sie bestimmte Stilelemente Ihres Inhalts bearbeiten, die nur angezeigt werden, wenn der dunkle Modus im E-Mail-Client des Empfängers aktiviert ist (sofern er diese Funktion unterstützt).

>[!NOTE]
>
>Das endgültige Rendering im dunklen Modus hängt vom individuellen E-Mail-Client ab, die Ergebnisse können daher variieren. Weitere Informationen finden Sie unter [Überlegungen zum E](#email-client-considerations)Mail-Client“.

Der benutzerdefinierte Dunkelmodus-Stil im E-Mail-Design verwendet die<!-- `@media (prefers-color-scheme: dark)` method--> `@media (prefers-color-scheme: dark)` CSS-Abfrage, die erkennt, ob der E-Mail-Client auf den Dunkelmodus eingestellt ist, und das dunkle Design anwendet, das in Ihrer E-Mail definiert ist.

_So definieren Sie benutzerdefinierte Einstellungen für den Dunkelmodus :_

1. Verschieben Sie bei Bedarf die Auswahl in _Dunkelmodus_ ( ![Dunkelmodussymbol](../assets/do-not-localize/icon-content-dark-mode.svg) ) oben rechts auf der Design-Arbeitsfläche.

1. Bearbeiten Sie alle Stilattribute wie Text, Hintergrund oder Schaltflächen.

   ![Bedienfeld für Textformatierungseinstellungen im Dunkelmodus mit Farb- und Schriftoptionen](./assets/email-color-mode-dark-text-settings.png){width="700" zoomable="yes"}

1. Definieren Sie für die Bilder und Symbole bestimmte Assets nur für den Dunkelmodus.

   Sie können die Farben von Bildern und Symbolen nicht ändern, aber Sie können alternative Assets definieren, die für den Dunkelmodus verwendet werden sollen. Sie können mit verschiedenen Farbkombinationen für Ihre Symbole experimentieren oder Anpassungen für Farbe und Sättigung für fotografische Bilder vornehmen.

   ![Symbole mit unterschiedlichen Farbkombinationen](../assets/do-not-localize/color-contrast-images-diagram.svg){width="80%"}

   Wählen Sie ein beliebiges Bild aus und wechseln Sie **[!UICONTROL Dunkelmodus]** mithilfe des entsprechenden Umschalters im Bereich **[!UICONTROL Einstellungen]**. Wählen Sie dann ein anderes Bild-Asset aus.

   ![Einstellungen für den Dunkelmodus mit Anzeige der Option zur Auswahl eines anderen Bild-Assets für den Dunkelmodus](./assets/email-color-mode-dark-image-settings.png){width="700" zoomable="yes"}

   Weitere Informationen [&#x200B; Auswahl eines Bild-Assets finden &#x200B;](./email-authoring.md#add-image-assets) unter „Hinzufügen von Bild-Assets“.

1. Wählen Sie zu einem beliebigen Zeitpunkt während der Designänderungen **[!UICONTROL Zur Live-Ansicht wechseln]**, um zu überprüfen, wie Ihre Inhalte möglicherweise auf verschiedenen Gerätegrößen gerendert werden.

   Ändern Sie in dieser Ansicht den Selektor in _Dunkelmodus_ ( ![Dunkelmodussymbol](../assets/do-not-localize/icon-content-dark-mode.svg) ), um eine Vorschau der Dunkelmodusversion Ihres Inhalts auf den verschiedenen Geräten anzuzeigen.

   ![Bedienfeld „Live-Ansicht“ mit E-Mail-Inhalten im Dunkelmodus über verschiedene Gerätegrößen hinweg](./assets/email-color-mode-dark-live-view.png){width="800" zoomable="yes"}

   >[!CAUTION]
   >
   >Die Live-Ansicht ist eine allgemeine Vorschau, die vergleicht, wie das Rendering über verschiedene Gerätegrößen hinweg aussehen könnte. Das endgültige Rendering kann je nach E-Mail-Client des Empfängers variieren.

1. Wenn die Änderungen am Dunkelmodus abgeschlossen sind, klicken Sie auf **[!UICONTROL Inhalt simulieren]**.

   ![E-Mail-Design-Arbeitsfläche mit hervorgehobener Schaltfläche „Inhalt simulieren“ zum Testen des Dunkelmodus](./assets/email-color-mode-dark-simulate-content.png){width="700" zoomable="yes"}

   Testen Sie Ihr E-Mail-Design mit den Vorschau- und Proofing-Tools. Weitere [&#x200B; finden Sie unter „Vorschau und Test &#x200B;](./email-simulate-content.md) E-Mail-Inhalts“.

1. Wenn Sie über ein Litmus Enterprise-Konto verfügen, wählen Sie **[!UICONTROL E-Mail rendern]** aus, um das endgültige Rendering des Dunkelmodus für verschiedene E-Mail-Clients in Litmus anzuzeigen.

   Weitere Informationen finden [&#x200B; unter „Testen von E](./email-test-rendering.md)Mail-Rendering mit Litmus“.

   >[!CAUTION]
   >
   >Während die Simulation der Darstellung von E-Mails im Dunkelmodus sehr nahe kommt, kann das tatsächliche Rendering aufgrund von Variationen bei E-Mail-Dienstanbietern oder Einstellungen auf Geräteebene unterschiedlich sein.

## Best Practices {#best-practices}

Da der dunkle Modus in den wichtigsten E-Mail-Clients immer beliebter wird, müssen Sie berücksichtigen, wie Ihre E-Mails in hellen und dunklen Umgebungen gerendert werden – unabhängig davon, ob Sie einen [benutzerdefinierten dunklen Modus](#define-custom-dark-mode) verwenden oder nicht.

Der dunkle Modus kann Farben, Hintergründe und Bilder verändern – und manchmal bestimmte Design-Entscheidungen überschreiben. Befolgen Sie die folgenden Best Practices, um visuelle Konsistenz, Barrierefreiheit und Markenintegrität sicherzustellen:

| Übung |            |
| -------- | ---------- |
| Optimieren von Bildern und Logos | Checkliste:<ul><li>Speichern Sie Logos und Symbole als PNG-Dateien mit transparentem Hintergrund, um sichtbare weiße Kästchen im Dunkelmodus zu vermeiden. <li>Vermeiden Sie Bilder mit hartcodierten weißen oder hellen Hintergründen. <li>Wenn Transparenz nicht möglich ist, platzieren Sie Bilder in Ihrem Design auf einem einfarbigen Hintergrund, um unangenehme Farbinversionen zu verhindern. |
| Ihre Hintergründe ansehen | Checkliste:<ul><li>Stellen Sie einen ausreichenden Kontrast zwischen Text- und Hintergrundfarben sicher, damit die Lesbarkeit sowohl im hellen als auch im dunklen Modus gewahrt bleibt. <li>Vermeiden Sie es, sich bei kritischen Inhalten allein auf Hintergrundfarben zu verlassen. Einige Clients überschreiben Hintergrundfarben im Dunkelmodus, sodass wichtige Informationen weiterhin sichtbar sind. |
| Entwerfen barrierefreier Inhalte im Dunkelmodus | Checkliste:<ul><li>Verwenden Sie Farbkombinationen, die für Menschen mit Farbenblindheit leicht zu unterscheiden sind. <li>Verwenden Sie eine Mitteltonpalette, um sowohl vor hellen als auch vor dunklen Hintergründen einen Kontrast sicherzustellen. <li>Verwenden Sie barrierefreie Farbkombinationen mit hohem Kontrast, um die Lesbarkeit zu verbessern und [!DNL Web Content Accessibility Guidelines (WCAG)] Standards zu erfüllen. Verwenden Sie Tools wie [!DNL WebAIM Contrast Checker], um den Farbkontrast zu überprüfen. <li>Vermeiden Sie dünne Schriftarten, da sie die Lesbarkeit beeinträchtigen können. Wenn für Ihre Marke eine dünne Schriftart erforderlich ist, verwenden Sie sie für den dunklen Modus eine Fettformatierung. <li>Überspringen Sie reines Weiß auf reinem Schwarz, was zu Augenbelastungen führen kann und in einigen E-Mail-Clients automatisch invertiert werden könnte. <li>Wenn der dunkle Modus nicht unterstützt wird, können Sie barrierefreie Fallback-Stile bereitstellen. |
| Testen von E-Mails in einer Umgebung mit dunklem Modus | Checkliste:<ul><li>Verwenden Sie die [Dunkelmodusvorschau](#preview-dark-mode) im E-Mail-Design-Bereich, der invertierte Farbschemata verwendet, um Probleme frühzeitig zu erkennen. <li>Verwenden Sie ein Litmus Enterprise-Konto mit der Option [[!UICONTROL E-Mail rendern]](./email-test-rendering.md), um Ihre Designs für gängige E-Mail-Clients (wie Apple Mail, Gmail und Outlook) zu simulieren und zu sehen, wie sich Farben und Bilder im Dunkelmodus verhalten. |

<!--KEEP dark mode accessibility best practices IN ONE SINGLE LOCATION - for now listed on this page.
If needed, it can be moved to the Design accessible content page:
The best practices for designing accesible content in dark mode are listed in [this section](accessible-content.md#dark-mode).-->

<!--**Inline critical styles**

Inline CSS helps maintain more control over styling, as some clients strip external styles in dark mode.-->
