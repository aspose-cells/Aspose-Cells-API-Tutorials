---
title: Bescherm specifieke kolom in Excel-werkblad
linktitle: Bescherm specifieke kolom in Excel-werkblad
second_title: Aspose.Cells voor .NET API-referentie
description: Leer hoe u een specifieke kolom in een Excel-werkblad kunt beveiligen met Aspose.Cells voor .NET. Stap voor stap handleiding in C#.
type: docs
weight: 80
url: /nl/net/protect-excel-file/protect-specific-column-in-excel-worksheet/
---
Wanneer u met Excel-werkbladen in C# werkt, is het vaak nodig om specifieke kolommen te beveiligen om onbedoelde wijzigingen te voorkomen. In deze zelfstudie begeleiden we u bij het beveiligen van een specifieke kolom in een Excel-werkblad met behulp van de Aspose.Cells voor .NET-bibliotheek. Wij geven u stapsgewijs uitleg over de C#-broncode die u hiervoor nodig heeft. Dus laten we beginnen!

## Overzicht van het beveiligen van specifieke kolommen in een Excel-werkblad

Door specifieke kolommen in een Excel-werkblad te beveiligen, zorgt u ervoor dat deze kolommen vergrendeld blijven en niet kunnen worden gewijzigd zonder de juiste autorisatie. Dit is met name handig als u de bewerkingstoegang tot bepaalde gegevens of formules wilt beperken, terwijl gebruikers wel met de rest van het werkblad kunnen communiceren. De Aspose.Cells voor .NET-bibliotheek biedt een uitgebreide reeks functies om Excel-bestanden programmatisch te manipuleren, inclusief kolombeveiliging.

## De omgeving instellen

Voordat we beginnen, moet u ervoor zorgen dat de Aspose.Cells voor .NET-bibliotheek in uw ontwikkelomgeving is geïnstalleerd. U kunt de bibliotheek downloaden van de officiële Aspose-website en installeren met behulp van het meegeleverde installatieprogramma.

## Een nieuwe werkmap en werkblad maken

Om specifieke kolommen te gaan beschermen, moeten we een nieuwe werkmap en werkblad maken met Aspose.Cells voor .NET. Hier is het codefragment:

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
```

Zorg ervoor dat u "UW DOCUMENTENMAP" vervangt door het daadwerkelijke mappad waar u het Excel-bestand wilt opslaan.

## De stijl en stijlvlagobjecten definiëren

Om specifieke stijlen en beveiligingsvlaggen voor de kolommen in te stellen, moeten we de stijl- en stijlvlagobjecten definiëren. Hier is het codefragment:

```csharp
// Definieer het stijlobject.
Style style;

// Definieer het stijlvlagobject.
StyleFlag flag;
```

## Door kolommen bladeren en ze ontgrendelen

Vervolgens moeten we alle kolommen in het werkblad doorlopen en ze ontgrendelen. Dit zorgt ervoor dat alle kolommen bewerkbaar zijn, behalve degene die we willen beschermen. Hier is het codefragment:

```csharp
// Loop door alle kolommen in het werkblad en ontgrendel ze.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    flag = new StyleFlag();
    flag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
```

## Een specifieke kolom vergrendelen

Laten we nu een specifieke kolom vergrendelen. In dit voorbeeld vergrendelen we de eerste kolom (kolomindex 0). Hier is het codefragment:

```csharp
// Haal de eerste kolomstijl op.
style = sheet.Cells.Columns[0].Style;

// Sluit het.
style.IsLocked = true;
```

## Stijlen toepassen op kolommen

Nadat we de specifieke kolom hebben vergrendeld, moeten we de stijl en vlag op die kolom toepassen. Hier is het codefragment:

```csharp
//Instantieer de vlag.
flag = new StyleFlag();

// Stel de vergrendelingsinstelling in.
flag.Locked = true;

// Pas de stijl toe op de eerste kolom.
sheet.Cells.Columns[0].ApplyStyle(style, flag);
```

## Het werkblad beschermen

Om de beveiliging te voltooien, moeten we het werkblad beveiligen om ervoor te zorgen dat de vergrendelde kolommen niet kunnen worden gewijzigd. Hier is het codefragment:

```csharp
// Bescherm het blad.
sheet.Protect(ProtectionType.All);
```

## Het Excel-bestand opslaan

Tenslotte slaan wij het gewijzigde Excel-bestand op de gewenste locatie op. Hier is het codefragment:

```csharp
// Sla het Excel-bestand op.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Zorg ervoor dat u "output.out.xls" vervangt door de gewenste bestandsnaam en extensie.

### Voorbeeldbroncode voor het beveiligen van specifieke kolommen in Excel-werkbladen met Aspose.Cells voor .NET 
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
// Definieer het styleflag-object.
StyleFlag flag;
// Loop door alle kolommen in het werkblad en ontgrendel ze.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    flag = new StyleFlag();
    flag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
// Haal de eerste kolomstijl op.
style = sheet.Cells.Columns[0].Style;
// Sluit het.
style.IsLocked = true;
//Instantieer de vlag.
flag = new StyleFlag();
// Stel de vergrendelingsinstelling in.
flag.Locked = true;
// Pas de stijl toe op de eerste kolom.
sheet.Cells.Columns[0].ApplyStyle(style, flag);
// Bescherm het blad.
sheet.Protect(ProtectionType.All);
// Sla het Excel-bestand op.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## Conclusie

In deze zelfstudie hebben we het stapsgewijze proces uitgelegd voor het beveiligen van een specifieke kolom in een Excel-werkblad met behulp van de Aspose.Cells voor .NET-bibliotheek. We zijn begonnen met het maken van een nieuwe werkmap en een nieuw werkblad, waarbij we de stijl- en stijlvlagobjecten definieerden, en gingen vervolgens verder met het ontgrendelen en vergrendelen van specifieke kolommen. Ten slotte hebben we het werkblad beveiligd en het gewijzigde Excel-bestand opgeslagen. Door deze handleiding te volgen, zou u nu specifieke kolommen in Excel-werkbladen moeten kunnen beveiligen met C# en Aspose.Cells voor .NET.

### Veelgestelde vragen (FAQ's)

#### Kan ik meerdere kolommen beveiligen met deze methode?

Ja, u kunt meerdere kolommen beveiligen door de code dienovereenkomstig aan te passen. Loop eenvoudig door het gewenste kolombereik en pas de vergrendelingsstijlen en vlaggen toe.

#### Is het mogelijk om het beveiligde werkblad met een wachtwoord te beveiligen?

 Ja, u kunt wachtwoordbeveiliging toevoegen aan het beveiligde werkblad door het wachtwoord op te geven terwijl u de`Protect` methode.

#### Ondersteunt Aspose.Cells voor .NET andere Excel-bestandsindelingen?

Ja, Aspose.Cells voor .NET ondersteunt verschillende Excel-bestandsindelingen, waaronder XLS, XLSX, XLSM en meer.

#### Kan ik specifieke rijen in plaats van kolommen beveiligen?

Ja, u kunt de code aanpassen om specifieke rijen in plaats van kolommen te beschermen door de stijlen en vlaggen toe te passen op rijcellen in plaats van kolomcellen.