---
title: Regex ersetzen
linktitle: Regex ersetzen
second_title: Aspose.Cells für .NET API-Referenz
description: Erfahren Sie, wie Sie mit Aspose.Cells für .NET eine Regex-Ersetzung in Excel-Dateien durchführen.
type: docs
weight: 140
url: /de/net/excel-workbook/regex-replace/
---
Textersetzung auf Basis regulärer Ausdrücke (Regex) ist eine häufige Aufgabe bei der Bearbeitung von Daten in Excel-Dateien. Mit Aspose.Cells für .NET können Sie ganz einfach einen Regex-Ersatz durchführen, indem Sie die folgenden Schritte ausführen:

## Schritt 1: Geben Sie das Quellverzeichnis und das Ausgabeverzeichnis an

Zunächst müssen Sie das Quellverzeichnis angeben, in dem sich die Excel-Datei mit den zu ersetzenden Daten befindet, sowie das Ausgabeverzeichnis, in dem Sie die geänderte Datei speichern möchten. So machen Sie es mit Aspose.Cells:

```csharp
// Quellverzeichnis
string sourceDir = RunExamples.Get_SourceDirectory();

// Ausgabe Verzeichnis
string outputDir = RunExamples.Get_OutputDirectory();
```

## Schritt 2: Laden Sie die Excel-Quelldatei

Als Nächstes müssen Sie die Excel-Quelldatei laden, für die Sie die Regex-Ersetzung durchführen möchten. So geht's:

```csharp
// Laden Sie die Excel-Quelldatei
Workbook workbook = new Workbook(sourceDir + "SampleRegexReplace.xlsx");
```

## Schritt 3: Regex-Ersetzung durchführen

Nach dem Hochladen der Datei können Sie Ersetzungsoptionen festlegen, einschließlich der Berücksichtigung der Groß-/Kleinschreibung und der genauen Übereinstimmung des Zellinhalts. Hier ist ein Beispielcode zum Durchführen der Regex-Ersetzung:

```csharp
// Ersetzungsoptionen festlegen
ReplaceOptions replace = new ReplaceOptions();
replace.CaseSensitive = false;
replace.MatchEntireCellContents = false;

// Definieren Sie, dass der Suchschlüssel ein regulärer Ausdruck ist
replace. RegexKey = true;

// Führen Sie einen Regex-Ersatz durch
workbook. Replace("\\bKIM\\b", "^^^TIM^^^", replace);
```

## Schritt 4: Speichern Sie die ausgegebene Excel-Datei

Sobald die Regex-Ersetzung abgeschlossen ist, können Sie die geänderte Excel-Datei im angegebenen Ausgabeverzeichnis speichern. So geht's:

```csharp
// Speichern Sie die ausgegebene Excel-Datei
workbook.Save(outputDir + "RegexReplace_out.xlsx");
Console.WriteLine("RegexReplace executed successfully.\r\n");
```

### Beispielquellcode für Regex Replacement mit Aspose.Cells für .NET 
```csharp
//Quellverzeichnis
string sourceDir = RunExamples.Get_SourceDirectory();
//Ausgabe Verzeichnis
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "SampleRegexReplace.xlsx");
ReplaceOptions replace = new ReplaceOptions();
replace.CaseSensitive = false;
replace.MatchEntireCellContents = false;
// Auf „true“ setzen, um anzugeben, dass der gesuchte Schlüssel ein regulärer Ausdruck ist
replace.RegexKey = true;
workbook.Replace("\\bKIM\\b", "^^^TIM^^^", replace);
workbook.Save(outputDir + "RegexReplace_out.xlsx");
Console.WriteLine("RegexReplace executed successfully.");
```

## Abschluss

Die Regex-Ersetzung ist eine leistungsstarke Technik zum dynamischen Ändern von Daten in einer Excel-Datei. Mit Aspose.Cells für .NET können Sie ganz einfach einen Regex-Ersatz durchführen, indem Sie die oben beschriebenen Schritte ausführen. Experimentieren Sie mit Ihren eigenen regulären Ausdrücken und nutzen Sie die Flexibilität von Aspose.Cells.

### FAQs

#### F: Was ist Regex-Ersatz?
    
A: Regex-Ersetzung ist eine Technik zum Ersetzen von Textmustern basierend auf regulären Ausdrücken in einer Excel-Datei. Dies ermöglicht schnelle und genaue Änderungen an den Daten.

#### F: Ist beim Regex-Ersatz die Groß-/Kleinschreibung beachtet?
    
A: Nein, mit Aspose.Cells können Sie festlegen, ob bei der Regex-Ersetzung die Groß-/Kleinschreibung beachtet werden soll oder nicht. Sie haben die volle Kontrolle über diese Funktion.

#### F: Wie kann ich beim Ersetzen von Regex eine genaue Übereinstimmung des Zellinhalts angeben?
    
A: Mit Aspose.Cells können Sie festlegen, ob die Regex-Ersetzung genau mit dem Zellinhalt übereinstimmen soll oder nicht. Sie können diese Option entsprechend Ihren Bedürfnissen anpassen.

#### F: Kann ich erweiterte reguläre Ausdrücke verwenden, wenn ich Regex durch Aspose.Cells ersetze?
    
A: Ja, Aspose.Cells unterstützt erweiterte reguläre Ausdrücke, sodass Sie komplexe und anspruchsvolle Ersetzungen in Ihren Excel-Dateien durchführen können.

#### F: Wie kann ich überprüfen, ob der Regex-Ersatz erfolgreich war?
    
A: Nachdem Sie die Regex-Ersetzung durchgeführt haben, können Sie überprüfen, ob der Vorgang erfolgreich war, indem Sie die Ausgabe überprüfen und sicherstellen, dass die Excel-Ausgabedatei korrekt erstellt wurde.
	