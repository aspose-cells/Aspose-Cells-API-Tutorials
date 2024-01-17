---
title: Kopieer de pagina-instellingsinstellingen van een ander werkblad
linktitle: Kopieer de pagina-instellingsinstellingen van een ander werkblad
second_title: Aspose.Cells voor .NET API-referentie
description: Leer hoe u paginaconfiguratie-instellingen van de ene spreadsheet naar de andere kunt kopiëren met Aspose.Cells voor .NET. Een stapsgewijze handleiding voor het optimaliseren van het gebruik van deze bibliotheek.
type: docs
weight: 10
url: /nl/net/excel-page-setup/copy-page-setup-settings-from-other-worksheet/
---
In dit artikel nemen we u stap voor stap mee om de volgende C#-broncode uit te leggen: Kopieer paginaconfiguratie-instellingen uit een andere spreadsheet met Aspose.Cells voor .NET. We zullen de Aspose.Cells-bibliotheek voor .NET gebruiken om deze bewerking uit te voeren. Als u de pagina-instellingen van het ene werkblad naar het andere wilt kopiëren, volgt u de onderstaande stappen.

## Stap 1: De werkmap maken
De eerste stap is het maken van een werkmap. In ons geval gebruiken we de Workbook-klasse die wordt geleverd door de Aspose.Cells-bibliotheek. Hier is de code om een werkmap te maken:

```csharp
Workbook wb = new Workbook();
```

## Stap 2: Testwerkbladen toevoegen
Nadat we de werkmap hebben gemaakt, moeten we testwerkbladen toevoegen. In dit voorbeeld voegen we twee werkbladen toe. Hier is de code om twee werkbladen toe te voegen:

```csharp
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
```

## Stap 3: Toegang tot werkbladen
Nu we de werkbladen hebben toegevoegd, moeten we ze openen om hun instellingen te kunnen wijzigen. We krijgen toegang tot de werkbladen "TestSheet1" en "TestSheet2" met behulp van hun namen. Hier is de code om er toegang toe te krijgen:

```csharp
Worksheet TestSheet1 = wb. Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb. Worksheets["TestSheet2"];
```

## Stap 4: Papierformaat instellen
 In deze stap stellen we het papierformaat van het werkblad "TestSheet1" in. Wij zullen gebruik maken van de`PageSetup.PaperSize` eigenschap om het papierformaat in te stellen. We zullen het papierformaat bijvoorbeeld instellen op "PaperA3ExtraTransverse". Hier is de code daarvoor:

```csharp
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
```

## Stap 5: Pagina-instellingsinstellingen kopiëren
Nu kopiëren we de paginaconfiguratie-instellingen van het werkblad "TestSheet1" naar "TestSheet2". Wij zullen gebruik maken van de`PageSetup.Copy` methode om deze handeling uit te voeren. Hier is de code daarvoor:

```csharp
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
```

## Stap 6: Papierformaten afdrukken
 Nadat we de pagina-instellingen hebben gekopieerd, zullen we de papierformaten van de twee werkbladen afdrukken. We zullen gebruiken`Console.WriteLine` om de papierformaten weer te geven. Hier is de code daarvoor:

```csharp
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
```

### Voorbeeldbroncode voor het kopiëren van pagina-instellingen uit een ander werkblad met Aspose.Cells voor .NET 
```csharp
//Werkmap maken
Workbook wb = new Workbook();
//Voeg twee testwerkbladen toe
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
//Toegang tot beide werkbladen als TestSheet1 en TestSheet2
Worksheet TestSheet1 = wb.Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb.Worksheets["TestSheet2"];
//Stel het papierformaat van TestSheet1 in op PaperA3ExtraTransverse
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
//Druk het papierformaat van beide werkbladen af
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
//Kopieer de Pagina-instelling van TestSheet1 naar TestSheet2
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
//Druk het papierformaat van beide werkbladen af
Console.WriteLine("After Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("After Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
Console.WriteLine("CopyPageSetupSettingsFromSourceWorksheetToDestinationWorksheet executed successfully.\r\n");
```

## Conclusie
In dit artikel hebben we geleerd hoe u paginaconfiguratie-instellingen van het ene werkblad naar het andere kunt kopiëren met behulp van Aspose.Cells voor .NET. We hebben de volgende stappen doorlopen: de werkmap maken, testwerkbladen toevoegen, toegang krijgen tot de werkbladen, het papierformaat instellen, de pagina-instellingen kopiëren en papierformaten afdrukken. Nu kunt u deze kennis gebruiken om paginaconfiguratie-instellingen naar uw eigen projecten te kopiëren.

### Veelgestelde vragen

#### Vraag: Kan ik paginaconfiguratie-instellingen kopiëren tussen verschillende werkmapinstanties?

 A: Ja, u kunt pagina-instellingen kopiëren tussen verschillende werkmapinstanties met behulp van de`PageSetup.Copy` methode van de Aspose.Cells-bibliotheek.

#### Vraag: Kan ik andere pagina-instellingen kopiëren, zoals richting of marges?

 A: Ja, u kunt andere pagina-instellingen kopiëren met behulp van de`PageSetup.Copy` methode met de juiste opties. U kunt bijvoorbeeld de richting kopiëren met`CopyOptions.Orientation` en marges gebruiken`CopyOptions.Margins`.

#### Vraag: Hoe weet ik welke opties beschikbaar zijn voor het papierformaat?

A: U kunt de API-referentie van de Aspose.Cells-bibliotheek raadplegen voor beschikbare opties voor papierformaat. Er is een enum genaamd`PaperSizeType` waarin de verschillende ondersteunde papierformaten worden vermeld.

#### Vraag: Hoe kan ik de Aspose.Cells-bibliotheek voor .NET downloaden?

 A: U kunt de Aspose.Cells-bibliotheek voor .NET downloaden van[Aspose-releases](https://releases.aspose.com/cells/net). Er zijn gratis proefversies beschikbaar, evenals betaalde licenties voor commercieel gebruik.

#### Vraag: Ondersteunt de Aspose.Cells-bibliotheek andere programmeertalen?

A: Ja, de Aspose.Cells-bibliotheek ondersteunt meerdere programmeertalen, waaronder C#, Java, Python en nog veel meer.