---
title: Werken met inhoudstype-eigenschappen
linktitle: Werken met inhoudstype-eigenschappen
second_title: Aspose.Cells voor .NET API-referentie
description: Leer hoe u met inhoudstype-eigenschappen kunt werken met Aspose.Cells voor .NET.
type: docs
weight: 180
url: /nl/net/excel-workbook/working-with-content-type-properties/
---
Eigenschappen van inhoudstypen spelen een cruciale rol bij het beheren en manipuleren van Excel-bestanden met behulp van de Aspose.Cells-bibliotheek voor .NET. Met deze eigenschappen kunt u aanvullende metagegevens voor Excel-bestanden definiëren, waardoor het gemakkelijker wordt om gegevens te ordenen en te vinden. In deze zelfstudie laten we u stap voor stap zien hoe u inhoudstype-eigenschappen kunt begrijpen en ermee kunt werken met behulp van voorbeeld-C#-code.

## Vereisten

Zorg ervoor dat u over het volgende beschikt voordat u begint:

- Aspose.Cells voor .NET geïnstalleerd op uw ontwikkelmachine.
- Een geïntegreerde ontwikkelomgeving (IDE) die compatibel is met C#, zoals Visual Studio.

## Stap 1: De omgeving instellen

Voordat u met inhoudstype-eigenschappen gaat werken, moet u ervoor zorgen dat u uw ontwikkelomgeving hebt ingesteld met Aspose.Cells voor .NET. U kunt de verwijzing toevoegen aan de Aspose.Cells-bibliotheek in uw project en de vereiste naamruimte in uw klas importeren.

```csharp
using Aspose.Cells;
```

## Stap 2: Een nieuwe Excel-werkmap maken

 Eerst maken we een nieuwe Excel-werkmap met behulp van de`Workbook`klasse geleverd door Aspose.Cells. De volgende code laat zien hoe u een nieuwe Excel-werkmap maakt en deze opslaat in een opgegeven uitvoermap.

```csharp
// Doelmap
string outputDir = RunExamples.Get_OutputDirectory();

// Maak een nieuwe Excel-werkmap
Workbook workbook = new Workbook(FileFormatType.Xlsx);
```

## Stap 3: Eigenschappen van inhoudstype toevoegen

 Nu we onze Excel-werkmap hebben, kunnen we inhoudstype-eigenschappen toevoegen met behulp van de`Add` werkwijze van de`ContentTypeProperties` verzameling van de`Workbook` klas. Elke eigenschap wordt weergegeven door een naam en een waarde. JIJ

  U kunt ook het gegevenstype van de eigenschap opgeven.

```csharp
// Voeg de eerste eigenschap van het inhoudstype toe
int index = workbook.ContentTypeProperties.Add("MK31", "Simple Data");
workbook.ContentTypeProperties[index].IsNillable = false;

// Voeg de tweede eigenschap van het inhoudstype toe
index = workbook.ContentTypeProperties.Add("MK32", DateTime.Now.ToString("yyyy-MM-dd'T'hh:mm:ss"), "DateTime");
workbook.ContentTypeProperties[index].IsNillable = true;
```

## Stap 4: De Excel-werkmap opslaan

 Nadat we de eigenschappen van het inhoudstype hebben toegevoegd, kunnen we de Excel-werkmap met de wijzigingen opslaan. Gebruik de`Save` werkwijze van de`Workbook` class om de uitvoermap en bestandsnaam op te geven.

```csharp
// Sla de Excel-werkmap op
workbook.Save(outputDir + "WorkingWithContentTypeProperties_out.xlsx");
```

### Voorbeeldbroncode voor het werken met inhoudstype-eigenschappen met Aspose.Cells voor .NET 
```csharp
//bronmap
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(FileFormatType.Xlsx);
int index = workbook.ContentTypeProperties.Add("MK31", "Simple Data");
workbook.ContentTypeProperties[index].IsNillable = false;
index = workbook.ContentTypeProperties.Add("MK32", DateTime.Now.ToString("yyyy-MM-dd'T'hh:mm:ss"), "DateTime");
workbook.ContentTypeProperties[index].IsNillable = true;
workbook.Save(outputDir + "WorkingWithContentTypeProperties_out.xlsx");
Console.WriteLine("WorkingWithContentTypeProperties executed successfully.");
```

## Conclusie

Gefeliciteerd! U hebt geleerd hoe u met inhoudstype-eigenschappen kunt werken met behulp van Aspose.Cells voor .NET. Nu kunt u aangepaste metagegevens aan uw Excel-bestanden toevoegen en deze efficiënter beheren.

### Veelgestelde vragen

#### Vraag: Zijn de eigenschappen van het inhoudstype compatibel met alle versies van Excel?

A: Ja, de eigenschappen van het inhoudstype zijn compatibel met Excel-bestanden die in alle versies van Excel zijn gemaakt.

#### Vraag: Kan ik de eigenschappen van het inhoudstype bewerken nadat ik ze aan de Excel-werkmap heb toegevoegd?

 A: Ja, u kunt de eigenschappen van het inhoudstype op elk gewenst moment wijzigen door naar de`ContentTypeProperties` verzameling van de`Workbook` klasse en met behulp van de en p-methodengeschikte eigenschappen.

#### Vraag: Worden eigenschappen van het inhoudstype ondersteund bij het opslaan naar PDF?

A: Nee, eigenschappen van het inhoudstype worden niet ondersteund bij het opslaan naar PDF. Ze zijn specifiek voor Excel-bestanden.