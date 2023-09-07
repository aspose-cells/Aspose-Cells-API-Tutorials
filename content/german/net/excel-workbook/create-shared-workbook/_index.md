---
title: Erstellen Sie eine freigegebene Arbeitsmappe
linktitle: Erstellen Sie eine freigegebene Arbeitsmappe
second_title: Aspose.Cells für .NET API-Referenz
description: Erstellen Sie mit Aspose.Cells für .NET eine freigegebene Excel-Arbeitsmappe, um die gleichzeitige Datenzusammenarbeit zu ermöglichen.
type: docs
weight: 70
url: /de/net/excel-workbook/create-shared-workbook/
---
In diesem Tutorial führen wir Sie durch den bereitgestellten C#-Quellcode, der es Ihnen ermöglicht, eine freigegebene Arbeitsmappe mit Aspose.Cells für .NET zu erstellen. Befolgen Sie die nachstehenden Schritte, um diesen Vorgang auszuführen.

## Schritt 1: Ausgabeverzeichnis festlegen

```csharp
// Ausgabe Verzeichnis
string outputDir = RunExamples.Get_OutputDirectory();
```

In diesem ersten Schritt definieren wir das Ausgabeverzeichnis, in dem die freigegebene Arbeitsmappe gespeichert wird.

## Schritt 2: Erstellen Sie ein Arbeitsmappenobjekt

```csharp
// Erstellen Sie ein Workbook-Objekt
Workbook wb = new Workbook();
```

Wir erstellen ein neues Workbook-Objekt, das unsere Excel-Arbeitsmappe darstellt.

## Schritt 3: Aktivieren Sie die Arbeitsmappenfreigabe

```csharp
// Teilen Sie die Arbeitsmappe
wb.Settings.Shared = true;
```

 Wir aktivieren die Freigabefunktion der Arbeitsmappe, indem wir Folgendes festlegen`Shared` Eigenschaft des Workbook-Objekts auf`true`.

## Schritt 4: Speichern Sie die freigegebene Arbeitsmappe

```csharp
// Speichern Sie die freigegebene Arbeitsmappe
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
```

Wir speichern die freigegebene Arbeitsmappe, indem wir den Pfad und Namen der Ausgabedatei angeben.

### Beispielquellcode für „Freigegebene Arbeitsmappe erstellen“ mit Aspose.Cells für .NET 
```csharp
//Ausgabe Verzeichnis
string outputDir = RunExamples.Get_OutputDirectory();
//Arbeitsmappenobjekt erstellen
Workbook wb = new Workbook();
//Teilen Sie die Arbeitsmappe
wb.Settings.Shared = true;
//Speichern Sie die freigegebene Arbeitsmappe
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
Console.WriteLine("CreateSharedWorkbook executed successfully.\r\n");
```

## Abschluss

Herzlichen Glückwunsch! Sie haben gelernt, wie Sie mit Aspose.Cells für .NET eine freigegebene Arbeitsmappe erstellen. Die freigegebene Arbeitsmappe kann von mehreren Benutzern gleichzeitig verwendet werden, um gemeinsam an Daten zu arbeiten. Experimentieren Sie mit Ihren eigenen Daten und erkunden Sie die Funktionen von Aspose.Cells weiter, um leistungsstarke und personalisierte Excel-Arbeitsmappen zu erstellen.

### FAQs

#### F: Was ist eine freigegebene Arbeitsmappe?

A: Eine freigegebene Arbeitsmappe ist eine Excel-Arbeitsmappe, die von mehreren Benutzern gleichzeitig zur Zusammenarbeit an Daten verwendet werden kann. Jeder Benutzer kann Änderungen an der Arbeitsmappe vornehmen und andere Benutzer sehen Aktualisierungen in Echtzeit.

#### F: Wie aktiviere ich die Freigabe einer Arbeitsmappe in Aspose.Cells für .NET?

 A: Um die Freigabe einer Arbeitsmappe in Aspose.Cells für .NET zu aktivieren, müssen Sie Folgendes festlegen`Shared` Eigenschaft des Workbook-Objekts auf`true`. Dadurch können Benutzer gleichzeitig an der Arbeitsmappe arbeiten.

#### F: Kann ich Benutzerberechtigungen in einer freigegebenen Arbeitsmappe einschränken?

A: Ja, Sie können Benutzerberechtigungen in einer freigegebenen Arbeitsmappe mithilfe der Sicherheitsfunktionen von Excel einschränken. Sie können für jeden Benutzer bestimmte Berechtigungen festlegen, z. B. die Möglichkeit zum Bearbeiten, nur zum Lesen usw.

#### F: Wie kann ich die Arbeitsmappe mit anderen Benutzern teilen?

A: Sobald Sie die freigegebene Arbeitsmappe erstellt haben, können Sie sie mit anderen Benutzern teilen, indem Sie ihnen die Excel-Datei senden. Andere Benutzer können die Datei öffnen und gleichzeitig daran arbeiten.

#### F: Werden alle Excel-Funktionen in einer freigegebenen Arbeitsmappe unterstützt?

A: Die meisten Excel-Funktionen werden in einer freigegebenen Arbeitsmappe unterstützt. Für einige erweiterte Funktionen wie Makros und Add-Ins können jedoch Einschränkungen oder Einschränkungen gelten, wenn sie in einer freigegebenen Arbeitsmappe verwendet werden.