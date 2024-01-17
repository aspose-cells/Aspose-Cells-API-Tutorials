---
title: Update Power Query-formule-item
linktitle: Update Power Query-formule-item
second_title: Aspose.Cells voor .NET API-referentie
description: Leer hoe u Power Query-formule-elementen in Excel-bestanden kunt bijwerken met Aspose.Cells voor .NET.
type: docs
weight: 160
url: /nl/net/excel-workbook/update-power-query-formula-item/
---
Het bijwerken van een Power Query-formule-item is een veel voorkomende bewerking bij het werken met gegevens in Excel-bestanden. Met Aspose.Cells voor .NET kunt u eenvoudig een Power Query-formule-item bijwerken door deze stappen te volgen:

## Stap 1: Geef de bron- en uitvoermappen op

Eerst moet u de bronmap opgeven waar het Excel-bestand met de Power Query-formules die moeten worden bijgewerkt, zich bevindt, evenals de uitvoermap waar u het gewijzigde bestand wilt opslaan. Hier leest u hoe u dit doet met Aspose.Cells:

```csharp
// bronmap
string SourceDir = RunExamples.Get_SourceDirectory();

// Uitvoermap
string outputDir = RunExamples.Get_OutputDirectory();
```

## Stap 2: Laad de bron-Excel-werkmap

Vervolgens moet u de Excel-bronwerkmap laden waarin u het Power Query-formule-item wilt bijwerken. Hier leest u hoe u het moet doen:

```csharp
// Laad de bron-Excel-werkmap
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
```

## Stap 3: Blader door Power Query-formule-items en werk deze bij

Nadat u de werkmap hebt geladen, kunt u naar de Power Query-formuleverzameling navigeren en door elke formule en de bijbehorende elementen bladeren. In dit voorbeeld zoeken we naar het formule-item met de naam 'Bron' en werken we de waarde ervan bij. Hier volgt een voorbeeldcode voor het bijwerken van een Power Query-formule-item:

```csharp
// Toegang tot de Power Query-formuleverzameling
DataMashup mashupData = workbook.DataMashup;

// Loop door Power Query-formules en hun elementen
foreach(PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
     foreach(PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
     {
         if (item.Name == "Source")
         {
             item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
         }
     }
}
```

## Stap 4: Sla de uitgevoerde Excel-werkmap op

Nadat u het Power Query-formule-item hebt bijgewerkt, kunt u de gewijzigde Excel-werkmap opslaan in de opgegeven uitvoermap. Hier leest u hoe u het moet doen:

```csharp
// Sla de uitgevoerde Excel-werkmap op
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.\r\n");
```

### Voorbeeldbroncode voor het bijwerken van het Power Query-formule-item met Aspose.Cells voor .NET 
```csharp
// Werkende mappen
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
DataMashup mashupData = workbook.DataMashup;
foreach (PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
	foreach (PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
	{
		if (item.Name == "Source")
		{
			item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
		}
	}
}
// Sla de uitvoerwerkmap op.
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.");
```

## Conclusie

Het bijwerken van Power Query-formule-elementen is een essentiële bewerking bij het gebruik van Aspose.Cells om gegevens in Excel-bestanden te manipuleren en verwerken. Door de bovenstaande stappen te volgen, kunt u formule-elementen eenvoudig bijwerken

### Veelgestelde vragen

#### Vraag: Wat is Power Query in Excel?
     
A: Power Query is een functie in Excel waarmee u gegevens uit verschillende bronnen kunt verzamelen, transformeren en laden. Het biedt krachtige tools om gegevens op te schonen, te combineren en opnieuw vorm te geven voordat deze in Excel worden geïmporteerd.

#### V: Hoe weet ik of een Power Query-formule-item met succes is bijgewerkt?
    A: After running the Power Query Formula Item Update, you can check if the operation was successful by viewing the output and ensuring that the output Excel file was created correctly.

#### V: Kan ik meerdere Power Query-formule-items tegelijk bijwerken?
    
A: Ja, u kunt de verzameling Power Query-formule-items doorlopen en meerdere items in één lus bijwerken, afhankelijk van uw specifieke behoeften.

#### V: Zijn er andere bewerkingen die ik kan uitvoeren op Power Query-formules met Aspose.Cells?
    
A: Ja, Aspose.Cells biedt een volledige reeks functies voor het werken met Power Query-formules, inclusief het maken, verwijderen, kopiëren en doorzoeken van formules in een Excel-werkmap.