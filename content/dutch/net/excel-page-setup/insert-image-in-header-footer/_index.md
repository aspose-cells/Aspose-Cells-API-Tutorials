---
title: Afbeelding invoegen in koptekst-voettekst
linktitle: Afbeelding invoegen in koptekst-voettekst
second_title: Aspose.Cells voor .NET API-referentie
description: Leer hoe u een afbeelding invoegt in de kop- of voettekst van een Excel-document met Aspose.Cells voor .NET. Stap voor stap handleiding met broncode in C#.
type: docs
weight: 60
url: /nl/net/excel-page-setup/insert-image-in-header-footer/
---
De mogelijkheid om een afbeelding in de kop- of voettekst van een Excel-document in te voegen kan erg handig zijn voor het aanpassen van uw rapporten of het toevoegen van bedrijfslogo's. In dit artikel begeleiden we u stap voor stap bij het invoegen van een afbeelding in de kop- of voettekst van een Excel-document met behulp van Aspose.Cells voor .NET. U leert hoe u dit kunt bereiken met behulp van C#-broncode.

## Stap 1: De omgeving instellen

Zorg ervoor dat Aspose.Cells voor .NET op uw computer is geïnstalleerd voordat u begint. Maak ook een nieuw project aan in de ontwikkelomgeving van uw voorkeur.

## Stap 2: Importeer de benodigde bibliotheken

Importeer in uw codebestand de bibliotheken die nodig zijn om met Aspose.Cells te werken. Hier is de bijbehorende code:

```csharp
using Aspose.Cells;
```

## Stap 3: Stel de documentmap in

Stel de map in waar het Excel-document waarmee u wilt werken zich bevindt. Gebruik de volgende code om de map in te stellen:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

Zorg ervoor dat u het volledige mappad opgeeft.

## Stap 4: Een werkmapobject maken

Het Workbook-object vertegenwoordigt het Excel-document waarmee u gaat werken. Je kunt het maken met de volgende code:

```csharp
Workbook workbook = new Workbook();
```

Hierdoor wordt een nieuw leeg werkmapobject gemaakt.

## Stap 5: De afbeeldings-URL opslaan

Definieer de URL of het pad van de afbeelding die u in de kop- of voettekst wilt invoegen. Gebruik de volgende code om de afbeeldings-URL op te slaan:

```csharp
string logo_url = dataDir + "aspose-logo.jpg";
```

Zorg ervoor dat het opgegeven pad correct is en dat de afbeelding op die locatie bestaat.

## Stap 6: Het afbeeldingsbestand openen

Om het afbeeldingsbestand te openen, gebruiken we een FileStream-object en lezen we de binaire gegevens uit de afbeelding. Hier is de bijbehorende code:

```csharp
FileStream inFile;
byte[] binaryData;

inFile = new System.IO.FileStream(logo_url, System.IO.FileMode.Open, System.IO.FileAccess.Read);
binaryData = new Byte[inFile.Length];
long bytesRead = inFile.Read(binaryData, 0, (int)inFile.Length);
```

Zorg ervoor dat het afbeeldingspad correct is en dat u over de juiste toegangsrechten beschikt.

## Stap 7: Configureren van de PageSetup

Het PageSetup-object wordt gebruikt om de pagina-instellingen van het Excel-document in te stellen, inclusief de kop- en voettekst. Gebruik de volgende code om het PageSetup-object van het eerste werkblad op te halen:

```csharp
PageSetup pageSetup = workbook. Worksheets

[0].PageSetup;
```

Hiermee krijgt u toegang tot de pagina-instellingen voor het eerste werkblad in de werkmap.

## Stap 8: De afbeelding aan de header toevoegen

Gebruik de SetHeaderPicture() -methode van het PageSetup-object om de afbeelding in het middelste gedeelte van de paginakop in te stellen. Hier is de bijbehorende code:

```csharp
pageSetup.SetHeaderPicture(1, binaryData);
```

Hierdoor wordt de opgegeven afbeelding aan de paginakop toegevoegd.

## Stap 9: Een script aan de header toevoegen

Als u script aan de paginakop wilt toevoegen, gebruikt u de SetHeader()-methode van het PageSetup-object. Hier is de bijbehorende code:

```csharp
pageSetup.SetHeader(1, "&G");
```

Hierdoor wordt het opgegeven script aan de paginakop toegevoegd. In dit voorbeeld geeft het script "&G" het paginanummer weer.

## Stap 10: Voeg de bladnaam toe aan de koptekst

Om de bladnaam in de paginakop weer te geven, gebruikt u opnieuw de SetHeader()-methode van het PageSetup-object. Hier is de bijbehorende code:

```csharp
pageSetup.SetHeader(2, "&A");
```

