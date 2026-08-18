---
title: C2PA-Metadaten
description: Erfahren Sie, wie Adobe Journey Optimizer B2B Prime automatisch C2PA-Metadaten auf Bilder anwendet, die mit generativer KI generiert wurden, und was dies für Ihre Inhalte bedeutet.
feature: Assets, Content
role: User
badgeBeta: label="Beta" type="informative" tooltip="Diese Funktion ist Teil einer eingeschränkten Beta-Version."
autotag-review: '2026-07-31T22:31:06.899Z'
TQID: 'https://experienceleague.adobe.com/fBPnAmupve3xMSw5fZPQBDTUfr-rwiH2-R3wbKvox-E'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a65c8aea-b21a-41ce-9ed7-6b517a69fd0bid: e666e996-b2cf-4c45-8fc2-1c625212ababid: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1fid: c8402946-ff35-44c5-ab98-74c1bba0975f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: dd969d66eab5649ccb19fe6582dafe0b7304772c
workflow-type: tm+mt
source-wordcount: 559
ht-degree: 1%

---

# C2PA-Metadaten

Marketing-Organisationen sind mehr denn je besorgt über Inhaltstransparenz, KI-Offenlegung und die Verhinderung von Manipulationen an Assets. Die Content Authenticity Initiative (CAI) von Adobe erstellt Tools, die dem technischen Standard [Coalition for Content Provenance and Authenticity](https://c2pa.org/specifications/specifications/1.1/specs/C2PA_Specification.html#_trust_model) (C2PA) entsprechen. _C2PA-_: sind verschlüsselte, manipulationssichere Informationen, die Betrachtern helfen können, die Herkunft von Inhalten zu verstehen und die Integrität von Marken-Assets sicherzustellen. Zu diesen Informationen gehören:

* Aussteller oder Unterzeichner — Informationen über die Entität oder das Unternehmen, die bzw. das die digitale Signatur zum Zertifizieren oder Signieren des Assets ausgestellt hat.
* Ausstellungsdatum - Das Datum, an dem die C2PA-Metadaten auf das Asset angewendet wurden.
* Kredit und Nutzung — Informationen über den Produzenten des Assets, einschließlich Name, Social-Media-Handles oder andere identitätsbezogene Informationen.
* Prozess - Aufzeichnungen aller Bearbeitungen oder Änderungen am Asset.
* Gerätedetails - Informationen zu der App oder dem Gerät, die bzw. das zum Erstellen oder Bearbeiten des Assets verwendet wird.
* Verwendetes KI-Tool — Wenn generative KI zum Erstellen des Assets verwendet wurde, kann der Name des verwendeten Modells einbezogen werden.
* Weitere relevante Informationen - Es sind auch zusätzliche Daten enthalten, um mehr Kontext über den Verlauf eines Assets anzubieten.

Umfassende Informationen zum Asset-Verlauf erhalten Sie mit dem Adobe Content Authenticity [Inspektions-Tool](https://contentauthenticity.adobe.com/inspect).

C2PA-Metadaten bleiben in der Bilddatei erhalten. Wenn ein Bild, das mit generativer KI generiert oder bearbeitet wurde, in [!DNL Adobe Journey Optimizer B2B Prime] hochgeladen oder aus exportiert wird, bleiben seine C2PA-Metadaten erhalten.

>[!NOTE]
>
>Bei einigen Methoden zum Importieren von Bildern in Ihre Inhalte, z. B. beim Extrahieren eines Bildes aus einer PDF oder aus einer eingebetteten (base64) Quelle, bleiben die ursprünglichen C2PA-Metadaten möglicherweise nicht erhalten. In diesen Fällen können C2PA-Metadaten nicht aus der Quelle gelesen werden, und es wird keine für das Ergebnis erstellt.

>[!BEGINSHADEBOX]

## Persistenz von C2PA-Metadaten über Kanäle {#channels}

Wenn Sie Bilder in Ihre E-Mail- oder WhatsApp-Nachrichten einfügen, werden die C2PA-Metadaten für die bereitgestellten Bilder ebenfalls beibehalten:

* **E-**: Wenn Sie die Aktion _E-Mail senden_ Journey verwenden, fügen Sie das Bild aus der _Assets_ Bibliothek zu Ihrem E-Mail-Inhalt hinzu. Wenn die E-Mail zugestellt wird, kann der Empfänger das Bild aus der Nachricht herunterladen und die C2PA-Metadaten sind intakt.
* **WhatsApp** - Fügen Sie das Bild zu Ihrer WhatsApp-Nachrichtenvorlage in Ihrem Meta-Geschäftskonto hinzu. Sie können sie direkt von Ihrem System hinzufügen oder eine Bilddatei aus der Bibliothek _Assets_ herunterladen. Verwenden Sie die Vorlage für eine Aktion _WhatsApp senden_ Journey. Wenn die WhatsApp-Nachricht zugestellt wird, kann der Empfänger das Bild aus der Nachricht herunterladen und die C2PA-Metadaten sind intakt.

>[!ENDSHADEBOX]

## Bildgenerierung {#generate}

>[!INFO]
>
>Im Bereich der generativen KI-Transparenz entstehen neue Gesetze, und Adobe arbeitet daran, die geltenden Anforderungen in allen Rechtssystemen zu erfüllen. C2PA-Metadaten sind das Herkunftstool, das Adobe verwendet, um die Anforderungen dieser Gesetze zu erfüllen.

Wenn Sie generative KI zum Erstellen eines Bildes für Ihren E-Mail-Inhalt in [!DNL Journey Optimizer B2B Prime] verwenden, werden C2PA-Metadaten automatisch an das generierte Bild angehängt, sodass keine Aktion Ihrerseits erforderlich ist. Generative KI-Tools erstellen ein kombiniertes C2PA-Metadatenelement für Varianten von Bildern mit vorhandenen Metadaten, einschließlich der Originalquelle.

>[!NOTE]
>
>[!DNL Journey Optimizer B2B Prime] unterstützt derzeit keine manuellen Bildbearbeitungsaktionen. C2PA-Metadaten-Workflows für diese Aktionen sind derzeit nicht anwendbar.
