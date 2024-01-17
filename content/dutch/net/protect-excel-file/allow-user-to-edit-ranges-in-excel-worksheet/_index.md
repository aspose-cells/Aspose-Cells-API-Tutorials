---
title: Sta de gebruiker toe om bereiken in het Excel-werkblad te bewerken
linktitle: Sta de gebruiker toe om bereiken in het Excel-werkblad te bewerken
second_title: Aspose.Cells voor .NET API-referentie
description: Sta gebruikers toe specifieke bereiken in een Excel-spreadsheet te bewerken met Aspose.Cells voor .NET. Stap voor stap handleiding met broncode in C#.
type: docs
weight: 10
url: /nl/net/protect-excel-file/allow-user-to-edit-ranges-in-excel-worksheet/
---
In deze handleiding laten we u zien hoe u Aspose.Cells voor .NET kunt gebruiken, zodat de gebruiker specifieke bereiken in een Excel-spreadsheet kan bewerken. Volg de onderstaande stappen om deze taak te volbrengen.

## Stap 1: De omgeving instellen

Zorg ervoor dat u uw ontwikkelomgeving hebt ingesteld en Aspose.Cells voor .NET hebt geïnstalleerd. U kunt de nieuwste versie van de bibliotheek downloaden van de officiële website van Aspose.

## Stap 2: Importeer de vereiste naamruimten

Importeer in uw C#-project de benodigde naamruimten om met Aspose.Cells te werken:

```csharp
using Aspose.Cells;
```

## Stap 3: Het pad naar de documentenmap instellen

 Verklaar een`dataDir` variabele om het pad op te geven naar de map waar u het gegenereerde Excel-bestand wilt opslaan:

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Zeker vervangen`"YOUR_DOCUMENT_DIRECTORY"` met het juiste pad op uw systeem.

## Stap 4: Een werkmapobject maken

Instantieer een nieuw werkmapobject dat de Excel-werkmap vertegenwoordigt die u wilt maken:

```csharp
Workbook book = new Workbook();
```

## Stap 5: Toegang tot het eerste werkblad

Navigeer naar het eerste werkblad in de Excel-werkmap met behulp van de volgende code:

```csharp
Worksheet sheet = book.Worksheets[0];
```

## Stap 6: Geautoriseerde wijzigingsbereiken ophalen

 Haal de verzameling toegestane bewerkingsbereiken op met behulp van de`AllowEditRanges` eigendom:

```csharp
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
```

## Stap 7: Definieer een beschermd bereik

 Definieer een beveiligd bereik met behulp van de`Add` werkwijze van de`AllowEditRanges` verzameling:

```csharp
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
protectedRange protectedRange = allowRanges[idx];
```

Hier hebben we een beveiligd bereik "r2" gemaakt dat zich uitstrekt van cel A1 tot cel C3.

## Stap 8: Het wachtwoord opgeven

 Geef een wachtwoord op voor het beveiligde bereik met behulp van de`Password` eigendom:

```csharp
protectedRange.Password = "YOUR_PASSWORD";
```

 Zeker vervangen`"YOUR_PASSWORD"` met het gewenste wachtwoord.

## Stap 9: Het werkblad beschermen

 Beveilig het werkblad met behulp van de`Protect` werkwijze van de`Worksheet` voorwerp:

```csharp
sheet.Protect(ProtectionType.All);
```

Hierdoor wordt de spreadsheet beschermd door elke wijziging buiten het toegestane bereik te voorkomen.

## Stap 10: Registreren van de

  Excel bestand

 Sla het gegenereerde Excel-bestand op met behulp van de`Save` werkwijze van de`Workbook` voorwerp:

```csharp
book.Save(dataDir + "protectedrange.out.xls");
```

Zorg ervoor dat u de gewenste bestandsnaam en het juiste pad opgeeft.

### Voorbeeldbroncode voor Toestaan dat gebruiker bereiken in Excel-werkblad bewerkt met Aspose.Cells voor .NET 
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
proteced_range.Password = "123";
// Bescherm het blad
sheet.Protect(ProtectionType.All);
// Sla het Excel-bestand op
book.Save(dataDir + "protectedrange.out.xls");
```

## Conclusie

U hebt nu geleerd hoe u Aspose.Cells voor .NET kunt gebruiken, zodat de gebruiker specifieke bereiken in een Excel-spreadsheet kan bewerken. Voel je vrij om de functies van Aspose.Cells verder te verkennen om aan jouw specifieke behoeften te voldoen.


### Veelgestelde vragen

#### 1. Hoe kan ik de gebruiker toestaan specifieke bereiken in een Excel-spreadsheet te bewerken?

 U kunt gebruik maken van de`ProtectedRangeCollection` klasse om toegestane wijzigingsbereiken te definiëren. Gebruik de`Add` methode om een nieuw beveiligd bereik met de gewenste cellen te maken.

#### 2. Kan ik een wachtwoord instellen voor geautoriseerde wijzigingsbereiken?

 Ja, u kunt een wachtwoord opgeven via de`Password` eigendom van de`ProtectedRange` voorwerp. Hierdoor wordt de toegang alleen beperkt tot gebruikers met het wachtwoord.

#### 3. Hoe beveilig ik het spreadsheet zodra de toegestane bereiken zijn ingesteld?

 Gebruik de`Protect` werkwijze van de`Worksheet` object om het werkblad te beschermen. Hierdoor worden wijzigingen buiten het toegestane bereik voorkomen en wordt er mogelijk om een wachtwoord gevraagd als u dat hebt opgegeven.