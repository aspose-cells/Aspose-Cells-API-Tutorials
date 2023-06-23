---
title: Läs och skriv extern anslutning av XLSB-fil
linktitle: Läs och skriv extern anslutning av XLSB-fil
second_title: Aspose.Cells för .NET API-referens
description: Lär dig hur du läser och ändrar de externa anslutningarna för en XLSB-fil med Aspose.Cells för .NET.
type: docs
weight: 130
url: /sv/net/excel-workbook/read-and-write-external-connection-of-xlsb-file/
---
Att läsa och skriva externa anslutningar till en XLSB-fil är viktigt för att manipulera data från externa källor i dina Excel-arbetsböcker. Med Aspose.Cells för .NET kan du enkelt läsa och skriva externa anslutningar genom att använda följande steg:

## Steg 1: Ange källkatalog och utdatakatalog

Först måste du ange källkatalogen där XLSB-filen som innehåller den externa anslutningen finns, samt utdatakatalogen där du vill spara den ändrade filen. Så här gör du med Aspose.Cells:

```csharp
// källkatalog
string sourceDir = RunExamples.Get_SourceDirectory();

// Utdatakatalog
string outputDir = RunExamples.Get_OutputDirectory();
```

## Steg 2: Ladda källfilen för Excel XLSB

Därefter måste du ladda källfilen för Excel XLSB som du vill utföra läs- och skrivoperationer för extern anslutning. Här är en exempelkod:

```csharp
// Ladda källfilen för Excel XLSB
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
```

## Steg 3: Läs och ändra den externa anslutningen

Efter att ha laddat filen kan du komma åt den första externa anslutningen som egentligen är en databasanslutning. Du kan läsa och ändra olika egenskaper för den externa anslutningen. Här är hur:

```csharp
// Läs den första externa anslutningen som är en databasanslutning
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;

// Visa databasanslutningens namn, kommando och anslutningsinformation
Console.WriteLine("Connection name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);

// Ändra namnet på anslutningen
dbCon.Name = "NewCustomer";
```

## Steg 4: Spara den utgående Excel XLSB-filen

När du har gjort de nödvändiga ändringarna kan du spara den modifierade Excel XLSB-filen i den angivna utdatakatalogen. Så här gör du:

```csharp
// Spara den utgående Excel XLSB-filen
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

### Exempel på källkod för läs och skriv extern anslutning av XLSB-fil med Aspose.Cells för .NET 
```csharp
//Källkatalog
string sourceDir = RunExamples.Get_SourceDirectory();
//Utdatakatalog
string outputDir = RunExamples.Get_OutputDirectory();
//Ladda källfilen Excel Xlsb
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
//Läs den första externa anslutningen som egentligen är en DB-Anslutning
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;
//Skriv ut namn, kommando och anslutningsinformation för DB-anslutningen
Console.WriteLine("Connection Name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);
//Ändra anslutningsnamnet
dbCon.Name = "NewCust";
//Spara Excel Xlsb-filen
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

## Slutsats

Genom att läsa och skriva externa anslutningar till en XLSB-fil kan du manipulera data från externa källor i dina Excel-arbetsböcker. Med Aspose.Cells för .NET kan du enkelt komma åt externa anslutningar, läsa och ändra anslutningsinformation och spara ändringar. Experimentera med dina egna XLSB-filer och utnyttja kraften i externa anslutningar i dina Excel-program.

### Vanliga frågor

#### F: Vad är en extern anslutning i en XLSB-fil?
    
S: En extern anslutning i en XLSB-fil hänvisar till en anslutning som upprättats med en extern datakälla såsom en databas. Det låter dig importera data från denna externa källa till Excel-arbetsboken.

#### F: Kan jag ha flera externa anslutningar i en XLSB-fil?
     
S: Ja, du kan ha flera externa anslutningar i en XLSB-fil. Du kan hantera dem individuellt genom att komma åt varje anslutningsobjekt.

#### F: Hur kan jag läsa detaljerna för en extern anslutning i en XLSB-fil med Aspose.Cells?
     
S: Du kan använda funktionerna som tillhandahålls av Aspose.Cells för att komma åt egenskaper för en extern anslutning, såsom anslutningsnamn, tillhörande kommando och anslutningsinformation.

#### F: Är det möjligt att modifiera en extern anslutning i en XLSB-fil med Aspose.Cells?
     
S: Ja, du kan ändra egenskaperna för en extern anslutning, till exempel anslutningens namn, för att möta dina specifika behov. Aspose.Cells tillhandahåller metoder för att göra dessa ändringar.

#### F: Hur kan jag spara ändringar som gjorts på en extern anslutning till en XLSB-fil med Aspose.Cells?
     
S: När du har gjort de nödvändiga ändringarna i en extern anslutning kan du helt enkelt spara den modifierade Excel XLSB-filen med hjälp av lämplig metod från Aspose.Cells.