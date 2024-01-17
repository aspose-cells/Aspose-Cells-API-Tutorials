---
title: Bereiken bewerken in Excel-werkblad
linktitle: Bereiken bewerken in Excel-werkblad
second_title: Aspose.Cells voor .NET API-referentie
description: Leer specifieke bereiken in een Excel-spreadsheet bewerken met Aspose.Cells voor .NET. Stap voor stap tutorial in C#.
type: docs
weight: 20
url: /nl/net/protect-excel-file/edit-ranges-in-excel-worksheet/
---
Microsoft Excel is een krachtig hulpmiddel voor het maken en beheren van spreadsheets en biedt vele functies voor het beheren en beveiligen van gegevens. Eén van deze functies is dat gebruikers specifieke bereiken in een werkblad kunnen bewerken terwijl andere delen worden beschermd. In deze tutorial begeleiden we u stap voor stap bij het implementeren van deze functionaliteit met behulp van Aspose.Cells voor .NET, een populaire bibliotheek voor het programmatisch werken met Excel-bestanden.

Door Aspose.Cells voor .NET te gebruiken, kunt u gemakkelijk bereiken in een Excel-spreadsheet manipuleren, waardoor een gebruiksvriendelijke interface en geavanceerde functies worden geboden. Volg de onderstaande stappen om gebruikers in staat te stellen specifieke bereiken in een Excel-spreadsheet te bewerken met Aspose.Cells voor .NET.
## Stap 1: De omgeving instellen

Zorg ervoor dat Aspose.Cells voor .NET in uw ontwikkelomgeving is geïnstalleerd. Download de bibliotheek van de officiële website van Aspose en bekijk de documentatie voor installatie-instructies.

## Stap 2: Werkmap en werkblad initialiseren

Om te beginnen moeten we een nieuwe werkmap maken en de verwijzing naar het werkblad ophalen waar we willen dat bereiken worden gewijzigd. Gebruik de volgende code om dit te bereiken:

```csharp
// Pad naar de documentenmap.
string dataDir = "YOUR DOCUMENTS DIRECTORY";
// Maak de map als deze nog niet bestaat.
bool exists = System.IO.Directory.Exists(dataDir);
if (! exists)
     System.IO.Directory.CreateDirectory(dataDir);

// Een nieuwe werkmap instantiëren
Workbook workbook = new Workbook();

// Het eerste werkblad ophalen (standaard)
Worksheet sheet = workbook.Worksheets[0];
```

 In dit codefragment definiëren we eerst het pad naar de map waar het Excel-bestand wordt opgeslagen. Vervolgens maken we een nieuw exemplaar van de`Workbook` klasse en haal de verwijzing naar het eerste werkblad op met behulp van de`Worksheets` eigendom.

## Stap 3: verkrijg bewerkbare bereiken

Nu moeten we de bereiken ophalen waarin we wijzigingen willen toestaan. Gebruik de volgende code:

```csharp
// Verkrijg de aanpasbare bereiken
ProtectedRangeCollection EditableRanges = Sheet.AllowEditRanges;
```

## Stap 4: Stel het beschermde bereik in

Voordat we toelaten dat bereiken worden gewijzigd, moeten we een beveiligd bereik definiëren. Hier is hoe:

```csharp
// Definieer een beveiligd bereik
ProtectedRange ProtectedRange;

// Maak het bereik
int index = ModifiableRanges.Add("r2", 1, 1, 3, 3);
rangeProtected = rangesEditable[index];
```

 In deze code maken we een nieuw exemplaar van de`ProtectedRange` klasse en gebruik de`Add` methode om het te beveiligen bereik op te geven.

## Stap 5: Geef een wachtwoord op

Om de beveiliging te verbeteren, kunt u een wachtwoord opgeven voor het beveiligde bereik. Hier is hoe:

```csharp
// Geef wachtwoord op
protectedBeach.Password = "YOUR_PASSWORD";
```

## Stap 6: Bescherm het werkblad

Nu we het beveiligde bereik hebben ingesteld, kunnen we het werkblad beveiligen om ongeoorloofde wijzigingen te voorkomen. Gebruik de volgende code:

```csharp
// Bescherm het werkblad
leaf.Protect(ProtectionType.All);
```

## Stap 7: Sla het Excel-bestand op

Ten slotte slaan we het Excel-bestand op met de aangebrachte wijzigingen. Hier is de benodigde code:

```csharp
// Sla het Excel-bestand op
workbook.Save(dataDir + "protectedrange.out.xls");
```

### Voorbeeldbroncode voor het bewerken van bereiken in Excel-werkblad met Aspose.Cells voor .NET 
```csharp
//Het pad naar de documentenmap.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Maak een directory aan als deze nog niet aanwezig is.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);

// Instantieer een nieuwe werkmap
Workbook book = new Workbook();

// Haal het eerste (standaard) werkblad op
Worksheet sheet = book.Worksheets[0];

// Haal het bereik voor het toestaan van bewerkingen op
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;

// Definieer Beschermd bereik
ProtectedRange proteced_range;

// Maak het bereik
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
proteced_range = allowRanges[idx];

// Geef het wachtwoord op
proteced_range.Password = "YOUR_PASSWORD";

// Bescherm het blad
sheet.Protect(ProtectionType.All);

// Sla het Excel-bestand op
book.Save(dataDir + "protectedrange.out.xls");
```

## Conclusie

Gefeliciteerd! U hebt geleerd hoe u gebruikers kunt toestaan specifieke bereiken in een Excel-spreadsheet te bewerken met behulp van Aspose.Cells voor .NET. U kunt deze techniek nu in uw eigen projecten toepassen en de beveiliging van uw Excel-bestanden verbeteren.


#### Veelgestelde vragen

#### Vraag: Waarom zou ik Aspose.Cells voor .NET gebruiken om bereiken in een Excel-spreadsheet te bewerken?

A: Aspose.Cells voor .NET biedt een krachtige en eenvoudig te gebruiken API voor het werken met Excel-bestanden. Het biedt geavanceerde functies, zoals bereikmanipulatie, werkbladbescherming, enz.

#### Vraag: Kan ik meerdere bewerkbare bereiken in een werkblad instellen?

 A: Ja, u kunt meerdere bewerkbare bereiken definiëren met behulp van de`Add` werkwijze van de`ProtectedRangeCollection` verzameling. Elk bereik kan zijn eigen beveiligingsinstellingen hebben.

####  Vraag: Is het mogelijk om een bewerkbaar bereik te verwijderen nadat het is gedefinieerd?

 A: Ja, u kunt de`RemoveAt` werkwijze van de`ProtectedRangeCollection` collectie om een specifiek bewerkbaar bereik te verwijderen door de index ervan op te geven.

#### Vraag: Hoe kan ik het beveiligde Excel-bestand openen nadat ik het heb opgeslagen?

A: U moet het wachtwoord opgeven dat is opgegeven bij het maken van het beveiligde bereik om het beveiligde Excel-bestand te openen. Zorg ervoor dat u het wachtwoord op een veilige plaats bewaart om verlies van toegang tot gegevens te voorkomen.