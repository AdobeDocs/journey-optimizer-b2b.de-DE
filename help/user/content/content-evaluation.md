---
title: Bewertung und Bewertung von Inhalten
description: Bewerten von E-Mail-Inhalten mit Bewertung der Markenausrichtung - Validieren Sie Farben, Schriftarten, Logos und den Schreibstil anhand der Markenrichtlinien in Journey Optimizer B2B edition.
badge: label="Beta" type="Informative"
feature: Content, Brand Identity
role: User
level: Beginner, Intermediate
exl-id: 686d5ce0-c597-48e1-a51f-e91e95a942d5
source-git-commit: bbdbf74b2fb0003b84ed4d7f84dce9aa3b796aea
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 9%

---

# Bewertung und Bewertung von Inhalten {#content-scoring}

Die Inhaltsauswertung und -bewertung helfen Ihnen bei der Erstellung, Überprüfung und Verwaltung von Inhalten, die den Richtlinien [in der ausgewählten Marke definiert](./brands-manage-create.md#brand-definitions) und den allgemeinen Qualitätsstandards entsprechen. Die Durchführung einer Evaluierung gewährleistet die Konsistenz in Ton, Messaging und visueller Identität in Ihren E-Mail-Kampagnen und dient gleichzeitig als Qualitätsprüfung vor der Live-Schaltung Ihres Inhalts.

>[!AVAILABILITY]
>
>Eine [Benutzervereinbarung](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"} ist erforderlich, bevor Sie KI-gestützte Funktionen in Adobe Journey Optimizer B2B edition verwenden können. Weitere Informationen erhalten Sie beim Adobe-Support.
>
>Unter [Markenbezogene Berechtigungen](./brands-overview.md#brand-related-permissions) finden Sie Informationen darüber, wie Produktadministratoren diese Funktionen aktivieren können.

## Ausführen einer Evaluierung

1. Nachdem Sie den E-Mail-Inhalt erstellt haben, klicken Sie auf das Symbol _Markenausrichtung_ ( ![Markenausrichtungssymbol](../assets/do-not-localize/icon-brand-compliance.svg) ) auf der rechten Seite, um das rechte Bedienfeld _Markenausrichtung_ im E-Mail-Design zu öffnen.

   Die [Standardmarke](./brands-manage-create.md#default-brand) wird automatisch ausgewählt.

   ![Zugriff auf die Tools zur Markenausrichtung](./assets/brands-alignment-sidebar.png){width="600" zoomable="yes"}

   Sie können auf das Symbol _Vollbild_ ( ![Vollbildsymbol](../assets/do-not-localize/icon-full-screen.svg) ) oben im Bedienfeld klicken, um die Tools für die Markenausrichtung im Vollbildmodus anzuzeigen.

1. Klicken Sie bei Bedarf auf den Menüpfeil **[!UICONTROL Marke]** ( ![Nach-unten-](../assets/do-not-localize/icon-down-menu.svg) ), um eine andere veröffentlichte Marke auszuwählen.

1. Klicken Sie **[!UICONTROL Bewertung auswerten]**, um die Ausrichtung des Inhalts an der ausgewählten Marke zu bewerten.

   Das System bewertet den Inhalt anhand der Richtlinien für die ausgewählte Marke und zeigt die daraus resultierende Bewertung an.

   ![Auswertungswerte im rechten Bedienfeld](./assets/brands-alignment-evaluation.png){width="600" zoomable="yes"}

## Markenausrichtungswert {#brand-alignment-score}

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_score_overview"
>title="Markenauswahl"
>abstract="Wählen Sie Ihre Marke aus, um sicherzustellen, dass Ihre Inhalte in Übereinstimmung mit den spezifischen Richtlinien, Standards und der Markenidentität erstellt werden und die Konsistenz und Markenintegrität gewahrt bleiben."

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_score"
>title="Markenausrichtungswert"
>abstract="Die Bewertung Ihrer Markenausrichtung misst, wie gut Ihr Inhalt den Markenrichtlinien entspricht, um Konsistenz in Farben, Schriftarten, Logo, Bildern und Schreibstil sicherzustellen."

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_colors_score"
>title="Farbwert"
>abstract="Farbwert"

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_fonts_score"
>title="Schriftartenwert"
>abstract="Schriftartenwert"

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_logos_score"
>title="Logowert"
>abstract="Logowert"

>[!AVAILABILITY]
>
>Diese Funktion ist derzeit als öffentliche Betaversion verfügbar.

Wenn Ihre Marke klar definiert und veröffentlicht ist, bewerten Sie Ihre Markenausrichtung direkt im E-Mail-Design-Bereich, um sicherzustellen, dass der Inhalt mit Ihren Markenrichtlinien übereinstimmt:

Die Punktzahl wird anhand der festgestellten Verstöße im ausgewerteten E-Mail-Inhalt berechnet:

* 100 = Perfekt - Keine Verstöße gefunden
* 80-99 = Gut - nur geringfügige Verstöße
* 60-79 = Fair - Einige bedeutende Verstöße
* Unter 60 = Schlecht - Schwere Verletzungen erfordern Aufmerksamkeit

Sie können die Auswertungsergebnisse detaillierter überprüfen, um Verstöße zu identifizieren und Ihre Kategorieausrichtungswerte zu verbessern (_Hoch_, _Medium_ und _Niedrig_).

Klicken Sie für **[!UICONTROL Schreibstil]** oder **[!UICONTROL visueller Inhalt]** auf den _Erweitern_ ( ![Erweiterungspfeil](../assets/do-not-localize/icon-expand-right.svg) ), um die Details für die Auswertung anzuzeigen.

![Details zur Markenausrichtung](./assets/brands-alignment-evaluation-details.png){width="600" zoomable="yes"}

Klicken Sie auf _Vollbildsymbol_ ( ![Vollbildsymbol für detaillierte Einblicke](../assets/do-not-localize/icon-full-screen.svg) ), um eine detaillierte Ansicht der einzelnen insight-Bewertungen zu erhalten.

Wählen Sie eine gekennzeichnete Richtlinie aus, um spezifisches Feedback und Vorschläge anzuzeigen.

![Auswertungsdetails zur Markenausrichtung in der Vollbildansicht](./assets/brands-alignment-evaluation-details-full-screen.png){width="700" zoomable="yes"}

Sie können Änderungen am Inhalt vornehmen und auf **[!UICONTROL Punktzahl neu auswerten]** klicken, um eine weitere Auswertung durchzuführen und nach einem verbesserten Ergebnis zu suchen.

## Bewertung der Inhaltsqualität {#quality-score}

>[!CONTEXTUALHELP]
>id="ajo-b2b_quality_score_overview"
>title="Qualität der Inhalte"
>abstract="Bewertung der allgemeinen Inhaltsqualität zur Identifizierung potenzieller Probleme mit Lesbarkeit, Inhaltskohärenz und Effektivität. Die Qualitätsbewertung ist unabhängig von Ihren Markenrichtlinien."

>[!NOTE]
>
>Die Bewertung der Inhaltsqualität ist unabhängig von den Markenrichtlinien. Auch wenn eine Marke ausgewählt wird, werden ihre Richtlinien nicht auf die Qualitätsprüfung angewendet. Die Markenauswahl ist nur für die Bewertung der Markenausrichtung relevant.

Zusätzlich zur Markenausrichtung können Sie die allgemeine Inhaltsqualität bewerten, um potenzielle Probleme mit Lesbarkeit, Inhaltskohärenz und Effektivität zu identifizieren, unabhängig von Ihren Markenrichtlinien.

Scrollen Sie zum Abschnitt **[!UICONTROL Inhaltsqualität]**, um die Qualitätseinblicke und Empfehlungen anzuzeigen.

![Bewertung der Inhaltsqualität](./assets/content-scoring-quality-insights.png){width="600" zoomable="yes"}

Wählen Sie ein markiertes Element aus, um spezifisches Feedback und umsetzbare Verbesserungsvorschläge anzuzeigen. Die Bewertungen basieren auf den folgenden Kategorien:

* **[!UICONTROL Effektivität von CTA]**: Wertet aus, wie gut Ihr call-to-action Ihre Leser dazu motiviert, die gewünschte Aktion durchzuführen.
* **[!UICONTROL Betreffzeile]**: Bewertet Klarheit, Relevanz und Aufmerksamkeit erregende Qualität, um E-Mail-Öffnungen zu fördern.
* **[!UICONTROL Lesbarkeit]**: Misst, wie einfach und ansprechend Ihre Inhalte für Leser sind.
* **[!UICONTROL Spam-Prüfung]**: Identifiziert gängige Spam-Trigger, die die Zustellbarkeit beeinträchtigen können.
* **[!UICONTROL Inhaltskohärenz]**: Stellt sicher, dass Ihre Inhalte reibungslos fließen und auf dem Thema bleiben.
* **[!UICONTROL Korrekturlesen]**: Überprüft Rechtschreibung, Grammatik und Klarheit.

Klicken Sie auf _Vollbildsymbol_ ( ![Vollbildsymbol für detaillierte Einblicke](../assets/do-not-localize/icon-full-screen.svg) ), um eine detaillierte Ansicht Ihrer Qualitätsbewertung zu erhalten.

![Vollbildansicht der Bewertung der Inhaltsqualität](./assets/content-scoring-quality-full-screen.png){width="700" zoomable="yes"}

Basierend auf den Empfehlungen können Sie Ihre Inhalte bearbeiten, um die Lesbarkeit, die Inhaltskohärenz und die Gesamtqualität zu verbessern. Klicken Sie **[!UICONTROL Bewertung erneut bewerten]**, nachdem Sie Änderungen vorgenommen haben, um den Qualitätswert zu aktualisieren.
