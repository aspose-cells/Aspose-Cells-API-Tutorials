---
title: Geavanceerde beveiligingsinstellingen voor Excel-werkblad
linktitle: Geavanceerde beveiligingsinstellingen voor Excel-werkblad
second_title: Aspose.Cells voor .NET API-referentie
description: Bescherm uw Excel-bestanden door geavanceerde beveiligingsinstellingen in te stellen met Aspose.Cells voor .NET.
type: docs
weight: 10
url: /nl/net/excel-security/advanced-protection-settings-for-excel-worksheet/
---
In deze zelfstudie leiden we u door de stappen voor het instellen van geavanceerde beveiligingsinstellingen voor een Excel-spreadsheet met behulp van de Aspose.Cells-bibliotheek voor .NET. Volg de onderstaande instructies om deze taak te voltooien.

## Stap 1: Voorbereiding

Zorg ervoor dat u Aspose.Cells voor .NET hebt geïnstalleerd en een C#-project hebt gemaakt in de geïntegreerde ontwikkelomgeving (IDE) van uw voorkeur.

## Stap 2: Stel het pad naar de documentmap in

 Verklaar een`dataDir` variabele en initialiseer deze met het pad naar uw documentenmap. Bijvoorbeeld :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Zeker vervangen`"YOUR_DOCUMENTS_DIRECTORY"` met het daadwerkelijke pad naar uw directory.

## Stap 3: Maak een bestandsstream om het Excel-bestand te openen

 Maak een`FileStream` object met het Excel-bestand dat moet worden geopend:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 Zorg ervoor dat u het Excel-bestand hebt`book1.xls` in uw documentenmap of geef de juiste bestandsnaam en locatie op.

## Stap 4: Instantieer een werkmapobject en open het Excel-bestand

 Gebruik de`Workbook`class van Aspose.Cells om een Workbook-object te instantiëren en het opgegeven Excel-bestand te openen via de bestandsstroom:

```csharp
Workbook excel = new Workbook(fstream);
```

## Stap 5: Open het eerste werkblad

Navigeer naar het eerste werkblad van het Excel-bestand:

```csharp
Worksheet worksheet = excel.Worksheets[0];
```

## Stap 6: Stel de werkbladbeveiligingsinstellingen in

Gebruik de eigenschappen van werkbladobjecten om indien nodig de beveiligingsinstellingen voor werkbladen in te stellen. Bijvoorbeeld :

```csharp
worksheet.Protection.AllowDeletingColumn = false;
worksheet.Protection.AllowDeletingRow = false;
worksheet.Protection.AllowEditingContent = false;
worksheet.Protection.AllowEditingObject = false;
// ... Stel indien nodig andere beveiligingsinstellingen in...
```

## Stap 7: Sla het gewijzigde Excel-bestand op

 Sla het gewijzigde Excel-bestand op met behulp van de`Save` methode van het Workbook-object:

```csharp
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

Zorg ervoor dat u het gewenste pad en de gewenste bestandsnaam voor het uitvoerbestand opgeeft.

## Stap 8: Sluit de bestandsstream

Eenmaal opgeslagen, sluit u de bestandsstream om alle bijbehorende bronnen vrij te geven:

```csharp
fstream.Close();
```
	
### Voorbeeldbroncode voor geavanceerde beveiligingsinstellingen voor Excel-werkblad met Aspose.Cells voor .NET 
```csharp
//Het pad naar de documentenmap.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Een bestandsstream maken met het te openen Excel-bestand
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Een werkmapobject instantiëren
// Het Excel-bestand openen via de bestandsstream
Workbook excel = new Workbook(fstream);
// Toegang tot het eerste werkblad in het Excel-bestand
Worksheet worksheet = excel.Worksheets[0];
// Gebruikers beperken in het verwijderen van kolommen van het werkblad
worksheet.Protection.AllowDeletingColumn = false;
// Gebruikers beperken om de rij van het werkblad te verwijderen
worksheet.Protection.AllowDeletingRow = false;
// Gebruikers beperken in het bewerken van de inhoud van het werkblad
worksheet.Protection.AllowEditingContent = false;
// Gebruikers beperken om objecten van het werkblad te bewerken
worksheet.Protection.AllowEditingObject = false;
// Gebruikers beperken in het bewerken van scenario's van het werkblad
worksheet.Protection.AllowEditingScenario = false;
//Gebruikers beperken om te filteren
worksheet.Protection.AllowFiltering = false;
// Gebruikers toestaan cellen van het werkblad op te maken
worksheet.Protection.AllowFormattingCell = true;
// Gebruikers toestaan rijen van het werkblad op te maken
worksheet.Protection.AllowFormattingRow = true;
// Gebruikers toestaan kolommen in het werkblad in te voegen
worksheet.Protection.AllowFormattingColumn = true;
// Gebruikers toestaan hyperlinks in het werkblad in te voegen
worksheet.Protection.AllowInsertingHyperlink = true;
// Gebruikers toestaan rijen in het werkblad in te voegen
worksheet.Protection.AllowInsertingRow = true;
// Gebruikers toestaan vergrendelde cellen van het werkblad te selecteren
worksheet.Protection.AllowSelectingLockedCell = true;
// Gebruikers toestaan ontgrendelde cellen van het werkblad te selecteren
worksheet.Protection.AllowSelectingUnlockedCell = true;
// Gebruikers toestaan te sorteren
worksheet.Protection.AllowSorting = true;
// Gebruikers toestaan draaitabellen in het werkblad te gebruiken
worksheet.Protection.AllowUsingPivotTable = true;
// Het gewijzigde Excel-bestand opslaan
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
// De bestandsstroom sluiten om alle bronnen vrij te maken
fstream.Close();
```

## Conclusie

Gefeliciteerd! U hebt nu geleerd hoe u geavanceerde beveiligingsinstellingen voor een Excel-spreadsheet kunt instellen met Aspose.Cells voor .NET. Gebruik deze kennis om uw Excel-bestanden te beveiligen en gebruikersacties te beperken.

### Veelgestelde vragen

#### Vraag: Hoe kan ik een nieuw C#-project maken in mijn IDE?

A: De stappen voor het maken van een nieuw C#-project kunnen variëren, afhankelijk van de IDE die u gebruikt. Raadpleeg de documentatie van uw IDE voor gedetailleerde instructies.

#### Vraag: Is het mogelijk om andere aangepaste beveiligingsinstellingen in te stellen dan die vermeld in de zelfstudie?

A: Ja, Aspose.Cells biedt een breed scala aan beveiligingsinstellingen die u kunt aanpassen aan uw specifieke behoeften. Zie de Aspose.Cells-documentatie voor meer details.

#### Vraag: Wat is het bestandsformaat dat wordt gebruikt om het gewijzigde Excel-bestand in de voorbeeldcode op te slaan?

A: In de voorbeeldcode wordt het gewijzigde Excel-bestand opgeslagen in Excel 97-2003 (.xls)-formaat. U kunt indien nodig andere formaten kiezen die door Aspose.Cells worden ondersteund.

#### Vraag: Hoe krijg ik toegang tot andere werkbladen in het Excel-bestand?

 A: U kunt toegang krijgen tot andere werkbladen met behulp van de index of de bladnaam, bijvoorbeeld:`Worksheet worksheet = excel.Worksheets[1];` of`Worksheet worksheet = excel.Worksheets[" SheetName"];`.