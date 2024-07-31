---
title: XDM-Feldzuordnung
description: Überprüfen Sie die Feldzuordnung zwischen dem AEP XDM-Schema, Marketo Engage und Journey Optimizer B2B Edition.
exl-id: 8c65fdec-e32d-4ba8-be7b-48522cc3dace
source-git-commit: 838308621a27bcfc6425b8683f642a66f1fa6a7b
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 27%

---

# XDM-Feldzuordnung

Der Data Transfer Service (DTS) ist für die Synchronisierung von Daten von Adobe Experience Platform mit Journey Optimizer B2B Edition zuständig. DTS stützt sich auf Zuordnungen zwischen Experience Platform-XDM-Schemafeldern und ihren Entsprechungen in Marketo Engage.

## Standardfeldzuordnungen für XDM Business Person

| [XDM-Geschäftsmann](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md) | XDM-Anzeigename | Anzeigename Marketo Engage | XDM-Typ | Marketo-Typ | XDM-Beschreibung |
|------------------- |---------------------------------- |--------------------------- |-------- |------------ |--------------- |
| `b2b.companyName` | Firmenname | Firmenname | string | string | Name des Unternehmens, mit dem eine geschäftliche Person verbunden ist. |
| `b2b.companyWebsite` | Firmenwebsite | Website | string | URL | Website des Unternehmens, mit dem eine Geschäftsperson verbunden ist. |
| `b2b.isMarketingSuspended` | Marketing-Indikator ausgesetzt | Marketing eingestellt | boolean | boolean | Der Wert gibt an, ob das Marketing für die Person ausgesetzt wird. |
| `b2b.marketingSuspendedCause` | Marketing angehalten – Grund | Marketing angehalten – Grund | string | string | Wenn das Marketing für die Person unterbrochen wird, liefert diese Eigenschaft den Grund. |
| `b2b.personStatus` | Personen-Status | Lead-Status | string | string | Feld zur Aufzeichnung des aktuellen Marketing-/Verkaufsstatus der Person. |
| `consents.marketing.email.reason` | Abmeldegrund | Ursache für Abbestellung | string | string | Grund für die E-Mail-Abmeldung. |
| `consents.marketing.email.val` | Abbestellt | Abbestellt | string | boolean | Wenn die Abmeldung true ist (z. B. value = 1), setzen Sie `consents.marketing.email.val` auf (n). Wenn die Abmeldung &quot;false&quot;ist (z. B. Wert = 0), legen Sie &quot;consent.marketing.email.val&quot;als null fest. |
| `extendedWorkDetails.jobTitle` | Jobtitel | Jobtitel | string | string | Berufsbezeichnung der Person. |
| `faxPhone.number` | Zahl | Faxnummer | string | Telefon | Faxnummer. |
| `mobilePhone.number` | Zahl | Mobiltelefonnummer | string | Telefon | Die mit der Person verknüpfte Mobiltelefonnummer. |
| `person.birthDate` | Geburtsdatum (JJJ-MM-TT) | Geburtsdatum | string | Datum | Das vollständige Datum, an dem eine Person geboren wurde. YYYY-MM-DD |
| `person.name.courtesyTitle` | Höflichkeitstitel | Anrede | string | string | Normalerweise eine Abkürzung für den Titel, die Ehrlichkeit oder die Anrede einer Person. Der courtesyTitle wird in einleitenden Texten vor dem vollständigen oder Nachnamen verwendet. Zum Beispiel Herr, Frau oder Dr. |
| `person.name.firstName` | Vorname | Vorname | string | string | Das erste Segment des Namens in der schriftlichen Reihenfolge, das am häufigsten in der Sprache des Namens akzeptiert wird. In vielen Kulturen ist es der bevorzugte persönliche oder Vorname. Die Eigenschaften firstName und lastName wurden eingeführt, um die Kompatibilität mit vorhandenen Systemen zu gewährleisten, die Namen auf vereinfachte, nicht semantische und nicht internationalisierbare Weise modellieren. Die Verwendung von `xdm:fullName` ist immer vorzuziehen. |
| `person.name.lastName` | Nachname | Nachname | string | string | Das letzte Segment des Namens in der schriftlichen Reihenfolge, das am häufigsten in der Sprache des Namens akzeptiert wird. In vielen Kulturen ist es der geerbte Familienname, Nachname, Vater- oder Muttername. Die Eigenschaften firstName und lastName wurden eingeführt, um die Kompatibilität mit vorhandenen Systemen zu gewährleisten, die Namen auf vereinfachte, nicht semantische und nicht internationalisierbare Weise modellieren. Die Verwendung von `xdm:fullName` ist immer vorzuziehen. |
| `person.name.middleName` | Zweiter Vorname | Zweiter Vorname | string | Telefon | Zwischen dem Vor- und dem Nachnamen angegebene mittlere, alternative oder zusätzliche Namen. |
| `workAddress.city ` | Stadt | Stadt | string | string | Der Name der Stadt. |
| `workAddress.country` | Land | Land | string | string | Der Name des von der Regierung verwalteten Gebiets. Mit Ausnahme von `xdm:countryCode` ist es ein Freiformfeld, das den Ländernamen in einer beliebigen Sprache enthalten kann. |
| `workAddress.postalCode` | Postleitzahl | Postleitzahl | string | string | Die Postleitzahl des Ortes. Postleitzahlen sind nicht für alle Länder verfügbar. In einigen Ländern enthält sie nur einen Teil der Postleitzahl. |
| `workAddress.state` | Land | Land | string | string | Der Name des Status für die Adresse. Es ist ein Freiformfeld. |
| `workAddress.street1` | Straße 1 | Adresse | string | Text | Primäre Straßeninformationen, Wohnungsnummer, Straßennummer und Straßenname. |
| `workEmail.address` | Adresse | E-Mail-Adresse | Zeichenfolge | E-Mail | Die technische Adresse, z. B. `<name@domain.com>`, wie sie üblicherweise in RFC2822 und nachfolgenden Standards definiert ist. |
| `workEmail.status` | Status | E-Mail angehalten | string | boolean | Ein Hinweis auf die Möglichkeit, die E-Mail-Adresse zu verwenden. |
| `workPhone.number` | Zahl | Telefonnummer | string | Telefon | Geschäftliche Telefonnummer. |

