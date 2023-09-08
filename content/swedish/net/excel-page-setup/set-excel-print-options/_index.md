---
title: Ställ in Excel utskriftsalternativ
linktitle: Ställ in Excel utskriftsalternativ
second_title: Aspose.Cells för .NET API-referens
description: Lär dig att manipulera Excel-filer och anpassa utskriftsalternativ med lätthet med Aspose.Cells för .NET.
type: docs
weight: 150
url: /sv/net/excel-page-setup/set-excel-print-options/
---
I den här guiden går vi igenom hur du ställer in utskriftsalternativ för en Excel-arbetsbok med Aspose.Cells för .NET. Vi tar dig steg-för-steg genom den medföljande C#-källkoden för att utföra denna uppgift.

## Steg 1: Sätta upp miljön

Innan du börjar, se till att du har konfigurerat din utvecklingsmiljö och installerat Aspose.Cells för .NET. Du kan ladda ner den senaste versionen av biblioteket från Asposes officiella webbplats.

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

## Steg 5: Skaffa kalkylbladets PageSetup-referens

För att ställa in utskriftsalternativen måste vi först hämta PageSetup-referensen från kalkylbladet. Använd följande kod för att få referensen:

```csharp
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## Steg 6: Aktivera utskrift av rutnätslinjer

För att göra det möjligt att skriva ut rutnätslinjer, använd följande kod:

```csharp
pageSetup. PrintGridlines = true;
```

## Steg 7: Aktivera utskrift av rad-/kolumnhuvud

För att aktivera utskrift av rad- och kolumnrubriker, använd följande kod:

```csharp
pageSetup.PrintHeadings = true;
```

## Steg 8: Aktivera svartvitt utskriftsläge

För att aktivera utskrift av kalkylbladet i svartvitt läge, använd följande kod:

```csharp
pageSetup.BlackAndWhite = true;
```

## Steg 9: Aktivera feedbackutskrift

Använd följande kod för att tillåta att kommentarer skrivs ut som de visas i kalkylarket:

```csharp
pageSetup.PrintComments = PrintCommentsType.PrintInPlace;
```

## Steg 10: Aktivera utskrift av utkastläge

För att aktivera utskrift av kalkylarket i utkastläge, använd följande kod:

```csharp
pageSetup.PrintDraft = true;
```

## Steg 11: Aktivera utskriftscellfel som N/A

För att tillåta cellfel att skrivas ut som

  än N/A, använd följande kod:

```csharp
pageSetup.PrintErrors = PrintErrorsType.PrintErrorsNA;
```

## Steg 12: Spara Excel-arbetsboken

 För att spara Excel-arbetsboken med utskriftsalternativen, använd`Save` metod för arbetsboksobjektet:

```csharp
workbook.Save(dataDir + "OtherPrintOptions_out.xls");
```

Detta kommer att spara Excel-arbetsboken med filnamnet "OtherPrintOptions_out.xls" i den angivna katalogen.

### Exempel på källkod för Ställ in Excel-utskriftsalternativ med Aspose.Cells för .NET 
```csharp
//Sökvägen till dokumentkatalogen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instantiera ett arbetsboksobjekt
Workbook workbook = new Workbook();
// Få referensen till kalkylbladets PageSetup
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Tillåter att skriva ut rutnät
pageSetup.PrintGridlines = true;
// Tillåter att skriva ut rad-/kolumnrubriker
pageSetup.PrintHeadings = true;
// Tillåter att skriva ut kalkylblad i svartvitt läge
pageSetup.BlackAndWhite = true;
// Tillåter att skriva ut kommentarer som visas på kalkylbladet
pageSetup.PrintComments = PrintCommentsType.PrintInPlace;
// Tillåter att skriva ut kalkylblad med utkastkvalitet
pageSetup.PrintDraft = true;
// Tillåter att skriva ut cellfel som N/A
pageSetup.PrintErrors = PrintErrorsType.PrintErrorsNA;
// Spara arbetsboken.
workbook.Save(dataDir + "OtherPrintOptions_out.xls");
```
## Slutsats

Du har nu lärt dig hur du ställer in utskriftsalternativ för en Excel-arbetsbok med Aspose.Cells för .NET. Detta kraftfulla och användarvänliga bibliotek låter dig anpassa utskriftsinställningarna för dina Excel-arbetsböcker på ett enkelt och effektivt sätt.

### Vanliga frågor


#### 1. Kan jag anpassa utskriftsalternativ ytterligare, såsom marginaler eller sidriktning?

Ja, Aspose.Cells för .NET erbjuder ett brett utbud av anpassningsbara utskriftsalternativ, såsom marginaler, sidorientering, skala, etc.

#### 2. Stöder Aspose.Cells for .NET andra Excel-filformat?

Ja, Aspose.Cells för .NET stöder en mängd olika Excel-filformat, som XLSX, XLS, CSV, HTML, PDF, etc.

#### 3. Är Aspose.Cells för .NET kompatibelt med alla versioner av .NET Framework?

Aspose.Cells för .NET är kompatibel med .NET Framework 2.0 eller senare, inklusive versionerna 3.5, 4.0, 4.5, 4.6, etc.