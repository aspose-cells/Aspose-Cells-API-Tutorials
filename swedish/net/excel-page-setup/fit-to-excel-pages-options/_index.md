---
title: Alternativ för Anpassa till Excel-sidor
linktitle: Alternativ för Anpassa till Excel-sidor
second_title: Aspose.Cells för .NET API-referens
description: Lär dig hur du automatiskt anpassar sidor i ett Excel-kalkylblad med Aspose.Cells för .NET.
type: docs
weight: 30
url: /sv/net/excel-page-setup/fit-to-excel-pages-options/
---
I den här artikeln tar vi dig steg för steg för att förklara följande C#-källkod: Anpassa till Excel Pages-alternativ med Aspose.Cells för .NET. Vi kommer att använda Aspose.Cells-biblioteket för .NET för att utföra denna operation. Följ stegen nedan för att konfigurera anpassning till sidor i Excel.

## Steg 1: Skapa en arbetsbok
Det första steget är att skapa en arbetsbok. Vi kommer att instansiera ett Workbook-objekt. Här är koden för att skapa en arbetsbok:

```csharp
// Sökvägen till dokumentkatalogen
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Instantiera ett arbetsboksobjekt
Workbook workbook = new Workbook();
```

## Steg 2: Åtkomst till kalkylbladet
Nu när vi har skapat arbetsboken måste vi navigera till det första kalkylbladet. Vi kommer att använda index 0 för att komma åt det första arket. Här är koden för att komma åt den:

```csharp
// Tillgång till det första kalkylbladet i arbetsboken
Worksheet worksheet = workbook.Worksheets[0];
```

## Steg 3: Ställ in Anpassa till sidor
 I det här steget kommer vi att konfigurera justeringen till sidorna i kalkylbladet. Vi kommer att använda`FitToPagesTall` och`FitToPagesWide` egenskaper hos`PageSetup` objekt för att ange önskat antal sidor för kalkylbladets höjd och bredd. Här är koden för det:

```csharp
// Konfigurera antalet sidor för höjden på kalkylbladet
worksheet.PageSetup.FitToPagesTall = 1;

// Konfigurera antalet sidor för bredden på kalkylbladet
worksheet.PageSetup.FitToPagesWide = 1;
```

## Steg 4: Spara arbetsboken
 Nu när vi har konfigurerat passform till sidor kan vi spara arbetsboken. Vi kommer att använda`Save` metod för Workbook-objektet för detta. Här är koden för att spara arbetsboken:

```csharp
// Spara arbetsboken
workbook.Save(dataDir + "FitToPagesOptions_out.xls");
```

### Exempel på källkod för Fit To Excel Pages-alternativ med Aspose.Cells för .NET 
```csharp
// Sökvägen till dokumentkatalogen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instantiera ett arbetsboksobjekt
Workbook workbook = new Workbook();
// Åtkomst till det första kalkylbladet i Excel-filen
Worksheet worksheet = workbook.Worksheets[0];
// Ställa in antalet sidor som längden på kalkylbladet ska sträckas över
worksheet.PageSetup.FitToPagesTall = 1;
//Ställa in antalet sidor som kalkylbladets bredd ska sträckas över
worksheet.PageSetup.FitToPagesWide = 1;
// Spara arbetsboken.
workbook.Save(dataDir + "FitToPagesOptions_out.xls");
```

## Slutsats
I den här artikeln lärde vi oss hur man konfigurerar anpassning till sidor i Excel med Aspose.Cells för .NET. Vi gick igenom följande steg: skapa arbetsboken, komma åt kalkylbladet, konfigurera passform till sidor och spara arbetsboken. Nu kan du använda denna kunskap för att anpassa dina kalkylblad till önskade sidor.

### Vanliga frågor

F: Hur kan jag installera Aspose.Cells för .NET?

S: För att installera Aspose.Cells för .NET kan du använda NuGet-pakethanteraren i Visual Studio. Hitta paketet "Aspose.Cells" och installera det i ditt projekt.

F: Kan jag passa sidor både i höjd och bredd?

 S: Ja, du kan justera både höjd och bredd på kalkylbladet med hjälp av`FitToPagesTall` och`FitToPagesWide` egenskaper. Du kan ange önskat antal sidor för varje dimension.

F: Hur kan jag anpassa alternativen Anpassa till sidor?

S: Förutom att ange antalet sidor kan du även anpassa andra alternativ för passning till sidor som kalkylbladsskala, pappersorientering, marginaler och mer. Använd de egenskaper som finns tillgängliga i`PageSetup` objekt för detta.

F: Kan jag använda Aspose.Cells för .NET för att bearbeta befintliga arbetsböcker?

S: Ja, du kan använda Aspose.Cells för .NET för att öppna och redigera befintliga arbetsböcker. Du kan komma åt kalkylblad, celler, formler, stilar och andra arbetsboksobjekt för att utföra olika operationer.