---
title: Extrahera inbäddad Mol-fil
linktitle: Extrahera inbäddad Mol-fil
second_title: Aspose.Cells för .NET API-referens
description: Lär dig hur du enkelt extraherar inbäddade MOL-filer från en Excel-arbetsbok med Aspose.Cells för .NET.
type: docs
weight: 90
url: /sv/net/excel-workbook/extract-embedded-mol-file/
---
I den här handledningen går vi igenom steg-för-steg hur du extraherar en inbäddad MOL-fil från en Excel-arbetsbok med Aspose.Cells-biblioteket för .NET. Du kommer att lära dig hur du bläddrar i arbetsboksbladen, extraherar motsvarande OLE-objekt och sparar de extraherade MOL-filerna. Följ stegen nedan för att slutföra denna uppgift.

## Steg 1: Definiera käll- och utdatakataloger
Först måste vi definiera käll- och utdatakatalogerna i vår kod. Dessa kataloger anger var källarbetsboken för Excel finns och var de extraherade MOL-filerna kommer att sparas. Här är motsvarande kod:

```csharp
// Kataloger
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
```

Var noga med att ange lämpliga sökvägar efter behov.

## Steg 2: Laddar Excel-arbetsboken
Nästa steg är att ladda Excel-arbetsboken som innehåller de inbäddade OLE-objekten och MOL-filerna. Här är koden för att ladda arbetsboken:

```csharp
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
```

Se till att ange källfilens namn korrekt i koden.

## Steg 3: Gå igenom arken och extrahera MOL-filerna
Nu ska vi gå igenom varje ark i arbetsboken och extrahera motsvarande OLE-objekt, som innehåller MOL-filerna. Här är motsvarande kod:

```csharp
var index = 1;
foreach(Worksheet sheet in workbook.Worksheets)
{
     OleObjectCollection oles = sheet.OleObjects;
     foreach(OleObject ole in oles)
     {
         string fileName = outputDir + "OleObject" + index + ".mol";
         FileStream fs = File.Create(fileName);
         fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
         fs. Close();
         index++;
     }
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

Den här koden går igenom varje ark i arbetsboken, hämtar OLE-objekten och sparar de extraherade MOL-filerna till utdatakatalogen.

### Exempel på källkod för Extrahera Embedded Mol File med Aspose.Cells för .NET 
```csharp
//kataloger
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
var index = 1;
foreach (Worksheet sheet in workbook.Worksheets)
{
	OleObjectCollection oles = sheet.OleObjects;
	foreach (OleObject ole in oles)
	{
		string fileName = outputDir + "OleObject" + index + ".mol ";
		FileStream fs = File.Create(fileName);
		fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
		fs.Close();
		index++;
	}
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

## Slutsats
Grattis! Du har lärt dig hur du extraherar en inbäddad MOL-fil från en Excel-arbetsbok med Aspose.Cells för .NET. Du kan nu tillämpa denna kunskap för att extrahera MOL-filer från dina egna Excel-arbetsböcker. Utforska gärna Aspose.Cells-biblioteket ytterligare och lär dig om dess andra kraftfulla funktioner.

### Vanliga frågor

#### F: Vad är en MOL-fil?
 
S: En MOL-fil är ett filformat som används för att representera kemiska strukturer inom beräkningskemi. Den innehåller information om atomer, bindningar och andra molekylära egenskaper.

#### F: Fungerar den här metoden med alla Excel-filtyper?

S: Ja, den här metoden fungerar med alla Excel-filtyper som stöds av Aspose.Cells.

#### F: Kan jag extrahera flera MOL-filer samtidigt?

S: Ja, du kan extrahera flera MOL-filer samtidigt genom att iterera genom OLE-objekt på varje ark i arbetsboken.