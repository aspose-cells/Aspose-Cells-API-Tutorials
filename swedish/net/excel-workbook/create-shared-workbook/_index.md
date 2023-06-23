---
title: Skapa delad arbetsbok
linktitle: Skapa delad arbetsbok
second_title: Aspose.Cells för .NET API-referens
description: Skapa en Excel-arbetsbok med Aspose.Cells för .NET för att möjliggöra samtidig datasamarbete.
type: docs
weight: 70
url: /sv/net/excel-workbook/create-shared-workbook/
---
den här handledningen går vi igenom den medföljande C#-källkoden som gör att du kan skapa en delad arbetsbok med Aspose.Cells för .NET. Följ stegen nedan för att utföra denna operation.

## Steg 1: Ställ in utdatakatalog

```csharp
// Utdatakatalog
string outputDir = RunExamples.Get_OutputDirectory();
```

I detta första steg definierar vi utdatakatalogen där den delade arbetsboken ska sparas.

## Steg 2: Skapa ett arbetsboksobjekt

```csharp
// Skapa ett arbetsboksobjekt
Workbook wb = new Workbook();
```

Vi skapar ett nytt arbetsboksobjekt som kommer att representera vår Excel-arbetsbok.

## Steg 3: Aktivera delning av arbetsbok

```csharp
// Dela arbetsboken
wb.Settings.Shared = true;
```

 Vi aktiverar arbetsbokens delningsfunktion genom att ställa in`Shared` egenskapen för arbetsbokobjektet till`true`.

## Steg 4: Spara den delade arbetsboken

```csharp
// Spara den delade arbetsboken
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
```

Vi sparar den delade arbetsboken genom att ange sökvägen och namnet på utdatafilen.

### Exempel på källkod för Skapa delad arbetsbok med Aspose.Cells för .NET 
```csharp
//Utdatakatalog
string outputDir = RunExamples.Get_OutputDirectory();
//Skapa arbetsboksobjekt
Workbook wb = new Workbook();
//Dela arbetsboken
wb.Settings.Shared = true;
//Spara den delade arbetsboken
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
Console.WriteLine("CreateSharedWorkbook executed successfully.\r\n");
```

## Slutsats

Grattis! Du lärde dig hur du skapar en delad arbetsbok med Aspose.Cells för .NET. Den delade arbetsboken kan användas av flera användare samtidigt för att samarbeta om data. Experimentera med din egen data och utforska funktionerna i Aspose.Cells ytterligare för att skapa kraftfulla och personliga Excel-arbetsböcker.

### Vanliga frågor

#### F: Vad är en delad arbetsbok?

S: En delad arbetsbok är en Excel-arbetsbok som kan användas samtidigt av flera användare för att samarbeta med data. Varje användare kan göra ändringar i arbetsboken och andra användare kommer att se uppdateringar i realtid.

#### F: Hur aktiverar man delning av en arbetsbok i Aspose.Cells för .NET?

 S: För att möjliggöra delning av en arbetsbok i Aspose.Cells för .NET måste du ställa in`Shared` egenskapen för arbetsbokobjektet till`true`. Detta gör att användare kan arbeta med arbetsboken samtidigt.

#### F: Kan jag begränsa användarbehörigheter i en delad arbetsbok?

S: Ja, du kan begränsa användarbehörigheter i en delad arbetsbok med hjälp av Excels säkerhetsfunktioner. Du kan ställa in specifika behörigheter för varje användare, såsom möjligheten att redigera, endast läs, etc.

#### F: Hur kan jag dela arbetsboken med andra användare?

S: När du har skapat den delade arbetsboken kan du dela den med andra användare genom att skicka Excel-filen till dem. Andra användare kommer att kunna öppna filen och arbeta med den samtidigt.

#### F: Stöds alla Excel-funktioner i en delad arbetsbok?

S: De flesta Excel-funktioner stöds i en delad arbetsbok. Vissa avancerade funktioner, såsom makron och tillägg, kan dock ha begränsningar eller begränsningar när de används i en delad arbetsbok.