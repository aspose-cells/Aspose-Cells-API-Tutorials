---
title: Ta bort paneler i arbetsbladet
linktitle: Ta bort paneler i arbetsbladet
second_title: Aspose.Cells för .NET API-referens
description: Steg för steg guide för att ta bort rutor från ett Excel-kalkylblad med Aspose.Cells för .NET.
type: docs
weight: 120
url: /sv/net/excel-display-settings-csharp-tutorials/remove-panes-of-worksheet/
---
I den här handledningen kommer vi att förklara hur man tar bort rutor från ett Excel-kalkylblad med Aspose.Cells för .NET. Följ dessa steg för att få önskat resultat:

## Steg 1: Sätta upp miljön

Se till att du har installerat Aspose.Cells för .NET och ställt in din utvecklingsmiljö. Se också till att du har en kopia av Excel-filen du vill ta bort rutorna från.

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

## Steg 6: Ta bort rutorna

 Ta bort rutor från kalkylbladsfönstret med hjälp av`RemoveSplit` metod:

```csharp
book.Worksheets[0].RemoveSplit();
```

## Steg 7: Spara ändringar

Spara ändringarna som gjorts i Excel-filen:

```csharp
book.Save(dataDir + "output.xls");
```

### Exempel på källkod för Ta bort paneler i arbetsbladet med Aspose.Cells för .NET 
```csharp
// Sökvägen till dokumentkatalogen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instantiera en ny arbetsbok och öppna en mallfil
Workbook book = new Workbook(dataDir + "Book1.xls");
// Ställ in den aktiva cellen
book.Worksheets[0].ActiveCell = "A20";
// Dela upp kalkylbladets fönster
book.Worksheets[0].RemoveSplit();
// Spara excel-filen
book.Save(dataDir + "output.xls");
```

## Slutsats

I den här handledningen lärde du dig hur du tar bort rutor från ett Excel-kalkylblad med Aspose.Cells för .NET. Genom att följa de beskrivna stegen kan du enkelt anpassa utseendet och beteendet för dina Excel-filer.

### Vanliga frågor (FAQ)

#### Vad är Aspose.Cells för .NET?

Aspose.Cells för .NET är ett populärt programbibliotek för att manipulera Excel-filer i .NET-applikationer.

#### Hur kan jag ställa in den aktiva cellen i ett kalkylblad i Aspose.Cells?

 Du kan ställa in den aktiva cellen med hjälp av`ActiveCell`egenskapen för kalkylbladsobjektet.

#### Kan jag ta bort endast horisontella eller vertikala rutor från kalkylbladsfönstret?

 Ja, med Aspose.Cells kan du bara ta bort horisontella eller vertikala rutor med lämpliga metoder som t.ex`RemoveHorizontalSplit` eller`RemoveVerticalSplit`.

#### Fungerar Aspose.Cells bara med Excel-filer i .xls-format?

Nej, Aspose.Cells stöder olika Excel-filformat inklusive .xls och .xlsx.
	