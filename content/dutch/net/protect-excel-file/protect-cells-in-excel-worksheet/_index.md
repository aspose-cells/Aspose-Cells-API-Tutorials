---
title: Bescherm cellen in Excel-werkblad
linktitle: Bescherm cellen in Excel-werkblad
second_title: Aspose.Cells voor .NET API-referentie
description: Leer hoe u specifieke cellen in Excel kunt beschermen met Aspose.Cells voor .NET. Stap voor stap tutorial in C#.
type: docs
weight: 30
url: /nl/net/protect-excel-file/protect-cells-in-excel-worksheet/
---
Microsoft Excel is een veelgebruikte tool voor het maken en beheren van spreadsheets. Een van de kernfuncties van Excel is de mogelijkheid om bepaalde cellen te beschermen om de gegevensintegriteit te behouden. In deze zelfstudie begeleiden we u stap voor stap bij het beschermen van specifieke cellen in een Excel-spreadsheet met Aspose.Cells voor .NET. Aspose.Cells voor .NET is een krachtige programmeerbibliotheek waarmee u eenvoudig Excel-bestanden kunt manipuleren met grote flexibiliteit en geavanceerde functies. Volg de aangegeven stappen om te leren hoe u uw belangrijke cellen kunt beschermen en uw gegevens veilig kunt houden.

## Stap 1: De omgeving instellen

Zorg ervoor dat Aspose.Cells voor .NET in uw ontwikkelomgeving is geïnstalleerd. Download de bibliotheek van de officiële website van Aspose en bekijk de documentatie voor installatie-instructies.

## Stap 2: Werkmap en werkblad initialiseren

Om te beginnen moeten we een nieuwe werkmap maken en de verwijzing naar het werkblad ophalen waar we de cellen willen beschermen. Gebruik de volgende code:

```csharp
// Pad naar de documentenmap.
string dataDir = "YOUR DOCUMENTS DIRECTORY";
// Maak de map als deze nog niet bestaat.
bool exists = System.IO.Directory.Exists(dataDir);
if (! exists)
     System.IO.Directory.CreateDirectory(dataDir);

// Maak een nieuwe werkmap
Workbook workbook = new Workbook();

// Haal het eerste werkblad
Worksheet sheet = workbook.Worksheets[0];
```

 In dit codefragment definiëren we eerst het pad naar de map waar het Excel-bestand wordt opgeslagen. Vervolgens maken we een nieuw exemplaar van de`Workbook` klasse en haal de verwijzing naar het eerste werkblad op met behulp van de`Worksheets` eigendom.

## Stap 3: Definieer celstijl

Nu moeten we de stijl definiëren van de cellen die we willen beschermen. Gebruik de volgende code:

```csharp
// Definieer het stijlobject
Styling styling;

// Loop door alle kolommen in het werkblad en ontgrendel ze
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     leaf.Cells.Columns[(byte)i].ApplyStyle(style, new StyleFlag { Locked = true });
}
```

 In deze code gebruiken we een lus om alle kolommen in het werkblad te doorlopen en hun cellen te ontgrendelen door de stijl in te stellen`IsLocked` eigendom aan`false` . Wij gebruiken dan de`ApplyStyle` methode om de stijl toe te passen op de kolommen met de`StyleFlag` vlag om de cellen te vergrendelen.

## Stap 4: Bescherm specifieke cellen

Nu gaan we de specifieke cellen beschermen die we willen vergrendelen. Gebruik de volgende code:

```csharp
// Vergrendel de drie cellen: A1, B1, C1
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

 In deze code krijgen we de stijl van elke specifieke cel met behulp van de`GetStyle` methode, en dan stellen we de`IsLocked` eigenschap van de stijl`true`om de cel op slot te doen. Ten slotte passen we de bijgewerkte stijl toe op elke cel met behulp van de`SetStyle` methode.

## Stap 5: Het werkblad beschermen

Nu we de te beschermen cellen hebben gedefinieerd, kunnen we het werkblad zelf beschermen. Gebruik de volgende code:

```csharp
// Bescherm het werkblad
leaf.Protect(ProtectionType.All);
```

 Deze code maakt gebruik van de`Protect` methode om in dit geval het werkblad te beschermen met het opgegeven beveiligingstype`ProtectionType.All` die alle items in het werkblad beschermt.

## Stap 6: Sla het Excel-bestand op

Ten slotte slaan we het Excel-bestand op met de aangebrachte wijzigingen. Gebruik de volgende code:

```csharp
// Sla het Excel-bestand op
workbook.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

 In deze code gebruiken we de`Save` methode om de werkmap in de opgegeven map op te slaan met de`Excel97To2003` formaat.

### Voorbeeldbroncode voor het beschermen van cellen in Excel-werkblad met Aspose.Cells voor .NET 
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
wb.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

## Conclusie

Gefeliciteerd! U hebt geleerd hoe u specifieke cellen in een Excel-spreadsheet kunt beveiligen met Aspose.Cells voor .NET. U kunt deze techniek nu in uw eigen projecten toepassen en de beveiliging van uw Excel-bestanden verbeteren.


### Veelgestelde vragen

#### Vraag: Waarom zou ik Aspose.Cells voor .NET gebruiken om cellen in een Excel-spreadsheet te beschermen?

A: Aspose.Cells voor .NET is een krachtige bibliotheek waarmee u eenvoudig met Excel-bestanden kunt werken. Het biedt geavanceerde functies om cellen te beschermen, bereik te ontgrendelen, enz.

#### Vraag: Is het mogelijk om celbereiken te beschermen in plaats van individuele cellen?

 A: Ja, u kunt specifieke celbereiken definiëren om te beschermen met behulp van de`ApplyStyle` methode met een passende`StyleFlag`.

#### Vraag: Hoe kan ik het beveiligde Excel-bestand openen nadat ik het heb opgeslagen?

A: Wanneer u het beveiligde Excel-bestand opent, moet u het wachtwoord opgeven dat is opgegeven bij het beveiligen van het werkblad.

#### Vraag: Zijn er andere soorten beveiliging die ik op een Excel-spreadsheet kan toepassen?

A: Ja, Aspose.Cells voor .NET ondersteunt meerdere soorten bescherming, zoals structuurbescherming, raambescherming, enz. U kunt het juiste type bescherming kiezen op basis van uw behoeften.