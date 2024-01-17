---
title: Excel-Arbeitsblatt aus einer anderen Arbeitsmappe kopieren
linktitle: Excel-Arbeitsblatt aus einer anderen Arbeitsmappe kopieren
second_title: Aspose.Cells für .NET API-Referenz
description: Kopieren Sie mit Aspose.Cells für .NET ganz einfach ein Excel-Arbeitsblatt von einer Arbeitsmappe in eine andere.
type: docs
weight: 10
url: /de/net/excel-copy-worksheet/excel-copy-worksheet-from-other-workbook/
---
In diesem Tutorial führen wir Sie durch die Schritte zum Kopieren eines Excel-Arbeitsblatts aus einer anderen Arbeitsmappe mithilfe der Aspose.Cells-Bibliothek für .NET. Befolgen Sie die nachstehenden Anweisungen, um diese Aufgabe abzuschließen.

## Schritt 1: Vorbereitung

Bevor Sie beginnen, stellen Sie sicher, dass Sie Aspose.Cells für .NET installiert und ein C#-Projekt in Ihrer bevorzugten integrierten Entwicklungsumgebung (IDE) erstellt haben.

## Schritt 2: Legen Sie den Dokumentverzeichnispfad fest

 Erkläre a`dataDir` Variable und initialisieren Sie sie mit dem Pfad zu Ihrem Dokumentenverzeichnis. Zum Beispiel :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Unbedingt austauschen`"YOUR_DOCUMENTS_DIRECTORY"` mit dem tatsächlichen Pfad zu Ihrem Verzeichnis.

## Schritt 3: Erstellen Sie eine neue Excel-Arbeitsmappe

 Benutzen Sie die`Workbook` Klasse von Aspose.Cells, um eine neue Excel-Arbeitsmappe zu erstellen:

```csharp
Workbook excelWorkbook0 = new Workbook();
```

## Schritt 4: Holen Sie sich das erste Arbeitsblatt in die Arbeitsmappe

Navigieren Sie mit Index 0 zum ersten Arbeitsblatt in der Arbeitsmappe:

```csharp
Worksheet ws0 = excelWorkbook0.Worksheets[0];
```

## Schritt 5: Daten zu Kopfzeilen hinzufügen (A1:A4)

 Benutze einen`for` Schleife zum Hinzufügen von Daten zu den Kopfzeilen (A1:A4):

```csharp
for (int i = 0; i < 5; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Header row {0}", i));
}
```

## Schritt 6: Detaillierte Daten hinzufügen (A5:A999)

 Benutzen Sie ein anderes`for` Schleife zum Hinzufügen detaillierter Daten (A5:A999):

```csharp
for (int i = 5; i < 1000; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Detail row {0}", i));
}
```

## Schritt 7: Layoutoptionen festlegen

 Legen Sie Seiteneinrichtungsoptionen für das Arbeitsblatt mithilfe von fest`PageSetup` Objekt:

```csharp
PageSetup pagesetup = ws0.PageSetup;
pagesetup.PrintTitleRows = "$1:$5";
```

## Schritt 8: Erstellen Sie eine weitere Excel-Arbeitsmappe

Erstellen Sie eine weitere Excel-Arbeitsmappe:

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## Schritt 9: Holen Sie sich das erste Arbeitsblatt aus der zweiten Arbeitsmappe

Navigieren Sie zum ersten Arbeitsblatt in der zweiten Arbeitsmappe:

```csharp
Worksheet ws1 = excelWorkbook1.Worksheets[0];
```

## Schritt 10: Benennen Sie das Arbeitsblatt

Benennen Sie das Feuer

Berechnungsinsel:

```csharp
ws1.Name = "MySheet";
```

## Schritt 11: Kopieren Sie Daten aus dem ersten Arbeitsblatt der ersten Arbeitsmappe in das erste Arbeitsblatt der zweiten Arbeitsmappe

