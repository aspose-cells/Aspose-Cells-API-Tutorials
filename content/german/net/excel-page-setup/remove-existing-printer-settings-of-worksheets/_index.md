---
title: Entfernen Sie vorhandene Druckereinstellungen von Arbeitsblättern
linktitle: Entfernen Sie vorhandene Druckereinstellungen von Arbeitsblättern
second_title: Aspose.Cells für .NET API-Referenz
description: Erfahren Sie, wie Sie mit Aspose.Cells für .NET vorhandene Druckereinstellungen aus Excel-Tabellen entfernen.
type: docs
weight: 80
url: /de/net/excel-page-setup/remove-existing-printer-settings-of-worksheets/
---
In diesem Tutorial führen wir Sie Schritt für Schritt durch, wie Sie mithilfe von Aspose.Cells für .NET vorhandene Druckereinstellungen aus Arbeitsblättern in Excel entfernen. Wir werden C#-Quellcode verwenden, um den Prozess zu veranschaulichen.

## Schritt 1: Einrichten der Umgebung

Stellen Sie sicher, dass Aspose.Cells für .NET auf Ihrem Computer installiert ist. Erstellen Sie außerdem ein neues Projekt in Ihrer bevorzugten Entwicklungsumgebung.

## Schritt 2: Erforderliche Bibliotheken importieren

Importieren Sie in Ihre Codedatei die Bibliotheken, die für die Arbeit mit Aspose.Cells erforderlich sind. Hier ist der entsprechende Code:

```csharp
using Aspose.Cells;
```

## Schritt 3: Quell- und Ausgabeverzeichnis festlegen

Legen Sie die Quell- und Ausgabeverzeichnisse fest, in denen sich die ursprüngliche Excel-Datei befindet bzw. in denen Sie die geänderte Datei speichern möchten. Verwenden Sie den folgenden Code:

```csharp
string sourceDir = "SOURCE DIRECTORY PATH";
string outputDir = "OUTPUT DIRECTORY PATH";
```

Stellen Sie sicher, dass Sie vollständige Verzeichnispfade angeben.

## Schritt 4: Laden der Excel-Quelldatei

Laden Sie die Excel-Quelldatei mit dem folgenden Code:

```csharp
Workbook wb = new Workbook(sourceDir + "fileName.xlsx");
```

Dadurch wird die angegebene Excel-Datei in das Workbook-Objekt geladen.

## Schritt 5: Navigieren Sie durch die Arbeitsblätter

Durchlaufen Sie alle Arbeitsblätter in der Arbeitsmappe mithilfe einer Schleife. Verwenden Sie den folgenden Code:

```csharp
int sheetCount = wb. Worksheets. Count;

for (int i = 0; i < sheetCount; i++)
{
     Worksheet ws = wb.Worksheets[i];
     // Der Rest des Codes wird im nächsten Schritt hinzugefügt.
}
```

## Schritt 6: Vorhandene Druckereinstellungen löschen

Überprüfen Sie, ob für jedes Arbeitsblatt Druckereinstellungen vorhanden sind, und löschen Sie diese gegebenenfalls. Verwenden Sie den folgenden Code:

```csharp
PageSetup ps = ws.PageSetup;

if (ps.PrinterSettings != null)
{
     Console.WriteLine("Printer settings for this spreadsheet exist.");
     Console.WriteLine("Sheet name: " + ws.Name);
     Console.WriteLine("Paper size: " + ps.PaperSize);

     ps.PrinterSettings = null;

     Console.WriteLine("Printer settings for this spreadsheet have been removed by setting them to null.");
     Console.WriteLine("");
}
```

## Schritt 7: Speichern der geänderten Arbeitsmappe

Speichern Sie die geänderte Arbeitsmappe mit dem folgenden Code:

```csharp
wb.Save(outputDir + "modifiedFilename.xlsx");
```

Dadurch wird die geänderte Arbeitsmappe im angegebenen Ausgabeverzeichnis gespeichert.

