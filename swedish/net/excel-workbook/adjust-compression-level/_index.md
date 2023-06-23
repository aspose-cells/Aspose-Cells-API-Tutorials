---
title: Justera kompressionsnivån
linktitle: Justera kompressionsnivån
second_title: Aspose.Cells för .NET API-referens
description: Minska storleken på dina Excel-arbetsböcker genom att justera komprimeringsnivån med Aspose.Cells för .NET.
type: docs
weight: 50
url: /sv/net/excel-workbook/adjust-compression-level/
---
I denna steg-för-steg handledning kommer vi att förklara den medföljande C#-källkoden som gör att du kan justera komprimeringsnivån med Aspose.Cells för .NET. Följ stegen nedan för att justera komprimeringsnivån i din Excel-arbetsbok.

## Steg 1: Ställ in käll- och utdatakataloger

```csharp
// källkatalog
string sourceDir = RunExamples.Get_SourceDirectory();
// Utdatakatalog
string outDir = RunExamples.Get_OutputDirectory();
```

I detta första steg definierar vi käll- och utdatakatalogerna för Excel-filerna.

## Steg 2: Ladda Excel-arbetsbok

```csharp
//Ladda Excel-arbetsboken
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
```

 Vi laddar Excel-arbetsboken från den angivna filen med hjälp av`Workbook` klass från Aspose.Cells.

## Steg 3: Ställ in alternativ för säkerhetskopiering

```csharp
// Definiera alternativ för säkerhetskopiering
XlsbSaveOptions options = new XlsbSaveOptions();
```

 Vi skapar en instans av`XlsbSaveOptions` klass för att ställa in sparalternativ.

## Steg 4: Justera komprimeringsnivån (nivå 1)

```csharp
// Justera komprimeringsnivån (nivå 1)
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
let elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 1): " + elapsedMs);
```

 Vi justerar komprimeringsnivån genom att ställa in`CompressionType` till`Level1`. Sedan sparar vi Excel-arbetsboken med detta komprimeringsalternativ specificerat.

## Steg 5: Justera komprimeringsnivån (nivå 6)

```csharp
// Justera komprimeringsnivån (nivå 6)
options.CompressionType = OoxmlCompressionType.Level6;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 6): " + elapsedMs);
```

 Vi upprepar processen för att justera komprimeringsnivån till`Level6` och spara Excel-arbetsboken med det här alternativet.

## Steg 6: Justera komprimeringsnivån (nivå 9)

```csharp
// Justera komprimeringsnivån (nivå 9)
options.CompressionType = OoxmlCompressionType.Level9;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 9): " + elapsedMs);
```

 Vi upprepar processen en sista gång för att justera komprimeringsnivån till`Level9` och spara Excel-arbetsboken med det här alternativet.

### Exempel på källkod för Justera komprimeringsnivå med Aspose.Cells för .NET 
```csharp
//Källkatalog
string sourceDir = RunExamples.Get_SourceDirectory();
string outDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
XlsbSaveOptions options = new XlsbSaveOptions();
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
var elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 1 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level6;
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 6 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level9;
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 9 Elapsed Time: " + elapsedMs);
Console.WriteLine("AdjustCompressionLevel executed successfully.");
```

## Slutsats

Grattis! Du lärde dig hur du justerar komprimeringsnivån i en Excel-arbetsbok med Aspose.Cells för .NET. Experimentera med olika nivåer av komprimering för att hitta den som bäst passar dina behov.

### Vanliga frågor

#### F: Vad är komprimering i en Excel-arbetsbok?

S: Komprimering i en Excel-arbetsbok är en process för att minska filstorleken genom att använda komprimeringsalgoritmer. Detta minskar det lagringsutrymme som krävs och förbättrar prestandan när du laddar och manipulerar filen.

#### F: Vilka nivåer av komprimering är tillgängliga med Aspose.Cells?

S: Med Aspose.Cells kan du justera komprimeringsnivån från 1 till 9. Ju högre komprimeringsnivå, desto mindre blir filstorleken, men det kan också öka bearbetningstiden.

#### F: Hur väljer jag rätt komprimeringsnivå för min Excel-arbetsbok?

S: Valet av komprimeringsnivå beror på dina specifika behov. Om du vill ha maximal komprimering och bearbetningstid är inget problem kan du gå till nivå 9. Om du föredrar en kompromiss mellan filstorlek och bearbetningstid kan du välja en mellannivå.

#### F: Påverkar komprimering datakvaliteten i Excel-arbetsboken?

S: Nej, komprimeringen påverkar inte datakvaliteten i Excel-arbetsboken. Det minskar helt enkelt filstorleken med hjälp av komprimeringstekniker utan att ändra själva data.

#### F: Kan jag justera komprimeringsnivån efter att ha sparat Excel-filen?

S: Nej, när du väl har sparat Excel-filen med en specifik komprimeringsnivå kan du inte justera komprimeringsnivån senare. Du måste spara filen igen med den nya komprimeringsnivån om du vill ändra den.