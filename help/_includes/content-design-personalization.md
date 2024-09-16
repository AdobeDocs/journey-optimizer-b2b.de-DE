---
title: Inhaltserstellung - Personalisierung
description: Wiederverwendeter Abschnitt zur Verwendung der Personalisierung für die Inhaltserstellung
source-git-commit: 0a9c05ac2ddd95e1fa5321f44f5cbe8cfa595007
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 2%

---

# Inhaltserstellung - Personalisierung

Journey Optimizer B2B Edition verwendet eine einfache Inline-Syntax, mit der Sie Ausdrücke mit personalisierten Inhalten erstellen können, die durch doppelte geschweifte Klammern `{}` eingeschlossen sind. Sie können im selben Inhalt oder Feld mehrere Ausdrücke ohne Einschränkungen hinzufügen.

Beispiele:

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`

* `Hello {{profile.person.name.fullName}}`

Bei der Verarbeitung der Nachricht (E-Mail und SMS) ersetzt Journey Optimizer B2B Edition den Ausdruck durch die in der Experience Platform-Datenbank enthaltenen Daten. Das erste Beispiel lautet also _Hallo, Max Mustermann_.

Im folgenden Beispiel werden Schritte zum Personalisieren von Inhalten mit Lead-/Kontoattributen und System-Token beschrieben.

1. Wählen Sie die Textkomponente aus und klicken Sie in der Symbolleiste auf das Symbol _Personalisierung hinzufügen_ .

   ![Klicken Sie auf das Personalisierungssymbol](../assets/content-design-shared/visual-designer-personalize-icon.png){width="600"}

   Dadurch wird das Dialogfeld _Personalization bearbeiten_ geöffnet.

1. Klicken Sie auf **+** oder **...** , um dem leeren Bereich ein Token hinzuzufügen.

   ![Erstellen von personalisiertem Text mithilfe von Token](../assets/content-design-shared/visual-designer-personalize-dialog.png){width="700" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Speichern]**.
