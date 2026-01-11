---
title: Web-Kanalkonfigurationen
description: Erfahren Sie, wie Sie Web-Kanaleinstellungen konfigurieren, um Web-Eigenschaften und Seitenabgleichregeln für die Inhaltsbereitstellung in Journey Optimizer B2B edition zu definieren.
feature: Setup, Channels
role: Admin
badgeBeta: label="Beta" type="informative" tooltip="Diese Funktion befindet sich derzeit in einer eingeschränkten Beta-Version"
source-git-commit: 2f9b007df233cf8a233c3646bf691b7cff139f86
workflow-type: tm+mt
source-wordcount: '1064'
ht-degree: 3%

---

# Web-Kanalkonfigurationen

Eine Web-Konfiguration ist eine Web-Eigenschaft, die durch eine URL identifiziert wird, über die der Inhalt bereitgestellt wird. Es kann einer einzelnen Seiten-URL oder mehreren Seiten entsprechen, sodass Web-Erlebnisse Änderungen über eine oder mehrere Web-Seiten hinweg bereitstellen können. Diese Konfigurationen sind erforderlich, damit Marketing[Fachleute „Aktionsknoten für die Web-Personalisierung in Journey hinzufügen](../content/web-experiences.md#create-a-web-experience) und [Erlebnisänderungen entwerfen](../content/web-experience-design.md) für eine Kampagne verwenden können.

>[!BEGINSHADEBOX]

**Voraussetzungen**

Um Web-Kanäle nutzen zu können, muss auf Ihrer Website für die Besucheridentifizierung und Inhaltsbereitstellung der [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/de/docs/experience-platform/collection/js/js-overview) (`alloy.js`) implementiert sein. Stellen Sie sicher, dass die Adobe Experience Platform Web SDK-Version 2.16 oder höher ist.

Die Webkanalkonfiguration in Journey Optimizer B2B edition erfordert die folgenden [Berechtigungen](../admin/user-management.md#b2b-product-permissions):

* _[!UICONTROL Kanalkonfigurationen]_ > _[!UICONTROL Nachrichtenvoreinstellungen verwalten]_ - Erforderlich zum Erstellen, Aktualisieren und Löschen von Webkanalkonfigurationen.
* _[!UICONTROL Kanalkonfigurationen]_ > _[!UICONTROL Nachrichtenvoreinstellungen anzeigen]_ - Erforderlich zum Anzeigen von Webkanalkonfigurationen.

>[!ENDSHADEBOX]

## Erstellen einer Web-Kanalkonfiguration

1. Navigieren Sie in der linken Navigation zu **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]**.

1. Wählen _[!UICONTROL im]_ unter „Web“ die Option **[!UICONTROL Kanalkonfigurationen]** aus.

   ![Zugreifen auf die Web-Kanal-Konfigurationen](./assets/config-web-channels.png){width="800" zoomable="yes"}

1. Klicken **[!UICONTROL oben]** auf „Kanalkonfiguration erstellen“.

1. Geben Sie einen **[!UICONTROL Namen]** (erforderlich) und einen **[!UICONTROL Beschreibung]** (optional) für die Konfiguration ein.

   >[!NOTE]
   >
   >Namen müssen mit einem Buchstaben (A-Z) beginnen und dürfen nur alphanumerische Zeichen enthalten. Sie können auch die Zeichen Unterstrich `_`, Punkt `.` und Bindestrich `-`.

1. Wählen Sie im Abschnitt **[!UICONTROL Web-Einstellungen]** eine der folgenden Optionen aus:

   * **[!UICONTROL Einzelne Seite]** - Wenn Sie die Änderungen nur auf eine einzelne Seite anwenden möchten, geben Sie eine (Seiten **[!UICONTROL URL ein oder wählen Sie diese aus]**.

     ![Auswählen einer Seiten-URL für eine einseitige Web-Kanal-Konfiguration](./assets/config-web-channel-create-single-page.png){width="600" zoomable="yes"}

   * **[!UICONTROL Matching-Regel für Seiten]** - Um mehrere URLs als Ziel auszuwählen, die derselben Regel entsprechen, erstellen Sie eine [Matching-Regel für Seiten](#build-a-pages-matching-rule) und geben Sie eine **[!UICONTROL Standard-Autoren- und Vorschau-URL]** ein.

1. Klicken Sie auf **[!UICONTROL Senden]**, um die Änderungen zu speichern.

Nachdem Sie die Konfiguration gespeichert haben, befindet sie sich im Status _Entwurf_ und steht Marketing-Experten zur Verfügung, wenn sie einen Web-Kanal in ihren Journey verwenden. Sie können die Konfiguration weiter bearbeiten, solange sie im Entwurfsstatus verbleibt. Sie können eine Entwurfs-Web-Kanal-Konfiguration auch löschen, indem Sie auf das _Mehr_-Symbol (**…**) neben dem Namen klicken und **[!UICONTROL Löschen]** auswählen.

Sobald der Webkanal auf einer Journey verwendet wird, wechselt er in den Status _Aktiv_. In diesem Status können Sie den Namen und die Beschreibung der Konfiguration bearbeiten. Sie können weder die Web-Einstellungen ändern noch die Konfiguration löschen.

## Matching-Regeln für Seiten {#pages-matching-rule}

Beim Erstellen einer Web-Konfiguration können Sie eine Regel _[!UICONTROL Seitenabgleich“ erstellen]_ um mehrere URLs auszuwählen, die derselben Regel entsprechen. Diese Regeln ermöglichen es Ihnen, dieselben Inhaltsänderungen auf mehrere Seiten anzuwenden.

Beispielsweise können Sie Änderungen an einem Hero-Banner auf einer ganzen Website anwenden oder oben ein Bild hinzufügen, das auf allen Produktseiten angezeigt wird.

### Erstellen einer Regel

1. Wenn Sie [eine Web-Kanal-Konfiguration erstellen](#create-a-web-channel-configuration) wählen Sie **[!UICONTROL Seitenabgleichregel]**.

1. Definieren Sie Ihre Kriterien für die Felder **[!UICONTROL Domain]** und **[!UICONTROL Page]** unter Verwendung der verschiedenen Operatoren in jedem Abschnitt, um die Regel zu erstellen.

   +++Domain-Operatoren

   Verwenden Sie die folgenden Operatoren für den Abgleich von Domains entsprechend dem eingegebenen Zeichenfolgenwert:

   | Benutzerin oder Benutzer | Beschreibung | Beispiele |
   | --- | --- | --- |
   | [!UICONTROL Gleich] | Exakte Übereinstimmung mit der Domain. | |
   | [!UICONTROL Beginnt mit] | Entspricht allen Domains (einschließlich Subdomains), die mit der eingegebenen Zeichenfolge beginnen. | `Starts with: dev` entspricht allen Domains und Subdomains, die mit `dev` beginnen, z. B. `dev.example.com`, `dev.products.example.com` und `developer.example.com` |
   | [!UICONTROL Endet mit] | Sucht alle Domains (einschließlich Subdomains), die mit der eingegebenen Zeichenfolge enden. | `Ends with: example.com` entspricht allen Domains und Subdomains, die auf `example.com` enden, z. B. `stage.example.com`, `prod.example.com` und `myexample.com` |
   | [!UICONTROL Platzhalterabgleich] | Ermöglicht die Definition einer Wildcard-Übereinstimmung in der Mitte der Zeichenfolge, z. B. `dev.*.example.com`. Die Validierungsregeln erfordern, dass der Wert genau einen Platzhalter (Sternchen) enthält, wenn der Operator „Platzhalterabgleich _ist_. | `Wildcard matching: dev.*.example.com` entspricht Domains wie `dev.products.example.com`, `dev.mytest.products.example.com` und `dev.blog.example.com` |
   | [!UICONTROL Beliebig] | Entspricht allen Domains. Dies ist beim Testen eines bestimmten Pfads über Domains hinweg nützlich. | |

   +++

   +++Pfadoperatoren

   Verwenden Sie die folgenden Operatoren für die Zuordnung von Pfaden entsprechend dem eingegebenen Zeichenfolgenwert:

   | Benutzerin oder Benutzer | Beschreibung | Beispiele |
   | --- | --- | --- |
   | [!UICONTROL Gleich] | Exakte Übereinstimmung mit dem Pfad. | |
   | [!UICONTROL Beginnt mit] | Entspricht allen Pfaden (einschließlich Unterpfaden), die mit der Zeichenfolge beginnen. | |
   | [!UICONTROL Endet mit] | Sucht alle Pfade (einschließlich Unterpfaden), die mit der Zeichenfolge enden. | |
   | [!UICONTROL Beliebig] | Entspricht allen Pfaden. Dies ist nützlich, wenn alle Pfade unter einer oder mehreren Domains ausgewählt werden sollen. | |
   | [!UICONTROL Platzhalterabgleich] | Ermöglicht die Definition eines internen Platzhalters innerhalb des Pfads, z. B. `/products/*/detail`. Das in der Pfadkomponente `*` Platzhalterzeichen stimmt mit jeder Zeichenfolge überein, bis das erste `/` Zeichen erreicht ist.  Und `/*/` entspricht einer beliebigen Zeichenfolge (einschließlich Unterpfaden). | `Wildcard matching: /products/*/detail` entspricht Pfaden wie `example.com/products/yoga/detail`, `example.com/products/surf/detail`, `example.com/products/tennis/detail` und `example.com/products/yoga/pants/detail` |
   | [!UICONTROL Enthält] | Der Wert wird in einen Platzhalter wie `*mystring*` übersetzt und entspricht allen Pfaden, die die Zeichenfolge enthalten. | `Contains: product` entspricht allen Pfaden, die die `product` enthalten, z. B. `example.com/products`, `example.com/yoga/perfproduct`, `example.com/surf/productdescription` und `example.com/home/product/page` |

   +++

   Um beispielsweise Inhaltsänderungen auf allen _LumaSecure_-Lösungsseiten Ihrer _Bodea_-Website zu unterstützen, wählen Sie **[!UICONTROL Domain]** > **[!UICONTROL Beginnt mit]** > `bodea` und **[!UICONTROL Page]** > **[!UICONTROL Contains]** > `lumasecure`.

   ![Definieren einer Matching-Regel für Seiten für eine Web-Kanal-Konfiguration](./assets/config-web-channel-pages-matching-rules.png){width="600" zoomable="yes"}

1. Wenn für Ihren Anwendungsfall mehrere Regeln erforderlich sind, klicken Sie auf **[!UICONTROL Weitere Seitenregel hinzufügen]** und wiederholen Sie den vorherigen Schritt.

   * Sie können bis zu 10 Regeln definieren.

   * Verwenden Sie die Operatoren **[!UICONTROL Oder]** oder **[!UICONTROL Ausschließen]** zwischen den verschiedenen Regeln.

     _[!UICONTROL Oder]_ ist der Standardoperator zum Definieren mehrerer Regeln und ist nützlich, um mehrere Kriteriendefinitionen hinzuzufügen, die abgeglichen werden können.

     _[!UICONTROL Ausschließen]_ ist nützlich, wenn eine der Seiten, die der definierten Regel entsprechen, nicht als Ziel ausgewählt werden soll. Sie können beispielsweise alle `bodea.com` Seiten ansprechen, die `lumasecure` enthalten, aber ausschließlich Blog-Seiten (z. B. `bodea.com/blogs/lumasecure/latest-release`).

   ![Seiten, die Regeln mit Ausschluss entsprechen](./assets/config-web-channel-pages-matching-rules-exclude.png){width="600" zoomable="yes"}

1. Geben Sie die **[!UICONTROL Standard-URL für Authoring und Vorschau]** ein.

   Dieser Schritt stellt sicher, dass die Seiten, die von der Regel generiert oder abgeglichen werden, eine bestimmte URL sowohl für das Design von Web-Erlebnisinhalten als auch für die Vorschau haben.

## Duplizieren eines Web-Kanals

Sie können eine vorhandene Web-Kanal-Konfiguration duplizieren und ändern, um einen neuen Web-Kanal basierend auf einer vorhandenen zu erstellen. Eine in der Bibliothek gespeicherte aktive Webkanalkonfiguration kann nicht geändert werden.

1. Klicken Sie auf das _Mehr Menü_-Symbol (**…**) für die Variante und wählen Sie **[!UICONTROL Duplizieren]**.

   ![Klicken Sie auf das Menüsymbol Mehr , um eine vorhandene Web-Kanal-Konfiguration zu duplizieren](./assets/config-web-channels-more-menu.png){width="450"}

   Diese Aktion erstellt einen doppelten Web-Kanal, bei dem `_Copy_nnn` an den Namen angehängt wird.

1. Klicken Sie auf den Namen des duplizierten Web-Kanals, um die Parameter zu bearbeiten.

   * Ändern Sie den Namen und die Beschreibung entsprechend dem Zweck oder den Elementen in der Regel.
   * Ändern Sie bei Bedarf die Einzelseiten-URL.
   * Ändern Sie bei Bedarf die Matching-Regel für Seiten entsprechend Ihren Anforderungen.

1. Klicken Sie nach Abschluss der Konfiguration auf **[!UICONTROL Senden]**.
