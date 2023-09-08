---
title: Ställ in Excel-utskriftstitel
linktitle: Ställ in Excel-utskriftstitel
second_title: Aspose.Cells för .NET API-referens
description: Lär dig att enkelt manipulera Excel-filer och anpassa utskriftsalternativ med Aspose.Cells för .NET.
type: docs
weight: 170
url: /sv/net/excel-page-setup/set-excel-print-title/
---
I den här guiden går vi igenom hur du ställer in utskriftstitlar i ett Excel-kalkylblad med Aspose.Cells för .NET. Följ stegen nedan för att utföra denna uppgift.

## Steg 1: Sätta upp miljön

Se till att du har ställt in din utvecklingsmiljö och installerat Aspose.Cells för .NET. Du kan ladda ner den senaste versionen av biblioteket från Asposes officiella webbplats.

## Steg 2: Importera nödvändiga namnrymder

I ditt C#-projekt, importera de nödvändiga namnrymden för att arbeta med Aspose.Cells:

```csharp
using Aspose.Cells;
```

## Steg 3: Ställ in sökvägen till dokumentkatalogen

 Deklarera a`dataDir` variabel för att ange sökvägen till katalogen där du vill spara den genererade Excel-filen:

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Se till att byta ut`"YOUR_DOCUMENT_DIRECTORY"` med rätt sökväg på ditt system.

## Steg 4: Skapa ett arbetsboksobjekt

Instantiera ett arbetsboksobjekt som representerar den Excel-arbetsbok du vill skapa:

```csharp
Workbook workbook = new Workbook();
```

## Steg 5: Tillgång till det första kalkylbladet

Navigera till det första kalkylbladet i Excel-arbetsboken med följande kod:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Steg 6: Definiera rubrikkolumner

Definiera rubrikkolumnerna med följande kod:

```csharp
pageSetup.PrintTitleColumns = "$A:$B";
```

Här har vi definierat kolumnerna A och B som rubrikkolumner. Du kan justera detta värde efter dina behov.

## Steg 7: Definiera titelrader

Definiera rubrikraderna med följande kod:

```csharp
pageSetup.PrintTitleRows = "$1:$2";
```

Vi har definierat rad 1 och 2 som titelrader. Du kan justera dessa värden efter dina behov.

## Steg 8: Spara Excel-arbetsboken

 För att spara Excel-arbetsboken med de definierade utskriftstitlarna, använd`Save` metod för arbetsboksobjektet:

```csharp
workbook.Save(dataDir + "SetPrintTitle_out.xls");
```

Detta kommer att spara Excel-arbetsboken med filnamnet "SetPrintTitle_out.xls" i den angivna katalogen.

### Exempel på källkod för Set Excel Print Title med Aspose.Cells för .NET 
```csharp
//Sökvägen till dokumentkatalogen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instantiera ett arbetsboksobjekt
Workbook workbook = new Workbook();
// Få referensen till kalkylbladets PageSetup
Aspose.Cells.PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Definiera kolumnnummer A & B som rubrikkolumner
pageSetup.PrintTitleColumns = "$A:$B";
// Definiera radnummer 1 och 2 som titelrader
pageSetup.PrintTitleRows = "$1:$2";
// Spara arbetsboken.
workbook.Save(dataDir + "SetPrintTitle_out.xls");
```

## Slutsats

Grattis! Du har lärt dig hur du ställer in utskriftstitlar i ett Excel-kalkylblad med Aspose.Cells för .NET. Utskriftstitlar låter dig visa specifika rader och kolumner på varje utskriven sida, vilket gör data lättare att läsa och referera.

### Vanliga frågor

#### 1. Kan jag ställa in utskriftsrubriker för specifika kolumner i Excel?

 Ja, med Aspose.Cells för .NET kan du ställa in specifika kolumner som utskriftstitlar med hjälp av`PrintTitleColumns` egendom av`PageSetup` objekt.

#### 2. Är det möjligt att definiera både kolumn- och utskriftsradtitlar?

 Ja, du kan ställa in både utskriftskolumn- och radtitlar med hjälp av`PrintTitleColumns` och`PrintTitleRows` egenskaper hos`PageSetup` objekt.

#### 3. Vilka andra layoutinställningar kan jag anpassa med Aspose.Cells för .NET?

Med Aspose.Cells för .NET kan du anpassa olika sidlayoutinställningar, såsom marginaler, sidorientering, utskriftsskala och mer.