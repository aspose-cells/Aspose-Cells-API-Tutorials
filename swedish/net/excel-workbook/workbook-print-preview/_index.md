---
title: Förhandsgranskning av arbetsbok
linktitle: Förhandsgranskning av arbetsbok
second_title: Aspose.Cells för .NET API-referens
description: Lär dig hur du genererar en förhandsvisning av en arbetsbok med Aspose.Cells för .NET.
type: docs
weight: 170
url: /sv/net/excel-workbook/workbook-print-preview/
---
Förhandsgranskning av en arbetsbok är en viktig funktion när du arbetar med Excel-filer med Aspose.Cells för .NET. Du kan enkelt skapa en förhandsgranskning genom att följa dessa steg:

## Steg 1: Ange källkatalog

Först måste du ange källkatalogen där Excel-filen du vill förhandsgranska finns. Så här gör du:

```csharp
// källkatalog
string sourceDir = RunExamples.Get_SourceDirectory();
```

## Steg 2: Ladda arbetsboken

Sedan måste du ladda arbetsboken från den angivna Excel-filen. Så här gör du:

```csharp
// Ladda arbetsboken arbetsbok
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
```

## Steg 3: Konfigurera bild- och utskriftsalternativ

Innan du skapar förhandsgranskningen kan du konfigurera bilden och utskriftsalternativen efter behov. I det här exemplet använder vi standardalternativen. Så här gör du:

```csharp
// Bild- och utskriftsalternativ
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
```

## Steg 4: Skapa förhandsgranskningen av arbetsboken

Nu kan du skapa förhandsgranskningen av arbetsboken genom att använda klassen WorkbookPrintingPreview. Så här gör du:

```csharp
// Skriv ut förhandsvisning av arbetsboken
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
```

## Steg 5: Skapa förhandsvisningen av kalkylbladet

Om du vill generera förhandsvisningen av ett specifikt kalkylblad kan du använda klassen SheetPrintingPreview. Här är ett exempel :

```csharp
// Skriv ut förhandsvisning av kalkylbladet
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Number of worksheet pages: " + preview2.EvaluatedPageCount);
```

### Exempel på källkod för förhandsvisning av arbetsbok med Aspose.Cells för .NET 
```csharp
//Källkatalog
string sourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Worksheet page count: " + preview2.EvaluatedPageCount);
Console.WriteLine("PrintPreview executed successfully.");
```

## Slutsats

Att generera förhandsgranskningen av en arbetsbok är en kraftfull funktion som erbjuds av Aspose.Cells för .NET. Genom att följa stegen ovan kan du enkelt förhandsgranska din Excel-arbetsbok och få information om antalet sidor som ska skrivas ut.

### Vanliga frågor

#### F: Hur kan jag ange en annan källkatalog för att ladda min arbetsbok?
    
 S: Du kan använda`Set_SourceDirectory` metod för att ange en annan källkatalog. Till exempel:`RunExamples.Set_SourceDirectory("Path_to_the_source_directory")`.

#### F: Kan jag anpassa bilden och utskriftsalternativen när jag skapar förhandsgranskningen?
    
 S: Ja, du kan anpassa bild- och utskriftsalternativ genom att ändra egenskaperna för`ImageOrPrintOptions` objekt. Du kan till exempel ställa in bildupplösning, utdatafilformat etc.

#### F: Är det möjligt att skapa en förhandsgranskning för flera kalkylblad i en arbetsbok?
    
S: Ja, du kan iterera över de olika kalkylbladen i arbetsboken och generera en förhandsgranskning för varje ark med`SheetPrintingPreview` klass.

#### F: Hur sparar jag förhandsgranskningen som en bild eller PDF-fil?
    
 A: Du kan använda`ToImage` eller`ToPdf` metod av`WorkbookPrintingPreview` eller`SheetPrintingPreview` objekt för att spara förhandsvisningen som bild eller PDF-fil.

#### F: Vad kan jag göra med förhandsgranskningen när den har skapats?
    
S: När du har skapat förhandsgranskningen kan du visa den på skärmen, spara den som en bild eller PDF-fil, eller använda den för andra operationer som att skicka via e-post eller skriva ut.
	