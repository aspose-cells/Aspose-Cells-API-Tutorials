---
title: Delade rutor av arbetsblad
linktitle: Delade rutor av arbetsblad
second_title: Aspose.Cells för .NET API-referens
description: Steg-för-steg-guide för att dela rutor i ett Excel-kalkylblad med Aspose.Cells för .NET.
type: docs
weight: 130
url: /sv/net/excel-display-settings-csharp-tutorials/split-panes-of-worksheet/
---
I den här handledningen kommer vi att förklara hur man delar upp rutor i ett Excel-kalkylblad med Aspose.Cells för .NET. Följ dessa steg för att få önskat resultat:

## Steg 1: Sätta upp miljön

Se till att du har installerat Aspose.Cells för .NET och ställt in din utvecklingsmiljö. Se också till att du har en kopia av Excel-filen du vill dela rutor på.

## Steg 2: Importera nödvändiga beroenden

Lägg till de nödvändiga direktiven för att använda klasserna från Aspose.Cells:

```csharp
using Aspose.Cells;
```

## Steg 3: Kodinitiering

Börja med att initiera sökvägen till katalogen som innehåller dina Excel-dokument:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## Steg 4: Öppna Excel-filen

 Instantiera en ny`Workbook` objekt och öppna Excel-filen med hjälp av`Open` metod:

```csharp
Workbook book = new Workbook(dataDir + "Book1.xls");
```

## Steg 5: Definiera den aktiva cellen

 Ställ in den aktiva cellen i kalkylbladet med hjälp av`ActiveCell` fast egendom:

```csharp
book.Worksheets[0].ActiveCell = "A20";
```

## Steg 6: Uppdelning av flikarna

 Dela upp kalkylbladet med hjälp av`Split` metod:

```csharp
book.Worksheets[0].Split();
```

## Steg 7: Spara ändringar

Spara ändringarna som gjorts i Excel-filen:

```csharp
book.Save(dataDir + "output.xls");
```

### Exempel på källkod för delade paneler av arbetsblad med Aspose.Cells för .NET 

```csharp
//Sökvägen till dokumentkatalogen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instantiera en ny arbetsbok och öppna en mallfil
Workbook book = new Workbook(dataDir + "Book1.xls");
// Ställ in den aktiva cellen
book.Worksheets[0].ActiveCell = "A20";
// Dela upp kalkylbladets fönster
book.Worksheets[0].Split();
// Spara excel-filen
book.Save(dataDir + "output.xls");
```

## Slutsats

den här handledningen lärde du dig hur du delar upp rutor i ett Excel-kalkylblad med Aspose.Cells för .NET. Genom att följa de beskrivna stegen kan du enkelt anpassa utseendet och beteendet för dina Excel-filer.

### Vanliga frågor (FAQ)

#### Vad är Aspose.Cells för .NET?

Aspose.Cells för .NET är ett populärt programbibliotek för att manipulera Excel-filer i .NET-applikationer.

#### Hur kan jag ställa in den aktiva cellen i ett kalkylblad i Aspose.Cells?

 Du kan ställa in den aktiva cellen med hjälp av`ActiveCell`egenskapen för kalkylbladsobjektet.

#### Kan jag bara dela de horisontella eller vertikala rutorna i kalkylbladsfönstret?

 Ja, med Aspose.Cells kan du bara dela horisontella eller vertikala rutor med lämpliga metoder som t.ex`SplitColumn` eller`SplitRow`.

#### Fungerar Aspose.Cells bara med Excel-filer i .xls-format?

Nej, Aspose.Cells stöder olika Excel-filformat inklusive .xls och .xlsx.