---
title: Afdrukvoorbeeld van werkmap
linktitle: Afdrukvoorbeeld van werkmap
second_title: Aspose.Cells voor .NET API-referentie
description: Leer hoe u een afdrukvoorbeeld van een werkmap kunt genereren met Aspose.Cells voor .NET.
type: docs
weight: 170
url: /nl/net/excel-workbook/workbook-print-preview/
---
Afdrukvoorbeeld van een werkmap is een essentiële functie bij het werken met Excel-bestanden met Aspose.Cells voor .NET. U kunt eenvoudig een afdrukvoorbeeld genereren door deze stappen te volgen:

## Stap 1: Geef de bronmap op

Eerst moet u de bronmap opgeven waar het Excel-bestand waarvan u een voorbeeld wilt bekijken, zich bevindt. Hier leest u hoe u het moet doen:

```csharp
// bronmap
string sourceDir = RunExamples.Get_SourceDirectory();
```

## Stap 2: Laad de werkmap

Vervolgens moet u de werkmap Werkmap laden vanuit het opgegeven Excel-bestand. Hier leest u hoe u het moet doen:

```csharp
// Laad de werkmap Werkmap
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
```

## Stap 3: Configureer afbeeldings- en afdrukopties

Voordat u het afdrukvoorbeeld genereert, kunt u de afbeelding en afdrukopties naar wens configureren. In dit voorbeeld gebruiken we de standaardopties. Hier leest u hoe u het moet doen:

```csharp
// Afbeeldings- en printopties
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
```

## Stap 4: Genereer het afdrukvoorbeeld van de werkmap

Nu kunt u het afdrukvoorbeeld van de Workbook-werkmap genereren met behulp van de WorkbookPrintingPreview-klasse. Hier leest u hoe u het moet doen:

```csharp
// Afdrukvoorbeeld van de werkmap
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
```

## Stap 5: Genereer het afdrukvoorbeeld van het werkblad

Als u het afdrukvoorbeeld van een specifiek werkblad wilt genereren, kunt u de klasse SheetPrintingPreview gebruiken. Hier is een voorbeeld :

```csharp
// Afdrukvoorbeeld van het werkblad
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Number of worksheet pages: " + preview2.EvaluatedPageCount);
```

### Voorbeeldbroncode voor afdrukvoorbeeld van werkmap met Aspose.Cells voor .NET 
```csharp
//Bronmap
string sourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Worksheet page count: " + preview2.EvaluatedPageCount);
Console.WriteLine("PrintPreview executed successfully.");
```

## Conclusie

Het genereren van een afdrukvoorbeeld van een werkmap is een krachtige functie die wordt aangeboden door Aspose.Cells voor .NET. Door de bovenstaande stappen te volgen, kunt u eenvoudig een voorbeeld van uw Excel-werkmap bekijken en informatie krijgen over het aantal af te drukken pagina's.

### Veelgestelde vragen

#### Vraag: Hoe kan ik een andere bronmap opgeven om mijn werkmap te laden?
    
 Antwoord: U kunt de`Set_SourceDirectory` methode om een andere bronmap op te geven. Bijvoorbeeld:`RunExamples.Set_SourceDirectory("Path_to_the_source_directory")`.

#### Vraag: Kan ik de afbeeldings- en afdrukopties aanpassen bij het genereren van het afdrukvoorbeeld?
    
 A: Ja, u kunt afbeeldings- en afdrukopties aanpassen door de eigenschappen van het`ImageOrPrintOptions` voorwerp. U kunt bijvoorbeeld de afbeeldingsresolutie, het uitvoerbestandsformaat, enz. instellen.

#### Vraag: Is het mogelijk om een afdrukvoorbeeld te genereren voor meerdere werkbladen in een werkmap?
    
A: Ja, u kunt de verschillende werkbladen in de werkmap doorlopen en voor elk werkblad een afdrukvoorbeeld genereren met behulp van de`SheetPrintingPreview` klas.

#### Vraag: Hoe bewaar ik het afdrukvoorbeeld als afbeelding of PDF-bestand?
    
 EEN: U kunt gebruiken`ToImage` of`ToPdf` methode van`WorkbookPrintingPreview` of`SheetPrintingPreview` object om het afdrukvoorbeeld op te slaan als afbeelding of PDF-bestand.

#### Vraag: Wat kan ik doen met het afdrukvoorbeeld nadat het is gegenereerd?
    
A: Nadat u het afdrukvoorbeeld heeft gegenereerd, kunt u het op het scherm bekijken, opslaan als afbeelding of PDF-bestand of gebruiken voor andere bewerkingen, zoals verzenden per e-mail of afdrukken.
	