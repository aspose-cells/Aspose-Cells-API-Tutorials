---
title: Lägg till digital signatur till en redan signerad Excel-fil
linktitle: Lägg till digital signatur till en redan signerad Excel-fil
second_title: Aspose.Cells för .NET API-referens
description: Lägg enkelt till digitala signaturer till befintliga Excel-filer med Aspose.Cells för .NET.
type: docs
weight: 30
url: /sv/net/excel-workbook/add-digital-signature-to-an-already-signed-excel-file/
---
I denna steg-för-steg-guide kommer vi att förklara den medföljande C#-källkoden som gör att du kan lägga till en digital signatur till en redan signerad Excel-fil med Aspose.Cells för .NET. Följ stegen nedan för att lägga till en ny digital signatur i en befintlig Excel-fil.

## Steg 1: Ställ in käll- och utdatakataloger

```csharp
// källkatalog
string sourceDir = RunExamples.Get_SourceDirectory();

// Utdatakatalog
string outputDir = RunExamples.Get_OutputDirectory();
```

detta första steg definierar vi käll- och utdatakatalogerna som ska användas för att ladda den befintliga Excel-filen och spara filen med den nya digitala signaturen.

## Steg 2: Ladda befintlig Excel-fil

```csharp
// Ladda den redan signerade Excel-arbetsboken
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
```

 Här laddar vi den redan signerade Excel-filen med hjälp av`Workbook` klass av Aspose.Cells.

## Steg 3: Skapa samlingen av digitala signaturer

```csharp
// Skapa samlingen av digitala signaturer
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
```

 Vi skapar en ny samling av digitala signaturer med hjälp av`DigitalSignatureCollection` klass.

## Steg 4: Skapa ett nytt certifikat

```csharp
// Skapa ett nytt certifikat
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
```

Här skapar vi ett nytt certifikat från den angivna filen och lösenordet.

## Steg 5: Lägg till en ny digital signatur i samlingen

```csharp
// Skapa en ny digital signatur
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added a new digital signature to the already signed workbook.", DateTime.Now);

// Lägg till den digitala signaturen i samlingen
dsCollection.Add(signature);
```

 Vi skapar en ny digital signatur med hjälp av`DigitalSignature` klass och lägg till den i samlingen av digitala signaturer.

## Steg 6: Lägg till samlingen av digitala signaturer i arbetsboken

```csharp
//Lägg till samlingen av digitala signaturer i arbetsboken
workbook.AddDigitalSignature(dsCollection);
```

 Vi lägger till samlingen av digitala signaturer till den befintliga Excel-arbetsboken med hjälp av`AddDigitalSignature()` metod.

## Steg 7: Spara och stäng arbetsboken

```csharp
// Spara arbetsboken och stäng den
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
```

Vi sparar arbetsboken med den nya digitala signaturen till den angivna utdatakatalogen, stänger den sedan och släpper de tillhörande resurserna.

### Exempel på källkod för att lägga till digital signatur till en redan signerad Excel-fil med Aspose.Cells för .NET 
```csharp
//Källkatalog
string sourceDir = RunExamples.Get_SourceDirectory();
//Utdatakatalog
string outputDir = RunExamples.Get_OutputDirectory();
//Certifikatfil och dess lösenord
string certFileName = sourceDir + "AsposeDemo.pfx";
string password = "aspose";
//Ladda arbetsboken som redan är digitalt signerad för att lägga till ny digital signatur
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
//Skapa den digitala signatursamlingen
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
//Skapa nytt certifikat
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
//Skapa ny digital signatur och lägg till den i digital signatursamling
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added new digital signature in existing digitally signed workbook.", DateTime.Now);
dsCollection.Add(signature);
//Lägg till digital signatursamling i arbetsboken
workbook.AddDigitalSignature(dsCollection);
//Spara arbetsboken och kassera den.
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
Console.WriteLine("AddDigitalSignatureToAnAlreadySignedExcelFile executed successfully.\r\n");
```

## Slutsats

Grattis! Du har nu lärt dig hur du lägger till en digital signatur i en redan signerad Excel-fil med Aspose.Cells för .NET. Digitala signaturer lägger till ett extra lager av säkerhet till dina Excel-filer, vilket säkerställer deras autenticitet och integritet.

### Vanliga frågor

#### F: Vad är Aspose.Cells för .NET?

S: Aspose.Cells för .NET är ett kraftfullt klassbibliotek som låter .NET-utvecklare skapa, modifiera, konvertera och manipulera Excel-filer med lätthet.

#### F: Vad är en digital signatur i en Excel-fil?

S: En digital signatur i en Excel-fil är ett elektroniskt märke som garanterar dokumentets äkthet, integritet och ursprung. Den används för att verifiera att filen inte har ändrats sedan den signerades och kommer från en pålitlig källa.

#### F: Vilka är fördelarna med att lägga till en digital signatur i en Excel-fil?

S: Att lägga till en digital signatur i en Excel-fil ger flera fördelar, inklusive skydd mot obehöriga ändringar, säkerställande av dataintegritet, autentisering av författaren till dokumentet och tillhandahållande av förtroende för informationen som den innehåller.

#### F: Kan jag lägga till flera digitala signaturer i en Excel-fil?

S: Ja, Aspose.Cells låter dig lägga till flera digitala signaturer i en Excel-fil. Du kan skapa en samling digitala signaturer och lägga till dem i filen i en operation.

#### F: Vilka är kraven för att lägga till en digital signatur i en Excel-fil?

S: För att lägga till en digital signatur i en Excel-fil behöver du ett giltigt digitalt certifikat som kommer att användas för att signera dokumentet. Se till att du har rätt certifikat och lösenord innan du lägger till den digitala signaturen.