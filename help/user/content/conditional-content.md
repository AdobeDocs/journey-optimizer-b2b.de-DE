---
title: Bedingter Inhalt
description: Erfahren Sie, wie Sie Inhaltsvarianten erstellen und bedingte Regeln anwenden, wenn Sie E-Mail-Inhalte für Account-Journey erstellen.
feature: Email Authoring, Content
exl-id: 7a789412-ea52-482f-8dc9-4a1599e85268
source-git-commit: 60fa6211666d1602dcd358ffc5ffc39caaf5475a
workflow-type: tm+mt
source-wordcount: '1347'
ht-degree: 13%

---

# Bedingter Inhalt

Bedingter Inhalt ermöglicht die Anpassung von E-Mail-Inhalten auf der Grundlage von bedingten Regeln. Diese Regeln werden mithilfe von Profilattributen oder kontextuellen Ereignissen definiert. Sie können im Regel-Builder bedingte Regeln erstellen und diese zur Wiederverwendung in Ihren Account-Journey speichern.

Um bedingte Inhalte in Ihre E-Mail-Nachrichten einzufügen, können Sie mit Adobe Journey Optimizer bedingte Regeln anwenden, die in der Bibliothek _Bedingungen_ gespeichert sind. Wenden Sie bedingte Regeln im E-Mail-Design an, während Sie [eine E-Mail in einer Konto-Journey erstellen](./email-authoring.md).

## Hinzufügen von bedingten Inhalten zu E-Mails {#email-content}

>[!CONTEXTUALHELP]
>id="ajo-b2b_conditional_content"
>title="Bedingter Inhalt"
>abstract="Verwenden Sie bedingte Regeln, um mehrere Varianten einer Inhaltskomponente zu erstellen. Wenn beim Senden der Nachricht keine der Bedingungen erfüllt ist, wird der Inhalt der Standardvariante angezeigt."

>[!CONTEXTUALHELP]
>id="ajo-b2b_conditional_rule_select"
>title="Bedingter Inhalt"
>abstract="Verwenden Sie eine in der Bibliothek gespeicherte bedingte Regel oder erstellen Sie eine neue."

Verwenden Sie beim Erstellen einer E-Mail für Ihr Account-Journey im E-Mail-Design bedingte Regeln, um mehrere Varianten für eine Inhaltskomponente zu definieren.

1. Wählen Sie eine Inhaltskomponente aus und klicken Sie auf das Symbol **[!UICONTROL Bedingten Inhalt aktivieren]** in der Komponenten-Symbolleiste.

   Die Komponente ist orange umrandet, um anzugeben, dass sie als bedingte Komponente aktiviert ist. Der Bereich **[!UICONTROL Bedingter Inhalt]** wird auf der linken Seite mit den _Standardvariante_ und _Variante - 1 angezeigt.

   ![Bedingten Inhalt für die Textkomponente aktivieren](./assets/conditions-enable.png){width="700" zoomable="yes"}{width=„700“ zoomable=„yes“}

   Der ausgewählte und aktivierte Originalinhalt ist die Standardeinstellung und wird angewendet, wenn keine der bedingten Regeln für eine der von Ihnen definierten Varianten erfüllt ist.

   In diesem Bereich können Sie mithilfe von bedingten Regeln mehrere Varianten für die ausgewählte Inhaltskomponente definieren.

