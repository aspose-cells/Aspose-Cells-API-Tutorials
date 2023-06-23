---
title: Extrahieren Sie die eingebettete Mol-Datei
linktitle: Extrahieren Sie die eingebettete Mol-Datei
second_title: Aspose.Cells für .NET API-Referenz
description: Erfahren Sie, wie Sie mit Aspose.Cells für .NET ganz einfach eingebettete MOL-Dateien aus einer Excel-Arbeitsmappe extrahieren.
type: docs
weight: 90
url: /de/net/excel-workbook/extract-embedded-mol-file/
---
In diesem Tutorial führen wir Sie Schritt für Schritt durch das Extrahieren einer eingebetteten MOL-Datei aus einer Excel-Arbeitsmappe mithilfe der Aspose.Cells-Bibliothek für .NET. Sie erfahren, wie Sie die Arbeitsmappenblätter durchsuchen, die entsprechenden OLE-Objekte extrahieren und die extrahierten MOL-Dateien speichern. Führen Sie die folgenden Schritte aus, um diese Aufgabe erfolgreich abzuschließen.

## Schritt 1: Definieren Sie Quell- und Ausgabeverzeichnisse
Zuerst müssen wir die Quell- und Ausgabeverzeichnisse in unserem Code definieren. Diese Verzeichnisse geben an, wo sich die Excel-Quellarbeitsmappe befindet und wo die extrahierten MOL-Dateien gespeichert werden. Hier ist der entsprechende Code:

```csharp
// Verzeichnisse
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
```

Stellen Sie sicher, dass Sie bei Bedarf die entsprechenden Pfade angeben.

## Schritt 2: Laden der Excel-Arbeitsmappe
Der nächste Schritt besteht darin, die Excel-Arbeitsmappe zu laden, die die eingebetteten OLE-Objekte und MOL-Dateien enthält. Hier ist der Code zum Laden der Arbeitsmappe:

```csharp
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
```

Stellen Sie sicher, dass Sie den Namen der Quelldatei im Code korrekt angeben.

## Schritt 3: Durchsuchen Sie die Blätter und extrahieren Sie die MOL-Dateien
Jetzt durchlaufen wir jedes Blatt in der Arbeitsmappe und extrahieren die entsprechenden OLE-Objekte, die die MOL-Dateien enthalten. Hier ist der entsprechende Code:

```csharp
var index = 1;
foreach(Worksheet sheet in workbook.Worksheets)
{
     OleObjectCollection oles = sheet.OleObjects;
     foreach(OleObject ole in oles)
     {
         string fileName = outputDir + "OleObject" + index + ".mol";
         FileStream fs = File.Create(fileName);
         fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
         fs. Close();
         index++;
     }
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

Dieser Code durchläuft jedes Blatt in der Arbeitsmappe, ruft die OLE-Objekte ab und speichert die extrahierten MOL-Dateien im Ausgabeverzeichnis.

### Beispielquellcode für „Embedded Mol File extrahieren“ mit Aspose.Cells für .NET 
```csharp
//Verzeichnisse
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
var index = 1;
foreach (Worksheet sheet in workbook.Worksheets)
{
	OleObjectCollection oles = sheet.OleObjects;
	foreach (OleObject ole in oles)
	{
		string fileName = outputDir + "OleObject" + index + ".mol ";
		FileStream fs = File.Create(fileName);
		fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
		fs.Close();
		index++;
	}
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

## Abschluss
Herzlichen Glückwunsch! Sie haben gelernt, wie Sie mit Aspose.Cells für .NET eine eingebettete MOL-Datei aus einer Excel-Arbeitsmappe extrahieren. Sie können dieses Wissen nun anwenden, um MOL-Dateien aus Ihren eigenen Excel-Arbeitsmappen zu extrahieren. Erkunden Sie die Aspose.Cells-Bibliothek weiter und erfahren Sie mehr über ihre anderen leistungsstarken Funktionen.

### FAQs

#### F: Was ist eine MOL-Datei?
 
A: Eine MOL-Datei ist ein Dateiformat, das zur Darstellung chemischer Strukturen in der Computerchemie verwendet wird. Es enthält Informationen über Atome, Bindungen und andere molekulare Eigenschaften.

#### F: Funktioniert diese Methode mit allen Excel-Dateitypen?

A: Ja, diese Methode funktioniert mit allen von Aspose.Cells unterstützten Excel-Dateitypen.

#### F: Kann ich mehrere MOL-Dateien gleichzeitig extrahieren?

A: Ja, Sie können mehrere MOL-Dateien gleichzeitig extrahieren, indem Sie die OLE-Objekte auf jedem Blatt in der Arbeitsmappe durchlaufen.