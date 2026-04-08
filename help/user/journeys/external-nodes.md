---
title: Externe Knoten
description: Erfahren Sie, wie Sie externe Aktionsknoten und externe Aufspaltungspfadknoten in den Account-Journey verwenden, um eine Verbindung mit externen Services herzustellen und Konten und Personen basierend auf der Service-Antwort zu routen.
feature: Account Journeys, Integrations
role: User
source-git-commit: c88ea3ce8c17e78b3e48cb3c2f9951358e822618
workflow-type: tm+mt
source-wordcount: '870'
ht-degree: 0%

---

# Externe Knoten

Verwenden Sie externe Knoten, um Ihre Konto-Journey mit einem externen Service zu verbinden. Wenn eine Konto-Zielgruppe einen dieser Knoten erreicht, sendet Journey Optimizer B2B edition Zielgruppenattributdaten asynchron an den externen Service. Der Service verarbeitet die Daten und antwortet mithilfe eines Callbacks, wobei Zielgruppeninformationen und Metadaten zurückgegeben werden, die die Journey zum Fortsetzen verwendet.

>[!NOTE]
>
>Externe Aktionsknoten sind nur in den Account-Journey verfügbar. Sie werden in persönlichen Journey nicht unterstützt.
>
>Ein Administrator muss [die externe Aktion konfigurieren und aktivieren](../admin/configure-external-actions.md) bevor Marketer diese Knoten auf einer Journey hinzufügen und implementieren können.

Es gibt zwei Knotentypen für externe Aktionen:

