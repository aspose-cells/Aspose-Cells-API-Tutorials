---
title: Maak een gedeelde werkmap
linktitle: Maak een gedeelde werkmap
second_title: Aspose.Cells voor .NET API-referentie
description: Maak een gedeelde Excel-werkmap met Aspose.Cells voor .NET om gelijktijdige gegevenssamenwerking mogelijk te maken.
type: docs
weight: 70
url: /nl/net/excel-workbook/create-shared-workbook/
---
In deze zelfstudie leiden we u door de meegeleverde C#-broncode waarmee u een gedeelde werkmap kunt maken met Aspose.Cells voor .NET. Volg de onderstaande stappen om deze handeling uit te voeren.

## Stap 1: Stel de uitvoermap in

```csharp
// Uitvoermap
string outputDir = RunExamples.Get_OutputDirectory();
```

In deze eerste stap definiëren we de uitvoermap waar de gedeelde werkmap zal worden opgeslagen.

## Stap 2: Maak een werkmapobject

```csharp
// Maak een werkboekobject
Workbook wb = new Workbook();
```

We maken een nieuw werkmapobject dat onze Excel-werkmap vertegenwoordigt.

## Stap 3: Schakel werkmappen delen in

```csharp
// Deel de werkmap
wb.Settings.Shared = true;
```

 We schakelen de deelfunctie van de werkmap in door de`Shared` eigenschap van het werkmapobject`true`.

## Stap 4: Sla de gedeelde werkmap op

```csharp
// Sla de gedeelde werkmap op
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
```

We slaan de gedeelde werkmap op door het pad en de naam van het uitvoerbestand op te geven.

### Voorbeeldbroncode voor het maken van een gedeelde werkmap met Aspose.Cells voor .NET 
```csharp
//Uitvoermap
string outputDir = RunExamples.Get_OutputDirectory();
//Maak een werkboekobject
Workbook wb = new Workbook();
//Deel de werkmap
wb.Settings.Shared = true;
//Sla de gedeelde werkmap op
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
Console.WriteLine("CreateSharedWorkbook executed successfully.\r\n");
```

## Conclusie

Gefeliciteerd! U hebt geleerd hoe u een gedeelde werkmap kunt maken met Aspose.Cells voor .NET. De gedeelde werkmap kan door meerdere gebruikers tegelijk worden gebruikt om samen aan gegevens te werken. Experimenteer met uw eigen gegevens en verken de functies van Aspose.Cells verder om krachtige en gepersonaliseerde Excel-werkmappen te maken.

### Veelgestelde vragen

#### Vraag: Wat is een gedeelde werkmap?

A: Een gedeelde werkmap is een Excel-werkmap die door meerdere gebruikers tegelijkertijd kan worden gebruikt om samen aan gegevens te werken. Elke gebruiker kan wijzigingen aanbrengen in de werkmap en andere gebruikers zien updates in realtime.

#### Vraag: Hoe kan ik het delen van een werkmap in Aspose.Cells voor .NET inschakelen?

 A: Om het delen van een werkmap in Aspose.Cells voor .NET in te schakelen, moet u de`Shared` eigenschap van het werkmapobject`true`. Hierdoor kunnen gebruikers tegelijkertijd aan de werkmap werken.

#### Vraag: Kan ik gebruikersmachtigingen in een gedeelde werkmap beperken?

A: Ja, u kunt gebruikersmachtigingen in een gedeelde werkmap beperken met behulp van de beveiligingsfuncties van Excel. U kunt voor elke gebruiker specifieke rechten instellen, zoals de mogelijkheid om te bewerken, alleen-lezen, enz.

#### Vraag: Hoe kan ik de werkmap delen met andere gebruikers?

A: Nadat u de gedeelde werkmap heeft gemaakt, kunt u deze delen met andere gebruikers door hen het Excel-bestand te sturen. Andere gebruikers kunnen het bestand openen en er tegelijkertijd aan werken.

#### Vraag: Worden alle Excel-functies ondersteund in een gedeelde werkmap?

A: De meeste Excel-functies worden ondersteund in een gedeelde werkmap. Sommige geavanceerde functies, zoals macro's en invoegtoepassingen, kunnen echter beperkingen of restricties hebben bij gebruik in een gedeelde werkmap.