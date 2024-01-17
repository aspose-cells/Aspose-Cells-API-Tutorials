---
title: Excel-werkblad kopiëren uit andere werkmap
linktitle: Excel-werkblad kopiëren uit andere werkmap
second_title: Aspose.Cells voor .NET API-referentie
description: Kopieer eenvoudig een Excel-werkblad van de ene werkmap naar de andere met Aspose.Cells voor .NET.
type: docs
weight: 10
url: /nl/net/excel-copy-worksheet/excel-copy-worksheet-from-other-workbook/
---
In deze zelfstudie leiden we u door de stappen om een Excel-werkblad uit een andere werkmap te kopiëren met behulp van de Aspose.Cells-bibliotheek voor .NET. Volg de onderstaande instructies om deze taak te voltooien.

## Stap 1: Voorbereiding

Voordat u begint, moet u ervoor zorgen dat u Aspose.Cells voor .NET hebt geïnstalleerd en een C#-project hebt gemaakt in de geïntegreerde ontwikkelomgeving (IDE) van uw voorkeur.

## Stap 2: Stel het pad naar de documentmap in

 Verklaar een`dataDir` variabele en initialiseer deze met het pad naar uw documentenmap. Bijvoorbeeld :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Zeker vervangen`"YOUR_DOCUMENTS_DIRECTORY"` met het daadwerkelijke pad naar uw directory.

## Stap 3: Maak een nieuwe Excel-werkmap

 Gebruik de`Workbook` klasse van Aspose.Cells om een nieuwe Excel-werkmap te maken:

```csharp
Workbook excelWorkbook0 = new Workbook();
```

## Stap 4: Haal het eerste werkblad in de werkmap op

Navigeer naar het eerste werkblad in de werkmap met index 0:

```csharp
Worksheet ws0 = excelWorkbook0.Worksheets[0];
```

## Stap 5: Gegevens toevoegen aan koprijen (A1:A4)

 Gebruik een`for` lus om gegevens toe te voegen aan de koprijen (A1:A4):

```csharp
for (int i = 0; i < 5; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Header row {0}", i));
}
```

## Stap 6: Gedetailleerde gegevens toevoegen (A5:A999)

 Gebruik een andere`for` lus om gedetailleerde gegevens toe te voegen (A5:A999):

```csharp
for (int i = 5; i < 1000; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Detail row {0}", i));
}
```

## Stap 7: Stel de lay-outopties in

 Stel pagina-instellingsopties voor het werkblad in met behulp van de`PageSetup` voorwerp:

```csharp
PageSetup pagesetup = ws0.PageSetup;
pagesetup.PrintTitleRows = "$1:$5";
```

## Stap 8: Maak nog een Excel-werkmap

Maak nog een Excel-werkmap:

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## Stap 9: Haal het eerste werkblad uit de tweede werkmap

Navigeer naar het eerste werkblad in de tweede werkmap:

```csharp
Worksheet ws1 = excelWorkbook1.Worksheets[0];
```

## Stap 10: Geef het werkblad een naam

noem het vuur

reken eiland:

```csharp
ws1.Name = "MySheet";
```

## Stap 11: Kopieer gegevens van het eerste werkblad van de eerste werkmap naar het eerste werkblad van de tweede werkmap

Kopieer de gegevens van het eerste werkblad van de eerste werkmap naar het eerste werkblad van de tweede werkmap:

```csharp
ws1.Copy(ws0);
```

## Stap 12: Sla het Excel-bestand op

Sla het Excel-bestand op:

```csharp
excelWorkbook1.Save(dataDir + "CopyWorkbookSheetToOther_out.xls");
```

Zorg ervoor dat u het gewenste pad en de gewenste bestandsnaam voor het uitvoerbestand opgeeft.

### Voorbeeldbroncode voor Excel Kopieer het werkblad uit een andere werkmap met Aspose.Cells voor .NET 
```csharp
//Het pad naar de documentenmap.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Maak een nieuwe werkmap.
Workbook excelWorkbook0 = new Workbook();
// Haal het eerste werkblad uit het boek.
Worksheet ws0 = excelWorkbook0.Worksheets[0];
// Plaats enkele gegevens in koprijen (A1:A4)
for (int i = 0; i < 5; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Header Row {0}", i));
}
// Voeg enkele detailgegevens toe (A5:A999)
for (int i = 5; i < 1000; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Detail Row {0}", i));
}
// Definieer een pagesetup-object op basis van het eerste werkblad.
PageSetup pagesetup = ws0.PageSetup;
// De eerste vijf rijen worden op elke pagina herhaald...
// Het is te zien in het afdrukvoorbeeld.
pagesetup.PrintTitleRows = "$1:$5";
// Maak nog een werkmap.
Workbook excelWorkbook1 = new Workbook();
// Haal het eerste werkblad uit het boek.
Worksheet ws1 = excelWorkbook1.Worksheets[0];
// Geef het werkblad een naam.
ws1.Name = "MySheet";
// Kopieer gegevens van het eerste werkblad van de eerste werkmap naar het
// eerste werkblad van de tweede werkmap.
ws1.Copy(ws0);
// Sla het Excel-bestand op.
excelWorkbook1.Save(dataDir + "CopyWorksheetFromWorkbookToOther_out.xls");
```

## Conclusie

Gefeliciteerd! U hebt nu geleerd hoe u een Excel-werkblad uit een andere werkmap kunt kopiëren met Aspose.Cells voor .NET. Voel je vrij om deze methode in je eigen projecten te gebruiken om Excel-bestanden efficiënt te manipuleren.

### Veelgestelde vragen

#### V. Welke bibliotheken zijn nodig om Aspose.Cells voor .NET te gebruiken?

A. Als u Aspose.Cells voor .NET wilt gebruiken, moet u de Aspose.Cells-bibliotheek in uw project opnemen. Zorg ervoor dat u correct naar deze bibliotheek verwijst in uw geïntegreerde ontwikkelomgeving (IDE).

#### V. Ondersteunt Aspose.Cells andere Excel-bestandsindelingen, zoals XLSX?

A. Ja, Aspose.Cells ondersteunt verschillende Excel-bestandsindelingen, waaronder XLSX, XLS, CSV, HTML en nog veel meer. U kunt deze bestandsformaten manipuleren met behulp van de functies van Aspose.Cells voor .NET.

#### V. Kan ik de lay-outopties aanpassen wanneer ik het werkblad kopieer?

A.  Ja, u kunt de opties voor de pagina-instelling aanpassen wanneer u het werkblad kopieert met behulp van de eigenschappen van het`PageSetup` voorwerp. U kunt paginakopteksten, voetteksten, marges, oriëntaties, enz. opgeven.