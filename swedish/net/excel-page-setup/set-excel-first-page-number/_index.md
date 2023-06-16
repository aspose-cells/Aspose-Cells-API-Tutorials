---
title: Ställ in Excel första sidnummer
linktitle: Ställ in Excel första sidnummer
second_title: Aspose.Cells för .NET API-referens
description: Lär dig hur du ställer in det första sidnumret i Excel med Aspose.Cells för .NET.
type: docs
weight: 90
url: /sv/net/excel-page-setup/set-excel-first-page-number/
---
I den här handledningen går vi igenom hur du ställer in det första sidnumret i Excel med Aspose.Cells för .NET. Vi kommer att använda C#-källkod för att illustrera processen.

## Steg 1: Sätta upp miljön

Se till att du har Aspose.Cells för .NET installerat på din maskin. Skapa också ett nytt projekt i din föredragna utvecklingsmiljö.

## Steg 2: Importera nödvändiga bibliotek

Importera de bibliotek som behövs för att arbeta med Aspose.Cells i din kodfil. Här är motsvarande kod:

```csharp
using Aspose.Cells;
```

## Steg 3: Ställ in datakatalog

Ställ in datakatalogen där du vill spara den modifierade Excel-filen. Använd följande kod:

```csharp
string dataDir = "YOUR DATA DIRECTORY";
```

Var noga med att ange hela katalogsökvägen.

## Steg 4: Skapa arbetsboken och arbetsbladet

Skapa ett nytt arbetsboksobjekt och navigera till det första kalkylbladet i arbetsboken med följande kod:

```csharp
Workbook workbook = new Workbook();
Worksheet worksheet = workbook.Worksheets[0];
```

Detta kommer att skapa en tom arbetsbok med ett kalkylblad.

## Steg 5: Ställ in numret på den första sidan

Ställ in numret på den första sidan av kalkylbladssidorna med följande kod:

```csharp
worksheet.PageSetup.FirstPageNumber = 2;
```

Detta kommer att ställa in första sidnumret till 2.

## Steg 6: Spara den modifierade arbetsboken

Spara den ändrade arbetsboken med följande kod:

```csharp
workbook.Save(dataDir + "OutputFileName.xls");
```

Detta kommer att spara den modifierade arbetsboken i den angivna datakatalogen.

### Exempel på källkod för Set Excel First Page Number med Aspose.Cells för .NET 
```csharp
// Sökvägen till dokumentkatalogen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instantiera ett arbetsboksobjekt
Workbook workbook = new Workbook();
// Åtkomst till det första kalkylbladet i Excel-filen
Worksheet worksheet = workbook.Worksheets[0];
// Ställa in det första sidnumret på kalkylbladssidorna
worksheet.PageSetup.FirstPageNumber = 2;
// Spara arbetsboken.
workbook.Save(dataDir + "SetFirstPageNumber_out.xls");
```

## Slutsats

Du har nu lärt dig hur du ställer in första sidnumret i Excel med Aspose.Cells för .NET. Denna handledning ledde dig genom varje steg i processen, från att ställa in miljön till att ställa in det första sidnumret. Du kan nu använda denna kunskap för att anpassa sidnumreringen i dina Excel-filer.

### FAQ's

#### F1: Kan jag ställa in olika första sidnummer för varje kalkylblad?

 S1: Ja, du kan ställa in olika första sidnummer för varje kalkylblad genom att gå till`FirstPageNumber`respektive arbetsblads egendom`PageSetup` objekt.

#### F2: Hur kan jag kontrollera första sidnumret i ett befintligt kalkylblad?

 S2: Du kan kontrollera första sidnumret i ett befintligt kalkylblad genom att gå till`FirstPageNumber` egendom av`PageSetup` objekt som motsvarar det arbetsbladet.

#### F3: Börjar sidnumreringen alltid från 1 som standard?

S3: Ja, sidnumreringen börjar från 1 som standard i Excel. Du kan dock använda koden som visas i denna handledning för att ställa in ett annat första sidnummer.

#### F4: Är ändringar av första sidnumret permanenta i den redigerade Excel-filen?

S4: Ja, ändringarna som gjorts av första sidnumret sparas permanent i den modifierade Excel-filen.

#### F5: Fungerar den här metoden för alla Excel-filformat, som .xls och .xlsx?

S5: Ja, den här metoden fungerar för alla Excel-filformat som stöds av Aspose.Cells, inklusive .xls och .xlsx.