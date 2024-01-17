---
title: Excel-afdrukkwaliteit instellen
linktitle: Excel-afdrukkwaliteit instellen
second_title: Aspose.Cells voor .NET API-referentie
description: Leer Excel-bestanden beheren en aanpassen, inclusief afdrukopties met Aspose.Cells voor .NET.
type: docs
weight: 160
url: /nl/net/excel-page-setup/set-excel-print-quality/
---
In deze handleiding leggen we uit hoe u de afdrukkwaliteit van een Excel-spreadsheet kunt instellen met Aspose.Cells voor .NET. We leiden u stap voor stap door de meegeleverde C#-broncode om deze taak te volbrengen.

## Stap 1: De omgeving instellen

Voordat u begint, moet u ervoor zorgen dat u uw ontwikkelomgeving hebt ingesteld en Aspose.Cells voor .NET hebt geïnstalleerd. U kunt de nieuwste versie van de bibliotheek downloaden van de officiële website van Aspose.

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

## Stap 6: De afdrukkwaliteit instellen

Gebruik de volgende code om de afdrukkwaliteit van het werkblad in te stellen:

```csharp
worksheet.PageSetup.PrintQuality = 180;
```

Hier hebben wij de printkwaliteit ingesteld op 180 dpi, maar u kunt deze waarde aanpassen aan uw wensen.

## Stap 7: De Excel-werkmap opslaan

 Om de Excel-werkmap met de gedefinieerde afdrukkwaliteit op te slaan, gebruikt u de`Save` methode van het Workbook-object:

```csharp
workbook.Save(dataDir + "SetPrintQuality_out.xls");
```

Hiermee wordt de Excel-werkmap met de bestandsnaam "SetPrintQuality_out.xls" in de opgegeven map opgeslagen.

### Voorbeeldbroncode voor Excel-afdrukkwaliteit instellen met Aspose.Cells voor .NET 
```csharp
//Het pad naar de documentenmap.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Een werkmapobject instantiëren
Workbook workbook = new Workbook();
// Toegang tot het eerste werkblad in het Excel-bestand
Worksheet worksheet = workbook.Worksheets[0];
// De afdrukkwaliteit van het werkblad instellen op 180 dpi
worksheet.PageSetup.PrintQuality = 180;
// Sla de werkmap op.
workbook.Save(dataDir + "SetPrintQuality_out.xls");
```

## Conclusie

Gefeliciteerd! U hebt geleerd hoe u de afdrukkwaliteit van een Excel-spreadsheet kunt instellen met Aspose.Cells voor .NET. U kunt nu de afdrukkwaliteit van uw Excel-bestanden aanpassen aan uw specifieke voorkeuren en behoeften.

## Veelgestelde vragen


#### 1. Kan ik de afdrukkwaliteit van verschillende werkbladen in hetzelfde Excel-bestand aanpassen?

Ja, u kunt de afdrukkwaliteit van elk werkblad afzonderlijk aanpassen door naar het bijbehorende werkbladobject te gaan en de juiste afdrukkwaliteit in te stellen.

#### 2. Welke andere afdrukopties kan ik aanpassen met Aspose.Cells voor .NET?

Naast de afdrukkwaliteit kunt u diverse andere afdrukopties aanpassen, zoals marges, paginarichting, afdrukschaal, enz.

#### 3. Ondersteunt Aspose.Cells voor .NET verschillende Excel-bestandsformaten?

Ja, Aspose.Cells voor .NET ondersteunt een breed scala aan Excel-bestandsindelingen, waaronder XLSX, XLS, CSV, HTML, PDF, enz.