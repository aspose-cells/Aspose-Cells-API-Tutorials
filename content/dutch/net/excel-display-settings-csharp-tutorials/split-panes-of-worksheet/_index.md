---
title: Gesplitste deelvensters van het werkblad
linktitle: Gesplitste deelvensters van het werkblad
second_title: Aspose.Cells voor .NET API-referentie
description: Stapsgewijze handleiding voor het splitsen van deelvensters in een Excel-werkblad met Aspose.Cells voor .NET.
type: docs
weight: 130
url: /nl/net/excel-display-settings-csharp-tutorials/split-panes-of-worksheet/
---
In deze zelfstudie leggen we uit hoe u deelvensters in een Excel-werkblad kunt splitsen met Aspose.Cells voor .NET. Volg deze stappen om het gewenste resultaat te krijgen:

## Stap 1: De omgeving instellen

Zorg ervoor dat u Aspose.Cells voor .NET hebt geïnstalleerd en uw ontwikkelomgeving hebt ingesteld. Zorg er ook voor dat u een kopie hebt van het Excel-bestand waarin u de vensters wilt splitsen.

## Stap 2: Importeer de benodigde afhankelijkheden

Voeg de nodige richtlijnen toe om de klassen van Aspose.Cells te gebruiken:

```csharp
using Aspose.Cells;
```

## Stap 3: Code-initialisatie

Begin met het initialiseren van het pad naar de map met uw Excel-documenten:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## Stap 4: Het Excel-bestand openen

 Instantieer een nieuwe`Workbook` object en open het Excel-bestand met behulp van de`Open` methode:

```csharp
Workbook book = new Workbook(dataDir + "Book1.xls");
```

## Stap 5: Definieer de actieve cel

 Stel de actieve cel van het werkblad in met behulp van de`ActiveCell` eigendom:

```csharp
book.Worksheets[0].ActiveCell = "A20";
```

## Stap 6: Verdeling van de flappen

 Splits het werkbladvenster met behulp van de`Split` methode:

```csharp
book.Worksheets[0].Split();
```

## Stap 7: Wijzigingen opslaan

Sla de wijzigingen in het Excel-bestand op:

```csharp
book.Save(dataDir + "output.xls");
```

### Voorbeeldbroncode voor gesplitste deelvensters van werkbladen met Aspose.Cells voor .NET 

```csharp
//Het pad naar de documentenmap.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instantieer een nieuwe werkmap en open een sjabloonbestand
Workbook book = new Workbook(dataDir + "Book1.xls");
// Stel de actieve cel in
book.Worksheets[0].ActiveCell = "A20";
// Splits het werkbladvenster
book.Worksheets[0].Split();
// Sla het Excel-bestand op
book.Save(dataDir + "output.xls");
```

## Conclusie

In deze zelfstudie hebt u geleerd hoe u deelvensters in een Excel-werkblad kunt splitsen met Aspose.Cells voor .NET. Door de beschreven stappen te volgen, kunt u het uiterlijk en het gedrag van uw Excel-bestanden eenvoudig aanpassen.

### Veelgestelde vragen (FAQ)

#### Wat is Aspose.Cells voor .NET?

Aspose.Cells voor .NET is een populaire softwarebibliotheek voor het manipuleren van Excel-bestanden in .NET-toepassingen.

#### Hoe kan ik de actieve cel van een werkblad instellen in Aspose.Cells?

 U kunt de actieve cel instellen met behulp van de`ActiveCell`eigenschap van het werkbladobject.

#### Kan ik alleen de horizontale of verticale panelen van het werkbladvenster splitsen?

 Ja, met Aspose.Cells kunt u alleen horizontale of verticale panelen splitsen met behulp van de juiste methoden, zoals`SplitColumn` of`SplitRow`.

#### Werkt Aspose.Cells alleen met Excel-bestanden in .xls-indeling?

Nee, Aspose.Cells ondersteunt verschillende Excel-bestandsindelingen, waaronder .xls en .xlsx.