---
title: Ta bort befintliga skrivarinställningar för arbetsblad
linktitle: Ta bort befintliga skrivarinställningar för arbetsblad
second_title: Aspose.Cells för .NET API-referens
description: Lär dig hur du tar bort befintliga skrivarinställningar från Excel-kalkylblad med Aspose.Cells för .NET.
type: docs
weight: 80
url: /sv/net/excel-page-setup/remove-existing-printer-settings-of-worksheets/
---
I den här handledningen går vi igenom steg för steg hur du tar bort befintliga skrivarinställningar från kalkylblad i Excel med Aspose.Cells för .NET. Vi kommer att använda C#-källkod för att illustrera processen.

## Steg 1: Sätta upp miljön

Se till att du har Aspose.Cells för .NET installerat på din maskin. Skapa också ett nytt projekt i din föredragna utvecklingsmiljö.

## Steg 2: Importera nödvändiga bibliotek

Importera de bibliotek som behövs för att arbeta med Aspose.Cells i din kodfil. Här är motsvarande kod:

```csharp
using Aspose.Cells;
```

## Steg 3: Ställ in käll- och utdatakataloger

Ställ in käll- och utdatakatalogerna där den ursprungliga Excel-filen finns och var du vill spara den ändrade filen. Använd följande kod:

```csharp
string sourceDir = "SOURCE DIRECTORY PATH";
string outputDir = "OUTPUT DIRECTORY PATH";
```

Var noga med att ange fullständiga katalogsökvägar.

## Steg 4: Laddar källfilen för Excel

Ladda källfilen för Excel med följande kod:

```csharp
Workbook wb = new Workbook(sourceDir + "fileName.xlsx");
```

Detta kommer att ladda den angivna Excel-filen i arbetsboksobjektet.

## Steg 5: Navigera i kalkylbladen

Iterera genom alla kalkylblad i arbetsboken med hjälp av en slinga. Använd följande kod:

```csharp
int sheetCount = wb. Worksheets. Count;

for (int i = 0; i < sheetCount; i++)
{
     Worksheet ws = wb.Worksheets[i];
     // Resten av koden kommer att läggas till i nästa steg.
}
```

## Steg 6: Ta bort befintliga skrivarinställningar

Kontrollera om det finns skrivarinställningar för varje kalkylblad och ta bort dem vid behov. Använd följande kod:

```csharp
PageSetup ps = ws.PageSetup;

if (ps.PrinterSettings != null)
{
     Console.WriteLine("Printer settings for this spreadsheet exist.");
     Console.WriteLine("Sheet name: " + ws.Name);
     Console.WriteLine("Paper size: " + ps.PaperSize);

     ps.PrinterSettings = null;

     Console.WriteLine("Printer settings for this spreadsheet have been removed by setting them to null.");
     Console.WriteLine("");
}
```

## Steg 7: Spara den modifierade arbetsboken

Spara den ändrade arbetsboken med följande kod:

```csharp
wb.Save(outputDir + "modifiedFilename.xlsx");
```

Detta kommer att spara den modifierade arbetsboken i den angivna utdatakatalogen.

### Exempel på källkod för att ta bort befintliga skrivarinställningar för arbetsblad med Aspose.Cells för .NET 
```csharp
//Källkatalog
string sourceDir = RunExamples.Get_SourceDirectory();
//Utdatakatalog
string outputDir = RunExamples.Get_OutputDirectory();
//Ladda källfilen i Excel
Workbook wb = new Workbook(sourceDir + "sampleRemoveExistingPrinterSettingsOfWorksheets.xlsx");
//Få arbetsbokens antal ark
int sheetCount = wb.Worksheets.Count;
//Iterera alla ark
for (int i = 0; i < sheetCount; i++)
{
    //Öppna det i-te arbetsbladet
    Worksheet ws = wb.Worksheets[i];
    //Få åtkomst till sidinställningar för kalkylblad
    PageSetup ps = ws.PageSetup;
    //Kontrollera om det finns skrivarinställningar för detta kalkylblad
    if (ps.PrinterSettings != null)
    {
        //Skriv ut följande meddelande
        Console.WriteLine("PrinterSettings of this worksheet exist.");
        //Skriv ut arkets namn och dess pappersstorlek
        Console.WriteLine("Sheet Name: " + ws.Name);
        Console.WriteLine("Paper Size: " + ps.PaperSize);
        //Ta bort skrivarinställningarna genom att ställa in dem på null
        ps.PrinterSettings = null;
        Console.WriteLine("Printer settings of this worksheet are now removed by setting it null.");
        Console.WriteLine("");
    }//om
}//för
//Spara arbetsboken
wb.Save(outputDir + "outputRemoveExistingPrinterSettingsOfWorksheets.xlsx");
```

## Slutsats

Du har nu lärt dig hur du tar bort befintliga skrivarinställningar från kalkylblad i Excel med Aspose.Cells för .NET. Den här handledningen ledde dig genom varje steg i processen, från att ställa in miljön till att navigera genom kalkylblad och rensa skrivarinställningar. Du kan nu använda denna kunskap för att hantera skrivarinställningar i dina Excel-filer.

### FAQ's

#### F1: Hur vet jag om ett kalkylblad har befintliga skrivarinställningar?

 S1: Du kan kontrollera om det finns skrivarinställningar för ett kalkylblad genom att öppna`PrinterSettings` egendom av`PageSetup` objekt. Om värdet inte är null betyder det att det finns befintliga skrivarinställningar.

#### F2: Kan jag ta bort skrivarinställningar endast för ett specifikt kalkylblad?

 S2: Ja, du kan använda samma tillvägagångssätt för att ta bort skrivarinställningar för ett specifikt kalkylblad genom att komma åt det kalkylbladets`PageSetup` objekt.

#### F3: Tar den här metoden bort andra layoutinställningar också?

S3: Nej, den här metoden tar bara bort skrivarinställningar. Andra layoutinställningar, såsom marginaler, pappersorientering, etc., förblir oförändrade.

#### F4: Fungerar den här metoden för alla Excel-filformat, som .xls och .xlsx?

S4: Ja, den här metoden fungerar för alla Excel-filformat som stöds av Aspose.Cells, inklusive .xls och .xlsx.

#### F5: Görs ändringar i skrivarinställningarna permanenta i den redigerade Excel-filen?

S5: Ja, ändringar av skrivarinställningarna sparas permanent i den redigerade Excel-filen.