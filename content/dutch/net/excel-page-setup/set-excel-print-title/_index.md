---
title: Excel-afdruktitel instellen
linktitle: Excel-afdruktitel instellen
second_title: Aspose.Cells voor .NET API-referentie
description: Leer eenvoudig Excel-bestanden manipuleren en afdrukopties aanpassen met Aspose.Cells voor .NET.
type: docs
weight: 170
url: /nl/net/excel-page-setup/set-excel-print-title/
---
In deze handleiding laten we u zien hoe u afdruktitels in een Excel-spreadsheet kunt instellen met behulp van Aspose.Cells voor .NET. Volg de onderstaande stappen om deze taak te volbrengen.

## Stap 1: De omgeving instellen

Zorg ervoor dat u uw ontwikkelomgeving hebt ingesteld en Aspose.Cells voor .NET hebt geïnstalleerd. U kunt de nieuwste versie van de bibliotheek downloaden van de officiële website van Aspose.

## Stap 2: Importeer de vereiste naamruimten

Importeer in uw C#-project de benodigde naamruimten om met Aspose.Cells te werken:

```csharp
using Aspose.Cells;
```

## Stap 3: Het pad naar de documentenmap instellen

 Verklaar een`dataDir` variabele om het pad op te geven naar de map waar u het gegenereerde Excel-bestand wilt opslaan:

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Zeker vervangen`"YOUR_DOCUMENT_DIRECTORY"` met het juiste pad op uw systeem.

## Stap 4: Een werkmapobject maken

Instantieer een werkmapobject dat de Excel-werkmap vertegenwoordigt die u wilt maken:

```csharp
Workbook workbook = new Workbook();
```

## Stap 5: Toegang tot het eerste werkblad

Navigeer naar het eerste werkblad in de Excel-werkmap met behulp van de volgende code:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Stap 6: Titelkolommen definiëren

Definieer de titelkolommen met behulp van de volgende code:

```csharp
pageSetup.PrintTitleColumns = "$A:$B";
```

Hier hebben we kolommen A en B gedefinieerd als titelkolommen. U kunt deze waarde aanpassen aan uw behoeften.

## Stap 7: Titelregels definiëren

Definieer de titelregels met behulp van de volgende code:

```csharp
pageSetup.PrintTitleRows = "$1:$2";
```

We hebben rijen 1 en 2 gedefinieerd als titelrijen. U kunt deze waarden aanpassen aan uw behoeften.

## Stap 8: De Excel-werkmap opslaan

 Om de Excel-werkmap op te slaan met de gedefinieerde afdruktitels, gebruikt u de`Save` methode van het Workbook-object:

```csharp
workbook.Save(dataDir + "SetPrintTitle_out.xls");
```

Hiermee wordt de Excel-werkmap met de bestandsnaam "SetPrintTitle_out.xls" in de opgegeven map opgeslagen.

### Voorbeeldbroncode voor Excel Print Title instellen met Aspose.Cells voor .NET 
```csharp
//Het pad naar de documentenmap.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Een werkmapobject instantiëren
Workbook workbook = new Workbook();
// De referentie van de PageSetup van het werkblad verkrijgen
Aspose.Cells.PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Kolomnummers A en B definiëren als titelkolommen
pageSetup.PrintTitleColumns = "$A:$B";
// Rijnummers 1 en 2 definiëren als titelrijen
pageSetup.PrintTitleRows = "$1:$2";
// Sla de werkmap op.
workbook.Save(dataDir + "SetPrintTitle_out.xls");
```

## Conclusie

Gefeliciteerd! U hebt geleerd hoe u afdruktitels in een Excel-spreadsheet kunt instellen met behulp van Aspose.Cells voor .NET. Met afdruktitels kunt u specifieke rijen en kolommen op elke afgedrukte pagina weergeven, waardoor gegevens gemakkelijker te lezen en te raadplegen zijn.

### Veelgestelde vragen

#### 1. Kan ik printtitels instellen voor specifieke kolommen in Excel?

 Ja, met Aspose.Cells voor .NET kunt u specifieke kolommen instellen als printtitels met behulp van de`PrintTitleColumns` eigendom van de`PageSetup` voorwerp.

#### 2. Is het mogelijk om zowel kolomtitels als rijtitels te definiëren?

 Ja, u kunt zowel kolom- als rijtitels afdrukken met behulp van de`PrintTitleColumns` En`PrintTitleRows` eigenschappen van de`PageSetup` voorwerp.

#### 3. Welke andere lay-outinstellingen kan ik aanpassen met Aspose.Cells voor .NET?

Met Aspose.Cells voor .NET kunt u verschillende instellingen voor de pagina-indeling aanpassen, zoals marges, paginarichting, afdrukschaal en meer.