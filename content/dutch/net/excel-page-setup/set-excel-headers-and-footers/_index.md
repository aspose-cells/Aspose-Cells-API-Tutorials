---
title: Excel-kop- en voetteksten instellen
linktitle: Excel-kop- en voetteksten instellen
second_title: Aspose.Cells voor .NET API-referentie
description: Leer hoe u kop- en voetteksten in Excel instelt met Aspose.Cells voor .NET.
type: docs
weight: 100
url: /nl/net/excel-page-setup/set-excel-headers-and-footers/
---

In deze zelfstudie laten we u stap voor stap zien hoe u kop- en voetteksten in Excel instelt met Aspose.Cells voor .NET. We zullen C#-broncode gebruiken om het proces te illustreren.

## Stap 1: De omgeving instellen

Zorg ervoor dat Aspose.Cells voor .NET op uw computer is geïnstalleerd. Maak ook een nieuw project aan in de ontwikkelomgeving van uw voorkeur.

## Stap 2: Importeer de benodigde bibliotheken

Importeer in uw codebestand de bibliotheken die nodig zijn om met Aspose.Cells te werken. Hier is de bijbehorende code:

```csharp
using Aspose.Cells;
```

## Stap 3: Stel de gegevensmap in

Stel de gegevensmap in waar u het gewijzigde Excel-bestand wilt opslaan. Gebruik de volgende code:

```csharp
string dataDir = "YOUR DATA DIRECTORY";
```

Zorg ervoor dat u het volledige mappad opgeeft.

## Stap 4: De werkmap en het werkblad maken

Maak een nieuw werkmapobject en navigeer naar het eerste werkblad in de werkmap met behulp van de volgende code:

```csharp
Workbook excel = new Workbook();
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
```

Hierdoor wordt een lege werkmap met een werkblad gemaakt en krijgt u toegang tot het PageSetup-object van dat werkblad.

## Stap 5: Kopteksten instellen

 Stel de spreadsheetkopteksten in met behulp van de`SetHeader` methoden van het PageSetup-object. Hier is een voorbeeldcode:

```csharp
pageSetup.SetHeader(0, "&A");
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
```

Hiermee worden respectievelijk de werkbladnaam, de huidige datum en tijd en de bestandsnaam in de headers ingesteld.

## Stap 6: Voetteksten definiëren

 Stel spreadsheetvoetteksten in met behulp van de`SetFooter` methoden van het PageSetup-object. Hier is een voorbeeldcode:

```csharp
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
pageSetup.SetFooter(1, "&P");
pageSetup.SetFooter(2, "&N");
```

Hierdoor wordt respectievelijk een tekstreeks, het huidige paginanummer en het totale aantal pagina's in de voetteksten ingesteld.

## Stap 7: De gewijzigde werkmap opslaan

Sla de gewijzigde werkmap op met behulp van de volgende code:

```csharp
excel.Save(dataDir + "OutputFileName.xls");
```

Hierdoor wordt de gewijzigde werkmap opgeslagen in de opgegeven gegevensmap.

### Voorbeeldbroncode voor Excel-kop- en voetteksten instellen met Aspose.Cells voor .NET 
```csharp
//Het pad naar de documentenmap.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Een werkmapobject instantiëren
Workbook excel = new Workbook();
// De referentie van de PageSetup van het werkblad verkrijgen
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
// Werkbladnaam instellen in het linkergedeelte van de koptekst
pageSetup.SetHeader(0, "&A");
//De huidige datum en huidige tijd instellen in het middengedeelte van de koptekst
// en het wijzigen van het lettertype van de koptekst
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
// De huidige bestandsnaam instellen in het rechtergedeelte van de header en het
// lettertype van de koptekst
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
// Een tekenreeks instellen in het linkergedeelte van de voettekst en het lettertype wijzigen
// van een deel van deze string ("123")
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
// Het huidige paginanummer instellen in het centrale gedeelte van de voettekst
pageSetup.SetFooter(1, "&P");
// Het aantal pagina's instellen in het rechtergedeelte van de voettekst
pageSetup.SetFooter(2, "&N");
// Sla de werkmap op.
excel.Save(dataDir + "SetHeadersAndFooters_out.xls");
```


## Conclusie

U hebt nu geleerd hoe u kop- en voetteksten in Excel kunt instellen met Aspose.Cells voor .NET. In deze zelfstudie wordt u door elke stap van het proces geleid, van het instellen van de omgeving tot het opslaan van de gewijzigde werkmap. Voel je vrij om de functies van Aspose.Cells verder te verkennen om verdere manipulaties in uw Excel-bestanden uit te voeren.

### Veelgestelde vragen (FAQ)

#### 1. Hoe kan ik Aspose.Cells voor .NET op mijn systeem installeren?
Om Aspose.Cells voor .NET te installeren, moet u het installatiepakket downloaden van de officiële website van Aspose en de instructies in de documentatie volgen.

#### 2. Werkt deze methode met alle versies van Excel?
Ja, de methode voor het instellen van kop- en voetteksten met Aspose.Cells voor .NET werkt met alle ondersteunde versies van Excel.

#### 3. Kan ik kop- en voetteksten verder aanpassen?
Ja, Aspose.Cells biedt een uitgebreid scala aan functies om kop- en voetteksten aan te passen, inclusief tekstplaatsing, kleur, lettertype, paginanummers en meer.

#### 4. Hoe kan ik dynamische informatie toevoegen aan kop- en voetteksten?
U kunt speciale variabelen en opmaakcodes gebruiken om dynamische informatie, zoals de huidige datum, tijd, bestandsnaam, paginanummer, enzovoort, aan kop- en voetteksten toe te voegen.

#### 5. Kan ik kop- en voetteksten verwijderen nadat ik deze heb ingesteld?
 Ja, u kunt kop- en voetteksten verwijderen met behulp van de`ClearHeaderFooter` werkwijze van de`PageSetup` voorwerp. Hiermee worden de standaard kop- en voetteksten hersteld.