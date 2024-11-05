---
title: Bedingter Inhalt
description: Erfahren Sie, wie Sie Inhaltsvarianten erstellen und bedingte Regeln anwenden, wenn Sie E-Mail-Inhalte für Konto-Journey erstellen.
feature: Email Authoring, Content
source-git-commit: 15a5144554f25634efa29efc42d41350b19c2bfb
workflow-type: tm+mt
source-wordcount: '1071'
ht-degree: 4%

---

# Bedingter Inhalt

Bedingter Inhalt ermöglicht es Ihnen, E-Mail-Inhalte auf der Grundlage von bedingten Regeln anzupassen. Diese Regeln werden mithilfe von Profilattributen oder kontextbezogenen Ereignissen definiert. Sie können bedingte Regeln im Regel-Builder erstellen und sie zur Wiederverwendung in Ihren Konto-Journey speichern.

Um bedingte Inhalte zu Ihren E-Mail-Nachrichten hinzuzufügen, können Sie in Adobe Journey Optimizer Bedingungsregeln anwenden, die in der Bibliothek _Bedingungen_ gespeichert sind. Wenden Sie bedingte Regeln im E-Mail-Designer an, während Sie [eine E-Mail in einem Konto-Journey erstellen](./email-authoring.md).

## Bedingten Inhalt zu E-Mails hinzufügen {#email-content}

>[!CONTEXTUALHELP]
>id="ajo-b2b_conditional_content"
>title="Bedingter Inhalt"
>abstract="Verwenden Sie bedingte Regeln, um mehrere Varianten einer Inhaltskomponente zu erstellen. Wenn beim Versand der Nachricht keine der Bedingungen erfüllt ist, wird der Inhalt der Standardvariante angezeigt."

>[!CONTEXTUALHELP]
>id="ajo-b2b_conditional_rule_select"
>title="Bedingter Inhalt"
>abstract="Verwenden Sie eine in der Bibliothek gespeicherte bedingte Regel oder erstellen Sie eine neue."

Wenn Sie eine E-Mail für Ihre Konto-Journey im E-Mail-Designer erstellen, verwenden Sie Bedingungsregeln, um mehrere Varianten für eine Inhaltskomponente zu definieren.

1. Wählen Sie eine Inhaltskomponente aus und klicken Sie in der Komponenten-Symbolleiste auf das Symbol **[!UICONTROL Bedingten Inhalt aktivieren]** .

   Die Komponente ist orange dargestellt, um anzugeben, dass sie als bedingte Komponente aktiviert ist. Der Bereich **[!UICONTROL Bedingter Inhalt]** wird links mit der Variante _Standard_ und _Variante - 1 angezeigt.

   ![Bedingten Inhalt für die Textkomponente aktivieren](./assets/conditions-enable.png){width="700" zoomable="yes"}

   Der ausgewählte und aktivierte Originalinhalt wird standardmäßig verwendet, wenn keine der bedingten Regeln für die von Ihnen definierten Varianten erfüllt ist.

   In diesem Bereich können Sie mithilfe von Bedingungsregeln mehrere Varianten für die ausgewählte Inhaltskomponente definieren.

