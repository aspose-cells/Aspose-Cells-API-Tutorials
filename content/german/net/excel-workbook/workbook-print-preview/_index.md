---
title: Druckvorschau der Arbeitsmappe
linktitle: Druckvorschau der Arbeitsmappe
second_title: Aspose.Cells für .NET API-Referenz
description: Erfahren Sie, wie Sie mit Aspose.Cells für .NET eine Druckvorschau einer Arbeitsmappe erstellen.
type: docs
weight: 170
url: /de/net/excel-workbook/workbook-print-preview/
---
Die Druckvorschau einer Arbeitsmappe ist eine wesentliche Funktion beim Arbeiten mit Excel-Dateien mit Aspose.Cells für .NET. Sie können ganz einfach eine Druckvorschau erstellen, indem Sie die folgenden Schritte ausführen:

## Schritt 1: Quellverzeichnis angeben

Zunächst müssen Sie das Quellverzeichnis angeben, in dem sich die Excel-Datei befindet, die Sie in der Vorschau anzeigen möchten. So geht's:

```csharp
// Quellverzeichnis
string sourceDir = RunExamples.Get_SourceDirectory();
```

## Schritt 2: Laden Sie die Arbeitsmappe

Anschließend müssen Sie die Arbeitsmappe „Workbook“ aus der angegebenen Excel-Datei laden. So geht's:

```csharp
// Laden Sie die Arbeitsmappe „Arbeitsmappe“.
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
```

## Schritt 3: Bild- und Druckoptionen konfigurieren

Bevor Sie die Druckvorschau erstellen, können Sie die Bild- und Druckoptionen nach Bedarf konfigurieren. In diesem Beispiel verwenden wir die Standardoptionen. So geht's:

```csharp
// Bild- und Druckoptionen
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
```

## Schritt 4: Generieren Sie die Druckvorschau der Arbeitsmappe

Jetzt können Sie die Druckvorschau der Workbook-Arbeitsmappe mithilfe der WorkbookPrintingPreview-Klasse generieren. So geht's:

```csharp
// Druckvorschau der Arbeitsmappe
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
```

## Schritt 5: Generieren Sie die Druckvorschau des Arbeitsblatts

Wenn Sie die Druckvorschau eines bestimmten Arbeitsblatts generieren möchten, können Sie die Klasse SheetPrintingPreview verwenden. Hier ist ein Beispiel :

```csharp
// Druckvorschau des Arbeitsblattes
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Number of worksheet pages: " + preview2.EvaluatedPageCount);
```

### Beispielquellcode für die Arbeitsmappen-Druckvorschau mit Aspose.Cells für .NET 
```csharp
//Quellverzeichnis
string sourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Worksheet page count: " + preview2.EvaluatedPageCount);
Console.WriteLine("PrintPreview executed successfully.");
```

## Abschluss

Das Generieren der Druckvorschau einer Arbeitsmappe ist eine leistungsstarke Funktion von Aspose.Cells für .NET. Wenn Sie die oben genannten Schritte ausführen, können Sie ganz einfach eine Vorschau Ihrer Excel-Arbeitsmappe anzeigen und Informationen über die Anzahl der zu druckenden Seiten erhalten.

### FAQs

#### F: Wie kann ich ein anderes Quellverzeichnis zum Laden meiner Arbeitsmappe angeben?
    
 A: Sie können das verwenden`Set_SourceDirectory` Methode, um ein anderes Quellverzeichnis anzugeben. Zum Beispiel:`RunExamples.Set_SourceDirectory("Path_to_the_source_directory")`.

#### F: Kann ich die Bild- und Druckoptionen beim Generieren der Druckvorschau anpassen?
    
 A: Ja, Sie können Bild- und Druckoptionen anpassen, indem Sie die Eigenschaften des ändern`ImageOrPrintOptions` Objekt. Sie können beispielsweise die Bildauflösung, das Ausgabedateiformat usw. festlegen.

#### F: Ist es möglich, eine Druckvorschau für mehrere Arbeitsblätter in einer Arbeitsmappe zu erstellen?
    
A: Ja, Sie können die verschiedenen Arbeitsblätter in der Arbeitsmappe durchlaufen und mithilfe von eine Druckvorschau für jedes Blatt erstellen`SheetPrintingPreview` Klasse.

#### F: Wie speichere ich die Druckvorschau als Bild oder PDF-Datei?
    
 A: Sie können verwenden`ToImage` oder`ToPdf` Methode von`WorkbookPrintingPreview` oder`SheetPrintingPreview` Objekt zum Speichern der Druckvorschau als Bild oder PDF-Datei.

#### F: Was kann ich mit der einmal erstellten Druckvorschau machen?
    
A: Sobald Sie die Druckvorschau erstellt haben, können Sie sie auf dem Bildschirm anzeigen, als Bild oder PDF-Datei speichern oder für andere Vorgänge wie den Versand per E-Mail oder den Ausdruck verwenden.
	