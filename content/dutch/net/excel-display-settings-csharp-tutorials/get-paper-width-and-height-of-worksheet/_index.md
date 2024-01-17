---
title: Krijg papierbreedte en hoogte van het werkblad
linktitle: Krijg papierbreedte en hoogte van het werkblad
second_title: Aspose.Cells voor .NET API-referentie
description: Maak een stapsgewijze handleiding om de volgende C#-broncode uit te leggen om de papierbreedte en -hoogte van een spreadsheet te verkrijgen met behulp van Aspose.Cells voor .NET.
type: docs
weight: 80
url: /nl/net/excel-display-settings-csharp-tutorials/get-paper-width-and-height-of-worksheet/
---
In deze zelfstudie nemen we u stap voor stap mee om de volgende C#-broncode uit te leggen om de papierbreedte en -hoogte van een werkblad te verkrijgen met behulp van Aspose.Cells voor .NET. Volg onderstaande stappen:

## Stap 1: Maak de werkmap
 Begin met het maken van een nieuwe werkmap met behulp van de`Workbook` klas:

```csharp
Workbook wb = new Workbook();
```

## Stap 2: Open het eerste werkblad
 Navigeer vervolgens naar het eerste werkblad in de werkmap met behulp van de`Worksheet` klas:

```csharp
Worksheet ws = wb.Worksheets[0];
```

## Stap 3: Stel het papierformaat in op A2 en toon de papierbreedte en -hoogte in inches
 Gebruik de`PaperSize` eigendom van de`PageSetup` object om het papierformaat in te stellen op A2 en gebruik vervolgens de`PaperWidth` En`PaperHeight` eigenschappen om respectievelijk de papierbreedte en -hoogte te verkrijgen. Geef deze waarden weer met behulp van de`Console.WriteLine` methode:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

## Stap 4: Herhaal de stappen voor andere papierformaten
Herhaal de voorgaande stappen, wijzig het papierformaat in A3, A4 en Letter en geef vervolgens de papierbreedte- en hoogtewaarden voor elk formaat weer:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

### Voorbeeldbroncode voor Papierbreedte en hoogte van werkblad ophalen met Aspose.Cells voor .NET 

```csharp
//Werkmap maken
Workbook wb = new Workbook();
//Toegang tot het eerste werkblad
Worksheet ws = wb.Worksheets[0];
//Stel het papierformaat in op A2 en druk de papierbreedte en -hoogte af in inches
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Stel het papierformaat in op A3 en druk de papierbreedte en -hoogte af in inches
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Stel het papierformaat in op A4 en druk de papierbreedte en -hoogte af in inches
ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Stel het papierformaat in op Letter en druk de breedte en hoogte van het papier af in inches
ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```


## Conclusie

U hebt geleerd hoe u Aspose.Cells voor .NET kunt gebruiken om de papierbreedte en -hoogte van een spreadsheet te bepalen. Deze functie kan handig zijn voor de configuratie en nauwkeurige lay-out van uw Excel-documenten.

### Veelgestelde vragen (FAQ)

#### Wat is Aspose.Cells voor .NET?

Aspose.Cells voor .NET is een krachtige bibliotheek voor het manipuleren en verwerken van Excel-bestanden in .NET-toepassingen. Het biedt vele functies voor het maken, wijzigen, converteren en analyseren van Excel-bestanden.

#### Hoe kan ik het papierformaat van een spreadsheet verkrijgen met Aspose.Cells voor .NET?

 U kunt gebruik maken van de`PageSetup` klasse van de`Worksheet` object om toegang te krijgen tot het papierformaat. Gebruik de`PaperSize` eigenschap om het papierformaat en de`PaperWidth` En`PaperHeight` eigenschappen om respectievelijk de papierbreedte en -hoogte te verkrijgen.

#### Welke papierformaten ondersteunt Aspose.Cells voor .NET?

Aspose.Cells voor .NET ondersteunt een breed scala aan veelgebruikte papierformaten, zoals A2, A3, A4 en Letter, evenals vele andere aangepaste formaten.

#### Kan ik het papierformaat van een spreadsheet aanpassen met Aspose.Cells voor .NET?

 Ja, u kunt een aangepast papierformaat instellen door de exacte breedte- en hoogte-afmetingen op te geven met behulp van de`PaperWidth` En`PaperHeight` eigenschappen van de`PageSetup` klas.