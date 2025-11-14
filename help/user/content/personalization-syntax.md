---
title: Personalisierungssyntax
description: Erfahren Sie mehr über die auf Handlebars basierende Personalisierungssyntax in Journey Optimizer B2B edition, einschließlich Ausdrücken, Helper, Literaltypen und Formatierungsregeln.
feature: Personalization, Content Design Tools
topic: Personalization
role: Developer
level: Intermediate
keywords: Ausdruck, Editor, Syntax, Personalisierung
source-git-commit: fee5bddcce11b3035da6ab93b18bcc7006b4b554
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 44%

---

# Personalisierungssyntax {#personalization-syntax}

Ausdrücke im [!DNL Journey Optimizer B2B Edition] [Personalisierungseditor](./personalization.md#personalization-editor) basieren auf der Vorlagensyntax _Handlebars_. Sie verwendet eine Vorlage und ein Eingabeobjekt, um HTML oder andere Textformate zu generieren. Handlebars-Vorlagen sehen wie normaler Text mit eingebetteten Handlebars-Ausdrücken aus.

Weitere Informationen zu Handlebars und seiner Funktionsweise finden Sie in der [HandlebarsJS-Dokumentation](https://handlebarsjs.com/){target="_blank"}.

## Allgemeine Regeln

Beispiel für einen einfachen Ausdruck:

```
{{account.accountName}}
```

Dabei gilt:

* `account` ist ein Namespace.
* `accountName` ist ein Token, das aus Attributen besteht.

  >[!NOTE]
  >
  >Die Attributstruktur wird in einem [Adobe Experience Platform-XDM-Schema definiert](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/home){target="_blank"}.

* Kennungen können jedes beliebige Unicode-Zeichen sein, mit Ausnahme der folgenden:

  ```
  Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
  ```

* Die Syntax unterscheidet zwischen Groß- und Kleinschreibung.

* Die Wörter **true**, **false**, **null** und **undefined** sind nur im ersten Teil eines Pfadausdrucks zulässig.

* In Handlebars werden den von {\{expression}\} zurückgegebenen Werten _HTML-Escape-Zeichen_. Wenn der Ausdruck `&` enthält, wird die Ausgabe mit HTML-Escape-Zeichen als `&amp;` generiert. Wenn ein Wert nicht mit einem Escape-Zeichen versehen werden soll, verwenden Sie +triple-stash_.

<!-- For example:

    If the value of the field `profile.person.name` is _Mark & Mary_, the `{\{profile.person.name}\}` value generates as `Mark &amp; Mary` and `{\{\{profile.person.name}}}` renders as `Mark & Mary`. -->

* Für Argumente mit literalen Funktionen unterstützt der Sprach-Parser für Vorlagen keinen einfachen umgekehrten Schrägstrich (`\`) ohne Escape-Zeichen. Dieses Zeichen muss mit einem zusätzlichen umgekehrten Schrägstrich (`\`) escaped werden. Beispiel :

  ```
  {%= regexGroup("abc@xyz.com","@(\\w+)", 1)%}
  ```

## Helper {#helpers-all}

Eine Handlebars-Hilfsfunktion ist eine einfache Kennung, die mit Parametern angehängt werden kann. Jeder Parameter ist ein Handlebars-Ausdruck. Auf diese Helper kann in jedem Kontext einer E-Mail-Vorlage zugegriffen werden.

```sql
{{#each account.accountOrganization.annualRevenue.amount}}
    <li>{{this.name}}</li>
{{/each }}
```

<!-- These block helpers are identified with a `#` preceding the helper name and require a matching closing `/`, of the same name. 

Blocks are expressions that have a block opening ( {\{# }\} ) and closing ( {\{/} } ). -->

Weitere Informationen zu diesen Funktionen finden Sie unter [Hilfsfunktionen](./personalization-helper-functions.md).

## Literaltypen {#literal-types}

[!DNL Adobe Journey Optimizer B2B Edition] unterstützt die folgenden Literaltypen:

| Literal | Definition |
| ------- | ---------- |
| Zeichenfolge | Ein Datentyp, der aus Zeichen besteht, die von doppelten Anführungszeichen umgeben sind. <br>Beispiele: `"prospect"`, `"jobs"`, `"articles"` |
| Boolesch | Ein Datentyp, der entweder „true“ oder „false“ ist. |
| Ganzzahl | Ein Datentyp, der eine ganze Zahl darstellt. Sie kann positiv, negativ oder null sein. <br>Beispiele: `-201`, `0`, `412` |
| Array | Ein Datentyp, der aus einer Gruppe anderer Literalwerte besteht. Zur Gruppierung werden eckige Klammern und Kommas verwendet, um zwischen verschiedenen Werten zu trennen. <br> **Hinweis:** Sie können nicht direkt auf die Eigenschaften von Elementen in einem Array zugreifen. <br> Beispiele: `[1, 4, 7]`, `["US", "FR"]` |

>[!CAUTION]
>
>Die Variable **xEvent** ist in Personalisierungsausdrücken nicht verfügbar. Jeder Verweis auf xEvent führt zu Validierungsfehlern.
