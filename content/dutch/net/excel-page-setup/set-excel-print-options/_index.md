---
title: Excel-afdrukopties instellen
linktitle: Excel-afdrukopties instellen
second_title: Aspose.Cells voor .NET API-referentie
description: Leer Excel-bestanden manipuleren en afdrukopties eenvoudig aanpassen met Aspose.Cells voor .NET.
type: docs
weight: 150
url: /nl/net/excel-page-setup/set-excel-print-options/
---
In deze handleiding laten we u zien hoe u afdrukopties instelt voor een Excel-werkmap met behulp van Aspose.Cells voor .NET. We leiden u stap voor stap door de meegeleverde C#-broncode om deze taak te volbrengen.

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

## Stap 5: De PageSetup-referentie van het werkblad verkrijgen

Om de afdrukopties in te stellen, moeten we eerst de PageSetup-referentie uit het werkblad halen. Gebruik de volgende code om de referentie op te halen:

```csharp
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## Stap 6: Schakel het afdrukken van rasterlijnen in

Om het afdrukken van rasterlijnen mogelijk te maken, gebruikt u de volgende code:

```csharp
pageSetup. PrintGridlines = true;
```

## Stap 7: Schakel het afdrukken van rij-/kolomkoppen in

Gebruik de volgende code om het afdrukken van rij- en kolomkoppen in te schakelen:

```csharp
pageSetup.PrintHeadings = true;
```

## Stap 8: Zwart-witafdrukmodus inschakelen

Om het afdrukken van het werkblad in zwart-witmodus mogelijk te maken, gebruikt u de volgende code:

```csharp
pageSetup.BlackAndWhite = true;
```

## Stap 9: Feedback afdrukken inschakelen

Om ervoor te zorgen dat opmerkingen worden afgedrukt zoals ze in het spreadsheet verschijnen, gebruikt u de volgende code:

```csharp
pageSetup.PrintComments = PrintCommentsType.PrintInPlace;
```

## Stap 10: Afdrukken in conceptmodus inschakelen

Om het afdrukken van het spreadsheet in conceptmodus mogelijk te maken, gebruikt u de volgende code:

```csharp
pageSetup.PrintDraft = true;
```

## Stap 11: Schakel celfouten voor afdrukken in als N.v.t

Om ervoor te zorgen dat celfouten kunnen worden afgedrukt als

  dan N.v.t., gebruik de volgende code:

```csharp
pageSetup.PrintErrors = PrintErrorsType.PrintErrorsNA;
```

## Stap 12: De Excel-werkmap opslaan

 Om de Excel-werkmap op te slaan met de ingestelde afdrukopties, gebruikt u de`Save` methode van het Workbook-object:

```csharp
workbook.Save(dataDir + "OtherPrintOptions_out.xls");
```

Hiermee wordt de Excel-werkmap met de bestandsnaam "OtherPrintOptions_out.xls" in de opgegeven map opgeslagen.

### Voorbeeldbroncode voor Excel-afdrukopties instellen met Aspose.Cells voor .NET 
```csharp
//Het pad naar de documentenmap.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Een werkmapobject instantiëren
Workbook workbook = new Workbook();
// De referentie van de PageSetup van het werkblad verkrijgen
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Mogelijkheid om rasterlijnen af te drukken
pageSetup.PrintGridlines = true;
// Mogelijkheid om rij-/kolomkoppen af te drukken
pageSetup.PrintHeadings = true;
// Maakt het mogelijk om het werkblad in zwart-witmodus af te drukken
pageSetup.BlackAndWhite = true;
// Maakt het mogelijk om opmerkingen af te drukken zoals weergegeven op het werkblad
pageSetup.PrintComments = PrintCommentsType.PrintInPlace;
// Maakt het mogelijk om het werkblad af te drukken met conceptkwaliteit
pageSetup.PrintDraft = true;
// Mogelijkheid om celfouten af te drukken als N.v.t
pageSetup.PrintErrors = PrintErrorsType.PrintErrorsNA;
// Sla de werkmap op.
workbook.Save(dataDir + "OtherPrintOptions_out.xls");
```
## Conclusie

hebt nu geleerd hoe u afdrukopties voor een Excel-werkmap kunt instellen met Aspose.Cells voor .NET. Met deze krachtige en gebruiksvriendelijke bibliotheek kunt u de afdrukinstellingen van uw Excel-werkmappen op een eenvoudige en efficiënte manier aanpassen.

### Veelgestelde vragen


#### 1. Kan ik de afdrukopties, zoals marges of paginarichting, verder aanpassen?

Ja, Aspose.Cells voor .NET biedt een breed scala aan aanpasbare afdrukopties, zoals marges, paginarichting, schaal, enz.

#### 2. Ondersteunt Aspose.Cells voor .NET andere Excel-bestandsformaten?

Ja, Aspose.Cells voor .NET ondersteunt verschillende Excel-bestandsformaten, zoals XLSX, XLS, CSV, HTML, PDF, enz.

#### 3. Is Aspose.Cells voor .NET compatibel met alle versies van .NET Framework?

Aspose.Cells voor .NET is compatibel met .NET Framework 2.0 of hoger, inclusief versies 3.5, 4.0, 4.5, 4.6, enz.