---
title: Få pappersbredd och höjd på arbetsbladet
linktitle: Få pappersbredd och höjd på arbetsbladet
second_title: Aspose.Cells för .NET API-referens
description: Skapa en steg-för-steg-guide för att förklara följande C#-källkod för att få pappersbredden och höjden på ett kalkylblad med Aspose.Cells för .NET.
type: docs
weight: 80
url: /sv/net/excel-display-settings-csharp-tutorials/get-paper-width-and-height-of-worksheet/
---
I den här handledningen tar vi dig steg för steg för att förklara följande C#-källkod för att få pappersbredden och höjden på ett kalkylblad med Aspose.Cells för .NET. Följ stegen nedan:

## Steg 1: Skapa arbetsboken
 Börja med att skapa en ny arbetsbok med hjälp av`Workbook` klass:

```csharp
Workbook wb = new Workbook();
```

## Steg 2: Öppna det första kalkylbladet
 Navigera sedan till det första kalkylbladet i arbetsboken med hjälp av`Worksheet` klass:

```csharp
Worksheet ws = wb.Worksheets[0];
```

## Steg 3: Ställ in pappersstorleken till A2 och visa papperets bredd och höjd i tum
 Använd`PaperSize` egendom av`PageSetup` objekt för att ställa in pappersstorleken till A2, använd sedan`PaperWidth` och`PaperHeight` egenskaper för att få papperets bredd respektive höjd. Visa dessa värden med hjälp av`Console.WriteLine` metod:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

## Steg 4: Upprepa stegen för andra pappersstorlekar
Upprepa de föregående stegen, ändra pappersstorleken till A3, A4 och Letter, och visa sedan värdena för pappersbredd och höjd för varje storlek:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

### Exempel på källkod för få pappersbredd och höjd på arbetsblad med Aspose.Cells för .NET 

```csharp
//Skapa arbetsbok
Workbook wb = new Workbook();
//Öppna första kalkylbladet
Worksheet ws = wb.Worksheets[0];
//Ställ in pappersstorleken till A2 och skriv ut papperets bredd och höjd i tum
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Ställ in pappersstorleken till A3 och skriv ut papperets bredd och höjd i tum
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Ställ in pappersstorleken till A4 och skriv ut papperets bredd och höjd i tum
ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Ställ in pappersstorleken på Letter och skriv papperets bredd och höjd i tum
ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```


## Slutsats

Du lärde dig hur du använder Aspose.Cells för .NET för att få pappersbredden och höjden på ett kalkylark. Den här funktionen kan vara användbar för konfiguration och exakt layout av dina Excel-dokument.

### Vanliga frågor (FAQ)

#### Vad är Aspose.Cells för .NET?

Aspose.Cells för .NET är ett kraftfullt bibliotek för att manipulera och bearbeta Excel-filer i .NET-applikationer. Den erbjuder många funktioner för att skapa, ändra, konvertera och analysera Excel-filer.

#### Hur kan jag få pappersstorleken för ett kalkylark med Aspose.Cells för .NET?

 Du kan använda`PageSetup` klass av`Worksheet` objekt för att komma åt pappersstorleken. Använd`PaperSize` egenskap för att ställa in pappersstorleken och`PaperWidth` och`PaperHeight` egenskaper för att få papperets bredd respektive höjd.

#### Vilka pappersstorlekar stöder Aspose.Cells för .NET?

Aspose.Cells för .NET stöder ett brett utbud av vanliga pappersstorlekar, såsom A2, A3, A4 och Letter, såväl som många andra anpassade storlekar.

#### Kan jag anpassa pappersstorleken för ett kalkylark med Aspose.Cells för .NET?

Ja, du kan ställa in en anpassad pappersstorlek genom att ange exakta bredd- och höjdmått med hjälp av`PaperWidth` och`PaperHeight` egenskaper hos`PageSetup` klass.