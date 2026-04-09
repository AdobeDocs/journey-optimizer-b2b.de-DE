---
title: Generative KI für Inhalte
description: Erfahren Sie, wie Sie personalisierte E-Mails und Landingpages mit generativer KI in  [!DNL Journey Optimizer B2B Edition] erstellen, einschließlich Best Practices für die Eingabeaufforderung.
feature: AI Assistant, Generative AI, Content
level: Beginner
topic: Artificial Intelligence
role: User
exl-id: 36baf7f9-2fff-4c33-bca0-7d43ec48e74a
source-git-commit: 8073984ced07e86a3fa500c5bf0bd393abbe0990
workflow-type: tm+mt
source-wordcount: '2506'
ht-degree: 32%

---

# Generative KI für Inhalte {#generative-ai-content}

>[!CONTEXTUALHELP]
>id="ajo_b2b_ai-generation-settings"
>title="KI-Inhaltserstellung"
>abstract="Nachdem Sie Ihr Layout erstellt haben, können Sie generative KI-Tools in [!DNL Journey Optimizer B2B Edition] verwenden, um Ihre Inhalte zu verbessern. Diese Funktion vereinfacht den Prozess der Personalisierung und Inhaltsverbesserung, indem sie den Inhalt entsprechend Ihrer beschreibenden Eingabeaufforderung optimiert."

>[!CONTEXTUALHELP]
>id="ajo_b2b_ai-generation-reference-context"
>title="Referenzinhalt"
>abstract="Verwenden Sie _Referenzinhalt_ um eine Asset-Datei hochzuladen, die Inhalt enthält, der zusätzlichen Kontext für generative KI in [!DNL Journey Optimizer B2B Edition] bietet, oder um eine zuvor hochgeladene Datei auszuwählen. Mit dieser Option wird sichergestellt, dass alle erforderlichen Materialien verfügbar sind, um die Qualität und Relevanz der generierten Inhalte zu verbessern."

>[!CONTEXTUALHELP]
>id="ajo_b2b_ai-generation-start"
>title="Adobe Generative AI-Begriffe"
>abstract="Der Zugriff auf diese Funktion unterliegt der Zustimmung zu den Benutzerrichtlinien für generative KI in Adobe Experience Cloud. Überprüfen Sie alle Ausgaben aus dieser Funktion auf Genauigkeit und stellen Sie sicher, dass sie für Ihren Anwendungsfall geeignet sind."
>additional-url="https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html" text="Benutzerrichtlinien für die generative KI von Adobe"

Die generative KI für Inhalte in [!DNL Adobe Journey Optimizer B2B Edition] basiert auf Microsoft Azure OpenAI und Adobe Firefly und bietet proaktive Vorschläge für Inhaltsvarianten für Text und Bilder. Optimieren Sie die Wirkung Ihrer Inhalte, indem Sie mit verschiedenen Haupttiteln und -bildern experimentieren.

Verwenden Sie die Funktionen der generativen KI für die Inhaltserstellung, [!DNL Journey Optimizer B2B Edition] die Funktionen der generativen KI von Adobe zu nutzen. Erstellen Sie personalisierten Text und personalisierte Visualisierungen für E-Mails, SMS-Nachrichten, Landingpages und mehr. Wenn Sie eine vollständige Kampagne erstellen oder bestimmte Assets verfeinern, helfen Ihnen diese Funktionen, Inhalte nahtlos an Ihren Markenrichtlinien auszurichten und dabei wertvolle Zeit zu sparen.

<!--
Generate multiple variants and build an experiment to compare them. Leveraging Journey Optimizer Content Experiment, you can define multiple message treatments to measure which one performs best for your target audience. You can choose to vary the delivery content, or subject. The message audience is randomly allocated to each treatment to determine which one works best in terms of the specified metric. Learn more about Content Experiment in this section. 
-->