Hiermee wordt de bladnaam aan de paginakop toegevoegd. Het "&A"-script wordt gebruikt om de bladnaam weer te geven.

## Stap 11: De werkmap opslaan

Als u wijzigingen in de werkmap wilt opslaan, gebruikt u de Save()-methode van het Workbook-object. Hier is de bijbehorende code:

```csharp
workbook.Save(dataDir + "InsertImageInHeaderFooter_out.xls");
```

Hiermee wordt de werkmap opgeslagen met de wijzigingen in de opgegeven map.

## Stap 12: FileStream sluiten

Nadat u de binaire gegevens van de afbeelding hebt gelezen, moet u FileStream sluiten om de bronnen vrij te maken. Gebruik de volgende code om FileStream te sluiten:

```csharp
inFile.Close();
```

Zorg ervoor dat u FileStreams altijd sluit als u klaar bent met het gebruik ervan.

### Voorbeeldbroncode voor het invoegen van een afbeelding in de koptekstvoettekst met Aspose.Cells voor .NET 
```csharp
//Het pad naar de documentenmap.
string dataDir = "YOUR DOCUMENT DIRECTORY";
//Een werkmapobject maken
Workbook workbook = new Workbook();
// Een stringvariabele maken om de URL van het logo/de afbeelding op te slaan
string logo_url = dataDir + "aspose-logo.jpg";
// Een FileStream-object declareren
FileStream inFile;
// Een byte-array declareren
byte[] binaryData;
// Het exemplaar van het FileStream-object maken om het logo/de afbeelding in de stream te openen
inFile = new System.IO.FileStream(logo_url, System.IO.FileMode.Open, System.IO.FileAccess.Read);
// Instantie van de byte-array van de grootte van het FileStream-object
binaryData = new Byte[inFile.Length];
// Leest een blok bytes uit de stroom en schrijft gegevens in een bepaalde buffer of byte-array.
long bytesRead = inFile.Read(binaryData, 0, (int)inFile.Length);
// Een PageSetup-object maken om de pagina-instellingen van het eerste werkblad van de werkmap op te halen
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Het logo/afbeelding instellen in het centrale gedeelte van de paginakop
pageSetup.SetHeaderPicture(1, binaryData);
// Het script voor het logo/de afbeelding instellen
pageSetup.SetHeader(1, "&G");
// De naam van het blad instellen in het rechtergedeelte van de paginakop met het script
pageSetup.SetHeader(2, "&A");
// De werkmap opslaan
workbook.Save(dataDir + "InsertImageInHeaderFooter_out.xls");
//Het FileStream-object sluiten
inFile.Close();       
```
## Conclusie

Gefeliciteerd! U weet nu hoe u een afbeelding in de kop- of voettekst van een Excel-document kunt invoegen met Aspose.Cells voor .NET. In deze zelfstudie wordt u door elke stap van het proces geleid, van het instellen van de omgeving tot het opslaan van de gewijzigde werkmap. Voel je vrij om meer te experimenteren met de functies van Aspose.Cells om gepersonaliseerde en professionele Excel-documenten te maken.

### Veelgestelde vragen

#### Vraag 1: Is het mogelijk om meerdere afbeeldingen in de kop- of voettekst van een Excel-document in te voegen?

A1: Ja, u kunt meerdere afbeeldingen in de kop- of voettekst van een Excel-document invoegen door stap 8 en 9 voor elke extra afbeelding te herhalen.

#### Vraag 2: Welke afbeeldingsformaten worden ondersteund voor invoeging in kop- of voettekst?
A2: Aspose.Cells ondersteunt een verscheidenheid aan veelgebruikte afbeeldingsformaten zoals JPEG, PNG, GIF, BMP, enz.

#### V3: Kan ik het uiterlijk van de kop- of voettekst verder aanpassen?

A3: Ja, u kunt speciale scripts en codes gebruiken om het uiterlijk van de kop- of voettekst verder op te maken en aan te passen. Raadpleeg de Aspose.Cells-documentatie voor meer informatie over aanpassingsopties.

#### V4: Werkt Aspose.Cells met verschillende versies van Excel?

A4: Ja, Aspose.Cells is compatibel met verschillende versies van Excel, waaronder Excel 2003, Excel 2007, Excel 2010, Excel 2013, Excel 2016 en Excel 2019.

#### Vraag 5: Is het mogelijk om afbeeldingen in andere delen van het Excel-document in te voegen, zoals cellen of grafieken?

A5: Ja, Aspose.Cells biedt uitgebreide functionaliteit voor het invoegen van afbeeldingen in verschillende delen van het Excel-document, inclusief cellen, grafieken en tekenobjecten.