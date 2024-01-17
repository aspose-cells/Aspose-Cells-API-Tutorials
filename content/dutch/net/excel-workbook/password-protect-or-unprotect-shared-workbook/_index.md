---
title: Wachtwoord beveiligen of de beveiliging van een gedeelde werkmap opheffen
linktitle: Wachtwoord beveiligen of de beveiliging van een gedeelde werkmap opheffen
second_title: Aspose.Cells voor .NET API-referentie
description: Leer hoe u een gedeelde werkmap met een wachtwoord kunt beveiligen of de beveiliging ervan kunt opheffen met Aspose.Cells voor .NET.
type: docs
weight: 120
url: /nl/net/excel-workbook/password-protect-or-unprotect-shared-workbook/
---
Het beveiligen van een gedeelde werkmap met een wachtwoord is belangrijk om de gegevensprivacy te garanderen. Met Aspose.Cells voor .NET kunt u eenvoudig een gedeelde werkmap beveiligen of de beveiliging ervan opheffen met behulp van wachtwoorden. Volg de onderstaande stappen om de gewenste resultaten te krijgen:

## Stap 1: Geef de uitvoermap op

Eerst moet u de uitvoermap opgeven waar het beveiligde Excel-bestand zal worden opgeslagen. Hier leest u hoe u dit doet met Aspose.Cells:

```csharp
// Uitvoermap
string outputDir = RunExamples.Get_OutputDirectory();
```

## Stap 2: Maak een leeg Excel-bestand

Vervolgens kunt u een leeg Excel-bestand maken waarop u de beveiliging wilt toepassen of de beveiliging wilt opheffen. Hier is een voorbeeldcode:

```csharp
// Maak een lege Excel-werkmap
Workbook wb = new Workbook();
```

## Stap 3: Beveilig de gedeelde werkmap of hef de beveiliging op

Nadat u de werkmap hebt gemaakt, kunt u de gedeelde werkmap beveiligen of de beveiliging ervan opheffen door het juiste wachtwoord op te geven. Hier is hoe:

```csharp
// Beveilig de gedeelde werkmap met een wachtwoord
wb.ProtectSharedWorkbook("1234");

// Verwijder het commentaar op deze regel om de beveiliging van de gedeelde werkmap op te heffen
// wb.UnprotectSharedWorkbook("1234");
```

## Stap 4: Sla het uitgevoerde Excel-bestand op

Nadat u de beveiliging hebt toegepast of de beveiliging heeft opgeheven, kunt u het beveiligde Excel-bestand opslaan in de opgegeven uitvoermap. Hier leest u hoe u het moet doen:

```csharp
// Sla het uitgevoerde Excel-bestand op
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

### Voorbeeldbroncode voor het beveiligen of opheffen van de beveiliging van een gedeelde werkmap met Aspose.Cells voor .NET 
```csharp
//Uitvoermap
string outputDir = RunExamples.Get_OutputDirectory();
//Maak een leeg Excel-bestand
Workbook wb = new Workbook();
//Bescherm de gedeelde werkmap met een wachtwoord
wb.ProtectSharedWorkbook("1234");
//Verwijder het commentaar op deze regel om de beveiliging van de gedeelde werkmap op te heffen
//wb.UnprotectSharedWorkbook("1234");
//Sla het uitgevoerde Excel-bestand op
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

## Conclusie

Het beveiligen of opheffen van de beveiliging van een gedeelde werkmap met een wachtwoord is essentieel om de gegevensbeveiliging te garanderen. Met Aspose.Cells voor .NET kunt u deze functionaliteit eenvoudig toevoegen aan uw Excel-bestanden. Door de stappen in deze handleiding te volgen, kunt u uw gedeelde werkmappen effectief beveiligen of de beveiliging opheffen met behulp van wachtwoorden. Experimenteer met uw eigen Excel-bestanden en zorg ervoor dat uw gevoelige gegevens veilig zijn.

### Veelgestelde vragen

#### Vraag: Welke soorten beveiliging kan ik toepassen op een werkmap die wordt gedeeld met Aspose.Cells?
    
A: Met Aspose.Cells kunt u een gedeelde werkmap beveiligen door een wachtwoord op te geven om ongeoorloofde toegang, wijziging of verwijdering van gegevens te voorkomen.

#### Vraag: Kan ik een gedeelde werkmap beveiligen zonder een wachtwoord op te geven?
    
A: Ja, u kunt een gedeelde werkmap beveiligen zonder een wachtwoord op te geven. Voor een betere beveiliging wordt echter aanbevolen een sterk wachtwoord te gebruiken.

#### Vraag: Hoe kan ik de beveiliging opheffen van een werkmap die is gedeeld met Aspose.Cells?
    
A: Om de beveiliging van een gedeelde werkmap op te heffen, moet u hetzelfde wachtwoord opgeven dat is gebruikt bij het beveiligen van de werkmap. Hierdoor kan de bescherming worden verwijderd en zijn de gegevens vrij toegankelijk.

#### Vraag: Heeft het beschermen van een gedeelde werkmap invloed op de functies en formules in de werkmap?
    
A: Wanneer u een gedeelde werkmap beveiligt, hebben gebruikers nog steeds toegang tot de functies en formules in de werkmap. Beveiliging heeft alleen invloed op structurele wijzigingen in de werkmap.