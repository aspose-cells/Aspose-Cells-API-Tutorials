---
title: Arbeiten mit Inhaltstypeigenschaften
linktitle: Arbeiten mit Inhaltstypeigenschaften
second_title: Aspose.Cells für .NET API-Referenz
description: Erfahren Sie, wie Sie mit Aspose.Cells für .NET mit Inhaltstypeigenschaften arbeiten.
type: docs
weight: 180
url: /de/net/excel-workbook/working-with-content-type-properties/
---
Inhaltstypeigenschaften spielen eine wichtige Rolle bei der Verwaltung und Bearbeitung von Excel-Dateien mithilfe der Aspose.Cells-Bibliothek für .NET. Mit diesen Eigenschaften können Sie zusätzliche Metadaten für Excel-Dateien definieren und so die Organisation und Suche von Daten erleichtern. In diesem Tutorial führen wir Sie Schritt für Schritt durch das Verständnis und die Arbeit mit Inhaltstypeigenschaften mithilfe von C#-Beispielcode.

## Voraussetzungen

Bevor Sie beginnen, stellen Sie sicher, dass Sie über Folgendes verfügen:

- Aspose.Cells für .NET ist auf Ihrem Entwicklungscomputer installiert.
- Eine integrierte Entwicklungsumgebung (IDE), die mit C# kompatibel ist, z. B. Visual Studio.

## Schritt 1: Einrichten der Umgebung

Bevor Sie mit der Arbeit mit Inhaltstypeigenschaften beginnen, stellen Sie sicher, dass Sie Ihre Entwicklungsumgebung mit Aspose.Cells für .NET eingerichtet haben. Sie können den Verweis auf die Aspose.Cells-Bibliothek in Ihrem Projekt hinzufügen und den erforderlichen Namespace in Ihre Klasse importieren.

```csharp
using Aspose.Cells;
```

## Schritt 2: Erstellen einer neuen Excel-Arbeitsmappe

 Zuerst erstellen wir eine neue Excel-Arbeitsmappe mit`Workbook`Klasse, bereitgestellt von Aspose.Cells. Der folgende Code zeigt, wie Sie eine neue Excel-Arbeitsmappe erstellen und in einem angegebenen Ausgabeverzeichnis speichern.

```csharp
// Zielverzeichnis
string outputDir = RunExamples.Get_OutputDirectory();

// Erstellen Sie eine neue Excel-Arbeitsmappe
Workbook workbook = new Workbook(FileFormatType.Xlsx);
```

## Schritt 3: Inhaltstypeigenschaften hinzufügen

 Da wir nun über unsere Excel-Arbeitsmappe verfügen, können wir mithilfe von Inhaltstypeigenschaften hinzufügen`Add` Methode der`ContentTypeProperties` Sammlung der`Workbook` Klasse. Jede Eigenschaft wird durch einen Namen und einen Wert dargestellt. DU

  Sie können auch den Datentyp der Eigenschaft angeben.

```csharp
// Fügen Sie die erste Inhaltstypeigenschaft hinzu
int index = workbook.ContentTypeProperties.Add("MK31", "Simple Data");
workbook.ContentTypeProperties[index].IsNillable = false;

// Fügen Sie die zweite Inhaltstypeigenschaft hinzu
index = workbook.ContentTypeProperties.Add("MK32", DateTime.Now.ToString("yyyy-MM-dd'T'hh:mm:ss"), "DateTime");
workbook.ContentTypeProperties[index].IsNillable = true;
```

## Schritt 4: Speichern der Excel-Arbeitsmappe

 Nachdem wir die Inhaltstypeigenschaften hinzugefügt haben, können wir die Excel-Arbeitsmappe mit den Änderungen speichern. Benutzen Sie die`Save` Methode der`Workbook` Klasse, um das Ausgabeverzeichnis und den Dateinamen anzugeben.

```csharp
// Speichern Sie die Excel-Arbeitsmappe
workbook.Save(outputDir + "WorkingWithContentTypeProperties_out.xlsx");
```

### Beispielquellcode für das Arbeiten mit Inhaltstypeigenschaften mithilfe von Aspose.Cells für .NET 
```csharp
//Quellverzeichnis
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(FileFormatType.Xlsx);
int index = workbook.ContentTypeProperties.Add("MK31", "Simple Data");
workbook.ContentTypeProperties[index].IsNillable = false;
index = workbook.ContentTypeProperties.Add("MK32", DateTime.Now.ToString("yyyy-MM-dd'T'hh:mm:ss"), "DateTime");
workbook.ContentTypeProperties[index].IsNillable = true;
workbook.Save(outputDir + "WorkingWithContentTypeProperties_out.xlsx");
Console.WriteLine("WorkingWithContentTypeProperties executed successfully.");
```

## Abschluss

Herzlichen Glückwunsch! Sie haben gelernt, wie Sie mit Aspose.Cells für .NET mit Inhaltstypeigenschaften arbeiten. Jetzt können Sie Ihren Excel-Dateien benutzerdefinierte Metadaten hinzufügen und diese effizienter verwalten.

### FAQs

#### F: Sind Inhaltstypeigenschaften mit allen Excel-Versionen kompatibel?

A: Ja, Inhaltstypeigenschaften sind mit Excel-Dateien kompatibel, die in allen Excel-Versionen erstellt wurden.

#### F: Kann ich Inhaltstypeigenschaften bearbeiten, nachdem ich sie zur Excel-Arbeitsmappe hinzugefügt habe?

 A: Ja, Sie können die Eigenschaften des Inhaltstyps jederzeit ändern, indem Sie auf gehen`ContentTypeProperties` Sammlung der`Workbook` Klasse und Verwendung der und p-Methoden entsprechender Eigenschaften.

#### F: Werden Inhaltstypeigenschaften beim Speichern als PDF unterstützt?

A: Nein, Inhaltstypeigenschaften werden beim Speichern als PDF nicht unterstützt. Sie sind spezifisch für Excel-Dateien.