---
title: Toon en verberg rijkolomkoppen van het werkblad
linktitle: Toon en verberg rijkolomkoppen van het werkblad
second_title: Aspose.Cells voor .NET API-referentie
description: Toon of verberg rij- en kolomkoppen in het Excel-werkblad met Aspose.Cells voor .NET.
type: docs
weight: 40
url: /nl/net/excel-display-settings-csharp-tutorials/display-and-hide-row-column-headers-of-worksheet/
---
In deze zelfstudie laten we u zien hoe u rij- en kolomkoppen van een Excel-werkblad kunt weergeven of verbergen met behulp van C#-broncode met Aspose.Cells voor .NET. Volg onderstaande stappen om het gewenste resultaat te verkrijgen.

## Stap 1: Importeer de benodigde bibliotheken

Zorg ervoor dat u de Aspose.Cells-bibliotheek voor .NET hebt geïnstalleerd en importeer de benodigde bibliotheken in uw C#-project.

```csharp
using Aspose.Cells;
using System.IO;
```

## Stap 2: Stel het mappad in en open het Excel-bestand

 Stel het pad in naar de map die uw Excel-bestand bevat en open vervolgens het bestand door een bestandsstream te maken en een`Workbook` voorwerp.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## Stap 3: Ga naar het eerste werkblad en verberg de rij- en kolomkoppen

 Open het eerste werkblad in het Excel-bestand met behulp van de`Worksheets` eigendom van de`Workbook` voorwerp. Gebruik dan de`IsRowColumnHeadersVisible` eigendom van de`Worksheet` object om de rij- en kolomkoppen te verbergen.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. IsRowColumnHeadersVisible = false;
```

## Stap 4: Wijzigingen opslaan

 Nadat u de nodige wijzigingen heeft aangebracht, slaat u het gewijzigde Excel-bestand op met behulp van de`Save` werkwijze van de`Workbook` voorwerp.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Voorbeeldbroncode voor het weergeven en verbergen van rijkolomkoppen van werkbladen met Aspose.Cells voor .NET 
```csharp
//Het pad naar de documentenmap.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Een bestandsstream maken met het te openen Excel-bestand
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Een werkmapobject instantiëren
// Het Excel-bestand openen via de bestandsstream
Workbook workbook = new Workbook(fstream);
// Toegang tot het eerste werkblad in het Excel-bestand
Worksheet worksheet = workbook.Worksheets[0];
// De kopteksten van rijen en kolommen verbergen
worksheet.IsRowColumnHeadersVisible = false;
// Het gewijzigde Excel-bestand opslaan
workbook.Save(dataDir + "output.xls");
// De bestandsstroom sluiten om alle bronnen vrij te maken
fstream.Close(); 
```

## Conclusie

Deze stapsgewijze handleiding liet u zien hoe u rij- en kolomkoppen in een Excel-spreadsheet kunt weergeven of verbergen met Aspose.Cells voor .NET. Met behulp van de meegeleverde C#-broncode kunt u eenvoudig de weergave van headers in uw Excel-bestanden aanpassen.

### Veelgestelde vragen (FAQ)

#### Wat is Aspose.Cells voor .NET?

Aspose.Cells voor .NET is een krachtige bibliotheek voor het manipuleren van Excel-bestanden in .NET-toepassingen.

#### Hoe kan ik Aspose.Cells voor .NET installeren?

 Om Aspose.Cells voor .NET te installeren, moet u het relevante pakket downloaden van[Aspose-releases](https://releases/aspose.com/cells/net/) en voeg het toe aan uw .NET-project.

#### Hoe kan ik rij- en kolomkoppen van een Excel-spreadsheet weergeven of verbergen met Aspose.Cells voor .NET?

 U kunt gebruik maken van de`IsRowColumnHeadersVisible` eigendom van de`Worksheet`object om rij- en kolomkoppen weer te geven of te verbergen. Stel het in`true` om ze te laten zien en aan`false` om ze te verbergen.

#### Welke andere Excel-bestandsindelingen worden ondersteund door Aspose.Cells voor .NET?

Aspose.Cells voor .NET ondersteunt verschillende Excel-bestandsindelingen, zoals XLS, XLSX, CSV, HTML, PDF en nog veel meer.
