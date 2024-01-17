---
title: Laat leidende apostrof toe
linktitle: Laat leidende apostrof toe
second_title: Aspose.Cells voor .NET API-referentie
description: Sta leidende apostrof toe in Excel-werkmappen met Aspose.Cells voor .NET.
type: docs
weight: 60
url: /nl/net/excel-workbook/allow-leading-apostrophe/
---
In deze stapsgewijze zelfstudie leggen we de meegeleverde C#-broncode uit waarmee u het gebruik van een leidende apostrof in een Excel-werkmap kunt toestaan met behulp van Aspose.Cells voor .NET. Volg de onderstaande stappen om deze handeling uit te voeren.

## Stap 1: Stel de bron- en uitvoermappen in

```csharp
// bronmap
string sourceDir = RunExamples.Get_SourceDirectory();
// Uitvoermap
string outputDir = RunExamples.Get_OutputDirectory();
```

In deze eerste stap definiëren we de bron- en uitvoermappen voor de Excel-bestanden.

## Stap 2: Instantieer een WorkbookDesigner-object

```csharp
// Instantieer een WorkbookDesigner-object
WorkbookDesigner designer = new WorkbookDesigner();
```

 We maken een exemplaar van de`WorkbookDesigner` klasse van Aspose.Cells.

## Stap 3: Excel-werkmap laden

```csharp
// Laad de Excel-werkmap
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
designer.Workbook = workbook;
```

We laden de Excel-werkmap vanuit het opgegeven bestand en schakelen de automatische conversie van initiële apostrofs naar tekststijl uit.

## Stap 4: Stel de gegevensbron in

```csharp
// Definieer de gegevensbron voor de ontwerperwerkmap
List<DataObject> list = new List<DataObject>
{
new DataObject
{
Id=1,
Name = "demo"
},
new DataObject
{
ID=2,
Name = "'demo"
}
};
designer.SetDataSource("sampleData", list);
```

 We definiëren een lijst met gegevensobjecten en gebruiken de`SetDataSource` methode om de gegevensbron voor de ontwerperwerkmap in te stellen.

## Stap 5: Verwerk slimme markers

```csharp
// Verwerk slimme markers
designer. Process();
```

 Wij gebruiken de`Process` methode om slimme markeringen in de ontwerperwerkmap te verwerken.

## Stap 6: Sla de gewijzigde Excel-werkmap op

```csharp
// Sla de gewijzigde Excel-werkmap op
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
```

We slaan de aangepaste Excel-werkmap op met de aangebrachte wijzigingen.

### Voorbeeldbroncode voor Leading Apostrofe toestaan met Aspose.Cells voor .NET 
```csharp
//Bronmap
string sourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
// Een WorkbookDesigner-object instantiëren
WorkbookDesigner designer = new WorkbookDesigner();
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
// Open een ontwerperspreadsheet met slimme markeringen
designer.Workbook = workbook;
List<DataObject> list = new List<DataObject>
{
	new DataObject
	{
		 Id =1,
		 Name = "demo"
	},
	new DataObject
	{
		Id=2,
		Name = "'demo"
	}
};
// Stel de gegevensbron voor de ontwerperspreadsheet in
designer.SetDataSource("sampleData", list);
// Verwerk de slimme markers
designer.Process();
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
Console.WriteLine("AllowLeadingApostrophe executed successfully.");
```

## Conclusie

Gefeliciteerd! U hebt geleerd hoe u het gebruik van een leidende apostrof in een Excel-werkmap kunt toestaan met behulp van Aspose.Cells voor .NET. Experimenteer met uw eigen gegevens om uw Excel-werkmappen verder aan te passen.

### Veelgestelde vragen

#### Vraag: Wat is de toestemming voor leidende apostrofs in een Excel-werkmap?

A: Door de initiële apostrof in een Excel-werkmap toe te staan, kunnen gegevens die beginnen met een apostrof correct worden weergegeven zonder deze naar een tekststijl te converteren. Dit is handig als u de apostrof als onderdeel van de gegevens wilt behouden.

#### Vraag: Waarom moet ik de automatische conversie van initiële apostrofs uitschakelen?

A: Door de automatische conversie van leidende citaten uit te schakelen, kunt u het gebruik ervan in uw gegevens behouden. Dit voorkomt onbedoelde wijziging van de gegevens tijdens het openen of manipuleren van de Excel-werkmap.

#### Vraag: Hoe kan ik de gegevensbron instellen in de ontwerperwerkmap?

 A: Om de gegevensbron in de ontwerperwerkmap in te stellen, kunt u de`SetDataSource` methode die de naam van de gegevensbron en een lijst met bijbehorende gegevensobjecten specificeert.

#### Vraag: Heeft het toestaan van een apostrof vooraan invloed op andere gegevens in de Excel-werkmap?

A: Nee, het toestaan van de leidende apostrof heeft alleen invloed op gegevens die beginnen met een apostrof. Andere gegevens in de Excel-werkmap blijven ongewijzigd.

#### Vraag: Kan ik deze functie gebruiken met andere Excel-bestandsindelingen?

A: Ja, u kunt deze functie gebruiken met andere Excel-bestandsindelingen die worden ondersteund door Aspose.Cells, zoals .xls, .xlsm, enz.