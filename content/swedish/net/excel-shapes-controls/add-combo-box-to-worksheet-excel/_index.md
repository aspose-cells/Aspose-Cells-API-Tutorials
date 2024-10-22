---
title: Lägg till kombinationsruta till kalkylblad i Excel
linktitle: Lägg till kombinationsruta till kalkylblad i Excel
second_title: Aspose.Cells .NET Excel Processing API
description: Lär dig hur du lägger till en kombinationsruta i ett Excel-kalkylblad programmatiskt med Aspose.Cells för .NET. Denna steg-för-steg guide leder dig genom varje detalj.
type: docs
weight: 21
url: /sv/net/excel-shapes-controls/add-combo-box-to-worksheet-excel/
---
## Introduktion
Att skapa interaktiva Excel-kalkylblad kan förbättra användarupplevelsen avsevärt, särskilt när du lägger till formulärelement som kombinationsrutor. Kombinationsrutor låter användare välja alternativ från en fördefinierad lista, vilket gör datainmatningen lätt och effektiv. Med Aspose.Cells för .NET kan du programmässigt skapa kombinationsrutor i Excel-ark utan att använda Excel direkt. Detta kraftfulla bibliotek låter utvecklare manipulera Excel-filer på olika sätt, inklusive möjligheten att automatisera formulärkontroller.
I den här handledningen går vi igenom processen att lägga till en kombinationsruta i ett kalkylblad i Excel med Aspose.Cells för .NET. Om du funderar på att bygga dynamiska, användarvänliga kalkylblad hjälper den här guiden dig att komma igång.
## Förutsättningar
Innan vi dyker in i koden, låt oss se till att du har allt du behöver:
- Aspose.Cells for .NET: Ladda ner och installera Aspose.Cells for .NET-biblioteket från[nedladdningssida](https://releases.aspose.com/cells/net/).
- .NET Framework: Se till att du har .NET Framework installerat på din dator. Alla versioner som stöds av Aspose.Cells kommer att fungera.
- Utvecklingsmiljö: Använd en IDE som Visual Studio för att hantera ditt projekt och skriva kod.
-  Aspose-licens: Du kan arbeta utan licens i utvärderingsläge, men för en fullständig version måste du ansöka om en licens. Skaffa en[tillfällig licens](https://purchase.aspose.com/temporary-license/) om det behövs.
## Importera paket
För att komma igång måste du importera de nödvändiga namnrymden till ditt projekt. Här är vad du behöver:
```csharp
using System.IO;
using Aspose.Cells;
```
Dessa är viktiga för att interagera med Excel-filer och manipulera formulärelement som kombinationsrutor i arbetsboken.
Låt oss dela upp processen med att lägga till en kombinationsruta i flera enkla steg för enkel förståelse.
## Steg 1: Konfigurera dokumentkatalogen
Det första steget är att skapa en katalog där dina Excel-filer kommer att sparas. Du kan skapa en ny mapp om den inte redan finns.
```csharp
// Sökvägen till dokumentkatalogen.
string dataDir = "Your Document Directory";
//Skapa katalog om den inte redan finns.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
```
- dataDir: Anger platsen där utdatafilen ska sparas.
- System.IO.Directory.Exists: Kontrollerar om katalogen redan finns.
- System.IO.Directory.CreateDirectory: Skapar katalogen om den saknas.
## Steg 2: Skapa en ny arbetsbok
Skapa nu en ny Excel-arbetsbok där du lägger till kombinationsrutan.

```csharp
// Skapa en ny arbetsbok.
Workbook workbook = new Workbook();
```

- Arbetsbok arbetsbok: Initierar en ny instans av klassen Workbook, som representerar en Excel-fil.
## Steg 3: Hämta kalkylbladet och cellerna
Gå sedan till det första kalkylbladet från arbetsboken och hämta cellsamlingen där du ska mata in data.

```csharp
// Skaffa det första arbetsbladet.
Worksheet sheet = workbook.Worksheets[0];
// Hämta samlingen av kalkylbladsceller.
Cells cells = sheet.Cells;
```

- Kalkylblad: Hämtar det första kalkylbladet från arbetsboken.
- Celler celler: Hämtar samlingen av celler från kalkylbladet.
## Steg 4: Inmatningsvärden för kombinationsrutan
Nu måste vi mata in några värden i cellerna. Dessa värden kommer att fungera som alternativ för kombinationsrutan.

```csharp
// Ange ett värde.
cells["B3"].PutValue("Employee:");
// Sätt den i fet stil.
cells["B3"].GetStyle().Font.IsBold = true;
// Mata in några värden som anger inmatningsintervallet för kombinationsrutan.
cells["A2"].PutValue("Emp001");
cells["A3"].PutValue("Emp002");
cells["A4"].PutValue("Emp003");
cells["A5"].PutValue("Emp004");
cells["A6"].PutValue("Emp005");
cells["A7"].PutValue("Emp006");
```

- celler["B3"].PutValue: Placerar etiketten "Anställd" i cell B3.
- Font.IsBold = true: Ställer in texten till fetstil så att den sticker ut.
- Inmatningsområde: Matar in flera medarbetar-ID:n i cellerna A2 till A7. Dessa kommer att visas i rullgardinsmenyn i kombinationsrutan.
## Steg 5: Lägg till kombinationsrutan i arbetsbladet
Nästa steg är att lägga till kombinationsrutekontrollen till ditt kalkylblad. Den här kombinationsrutan låter användare välja ett av de anställda ID:n du angav tidigare.

```csharp
// Lägg till en ny kombinationsruta.
Aspose.Cells.Drawing.ComboBox comboBox = sheet.Shapes.AddComboBox(2, 0, 2, 0, 22, 100);
```

- AddComboBox: Lägger till en ny kombinationsruta i kalkylbladet. Siffrorna (2, 0, 2, 0, 22, 100) representerar kombinationsrutans position och dimensioner.
## Steg 6: Länka kombinationsrutan till en cell och ställ in inmatningsintervallet
För att göra kombinationsrutan funktionell måste vi länka den till en specifik cell och definiera intervallet av celler som den kommer att hämta sina alternativ från.

```csharp
// Ställ in den länkade cellen.
comboBox.LinkedCell = "A1";
// Ställ in ingångsintervallet.
comboBox.InputRange = "A2:A7";
```

- LinkedCell: Länkar kombinationsrutans val till cell A1. Det valda värdet från kombinationsrutan visas i den här cellen.
- InputRange: Definierar cellintervallet (A2:A7) som innehåller de värden som kommer att fylla i kombinationsrutans alternativ.
## Steg 7: Anpassa kombinationsrutans utseende
Du kan anpassa kombinationsrutan ytterligare genom att ange antalet rullgardinsrader och aktivera 3D-skuggning för bättre estetik.

```csharp
// Set nr. listrader som visas i kombinationsrutans listdel.
comboBox.DropDownLines = 5;
// Ställ in kombinationsrutan med 3D-skuggning.
comboBox.Shadow = true;
```

- DropDownLines: Styr hur många alternativ som ska vara synliga i kombinationsrutan samtidigt.
- Skugga: Lägger till en 3D-skuggningseffekt i kombinationsrutan.
## Steg 8: Anpassa kolumner automatiskt och spara arbetsboken
Slutligen, låt oss automatiskt anpassa kolumnerna för en ren layout och spara arbetsboken.

```csharp
// AutoFit-kolumner
sheet.AutoFitColumns();
// Sparar filen.
workbook.Save(dataDir + "book1.out.xls");
```

- AutoFitColumns: Justerar automatiskt kolumnbredderna för att passa innehållet.
- Spara: Sparar arbetsboken som en Excel-fil i den angivna katalogen.

## Slutsats
Att lägga till en kombinationsruta i dina Excel-kalkylblad med Aspose.Cells för .NET är en enkel process som avsevärt förbättrar flexibiliteten för datainmatning. Genom att programmatiskt skapa formulärkontroller kan du enkelt bygga interaktiva kalkylblad. Denna handledning visade dig hur du lägger till en kombinationsruta, länkar den till en cell och konfigurerar dess inmatningsintervall, allt med Aspose.Cells.
 Aspose.Cells tillhandahåller ett brett utbud av funktioner för Excel-filmanipulering, vilket gör det till ett idealiskt val för utvecklare som vill automatisera kalkylbladsuppgifter. Prova det med en[gratis provperiod](https://releases.aspose.com/).
## FAQ's
### Kan jag använda Aspose.Cells utan att Excel är installerat?
Ja, Aspose.Cells fungerar oberoende av Excel och kräver inte att Excel installeras.
### Hur ansöker jag om en licens i Aspose.Cells?
 Du kan ansöka om en licens genom att skaffa den från[här](https://purchase.aspose.com/buy) och ringer`License.SetLicense()` i din kod.
### Vilka format stöder Aspose.Cells för att spara filer?
Aspose.Cells stöder att spara filer i flera format som XLSX, XLS, CSV, PDF och mer.
### Finns det en gräns för antalet kombinationsrutor jag kan lägga till?
Nej, det finns ingen strikt gräns; du kan lägga till så många kombinationsrutor som ditt projekt kräver.
### Hur får jag support för Aspose.Cells?
 Du kan få stöd från[Aspose forum](https://forum.aspose.com/c/cells/9).