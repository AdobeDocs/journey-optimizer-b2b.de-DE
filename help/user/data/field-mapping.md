---
title: XDM-Felder
description: Überprüfen Sie die standardmäßigen Attributfelder, die zwischen Adobe Experience Platform und Journey Optimizer B2B edition synchronisiert werden.
exl-id: 8c65fdec-e32d-4ba8-be7b-48522cc3dace
source-git-commit: 6578fdf35ec565ba315c00eeb3d2466c925cf816
workflow-type: tm+mt
source-wordcount: '965'
ht-degree: 24%

---

# XDM-Felder

Zielgruppendaten für Konten werden als Attribute sowohl in der XDM Business Account- als auch in der XDM Business Person-Klasse gespeichert. Die Daten werden regelmäßig zwischen Adobe Experience Platform und Journey Optimizer B2B edition synchronisiert. In den folgenden Abschnitten werden die standardmäßigen Attributsätze aufgelistet.

## XDM-Geschäftspersonalattribute

>[!IMPORTANT]
>
>Das Attribut `workEmail.Address` ist erforderlich. Wenn es für ein Mitglied der Zielgruppe &quot;Konto&quot;leer ist, wird diese Person nicht erfasst und in den Journey- und Einkaufsgruppen des Kontos, die auf die Zielgruppe verweisen, weggelassen.

| [Eigenschaft](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md) | Anzeigename | Journey Optimizer B2B-Anzeigename | Datentyp | Beschreibung |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `b2b.companyName` | Firmenname | Firmenname | String | Name des Unternehmens, mit dem eine geschäftliche Person verbunden ist. |
| `b2b.companyWebsite` | Firmenwebsite | Website | String | Website des Unternehmens, mit dem eine Geschäftsperson verbunden ist. |
| `b2b.isMarketingSuspended` | Marketing-Indikator ausgesetzt | Marketing eingestellt | Boolesch | Der Wert gibt an, ob das Marketing für die Person ausgesetzt wird. |
| `b2b.marketingSuspendedCause` | Marketing angehalten – Grund | Marketing angehalten – Grund | String | Wenn das Marketing für die Person unterbrochen wird, liefert diese Eigenschaft den Grund. |
| `b2b.personStatus` | Personen-Status | Lead-Status | String | Feld zur Aufzeichnung des aktuellen Marketing-/Verkaufsstatus der Person. |
| `consents.marketing.email.reason` | Abmeldegrund | Ursache für Abbestellung | String | Grund für die E-Mail-Abmeldung. |
| `consents.marketing.email.val` | Abbestellt | Abbestellt | String | Wenn die Abmeldung true ist (z. B. value = 1), setzen Sie `consents.marketing.email.val` auf (n). Wenn die Abmeldung false ist (z. B. value = 0), legen Sie `consents.marketing.email.val` als null fest. |
| `extendedWorkDetails.jobTitle` | Jobtitel | Jobtitel | String | Berufsbezeichnung der Person. |
| `faxPhone.number` | Zahl | Faxnummer | String | Faxnummer. |
| `mobilePhone.number` | Zahl | Mobiltelefonnummer | String | Die mit der Person verknüpfte Mobiltelefonnummer. |
| `person.birthDate` | Geburtsdatum (JJJ-MM-TT) | Geburtsdatum | String | Das vollständige Datum, an dem eine Person geboren wurde. YYYY-MM-DD |
| `person.name.courtesyTitle` | Höflichkeitstitel | Anrede | String | Normalerweise eine Abkürzung für den Titel, die Ehrlichkeit oder die Anrede einer Person. Der courtesyTitle wird in einleitenden Texten vor dem vollständigen oder Nachnamen verwendet. Zum Beispiel Herr, Frau oder Dr. |
| `person.name.firstName` | Vorname | Vorname | String | Das erste Segment des Namens in der schriftlichen Reihenfolge, das am häufigsten in der Sprache des Namens akzeptiert wird. In vielen Kulturen ist es der bevorzugte persönliche oder Vorname. Die Eigenschaften firstName und lastName wurden eingeführt, um die Kompatibilität mit vorhandenen Systemen zu gewährleisten, die Namen auf vereinfachte, nicht semantische und nicht internationalisierbare Weise modellieren. Die Verwendung von `xdm:fullName` ist immer vorzuziehen. |
| `person.name.lastName` | Nachname | Nachname | String | Das letzte Segment des Namens in der schriftlichen Reihenfolge, das am häufigsten in der Sprache des Namens akzeptiert wird. In vielen Kulturen ist es der geerbte Familienname, Nachname, Vater- oder Muttername. Die Eigenschaften firstName und lastName wurden eingeführt, um die Kompatibilität mit vorhandenen Systemen zu gewährleisten, die Namen auf vereinfachte, nicht semantische und nicht internationalisierbare Weise modellieren. Die Verwendung von `xdm:fullName` ist immer vorzuziehen. |
| `person.name.middleName` | Zweiter Vorname | Zweiter Vorname | String | Zwischen dem Vor- und dem Nachnamen angegebene mittlere, alternative oder zusätzliche Namen. |
| `workAddress.city ` | Stadt | Stadt | String | Der Name der Stadt. |
| `workAddress.country` | Land | Land | String | Der Name des von der Regierung verwalteten Gebiets. Mit Ausnahme von `xdm:countryCode` ist es ein Freiformfeld, das den Ländernamen in einer beliebigen Sprache enthalten kann. |
| `workAddress.postalCode` | Postleitzahl | Postleitzahl | String | Die Postleitzahl des Ortes. Postleitzahlen sind nicht für alle Länder verfügbar. In einigen Ländern enthält sie nur einen Teil der Postleitzahl. |
| `workAddress.state` | Land | Land | String | Der Name des Status für die Adresse. Es ist ein Freiformfeld. |
| `workAddress.street1` | Straße 1 | Adresse | String | Primäre Straßeninformationen, Wohnungsnummer, Straßennummer und Straßenname. |
| `workEmail.address` | Adresse | E-Mail-Adresse | String | **Erforderliches Feld** <br/>Die technische Adresse, z. B. `<name@domain.com>`, wie sie üblicherweise in RFC2822 und nachfolgenden Standards definiert ist. |
| `workEmail.status` | Status | E-Mail angehalten | String | Ein Hinweis auf die Möglichkeit, die E-Mail-Adresse zu verwenden. |
| `workPhone.number` | Zahl | Telefonnummer | String | Geschäftliche Telefonnummer. |

