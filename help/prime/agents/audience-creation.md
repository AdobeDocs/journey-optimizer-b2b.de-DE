---
title: Erstellen von Zielgruppen für Programme
description: Verwenden Sie die Fähigkeit zur Zielgruppenerstellung in Journey Optimizer B2B Prime, um Personenlisten zu erstellen, Marketo-Smart-Listen anzupassen und Listenregeln im Chat zu bearbeiten.
badgeBeta: label="Beta" type="informative" tooltip="Diese Funktion befindet sich derzeit in einer eingeschränkten Beta-Version"
autotag-review: '2026-06-25T19:19:21.361Z'
TQID: 'https://experienceleague.adobe.com/l3xd0u8LR0UDLfeGMXPEEJ9qwXPJX5DxkaH41W4Q7PE'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
  - id: bef5003b-cad2-4f40-bdb2-a80426d52ef5
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
  - id: ff10f619-348f-47e3-99bf-3ce4c817cf2c
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 0f014bd931324eb41e841a788ee4cf2058522455
workflow-type: tm+mt
source-wordcount: 1496
ht-degree: 2%

---

# Erstellen von Zielgruppen für Programme

In [!DNL Adobe Journey Optimizer B2B Prime] definieren [_Personenlisten_](../audiences/people-lists.md) die Zielgruppe für Personen-Journeys - entweder als dynamische filterbasierte Listen, die automatisch aktualisiert werden, oder als statische Listen mit fester Zugehörigkeit. In der [Chat](./chat-interface.md)Oberfläche werden mit der _Zielgruppenerstellung_ durch eine geführte Konversation Personenlisten erstellt, angepasst und bearbeitet.

* **Kenntnisse** - `audience-creation` und `people-list-comparison`
* **Aufruf** - Zielgruppenkriterien direkt beschreiben, eine [!DNL Marketo Engage] Smart-Liste hochladen oder eine vorhandene Liste zur Bearbeitung benennen
* **Lese-/Schreibvorgänge nach** - [!DNL Journey Optimizer B2B Prime]; liest [!DNL Marketo Engage] bei der Anpassung von Smart-Listen

## Unterstützte Workflows {#workflows}

Der Assistent unterstützt drei Workflows und bestimmt anhand Ihrer Anfrage, welcher Workflows angewendet wird. Wenn der Zweck mehrdeutig ist, werden Sie gefragt, bevor Sie fortfahren.

| Workflow | Einsatz | Beispiel-Eingabeaufforderung |
|---|---|---|
| **Neu erstellen** | Sie möchten eine neue Personenliste, die durch Kriterien oder Mitgliedschaft definiert ist. | _„Erstellen Sie eine dynamische Liste von VPs für Marketing bei SaaS-Unternehmen in Nordamerika._ |
| **Anpassen einer [!DNL Marketo Engage] Smart List** | Sie haben bereits eine [!DNL Marketo Engage] Smart List oder Smart Campaign und möchten eine entsprechende Personenliste. | _„Passen Sie diese Smart-Liste von Marketo in eine Personen-Liste an.“_ (Asset anhängen) |
| **Bearbeiten einer vorhandenen Liste** | Sie möchten die Regeln einer bereits vorhandenen Liste hinzufügen oder ersetzen. | _„Regel für Lead-Score über 50 zu meiner Liste &#39;Enterprise Trials&#39; hinzufügen._ |

## Erstellen einer neuen Personenliste {#create-from-scratch}

Bevor Sie etwas generieren, bestätigt der Assistent alle vier folgenden Punkte. Es fragt nach allen, die fehlen - in einer einzigen Nachricht.

1. **Regeln/Kriterien** - Eine einfache Beschreibung dessen, wer in die Liste gehört.
1. **Name** - Wie nennt man die Liste?
1. **Location** - In welchem Programm die Liste leben soll. Geben Sie einen Programmnamen an, und der Assistent findet ihn. Wenn mehrere Übereinstimmungen vorliegen, werden Sie aufgefordert, ihn auszuwählen.
1. **Type** - Dynamisch (filterbasiert, automatisch aktualisiert) oder Statisch (feste Mitgliedschaft). Dies ist erforderlich - der Assistent wird es nicht erraten; wenn Sie es nicht angeben, wird er gefragt.

