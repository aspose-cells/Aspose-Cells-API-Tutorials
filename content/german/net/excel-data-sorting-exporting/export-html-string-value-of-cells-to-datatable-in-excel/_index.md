---
title: Exportieren Sie den HTML-String-Wert von Zellen in eine DataTable in Excel
linktitle: Exportieren Sie den HTML-String-Wert von Zellen in eine DataTable in Excel
second_title: Aspose.Cells .NET Excel-Verarbeitungs-API
description: Erfahren Sie in einem einfachen Schritt-für-Schritt-Tutorial, wie Sie mit Aspose.Cells für .NET HTML-Zeichenfolgenwerte aus Excel-Zellen in eine DataTable exportieren.
type: docs
weight: 11
url: /de/net/excel-data-sorting-exporting/export-html-string-value-of-cells-to-datatable-in-excel/
---
## Einführung

Wenn Sie mit Excel-Dateien in einer .NET-Umgebung arbeiten, müssen Sie möglicherweise Informationen aus Zellen extrahieren, und zwar nicht nur als einfachen Text, sondern auch als HTML-Zeichenfolgen. Dies kann sehr praktisch sein, wenn Sie mit Rich-Text-Daten arbeiten oder die Formatierung beibehalten möchten. In dieser Anleitung führe ich Sie durch den Export des HTML-Zeichenfolgenwerts von Zellen in eine DataTable mithilfe von Aspose.Cells für .NET. 

## Voraussetzungen

Bevor wir uns in den Code vertiefen, stellen wir sicher, dass Sie alles haben, was Sie brauchen. Hier ist eine kurze Checkliste:

