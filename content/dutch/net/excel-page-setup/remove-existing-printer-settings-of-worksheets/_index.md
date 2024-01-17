---
title: Verwijder bestaande printerinstellingen van werkbladen
linktitle: Verwijder bestaande printerinstellingen van werkbladen
second_title: Aspose.Cells voor .NET API-referentie
description: Leer hoe u bestaande printerinstellingen uit Excel-spreadsheets verwijdert met Aspose.Cells voor .NET.
type: docs
weight: 80
url: /nl/net/excel-page-setup/remove-existing-printer-settings-of-worksheets/
---
In deze zelfstudie laten we u stap voor stap zien hoe u bestaande printerinstellingen uit werkbladen in Excel kunt verwijderen met behulp van Aspose.Cells voor .NET. We zullen C#-broncode gebruiken om het proces te illustreren.

## Stap 1: De omgeving instellen

Zorg ervoor dat Aspose.Cells voor .NET op uw computer is geïnstalleerd. Maak ook een nieuw project aan in de ontwikkelomgeving van uw voorkeur.

## Stap 2: Importeer de benodigde bibliotheken

Importeer in uw codebestand de bibliotheken die nodig zijn om met Aspose.Cells te werken. Hier is de bijbehorende code:

```csharp
using Aspose.Cells;
```

## Stap 3: Stel de bron- en uitvoermappen in

Stel de bron- en uitvoermappen in waar het originele Excel-bestand zich bevindt en waar u het gewijzigde bestand wilt opslaan. Gebruik de volgende code:

```csharp
string sourceDir = "SOURCE DIRECTORY PATH";
string outputDir = "OUTPUT DIRECTORY PATH";
```

Zorg ervoor dat u volledige mappaden opgeeft.

## Stap 4: Het bron-Excel-bestand laden

Laad het bron-Excel-bestand met de volgende code:

```csharp
Workbook wb = new Workbook(sourceDir + "fileName.xlsx");
```

Hierdoor wordt het opgegeven Excel-bestand in het werkmapobject geladen.

## Stap 5: Navigeer door de werkbladen

Doorloop alle werkbladen in de werkmap met behulp van een lus. Gebruik de volgende code:

```csharp
int sheetCount = wb. Worksheets. Count;

for (int i = 0; i < sheetCount; i++)
{
     Worksheet ws = wb.Worksheets[i];
     // De rest van de code wordt in de volgende stap toegevoegd.
}
```

## Stap 6: Bestaande printerinstellingen verwijderen

Controleer of er voor elk werkblad printerinstellingen bestaan en verwijder deze indien nodig. Gebruik de volgende code:

```csharp
PageSetup ps = ws.PageSetup;

if (ps.PrinterSettings != null)
{
     Console.WriteLine("Printer settings for this spreadsheet exist.");
     Console.WriteLine("Sheet name: " + ws.Name);
     Console.WriteLine("Paper size: " + ps.PaperSize);

     ps.PrinterSettings = null;

     Console.WriteLine("Printer settings for this spreadsheet have been removed by setting them to null.");
     Console.WriteLine("");
}
```

## Stap 7: De gewijzigde werkmap opslaan

Sla de gewijzigde werkmap op met behulp van de volgende code:

```csharp
wb.Save(outputDir + "modifiedFilename.xlsx");
```

Hiermee wordt de gewijzigde werkmap opgeslagen in de opgegeven uitvoermap.

### Voorbeeldbroncode voor het verwijderen van bestaande printerinstellingen van werkbladen met Aspose.Cells voor .NET 
```csharp
//Bronmap
string sourceDir = RunExamples.Get_SourceDirectory();
//Uitvoermap
string outputDir = RunExamples.Get_OutputDirectory();
//Bron-Excel-bestand laden
Workbook wb = new Workbook(sourceDir + "sampleRemoveExistingPrinterSettingsOfWorksheets.xlsx");
//Haal het aantal vellen van de werkmap op
int sheetCount = wb.Worksheets.Count;
//Herhaal alle bladen
for (int i = 0; i < sheetCount; i++)
{
    //Open het i-de werkblad
    Worksheet ws = wb.Worksheets[i];
    //Toegang tot de werkbladpagina-instellingen
    PageSetup ps = ws.PageSetup;
    //Controleer of er printerinstellingen voor dit werkblad bestaan
    if (ps.PrinterSettings != null)
    {
        //Druk het volgende bericht af
        Console.WriteLine("PrinterSettings of this worksheet exist.");
        //Druk de bladnaam en het papierformaat ervan af
        Console.WriteLine("Sheet Name: " + ws.Name);
        Console.WriteLine("Paper Size: " + ps.PaperSize);
        //Verwijder de printerinstellingen door ze op nul te zetten
        ps.PrinterSettings = null;
        Console.WriteLine("Printer settings of this worksheet are now removed by setting it null.");
        Console.WriteLine("");
    }//als
}//voor
//Sla de werkmap op
wb.Save(outputDir + "outputRemoveExistingPrinterSettingsOfWorksheets.xlsx");
```

## Conclusie

U hebt nu geleerd hoe u bestaande printerinstellingen uit werkbladen in Excel kunt verwijderen met Aspose.Cells voor .NET. In deze zelfstudie wordt u door elke stap van het proces geleid, van het instellen van de omgeving tot het navigeren door spreadsheets en het wissen van printerinstellingen. Deze kennis kunt u nu gebruiken om printerinstellingen in uw Excel-bestanden te beheren.

### Veelgestelde vragen

#### Vraag 1: Hoe weet ik of een spreadsheet bestaande printerinstellingen heeft?

 A1: U kunt controleren of er printerinstellingen voor een werkblad bestaan door naar het bestand te gaan`PrinterSettings` eigendom van de`PageSetup` voorwerp. Als de waarde niet nul is, betekent dit dat er bestaande printerinstellingen zijn.

#### Vraag 2: Kan ik de printerinstellingen alleen voor een specifiek spreadsheet verwijderen?

 A2: Ja, u kunt dezelfde aanpak gebruiken om printerinstellingen voor een specifiek werkblad te verwijderen door naar de map van dat werkblad te gaan.`PageSetup` voorwerp.

#### Vraag 3: Verwijdert deze methode ook andere lay-outinstellingen?

A3: Nee, met deze methode worden alleen printerinstellingen verwijderd. Andere lay-outinstellingen, zoals marges, papierrichting, enz., blijven ongewijzigd.

#### Vraag 4: Werkt deze methode voor alle Excel-bestandsindelingen, zoals .xls en .xlsx?

A4: Ja, deze methode werkt voor alle Excel-bestandsindelingen die worden ondersteund door Aspose.Cells, inclusief .xls en .xlsx.

#### Vraag 5: Zijn wijzigingen in de printerinstellingen permanent in het bewerkte Excel-bestand?

A5: Ja, wijzigingen in de printerinstellingen worden permanent opgeslagen in het bewerkte Excel-bestand.