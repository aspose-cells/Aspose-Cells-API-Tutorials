---
title: Bescherm specifieke cellen in een Excel-werkblad
linktitle: Bescherm specifieke cellen in een Excel-werkblad
second_title: Aspose.Cells voor .NET API-referentie
description: Leer hoe u specifieke cellen in Excel kunt beschermen met Aspose.Cells voor .NET. Stap voor stap tutorial in C#.
type: docs
weight: 70
url: /nl/net/protect-excel-file/protect-specific-cells-in-a-excel-worksheet/
---
In deze zelfstudie bekijken we de C#-broncode die de Aspose.Cells-bibliotheek gebruikt om specifieke cellen in een Excel-spreadsheet te beschermen. We doorlopen elke stap van de code en leggen uit hoe deze werkt. Volg de instructies zorgvuldig om de gewenste resultaten te krijgen.

## Stap 1: Vereisten

Zorg ervoor dat u, voordat u begint, de Aspose.Cells-bibliotheek voor .NET hebt geïnstalleerd. Je kunt het verkrijgen via de officiële website van Aspose. Zorg er ook voor dat je over een recente versie van Visual Studio of een andere C#-ontwikkelomgeving beschikt.

## Stap 2: Importeer de vereiste naamruimten

Om de Aspose.Cells-bibliotheek te gebruiken, moeten we de benodigde naamruimten in onze code importeren. Voeg de volgende regels toe bovenaan uw C#-bronbestand:

```csharp
using Aspose.Cells;
```

## Stap 3: Een Excel-werkmap maken

In deze stap gaan we een nieuwe Excel-werkmap maken. Gebruik de volgende code om een Excel-werkmap te maken:

```csharp
// Pad naar de documentenmap.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Maak een nieuwe werkmap.
Workbook wb = new Workbook();
```

 Zeker vervangen`"YOUR_DOCUMENTS_DIR"` met het juiste pad naar uw documentenmap.

## Stap 4: Een spreadsheet maken

Nu we de Excel-werkmap hebben gemaakt, gaan we een werkblad maken en het eerste blad ophalen. Gebruik de volgende code:

```csharp
// Maak een spreadsheetobject en haal het eerste blad op.
Worksheet sheet = wb.Worksheets[0];
```

## Stap 5: De stijl definiëren

In deze stap definiëren we de stijl die op specifieke cellen moet worden toegepast. Gebruik de volgende code:

```csharp
// Definitie van het stijlobject.
Styling styling;
```

## Stap 6: Loop om alle kolommen te ontgrendelen

Nu zullen we alle kolommen in het werkblad doorlopen en ze ontgrendelen. Gebruik de volgende code:

```csharp
// Loop door alle kolommen in het werkblad en ontgrendel ze.
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style);
}
```

## Stap 7: Specifieke cellen vergrendelen

In deze stap vergrendelen we specifieke cellen. Gebruik de volgende code:

```csharp
//Alle drie de cellen vergrendelen... dwz A1, B1, C1.
style = sheet.Cells["A1"].GetStyle();
style. IsLocked = true;
sheet.Cells["A1"].SetStyle(style);

style = sheet.Cells["B1"].GetStyle();
style. IsLocked = true;
sheet.Cells["B1"].SetStyle(style);

style = sheet.Cells["C1"].GetStyle();
style. IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
```

## Stap 8: Het werkblad beschermen

Ten slotte beschermen we het werkblad om te voorkomen dat specifieke cellen worden gewijzigd. Gebruik de volgende code:

```csharp
// Bescherm het werkblad.
sheet.Protect(ProtectionType.All);
```

## Stap 9: Het Excel-bestand opslaan

We slaan nu het gewijzigde Excel-bestand op. Gebruik de volgende code:

```csharp
// Sla het Excel-bestand op.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Zorg ervoor dat u het juiste pad opgeeft om het gewijzigde Excel-bestand op te slaan.

### Voorbeeldbroncode voor het beschermen van specifieke cellen in een Excel-werkblad met Aspose.Cells voor .NET 
```csharp
//Het pad naar de documentenmap.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Maak een directory aan als deze nog niet aanwezig is.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Maak een nieuwe werkmap.
Workbook wb = new Workbook();
// Maak een werkbladobject en verkrijg het eerste werkblad.
Worksheet sheet = wb.Worksheets[0];
// Definieer het stijlobject.
Style style;
// Definieer het styleflag-object
StyleFlag styleflag;
// Loop door alle kolommen in het werkblad en ontgrendel ze.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    styleflag = new StyleFlag();
    styleflag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, styleflag);
}
// Vergrendel de drie cellen...dat wil zeggen A1, B1, C1.
style = sheet.Cells["A1"].GetStyle();
style.IsLocked = true;
sheet.Cells["A1"].SetStyle(style);
style = sheet.Cells["B1"].GetStyle();
style.IsLocked = true;
sheet.Cells["B1"].SetStyle(style);
style = sheet.Cells["C1"].GetStyle();
style.IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
// Tenslotte: bescherm het blad nu.
sheet.Protect(ProtectionType.All);
// Sla het Excel-bestand op.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```


## Conclusie

Gefeliciteerd! U beschikt nu over C#-broncode waarmee u specifieke cellen in een Excel-werkblad kunt beveiligen met behulp van de Aspose.Cells-bibliotheek voor .NET. U kunt de code gerust aanpassen aan uw specifieke behoeften.

### Veelgestelde vragen (veelgestelde vragen)

#### Werkt deze code met recente versies van Excel?

Ja, deze code werkt met recente versies van Excel, inclusief bestanden in de indeling Excel 2010 en hoger.

#### Kan ik naast A1, B1 en C1 nog andere cellen beschermen?

Ja, u kunt de code wijzigen om andere specifieke cellen te vergrendelen door de celverwijzingen in de overeenkomstige coderegels aan te passen.

#### Hoe kan ik vergrendelde cellen weer ontgrendelen?

 Je kunt gebruiken`SetStyle` methode met`IsLocked` ingesteld op`false` cellen te ontgrendelen.

#### Kan ik meer werkbladen aan de werkmap toevoegen?

 Ja, u kunt andere werkbladen aan de werkmap toevoegen met behulp van de`Worksheets.Add()`methode en herhaal de stappen voor celbescherming voor elk werkblad.

#### Hoe kan ik het opslagformaat van het Excel-bestand wijzigen?

 U kunt het opslagformaat wijzigen met behulp van de`SaveFormat` met bijvoorbeeld het gewenste formaat`SaveFormat.Xlsx` voor Excel 2007 en hoger.