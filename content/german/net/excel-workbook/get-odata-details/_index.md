---
title: Holen Sie sich Odata-Details
linktitle: Holen Sie sich Odata-Details
second_title: Aspose.Cells für .NET API-Referenz
description: Erfahren Sie, wie Sie mit Aspose.Cells für .NET OData-Details aus einer Excel-Arbeitsmappe abrufen.
type: docs
weight: 110
url: /de/net/excel-workbook/get-odata-details/
---
Der Einsatz von OData ist üblich, wenn es darum geht, strukturierte Daten aus externen Datenquellen abzurufen. Mit Aspose.Cells für .NET können Sie OData-Details ganz einfach aus einer Excel-Arbeitsmappe abrufen. Befolgen Sie die folgenden Schritte, um die gewünschten Ergebnisse zu erzielen:

## Schritt 1: Quellverzeichnis angeben

Zunächst müssen Sie das Quellverzeichnis angeben, in dem sich die Excel-Datei mit den OData-Details befindet. So machen Sie es mit Aspose.Cells:

```csharp
// Quellverzeichnis
string SourceDir = RunExamples.Get_SourceDirectory();
```

## Schritt 2: Laden Sie die Arbeitsmappe

Sobald das Quellverzeichnis angegeben ist, können Sie die Excel-Arbeitsmappe aus der Datei laden. Hier ist ein Beispielcode:

```csharp
// Laden Sie die Arbeitsmappe
Workbook workbook = new Workbook(SourceDir + "ODataSample.xlsx");
```

## Schritt 3: Rufen Sie die OData-Details ab

Nach dem Laden der Arbeitsmappe können Sie mithilfe der PowerQueryFormulas-Sammlung auf die OData-Details zugreifen. Hier ist wie:

```csharp
// Rufen Sie die Sammlung von Power Query-Formeln ab
PowerQueryFormulaCollction PQFcoll = workbook.DataMashup.PowerQueryFormulas;

// Gehen Sie jede Power Query-Formel durch
foreach(PowerQueryFormula PQF in PQFcoll)
{
Console.WriteLine("Connection name: " + PQF.Name);

// Rufen Sie die Sammlung von Power Query-Formelelementen ab
PowerQueryFormulaItemCollection PQFIcoll = PQF.PowerQueryFormulaItems;

// Durchlaufen Sie jedes Power Query-Formelelement
foreach (PowerQueryFormulaItem PQFI in PQFIcoll)
{
Console.WriteLine("Name: " + PQFI.Name);
Console.WriteLine("Value: " + PQFI.Value);
}
}

Console.WriteLine("GetOdataDetails executed successfully.");
```

### Beispielquellcode zum Abrufen von Odata-Details mit Aspose.Cells für .NET 
```csharp
// Quellverzeichnis
string SourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(SourceDir + "ODataSample.xlsx");
PowerQueryFormulaCollction PQFcoll = workbook.DataMashup.PowerQueryFormulas;
foreach (PowerQueryFormula PQF in PQFcoll)
{
	Console.WriteLine("Connection Name: " + PQF.Name);
	PowerQueryFormulaItemCollection PQFIcoll = PQF.PowerQueryFormulaItems;
	foreach (PowerQueryFormulaItem PQFI in PQFIcoll)
	{
		Console.WriteLine("Name: " + PQFI.Name);
		Console.WriteLine("Value: " + PQFI.Value);
	}
}
Console.WriteLine("GetOdataDetails executed successfully.");
```

## Abschluss

Mit Aspose.Cells für .NET ist das Abrufen von OData-Details aus einer Excel-Arbeitsmappe jetzt ganz einfach. Wenn Sie die in diesem Leitfaden beschriebenen Schritte befolgen, können Sie effizient auf OData-Daten zugreifen und diese verarbeiten. Experimentieren Sie mit Ihren eigenen Excel-Dateien mit OData-Details und holen Sie das Beste aus dieser leistungsstarken Funktion heraus.

### FAQs

#### F: Unterstützt Aspose.Cells neben OData auch andere Datenquellen?
    
A: Ja, Aspose.Cells unterstützt mehrere Datenquellen wie SQL-Datenbanken, CSV-Dateien, Webdienste usw.

#### F: Wie kann ich abgerufene OData-Details in meiner Anwendung verwenden?
    
A: Sobald Sie die OData-Details mit Aspose.Cells abgerufen haben, können Sie sie für die Datenanalyse, die Berichtserstellung oder andere Manipulationen in Ihrer Anwendung verwenden.

#### F: Kann ich OData-Daten beim Abrufen mit Aspose.Cells filtern oder sortieren?
    
A: Ja, Aspose.Cells bietet erweiterte Funktionen zum Filtern, Sortieren und Bearbeiten von OData-Daten, um Ihre spezifischen Anforderungen zu erfüllen.

#### F: Kann ich den Prozess des Abrufens von OData-Details mit Aspose.Cells automatisieren?
    
A: Ja, Sie können den Prozess des Abrufens von OData-Details automatisieren, indem Sie Aspose.Cells in Ihre Arbeitsabläufe integrieren oder Programmierskripts verwenden.