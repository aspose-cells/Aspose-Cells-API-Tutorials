---
title: Skydda specifika celler i ett Excel-kalkylblad
linktitle: Skydda specifika celler i ett Excel-kalkylblad
second_title: Aspose.Cells för .NET API-referens
description: Lär dig hur du skyddar specifika celler i Excel med Aspose.Cells för .NET. Steg för steg handledning i C#.
type: docs
weight: 70
url: /sv/net/protect-excel-file/protect-specific-cells-in-a-excel-worksheet/
---
I den här handledningen kommer vi att titta på C#-källkoden som använder Aspose.Cells-biblioteket för att skydda specifika celler i ett Excel-kalkylblad. Vi går igenom varje steg i koden och förklarar hur det fungerar. Följ instruktionerna noggrant för att få önskat resultat.

## Steg 1: Förutsättningar

Innan du börjar, se till att du har installerat Aspose.Cells-biblioteket för .NET. Du kan hämta det från Asposes officiella hemsida. Se också till att du har en senaste version av Visual Studio eller någon annan C#-utvecklingsmiljö.

## Steg 2: Importera nödvändiga namnrymder

För att använda Aspose.Cells-biblioteket måste vi importera de nödvändiga namnrymden till vår kod. Lägg till följande rader överst i din C#-källfil:

```csharp
using Aspose.Cells;
```

## Steg 3: Skapa en Excel-arbetsbok

I det här steget kommer vi att skapa en ny Excel-arbetsbok. Använd följande kod för att skapa en Excel-arbetsbok:

```csharp
// Sökväg till dokumentkatalogen.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Skapa en ny arbetsbok.
Workbook wb = new Workbook();
```

 Se till att byta ut`"YOUR_DOCUMENTS_DIR"` med lämplig sökväg till din dokumentkatalog.

## Steg 4: Skapa ett kalkylblad

Nu när vi har skapat Excel-arbetsboken, låt oss skapa ett kalkylblad och få det första bladet. Använd följande kod:

```csharp
// Skapa ett kalkylarksobjekt och få det första arket.
Worksheet sheet = wb.Worksheets[0];
```

## Steg 5: Definiera stilen

I det här steget kommer vi att definiera stilen som ska tillämpas på specifika celler. Använd följande kod:

```csharp
// Definition av stilobjektet.
Styling styling;
```

## Steg 6: Slinga för att låsa upp alla kolumner

Nu ska vi gå igenom alla kolumner i kalkylbladet och låsa upp dem. Använd följande kod:

```csharp
// Gå igenom alla kolumner i kalkylbladet och lås upp dem.
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style);
}
```

## Steg 7: Låsa specifika celler

I det här steget kommer vi att låsa specifika celler. Använd följande kod:

```csharp
//Låser alla tre celler... dvs A1, B1, C1.
style = sheet.Cells["A1"].GetStyle();
style. IsLocked = true;
sheet.Cells["A1"].SetStyle(style);

style = sheet.Cells["B1"].GetStyle();
style. IsLocked = true;
sheet.Cells["B1"].SetStyle(style);

style = sheet.Cells["C1"].GetStyle();
style. IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
```

## Steg 8: Skydda kalkylbladet

Slutligen kommer vi att skydda kalkylbladet för att förhindra att specifika celler ändras. Använd följande kod:

```csharp
// Skydda arbetsbladet.
sheet.Protect(ProtectionType.All);
```

## Steg 9: Spara Excel-filen

Vi kommer nu att spara den modifierade Excel-filen. Använd följande kod:

```csharp
// Spara Excel-filen.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Se till att ange rätt sökväg för att spara den modifierade Excel-filen.

### Exempel på källkod för att skydda specifika celler i ett Excel-kalkylblad med Aspose.Cells för .NET 
```csharp
//Sökvägen till dokumentkatalogen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Skapa katalog om den inte redan finns.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Skapa en ny arbetsbok.
Workbook wb = new Workbook();
// Skapa ett kalkylbladsobjekt och få det första arket.
Worksheet sheet = wb.Worksheets[0];
// Definiera stilobjektet.
Style style;
// Definiera styleflag-objektet
StyleFlag styleflag;
// Gå igenom alla kolumner i kalkylbladet och lås upp dem.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    styleflag = new StyleFlag();
    styleflag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, styleflag);
}
// Lås de tre cellerna... dvs A1, B1, C1.
style = sheet.Cells["A1"].GetStyle();
style.IsLocked = true;
sheet.Cells["A1"].SetStyle(style);
style = sheet.Cells["B1"].GetStyle();
style.IsLocked = true;
sheet.Cells["B1"].SetStyle(style);
style = sheet.Cells["C1"].GetStyle();
style.IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
// Slutligen, Skydda arket nu.
sheet.Protect(ProtectionType.All);
// Spara excel-filen.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```


## Slutsats

Grattis! Du har nu C#-källkod som låter dig skydda specifika celler i ett Excel-kalkylblad med Aspose.Cells-biblioteket för .NET. Skräddarsy gärna koden för att passa dina specifika behov.

### Vanliga frågor (vanliga frågor)

#### Fungerar den här koden med de senaste versionerna av Excel?

Ja, den här koden fungerar med de senaste versionerna av Excel, inklusive filer i Excel 2010 och högre format.

#### Kan jag skydda andra celler förutom A1, B1 och C1?

Ja, du kan ändra koden för att låsa andra specifika celler genom att justera cellreferenserna i motsvarande kodrader.

#### Hur kan jag låsa upp låsta celler igen?

 Du kan använda`SetStyle` metod med`IsLocked` satt till`false` för att låsa upp celler.

#### Kan jag lägga till fler arbetsblad i arbetsboken?

 Ja, du kan lägga till andra kalkylblad till arbetsboken med hjälp av`Worksheets.Add()`metod och upprepa cellskyddsstegen för varje kalkylblad.

#### Hur kan jag ändra lagringsformatet för Excel-filen?

 Du kan ändra sparformatet med hjälp av`SaveFormat` metod med önskat format, till exempel`SaveFormat.Xlsx` för Excel 2007 och senare.