Kopieren Sie die Daten aus dem ersten Arbeitsblatt der ersten Arbeitsmappe in das erste Arbeitsblatt der zweiten Arbeitsmappe:

```csharp
ws1.Copy(ws0);
```

## Schritt 12: Speichern Sie die Excel-Datei

Speichern Sie die Excel-Datei:

```csharp
excelWorkbook1.Save(dataDir + "CopyWorkbookSheetToOther_out.xls");
```

Geben Sie unbedingt den gewünschten Pfad und Dateinamen für die Ausgabedatei an.

### Beispielquellcode für Excel-Arbeitsblatt aus anderer Arbeitsmappe kopieren mit Aspose.Cells für .NET 
```csharp
//Der Pfad zum Dokumentenverzeichnis.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Erstellen Sie eine neue Arbeitsmappe.
Workbook excelWorkbook0 = new Workbook();
// Holen Sie sich das erste Arbeitsblatt im Buch.
Worksheet ws0 = excelWorkbook0.Worksheets[0];
// Fügen Sie einige Daten in Kopfzeilen ein (A1:A4)
for (int i = 0; i < 5; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Header Row {0}", i));
}
// Geben Sie einige Detaildaten ein (A5:A999)
for (int i = 5; i < 1000; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Detail Row {0}", i));
}
// Definieren Sie ein Seiteneinrichtungsobjekt basierend auf dem ersten Arbeitsblatt.
PageSetup pagesetup = ws0.PageSetup;
// Die ersten fünf Zeilen werden auf jeder Seite wiederholt ...
// Es ist in der Druckvorschau zu sehen.
pagesetup.PrintTitleRows = "$1:$5";
// Erstellen Sie eine weitere Arbeitsmappe.
Workbook excelWorkbook1 = new Workbook();
// Holen Sie sich das erste Arbeitsblatt im Buch.
Worksheet ws1 = excelWorkbook1.Worksheets[0];
// Benennen Sie das Arbeitsblatt.
ws1.Name = "MySheet";
// Kopieren Sie Daten aus dem ersten Arbeitsblatt der ersten Arbeitsmappe in die
// erstes Arbeitsblatt der zweiten Arbeitsmappe.
ws1.Copy(ws0);
// Speichern Sie die Excel-Datei.
excelWorkbook1.Save(dataDir + "CopyWorksheetFromWorkbookToOther_out.xls");
```

## Abschluss

Herzlichen Glückwunsch! Sie haben jetzt gelernt, wie Sie mit Aspose.Cells für .NET ein Excel-Arbeitsblatt aus einer anderen Arbeitsmappe kopieren. Nutzen Sie diese Methode gerne in Ihren eigenen Projekten, um Excel-Dateien effizient zu bearbeiten.

### FAQs

#### F. Welche Bibliotheken werden benötigt, um Aspose.Cells für .NET zu verwenden?

A. Um Aspose.Cells für .NET verwenden zu können, müssen Sie die Aspose.Cells-Bibliothek in Ihr Projekt einbinden. Stellen Sie sicher, dass Sie in Ihrer integrierten Entwicklungsumgebung (IDE) korrekt auf diese Bibliothek verwiesen haben.

#### F. Unterstützt Aspose.Cells andere Excel-Dateiformate wie XLSX?

A. Ja, Aspose.Cells unterstützt verschiedene Excel-Dateiformate, darunter XLSX, XLS, CSV, HTML und viele mehr. Sie können diese Dateiformate mithilfe der Funktionen von Aspose.Cells für .NET bearbeiten.

#### F. Kann ich die Layoutoptionen beim Kopieren des Arbeitsblatts anpassen?

A.  Ja, Sie können die Seiteneinrichtungsoptionen beim Kopieren des Arbeitsblatts mithilfe der Eigenschaften anpassen`PageSetup` Objekt. Sie können Seitenkopfzeilen, Fußzeilen, Ränder, Ausrichtungen usw. angeben.