>[!IMPORTANT]
>
>Um auf diese Funktionen in [!DNL Journey Optimizer B2B Edition] zugreifen zu können, benötigen Sie die Berechtigung _[!UICONTROL KI-Assistent]_ > _[!UICONTROL Inhalt generieren]_. Weitere Informationen dazu, wie ein Produktadministrator Funktionsberechtigungen erteilen kann, finden Sie unter [Rollen für Produktberechtigungen bearbeiten](../admin/user-management.md#edit-roles-for-product-permissions).

KI-Assistenten-Tools für die Inhaltserstellung werden von den folgenden Asset-Typen unterstützt:

* [E-Mails](../content/ai-assistant-emails.md)
* [!BADGE Beta] [Landingpages](../content/ai-assistant-landing-pages.md)

## Allgemeine Richtlinien und Einschränkungen {#general-guidelines-and-limitations}

Ihre Verwendung von Funktionen der generativen KI unterliegt den [Benutzerrichtlinien für die generative KI von Adobe Experience Cloud](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}. Da sich Adobe bei der Verwendung von generativen KI-Tools für die Medienerstellung zu Transparenz verpflichtet hat, wendet Adobe [Inhaltsanmeldeinformationen](https://helpx.adobe.com/de/firefly/web/get-started/learn-the-basics/content-credentials-overview.html){target="_blank"} auf alle Inhalte oder Projekte an, die ein [!DNL Firefly] generiertes Asset enthalten, wenn es heruntergeladen oder exportiert wird.

Lesen Sie diese allgemeinen Richtlinien für die Verwendung von generativer KI für Inhalte in [!DNL Journey Optimizer B2B Edition]:

* Verwenden Sie klar definierte Eingabeaufforderungen für das generative KI-Modell, um die Interpretation präzise durchzuführen. Das von Ihnen angegebene Marketing-Ziel oder die von Ihnen angegebene Eingabeaufforderung wirkt sich stark auf die Qualität des generierten Inhalts aus.

* Laden Sie Inhaltsreferenzdateien hoch, um genaue markeninterne Inhalte zu erhalten. Andernfalls basiert der Inhalt auf öffentlich verfügbaren Informationen. Der hochgeladene Inhalt kann in den folgenden Dateiformaten vorliegen: PDF, JPEG, PNG oder ZIP (mit unterstützten Dateiformaten). Die maximale Größe für eine hochgeladene Datei beträgt 50 MB. Größere Dateien oder eine große Anzahl von Bildern können funktionieren, aber das erhöht die Verarbeitungszeit.

* Verwenden Sie eine markenspezifische oder benutzerdefinierte Vorlage, um Ihren E-Mail-Inhalt zu erstellen. E-Mail-Vorlagen mit bis zu 8-10 Bildern werden empfohlen.

* Achten Sie bei der Auswahl von Varianten darauf, problematische Ausgaben mit den Symbolen „Daumen hoch“, „Daumen runter“ oder „Flag“ zu melden.

## Prompt Best Practices für generative KI {#generative-ai-prompting-guide}

>[!CONTEXTUALHELP]
>id="ajo_b2b_ai_content_prompt"
>title="Prompt-Anleitung"
>abstract="In [!DNL Journey Optimizer B2B Edition] Dokumentation erfahren Sie, wie Sie effektive Eingabeaufforderungen erstellen, mit denen hocheffiziente, markeninterne Marketing-Inhalte erstellt werden."

Dieser Leitfaden hilft Ihnen, Ihre Anfragen zu strukturieren, den Zweck klar und deutlich zu kommunizieren und sicherzustellen, dass die KI-Kommunikation Messaging produziert, die mit Ihren Markenrichtlinien, Zielgruppenanforderungen und Kampagnenzielen übereinstimmt.

Erfahren Sie, wie Sie effektive Prompts schreiben, mit denen der KI-Assistent hochwertige markenkonforme Marketing-Inhalte generieren kann, die auf Ihre Ziele abgestimmt sind.

### Verwenden des CO-STAR-Frameworks {#costar-framework}

Um die besten Ergebnisse mit den generierten Inhalten zu erzielen, sollten Sie die Eingabeaufforderungen mit dem CO-STAR-Framework organisieren. Dieser strukturierte Ansatz bietet Klarheit für genau das, was Sie benötigen.

| Komponente | Bedeutung | Warum dies wichtig ist |
| --- | ---- | ------ |
| **C – Kontext** | Hintergrund zur Kampagne, zum Produkt oder zur Situation | Bietet Verständnis für das Gesamtbild |
| **O – Ziel** | Ihr spezifisches Marketing-Ziel | Gibt an, was mit dem Inhalt erreicht werden soll |
| **S – Stil** | Gewünschte Art der Kommunikation | Legt den Ansatz fest |
| **T – Ton** | Die Emotion von Stil und Sprache | Gestaltet das Gefühl Ihrer Nachricht |
| **A – Zielgruppe** | Die Audience, auf die Sie abzielen | Stellt sicher, dass die Botschaft bei den richtigen Menschen Anklang findet |
| **R – Anforderungen** | Spezifische Einschränkungen oder unverzichtbare Komponenten | Definiert Grenzen und kritische Elemente |

{style="table-layout:fixed"}

### Grundlagen zur Eingabeaufforderung {#key-takeaways}

<table style="table-layout: fixed; width: 100%; border: 0;">
<thead style="border: 0; background-color: #FFFFFF;">
<tr>
<th>Empfohlen</th>
<th>Zu vermeiden</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<ul><li>CO-STAR-Framework zur Strukturierung verwenden
<li>Scharf zwischen neuen und vorhandenen Inhalten trennen
<li>Fokus auf die Dokumentverwendung mit spezifischer Extraktionsanleitung
<li>Auswahl für Ton, Strategie und Gebietsschema treffen
<li>Marketing-Ziele auf die Funktionalität der Inhaltstypen abstimmen
<li>Mehrere Varianten für A/B-Tests generieren</ul>
</td>
<td>
<ul><li>In Prompts Strukturänderungen, Formate oder Bildbearbeitung anfordern
<li>Erwähnen Sie den Ton/die Strategie in den Eingabeaufforderungen, sofern in Optionen verfügbar
<li>Verwenden vager Ziele wie „_promote the product_“
<li>Auswahl bedingter Elemente anfordern
<li>Layout-Änderungen über Prompts erwarten</ul>
</td>
</tr>
</tbody>
</table>

### In Prompts nicht unterstützte Inhalte

>[!TIP]
>
>Verwenden Sie die Design-Tools oder [!DNL Adobe Express] für visuelle/Bild-Änderungen.

Die folgenden Anfragen werden **_nicht unterstützt_** und sollten über andere Tools verarbeitet werden:

<table style="table-layout: fixed; border: 0;">
<thead style="border: 0; background-color: #FFFFFF">
<tr>
<th><img src="../../assets/do-not-localize/check-box-red.svg" alt="Rotes Kreuz">  E-Mail-Strukturänderungen</th>
<th><img src="../../assets/do-not-localize/check-box-red.svg" alt="Rotes Kreuz">  Änderungen am visuellen Stil</th>
<th><img src="../../assets/do-not-localize/check-box-red.svg" alt="Rotes Kreuz">  Bildbearbeitungsvorgänge</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<ul>
<li>Auswählen bestimmter zu ändernder Abschnitte</li>
<li>Löschen oder Klonen von Elementen</li>
<li>Bedingte Auswahlen</li>
<li>Hinzufügen oder Entfernen von Layout-Abschnitten</li>
</ul>
</td>
<td>
<ul>
<li>Textformatierung (fett, kursiv, Schriftgröße)</li>
<li>Farbänderungen</li>
<li>Layout-Stile (Rahmen, Abstände, Ränder)</li>
<li>Visuelle Effekte (Schatten)</li>
</ul>
</td>
<td>
<ul>
<li>Hintergrundänderungen</li>
<li>Hinzufügen von Textüberlagerungen oder Logos</li>
<li>Beschneiden oder Ändern der Größe von Bildern</li>
<li>Farbkorrekturen</li>
<li>Bildersetzung</li>
</ul>
</td>
</tr>
</tbody>
</table>

### Qualitäts-Checkliste {#quality-checklist}

Stellen Sie vor dem Generieren von Inhalten Folgendes sicher:

![Grünes Häkchen](../../assets/do-not-localize/check-box-green.svg){width="20"} **Ziel löschen**: Gibt die Aktion, das Produkt/die Dienstleistung, den Wert und den Kontext klar an.

![Grünes Häkchen](../../assets/do-not-localize/check-box-green.svg){width="20"} **Definierte Zielgruppe**: Gibt die Demografie, die Rolle oder das Segment an.

![Grünes Häkchen](../../assets/do-not-localize/check-box-green.svg){width="20"} **Ausrichtung des Inhaltstyps**: Das Ziel entspricht dem ausgewählten Kanal oder Format.

![Grünes Häkchen](../../assets/do-not-localize/check-box-green.svg){width="20"} **Auswahloptionen überprüfen**: „Ton“, „Strategie“ und „Gebietsschema“ sind ausgewählt. Schließen Sie diese nicht in die Eingabeaufforderung ein.

![Grünes Häkchen](../../assets/do-not-localize/check-box-green.svg){width="20"} **Dokumentfokus wurde angegeben**: Markiert, auf welche Inhalte oder Abschnitte verwiesen werden soll.

![Grünes Häkchen](../../assets/do-not-localize/check-box-green.svg){width="20"} **Angewendete Marke**: Es werden die entsprechenden Markenrichtlinien ausgewählt.

![Grünes Häkchen](../../assets/do-not-localize/check-box-green.svg){width="20"} **Realistischer Umfang**: Vermeiden Sie Anfragen für Layout-Änderungen, Stile oder strukturelle Bearbeitungen.

### Effektive Marketingziele {#marketing-objectives}

Achten Sie bei der Formulierung von Marketing-Zielen darauf, dass diese klar, umsetzbar und messbar sind. Vermeiden Sie schwammige oder generische Aussagen.

**Beispiele für gute Ziele:**

![Grünes Häkchen](../../assets/do-not-localize/check-box-green.svg){width="20"} „Fordern Sie Anmeldungen für die kostenlose 30-tägige Testversion des neuen KI-gestützten Analyse-Dashboards an“

![Grünes Häkchen](../../assets/do-not-localize/check-box-green.svg){width="20"} „Generieren Sie Leads für das B2B-Webinar zum Thema „Reduzierung der Cloud-Kosten um 40 %&quot;, das am 15. März stattfindet“

![Grünes Häkchen](../../assets/do-not-localize/check-box-green.svg){width="20"} „Werben Sie für den zeitlich begrenzten Rabatt von 25 % auf Premium-Abonnements, der am 25. Dezember endet“

**Beispiele zu vermeidender Formulierungen:**

![Rotes Kreuz ausblenden](../../assets/do-not-localize/check-box-red.svg){width="20"} „Produkt bewerben“ (zu vage)

![Rotes Kreuz raus](../../assets/do-not-localize/check-box-red.svg){width="20"} „Leute dazu bringen, Geschäfte zu unterzeichnen“ (Wert unklar)

![Rotes Kreuz aus](../../assets/do-not-localize/check-box-red.svg){width="20"} „E-Mail über neue Funktionen“ (Zweck fehlt)

#### Strukturieren des Ziels

Geben Sie immer den Kontext und das Wertversprechen für die Erstellung relevanter Inhalte an. Verwenden Sie die folgende Formel, um effektive Ziele zu schreiben: **Aktion + Produkt/Service + Wert/Nutzen + Dringlichkeit/Kontext**

**Beispiele für gute Ziele:**

![Grünes Häkchen](../../assets/do-not-localize/check-box-green.svg){width="20"} „Ermutigen Sie Downloads der neuen mobilen App, die Benutzern hilft, nachhaltige Lebensgewohnheiten mit personalisierten umweltfreundlichen Empfehlungen zu verfolgen“

![Grünes Häkchen](../../assets/do-not-localize/check-box-green.svg){width="20"} „Bewerben Sie sich für den exklusiven Workshop zu fortgeschrittenen Datenvisualisierungstechniken für Marketing-Experten“

![Grünes Häkchen](../../assets/do-not-localize/check-box-green.svg){width="20"} „Lenken Sie die Teilnahme an der Produkteinführungsveranstaltung, bei der der revolutionäre KI-Schreibassistent vorgestellt wird, der mehr als 5 Stunden pro Woche spart“

**Beispiele zu vermeidender Formulierungen:**

![Rotes Kreuz ausblenden](../../assets/do-not-localize/check-box-red.svg){width="20"} „Neue App ankündigen“ (Wertversprechen und Kontext fehlen)

![Rotes Kreuz](../../assets/do-not-localize/check-box-red.svg){width="20"} „Anmeldung für Workshop“ (mangelt es an Spezifität bezüglich Zielgruppe und Nutzen)

![Rotes Kreuz ausblenden](../../assets/do-not-localize/check-box-red.svg){width="20"} „Ereignis bewerben“ (keine klare Aktion, kein Wert oder keine Dringlichkeit)

#### Beispielaufforderungen nach Kanaltyp {#channel-type-practices}

<table style="table-layout: auto; border: 0;">
<thead>
<tr style="border: 0;background-color: #FFFFFF;">
<th>Kanal</th>
<th>Beispiel</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>E-Mail</strong></td>
<td>„Fördern Sie potenzielle Unternehmen, indem Sie drei Kundenerfolgsgeschichten mit detaillierten ROI-Metriken präsentieren (Oracle: 45 % Kostensenkung, Accenture: 200 % Lead-Steigerung, Microsoft: 60 % Zeitersparnis). Targeting von IT-Direktoren in Unternehmen mit mehr als 1000 Mitarbeitern“</td>
</tr>
<tr>
<td><strong>Landingpages</strong></td>
<td>„Konvertieren Sie B2B-Besucher in qualifizierte Leads, indem Sie demonstrieren, wie die Sicherheitslösung für Unternehmen 99,9 % der Cyber-Angriffe verhindert, mit Fortune 500-Erfahrungsberichten und kostenlosem Sicherheits-Audit.“</td>
</tr>
</tbody>
</table>

<!--
 channels not yet supported
<tr>
<td><strong>SMS</strong></td>
<td>"Alert VIP customers about a 4-hour flash sale on premium electronics with 40% discount, limited to the first 100 customers"</td>
</tr>
<tr>
<td><strong>Push Notifications</strong></td>
<td>"Re-engage users who haven't opened the app in 7 days with personalized content recommendations based on their reading history"</td>
</tr> 
-->

<!--
 Wait on more B2B specific examples

### Industry-specific approaches {#industry-approaches}

<table style="table-layout: fixed; border-collapse: collapse; border: 0;">
<thead>
<tr style="border: 0;background-color: #FFFFFF;">
<th>Industry</th>
<th>Example Prompt</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>B2B Technology</strong></td>
<td>"Demonstrate ROI and technical specifications while addressing security concerns for IT decision-makers evaluating our cloud infrastructure solution, emphasizing 99.9% uptime SLA, SOC 2 compliance, and 40% cost savings."</td>
</tr>
<tr>
<td><strong>E-commerce Retail</strong></td>
<td>"Create urgency around limited-stock holiday items while highlighting free shipping and easy returns for last-minute shoppers, emphasizing limited quantities (less than 50 remaining) and 24-hour shipping cutoff."</td>
</tr>
<tr>
<td><strong>Financial Services</strong></td>
<td>"Educate clients about investment portfolio diversification strategies while maintaining regulatory compliance, featuring certified financial advisor insights and risk disclaimers."</td>
</tr>
<tr>
<td><strong>Healthcare & Wellness</strong></td>
<td>"Promote preventive care benefits and annual health screenings while maintaining medical accuracy, featuring board-certified physician recommendations and patient privacy assurances."</td>
</tr>
<tr>
<td><strong>Education & Training</strong></td>
<td>"Emphasize career advancement outcomes and industry certifications while showcasing instructor expertise, highlighting 92% job placement rate and project-based curriculum."</td>
</tr>
<tr>
<td><strong>SaaS Platforms</strong></td>
<td>"Highlight time savings and automation benefits with specific metrics while addressing integration concerns, featuring average 25-hour weekly time savings and integration with 200+ popular tools."</td>
</tr>
</tbody>
</table>
 
-->

### Neue Inhalte vs. Änderung vorhandener Inhalte {#new-vs-modify}

Geben Sie klar an, ob Ihre Anfrage die Erstellung neuer Inhalte oder die Aktualisierung vorhandener Materialien beinhaltet. Diese Unterscheidung ist wichtig, da sie die KI bei der Auswahl des geeigneten Ansatzes anleitet und ein genaueres und hilfreicheres Ergebnis sicherstellt.

#### Erstellen neuer Inhalte

Wenden Sie diese Strategie an, wenn Sie Marketing-Kampagnen starten, neue Lösungen vorstellen oder eine aktualisierte/aktualisierte Kommunikation starten. Dadurch wird sichergestellt, dass Ihre Botschaft stark beginnt und mit Ihren Zielen übereinstimmt.

**So formulieren Sie Prompts** ➤ Konzentrieren Sie sich bei der Erstellung neuer Inhalte auf Ihr Marketing-Ziel, ohne auf vorhandene Inhalte zu verweisen.

>[!BEGINSHADEBOX „Beispiele“]

* **SaaS-Testversion**: „Launch der neuen CRM-Software für Inhaber kleiner Unternehmen, Hervorhebung von 50 % Zeitersparnis, 90 % schnellerer Lead-Qualifizierung und Angebot einer 30-tägigen kostenlosen Testversion mit personalisiertem Onboarding“
* **Funktionsankündigung**: „Kündige neue API-Integrationsfunktionen an, die die Entwicklungszeit für Unternehmenskunden um 60 % verkürzen und sich an technische Entscheidungstragende richten.“
* **Ereignisförderung**: „Fordern Sie Registrierungen für das Webinar „Digitale Marketing-Trends 2024“ an, in dem Experten aus Google, Meta und Adobe vertreten sind, wobei sie umsetzbare Einblicke und begrenzte Plätze (max. 500) betonen.“

>[!ENDSHADEBOX]

#### Ändern vorhandener Inhalte

>[!TIP]
>
>Bei Standardänderungen, wie z. B. „Aufbereiten“, „Zusammenfassen“ oder „Vereinfachen“, wählen Sie **_Verfeinern_** anstatt benutzerdefinierte Eingabeaufforderungen zu schreiben.

Verwenden Sie eine Änderungsaufforderung, wenn Sie Ihre aktuellen Marketing-Kampagnen aktualisieren, aktualisieren oder anpassen müssen. Diese Methode unterstützt inkrementelle Verbesserungen, um sicherzustellen, dass Ihr Messaging relevant bleibt, ohne dass Sie von Grund auf neu beginnen müssen.

**So formulieren Sie Prompts** ➤ Geben Sie beim Ändern vorhandener Inhalte klar an, was Sie ändern möchten und wie dies erfolgen soll.

>[!BEGINSHADEBOX „Beispiele“]

* **Kampagnenaktualisierung**: „Ändern Sie die E-Mail zum Programmstart, um sich auf Unternehmenssicherheitsfunktionen anstatt auf allgemeine Produktivitätsvorteile zu konzentrieren und IT-Entscheidungsträger mit Compliance-Zertifizierungen anzusprechen.“
* **Zielgruppen-Pivot**: „Passen Sie die Einladung zur Softwaredemo an, um das Gesundheitswesen gezielt anzusprechen, indem Sie allgemeine Beispiele durch Anwendungsfälle im Gesundheitswesen und HIPAA-Compliance-Vorteile ersetzen“
* **Saisonale Aktualisierung**: „Aktualisieren Sie die Werbekampagne für das 4. Quartal zum Weihnachtseinkauf, wobei der Fokus von der Schulaktivität auf die Geschenke für die Feiertage verlagert wird, wobei der Schwerpunkt auf schnellem Versand liegt.“

>[!ENDSHADEBOX]

## Erweiterte Texteinstellungen {#text-settings}

Neben der Verwendung einer klaren und wohlgeformten Eingabeaufforderung enthalten die Texteinstellungen in den Content-Tools des KI-Assistenten Texteinstellungen, mit denen Sie die generierten Ausgaben optimieren können.

>[!TIP]
>
>Verwenden Sie die Optionen _[!UICONTROL Kommunikationsstrategie]_ und _[!UICONTROL Ton]_ in den _[!UICONTROL Texteinstellungen]_ anstatt diese Merkmale in Ihrer Eingabeaufforderung zu erwähnen.

### Arten von Kommunikationsstrategie

Ihre Kommunikationsstrategie bestimmt, wie Sie Ihre Botschaft präsentieren, um die Wirkung zu maximieren. Je nach den Zielen eignen sich unterschiedliche Strategien besser, sei es beim Vermitteln von Dringlichkeit, beim Aufbau von Vertrauen oder beim Fördern sofortiger Handlungen. Wählen Sie die Strategie aus, die am besten zu Ihren Kampagnenzielen und zur Mentalität Ihrer Zielgruppe passt.

| **Strategie** | **Geeignet für** | **Nachrichtenstil** | **Beispiele** |
| ------------ | ------------ | ------------------- | ------------ |
| **Dringlich** | Zeitkritische Angebote, Fristen, sofortiges Handeln | Erstellt unmittelbaren Druck durch zeitbasierte Sprache | <li>„Jetzt handeln: Angebot läuft um Mitternacht ab“ <li>„Melden Sie sich noch heute an, bevor sich die Plätze füllen.“ <li>„Der 48-Stunden-Flash-Verkauf beginnt jetzt“ |
| **FOMO (Angst, etwas zu verpassen)** | Zeitlich begrenzte Angebote, Veranstaltungen, exklusiver Zugriff | Verwendet Signale, die Dringlichkeit, begrenzte Stückzahlen und Zeitdruck vermitteln | <li>„Nur noch 24 Stunden! Limitierte Lagerbestände mit 40% Rabatt“ <li>„Letzte Chance: Early Bird Preise enden morgen“ <li>„Nur noch 100 Beta-Spots“ |
| **Social Proof** | Vertrauensbildung, Erfahrungsberichte, beliebte Produkte | Nutzt die Erfahrungen und Bewertungen anderer Benutzerinnen und Benutzer | <li>„Nehmen Sie an mehr als 50.000 zufriedenen Kunden teil“ <li>„Bewertet mit 4,9/5 Sternen von Branchenexperten“ <li>„Vertrauenswürdig durch Fortune 500-Unternehmen“ |
| **Begrenzte Stückzahlen** | Begrenzter Bestand, exklusive Versionen, stark nachgefragte Artikel | Betont begrenzte Verfügbarkeit und Exklusivität | <li>„Nur noch 5 auf Lager“ <li>„Limitierte Auflage: 100 Stück verfügbar“ <li>„Exklusive Version: Wer zuerst kommt, mahlt zuerst“ |
| **Incentive** | Promotions, Prämienprogramme, Sonderangebote | Hebt konkrete Vorteile und Prämien hervor | <li>„Erhalten Sie 20 % Rabatt auf Ihre erste Bestellung“ <li>„An diesem Wochenende doppelte Punkte sammeln“ <li>„Kostenloser Versand bei Bestellungen über 50 $&quot; |
| **Exklusivität** | Premium-Produkte, VIP-Erlebnisse, Angebote nur für Mitglieder | Verwendet Premium-Positionierung und Sprache für speziellen Zugang | <li>„Exklusive Einladung zu einer privaten Vorschau“ <li>„Elite-Mitgliedschaft entsperrt erweiterte Analysen“ <li>„Werden Sie Mitglied bei ausgewählten Fortune 500-Unternehmen, die bereits mit uns arbeiten“ |
| **Gamification** | Interaktionskampagnen, Treueprogramme, interaktive Inhalte | Verwendet Spielmechanik und auf Erfolge bezogene Sprache | <li>„Entsperren Sie Ihre nächste Belohnungsstufe“ <li>„Challenges erledigen, um Abzeichen zu erwerben“ <li>„Besteige die Rangliste für exklusive Preise“ |
| **Information** | Bildung, Forschung, komplexe Produkte, Innovationen | Verwendet Fakten, Daten, Erkenntnisse und Erklärungen | <li>„5 Erkenntnisse aus der Analyse von über 10.000 Interaktionen“ <li>„Neue Forschung zeigt 3 bahnbrechende Ansätze“ <li>„Vollständige Anleitung zur Implementierung von KI im Marketing“ |
| **Bildung und Erkenntnisse** | Lerninhalte, Branchen-Trends, Best Practices | Bietet wertvolles Wissen und umsetzbare Erkenntnisse | <li>„Lernen Sie fortschrittliche Techniken mit einem Expertenführer kennen“ <li>„Entdecken Sie 7 Strategien, die Top-Marketing-Experten verwenden“ <li>„Erfahren Sie in fünf Schritten, wie Sie Ihren Workflow optimieren können“ |

### Festlegen des passenden Tons {#tone}

Der Ton bestimmt, wie Ihre Zielgruppe Ihre Nachricht wahrnimmt und darauf reagiert. Wählen Sie stets einen Ton aus, der zu Ihrer Markensprache und der Journey-Phase des Profils passt.

Überprüfen Sie die verfügbaren Ton-Optionen, einschließlich der besten Ergebnisse und Beispiele für Inhalte, die zu jedem Stil passen.

| Tonalität | Geeignet für | Inhaltsbeispiel |
| ---- | ----- | ----- |
| Professionell | B2B-Kommunikation, formelle Ankündigungen | „Wir freuen uns, unsere strategische Partnerschaft mit … bekannt geben zu können“ |
| Einfühlsam | Kunden-Support, sensible Themen | „Wir verstehen, wie frustrierend dieses Thema für Sie sein muss…“ |
| Humorvoll | Ansprechende Kampagnen, heitere Inhalte | „Warnung: Kann zu erheblichen Produktivitätssteigerungen führen!“ |
| Spannend | Produkteinführungen, Veranstaltungswerbung | „Das ist der Moment, auf den du gewartet hast!“ |
| Inspirierend | Motivationskampagnen, Markenzweck | „Gemeinsam können wir die Welt verändern …“ |
| Überzeugend | Verkaufskampagnen, Konversionen | „Verpassen Sie nicht diese befristete Gelegenheit, um …“ |
| Freundlich | Kundeninteraktion, Begrüßungsnachrichten | „Schön, dass du hier bei uns bist!“ |
| Förmlich | Rechtliche Kommunikation, amtliche Mitteilungen | „Dies ist eine Benachrichtigung über die folgenden Änderungen…“ |
| Entschuldigend | Service-Wiederherstellung, Problembehebung | „Bodea entschuldigt sich aufrichtig für jegliche Unannehmlichkeiten…“ |
| Bestimmt | Inhalt für Führungskräfte, verbindliches Messaging | „Das müssen Sie jetzt tun …“ |
| Storytelling | Markenerzählungen, emotionale Verknüpfungen | „Alles fing mit einer einfachen Frage an …“ |
| Dialogorientiert | Nurturing-Kampagnen, Aufbau von Beziehungen | „Sprechen wir darüber, wie dieses Programm Ihnen helfen kann…“ |

## Optimierter Referenzinhalt {#reference-content}

>[!TIP]
>
>Wenn Sie ein Asset bereits über das Menü **[!UICONTROL Referenzinhalt]** hochgeladen haben, müssen Sie in der Eingabeaufforderung nicht darauf verweisen. Das System verwendet automatisch alle ausgewählten Dokumente.

Referenzinhaltsdateien enthalten Fakten, die Ihre generierten Inhalte mit spezifischen, präzisen Details anreichern. Wenn Sie Dokumente wie Produktbroschüren oder Whitepapers hochladen, ändern Sie die Eingabeaufforderung, um anzugeben, welche Teile im Fokus sind:

* **Anstelle von** _„Verwende die Produktbroschüre“_ **sollten Sie** _„Lege den Fokus auf die erweiterten Sicherheitsfunktionen und Compliance-Zertifizierungen, insbesondere auf die SOC 2-Konformität und die Datenverschlüsselung“_ verwenden

* **Anstelle von** _„Verweise auf die Fallstudien“_ **sollten Sie** _„Hebe die ROI-Ergebnisse von Kundinnen und Kunden im Gesundheitswesen hervor, insbesondere die Kostenreduzierung um 40 % im regionalen Medizinzentrum“_ verwenden

* **Anstelle von** _„Beziehe technische Details ein“_ **sollten Sie** _„Betone die API-Integrationsfunktionen und die Entwicklervorteile und lege den Fokus auf REST-API-Endpunkte und den SLA-Wert von 99,9 %&quot;_ verwenden

### Inhaltsverfeinerung

Nachdem der Inhalt generiert wurde, verwenden Sie die Funktion **_[!UICONTROL Verfeinern]_** , um ihn zu iterieren und mit den folgenden Optionen zu erweitern:

* **[!UICONTROL Entwickeln]** - Der KI-Assistent kann Ihnen dabei helfen, bestimmte Themen zu vertiefen und zusätzliche Details bereitzustellen, um das Verständnis und die Interaktion zu verbessern.

* **[!UICONTROL Zusammenfassen]** - Lange Informationen können Seitenbetrachter überlasten. Nutzen Sie den KI-Assistenten, um die wichtigsten Punkte in klaren, prägnanten Aussagen zusammenzufassen, die die Aufmerksamkeit der Leserinnen und Leser wecken und sie zum Weiterlesen anregen.

* **[!UICONTROL Umformulieren]** - Die Nachricht wird neu geschrieben, wobei ihre Bedeutung erhalten bleibt. Mit dieser Option können Sie alternative Formulierungen generieren, den Lesefluss verbessern oder die Ausdrucksweise anpassen, ohne die Kernbotschaft zu ändern.

* **[!UICONTROL Einfachere Sprache verwenden]** - Vereinfachen Sie die Sprache, indem Sie für ein breiteres Publikum Klarheit und Barrierefreiheit gewährleisten.

* **[!UICONTROL Übersetzen]** - Übersetzen Sie den Text in eine andere Sprache. (Derzeit wird nur Englisch unterstützt.)

* **[!UICONTROL Ton ändern]** - Passen Sie den Ton der Nachricht an Ihren Kommunikationsstil an, z. B. freundlicher, professioneller, dringender oder inspirierender.

* **[!UICONTROL Kommunikationsstrategie ändern]** - Ändern Sie den Messaging-Ansatz basierend auf Ihren Zielen, z. B. der Schaffung von Dringlichkeit oder der Betonung aufregender Attraktivität.
