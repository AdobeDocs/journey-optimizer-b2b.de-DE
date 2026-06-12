---
title: Landingpages
description: Landingpages für Personen-Journey erstellen, entwerfen und veröffentlichen - von Grund auf neu erstellen, HTML importieren, Formulare hinzufügen, Inhalte personalisieren und Links aus E-Mails in Journey Optimizer B2B Prime erstellen.
autotag-review: '2026-06-12T22:53:39.337Z'
TQID: 'https://experienceleague.adobe.com/BvtB0i5CzlVutPA6HAzZy-Gfymw7ppZwthyBauyciLc'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: e666e996-b2cf-4c45-8fc2-1c625212abab
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: a96755d6-1f54-4f3f-a971-d31f83705ab7
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: cb3217c9fd7beb712d0c61638d143b798010d2b7
workflow-type: tm+mt
source-wordcount: 1461
ht-degree: 6%

---

# Landingpages

Eine Landingpage ist eine eigenständige Web-Seite, auf der Sie Kontakte und Kunden leiten können, nachdem sie auf ein verknüpftes Element in einer E-Mail, SMS-Nachricht oder einem beliebigen digitalen Ort geklickt haben. Sie können diese Seiten in Ihre Account-Journey integrieren, damit Ihre Interessenten und Kunden Ihre Nachrichten im Internet anzeigen und in Ihren Account-Journey Fortschritte erzielen können. Im visuellen Design-Bereich für Landingpages können Sie Landingpages erstellen, personalisieren und in der Vorschau anzeigen.

Häufige Anwendungsfälle für Landingpages:

* Bereitstellen von Opt-in- oder Opt-out-Kampagnen für Marketing-Nachrichten oder einen bestimmten Service. Verwenden Sie einen Link in einer E-Mail oder einer anderen Kommunikation zu einer Zielliste.
* Sammeln Sie das Einverständnis, bevor Sie Nachrichten senden, und senden Sie eine Bestätigungs-E-Mail beim Opt-in oder Opt-out.
* Profildaten (progressive Profilerstellung, Voreinstellungen, Registrierungen und ähnliche Szenarien) mithilfe von Formularen auf Landingpages erfassen oder aktualisieren.
* Personen zu kampagnenspezifischen Informationen weiterleiten, die für Ihre Journey-Orchestrierung entwickelt wurden.
* Personen zu einem dedizierten Web-Formular umleiten, ohne eine externe Seite außerhalb von Journey Optimizer B2B Prime zu erstellen.

<!-- 
## Landing page workflow

To direct members of a journey audience to a defined web page when they click a specific link, create a landing page in Journey Optimizer B2B Edition: 


