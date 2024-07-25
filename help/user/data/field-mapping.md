---
title: XDM-Feldzuordnung
description: Überprüfen Sie die Feldzuordnung zwischen dem AEP XDM-Schema, Marketo Engage und Journey Optimizer B2B Edition.
exl-id: 8c65fdec-e32d-4ba8-be7b-48522cc3dace
source-git-commit: 7103e4f6666482a72511661dfaed1392d4eb16b1
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 42%

---

# XDM-Feldzuordnung

Der Datenübertragungsdienst (DTS) in ist für die Synchronisierung von Daten von Adobe Experience Platform mit Journey Optimizer B2B Edition zuständig. DTS stützt sich auf Zuordnungen zwischen Experience Platform-XDM-Schemafeldern und ihren Entsprechungen in Marketo Engage.

## Standardfeldzuordnungen für XDM Business Person

| XDM-Geschäftsperson | Anzeigename für Marketo Engage Person | AJO B2B Person Display Name | XDM-Typ | Marketo-Typ | XDM-Beschreibung |
|------------------- |---------------------------------- |--------------------------- |-------- |------------ |--------------- |
| `workAddress.street1` | Adresse | Nicht zutreffend | string | Text | Primäre Straßeninformationen, Wohnungsnummer, Straßennummer und Straßenname. |
| `workAddress.city ` | Stadt | Stadt | string | string | Der Name der Stadt. |
| `b2b.companyName` | Unternehmensname | Unternehmen | string | string | Name des Unternehmens, mit dem eine geschäftliche Person verbunden ist. |
| `workAddress.country` | Land | Land | string | string | Der Name des von der Regierung verwalteten Gebiets. Mit Ausnahme von `xdm:countryCode` ist dies ein Freiformfeld, das den Ländernamen in jeder Sprache enthalten kann. |
| `person.birthDate` | Geburtsdatum | Geburtsdatum | string | Datum | Das vollständige Datum, an dem eine Person geboren wurde.  YYYY-MM-DD |
| `workEmail.address` | E-Mail-Adresse | E-Mail-Adresse | Zeichenfolge | E-Mail | Die technische Adresse, z. B. &quot;<name@domain.com>&quot;, wie sie üblicherweise in RFC2822 und nachfolgenden Standards definiert ist. |
| `workEmail.status` | E-Mail angehalten | E-Mail angehalten | string | boolean | Ein Hinweis auf die Möglichkeit, die E-Mail-Adresse zu verwenden. |
| `faxPhone.number` | Faxnummer | Nicht zutreffend | string | Telefon | Faxnummer. |
| `person.name.firstName` | Vorname | Vorname | string | string | Das erste Segment des Namens in der am häufigsten akzeptierten Schreibreihenfolge in der Sprache des Namens. In vielen Kulturen ist dies der bevorzugte persönliche oder Vorname. Die Eigenschaften firstName und lastName wurden eingeführt, um die Kompatibilität mit vorhandenen Systemen zu gewährleisten, die Namen auf vereinfachte, nicht semantische und nicht internationalisierbare Weise modellieren. Die Verwendung von xdm:fullName ist immer vorzuziehen. |
| `extendedWorkDetails.jobTitle` | Jobtitel | Jobtitel | string | string | Berufsbezeichnung der Person. |
| `person.name.lastName` | Nachname | Nachname | string | string | Das letzte Segment des Namens in der am häufigsten akzeptierten Schreibreihenfolge in der Sprache des Namens. In vielen Kulturen ist dies der geerbte Familienname, Nachname, Vater- oder Muttername. Die Eigenschaften firstName und lastName wurden eingeführt, um die Kompatibilität mit vorhandenen Systemen zu gewährleisten, die Namen auf vereinfachte, nicht semantische und nicht internationalisierbare Weise modellieren. Die Verwendung von xdm:fullName ist immer vorzuziehen. |
| `b2b.personStatus` | Lead-Status | Nicht zutreffend | string | string | Feld zur Aufzeichnung des aktuellen Marketing-/Verkaufsstatus der Person. |
| `b2b.isMarketingSuspended` | Marketing eingestellt | Nicht zutreffend | boolean | boolean | Gibt an, ob die Vermarktung für die Person ausgesetzt wurde. |
| `b2b.marketingSuspendedCause` | Marketing angehalten – Grund | Nicht zutreffend | string | string | Wenn das Marketing für die Person unterbrochen wird, liefert diese Eigenschaft den Grund. |
| `person.name.middleName` | Zweiter Vorname | Nicht zutreffend | string | Telefon | Zwischen dem Vor- und dem Nachnamen angegebene mittlere, alternative oder zusätzliche Namen. |
| `mobilePhone.number` | Mobiltelefonnummer | Mobiltelefonnummer | string | Telefon | Mobiltelefonnummer. |
| `workPhone.number` | Telefonnummer | Telefonnummer | string | Telefon | Geschäftliche Telefonnummer. |
| `workAddress.postalCode` | Postleitzahl | Postleitzahl | string | string | Die Postleitzahl des Ortes. Postleitzahlen sind nicht für alle Länder verfügbar. In einigen Ländern wird dies nur einen Teil der Postleitzahl enthalten. |
| `person.name.courtesyTitle` | Anrede | Nicht zutreffend | string | string | Normalerweise eine Abkürzung eines Personentitels, eines Ehrentitels oder einer Anrede. Der courtesyTitle wird in einleitenden Texten vor dem vollständigen oder Nachnamen verwendet. Zum Beispiel Herr, Fräulein oder Dr. |
| `workAddress.state` | Land | Land | string | string | Der Name des Staates. Dies ist ein Freiformfeld. |
| `consents.marketing.email.val` | Abbestellt | Abbestellt | string | boolean | Wenn die Abmeldung true ist (z. B. value = 1), setzen Sie `consents.marketing.email.val` auf (n). Wenn die Abmeldung &quot;false&quot;ist (z. B. Wert = 0), legen Sie &quot;consent.marketing.email.val&quot;als null fest. |
| `consents.marketing.email.reason` | Ursache für Abbestellung | Ursache für Abbestellung | string | string |  |
| `b2b.companyWebsite` | Website | Nicht zutreffend | string | URL | Website des Unternehmens, mit dem eine Geschäftsperson verbunden ist. |
