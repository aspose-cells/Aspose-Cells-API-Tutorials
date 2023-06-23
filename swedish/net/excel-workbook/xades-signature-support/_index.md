---
title: Xades Signature Support
linktitle: Xades Signature Support
second_title: Aspose.Cells för .NET API-referens
description: Lär dig hur du lägger till en Xades-signatur i en Excel-fil med Aspose.Cells för .NET.
type: docs
weight: 190
url: /sv/net/excel-workbook/xades-signature-support/
---
den här artikeln tar vi dig steg för steg för att förklara C#-källkoden nedan, som handlar om Xades-signaturstöd som använder Aspose.Cells-biblioteket för .NET. Du kommer att få reda på hur du använder det här biblioteket för att lägga till en Xades digital signatur i en Excel-fil. Vi kommer också att ge dig en översikt över signeringsprocessen och dess genomförande. Följ stegen nedan för att få avgörande resultat.

## Steg 1: Definiera käll- och utdatakataloger
Till att börja med måste vi definiera käll- och utdatakatalogerna i vår kod. Dessa kataloger anger var källfilerna finns och var utdatafilen kommer att sparas. Här är motsvarande kod:

```csharp
// Källkatalog
string sourceDir = RunExamples.Get_SourceDirectory();
// Utdatakatalog
string outputDir = RunExamples.Get_OutputDirectory();
```

Se till att anpassa katalogsökvägarna efter behov.

## Steg 2: Laddar Excel-arbetsboken
Nästa steg är att ladda Excel-arbetsboken som vi vill lägga till Xades digitala signatur på. Här är koden för att ladda arbetsboken:

```csharp
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
```

Se till att ange källfilens namn korrekt i koden.

## Steg 3: Konfigurera den digitala signaturen
Nu kommer vi att konfigurera Xades digitala signatur genom att tillhandahålla nödvändig information. Vi måste ange PFX-filen som innehåller det digitala certifikatet, samt tillhörande lösenord. Här är motsvarande kod:

```csharp
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
```

Se till att ersätta "pfxPassword" med ditt faktiska lösenord och "pfxFile" med sökvägen till PFX-filen.

## Steg 4: Lägga till den digitala signaturen
Nu när vi har konfigurerat den digitala signaturen kan vi lägga till den i Excel-arbetsboken. Här är motsvarande kod:

```csharp
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
```

Detta steg lägger till Xades digitala signatur i Excel-arbetsboken.

## Steg 5: Spara arbetsboken med signaturen
Slutligen sparar vi Excel-arbetsboken med den digitala signaturen tillagd. Här är motsvarande kod:

```csharp
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
```

Se till att anpassa namnet på utdatafilen efter dina behov.

### Exempel på källkod för Xades Signature Support med Aspose.Cells för .NET 
```csharp
//Källkatalog
string sourceDir = RunExamples.Get_SourceDirectory();
//Utdatakatalog
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
Console.WriteLine("XAdESSignatureSupport executed successfully.");
```

## Slutsats
Grattis! Du har lärt dig hur du använder Aspose.Cells-biblioteket för .NET för att lägga till en Xades digital signatur till en Excel-fil. Genom att följa stegen i den här artikeln kommer du att kunna implementera den här funktionen i dina egna projekt. Experimentera gärna mer med biblioteket och upptäck andra kraftfulla funktioner som det erbjuder.

### Vanliga frågor

#### F: Vad är Xades?

S: Xades är en avancerad elektronisk signaturstandard som används för att säkerställa integriteten och äktheten hos digitala dokument.

#### F: Kan jag använda andra typer av digitala signaturer med Aspose.Cells?

S: Ja, Aspose.Cells stöder även andra typer av digitala signaturer, som XMLDSig-signaturer och PKCS#7-signaturer.

#### F: Kan jag använda en signatur på andra filtyper än Excel-filer?
 
S: Ja, Aspose.Cells tillåter även tillämpning av digitala signaturer på andra filtyper som stöds såsom Word-, PDF- och PowerPoint-filer.