---
title: Pas het compressieniveau aan
linktitle: Pas het compressieniveau aan
second_title: Aspose.Cells voor .NET API-referentie
description: Verklein de grootte van uw Excel-werkmappen door het compressieniveau aan te passen met Aspose.Cells voor .NET.
type: docs
weight: 50
url: /nl/net/excel-workbook/adjust-compression-level/
---
In deze stapsgewijze zelfstudie leggen we de meegeleverde C#-broncode uit waarmee u het compressieniveau kunt aanpassen met Aspose.Cells voor .NET. Volg de onderstaande stappen om het compressieniveau in uw Excel-werkmap aan te passen.

## Stap 1: Stel de bron- en uitvoermappen in

```csharp
// bronmap
string sourceDir = RunExamples.Get_SourceDirectory();
// Uitvoermap
string outDir = RunExamples.Get_OutputDirectory();
```

In deze eerste stap definiëren we de bron- en uitvoermappen voor de Excel-bestanden.

## Stap 2: Excel-werkmap laden

```csharp
// Laad de Excel-werkmap
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
```

We laden de Excel-werkmap vanuit het opgegeven bestand met behulp van de`Workbook` klasse van Aspose.Cells.

## Stap 3: Stel back-upopties in

```csharp
// Definieer back-upopties
XlsbSaveOptions options = new XlsbSaveOptions();
```

 We maken een exemplaar van de`XlsbSaveOptions` klasse om opslagopties in te stellen.

## Stap 4: Pas het compressieniveau aan (niveau 1)

```csharp
// Pas het compressieniveau aan (niveau 1)
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
let elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 1): " + elapsedMs);
```

 We passen het compressieniveau aan door in te stellen`CompressionType` naar`Level1`. Vervolgens slaan we de Excel-werkmap op met deze compressieoptie gespecificeerd.

## Stap 5: Pas het compressieniveau aan (niveau 6)

```csharp
// Pas het compressieniveau aan (niveau 6)
options.CompressionType = OoxmlCompressionType.Level6;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 6): " + elapsedMs);
```

 We herhalen het proces om het compressieniveau aan te passen`Level6` en sla de Excel-werkmap op met deze optie.

## Stap 6: Pas het compressieniveau aan (niveau 9)

```csharp
// Pas het compressieniveau aan (niveau 9)
options.CompressionType = OoxmlCompressionType.Level9;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 9): " + elapsedMs);
```

 We herhalen het proces nog een laatste keer om het compressieniveau aan te passen`Level9` en sla de Excel-werkmap op met deze optie.

### Voorbeeldbroncode voor het aanpassen van het compressieniveau met Aspose.Cells voor .NET 
```csharp
//Bronmap
string sourceDir = RunExamples.Get_SourceDirectory();
string outDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
XlsbSaveOptions options = new XlsbSaveOptions();
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
var elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 1 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level6;
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 6 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level9;
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 9 Elapsed Time: " + elapsedMs);
Console.WriteLine("AdjustCompressionLevel executed successfully.");
```

## Conclusie

Gefeliciteerd! U hebt geleerd hoe u het compressieniveau in een Excel-werkmap kunt aanpassen met Aspose.Cells voor .NET. Experimenteer met verschillende compressieniveaus om het niveau te vinden dat het beste bij uw behoeften past.

### Veelgestelde vragen

#### Vraag: Wat is compressie in een Excel-werkmap?

A: Compressie in een Excel-werkmap is een proces waarbij de bestandsgrootte wordt verkleind met behulp van compressie-algoritmen. Dit vermindert de benodigde opslagruimte en verbetert de prestaties bij het laden en manipuleren van het bestand.

#### Vraag: Welke compressieniveaus zijn beschikbaar met Aspose.Cells?

A: Met Aspose.Cells kunt u het compressieniveau aanpassen van 1 tot 9. Hoe hoger het compressieniveau, hoe kleiner de bestandsgrootte, maar dit kan ook de verwerkingstijd verlengen.

#### Vraag: Hoe kies ik het juiste compressieniveau voor mijn Excel-werkmap?

A: De keuze van het compressieniveau hangt af van uw specifieke behoeften. Als je maximale compressie wilt en verwerkingstijd geen probleem is, kun je voor niveau 9 gaan. Als je de voorkeur geeft aan een compromis tussen bestandsgrootte en verwerkingstijd, kun je een tussenliggend niveau kiezen.

#### Vraag: Heeft compressie invloed op de gegevenskwaliteit in de Excel-werkmap?

A: Nee, de compressie heeft geen invloed op de gegevenskwaliteit in de Excel-werkmap. Het verkleint eenvoudigweg de bestandsgrootte met behulp van compressietechnieken zonder de gegevens zelf te wijzigen.

#### Vraag: Kan ik het compressieniveau aanpassen nadat ik het Excel-bestand heb opgeslagen?

A: Nee, zodra u het Excel-bestand met een specifiek compressieniveau heeft opgeslagen, kunt u het compressieniveau later niet meer aanpassen. Als u het bestand wilt wijzigen, moet u het bestand opnieuw opslaan met het nieuwe compressieniveau.