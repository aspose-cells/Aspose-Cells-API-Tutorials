---
title: Ermitteln Sie die Papierbreite und -höhe des Arbeitsblatts
linktitle: Ermitteln Sie die Papierbreite und -höhe des Arbeitsblatts
second_title: Aspose.Cells für .NET API-Referenz
description: Erstellen Sie eine Schritt-für-Schritt-Anleitung, um den folgenden C#-Quellcode zu erklären, um die Papierbreite und -höhe einer Tabelle mit Aspose.Cells für .NET zu ermitteln.
type: docs
weight: 80
url: /de/net/excel-display-settings-csharp-tutorials/get-paper-width-and-height-of-worksheet/
---
In diesem Tutorial erklären wir Ihnen Schritt für Schritt den folgenden C#-Quellcode, um die Papierbreite und -höhe eines Arbeitsblatts mithilfe von Aspose.Cells für .NET zu ermitteln. Folgen Sie den unteren Schritten:

## Schritt 1: Erstellen Sie die Arbeitsmappe
 Erstellen Sie zunächst eine neue Arbeitsmappe mit`Workbook` Klasse:

```csharp
Workbook wb = new Workbook();
```

## Schritt 2: Greifen Sie auf das erste Arbeitsblatt zu
 Navigieren Sie als Nächstes mit zum ersten Arbeitsblatt in der Arbeitsmappe`Worksheet` Klasse:

```csharp
Worksheet ws = wb.Worksheets[0];
```

## Schritt 3: Stellen Sie das Papierformat auf A2 ein und zeigen Sie die Papierbreite und -höhe in Zoll an
 Benutzen Sie die`PaperSize` Eigentum der`PageSetup` Objekt, um das Papierformat auf A2 einzustellen, und verwenden Sie dann das`PaperWidth` Und`PaperHeight` Eigenschaften, um die Papierbreite bzw. -höhe zu erhalten. Zeigen Sie diese Werte mit dem an`Console.WriteLine` Methode:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

## Schritt 4: Wiederholen Sie die Schritte für andere Papierformate
Wiederholen Sie die vorherigen Schritte, ändern Sie das Papierformat in A3, A4 und Letter und zeigen Sie dann die Werte für die Papierbreite und -höhe für jedes Format an:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

### Beispielquellcode zum Abrufen der Papierbreite und -höhe des Arbeitsblatts mit Aspose.Cells für .NET 

```csharp
//Arbeitsmappe erstellen
Workbook wb = new Workbook();
//Greifen Sie auf das erste Arbeitsblatt zu
Worksheet ws = wb.Worksheets[0];
//Stellen Sie das Papierformat auf A2 ein und geben Sie die Breite und Höhe des Papiers in Zoll an
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Stellen Sie das Papierformat auf A3 ein und geben Sie die Breite und Höhe des Papiers in Zoll an
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Stellen Sie das Papierformat auf A4 ein und drucken Sie die Breite und Höhe des Papiers in Zoll
ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Stellen Sie das Papierformat auf „Letter“ ein und geben Sie die Breite und Höhe des Druckpapiers in Zoll an
ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```


## Abschluss

Sie haben gelernt, wie Sie mit Aspose.Cells für .NET die Papierbreite und -höhe einer Tabellenkalkulation ermitteln. Diese Funktion kann für die Konfiguration und das präzise Layout Ihrer Excel-Dokumente nützlich sein.

### Häufig gestellte Fragen (FAQ)

#### Was ist Aspose.Cells für .NET?

Aspose.Cells für .NET ist eine leistungsstarke Bibliothek zum Bearbeiten und Verarbeiten von Excel-Dateien in .NET-Anwendungen. Es bietet viele Funktionen zum Erstellen, Ändern, Konvertieren und Analysieren von Excel-Dateien.

#### Wie kann ich mit Aspose.Cells für .NET die Papiergröße einer Tabelle ermitteln?

 Du kannst den ... benutzen`PageSetup` Klasse der`Worksheet` Objekt, um auf das Papierformat zuzugreifen. Benutzen Sie die`PaperSize` Eigenschaft zum Festlegen des Papierformats und der`PaperWidth` Und`PaperHeight` Eigenschaften, um die Papierbreite bzw. -höhe zu erhalten.

#### Welche Papierformate unterstützt Aspose.Cells für .NET?

Aspose.Cells für .NET unterstützt eine Vielzahl häufig verwendeter Papierformate wie A2, A3, A4 und Letter sowie viele andere benutzerdefinierte Formate.

#### Kann ich die Papiergröße einer Tabelle mit Aspose.Cells für .NET anpassen?

Ja, Sie können ein benutzerdefiniertes Papierformat festlegen, indem Sie mithilfe von die genauen Breiten- und Höhenabmessungen angeben`PaperWidth` Und`PaperHeight` Eigenschaften der`PageSetup` Klasse.