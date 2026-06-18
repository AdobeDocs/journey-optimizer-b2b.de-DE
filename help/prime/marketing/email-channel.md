---
title: E-Mail-Kanal
description: 'Hinzufügen von E-Mail-Aktionsknoten zu Account-Journey: Erstellen Sie neue E-Mails oder verwenden Sie bestehende Marketo Engage-E-Mails für zielgerichtete Kommunikation in Journey Optimizer B2B edition.'
feature: Email Authoring, Account Journeys
role: User
autotag-review: '2026-06-18T20:30:25.418Z'
TQID: 'https://experienceleague.adobe.com/K3OZnLvtSdwSq6AT4JlRQ62t32d6smIJ4K9EEnK-QUc'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
  - id: f01b5556-e951-40ba-8625-2e3001864f2b
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: ff0c35fa-aa7e-4050-a37c-198fcacd09e6
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 0a877cc1fc0dfd9c3d8271c8f7be6a5e34a69a9a
workflow-type: tm+mt
source-wordcount: 881
ht-degree: 4%

---

# E-Mail-Kanal

[!DNL Adobe Journey Optimizer B2B Prime] bietet B2B-Marketern ein modernes, für Unternehmen geeignetes Erlebnis für E-Mail-Authoring und -Versand. Diese Version führt neu gestaltete E-Mail-Design-Tools und einen kompletten Satz von E-Mail-Zustellbarkeitssteuerelementen ein.

>[!NOTE]
>
>Wenn Sie zum ersten Mal eine E-Mail senden, stellen Sie sicher, dass der [E-Mail-Kanal und Zustellbarkeit](../admin/configuration-email-deliverability.md) konfiguriert ist.

## E-Mail-Kanal - Übersicht {#overview}

* **E-Mail** Kanalkonfigurationen - Verwalten der Absenderidentität, des Antwortverhaltens, des Marketing- vs. Transaktionsnachrichtentyps und des Trackings.
* **E-Mail-Zustellbarkeitskontrollen** - Richten Sie Ihren E-Mail-Zustellbarkeitskanal ein, einschließlich der Zuweisung von Subdomains (vollständig delegierte und CNAME-Methoden), der automatischen Konfiguration von DMARC, SPF/DKIM und der Unterstützung eines freigegebenen IP-Pools.
* **Aktion „E-Mail senden** - Fügen Sie von einer Journey aus einen Aktionsknoten _E-Mail senden_ hinzu, einschließlich Personalisierung mithilfe von Profilattributen (Handlebars-Syntax).
* **Visuelle E-Mail-Design-Tools per Drag-and-Drop** - Entwerfen Sie Ihren E-Mail-Inhalt mit Strukturen, Inhaltskomponenten, Designs, Unterstützung für den Dunkelmodus und wiederverwendbaren visuellen Fragmenten.
* **Marketo Design Studio-Assets** - Wählen Sie Bilder und Assets aus einer einmaligen Kopie Ihrer Marketo Engage-Asset-Bibliothek direkt auf der E-Mail-Arbeitsfläche.
* **Wiederverwendbare Vorlagen und Fragmente** - Speichern Sie allgemeine Kopf- und Fußzeilen, CTAs und vollständige E-Mail-Layouts und verwenden Sie sie in allen Journey.
* **Rollenbasierte Zugriffssteuerung (RBAC)** - Wenden Sie granulare Berechtigungen zum Erstellen, Bearbeiten, Genehmigen und Senden von E-Mails an.

## Schlüsselkonzepte {#key-concepts}

Bevor Sie E-Mails für Personen-Journey erstellen und E-Mail-Inhalte verfassen, sollten Sie die folgenden Konzepte überprüfen:

| Konzept | In [!DNL Journey Optimizer B2B Prime] Prime |
| ------- | ---------------------- |
| **_E-Mail-Design-Bereich_** | Die visuelle Arbeitsfläche und Design-Tools, die zum Erstellen von E-Mail-Inhalten verwendet werden. Es enthält Layout-Komponenten, Vorlagen, Fragmente und Designs per Drag-and-Drop und einen Personalisierungseditor. |
| **_Vorlage_** | Ein wiederverwendbares E-Mail-Layout, das zum Erstellen einer neuen E-Mail verfügbar ist. Dabei kann es sich entweder um eine integrierte Beispielvorlage handeln, die von Adobe bereitgestellt wird, oder um eine benutzerdefinierte Vorlage, die von Ihrem Team erstellt wurde. |
| **_Visuelles Fragment_** | Ein wiederverwendbarer Inhaltsblock (z. B. Kopf- und Fußzeile, CTA, Haftungsausschluss), der in mehrere E-Mails eingefügt werden kann. Beim Aktualisieren eines Fragments wird die Änderung an jede E-Mail weitergegeben, die es verwendet. |
| **_Design_** | Eine wiederverwendbare Stilvorgabe (Farben, Typografie, Abstände, Schaltflächenstile), die auf eine E-Mail angewendet wird. |
| **_Personalization-Token_** | Ein Handlebars-Ausdruck, z. B. `{{profile.firstName}}`, wird zum Sendezeitpunkt mithilfe der Profildaten jedes Empfängers aufgelöst. |
| **_Aktion „E-Mail senden“_** | Der Journey-Aktionsknoten, der eine Kanalkonfiguration und E-Mail-Inhalt zum Versand einer E-Mail verwendet. |

## Hinzufügen einer E-Mail von einer Journey

Um E-Mails von einer Journey zu senden, fügen Sie den Knoten _Aktion ausführen_ hinzu und konfigurieren Sie ihn so, dass E-Mails gesendet werden.

