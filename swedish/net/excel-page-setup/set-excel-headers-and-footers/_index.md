---
title: Ställ in sidhuvuden och sidfötter i Excel
linktitle: Ställ in sidhuvuden och sidfötter i Excel
second_title: Aspose.Cells för .NET API-referens
description: Lär dig hur du ställer in sidhuvuden och sidfötter i Excel med Aspose.Cells för .NET.
type: docs
weight: 100
url: /sv/net/excel-page-setup/set-excel-headers-and-footers/
---

den här handledningen kommer vi att visa dig steg för steg hur du ställer in sidhuvuden och sidfötter i Excel med Aspose.Cells för .NET. Vi kommer att använda C#-källkod för att illustrera processen.

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
Workbook excel = new Workbook();
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
```

Detta skapar en tom arbetsbok med ett kalkylblad och ger åtkomst till det kalkylbladets PageSetup-objekt.

## Steg 5: Ställ in rubriker

 Ställ in kalkylbladets rubriker med hjälp av`SetHeader` metoder för PageSetup-objektet. Här är en exempelkod:

```csharp
pageSetup.SetHeader(0, "&A");
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
```

Detta kommer att ställa in kalkylbladets namn, aktuellt datum och tid samt filnamnet i respektive rubrik.

## Steg 6: Definiera sidfötter

 Ställ in sidfötter för kalkylblad med hjälp av`SetFooter` metoder för PageSetup-objektet. Här är en exempelkod:

```csharp
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
pageSetup.SetFooter(1, "&P");
pageSetup.SetFooter(2, "&N");
```

Detta kommer att ställa in en textsträng, det aktuella sidnumret respektive det totala antalet sidor i sidfötterna.

## Steg 7: Spara den modifierade arbetsboken

Spara den ändrade arbetsboken med följande kod:

```csharp
excel.Save(dataDir + "OutputFileName.xls");
```

Detta kommer att spara den modifierade arbetsboken i den angivna datakatalogen.

### Exempel på källkod för Ställ in sidhuvuden och sidfötter i Excel med Aspose.Cells för .NET 
```csharp
// Sökvägen till dokumentkatalogen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instantiera ett arbetsboksobjekt
Workbook excel = new Workbook();
// Få referensen till kalkylbladets PageSetup
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
// Ställer in kalkylbladsnamn till vänster i rubriken
pageSetup.SetHeader(0, "&A");
//Ställa in aktuellt datum och aktuell tid i mitten av rubriken
// och ändra teckensnittet för rubriken
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
// Ställa in aktuellt filnamn i den högra delen av rubriken och ändra
// teckensnitt för rubriken
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
// Ställa in en sträng i den vänstra delen av sidfoten och ändra teckensnitt
// av en del av denna sträng ("123")
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
// Ställa in aktuellt sidnummer i mitten av sidfoten
pageSetup.SetFooter(1, "&P");
// Ställ in sidantal i den högra delen av sidfoten
pageSetup.SetFooter(2, "&N");
// Spara arbetsboken.
excel.Save(dataDir + "SetHeadersAndFooters_out.xls");
```


## Slutsats

Du har nu lärt dig hur du ställer in sidhuvuden och sidfötter i Excel med Aspose.Cells för .NET. Denna handledning ledde dig genom varje steg i processen, från att ställa in miljön till att spara den modifierade arbetsboken. Utforska gärna funktionerna i Aspose.Cells ytterligare för att utföra ytterligare manipulationer i dina Excel-filer.

### Vanliga frågor (FAQ)

#### 1. Hur kan jag installera Aspose.Cells för .NET på mitt system?
För att installera Aspose.Cells för .NET måste du ladda ner installationspaketet från Asposes officiella webbplats och följa instruktionerna i dokumentationen.

#### 2. Fungerar den här metoden med alla versioner av Excel?
Ja, metoden att ställa in sidhuvuden och sidfötter med Aspose.Cells för .NET fungerar med alla versioner av Excel som stöds.

#### 3. Kan jag anpassa sidhuvuden och sidfötter ytterligare?
Ja, Aspose.Cells erbjuder ett omfattande utbud av funktioner för att anpassa sidhuvuden och sidfötter, inklusive textplacering, färg, teckensnitt, sidnummer och mer.

#### 4. Hur kan jag lägga till dynamisk information i sidhuvuden och sidfötter?
Du kan använda speciella variabler och formateringskoder för att lägga till dynamisk information som aktuellt datum, tid, filnamn, sidnummer, etc., till sidhuvuden och sidfötter.

#### 5. Kan jag ta bort sidhuvuden och sidfötter efter att ha ställt in dem?
 Ja, du kan ta bort sidhuvuden och sidfötter med hjälp av`ClearHeaderFooter` metod för`PageSetup` objekt. Detta kommer att återställa standardhuvuden och sidfötter.