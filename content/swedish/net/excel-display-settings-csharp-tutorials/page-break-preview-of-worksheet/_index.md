---
title: Förhandsvisning av sidbrytning av arbetsblad
linktitle: Förhandsvisning av sidbrytning av arbetsblad
second_title: Aspose.Cells för .NET API-referens
description: Steg för steg guide för att visa sidbrytningsförhandsvisning av kalkylblad med Aspose.Cells för .NET.
type: docs
weight: 110
url: /sv/net/excel-display-settings-csharp-tutorials/page-break-preview-of-worksheet/
---
I den här handledningen kommer vi att förklara hur man visar sidbrytningsförhandsvisningen av ett kalkylblad med Aspose.Cells för .NET. Följ dessa steg för att få önskat resultat:

## Steg 1: Sätta upp miljön

Se till att du har installerat Aspose.Cells för .NET och ställt in din utvecklingsmiljö. Se också till att du har en kopia av Excel-filen som du vill visa förhandsvisningen av sidbrytningen på.

## Steg 2: Importera nödvändiga beroenden

Lägg till de nödvändiga direktiven för att använda klasserna från Aspose.Cells:

```csharp
using Aspose.Cells;
using System.IO;
```

## Steg 3: Kodinitiering

Börja med att initiera sökvägen till katalogen som innehåller dina Excel-dokument:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## Steg 4: Öppna Excel-filen

 Skapa en`FileStream` objekt som innehåller Excel-filen som ska öppnas:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 Instantiera en`Workbook` objekt och öppna Excel-filen med filströmmen:

```csharp
Workbook workbook = new Workbook(fstream);
```

## Steg 5: Få åtkomst till kalkylarket

Navigera till det första kalkylbladet i Excel-filen:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Steg 6: Visar förhandsvisningen sida för visning

Aktivera sida för förhandsgranskning för kalkylarket:

```csharp
worksheet. IsPageBreakPreview = true;
```

## Steg 7: Spara ändringar

Spara ändringarna som gjorts i Excel-filen:

```csharp
workbook.Save(dataDir + "output.xls");
```

## Steg 8: Stänga filströmmen

Stäng filströmmen för att frigöra alla resurser:

```csharp
fstream.Close();
```

### Exempel på källkod för Page Break Preview of Worksheet med Aspose.Cells för .NET 
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
// Visar arbetsbladet i förhandsvisning av sidbrytning
worksheet.IsPageBreakPreview = true;
// Sparar den ändrade Excel-filen
workbook.Save(dataDir + "output.xls");
// Stänger filströmmen för att frigöra alla resurser
fstream.Close();
```

## Slutsats

I den här handledningen lärde du dig hur du visar sidbrytningsförhandsvisningen av ett kalkylblad med Aspose.Cells för .NET. Genom att följa stegen som beskrivs kan du enkelt kontrollera utseendet och layouten på dina Excel-filer.

### Vanliga frågor (FAQ)

#### Vad är Aspose.Cells för .NET?

Aspose.Cells för .NET är ett populärt programbibliotek för att manipulera Excel-filer i .NET-applikationer.

#### Kan jag visa förhandsvisningen sida för ett specifikt kalkylblad istället för hela kalkylbladet?

Ja, med Aspose.Cells kan du aktivera förhandsvisning av sidbrytning för ett specifikt kalkylblad genom att komma åt motsvarande kalkylbladsobjekt.

#### Stöder Aspose.Cells andra Excel-filredigeringsfunktioner?

Ja, Aspose.Cells erbjuder ett brett utbud av funktioner för att redigera och manipulera Excel-filer, som att lägga till data, formatera, skapa diagram, etc.

#### Fungerar Aspose.Cells bara med Excel-filer i .xls-format?

Nej, Aspose.Cells stöder olika Excel-filformat inklusive .xls och .xlsx.
	