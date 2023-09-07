---
title: Infoga bild i sidhuvudet
linktitle: Infoga bild i sidhuvudet
second_title: Aspose.Cells för .NET API-referens
description: Lär dig hur du infogar en bild i sidhuvudet eller sidfoten i ett Excel-dokument med Aspose.Cells för .NET. Steg för steg guide med källkod i C#.
type: docs
weight: 60
url: /sv/net/excel-page-setup/insert-image-in-header-footer/
---
Möjligheten att infoga en bild i sidhuvudet eller sidfoten i ett Excel-dokument kan vara mycket användbart för att anpassa dina rapporter eller lägga till företagslogotyper. I den här artikeln guidar vi dig steg för steg för att infoga en bild i sidhuvudet eller sidfoten i ett Excel-dokument med Aspose.Cells för .NET. Du kommer att lära dig hur du gör detta med C#-källkoden.

## Steg 1: Sätta upp miljön

Innan du börjar, se till att du har Aspose.Cells för .NET installerat på din maskin. Skapa också ett nytt projekt i din föredragna utvecklingsmiljö.

## Steg 2: Importera nödvändiga bibliotek

Importera de bibliotek som behövs för att arbeta med Aspose.Cells i din kodfil. Här är motsvarande kod:

```csharp
using Aspose.Cells;
```

## Steg 3: Ställ in dokumentkatalog

Ställ in katalogen där Excel-dokumentet du vill arbeta med finns. Använd följande kod för att ställa in katalogen:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

Var noga med att ange den fullständiga katalogsökvägen.

## Steg 4: Skapa ett arbetsboksobjekt

Arbetsboksobjektet representerar Excel-dokumentet som du ska arbeta med. Du kan skapa den med följande kod:

```csharp
Workbook workbook = new Workbook();
```

Detta skapar ett nytt tomt arbetsboksobjekt.

## Steg 5: Lagra bildens URL

Definiera webbadressen eller sökvägen till bilden du vill infoga i sidhuvudet eller sidfoten. Använd följande kod för att lagra bildens URL:

```csharp
string logo_url = dataDir + "aspose-logo.jpg";
```

Se till att den angivna sökvägen är korrekt och att bilden finns på den platsen.

## Steg 6: Öppna bildfilen

För att öppna bildfilen använder vi ett FileStream-objekt och läser binärdata från bilden. Här är motsvarande kod:

```csharp
FileStream inFile;
byte[] binaryData;

inFile = new System.IO.FileStream(logo_url, System.IO.FileMode.Open, System.IO.FileAccess.Read);
binaryData = new Byte[inFile.Length];
long bytesRead = inFile.Read(binaryData, 0, (int)inFile.Length);
```

Se till att bildsökvägen är korrekt och att du har rätt behörighet att komma åt den.

## Steg 7: Konfigurera PageSetup

Objektet PageSetup används för att ställa in Excel-dokumentets sidinställningar inklusive sidhuvud och sidfot. Använd följande kod för att hämta PageSetup-objektet i det första kalkylbladet:

```csharp
PageSetup pageSetup = workbook. Worksheets

[0].PageSetup;
```

Detta ger dig tillgång till sidinställningarna för det första kalkylbladet i arbetsboken.

## Steg 8: Lägga till bilden i rubriken

Använd metoden SetHeaderPicture() för objektet PageSetup för att ställa in bilden i mittsektionen av sidhuvudet. Här är motsvarande kod:

```csharp
pageSetup.SetHeaderPicture(1, binaryData);
```

Detta kommer att lägga till den angivna bilden i sidhuvudet.

## Steg 9: Lägga till ett skript i rubriken

För att lägga till skript till sidhuvudet, använd metoden SetHeader() för objektet PageSetup. Här är motsvarande kod:

```csharp
pageSetup.SetHeader(1, "&G");
```

Detta kommer att lägga till det angivna skriptet till sidhuvudet. I det här exemplet visar skriptet "&G" sidnumret.

## Steg 10: Lägg till arbetsbladsnamn i rubriken

Om du vill visa arknamnet i sidhuvudet använder du metoden SetHeader() för objektet PageSetup igen. Här är motsvarande kod:

```csharp
pageSetup.SetHeader(2, "&A");
```

