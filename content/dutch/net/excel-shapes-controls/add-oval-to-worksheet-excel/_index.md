---
title: Ovaal toevoegen aan werkblad in Excel
linktitle: Ovaal toevoegen aan werkblad in Excel
second_title: Aspose.Cells .NET Excel-verwerkings-API
description: Leer hoe u een ovaal toevoegt aan een Excel-werkblad met Aspose.Cells voor .NET. Stapsgewijze handleiding met gedetailleerde code-uitleg.
type: docs
weight: 17
url: /nl/net/excel-shapes-controls/add-oval-to-worksheet-excel/
---
## Invoering
Het maken van verbluffende en interactieve Excel-bestanden kan meer omvatten dan alleen getallen en formules. Vormen zoals ovalen kunnen een visuele aantrekkingskracht toevoegen of functionele elementen in uw werkbladen leveren. In deze tutorial onderzoeken we hoe u Aspose.Cells voor .NET kunt gebruiken om ovalen programmatisch toe te voegen aan een Excel-werkblad. Of u nu wat flair of functionaliteit wilt toevoegen, wij hebben een stapsgewijze handleiding die alles uitlegt.
## Vereisten
Voordat u in de code duikt, moet u een aantal zaken regelen:
1.  Aspose.Cells voor .NET-bibliotheek: U kunt het downloaden van[hier](https://releases.aspose.com/cells/net/) of installeer het met behulp van NuGet in Visual Studio.
2. Ontwikkelomgeving: AC# IDE zoals Visual Studio.
3. Basiskennis van C#: U moet bekend zijn met de basisconcepten van C#-codering.
 Vergeet ook niet om uw project in te stellen door de Aspose.Cells for .NET-bibliotheek te installeren. Als u nog geen licentie hebt, kunt u een aanvraag indienen voor een[tijdelijke licentie](https://purchase.aspose.com/temporary-license/) of gebruik de[gratis proefperiode](https://releases.aspose.com/) versie.
## Pakketten importeren
Voordat u code schrijft, moet u ervoor zorgen dat u de vereiste namespaces hebt opgenomen. Hier is het C#-codefragment om ervoor te zorgen dat u de juiste bibliotheken gebruikt:
```csharp
using System.IO;
using Aspose.Cells;
using Aspose.Cells.Drawing;
using System.Drawing;
```
## Stap 1: Stel uw directory in
De eerste stap bij het toevoegen van een ovaal aan een Excel-sheet is het specificeren waar uw Excel-bestand wordt opgeslagen. Laten we het directorypad definiëren en ervoor zorgen dat de directory bestaat voordat we ons werk opslaan.

We maken een directorypad en verifiëren of het bestaat. Als de map niet bestaat, wordt deze gemaakt.
```csharp
// Het pad naar de documentenmap.
string dataDir = "Your Document Directory";
//Maak een map aan als deze nog niet bestaat.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
```
Deze stap is cruciaal omdat u hiermee zeker weet dat uw bestand op de juiste locatie wordt opgeslagen en dat u later geen problemen krijgt met het bestandspad.
## Stap 2: Initialiseer een nieuwe werkmap
Vervolgens moeten we een nieuwe werkmap maken waarin we onze ovale vormen toevoegen. De werkmap vertegenwoordigt een Excel-bestand en we kunnen er inhoud of vormen aan toevoegen.

 In deze stap instantiëren we een nieuwe`Workbook` object dat als onze Excel-bestandscontainer zal dienen.
```csharp
// Een nieuwe werkmap maken.
Workbook excelbook = new Workbook();
```
## Stap 3: Voeg de eerste ovale vorm toe
Nu komt het leuke gedeelte: een ovale vorm toevoegen aan het werkblad. Deze ovaal kan een visueel element voorstellen, zoals een knop of een markering. We beginnen met het toevoegen van de eerste ovale vorm aan het eerste werkblad van onze werkmap.

 Hier gebruiken we de`Shapes.AddOval()` Methode om een ovaal op het werkblad te maken op een specifieke rij en kolom.
```csharp
// Voeg een ovale vorm toe.
Aspose.Cells.Drawing.Oval oval1 = excelbook.Worksheets[0].Shapes.AddOval(2, 0, 2, 0, 130, 160);
```
 De parameters binnenin`AddOval()` zijn als volgt:
- De eerste twee getallen stellen de rij en kolom voor de linkerbovenhoek van het ovaal voor.
- De volgende twee getallen geven de hoogte en breedte van het ovaal aan.
## Stap 4: De plaatsing en stijl van het ovaal instellen
 Zodra de ovaal is gemaakt, kunnen we de positie, lijndikte en streepjesstijl instellen.`Placement` eigenschap bepaalt hoe de ovaal zich gedraagt wanneer u cellen in het werkblad verplaatst of het formaat ervan wijzigt.

Wij maken de ovaal zwevend en passen het uiterlijk aan.
```csharp
// Bepaal de plaatsing van het ovaal.
oval1.Placement = PlacementType.FreeFloating;
// Stel de lijndikte in.
oval1.Line.Weight = 1;
// Stel de streepjesstijl van het ovaal in.
oval1.Line.DashStyle = MsoLineDashStyle.Solid;
```
Hierdoor kan de ovaal vrij binnen het werkblad bewegen en worden de lijndikte en -stijl ingesteld voor visuele consistentie.
## Stap 5: Voeg nog een ovale (cirkel) vorm toe
Waarom zouden we bij één stoppen? In deze stap voegen we nog een ovale vorm toe, dit keer creëren we een perfecte cirkel door de hoogte en breedte gelijk te maken.

We maken nog een ovaal, plaatsen deze op een andere locatie en zorgen ervoor dat deze rond wordt door de hoogte en breedte gelijk te stellen.
```csharp
// Voeg nog een ovale (cirkel)vorm toe.
Aspose.Cells.Drawing.Oval oval2 = excelbook.Worksheets[0].Shapes.AddOval(9, 0, 2, 15, 130, 130);
```
## Stap 6: Style de tweede ovaal
Net als eerder passen we de plaatsing, het gewicht en de streepjesstijl van deze tweede ovaal (of cirkel) aan.

We passen soortgelijke eigenschappen toe op het tweede ovaal, zodat het qua stijl overeenkomt met het eerste.
```csharp
// Bepaal de plaatsing van het ovaal.
oval2.Placement = PlacementType.FreeFloating;
// Stel de lijndikte in.
oval2.Line.Weight = 1;
// Stel de streepjesstijl van het ovaal in.
oval2.Line.DashStyle = MsoLineDashStyle.Solid;
```
## Stap 7: Sla de werkmap op
Ten slotte moeten we de werkmap met de ovalen die we zojuist hebben toegevoegd opslaan. Door het bestand op te slaan, zorgen we ervoor dat al onze wijzigingen worden opgeslagen.

We slaan de werkmap op in het directorypad dat we eerder hebben gedefinieerd.
```csharp
// Sla het Excel-bestand op.
excelbook.Save(dataDir + "book1.out.xls");
```
En dat is alles! U hebt succesvol ovalen toegevoegd aan uw Excel-werkblad en het bestand opgeslagen.
## Conclusie
Het toevoegen van vormen zoals ovalen aan een Excel-sheet met Aspose.Cells voor .NET is niet alleen eenvoudig, maar ook een leuke manier om uw spreadsheets te verbeteren met extra visuele elementen. Of het nu voor ontwerpdoeleinden is of om klikbare elementen toe te voegen, vormen kunnen een belangrijke rol spelen in hoe uw Excel-bestanden eruit zien en functioneren. Dus de volgende keer dat u werkt aan een project dat interactieve of visueel aantrekkelijke Excel-sheets vereist, weet u precies hoe u die perfecte ovalen toevoegt!
## Veelgestelde vragen
### Kan ik andere vormen, zoals rechthoeken of lijnen, toevoegen met Aspose.Cells voor .NET?
 Ja, u kunt verschillende vormen toevoegen, zoals rechthoeken, lijnen en pijlen met behulp van de`Shapes` verzameling in Aspose.Cells.
### Is het mogelijk om de ovalen groter of kleiner te maken nadat ik ze heb toegevoegd?
Absoluut! Je kunt de hoogte- en breedte-eigenschappen van de ovalen aanpassen nadat je ze hebt toegevoegd.
### In welke bestandsformaten kan ik de werkmap opslaan, naast XLS?
Aspose.Cells ondersteunt meerdere formaten, zoals XLSX, CSV en PDF.
### Kan ik de kleur van de omtrek van het ovaal aanpassen?
 Ja, u kunt de lijnkleur van het ovaal wijzigen met behulp van de`Line.Color` eigendom.
### Is een licentie voor Aspose.Cells noodzakelijk?
 Hoewel u Aspose.Cells gratis kunt uitproberen, hebt u een[licentie](https://purchase.aspose.com/buy) voor langdurig gebruik of voor toegang tot geavanceerde functies.