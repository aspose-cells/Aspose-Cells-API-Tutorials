---
title: Ställ in sidordning i Excel
linktitle: Ställ in sidordning i Excel
second_title: Aspose.Cells för .NET API-referens
description: Steg för steg guide för att ställa in sidordning i Excel med Aspose.Cells för .NET. Detaljerade instruktioner och källkod ingår.
type: docs
weight: 120
url: /sv/net/excel-page-setup/set-excel-page-order/
---
den här artikeln kommer vi att guida dig steg för steg för att förklara följande C#-källkod för att ställa in sidordning i Excel med Aspose.Cells för .NET. Vi visar dig hur du ställer in dokumentkatalogen, instansierar ett Workbook-objekt, hämtar PageSetup-referensen, ställer in sidutskriftsordningen och sparar arbetsboken.

## Steg 1: Installation av dokumentkatalog

 Innan du börjar måste du konfigurera dokumentkatalogen där du vill spara Excel-filen. Du kan ange katalogsökvägen genom att ersätta värdet på`dataDir` variabel med din egen väg.

```csharp
// Sökvägen till dokumentkatalogen.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

## Steg 2: Instantiera ett arbetsboksobjekt

Det första steget är att instansiera ett arbetsboksobjekt. Detta representerar Excel-arbetsboken vi kommer att arbeta med.

```csharp
// Instantiera ett arbetsboksobjekt
Workbook workbook = new Workbook();
```

## Steg 3: Skaffa referensen för PageSetup

Därefter måste vi hämta PageSetup-objektreferensen för det kalkylblad som vi vill ställa in sidordningen på.

```csharp
// Skaffa kalkylbladets PageSetup-referens
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## Steg 4: Ställa in utskriftsordningen för sidor

Nu kan vi ställa in utskriftsordningen för sidorna. I det här exemplet använder vi alternativet "OverThenDown", vilket innebär att sidorna kommer att skrivas ut från vänster till höger, sedan uppifrån och ned.

```csharp
// Ställ in sidutskriftsordningen till "OverThenDown"
pageSetup.Order = PrintOrderType.OverThenDown;
```

## Steg 5: Spara arbetsboken

Slutligen sparar vi Excel-arbetsboken med sidordningsändringarna.

```csharp
// Spara arbetsboken
workbook.Save(dataDir + "SetPageOrder_out.xls");
```

### Exempel på källkod för Set Excel Page Order med Aspose.Cells för .NET 
```csharp
// Sökvägen till dokumentkatalogen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instantiera ett arbetsboksobjekt
Workbook workbook = new Workbook();
// Få referensen till kalkylbladets PageSetup
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Ställer in utskriftsordningen för sidorna till över och nedåt
pageSetup.Order = PrintOrderType.OverThenDown;
// Spara arbetsboken.
workbook.Save(dataDir + "SetPageOrder_out.xls");
```

## Slutsats

I den här handledningen förklarade vi hur man ställer in sidordning i en Excel-fil med Aspose.Cells för .NET. Genom att följa de angivna stegen kan du enkelt konfigurera dokumentkatalogen, instansiera ett arbetsboksobjekt, hämta PageSetup-referensen, ställa in sidutskriftsordningen och spara arbetsboken.

### FAQ's

#### F1: Varför är det viktigt att ställa in sidordning i en Excel-fil?

Att definiera ordningen på sidorna i en Excel-fil är viktigt eftersom det avgör hur sidorna ska skrivas ut eller visas. Genom att ange en specifik ordning kan du organisera data logiskt och göra filen lättare att läsa eller skriva ut.

#### F2: Kan jag använda andra sidutskriftsbeställningar med Aspose.Cells för .NET?

Ja, Aspose.Cells för .NET stöder utskrift av flera sidor som "DownThenOver", "OverThenDown", "DownThenOverThenDownAgain", etc. Du kan välja den som bäst passar dina behov.

#### F3: Kan jag ställa in ytterligare alternativ för utskrift av sidor med Aspose.Cells för .NET?

Ja, du kan ställa in olika alternativ för sidutskrift som skala, orientering, marginaler etc., med hjälp av egenskaperna för objektet PageSetup i Aspose.Cells för .NET.

#### F4: Stöder Aspose.Cells for .NET andra Excel-filformat?

Ja, Aspose.Cells för .NET stöder ett brett utbud av Excel-filformat som XLSX, XLS, CSV, HTML, PDF, etc. Du kan enkelt konvertera mellan dessa format med hjälp av funktionerna i biblioteket.