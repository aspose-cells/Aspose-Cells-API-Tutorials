---
title: Excel-werkbladen kopiëren tussen werkmappen
linktitle: Excel-werkbladen kopiëren tussen werkmappen
second_title: Aspose.Cells voor .NET API-referentie
description: Kopieer eenvoudig werkbladen tussen Excel-werkmappen met Aspose.Cells voor .NET.
type: docs
weight: 30
url: /nl/net/excel-copy-worksheet/excel-copy-worksheets-between-workbooks/
---
In deze zelfstudie begeleiden we u bij de stappen voor het kopiëren van werkbladen tussen Excel-werkmappen met behulp van de Aspose.Cells-bibliotheek voor .NET. Volg de onderstaande instructies om deze taak te voltooien.

## Stap 1: Voorbereiding

Zorg ervoor dat u Aspose.Cells voor .NET hebt geïnstalleerd en een C#-project hebt gemaakt in de geïntegreerde ontwikkelomgeving (IDE) van uw voorkeur.

## Stap 2: Stel het pad naar de documentmap in

 Verklaar een`dataDir` variabele en initialiseer deze met het pad naar uw documentenmap. Bijvoorbeeld :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Zeker vervangen`"YOUR_DOCUMENTS_DIRECTORY"` met het daadwerkelijke pad naar uw directory.

## Stap 3: Definieer het invoerbestandspad

 Verklaar een`InputPath` variabele en initialiseer deze met het volledige pad van het Excel-bestand waaruit u het werkblad wilt kopiëren. Bijvoorbeeld :

```csharp
string InputPath = dataDir + "book1.xls";
```

 Zorg ervoor dat u het Excel-bestand hebt`book1.xls` in uw documentenmap of geef de juiste bestandsnaam en locatie op.

## Stap 4: Maak een eerste Excel-werkmap

 Gebruik de`Workbook` klasse Aspose.Cells om een eerste Excel-werkmap te maken en het opgegeven bestand te openen:

```csharp
Workbook excelWorkbook0 = new Workbook(InputPath);
```

## Stap 5: Maak een tweede Excel-werkmap

Maak een tweede Excel-werkmap:

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## Stap 6: Kopieer het werkblad van de eerste werkmap naar de tweede werkmap

 Gebruik de`Copy`methode om het eerste werkblad van de eerste werkmap naar de tweede werkmap te kopiëren:

```csharp
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
```

## Stap 7: Sla het Excel-bestand op

Sla het Excel-bestand met het gekopieerde spreadsheet op:

```csharp
excelWorkbook1.Save(dataDir + "Copy WorksheetsBetweenWorkbooks_out.xls");
```

Zorg ervoor dat u het gewenste pad en de gewenste bestandsnaam voor het uitvoerbestand opgeeft.

### Voorbeeldbroncode voor Excel Werkbladen kopiëren tussen werkmappen met Aspose.Cells voor .NET 
```csharp
//Het pad naar de documentenmap.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Maak een werkmap.
// Open een bestand in het eerste boek.
Workbook excelWorkbook0 = new Workbook(InputPath);
// Maak nog een werkmap.
Workbook excelWorkbook1 = new Workbook();
// Kopieer het eerste vel van het eerste boek naar het tweede boek.
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
// Bewaar het bestand.
excelWorkbook1.Save(dataDir + "CopyWorksheetsBetweenWorkbooks_out.xls");
```

## Conclusie

Gefeliciteerd! U hebt nu geleerd hoe u werkbladen tussen Excel-werkmappen kunt kopiëren met Aspose.Cells voor .NET. Voel je vrij om deze methode in je eigen projecten te gebruiken om Excel-bestanden efficiënt te manipuleren.

### Veelgestelde vragen

#### V. Welke bibliotheken zijn nodig om Aspose.Cells voor .NET te gebruiken?

A. Als u Aspose.Cells voor .NET wilt gebruiken, moet u de Aspose.Cells-bibliotheek in uw project opnemen. Zorg ervoor dat u correct naar deze bibliotheek verwijst in uw geïntegreerde ontwikkelomgeving (IDE).

#### V. Ondersteunt Aspose.Cells andere Excel-bestandsindelingen, zoals XLSX?

A. Ja, Aspose.Cells ondersteunt verschillende Excel-bestandsindelingen, waaronder XLSX, XLS, CSV, HTML en nog veel meer. U kunt deze bestandsformaten manipuleren met behulp van de functies van Aspose.Cells voor .NET.

#### V. Kan ik de lay-outopties aanpassen wanneer ik de spreadsheet kopieer?

A.  Ja, u kunt de opties voor de pagina-instelling aanpassen wanneer u het werkblad kopieert met behulp van de eigenschappen van het`PageSetup` voorwerp. U kunt paginakopteksten, voetteksten, marges, oriëntaties, enz. opgeven.