---
title: Bereiche des Arbeitsblatts einfrieren
linktitle: Bereiche des Arbeitsblatts einfrieren
second_title: Aspose.Cells für .NET API-Referenz
description: Bearbeiten Sie eingefrorene Bereiche von Excel-Arbeitsblättern ganz einfach mit Aspose.Cells für .NET.
type: docs
weight: 70
url: /de/net/excel-display-settings-csharp-tutorials/freeze-panes-of-worksheet/
---
In diesem Tutorial zeigen wir Ihnen, wie Sie Bereiche in einem Excel-Arbeitsblatt mithilfe von C#-Quellcode mit Aspose.Cells für .NET sperren. Befolgen Sie die nachstehenden Schritte, um das gewünschte Ergebnis zu erzielen.

## Schritt 1: Importieren Sie die erforderlichen Bibliotheken

Stellen Sie sicher, dass Sie die Aspose.Cells-Bibliothek für .NET installiert haben und importieren Sie die erforderlichen Bibliotheken in Ihr C#-Projekt.

```csharp
using Aspose.Cells;
```

## Schritt 2: Verzeichnispfad festlegen und Excel-Datei öffnen

 Legen Sie den Pfad zu dem Verzeichnis fest, das Ihre Excel-Datei enthält, und öffnen Sie dann die Datei, indem Sie a instanziieren`Workbook` Objekt.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## Schritt 3: Gehen Sie zur Tabelle und wenden Sie die Einstellungen für die Fenstersperre an

 Navigieren Sie mit zum ersten Arbeitsblatt in der Excel-Datei`Worksheet` Objekt. Dann nutzen Sie die`FreezePanes` Methode zum Anwenden der Fenstersperreinstellungen.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. FreezePanes(3, 2, 3, 2);
```

Im obigen Beispiel sind die Bereiche an die Zelle in Zeile 3 und Spalte 2 gebunden.

## Schritt 4: Änderungen speichern

 Nachdem Sie die notwendigen Änderungen vorgenommen haben, speichern Sie die geänderte Excel-Datei mit`Save` Methode der`Workbook` Objekt.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Beispielquellcode für Freeze Panes Of Worksheet mit Aspose.Cells für .NET 

```csharp
// Der Pfad zum Dokumentenverzeichnis.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Erstellen eines Dateistreams, der die zu öffnende Excel-Datei enthält
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Instanziieren eines Workbook-Objekts
// Öffnen der Excel-Datei über den Dateistream
Workbook workbook = new Workbook(fstream);
// Zugriff auf das erste Arbeitsblatt in der Excel-Datei
Worksheet worksheet = workbook.Worksheets[0];
// Anwenden der Einstellungen für eingefrorene Fenster
worksheet.FreezePanes(3, 2, 3, 2);
// Speichern der geänderten Excel-Datei
workbook.Save(dataDir + "output.xls");
// Schließen des Dateistreams, um alle Ressourcen freizugeben
fstream.Close();
```

## Abschluss

Diese Schritt-für-Schritt-Anleitung zeigte Ihnen, wie Sie Bereiche in einer Excel-Tabelle mit Aspose.Cells für .NET sperren. Mithilfe des bereitgestellten C#-Quellcodes können Sie die Einstellungen für die Fenstersperre ganz einfach anpassen, um Ihre Daten in Excel-Dateien besser zu organisieren und zu visualisieren.

### Häufig gestellte Fragen (FAQ)

#### Was ist Aspose.Cells für .NET?

Aspose.Cells für .NET ist eine leistungsstarke Bibliothek zum Bearbeiten von Excel-Dateien in .NET-Anwendungen.

#### Wie kann ich Aspose.Cells für .NET installieren?

 Um Aspose.Cells für .NET zu installieren, müssen Sie das entsprechende Paket von herunterladen[Aspose-Veröffentlichungen](https://releases/aspose.com/cells/net/) und fügen Sie es Ihrem .NET-Projekt hinzu.

#### Wie sperre ich Bereiche in einem Excel-Arbeitsblatt mit Aspose.Cells für .NET?

 Du kannst den ... benutzen`FreezePanes` Methode der`Worksheet` Objekt zum Sperren der Bereiche eines Arbeitsblatts. Geben Sie die zu sperrenden Zellen an, indem Sie Zeilen- und Spaltenindizes angeben.

#### Kann ich die Einstellungen für die Fenstersperre mit Aspose.Cells für .NET anpassen?

 Ja, mit der`FreezePanes` Mit der Methode können Sie bei Bedarf angeben, welche Zellen gesperrt werden sollen, und dabei die entsprechenden Zeilen- und Spaltenindizes bereitstellen.