## XDM-Geschäftskontoattribute

>[!IMPORTANT]
>
>Das Attribut `accountName` ist erforderlich. Wenn es für ein Konto in einer Konto-Audience leer ist, wird dieses Konto nicht erfasst und in den Konto-Journey und Kaufgruppen, die auf die Zielgruppe verweisen, weggelassen.

| [Eigenschaft](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/account/account-details.schema.md) | Anzeigename | Journey Optimizer B2B-Anzeigename | Datentyp | Beschreibung |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `accountBillingAddress.city` | Stadt | Stadt | String | Der Name der Stadt, der in der Rechnungsadresse verwendet wird. |
| `accountBillingAddress.country` | Land | Land | String | Der Name des von der Regierung verwalteten Gebiets, das in der Rechnungsadresse verwendet wird. Mit Ausnahme von `xdm:countryCode` ist es ein Freiformfeld, das den Ländernamen in einer beliebigen Sprache enthalten kann. |
| `accountBillingAddress.postalCode` | Postleitzahl | Adresse Postleitzahl | String | Die Postleitzahl des Standorts der Rechnungsadresse. Postleitzahlen sind nicht für alle Länder verfügbar. In einigen Ländern enthält sie nur einen Teil der Postleitzahl. |
| `accountBillingAddress.region` | Region | Adressenregion | String | Die Region, der Bezirk oder der Bezirk der Abrechnungsadresse. |
| `accountBillingAddress.state` | Land | Land | String | Der Name des Bundesstaates für die Abrechnungsadresse. Es ist ein Freiformfeld. |
| `accountBillingAddress.street1` | Straße 1 | Straße 1 | String | Primäre Informationen auf Straßenebene für die Rechnungsadresse, die normalerweise die Wohnungsnummer, die Straßennummer und den Straßennamen enthalten würden. |
| `accountName` | Name | Name | **Erforderliches Feld** <br/>Zeichenfolge | Name des Unternehmens. In diesem Feld sind bis zu 255 Zeichen zulässig. |
| `accountOrganization.annualRevenue.amount` | Jahresumsatz | Jahresumsatz | Zahl | Geschätzter Betrag der jährlichen Einnahmen der Organisation. |
| `accountOrganization.industry` | Branche | Branche | String | Der Wirtschaftszweig wurde der Organisation zugeordnet. Es handelt sich um ein Freiformfeld. Es empfiehlt sich, einen strukturierten Wert für Abfragen oder die Eigenschaft `xdm:classifier` zu verwenden. |
| `accountOrganization.logoUrl` | Logo-URL | Logo-URL | String | Pfad, der mit der URL einer Salesforce-Instanz kombiniert werden soll (z. B. `https://yourInstance.salesforce.com/`), um eine URL zu generieren, mit der das Profilbild des sozialen Netzwerks abgerufen werden kann, das mit dem Konto verknüpft ist. Die generierte URL gibt eine HTTP-Umleitung (Code 302) zum Profilbild des sozialen Netzwerks für das Konto zurück. |
| `accountOrganization.numberOfEmployees` | Anzahl der Mitarbeiter | Anzahl Mitarbeiter | Ganzzahl | Die Anzahl der Mitarbeiter in der Organisation. |
| `accountOrganization.SICCode` | SIC-Code | SIC-Code | String | Der SIC-Code (Standard Industrial Classification) ist ein vierstelliger Code, der die Branchen, zu denen Unternehmen gehören, anhand ihrer Geschäftstätigkeit kategorisiert. |
| `accountOrganization.website` | Website-URL | Domänenname | String | Die URL der Website der Organisation. |
| `accountPhone.number` | Nicht zutreffend | Telefonnummer des Kontos | String | Die mit dem Konto verknüpfte Telefonnummer. |
| `accountSourceType` | Nicht zutreffend | Quellentyp | String | Source-Typ für das Konto. |
