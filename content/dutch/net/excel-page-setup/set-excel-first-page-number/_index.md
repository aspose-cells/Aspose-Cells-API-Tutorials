---
title: Stel het eerste paginanummer van Excel in
linktitle: Stel het eerste paginanummer van Excel in
second_title: Aspose.Cells voor .NET API-referentie
description: Leer hoe u het eerste paginanummer in Excel instelt met Aspose.Cells voor .NET.
type: docs
weight: 90
url: /nl/net/excel-page-setup/set-excel-first-page-number/
---
In deze zelfstudie laten we u zien hoe u het eerste paginanummer in Excel instelt met Aspose.Cells voor .NET. We zullen C#-broncode gebruiken om het proces te illustreren.

## Stap 1: De omgeving instellen

Zorg ervoor dat Aspose.Cells voor .NET op uw computer is geïnstalleerd. Maak ook een nieuw project aan in de ontwikkelomgeving van uw voorkeur.

## Stap 2: Importeer de benodigde bibliotheken

Importeer in uw codebestand de bibliotheken die nodig zijn om met Aspose.Cells te werken. Hier is de bijbehorende code:

```csharp
using Aspose.Cells;
```

## Stap 3: Stel de gegevensmap in

Stel de gegevensmap in waar u het gewijzigde Excel-bestand wilt opslaan. Gebruik de volgende code:

```csharp
string dataDir = "YOUR DATA DIRECTORY";
```

Zorg ervoor dat u het volledige mappad opgeeft.

## Stap 4: De werkmap en het werkblad maken

Maak een nieuw werkmapobject en navigeer naar het eerste werkblad in de werkmap met behulp van de volgende code:

```csharp
Workbook workbook = new Workbook();
Worksheet worksheet = workbook.Worksheets[0];
```

Hierdoor wordt een lege werkmap met een werkblad gemaakt.

## Stap 5: Het nummer van de eerste pagina instellen

Stel het nummer van de eerste pagina van de werkbladpagina's in met behulp van de volgende code:

```csharp
worksheet.PageSetup.FirstPageNumber = 2;
```

Hierdoor wordt het eerste paginanummer ingesteld op 2.

## Stap 6: De gewijzigde werkmap opslaan

Sla de gewijzigde werkmap op met behulp van de volgende code:

```csharp
workbook.Save(dataDir + "OutputFileName.xls");
```

Hierdoor wordt de gewijzigde werkmap opgeslagen in de opgegeven gegevensmap.

### Voorbeeldbroncode voor Excel-eerste paginanummer instellen met Aspose.Cells voor .NET 
```csharp
//Het pad naar de documentenmap.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Een werkmapobject instantiëren
Workbook workbook = new Workbook();
// Toegang tot het eerste werkblad in het Excel-bestand
Worksheet worksheet = workbook.Worksheets[0];
// Het eerste paginanummer van de werkbladpagina's instellen
worksheet.PageSetup.FirstPageNumber = 2;
// Sla de werkmap op.
workbook.Save(dataDir + "SetFirstPageNumber_out.xls");
```

## Conclusie

U hebt nu geleerd hoe u het eerste paginanummer in Excel kunt instellen met Aspose.Cells voor .NET. In deze tutorial wordt u door elke stap van het proces geleid, van het instellen van de omgeving tot het instellen van het eerste paginanummer. Deze kennis kunt u nu gebruiken om de paginanummering in uw Excel-bestanden aan te passen.

### Veelgestelde vragen

#### Vraag 1: Kan ik voor elk werkblad een ander eerste paginanummer instellen?

 A1: Ja, u kunt voor elk werkblad een ander eerste paginanummer instellen door naar het bestand te gaan`FirstPageNumber`eigendom van het betreffende werkblad`PageSetup` voorwerp.

#### Vraag 2: Hoe kan ik het eerste paginanummer van een bestaand spreadsheet controleren?

 A2: U kunt het eerste paginanummer van een bestaand werkblad controleren door naar het bestand te gaan`FirstPageNumber` eigendom van de`PageSetup` object dat overeenkomt met dat werkblad.

#### Vraag 3: Begint de paginanummering standaard altijd vanaf 1?

A3: Ja, paginanummering begint standaard bij 1 in Excel. U kunt echter de code uit deze zelfstudie gebruiken om een ander eerste paginanummer in te stellen.

#### Vraag 4: Zijn wijzigingen aan het eerste paginanummer permanent in het bewerkte Excel-bestand?

A4: Ja, de wijzigingen aan het eerste paginanummer worden permanent opgeslagen in het gewijzigde Excel-bestand.

#### Vraag 5: Werkt deze methode voor alle Excel-bestandsindelingen, zoals .xls en .xlsx?

A5: Ja, deze methode werkt voor alle Excel-bestandsindelingen die worden ondersteund door Aspose.Cells, inclusief .xls en .xlsx.