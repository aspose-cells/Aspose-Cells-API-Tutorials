---
title: Filter gedefinieerde namen tijdens het laden van de werkmap
linktitle: Filter gedefinieerde namen tijdens het laden van de werkmap
second_title: Aspose.Cells voor .NET API-referentie
description: Leer hoe u gedefinieerde namen filtert bij het laden van een Excel-werkmap met Aspose.Cells voor .NET.
type: docs
weight: 100
url: /nl/net/excel-workbook/filter-defined-names-while-loading-workbook/
---
Wanneer u met Excel-werkmappen in een .NET-toepassing werkt, is het vaak nodig om gegevens tijdens het laden te filteren. Aspose.Cells voor .NET is een krachtige bibliotheek waarmee u eenvoudig Excel-werkmappen kunt manipuleren. In deze handleiding laten we u zien hoe u de namen filtert die zijn gedefinieerd bij het laden van een werkmap met Aspose.Cells voor .NET. Volg deze eenvoudige stappen om de gewenste resultaten te krijgen:

## Stap 1: Geef laadopties op

Eerst moet u de laadopties opgeven om het laadgedrag van de werkmap te definiëren. In ons geval willen we de namen negeren die tijdens het laden zijn ingesteld. Hier leest u hoe u dit doet met Aspose.Cells:

```csharp
// Specificeert laadopties
LoadOptions opts = new LoadOptions();

// Laad geen gedefinieerde namen
opts. LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
```

## Stap 2: Laad de werkmap

Zodra de laadopties zijn geconfigureerd, kunt u de Excel-werkmap vanuit het bronbestand laden. Zorg ervoor dat u het juiste bestandspad opgeeft. Hier is een voorbeeldcode:

```csharp
// Laad de werkmap
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
```

## Stap 3: Sla de gefilterde werkmap op

Nadat u de werkmap hebt geladen, kunt u indien nodig andere bewerkingen of bewerkingen uitvoeren. Vervolgens kunt u de gefilterde werkmap opslaan in een uitvoerbestand. Hier is hoe:

```csharp
// Sla de gefilterde Excel-werkmap op
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
```

### Voorbeeldbroncode voor door filter gedefinieerde namen tijdens het laden van de werkmap met Aspose.Cells voor .NET 
```csharp
//Geef de laadopties op
LoadOptions opts = new LoadOptions();
//We willen geen gedefinieerde namen laden
opts.LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
//Laad de werkmap
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
//Sla het Excel-uitvoerbestand op. Het zal de formule in C1 breken
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
Console.WriteLine("FilterDefinedNamesWhileLoadingWorkbook executed successfully.");
```

## Conclusie

Het filteren van gedefinieerde namen bij het laden van een Excel-werkmap kan voor veel toepassingen van cruciaal belang zijn. Aspose.Cells voor .NET maakt deze taak eenvoudiger door flexibele opties te bieden voor het laden en filteren van gegevens. Door de stappen in deze handleiding te volgen, kunt u de gedefinieerde namen effectief uitfilteren en de gewenste resultaten in uw Excel-werkmappen bereiken.


### Veelgestelde vragen

#### Vraag: Ondersteunt Aspose.Cells naast C# ook andere programmeertalen?
    
A: Ja, Aspose.Cells is een platformonafhankelijke bibliotheek die vele programmeertalen ondersteunt, zoals Java, Python, C++en nog veel meer.

#### Vraag: Kan ik andere gegevenstypen filteren bij het laden van een werkmap met Aspose.Cells?
    
A: Ja, Aspose.Cells biedt een reeks filteropties voor gegevens, waaronder formules, stijlen, macro's, enz.

#### Vraag: Behoudt Aspose.Cells de opmaak en eigenschappen van de originele werkmap?
    
A: Ja, Aspose.Cells behoudt de opmaak, stijlen, formules en andere eigenschappen van de originele werkmap bij het werken met Excel-bestanden.