### Dynamische Listen

Für dynamische Listen schlägt der Assistent proaktiv die Verwendung von Personalisierungsattributen vor, um die Zielgruppenbestimmung zu verfeinern. Diese Attribute sind **_standardmäßig enthalten - Sie schließen die Funktion ab, nicht_**:

| Attribut | Warum es hilft |
|---|---|
| **Abgeleitete Rolle** | KI-abgeleitete Käuferrolle für personalbasiertes Content-Targeting. |
| **Abgeleitete Absicht** | Abgeleitete Kaufabsichtssignale, die auf Marktkonten hindeuten. |
| **Interaktionsstufe** | Berechneter Interaktionsgrad, der interaktive Kontakte priorisiert. |

Teilen Sie dem Assistenten mit, ob Sie eine dieser Komponenten entfernen möchten, bevor der Vorgang fortgesetzt wird.

### Statische Listen

* **Statisch, keine Kriterien** - Die Liste wird leer erstellt und kann manuell hinzugefügt werden.
* **Statisch aus Kriterien (eine Momentaufnahme)** - Der KI-Assistent erstellt den passenden Satz und kopiert die Personen in . Population ist asynchron - Der Assistent bestätigt, dass die Liste erstellt wurde, merkt aber an, dass es einige Minuten dauern kann, bis Personen angezeigt werden. Sie wird nicht für sich in Anspruch nehmen, dass die Liste sofort bereit ist.

## Karte prüfen {#review-card}

Es wird nichts erstellt, bis Sie es genehmigen. Nachdem Sie Ihre Kriterien beschrieben haben, präsentiert der Assistent eine interaktive Karte _People List Creation Review_ (für Anpassungen aus [!DNL Marketo Engage] Listen heißt die Karte _People List Conversion Review_).

Jede Zeile in der Karte stellt eine Bedingung dar:

| Spalte | Bedeutung |
|---|---|
| **Anforderungen** (oder der Name der [!DNL Marketo Engage] für Anpassungen) | Ihre ursprüngliche Anfrage oder der Marketo-Quellfilter. |
| **(Regel)** | Die tatsächliche attributbasierte Regel, die für diese Bedingung generiert wurde. |
| **Einschließen** | Ein Kontrollkästchen zum Beibehalten oder Ablegen dieser Regel. |

**Konfidenzniveaus:**

* **Hohe Konfidenz** Zeilen werden sauber abgeglichen und standardmäßig aktiviert.
* **Geringe Konfidenz** Zeilen (ungefähre Zuordnungen oder alles, was gekennzeichnet ist) werden mit einem Hinweis angezeigt und sind standardmäßig deaktiviert.
* Zeilen, die das System nicht zuordnen konnte, zeigen **„Keine Entsprechung gefunden“** — diese haben keine Regel und bleiben deaktiviert.

Eine _Konversionszusammenfassung_ ergibt _N Konfidenz_ und _N Konfidenz_ mit einem Hinweis: Regeln mit geringer Konfidenz sind standardmäßig deaktiviert. Aktivieren Sie diese, um sie in den Chat einzubeziehen oder die gewünschte Änderung zu beschreiben.

**Kartenaktionen:**

* **Fortfahren** - Erstellt die Liste nur unter Verwendung der aktivierten Regeln.
* **Beschreiben Sie die gewünschten Änderungen im Chat** - Füllen Sie die Eingabe vorab mit _aus„Ich möchte Folgendes ändern: &quot;_, damit Sie verfeinern können; Der KI-Assistent generiert und zeigt eine neue Karte an, wobei die Regeln, die Sie bereits genehmigt hatten, beibehalten werden.

Sie können auch jederzeit eine Folgenachricht eingeben (z. B. _„auch auf Unternehmen mit mehr als 500 Mitarbeitern beschränken“_) und der KI-Assistent regeneriert die Karte.

## Attributzuordnung {#attribute-mapping}

Wenn Sie Kriterien beschreiben, übersetzt der Assistent jede Bedingung in ein reales, bekanntes Attribut auf Personenebene. Auf der Überprüfungskarte können drei Ergebnisse angezeigt werden:

