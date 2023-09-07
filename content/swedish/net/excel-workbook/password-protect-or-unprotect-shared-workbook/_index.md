---
title: Lösenordsskydda eller avskydda delad arbetsbok
linktitle: Lösenordsskydda eller avskydda delad arbetsbok
second_title: Aspose.Cells för .NET API-referens
description: Lär dig hur du lösenordsskyddar eller avskyddar en delad arbetsbok med Aspose.Cells för .NET.
type: docs
weight: 120
url: /sv/net/excel-workbook/password-protect-or-unprotect-shared-workbook/
---
Att skydda en delad arbetsbok med ett lösenord är viktigt för att säkerställa datasekretess. Med Aspose.Cells för .NET kan du enkelt skydda eller avskydda en delad arbetsbok med lösenord. Följ stegen nedan för att få önskat resultat:

## Steg 1: Ange utdatakatalog

Först måste du ange utdatakatalogen där den skyddade Excel-filen ska sparas. Så här gör du med Aspose.Cells:

```csharp
// Utdatakatalog
string outputDir = RunExamples.Get_OutputDirectory();
```

## Steg 2: Skapa en tom Excel-fil

Sedan kan du skapa en tom Excel-fil som du vill tillämpa skydd eller avskydd på. Här är en exempelkod:

```csharp
// Skapa en tom Excel-arbetsbok
Workbook wb = new Workbook();
```

## Steg 3: Skydda eller avskydda den delade arbetsboken

När du har skapat arbetsboken kan du skydda eller avskydda den delade arbetsboken genom att ange lämpligt lösenord. Här är hur:

```csharp
// Skydda den delade arbetsboken med ett lösenord
wb.ProtectSharedWorkbook("1234");

// Avkommentera den här raden för att avskydda den delade arbetsboken
// wb.UnprotectSharedWorkbook("1234");
```

## Steg 4: Spara den utgående Excel-filen

När du har tillämpat skydd eller avskydd kan du spara den skyddade Excel-filen i den angivna utdatakatalogen. Så här gör du:

```csharp
// Spara den utgående Excel-filen
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

### Exempel på källkod för Lösenordsskydda eller avskydda delad arbetsbok med Aspose.Cells för .NET 
```csharp
//Utdatakatalog
string outputDir = RunExamples.Get_OutputDirectory();
//Skapa en tom Excel-fil
Workbook wb = new Workbook();
//Skydda den delade arbetsboken med lösenord
wb.ProtectSharedWorkbook("1234");
//Avkommentera den här raden för att ta bort skyddet för den delade arbetsboken
//wb.UnprotectSharedWorkbook("1234");
//Spara den utgående Excel-filen
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

## Slutsats

Att skydda eller avskydda en delad arbetsbok med ett lösenord är viktigt för att säkerställa datasäkerheten. Med Aspose.Cells för .NET kan du enkelt lägga till denna funktion i dina Excel-filer. Genom att följa stegen i den här guiden kan du effektivt skydda eller avskydda dina delade arbetsböcker med hjälp av lösenord. Experimentera med dina egna Excel-filer och se till att upprätthålla säkerheten för dina känsliga data.

### Vanliga frågor

#### F: Vilka typer av skydd kan jag tillämpa på en arbetsbok som delas med Aspose.Cells?
    
S: Med Aspose.Cells kan du skydda en delad arbetsbok genom att ange ett lösenord för att förhindra obehörig åtkomst, modifiering eller radering av data.

#### F: Kan jag skydda en delad arbetsbok utan att ange ett lösenord?
    
S: Ja, du kan skydda en delad arbetsbok utan att ange ett lösenord. Det rekommenderas dock att använda ett starkt lösenord för bättre säkerhet.

#### F: Hur kan jag avskydda en arbetsbok som delas med Aspose.Cells?
    
S: För att ta bort skyddet för en delad arbetsbok måste du ange samma lösenord som användes när du skyddade arbetsboken. Detta gör att skyddet kan tas bort och data kan kommas åt fritt.

#### F: Påverkar skyddet av en delad arbetsbok funktionerna och formlerna i arbetsboken?
    
S: När du skyddar en delad arbetsbok kan användare fortfarande komma åt funktioner och formler som finns i arbetsboken. Skydd påverkar endast strukturella ändringar i arbetsboken.