---
title: Hilfsfunktionen
description: Referenzhandbuch für Personalisierungs-Hilfsfunktionen in Journey Optimizer B2B edition. Es enthält Syntax und Beispiele für Zeichenfolgen, Daten, Mathematik und mehr.
feature: Personalization, Content Design Tools
topic: Personalization
role: Developer
level: Intermediate
keywords: Ausdruck, Editor, Syntax, Personalisierung
source-git-commit: fee5bddcce11b3035da6ab93b18bcc7006b4b554
workflow-type: tm+mt
source-wordcount: '4857'
ht-degree: 44%

---

# Hilfsfunktionen

Verwenden Sie die Helper-Funktionen im Personalisierungseditor, um personalisierte Inhaltserlebnisse präzise und effizient zu definieren, indem Sie Daten bearbeiten, Berechnungen durchführen und Inhalte formatieren. Erkunden Sie diese Funktionen, Operatoren und Helper und experimentieren Sie mit ihnen, um zu erfahren, wie sie zusammenarbeiten, um Ihnen bei der Erstellung maßgeschneiderter, datengesteuerter Journey zu helfen.

>[!AVAILABILITY]
>
>Helper-Funktionen sind für Journey Optimizer-B2B edition-Umgebungen verfügbar, die auf der [vereinfachten Architektur“ bereitgestellt ](../simplified-architecture.md).

## Aggregationsfunktionen

Verwenden Sie Aggregationsfunktionen, um mehrere Werte zu gruppieren, um einen einzigen Zusammenfassungswert zu bilden. Sie können auch Array- und Listenfunktionen verwenden, um die Interaktion mit Arrays, Listen und Zeichenfolgen einfacher zu definieren.

### Durchschnitt {#average}

Verwenden Sie die Funktion `average` , um das arithmetische Mittel aller ausgewählten Werte im Array zurückzugeben.

+++Syntax

```sql
{%= average(array) %}
```

**Beispiel**

Durch den folgenden Vorgang wird der Durchschnittspreis aller Bestellungen zurückgegeben.

```sql
{%=average(orders.order.price)%}
```

+++

### count {#count}

Verwenden Sie die Funktion `count` , um die Anzahl der Elemente innerhalb des angegebenen Arrays zurückzugeben.

+++Syntax

```sql
{%= count(array) %}
```

**Beispiel**

Durch den folgenden Vorgang wird die Anzahl der Bestellungen im Array zurückgegeben.

```sql
{%= count(orders) %}
```

+++

### max {#max}

Verwenden Sie die Funktion `max` , um den größten der ausgewählten Werte im Array zurückzugeben.

+++Syntax

```sql
{%= max(array) %}
```

**Beispiel**

Durch den folgenden Vorgang wird der höchste Preis aller Bestellungen zurückgegeben.

```sql
{%=max(orders.order.price)%}
```

+++

### min {#min}

Verwenden Sie die Funktion `min` , um den kleinsten aller ausgewählten Werte im Array zurückzugeben.

+++Syntax

```sql
{%= min(array) %}
```

**Beispiel**

Durch den folgenden Vorgang wird der niedrigste Preis aller Bestellungen zurückgegeben.

```sql
{%=min(orders.order.price) %}
```

+++

### sum {#sum}

Verwenden Sie die Funktion `sum` , um die Summe aller ausgewählten Werte im Array zurückzugeben.

+++Syntax

```sql
{%= sum(array) %}
```

**Beispiel**

Durch den folgenden Vorgang wird die Summe aller Bestellungen zurückgegeben.

```sql
 {%=sum(orders.order.price)%}
```

+++

## Arithmetische Funktionen {#maths}

Verwenden Sie arithmetische Funktionen, um einfache Berechnungen für Werte durchzuführen.

### hinzufügen {#add}

Mit der Funktion `+` (Addition) können Sie die Summe zweier Argumentausdrücke ermitteln.

+++Syntax

```sql
{%= double + double %}
```

**Beispiel**

Die folgende Operation addiert die Preise von zwei verschiedenen Produkten.

```sql
{%= product1.price + product2.price %}
```

+++

### multiplizieren {#multiply}

Verwenden Sie die Funktion `*` (Multiplikation), um das Produkt zweier Argumentausdrücke zu finden.

+++Syntax

```sql
{%= double * double %}
```

**Beispiel**

Die folgende Operation ermittelt das Produkt im Bestand sowie den Preis eines Produkts, um den Bruttowert des Produkts zu berechnen.

```sql
{%= product.inventory * product.price %}
```

+++

### abziehen {#substract}

Verwenden Sie die `-` (Subtraktion)-Funktion, um den Unterschied von zwei Argumentausdrücken zu finden.

+++Syntax

```sql
{%= double - double %}
```

**Beispiel**

Die folgende Operation ermittelt den Preisunterschied zwischen zwei verschiedenen Produkten.

```sql
{%= product1.price - product2.price %}
```

+++

### Dividieren {#divide}

Verwenden Sie die `/` (Division)-Funktion, um den Quotienten zweier Argumentausdrücke zu finden.

+++Syntax

```sql
{%= double / double %}
```

**Beispiel**

Die folgende Operation ermittelt den Quotienten zwischen den insgesamt verkauften Produkten und dem insgesamt verdienten Geld, um so die durchschnittlichen Kosten pro Artikel zu berechnen.

```sql
{%= totalProduct.price / totalProduct.sold %}
```

+++

### Rest {#remainder}

Verwenden Sie die Funktion `%` (Rest), um den Rest nach der Division der beiden Argumentausdrücke zu finden.

+++Syntax

```sql
{%= double % double %}
```

**Beispiel**

Die folgende Operation prüft, ob das Alter der Person durch fünf teilbar ist.

```sql
{%= person.age % 5 = 0 %}
```

+++

## Array- und Listenfunktionen {#arrays}

Verwenden Sie diese Funktionen, um die Interaktion mit Arrays, Listen und Zeichenfolgen zu vereinfachen.

### countOnlyNull {#count-only-null}

Mit der Funktion `countOnlyNull` können Sie die Anzahl der Nullwerte in einer Liste zählen.

+++Syntax

```sql
{%= countOnlyNull(array) %}
```

**Beispiel**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

Gibt 3 zurück.

+++

### countWithNull {#count-with-null}

Verwenden Sie die Funktion `countWithNull` , um alle Elemente einer Liste einschließlich Nullwerten zu zählen.

+++Syntax

```sql
{%= countWithNull(array) %}
```

**Beispiel**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

Gibt 6 zurück.

+++

### distinct {#distinct}

Verwenden Sie die Funktion `distinct` , um Werte aus einem Array oder einer Liste abzurufen, aus denen doppelte Werte entfernt wurden.

+++Syntax

```sql
{%= distinct(array) %}
```

**Beispiel**

Mit dem folgenden Vorgang werden Personen definiert, die Bestellungen in mehr als einem Geschäft aufgegeben haben.

```sql
{%= distinct(person.orders.storeId).count() > 1 %}
```

+++

### distinctCountWithNull {#distinct-count-with-null}

Mit der Funktion `distinctCountWithNull` können Sie die Anzahl verschiedener Werte in einer Liste einschließlich der Nullwerte zählen.

+++Syntax

```sql
{%= distinctCountWithNull(array) %}
```

**Beispiel**

```sql
{%= distinctCountWithNull([10,2,10,null]) %}
```

Gibt 3 zurück.

+++

### anführen {#head}

Verwenden Sie die Funktion `head` , um das erste Element in einem Array oder einer Liste zurückzugeben.

+++Syntax

```sql
{%= head(array) %}
```

**Beispiel**

