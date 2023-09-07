---
title: Aktualisieren Sie das Power Query-Formelelement
linktitle: Aktualisieren Sie das Power Query-Formelelement
second_title: Aspose.Cells für .NET API-Referenz
description: Erfahren Sie, wie Sie Power Query-Formelelemente in Excel-Dateien mit Aspose.Cells für .NET aktualisieren.
type: docs
weight: 160
url: /de/net/excel-workbook/update-power-query-formula-item/
---
Das Aktualisieren eines Power Query-Formelelements ist ein häufiger Vorgang beim Arbeiten mit Daten in Excel-Dateien. Mit Aspose.Cells für .NET können Sie ein Power Query-Formelelement einfach aktualisieren, indem Sie die folgenden Schritte ausführen:

## Schritt 1: Geben Sie Quell- und Ausgabeverzeichnisse an

Zunächst müssen Sie das Quellverzeichnis angeben, in dem sich die Excel-Datei mit den zu aktualisierenden Power Query-Formeln befindet, sowie das Ausgabeverzeichnis, in dem Sie die geänderte Datei speichern möchten. So machen Sie es mit Aspose.Cells:

```csharp
// Quellverzeichnis
string SourceDir = RunExamples.Get_SourceDirectory();

// Ausgabe Verzeichnis
string outputDir = RunExamples.Get_OutputDirectory();
```

## Schritt 2: Laden Sie die Excel-Quellarbeitsmappe

Als Nächstes müssen Sie die Excel-Quellarbeitsmappe laden, in der Sie das Power Query-Formelelement aktualisieren möchten. So geht's:

```csharp
// Laden Sie die Excel-Quellarbeitsmappe
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
```

## Schritt 3: Power Query-Formelelemente durchsuchen und aktualisieren

Nach dem Laden der Arbeitsmappe können Sie zur Power Query-Formelsammlung navigieren und jede Formel und ihre Elemente durchsuchen. In diesem Beispiel suchen wir nach dem Formelelement mit dem Namen „Quelle“ und aktualisieren seinen Wert. Hier ist ein Beispielcode zum Aktualisieren eines Power Query-Formelelements:

```csharp
// Greifen Sie auf die Power Query-Formelsammlung zu
DataMashup mashupData = workbook.DataMashup;

// Durchlaufen Sie Power Query-Formeln und ihre Elemente
foreach(PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
     foreach(PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
     {
         if (item.Name == "Source")
         {
             item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
         }
     }
}
```

## Schritt 4: Speichern Sie die ausgegebene Excel-Arbeitsmappe

Nachdem Sie das Power Query-Formelelement aktualisiert haben, können Sie die geänderte Excel-Arbeitsmappe im angegebenen Ausgabeverzeichnis speichern. So geht's:

```csharp
// Speichern Sie die ausgegebene Excel-Arbeitsmappe
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.\r\n");
```

### Beispielquellcode für die Aktualisierung eines Power Query-Formelelements mit Aspose.Cells für .NET 
```csharp
// Arbeitsverzeichnisse
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
DataMashup mashupData = workbook.DataMashup;
foreach (PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
	foreach (PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
	{
		if (item.Name == "Source")
		{
			item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
		}
	}
}
// Speichern Sie die Ausgabearbeitsmappe.
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.");
```

## Abschluss

Das Aktualisieren von Power Query-Formelelementen ist ein wesentlicher Vorgang, wenn Aspose.Cells zum Bearbeiten und Verarbeiten von Daten in Excel-Dateien verwendet wird. Indem Sie die oben angegebenen Schritte ausführen, können Sie Formelelemente einfach aktualisieren

### FAQs

#### F: Was ist Power Query in Excel?
     
A: Power Query ist eine Funktion in Excel, die beim Sammeln, Transformieren und Laden von Daten aus verschiedenen Quellen hilft. Es bietet leistungsstarke Tools zum Bereinigen, Kombinieren und Umformen von Daten vor dem Import in Excel.

#### F: Woher weiß ich, ob ein Power Query-Formelelement erfolgreich aktualisiert wurde?
    A: After running the Power Query Formula Item Update, you can check if the operation was successful by viewing the output and ensuring that the output Excel file was created correctly.

#### F: Kann ich mehrere Power Query-Formelelemente gleichzeitig aktualisieren?
    
A: Ja, Sie können die Power Query-Formelelementsammlung durchlaufen und je nach Ihren spezifischen Anforderungen mehrere Elemente in einer einzigen Schleife aktualisieren.

#### F: Gibt es andere Vorgänge, die ich mit Aspose.Cells an Power Query-Formeln ausführen kann?
    
A: Ja, Aspose.Cells bietet eine umfassende Palette an Funktionen für die Arbeit mit Power Query-Formeln, einschließlich des Erstellens, Löschens, Kopierens und Durchsuchens von Formeln in einer Excel-Arbeitsmappe.