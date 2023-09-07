---
title: Avancerade skyddsinställningar för Excel-arbetsblad
linktitle: Avancerade skyddsinställningar för Excel-arbetsblad
second_title: Aspose.Cells för .NET API-referens
description: Skydda dina Excel-filer genom att ställa in avancerade skyddsinställningar med Aspose.Cells för .NET.
type: docs
weight: 10
url: /sv/net/excel-security/advanced-protection-settings-for-excel-worksheet/
---
I den här handledningen går vi igenom stegen för att ställa in avancerade skyddsinställningar för ett Excel-kalkylblad med Aspose.Cells-biblioteket för .NET. Följ instruktionerna nedan för att slutföra denna uppgift.

## Steg 1: Förberedelser

Se till att du har installerat Aspose.Cells för .NET och skapat ett C#-projekt i din föredragna integrerade utvecklingsmiljö (IDE).

## Steg 2: Ställ in sökvägen till dokumentkatalogen

 Deklarera a`dataDir` variabel och initiera den med sökvägen till din dokumentkatalog. Till exempel :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Se till att byta ut`"YOUR_DOCUMENTS_DIRECTORY"` med den faktiska sökvägen till din katalog.

## Steg 3: Skapa en filström för att öppna Excel-filen

 Skapa en`FileStream` objekt som innehåller Excel-filen som ska öppnas:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 Se till att du har Excel-filen`book1.xls` i din dokumentkatalog eller ange korrekt filnamn och plats.

## Steg 4: Instantiera ett arbetsboksobjekt och öppna Excel-filen

 Använd`Workbook`klass från Aspose.Cells för att instansiera ett Workbook-objekt och öppna den angivna Excel-filen via filströmmen:

```csharp
Workbook excel = new Workbook(fstream);
```

## Steg 5: Öppna det första kalkylbladet

Navigera till det första kalkylbladet i Excel-filen:

```csharp
Worksheet worksheet = excel.Worksheets[0];
```

## Steg 6: Ange skyddsinställningar för kalkylblad

Använd kalkylbladsobjektegenskaper för att ställa in kalkylbladsskydd efter behov. Till exempel :

```csharp
worksheet.Protection.AllowDeletingColumn = false;
worksheet.Protection.AllowDeletingRow = false;
worksheet.Protection.AllowEditingContent = false;
worksheet.Protection.AllowEditingObject = false;
// ... Ställ in andra skyddsinställningar efter behov...
```

## Steg 7: Spara den ändrade Excel-filen

 Spara den ändrade Excel-filen med hjälp av`Save` metod för arbetsboksobjektet:

```csharp
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

Var noga med att ange önskad sökväg och filnamn för utdatafilen.

## Steg 8: Stäng filströmmen

När du har sparat stänger du filströmmen för att frigöra alla associerade resurser:

```csharp
fstream.Close();
```
	
### Exempel på källkod för avancerade skyddsinställningar för Excel-arbetsblad med Aspose.Cells för .NET 
```csharp
// Sökvägen till dokumentkatalogen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Skapa en filström som innehåller Excel-filen som ska öppnas
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Instantiera ett arbetsboksobjekt
// Öppna Excel-filen genom filströmmen
Workbook excel = new Workbook(fstream);
// Åtkomst till det första kalkylbladet i Excel-filen
Worksheet worksheet = excel.Worksheets[0];
// Begränsa användare att ta bort kolumner i kalkylbladet
worksheet.Protection.AllowDeletingColumn = false;
// Begränsa användare att ta bort rad i kalkylbladet
worksheet.Protection.AllowDeletingRow = false;
// Begränsa användare att redigera innehållet i kalkylbladet
worksheet.Protection.AllowEditingContent = false;
// Begränsa användare att redigera objekt i kalkylbladet
worksheet.Protection.AllowEditingObject = false;
// Begränsa användare att redigera scenarier i kalkylbladet
worksheet.Protection.AllowEditingScenario = false;
//Begränsa användare att filtrera
worksheet.Protection.AllowFiltering = false;
// Tillåter användare att formatera celler i kalkylbladet
worksheet.Protection.AllowFormattingCell = true;
// Tillåter användare att formatera rader i kalkylbladet
worksheet.Protection.AllowFormattingRow = true;
// Tillåter användare att infoga kolumner i kalkylbladet
worksheet.Protection.AllowFormattingColumn = true;
// Tillåter användare att infoga hyperlänkar i kalkylbladet
worksheet.Protection.AllowInsertingHyperlink = true;
// Tillåter användare att infoga rader i kalkylbladet
worksheet.Protection.AllowInsertingRow = true;
// Tillåter användare att välja låsta celler i kalkylbladet
worksheet.Protection.AllowSelectingLockedCell = true;
// Tillåter användare att välja olåsta celler i kalkylbladet
worksheet.Protection.AllowSelectingUnlockedCell = true;
// Tillåter användare att sortera
worksheet.Protection.AllowSorting = true;
// Tillåter användare att använda pivottabeller i kalkylbladet
worksheet.Protection.AllowUsingPivotTable = true;
// Sparar den ändrade Excel-filen
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
// Stänger filströmmen för att frigöra alla resurser
fstream.Close();
```

## Slutsats

Grattis! Du har nu lärt dig hur du ställer in avancerade skyddsinställningar för ett Excel-kalkylblad med Aspose.Cells för .NET. Använd denna kunskap för att säkra dina Excel-filer och begränsa användaråtgärder.

### Vanliga frågor

#### F: Hur kan jag skapa ett nytt C#-projekt i min IDE?

S: Stegen för att skapa ett nytt C#-projekt kan variera beroende på vilken IDE du använder. Se din IDE:s dokumentation för detaljerade instruktioner.

#### F: Är det möjligt att ställa in andra anpassade skyddsinställningar än de som nämns i handledningen?

S: Ja, Aspose.Cells erbjuder ett brett utbud av skyddsinställningar som du kan anpassa efter dina specifika behov. Se Aspose.Cells dokumentation för mer information.

#### F: Vilket filformat används för att spara den modifierade Excel-filen i exempelkoden?

S: I exempelkoden sparas den modifierade Excel-filen i Excel 97-2003 (.xls)-format. Du kan välja andra format som stöds av Aspose.Cells om det behövs.

#### F: Hur kommer jag åt andra kalkylblad i Excel-filen?

 S: Du kan komma åt andra kalkylblad med hjälp av index eller arknamn, till exempel:`Worksheet worksheet = excel.Worksheets[1];` eller`Worksheet worksheet = excel.Worksheets[" SheetName"];`.