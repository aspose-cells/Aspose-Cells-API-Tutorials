---
title: Komprimierungsstufe anpassen
linktitle: Komprimierungsstufe anpassen
second_title: Aspose.Cells für .NET API-Referenz
description: Reduzieren Sie die Größe Ihrer Excel-Arbeitsmappen, indem Sie die Komprimierungsstufe mit Aspose.Cells für .NET anpassen.
type: docs
weight: 50
url: /de/net/excel-workbook/adjust-compression-level/
---
In diesem Schritt-für-Schritt-Tutorial erklären wir den bereitgestellten C#-Quellcode, mit dem Sie die Komprimierungsstufe mithilfe von Aspose.Cells für .NET anpassen können. Führen Sie die folgenden Schritte aus, um die Komprimierungsstufe in Ihrer Excel-Arbeitsmappe anzupassen.

## Schritt 1: Quell- und Ausgabeverzeichnis festlegen

```csharp
// Quellverzeichnis
string sourceDir = RunExamples.Get_SourceDirectory();
// Ausgabe Verzeichnis
string outDir = RunExamples.Get_OutputDirectory();
```

In diesem ersten Schritt definieren wir die Quell- und Ausgabeverzeichnisse für die Excel-Dateien.

## Schritt 2: Excel-Arbeitsmappe laden

```csharp
// Laden Sie die Excel-Arbeitsmappe
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
```

Wir laden die Excel-Arbeitsmappe aus der angegebenen Datei mit`Workbook` Klasse von Aspose.Cells.

## Schritt 3: Sicherungsoptionen festlegen

```csharp
// Definieren Sie Backup-Optionen
XlsbSaveOptions options = new XlsbSaveOptions();
```

 Wir erstellen eine Instanz davon`XlsbSaveOptions` Klasse zum Festlegen von Speicheroptionen.

## Schritt 4: Komprimierungsstufe anpassen (Stufe 1)

```csharp
// Komprimierungsstufe anpassen (Stufe 1)
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
let elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 1): " + elapsedMs);
```

 Wir passen die Komprimierungsstufe durch Einstellung an`CompressionType` Zu`Level1`. Dann speichern wir die Excel-Arbeitsmappe mit dieser angegebenen Komprimierungsoption.

## Schritt 5: Komprimierungsstufe anpassen (Stufe 6)

```csharp
// Komprimierungsstufe anpassen (Stufe 6)
options.CompressionType = OoxmlCompressionType.Level6;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 6): " + elapsedMs);
```

 Wir wiederholen den Vorgang, um die Komprimierungsstufe anzupassen`Level6` und speichern Sie die Excel-Arbeitsmappe mit dieser Option.

## Schritt 6: Komprimierungsstufe anpassen (Stufe 9)

```csharp
// Komprimierungsstufe anpassen (Stufe 9)
options.CompressionType = OoxmlCompressionType.Level9;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 9): " + elapsedMs);
```

 Wir wiederholen den Vorgang ein letztes Mal, um die Komprimierungsstufe anzupassen`Level9` und speichern Sie die Excel-Arbeitsmappe mit dieser Option.

### Beispielquellcode für „Komprimierungsstufe anpassen“ mit Aspose.Cells für .NET 
```csharp
//Quellverzeichnis
string sourceDir = RunExamples.Get_SourceDirectory();
string outDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
XlsbSaveOptions options = new XlsbSaveOptions();
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
var elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 1 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level6;
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 6 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level9;
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 9 Elapsed Time: " + elapsedMs);
Console.WriteLine("AdjustCompressionLevel executed successfully.");
```

## Abschluss

Herzlichen Glückwunsch! Sie haben gelernt, wie Sie die Komprimierungsstufe in einer Excel-Arbeitsmappe mithilfe von Aspose.Cells für .NET anpassen. Experimentieren Sie mit verschiedenen Komprimierungsstufen, um diejenige zu finden, die Ihren Anforderungen am besten entspricht.

### FAQs

#### F: Was ist Komprimierung in einer Excel-Arbeitsmappe?

A: Bei der Komprimierung in einer Excel-Arbeitsmappe wird die Dateigröße mithilfe von Komprimierungsalgorithmen reduziert. Dadurch wird der benötigte Speicherplatz reduziert und die Leistung beim Laden und Bearbeiten der Datei verbessert.

#### F: Welche Komprimierungsstufen sind mit Aspose.Cells verfügbar?

A: Mit Aspose.Cells können Sie die Komprimierungsstufe von 1 bis 9 anpassen. Je höher die Komprimierungsstufe, desto kleiner wird die Dateigröße, aber es kann auch die Verarbeitungszeit verlängern.

#### F: Wie wähle ich die richtige Komprimierungsstufe für meine Excel-Arbeitsmappe aus?

A: Die Wahl der Komprimierungsstufe hängt von Ihren spezifischen Anforderungen ab. Wenn Sie eine maximale Komprimierung wünschen und die Verarbeitungszeit kein Problem darstellt, können Sie sich für Stufe 9 entscheiden. Wenn Sie einen Kompromiss zwischen Dateigröße und Verarbeitungszeit bevorzugen, können Sie eine mittlere Stufe wählen.

#### F: Beeinträchtigt die Komprimierung die Datenqualität in Excel-Arbeitsmappen?

A: Nein, die Komprimierung hat keinen Einfluss auf die Datenqualität in der Excel-Arbeitsmappe. Es reduziert lediglich die Dateigröße mithilfe von Komprimierungstechniken, ohne die Daten selbst zu verändern.

#### F: Kann ich die Komprimierungsstufe nach dem Speichern der Excel-Datei anpassen?

A: Nein, sobald Sie die Excel-Datei mit einer bestimmten Komprimierungsstufe gespeichert haben, können Sie die Komprimierungsstufe später nicht mehr anpassen. Sie müssen die Datei erneut mit der neuen Komprimierungsstufe speichern, wenn Sie sie ändern möchten.