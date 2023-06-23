---
title: Visa Fliken Av Kalkylarket
linktitle: Visa Fliken Av Kalkylarket
second_title: Aspose.Cells för .NET API-referens
description: Visa en Excel-kalkylbladsflik med Aspose.Cells för .NET.
type: docs
weight: 60
url: /sv/net/excel-display-settings-csharp-tutorials/display-tab-of-spreadsheet/
---
I den här handledningen kommer vi att visa dig hur du visar fliken i ett Excel-kalkylblad med C#-källkod med Aspose.Cells för .NET. Följ stegen nedan för att få önskat resultat.

## Steg 1: Importera nödvändiga bibliotek

Se till att du har installerat Aspose.Cells-biblioteket för .NET och importera de nödvändiga biblioteken till ditt C#-projekt.

```csharp
using Aspose.Cells;
```

## Steg 2: Ställ in katalogsökväg och öppna Excel-fil

 Ställ in sökvägen till katalogen som innehåller din Excel-fil och öppna sedan filen genom att instansiera en`Workbook` objekt.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
Workbook workbook = new Workbook(dataDir + "book1.xls");
```

## Steg 3: Visa kalkylbladsfliken

 Använd`ShowTabs` egendom av`Workbook.Settings` objekt för att visa Excel-kalkylbladsfliken.

```csharp
workbook.Settings.ShowTabs = true;
```

## Steg 4: Spara ändringar

 När du har gjort de nödvändiga ändringarna, spara den modifierade Excel-filen med hjälp av`Save` metod för`Workbook` objekt.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Exempel på källkod för Visa Tab Of Spreadsheet med Aspose.Cells för .NET 

```csharp
// Sökvägen till dokumentkatalogen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instantiera ett arbetsboksobjekt
// Öppnar Excel-filen
Workbook workbook = new Workbook(dataDir + "book1.xls");
// Döljer flikarna i Excel-filen
workbook.Settings.ShowTabs = true;
// Sparar den ändrade Excel-filen
workbook.Save(dataDir + "output.xls");
```

### Slutsats

Den här steg-för-steg-guiden visade hur du visar fliken i ett Excel-kalkylblad med Aspose.Cells för .NET. Med den medföljande C#-källkoden kan du enkelt anpassa visningen av flikar i dina Excel-filer.

### Vanliga frågor (FAQ)

#### Vad är Aspose.Cells för .NET?

Aspose.Cells för .NET är ett kraftfullt bibliotek för att manipulera Excel-filer i .NET-applikationer.

#### Hur kan jag installera Aspose.Cells för .NET?

 För att installera Aspose.Cells för .NET måste du ladda ner det relevanta paketet från[Aspose släpper](https://releases/aspose.com/cells/net/) och lägg till det i ditt .NET-projekt.

#### Hur visar man fliken i ett Excel-kalkylblad med Aspose.Cells för .NET?

 Du kan använda`ShowTabs` egendom av`Workbook.Settings` objekt och ställ in det på`true` för att visa kalkylbladsfliken.

#### Vilka andra Excel-filformat stöds av Aspose.Cells för .NET?

Aspose.Cells för .NET stöder en mängd olika Excel-filformat, som XLS, XLSX, CSV, HTML, PDF, etc.
