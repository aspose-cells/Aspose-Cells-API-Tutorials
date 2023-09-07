---
title: Excel kopia arbetsblad
linktitle: Excel kopia arbetsblad
second_title: Aspose.Cells för .NET API-referens
description: Kopiera ett Excel-kalkylblad till ett annat med Aspose.Cells för .NET.
type: docs
weight: 20
url: /sv/net/excel-copy-worksheet/excel-copy-worksheet/
---

den här guiden kommer vi att förklara hur man kopierar ett Excel-kalkylblad med Aspose.Cells-biblioteket för .NET. Vi förser dig med C#-källkod och leder dig genom stegen som krävs för att slutföra denna uppgift. I slutet kommer vi att visa dig det förväntade resultatet. Följ instruktionerna nedan för att komma igång.

## Steg 1: Förberedelser

Innan du börjar, se till att du har installerat Aspose.Cells för .NET och skapat ett C#-projekt i din föredragna integrerade utvecklingsmiljö (IDE). Se också till att du har en kopia av Excel-filen du vill manipulera.

## Steg 2: Importera nödvändiga bibliotek

 I din C#-källfil, importera de nödvändiga biblioteken från Aspose.Cells med hjälp av`using` direktiv:

```csharp
using Aspose.Cells;
```

## Steg 3: Ställ in filsökvägen

 Deklarera a`dataDir` variabel och initiera den med katalogen som innehåller din Excel-fil. Till exempel :

```csharp
string dataDir = "PATH_TO_YOUR_DOCUMENT_DIRECTORY";
```

 Se till att byta ut`"PATH_TO_YOUR_DOCUMENT_DIRECTORY"` med den faktiska sökvägen till din katalog.

## Steg 4: Ladda befintlig Excel-fil

 Använd`Workbook`klass från Aspose.Cells för att öppna den befintliga Excel-filen. Använd`InputPath` variabel för att ange filsökvägen:

```csharp
string InputPath = dataDir + "book1.xls";
Workbook wb = new Workbook(InputPath);
```

 Se till att du har bytt ut`"book1.xls"` med det faktiska namnet på din Excel-fil.

## Steg 5: Kopiera arbetsbladet

 Nu kommer vi att kopiera det befintliga kalkylbladet till ett nytt kalkylblad. Använd`Worksheets` egendom av`Workbook` objekt för att komma åt samlingen av kalkylblad:

```csharp
WorksheetCollection sheets = wb.Worksheets;
```

 Använd sedan`AddCopy` metod för att kopiera det angivna arbetsbladet. Till exempel, för att kopiera "Sheet1":

```csharp
sheets.AddCopy("Sheet1");
```

## Steg 6: Spara Excel-filen

 Använd`Save` metod för`Workbook` objekt för att spara ändringar i en ny fil:

```csharp
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

Var noga med att ange önskad sökväg och filnamn för utdatafilen.

### Exempel på källkod för Excel Copy Worksheet med Aspose.Cells för .NET 

```csharp
// Sökvägen till dokumentkatalogen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Öppna en befintlig Excel-fil.
Workbook wb = new Workbook(InputPath);
// Skapa ett kalkylbladsobjekt med hänvisning till
// arken i arbetsboken.
WorksheetCollection sheets = wb.Worksheets;
// Kopiera data till ett nytt ark från ett befintligt
// ark i arbetsboken.
sheets.AddCopy("Sheet1");
// Spara Excel-filen.
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

## Slutsats

Grattis! Du har nu lärt dig hur du kopierar ett Excel-kalkylblad med Aspose.Cells för .NET. Denna steg-för-steg-guide visade hur man importerar de nödvändiga biblioteken, laddar en befintlig Excel-fil, kopierar arbetsbladet och sparar den ändrade filen. Använd gärna denna metod i dina egna projekt för att effektivt manipulera Excel-filer.

### Vanliga frågor

#### F. Är Aspose.Cells kompatibel med andra programmeringsspråk?

A. Ja, Aspose.Cells stöder flera programmeringsspråk inklusive C#, Java, Python och många fler.

#### F. Kan jag kopiera ett kalkylblad till en annan Excel-arbetsbok?

A.  Ja, du kan använda`AddCopy` metod för att kopiera ett kalkylblad till en annan Excel-arbetsbok.

#### F. Behåller Aspose.Cells formler och formatering när man kopierar arbetsbladet?

A. Ja, Aspose.Cells bevarar formler, formatering och andra egenskaper när du kopierar ett kalkylblad.

#### F. Kräver Aspose.Cells en licens för kommersiellt bruk?

A. Ja, Aspose.Cells är en kommersiell produkt och kräver köp av en licens för kommersiellt bruk. Du kan hitta mer licensinformation på Asposes officiella webbplats.