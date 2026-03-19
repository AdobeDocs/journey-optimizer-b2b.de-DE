---
title: B2B-Namespaces und -Schemata
description: Konfigurieren Sie Experience Platform B2B-Namespaces und -Schemata für Journey Optimizer B2B edition mithilfe des Dienstprogramms zur automatischen Generierung von Postman.
feature: Setup, Data Management
role: Admin
source-git-commit: 023e44e1ad2baed2a5586d95a26ef8693020667a
workflow-type: tm+mt
source-wordcount: '1010'
ht-degree: 15%

---

# B2B-Namespaces und -Schemata

Das Journey Optimizer B2B edition-Setup für die vereinfachte Architektur umfasst die Konfiguration der Experience Platform-Namespaces und -Schemata, die mit B2B-Quellen verwendet werden. Das Postman-Automatisierungsdienstprogramm ist für die Generierung von B2B-Namespaces und -Schemata erforderlich.

>[!AVAILABILITY]
>
>- Sie müssen Zugriff auf [Adobe Real-Time Customer Data Platform B2B edition](https://experienceleague.adobe.com/de/docs/experience-platform/rtcdp/intro/rtcdpb2b-intro/b2b-overview){target="_blank"} haben, damit Ihre B2B-Schemata im [Echtzeit-Kundenprofil) &#x200B;](https://experienceleague.adobe.com/de/docs/experience-platform/profile/home){target="_blank"} werden können.
>
>- Ihre Experience Platform B2B-Entitäten müssen die Standardbeziehungen verwenden, die im Handbuch [B2B-Namespaces und -Schemata](https://experienceleague.adobe.com/de/docs/experience-platform/rtcdp/schemas/b2b){target="_blank"} beschrieben sind.

Überprüfen Sie die folgenden Informationen über die zugrunde liegende Einrichtung für die Namespaces und Schemas, die mit B2B-Quellen verwendet werden sollen. Außerdem enthält es Details zum Einrichten Ihres Postman-Automatisierungsprogramms, das zum Generieren von B2B-Namespaces und -Schemata erforderlich ist.

## Einrichten des Dienstprogramms zur automatischen Generierung

In den folgenden Ressourcen finden Sie die Voraussetzungen und detaillierte Informationen zum Einrichten Ihrer [!DNL Postman]-Umgebung zur Unterstützung des B2B-Namespace- und des Dienstprogramms zur automatischen Schemaerstellung.

- Laden Sie die Sammlung und Umgebung des Dienstprogramms zur automatischen Schemaerstellung aus dem GitHub[Repository &#x200B;](https://github.com/adobe/experience-platform-postman-samples/tree/master/Postman%20Collections/CDP%20Namespaces%20and%20Schemas%20Utility){target="_blank"}.
- Informationen zur Verwendung von Experience Platform-APIs, einschließlich Details zum Erfassen von Werten für erforderliche Kopfzeilen und zum Lesen von Beispiel-API-Aufrufen, finden [_unter „Erste Schritte mit Adobe Experience Platform-APIs_](https://experienceleague.adobe.com/de/docs/experience-platform/landing/platform-apis/api-guide){target="_blank"}.
- Informationen zum Generieren Ihrer Anmeldeinformationen für Experience Platform-APIs finden Sie unter [_Authentifizieren und Zugreifen auf Experience Platform-APIs_](https://experienceleague.adobe.com/de/docs/experience-platform/landing/platform-apis/api-authentication){target="_blank"}.
- Informationen zum Einrichten von [!DNL Postman] für Experience Platform-APIs finden Sie unter [_[!DNL Postman] in Adobe Experience Platform _](https://experienceleague.adobe.com/de/docs/experience-platform/landing/platform-apis/postman){target="_blank"}.

### Umgebungswerte

Wenn eine Experience Platform-Entwicklerkonsole und [!DNL Postman] eingerichtet sind, können Sie die entsprechenden Umgebungswerte auf Ihre [!DNL Postman] anwenden. Die folgende Tabelle enthält Beispielwerte und zusätzliche Informationen zum Ausfüllen Ihrer [!DNL Postman]:

| Variable | Beschreibung | Beispiel |
| --- | --- | --- |
| `CLIENT_SECRET` | Eine eindeutige Kennung, die zum Generieren Ihres `{ACCESS_TOKEN}` verwendet wird. | `{CLIENT_SECRET}` |
| `API_KEY` | Eine eindeutige Kennung, die zum Authentifizieren von Aufrufen an Experience Platform-APIs verwendet wird. | `c8d9a2f5c1e03789bd22e8efdd1bdc1b` |
| `ACCESS_TOKEN` | Das Autorisierungs-Token, das zum Abschließen von Aufrufen an Experience Platform-APIs erforderlich ist. | `Bearer {ACCESS_TOKEN}` |
| `META_SCOPE` | In Bezug auf [!DNL Journey Optimizer B2B] und [!DNL Marketo Engage] ist dieser Wert festgelegt und immer auf: `ent_dataservices_sdk` festgelegt. | `ent_dataservices_sdk` |
| `CONTAINER_ID` | Der `global`-Container enthält alle standardmäßigen von Adobe und Experience Platform bereitgestellten Partnerklassen, Schemafeldgruppen, Datentypen und Schemata. In Bezug auf [!DNL Marketo] ist dieser Wert fest und wird immer auf `global` festgelegt. | `global` |
| `TECHNICAL_ACCOUNT_ID` | Eine Berechtigung, die zur Integration mit Adobe I/O verwendet wird. | `D42AEVJZTTJC6LZADUBVPA15@techacct.adobe.com` |
| `IMS` | Das Identity Management-System (IMS) stellt das Framework für die Authentifizierung für Adobe-Services bereit. In Bezug auf [!DNL Journey Optimizer B2B] und [!DNL Marketo Engage] ist dieser Wert festgelegt und immer auf: `ims-na1.adobelogin.com` festgelegt. | `ims-na1.adobelogin.com` |
| `IMS_ORG` | Eine Unternehmenseinheit, die Produkte und Dienstleistungen besitzen oder lizenzieren und ihren Mitgliedern Zugang gewähren kann. | `ABCEH0D9KX6A7WA7ATQE0TE@adobeOrg` |
| `SANDBOX_NAME` | Der Name der virtuellen Sandbox-Partition, die Sie verwenden. | `prod` |
| `TENANT_ID` | Eine ID, mit der sichergestellt wird, dass die von Ihnen erstellten Ressourcen über den richtigen Namespace verfügen und in Ihrer Organisation enthalten sind. | `b2bcdpproductiontest` |
| `PLATFORM_URL` | Der URL-Endpunkt, an den Sie API-Aufrufe durchführen. Dieser Wert ist fest und immer auf `http://platform.adobe.io/` festgelegt. | `http://platform.adobe.io/` |

{style="table-layout:auto"}

### Skripte ausführen

Nachdem die Umgebungswerte eingerichtet sind, verwenden Sie die [!DNL Postman], um das Skript zum Erstellen der Namespaces und Schemata auszuführen. Wählen Sie den Stammordner des Dienstprogramms zur automatischen Generierung und dann **[!DNL Run]** aus der oberen Kopfzeile aus.

![Stammordner des Generators „Namespaces und Schemata“ in der Postman-Benutzeroberfläche](./assets/namespaces-schemas-postman-root-folder.png){width="500" zoomable="yes"}

Die [!DNL Runner] wird angezeigt. Stellen Sie von hier aus sicher, dass alle Kontrollkästchen aktiviert sind, und wählen Sie dann **[!DNL Run Namespaces and Schemas Autogeneration Utility]** aus.

![Postman-Benutzeroberfläche mit mehreren Anforderungen in der ausgewählten Namespaces- und Schemaauflistung.](./assets/namespaces-schemas-postman-run-generator.png){width="800" zoomable="yes"}

Bei einer erfolgreichen Anfrage werden die erforderlichen B2B-Namespaces und -Schemata erstellt.

## B2B-Namespaces

Identity-Namespaces sind eine Komponente von Experience Platform [[!DNL Identity Service]](https://experienceleague.adobe.com/de/docs/experience-platform/identity/home){target="_blank"}, die dazu dienen, den Kontext einer Identität zu unterscheiden. Eine vollqualifizierte Identität enthält einen Identitätswert und einen Namespace. Weitere [&#x200B; finden Sie unter &#x200B;](https://experienceleague.adobe.com/de/docs/experience-platform/identity/features/namespaces){target="_blank"} von Namespaces .

B2B-Namespaces werden in der primären Identität der Entität verwendet.

| Anzeigename | Identitätssymbol | Identitätstyp |
| --- | --- | --- |
| B2B-Person | `b2b_person` | `CROSS_DEVICE` |
| B2B-Konto | `b2b_account` | `B2B_ACCOUNT` |
| B2B-Opportunity | `b2b_opportunity` | `B2B_OPPORTUNITY` |
| B2B-Opportunity-Person-Beziehung | `b2b_opportunity_person_relation` | `B2B_OPPORTUNITY_PERSON` |
| B2B-Kampagne | `b2b_campaign` | `B2B_CAMPAIGN` |
| B2B-Kampagnenmitglied | `b2b_campaign_member` | `B2B_CAMPAIGN_MEMBER` |
| B2B-Marketing-Liste | `b2b_marketing_list` | `B2B_MARKETING_LIST` |
| B2B-Marketing-Listenmitglied | `b2b_marketing_list_member` | `B2B_MARKETING_LIST_MEMBER` |
| B2B-Konto-Personen-Beziehung | `b2b_account_person_relation` | `B2B_ACCOUNT_PERSON` |

{style="table-layout:auto"}

## B2B-Schemata

Schemata dienen in Experience Platform zur konsistenten und wiederverwendbaren Beschreibung der Struktur von Daten. Durch die systemübergreifende einheitliche Definition von Daten wird es einfacher, deren Bedeutung beizubehalten und somit Wert aus Daten zu ziehen.

Bevor Experience Platform Daten aufnehmen kann, muss ein Schema vorhanden sein, das die Datenstruktur beschreibt und den Datentyp einschränkt, der in den einzelnen Feldern enthalten sein kann. Schemata bestehen aus einer Basisklasse und keiner oder mehreren Schema-Feldergruppen.

Weitere Informationen zum Schemakompositionsmodell, einschließlich Planungsgrundsätzen und Best Practices, finden Sie [_Grundlagen der Schemakomposition_](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/schema/composition){target="_blank"}.

+++ B2B-Konto

<table>
    <tr>
        <td style="width: 30%;">Basisklasse</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/de/docs/experience-platform/xdm/classes/b2b/business-account" target="_blank">XDM-Geschäftskonto</a></td>
    </tr>
    <tr>
        <td>Feldergruppen</td>
        <td>XDM-Geschäftskonto – Details</td>
    </tr>
    <tr>
        <td>[!DNL Profile] im Schema</td>
        <td>Aktiviert</td>
    </tr>
    <tr>
        <td>Primäre Identität</td>
        <td><code>accountKey.sourceKey</code> in der Basisklasse</td>
    </tr>
    <tr>
        <td>Primärer Identity-Namespace</td>
        <td>B2B-Konto</td>
    </tr>
    <tr>
        <td>Sekundäre Identität</td>
        <td><code>extSourceSystemAudit.externalKey.sourceKey</code> in der Basisklasse</td>
    </tr>
    <tr>
        <td>Sekundärer Identity-Namespace</td>
        <td>B2B-Konto</td>
    </tr>
    <tr>
        <td>Beziehung</td>
        <td><ul><li><code>accountParentKey.sourceKey</code> in der Feldergruppe XDM Business-Kontodetails</li><li>Ziel-Eigenschaft: <code>/accountKey/sourceKey</code></li><li>Typ: Eins-zu-eins</li><li>Referenzschema: B2B-Konto</li><li>Namespace: B2B-Konto</li></ul> </td>
    </tr>
</table>

+++

+++ B2B-Person

<table>
    <tr>
        <td style="width: 30%;">Basisklasse</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/de/docs/experience-platform/xdm/classes/individual-profile">Individuelles XDM-Profil</a>{target=„_blank“}</td>
    </tr>
    <tr>
        <td>Feldergruppen</td>
        <td><ul><li>XDM-Geschäftspersonendetails</li><li>XDM-Geschäftspersonenkomponenten</li><li>IdentityMap</li><li>Details zu Einverständnis und Voreinstellungen</li></ul> </td>
    </tr>
    <tr>
        <td>[!DNL Profile] im Schema</td>
        <td>Aktiviert</td>
    </tr>
    <tr>
        <td>Primäre Identität</td>
        <td><code>b2b.personKey.sourceKey</code> in der Feldergruppe XDM-Geschäftspersonendetails .</td>
    </tr>
    <tr>
        <td>Primärer Identity-Namespace</td>
        <td>B2B-Person</td>
    </tr>
    <tr>
        <td>Sekundäre Identität</td>
        <td><ol><li><code>extSourceSystemAudit.externalKey.sourceKey</code> der Feldergruppe „XDM-Geschäftspersonendetails“</li><li><code>workEmail.address</code> der Feldergruppe „XDM-Geschäftspersonendetails“</li></ol></td>
    </tr>
    <tr>
        <td>Sekundärer Identity-Namespace</td>
        <td><ol><li>B2B-Person</li><li>E-Mail</li></ol></td>
    </tr>
    <tr>
        <td>Beziehung</td>
        <td><ul><li><code>personComponents.sourceAccountKey.sourceKey</code> der Feldergruppe „XDM-Geschäftspersonenkomponenten“</li><li>Typ: Viele-zu-eins</li><li>Referenzschema: B2B-Konto</li><li>Namespace: B2B-Konto</li><li>Ziel-Eigenschaft: accountKey.sourceKey</li><li>Beziehungsname aus aktuellem Schema: Konto</li><li>Beziehungsname aus Referenzschema: Personen</li></ul> </td>
    </tr>
</table>

+++

<!--

+++B2B Opportunity

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/de/docs/experience-platform/xdm/classes/b2b/business-opportunity">XDM Business Opportunity</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>XDM Business Opportunity Details</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>opportunityKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Opportunity</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td><code>extSourceSystemAudit.externalKey.sourceKey</code> in the base class</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>B2B Opportunity</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td><ul><li><code>accountKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Account</li><li>Namespace: B2B Account</li><li>Destination property: <code>accountKey.sourceKey</code></li><li>Relationship name from current schema: Account</li><li>Relationship name from reference schema: Opportunities</li></ul></td>
    </tr>
</table>

+++

+++B2B Opportunity Person Relation

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/de/docs/experience-platform/xdm/classes/b2b/business-opportunity-person-relation">XDM Business Opportunity Person Relation</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>None</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>opportunityPersonKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Opportunity Person Relation</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td> **First relationship**<ul><li><code>personKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Person</li><li>Namespace: B2B Person</li><li>Destination property: <code>b2b.personKey.sourceKey</code></li><li>Relationship name from current schema: Person</li><li>Relationship name from reference schema: Opportunities</li></ul>**Second relationship**<ul><li><code>opportunityKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Opportunity </li><li>Namespace: B2B Opportunity </li><li>Destination property: <code>opportunityKey.sourceKey</code></li><li>Relationship name from current schema: Opportunity</li><li>Relationship name from reference schema: People</li></ul> </td>
    </tr>
</table>


+++

+++B2B Campaign

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/de/docs/experience-platform/xdm/classes/b2b/business-campaign">XDM Business Campaign</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>XDM Business Campaign Details</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>campaignKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Campaign</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td>None</td>
    </tr>
</table>

+++

+++B2B Campaign Member

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/de/docs/experience-platform/xdm/classes/b2b/business-campaign-members">XDM Business Campaign Members</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>XDM Business Campaign Member Details</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>campaignMemberKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Campaign Member</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td>**First relationship**<ul><li><code>personKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Person</li><li>Namespace: B2B Person</li><li>Destination property: <code>b2b.personKey.sourceKey</code></li><li>Relationship name from current schema: Person</li><li>Relationship name from reference schema: Campaigns</li></ul>**Second relationship**<ul><li><code>campaignKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Campaign</li><li>Namespace: B2B Campaign</li><li>Destination property: <code>campaignKey.sourceKey</code></li><li>Relationship name from current schema: Campaign</li><li>Relationship name from reference schema: People</li></ul></td>
    </tr>
</table>

+++B2B Marketing List

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/de/docs/experience-platform/xdm/classes/b2b/business-marketing-list">XDM Business Marketing List</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>None</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>marketingListKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Marketing List</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td>None</td>
    </tr>
</table>

>[!NOTE]
>
>Static List in [!UICONTROL Marketo Engage] is not synced from Salesforce and therefore does not have a secondary identity.

+++

+++B2B Marketing List Member

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/de/docs/experience-platform/xdm/classes/b2b/business-marketing-list-members">XDM Business Marketing List Members</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>None</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>marketingListMemberKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Marketing List Member</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td>**First relationship**<ul><li><code>personKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Person</li><li>Namespace: B2B Person</li><li>Destination property: <code>b2b.personKey.sourceKey</code></li><li>Relationship name from current schema: Person</li><li>Relationship name from reference schema: Marketing Lists</li></ul>**Second relationship**<ul><li><code>marketingListKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Marketing List</li><li>Namespace: B2B Marketing List</li><li>Destination property: <code>marketingListKey.sourceKey</code></li><li>Relationship name from current schema: Marketing List</li><li>Relationship name from reference schema: People</li></ul></td>
    </tr>
</table>

>[!NOTE]
>
>Static List member in [!UICONTROL Marketo Engage] is not synced from Salesforce and therefore does not have a secondary identity.

+++

+++B2B Account Person Relation

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/de/docs/experience-platform/xdm/classes/b2b/business-account-person-relation">XDM Business Account Person Relation</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>Identity Map</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>accountPersonKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Account Person Relation</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td>**First relationship**<ul><li><code>personKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Person</li><li>Namespace: B2B Person</li><li>Destination property: <code>b2b.personKey.sourceKey</code></li><li>Relationship name from current schema: People</li><li>Relationship name from reference schema: Account</li></ul>**Second relationship**<ul><li><code>accountKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Account</li><li>Namespace: B2B Account</li><li>Destination property: <code>accountKey.sourceKey</code></li><li>Relationship name from current schema: Account</li><li>Relationship name from reference schema: People</li></ul></td>
    </tr>
</table>

+++

-->
