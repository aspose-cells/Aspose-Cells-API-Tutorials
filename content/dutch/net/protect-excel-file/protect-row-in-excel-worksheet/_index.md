---
title: Bescherm rij in Excel-werkblad
linktitle: Bescherm rij in Excel-werkblad
second_title: Aspose.Cells voor .NET API-referentie
description: Ontdek in deze tutorial hoe u de rijen van een Excel-spreadsheet kunt beveiligen met Aspose.Cells voor .NET. Stap voor stap tutorial in C#.
type: docs
weight: 60
url: /nl/net/protect-excel-file/protect-row-in-excel-worksheet/
---
In deze zelfstudie bekijken we C#-broncode die de Aspose.Cells-bibliotheek gebruikt om rijen in een Excel-spreadsheet te beschermen. We doorlopen elke stap van de code en leggen uit hoe deze werkt. Volg de instructies zorgvuldig om de gewenste resultaten te krijgen.

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

In deze stap definiëren we de stijl die op de rijen van het spreadsheet moet worden toegepast. Gebruik de volgende code:

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

## Stap 7: De eerste regel vergrendelen

In deze stap vergrendelen we de eerste rij van het werkblad. Gebruik de volgende code:

```csharp
// Verkrijg de stijl van de eerste regel.
style = sheet.Cells.Rows[0].Style;
// Vergrendel de stijl.
style. IsLocked = true;
// Pas de stijl toe op de eerste regel.
sheet.Cells.ApplyRowStyle(0, style);
```

## Stap 8: Het werkblad beschermen

Nu we de stijlen hebben ingesteld en de rijen hebben vergrendeld, gaan we de spreadsheet beveiligen. Gebruik de volgende code:

```csharp
// Bescherm het werkblad.
sheet.Protect(ProtectionType.All);
```

## Stap 9: Het Excel-bestand opslaan

Ten slotte slaan we het gewijzigde Excel-bestand op. Gebruik de volgende code:

```csharp
// Sla het Excel-bestand op.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Zorg ervoor dat u het juiste pad opgeeft om het gewijzigde Excel-bestand op te slaan.

### Voorbeeldbroncode voor Protect Row in Excel Worksheet met Aspose.Cells voor .NET 
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
// Definieer het styleflag-object.
StyleFlag flag;
// Loop door alle kolommen in het werkblad en ontgrendel ze.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    flag = new StyleFlag();
    flag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
// Verkrijg de eerste rijstijl.
style = sheet.Cells.Rows[0].Style;
// Sluit het.
style.IsLocked = true;
//Instantieer de vlag.
flag = new StyleFlag();
// Stel de vergrendelingsinstelling in.
flag.Locked = true;
// Pas de stijl toe op de eerste rij.
sheet.Cells.ApplyRowStyle(0, style, flag);
// Bescherm het blad.
sheet.Protect(ProtectionType.All);
// Sla het Excel-bestand op.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## Conclusie

Gefeliciteerd! U beschikt nu over C#-broncode waarmee u rijen in een Excel-spreadsheet kunt beveiligen met behulp van de Aspose.Cells-bibliotheek voor .NET. Zorg ervoor dat u de stappen zorgvuldig volgt en de code aanpast aan uw specifieke behoeften.

### Veelgestelde vragen (veelgestelde vragen)

#### Werkt deze code met recente versies van Excel?

Ja, deze code werkt met recente versies van Excel, inclusief bestanden in de indeling Excel 2010 en hoger.

#### Kan ik alleen specifieke rijen beveiligen in plaats van alle rijen in het werkblad?

Ja, u kunt de code wijzigen om de specifieke rijen op te geven die u wilt beveiligen. U moet de lus en de indexen dienovereenkomstig aanpassen.

#### Hoe kan ik vergrendelde lijnen weer ontgrendelen?

 U kunt gebruik maken van de`IsLocked` werkwijze van de`Style` object waarop u de waarde wilt instellen`false` en ontgrendel de rijen.

#### Is het mogelijk om meerdere werkbladen in dezelfde Excel-werkmap te beveiligen?

Ja, u kunt de stappen voor het maken van een werkblad herhalen, waarbij u de stijl en beveiliging voor elk werkblad in de werkmap instelt.

#### Hoe kan ik het wachtwoord voor spreadsheetbeveiliging wijzigen?

 U kunt het wachtwoord wijzigen via de`Protect` methode en geef een nieuw wachtwoord op als argument.