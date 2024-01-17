---
title: Ondersteuning voor Xades-handtekeningen
linktitle: Ondersteuning voor Xades-handtekeningen
second_title: Aspose.Cells voor .NET API-referentie
description: Leer hoe u een Xades-handtekening aan een Excel-bestand toevoegt met Aspose.Cells voor .NET.
type: docs
weight: 190
url: /nl/net/excel-workbook/xades-signature-support/
---
In dit artikel nemen we je stap voor stap mee om de onderstaande C#-broncode uit te leggen, die gaat over ondersteuning van Xades-handtekeningen met behulp van de Aspose.Cells-bibliotheek voor .NET. U leert hoe u deze bibliotheek kunt gebruiken om een digitale Xades-handtekening aan een Excel-bestand toe te voegen. Ook geven wij u een overzicht van het ondertekenproces en de uitvoering ervan. Volg de onderstaande stappen om overtuigende resultaten te krijgen.

## Stap 1: Definieer bron- en uitvoermappen
Om te beginnen moeten we de bron- en uitvoermappen in onze code definiëren. Deze mappen geven aan waar de bronbestanden zich bevinden en waar het uitvoerbestand wordt opgeslagen. Hier is de bijbehorende code:

```csharp
// Bronmap
string sourceDir = RunExamples.Get_SourceDirectory();
// Uitvoermap
string outputDir = RunExamples.Get_OutputDirectory();
```

Zorg ervoor dat u de mappaden indien nodig aanpast.

## Stap 2: Het laden van de Excel-werkmap
De volgende stap is het laden van de Excel-werkmap waaraan we de digitale handtekening van Xades willen toevoegen. Hier is de code om de werkmap te laden:

```csharp
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
```

Zorg ervoor dat u de naam van het bronbestand correct opgeeft in de code.

## Stap 3: De digitale handtekening configureren
Nu zullen we de digitale handtekening van Xades configureren door de nodige informatie te verstrekken. We moeten het PFX-bestand opgeven dat het digitale certificaat bevat, evenals het bijbehorende wachtwoord. Hier is de bijbehorende code:

```csharp
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
```

Zorg ervoor dat u "pfxPassword" vervangt door uw daadwerkelijke wachtwoord en "pfxFile" door het pad naar het PFX-bestand.

## Stap 4: Het toevoegen van de digitale handtekening
Nu we de digitale handtekening hebben geconfigureerd, kunnen we deze toevoegen aan de Excel-werkmap. Hier is de bijbehorende code:

```csharp
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
```

Met deze stap wordt de digitale handtekening van Xades toegevoegd aan de Excel-werkmap.

## Stap 5: De werkmap opslaan met de handtekening
Ten slotte slaan we de Excel-werkmap op met de toegevoegde digitale handtekening. Hier is de bijbehorende code:

```csharp
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
```

Zorg ervoor dat u de naam van het uitvoerbestand aanpast aan uw behoeften.

### Voorbeeldbroncode voor Xades Signature-ondersteuning met Aspose.Cells voor .NET 
```csharp
//Bronmap
string sourceDir = RunExamples.Get_SourceDirectory();
//Uitvoermap
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
Console.WriteLine("XAdESSignatureSupport executed successfully.");
```

## Conclusie
Gefeliciteerd! U hebt geleerd hoe u de Aspose.Cells-bibliotheek voor .NET kunt gebruiken om een digitale Xades-handtekening aan een Excel-bestand toe te voegen. Door de stappen in dit artikel te volgen, kunt u deze functionaliteit in uw eigen projecten implementeren. Voel je vrij om meer met de bibliotheek te experimenteren en andere krachtige functies te ontdekken die deze biedt.

### Veelgestelde vragen

#### Vraag: Wat is Xades?

A: Xades is een geavanceerde standaard voor elektronische handtekeningen die wordt gebruikt om de integriteit en authenticiteit van digitale documenten te garanderen.

#### Vraag: Kan ik andere soorten digitale handtekeningen gebruiken met Aspose.Cells?

A: Ja, Aspose.Cells ondersteunt ook andere soorten digitale handtekeningen, zoals XMLDSig-handtekeningen en PKCS#7-handtekeningen.

#### Vraag: Kan ik een handtekening toepassen op andere bestandstypen dan Excel-bestanden?
 
A: Ja, Aspose.Cells maakt het ook mogelijk om digitale handtekeningen toe te passen op andere ondersteunde bestandstypen, zoals Word-, PDF- en PowerPoint-bestanden.