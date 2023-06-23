---
title: Bestäm om pappersstorleken på arbetsbladet är automatisk
linktitle: Bestäm om pappersstorleken på arbetsbladet är automatisk
second_title: Aspose.Cells för .NET API-referens
description: Lär dig hur du avgör om ett kalkylarks pappersstorlek är automatisk med Aspose.Cells för .NET.
type: docs
weight: 20
url: /sv/net/excel-page-setup/determine-if-paper-size-of-worksheet-is-automatic/
---
den här artikeln tar vi dig steg för steg för att förklara följande C#-källkod: Bestäm om pappersstorleken för ett kalkylblad är automatisk med Aspose.Cells för .NET. Vi kommer att använda Aspose.Cells-biblioteket för .NET för att utföra denna operation. Följ stegen nedan för att avgöra om pappersstorleken för ett kalkylblad är automatisk.

## Steg 1: Ladda arbetsböcker
Det första steget är att ladda arbetsböckerna. Vi kommer att ha två arbetsböcker: en med automatisk pappersstorlek inaktiverad och den andra med automatisk pappersstorlek aktiverad. Här är koden för att ladda arbetsböckerna:

```csharp
// källkatalog
string sourceDir = "YOUR_SOURCE_DIR";
// Utdatakatalog
string outputDir = "YOUR_OUTPUT_DIRECTORY";

// Ladda den första arbetsboken med automatisk pappersstorlek inaktiverad
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");

// Ladda den andra arbetsboken med automatisk pappersstorlek aktiverad
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
```

## Steg 2: Få åtkomst till kalkylblad
Nu när vi har laddat arbetsböckerna måste vi komma åt arbetsbladen så att vi kan kontrollera den automatiska pappersstorleken. Vi kommer att gå till det första arbetsbladet av de två arbetsböckerna. Här är koden för att komma åt den:

```csharp
//Gå till det första kalkylbladet i den första arbetsboken
Worksheet ws11 = wb1.Worksheets[0];

// Gå till det första kalkylbladet i den andra arbetsboken
Worksheet ws12 = wb2.Worksheets[0];
```

## Steg 3: Kontrollera den automatiska pappersstorleken
 I det här steget kommer vi att kontrollera om kalkylbladets pappersstorlek är automatisk. Vi kommer att använda`PageSetup.IsAutomaticPaperSize` egendom för att få denna information. Vi visar sedan resultatet. Här är koden för det:

```csharp
// Visa egenskapen IsAutomaticPaperSize för det första kalkylbladet i den första arbetsboken
Console.WriteLine("First worksheet in first workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);

// Visa egenskapen IsAutomaticPaperSize för det första kalkylbladet i den andra arbetsboken
Console.WriteLine("First worksheet of second workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);

```

### Exempel på källkod för Bestäm om pappersstorleken på arbetsbladet är automatisk med Aspose.Cells för .NET 
```csharp
//Källkatalog
string sourceDir = "YOUR_SOURCE_DIRECTORY";
//Utdatakatalog
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//Ladda den första arbetsboken med automatisk pappersstorlek falsk
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");
//Ladda den andra arbetsboken med automatisk pappersstorlek sann
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
//Få tillgång till det första kalkylbladet i båda arbetsböckerna
Worksheet ws11 = wb1.Worksheets[0];
Worksheet ws12 = wb2.Worksheets[0];
//Skriv ut egenskapen PageSetup.IsAutomaticPaperSize för båda kalkylbladen
Console.WriteLine("First Worksheet of First Workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);
Console.WriteLine("First Worksheet of Second Workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);
Console.WriteLine();
Console.WriteLine("DetermineIfPaperSizeOfWorksheetIsAutomatic executed successfully.\r\n");
```


## Slutsats
den här artikeln lärde vi oss hur man avgör om pappersstorleken på ett kalkylblad är automatisk med Aspose.Cells för .NET. Vi följde följande steg: laddade arbetsböckerna,

tillgång till kalkylblad och automatisk pappersstorlekskontroll. Nu kan du använda denna kunskap för att avgöra om pappersstorleken på dina kalkylblad är automatisk.

### Vanliga frågor

#### F: Hur kan jag ladda arbetsböcker med Aspose.Cells för .NET?

S: Du kan ladda arbetsböcker med klassen Workbook från Aspose.Cells-biblioteket. Använd metoden Workbook.Load för att ladda en arbetsbok från en fil.

#### F: Kan jag kontrollera den automatiska pappersstorleken för andra kalkylblad?

S: Ja, du kan kontrollera den automatiska pappersstorleken för alla kalkylblad genom att gå till egenskapen PageSetup.IsAutomaticPaperSize för motsvarande kalkylbladsobjekt.

#### F: Hur kan jag ändra den automatiska pappersstorleken för ett kalkylark?

S: För att ändra den automatiska pappersstorleken för ett kalkylblad kan du använda egenskapen PageSetup.IsAutomaticPaperSize och ställa in det på önskat värde (sant eller falskt).

#### F: Vilka andra funktioner erbjuder Aspose.Cells för .NET?

S: Aspose.Cells för .NET erbjuder många funktioner för att arbeta med kalkylblad, som att skapa, ändra och konvertera arbetsböcker, samt manipulera data, formler och formatering.