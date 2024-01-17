---
title: Regex vervangen
linktitle: Regex vervangen
second_title: Aspose.Cells voor .NET API-referentie
description: Leer hoe u Regex-vervanging in Excel-bestanden uitvoert met Aspose.Cells voor .NET.
type: docs
weight: 140
url: /nl/net/excel-workbook/regex-replace/
---
Tekstvervanging op basis van reguliere expressies (Regex) is een veel voorkomende taak bij het manipuleren van gegevens in Excel-bestanden. Met Aspose.Cells voor .NET kunt u eenvoudig een Regex-vervanging uitvoeren door deze stappen te volgen:

## Stap 1: Geef de bronmap en de uitvoermap op

Allereerst moet u de bronmap opgeven waar het Excel-bestand met de te vervangen gegevens zich bevindt, evenals de uitvoermap waar u het gewijzigde bestand wilt opslaan. Hier leest u hoe u dit doet met Aspose.Cells:

```csharp
// bronmap
string sourceDir = RunExamples.Get_SourceDirectory();

// Uitvoermap
string outputDir = RunExamples.Get_OutputDirectory();
```

## Stap 2: Laad het bron-Excel-bestand

Vervolgens moet u het Excel-bronbestand laden waarop u de Regex-vervanging wilt uitvoeren. Hier leest u hoe u het moet doen:

```csharp
// Laad het bron-Excel-bestand
Workbook workbook = new Workbook(sourceDir + "SampleRegexReplace.xlsx");
```

## Stap 3: Voer Regex-vervanging uit

Nadat u het bestand heeft geüpload, kunt u vervangingsopties instellen, waaronder hoofdlettergevoeligheid en exacte afstemming van de celinhoud. Hier is voorbeeldcode om de Regex-vervanging uit te voeren:

```csharp
// Vervangingsopties instellen
ReplaceOptions replace = new ReplaceOptions();
replace.CaseSensitive = false;
replace.MatchEntireCellContents = false;

// Definieer dat de zoeksleutel een reguliere expressie is
replace. RegexKey = true;

// Voer Regex-vervanging uit
workbook. Replace("\\bKIM\\b", "^^^TIM^^^", replace);
```

## Stap 4: Sla het uitgevoerde Excel-bestand op

Zodra de Regex-vervanging is voltooid, kunt u het gewijzigde Excel-bestand opslaan in de opgegeven uitvoermap. Hier leest u hoe u het moet doen:

```csharp
// Sla het uitgevoerde Excel-bestand op
workbook.Save(outputDir + "RegexReplace_out.xlsx");
Console.WriteLine("RegexReplace executed successfully.\r\n");
```

### Voorbeeldbroncode voor Regex Replace met Aspose.Cells voor .NET 
```csharp
//Bronmap
string sourceDir = RunExamples.Get_SourceDirectory();
//Uitvoermap
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "SampleRegexReplace.xlsx");
ReplaceOptions replace = new ReplaceOptions();
replace.CaseSensitive = false;
replace.MatchEntireCellContents = false;
// Stel deze in op true om aan te geven dat de gezochte sleutel regex is
replace.RegexKey = true;
workbook.Replace("\\bKIM\\b", "^^^TIM^^^", replace);
workbook.Save(outputDir + "RegexReplace_out.xlsx");
Console.WriteLine("RegexReplace executed successfully.");
```

## Conclusie

Regex-vervanging is een krachtige techniek voor het dynamisch wijzigen van gegevens in een Excel-bestand. Met Aspose.Cells voor .NET kunt u eenvoudig een Regex-vervanging uitvoeren door de hierboven beschreven stappen te volgen. Experimenteer met uw eigen reguliere expressies en profiteer van de flexibiliteit die Aspose.Cells biedt.

### Veelgestelde vragen

#### Vraag: Wat is Regex-vervanging?
    
A: Regex-vervanging is een techniek die wordt gebruikt om tekstpatronen te vervangen op basis van reguliere expressies in een Excel-bestand. Hierdoor zijn snelle en nauwkeurige wijzigingen in de gegevens mogelijk.

#### Vraag: Is Regex-vervanging hoofdlettergevoelig?
    
A: Nee, met Aspose.Cells kunt u opgeven of de Regex-vervanging hoofdlettergevoelig moet zijn of niet. U heeft volledige controle over deze functie.

#### Vraag: Hoe kan ik een exacte overeenkomst van celinhoud opgeven bij het vervangen van Regex?
    
A: Met Aspose.Cells kunt u definiëren of de Regex-vervanging exact moet overeenkomen met de celinhoud of niet. U kunt deze optie aanpassen aan uw behoeften.

#### Vraag: Kan ik geavanceerde reguliere expressies gebruiken bij het vervangen van Regex door Aspose.Cells?
    
A: Ja, Aspose.Cells ondersteunt geavanceerde reguliere expressies, waardoor u complexe en geavanceerde vervangingen in uw Excel-bestanden kunt uitvoeren.

#### Vraag: Hoe kan ik controleren of de Regex-vervanging succesvol was?
    
A: Nadat u de Regex-vervanging hebt uitgevoerd, kunt u verifiëren of de bewerking succesvol was door de uitvoer te controleren en ervoor te zorgen dat het Excel-uitvoerbestand correct is gemaakt.
	