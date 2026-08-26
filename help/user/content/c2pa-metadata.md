---
title: C2PA-Metadaten
description: Erfahren Sie, wie Adobe Journey Optimizer B2B edition C2PA-Metadaten automatisch auf Bilder anwendet, die mit generativen KI-Tools generiert oder bearbeitet wurden, und was dies für Ihre Inhalte bedeutet.
feature: Assets, Content
hide: true
role: User
autotag-review: '2026-07-31T22:15:54.535Z'
TQID: 'https://experienceleague.adobe.com/9XCqPWz62uDDLFAyxARfD2jErYx2aOiOB5fAOGLLTbo'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a65c8aea-b21a-41ce-9ed7-6b517a69fd0bid: bef5003b-cad2-4f40-bdb2-a80426d52ef5id: e666e996-b2cf-4c45-8fc2-1c625212abab
subfeature_v2: id: c8402946-ff35-44c5-ab98-74c1bba0975f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 14e960aa56ce951f3606ffe35e0481c659021ad6
workflow-type: tm+mt
source-wordcount: 952
ht-degree: 0%

---

# C2PA-Metadaten

Marketing-Organisationen sind mehr denn je besorgt über Inhaltstransparenz, KI-Offenlegung und die Verhinderung von Manipulationen an Assets. Die Content Authenticity Initiative (CAI) von Adobe erstellt Tools, die dem technischen Standard [Coalition for Content Provenance and Authenticity](https://c2pa.org/specifications/specifications/1.1/specs/C2PA_Specification.html#_trust_model) (C2PA) entsprechen. _C2PA-_: sind verschlüsselte, manipulationssichere Informationen, die Betrachtern helfen, die Herkunft von Inhalten zu verstehen und die Integrität von Marken-Assets sicherzustellen. Zu diesen Informationen gehören:

* Aussteller oder Unterzeichner - Informationen über die Entität oder das Unternehmen, die bzw. das die digitale Signatur zum Zertifizieren oder Signieren des Assets ausgestellt hat.
* Anfragedatum - Das Datum, an dem die C2PA-Metadaten auf das Asset angewendet wurden.
* Kredit und Nutzung : Informationen zum Produzenten des Assets, einschließlich Name, Social-Media-Handles oder anderer identitätsbezogener Informationen.
* Prozess : Aufzeichnung von Änderungen am Asset.
* Gerätedetails - Informationen zu der App oder dem Gerät, die bzw. das zum Erstellen oder Bearbeiten des Assets verwendet wird.
* Verwendetes KI-Tool : Wenn zum Bearbeiten oder Erstellen des Assets generative KI verwendet wurde, kann der Name des verwendeten Modells einbezogen werden.
* Weitere relevante Informationen - Es können auch zusätzliche Daten aufgenommen werden, um mehr Kontext über den Verlauf eines Assets anzubieten.

Umfassende Informationen zum Asset-Verlauf erhalten Sie mit dem Adobe Content Authenticity [Inspektions-Tool](https://contentauthenticity.adobe.com/inspect).

C2PA-Metadaten bleiben in der Bilddatei erhalten. Wenn ein Bild, das mit generativer KI generiert oder bearbeitet wurde, in [!DNL Adobe Journey Optimizer B2B Edition] hochgeladen oder aus exportiert wird, bleiben seine C2PA-Metadaten erhalten.

Weitere Informationen zum automatischen Anhängen von C2PA-Metadaten an Adobe CX Enterprise-Anwendungen finden Sie unter [_Generative KI-Inhaltstransparenz_](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/overview/content-transparency){target="_blank"} im Handbuch zu KI in CX Enterprise .

>[!NOTE]
>
>Bei einigen Methoden zum Importieren von Bildern in Ihre Inhalte, z. B. beim Extrahieren eines Bildes aus einer PDF oder aus einer eingebetteten (base64) Quelle, bleiben die ursprünglichen C2PA-Metadaten möglicherweise nicht erhalten. In diesen Fällen können C2PA-Metadaten nicht aus der Quelle gelesen werden, und es wird keine für das Ergebnis erstellt.

>[!BEGINSHADEBOX]

## Persistenz von C2PA-Metadaten über Kanäle {#channels}

Wenn Sie Bilder in Ihre E-Mail- oder WhatsApp-Nachrichten einfügen, werden die C2PA-Metadaten für die bereitgestellten Bilder ebenfalls beibehalten:

* **E-**: Wenn Sie die Aktion _E-Mail senden_ Journey verwenden, fügen Sie das Bild aus der _Assets_ Bibliothek zu Ihrem E-Mail-Inhalt hinzu. Wenn die E-Mail zugestellt wird, kann der Empfänger das Bild aus der Nachricht herunterladen und die C2PA-Metadaten sind intakt.
* **WhatsApp** - Fügen Sie das Bild zu Ihrer WhatsApp-Nachrichtenvorlage in Ihrem Meta-Geschäftskonto hinzu. Sie können sie direkt von Ihrem eigenen System hinzufügen oder eine Bilddatei aus der Bibliothek _Assets_ herunterladen. Verwenden Sie die Vorlage für eine Aktion _WhatsApp senden_ Journey. Wenn die WhatsApp-Nachricht zugestellt wird, kann der Empfänger das Bild aus der Nachricht herunterladen und die C2PA-Metadaten sind intakt.

>[!ENDSHADEBOX]

## Aktionen, die C2PA-Metadaten betreffen {#cc-workflows}

>[!INFO]
>
>Im Bereich der generativen KI-Transparenz entstehen neue Gesetze, und Adobe arbeitet daran, die geltenden Anforderungen in allen Rechtssystemen zu erfüllen. C2PA-Metadaten sind das Herkunftstool, das Adobe verwendet, um die Anforderungen dieser Gesetze zu erfüllen.

Wenn Sie ein Bild mit Tools für generative KI in [!DNL Journey Optimizer B2B Edition] generieren oder bearbeiten, werden C2PA-Metadaten automatisch an dieses Bild angehängt, sodass keine Aktion Ihrerseits erforderlich ist.

### Bild erzeugen {#generate}

**_Example:_** Generieren eines Bannerbilds für eine E-Mail über eine Textaufforderung, die das gewünschte visuelle Element beschreibt. C2PA-Metadaten werden an das generierte Bild angehängt.

Wenn Sie ein neues Bild über eine Textaufforderung, ein Referenzbild oder ein ähnliches Bild erstellen, werden immer C2PA-Metadaten angehängt.

### Beschneiden eines Bildes {#crop}

**_Examples:_**

* Beschneiden Sie ein generiertes Bannerbild, damit es auf eine Web-Seite passt. Die C2PA-Metadaten werden beim Zuschneiden beibehalten.
* Verwenden Sie ein hochgeladenes Stockfoto als E-Mail-Hintergrund und schneiden Sie es so zu, dass es auf den Bildschirm passt. Wenn das Stockfoto keine generativen KI-Informationen enthält, werden keine C2PA-Metadaten erstellt.

Wenn Sie eine Anpassung an eine Bilddatei vornehmen, z. B. sie auf die angeforderten Abmessungen zuschneiden, werden die C2PA-Metadaten nur beibehalten, wenn das Quellbild bereits über sie verfügt. Beim Zuschneiden werden die Bildpixel neu erstellt, wodurch normalerweise diese C2PA-Metadaten entfernt werden, sodass der KI-Assistent sie vor dem Zuschneiden aus dem Quellbild liest, sie dann neu erstellt und erneut an das zugeschnittene Ergebnis anhängt. Beim Zuschneiden selbst wird keine neue generative KI-Aktion hinzugefügt, sondern die vorhandene beibehalten.

### Hinzufügen einer Textüberlagerung

**_Example:_** Erstellen einer Werbe-Überschrift als Textüberlagerung auf einem generierten Hintergrundbild für eine Landingpage. Die C2PA-Metadaten aus dem Hintergrundbild werden beibehalten.

Wenn Sie generierten Text über einem Hintergrundbild rendern, werden C2PA-Metadaten nur dann an das resultierende Bild angehängt, wenn das Hintergrundbild bereits C2PA-Metadaten enthält. Durch das Rendern der Überlagerung wird ein neues Bild erstellt, sodass das Bildbearbeitungs-Tool die C2PA-Metadaten aus dem Hintergrund liest und erneut an das Ergebnis anhängt. Der Überlagerungsschritt fügt keine neue generative KI-Aktion hinzu.

### Überlagern eines Bildes

**_Examples:_**

* Erstellen Sie eine E-Mail-Kopfzeile, indem Sie ein generiertes Produktbild mit einem generierten Hintergrund kombinieren. Das Ergebnis enthält C2PA-Metadaten, die beide generativen KI-Quellen widerspiegeln.
* Kombinieren Sie zwei hochgeladene Markenfotos zu einem Collage-Bild. Da keines der Quellbilder über eine generative KI-Aktion verfügt, werden keine C2PA-Metadaten erstellt.

Wenn Sie zwei oder mehr Bilder zusammenführen und eines der Quellbilder C2PA-Metadaten enthält, behält das kombinierte Bild diese bei und wird zu einem einzigen C2PA-Metadatenelement zusammengeführt. Beim Zusammensetzen wird ein neues Bild aus den Quellen erstellt, wodurch diese C2PA-Metadaten normalerweise entfernt werden. Die Bildbearbeitungs-Tools lesen jedoch die Quellmetadaten vor der Komposition und erstellen dann ein einzelnes kombiniertes C2PA-Metadatenelement, das jede Quelle auflistet, die zu einer generativen KI-Aktion beigetragen hat.

<!--

In [!DNL Adobe Journey Optimizer B2B Edition], you can see C2PA metadata directly within the _Assets_ library. When you open the asset details, any image with C2PA metadata (such as those created with GenAI services) shows the manifest details in a dedicated panel. If the asset is downloaded, published, or shared, the C2PA metadata remains intact with the asset.

_To access C2PA metadata:_

1. In the left navigation, expand **[!UICONTROL Content Management]** and select **[!UICONTROL Assets]**.

   This action opens a listing page with all the assets listed.

1. Navigate to a folder, and select the desired asset.

1. In the right panel, ??? where is it.

-->
