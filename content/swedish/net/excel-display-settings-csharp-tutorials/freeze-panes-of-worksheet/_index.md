---
title: Frys rutor av arbetsblad
linktitle: Frys rutor av arbetsblad
second_title: Aspose.Cells för .NET API-referens
description: Hantera enkelt frysa rutor i Excel-kalkylblad med Aspose.Cells för .NET.
type: docs
weight: 70
url: /sv/net/excel-display-settings-csharp-tutorials/freeze-panes-of-worksheet/
---
I den här handledningen kommer vi att visa dig hur du låser rutor i ett Excel-kalkylblad med C#-källkod med Aspose.Cells för .NET. Följ stegen nedan för att få önskat resultat.

## Steg 1: Importera nödvändiga bibliotek

Se till att du har installerat Aspose.Cells-biblioteket för .NET och importera de nödvändiga biblioteken till ditt C#-projekt.

```csharp
using Aspose.Cells;
```

## Steg 2: Ställ in katalogsökväg och öppna Excel-fil

 Ställ in sökvägen till katalogen som innehåller din Excel-fil och öppna sedan filen genom att instansiera en`Workbook` objekt.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## Steg 3: Gå till kalkylbladet och använd fönsterlåsinställningar

 Navigera till det första kalkylbladet i Excel-filen med hjälp av`Worksheet` objekt. Använd sedan`FreezePanes` metod för att tillämpa fönsterlåsinställningarna.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. FreezePanes(3, 2, 3, 2);
```

I exemplet ovan är rutorna låsta till cellen i rad 3 och kolumn 2.

## Steg 4: Spara ändringar

 När du har gjort de nödvändiga ändringarna, spara den modifierade Excel-filen med hjälp av`Save` metod för`Workbook` objekt.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Exempel på källkod för Freeze Panes Of Worksheet med Aspose.Cells för .NET 

```csharp
//Sökvägen till dokumentkatalogen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Skapa en filström som innehåller Excel-filen som ska öppnas
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Instantiera ett arbetsboksobjekt
// Öppna Excel-filen genom filströmmen
Workbook workbook = new Workbook(fstream);
// Åtkomst till det första kalkylbladet i Excel-filen
Worksheet worksheet = workbook.Worksheets[0];
// Tillämpar inställningar för frysta rutor
worksheet.FreezePanes(3, 2, 3, 2);
// Sparar den ändrade Excel-filen
workbook.Save(dataDir + "output.xls");
// Stänger filströmmen för att frigöra alla resurser
fstream.Close();
```

## Slutsats

Denna steg-för-steg-guide visade dig hur du låser rutor i ett Excel-kalkylblad med Aspose.Cells för .NET. Med den medföljande C#-källkoden kan du enkelt anpassa fönsterlåsinställningarna för att bättre organisera och visualisera dina data i Excel-filer.

### Vanliga frågor (FAQ)

#### Vad är Aspose.Cells för .NET?

Aspose.Cells för .NET är ett kraftfullt bibliotek för att manipulera Excel-filer i .NET-applikationer.

#### Hur kan jag installera Aspose.Cells för .NET?

 För att installera Aspose.Cells för .NET måste du ladda ner det relevanta paketet från[Aspose släpper](https://releases/aspose.com/cells/net/) och lägg till det i ditt .NET-projekt.

#### Hur låser man rutor i ett Excel-kalkylblad med Aspose.Cells för .NET?

 Du kan använda`FreezePanes` metod för`Worksheet` objekt för att låsa rutorna i ett kalkylblad. Ange cellerna som ska låsas genom att tillhandahålla rad- och kolumnindex.

#### Kan jag anpassa fönsterlåsinställningarna med Aspose.Cells för .NET?

 Ja, med hjälp av`FreezePanes` metod kan du ange vilka celler som ska låsas efter behov, och tillhandahålla lämpliga rad- och kolumnindex.
