---
title: Filtern Sie definierte Namen beim Laden der Arbeitsmappe
linktitle: Filtern Sie definierte Namen beim Laden der Arbeitsmappe
second_title: Aspose.Cells für .NET API-Referenz
description: Erfahren Sie, wie Sie definierte Namen filtern, wenn Sie eine Excel-Arbeitsmappe mit Aspose.Cells für .NET laden.
type: docs
weight: 100
url: /de/net/excel-workbook/filter-defined-names-while-loading-workbook/
---
Beim Arbeiten mit Excel-Arbeitsmappen in einer .NET-Anwendung ist es häufig erforderlich, Daten beim Laden zu filtern. Aspose.Cells für .NET ist eine leistungsstarke Bibliothek zur einfachen Bearbeitung von Excel-Arbeitsmappen. In dieser Anleitung zeigen wir Ihnen, wie Sie die beim Laden einer Arbeitsmappe mit Aspose.Cells für .NET definierten Namen filtern. Befolgen Sie diese einfachen Schritte, um die gewünschten Ergebnisse zu erzielen:

## Schritt 1: Ladeoptionen festlegen

Zunächst müssen Sie die Ladeoptionen angeben, um das Ladeverhalten der Arbeitsmappe zu definieren. In unserem Fall möchten wir die beim Laden festgelegten Namen ignorieren. So machen Sie es mit Aspose.Cells:

```csharp
// Gibt Ladeoptionen an
LoadOptions opts = new LoadOptions();

// Laden Sie keine definierten Namen
opts. LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
```

## Schritt 2: Laden Sie die Arbeitsmappe

Sobald die Ladeoptionen konfiguriert sind, können Sie die Excel-Arbeitsmappe aus der Quelldatei laden. Stellen Sie sicher, dass Sie den richtigen Dateipfad angeben. Hier ist ein Beispielcode:

```csharp
// Laden Sie die Arbeitsmappe
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
```

## Schritt 3: Speichern Sie die gefilterte Arbeitsmappe

Nach dem Laden der Arbeitsmappe können Sie bei Bedarf weitere Vorgänge oder Bearbeitungen durchführen. Anschließend können Sie die gefilterte Arbeitsmappe in einer Ausgabedatei speichern. Hier ist wie:

```csharp
// Speichern Sie die gefilterte Excel-Arbeitsmappe
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
```

### Beispielquellcode zum Filtern definierter Namen beim Laden der Arbeitsmappe mit Aspose.Cells für .NET 
```csharp
//Geben Sie die Ladeoptionen an
LoadOptions opts = new LoadOptions();
//Wir möchten keine definierten Namen laden
opts.LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
//Laden Sie die Arbeitsmappe
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
//Speichern Sie die ausgegebene Excel-Datei. Dadurch wird die Formel in C1 unterbrochen
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
Console.WriteLine("FilterDefinedNamesWhileLoadingWorkbook executed successfully.");
```

## Abschluss

Das Filtern definierter Namen beim Laden einer Excel-Arbeitsmappe kann für viele Anwendungen von entscheidender Bedeutung sein. Aspose.Cells für .NET erleichtert diese Aufgabe, indem es flexible Optionen zum Laden und Filtern von Daten bietet. Wenn Sie die Schritte in dieser Anleitung befolgen, können Sie die definierten Namen effektiv herausfiltern und die gewünschten Ergebnisse in Ihren Excel-Arbeitsmappen erzielen.


### FAQs

#### F: Unterstützt Aspose.Cells neben C# auch andere Programmiersprachen?
    
A: Ja, Aspose.Cells ist eine plattformübergreifende Bibliothek, die viele Programmiersprachen wie Java, Python, C unterstützt++, und viele mehr.

#### F: Kann ich beim Laden einer Arbeitsmappe mit Aspose.Cells andere Datentypen filtern?
    
A: Ja, Aspose.Cells bietet eine Reihe von Filteroptionen für Daten, darunter Formeln, Stile, Makros usw.

#### F: Behält Aspose.Cells die Formatierung und Eigenschaften der ursprünglichen Arbeitsmappe bei?
    
A: Ja, Aspose.Cells behält Formatierungen, Stile, Formeln und andere Eigenschaften der ursprünglichen Arbeitsmappe bei, wenn mit Excel-Dateien gearbeitet wird.