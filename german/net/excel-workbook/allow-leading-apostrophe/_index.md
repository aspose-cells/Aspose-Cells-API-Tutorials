---
title: Erlauben Sie führende Apostrophe
linktitle: Erlauben Sie führende Apostrophe
second_title: Aspose.Cells für .NET API-Referenz
description: Erlauben Sie führende Apostrophe in Excel-Arbeitsmappen mit Aspose.Cells für .NET.
type: docs
weight: 60
url: /de/net/excel-workbook/allow-leading-apostrophe/
---
In diesem Schritt-für-Schritt-Tutorial erklären wir den bereitgestellten C#-Quellcode, der es Ihnen ermöglicht, mithilfe von Aspose.Cells für .NET die Verwendung eines führenden Apostrophs in einer Excel-Arbeitsmappe zu ermöglichen. Befolgen Sie die nachstehenden Schritte, um diesen Vorgang auszuführen.

## Schritt 1: Quell- und Ausgabeverzeichnis festlegen

```csharp
// Quellverzeichnis
string sourceDir = RunExamples.Get_SourceDirectory();
// Ausgabe Verzeichnis
string outputDir = RunExamples.Get_OutputDirectory();
```

In diesem ersten Schritt definieren wir die Quell- und Ausgabeverzeichnisse für die Excel-Dateien.

## Schritt 2: Instanziieren Sie ein WorkbookDesigner-Objekt

```csharp
// Instanziieren Sie ein WorkbookDesigner-Objekt
WorkbookDesigner designer = new WorkbookDesigner();
```

 Wir erstellen eine Instanz davon`WorkbookDesigner` Klasse von Aspose.Cells.

## Schritt 3: Excel-Arbeitsmappe laden

```csharp
//Laden Sie die Excel-Arbeitsmappe
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
designer.Workbook = workbook;
```

Wir laden die Excel-Arbeitsmappe aus der angegebenen Datei und deaktivieren die automatische Konvertierung der anfänglichen Apostrophe in den Textstil.

## Schritt 4: Datenquelle festlegen

```csharp
// Definieren Sie die Datenquelle für die Designer-Arbeitsmappe
List<DataObject> list = new List<DataObject>
{
new DataObject
{
Id=1,
Name = "demo"
},
new DataObject
{
ID=2,
Name = "'demo"
}
};
designer.SetDataSource("sampleData", list);
```

 Wir definieren eine Liste von Datenobjekten und verwenden die`SetDataSource` Methode zum Festlegen der Datenquelle für die Designer-Arbeitsmappe.

## Schritt 5: Smart Marker verarbeiten

```csharp
// Verarbeiten Sie intelligente Marker
designer. Process();
```

 Wir benutzen das`Process` Methode zum Verarbeiten intelligenter Markierungen in der Designer-Arbeitsmappe.

## Schritt 6: Speichern Sie die geänderte Excel-Arbeitsmappe

```csharp
// Speichern Sie die geänderte Excel-Arbeitsmappe
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
```

Wir speichern die geänderte Excel-Arbeitsmappe mit den vorgenommenen Änderungen.

### Beispielquellcode für „Erlauben Sie führende Apostrophe“ mit Aspose.Cells für .NET 
```csharp
//Quellverzeichnis
string sourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
// Instanziieren eines WorkbookDesigner-Objekts
WorkbookDesigner designer = new WorkbookDesigner();
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
// Öffnen Sie eine Designer-Tabelle mit Smart Markers
designer.Workbook = workbook;
List<DataObject> list = new List<DataObject>
{
	new DataObject
	{
		 Id =1,
		 Name = "demo"
	},
	new DataObject
	{
		Id=2,
		Name = "'demo"
	}
};
// Legen Sie die Datenquelle für die Designer-Tabelle fest
designer.SetDataSource("sampleData", list);
// Verarbeiten Sie die Smart Marker
designer.Process();
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
Console.WriteLine("AllowLeadingApostrophe executed successfully.");
```

## Abschluss

Herzlichen Glückwunsch! Sie haben gelernt, wie Sie mithilfe von Aspose.Cells für .NET die Verwendung eines führenden Apostrophs in einer Excel-Arbeitsmappe zulassen. Experimentieren Sie mit Ihren eigenen Daten, um Ihre Excel-Arbeitsmappen weiter anzupassen.

### FAQs

#### F: Was ist die Berechtigung für führende Apostrophe in einer Excel-Arbeitsmappe?

A: Wenn Sie das anfängliche Apostroph in einer Excel-Arbeitsmappe zulassen, können Daten, die mit einem Apostroph beginnen, korrekt angezeigt werden, ohne dass sie in einen Textstil konvertiert werden müssen. Dies ist nützlich, wenn Sie das Apostroph als Teil der Daten behalten möchten.

#### F: Warum muss ich die automatische Konvertierung von Apostrophen am Anfang deaktivieren?

A: Durch Deaktivieren der automatischen Konvertierung führender Anführungszeichen können Sie deren Verwendung in Ihren Daten beibehalten. Dadurch wird eine unbeabsichtigte Änderung der Daten beim Öffnen oder Bearbeiten der Excel-Arbeitsmappe vermieden.

#### F: Wie lege ich eine Datenquelle in der Designer-Arbeitsmappe fest?

 A: Um die Datenquelle in der Designer-Arbeitsmappe festzulegen, können Sie die verwenden`SetDataSource` Methode, die den Namen der Datenquelle und eine Liste der entsprechenden Datenobjekte angibt.

#### F: Hat das Zulassen eines führenden Apostrophs Auswirkungen auf andere Daten in der Excel-Arbeitsmappe?

A: Nein, das Erlauben des führenden Apostrophs betrifft nur Daten, die mit einem Apostroph beginnen. Andere Daten in der Excel-Arbeitsmappe bleiben unverändert.

#### F: Kann ich diese Funktion mit anderen Excel-Dateiformaten verwenden?

A: Ja, Sie können diese Funktion mit anderen von Aspose.Cells unterstützten Excel-Dateiformaten wie .xls, .xlsm usw. verwenden.