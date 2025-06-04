---
title: XDM-Felder
description: Überprüfen Sie die Standardattributfelder, die zwischen Adobe Experience Platform und Journey Optimizer B2B edition synchronisiert werden.
feature: Data Management, Integrations
role: User
exl-id: 8c65fdec-e32d-4ba8-be7b-48522cc3dace
source-git-commit: 9ad8ba495cdae4c88d9422f758ea912ca84e143c
workflow-type: tm+mt
source-wordcount: '1004'
ht-degree: 23%

---

# XDM-Felder

Konto-Zielgruppendaten werden als Attribute sowohl in der Klasse XDM Business Account als auch in der Klasse XDM Business Person gespeichert. Die Daten werden regelmäßig zwischen Adobe Experience Platform und Journey Optimizer B2B edition synchronisiert. In den folgenden Abschnitten werden die Standardsätze von Attributen aufgeführt.

>[!TIP]
>
>Sie können XDM Business Person- und XDM Business Account-Klassen in einer Viele-zu-viele-Beziehung modellieren, indem Sie die XDM Business Account Person Relation-Klasse verwenden, wie in der [Experience Platform XDM-Dokumentation beschrieben](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/tutorials/relationship-b2b){target="_blank"}.

## Personenbeziehungsattribute für XDM Business-Konto

| [Eigenschaft](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md){target="_blank"} | Anzeigename | Journey Optimizer B2B-Anzeigename | Datentyp | Beschreibung |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `personRoles` | Personenrollen | Rolle | Zeichenfolgen-Array | Ein Array von Rollen, die der Person im Konto zugeordnet sind, z. B. `owner, accountant, designer`. |

## XDM-Geschäftspersonenattribute

>[!IMPORTANT]
>
>Das Attribut `workEmail.Address` ist erforderlich. Wenn es für ein Mitglied der Account-Zielgruppe leer ist, wird diese Person nicht aufgenommen und in den Account-Journey und Einkaufsgruppen, die auf die Zielgruppe verweisen, weggelassen.

| [Eigenschaft](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md){target="_blank"} | Anzeigename | Journey Optimizer B2B-Anzeigename | Datentyp | Beschreibung |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `b2b.isMarketingSuspended` | Indikator für ausgesetztes Marketing | Marketing eingestellt | Boolesch | Der Wert gibt an, ob das Marketing für die Person ausgesetzt wird. |
| `b2b.marketingSuspendedCause` | Marketing angehalten – Grund | Marketing angehalten – Grund | String | Wenn das Marketing für die Person ausgesetzt wird, gibt diese Eigenschaft den Grund dafür an. |
| `b2b.personStatus` | Personen-Status | Lead-Status | String | Feld, das den aktuellen Marketing-/Verkaufsstatus der Person aufzeichnet. |
| `consents.marketing.email.reason` | Grund für die Abmeldung | Ursache für Abbestellung | String | Grund für die Abmeldung von E-Mails. |
| `consents.marketing.email.val` | Abbestellt | Abbestellt | String | Wenn die Abmeldung wahr ist (z. B. Wert = 1), dann wird `consents.marketing.email.val` als (n) festgelegt. Wenn die Abmeldung „false“ ist (z. B. Wert = 0), dann wird `consents.marketing.email.val` als null festgelegt. |
| `extendedWorkDetails.jobTitle` | Jobtitel | Jobtitel | String | Berufsbezeichnung der Person. |
| `faxPhone.number` | Zahl | Faxnummer | String | Faxnummer. |
| `mobilePhone.number` | Zahl | Mobiltelefonnummer | String | Die der Person zugeordnete Mobiltelefonnummer. |
| `person.birthDate` | Geburtsdatum (JJJJ-MM-TT) | Geburtsdatum | String | Das vollständige Datum, an dem eine Person geboren wurde. JJJJ-MM-TT |
| `person.name.courtesyTitle` | Höflichkeitstitel | Anrede | String | Normalerweise eine Abkürzung des Titels, des Ehrentitels oder der Anrede einer Person. Der Höflichkeits-Titel wird in Eröffnungstexten vor dem vollständigen Namen oder Nachnamen verwendet. Zum Beispiel Mr., Ms. oder Dr. |
| `person.name.firstName` | Vorname | Vorname | String | Das erste Segment des Namens in der geschriebenen Reihenfolge, die am häufigsten in der Sprache des Namens akzeptiert wird. In vielen Kulturen ist es der bevorzugte persönliche oder Vorname. Die Eigenschaften firstName und lastName wurden eingeführt, um die Kompatibilität mit vorhandenen Systemen zu gewährleisten, die Namen auf vereinfachte, nicht semantische und nicht internationalisierbare Weise modellieren. Die Verwendung von `xdm:fullName` ist immer vorzuziehen. |
| `person.name.lastName` | Nachname | Nachname | String | Das letzte Segment des Namens in der geschriebenen Reihenfolge, die am häufigsten in der Sprache des Namens akzeptiert wird. In vielen Kulturen ist es der vererbte Familienname, Familienname, Vatername oder Matronymname. Die Eigenschaften firstName und lastName wurden eingeführt, um die Kompatibilität mit vorhandenen Systemen zu gewährleisten, die Namen auf vereinfachte, nicht semantische und nicht internationalisierbare Weise modellieren. Die Verwendung von `xdm:fullName` ist immer vorzuziehen. |
| `person.name.middleName` | Zweiter Vorname | Zweiter Vorname | String | Zwischen dem Vor- und dem Nachnamen angegebene mittlere, alternative oder zusätzliche Namen. |
| `workAddress.city ` | Stadt | Stadt | String | Der Name der Stadt. |
| `workAddress.country` | Land | Land | String | Der Name des von der Regierung verwalteten Gebiets. Anders als `xdm:countryCode` handelt es sich um ein Freiformfeld, das den Ländernamen in einer beliebigen Sprache enthalten kann. |
| `workAddress.postalCode` | Postleitzahl | Postleitzahl | String | Die Postleitzahl des Ortes. Postleitzahlen sind nicht für alle Länder verfügbar. In einigen Ländern enthält es nur einen Teil der Postleitzahl. |
| `workAddress.state` | Land | Land | String | Der Name des Bundeslandes für die Adresse. Es handelt sich um ein Freiformfeld. |
| `workAddress.street1` | Straße 1 | Adresse | String | Primäre Straßeninformationen, Wohnungsnummer, Straßennummer und Straßenname. |
| `workEmail.address` | Adresse | E-Mail-Adresse | String | **Erforderliches Feld** <br/>Die technische Adresse, die beispielsweise in RFC2822 und nachfolgenden Standards `<name@domain.com>` definiert ist. |
| `workEmail.status` | Status | E-Mail angehalten | String | Ein Hinweis auf die Möglichkeit, die E-Mail-Adresse zu verwenden. |
| `workPhone.number` | Zahl | Telefonnummer | String | Geschäftliche Telefonnummer. |

