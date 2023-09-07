---
title: Visa och dölj rullningslister av arbetsblad
linktitle: Visa och dölj rullningslister av arbetsblad
second_title: Aspose.Cells för .NET API-referens
description: Visa eller dölj rullningslister i Excel-kalkylblad med Aspose.Cells för .NET.
type: docs
weight: 50
url: /sv/net/excel-display-settings-csharp-tutorials/display-and-hide-scroll-bars-of-worksheet/
---
I den här handledningen kommer vi att visa dig hur du visar eller döljer vertikala och horisontella rullningslister i ett Excel-kalkylblad med C#-källkod med Aspose.Cells för .NET. Följ stegen nedan för att få önskat resultat.

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

## Steg 3: Dölj rullningslister

 Använd`IsVScrollBarVisible` och`IsHScrollBarVisible` egenskaper hos`Workbook.Settings` objekt för att dölja de vertikala och horisontella rullningslisterna i kalkylbladet.

```csharp
workbook.Settings.IsVScrollBarVisible = false;
workbook.Settings.IsHScrollBarVisible = false;
```

## Steg 4: Spara ändringar

 När du har gjort de nödvändiga ändringarna, spara den modifierade Excel-filen med hjälp av`Save` metod för`Workbook` objekt.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Exempel på källkod för att visa och dölja rullningslister i arbetsbladet med Aspose.Cells för .NET 

```csharp
// Sökvägen till dokumentkatalogen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Skapa en filström som innehåller Excel-filen som ska öppnas
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Instantiera ett arbetsboksobjekt
// Öppna Excel-filen genom filströmmen
Workbook workbook = new Workbook(fstream);
// Döljer den vertikala rullningslisten i Excel-filen
workbook.Settings.IsVScrollBarVisible = false;
// Döljer den horisontella rullningslisten i Excel-filen
workbook.Settings.IsHScrollBarVisible = false;
// Sparar den ändrade Excel-filen
workbook.Save(dataDir + "output.xls");
// Stänger filströmmen för att frigöra alla resurser
fstream.Close();
```

### Slutsats

Den här steg-för-steg-guiden visade hur du visar eller döljer vertikala och horisontella rullningslister i ett Excel-kalkylblad med Aspose.Cells för .NET. Med den medföljande C#-källkoden kan du enkelt anpassa visningen av rullningslister i dina Excel-filer.

### Vanliga frågor (FAQ)

#### Vad är Aspose.Cells för .NET?

Aspose.Cells för .NET är ett kraftfullt bibliotek för att manipulera Excel-filer i .NET-applikationer.

#### Hur kan jag installera Aspose.Cells för .NET?

 För att installera Aspose.Cells för .NET måste du ladda ner det relevanta paketet från[Aspose släpper](https://releases/aspose.com/cells/net/) och lägg till det i ditt .NET-projekt.

#### Hur kan jag visa eller dölja rullningslister i ett Excel-kalkylblad med Aspose.Cells för .NET?

 Du kan använda`IsVScrollBarVisible` och`IsHScrollBarVisible` egenskaper hos`Workbook.Settings` objekt för att visa eller dölja den vertikala respektive horisontella rullningslisten i ett Excel-kalkylblad.

#### Vilka andra Excel-filformat stöds av Aspose.Cells för .NET?

Aspose.Cells för .NET stöder en mängd olika Excel-filformat, som XLS, XLSX, CSV, HTML, PDF, etc.