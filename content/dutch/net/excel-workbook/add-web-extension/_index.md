---
title: Webextensie toevoegen
linktitle: Webextensie toevoegen
second_title: Aspose.Cells voor .NET API-referentie
description: Voeg eenvoudig een webextensie toe aan uw Excel-werkmappen met Aspose.Cells voor .NET.
type: docs
weight: 40
url: /nl/net/excel-workbook/add-web-extension/
---
In deze stapsgewijze zelfstudie leggen we de meegeleverde C#-broncode uit waarmee u een webextensie kunt toevoegen met Aspose.Cells voor .NET. Volg de onderstaande stappen om een webextensie aan uw Excel-werkmap toe te voegen.

## Stap 1: Stel de uitvoermap in

```csharp
// Uitvoermap
string outDir = RunExamples.Get_OutputDirectory();
```

In deze eerste stap definiëren we de uitvoermap waar de gewijzigde Excel-werkmap zal worden opgeslagen.

## Stap 2: Maak een nieuwe werkmap

```csharp
// Maak een nieuwe werkmap
Workbook workbook = new Workbook();
```

Hier maken we een nieuwe Excel-werkmap met behulp van de`Workbook` klasse van Aspose.Cells.

## Stap 3: Open de verzameling webextensies

```csharp
// Toegang tot de verzameling webextensies
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
```

 We hebben toegang tot de verzameling webextensies van de Excel-werkmap met behulp van de`WebExtensions` eigendom van de`Worksheets` voorwerp.

## Stap 4: Voeg een nieuwe webextensie toe

```csharp
// Voeg een nieuwe webextensie toe
int extensionIndex = extensions.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
```

We voegen een nieuwe webextensie toe aan de extensiecollectie. We definiëren de referentie-ID, winkelnaam en winkeltype van de extensie.

## Stap 5: Open de taakvensterverzameling van de webextensie

```csharp
// Toegang tot de taakvensterverzameling van de webextensie
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
```

 We hebben toegang tot de verzameling taakvensters van Excel Workbook Web Extension met behulp van de`WebExtensionTaskPanes` eigendom van de`Worksheets` voorwerp.

## Stap 6: Voeg een nieuw taakvenster toe

```csharp
// Voeg een nieuw taakvenster toe
int taskPaneIndex = taskPanes.Add();
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane. IsVisible = true;
taskPane. DockState = "right";
taskPane. WebExtension = extension;
```

We voegen een nieuw taakvenster toe aan de taakvenstercollectie. We stellen de zichtbaarheid van het paneel, de dockingstatus en de bijbehorende webextensie in.

## Stap 7: Bewaar en sluit de werkmap

```csharp
// Bewaar en sluit de werkmap
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

We slaan de gewijzigde werkmap op in de opgegeven uitvoermap en sluiten deze vervolgens.

### Voorbeeldbroncode voor het toevoegen van een webextensie met Aspose.Cells voor .NET 
```csharp
//Bronmap
string outDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook();
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
int extensionIndex = extensions.Add();
int taskPaneIndex = taskPanes.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane.IsVisible = true;
taskPane.DockState = "right";
taskPane.WebExtension = extension;
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

## Conclusie

Gefeliciteerd! U hebt nu geleerd hoe u een webextensie kunt toevoegen met Aspose.Cells voor .NET. Experimenteer met code en ontdek extra functies van Aspose.Cells om het meeste uit het manipuleren van webextensies in uw Excel-werkmappen te halen.

## Veelgestelde vragen

#### Vraag: Wat is een webextensie in een Excel-werkmap?

A: Een webextensie in een Excel-werkmap is een component waarmee u extra functionaliteit aan Excel kunt toevoegen door webapplicaties te integreren. Het kan interactieve functies, aangepaste dashboards, externe integraties en meer bieden.

#### Vraag: Hoe kan ik een webextensie toevoegen aan de Excel-werkmap met Aspose.Cells?

 A: Om een webextensie toe te voegen aan een Excel-werkmap met Aspose.Cells, kunt u de stappen volgen in onze stapsgewijze handleiding. Gebruik de`WebExtensionCollection` En`WebExtensionTaskPaneCollection` klassen om de webextensie en het bijbehorende taakvenster toe te voegen en te configureren.

#### Vraag: Welke informatie is vereist om een webextensie toe te voegen?

A: Wanneer u een webextensie toevoegt, moet u de SKU-ID van de extensie, de winkelnaam en het winkeltype opgeven. Deze informatie helpt om de extensie correct te identificeren en te laden.

#### Vraag: Kan ik meerdere webextensies toevoegen aan één Excel-werkmap?

 A: Ja, u kunt meerdere webextensies toevoegen aan één Excel-werkmap. Gebruik de`Add` methode van de verzameling webextensies om elke extensie toe te voegen en deze vervolgens aan de overeenkomstige taakvensters te koppelen.