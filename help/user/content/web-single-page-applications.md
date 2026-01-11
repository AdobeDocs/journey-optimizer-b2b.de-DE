---
title: Single Page Applications
description: Erstellen von Web-Erlebnissen für Single Page Applications (SPAs) - Konfigurieren Sie das Anzeigen-Tracking, verarbeiten Sie dynamische Inhalte und verwalten Sie die Client-seitige Navigation in Journey Optimizer B2B edition.
feature: Channels, Personalization
role: User
badgeBeta: label="Beta" type="informative" tooltip="Diese Funktion befindet sich derzeit in einer eingeschränkten Beta-Version"
source-git-commit: e50b6830736bf763d3aae6a58595e868bbac36e0
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 1%

---

# Single Page Applications

Single Page Applications (SPAs) stellen die Web-Personalisierung vor einzigartige Herausforderungen, da sie Seiteninhalte dynamisch aktualisieren, ohne dass die Seiten vollständig neu geladen werden. Journey Optimizer B2B edition bietet spezielle Tools für eine effektive SPA-Personalisierung.

## Grundlegendes zu SPAs

Im Gegensatz zu herkömmlichen mehrseitigen Websites, auf denen jeder Navigations-Trigger eine vollständige Seitenladezeit hat, verwenden SPAs JavaScript, um Inhalte dynamisch zu aktualisieren und gleichzeitig eine einzige HTML-Seite zu verwalten. Dieser Ansatz bietet verschiedene Überlegungen für Web-Erlebnisse:

* **Keine Seitenneuladungen** - Inhaltsänderungen treten auf, ohne dass herkömmliche Seitenladeereignisse ausgelöst werden.
* **Virtuelle Ansichten** - Verschiedene _Ansichten_ oder _Bildschirme_ innerhalb der SPA, die als separate Seiten verfolgt werden müssen.
* **Client-seitiges Routing** - JavaScript-Router (z. B. React Router, Vue Router und Angular Router) verarbeiten die Navigation anstelle von Server-Anfragen.
* **Dynamisches DOM** - Seitenelemente können nach dem ersten Laden der Seite erstellt, geändert oder entfernt werden.

## Konfigurieren der SPA-Unterstützung

Um SPAs effektiv zu personalisieren, müssen Sie das Ansichtstracking so konfigurieren, dass Journey Optimizer B2B edition erkennt, wenn Benutzende zwischen virtuellen Ansichten navigieren.

### Ansichtsdeklarationen einrichten

Arbeiten Sie mit Ihrem Entwicklungs-Team zusammen, um mithilfe der Adobe Web SDK Ansichtsdeklarationen zu implementieren. Bei der Verwendung dieser Ansichtsdeklarationen wird der `sendEvent`-Befehl mit Ansichtsinformationen aufgerufen, sobald die SPA zu einer neuen Ansicht navigiert.

**Beispielimplementierung:**

```javascript
// When a new view is rendered in your SPA
alloy("sendEvent", {
  "xdm": {
    "web": {
      "webPageDetails": {
        "viewName": "product-detail",
        "URL": window.location.href
      }
    }
  },
  "data": {
    "__adobe": {
      "target": {
        "viewName": "product-detail"
      }
    }
  }
});
```

### Namenskonventionen anzeigen

Verwenden Sie konsistente, beschreibende Ansichtsnamen, die der logischen Struktur Ihrer Anwendung entsprechen:

| Ansicht | Name des Beispiels |
| ---- | ------------ |
| Startseite | `home` |
| Produktliste | `product-list` |
| Produktdetails | `product-detail` |
| Warenkorb | `cart` |
| Checkout | `checkout` |
| Konto-Dashboard | `account-dashboard` |

>[!NOTE]
>
>Bei Namen der Ansichten wird zwischen Groß- und Kleinschreibung unterschieden. Verwenden Sie in Ihrer Implementierung eine konsistente Namenskonvention (empfohlen wird die Verwendung von Kleinbuchstaben mit Bindestrichen).

## Erstellen von Web-Erlebnissen für SPAs

Beachten Sie beim Erstellen von Web-Erlebnissen für SPAs die folgenden Best Practices:

### Targeting-spezifische Ansichten

* Richten Sie in der [Webkanal-Konfiguration](../admin/configure-channels-web.md) Regeln zum URL-Abgleich ein, die Ihrer SPA-Routing-Struktur entsprechen.

* Geben Sie beim Erstellen von Änderungen die Ansicht an, in der die Änderung angewendet werden soll.

* Verwenden Sie CSS-Selektoren, die auf die für die jeweilige Ansicht spezifischen Elemente abzielen.

### Verarbeiten dynamischer Inhalte

SPAs laden Inhalte häufig dynamisch nach dem ersten Rendern der Seite. Verwenden Sie diese Verfahren, um sicherzustellen, dass Änderungen korrekt angewendet werden:

#### Auf Elemente warten

Konfigurieren Sie die Änderungen so, dass sie auf das Vorhandensein der Zielelemente warten, bevor Sie sie anwenden:

1. Fügen Sie im nicht visuellen Editor eine Änderung mit einer CSS-Auswahl hinzu.

1. Aktivieren Sie **[!UICONTROL Auf Element warten]** und geben Sie die maximale Wartezeit an.

1. Die Änderung gilt, sobald das Zielelement im DOM angezeigt wird.

#### Verwenden von Mutationsbeobachtern

