---
title: Implementera anpassad pappersstorlek på arbetsbladet för rendering
linktitle: Implementera anpassad pappersstorlek på arbetsbladet för rendering
second_title: Aspose.Cells för .NET API-referens
description: Steg-för-steg-guide för att implementera anpassad kalkylbladsstorlek med Aspose.Cells för .NET. Ställ in måtten, lägg till ett meddelande och spara som PDF.
type: docs
weight: 50
url: /sv/net/excel-page-setup/implement-custom-paper-size-of-worksheet-for-rendering/
---
Att implementera en anpassad storlek för ditt kalkylblad kan vara mycket användbart när du vill skapa ett PDF-dokument med en viss storlek. I den här handledningen kommer vi att lära oss hur du använder Aspose.Cells för .NET för att ställa in en anpassad storlek för ett kalkylblad och sedan spara dokumentet som en PDF.

## Steg 1: Skapa utdatamappen

Innan du börjar måste du skapa en utdatamapp där den genererade PDF-filen kommer att sparas. Du kan använda vilken sökväg du vill för din utdatamapp.

```csharp
// Utdatakataloger
string outputDir = "YOUR_OUTPUT_FOLDER";
```

Se till att du anger rätt sökväg till din utdatamapp.

## Steg 2: Skapa arbetsboksobjektet

För att komma igång måste du skapa ett Workbook-objekt med Aspose.Cells. Detta objekt representerar ditt kalkylblad.

```csharp
// Skapa arbetsboksobjektet
Workbook wb = new Workbook();
```

## Steg 3: Tillgång till det första kalkylbladet

När du har skapat arbetsboksobjektet kan du komma åt det första kalkylbladet i det.

```csharp
// Tillgång till det första arbetsbladet
Worksheet ws = wb.Worksheets[0];
```

## Steg 4: Ställ in anpassad kalkylbladsstorlek

 Nu kan du ställa in anpassad kalkylbladsstorlek med`CustomPaperSize(width, height)` metod för klassen PageSetup.

```csharp
// Ställ in anpassad kalkylbladsstorlek (i tum)
ws.PageSetup.CustomPaperSize(6, 4);
```

I det här exemplet har vi ställt in kalkylbladets storlek till 6 tum bred och 4 tum hög.

## Steg 5: Tillgång till cell B4

Efter det kan vi komma åt en specifik cell i kalkylbladet. I det här fallet kommer vi åt cell B4.

```csharp
// Tillgång till cell B4
Cell b4 = ws.Cells["B4"];
```

## Steg 6: Lägga till meddelandet i cell B4

 Vi kan nu lägga till ett meddelande i cell B4 med hjälp av`PutValue(value)` metod.

```csharp
// Lägg till meddelandet i cell B4
b4.PutValue("PDF page size: 6.00 x 4.00 inches");
```

I det här exemplet har vi lagt till meddelandet "PDF-sidstorlek: 6,00" x 4,00" i cell B4.

## Steg 7: Spara kalkylbladet i PDF-format

 Slutligen kan vi spara arbetsbladet i PDF-format med hjälp av`Save(filePath)` arbetsboksobjektets metod.

```csharp
// Spara arbetsbladet i PDF-format
wb.Save(outputDir + "outputCustomPaperSize.pdf");
```

Ange önskad sökväg till den genererade PDF-filen med hjälp av utdatamappen som skapats tidigare.

### Exempel på källkod för Implementera anpassad pappersstorlek på arbetsblad för rendering med Aspose.Cells för .NET 
```csharp
//Utdatakatalog
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//Skapa arbetsboksobjekt
Workbook wb = new Workbook();
//Öppna första kalkylbladet
Worksheet ws = wb.Worksheets[0];
//Ställ in anpassad pappersstorlek i enhet av tum
ws.PageSetup.CustomPaperSize(6, 4);
//Öppna cell B4
Cell b4 = ws.Cells["B4"];
//Lägg till meddelandet i cell B4
b4.PutValue("Pdf Page Dimensions: 6.00 x 4.00 in");
//Spara arbetsboken i pdf-format
wb.Save(outputDir + "outputCustomPaperSize.pdf");
```

## Slutsatser

I den här handledningen lärde du dig hur du implementerar anpassad storlek på ett kalkylblad med Aspose.Cells för .NET. Du kan använda dessa steg för att ställa in specifika dimensioner för dina kalkylblad och sedan spara dokumenten i PDF-format. Vi hoppas att den här guiden har varit till hjälp för att förstå processen för att implementera en anpassad kalkylarksstorlek.

### Vanliga frågor (FAQ)

#### Fråga 1: Kan jag anpassa kalkylarkslayouten ytterligare?

Ja, Aspose.Cells erbjuder många alternativ för att anpassa din kalkylbladslayout. Du kan ställa in anpassade mått, sidorientering, marginaler, sidhuvuden och sidfötter och mycket mer.

#### Fråga 2: Vilka andra utdataformat stöder Aspose.Cells?

Aspose.Cells stöder många olika utdataformat, inklusive PDF, XLSX, XLS, CSV, HTML, TXT och många fler. Du kan välja önskat utdataformat efter dina behov.