1. Bewegen Sie den Mauszeiger über die erste Variante (_Variante - 1_) und klicken Sie auf das Symbol _Bedingung auswählen_ ( ![Bedingungssymbol](../assets/do-not-localize/icon-select-condition.svg) ).

   ![Bedingung für Variante auswählen](./assets/conditions-variant-select.png){width="700" zoomable="yes"}

   Das Dialogfeld _[!UICONTROL Bedingung auswählen]_ wird geöffnet und die Bedingungsbibliothek wird angezeigt.

   Wenn Sie Details für eine Bedingung anzeigen möchten, um sicherzustellen, dass sie das ist, was Sie möchten, klicken Sie auf das Symbol _Mehr Menü_ (**...**) und wählen Sie **[!UICONTROL Informationen anzeigen]**.

   ![Details der Zugriffsbedingung für die Bibliothek für Bedingungen](assets/conditions-select-dialog.png){width="600" zoomable="yes"}

   Wenn die benötigte Bedingung nicht vorhanden ist, erstellen Sie [eine bedingte Regel](#create-a-conditional-rule), indem Sie auf **[!UICONTROL Neu erstellen]** klicken.

1. Wählen Sie die bedingte Regel aus und klicken Sie auf **[!UICONTROL Auswählen]** , um sie mit der Variante zu verknüpfen.

   Sie können die zugehörige Bedingung überprüfen, indem Sie auf das Symbol _Mehr Menü_ (**...**) für die Variante klicken und **[!UICONTROL Bedingung anzeigen]** auswählen.

   ![Anzeigen der mit der Variante verknüpften Bedingung](./assets/conditions-variant-view-condition.png){width="600" zoomable="yes"}

   Klicken Sie oben rechts auf X , um das Popup zu schließen.

   ![Details für die zugehörige Bedingung anzeigen](./assets/conditions-info-popup.png){width="500"}

1. Um die Lesbarkeit zu verbessern, benennen Sie die Variante um, indem Sie auf das Symbol _Mehr Menü_ (**..**) für die Variante klicken und **[!UICONTROL Umbenennen]** auswählen.

   Geben Sie einen aussagekräftigen Namen für die Variante ein, anhand dessen Sie die Variante und ihre Absicht identifizieren können.

   ![Umbenennen der Variante](./assets/conditions-variant-rename.png){width="600" zoomable="yes"}

1. Wenn die Variante im linken Bereich ausgewählt ist, ändern Sie die Komponente, um zu ändern, wie sie in der E-Mail-Nachricht angezeigt wird, wenn die Bedingung wahr ist.

   In diesem Beispiel verwendet die Variante für die Textkomponente eine andere Beschreibung, die auf der Region des Empfängers basiert.

   ![Ändern der Komponente für die Variante](./assets/conditions-variant-component-edit.png){width="600" zoomable="yes"}

1. Definieren Sie bei Bedarf eine weitere Variante, indem Sie auf **[!UICONTROL Variante hinzufügen]** klicken.

   Wiederholen Sie die Schritte 2 bis 5, um eine Bedingung auszuwählen, die Variante umzubenennen und die Komponente für die Variante zu ändern.

   Sie können so viele Varianten hinzufügen, wie für die Inhaltskomponente erforderlich sind. Ändern Sie die ausgewählte Variante im linken Bereich jederzeit, um zu überprüfen, wie die Inhaltskomponente für die Bedingung angezeigt wird.

   >[!IMPORTANT]
   >
   >Bedingter Inhalt wird anhand verknüpfter Regeln in der Reihenfolge ausgewertet, in der die Varianten aufgelistet werden. Die erste Variante mit einer Bedingung, die als &quot;true&quot;ausgewertet wird, wird für die Komponente verwendet.
   >
   >Wenn keine der definierten Variantenbedingungen beim Senden der E-Mail als &quot;true&quot;ausgewertet wird, wird die Inhaltskomponente gemäß der **[!UICONTROL Standardvariante]** angezeigt.

1. Um eine Variante zu löschen, klicken Sie auf das Symbol _Mehr Menü_ (**...**) für die Variante und wählen Sie **[!UICONTROL Löschen]**.

   Klicken Sie im Bestätigungsdialogfeld auf **[!UICONTROL Löschen]** .

## Bedingte Regeln

Bedingte Regeln sind ein Satz bedingter Ausdrücke, die als &quot;true&quot;oder &quot;false&quot;ausgewertet werden können. Mithilfe dieser Regeln können Sie festlegen, welche Inhaltsvariante in einer E-Mail-Nachricht basierend auf verschiedenen Kriterien wie Profilattributen oder Kontextereignissen angezeigt werden soll.

Bedingte Regeln werden in der Bedingungsbibliothek gespeichert, wo sie für Ihre Organisation über Journey-Inhalte hinweg wiederverwendet werden können.
<!-- 

>[!NOTE]
>
>You need the [Manage Library Items](../administration/ootb-product-profiles.md) permission to save or delete conditional rules. Saved conditions are available for use by all users within an organization. -->

### Erstellen einer bedingten Regel {#create-condition}

>[!CONTEXTUALHELP]
>id="ajo-b2b_conditions_rule_editor"
>title="Erstellen einer Bedingung"
>abstract="Kombinieren Sie Attribute und kontextbezogene Ereignisse, um Regeln zu erstellen, die bestimmen, welche Inhaltsvariante in E-Mail-Nachrichten angezeigt werden soll."

Sie können über den E-Mail-Designer auf den Builder für bedingte Regeln zugreifen, wenn Sie eine Bedingung für eine Komponentenvariante auswählen.

1. Klicken Sie im Dialogfeld _[!UICONTROL Bedingung auswählen]_ auf **[!UICONTROL Neu erstellen]** und wählen Sie den Bedingungstyp aus:

   * **[!UICONTROL Personenbedingung]** - Wählen Sie diesen Typ aus, um die bedingte Regel mithilfe von Personenattributen und kontextbezogenen Ereignissen zu erstellen.
   * **[!UICONTROL Kontobedingung]** - Wählen Sie diesen Typ aus, um die bedingte Regel mithilfe von Kontoattributen zu erstellen.

   ![Wählen Sie den Bedingungstyp aus, der erstellt werden soll](./assets/conditions-select-create-new.png){width="600" zoomable="yes"}

1. Erstellen Sie die bedingte Regel entsprechend Ihren Anforderungen.

   Ziehen Sie das Element für jedes Attribut oder Ereignis, das Sie in die Regel aufnehmen möchten, auf die Arbeitsfläche der Regel. Erweitern Sie den Filter und füllen Sie den Ausdruck aus.

   ![Vervollständigen Sie den Ausdruck für die Auswertung](./assets/conditions-rule-add-attribute.png){width="600" zoomable="yes"}

   Wenn Sie mehr als einen Filter einschließen, legen Sie die **[!UICONTROL Filterlogik]** fest:

   * **[!UICONTROL Alle Filter anwenden]** - Die Regel wird als &quot;true&quot;ausgewertet, wenn **all** die Filter wahr sind.
   * **[!UICONTROL Alle Filter anwenden]** - Die Regel wird als &quot;true&quot;ausgewertet, wenn **any** der Filter wahr ist.

1. Geben Sie rechts den **[!UICONTROL Namen]** und eine **[!UICONTROL Beschreibung]** (optional) für die Regel ein.

   Verwenden Sie einen aussagekräftigen Namen und eine nützliche Beschreibung, um anderen in Ihrer Organisation zu helfen, damit sie ihn wiederverwenden können, anstatt eine weitere doppelte Bedingung zu erstellen.

   ![Fügen Sie einen Namen und eine Beschreibung für die bedingte Regel hinzu](./assets/conditions-rule-name-description.png){width="600" zoomable="yes"}

1. Wenn die bedingte Regel abgeschlossen ist, klicken Sie auf **[!UICONTROL Speichern]**.

   Die bedingte Regel wird in der Bibliothek gespeichert und Sie können sie für die aktuelle Variante auswählen. Sie ist auch für die Verwendung durch andere dynamische Inhaltsvarianten in Konto-Journey in der -Bibliothek enthalten.

### Regel duplizieren

In der Bibliothek gespeicherte bedingte Regeln können nicht geändert werden. Sie können jedoch eine vorhandene Regel duplizieren und sie ändern, um eine neue Regel zu erstellen.

1. Klicken Sie auf das Symbol _Mehr Menü_ (**...**) für die Variante und wählen Sie **[!UICONTROL Duplizieren]**.

   Ein Duplikat der Regel wird im Regel-Builder geöffnet. Verwenden Sie das Duplikat als Ausgangspunkt für die Regel, die Sie erstellen möchten.

   ![Verwenden Sie eine doppelte Regel, um die Regel zu erstellen, die Sie benötigen](./assets/conditions-rule-duplicate.png){width="600" zoomable="yes"}

1. Ändern, fügen oder löschen Sie im Regel-Builder Bedingungen entsprechend Ihren Anforderungen.

1. Ändern Sie den Namen und die Beschreibung so, dass sie dem Zweck oder den Elementen in der Regel entsprechen.

1. Wenn die bedingte Regel abgeschlossen ist, klicken Sie auf **[!UICONTROL Speichern]**.
