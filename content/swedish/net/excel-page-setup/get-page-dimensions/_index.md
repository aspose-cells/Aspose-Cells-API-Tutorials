---
title: Skaffa sidmått
linktitle: Skaffa sidmått
second_title: Aspose.Cells för .NET API-referens
description: Lär dig hur du hämtar siddimensioner i Excel med Aspose.Cells för .NET. Steg för steg guide med källkod i C#.
type: docs
weight: 40
url: /sv/net/excel-page-setup/get-page-dimensions/
---
Aspose.Cells för .NET är ett kraftfullt bibliotek som låter utvecklare arbeta med Microsoft Excel-filer programmatiskt. Den erbjuder ett brett utbud av funktioner för att manipulera Excel-dokument, inklusive möjligheten att få siddimensioner. I den här handledningen går vi igenom stegen för att hämta siddimensioner med Aspose.Cells för .NET.

## Steg 1: Skapa en instans av klassen Workbook

Till att börja med måste vi skapa en instans av klassen Workbook, som representerar Excel-arbetsboken. Detta kan uppnås med hjälp av följande kod:

```csharp
Workbook book = new Workbook();
```

## Steg 2: Få åtkomst till kalkylarket

Därefter måste vi navigera till kalkylbladet i arbetsboken där vi vill ställa in sidmåtten. I det här exemplet, anta att vi vill arbeta med det första kalkylbladet. Vi kan komma åt den med följande kod:

```csharp
Worksheet sheet = book.Worksheets[0];
```

## Steg 3: Ställ in pappersstorleken till A2 och skriv ut bredd och höjd i tum

Nu kommer vi att ställa in pappersstorleken till A2 och skriva ut sidans bredd och höjd i tum. Detta kan uppnås med hjälp av följande kod:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("A2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Steg 4: Ställ in pappersstorleken till A3 och skriv ut bredd och höjd i tum

Därefter ställer vi in pappersstorleken till A3 och skriver ut sidans bredd och höjd i tum. Här är motsvarande kod:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("A3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Steg 5: Ställ in pappersstorleken till A4 och skriv ut bredd och höjd i tum

Vi kommer nu att ställa in pappersstorleken till A4 och skriva ut sidans bredd och höjd i tum. Här är koden:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("A4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Steg 6: Ställ in pappersstorleken på Letter och skriv ut bredden och höjden i tum

Slutligen ställer vi in pappersstorleken till Letter och skriver ut sidans bredd och höjd i tum. Här är koden:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("Letter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

### Exempel på källkod för Get Page Dimensions med Aspose.Cells för .NET 
```csharp
// Skapa en instans av Workbook-klassen
Workbook book = new Workbook();
// Öppna första kalkylbladet
Worksheet sheet = book.Worksheets[0];
// Ställ in pappersstorleken till A2 och skriv ut papperets bredd och höjd i tum
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Ställ in pappersstorleken till A3 och skriv ut papperets bredd och höjd i tum
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Ställ in pappersstorleken till A4 och skriv ut papperets bredd och höjd i tum
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Ställ in pappersstorleken på Letter och skriv papperets bredd och höjd i tum
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
Console.WriteLine("GetPageDimensions executed successfully.\r\n");
```

## Slutsats

Grattis! Du lärde dig hur du hämtar siddimensioner med Aspose.Cells för .NET. Den här funktionen kan vara användbar när du behöver utföra specifika operationer baserat på siddimensioner i dina Excel-filer.

Glöm inte att ytterligare utforska dokumentationen av Aspose.Cells för att upptäcka alla kraftfulla funktioner som den erbjuder.

### FAQ's

#### 1. Vilka andra pappersstorlekar stöder Aspose.Cells for .NET?

Aspose.Cells för .NET stöder en mängd olika pappersstorlekar inklusive A1, A5, B4, B5, Executive, Legal, Letter och många fler. Du kan kontrollera dokumentationen för en fullständig lista över pappersstorlekar som stöds.

#### 2. Kan jag ställa in anpassade siddimensioner med Aspose.Cells för .NET?

Ja, du kan ställa in anpassade sidmått genom att ange önskad bredd och höjd. Aspose.Cells erbjuder full flexibilitet för att anpassa siddimensioner efter dina behov.

#### 3. Kan jag få sidmått i andra enheter än tum?

Ja, Aspose.Cells för .NET låter dig få siddimensioner i olika enheter, inklusive tum, centimeter, millimeter och punkter.

#### 4. Har Aspose.Cells för .NET stöd för andra redigeringsfunktioner för sidinställningar?

Ja, Aspose.Cells erbjuder ett komplett utbud av funktioner för att redigera sidinställningar, inklusive inställning av marginaler, orientering, sidhuvuden och sidfötter, etc.