---
title: Geef auteur op tijdens schrijfbeveiliging van Excel-werkmap
linktitle: Geef auteur op tijdens schrijfbeveiliging van Excel-werkmap
second_title: Aspose.Cells voor .NET API-referentie
description: Leer hoe u uw Excel-werkmappen kunt beveiligen en aanpassen met Aspose.Cells voor .NET. Stap voor stap tutorial in C#.
type: docs
weight: 30
url: /nl/net/excel-security/specify-author-while-write-protecting-excel-workbook/
---

In deze zelfstudie laten we u zien hoe u de auteur kunt opgeven bij het beveiligen van een Excel-werkmap tegen schrijven met behulp van de Aspose.Cells-bibliotheek voor .NET.

## Stap 1: De omgeving voorbereiden

Zorg ervoor dat Aspose.Cells voor .NET op uw computer is geïnstalleerd voordat u begint. Download de bibliotheek van de officiële website van Aspose en volg de meegeleverde installatie-instructies.

## Stap 2: Bron- en uitvoermappen configureren

In de meegeleverde broncode moet u de bron- en uitvoermappen opgeven. Wijzig de`sourceDir` En`outputDir` variabelen door "UW BRON DIRECTORY" en "UW UITVOER DIRECTORY" te vervangen door de respectievelijke absolute paden op uw computer.

```csharp
// Bronmap
string sourceDir = "PATH TO YOUR SOURCE DIRECTORY";

// Uitvoermap
string outputDir = "YOUR OUTPUT DIRECTORY PATH";
```

## Stap 3: Een lege Excel-werkmap maken

Om te beginnen maken we een Workbook-object dat een lege Excel-werkmap vertegenwoordigt.

```csharp
// Maak een lege werkmap.
Workbook wb = new Workbook();
```

## Stap 4: Schrijfbeveiliging met wachtwoord

 Vervolgens specificeren we een wachtwoord om de Excel-werkmap tegen schrijven te beveiligen met behulp van de`WriteProtection.Password` eigenschap van het Workbook-object.

```csharp
// Schrijfbeveiligde werkmap met wachtwoord.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";
```

## Stap 5: Auteursspecificatie

 Nu specificeren we de auteur van de Excel-werkmap met behulp van de`WriteProtection.Author` eigenschap van het Workbook-object.

```csharp
// Geef de auteur op terwijl u de werkmap tegen schrijven beschermt.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";
```

## Stap 6: Maak een back-up van een beveiligde Excel-werkmap

 Zodra de schrijfbeveiliging en de auteur zijn opgegeven, kunnen we de Excel-werkmap opslaan in het XLSX-formaat met behulp van de`Save()` methode.

```csharp
// Sla de werkmap op in XLSX-indeling.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");
```

### Voorbeeldbroncode voor Auteur opgeven tijdens schrijfbeveiliging Excel-werkmap met Aspose.Cells voor .NET 
```csharp
//Bronmap
string sourceDir = "YOUR SOURCE DIRECTORY";

//Uitvoermap
string outputDir = "YOUR OUTPUT DIRECTORY";

// Maak een lege werkmap.
Workbook wb = new Workbook();

// Schrijfbeveiligde werkmap met wachtwoord.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";

// Geef de auteur op terwijl u de werkmap tegen schrijven beschermt.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";

// Sla de werkmap op in XLSX-indeling.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");

```

## Conclusie

Gefeliciteerd! U hebt nu geleerd hoe u de auteur kunt opgeven bij het beveiligen van een Excel-werkmap met Aspose.Cells voor .NET. U kunt deze stappen toepassen op uw eigen projecten om uw Excel-werkmappen te beschermen en aan te passen.

Voel je vrij om de functies van Aspose.Cells voor .NET verder te verkennen voor meer geavanceerde bewerkingen op Excel-bestanden.

## Veelgestelde vragen

#### Vraag: Kan ik een Excel-werkmap tegen schrijven beveiligen zonder een wachtwoord op te geven?

 A: Ja, u kunt het Workbook-object gebruiken`WriteProtect()` methode zonder een wachtwoord op te geven om een Excel-werkmap tegen schrijven te beveiligen. Hierdoor worden wijzigingen in de werkmap beperkt zonder dat een wachtwoord vereist is.

#### Vraag: Hoe verwijder ik de schrijfbeveiliging van een Excel-werkmap?

 A: Om de schrijfbeveiliging van een Excel-werkmap te verwijderen, kunt u de`Unprotect()` methode van het werkbladobject of de`RemoveWriteProtection()` methode van het Workbook-object, afhankelijk van uw specifieke gebruiksscenario. .

#### Vraag: Ik ben het wachtwoord vergeten om mijn Excel-werkmap te beschermen. Wat kan ik doen ?

A: Als u het wachtwoord bent vergeten om uw Excel-werkmap te beschermen, kunt u dit niet rechtstreeks verwijderen. U kunt echter proberen gespecialiseerde hulpprogramma's van derden te gebruiken die functies voor wachtwoordherstel bieden voor beveiligde Excel-bestanden.

#### Vraag: Is het mogelijk om meerdere auteurs op te geven bij het beveiligen van een Excel-werkmap tegen schrijven?

A: Nee, met de Aspose.Cells voor .NET-bibliotheek kunt u één auteur opgeven bij het beveiligen van een Excel-werkmap tegen schrijven. Als u meerdere auteurs wilt opgeven, moet u aangepaste oplossingen overwegen door het Excel-bestand rechtstreeks te manipuleren.