---
title: Werkblad verbergen en zichtbaar maken
linktitle: Werkblad verbergen en zichtbaar maken
second_title: Aspose.Cells voor .NET API-referentie
description: Een krachtige bibliotheek voor het werken met Excel-bestanden, inclusief het maken, wijzigen en manipuleren van gegevens.
type: docs
weight: 90
url: /nl/net/excel-display-settings-csharp-tutorials/hide-and-unhide-worksheet/
---
In deze zelfstudie nemen we u stap voor stap mee om de volgende C#-broncode uit te leggen die wordt gebruikt om een werkblad te verbergen en weer te geven met Aspose.Cells voor .NET. Volg onderstaande stappen:

## Stap 1: De omgeving voorbereiden

Zorg ervoor dat Aspose.Cells voor .NET op uw systeem is geïnstalleerd voordat u begint. Als u het nog niet hebt geïnstalleerd, kunt u het downloaden van de officiële website van Aspose. Eenmaal geïnstalleerd, kunt u een nieuw project maken in de geïntegreerde ontwikkelomgeving (IDE) van uw voorkeur.

## Stap 2: Importeer de vereiste naamruimten

Voeg in uw C#-bronbestand de benodigde naamruimten toe om de functies van Aspose.Cells te gebruiken. Voeg de volgende regels toe aan het begin van uw bestand:

```csharp
using Aspose.Cells;
using System.IO;
```

## Stap 3: Laad het Excel-bestand

Voordat u een werkblad verbergt of zichtbaar maakt, moet u het Excel-bestand in uw toepassing laden. Zorg ervoor dat het Excel-bestand dat u wilt gebruiken in dezelfde map staat als uw project. Gebruik de volgende code om het Excel-bestand te laden:

```csharp
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

Zorg ervoor dat u "PAD NAAR UW DOCUMENTENMAP" vervangt door het daadwerkelijke pad naar de map die uw Excel-bestand bevat.

## Stap 4: Open de spreadsheet

Zodra het Excel-bestand is geladen, kunt u naar het werkblad navigeren dat u wilt verbergen of zichtbaar maken. Gebruik de volgende code om toegang te krijgen tot het eerste werkblad in het bestand:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Stap 5: Verberg het werkblad

 Nu u het werkblad hebt geopend, kunt u het verbergen met behulp van de`IsVisible` eigendom. Gebruik de volgende code om het eerste werkblad in het bestand te verbergen:

```csharp
worksheet. IsVisible = false;
```

## Stap 6: Geef het werkblad opnieuw weer

Als u het eerder verborgen werkblad opnieuw wilt weergeven, kunt u dezelfde code gebruiken door de waarde van de`IsVisible` eigendom. Gebruik de volgende code om het eerste werkblad opnieuw weer te geven:

```csharp
worksheet. IsVisible = true;
```

## Stap 7: Wijzigingen opslaan

Als je eenmaal

  Als u het werkblad indien nodig hebt verborgen of zichtbaar gemaakt, moet u de wijzigingen in het Excel-bestand opslaan. Gebruik de volgende code om wijzigingen op te slaan:

```csharp
workbook.Save(dataDir + "output.out.xls");
fstream.Close();
```

Zorg ervoor dat u het juiste uitvoerpad opgeeft om het gewijzigde Excel-bestand op te slaan.

### Voorbeeldbroncode voor werkblad verbergen en zichtbaar maken met Aspose.Cells voor .NET 

```csharp
//Het pad naar de documentenmap.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Een bestandsstream maken met het te openen Excel-bestand
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Een werkmapobject instantiëren door het Excel-bestand te openen via de bestandsstroom
Workbook workbook = new Workbook(fstream);
// Toegang tot het eerste werkblad in het Excel-bestand
Worksheet worksheet = workbook.Worksheets[0];
// Het eerste werkblad van het Excel-bestand verbergen
worksheet.IsVisible = false;
// Toont het eerste werkblad van het Excel-bestand
//Werkblad.IsVisible = waar;
// Het gewijzigde Excel-bestand opslaan in het standaardformaat (dat wil zeggen Excel 2003).
workbook.Save(dataDir + "output.out.xls");
// De bestandsstroom sluiten om alle bronnen vrij te maken
fstream.Close();
```

## Conclusie

Gefeliciteerd! Je hebt geleerd hoe je een spreadsheet kunt verbergen en weergeven met Aspose.Cells voor .NET. U kunt deze functie nu gebruiken om de zichtbaarheid van uw spreadsheets in uw Excel-bestanden te bepalen.

### Veelgestelde vragen (FAQ)

#### Hoe kan ik Aspose.Cells voor .NET installeren?

 U kunt Aspose.Cells voor .NET installeren door het relevante NuGet-pakket te downloaden van[Aspose-releases](https://releases/aspose.com/cells/net/) en voeg het toe aan uw Visual Studio-project.

#### Wat is de minimaal vereiste versie van .NET Framework om Aspose.Cells voor .NET te gebruiken?

Aspose.Cells voor .NET ondersteunt .NET Framework 2.0 en hoger.

#### Kan ik bestaande Excel-bestanden openen en bewerken met Aspose.Cells voor .NET?

Ja, u kunt bestaande Excel-bestanden openen en bewerken met Aspose.Cells voor .NET. U hebt toegang tot werkbladen, cellen, formules en andere elementen van het Excel-bestand.

#### Ondersteunt Aspose.Cells voor .NET rapportage en export naar andere bestandsformaten?

Ja, Aspose.Cells voor .NET ondersteunt het genereren van rapporten en het exporteren naar formaten zoals PDF, HTML, CSV, TXT, enz.

#### Is de wijziging van het Excel-bestand blijvend?

Ja, de bewerking van het Excel-bestand is permanent zodra u deze opslaat. Zorg ervoor dat u een reservekopie opslaat voordat u wijzigingen aanbrengt in het originele bestand.