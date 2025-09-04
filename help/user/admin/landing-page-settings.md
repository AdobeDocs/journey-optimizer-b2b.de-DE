---
title: Konfiguration einer Landingpage
description: Erfahren Sie, wie Sie auf die Einstellungen der Landingpage zugreifen und diese konfigurieren können, damit Ihr Marketing-Team Web-Seiten zur Unterstützung seiner Kampagnen erstellen und veröffentlichen kann.
feature: Setup, Landing Pages, Content
role: Admin
hide: true
hidefromtoc: true
badgeBeta: label="Beta" type="informative" tooltip="Diese Funktion befindet sich derzeit in einer eingeschränkten Beta-Version"
exl-id: 54b812cb-0129-4253-8e9e-538c25fc4709
source-git-commit: 8bd3d696a52a813b88de9e3b58145b1cbfb3fa32
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 26%

---

# Konfiguration einer Landingpage

Admins sollten sicherstellen, dass die Landingpage-Einstellungen für Marketing-Fachleute konfiguriert sind, die diese Seiten erstellen und veröffentlichen.

## Einstellungen

Um die Konfiguration der Landingpage zu überprüfen, gehen Sie zu **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]**. Wählen _[!UICONTROL im]_ unter „Landingpages“ die Option **[!UICONTROL Einstellungen]** aus.

![Landingpage-Einstellungen](./assets/config-landing-pages-settings.png){width="800" zoomable="yes"}

### Kontozeichenfolge {#account-string}

>[!CONTEXTUALHELP]
>id="ajo-b2b_landing_pages_account_string"
>title="Kontozeichenfolge für Landingpages"
>abstract="Die Kontozeichenfolge identifiziert die Instanz von Adobe Journey Optimizer B2B Edition, die die Landingpages hostet."

Die Kontozeichenfolge identifiziert die Adobe Journey Optimizer B2B edition-Instanz, die die Landingpages hostet. Stellen Sie sicher, dass Ihr System-Team den DNS-Eintrag hinzufügt und konfiguriert.

### Vorbefüllen von Formularen {#form-prefill}

>[!CONTEXTUALHELP]
>id="ajo-b2b_landing_pages_form_prefill"
>title="Einstellungen zum Vorbefüllen von Landingpage-Formularen"
>abstract="Sie können die Option zum Vorbefüllen von Formularen aktivieren, damit Formulare auf Ihren Landingpages vorbefüllte Informationen für bekannte Benutzerinnen und Benutzer verwenden können."

Aktivieren Sie die Option **[!UICONTROL Formularvorbefüllung]**, damit Formulare auf Ihren Landingpages vorbefüllte Informationen für bekannte Benutzer verwenden können. Wenn diese Option deaktiviert ist, können Autoren von Landingpages keine vorausgefüllten Formularfelder einschließen.

### Datenstrom {#datastream}

>[!CONTEXTUALHELP]
>id="ajo-b2b_landing_pages_datastream"
>title="Erforderlicher Datenstrom"
>abstract="Der Datenstrom ist erforderlich, um Seitenereignisse von den Landingpages in dieser Domain zu erfassen."

>[!CONTEXTUALHELP]
>id="ajo-b2b_landing_pages_missing_datastream"
>title="Fehlende Datenstrom-ID"
>abstract="In der Subdomain fehlt eine Datenstrom-ID, die für ein ordnungsgemäßes Routing erforderlich ist. Konfigurieren Sie ihn in den Einstellungen, um fortzufahren"

Legen Sie die Option **[!UICONTROL Datenstrom]** fest, um einen Datenstrom für die Ereigniserfassung von Landingpages zu konfigurieren.

## Subdomains {#add-subdomain}

>[!CONTEXTUALHELP]
>id="ajo-b2b_landing_pages_add_subdomain"
>title="Hinzufügen einer Landingpage-Subdomain"
>abstract="Sie können maximal 50 Subdomains hinzufügen. Richten Sie für jede eindeutige Marken-URL, die Sie in Adobe Journey Optimizer B2B Edition hosten möchten, eine neue Subdomain ein."

>[!CONTEXTUALHELP]
>id="ajo-b2b_landing_pages_configure_subdomain"
>title="Konfigurieren einer Landingpage-Subdomain"
>abstract="Zum Veröffentlichen von Landingpages ist eine konfigurierte Subdomain erforderlich. Sie können eine Subdomain verwenden, die bereits an Adobe delegiert ist, oder eine neue Subdomain erstellen."

Eine Landingpage-Subdomain sollte dabei helfen, den Inhaltstyp, den Produktnamen oder die Kampagne zu identifizieren und die Authentizität der Seite zu stärken. Bevor Sie die Subdomains konfigurieren, definieren Sie einen oder mehrere CNAMEs, die für Ihre Landingpages verwendet werden sollen. Beispiel:

* **Produkt**.[CompanyDomain].com
* **Los**.[CompanyDomain].com
* **Anmeldung**.[CompanyDomain].com

In diesen Beispielen ist der erste Teil (fett gedruckt) der `LandingPageCNAME`.

Fügen Sie für jede eindeutige Marken-URL, die Sie auf Adobe Journey Optimizer B2B edition hosten möchten, eine neue Subdomain hinzu. Sie können maximal 50 Subdomains hinzufügen.

>[!IMPORTANT]
>
>Es ist nicht zulässig, Adobe eine ungültige Subdomain zuzuweisen. Geben Sie eine gültige Subdomain ein, der Ihr Unternehmen gehört, z. B. _marketing.meinefirma.com_.

Um Ihre Subdomains zu überprüfen und neue hinzuzufügen, gehen Sie zu **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]**. Wählen _[!UICONTROL im]_ unter „Landingpages“ die Option **[!UICONTROL Subdomains]** aus.

![Landingpage-Subdomains](./assets/config-landing-pages-settings.png){width="800" zoomable="yes"}

_So fügen Sie eine Landingpage-Subdomain hinzu :_

1. Klicken Sie **[!UICONTROL oben]** auf „Subdomain hinzufügen“.

1. Geben Sie in _[!UICONTROL Details zur Subdomain]_ die Informationen zur Subdomain ein:

   * **[!UICONTROL Subdomain]** - Die zu verwendende Subdomain-URL wie `marketing.yourcompany.com`
   * **[!UICONTROL Standardseite]** - Die URL für die Standard-Subdomain-Seite, z. B. `marketing.yourcompany.com/products`
   * **[!UICONTROL Fallback-]**: Die URL für die Fallback-Seite, die verwendet werden soll, wenn eine Landingpage in der Subdomain nicht aktiv ist, z. B. `marketing.yourcompany.com/expired`

   ![Landingpage-Subdomain hinzufügen](./assets/config-landing-pages-add-subdomain.png){width="700" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Speichern]**.
