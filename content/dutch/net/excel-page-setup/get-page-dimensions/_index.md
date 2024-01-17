---
title: Pagina-afmetingen ophalen
linktitle: Pagina-afmetingen ophalen
second_title: Aspose.Cells voor .NET API-referentie
description: Leer hoe u paginadimensies in Excel kunt ophalen met Aspose.Cells voor .NET. Stap voor stap handleiding met broncode in C#.
type: docs
weight: 40
url: /nl/net/excel-page-setup/get-page-dimensions/
---
Aspose.Cells voor .NET is een krachtige bibliotheek waarmee ontwikkelaars programmatisch met Microsoft Excel-bestanden kunnen werken. Het biedt een breed scala aan functies voor het manipuleren van Excel-documenten, inclusief de mogelijkheid om paginaafmetingen op te halen. In deze zelfstudie leiden we u door de stappen om paginadimensies op te halen met Aspose.Cells voor .NET.

## Stap 1: Maak een exemplaar van de Workbook-klasse

Om te beginnen moeten we een exemplaar van de Workbook-klasse maken, die de Excel-werkmap vertegenwoordigt. Dit kan worden bereikt met behulp van de volgende code:

```csharp
Workbook book = new Workbook();
```

## Stap 2: Toegang tot de spreadsheet

Vervolgens moeten we naar het werkblad in de werkmap navigeren waar we de paginadimensies willen instellen. Stel dat we in dit voorbeeld met het eerste werkblad willen werken. We kunnen er toegang toe krijgen met behulp van de volgende code:

```csharp
Worksheet sheet = book.Worksheets[0];
```

## Stap 3: Stel het papierformaat in op A2 en druk de breedte en hoogte af in inches

Nu zullen we het papierformaat instellen op A2 en de paginabreedte en -hoogte in inches afdrukken. Dit kan worden bereikt met behulp van de volgende code:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("A2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Stap 4: Stel het papierformaat in op A3 en druk de breedte en hoogte af in inches

Vervolgens stellen we het papierformaat in op A3 en drukken we de paginabreedte en -hoogte af in inches. Hier is de bijbehorende code:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("A3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Stap 5: Stel het papierformaat in op A4 en druk de breedte en hoogte af in inches

We zullen nu het papierformaat instellen op A4 en de paginabreedte en -hoogte in inches afdrukken. Hier is de code:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("A4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Stap 6: Stel het papierformaat in op Letter en druk de breedte en hoogte af in inches

Ten slotte stellen we het papierformaat in op Letter en drukken we de paginabreedte en -hoogte af in inches. Hier is de code:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("Letter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

### Voorbeeldbroncode voor Get Page Dimensions met Aspose.Cells voor .NET 
```csharp
// Maak een exemplaar van de Workbook-klasse
Workbook book = new Workbook();
// Toegang tot het eerste werkblad
Worksheet sheet = book.Worksheets[0];
// Stel het papierformaat in op A2 en druk de papierbreedte en -hoogte af in inches
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Stel het papierformaat in op A3 en druk de papierbreedte en -hoogte af in inches
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Stel het papierformaat in op A4 en druk de papierbreedte en -hoogte af in inches
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Stel het papierformaat in op Letter en druk de breedte en hoogte van het papier af in inches
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
Console.WriteLine("GetPageDimensions executed successfully.\r\n");
```

## Conclusie

Gefeliciteerd! U hebt geleerd hoe u paginadimensies kunt ophalen met Aspose.Cells voor .NET. Deze functie kan handig zijn wanneer u specifieke bewerkingen moet uitvoeren op basis van paginaafmetingen in uw Excel-bestanden.

Vergeet niet de documentatie van Aspose.Cells verder te verkennen om alle krachtige functies die het biedt te ontdekken.

### Veelgestelde vragen

#### 1. Welke andere papierformaten ondersteunt Aspose.Cells voor .NET?

Aspose.Cells voor .NET ondersteunt een verscheidenheid aan papierformaten, waaronder A1, A5, B4, B5, Executive, Legal, Letter en nog veel meer. U kunt de documentatie raadplegen voor de volledige lijst met ondersteunde papierformaten.

#### 2. Kan ik aangepaste paginaafmetingen instellen met Aspose.Cells voor .NET?

Ja, u kunt aangepaste paginaafmetingen instellen door de gewenste breedte en hoogte op te geven. Aspose.Cells biedt volledige flexibiliteit om pagina-afmetingen aan uw behoeften aan te passen.

#### 3. Kan ik pagina-afmetingen in andere eenheden dan inches krijgen?

Ja, met Aspose.Cells voor .NET kunt u paginaafmetingen in verschillende eenheden verkrijgen, waaronder inches, centimeters, millimeters en punten.

#### 4. Ondersteunt Aspose.Cells voor .NET andere bewerkingsfuncties voor pagina-instellingen?

Ja, Aspose.Cells biedt een volledig scala aan functies voor het bewerken van pagina-instellingen, inclusief het instellen van marges, oriëntatie, kop- en voetteksten, enz.