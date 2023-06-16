---
title: Kopiera inställningar för sidinställningar från annat kalkylblad
linktitle: Kopiera inställningar för sidinställningar från annat kalkylblad
second_title: Aspose.Cells för .NET API-referens
description: Lär dig hur du kopierar sidkonfigurationsinställningar från ett kalkylblad till ett annat med Aspose.Cells för .NET. En steg-för-steg-guide för att optimera användningen av detta bibliotek.
type: docs
weight: 10
url: /sv/net/excel-page-setup/copy-page-setup-settings-from-other-worksheet/
---
den här artikeln tar vi dig steg för steg för att förklara följande C#-källkod: Kopiera sidkonfigurationsinställningar från ett annat kalkylblad med Aspose.Cells för .NET. Vi kommer att använda Aspose.Cells-biblioteket för .NET för att utföra denna operation. Om du vill kopiera sidinställningar från ett kalkylblad till ett annat följer du stegen nedan.

## Steg 1: Skapa arbetsboken
Det första steget är att skapa en arbetsbok. I vårt fall kommer vi att använda Workbook-klassen som tillhandahålls av Aspose.Cells-biblioteket. Här är koden för att skapa en arbetsbok:

```csharp
Workbook wb = new Workbook();
```

## Steg 2: Lägga till testarbetsblad
Efter att ha skapat arbetsboken måste vi lägga till testkalkylblad. I det här exemplet kommer vi att lägga till två kalkylblad. Här är koden för att lägga till två kalkylblad:

```csharp
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
```

## Steg 3: Få åtkomst till arbetsblad
Nu när vi har lagt till kalkylbladen måste vi komma åt dem för att kunna ändra deras inställningar. Vi kommer åt kalkylbladen "TestSheet1" och "TestSheet2" med deras namn. Här är koden för att komma åt den:

```csharp
Worksheet TestSheet1 = wb. Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb. Worksheets["TestSheet2"];
```

## Steg 4: Ställa in pappersstorlek
 I det här steget kommer vi att ställa in pappersstorleken för kalkylbladet "TestSheet1". Vi kommer att använda`PageSetup.PaperSize` egenskap för att ställa in pappersstorleken. Till exempel kommer vi att ställa in pappersstorleken till "PaperA3ExtraTransverse". Här är koden för det:

```csharp
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
```

## Steg 5: Kopiera inställningar för sidinställningar
 Nu kommer vi att kopiera sidkonfigurationsinställningarna från kalkylbladet "TestSheet1" till "TestSheet2". Vi kommer att använda`PageSetup.Copy` metod för att utföra denna operation. Här är koden för det:

```csharp
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
```

## Steg 6: Skriva ut pappersstorlekar
 Efter att ha kopierat sidinställningarna kommer vi att skriva ut pappersstorlekarna för de två arbetsbladen. Vi kommer använda`Console.WriteLine` för att visa pappersstorlekarna. Här är koden för det:

```csharp
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
```

### Exempel på källkod för Kopiera sidinställningar från annat kalkylblad med Aspose.Cells för .NET 
```csharp
//Skapa arbetsbok
Workbook wb = new Workbook();
//Lägg till två testark
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
//Få åtkomst till båda kalkylbladen som TestSheet1 och TestSheet2
Worksheet TestSheet1 = wb.Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb.Worksheets["TestSheet2"];
//Ställ in pappersstorleken för testark1 till PaperA3ExtraTransverse
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
//Skriv ut pappersstorleken för båda kalkylbladen
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
//Kopiera PageSetup från TestSheet1 till TestSheet2
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
//Skriv ut pappersstorleken för båda kalkylbladen
Console.WriteLine("After Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("After Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
Console.WriteLine("CopyPageSetupSettingsFromSourceWorksheetToDestinationWorksheet executed successfully.\r\n");
```

## Slutsats
I den här artikeln lärde vi oss hur man kopierar sidkonfigurationsinställningar från ett kalkylblad till ett annat med Aspose.Cells för .NET. Vi gick igenom följande steg: skapa arbetsboken, lägga till testark, komma åt arbetsbladen, ställa in pappersstorleken, kopiera sidinställningarna och skriva ut pappersstorlekar. Nu kan du använda denna kunskap för att kopiera sidkonfigurationsinställningar till dina egna projekt.

### Vanliga frågor

F: Kan jag kopiera sidkonfigurationsinställningar mellan olika arbetsboksinstanser?

 S: Ja, du kan kopiera sidinställningar mellan olika arbetsboksinstanser med hjälp av`PageSetup.Copy` metod för Aspose.Cells-biblioteket.

F: Kan jag kopiera andra sidinställningar, som orientering eller marginaler?

 S: Ja, du kan kopiera andra sidinställningar med hjälp av`PageSetup.Copy` metod med lämpliga alternativ. Du kan till exempel kopiera orientering med`CopyOptions.Orientation` och marginaler med hjälp av`CopyOptions.Margins`.

F: Hur vet jag vilka alternativ som finns tillgängliga för pappersstorlek?

 S: Du kan kontrollera Aspose.Cells biblioteks API-referens för tillgängliga alternativ för pappersstorlek. Det finns en uppräkning som heter`PaperSizeType` som listar de olika pappersstorlekarna som stöds.

F: Hur kan jag ladda ner Aspose.Cells-biblioteket för .NET?

 S: Du kan ladda ner Aspose.Cells-biblioteket för .NET från[Aspose släpper](https://releases.aspose.com/cells/net). Det finns gratis testversioner tillgängliga, såväl som betalda licenser för kommersiellt bruk.

F: Stöder Aspose.Cells-biblioteket andra programmeringsspråk?

S: Ja, Aspose.Cells-biblioteket stöder flera programmeringsspråk inklusive C#, Java, Python och många fler.