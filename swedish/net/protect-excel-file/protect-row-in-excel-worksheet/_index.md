---
title: Skydda rad i Excel-kalkylblad
linktitle: Skydda rad i Excel-kalkylblad
second_title: Aspose.Cells för .NET API-referens
description: Upptäck i denna handledning hur du skyddar raderna i ett Excel-kalkylblad med Aspose.Cells för .NET. Steg för steg handledning i C#.
type: docs
weight: 60
url: /sv/net/protect-excel-file/protect-row-in-excel-worksheet/
---
I den här handledningen ska vi titta på en del C#-källkod som använder Aspose.Cells-biblioteket för att skydda rader i ett Excel-kalkylblad. Vi går igenom varje steg i koden och förklarar hur det fungerar. Följ instruktionerna noggrant för att få önskat resultat.

## Steg 1: Förutsättningar

Innan du börjar, se till att du har installerat Aspose.Cells-biblioteket för .NET. Du kan få det från Asposes officiella hemsida. Se också till att du har en senaste version av Visual Studio eller någon annan C#-utvecklingsmiljö.

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

I det här steget kommer vi att definiera stilen som ska tillämpas på raderna i kalkylarket. Använd följande kod:

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

## Steg 7: Låsa den första raden

I det här steget kommer vi att låsa den första raden i kalkylbladet. Använd följande kod:

```csharp
// Få stilen på den första raden.
style = sheet.Cells.Rows[0].Style;
// Lås stilen.
style. IsLocked = true;
// Applicera stilen på den första raden.
sheet.Cells.ApplyRowStyle(0, style);
```

## Steg 8: Skydda kalkylbladet

Nu när vi har ställt in stilarna och låst raderna, låt oss skydda kalkylarket. Använd följande kod:

```csharp
// Skydda arbetsbladet.
sheet.Protect(ProtectionType.All);
```

## Steg 9: Spara Excel-filen

Slutligen kommer vi att spara den modifierade Excel-filen. Använd följande kod:

```csharp
// Spara Excel-filen.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Se till att ange rätt sökväg för att spara den modifierade Excel-filen.

### Exempel på källkod för Protect Row In Excel-arbetsblad med Aspose.Cells för .NET 
```csharp
// Sökvägen till dokumentkatalogen.
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
// Definiera styleflag-objektet.
StyleFlag flag;
// Gå igenom alla kolumner i kalkylbladet och lås upp dem.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    flag = new StyleFlag();
    flag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
// Få den första radens stil.
style = sheet.Cells.Rows[0].Style;
// Lås den.
style.IsLocked = true;
//Instantiera flaggan.
flag = new StyleFlag();
// Ställ in låsinställningen.
flag.Locked = true;
// Applicera stilen på den första raden.
sheet.Cells.ApplyRowStyle(0, style, flag);
// Skydda arket.
sheet.Protect(ProtectionType.All);
// Spara excel-filen.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## Slutsats

Grattis! Du har nu C#-källkod som låter dig skydda rader i ett Excel-kalkylblad med hjälp av Aspose.Cells-biblioteket för .NET. Se till att följa stegen noggrant och anpassa koden efter dina specifika behov.

### Vanliga frågor (vanliga frågor)

#### Fungerar den här koden med de senaste versionerna av Excel?

Ja, den här koden fungerar med de senaste versionerna av Excel, inklusive filer i Excel 2010 och högre format.

#### Kan jag skydda endast specifika rader istället för alla rader i kalkylbladet?

Ja, du kan ändra koden för att specificera de specifika raderna du vill skydda. Du måste justera loopen och indexen därefter.

#### Hur kan jag låsa upp låsta linjer igen?

 Du kan använda`IsLocked` metod för`Style` objekt att ställa in värdet på`false` och lås upp raderna.

#### Är det möjligt att skydda flera kalkylblad i samma Excel-arbetsbok?

Ja, du kan upprepa stegen att skapa ett kalkylblad, ställa in stilen och skydda för varje kalkylblad i arbetsboken.

#### Hur kan jag ändra lösenordet för kalkylbladsskydd?

 Du kan ändra lösenordet med hjälp av`Protect` metod och ange ett nytt lösenord som ett argument.