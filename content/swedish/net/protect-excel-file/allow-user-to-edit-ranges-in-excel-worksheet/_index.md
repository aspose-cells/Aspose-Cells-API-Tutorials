---
title: Tillåt användaren att redigera intervall i Excel-kalkylblad
linktitle: Tillåt användaren att redigera intervall i Excel-kalkylblad
second_title: Aspose.Cells för .NET API-referens
description: Tillåt användare att redigera specifika intervall i ett Excel-kalkylblad med Aspose.Cells för .NET. Steg för steg guide med källkod i C#.
type: docs
weight: 10
url: /sv/net/protect-excel-file/allow-user-to-edit-ranges-in-excel-worksheet/
---
I den här guiden går vi igenom hur du använder Aspose.Cells för .NET för att tillåta användaren att redigera specifika intervall i ett Excel-kalkylblad. Följ stegen nedan för att utföra denna uppgift.

## Steg 1: Sätta upp miljön

Se till att du har ställt in din utvecklingsmiljö och installerat Aspose.Cells för .NET. Du kan ladda ner den senaste versionen av biblioteket från Asposes officiella webbplats.

## Steg 2: Importera nödvändiga namnrymder

I ditt C#-projekt, importera de nödvändiga namnrymden för att arbeta med Aspose.Cells:

```csharp
using Aspose.Cells;
```

## Steg 3: Ställ in sökvägen till dokumentkatalogen

 Deklarera a`dataDir` variabel för att ange sökvägen till katalogen där du vill spara den genererade Excel-filen:

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Se till att byta ut`"YOUR_DOCUMENT_DIRECTORY"` med rätt sökväg på ditt system.

## Steg 4: Skapa ett arbetsboksobjekt

Instantiera ett nytt arbetsboksobjekt som representerar den Excel-arbetsbok du vill skapa:

```csharp
Workbook book = new Workbook();
```

## Steg 5: Tillgång till det första kalkylbladet

Navigera till det första kalkylbladet i Excel-arbetsboken med följande kod:

```csharp
Worksheet sheet = book.Worksheets[0];
```

## Steg 6: Hämta auktoriserade ändringsintervall

 Få samlingen av tillåtna redigeringsintervall med hjälp av`AllowEditRanges` fast egendom:

```csharp
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
```

## Steg 7: Definiera ett skyddat område

 Definiera ett skyddat område med hjälp av`Add` metod för`AllowEditRanges` samling:

```csharp
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
protectedRange protectedRange = allowRanges[idx];
```

Här har vi skapat ett skyddat område "r2" som sträcker sig från cell A1 till cell C3.

## Steg 8: Ange lösenordet

 Ange ett lösenord för det skyddade området med hjälp av`Password` fast egendom:

```csharp
protectedRange.Password = "YOUR_PASSWORD";
```

 Se till att byta ut`"YOUR_PASSWORD"` med önskat lösenord.

## Steg 9: Skydda kalkylbladet

 Skydda kalkylbladet med hjälp av`Protect` metod för`Worksheet` objekt:

```csharp
sheet.Protect(ProtectionType.All);
```

Detta skyddar kalkylarket genom att förhindra ändringar utanför de tillåtna intervallen.

## Steg 10: Registrera

  Excel fil

 Spara den genererade Excel-filen med hjälp av`Save` metod för`Workbook` objekt:

```csharp
book.Save(dataDir + "protectedrange.out.xls");
```

Var noga med att ange önskat filnamn och rätt sökväg.

### Exempel på källkod för Tillåt användare att redigera intervall i Excel-kalkylblad med Aspose.Cells för .NET 
```csharp
//Sökvägen till dokumentkatalogen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Skapa katalog om den inte redan finns.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Instantiera en ny arbetsbok
Workbook book = new Workbook();
// Hämta det första (standard) kalkylbladet
Worksheet sheet = book.Worksheets[0];
// Hämta Allow Edit Ranges
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
// Definiera ProtectedRange
ProtectedRange proteced_range;
// Skapa sortimentet
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
proteced_range = allowRanges[idx];
// Ange lösenordet
proteced_range.Password = "123";
// Skydda arket
sheet.Protect(ProtectionType.All);
// Spara Excel-filen
book.Save(dataDir + "protectedrange.out.xls");
```

## Slutsats

Du har nu lärt dig hur du använder Aspose.Cells för .NET för att tillåta användaren att redigera specifika intervall i ett Excel-kalkylblad. Utforska gärna funktionerna som erbjuds av Aspose.Cells för att möta dina specifika behov.


### Vanliga frågor

#### 1. Hur låter man användaren redigera specifika intervall i Excel-kalkylblad?

 Du kan använda`ProtectedRangeCollection` klass för att definiera tillåtna modifikationsintervall. Använd`Add` metod för att skapa ett nytt skyddat område med de önskade cellerna.

#### 2. Kan jag ställa in ett lösenord för auktoriserade ändringsintervall?

 Ja, du kan ange ett lösenord med hjälp av`Password` egendom av`ProtectedRange` objekt. Detta kommer endast att begränsa åtkomsten till användare med lösenordet.

#### 3. Hur skyddar jag kalkylarket när de tillåtna intervallen är inställda?

 Använd`Protect` metod för`Worksheet` objekt för att skydda kalkylbladet. Detta kommer att förhindra alla ändringar utanför de tillåtna intervallen, eventuellt uppmanas efter ett lösenord om du angav ett.