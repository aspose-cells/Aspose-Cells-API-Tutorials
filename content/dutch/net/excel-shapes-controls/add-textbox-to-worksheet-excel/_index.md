---
title: Een tekstvak toevoegen aan een werkblad in Excel
linktitle: Een tekstvak toevoegen aan een werkblad in Excel
second_title: Aspose.Cells .NET Excel-verwerkings-API
description: Leer in deze stapsgewijze zelfstudie hoe u aanpasbare tekstvakken aan Excel toevoegt met Aspose.Cells voor .NET.
type: docs
weight: 14
url: /nl/net/excel-shapes-controls/add-textbox-to-worksheet-excel/
---
## Invoering
Wilt u uw Excel-spreadsheets verbeteren met unieke visuals die uw publiek kunnen boeien? Tekstvakken toevoegen is een geweldige manier om dit te bereiken! Met Aspose.Cells voor .NET kunt u eenvoudig tekstvakken integreren in uw Excel-werkbladen, waardoor uw documenten informatiever en visueel aantrekkelijker worden. Deze stapsgewijze handleiding leidt u door het eenvoudige proces van het toevoegen van tekstvakken met Aspose.Cells, en laat zien hoe u ze kunt personaliseren met tekst, kleuren, hyperlinks en meer!
## Vereisten
Voordat we in het wonder van coderen duiken, zijn hier de essentiële voorwaarden om een soepele ervaring te garanderen:
1. .NET Development Environment: U hebt een werkend .NET framework nodig, samen met een IDE zoals Visual Studio. Zorg ervoor dat het is bijgewerkt naar de nieuwste versie!
2.  Aspose.Cells voor .NET: Zorg ervoor dat u de Aspose.Cells-bibliotheek hebt gedownload. U kunt de nieuwste versie ophalen van[hier](https://releases.aspose.com/cells/net/).
3. Basiskennis programmeren: Kennis van C# en enkele algemene concepten voor het werken met Excel-bestanden maken deze tutorial gemakkelijker!
## Pakketten importeren
Zorg ervoor dat u de benodigde pakketten aan het begin van uw C#-bestand importeert. Zo doet u dat:
```csharp
using System.IO;
using Aspose.Cells;
using Aspose.Cells.Drawing;
using System.Drawing;
```
## Aspose.Cells installeren
Als u dit nog niet hebt gedaan, kunt u Aspose.Cells toevoegen via NuGet Package Manager in Visual Studio:
1. Open Visual Studio.
2.  Ga naar`Tools` ->`NuGet Package Manager` ->`Manage NuGet Packages for Solution`.
3. Zoek naar “Aspose.Cells” en installeer het voor uw project.
Nu we de basis hebben gelegd, kunnen we beginnen met het leukste gedeelte!
## Stap 1: Uw documentenmap instellen
Laten we eerst de directory instellen waar al uw Excel-documenten worden opgeslagen. Het is essentieel om ervoor te zorgen dat deze directory bestaat voordat we beginnen met het maken van onze werkmap.
```csharp
// Het pad naar de documentenmap.
string dataDir = "Your Document Directory"; 
//Maak een map aan als deze nog niet bestaat.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists) 
    System.IO.Directory.CreateDirectory(dataDir);
```
Dit codefragment zal een map aanmaken met de naam`Your Document Directory` (vervang dit met je eigen pad) als het nog niet bestaat. Makkelijk toch?
## Stap 2: Een nieuwe werkmap instantiëren
Vervolgens moeten we een nieuwe werkmap maken waar we onze tekstvakken aan toevoegen. Dit kan eenvoudig worden gedaan met een paar regels code:
```csharp
// Een nieuwe werkmap maken.
Workbook workbook = new Workbook();
```
Deze regel code creëert een nieuwe Excel-werkmap. Simpel en duidelijk!
## Stap 3: Toegang tot het eerste werkblad
Nu onze werkmap klaar is, gaan we naar het eerste werkblad waar we het tekstvak aan gaan toevoegen:
```csharp
// Pak het eerste werkblad uit het boek.
Worksheet worksheet = workbook.Worksheets[0];
```
 Zo heb je nu toegang tot het eerste werkblad met de naam`worksheet`. Het is tijd om het te laten schitteren!
## Stap 4: Een tekstvak toevoegen
Oké, het is tijd om ons eerste tekstvak toe te voegen! Dit is hoe je dat doet:
```csharp
// Voeg een nieuw tekstvak toe aan de verzameling.
int textboxIndex = worksheet.TextBoxes.Add(2, 1, 160, 200);
```
In deze regel geven we de rij en kolom op waar het tekstvak wordt geplaatst, en stellen we de breedte en hoogte in (respectievelijk 160 en 200). U kunt deze getallen gerust aanpassen op basis van uw lay-out!
## Stap 5: Het TextBox-object ophalen
Nadat we het tekstvak hebben toegevoegd, moeten we er een verwijzing naar krijgen, zodat we de inhoud ervan kunnen aanpassen:
```csharp
// Haal het tekstvakobject op.
Aspose.Cells.Drawing.TextBox textbox0 = worksheet.TextBoxes[textboxIndex];
```
 Nu,`textbox0` is uw gouden ticket om dit tekstvak te wijzigen!
## Stap 6: Het tekstvak vullen met inhoud
Laten we nu wat tekst voor het tekstvak invoeren:
```csharp
// Vul de tekst in.
textbox0.Text = "ASPOSE______The .NET & JAVA Component Publisher!";
```
Zo eenvoudig is het om tekst in uw tekstvak in te voegen! 
## Stap 7: Pas het uiterlijk van het tekstvak aan
Wat dacht je ervan om het een beetje op te fleuren? Je kunt de kleuren van het lettertype, de stijlen en meer aanpassen!
```csharp
// Stel de kleur van het lettertype in.
textbox0.Font.Color = Color.Blue;
// Maak het lettertype vet.
textbox0.Font.IsBold = true;
// Stel de lettergrootte in.
textbox0.Font.Size = 14;
// Stel het lettertypekenmerk in op cursief.
textbox0.Font.IsItalic = true;
```
Experimenteer gerust met verschillende kleuren en stijlen om te zien wat het beste tot zijn recht komt!
## Stap 8: Een hyperlink toevoegen
Wilt u uw tekstvak omzetten in een klikbare link? Laten we dat doen:
```csharp
// Voeg een hyperlink toe aan het tekstvak.
textbox0.AddHyperlink("http://www.aspose.com/");
```
Nu wordt iedereen die op uw tekstvak klikt, naar de Aspose-website getransporteerd. Het is net magie!
## Stap 9: Het type tekstvakplaatsing instellen
hebt verschillende keuzes over hoe u wilt dat het tekstvak zich gedraagt in relatie tot uw werkblad. Hier is een voorbeeld van hoe u het instelt op vrij zwevend:
```csharp
// Plaatsing instellen.
textbox0.Placement = PlacementType.FreeFloating;
```
Als u wilt dat de grootte wordt aangepast en dat de cellen worden verplaatst, kunt u dit als volgt instellen:
```csharp
// Stel het plaatsingstype in, aangezien het tekstvak verplaatst en de grootte ervan wordt aangepast met de cellen.
textbox1.Placement = PlacementType.MoveAndSize;
```
## Stap 10: Lijn- en opvulformaten aanpassen
Zo kunt u het uiterlijk van de rand en vulling van het tekstvak wijzigen:
```csharp
// Haal het opvulformaat van het tekstvak op.
Aspose.Cells.Drawing.FillFormat fillformat = textbox0.Fill;            
// Haal het lijnopmaaktype van het tekstvak op.
Aspose.Cells.Drawing.LineFormat lineformat = textbox0.Line;           
// Stel de lijndikte in.
lineformat.Weight = 6;
// Stel de streepjesstijl in op vierkante stippen.
lineformat.DashStyle = MsoLineDashStyle.SquareDot;
```
Hiermee kunt u het tekstvak verder personaliseren en afbeeldingen toevoegen die bij uw stijl passen.
## Stap 11: Een ander tekstvak toevoegen
Niemand heeft gezegd dat we maar één tekstvak konden toevoegen! Laten we er nog een toevoegen met wat andere tekst:
```csharp
// Voeg nog een tekstvak toe.
textboxIndex = worksheet.TextBoxes.Add(15, 4, 85, 120);
// Pak het tweede tekstvak.
Aspose.Cells.Drawing.TextBox textbox1 = worksheet.TextBoxes[textboxIndex];
// Voer er wat tekst in.
textbox1.Text = "This is another simple text box";
```
Nu maakt u uw Excel-sheet echt compleet met meerdere tekstvakken!
## Stap 12: Uw werkmap opslaan
Eindelijk is het tijd om ons meesterwerk te redden! Hier is de laatste regel code voor vandaag:
```csharp
// Sla het Excel-bestand op.
workbook.Save(dataDir + "book1.out.xls");
```
Met slechts één regel code hebt u een Excel-bestand met aanpasbare tekstvakken gemaakt en gewijzigd!
## Conclusie
Gefeliciteerd! U bent succesvol door de wereld van tekstvakken in Excel genavigeerd met Aspose.Cells voor .NET. U hebt niet alleen geleerd hoe u een tekstvak toevoegt, maar ook hoe u het aanpast om uw spreadsheets aantrekkelijker te maken. Van het wijzigen van kleuren en stijlen tot zelfs het toevoegen van hyperlinks, de mogelijkheden zijn vrijwel eindeloos! 
Bent u klaar om uw Excel-documenten te transformeren? Laat uw creativiteit de vrije loop en experimenteer met verschillende lay-outs!
## Veelgestelde vragen
### Wat is Aspose.Cells voor .NET?
Aspose.Cells voor .NET is een krachtige bibliotheek waarmee ontwikkelaars moeiteloos Excel-bestanden kunnen maken, bewerken en converteren.
### Kan ik Aspose.Cells uitproberen voordat ik het koop?
 Ja! U kunt een gratis proefversie downloaden en gebruiken[hier](https://releases.aspose.com/).
### Waar kan ik de documentatie voor Aspose.Cells vinden?
 U kunt uitgebreide documentatie raadplegen op[Aspose.Cells-documentatie](https://reference.aspose.com/cells/net/).
### Is er ondersteuning beschikbaar als ik problemen tegenkom?
 Absoluut! Als je hulp nodig hebt, ga dan naar de[Aspose-forum](https://forum.aspose.com/c/cells/9) voor hulp.
### Kan ik Aspose.Cells gebruiken zonder licentie?
 Hoewel u een gratis proefversie kunt gebruiken, moet u een licentie kopen om toegang te krijgen tot de volledige functionaliteit. Bekijk de prijzen[hier](https://purchase.aspose.com/buy).