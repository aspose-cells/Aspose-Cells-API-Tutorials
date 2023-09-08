---
title: Filtrera definierade namn medan arbetsboken laddas
linktitle: Filtrera definierade namn medan arbetsboken laddas
second_title: Aspose.Cells för .NET API-referens
description: Lär dig hur du filtrerar definierade namn när du laddar en Excel-arbetsbok med Aspose.Cells för .NET.
type: docs
weight: 100
url: /sv/net/excel-workbook/filter-defined-names-while-loading-workbook/
---
När du arbetar med Excel-arbetsböcker i en .NET-applikation är det ofta nödvändigt att filtrera data vid belastning. Aspose.Cells för .NET är ett kraftfullt bibliotek för att enkelt manipulera Excel-arbetsböcker. I den här guiden kommer vi att visa dig hur du filtrerar de namn som definieras när du laddar en arbetsbok med Aspose.Cells för .NET. Följ dessa enkla steg för att få önskat resultat:

## Steg 1: Ange laddningsalternativ

Först måste du ange laddningsalternativen för att definiera arbetsbokens laddningsbeteende. I vårt fall vill vi ignorera namnen som ställs in vid laddning. Så här gör du med Aspose.Cells:

```csharp
// Anger laddningsalternativ
LoadOptions opts = new LoadOptions();

// Ladda inte definierade namn
opts. LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
```

## Steg 2: Ladda arbetsboken

När laddningsalternativen är konfigurerade kan du ladda Excel-arbetsboken från källfilen. Var noga med att ange rätt filsökväg. Här är en exempelkod:

```csharp
// Ladda arbetsboken
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
```

## Steg 3: Spara den filtrerade arbetsboken

Efter att ha laddat arbetsboken kan du utföra andra operationer eller redigeringar efter behov. Sedan kan du spara den filtrerade arbetsboken till en utdatafil. Här är hur:

```csharp
// Spara den filtrerade Excel-arbetsboken
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
```

### Exempel på källkod för filterdefinierade namn under laddning av arbetsbok med Aspose.Cells för .NET 
```csharp
//Ange laddningsalternativ
LoadOptions opts = new LoadOptions();
//Vi vill inte ladda definierade namn
opts.LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
//Ladda arbetsboken
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
//Spara den utgående Excel-filen, den kommer att bryta formeln i C1
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
Console.WriteLine("FilterDefinedNamesWhileLoadingWorkbook executed successfully.");
```

## Slutsats

Filtrering av definierade namn när du läser in en Excel-arbetsbok kan vara avgörande för många applikationer. Aspose.Cells för .NET gör denna uppgift enklare genom att tillhandahålla flexibla alternativ för att ladda och filtrera data. Genom att följa stegen i den här guiden kommer du effektivt att kunna filtrera bort de definierade namnen och uppnå önskade resultat i dina Excel-arbetsböcker.


### Vanliga frågor

#### F: Stöder Aspose.Cells andra programmeringsspråk förutom C#?
    
S: Ja, Aspose.Cells är ett plattformsoberoende bibliotek som stöder många programmeringsspråk som Java, Python, C++och många fler.

#### F: Kan jag filtrera andra datatyper när jag laddar en arbetsbok med Aspose.Cells?
    
S: Ja, Aspose.Cells erbjuder en rad filtreringsalternativ för data inklusive formler, stilar, makron, etc.

#### F: Behåller Aspose.Cells formateringen och egenskaperna för den ursprungliga arbetsboken?
    
S: Ja, Aspose.Cells behåller formatering, stilar, formler och andra egenskaper hos den ursprungliga arbetsboken när du arbetar med Excel-filer.