1. [Create the page](./landing-pages-create-publish.md) - Select a preset, set up the primary page, and add any required subpages.
1. [Design the landing page content](./landing-page-design.md) - Build the page content using drag-and-drop visual design components.
1. [Test and publish the landing page](./landing-pages-create-publish.md) - Preview the page, test form behavior, and then publish to make it live.
1. [Link to the page from your journey](#link-to-a-landing-page) - Add the landing page URL to an email, SMS, or journey action so that recipients can reach it.


For example, you can create and design landing pages to direct your users to online information. The page could include a form where they can opt in or opt out from receiving your communications. Or it could be an opportunity to subscribe to a recurring communications, such as a newsletter. 

You can create, personalize, and preview landing pages in the visual design space.
-->

## Zugreifen auf und Verwalten von Landingpages

Um auf die Landingpages in Journey Optimizer B2B Prime zuzugreifen, gehen Sie zum linken Navigationsbereich und klicken Sie auf **[!UICONTROL Content-Management]** > **[!UICONTROL Landingpages]**. Diese Aktion zeigt eine Liste aller in der Instanz erstellten Landingpages an.

Die Liste ist nach der Spalte _[!UICONTROL Geändert]_ sortiert, wobei die zuletzt aktualisierten Elemente oben stehen. Klicken Sie auf den Spaltentitel, um zwischen aufsteigender und absteigender Reihenfolge zu wechseln.

### Filtern der Landingpage-Liste

Um nach einer Landingpage anhand des Namens zu suchen, geben Sie eine Textzeichenfolge in die Suchleiste für eine Übereinstimmung ein. Klicken Sie auf das _Filter_-Symbol <!-- ( ![Show or hide filters icon](../assets/do-not-localize/icon-filter.svg) ) -->, um die verfügbaren Filteroptionen anzuzeigen und die Einstellungen zu ändern, um die angezeigten Elemente entsprechend Ihren angegebenen Kriterien zu filtern.

![Filtern Sie die angezeigten Landingpages](./assets/landing-pages-list-filtered.png){width="800" zoomable="yes"}

<!-- 
This is going away? ### Customize the column display

Customize the columns that you want to display in the table by clicking the _Customize table_ icon ( ![Customize table icon](../assets/do-not-localize/icon-column-settings.svg) ) at the top right. 

In the dialog, select the columns to display and click **[!UICONTROL Apply]**.

![Select the columns that you want to display](./assets/landing-pages-customize-table-dialog.png){width="300"} 
-->

### Status und Lebenszyklus der Landingpage

Der Landingpage-Status bestimmt, ob Links in Ihren E-Mail- und SMS-Inhalten verfügbar sind und welche Änderungen Sie daran vornehmen können.

| Status | Beschreibung |
| -------------------- | ----------- |
| Entwurf | Wenn Sie eine Landingpage erstellen, befindet sie sich im Status Entwurf . Er bleibt in diesem Status, bis Sie den visuellen Inhalt definieren oder bearbeiten und bis Sie ihn als gehostete Seite veröffentlichen. Verfügbare Aktionen:<br/><ul><li>Name oder Beschreibung bearbeiten<li>Link-URL bearbeiten<li>Bearbeiten im visuellen Design-Bereich<li>Veröffentlichen<li>Duplizieren<li>Löschen |
| Veröffentlicht | Wenn Sie eine Landingpage veröffentlichen, wird sie auf der Journey Optimizer B2B Prime-Instanz gehostet und steht dann für die Verknüpfung in E-Mail- oder SMS-Nachrichteninhalten zur Verfügung. Verfügbare Aktionen:<br/><ul><li>Name oder Beschreibung bearbeiten<li>Link-URL bearbeiten<li>Link im Inhalt von E-Mail- oder SMS-Nachrichten hinzufügen<li>Versionsentwurf erstellen<li>Duplizieren<li>Löschen |
| Mit Entwurf veröffentlicht | Wenn Sie einen Entwurf aus einer veröffentlichten Landingpage erstellen, bleibt die veröffentlichte Version erhalten, und der Entwurfsinhalt kann im visuellen Design-Bereich geändert werden. Wenn Sie die Entwurfsversion veröffentlichen, ersetzt sie die aktuell veröffentlichte Version, und der Inhalt wird auf der gehosteten Seite aktualisiert. Verfügbare Aktionen:<br/><ul><li>Name oder Beschreibung bearbeiten<li>Link-URL bearbeiten<li>Link im Inhalt von E-Mail- oder SMS-Nachrichten hinzufügen<li>Bearbeiten der Entwurfsversion im visuellen Entwurfsbereich<li>Entwurfsversion veröffentlichen<li>Duplizieren<li>Löschen (löscht beide Versionen)<li>Entwurf verwerfen (kehrt zum Status „Veröffentlicht“ zurück) |

<!-- ![Landing page status lifecycle](./assets/status-lifecycle-diagram.png){zoomable="yes"} -->

## Erstellen einer Landingpage {#create-landing-page}

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_lp_create"
>title="Definition und Konfiguration Ihrer Landingpage"
>abstract="Um eine Landingpage zu erstellen, müssen Sie eine Voreinstellung auswählen, dann die primäre Seite und die untergeordneten Seiten konfigurieren und Ihre Seite schließlich testen, bevor Sie sie veröffentlichen."

TBD

## Konfigurieren der Primärseite {#configure-primary-page}

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_lp_primary_page"
>title="Definieren der primären Seiteneinstellungen"
>abstract="Definieren Sie die Primärseite, die sofort angezeigt wird, wenn ein Empfänger auf den Landingpage-Link klickt, z. B. in einer E-Mail oder auf einer Website."

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_lp_access_settings"
>title="Definieren Ihrer Landingpage-URL"
>abstract="Definieren Sie in diesem Abschnitt eine eindeutige Landingpage-URL. Für den ersten Teil der URL müssen Sie zuvor eine Landingpage-Subdomain als Teil der von Ihnen ausgewählten Voreinstellung eingerichtet haben."

TBD

## Testen der Landingpage {#test-landing-page}

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_preview_lp_profiles"
>title="Erstellen einer Vorschau und Testen Ihrer Landingpage"
>abstract="Nachdem Sie die Einstellungen und den Inhalt Ihrer Landingpage definiert haben, können Sie mithilfe von Testprofilen eine Vorschau der Seite anzeigen."

TBD

## Bearbeiten einer Landingpage

Änderungen an einer Landingpage hängen vom aktuellen Status ab:

* Wenn sich eine Landingpage im Status **_Entwurf_** befindet, können Sie alle zugehörigen Details, die URL und den visuellen Inhalt bearbeiten.
* Wenn sich eine Landingpage im Status **_Veröffentlicht_** befindet, können Sie die Beschreibung bearbeiten, nicht jedoch den Namen. Um den visuellen Inhalt zu ändern, müssen Sie eine Entwurfsversion der Seite erstellen.
* Wenn sich eine Landingpage im Status **_Veröffentlicht mit Entwurf_** befindet, ist die Bearbeitung der Details auf die Beschreibung beschränkt. Sie können auch den visuellen Inhalt für die Entwurfsversion bearbeiten.

>[!BEGINTABS]

>[!TAB Entwurf]

1. Klicken Sie auf der _[!UICONTROL Landingpages]_ auf den Namen der Landingpage, um sie zu öffnen.

   Eine Vorschau des visuellen Inhalts mit den Details der Landingpage wird auf der rechten Seite angezeigt.

1. Ändern Sie alle Details, z. B. Namen und Beschreibung.

   <!-- ![Details for landing page with Draft status](./assets/landing-page-draft-details.png){width="700" zoomable="yes"} -->

1. Um Änderungen am Inhalt im visuellen Design-Bereich vorzunehmen, klicken Sie auf **[!UICONTROL Landingpage bearbeiten]**.

   <!-- 
   Use the visual design tools as needed:

   * [Add structure and content](./landing-page-design.md#structure-content-landing-page)
   * [Add Assets](./landing-page-design.md#add-assets)
   * [Navigate the layers, settings, and styles](./landing-page-design.md#navigate-the-layers-settings-and-styles)
   * [Personalize content](./landing-page-design.md#personalize-content)
   * [Edit linked URL tracking](./landing-page-design.md#edit-linked-url-tracking)
   -->

1. Klicken Sie **[!UICONTROL Speichern]** oder **[!UICONTROL Speichern und schließen]** um zu den Landingpage-Details zurückzukehren.

1. Wenn die Seite Ihren Kriterien entspricht und Sie sie zur Anzeige bereitstellen möchten, klicken Sie auf **[!UICONTROL Veröffentlichen]**.

>[!TAB Veröffentlicht]

1. Klicken Sie auf der _[!UICONTROL Landingpages]_ auf den Seitennamen, um die Seite zu öffnen.

   Eine Vorschau des visuellen Inhalts mit den Details der Landingpage wird auf der rechten Seite angezeigt.

1. Ändern Sie bei Bedarf die Beschreibung.

   Für eine veröffentlichte Landingpage können alle anderen Details nicht geändert werden.

1. Wenn Sie den Inhalt aktualisieren möchten, klicken Sie auf **[!UICONTROL rechten Seite auf]** Landingpage bearbeiten“.

   Klicken Sie **[!UICONTROL Dialogfeld auf]** Entwurfsversion erstellen“, um die Entwurfsversion im visuellen Entwurfsbereich zu öffnen.

   <!-- 
   ![Create draft version dialog](./assets/landing-page-create-draft-version.png){width="300"} 

   Use the visual design tools as needed:

   * [Add structure and content](./landing-page-design.md#structure-content-landing-page)
   * [Add Assets](./landing-page-design.md#add-assets)
   * [Navigate the layers, settings, and styles](./landing-page-design.md#navigate-the-layers-settings-and-styles)
   * [Personalize content](./landing-page-design.md#personalize-content)
   * [Edit linked URL tracking](./landing-page-design.md#edit-linked-url-tracking)
   -->

1. Klicken Sie **[!UICONTROL Speichern]** oder **[!UICONTROL Speichern und schließen]** um zu den Landingpage-Details zurückzukehren.

1. Wenn die Landingpage Ihren Kriterien entspricht und Sie die Änderungen auf der veröffentlichten Seite verfügbar machen möchten, klicken Sie auf **[!UICONTROL Veröffentlichen]**.

   Wenn Sie die Entwurfsversion veröffentlichen, ersetzt sie die aktuell veröffentlichte Version, und der Inhalt wird für die Seiten-URL aktualisiert.

>[!TAB Veröffentlicht mit Entwurf]

Beim Öffnen der Landingpage wird die Entwurfsversion angezeigt. Mit den Registerkarten oben im Vorschaubereich können Sie die Anzeige zwischen der veröffentlichten und der Entwurfsversion wechseln. Die Entwurfsaktionen und -details werden auf der rechten Seite angezeigt.

<!-- ![Preview and details for the landing page draft version](./assets/landing-page-published-draft-details.png){width="700" zoomable="yes"} -->

So aktualisieren Sie den Inhalt:

1. Klicken **[!UICONTROL oben]** auf „Landingpage bearbeiten“.

   <!--

   Use the visual design tools as needed:

   * [Add structure and content](./landing-page-design.md#structure-content-landing-page)
   * [Add Assets](./landing-page-design.md#add-assets)
   * [Navigate the layers, settings, and styles](./landing-page-design.md#navigate-the-layers-settings-and-styles)
   * [Personalize content](./landing-page-design.md#personalize-content)
   * [Edit linked URL tracking](./landing-page-design.md#edit-linked-url-tracking)

   -->

1. Klicken Sie **[!UICONTROL Speichern]** oder **[!UICONTROL Speichern und schließen]** um zu den Landingpage-Details zurückzukehren.

1. Wenn die Entwurfsseite Ihren Kriterien entspricht und Sie die Änderungen verfügbar machen möchten, klicken Sie auf **[!UICONTROL Veröffentlichen]**.

   Wenn Sie die Entwurfsversion veröffentlichen, ersetzt sie die aktuelle veröffentlichte Version, und der Inhalt wird auf der gehosteten Seite aktualisiert.

>[!ENDTABS]

## Duplizieren einer Landingpage

Sie können eine Landingpage mit einer der folgenden Methoden duplizieren:

* Klicken Sie auf der _[!UICONTROL Landingpage]_ auf das Symbol _Mehr_ (**…**) klicken Sie neben dem Namen der Landingpage auf **[!UICONTROL Duplizieren]**.
* Klicken Sie oben rechts auf der Detailseite der Landingpage auf **[!UICONTROL … Mehr]** und wählen Sie **[!UICONTROL Duplizieren]**.

<!-- ![Duplicate the landing page](./assets/landing-page-details-duplicate-delete.png){width="600" zoomable="yes"} -->

Geben Sie im Dialogfeld einen nützlichen Namen (eindeutig) und eine Beschreibung (optional) ein. Klicken Sie **[!UICONTROL Duplizieren]**, um die Aktion abzuschließen.

<!-- ![Enter a name and description for the duplicated landing page](./assets/landing-page-duplicate-dialog.png){width="350"} -->

Die duplizierte (neue) Seite wird dann in der Liste _Landingpages_ angezeigt.

## Löschen einer Landingpage

Sie können eine Landingpage mit einer der folgenden Methoden löschen:

* Klicken Sie auf der _[!UICONTROL Landingpage]_ auf das Symbol _Mehr_ (**…**) klicken Sie neben dem Namen der Landingpage auf **[!UICONTROL Löschen]**.
* Klicken Sie oben rechts auf der Detailseite der Landingpage auf **[!UICONTROL … Weitere]** und wählen Sie **[!UICONTROL Löschen]**.

Diese Aktion öffnet ein Bestätigungsdialogfeld. Sie können den Vorgang abbrechen, indem Sie auf **[!UICONTROL Abbrechen]** klicken oder auf **[!UICONTROL Löschen]** klicken, um den Löschvorgang zu bestätigen.

<!-- ![Delete landing page dialog](./assets/landing-page-delete-dialog.png){width="400"} -->

## Link zu einer Landingpage

Als Marketing-Experte oder Kreativschaffender, der E-Mail-, Fragment- und Seiteninhalte erstellt, können Sie Links zu den veröffentlichten (Live-)Landingpages einbetten, die in Ihrer Journey Optimizer B2B-Prime-Instanz erstellt werden.

1. Wählen Sie beim Arbeiten im visuellen Design für ein Fragment, eine E-Mail, eine Landingpage oder eine Vorlage einen Textauszug, eine Schaltflächenkomponente oder eine Bildkomponente für den Link aus.

   Die **[!UICONTROL Link]**-Optionen werden im rechten Bedienfeld angezeigt.

1. Wählen Sie für **[!UICONTROL Option]** Typ“ die Option **[!UICONTROL Landingpage]**.

   <!-- ![Link options for a landing page](/help/assets/content-design-shared/content-design-link-settings.png){width="700" zoomable="yes"} -->

1. Klicken Sie für die **[!UICONTROL Landingpage]**-Option auf das Symbol _Seite auswählen_ <!-- ( ![Show links icon](/help/assets/do-not-localize/icon-landing-page-select.svg) ) -->.

1. Legen Sie im Dialogfeld „Landingpage auswählen **[!UICONTROL als]** **[!UICONTROL Journey Optimizer B2B edition]** fest, aktivieren Sie das Kontrollkästchen für die Landingpage in der Liste der veröffentlichten Seiten und klicken Sie auf **[!UICONTROL Auswählen]**.

   <!-- ![Link options for a landing page](/help/assets/content-design-shared/content-design-link-landing-page-select.png){width="600" zoomable="yes"} -->

1. Wählen Sie für **[!UICONTROL Option]** das Verhalten des Link-Ziels aus:

   * **[!UICONTROL None]** - Öffnet den Link mit dem Standardverhalten des Browsers.
   * **[!UICONTROL Leer]** - Öffnet den Link in einem neuen Fenster oder in einer neuen Registerkarte.
   * **[!UICONTROL Self]** - Öffnet den Link im selben Frame.
   * **[!UICONTROL Parent]** - Öffnet den Link im übergeordneten Frame.
   * **[!UICONTROL Oben]** - Öffnet den Link im gesamten Fenster.

1. (Nur Text-Link) Wenn Sie den verknüpften Text unterstreichen möchten, aktivieren Sie das Kontrollkästchen **[!UICONTROL Link unterstreichen]**.

   Sie können zusätzliche Stile für den Link-Text festlegen, einschließlich der Link-Farbe, indem Sie die Registerkarte **[!UICONTROL Stile]** im rechten Bedienfeld auswählen.
