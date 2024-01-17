---
title: Bescherm specifieke rij in Excel-werkblad
linktitle: Bescherm specifieke rij in Excel-werkblad
second_title: Aspose.Cells voor .NET API-referentie
description: Bescherm een specifieke rij in Excel met Aspose.Cells voor .NET. Stapsgewijze handleiding voor het beveiligen van uw vertrouwelijke gegevens.
type: docs
weight: 90
url: /nl/net/protect-excel-file/protect-specific-row-in-excel-worksheet/
---
Het beschermen van vertrouwelijke gegevens in een Excel-spreadsheet is essentieel om de informatiebeveiliging te garanderen. Aspose.Cells voor .NET biedt een krachtige oplossing om specifieke rijen in een Excel-spreadsheet te beschermen. In deze handleiding wordt uitgelegd hoe u een specifieke rij in een Excel-werkblad kunt beveiligen met behulp van de meegeleverde C#-broncode. Volg deze eenvoudige stappen om rijbeveiliging in uw Excel-bestanden in te stellen.

## Stap 1: Importeer de vereiste bibliotheken

Zorg er om te beginnen voor dat Aspose.Cells voor .NET op uw systeem is geïnstalleerd. U moet ook de juiste referenties toevoegen aan uw C#-project om de functionaliteit van Aspose.Cells te kunnen gebruiken. Hier is de code om de vereiste bibliotheken te importeren:

```csharp
// Voeg de nodige referenties toe
using Aspose.Cells;
```

## Stap 2: Een Excel-werkmap en spreadsheet maken

Na het importeren van de benodigde bibliotheken kunt u een nieuwe Excel-werkmap en een nieuw werkblad maken. Hier leest u hoe u het moet doen:

```csharp
//Het pad naar de documentenmap.
string dataDir = "YOUR DOCUMENTS DIRECTORY";

// Maak een map als deze nog niet bestaat.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
     System.IO.Directory.CreateDirectory(dataDir);

// Maak een nieuwe werkmap.
Workbook wb = new Workbook();

// Maak een spreadsheetobject en haal het eerste blad op.
Worksheet sheet = wb.Worksheets[0];
```

## Stap 3: De stijl en stijlvlag instellen

Nu gaan we de celstijl en stijlvlag instellen om alle kolommen in het werkblad te ontgrendelen. Hier is de benodigde code:

```csharp
// Stel het stijlobject in.
Styling styling;

// Stel het styleflag-object in.
StyleFlag flag;

// Loop door alle kolommen in het werkblad en ontgrendel ze.
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     flag = new StyleFlag();
     flag. Locked = true;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
```

## Stap 4: Bescherm de specifieke lijn

Nu gaan we de specifieke rij in het werkblad beschermen. We gaan de eerste rij vergrendelen om elke wijziging te voorkomen. Hier is hoe:

```csharp
// Verkrijg de stijl van de eerste regel.
style = sheet.Cells.Rows[0].Style;

// Sluit het.
style. IsLocked = true;

//Instantieer de vlag.
flag = new StyleFlag();

// Stel de vergrendelingsparameter in.
flag. Locked = true;

// Pas de stijl toe op de eerste regel.
sheet.Cells.ApplyRowStyle(0, style, flag);
```

## Stap 5: Het werkblad beschermen

Ten slotte beschermen we het volledige Excel-werkblad om ongeoorloofde wijzigingen te voorkomen. Hier is hoe:

```csharp
// Bescherm het werkblad.
sheet.Protect(ProtectionType.All);
```

## Stap 6: Sla het beveiligde Excel-bestand op

Zodra u klaar bent met het beveiligen van de specifieke rij in het Excel-werkblad, kunt u het beveiligde Excel-bestand op uw systeem opslaan. Hier is hoe:

```csharp
// Sla het Excel-bestand op.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Nadat u deze stappen heeft gevolgd, heeft u met succes een specifieke rij in uw Excel-spreadsheet beveiligd met Aspose.Cells voor .NET.

### Voorbeeldbroncode voor Protect Specific Row In Excel Worksheet met Aspose.Cells voor .NET 
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

Het beschermen van gegevens in Excel-bestanden is van cruciaal belang om ongeautoriseerde toegang of ongewenste wijziging te voorkomen. Met behulp van de Aspose.Cells-bibliotheek voor .NET kunt u eenvoudig specifieke rijen in een Excel-spreadsheet beveiligen met behulp van de meegeleverde C#-broncode. Volg deze stapsgewijze handleiding om een extra beveiligingslaag aan uw Excel-bestanden toe te voegen.

### Veelgestelde vragen

#### Werkt specifieke rijbescherming in alle versies van Excel?

Ja, specifieke rijbeveiliging met Aspose.Cells voor .NET werkt in alle ondersteunde versies van Excel.

#### Kan ik meerdere specifieke rijen in een Excel-spreadsheet beveiligen?

Ja, u kunt meerdere specifieke rijen beveiligen met vergelijkbare methoden die in deze handleiding worden beschreven.

#### Hoe kan ik een specifieke rij in een Excel-spreadsheet ontgrendelen?

 Om een specifieke rij te ontgrendelen, moet u de broncode dienovereenkomstig aanpassen met behulp van de`IsLocked` werkwijze van de`Style` voorwerp.