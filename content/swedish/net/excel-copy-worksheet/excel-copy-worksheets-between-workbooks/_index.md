---
title: Excel Kopiera arbetsblad mellan arbetsböcker
linktitle: Excel Kopiera arbetsblad mellan arbetsböcker
second_title: Aspose.Cells för .NET API-referens
description: Kopiera enkelt kalkylblad mellan Excel-arbetsböcker med Aspose.Cells för .NET.
type: docs
weight: 30
url: /sv/net/excel-copy-worksheet/excel-copy-worksheets-between-workbooks/
---
den här handledningen guidar vi dig genom stegen för att kopiera kalkylblad mellan Excel-arbetsböcker med Aspose.Cells-biblioteket för .NET. Följ instruktionerna nedan för att slutföra denna uppgift.

## Steg 1: Förberedelser

Se till att du har installerat Aspose.Cells för .NET och skapat ett C#-projekt i din föredragna integrerade utvecklingsmiljö (IDE).

## Steg 2: Ställ in sökvägen till dokumentkatalogen

 Deklarera a`dataDir` variabel och initiera den med sökvägen till din dokumentkatalog. Till exempel :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Se till att byta ut`"YOUR_DOCUMENTS_DIRECTORY"` med den faktiska sökvägen till din katalog.

## Steg 3: Definiera sökvägen till indatafilen

 Deklarera en`InputPath` variabel och initiera den med den fullständiga sökvägen till Excel-filen från vilken du vill kopiera kalkylarket. Till exempel :

```csharp
string InputPath = dataDir + "book1.xls";
```

 Se till att du har Excel-filen`book1.xls` i din dokumentkatalog eller ange korrekt filnamn och plats.

## Steg 4: Skapa en första Excel-arbetsbok

 Använd`Workbook` klass av Aspose.Cells för att skapa en första Excel-arbetsbok och öppna den angivna filen:

```csharp
Workbook excelWorkbook0 = new Workbook(InputPath);
```

## Steg 5: Skapa en andra Excel-arbetsbok

Skapa en andra Excel-arbetsbok:

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## Steg 6: Kopiera kalkylbladet från den första arbetsboken till den andra arbetsboken

 Använd`Copy`metod för att kopiera det första kalkylbladet från den första arbetsboken till den andra arbetsboken:

```csharp
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
```

## Steg 7: Spara Excel-filen

Spara Excel-filen som innehåller det kopierade kalkylarket:

```csharp
excelWorkbook1.Save(dataDir + "Copy WorksheetsBetweenWorkbooks_out.xls");
```

Var noga med att ange önskad sökväg och filnamn för utdatafilen.

### Exempel på källkod för Excel Kopiera arbetsblad mellan arbetsböcker med Aspose.Cells för .NET 
```csharp
//Sökvägen till dokumentkatalogen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Skapa en arbetsbok.
// Öppna en fil i den första boken.
Workbook excelWorkbook0 = new Workbook(InputPath);
// Skapa en annan arbetsbok.
Workbook excelWorkbook1 = new Workbook();
// Kopiera det första arket i den första boken till den andra boken.
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
// Spara filen.
excelWorkbook1.Save(dataDir + "CopyWorksheetsBetweenWorkbooks_out.xls");
```

## Slutsats

Grattis! Du har nu lärt dig hur du kopierar kalkylblad mellan Excel-arbetsböcker med Aspose.Cells för .NET. Använd gärna denna metod i dina egna projekt för att effektivt manipulera Excel-filer.

### Vanliga frågor

#### F. Vilka bibliotek behövs för att använda Aspose.Cells för .NET?

A. För att använda Aspose.Cells för .NET måste du inkludera Aspose.Cells-biblioteket i ditt projekt. Se till att du har refererat till det här biblioteket korrekt i din integrerade utvecklingsmiljö (IDE).

#### F. Stöder Aspose.Cells andra Excel-filformat, såsom XLSX?

A. Ja, Aspose.Cells stöder olika Excel-filformat inklusive XLSX, XLS, CSV, HTML och många fler. Du kan manipulera dessa filformat med funktionerna i Aspose.Cells för .NET.

#### F. Kan jag anpassa layoutalternativen när jag kopierar kalkylarket?

A.  Ja, du kan anpassa sidinställningarna när du kopierar kalkylarket med hjälp av egenskaperna för`PageSetup` objekt. Du kan ange sidhuvuden, sidfötter, marginaler, orienteringar osv.