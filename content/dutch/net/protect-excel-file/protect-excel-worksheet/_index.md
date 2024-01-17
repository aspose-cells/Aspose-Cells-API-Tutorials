---
title: Bescherm Excel-werkblad
linktitle: Bescherm Excel-werkblad
second_title: Aspose.Cells voor .NET API-referentie
description: Ontdek in deze tutorial hoe u een Excel-spreadsheet kunt beveiligen met Aspose.Cells voor .NET. Stap voor stap handleiding in C#.
type: docs
weight: 50
url: /nl/net/protect-excel-file/protect-excel-worksheet/
---
In deze zelfstudie bekijken we C#-broncode die de Aspose.Cells-bibliotheek gebruikt om een Excel-spreadsheet te beschermen. We doorlopen elke stap van de code en leggen uit hoe deze werkt. Zorg ervoor dat u de instructies zorgvuldig volgt om de gewenste resultaten te krijgen.

## Stap 1: Vereisten

Zorg ervoor dat u, voordat u begint, de Aspose.Cells-bibliotheek voor .NET hebt geïnstalleerd. Je kunt het verkrijgen via de officiële website van Aspose. Zorg er ook voor dat je over een recente versie van Visual Studio of een andere C#-ontwikkelomgeving beschikt.

## Stap 2: Importeer de vereiste naamruimten

Om de Aspose.Cells-bibliotheek te gebruiken, moeten we de benodigde naamruimten in onze code importeren. Voeg de volgende regels toe bovenaan uw C#-bronbestand:

```csharp
using Aspose.Cells;
using System.IO;
```

## Stap 3: Laad het Excel-bestand

In deze stap laden we het Excel-bestand dat we willen beschermen. Zorg ervoor dat u het juiste pad opgeeft naar de map die het Excel-bestand bevat. Gebruik de volgende code om het bestand te uploaden:

```csharp
// Pad naar de documentenmap.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Maak een stroom bestanden met het Excel-bestand dat u wilt openen.
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);

// Een werkmapobject instantiëren.
//Open Excel-bestand via bestandsstream.
Workbook excel = new Workbook(fstream);
```

 Zeker vervangen`"YOUR_DOCUMENTS_DIR"` met het juiste pad naar uw documentenmap.

## Stap 4: Open de spreadsheet

Nu we het Excel-bestand hebben geladen, hebben we toegang tot het eerste werkblad. Gebruik de volgende code om toegang te krijgen tot het eerste werkblad:

```csharp
// Toegang tot het eerste werkblad in het Excel-bestand.
Worksheet worksheet = excel.Worksheets[0];
```

## Stap 5: Bescherm het werkblad

In deze stap beveiligen we de spreadsheet met een wachtwoord. Gebruik de volgende code om de spreadsheet te beveiligen:

```csharp
// Beveilig het werkblad met een wachtwoord.
worksheet.Protect(ProtectionType.All, "YOUR_PASSWORD", null);
```

 Vervangen`"YOUR_PASSWORD"` met het wachtwoord dat u wilt gebruiken om de spreadsheet te beveiligen.

## Stap 6: Bewaar het gewijzigde Excel-bestand Nu we het hebben beveiligd

Voor het spreadsheet slaan we het gewijzigde Excel-bestand op in het standaardformaat. Gebruik de volgende code om het Excel-bestand op te slaan:

```csharp
// Sla het gewijzigde Excel-bestand op in het standaardformaat.
excel.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Zorg ervoor dat u het juiste pad opgeeft om het gewijzigde Excel-bestand op te slaan.

## Stap 7: Sluit de bestandsstream

Om alle bronnen vrij te geven, moeten we de bestandsstroom sluiten die wordt gebruikt om het Excel-bestand te laden. Gebruik de volgende code om de bestandsstream te sluiten:

```csharp
// Sluit de bestandsstroom om alle bronnen vrij te geven.
fstream.Close();
```

Zorg ervoor dat u deze stap aan het einde van uw code opneemt.


### Voorbeeldbroncode voor Protect Excel Worksheet met Aspose.Cells voor .NET 
```csharp
//Het pad naar de documentenmap.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Een bestandsstream maken met het te openen Excel-bestand
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Een werkmapobject instantiëren
// Het Excel-bestand openen via de bestandsstream
Workbook excel = new Workbook(fstream);
// Toegang tot het eerste werkblad in het Excel-bestand
Worksheet worksheet = excel.Worksheets[0];
// Het werkblad beveiligen met een wachtwoord
worksheet.Protect(ProtectionType.All, "aspose", null);
// Het gewijzigde Excel-bestand opslaan in het standaardformaat
excel.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
// De bestandsstroom sluiten om alle bronnen vrij te maken
fstream.Close();
```

## Conclusie

Gefeliciteerd! U beschikt nu over C#-broncode waarmee u een Excel-spreadsheet kunt beveiligen met behulp van de Aspose.Cells-bibliotheek voor .NET. Zorg ervoor dat u de stappen zorgvuldig volgt en de code aanpast aan uw specifieke behoeften.

### Veelgestelde vragen (veelgestelde vragen)

#### Is het mogelijk om meerdere werkbladen in één Excel-bestand te beveiligen?

A: Ja, u kunt meerdere werkbladen in één Excel-bestand beveiligen door stap 4-6 voor elk werkblad te herhalen.

#### Hoe kan ik specifieke machtigingen voor geautoriseerde gebruikers opgeven?

 A: U kunt gebruik maken van de extra opties van de`Protect`methode om specifieke machtigingen voor geautoriseerde gebruikers op te geven. Zie de Aspose.Cells-documentatie voor meer informatie.

#### Kan ik het Excel-bestand zelf beveiligen met een wachtwoord?

A: Ja, u kunt het Excel-bestand zelf met een wachtwoord beveiligen met behulp van andere methoden die door de Aspose.Cells-bibliotheek worden aangeboden. Raadpleeg de documentatie voor specifieke voorbeelden.

#### Ondersteunt de Aspose.Cells-bibliotheek andere Excel-bestandsindelingen?

A: Ja, de Aspose.Cells-bibliotheek ondersteunt een breed scala aan Excel-bestandsindelingen, waaronder XLSX, XLSM, XLSB, CSV, enz.