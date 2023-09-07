---
title: Excel-Arbeitsblätter zwischen Arbeitsmappen kopieren
linktitle: Excel-Arbeitsblätter zwischen Arbeitsmappen kopieren
second_title: Aspose.Cells für .NET API-Referenz
description: Kopieren Sie Arbeitsblätter ganz einfach zwischen Excel-Arbeitsmappen mit Aspose.Cells für .NET.
type: docs
weight: 30
url: /de/net/excel-copy-worksheet/excel-copy-worksheets-between-workbooks/
---
In diesem Tutorial führen wir Sie durch die Schritte zum Kopieren von Arbeitsblättern zwischen Excel-Arbeitsmappen mithilfe der Aspose.Cells-Bibliothek für .NET. Befolgen Sie die nachstehenden Anweisungen, um diese Aufgabe abzuschließen.

## Schritt 1: Vorbereitung

Stellen Sie sicher, dass Sie Aspose.Cells für .NET installiert und ein C#-Projekt in Ihrer bevorzugten integrierten Entwicklungsumgebung (IDE) erstellt haben.

## Schritt 2: Legen Sie den Dokumentverzeichnispfad fest

 Erkläre a`dataDir` Variable und initialisieren Sie sie mit dem Pfad zu Ihrem Dokumentenverzeichnis. Zum Beispiel :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Unbedingt austauschen`"YOUR_DOCUMENTS_DIRECTORY"` mit dem tatsächlichen Pfad zu Ihrem Verzeichnis.

## Schritt 3: Definieren Sie den Eingabedateipfad

 Erklären Sie eine`InputPath` Variable und initialisieren Sie sie mit dem vollständigen Pfad der Excel-Datei, aus der Sie die Tabelle kopieren möchten. Zum Beispiel :

```csharp
string InputPath = dataDir + "book1.xls";
```

 Stellen Sie sicher, dass Sie über die Excel-Datei verfügen`book1.xls` in Ihrem Dokumentenverzeichnis oder geben Sie den richtigen Dateinamen und Speicherort an.

## Schritt 4: Erstellen Sie eine erste Excel-Arbeitsmappe

 Benutzen Sie die`Workbook` Klasse von Aspose.Cells, um eine erste Excel-Arbeitsmappe zu erstellen und die angegebene Datei zu öffnen:

```csharp
Workbook excelWorkbook0 = new Workbook(InputPath);
```

## Schritt 5: Erstellen Sie eine zweite Excel-Arbeitsmappe

Erstellen Sie eine zweite Excel-Arbeitsmappe:

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## Schritt 6: Kopieren Sie das Arbeitsblatt aus der ersten Arbeitsmappe in die zweite Arbeitsmappe

 Benutzen Sie die`Copy`Methode zum Kopieren des ersten Arbeitsblatts aus der ersten Arbeitsmappe in die zweite Arbeitsmappe:

```csharp
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
```

## Schritt 7: Speichern Sie die Excel-Datei

Speichern Sie die Excel-Datei mit der kopierten Tabelle:

```csharp
excelWorkbook1.Save(dataDir + "Copy WorksheetsBetweenWorkbooks_out.xls");
```

Geben Sie unbedingt den gewünschten Pfad und Dateinamen für die Ausgabedatei an.

### Beispielquellcode für Excel-Arbeitsblätter zwischen Arbeitsmappen kopieren mit Aspose.Cells für .NET 
```csharp
// Der Pfad zum Dokumentenverzeichnis.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Erstellen Sie eine Arbeitsmappe.
// Öffnen Sie eine Datei im ersten Buch.
Workbook excelWorkbook0 = new Workbook(InputPath);
// Erstellen Sie eine weitere Arbeitsmappe.
Workbook excelWorkbook1 = new Workbook();
// Kopieren Sie das erste Blatt des ersten Buches in das zweite Buch.
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
// Speicher die Datei.
excelWorkbook1.Save(dataDir + "CopyWorksheetsBetweenWorkbooks_out.xls");
```

## Abschluss

Herzlichen Glückwunsch! Sie haben jetzt gelernt, wie Sie mit Aspose.Cells für .NET Arbeitsblätter zwischen Excel-Arbeitsmappen kopieren. Nutzen Sie diese Methode gerne in Ihren eigenen Projekten, um Excel-Dateien effizient zu bearbeiten.

### FAQs

#### F. Welche Bibliotheken werden benötigt, um Aspose.Cells für .NET zu verwenden?

A. Um Aspose.Cells für .NET verwenden zu können, müssen Sie die Aspose.Cells-Bibliothek in Ihr Projekt einbinden. Stellen Sie sicher, dass Sie in Ihrer integrierten Entwicklungsumgebung (IDE) korrekt auf diese Bibliothek verwiesen haben.

#### F. Unterstützt Aspose.Cells andere Excel-Dateiformate wie XLSX?

A. Ja, Aspose.Cells unterstützt verschiedene Excel-Dateiformate, darunter XLSX, XLS, CSV, HTML und viele mehr. Sie können diese Dateiformate mithilfe der Funktionen von Aspose.Cells für .NET bearbeiten.

#### F. Kann ich die Layoutoptionen beim Kopieren der Tabelle anpassen?

A.  Ja, Sie können die Seiteneinrichtungsoptionen beim Kopieren der Tabelle mithilfe der Eigenschaften anpassen`PageSetup` Objekt. Sie können Seitenkopfzeilen, Fußzeilen, Ränder, Ausrichtungen usw. angeben.