1. Grundkenntnisse in C# und .NET: Bevor Sie mit dem Codieren beginnen, stellen Sie sicher, dass Sie mit der C#-Programmierung und den Grundlagen des .NET-Frameworks vertraut sind.
2.  Aspose.Cells für .NET: Falls noch nicht geschehen, müssen Sie Aspose.Cells für .NET installieren. Sie können eine kostenlose Testversion herunterladen von[Hier](https://releases.aspose.com/).
3. Visual Studio oder IDE Ihrer Wahl: Richten Sie Ihre Umgebung zum Schreiben von C#-Code ein. Visual Studio wird aufgrund seiner umfangreichen Funktionen und Benutzerfreundlichkeit empfohlen.
4. Beispiel-Excel-Datei: Sie benötigen eine Beispiel-Excel-Datei (`sampleExportTableAsHtmlString.xlsx`) zum Arbeiten. Stellen Sie sicher, dass es sich in einem zugänglichen Verzeichnis befindet.
5. NuGet-Paket-Manager: Stellen Sie sicher, dass Sie in Ihrem Projekt Zugriff auf den NuGet-Paket-Manager haben, um die Aspose.Cells-Bibliothek einfach hinzuzufügen.

Nachdem diese Voraussetzungen erfüllt sind, können wir mit dem Programmieren beginnen!

## Pakete importieren

Bevor wir mit Aspose.Cells arbeiten können, müssen wir die erforderlichen Pakete importieren. Dazu müssen Sie normalerweise das NuGet-Paket Aspose.Cells zu Ihrem Projekt hinzufügen. So geht's:

### Öffnen Sie den NuGet-Paket-Manager

Klicken Sie in Visual Studio mit der rechten Maustaste auf Ihr Projekt im Projektmappen-Explorer und wählen Sie „NuGet-Pakete verwalten“ aus.

### Suche nach Aspose.Cells

 Geben Sie im NuGet-Paket-Manager Folgendes ein:`Aspose.Cells` in die Suchleiste.

### Installieren des Pakets

Wenn Sie Aspose.Cells gefunden haben, klicken Sie auf die Schaltfläche Installieren. Dadurch wird die Bibliothek zu Ihrem Projekt hinzugefügt und Sie können sie in Ihren Code importieren.

### Importieren des Namespace

Fügen Sie oben in Ihrer Codedatei die folgende Using-Direktive hinzu:

```csharp
using System;
using System.IO;
using Aspose.Cells;
using System.Data;
```

Nachdem wir nun alles eingerichtet haben, tauchen wir Schritt für Schritt in den Prozess des Exportierens von HTML-Zeichenfolgenwerten aus einer Excel-Datei in eine DataTable ein. 

## Schritt 1: Definieren Sie das Quellverzeichnis

Sie beginnen mit der Definition des Verzeichnisses, in dem Ihre Excel-Beispieldatei gespeichert ist. Dies ist wichtig, da es Ihrer Anwendung mitteilt, wo die Datei zu finden ist. Hier ist der Code dafür:

```csharp
string sourceDir = "Your Document Directory";
```

 Ersetzen Sie unbedingt`"Your Document Directory"` durch den tatsächlichen Pfad zu Ihrer Excel-Datei.

## Schritt 2: Laden Sie die Excel-Beispieldatei

 Der nächste Schritt besteht darin, die Excel-Arbeitsmappe zu laden. Sie verwenden die`Workbook` Klasse von Aspose.Cells, um dies zu tun. So können Sie die Datei laden:

```csharp
Workbook wb = new Workbook(sourceDir + "sampleExportTableAsHtmlString.xlsx");
```

Diese einfache Codezeile initialisiert die Arbeitsmappe und lädt die angegebene Excel-Datei.

## Schritt 3: Zugriff auf das erste Arbeitsblatt

Sobald die Arbeitsmappe geladen ist, möchten Sie auf das spezifische Arbeitsblatt zugreifen, das die Daten enthält, an denen Sie interessiert sind. Im Allgemeinen beginnen Sie mit dem ersten Arbeitsblatt:

```csharp
Worksheet ws = wb.Worksheets[0];
```

Hier arbeiten wir mit dem ersten Arbeitsblatt (Index 0). Stellen Sie sicher, dass sich Ihre Daten auf dem richtigen Blatt befinden.

## Schritt 4: Optionen für den Tabellenexport festlegen

Um zu steuern, wie die Daten exportiert werden, müssen Sie Folgendes einrichten:`ExportTableOptions`. In diesem Fall möchten Sie sicherstellen, dass die Spaltennamen nicht exportiert werden und die Zellendaten als HTML-Strings exportiert werden:

```csharp
ExportTableOptions opts = new ExportTableOptions();
opts.ExportColumnName = false;
opts.ExportAsHtmlString = true;
```

Mit dieser Konfiguration können Sie die umfangreiche Formatierung Ihrer Zellendaten beim Exportieren beibehalten.

## Schritt 5: Zellen in DataTable exportieren

 Jetzt kommt der entscheidende Teil, bei dem Sie die Daten tatsächlich exportieren. Mit dem`ExportDataTable` können Sie die Daten aus dem Arbeitsblatt in ein`DataTable`So geht's:

```csharp
DataTable dt = ws.Cells.ExportDataTable(0, 0, 3, 3, opts);
```

Dieser Code exportiert einen angegebenen Zellbereich (von Zeile 0, Spalte 0 bis Zeile 3, Spalte 3) unter Verwendung der zuvor angegebenen Optionen in eine DataTable.

## Schritt 6: Drucken Sie den HTML-String-Wert

Lassen Sie uns abschließend den HTML-String-Wert aus einer bestimmten Zelle in der DataTable ausdrucken, um zu sehen, was wir exportiert haben. Wenn Sie beispielsweise den Wert aus der dritten Zeile und der zweiten Spalte ausdrucken möchten, gehen Sie wie folgt vor:

```csharp
Console.WriteLine(dt.Rows[2][1].ToString());
```

Diese Zeile druckt den gewünschten HTML-String aus der DataTable in die Konsole. 

## Abschluss 

Und da haben Sie es! Sie haben erfolgreich HTML-Stringwerte aus Zellen einer Excel-Datei mithilfe von Aspose.Cells für .NET in eine DataTable exportiert. Diese Funktion verbessert nicht nur Ihre Fähigkeiten zur Datenmanipulation, sondern erweitert auch Ihre Optionen beim Umgang mit formatierten Inhalten direkt aus Excel-Dateien. 

## Häufig gestellte Fragen

### Kann ich Aspose.Cells für andere Dateiformate außer Excel verwenden?  
Ja, Aspose.Cells ist in erster Linie für Excel gedacht, aber Aspose bietet andere Bibliotheken für verschiedene Formate.

### Benötige ich eine Lizenz für Aspose.Cells?  
 Ja, für den produktiven Einsatz ist eine gültige Lizenz erforderlich. Sie können eine temporäre Lizenz erhalten[Hier](https://purchase.aspose.com/temporary-license/).

### Was ist, wenn meine Excel-Datei Formeln enthält? Werden diese korrekt exportiert?  
Ja, Aspose.Cells kann Formeln verarbeiten und beim Exportieren werden sie anhand ihrer resultierenden Werte ausgewertet.

### Ist es möglich, die Exportoptionen zu ändern?  
 Absolut! Sie können anpassen`ExportTableOptions` um sie Ihren spezifischen Anforderungen anzupassen.

### Wo finde ich ausführlichere Dokumentation für Aspose.Cells?  
 Ausführliche Dokumentation finden Sie[Hier](https://reference.aspose.com/cells/net/).