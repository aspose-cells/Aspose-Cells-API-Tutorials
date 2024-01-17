---
title: Bepaal of het papierformaat van het werkblad automatisch is
linktitle: Bepaal of het papierformaat van het werkblad automatisch is
second_title: Aspose.Cells voor .NET API-referentie
description: Leer hoe u kunt bepalen of het papierformaat van een spreadsheet automatisch is met Aspose.Cells voor .NET.
type: docs
weight: 20
url: /nl/net/excel-page-setup/determine-if-paper-size-of-worksheet-is-automatic/
---
In dit artikel nemen we je stap voor stap mee om de volgende C#-broncode uit te leggen: Bepaal of het papierformaat van een werkblad automatisch is met behulp van Aspose.Cells voor .NET. We zullen de Aspose.Cells-bibliotheek voor .NET gebruiken om deze bewerking uit te voeren. Volg de onderstaande stappen om te bepalen of het papierformaat van een werkblad automatisch is.

## Stap 1: Werkmappen laden
De eerste stap is het laden van de werkmappen. We hebben twee werkmappen: één met automatisch papierformaat uitgeschakeld en de andere met automatisch papierformaat ingeschakeld. Hier is de code om de werkmappen te laden:

```csharp
// bronmap
string sourceDir = "YOUR_SOURCE_DIR";
// Uitvoermap
string outputDir = "YOUR_OUTPUT_DIRECTORY";

// Laad de eerste werkmap met automatisch papierformaat uitgeschakeld
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");

// Laad een tweede werkmap met automatisch papierformaat ingeschakeld
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
```

## Stap 2: Toegang tot spreadsheets
Nu we de werkmappen hebben geladen, moeten we toegang krijgen tot de werkbladen zodat we het automatische papierformaat kunnen controleren. We gaan naar het eerste werkblad van de twee werkmappen. Hier is de code om er toegang toe te krijgen:

```csharp
//Ga naar het eerste werkblad van de eerste werkmap
Worksheet ws11 = wb1.Worksheets[0];

// Ga naar het eerste werkblad van de tweede werkmap
Worksheet ws12 = wb2.Worksheets[0];
```

## Stap 3: Controleer het automatische papierformaat
 In deze stap controleren we of het papierformaat van het werkblad automatisch is. Wij zullen gebruik maken van de`PageSetup.IsAutomaticPaperSize` eigendom om deze informatie te verkrijgen. Wij zullen dan het resultaat weergeven. Hier is de code daarvoor:

```csharp
// Geef de eigenschap IsAutomaticPaperSize van het eerste werkblad in de eerste werkmap weer
Console.WriteLine("First worksheet in first workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);

// Geef de eigenschap IsAutomaticPaperSize van het eerste werkblad in de tweede werkmap weer
Console.WriteLine("First worksheet of second workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);

```

### Voorbeeldbroncode voor Bepalen of het papierformaat van het werkblad automatisch is met behulp van Aspose.Cells voor .NET 
```csharp
//Bronmap
string sourceDir = "YOUR_SOURCE_DIRECTORY";
//Uitvoermap
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//Laad de eerste werkmap met automatisch papierformaat false
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");
//Laad de tweede werkmap met automatisch papierformaat waar
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
//Toegang tot het eerste werkblad van beide werkmappen
Worksheet ws11 = wb1.Worksheets[0];
Worksheet ws12 = wb2.Worksheets[0];
//Druk de eigenschap PageSetup.IsAutomaticPaperSize van beide werkbladen af
Console.WriteLine("First Worksheet of First Workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);
Console.WriteLine("First Worksheet of Second Workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);
Console.WriteLine();
Console.WriteLine("DetermineIfPaperSizeOfWorksheetIsAutomatic executed successfully.\r\n");
```


## Conclusie
In dit artikel hebben we geleerd hoe we kunnen bepalen of het papierformaat van een werkblad automatisch is met behulp van Aspose.Cells voor .NET. We hebben de volgende stappen gevolgd: het laden van de werkmappen,

toegang tot spreadsheets en automatische controle van het papierformaat. Nu kunt u deze kennis gebruiken om te bepalen of het papierformaat van uw spreadsheets automatisch is.

### Veelgestelde vragen

#### Vraag: Hoe kan ik werkmappen laden met Aspose.Cells voor .NET?

A: U kunt werkmappen laden met behulp van de Workbook-klasse uit de Aspose.Cells-bibliotheek. Gebruik de Workbook.Load-methode om een werkmap uit een bestand te laden.

#### Vraag: Kan ik het automatische papierformaat voor andere spreadsheets controleren?

A: Ja, u kunt het automatische papierformaat voor elk werkblad controleren door de eigenschap PageSetup.IsAutomaticPaperSize van het overeenkomstige werkbladobject te openen.

#### Vraag: Hoe kan ik het automatische papierformaat van een spreadsheet wijzigen?

A: Om het automatische papierformaat van een werkblad te wijzigen, kunt u de eigenschap PageSetup.IsAutomaticPaperSize gebruiken en deze instellen op de gewenste waarde (true of false).

#### Vraag: Welke andere functies biedt Aspose.Cells voor .NET?

A: Aspose.Cells voor .NET biedt veel functies voor het werken met spreadsheets, zoals het maken, wijzigen en converteren van werkmappen, en het manipuleren van gegevens, formules en opmaak.