1. **Übereinstimmung (hohe Konfidenz)** - Ihre Bedingung wird direkt einem Attribut zugeordnet (z. B. _„email is acme.com“_ wird dem `email` Attribut zugeordnet). Standardmäßig aktiviert.
1. **Annähernd (geringe Konfidenz)** - Das Attribut, das dem Namen oder Datenmodell am nächsten liegt, unterscheidet sich (z. B. ein Marketo _Betrag_-Filter, der als _Lead-Score_). Wird mit einem Hinweis angezeigt, der den Unterschied erklärt; standardmäßig deaktiviert.
1. **Nicht gefunden** — Die Bedingung konnte keinem bekannten Attribut zugeordnet werden. Wird als _Kein Äquivalent gefunden“ angezeigt_ es wird keine Regel generiert.

Deshalb kann eine Liste, die Sie beschreiben, mit weniger Regeln zurückkommen als die von Ihnen angegebenen Bedingungen - nicht übereinstimmende Bedingungen werden explizit angezeigt, anstatt im Hintergrund gelöscht zu werden. Wenn wichtige Kriterien als „not found“ (nicht gefunden) landen, formulieren Sie sie mit dem tatsächlichen Namen des Attributs um und der Assistent versucht es erneut.

>[!NOTE]
>
>Wenn Sie Tabellenspalten Feldern zuordnen (eine Feldzuordnungskarte mit _Source-Spalte_, _Zielfeld_, ein Konfidenzprozentsatz und eine _Liste Nicht zugeordnete_), ist dies der Lead-Importfluss und nicht die Erstellung von Zielgruppen. Siehe die [Import-Leads-Qualifikation](./skills.md#audiences-people).

## Regeln für eine vorhandene Liste bearbeiten {#edit-rules}

Wenn Sie darum bitten, Regeln für eine bereits vorhandene Liste zu ändern, legt der Assistent fest, welche Liste und welcher Bearbeitungsmodus verwendet werden soll:

* **Hinzufügen/Anhängen** (Standard für _„Regeln hinzufügen“_, _„Weitere Regeln hinzufügen“_) — neue Regeln werden mit den vorhandenen zusammengeführt.
* **Ersetzen** (Standard für _„Ersetzungsregeln“_, _„Regeln ändern in“_) — Neue Regeln ersetzen alle vorhandenen Regeln in der Liste.

Der Assistent fasst zusammen, was angewendet wird, gibt klar an, ob er hinzugefügt oder ersetzt wird, und bittet Sie, dies zu bestätigen, bevor er eine Bestätigung sendet. Nach der Anwendung werden die Gesamtzahl der Regeln und die Anzahl der hinzugefügten oder ersetzten Elemente angezeigt.

>[!NOTE]
>
>Bearbeitungen verwenden einen zusammenführungsfähigen Pfad, sodass ein „Hinzufügen“-Vorgang Ihre vorhandenen Regeln nie unbeaufsichtigt überschreibt.

## Zielgruppenüberschneidung {#overlap}

Bitten Sie den KI-Assistenten, zwei Personenlisten zu vergleichen (z. B. _„Überschneidung zwischen Webinar im 3. Quartal und „Unternehmenskonten“ anzeigen“_) und eine Karte _Überschneidung der_&quot; zu rendern:

* Ein Kopfzeilenabzeichen, das die Anzahl anzeigt: **&quot;{N} gemeinsam.“**
* Eine Statistikzeile mit der Gesamtzahl der Mitglieder jeder Liste und der Überschneidung als **„X% von A ・ Y% von B“.**
* Eine Mitgliedertabelle der Personen in beiden Listen mit einer Spalte **Name** und einer zweiten Spalte, die Sie steuern können - **E-Mail** (Standard), **Unternehmen** oder **Stellenbezeichnung** je nachdem, was Sie gefragt haben.
* Klicken Sie auf einen beliebigen Namen, um diese Person im Arbeitsbereich zu öffnen.
* Wenn es keine Überschneidungen gibt, sagt die Karte so deutlich: _Keine Mitglieder zwischen diesen beiden Listen.“_

**Einschränkungen:**

| Beschränkungen | Detail |
|---|---|
| **Tabellengröße** | Zeigt bis zu 200 Mitglieder; darüber hinaus wird _„Zeige 200 von N — bitte mich, die Abfrage zu verfeinern, um die Ergebnisse einzugrenzen.“_ |
| **Berechnung der Überschneidung** | Wird nach E-Mail-Adresse berechnet. Personen ohne E-Mail werden von der Schnittmenge ausgeschlossen. |
| **Listengröße** | Liest ungefähr die ersten ~1.000 Mitglieder jeder Liste aus. Bei größeren Listen gibt der Assistent an, dass die Ergebnisse unvollständig sind. |
| **Dynamische Listen als Entwurf** | Nicht vergleichbar: Eine Liste, die noch nicht veröffentlicht wurde, hat kein Live-Segment. Der Assistent fordert Sie auf, die Liste zuerst zu veröffentlichen oder stattdessen eine statische Liste zu verwenden. |

## QA-Validierung {#qa-validation}

Nach der Erstellung oder Aktualisierung einer Liste bietet der KI-Assistent Folgendes: _„Soll ich überprüfen, ob die Liste korrekt konfiguriert ist?“_ Wenn Sie akzeptieren, ruft es die Liste erneut ab und meldet die folgenden Prüfungen:

| nachprüfen | Ergebnis |
|---|---|
| Liste unter dem richtigen Programm/Ordner gefunden | Bestanden/Nicht bestanden |
| Die Filteranzahl entspricht dem angewendeten | _N_ Filter/fehlende Übereinstimmung |
| Personalization-Attribute vorhanden (falls enthalten) | Vorhanden/fehlend |
| Der Listenname entspricht den Anforderungen | Bestanden/Nicht bestanden |
| Geschätzte Mitgliederzahl | _count_ oder nicht zutreffend |

## Einschränkungen {#limitations}

| Einschränkung | Detail |
|---|---|
| **Static-list adaption von[!DNL Marketo Engage]** | Sie können eine [!DNL Marketo Engage] statische Liste (oder eine E-Mail oder ein anderes nicht gefiltertes Asset) nicht in eine Personenliste anpassen. Statische Listen sind explizite Mitglieder-IDs und können nicht als Filter ausgedrückt werden. Der Assistent fragt stattdessen nach einer Smart-Liste oder einer Smart-Kampagne. |
| **Aktivitäts- und mitgliedsbasierte Filter** | Bei der Anpassung von [!DNL Marketo Engage] haben Filter wie _E-Mail wurde geöffnet_, _Besuchte Webseite_, _Formular wurde ausgefüllt_, _Mitglied der Liste_ und _Mitglied der Smart Campaign_ keine Entsprechung in der Personenliste und werden als „Keine Entsprechung gefunden“ zurückgegeben. |
| **Bedingungen auf Unternehmensebene** | Wenn möglich, in das nächste Attribut auf Personenebene übersetzt (Personenlisten werden mit Personenattributen betrieben) und mit geringer Konfidenz gekennzeichnet, wenn die Anpassung locker ist. |
| **Tief verschachtelte UND/ODER-Logik** | Komplexe verschachtelte Logik kann auf eine UND/ODER-Ebene der obersten Ebene reduziert werden. Der Assistent merkt dies an, wenn dies geschieht. |
| **Namenskollisionen** | Nicht automatisch aufgelöst - Wenn der Name verwendet wird, fragt der Assistent Sie nach einem anderen Namen, anstatt im Hintergrund ein Suffix anzuhängen. |
| **Genehmigung erforderlich** | Der Assistent erstellt oder ändert erst dann eine Liste, wenn Sie auf **[!UICONTROL Fortfahren]** klicken, bestätigen oder eine eindeutige Genehmigung erteilen (_„genehmigt“_, _„sieht gut aus“_, _„Erstellen“_). |
| **Statische Momentaufnahme der Population** | Die Mitgliedschaft in statischen Listen, die anhand von Kriterien erstellt wurden, wird innerhalb weniger Minuten ausgefüllt - nicht sofort. |