Bei hochdynamischen Inhalten enthält Web SDK integrierte Mutationsbeobachter, die erkennen, wenn neue Elemente zur Seite hinzugefügt werden. Diese Beobachter stellen sicher, dass Änderungen auch dann angewendet werden, wenn Elemente asynchron geladen werden.

### SPA-Frameworks

Journey Optimizer B2B edition-Web-Erlebnisse funktionieren mit gängigen SPA-Frameworks:

| Framework | Zu beachten |
| --------- | -------------- |
| **React** | Änderungen werden angewendet, nachdem React Komponenten im DOM rendert. Verwenden Sie Klassennamen oder Datenattribute für die Zielgruppenbestimmung. |
| **Angular** | Targeting von Elementen nach Ausführung der Änderungserkennung von Angular. Targeting von Elementen mit `*ngIf` vor dem Rendern vermeiden |
| **Vue.js** | Warten Sie auf die `nextTick` von Vue, um sicherzustellen, dass sich Elemente im DOM befinden. Verwenden Sie Verweise oder benutzerdefinierte Attribute für ein stabiles Targeting. |
| **Next.js / Nuxt.js** | Stellen Sie bei SSR-/SSG-Seiten sicher, dass die Web SDK-Hydrierung abgeschlossen ist, bevor Sie Änderungen erwarten. |

## Best Practices für die SPA-Personalisierung

### Stabile Selektoren verwenden

SPAs generieren häufig dynamische Klassennamen oder IDs (insbesondere bei CSS-in-JS-Lösungen). Als Alternative können Sie Folgendes verwenden:

* **Datenattribute** - Fügen Sie benutzerdefinierte Datenattribute (`data-testid`, `data-section` usw.) zu Elementen hinzu, die Sie ansprechen möchten.
* **Semantic HTML** - Target basierend auf HTML-Struktur und semantischen Elementen.
* **ID-Attribute** - Verwenden Sie nach Möglichkeit stabile ID-Attribute.

**Beispiel:**

```html
<!-- Instead of targeting dynamic class names -->
<button class="css-1a2b3c4d">Sign Up</button>

<!-- Add a stable data attribute -->
<button class="css-1a2b3c4d" data-action="signup">Sign Up</button>
```

**CSS-Auswahl:** `[data-action="signup"]`

### Testansichten

Beim Testen von SPA-Web-Erlebnissen:

1. Navigieren Sie durch alle Ansichten, für die Änderungen gelten.

1. Testen des gesamten Benutzerflusses, einschließlich:
   * Direkte Navigation zu einer Ansicht (Deep-Linking)
   * Navigation aus anderen Ansichten innerhalb der SPA
   * Rückwärts- und Vorwärtsnavigation des Browsers

1. Vergewissern Sie sich, dass Änderungen bei der Rückkehr zu einer zuvor besuchten Ansicht erneut angewendet werden.

### Ansichtübergänge handhaben

Einige SPAs verwenden Animationen oder Übergänge zwischen Ansichten. Bedenken Sie:

* **Zeitplanung** - Stellen Sie sicher, dass die Änderungen nach Abschluss der Übergangsanimationen angewendet werden.
* **Element-Sichtbarkeit** - Elemente können vorhanden sein, sind aber bei Übergängen ausgeblendet.
* **Flimmern** - Wenden Sie Änderungen früh genug an, um sichtbare Inhaltsänderungen zu vermeiden.

## Fehlerbehebung

Wenn Sie Änderungen am SPA-Design überprüfen, verwenden Sie die folgenden Empfehlungen, um einige häufige Probleme zu beheben:

* **Änderungen werden nicht angezeigt** - Wenn Änderungen nicht in Ihrer SPA angezeigt werden:

   1. **Ansichts-Tracking überprüfen** - Überprüfen Sie, ob `sendEvent` Aufrufe den richtigen Ansichtsnamen enthalten.

   1. **Überprüfen des Vorhandenseins von Elementen** - Stellen Sie sicher, dass sich Zielelemente im DOM befinden, wenn Änderungen vorgenommen werden.

   1. **Überprüfungsselektoren** - Bestätigen Sie, dass die CSS-Selektoren mit der tatsächlichen DOM-Struktur übereinstimmen.

   1. **Konsole überprüfen** - Suchen Sie nach JavaScript-Fehlern, die Änderungen verhindern können.

* **Änderungen werden kurz angezeigt und verschwinden dann** - Dieses Problem tritt in der Regel auf, wenn die SPA geänderte Elemente erneut rendert und ersetzt:

   1. Verwenden Sie spezifischere CSS-Selektoren, die über Renderings hinweg stabil bleiben.

   1. Aktivieren Sie es Mutationsbeobachtern, Änderungen beim Erstellen von Elementen erneut anzuwenden.

   1. Arbeiten Sie mit Ihrem Entwicklungs-Team zusammen, um den Zielelementen stabile Attribute hinzuzufügen.

* **Doppelte Änderungen** - Wenn Änderungen mehrmals angezeigt werden:

   1. Vergewissern Sie sich, dass Ansichts-Tracking-Ereignisse nur einmal pro Ansichtstransition ausgelöst werden.

   1. Überprüfen Sie, ob Änderungen sich auf bestimmte Ansichten beziehen, anstatt sie global anzuwenden.

## Verwandte Themen

* [Übersicht über Web-Erlebnisse](./web-experiences.md)
* [Web-Erlebnisdesign](./web-experience-design.md)
* [Web-Kanalkonfigurationen](../admin/configure-channels-web.md)