1. Klicken Sie auf der Journey-Arbeitsfläche auf das Symbol **+** und wählen Sie **[!UICONTROL Aktion ausführen]**.

1. Legen Sie in den Knoteneigenschaften auf der rechten Seite die Aktion auf **[!UICONTROL E-Mail senden]** fest.

   ![Aktion durchführen - E-Mail senden](./assets/person-action-node-send-email.png){width="450"}

1. E-Mail-Quelle auswählen:

   * **E-Mail erstellen/bearbeiten** - Wählen Sie diese Option, um den E-Mail-Inhalt einschließlich Betreffzeile, Absenderinformationen und E-Mail-Textkörper im E-Mail-Design-Bereich zu definieren.

   * **[!UICONTROL Verwenden einer von KI personalisierten E-]** - Wählen Sie diese Option, um eine von KI generierte E-Mail im E-Mail-Design-Bereich zu verfeinern. Diese E-Mails sind so optimiert, dass KI-unterstützte Posteingangskunden ihre Zusammenfassungen und Antworten in Ihren Angeboten und Aktionsaufrufen vermitteln.

1. Klicken Sie **[!UICONTROL E-Mail erstellen]**.

1. Geben _[!UICONTROL im Dialogfeld „E]_ Mail erstellen“ einen eindeutigen **[!UICONTROL Name]** (erforderlich) und einen **[!UICONTROL Beschreibung]** (optional) ein.

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

## Definieren der E-Mail-Eigenschaften und -Aktionen

1. Wenn der Knoten _[!UICONTROL E-Mail senden]_ auf der Arbeitsfläche &quot;Journey&quot; ausgewählt ist, klicken **[!UICONTROL in den]** auf der rechten Seite auf „E-Mail bearbeiten“.

<!-- Staging environment broken -->

für die E-Mail und eine **[!UICONTROL Betreffzeile]**.

Dadurch wird die Registerkarte **[!UICONTROL Aktionen]** geöffnet, auf der Sie die zu verwendende E-Mail-Konfiguration auswählen oder erstellen können.

1. (Optional) Wählen Sie einen Regelsatz in den Geschäftsregeln aus, um Begrenzungsregeln auf Ihre E-Mail-Aktion anzuwenden.

Sie können die Option [Versandzeitoptimierung“ verwenden](./email-send-time-optimization.md) um die beste Versandzeit für die Nachricht vorherzusagen und so die Interaktion basierend auf historischen Öffnungs- und Klickraten zu maximieren. Weitere Informationen

Wählen Sie die Schaltfläche Inhalt bearbeiten aus und erstellen Sie Ihren Inhalt nach Bedarf mit der E-Mail-Designer.

Zurück zur Journey-Arbeitsfläche. Schließen Sie bei Bedarf Ihren Journey-Fluss ab, indem Sie zusätzliche Aktionen oder Ereignisse per Drag-and-Drop verschieben.

Weiterführende Informationen zum Erstellen, Konfigurieren und Veröffentlichen von Journey finden Sie auf dieser Seite.


### E-Mail-Einstellungen definieren {#email-settings}

Konfigurieren Sie die Einstellungen auf **[!UICONTROL Registerkarte]** Details“ des Bedienfelds „Knotenübersicht“.

| Einstellung | Beschreibung |
| ------- | ----------- |
| **[!UICONTROL Absendername]** | Der Absendername wird in der E-Mail-Kopfzeile angezeigt. Unterstützt Personalisierungs-Token. |
| **[!UICONTROL Von E-Mail]** | Absender-E-Mail-Adresse. Standardwerte aus der Kanalkonfiguration. Unterstützt Personalisierung. |
| **[!UICONTROL Antwortadresse]** | Adresse, an die die Empfänger antworten. Unterstützt Personalisierung. |
| **[!UICONTROL Betreffzeile]** | E-Mail-Betreffzeile. Bearbeitbar ab dem bei der Erstellung eingegebenen Wert. |
| **[!UICONTROL Branding-Domain]** | Für den markenspezifischen Versand verwendete Domain. |
| **[!UICONTROL Dedizierte IP]** | Spezifische IP-Adresse für das Tracking der Zustellbarkeit. |
| **[!UICONTROL Operative E-Mail]** | Wenn diese Option aktiviert ist, werden Opt-out- und Abmeldeunterdrückung umgangen. Nur für legitime operative Nachrichten verwenden. |
| **[!UICONTROL Als Webseite anzeigen]** | Erzeugt einen Webseitenlink für den E-Mail-Inhalt. |
| **[!UICONTROL Öffnungs-Tracking deaktivieren]** | Verhindert das Tracking der Aktivität zum Öffnen von E-Mails. |
| **[!UICONTROL Preheader]** | Kurzer Zusammenfassungstext, der in der Vorschau des Posteingangs nach der Betreffzeile angezeigt wird. |
| **[!UICONTROL CC-Adressen]** | Fügen Sie bis zu 25 Lead- oder Unternehmens-E-Mail-Felder hinzu, um eine Kopie zu erhalten. |

### Prüfen von Warnhinweisen {#alerts}

[!DNL Journey Optimizer B2B Prime] Probleme werden oben rechts im E-Mail-Editor angezeigt. Beheben Sie alle Fehler, bevor Sie den Journey aktivieren - Warnhinweise sind nur Empfehlungen.

**Fehler** (Journey-Aktivierung verhindern):

* Absendername ist leer
* Betreffzeile fehlt
* E-Mail-Inhalt ist leer

**Warnungen** (Empfehlungen):

* Der Opt-out-Link ist nicht im Text der E-Mail enthalten
* Textversion von HTML ist leer
* Leere Links erkannt
* E-Mail überschreitet 100 KB
