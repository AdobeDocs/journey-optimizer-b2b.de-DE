---
title: XDM-Felder
description: Überprüfen Sie die Standardattributfelder, die zwischen Adobe Experience Platform und Journey Optimizer B2B edition synchronisiert werden.
exl-id: 8c65fdec-e32d-4ba8-be7b-48522cc3dace
source-git-commit: 9031191ead88652df95137a122f379b0ae2516a7
workflow-type: tm+mt
source-wordcount: '1346'
ht-degree: 22%

---

# XDM-Felder

Konto-Zielgruppendaten werden als Attribute sowohl in der Klasse XDM Business Account als auch in der Klasse XDM Business Person gespeichert. Die Daten werden regelmäßig zwischen Adobe Experience Platform und Journey Optimizer B2B edition synchronisiert. In den folgenden Abschnitten werden die Standardsätze von Attributen aufgeführt.

>[!TIP]
>
>Sie können XDM Business Person- und XDM Business Account-Klassen in einer Viele-zu-viele-Beziehung modellieren, indem Sie die XDM Business Account Person Relation-Klasse verwenden, wie in der [Experience Platform XDM-Dokumentation beschrieben](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/tutorials/relationship-b2b){target="_blank"}.

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

## XDM Business-Opportunity-Attribute

Darüber hinaus werden Opportunity-Daten als Attribute in der Klasse XDM Business Opportunity gespeichert, die über eine Viele-zu-eins-Beziehung mit der Klasse XDM Business Account verknüpft werden können, wie in der [Experience Platform-Dokumentation](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/tutorials/relationship-b2b#relationship-field){target="_blank"} beschrieben.

| [Eigenschaft](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/marketo/opportunity-marketo.schema.md){target="_blank"} | Anzeigename | Journey Optimizer B2B-Anzeigename | Datentyp | Beschreibung |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `expectedCloseDate` | Erwartetes Abschlussdatum | Voraussichtliches Opportunity-Abschlussdatum | String | Voraussichtliches Abschlussdatum für die Opportunity. |
| `expectedRevenue.amount` | Erwarteter Umsatz | Erwarteter Opportunity-Gesamtumsatz | String | Berechneter Umsatz basierend auf dem Betrag und der Wahrscheinlichkeit. |
| `fiscalQuarter` | Geschäftsquartal | Opportunity-Geschäftsquartal | String | Das angestrebte Geschäftsquartal für die Opportunity. |
| `fiscalYear` | Geschäftsjahr | Opportunity-Geschäftsjahr | String | Das angestrebte Geschäftsjahr für die Opportunity. |
| `forecastCategory` | Prognosekategorie | Prognosekategorie der Opportunity | String | Prognosekategorie, die durch den Wert der Opportunity-Phase bestimmt wird. |
| `forecastCategoryName` | Prognosekategoriename | Name der Opportunity-Vorhersagekategorie | String | Name der Vorhersagekategorie, der in Berichten für eine bestimmte Vorhersagekategorie angezeigt wird. |
| `isClosed` | Geschlossen-Markierung | Opportunity geschlossen | String | Markierung, die anzeigt, ob die Opportunity geschlossen ist. |
| `isWon` | Markierung „Gewonnen“ | Gewonnene Opportunity | String | Markierung, die anzeigt, ob die Opportunity gewonnen ist. |
| `lastActivityDate` | Letztes Aktivitätsdatum | Datum der letzten Aktivität | String | Datum der letzten Aktivität für die Opportunity. |
| `leadSource` | Lead-Quelle | Lead-Quelle | String | Source der Opportunity, z. B. Werbung, Partner oder Web. |
| `nextStep` | Nächster Schritt | Opportunity nächster Schritt | String | Beschreibung der nächsten Aufgabe zum Schließen der Opportunity. |
| `opportunityAmount.amount` | Opportunity-Betrag | Opportunity-Gesamtbetrag | String | Geschätzter Gesamtverkaufsbetrag für die Opportunity. |
| `opportunityDescription` | Opportunity-Beschreibung | Opportunity-Beschreibung | String | Zusätzliche Informationen zur Beschreibung der Opportunity, z. B. mögliche Produkte zum Verkauf oder frühere Käufe vom Kunden. |
| `opportunityName` | Opportunity-Name | Opportunity-Name | String | Betreff oder beschreibender Name, z. B. der erwartete Auftrag oder Firmenname, für die Opportunity. |
| `opportunityQuantity` | Opportunity-Menge | Menge der Opportunity | String | Summe aller Mengenfeldwerte für alle Produkte in der entsprechenden Produktliste für die Opportunity. |
| `opportunityStage` | Opportunity-Stadium | Opportunity-Phase | String | Verkaufsstufe der Gelegenheit, das Vertriebsteam bei seinen Bemühungen zu unterstützen, sie zu gewinnen. |
| `opportunityType` | Opportunity-Typ | Opportunity-Typ | String | Der Opportunity zugewiesener Typ, z. B. _Bestehendes Unternehmen_ oder _Neues Unternehmen_ |
| `probabilityPercentage` | Wahrscheinlichkeitsprozentsatz | Opportunity-Wahrscheinlichkeitsrate | String | Wahrscheinlichkeit, mit der die Opportunity geschlossen wird, angegeben in Prozent. |