* **[Externe Aktion](#external-action)** - Ruft einen externen Service auf und fährt über einen einzelnen ausgehenden Pfad fort. Verwenden Sie diesen Knoten, wenn Sie einen externen Prozess ohne Verzweigungslogik Trigger erstellen möchten, z. B. wenn Sie einen Datensatz in einem externen System aktualisieren oder ein Signal an einen nachgelagerten Service senden möchten.
* **[Externe Aufspaltungspfade](#external-split-paths)** - Ruft einen externen Service auf und bewertet die Antwort auf Routing-Konten entlang eines von mehreren definierten Pfaden. Verwenden Sie diesen Knoten, wenn der externe Service einen Wert zurückgibt, z. B. einen Score, eine Stufe oder eine Klassifizierung, die den nächsten Schritt im Journey bestimmt.

## Externer Aktionsknoten {#external-action}

Der _Externe Aktion_-Knoten ruft einen externen Service auf und fährt unabhängig vom Antwortinhalt über einen einzelnen ausgehenden Pfad fort. Verwenden Sie sie für Integrationen, bei denen nach dem externen Aufruf keine Verzweigung erforderlich ist.

1. Navigieren Sie zur Konto-Journey-Zuordnung.

1. Klicken Sie auf das Pluszeichen ( **+** ) auf einem Pfad und wählen Sie **[!UICONTROL Externe Aktion]** aus.

   ![Externen Aktionsknoten hinzufügen](./assets/node-external-action.png){width="400"}

1. Legen Sie in den Knoteneigenschaften auf der rechten Seite den Kontext **[!UICONTROL Aktion ein]** für die externe Aktion fest:

   * Wählen Sie **[!UICONTROL Konten]** aus, wenn Sie die externe Aktion auf alle Personen anwenden möchten, die Teil von Konten im Knotenpfad sind.
   * Wählen Sie **[!UICONTROL Personen]** aus, wenn Sie eine Änderung auf alle Personen im Knotenpfad anwenden möchten.

1. Wählen Sie den externen **[!UICONTROL Service-Namen]** aus.

   ![Externer Aktionsknoten - Wählen Sie Externer Service aus](./assets/node-external-action-service-name.png){width="600" zoomable="yes"}

   Die Liste enthält alle konfigurierten externen Aktionen, die aktiv sind und für den Typ _Externe Aktion_ und den Kontext bestimmt sind.

1. Wenn der Dienst globale Attribute hat, geben Sie die erforderlichen Werte in die Felder ein, die unter dem Namen des Dienstes angezeigt werden.

1. Fahren Sie mit dem Erstellen des Journey aus den ausgehenden Pfaden des Knotens fort.

   Der _[!UICONTROL Zeitüberschreitungs- oder Fehlerpfad]_ wird automatisch erstellt. Wenn die maximale Wartezeit (wie im Service konfiguriert) verstrichen ist, bevor eine Antwort empfangen wird, fährt das Konto oder die Person diesen Pfad ab. Dies ist dasselbe, wenn eine Fehlerantwort empfangen wird. Sie können diesem Pfad Journey-Knoten hinzufügen, um diese Szenarien zu handhaben, oder die Journey-Enden für das Mitglied der Zielgruppe.

## Knoten für externe Aufspaltungspfade {#external-split-paths}

Der Knoten Externe Aufspaltungspfade ruft einen externen Service auf und verwendet die Antwort, um zu bestimmen, welche Pfadkonten als Nächstes ausgeführt werden. Jeder Pfad wird durch eine Bedingung definiert, die auf einer Variablen (Accessor) basiert, die vom externen Service zurückgegeben wird. Der Journey bewertet die Antwort anhand der definierten Pfadbedingungen und leitet jedes Konto entlang des ersten übereinstimmenden Pfads weiter. Pfadbedingungen werden in der Reihenfolge von oben nach unten ausgewertet. Jedes Konto fährt auf dem ersten Pfad fort, dessen Bedingung mit dem vom externen Service zurückgegebenen Wert übereinstimmt.

1. Navigieren Sie zur Konto-Journey-Zuordnung.

1. Klicken Sie auf das Pluszeichen ( **+** ) auf einem Pfad und wählen Sie **[!UICONTROL Externe Aufspaltungspfade]**.

   ![Fügen Sie einen externen Pfad-Teilungsknoten hinzu](./assets/node-external-split-path.png){width="400"}

1. Wählen Sie in den Knoteneigenschaften auf der rechten Seite den Typ **[!UICONTROL Pfade aufteilen nach]** aus:

   * **[!UICONTROL Konten]** - Bei aufgeteilten Pfaden nach Konten können Sie innerhalb der definierten Pfade sowohl Konto- als auch Personenknoten hinzufügen.
   * **[!UICONTROL Personen]** - Bei aufgeteilten Pfaden nach Personen können Sie nur Personen-Aktionsknoten innerhalb der definierten Pfade hinzufügen. Eine personenbasierte Aufspaltung wird automatisch mit dem Knoten _[!UICONTROL Zusammenführungspfade]_ geschlossen, sodass alle Personen mit dem nächsten Schritt fortfahren können, ohne ihren Kontokontext zu verlieren.

1. Wählen Sie den **[!UICONTROL Service-Namen]** aus.

1. Wenn die Service-Konfiguration _globale Attribute_ aufweist, geben Sie die erforderlichen Werte in die Felder ein, die unter dem Service-Namen angezeigt werden.

1. Definieren _[!UICONTROL für]_ Pfad 1“ die Verzweigungsbedingung:

   * Ersetzen **[!UICONTROL für &quot;]**&quot; den Standardwert durch eine beschreibendere Beschriftung.
   * Wählen **[!UICONTROL für „Variable auswählen]** einen Accessor. Accessoren sind Werte, die vom externen Service zurückgegeben und beim Konfigurieren der Aktion definiert werden.
   * Wählen **[!UICONTROL unter „Operator]** den Operator aus.
   * Geben **[!UICONTROL unter „Werte eingeben]** den Wert ein, mit dem abgeglichen werden soll.

   ![Externer Pfad-Aufspaltungsknoten - Festlegen der Pfadbedingung mithilfe einer Service-Variablen](./assets/node-external-split-path-properties.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Die verfügbaren Bedingungsvariablen und der unterstützte Journey-Kontext (_Account_, _People_ oder _People in Account_) werden durch die Konfiguration der externen Aktion bestimmt. Wenden Sie sich an Ihren Administrator, wenn der erwartete Dienst oder die erwarteten Variablen nicht verfügbar sind.

1. Um weitere Pfade hinzuzufügen, klicken Sie auf **[!UICONTROL Pfad hinzufügen]** und definieren Sie eine Bedingung für jeden gewünschten Pfad.

1. Fahren Sie mit dem Erstellen des Journey aus jedem ausgehenden Pfad des Knotens fort.

   Der _[!UICONTROL Zeitüberschreitungs- oder Fehlerpfad]_ wird automatisch erstellt. Wenn die maximale Wartezeit (wie im Service konfiguriert) verstrichen ist, bevor eine Antwort empfangen wird, fährt das Konto oder die Person diesen Pfad ab. Dies ist dasselbe, wenn eine Fehlerantwort empfangen wird. Sie können diesem Pfad Journey-Knoten hinzufügen, um diese Szenarien zu handhaben, oder die Journey-Enden für das Mitglied der Zielgruppe.

1. Für _Aufspaltung nach Konten_ können Sie einen [Zusammenführungspfade-Knoten](./split-merge-paths-nodes.md#merge-paths) hinzufügen, um zwei oder mehr Pfade nach Bedarf zu kombinieren.
