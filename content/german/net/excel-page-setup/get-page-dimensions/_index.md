---
title: Seitenabmessungen abrufen
linktitle: Seitenabmessungen abrufen
second_title: Aspose.Cells für .NET API-Referenz
description: Erfahren Sie, wie Sie mit Aspose.Cells für .NET Seitenabmessungen in Excel abrufen. Schritt-für-Schritt-Anleitung mit Quellcode in C#.
type: docs
weight: 40
url: /de/net/excel-page-setup/get-page-dimensions/
---
Aspose.Cells für .NET ist eine leistungsstarke Bibliothek, die es Entwicklern ermöglicht, programmgesteuert mit Microsoft Excel-Dateien zu arbeiten. Es bietet zahlreiche Funktionen zum Bearbeiten von Excel-Dokumenten, einschließlich der Möglichkeit, Seitenabmessungen abzurufen. In diesem Tutorial führen wir Sie durch die Schritte zum Abrufen von Seitenabmessungen mit Aspose.Cells für .NET.

## Schritt 1: Erstellen Sie eine Instanz der Workbook-Klasse

Zunächst müssen wir eine Instanz der Workbook-Klasse erstellen, die die Excel-Arbeitsmappe darstellt. Dies kann mit dem folgenden Code erreicht werden:

```csharp
Workbook book = new Workbook();
```

## Schritt 2: Zugriff auf die Tabelle

Als Nächstes müssen wir zu dem Arbeitsblatt in der Arbeitsmappe navigieren, in dem wir die Seitenabmessungen festlegen möchten. Angenommen, wir möchten in diesem Beispiel mit dem ersten Arbeitsblatt arbeiten. Wir können mit dem folgenden Code darauf zugreifen:

```csharp
Worksheet sheet = book.Worksheets[0];
```

## Schritt 3: Stellen Sie das Papierformat auf A2 ein und geben Sie Breite und Höhe in Zoll an

Jetzt stellen wir das Papierformat auf A2 ein und drucken die Seitenbreite und -höhe in Zoll. Dies kann mit dem folgenden Code erreicht werden:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("A2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Schritt 4: Stellen Sie das Papierformat auf A3 ein und geben Sie Breite und Höhe in Zoll an

Als nächstes stellen wir das Papierformat auf A3 ein und drucken die Seitenbreite und -höhe in Zoll. Hier ist der entsprechende Code:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("A3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Schritt 5: Stellen Sie das Papierformat auf A4 ein und geben Sie Breite und Höhe in Zoll an

Wir stellen nun das Papierformat auf A4 ein und drucken die Seitenbreite und -höhe in Zoll. Hier ist der Code:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("A4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Schritt 6: Stellen Sie das Papierformat auf „Letter“ ein und drucken Sie die Breite und Höhe in Zoll

Zum Schluss stellen wir das Papierformat auf „Letter“ ein und drucken die Seitenbreite und -höhe in Zoll. Hier ist der Code:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("Letter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

### Beispielquellcode für „Get Page Dimensions“ mit Aspose.Cells für .NET 
```csharp
// Erstellen Sie eine Instanz der Workbook-Klasse
Workbook book = new Workbook();
// Greifen Sie auf das erste Arbeitsblatt zu
Worksheet sheet = book.Worksheets[0];
// Stellen Sie das Papierformat auf A2 ein und geben Sie die Breite und Höhe des Papiers in Zoll an
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Stellen Sie das Papierformat auf A3 ein und geben Sie die Breite und Höhe des Papiers in Zoll an
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Stellen Sie das Papierformat auf A4 ein und drucken Sie die Breite und Höhe des Papiers in Zoll
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Stellen Sie das Papierformat auf „Letter“ ein und geben Sie die Breite und Höhe des Druckpapiers in Zoll an
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
Console.WriteLine("GetPageDimensions executed successfully.\r\n");
```

## Abschluss

Herzlichen Glückwunsch! Sie haben gelernt, wie Sie Seitenabmessungen mit Aspose.Cells für .NET abrufen. Diese Funktion kann nützlich sein, wenn Sie bestimmte Vorgänge basierend auf den Seitenabmessungen in Ihren Excel-Dateien ausführen müssen.

Vergessen Sie nicht, die Dokumentation von Aspose.Cells weiter zu durchsuchen, um alle leistungsstarken Funktionen zu entdecken, die es bietet.

### FAQs

#### 1. Welche anderen Papierformate unterstützt Aspose.Cells für .NET?

Aspose.Cells für .NET unterstützt eine Vielzahl von Papierformaten, darunter A1, A5, B4, B5, Executive, Legal, Letter und viele mehr. Die vollständige Liste der unterstützten Papierformate finden Sie in der Dokumentation.

#### 2. Kann ich mit Aspose.Cells für .NET benutzerdefinierte Seitenabmessungen festlegen?

Ja, Sie können benutzerdefinierte Seitenabmessungen festlegen, indem Sie die gewünschte Breite und Höhe angeben. Aspose.Cells bietet volle Flexibilität, um die Seitenabmessungen an Ihre Bedürfnisse anzupassen.

#### 3. Kann ich Seitenabmessungen in anderen Einheiten als Zoll erhalten?

Ja, mit Aspose.Cells für .NET können Sie Seitenabmessungen in verschiedenen Einheiten abrufen, einschließlich Zoll, Zentimeter, Millimeter und Punkt.

#### 4. Unterstützt Aspose.Cells für .NET andere Bearbeitungsfunktionen für Seiteneinstellungen?

Ja, Aspose.Cells bietet eine umfassende Palette an Funktionen zum Bearbeiten von Seiteneinstellungen, einschließlich der Einstellung von Rändern, Ausrichtung, Kopf- und Fußzeilen usw.