## XDM Business-Kontoattribute

>[!IMPORTANT]
>
>Das Attribut `accountName` ist erforderlich. Wenn es für ein Konto in einer Konto-Zielgruppe leer ist, wird dieses Konto nicht aufgenommen und in den Konto-Journey und Einkaufsgruppen, die auf die Zielgruppe verweisen, weggelassen.

| [Eigenschaft](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/account/account-details.schema.md){target="_blank"} | Anzeigename | Journey Optimizer B2B-Anzeigename | Datentyp | Beschreibung |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `accountBillingAddress.city` | Stadt | Stadt | String | Der Name der Stadt, der in der Rechnungsadresse verwendet wird. |
| `accountBillingAddress.country` | Land | Land | String | Der Name des von der Regierung verwalteten Gebiets, das in der Rechnungsadresse verwendet wird. Anders als `xdm:countryCode` handelt es sich um ein Freiformfeld, das den Ländernamen in einer beliebigen Sprache enthalten kann. |
| `accountBillingAddress.postalCode` | Postleitzahl | Adresse Postleitzahl | String | Die Postleitzahl des Standorts der Rechnungsadresse. Postleitzahlen sind nicht für alle Länder verfügbar. In einigen Ländern enthält es nur einen Teil der Postleitzahl. |
| `accountBillingAddress.region` | Region | Adressbereich | String | Die Region, der Kreis oder der Bezirk der Rechnungsadresse. |
| `accountBillingAddress.state` | Land | Land | String | Der Name des Bundeslandes für die Rechnungsadresse. Es handelt sich um ein Freiformfeld. |
| `accountBillingAddress.street1` | Straße 1 | Straße 1 | String | Primäre Straßeninformationen für die Rechnungsadresse, die normalerweise die Wohnungsnummer, die Straßennummer und den Straßennamen enthalten würden. |
| `accountName` | Name | Name | String | **Erforderliches Feld** <br/>Name der Firma. In diesem Feld sind bis zu 255 Zeichen zulässig. |
| `accountOrganization.annualRevenue.amount` | Jahresumsatz | Jahresumsatz | Zahl | Geschätzte Höhe des Jahresumsatzes der Organisation. |
| `accountOrganization.industry` | Branche | Branche | String | Die der Organisation zugeschriebene Branche. Es handelt sich um ein Freiformfeld, und es wird empfohlen, einen strukturierten Wert für Abfragen zu verwenden oder die `xdm:classifier`-Eigenschaft zu verwenden. |
| `accountOrganization.logoUrl` | Logo-URL | Logo-URL | String | Pfad, der mit der URL einer Salesforce-Instanz (z. B. `https://yourInstance.salesforce.com/`) kombiniert werden soll, um eine URL zu generieren, mit der das mit dem Account verknüpfte Profilbild der Social Media angefordert werden kann. Die generierte URL gibt eine HTTP-Umleitung (Code 302) zum Profilbild der Social Media für das Konto zurück. |
| `accountOrganization.numberOfEmployees` | Anzahl der Mitarbeiter | Anzahl Mitarbeiter | Ganzzahl | Die Anzahl der Mitarbeiter in der Organisation. |
| `accountOrganization.SICCode` | SIC-Code | SIC-Code | String | Der Standard Industrial Classification (SIC)-Code ist ein vierstelliger Code, der die Wirtschaftszweige, zu denen Unternehmen gehören, anhand ihrer Geschäftstätigkeit kategorisiert. |
| `accountOrganization.website` | Website-URL | Domänenname | String | Die URL der Website der Organisation. |
| `accountPhone.number` | Nicht zutreffend | Telefonnummer des Kontos | String | Die dem Konto zugeordnete Telefonnummer. |
| `accountSourceType` | Nicht zutreffend | Quellentyp | String | Source-Typ für das Konto. |