1. Bewegen Sie den Mauszeiger über die erste Variante (_Variante - 1_) und klicken Sie auf das _Bedingung auswählen_-Symbol ( ![Bedingungssymbol](../assets/do-not-localize/icon-select-condition.svg) ).

   ![Bedingung für Variante auswählen](./assets/conditions-variant-select.png){width="700" zoomable="yes"}{width=„700“ zoomable=„yes“}

   Das _[!UICONTROL Bedingung auswählen]_ Dialogfeld wird geöffnet und die Bedingungsbibliothek wird angezeigt.

   Wenn Sie Details zu einer Bedingung anzeigen möchten, um sicherzustellen, dass sie korrekt ist, klicken Sie auf das _Mehr Menü_-Symbol (**…**) und wählen Sie **[!UICONTROL Info anzeigen]**.

   ![Details zu Bedingungen für den Zugriff auf die ](assets/conditions-select-dialog.png){width="600" zoomable="yes"}{width=„600“ zoomable=„yes“}

   Wenn die benötigte Bedingung nicht vorhanden ist, erstellen [ eine bedingte Regel, ](#create-a-conditional-rule) Sie auf **[!UICONTROL Neu erstellen]**.

1. Wählen Sie die bedingte Regel aus und klicken Sie auf **[!UICONTROL Auswählen]**, um sie mit der Variante zu verknüpfen.

   Sie können die zugehörige Bedingung überprüfen, indem Sie auf das Symbol _Mehr Menü_ (**…**) für die Variante klicken und **[!UICONTROL Bedingung anzeigen]** auswählen.

   ![Die mit der Variante verknüpfte Bedingung anzeigen](./assets/conditions-variant-view-condition.png){width="600" zoomable="yes"}{width=„600“ zoomable=„yes“}

   Klicken Sie oben rechts auf X , um das Popup zu schließen.

   ![Details für die zugehörige Bedingung anzeigen](./assets/conditions-info-popup.png){width="500"}{width=„500“}

1. Um die Lesbarkeit zu verbessern, benennen Sie die Variante um, indem Sie auf das _Mehr Menü_-Symbol (**…**) für die Variante klicken und **[!UICONTROL Umbenennen]** auswählen.

   Geben Sie einen aussagekräftigen Namen für die Variante ein, der Ihnen bei der Identifizierung der Variante und ihrer Absicht hilft.

   ![Umbenennen der Variante](./assets/conditions-variant-rename.png){width="600" zoomable="yes"}{width=„600“ zoomable=„yes“}

1. Wenn die Variante im linken Bereich ausgewählt ist, ändern Sie die Komponente, um zu ändern, wie sie in der E-Mail-Nachricht angezeigt wird, wenn die Bedingung erfüllt ist.

   In diesem Beispiel verwendet die Variante für die Textkomponente eine andere Beschreibung, die auf der Region des Empfängers basiert.

   ![Ändern der Komponente für die Variante](./assets/conditions-variant-component-edit.png){width="600" zoomable="yes"}{width=„600“ zoomable=„yes“}

1. Definieren Sie bei Bedarf eine andere Variante, indem Sie auf **[!UICONTROL Variante hinzufügen]** klicken.

   Wiederholen Sie die Schritte 2-5, um eine Bedingung auszuwählen, die Variante umzubenennen und die Komponente für die Variante zu ändern.

   Sie können so viele Varianten hinzufügen, wie für die Inhaltskomponente erforderlich sind. Sie können die ausgewählte Variante jederzeit im linken Bereich ändern, um zu überprüfen, wie die Inhaltskomponente für die Bedingung angezeigt wird.

   >[!IMPORTANT]
   >
   >Bedingte Inhalte werden anhand der zugehörigen Regeln in der Reihenfolge ausgewertet, in der die Varianten aufgelistet sind. Die erste Variante mit einer Bedingung, die als „true“ ausgewertet wird, wird für die Komponente verwendet.
   >
   >Wenn keine der definierten Variantenbedingungen beim Senden der E-Mail als „true“ ausgewertet wird, wird die Inhaltskomponente gemäß der **[!UICONTROL Standardvariante]** angezeigt.

1. Um eine Variante zu löschen, klicken Sie auf das _Mehr Menü_-Symbol (**…**) für die Variante und wählen Sie **[!UICONTROL Löschen]**.

   Klicken **[!UICONTROL im]** auf „Löschen“.

## Bedingte Regeln

Bedingte Regeln sind ein Satz bedingter Ausdrücke, die als „true“ oder „false“ ausgewertet werden können. Sie können diese Regeln verwenden, um auf der Grundlage verschiedener Filter, wie Profilattribute oder kontextuelle Ereignisse, zu bestimmen, welche Inhaltsvariante in einer E-Mail-Nachricht angezeigt werden soll.

Bedingte Regeln werden in der Bedingungsbibliothek gespeichert, wo sie für die Wiederverwendung über Journey-Inhalte für Ihr Unternehmen hinweg verfügbar sind.
<!-- 

>[!NOTE]
>
>You need the [Manage Library Items](../administration/ootb-product-profiles.md) permission to save or delete conditional rules. Saved conditions are available for use by all users within an organization. -->

### Bedingungsfilter {#condition-filters}

| Bedingungstyp | Filter | Beschreibung |
| -------------- | ------- | ----------- |
| **Konto** | Kontoattribute | Attribute aus dem Kontoprofil, einschließlich: <li>Jahresumsatz</li><li>Stadt</li><li>Land</li><li>Mitarbeiterzahl</li><li>Branche</li><li>Name</li><li>SIC-Code</li><li>Land</li> |
| | [!UICONTROL Sonderfilter] > [!UICONTROL Hat Einkaufsgruppe] | Das Konto hat keine Mitglieder von Einkaufsgruppen. Kann auch anhand eines oder mehrerer der folgenden Kriterien bewertet werden: <li>Interesse an der Lösung</li><li>Einkaufsgruppenstatus</li><li>Vollständigkeitsindex</li><li>Interaktionsbewertung</li> |
| | [!UICONTROL Spezialfilter] > [!UICONTROL Hat Gelegenheit] | Das Konto ist oder ist nicht mit einer Opportunity verbunden. Kann auch anhand eines oder mehrerer der folgenden Opportunity-Attribute ausgewertet werden: <li>Betrag<li>Abschlussdatum<li>Beschreibung<li>Erwarteter Umsatz<li>Geschäftsquartal<li>Geschäftsjahr<li>Prognosekategorie<li>Prognosekategoriename<li>Ist geschlossen<li>Wurde gewonnen</li><li>Datum der letzten Aktivität</li><li>Personenquelle<li>Name</li><li>Nächster Schritt</li><li>Wahrscheinlichkeit<li>Menge<li>Phase</li><li>Typ |
| **Person** | [!UICONTROL Aktivitätsverlauf] > [!UICONTROL E-Mail] | Mit der Journey verbundene E-Mail-Aktivitäten: <li>[!UICONTROL Link in E-Mail angeklickt]</li><li>Geöffnete E-Mail</li><li>Bekam E-Mail zugestellt</li><li>Bekam E-Mail zugesendet</li> Diese Bedingungen werden mithilfe einer ausgewählten E-Mail-Nachricht aus einem früheren Abschnitt der Journey ausgewertet. |
|  | [!UICONTROL Personenattribute] | Attribute aus dem Personenprofil, einschließlich: <li>Stadt</li><li>Land</li><li>Geburtsdatum</li><li>E-Mail-Adresse</li><li>E-Mail-Adresse ungültig</li><li>E-Mail angehalten</li><li>Vorname</li><li>Abgeleitetes Bundesland/abgeleitete Region</li><li>Stellenbezeichnung</li><li>Last name</li><li>Mobiltelefonnummer</li><li>Telefonnummer</li><li>Postleitzahl</li><li>Land</li><li>Abbestellt</li><li>Grund für Abmeldung</li> |
| | [!UICONTROL Sonderfilter] > [!UICONTROL Mitglied der Einkaufsgruppe] | Die Person ist oder ist kein Kauf-Gruppenmitglied, das anhand eines oder mehrerer der folgenden Kriterien bewertet wird: <li>Interesse an der Lösung</li><li>Einkaufsgruppenstatus</li><li>Vollständigkeitsindex</li><li>Interaktionsbewertung</li><li>Role</li> |

<!-- 

| | [!UICONTROL Activity history] > [!UICONTROL Data Value Changed] | For a selected person attribute, a value change occurred. These change types include: <li>New value</li><li>Previous value</li><li>Reason</li><li>Source</li><li>Date of activity</li><li>Min. number of times</li> |
| | [!UICONTROL Activity history] > [!UICONTROL Had Interesting Moment] | Interesting moment activity that is defined in the associated Marketo Engage instance. Constraints include: <li>Milestone</li><li>Email</li><li>Web</li>|

| | [!UICONTROL Special filters] > [!UICONTROL Member of List] | The person is or is not a member of one or more Marketo Engage lists. |
| | [!UICONTROL Special filters] > [!UICONTROL Member of Program] | The person is or is not a member of one or more Marketo Engage programs. |
|  [People](#add-a-split-path-by-people-node) > [!UICONTROL Account-person attributes only] | Role in account attributes | The person is or is not assigned a role in the account. Optional constraints: <li>Enter a role name</li> | 
-->

### Erstellen einer bedingten Regel {#create-condition}

>[!CONTEXTUALHELP]
>id="ajo-b2b_conditions_rule_editor"
>title="Erstellen einer Bedingung"
>abstract="Kombinieren Sie Attribute und kontextbezogene Ereignisse, um Regeln zu erstellen, die bestimmen, welche Inhaltsvariante in E-Mail-Nachrichten angezeigt werden soll."

Sie können über den E-Mail-Design-Bereich auf den Builder für bedingte Regeln zugreifen, wenn Sie eine Bedingung für eine Komponentenvariante auswählen.

1. Klicken Sie _[!UICONTROL Dialogfeld]_ Bedingung auswählen“ auf **[!UICONTROL Neu erstellen]** und wählen Sie den Bedingungstyp aus:

   * **[!UICONTROL Personenbedingung]** Wählen Sie diesen Typ aus, um die bedingte Regel mithilfe von Personenattributen und kontextuellen Ereignissen zu erstellen.
   * **[!UICONTROL Kontobedingung]** - Wählen Sie diesen Typ aus, um die bedingte Regel mithilfe von Kontoattributen zu erstellen.

   ![Zu erstellenden Bedingungstyp auswählen](./assets/conditions-select-create-new.png){width="600" zoomable="yes"}{width=„600“ zoomable=„yes“}

1. Erstellen Sie die bedingte Regel entsprechend Ihren Anforderungen.

   Ziehen Sie für jedes Attribut oder Ereignis, das Sie in die Regel aufnehmen möchten, das Element per Drag-and-Drop auf die Arbeitsfläche der Regel. Erweitern Sie den Filter und vervollständigen Sie den Ausdruck.

   ![Vervollständigen Sie den auszuwertenden Ausdruck](./assets/conditions-rule-add-attribute.png){width="600" zoomable="yes"}{width=„600“ zoomable=„yes“}

   Wenn Sie mehr als einen Filter einbeziehen, legen Sie die **[!UICONTROL Filterlogik]** fest:

   * **[!UICONTROL Alle Filter anwenden]** - Die Regel wird als „true“ ausgewertet, wenn **alle** Filter „true“ sind.
   * **[!UICONTROL Alle Filter anwenden]** - Die Regel wird als „true“ ausgewertet, wenn **einer** der Filter „true“ ist.

1. Geben Sie rechts den **[!UICONTROL Namen]** und eine **[!UICONTROL Beschreibung]** (optional) für die Regel ein.

   Verwenden Sie einen aussagekräftigen Namen und eine nützliche Beschreibung, um anderen in Ihrer Organisation zu helfen, damit sie ihn wiederverwenden können, anstatt eine weitere doppelte Bedingung zu erstellen.

   ![Fügen Sie einen Namen und eine Beschreibung für die bedingte Regel hinzu](./assets/conditions-rule-name-description.png){width="600" zoomable="yes"}{width=„600“ zoomable=„yes“}

1. Wenn Ihre bedingte Regel abgeschlossen ist, klicken Sie auf **[!UICONTROL Speichern]**.

   Die bedingte Regel wird in der Bibliothek gespeichert und kann für die aktuelle Variante ausgewählt werden. Es ist auch in der -Bibliothek enthalten, damit es von allen anderen Varianten dynamischer Inhalte in Account-Journey verwendet werden kann.

### Duplizieren einer Regel

In der Bibliothek gespeicherte bedingte Regeln können nicht geändert werden. Sie können jedoch eine vorhandene Regel duplizieren und ändern, um eine neue Regel zu erstellen.

1. Klicken Sie auf das _Mehr Menü_-Symbol (**…**) für die Variante und wählen Sie **[!UICONTROL Duplizieren]**.

   Ein Duplikat der Regel wird im Regel-Builder geöffnet. Verwenden Sie das Duplikat als Ausgangspunkt für die Regel, die Sie erstellen möchten.

   ![Verwenden Sie eine doppelte Regel, um die gewünschte Regel zu erstellen](./assets/conditions-rule-duplicate.png){width="600" zoomable="yes"}{width=„600“ zoomable=„yes“}

1. Ändern Sie im Regel-Builder Bedingungen entsprechend Ihren Anforderungen, fügen Sie sie hinzu oder löschen Sie sie.

1. Ändern Sie den Namen und die Beschreibung entsprechend dem Zweck oder den Elementen in der Regel.

1. Wenn Ihre bedingte Regel abgeschlossen ist, klicken Sie auf **[!UICONTROL Speichern]**.
