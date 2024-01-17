---
title: Voeg een digitale handtekening toe aan een reeds ondertekend Excel-bestand
linktitle: Voeg een digitale handtekening toe aan een reeds ondertekend Excel-bestand
second_title: Aspose.Cells voor .NET API-referentie
description: Voeg eenvoudig digitale handtekeningen toe aan bestaande Excel-bestanden met Aspose.Cells voor .NET.
type: docs
weight: 30
url: /nl/net/excel-workbook/add-digital-signature-to-an-already-signed-excel-file/
---
In deze stapsgewijze handleiding leggen we de meegeleverde C#-broncode uit waarmee u een digitale handtekening kunt toevoegen aan een reeds ondertekend Excel-bestand met behulp van Aspose.Cells voor .NET. Volg de onderstaande stappen om een nieuwe digitale handtekening toe te voegen aan een bestaand Excel-bestand.

## Stap 1: Stel de bron- en uitvoermappen in

```csharp
// bronmap
string sourceDir = RunExamples.Get_SourceDirectory();

// Uitvoermap
string outputDir = RunExamples.Get_OutputDirectory();
```

In deze eerste stap definiëren we de bron- en uitvoermappen die zullen worden gebruikt om het bestaande Excel-bestand te laden en het bestand op te slaan met de nieuwe digitale handtekening.

## Stap 2: Bestaand Excel-bestand laden

```csharp
// Laad de reeds ondertekende Excel-werkmap
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
```

 Hier laden we het reeds ondertekende Excel-bestand met behulp van de`Workbook` klasse van Aspose.Cells.

## Stap 3: Creëer de verzameling digitale handtekeningen

```csharp
// Creëer de verzameling digitale handtekeningen
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
```

 We creëren een nieuwe verzameling digitale handtekeningen met behulp van de`DigitalSignatureCollection` klas.

## Stap 4: Maak een nieuw certificaat

```csharp
// Maak een nieuw certificaat
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
```

Hier maken we een nieuw certificaat aan op basis van het opgegeven bestand en wachtwoord.

## Stap 5: Voeg een nieuwe digitale handtekening toe aan de collectie

```csharp
// Maak een nieuwe digitale handtekening
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added a new digital signature to the already signed workbook.", DateTime.Now);

// Voeg de digitale handtekening toe aan de collectie
dsCollection.Add(signature);
```

 We maken een nieuwe digitale handtekening met behulp van de`DigitalSignature` klasse en voeg deze toe aan de verzameling digitale handtekeningen.

## Stap 6: Voeg de verzameling digitale handtekeningen toe aan de werkmap

```csharp
//Voeg de verzameling digitale handtekeningen toe aan de werkmap
workbook.AddDigitalSignature(dsCollection);
```

 We voegen de verzameling digitale handtekeningen toe aan de bestaande Excel-werkmap met behulp van de`AddDigitalSignature()` methode.

## Stap 7: Bewaar en sluit de werkmap

```csharp
// Sla de werkmap op en sluit deze
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
```

We slaan de werkmap op met de nieuwe digitale handtekening in de opgegeven uitvoermap, sluiten deze vervolgens en geven de bijbehorende bronnen vrij.

### Voorbeeldbroncode voor het toevoegen van een digitale handtekening aan een reeds ondertekend Excel-bestand met Aspose.Cells voor .NET 
```csharp
//Bronmap
string sourceDir = RunExamples.Get_SourceDirectory();
//Uitvoermap
string outputDir = RunExamples.Get_OutputDirectory();
//Certificaatbestand en het bijbehorende wachtwoord
string certFileName = sourceDir + "AsposeDemo.pfx";
string password = "aspose";
//Laad de werkmap die al digitaal is ondertekend om een nieuwe digitale handtekening toe te voegen
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
//Maak de verzameling digitale handtekeningen
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
//Nieuw certificaat maken
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
//Maak een nieuwe digitale handtekening en voeg deze toe aan de verzameling digitale handtekeningen
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added new digital signature in existing digitally signed workbook.", DateTime.Now);
dsCollection.Add(signature);
//Voeg een verzameling digitale handtekeningen toe aan de werkmap
workbook.AddDigitalSignature(dsCollection);
//Sla de werkmap op en gooi deze weg.
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
Console.WriteLine("AddDigitalSignatureToAnAlreadySignedExcelFile executed successfully.\r\n");
```

## Conclusie

Gefeliciteerd! U hebt nu geleerd hoe u een digitale handtekening kunt toevoegen aan een reeds ondertekend Excel-bestand met behulp van Aspose.Cells voor .NET. Digitale handtekeningen voegen een extra beveiligingslaag toe aan uw Excel-bestanden, waardoor de authenticiteit en integriteit ervan wordt gegarandeerd.

### Veelgestelde vragen

#### Vraag: Wat is Aspose.Cells voor .NET?

A: Aspose.Cells voor .NET is een krachtige klassenbibliotheek waarmee .NET-ontwikkelaars eenvoudig Excel-bestanden kunnen maken, wijzigen, converteren en manipuleren.

#### Vraag: Wat is een digitale handtekening in een Excel-bestand?

A: Een digitale handtekening in een Excel-bestand is een elektronisch merkteken dat de authenticiteit, integriteit en herkomst van het document garandeert. Het wordt gebruikt om te verifiëren dat het bestand niet is gewijzigd sinds het is ondertekend en afkomstig is van een betrouwbare bron.

#### Vraag: Wat zijn de voordelen van het toevoegen van een digitale handtekening aan een Excel-bestand?

A: Het toevoegen van een digitale handtekening aan een Excel-bestand biedt verschillende voordelen, waaronder bescherming tegen ongeoorloofde wijzigingen, het garanderen van gegevensintegriteit, het authenticeren van de auteur van het document en het bieden van vertrouwen in de informatie die het bevat.

#### Vraag: Kan ik meerdere digitale handtekeningen toevoegen aan een Excel-bestand?

A: Ja, met Aspose.Cells kunt u meerdere digitale handtekeningen toevoegen aan een Excel-bestand. U kunt een verzameling digitale handtekeningen maken en deze in één handeling aan het bestand toevoegen.

#### Vraag: Wat zijn de vereisten voor het toevoegen van een digitale handtekening aan een Excel-bestand?

A: Om een digitale handtekening aan een Excel-bestand toe te voegen, heeft u een geldig digitaal certificaat nodig dat zal worden gebruikt om het document te ondertekenen. Zorg ervoor dat u over het juiste certificaat en wachtwoord beschikt voordat u de digitale handtekening toevoegt.