<!-- ## XDM Business Opportunity attributes

Additionally, opportunity data is stored as attributes in the XDM Business Opportunity class, which can be associated with the XDM Business Account class through a many-to-one relationship, as described in the [Exerience Platform documentation](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/tutorials/relationship-b2b#relationship-field){target="_blank"}.

|[Property](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/marketo/opportunity-marketo.schema.md){target="_blank"} |Display name |Journey Optimizer B2B display name |Data type |Description |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
|`expectedCloseDate` | Expected Close Date  | Expected opportunity close date   | String | Expected date of closure for the opportunity.   |
|`expectedRevenue.amount` | Expected Revenue  | Total opportunity expected revenue   | String | Calculated revenue based on the Amount and Probability.   |
|`fiscalQuarter` | Fiscal Quarter   | Opportunity fiscal quarter  | String | The targeted fiscal quarter for the opportunity.   |
|`fiscalYear` | Fiscal Year   | Opportunity fiscal year   | String | The targeted fiscal year for the opportunity.   |
|`forecastCategory`|Forecast Category | Opportunity Forecast category | String | Forecast Category determined by the opportunity Stage value. |
|`forecastCategoryName`|Forecast Category Name | Opportunity forecast category name | String | Forecast category name that is displayed in reports for a particular forecast category. |
|`isClosed` | Closed Flag  | Opportunity closed   | String | Flag that indicates if the opportunity is closed.   |
|`isWon` | Won Flag  | Opportunity won   | String | Flag that indicates if the opportunity is won.  |
|`lastActivityDate` | Last Activity Date  | Last activity date   | String | Last activity date for the opportunity.  |
|`leadSource` | Lead Source  | Lead source   | String | Source of the opportunity, such as Advertisement, Partner, or Web.   |
|`nextStep` | Next Step  | Opportunity next step   | String | Description of the next task for closing the opportunity.   |
|`opportunityAmount.amount` | Opportunity Amount  | Total Opportunity Amount | String | Estimated total sale amount for the opportunity.   |
|`opportunityDescription` | Opportunity Description   | Opportunity description  |String  | Additional information to describe the opportunity, such as possible products to sell or past purchases from the customer. |
|`opportunityName` | Opportunity Name   | Opportunity name |String  | Subject or descriptive name, such as the expected order or company name, for the opportunity. |
|`opportunityQuantity` | Opportunity Quantity  | Opportunity quantity   | String | Total of all quantity field values for all products in the related Products list for the opportunity.   |
|`opportunityStage` | Opportunity Stage   | Opportunity stage   | String | Sales stage of the opportunity to aid the sales team in their efforts to win it.  |
|`opportunityType` | Opportunity Type   | Opportunity type   | String | Type assigned to the opportunity, such as _Existing Business_ or _New Business_  |
|`probabilityPercentage` | Probability Percentage  | Opportunity probability percentage  | String | Likelihood of closing the opportunity, stated as a percentage.  |
 -->