## Standardfeldzuordnungen für XDM-Geschäftskonten

| [XDM-Geschäftskonto](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/account/account-details.schema.md) | XDM-Anzeigename | Anzeigename Marketo Engage | XDM-Typ | Marketo Engage-Typ | XDM-Beschreibung |
|------------------- |---------------------------------- |--------------------------- |-------- |------------ |--------------- |
| `accountBillingAddress.city` | Stadt | Stadt | string | string | Der Name der Stadt, der in der Rechnungsadresse verwendet wird. |
| `accountBillingAddress.country` | Land | Land | string | string | Der Name des von der Regierung verwalteten Gebiets, das in der Rechnungsadresse verwendet wird. Mit Ausnahme von `xdm:countryCode` ist es ein Freiformfeld, das den Ländernamen in einer beliebigen Sprache enthalten kann. |
| `accountBillingAddress.postalCode` | Postleitzahl | Adresse Postleitzahl | string | string | Die Postleitzahl des Standorts der Rechnungsadresse. Postleitzahlen sind nicht für alle Länder verfügbar. In einigen Ländern enthält sie nur einen Teil der Postleitzahl. |
| `accountBillingAddress.region` | Region | Adressenregion | string | string | Die Region, der Bezirk oder der Bezirk der Abrechnungsadresse. |
| `accountBillingAddress.state` | Land | Land | string | string | Der Name des Bundesstaates für die Abrechnungsadresse. Es ist ein Freiformfeld. |
| `accountBillingAddress.street1` | Straße 1 | Straße 1 | string | string | Primäre Informationen auf Straßenebene für die Rechnungsadresse, die normalerweise die Wohnungsnummer, die Straßennummer und den Straßennamen enthalten würden. |
| `accountName` | Name | Name | string | string | Name des Unternehmens. In diesem Feld sind bis zu 255 Zeichen zulässig. |
| `accountOrganization.annualRevenue.amount` | Jahresumsatz | Jahresumsatz | number | currency | Geschätzter Betrag der jährlichen Einnahmen der Organisation. |
| `accountOrganization.industry` | Branche | Branche | string | string | Der Wirtschaftszweig wurde der Organisation zugeordnet. Es handelt sich um ein Freiformfeld. Es empfiehlt sich, einen strukturierten Wert für Abfragen oder die Eigenschaft `xdm:classifier` zu verwenden. |
| `accountOrganization.logoUrl` | Logo-URL | Logo-URL | string | string | Pfad, der mit der URL einer Salesforce-Instanz kombiniert werden soll (z. B. `https://yourInstance.salesforce.com/`), um eine URL zu generieren, mit der das mit dem Konto verknüpfte Profilbild des sozialen Netzwerks angefordert wird. Die generierte URL gibt eine HTTP-Umleitung (Code 302) zum Profilbild des sozialen Netzwerks für das Konto zurück. |
| `accountOrganization.numberOfEmployees` | Anzahl der Mitarbeiter | Anzahl Mitarbeiter | integer | integer | Die Anzahl der Mitarbeiter in der Organisation. |
| `accountOrganization.SICCode` | SIC-Code | SIC-Code | string | string | Der SIC-Code (Standard Industrial Classification) ist ein vierstelliger Code, der die Branchen, zu denen Unternehmen gehören, anhand ihrer Geschäftstätigkeit kategorisiert. |
| `accountOrganization.website` | Website-URL | Domänenname | string | string | Die URL der Website der Organisation. |
| `accountPhone.number` | Nicht zutreffend | Telefonnummer des Kontos | string | string | Die mit dem Konto verknüpfte Telefonnummer. |
| `accountSourceType` | Nicht zutreffend | Quellentyp | string | string | Source-Typ für das Konto. |