Mit dem folgenden Vorgang wird die erste der fünf häufigsten Bestellungen mit dem höchsten Preis zurückgegeben. Weiterführende Informationen zur Funktion `topN` finden Sie im Abschnitt [Erste `n` in Array](#first-n).

```sql
{%= head(topN(orders,price, 5)) %}
```

+++

### topN {#first-n}

Die Funktion `topN` sortiert ein Array in absteigender Reihenfolge basierend auf dem angegebenen numerischen Ausdruck und gibt die ersten `N` Elemente zurück. Wenn die Array-Größe kleiner als `N` ist, wird das gesamte sortierte Array zurückgegeben.

+++Syntax

```sql
{%= topN(array, value, amount) %}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{ARRAY}` | Das zu sortierende Array oder die zu sortierende Liste. |
| `{VALUE}` | Die -Eigenschaft, die zum Sortieren des Arrays oder der Liste verwendet wird. |
| `{AMOUNT}` | Die Anzahl der zurückzugebenden Elemente. |

**Beispiel**

Mit dem folgenden Vorgang werden die ersten fünf Bestellungen mit dem niedrigsten Preis zurückgegeben.

```sql
{%= topN(orders,price, 5) %}
```

+++

### in {#in}

Verwenden Sie die Funktion `in` , um zu bestimmen, ob ein Element Mitglied eines Arrays oder einer Liste ist.

+++Syntax

```sql
{%= in(value, array) %}
```

**Beispiel**

Mit dem folgenden Vorgang werden Personen definiert, die im März, Juni oder September Geburtstag haben.

```sql
{%= in (person.birthMonth, [3, 6, 9]) %}
```

+++

### Umfasst {#includes}

Mit der Funktion `includes` können Sie bestimmen, ob ein Array oder eine Liste ein bestimmtes Element enthält.

+++Syntax

```sql
{%= includes(array,item) %}
```

**Beispiel**

Mit dem folgenden Vorgang werden Personen definiert, zu deren Lieblingsfarben Rot gehört.

```sql
{%= includes(person.favoriteColors,"red") %}
```

+++

### überschneidet {#intersects}

Mit der `intersects`-Funktion wird bestimmt, ob zwei Arrays oder Listen mindestens ein gemeinsames Element aufweisen.

+++Syntax

```sql
{%= intersects(array1, array2) %}
```

**Beispiel**

Mit dem folgenden Vorgang werden Personen definiert, deren Lieblingsfarben mindestens eine der folgenden Farben beinhalten: Rot, Blau oder Grün.

```sql
{%= intersects(person.favoriteColors,["red", "blue", "green"]) %}
```

+++

<!-- ## Intersection{#intersection}

The `intersection` function is used to determine the common members of two arrays or lists.

**Syntax**

```sql
intersection({ARRAY},{ARRAY})
```

**Example**

The following operation defines if person 1 and person 2 both have favorite colors of red, blue, and green.

```sql
intersection(person1.favoriteColors,person2.favoriteColors) = ["red", "blue", "green"]
```
-->

### bottomN {#last-n}

Die Funktion `bottomN` sortiert ein Array in aufsteigender Reihenfolge basierend auf dem angegebenen numerischen Ausdruck und gibt die ersten `N` Elemente zurück. Wenn die Array-Größe kleiner als `N` ist, wird das gesamte sortierte Array zurückgegeben.

+++Syntax

```sql
{%= bottomN(array, value, amount) %}
```

| Argument | Beschreibung |
| --------- | ----------- | 
| `{ARRAY}` | Das zu sortierende Array oder die zu sortierende Liste. |
| `{VALUE}` | Die -Eigenschaft, die zum Sortieren des Arrays oder der Liste verwendet wird. |
| `{AMOUNT}` | Die Anzahl der zurückzugebenden Elemente. |

**Beispiel**

Mit dem folgenden Vorgang werden die letzten fünf Bestellungen mit dem höchsten Preis zurückgegeben.

```sql
{%= bottomN(orders,price, 5) %}
```

+++

### notIn {#notin}

Verwenden Sie die Funktion `notIn` , um zu bestimmen, ob ein Element nicht Mitglied eines Arrays oder einer Liste ist.

>[!NOTE]
>
> Die `notIn`-Funktion stellt *außerdem* sicher, dass keiner der Werte null ist. Daher sind die Ergebnisse keine exakte Negation der `in`-Funktion.

+++Syntax

```sql
{%= notIn(value, array) %}
```

**Beispiel**

Mit dem folgenden Vorgang werden Personen definiert, die nicht im März, Juni oder September Geburtstag haben.

```sql
{%= notIn(person.birthMonth ,[3, 6, 9]) %}
```

+++

### subsetOf {#subset}

Verwenden Sie die Funktion `subsetOf` , um zu bestimmen, ob ein bestimmtes Array (Array A) eine Teilmenge eines anderen Arrays (Array B) ist. Mit anderen Worten: ob alle Elemente in Array A Elemente von Array B sind.

+++Syntax

```sql
{%= subsetOf(array1, array2) %}
```

**Beispiel**

Mit dem folgenden Vorgang werden Personen definiert, die alle ihrer Lieblingsstädte besucht haben.

```sql
{%= subsetOf(person.favoriteCities,person.visitedCities) %}
```

+++

### Obermenge {#superset}

Verwenden Sie die Funktion `supersetOf` , um zu bestimmen, ob ein bestimmtes Array (Array A) eine Obermenge eines anderen Arrays (Array B) ist. Mit anderen Worten: ob Array A alle Elemente in Array B enthält.

+++Syntax

```sql
{%= supersetOf(array1, array2) %}
```

**Beispiel**

Mit dem folgenden Vorgang werden Personen definiert, die mindestens einmal Sushi und mindestens einmal Pizza gegessen haben.

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"]) %}
```

+++

## Datums- und Uhrzeitfunktionen {#date-time}

Verwenden Sie die Datums- und Uhrzeitfunktionen, um Datums- und Uhrzeitvorgänge für Werte durchzuführen.

### Tage hinzufügen {#add-days}

Die Funktion `addDays` passt ein bestimmtes Datum um eine angegebene Anzahl von Tagen an, wobei positive Werte zum Erhöhen und negative Werte zum Verringern verwendet werden.

+++Syntax

```sql
{%= addDays(date, number) %}
```

**Beispiel**

* Eingabe: `{%= addDays(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* Ausgabe: `2024-11-11T17:19:51Z`

+++

### Stunden hinzufügen {#add-hours}

Die Funktion `addHours` passt ein bestimmtes Datum um eine angegebene Anzahl von Stunden an, wobei positive Werte zum Erhöhen und negative Werte zum Verringern verwendet werden.

+++Syntax

```sql
{%= addHours(date, number) %}
```

**Beispiel**

* Eingabe: `{%= addHours(stringToDate("2024-11-01T17:19:51Z"),1) %}`
* Ausgabe: `2024-11-01T18:19:51Z`

+++

### Minuten hinzufügen {#add-minutes}

Die Funktion `addMinutes` passt ein bestimmtes Datum um eine angegebene Anzahl von Minuten an, wobei positive Werte zum Erhöhen und negative Werte zum Verringern verwendet werden.

+++Syntax

```sql
{%= addMinutes(date, number) %}
```

**Beispiel**

* Eingabe: `{%= addMinutes(stringToDate("2024-11-01T17:59:51Z"),10) %}`
* Ausgabe: `2024-11-01T18:09:51Z`

+++

### AddMonths {#add-months}

Die Funktion `addMonths` passt ein bestimmtes Datum um eine angegebene Anzahl von Monaten an, wobei positive Werte zum Erhöhen und negative Werte zum Verringern verwendet werden.

+++Syntax

```sql
{%= addMonths(date, number) %}
```

**Beispiel**

* Eingabe: `{%= addMonths(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* Ausgabe: `2025-01-01T17:19:51Z`

+++

### addSecond {#add-seconds}

Die Funktion `addSeconds` passt ein bestimmtes Datum um eine angegebene Anzahl von Sekunden an, wobei positive Werte zum Erhöhen und negative Werte zum Verringern verwendet werden.

+++Syntax

```sql
{%= addSeconds(date, number) %}
```

**Beispiel**

* Eingabe: `{%= addSeconds(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* Ausgabe: `2024-11-01T17:20:01Z`

+++

### Jahre hinzufügen {#add-years}

Die Funktion `addYears` passt ein bestimmtes Datum um eine angegebene Anzahl von Jahren an, wobei positive Werte zum Erhöhen und negative Werte zum Verringern verwendet werden.

+++Syntax

```sql
{%= addYears(date, number) %}
```

**Beispiel**

* Eingabe: `{%= addYears(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* Ausgabe: `2026-11-01T17:19:51Z`

+++

### Alter {#age}

Verwenden Sie die `age`-Funktion, um das Alter zu einem bestimmten Datum abzurufen.

+++Syntax

```sql
 {%= age(datetime) %}
```

<!--
**Example**

The following operation gets the value of the identity map for the key `example@example.com`.

```sql
 {%= age(datetime) %}
```
-->

+++

### pageInDays {#age-days}

Die `ageInDays` berechnet die Anzahl der Tage zwischen dem angegebenen Datum und dem aktuellen Datum. Negative Werte werden für zukünftige Datumsangaben und positive Werte für vergangene Datumsangaben verwendet.

+++Syntax

```sql
{%= ageInDays(date) %}
```

**Beispiel**

currentDate = 2025-01-07T12:17:10.720122+05:30 (Asien/Kolkata)

* Eingabe: `{%= ageInDays(stringToDate("2025-01-01T17:19:51Z"))%}`
* Ausgabe: `5`

+++

### ageInMonths {#age-months}

Die `ageInMonths` berechnet die Anzahl der Monate zwischen dem angegebenen Datum und dem aktuellen Datum. Negative Werte werden für zukünftige Datumsangaben und positive Werte für vergangene Datumsangaben verwendet.

+++Syntax

```sql
{%= ageInMonths(date) %}
```

**Beispiel**

currentDate = 2025-01-07T12:22:46.993748+05:30(Asien/Kolkata)

* Eingabe: `{%=ageInMonths(stringToDate("2024-01-01T00:00:00Z"))%}`
* Ausgabe: `12`

+++

### compareDates {#compare-dates}

Die Funktion `compareDates` vergleicht das erste Eingabedatum mit einem anderen. Gibt 0 zurück, wenn date1 gleich date2 ist, -1, wenn date1 vor date2 liegt, und 1, wenn date1 nach date2 liegt.

+++Syntax

```sql
{%= compareDates(date1, date2) %}
```

**Beispiel**

* Eingabe: `{%=compareDates(stringToDate("2024-12-02T00:00:00Z"), stringToDate("2024-12-03T00:00:00Z"))%}`
* Ausgabe: `-1`

+++

### convertZonedDateTime {#convert-zoned-date-time}

Die Funktion `convertZonedDateTime` wandelt eine Datums-/Uhrzeitangabe in eine bestimmte Zeitzone um.

+++Syntax

```sql
{%= convertZonedDateTime(dateTime, timezone) %}
```

**Beispiel**

* Eingabe: `{%=convertZonedDateTime(stringToDate("2019-02-19T08:09:00Z"), "Asia/Tehran")%}`
* Ausgabe: `2019-02-19T11:39+03:30[Asia/Tehran]`

+++

### currentTimeInMillis {#current-time}

Verwenden Sie die `currentTimeInMillis`-Funktion, um die aktuelle Zeit in Epochenmillisekunden abzurufen.

+++Syntax

```sql
{%= currentTimeInMillis() %}
```

<!--
**Example**

The following operation gets all the keys for the map `identityMap`.

```sql
{%= keys(identityMap) %}
```
-->

+++

### Datumsdifferenz {#date-diff}

Verwenden Sie die `dateDiff`-Funktion, um die Differenz zwischen zwei Daten als Anzahl von Tagen abzurufen.

+++Syntax

```sql
{%= dateDiff(datetime,datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### Tag des Monats {#day-month}

Die Funktion `dayOfMonth` gibt die Zahl zurück, die dem Tag des Monats entspricht.

+++Syntax

```sql
{%= dayOfMonth(datetime) %}
```

**Beispiel**

* Eingabe: `{%= dayOfMonth(stringToDate("2024-11-05T17:19:51Z")) %}`
* Ausgabe: `5`

+++

### Tag der Woche {#day-week}

Verwenden Sie die Funktion `dayOfWeek` , um den Wochentag abzurufen.

+++Syntax

```sql
{%= dayOfWeek(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### dayOfYear {#day-year}

Verwenden Sie die `dayOfYear`-Funktion, um den Tag des Jahres abzurufen.

+++Syntax

```sql
{%= dayOfYear(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### diffInSeconds {#diff-seconds}

Die Funktion `diffInSeconds` gibt den Unterschied zwischen zwei Daten in Form von Sekunden zurück.

+++Syntax

```sql
{%= diffInSeconds(endDate, startDate) %}
```

**Beispiel**

* Eingabe: `{%=diffInSeconds(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T17:19:01Z"))%}`
* Ausgabe: `50`

+++

### extractHours {#extract-hours}

Die Funktion `extractHours` extrahiert die Stundenkomponente aus einem bestimmten Zeitstempel.

+++Syntax

```sql
{%= extractHours(date) %}
```

**Beispiel**

* Eingabe: `{%= extractHours(stringToDate("2024-11-01T17:19:51Z"))%}`
* Ausgabe: `17`

+++

### extractMinutes {#extract-minutes}

Die Funktion `extractMinutes` extrahiert die Minutenkomponente aus einem bestimmten Zeitstempel.

+++Syntax

```sql
{%= extractMinutes(date) %}
```

**Beispiel**

* Eingabe: `{%= extractMinutes(stringToDate("2024-11-01T17:19:51Z"))%}`
* Ausgabe: `19`

+++

### ExtractMonths {#extract-months}

Die Funktion `extractMonth` extrahiert die Monatskomponente aus einem bestimmten Zeitstempel.

+++Syntax

```sql
{%= extractMonths(date) %}
```

**Beispiel**

* Eingabe: `{%=extractMonth(stringToDate("2024-11-01T17:19:51Z"))%}`
* Ausgabe: `11`

+++

### extractSeconds {#extract-seconds}

Die Funktion `extractSeconds` extrahiert die Sekundenkomponente aus einem bestimmten Zeitstempel.

+++Syntax

```sql
{%= extractSeconds(date) %}
```

**Beispiel**

* Eingabe: `{%=extractSeconds(stringToDate("2024-11-01T17:19:51Z"))%}`
* Ausgabe: `51`

+++

### formatDate {#format-date}

Verwenden Sie die `formatDate`-Funktion zum Formatieren eines Datums-/Uhrzeitwerts. Das Format muss ein gültiges Java-`DateTimeFormat` sein.

+++Syntax

```sql
{%= formatDate(datetime, format) %}
```

Dabei ist die erste Zeichenfolge das Datumsattribut und der zweite Wert gibt an, wie das Datum konvertiert und angezeigt werden soll.

>[!NOTE]
>
> Wenn ein Datumsmuster ungültig ist, wird das Datum auf das ISO-Standardformat zurückgesetzt.
>
> Sie können zur Datumsformatierung die Java-Funktionen verwenden, die in der [Oracle-Dokumentation](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank} zusammengefasst sind.

**Beispiel**

Durch den folgenden Vorgang wird das Datum im folgenden Format zurückgegeben: MM/TT/JJ.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY") %}
```

+++

#### Musterzeichen {#pattern-characters}

Einige Musterbuchstaben sehen möglicherweise ähnlich aus, stellen jedoch unterschiedliche Konzepte dar.

| Muster | Bedeutung | Beispiel (für `2023-12-31T10:15:30Z`) |
|---------|---------|--------------------------------------|
| `y` | Kalenderjahr (Standardjahr) | `2023` |
| `Y` | Wochenbasiertes Jahr (ISO 8601). Sie kann sich an den Jahresgrenzen unterscheiden. | `2024` (31. Dezember 2023 fällt in die erste Woche des Jahres 2024) |
| `M` | Monat des Jahres (1-12 oder Text wie `Jan`, `January`) | `12` oder `Dec` |
| `m` | Minute der Stunde (0-59) | `15` |
| `d` | Tag des Monats (1-31) | `31` |
| `D` | Tag des Jahres (1-366) | `365` |

#### Formatieren des Datums mit Gebietsschema-Unterstützung {#format-date-locale}

Sie können die `formatDate`-Funktion verwenden, um einen Datums-/Uhrzeitwert in die entsprechende sprachabhängige Darstellung zu formatieren, z. B. für ein gewünschtes Gebietsschema. Das Format muss ein gültiges Java-`DateTimeFormat` sein.

+++Syntax

```sql
{%= formatDate(datetime, format, locale) %}
```

Dabei ist die erste Zeichenfolge das Datumsattribut, der zweite Wert ist die Art, wie das Datum konvertiert und angezeigt werden soll, und der dritte Wert stellt das Gebietsschema im Zeichenfolgenformat dar.

>[!NOTE]
>
> Wenn ein Datumsmuster ungültig ist, wird das Datum auf das ISO-Standardformat zurückgesetzt.
>
> Sie können zur Datumsformatierung die Java-Funktionen verwenden, die in der [Oracle-Dokumentation zusammengefasst ](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html).
>
> Sie können Formatierungen und gültige Gebietsschemata verwenden, die in der [Dokumentation zu Oracle ](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) und [Unterstützte Gebietsschemata](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html) zusammengefasst sind.

**Beispiel**

Durch den folgenden Vorgang wird das Datum im folgenden Format zurückgegeben: MM/TT/JJ und Gebietsschema FRANKREICH.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY", "fr_FR") %}
```

+++

### getCurrentZonedDateTime {#get-current-zoned-date-time}

Die Funktion `getCurrentZonedDateTime` gibt das aktuelle Datum und die aktuelle Uhrzeit mit Zeitzoneninformationen zurück.

+++Syntax

```sql
{%= getCurrentZonedDateTime() %}
```

**Beispiel**

* Eingabe: `{%= getCurrentZonedDateTime() %}`
* Ausgabe: `2024-12-06T17:22:02.281067+05:30[Asia/Kolkata]`

+++

### diffInHours {#hours-difference}

Die Funktion `diffInHours` gibt den Unterschied zwischen zwei Daten in Form von Stunden zurück.

+++Syntax

```sql
{%= diffInHours(endDate, startDate) %}
```

**Beispiel**

* Eingabe: `{%= diffInHours(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T07:19:51Z"))%}`
* Ausgabe: `10`

+++

### diffInMinutes {#diff-minutes}

Die `diffInMinutes` gibt die Differenz zwischen zwei Daten in Minuten zurück.

+++Syntax

```sql
{%= diffInMinutes(endDate, startDate) %}
```

**Beispiel**

* Eingabe: `{%= diffInMinutes(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T16:19:51Z"))%}`
* Ausgabe: `60`

+++

### diffInMonths {#months-difference}

Die Funktion `diffInMonths` gibt den Unterschied zwischen zwei Daten in Form von Monaten zurück.

+++Syntax

```sql
{%= diffInMonths(endDate, startDate) %}
```

**Beispiel**

* Eingabe: `{%=diffInMonths(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-08-01T17:19:51Z"))%}`
* Ausgabe: `3`

+++

### setDays {#set-days}

Verwenden Sie die `setDays` , um den Tag des Monats für die Datums-/Uhrzeitangabe festzulegen.

+++Syntax

```sql
{%= setDays(datetime, day) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### setHours {#set-hours}

Legen Sie mit der `setHours` die Stunde der Datums-/Uhrzeitangabe fest.

+++Syntax

```sql
{%= setHours(datetime, hour) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### toDateTime {#string-to-date-time}

Die Funktion `toDateTime` wandelt eine Zeichenfolge in ein Datum um. Bei einer ungültigen Eingabe wird als Ausgabe das Epochen-Datum zurückgegeben.

+++Syntax

```sql
{%= toDateTime(string, string) %}
```

**Beispiel**

* Eingabe: `{%=toDateTime("2024-11-01T17:19:51Z")%}`
* Ausgabe: `2024-11-01T17:19:51Z`

+++

### toUTC {#to-utc}

Verwenden Sie die `toUTC`-Funktion, um eine Datums-/Uhrzeitangabe in UTC zu konvertieren.

+++Syntax

```sql
{%= toUTC(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### truncateToStartOfDay {#truncate-day}

Verwenden Sie die `truncateToStartOfDay`, um eine bestimmte Datums-/Uhrzeitangabe zu ändern, indem Sie sie auf den Beginn des Tages mit der Zeit 00:00 festlegen.

+++Syntax

```sql
{%= truncateToStartOfDay(date) %}
```

**Beispiel**

* Eingabe: `{%= truncateToStartOfDay(stringToDate("2024-11-01T17:19:51Z")) %}`
* Ausgabe: `2024-11-01T00:00Z`

+++

### truncateToStartOfQuarter {#truncate-quarter}

Verwenden Sie die Funktion `truncateToStartOfQuarter` , um eine Datums-/Uhrzeitangabe auf den ersten Tag des Quartals zu kürzen (z. B. 1. Januar, 1. April, 1. Juli, 1. Oktober) um 00 :00.

+++Syntax

```sql
{%= truncateToStartOfQuarter(dateTime) %}
```

**Beispiel**

* Eingabe: `{%=truncateToStartOfQuarter(stringToDate("2024-11-01T17:19:51Z"))%}`
* Ausgabe: `2024-10-01T00:00Z`

+++

### truncateToStartOfWeek {#truncate-week}

Die `truncateToStartOfWeek`-Funktion ändert eine bestimmte Datums-/Uhrzeitangabe, indem sie sie auf den Beginn der Woche (Montag um 00 Uhr) :00.

+++Syntax

```sql
{%= truncateToStartOfWeek(dateTime) %}
```

**Beispiel**

* Eingabe: `{%= truncateToStartOfWeek(stringToDate("2024-11-19T17:19:51Z"))%} // tuesday`
* Ausgabe: `2024-11-18T00:00Z // monday`

+++

### truncateToStartOfYear {#truncate-year}

Verwenden Sie die `truncateToStartOfYear`, um eine bestimmte Datums-/Uhrzeitangabe zu ändern, indem Sie sie auf 00 :00 auf den ersten Tag des Jahres (1. Januar) kürzen.

+++Syntax

```sql
{%= truncateToStartOfYear(dateTime) %}
```

**Beispiel**

* Eingabe: `{%=truncateToStartOfYear(stringToDate("2024-11-01T17:19:51Z"))%}`
* Ausgabe: `2024-01-01T00:00Z`

+++

### weekOfYear {#week-of-year}

Verwenden Sie die `weekOfYear`-Funktion, um die Woche des Jahres abzurufen.

+++Syntax

```sql
{%= weekOfYear(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### diffInYears {#diff-years}

Verwenden Sie die `diffInYears`-Funktion, um die Differenz zwischen zwei Daten in Jahren zurückzugeben.

+++Syntax

```sql
{%= diffInYears(endDate, startDate) %}: int
```

**Beispiel**

* Eingabe: `{%=diffInYears(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2019-10-01T17:19:51Z"))%}`
* Ausgabe: `5`

+++

## Operatorfunktionen {#operators}

Verwenden Sie die booleschen und Vergleichsfunktionen, um logische Auswertungen durchzuführen.

### und {#and}

Die Funktion `and` wird zur Erstellung einer logischen Verknüpfung verwendet.

+++Syntax

```sql
{%= query1 and query2 %}
```

**Beispiel**

Der folgende Vorgang gibt alle Personen mit Wohnsitz (Frankreich) und Geburtsjahr (1985) zurück.

```sql
{%= profile.homeAddress.country = "France" and profile.person.birthYear = 1985 %}
```

+++

### oder {#or}

Die Funktion `or` wird verwendet, um eine logische Trennung zu erstellen.

+++Syntax

```sql
{%= query1 or query2 %}
```

**Beispiel**

Der folgende Vorgang gibt alle Personen mit Wohnsitz (Frankreich) oder Geburtsjahr (1985) zurück.

```sql
{%= profile.homeAddress.country = "France" or profile.person.birthYear = 1985 %}
```

+++

<!--
## Not{#not}

The `not` (or `!`) function is used to create a logical negation.

**Syntax**

```sql
not ({QUERY})
!({QUERY})
```

**Example**

The following operation will return all people who do not have their home country as Canada.

```sql
not (homeAddress.countryISO = "CA")
```
-->

### ist gleich {#operator-equals}

Die Funktion `=` (gleich) prüft, ob ein Wert oder Ausdruck gleich einem anderen Wert oder Ausdruck ist.

+++Syntax

```sql
{%= expression = value %}
```

**Beispiel**

Mit dem folgenden Vorgang wird geprüft, ob das Land der Wohnadresse Frankreich ist.

```sql
{%= profile.homeAddress.country = "France" %}
```

+++

### ungleich {#notequal}

Die Funktion `!=` (ungleich) prüft, ob ein Wert oder Ausdruck **ungleich** einem anderen Wert oder Ausdruck ist.

+++Syntax

```sql
{%= expression != value %}
```

**Beispiel**

Mit dem folgenden Vorgang wird geprüft, ob das Land der Wohnadresse nicht Frankreich ist.

```sql
{%= profile.homeAddress.country != "France" %}
```

+++

### größer als {#greaterthan}

Verwenden Sie die Funktion `>` (größer als), um zu überprüfen, ob der erste Wert größer als der zweite ist.

+++Syntax

```sql
{%= expression1 > expression2 %}
```

**Beispiel**

Mit dem folgenden Vorgang werden Personen definiert, die nach 1970 geboren wurden.

```sql
{%= profile.person.birthYear > 1970 %}
```

+++

### Größer oder gleich {#greaterthanorequal}

Mit der Funktion `>=` (größer oder gleich) können Sie überprüfen, ob der erste Wert größer oder gleich dem zweiten Wert ist.

+++Syntax

```sql
{%= expression1 >= expression2 %}
```

**Beispiel**

Mit dem folgenden Vorgang werden Personen definiert, die im Jahr 1970 oder danach geboren wurden.

```sql
{%= profile.person.birthYear >= 1970 %}
```

+++

### kleiner als {#lessthan}

Verwenden Sie die Vergleichsfunktion `<` (kleiner als), um zu überprüfen, ob der erste Wert kleiner als der zweite ist.

+++Syntax

```sql
{%= expression1 < expression2 %}
```

**Beispiel**

Mit dem folgenden Vorgang werden Personen definiert, die vor 2000 geboren wurden.

```sql
{%= profile.person.birthYear < 2000 %}
```

+++

### Kleiner oder gleich{#lessthanorequal}

Mit der Vergleichsfunktion `<=` (kleiner oder gleich) können Sie überprüfen, ob der erste Wert kleiner oder gleich dem zweiten Wert ist.

+++Syntax

```sql
{%= expression1 <= expression2 %}
```

**Beispiel**

Mit dem folgenden Vorgang werden Personen definiert, die im Jahr 2000 oder früher geboren wurden.

```sql
{%= profile.person.birthYear <= 2000 %}
```

+++

## Dynamische Funktionen {#dynamic-helpers}

Verwenden Sie die dynamischen Hilfsfunktionen, um bedingte Auswertungen, Iterationen und Variablenzuweisungen für die dynamische Personalisierung zu verwenden.

### Standardwert für Fallback {#default-value}

Der Helper `Default Fallback Value` wird verwendet, um einen standardmäßigen Fallback-Wert zurückzugeben, wenn ein Attribut leer oder null ist. Dieser Mechanismus funktioniert für Profilattribute und Journey-Ereignisse.

+++Syntax

```sql
Hello {%=profile.personalEmail.name.firstName ?: "there" %}!
```

In diesem Beispiel wird der Wert `there` angezeigt, wenn das Attribut `firstName` dieses Profils leer oder null ist.

+++

### if (conditions) {#if-function}

Der Helper `if` wird zum Definieren eines bedingten Blocks verwendet.
Wenn die Auswertung des Ausdrucks „true“ zurückgibt, wird der Block dargestellt, andernfalls wird er übersprungen.

+++Syntax

```sql
{%#if contains(account.accountOrganization.primaryEmailDomain, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

Nach dem Helper `if` können Sie eine `else`-Anweisung einfügen, um einen Code-Block auszuführen, wenn die Auswertung „false“ zurückgibt.
Die `elseif`-Anweisung gibt eine neue Bedingung an, die geprüft wird, wenn die erste Anweisung „false“ zurückgibt.


**Format**

```sql
{
    {
        {%#if condition1%} element_1 
        {%else if condition2%} element_2 
        {%else%} default_element 
        {%/if%}
    }
}
```

<!-- 
**Examples**

* **Render different store links based on conditional expressions**

    ```sql
    {%#if profile.homeAddress.countryCode = "FR"%}
    <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
    {%else%}
    <a href="https://www.somedomain.com/en">Checkout our catalogue</a>
    {%/if%}
    ```

* **Determine email address extension**

    ```sql
    {%#if contains(profile.personalEmail.address, ".edu")%}
    <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
    {%else if contains(profile.personalEmail.address, ".org")%}
    <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
    {%else%}
    <a href="https://www.adobe.com/users">Checkout our page</a>
    {%/if%}
    ```

* **Add a conditional link**

    The following operation adds a link to the `www.adobe.com/academia` website for profiles with '.edu' email addresses only, the `www.adobe.com/org` website for profiles with '.org' email addresses, and the default URL `www.adobe.com/users` for all other profiles:

    ```sql
    {%#if contains(profile.personalEmail.address, ".edu")%}
    <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
    {%else if contains(profile.personalEmail.address, ".org")%}
    <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
    {%else%}
    <a href="https://www.adobe.com/users">Checkout our page</a>
    {%/if%}
    ```

* **Conditional content based on audience membership**

    ```sql
    {%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
    Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
    {%else if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"%}
    Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
    {%/if%}
    ```
-->

+++

### außer {#unless}

Verwenden Sie den `unless` Helper , um einen bedingten Block zu definieren. Im Gegensatz zur Hilfsfunktion `if` wird der Block gerendert, wenn die Auswertung des Ausdrucks „falsch“ zurückgibt.

+++Syntax

```sql
{%#unless unlessCondition%} element_1 {%else%} default_element {%/unless%}
```

**Beispiel**

Darstellung von Inhalt je nach E-Mail-Adressenerweiterung:

```sql
{%#unless endsWith(account.accountOrganization.primaryEmailDomain}, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content
{%/unless%}
```

+++

### jeweils {#each}

Verwenden Sie den `each` Helper , um die Elemente eines Arrays zu verarbeiten.

Die Hilfsstruktur ist ```{{#each ArrayName}}``` YourContent-`{{/each}}`

Sie können das Keyword `this` innerhalb des Blocks verwenden, um auf die einzelnen Array-Elemente zu verweisen. Verwenden Sie `{{@index}}` , um den Index des Array-Elements zu rendern.

+++Syntax

```sql
{{#each profile.productsInCart}}
    <li>{{this.name}}</li>
{{/each}}
```

**Beispiel**

```sql
{{#each profile.homeAddress.city}}
  {{@index}} : {{this}}<br>
{{/each}}
```

**Beispiel**

So wird eine Liste von Produkten dargestellt, die dieser Benutzer in den Warenkorb gelegt hat:

```sql
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
{{/each}}
```

+++

### mit {#with}

Verwenden Sie den `with` Helper , um das Evaluierungs-Token des Vorlagenteils zu ändern.

+++Syntax

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

Der Helper `with` ist auch nützlich, um die Kurzform einer Variable zu definieren.

**Beispiel**

Verwenden Sie `with`, um lange Variablennamen in kürzere Namen umzuwandeln:

```sql
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```

+++

### belassen {#let}

Die `let`-Funktion ermöglicht das Speichern eines Ausdrucks als Variable, die später in einer Abfrage verwendet werden kann.

+++Syntax

```sql
{% let variable = expression %} {{variable}}
```

**Beispiel**

Im folgenden Beispiel können Sie die Gesamtsumme der Preise für Produkte im Warenkorb mit Preisen zwischen 100 und 1000 berechnen.

```sql
{% let sum = 0%}
    {{#each profile.productsInCart as |p|}}
        {%#if p.price>100 and p.price<1000%}
            {%let sum = sum + p.price %}
        {%/if%}
    {{/each}}
{{sum}}
```

+++

## Ausführungsmetadaten {#execution-metadata}

>[!AVAILABILITY]
>
>Diese Funktion ist nur eingeschränkt verfügbar. Wenden Sie sich an den Adobe-Support, um Zugriff zu erhalten.

Verwenden Sie den `executionMetadata`, um benutzerdefinierte Schlüssel-Wert-Paare dynamisch im Ausführungskontext der Nachricht zu erfassen und zu speichern.

Mit dieser Funktion können Sie kontextuelle Informationen an beliebige native Aktionen Ihrer Kampagnen oder Journeys anhängen. Verwenden Sie diese Option, um kontextuelle Echtzeit-Versanddaten für verschiedene Zwecke in externe Systeme zu exportieren, z. B. Tracking, Analyse, Personalisierung und nachgelagerte Verarbeitung.

>[!NOTE]
>
>Benutzerdefinierte Aktionen unterstützen die `executionMetadata` nicht.

Beispielsweise können Sie den `executionMetadata` Helper verwenden, um eine bestimmte ID an jeden Versand anzuhängen, der an jedes Profil gesendet wird. Diese Informationen werden zur Laufzeit generiert und die angereicherten Ausführungsmetadaten können dann zur nachgelagerten Abstimmung mit einer externen Reporting-Plattform exportiert werden.

+++Syntax

```
{{executionMetadata key="your_key" value="your_value"}}
```

In dieser Syntax bezieht sich `key` auf den Metadatennamen und `value` sind die beizubehaltenden Metadaten.

**Funktionsweise**

Wählen Sie in einer Kampagne oder Journey ein beliebiges Element aus Ihrem Kanalinhalt aus und fügen Sie mithilfe des Personalisierungseditors diesem Element die Hilfsfunktion `executionMetadata` hinzu.

>[!NOTE]
>
>Die `executionMetadata` Funktion ist nicht sichtbar, wenn der Inhalt selbst angezeigt wird.

Zur Laufzeit wird der Metadatenwert dem vorhandenen **[!UICONTROL Nachrichten-Feedback-Ereignisdatensatz“ hinzugefügt]** wobei das folgende Schema hinzugefügt wird:

```
"_experience": {
  "customerJourneyManagement": {
    "messageExecution": {
      "metadata": {
        "your_key": "your_value"
      }
    }
  }
}
```

>[!IMPORTANT]
>
>Für die Schlüssel-Wert-Paare pro Aktion gibt es eine Obergrenze von 2 KB. Wenn die Grenze von 2 KB überschritten wird, wird die Nachricht weiterhin zugestellt, aber jedes der Schlüssel-Wert-Paare kann abgeschnitten werden.

**Beispiel**

```
{{executionMetadata key="firstName" value=profile.person.name.firstName}}
```

In diesem Beispiel ist unter der Annahme `profile.person.name.firstName` = „Alex“ die resultierende Entität:

```
{
  "key": "firstName",
  "value": "Alex"
}
```

+++

## Zuordnungsfunktionen {#maps}

Verwenden Sie Zuordnungsfunktionen in der Personalisierung, um die Interaktion mit Zuordnungen zu erleichtern.

### get {#get}

Verwenden Sie die Funktion `get` , um den Wert einer Zuordnung für einen bestimmten Schlüssel abzurufen.

+++Syntax

```sql
{%= get(map, string) %}
```

**Beispiel**

Die folgende Operation ruft den Wert der Identitätszuordnung für den Schlüssel `example@example.com` ab.

```sql
{%= get(identityMap,"example@example.com") %}
```

+++

### Schlüssel {#keys}

Verwenden Sie die Funktion `keys` , um alle Schlüssel für eine bestimmte Zuordnung abzurufen.

+++Syntax

```sql
{%= keys(map) %}
```

**Beispiel**

Mit dem folgenden Vorgang werden alle Schlüssel für die `identityMap` abgerufen.

```sql
{%= keys(identityMap) %}
```

+++

### Werte {#values}

Die `values`-Funktion wird zum Abrufen aller Werte einer gegebenen Zuordnung verwendet.

+++Syntax

```sql
{%= values(map) %}
```

**Beispiel**

Mit dem folgenden Vorgang werden alle Werte für die `identityMap` abgerufen.

```sql
{%= values(identityMap) %}
```

+++

## Mathematische Funktionen {#math}

Erfahren Sie, wie Sie im Personalisierungseditor mathematische Funktionen verwenden.

### absolut {#absolute}

Verwenden Sie die Funktion `absolute` , um eine Zahl in ihren absoluten Wert zu konvertieren.

+++Syntax

```sql
{%= absolute(int) %}: int
```

+++

### formatNumber {#format-number}

Verwenden Sie die Funktion `formatNumber` , um eine beliebige Zahl in eine sprachabhängige Darstellung zu formatieren.

Sie akzeptiert eine Zahl und eine Zeichenfolge, die das Gebietsschema darstellt, und gibt eine formatierte Zeichenfolge der Zahl im gewünschten Gebietsschema zurück.

+++Syntax

```sql
{%= formatNumber(number/double,string) %}: string
```

Sie können Formatierungen und gültige Gebietsschemata verwenden, die in der [Dokumentation zu Oracle ](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) und [Unterstützte Gebietsschemata](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html){_blank} zusammengefasst sind

**Beispiel**

Diese Abfrage gibt eine formatierte Zeichenfolge auf Arabisch zurück, die 123456.789 als Eingabenummer entspricht.

```sql
{%= formatNumber(123456.789, "ar_EG") %}
```

+++

### random {#random}

Verwenden Sie die Funktion `random` , um einen zufälligen Wert zwischen 0 und 1 zurückzugeben.

+++Syntax

```sql
{%= random() %}: double
```

+++

### abgerundet {#round-down}

Mit der Funktion `roundDown` können Sie eine Zahl abrunden.

+++Syntax

```sql
{%= roundDown(double) %}: double
```

+++

### aufrunden {#round-up}

Mit der Funktion `roundUp` können Sie eine Zahl aufrunden.

+++Syntax

```sql
{%= roundUp(double) %}: double
```

+++

### toHexString {#to-hex-string}

Die Funktion `toHexString` konvertiert eine beliebige Zahl in ihre hexadezimale Zeichenfolge.

+++Syntax

```sql
{%= toHexString(number) %}: string
```

**Beispiel**

Diese Abfrage gibt den Hexadezimalwert 158 als 9e zurück.

```sql
{%= toHexString(158) %}
```

+++

### toInt {#to-int}

Verwenden Sie die Funktion `toInt` , um Typen (number, double, integer, long, float, short, byte, boolean, string) in eine Ganzzahl zu konvertieren.

+++Syntax

```sql
{%= toInt(<valueToConvert>) %}: integer
```

**Beispiel**

Diese Abfrage gibt den ganzzahligen Wert von 42,6 als 42 zurück.

```sql
{%= toInt(42.6) %}: integer
```

+++

### toPercentage {#to-percentage}

Verwenden Sie die Funktion `toPercentage` , um eine Zahl in einen Prozentwert zu konvertieren.

+++Syntax

```sql
{%= toPercentage(double) %}: string
```

+++

### toPrecision {#to-precision}

Verwenden Sie die Funktion `toPrecision` , um eine Zahl in die erforderliche Präzision zu konvertieren.

+++Syntax

```sql
{%= toPrecision(double,int) %}: string
```

+++

### toString {#to-string}

Die Funktion `toString` konvertiert eine beliebige Zahl in ihre Zeichenfolgendarstellung.

+++Syntax

```sql
{%= toString(string) %}: string
```

**Beispiel**

Diese Abfrage gibt `"12"` zurück.

```sql
{%= toString(12) %} 
```

+++

## Objektfunktionen {#objects}

Objektfunktionen zum Abfragen von Objekteigenschaften oder Attributen.

### isNull {#isNull}

Die `isNull`-Funktion ermittelt, ob eine Objektreferenz nicht vorhanden ist.

+++Syntax

```sql
{%= isNull(object) %}
```

**Beispiel**

Mit dem folgenden Vorgang wird geprüft, ob die Privatadresse der Person nicht vorhanden ist.

```sql
{%= isNull(person.homeAddress) %}
```

+++

### isNotNull {#isNotNull}

Die `isNotNull`-Funktion ermittelt, ob eine Objektreferenz nicht vorhanden ist.

+++Syntax

```sql
{%= isNotNull(object) %}
```

**Beispiel**

Mit dem folgenden Vorgang wird geprüft, ob die Privatadresse der Person vorhanden ist.

```sql
{%= isNotNull(person.homeAddress) %}
```

+++

## Zeichenfolgenfunktionen {#string-functions}

Erfahren Sie, wie Sie im Personalisierungseditor Zeichenfolgenfunktionen verwenden können.

### Binnenmajuskel {#camelCase}

Mit der Funktion `camelCase` wird der erste Buchstabe eines jeden Wortes einer Zeichenfolge großgeschrieben.

+++Syntax

```sql
{%= camelCase(string)%}
```

**Beispiel**

Mit der folgenden Funktion wird der erste Buchstabe eines Wortes in der Straßenadresse des Profils großgeschrieben.

```sql
{%= camelCase(profile.homeAddress.street) %}
```

+++

### charCodeAt {#char-code-at}

Die Funktion `charCodeAt` gibt den ASCII-Wert eines Zeichens zurück, z. B. die Funktion `charCodeAt` in JavaScript. Als Eingabeargumente werden eine Zeichenfolge und eine Ganzzahl (die die Position eines Zeichens definiert) benötigt und der entsprechende ASCII-Wert wird zurückgegeben.

+++Syntax

```sql
{%= charCodeAt(string,int) %}: int
```

**Beispiel**

Die folgende Funktion gibt den ASCII-Wert von `o` (111) zurück.

```sql
{%= charCodeAt("some", 1)%}
```

+++

### concat {#concate}

Die Funktion `concat` kombiniert zwei Zeichenfolgen zu einer.

+++Syntax

```sql
{%= concat(string,string) %}
```

**Beispiel**

Die folgende Funktion kombiniert die Stadt und das Land des Profils in einer einzigen Zeichenfolge.

```sql
{%= concat(profile.homeAddress.city,profile.homeAddress.country) %}
```

+++

### enthält {#contains}

Verwenden Sie die Funktion `contains` , um zu bestimmen, ob eine Zeichenfolge eine angegebene Unterzeichenfolge enthält.

+++Syntax

```sql
{%= contains(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `STRING_1` | Die Zeichenfolge, die überprüft werden soll. |
| `STRING_2` | Die Zeichenfolge, nach der in der ersten Zeichenfolge gesucht werden soll. |
| `CASE_SENSITIVE` | Ein optionaler Parameter, mit dem bestimmt wird, ob bei der Prüfung die Groß-/Kleinschreibung beachtet wird. Mögliche Werte: true (Standard)/false. |

**Beispiele**

* Die folgende Funktion prüft, ob der Vorname des Profils den Buchstaben A enthält (in Groß- oder Kleinbuchstaben). Wenn das Profil dies tut, wird `true` zurückgegeben. Wenn nicht, wird `false` zurückgegeben.

  ```sql
  {%= contains(profile.person.name.firstName, "A", false) %}
  ```

* Die folgende Abfrage bestimmt bei Beachtung der Groß-/Kleinschreibung, ob die E-Mail-Adresse der Person die `2010@gm` enthält.

  ```sql
  {%= contains(profile.person.emailAddress,"2010@gm") %}
  ```

+++

### doesNotContains {#doesNotContain}

Verwenden Sie die Funktion `doesNotContain` , um zu bestimmen, ob eine Zeichenfolge eine angegebene Unterzeichenfolge nicht enthält.

+++Syntax

```sql
{%= doesNotContain(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `STRING_1` | Die Zeichenfolge, die überprüft werden soll. |
| `STRING_2` | Die Zeichenfolge, nach der in der ersten Zeichenfolge gesucht werden soll. |
| `CASE_SENSITIVE` | Ein optionaler Parameter, mit dem bestimmt wird, ob bei der Prüfung die Groß-/Kleinschreibung beachtet wird. Mögliche Werte: true (Standard)/false. |

**Beispiel**

Die folgende Abfrage bestimmt bei Beachtung der Groß-/Kleinschreibung, ob die E-Mail-Adresse der Person die `2010@gm` nicht enthält.

```sql
{%= doesNotContain(profile.person.emailAddress,"2010@gm")%}
```

+++

### doesNotEndWith {#doesNotEndWith}

Verwenden Sie die Funktion `doesNotEndWith` , um zu bestimmen, ob eine Zeichenfolge nicht mit einer angegebenen Unterzeichenfolge endet.

+++Syntax

```sql
{%= doesNotEndWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die überprüft werden soll. |
| `{STRING_2}` | Die Zeichenfolge, nach der in der ersten Zeichenfolge gesucht werden soll. |
| `{CASE_SENSITIVE}` | Ein optionaler Parameter, mit dem bestimmt wird, ob bei der Prüfung die Groß-/Kleinschreibung beachtet wird. Mögliche Werte: true (Standard)/false. |

**Beispiel**

Die folgende Abfrage bestimmt bei Beachtung der Groß-/Kleinschreibung, ob die E-Mail-Adresse der Person nicht mit `.com` endet.

```sql
doesNotEndWith(person.emailAddress,".com")
```

+++

### doesNotStartWith {#doesNotStartWith}

Verwenden Sie die Funktion `doesNotStartWith` , um zu bestimmen, ob eine Zeichenfolge nicht mit einer angegebenen Unterzeichenfolge beginnt.

+++Syntax

```sql
{%= doesNotStartWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die überprüft werden soll. |
| `{STRING_2}` | Die Zeichenfolge, nach der in der ersten Zeichenfolge gesucht werden soll. |
| `{CASE_SENSITIVE}` | Ein optionaler Parameter, mit dem bestimmt wird, ob bei der Prüfung die Groß-/Kleinschreibung beachtet wird. Mögliche Werte: true (Standard)/false. |

**Beispiel**

Die folgende Abfrage bestimmt bei Beachtung der Groß-/Kleinschreibung, ob der Name der Person nicht mit `Joe` beginnt.

```sql
{%= doesNotStartWith(person.name,"Joe")%}
```

+++

### Encode64 {#encode64}

Verwenden Sie die Funktion `encode64` zum Codieren einer Zeichenfolge, um personenbezogene Daten (PI) beizubehalten, z. B. zur Aufnahme in eine URL.

+++Syntax

```sql
{%= encode64(string) %}
```

+++

### endet mit {#endsWith}

Verwenden Sie die Funktion `endsWith` , um zu bestimmen, ob eine Zeichenfolge mit einer angegebenen Unterzeichenfolge endet.

+++Syntax

```sql
{%= endsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die überprüft werden soll. |
| `{STRING_2}` | Die Zeichenfolge, nach der in der ersten Zeichenfolge gesucht werden soll. |
| `{CASE_SENSITIVE}` | Ein optionaler Parameter, mit dem bestimmt wird, ob bei der Prüfung die Groß-/Kleinschreibung beachtet wird. Mögliche Werte: true (Standard)/false. |

**Beispiel**

Die folgende Abfrage bestimmt bei Beachtung der Groß-/Kleinschreibung, ob die E-Mail-Adresse der Person mit `.com` endet.

```sql
{%= endsWith(person.emailAddress,".com") %}
```

+++

### ist gleich {#equals}

Mit der Funktion `equals` können Sie bestimmen, ob eine Zeichenfolge gleich der angegebenen Zeichenfolge ist, wobei zwischen Groß- und Kleinschreibung unterschieden wird.

+++Syntax

```sql
{%= equals(STRING_1, STRING_2) %}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die überprüft werden soll. |
| `{STRING_2}` | Die mit der ersten Zeichenfolge zu vergleichende Zeichenfolge. |

**Beispiel**

Die folgende Abfrage bestimmt bei Beachtung der Groß-/Kleinschreibung, ob der Name der Person `John` ist.

```sql
{%=equals(profile.person.name,"John") %}
```

+++

### equalsIgnoreCase {#equalsIgnoreCase}

Mit der Funktion `equalsIgnoreCase` können Sie bestimmen, ob eine Zeichenfolge gleich der angegebenen Zeichenfolge ist, wobei nicht zwischen Groß- und Kleinschreibung unterschieden wird.

+++Syntax

```sql
{%= equalsIgnoreCase(STRING_1, STRING_2) %}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die überprüft werden soll. |
| `{STRING_2}` | Die mit der ersten Zeichenfolge zu vergleichende Zeichenfolge. |

**Beispiel**

Die folgende Abfrage bestimmt ohne Berücksichtigung der Groß-/Kleinschreibung, ob der Name der Person `John` ist.

```sql
{%= equalsIgnoreCase(profile.person.name,"John") %}
```

+++

### extractEmailDomain {#extractEmailDomain}

Extrahieren Sie mit der Funktion `extractEmailDomain` die Domain einer E-Mail-Adresse.

+++Syntax

```sql
{%= extractEmailDomain(string) %}
```

**Beispiel**

Mit der folgenden Abfrage wird die E-Mail-Domain der persönlichen E-Mail-Adresse extrahiert.

```sql
{%= extractEmailDomain(profile.personalEmail.address) %}
```

+++

### formatCurrency {#format-currency}

Verwenden Sie die Funktion `formatCurrency` , um eine beliebige Zahl in die entsprechende sprachabhängige Währungsdarstellung zu konvertieren, je nachdem, welches Gebietsschema als Zeichenfolge im zweiten Argument übergeben wurde.

+++Syntax

```sql
{%= formatCurrency(number/double,string) %}: string
```

**Beispiel**

Diese Abfrage gibt 56,00 £ zurück.

```sql
{%= formatCurrency(56L,"en_GB") %}
```

+++

### getUrlHost {#get-url-host}

Verwenden Sie die Funktion `getUrlHost` , um den Host-Namen einer URL abzurufen.

+++Syntax

```sql
{%= getUrlHost(string) %}: string
```

**Beispiel**

```sql
{%= getUrlHost("https://www.myurl.com/contact") %}
```

Gibt „www.myurl.com“ zurück

+++

### getUrlPath {#get-url-path}

Verwenden Sie die Funktion `getUrlPath` , um den Pfad nach dem Domain-Namen einer URL abzurufen.

+++Syntax

```sql
{%= getUrlPath(string) %}: string
```

**Beispiel**

```sql
{%= getUrlPath("https://www.myurl.com/contact.html") %}
```

Gibt „/contact.html“ zurück

+++

### getUrlProtocol {#get-url-protocol}

Verwenden Sie die Funktion `getUrlProtocol` , um das Protokoll einer URL abzurufen.

+++Syntax

```sql
{%= getUrlProtocol(string) %}: string
```

**Beispiel**

```sql
{%= getUrlProtocol("https://www.myurl.com/contact.html") %}
```

Gibt „http“ zurück

+++

### indexOf {#index-of}

Verwenden Sie die Funktion `indexOf` , um die Position (im ersten Argument) des ersten Auftretens des zweiten Parameters zurückzugeben. Gibt -1 zurück, wenn keine Übereinstimmung vorliegt.

+++Syntax

```sql
{%= indexOf(STRING_1, STRING_2) %}: integer
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die überprüft werden soll. |
| `{STRING_2}` | Die Zeichenfolge, nach der im ersten Parameter gesucht werden soll. |

**Beispiel**

```sql
{%= indexOf("hello world","world" ) %}
```

Gibt 6 zurück.

+++

### isEmpty {#isEmpty}

Verwenden Sie die Funktion `isEmpty` , um zu bestimmen, ob eine Zeichenfolge leer ist.

+++Syntax

```sql
{%= isEmpty(string) %}
```

**Beispiel**

Die folgende Funktion gibt „true“ zurück, wenn die Mobiltelefonnummer des Profils leer ist. Andernfalls wird `false` zurückgegeben.

```sql
{%= isEmpty(profile.mobilePhone.number) %}
```

+++

### isNotEmpty {#is-not-empty}

Verwenden Sie die Funktion `isNotEmpty` , um zu bestimmen, ob eine Zeichenfolge nicht leer ist.

+++Syntax

```sql
{= isNotEmpty(string) %}: boolean
```

**Beispiel**

Die folgende Funktion gibt „true“ zurück, wenn die Mobiltelefonnummer des Profils nicht leer ist. Andernfalls wird `false` zurückgegeben.

```sql
{%= isNotEmpty(profile.mobilePhone.number) %}
```

+++

### lastIndexOf {#last-index-of}

Verwenden Sie die Funktion `lastIndexOf` , um die Position (im ersten Argument) des letzten Auftretens des zweiten Parameters zurückzugeben. Gibt -1 zurück, wenn keine Übereinstimmung vorliegt.

+++Syntax

```sql
{= lastIndexOf(STRING_1, STRING_2) %}: integer
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die überprüft werden soll. |
| `{STRING_2}` | Die Zeichenfolge, nach der im ersten Parameter gesucht werden soll. |

**Beispiel**

```sql
{%= lastIndexOf("hello world","o" ) %}
```

Gibt 7 zurück.

+++

### leftTrim {#leftTrim}

Verwenden Sie die Funktion `leftTrim` , um Leerzeichen vom Anfang einer Zeichenfolge zu entfernen.

+++Syntax

```sql
{%= leftTrim(string) %}
```

+++

### length {#length}

Verwenden Sie die Funktion `length` , um die Anzahl der Zeichen in einer Zeichenfolge oder einem Ausdruck abzurufen.

+++Syntax

```sql
{%= length(string) %}
```

**Beispiel**

Die folgende Funktion gibt die Länge des Stadtnamens des Profils zurück.

```sql
{%= length(profile.homeAddress.city) %}
```

+++

### Gefällt mir {#like}

Verwenden Sie die Funktion `like` , um zu bestimmen, ob eine Zeichenfolge einem angegebenen Muster entspricht.

+++Syntax

```sql
{%= like(STRING_1, STRING_2) %}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die überprüft werden soll. |
| `{STRING_2}` | Der Ausdruck, der mit der ersten Zeichenfolge übereinstimmen soll. Es werden zwei Sonderzeichen zum Erstellen eines Ausdrucks unterstützt: `%` und `_`. <ul><li>`%` wird verwendet, um 0 oder mehr Zeichen zu repräsentieren.</li><li>`_` wird verwendet, um genau ein Zeichen zu repräsentieren.</li></ul> |

**Beispiel**

Die folgende Abfrage ruft alle Städte ab, in denen Profile leben, und enthält die `es`.

```sql
{%= like(profile.homeAddress.city, "%es%")%}
```

+++

### Kleinbuchstaben {#lower}

Verwenden Sie die Funktion `lowerCase` , um eine Zeichenfolge in Kleinbuchstaben zu konvertieren.

+++Syntax

```sql
{%= lowerCase(string) %}
```

**Beispiel**

Mit dieser Funktion wird der Vorname des Profils in Kleinbuchstaben umgewandelt.

```sql
{%= lowerCase(profile.person.name.firstName) %}
```

+++

### „matches“ {#matches}

Verwenden Sie die Funktion `matches` , um zu bestimmen, ob eine Zeichenfolge mit einem bestimmten regulären Ausdruck übereinstimmt. Weitere Informationen zu Übereinstimmungsmustern in regulären Ausdrücken finden Sie in [Dokumentation zu Oracle](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html).

+++Syntax

```sql
{%= matches(STRING_1, STRING_2) %}
```

**Beispiel**

Die folgende Abfrage bestimmt ohne Unterscheidung der Groß-/Kleinschreibung, ob der Name der Person mit `John` beginnt.

```sql
{%= matches(person.name.,"(?i)^John") %}
```

+++

### Maske {#mask}

Verwenden Sie die Funktion `mask` , um einen Teil einer Zeichenfolge durch „X“-Zeichen zu ersetzen.

+++Syntax

```sql
{%= mask(string,integer,integer) %}
```

**Beispiel**

Die folgende Abfrage ersetzt die Zeichenfolge „123456789“ durch „X“, mit Ausnahme des ersten und der letzten beiden Zeichen.

```sql
{%= mask("123456789",1,2) %}
```

Die Abfrage gibt `1XXXXXX89` zurück.

+++

### md5 {#md5}

Verwenden Sie die Funktion `md5` , um den MD5-Hash einer Zeichenfolge zu berechnen und zurückzugeben.

+++Syntax

```sql
{%= md5(string) %}: string
```

**Beispiel**

```sql
{%= md5("hello world") %}
```

Gibt „5eb63bbbe01eeed093cb22bb8f5acdc3“ zurück

+++

### notEqualTo {#notEqualTo}

Verwenden Sie die Funktion `notEqualTo` , um zu bestimmen, ob eine Zeichenfolge nicht gleich der angegebenen Zeichenfolge ist.

+++Syntax

```sql
{%= notEqualTo(STRING_1, STRING_2) %}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die überprüft werden soll. |
| `{STRING_2}` | Die mit der ersten Zeichenfolge zu vergleichende Zeichenfolge. |

**Beispiel**

Die folgende Abfrage bestimmt bei Beachtung der Groß-/Kleinschreibung, ob der Name der Person nicht `John` ist.

```sql
{%= notEqualTo(profile.person.name,"John") %}
```

+++

### notEqualWithIgnoreCase {#not-equal-with-ignore-case}

Verwenden Sie die `notEqualWithIgnoreCase`-Funktion, um zwei Zeichenfolgen zu vergleichen, wobei die Groß-/Kleinschreibung ignoriert wird.

+++Syntax

```sql
{= notEqualWithIgnoreCase(STRING_1,STRING_2) %}: boolean
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die überprüft werden soll. |
| `{STRING_2}` | Die mit der ersten Zeichenfolge zu vergleichende Zeichenfolge. |

**Beispiel**

Die folgende Abfrage bestimmt, ob der Name der Person nicht `john` ist, wobei nicht zwischen Groß- und Kleinschreibung unterschieden wird.

```sql
{%= notEqualTo(profile.person.name,"john") %}
```

+++

### RegexGroup {#regexGroup}

Verwenden Sie die `regexGroup`-Funktion, um spezifische Informationen basierend auf dem bereitgestellten regulären Ausdruck zu extrahieren.

+++Syntax

```sql
{%= regexGroup(STRING, EXPRESSION, GROUP) %}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING}` | Die Zeichenfolge, die überprüft werden soll. |
| `{EXPRESSION}` | Der reguläre Ausdruck, der mit der ersten Zeichenfolge übereinstimmen soll. |
| `{GROUP}` | Ausdrucksgruppe, mit der eine Übereinstimmung gefunden werden soll. |

**Beispiel**

Mit der folgenden Abfrage wird der Domain-Name aus einer E-Mail-Adresse extrahiert.

```sql
{%= regexGroup(emailAddress,"@(\\w+)", 1) %}
```

+++

### replace {#replace}

Verwenden Sie die Funktion `replace` , um eine bestimmte Unterzeichenfolge in einer Zeichenfolge durch eine andere Unterzeichenfolge zu ersetzen.

+++Syntax

```sql
{%= replace(STRING_1,STRING_2,STRING_3) %}:string
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, in der die Teilzeichenfolge ersetzt werden muss. |
| `{STRING_2}` | Die zu ersetzende Teilzeichenfolge. |
| `{STRING_3}` | Die als Ersatz dienende Teilzeichenfolge. |

**Beispiel**

```sql
{%= replace("Hello John, here is your monthly newsletter!","John","Mark") %}
```

Gibt `Hello Mark, here is your monthly newsletter!` zurück

+++

### replaceAll {#replaceAll}

Verwenden Sie die Funktion `replaceAll` , um alle Unterzeichenfolgen eines Textes, die mit dem Regex-Ausdruck übereinstimmen, durch die angegebene literale Ersatzzeichenfolge zu ersetzen. Regex verfügt über eine besondere Handhabung von `\` und `+` und alle Regex-Ausdrücke folgen der PQL-Escaping-Strategie. Die Ersetzung erfolgt vom Anfang der Zeichenfolge zum Ende, z. B. führt ein Ersetzen von `aa` durch `b` in der Zeichenfolge `aaa` zu `ba` statt zu `ab`.

+++Syntax

```sql
{%= replaceAll(string,string,string) %}
```

>[!NOTE]
>
> Wenn der als zweites Argument verwendete Ausdruck ein spezielles Regex-Zeichen ist, verwenden Sie einen doppelten umgekehrten Schrägstrich (`//`).  Spezielle Regex-Zeichen sind: [., +, *, ?, ^, $, (, ), [,], {, }, |, \.]
> 
> Weitere Informationen finden Sie in der [Oracle-Dokumentation](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html){_blank}.
>

+++

### RightTrim {#rightTrim}

Die Funktion `rightTrim` entfernt Leerzeichen vom Ende einer Zeichenfolge.

+++Syntax

```sql
{%= rightTrim(string) %}
```

+++

### SHA256 {#sha256}

Mit der Funktion `sha256` wird der sha256-Hash eines Strings berechnet und zurückgegeben.

+++Syntax

```sql
{%= sha256(string) %} : string
```

**Beispiel**

```sql
{%= sha256("Eliechxh")%}
```

Gibt `0b0b207880b999adaad6231026abf87caa30760b6f326b21727b61139332257d` zurück

+++

### split {#split}

Verwenden Sie die Funktion `split` , um eine Zeichenfolge durch ein bestimmtes Zeichen zu teilen.

+++Syntax

```sql
{%= split(string,string) %}
```

+++

### startsWith {#startsWith}

Verwenden Sie die Funktion `startsWith` , um zu bestimmen, ob eine Zeichenfolge mit einer angegebenen Unterzeichenfolge beginnt.

+++Syntax

```sql
{%= startsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die überprüft werden soll. |
| `{STRING_2}` | Die Zeichenfolge, nach der in der ersten Zeichenfolge gesucht werden soll. |
| `{CASE_SENSITIVE}` | Ein optionaler Parameter, mit dem bestimmt wird, ob bei der Prüfung die Groß-/Kleinschreibung beachtet wird. Standardmäßig ist dies auf „true“ festgelegt. |

**Beispiel**

Die folgende Abfrage bestimmt bei Beachtung der Groß-/Kleinschreibung, ob der Name der Person mit `Joe` beginnt.

```sql
{%= startsWith(person.name,"Joe") %}
```

+++

### stringToDate {#string-to-date}

Die Funktion `stringToDate` konvertiert einen Zeichenfolgenwert in einen Datums-/Uhrzeitwert. Es gibt zwei Argumente: Zeichenfolgendarstellung eines Datums/Uhrzeit und Zeichenfolgendarstellung des Formatierers.

+++Syntax

```sql
{= stringToDate("date-time value","formatter" %}
```

**Beispiel**

```sql
{= stringToDate("2023-01-10 23:13:26", "yyyy-MM-dd HH:mm:ss") %}
```

+++

### string_to_integer {#string-to-integer}

Verwenden Sie die Funktion `string_to_integer` , um einen Zeichenfolgenwert in einen ganzzahligen Wert zu konvertieren.

+++Syntax

```sql
{= string_to_integer(string) %}: int
```

+++

### stringToNumber {#string-to-number}

Verwenden Sie die Funktion `stringToNumber` , um eine Zeichenfolge in eine Zahl zu konvertieren. Bei einer ungültigen Eingabe wird dieselbe Zeichenfolge als Ausgabe zurückgegeben.

+++Syntax

```sql
{%= stringToNumber(string) %}: double
```

+++

### substr {#sub-string}

Verwenden Sie die Funktion `substr` , um die Unterzeichenfolge des Zeichenfolgenausdrucks zwischen dem Anfangsindex und dem Endindex zurückzugeben.

+++Syntax

```sql
{= substr(string, integer, integer) %}: string
```

+++

### titleCase {#titleCase}

Verwenden Sie die Funktion `titleCase` , um die ersten Buchstaben jedes Wortes einer Zeichenfolge großzuschreiben.

+++Syntax

```sql
{%= titleCase(string) %}
```

**Beispiel**

Wenn die Person in der Washington High Street lebt, gibt diese Funktion `Washington High Street` zurück.

```sql
{%= titleCase(profile.person.location.Street) %}
```

+++

### toBool {#to-bool}

Verwenden Sie die Funktion `toBool` , um einen Argumentwert je nach Typ in einen booleschen Wert zu konvertieren.

+++Syntax

```sql
{= toBool(string) %}: boolean
```

+++

### toDateTime {#to-date-time}

Verwenden Sie die Funktion `toDateTime` , um die Zeichenfolge in ein Datum zu konvertieren. Bei einer ungültigen Eingabe wird als Ausgabe das Epochen-Datum zurückgegeben.

+++Syntax

```sql
{%= toDateTime(string, string) %}: date-time
```

+++

### toDateTimeOnly {#to-date-time-only}

Verwenden Sie die Funktion `toDateTimeOnly` , um einen Argumentwert in einen Uhrzeit-/Datumswert zu konvertieren. Bei einer ungültigen Eingabe wird als Ausgabe das Epoch-Datum zurückgegeben. Diese Funktion akzeptiert die Feldtypen string, date, long und integer.

+++Syntax

```sql
{%= toDateTimeOnly(string/date/long/int) %}: date-time
```

+++

### trim {#trim}

Die Funktion `trim` entfernt alle Leerzeichen vom Anfang und Ende einer Zeichenfolge.

+++Syntax

```sql
{%= trim(string) %}
```

+++

### Großbuchstaben {#upper}

Mit der Funktion `upperCase` wird eine Zeichenfolge in Großbuchstaben umgewandelt.

+++Syntax

```sql
{%= upperCase(string) %}
```

**Beispiel**

Mit dieser Funktion wird der Nachname des Profils in Großbuchstaben umgewandelt.

```sql
{%= upperCase(profile.person.name.lastName) %}
```

+++

### urlDecode {#url-decode}

Verwenden Sie die Funktion `urlDecode` zum Decodieren einer URL-codierten Zeichenfolge.

+++Syntax

```sql
{%= urlDecode(string) %}: string
```

+++

### urlEncode {#url-encode}

Verwenden Sie die Funktion `urlEncode` , um eine Zeichenfolge als URL zu codieren.

+++Syntax

```sql
{%= urlEncode(string) %}: string
```

+++
