---
title: Ange författare medan skrivskyddande Excel-arbetsbok
linktitle: Ange författare medan skrivskyddande Excel-arbetsbok
second_title: Aspose.Cells för .NET API-referens
description: Lär dig hur du skyddar och anpassar dina Excel-arbetsböcker med Aspose.Cells för .NET. Steg för steg handledning i C#.
type: docs
weight: 30
url: /sv/net/excel-security/specify-author-while-write-protecting-excel-workbook/
---

I den här handledningen kommer vi att visa dig hur du anger författaren när du skrivskyddar en Excel-arbetsbok med Aspose.Cells-biblioteket för .NET.

## Steg 1: Förbered miljön

Innan du börjar, se till att du har Aspose.Cells för .NET installerat på din maskin. Ladda ner biblioteket från Asposes officiella webbplats och följ installationsinstruktionerna.

## Steg 2: Konfigurera käll- och utdatakataloger

 den medföljande källkoden måste du ange käll- och utdatakataloger. Ändra`sourceDir` och`outputDir` variabler genom att ersätta "DIN KÄLLKATOGRAF" och "DIN UTGÅNGSKATALOG" med respektive absoluta sökvägar på din maskin.

```csharp
// Källkatalog
string sourceDir = "PATH TO YOUR SOURCE DIRECTORY";

// Utdatakatalog
string outputDir = "YOUR OUTPUT DIRECTORY PATH";
```

## Steg 3: Skapa en tom Excel-arbetsbok

Till att börja med skapar vi ett Workbook-objekt som representerar en tom Excel-arbetsbok.

```csharp
// Skapa en tom arbetsbok.
Workbook wb = new Workbook();
```

## Steg 4: Skrivskydd med lösenord

 Därefter anger vi ett lösenord för att skrivskydda Excel-arbetsboken med hjälp av`WriteProtection.Password` egenskapen för arbetsboksobjektet.

```csharp
// Skriv skydda arbetsbok med lösenord.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";
```

## Steg 5: Författarspecifikation

 Nu anger vi författaren till Excel-arbetsboken med hjälp av`WriteProtection.Author` egenskapen för arbetsboksobjektet.

```csharp
// Ange författare medan skrivskyddande arbetsbok.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";
```

## Steg 6: Säkerhetskopiera skyddad Excel-arbetsbok

 När skrivskyddet och författaren är specificerade kan vi spara Excel-arbetsboken i XLSX-format med hjälp av`Save()` metod.

```csharp
// Spara arbetsboken i XLSX-format.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");
```

### Exempel på källkod för Ange författare medan skrivskyddande Excel-arbetsbok använder Aspose.Cells för .NET 
```csharp
//Källkatalog
string sourceDir = "YOUR SOURCE DIRECTORY";

//Utdatakatalog
string outputDir = "YOUR OUTPUT DIRECTORY";

// Skapa en tom arbetsbok.
Workbook wb = new Workbook();

// Skriv skydda arbetsbok med lösenord.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";

// Ange författare medan skrivskyddande arbetsbok.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";

// Spara arbetsboken i XLSX-format.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");

```

## Slutsats

Grattis! Du har nu lärt dig hur du anger författaren när du skrivskyddar en Excel-arbetsbok med Aspose.Cells för .NET. Du kan tillämpa dessa steg på dina egna projekt för att skydda och anpassa dina Excel-arbetsböcker.

Utforska gärna funktionerna i Aspose.Cells för .NET ytterligare för mer avancerade funktioner för Excel-filer.

## Vanliga frågor

#### F: Kan jag skrivskydda en Excel-arbetsbok utan att ange ett lösenord?

 S: Ja, du kan använda arbetsboksobjektets`WriteProtect()` utan att ange ett lösenord för att skrivskydda en Excel-arbetsbok. Detta kommer att begränsa ändringar i arbetsboken utan att kräva ett lösenord.

#### F: Hur tar jag bort skrivskydd från en Excel-arbetsbok?

 S: För att ta bort skrivskydd från en Excel-arbetsbok kan du använda`Unprotect()` metod för kalkylbladsobjektet eller`RemoveWriteProtection()` metod för Workbook-objektet, beroende på ditt specifika användningsfall. .

#### F: Jag har glömt lösenordet för att skydda min Excel-arbetsbok. Vad kan jag göra ?

S: Om du har glömt lösenordet för att skydda din Excel-arbetsbok kan du inte ta bort det direkt. Du kan dock försöka använda specialiserade tredjepartsverktyg som tillhandahåller lösenordsåterställningsfunktioner för skyddade Excel-filer.

#### F: Är det möjligt att ange flera författare när man skrivskyddar en Excel-arbetsbok?

S: Nej, Aspose.Cells för .NET-biblioteket tillåter att en enskild författare specificeras när en Excel-arbetsbok skrivskyddas. Om du vill ange flera författare måste du överväga anpassade lösningar genom att direkt manipulera Excel-filen.