### Beispielquellcode zum Entfernen vorhandener Druckereinstellungen von Arbeitsblättern mit Aspose.Cells für .NET 
```csharp
//Quellverzeichnis
string sourceDir = RunExamples.Get_SourceDirectory();
//Ausgabe Verzeichnis
string outputDir = RunExamples.Get_OutputDirectory();
//Laden Sie die Excel-Quelldatei
Workbook wb = new Workbook(sourceDir + "sampleRemoveExistingPrinterSettingsOfWorksheets.xlsx");
//Rufen Sie die Blattanzahl der Arbeitsmappe ab
int sheetCount = wb.Worksheets.Count;
//Iterieren Sie alle Blätter
for (int i = 0; i < sheetCount; i++)
{
    //Greifen Sie auf das i-te Arbeitsblatt zu
    Worksheet ws = wb.Worksheets[i];
    //Greifen Sie auf die Einrichtung der Arbeitsblattseite zu
    PageSetup ps = ws.PageSetup;
    //Überprüfen Sie, ob Druckereinstellungen für dieses Arbeitsblatt vorhanden sind
    if (ps.PrinterSettings != null)
    {
        //Drucken Sie die folgende Nachricht aus
        Console.WriteLine("PrinterSettings of this worksheet exist.");
        //Blattname und Papierformat drucken
        Console.WriteLine("Sheet Name: " + ws.Name);
        Console.WriteLine("Paper Size: " + ps.PaperSize);
        //Entfernen Sie die Druckereinstellungen, indem Sie sie auf Null setzen
        ps.PrinterSettings = null;
        Console.WriteLine("Printer settings of this worksheet are now removed by setting it null.");
        Console.WriteLine("");
    }//Wenn
}//für
//Speichern Sie die Arbeitsmappe
wb.Save(outputDir + "outputRemoveExistingPrinterSettingsOfWorksheets.xlsx");
```

## Abschluss

Sie haben jetzt gelernt, wie Sie mit Aspose.Cells für .NET vorhandene Druckereinstellungen aus Arbeitsblättern in Excel entfernen. Dieses Tutorial führte Sie durch jeden Schritt des Prozesses, von der Einrichtung der Umgebung über die Navigation durch Tabellenkalkulationen bis hin zum Löschen der Druckereinstellungen. Dieses Wissen können Sie nun nutzen, um Druckereinstellungen in Ihren Excel-Dateien zu verwalten.

### FAQs

#### F1: Woher weiß ich, ob in einer Tabelle bereits Druckereinstellungen vorhanden sind?

 A1: Sie können überprüfen, ob Druckereinstellungen für ein Arbeitsblatt vorhanden sind, indem Sie auf zugreifen`PrinterSettings` Eigentum der`PageSetup` Objekt. Wenn der Wert ungleich Null ist, bedeutet dies, dass Druckereinstellungen vorhanden sind.

#### F2: Kann ich Druckereinstellungen nur für eine bestimmte Tabelle löschen?

 A2: Ja, Sie können den gleichen Ansatz verwenden, um Druckereinstellungen für ein bestimmtes Arbeitsblatt zu entfernen, indem Sie auf die Einstellungen dieses Arbeitsblatts zugreifen`PageSetup` Objekt.

#### F3: Entfernt diese Methode auch andere Layouteinstellungen?

A3: Nein, diese Methode löscht nur Druckereinstellungen. Andere Layouteinstellungen wie Ränder, Papierausrichtung usw. bleiben unverändert.

#### F4: Funktioniert diese Methode für alle Excel-Dateiformate wie .xls und .xlsx?

A4: Ja, diese Methode funktioniert für alle von Aspose.Cells unterstützten Excel-Dateiformate, einschließlich .xls und .xlsx.

#### F5: Werden an den Druckereinstellungen vorgenommene Änderungen dauerhaft in der bearbeiteten Excel-Datei übernommen?

A5: Ja, Änderungen an den Druckereinstellungen werden dauerhaft in der bearbeiteten Excel-Datei gespeichert.