Detta kommer att lägga till arknamnet i sidhuvudet. Skriptet "&A" används för att representera arknamnet.

## Steg 11: Spara arbetsboken

För att spara ändringar i arbetsboken, använd metoden Save() för Workbook-objektet. Här är motsvarande kod:

```csharp
workbook.Save(dataDir + "InsertImageInHeaderFooter_out.xls");
```

Detta kommer att spara arbetsboken med ändringarna i den angivna katalogen.

## Steg 12: Stänga FileStream

Efter att ha läst binärdata från bilden, se till att stänga FileStream för att frigöra resurserna. Använd följande kod för att stänga FileStream:

```csharp
inFile.Close();
```

Se till att alltid stänga FileStreams när du är klar med dem.

### Exempel på källkod för Infoga bild i sidhuvud med Aspose.Cells för .NET 
```csharp
// Sökvägen till dokumentkatalogen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
//Skapa ett arbetsboksobjekt
Workbook workbook = new Workbook();
// Skapa en strängvariabel för att lagra logotypens/bildens url
string logo_url = dataDir + "aspose-logo.jpg";
// Deklarera ett FileStream-objekt
FileStream inFile;
// Deklarerar en byte-array
byte[] binaryData;
// Skapar instansen av FileStream-objektet för att öppna logotypen/bilden i strömmen
inFile = new System.IO.FileStream(logo_url, System.IO.FileMode.Open, System.IO.FileAccess.Read);
// Instantiera byte-arrayen för FileStream-objektets storlek
binaryData = new Byte[inFile.Length];
// Läser ett block av byte från strömmen och skriver data i en given buffert av byte array.
long bytesRead = inFile.Read(binaryData, 0, (int)inFile.Length);
// Skapa ett PageSetup-objekt för att få sidinställningarna för det första kalkylbladet i arbetsboken
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Ställ in logotypen/bilden i mitten av sidhuvudet
pageSetup.SetHeaderPicture(1, binaryData);
// Ställa in manus för logotypen/bilden
pageSetup.SetHeader(1, "&G");
// Ställer in arkets namn i den högra delen av sidhuvudet med skriptet
pageSetup.SetHeader(2, "&A");
// Sparar arbetsboken
workbook.Save(dataDir + "InsertImageInHeaderFooter_out.xls");
//Stänger FileStream-objektet
inFile.Close();       
```
## Slutsats

Grattis! Du vet nu hur du infogar en bild i sidhuvudet eller sidfoten i ett Excel-dokument med Aspose.Cells för .NET. Denna handledning ledde dig genom varje steg i processen, från att ställa in miljön till att spara den modifierade arbetsboken. Experimentera gärna mer med funktionerna i Aspose.Cells för att skapa personliga och professionella Excel-dokument.

### FAQ's

#### F1: Är det möjligt att infoga flera bilder i sidhuvudet eller sidfoten i ett Excel-dokument?

S1: Ja, du kan infoga flera bilder i sidhuvudet eller sidfoten i ett Excel-dokument genom att upprepa steg 8 och 9 för varje ytterligare bild.

#### F2: Vilka bildformat stöds för infogning i sidhuvud eller sidfot?
S2: Aspose.Cells stöder en mängd vanliga bildformat som JPEG, PNG, GIF, BMP, etc.

#### F3: Kan jag anpassa utseendet på sidhuvudet eller sidfoten ytterligare?

S3: Ja, du kan använda speciella skript och koder för att ytterligare formatera och anpassa utseendet på sidhuvudet eller sidfoten. Se Aspose.Cells dokumentation för mer information om anpassningsalternativ.

#### F4: Fungerar Aspose.Cells med olika versioner av Excel?

S4: Ja, Aspose.Cells är kompatibel med olika versioner av Excel inklusive Excel 2003, Excel 2007, Excel 2010, Excel 2013, Excel 2016 och Excel 2019.

#### F5: Är det möjligt att infoga bilder i andra delar av Excel-dokumentet, till exempel celler eller diagram?

S5: Ja, Aspose.Cells tillhandahåller omfattande funktioner för att infoga bilder i olika delar av Excel-dokumentet, inklusive celler, diagram och ritobjekt.