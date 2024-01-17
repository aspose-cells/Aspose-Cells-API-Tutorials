---
title: Excel-kopieerwerkblad
linktitle: Excel-kopieerwerkblad
second_title: Aspose.Cells voor .NET API-referentie
description: Kopieer het ene Excel-werkblad naar het andere met Aspose.Cells voor .NET.
type: docs
weight: 20
url: /nl/net/excel-copy-worksheet/excel-copy-worksheet/
---

In deze handleiding leggen we uit hoe u een Excel-werkblad kopieert met behulp van de Aspose.Cells-bibliotheek voor .NET. We voorzien u van de C#-broncode en begeleiden u door de stappen die nodig zijn om deze taak te voltooien. Aan het einde laten we u het verwachte resultaat zien. Volg de onderstaande instructies om aan de slag te gaan.

## Stap 1: Voorbereiding

Voordat u begint, moet u ervoor zorgen dat u Aspose.Cells voor .NET hebt geïnstalleerd en een C#-project hebt gemaakt in de geïntegreerde ontwikkelomgeving (IDE) van uw voorkeur. Zorg er ook voor dat u een kopie heeft van het Excel-bestand dat u wilt manipuleren.

## Stap 2: Importeer de vereiste bibliotheken

 Importeer in uw C#-bronbestand de benodigde bibliotheken uit Aspose.Cells met behulp van de`using` richtlijn:

```csharp
using Aspose.Cells;
```

## Stap 3: Stel het bestandspad in

 Verklaar een`dataDir` variabele en initialiseer deze met de map die uw Excel-bestand bevat. Bijvoorbeeld :

```csharp
string dataDir = "PATH_TO_YOUR_DOCUMENT_DIRECTORY";
```

 Zeker vervangen`"PATH_TO_YOUR_DOCUMENT_DIRECTORY"` met het daadwerkelijke pad naar uw directory.

## Stap 4: Bestaand Excel-bestand laden

 Gebruik de`Workbook` class uit Aspose.Cells om het bestaande Excel-bestand te openen. Gebruik de`InputPath` variabele om het bestandspad op te geven:

```csharp
string InputPath = dataDir + "book1.xls";
Workbook wb = new Workbook(InputPath);
```

 Zorg ervoor dat je vervangen hebt`"book1.xls"` met de werkelijke naam van uw Excel-bestand.

## Stap 5: Kopieer het werkblad

 Nu kopiëren we het bestaande werkblad naar een nieuw werkblad. Gebruik de`Worksheets` eigendom van de`Workbook` object om toegang te krijgen tot de verzameling werkbladen:

```csharp
WorksheetCollection sheets = wb.Worksheets;
```

 Gebruik dan de`AddCopy` methode om het opgegeven werkblad te kopiëren. Om bijvoorbeeld 'Blad1' te kopiëren:

```csharp
sheets.AddCopy("Sheet1");
```

## Stap 6: Sla het Excel-bestand op

 Gebruik de`Save` werkwijze van de`Workbook` object om wijzigingen in een nieuw bestand op te slaan:

```csharp
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

Zorg ervoor dat u het gewenste pad en de gewenste bestandsnaam voor het uitvoerbestand opgeeft.

### Voorbeeldbroncode voor Excel Copy Worksheet met Aspose.Cells voor .NET 

```csharp
//Het pad naar de documentenmap.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Open een bestaand Excel-bestand.
Workbook wb = new Workbook(InputPath);
// Maak een Worksheets-object met verwijzing naar
// de bladen van het Werkboek.
WorksheetCollection sheets = wb.Worksheets;
// Kopieer gegevens naar een nieuw blad van een bestaand blad
// blad in de werkmap.
sheets.AddCopy("Sheet1");
// Sla het Excel-bestand op.
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

## Conclusie

Gefeliciteerd! U hebt nu geleerd hoe u een Excel-werkblad kunt kopiëren met Aspose.Cells voor .NET. Deze stapsgewijze handleiding liet zien hoe u de benodigde bibliotheken importeert, een bestaand Excel-bestand laadt, het werkblad kopieert en het gewijzigde bestand opslaat. Voel je vrij om deze methode in je eigen projecten te gebruiken om Excel-bestanden efficiënt te manipuleren.

### Veelgestelde vragen

#### V. Is Aspose.Cells compatibel met andere programmeertalen?

A. Ja, Aspose.Cells ondersteunt meerdere programmeertalen, waaronder C#, Java, Python en nog veel meer.

#### V. Kan ik een werkblad naar een andere Excel-werkmap kopiëren?

A.  Ja, u kunt gebruik maken van de`AddCopy` methode om een werkblad naar een andere Excel-werkmap te kopiëren.

#### V. Behoudt Aspose.Cells formules en opmaak bij het kopiëren van het werkblad?

A. Ja, Aspose.Cells behoudt formules, opmaak en andere eigenschappen bij het kopiëren van een werkblad.

#### V. Heeft Aspose.Cells een licentie nodig voor commercieel gebruik?

A. Ja, Aspose.Cells is een commercieel product en vereist de aankoop van een licentie voor commercieel gebruik. Meer licentie-informatie vindt u op de officiële website van Aspose.