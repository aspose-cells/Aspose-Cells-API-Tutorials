---
title: Pak het ingebedde Mol-bestand uit
linktitle: Pak het ingebedde Mol-bestand uit
second_title: Aspose.Cells voor .NET API-referentie
description: Leer hoe u eenvoudig ingesloten MOL-bestanden uit een Excel-werkmap kunt extraheren met Aspose.Cells voor .NET.
type: docs
weight: 90
url: /nl/net/excel-workbook/extract-embedded-mol-file/
---
In deze zelfstudie laten we u stap voor stap zien hoe u een ingesloten MOL-bestand uit een Excel-werkmap kunt extraheren met behulp van de Aspose.Cells-bibliotheek voor .NET. U leert hoe u door de werkmapbladen bladert, de overeenkomstige OLE-objecten uitpakt en de uitgepakte MOL-bestanden opslaat. Volg de onderstaande stappen om deze taak succesvol te voltooien.

## Stap 1: Definieer bron- en uitvoermappen
Eerst moeten we de bron- en uitvoermappen in onze code definiëren. Deze mappen geven aan waar de bron-Excel-werkmap zich bevindt en waar de uitgepakte MOL-bestanden worden opgeslagen. Hier is de bijbehorende code:

```csharp
// Telefoonboeken
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
```

Zorg ervoor dat u indien nodig de juiste paden opgeeft.

## Stap 2: Het laden van de Excel-werkmap
De volgende stap is het laden van de Excel-werkmap met de ingesloten OLE-objecten en MOL-bestanden. Hier is de code om de werkmap te laden:

```csharp
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
```

Zorg ervoor dat u de naam van het bronbestand correct opgeeft in de code.

## Stap 3: Doorloop de bladen en pak de MOL-bestanden uit
Nu doorlopen we elk blad in de werkmap en extraheren we de overeenkomstige OLE-objecten, die de MOL-bestanden bevatten. Hier is de bijbehorende code:

```csharp
var index = 1;
foreach(Worksheet sheet in workbook.Worksheets)
{
     OleObjectCollection oles = sheet.OleObjects;
     foreach(OleObject ole in oles)
     {
         string fileName = outputDir + "OleObject" + index + ".mol";
         FileStream fs = File.Create(fileName);
         fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
         fs. Close();
         index++;
     }
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

Deze code loopt door elk blad in de werkmap, haalt de OLE-objecten op en slaat de uitgepakte MOL-bestanden op in de uitvoermap.

### Voorbeeldbroncode voor het uitpakken van het ingebedde Mol-bestand met Aspose.Cells voor .NET 
```csharp
//mappen
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
var index = 1;
foreach (Worksheet sheet in workbook.Worksheets)
{
	OleObjectCollection oles = sheet.OleObjects;
	foreach (OleObject ole in oles)
	{
		string fileName = outputDir + "OleObject" + index + ".mol ";
		FileStream fs = File.Create(fileName);
		fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
		fs.Close();
		index++;
	}
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

## Conclusie
Gefeliciteerd! U hebt geleerd hoe u een ingesloten MOL-bestand uit een Excel-werkmap kunt extraheren met Aspose.Cells voor .NET. U kunt deze kennis nu toepassen om MOL-bestanden uit uw eigen Excel-werkmappen te extraheren. Voel je vrij om de Aspose.Cells-bibliotheek verder te verkennen en meer te leren over de andere krachtige functies.

### Veelgestelde vragen

#### Vraag: Wat is een MOL-bestand?
 
A: Een MOL-bestand is een bestandsformaat dat wordt gebruikt om chemische structuren in computationele chemie weer te geven. Het bevat informatie over atomen, bindingen en andere moleculaire eigenschappen.

#### Vraag: Werkt deze methode met alle Excel-bestandstypen?

A: Ja, deze methode werkt met alle Excel-bestandstypen die worden ondersteund door Aspose.Cells.

#### Vraag: Kan ik meerdere MOL-bestanden tegelijk uitpakken?

A: Ja, u kunt meerdere MOL-bestanden tegelijk extraheren door OLE-objecten op elk blad in de werkmap te doorlopen.