---
title: Deelvensters van het werkblad bevriezen
linktitle: Deelvensters van het werkblad bevriezen
second_title: Aspose.Cells voor .NET API-referentie
description: Bewerk eenvoudig vastgezette deelvensters van Excel-werkbladen met Aspose.Cells voor .NET.
type: docs
weight: 70
url: /nl/net/excel-display-settings-csharp-tutorials/freeze-panes-of-worksheet/
---
In deze zelfstudie laten we u zien hoe u deelvensters in een Excel-werkblad kunt vergrendelen met behulp van C#-broncode met Aspose.Cells voor .NET. Volg onderstaande stappen om het gewenste resultaat te verkrijgen.

## Stap 1: Importeer de benodigde bibliotheken

Zorg ervoor dat u de Aspose.Cells-bibliotheek voor .NET hebt geïnstalleerd en importeer de benodigde bibliotheken in uw C#-project.

```csharp
using Aspose.Cells;
```

## Stap 2: Stel het mappad in en open het Excel-bestand

 Stel het pad in naar de map die uw Excel-bestand bevat en open vervolgens het bestand door een`Workbook` voorwerp.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## Stap 3: Ga naar spreadsheet en pas de instellingen voor paneelvergrendeling toe

 Navigeer naar het eerste werkblad in het Excel-bestand met behulp van de`Worksheet` voorwerp. Gebruik dan de`FreezePanes` methode om de instellingen voor paneelvergrendeling toe te passen.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. FreezePanes(3, 2, 3, 2);
```

In het bovenstaande voorbeeld zijn de deelvensters vergrendeld op de cel in rij 3 en kolom 2.

## Stap 4: Wijzigingen opslaan

 Nadat u de nodige wijzigingen heeft aangebracht, slaat u het gewijzigde Excel-bestand op met behulp van de`Save` werkwijze van de`Workbook` voorwerp.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Voorbeeldbroncode voor het bevriezen van deelvensters van werkbladen met Aspose.Cells voor .NET 

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
// Instellingen voor vastzetvensters toepassen
worksheet.FreezePanes(3, 2, 3, 2);
// Het gewijzigde Excel-bestand opslaan
workbook.Save(dataDir + "output.xls");
// De bestandsstroom sluiten om alle bronnen vrij te maken
fstream.Close();
```

## Conclusie

In deze stapsgewijze handleiding werd uitgelegd hoe u deelvensters in een Excel-spreadsheet kunt vergrendelen met Aspose.Cells voor .NET. Met behulp van de meegeleverde C#-broncode kunt u eenvoudig de instellingen voor paneelvergrendeling aanpassen om uw gegevens in Excel-bestanden beter te organiseren en te visualiseren.

### Veelgestelde vragen (FAQ)

#### Wat is Aspose.Cells voor .NET?

Aspose.Cells voor .NET is een krachtige bibliotheek voor het manipuleren van Excel-bestanden in .NET-toepassingen.

#### Hoe kan ik Aspose.Cells voor .NET installeren?

 Om Aspose.Cells voor .NET te installeren, moet u het relevante pakket downloaden van[Aspose-releases](https://releases/aspose.com/cells/net/) en voeg het toe aan uw .NET-project.

#### Hoe deelvensters in een Excel-werkblad te vergrendelen met Aspose.Cells voor .NET?

 U kunt gebruik maken van de`FreezePanes` werkwijze van de`Worksheet` object om de deelvensters van een werkblad te vergrendelen. Geef de cellen op die u wilt vergrendelen door rij- en kolomindexen op te geven.

#### Kan ik de instellingen voor paneelvergrendeling aanpassen met Aspose.Cells voor .NET?

 Ja, met behulp van de`FreezePanes` Met de methode kunt u opgeven welke cellen indien nodig moeten worden vergrendeld, waarbij u de juiste rij- en kolomindexen opgeeft.
