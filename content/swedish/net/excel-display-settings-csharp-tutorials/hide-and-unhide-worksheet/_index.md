---
title: Dölj och visa arbetsblad
linktitle: Dölj och visa arbetsblad
second_title: Aspose.Cells för .NET API-referens
description: Ett kraftfullt bibliotek för att arbeta med Excel-filer, inklusive att skapa, ändra och manipulera data.
type: docs
weight: 90
url: /sv/net/excel-display-settings-csharp-tutorials/hide-and-unhide-worksheet/
---
I den här handledningen tar vi dig steg för steg för att förklara följande C#-källkod som används för att dölja och visa ett kalkylblad med Aspose.Cells för .NET. Följ stegen nedan:

## Steg 1: Förbered miljön

Innan du börjar, se till att du har Aspose.Cells för .NET installerat på ditt system. Om du inte redan har det installerat kan du ladda ner det från Asposes officiella hemsida. När det är installerat kan du skapa ett nytt projekt i din föredragna integrerade utvecklingsmiljö (IDE).

## Steg 2: Importera nödvändiga namnrymder

Lägg till de nödvändiga namnområdena i din C#-källfil för att använda funktionerna i Aspose.Cells. Lägg till följande rader i början av filen:

```csharp
using Aspose.Cells;
using System.IO;
```

## Steg 3: Ladda Excel-filen

Innan du döljer eller visar ett kalkylblad måste du ladda Excel-filen i din applikation. Se till att du har Excel-filen du vill använda i samma katalog som ditt projekt. Använd följande kod för att ladda Excel-filen:

```csharp
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

Var noga med att ersätta "SÖG TILL DIN DOKUMENTKATOLOG" med den faktiska sökvägen till katalogen som innehåller din Excel-fil.

## Steg 4: Öppna kalkylarket

När Excel-filen har laddats kan du navigera till det kalkylblad du vill dölja eller visa. Använd följande kod för att komma åt det första kalkylbladet i filen:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Steg 5: Göm kalkylbladet

 Nu när du har öppnat kalkylbladet kan du dölja det med hjälp av`IsVisible` fast egendom. Använd följande kod för att dölja det första kalkylbladet i filen:

```csharp
worksheet. IsVisible = false;
```

## Steg 6: Visa arbetsbladet igen

Om du vill visa det tidigare dolda kalkylbladet igen kan du använda samma kod genom att ändra värdet på`IsVisible` fast egendom. Använd följande kod för att visa det första kalkylbladet igen:

```csharp
worksheet. IsVisible = true;
```

## Steg 7: Spara ändringar

När du

  har gömt eller visat kalkylbladet efter behov, måste du spara ändringarna i Excel-filen. Använd följande kod för att spara ändringar:

```csharp
workbook.Save(dataDir + "output.out.xls");
fstream.Close();
```

Se till att ange rätt utdatasökväg för att spara den modifierade Excel-filen.

### Exempel på källkod för Hide And Unhide Worksheet med Aspose.Cells för .NET 

```csharp
//Sökvägen till dokumentkatalogen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Skapa en filström som innehåller Excel-filen som ska öppnas
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Instantiera ett arbetsboksobjekt genom att öppna Excel-filen genom filströmmen
Workbook workbook = new Workbook(fstream);
// Åtkomst till det första kalkylbladet i Excel-filen
Worksheet worksheet = workbook.Worksheets[0];
// Döljer det första kalkylbladet i Excel-filen
worksheet.IsVisible = false;
// Visar det första kalkylbladet i Excel-filen
//Worksheet.IsVisible = sant;
// Sparar den modifierade Excel-filen i standardformat (det vill säga Excel 2003).
workbook.Save(dataDir + "output.out.xls");
// Stänger filströmmen för att frigöra alla resurser
fstream.Close();
```

## Slutsats

Grattis! Du har lärt dig hur du döljer och visar ett kalkylblad med Aspose.Cells för .NET. Du kan nu använda den här funktionen för att kontrollera synligheten för dina kalkylblad i dina Excel-filer.

### Vanliga frågor (FAQ)

#### Hur kan jag installera Aspose.Cells för .NET?

 Du kan installera Aspose.Cells för .NET genom att ladda ner det relevanta NuGet-paketet från[Aspose släpper](https://releases/aspose.com/cells/net/) och lägga till det i ditt Visual Studio-projekt.

#### Vilken är den minsta nödvändiga versionen av .NET Framework för att använda Aspose.Cells för .NET?

Aspose.Cells för .NET stöder .NET Framework 2.0 och senare.

#### Kan jag öppna och redigera befintliga Excel-filer med Aspose.Cells för .NET?

Ja, du kan öppna och redigera befintliga Excel-filer med Aspose.Cells för .NET. Du kan komma åt kalkylblad, celler, formler och andra delar av Excel-filen.

#### Stöder Aspose.Cells for .NET rapportering och export till andra filformat?

Ja, Aspose.Cells för .NET stöder rapportgenerering och export till format som PDF, HTML, CSV, TXT, etc.

#### Är ändringen av Excel-filen permanent?

Ja, redigeringen av Excel-filen är permanent när du har sparat den. Se till att spara en säkerhetskopia innan du gör några ändringar i originalfilen.