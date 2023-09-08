---
title: Excel Kopiera kalkylblad från annan arbetsbok
linktitle: Excel Kopiera kalkylblad från annan arbetsbok
second_title: Aspose.Cells för .NET API-referens
description: Kopiera enkelt ett Excel-kalkylblad från en arbetsbok till en annan med Aspose.Cells för .NET.
type: docs
weight: 10
url: /sv/net/excel-copy-worksheet/excel-copy-worksheet-from-other-workbook/
---
I den här handledningen går vi igenom stegen för att kopiera ett Excel-kalkylblad från en annan arbetsbok med Aspose.Cells-biblioteket för .NET. Följ instruktionerna nedan för att slutföra denna uppgift.

## Steg 1: Förberedelser

Innan du börjar, se till att du har installerat Aspose.Cells för .NET och skapat ett C#-projekt i din föredragna integrerade utvecklingsmiljö (IDE).

## Steg 2: Ställ in sökvägen till dokumentkatalogen

 Deklarera a`dataDir` variabel och initiera den med sökvägen till din dokumentkatalog. Till exempel :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Se till att byta ut`"YOUR_DOCUMENTS_DIRECTORY"` med den faktiska sökvägen till din katalog.

## Steg 3: Skapa en ny Excel-arbetsbok

 Använd`Workbook` klass från Aspose.Cells för att skapa en ny Excel-arbetsbok:

```csharp
Workbook excelWorkbook0 = new Workbook();
```

## Steg 4: Få det första kalkylbladet i arbetsboken

Navigera till det första kalkylbladet i arbetsboken med index 0:

```csharp
Worksheet ws0 = excelWorkbook0.Worksheets[0];
```

## Steg 5: Lägg till data till rubrikrader (A1:A4)

 Använda en`for` loop för att lägga till data till rubrikraderna (A1:A4):

```csharp
for (int i = 0; i < 5; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Header row {0}", i));
}
```

## Steg 6: Lägg till detaljerad data (A5:A999)

 Använd en annan`for` loop för att lägga till detaljerad data (A5:A999):

```csharp
for (int i = 5; i < 1000; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Detail row {0}", i));
}
```

## Steg 7: Ställ in layoutalternativ

 Ställ in sidinställningar för kalkylbladet med hjälp av`PageSetup` objekt:

```csharp
PageSetup pagesetup = ws0.PageSetup;
pagesetup.PrintTitleRows = "$1:$5";
```

## Steg 8: Skapa en annan Excel-arbetsbok

Skapa en annan Excel-arbetsbok:

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## Steg 9: Hämta det första kalkylbladet från den andra arbetsboken

Navigera till det första kalkylbladet i den andra arbetsboken:

```csharp
Worksheet ws1 = excelWorkbook1.Worksheets[0];
```

## Steg 10: Namnge kalkylbladet

namnge elden

beräkningsö:

```csharp
ws1.Name = "MySheet";
```

## Steg 11: Kopiera data från det första kalkylbladet i den första arbetsboken till det första kalkylbladet i den andra arbetsboken

Kopiera data från det första kalkylbladet i den första arbetsboken till det första kalkylbladet i den andra arbetsboken:

```csharp
ws1.Copy(ws0);
```

## Steg 12: Spara Excel-filen

Spara Excel-filen:

```csharp
excelWorkbook1.Save(dataDir + "CopyWorkbookSheetToOther_out.xls");
```

Var noga med att ange önskad sökväg och filnamn för utdatafilen.

### Exempel på källkod för Excel Kopiera arbetsblad från annan arbetsbok med Aspose.Cells för .NET 
```csharp
//Sökvägen till dokumentkatalogen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Skapa en ny arbetsbok.
Workbook excelWorkbook0 = new Workbook();
// Skaffa det första arbetsbladet i boken.
Worksheet ws0 = excelWorkbook0.Worksheets[0];
// Lägg in lite data i rubrikrader (A1:A4)
for (int i = 0; i < 5; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Header Row {0}", i));
}
// Lägg in lite detaljdata (A5:A999)
for (int i = 5; i < 1000; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Detail Row {0}", i));
}
// Definiera ett siduppsättningsobjekt baserat på det första kalkylbladet.
PageSetup pagesetup = ws0.PageSetup;
// De första fem raderna upprepas på varje sida...
// Det kan ses i förhandsgranskning.
pagesetup.PrintTitleRows = "$1:$5";
// Skapa en annan arbetsbok.
Workbook excelWorkbook1 = new Workbook();
// Skaffa det första arbetsbladet i boken.
Worksheet ws1 = excelWorkbook1.Worksheets[0];
// Namnge arbetsbladet.
ws1.Name = "MySheet";
// Kopiera data från det första kalkylbladet i den första arbetsboken till
// första arbetsbladet i den andra arbetsboken.
ws1.Copy(ws0);
// Spara excel-filen.
excelWorkbook1.Save(dataDir + "CopyWorksheetFromWorkbookToOther_out.xls");
```

## Slutsats

Grattis! Du har nu lärt dig hur du kopierar ett Excel-kalkylblad från en annan arbetsbok med Aspose.Cells för .NET. Använd gärna denna metod i dina egna projekt för att effektivt manipulera Excel-filer.

### Vanliga frågor

#### F. Vilka bibliotek behövs för att använda Aspose.Cells för .NET?

A. För att använda Aspose.Cells för .NET måste du inkludera Aspose.Cells-biblioteket i ditt projekt. Se till att du har refererat till det här biblioteket korrekt i din integrerade utvecklingsmiljö (IDE).

#### F. Stöder Aspose.Cells andra Excel-filformat, såsom XLSX?

A. Ja, Aspose.Cells stöder olika Excel-filformat inklusive XLSX, XLS, CSV, HTML och många fler. Du kan manipulera dessa filformat med funktionerna i Aspose.Cells för .NET.

#### F. Kan jag anpassa layoutalternativen när jag kopierar arbetsbladet?

A.  Ja, du kan anpassa sidinställningarna när du kopierar arbetsbladet med hjälp av egenskaperna för`PageSetup` objekt. Du kan ange sidhuvuden, sidfötter, marginaler, orienteringar osv.