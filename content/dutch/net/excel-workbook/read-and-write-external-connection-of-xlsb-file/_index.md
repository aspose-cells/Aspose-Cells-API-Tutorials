---
title: Lezen en schrijven externe verbinding van XLSB-bestand
linktitle: Lezen en schrijven externe verbinding van XLSB-bestand
second_title: Aspose.Cells voor .NET API-referentie
description: Leer hoe u de externe verbindingen van een XLSB-bestand leest en wijzigt met Aspose.Cells voor .NET.
type: docs
weight: 130
url: /nl/net/excel-workbook/read-and-write-external-connection-of-xlsb-file/
---
Het lezen en schrijven van externe verbindingen naar een XLSB-bestand is essentieel voor het manipuleren van gegevens uit externe bronnen in uw Excel-werkmappen. Met Aspose.Cells voor .NET kunt u eenvoudig externe verbindingen lezen en schrijven met behulp van de volgende stappen:

## Stap 1: Geef de bronmap en de uitvoermap op

Eerst moet u de bronmap opgeven waar het XLSB-bestand met de externe verbinding zich bevindt, evenals de uitvoermap waar u het gewijzigde bestand wilt opslaan. Hier leest u hoe u dit doet met Aspose.Cells:

```csharp
// bronmap
string sourceDir = RunExamples.Get_SourceDirectory();

// Uitvoermap
string outputDir = RunExamples.Get_OutputDirectory();
```

## Stap 2: Laad het Excel XLSB-bronbestand

Vervolgens moet u het Excel XLSB-bronbestand laden waarop u lees- en schrijfbewerkingen voor externe verbindingen wilt uitvoeren. Hier is een voorbeeldcode:

```csharp
// Laad het Excel XLSB-bronbestand
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
```

## Stap 3: Lees en wijzig de externe verbinding

Na het laden van het bestand heeft u toegang tot de eerste externe verbinding, die feitelijk een databaseverbinding is. U kunt diverse eigenschappen van de externe verbinding lezen en wijzigen. Hier is hoe:

```csharp
// Lees de eerste externe verbinding, die een databaseverbinding is
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;

// Geef de databaseverbindingsnaam, opdracht en verbindingsinformatie weer
Console.WriteLine("Connection name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);

// Wijzig de naam van de verbinding
dbCon.Name = "NewCustomer";
```

## Stap 4: Sla het uitgevoerde Excel XLSB-bestand op

Nadat u de nodige wijzigingen heeft aangebracht, kunt u het gewijzigde Excel XLSB-bestand opslaan in de opgegeven uitvoermap. Hier leest u hoe u het moet doen:

```csharp
// Sla het uitvoer Excel XLSB-bestand op
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

### Voorbeeldbroncode voor lezen en schrijven van externe verbinding van XLSB-bestand met Aspose.Cells voor .NET 
```csharp
//Bronmap
string sourceDir = RunExamples.Get_SourceDirectory();
//Uitvoermap
string outputDir = RunExamples.Get_OutputDirectory();
//Laad het bron-Excel Xlsb-bestand
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
//Lees de eerste externe verbinding die eigenlijk een DB-verbinding is
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;
//Druk de naam, opdracht en verbindingsinformatie van de DB-verbinding af
Console.WriteLine("Connection Name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);
//Wijzig de verbindingsnaam
dbCon.Name = "NewCust";
//Sla het Excel Xlsb-bestand op
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

## Conclusie

Door externe verbindingen naar een XLSB-bestand te lezen en te schrijven, kunt u gegevens uit externe bronnen in uw Excel-werkmappen manipuleren. Met Aspose.Cells voor .NET kunt u eenvoudig toegang krijgen tot externe verbindingen, verbindingsinformatie lezen en wijzigen en wijzigingen opslaan. Experimenteer met uw eigen XLSB-bestanden en benut de kracht van externe verbindingen in uw Excel-applicaties.

### Veelgestelde vragen

#### Vraag: Wat is een externe verbinding in een XLSB-bestand?
    
A: Een externe verbinding in een XLSB-bestand verwijst naar een verbinding die tot stand is gebracht met een externe gegevensbron zoals een database. Hiermee kunt u gegevens uit deze externe bron importeren in de Excel-werkmap.

#### Vraag: Kan ik meerdere externe verbindingen in een XLSB-bestand hebben?
     
A: Ja, u kunt meerdere externe verbindingen hebben in een XLSB-bestand. U kunt ze afzonderlijk beheren door elk verbindingsobject te openen.

#### Vraag: Hoe kan ik de details van een externe verbinding in een XLSB-bestand lezen met Aspose.Cells?
     
A: U kunt de functionaliteit van Aspose.Cells gebruiken om toegang te krijgen tot eigenschappen van een externe verbinding, zoals de verbindingsnaam, de bijbehorende opdracht en verbindingsinformatie.

#### Vraag: Is het mogelijk om een externe verbinding in een XLSB-bestand te wijzigen met Aspose.Cells?
     
A: Ja, u kunt de eigenschappen van een externe verbinding, zoals de verbindingsnaam, aanpassen aan uw specifieke behoeften. Aspose.Cells biedt methoden om deze wijzigingen aan te brengen.

#### Vraag: Hoe kan ik wijzigingen in een externe verbinding opslaan in een XLSB-bestand met Aspose.Cells?
     
A: Zodra u de nodige wijzigingen heeft aangebracht aan een externe verbinding, kunt u het gewijzigde Excel XLSB-bestand eenvoudig opslaan met de juiste methode van Aspose.Cells.