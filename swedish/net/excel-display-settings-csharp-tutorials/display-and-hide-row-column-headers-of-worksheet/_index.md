---
title: Visa och dölj radkolumnrubriker av arbetsblad
linktitle: Visa och dölj radkolumnrubriker av arbetsblad
second_title: Aspose.Cells för .NET API-referens
description: Visa eller dölj rad- och kolumnrubriker i Excel-kalkylblad med Aspose.Cells för .NET.
type: docs
weight: 40
url: /sv/net/excel-display-settings-csharp-tutorials/display-and-hide-row-column-headers-of-worksheet/
---
I den här handledningen kommer vi att visa dig hur du visar eller döljer rad- och kolumnrubriker i ett Excel-kalkylblad med C#-källkod med Aspose.Cells för .NET. Följ stegen nedan för att få önskat resultat.

## Steg 1: Importera nödvändiga bibliotek

Se till att du har installerat Aspose.Cells-biblioteket för .NET och importera de nödvändiga biblioteken till ditt C#-projekt.

```csharp
using Aspose.Cells;
using System.IO;
```

## Steg 2: Ställ in katalogsökväg och öppna Excel-fil

 Ställ in sökvägen till katalogen som innehåller din Excel-fil och öppna sedan filen genom att skapa en filström och instansiera en`Workbook` objekt.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## Steg 3: Gå till det första kalkylbladet och dölj rad- och kolumnrubriker

 Öppna det första kalkylbladet i Excel-filen med hjälp av`Worksheets` egendom av`Workbook` objekt. Använd sedan`IsRowColumnHeadersVisible` egendom av`Worksheet` objekt för att dölja rad- och kolumnrubriker.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. IsRowColumnHeadersVisible = false;
```

## Steg 4: Spara ändringar

 När du har gjort de nödvändiga ändringarna, spara den modifierade Excel-filen med hjälp av`Save` metod för`Workbook` objekt.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Exempel på källkod för att visa och dölja radkolumnrubriker i arbetsblad med Aspose.Cells för .NET 
```csharp
// Sökvägen till dokumentkatalogen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Skapa en filström som innehåller Excel-filen som ska öppnas
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Instantiera ett arbetsboksobjekt
// Öppna Excel-filen genom filströmmen
Workbook workbook = new Workbook(fstream);
// Åtkomst till det första kalkylbladet i Excel-filen
Worksheet worksheet = workbook.Worksheets[0];
// Döljer rubrikerna för rader och kolumner
worksheet.IsRowColumnHeadersVisible = false;
// Sparar den ändrade Excel-filen
workbook.Save(dataDir + "output.xls");
// Stänger filströmmen för att frigöra alla resurser
fstream.Close(); 
```

## Slutsats

Den här steg-för-steg-guiden visade hur du visar eller döljer rad- och kolumnrubriker i ett Excel-kalkylblad med Aspose.Cells för .NET. Med den medföljande C#-källkoden kan du enkelt anpassa visningen av rubriker i dina Excel-filer.

### Vanliga frågor (FAQ)

#### Vad är Aspose.Cells för .NET?

Aspose.Cells för .NET är ett kraftfullt bibliotek för att manipulera Excel-filer i .NET-applikationer.

#### Hur kan jag installera Aspose.Cells för .NET?

 För att installera Aspose.Cells för .NET måste du ladda ner det relevanta paketet från[Aspose släpper](https://releases/aspose.com/cells/net/) och lägg till det i ditt .NET-projekt.

#### Hur kan jag visa eller dölja rad- och kolumnrubriker i ett Excel-kalkylblad med Aspose.Cells för .NET?

 Du kan använda`IsRowColumnHeadersVisible` egendom av`Worksheet` objekt för att visa eller dölja rad- och kolumnrubriker. Ställ in den på`true` att visa dem och till`false` att dölja dem.

#### Vilka andra Excel-filformat stöds av Aspose.Cells för .NET?

Aspose.Cells för .NET stöder olika Excel-filformat, såsom XLS, XLSX, CSV, HTML, PDF och många fler.
