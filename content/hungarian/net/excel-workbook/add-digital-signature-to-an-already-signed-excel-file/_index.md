---
title: Digitális aláírás hozzáadása egy már aláírt Excel-fájlhoz
linktitle: Digitális aláírás hozzáadása egy már aláírt Excel-fájlhoz
second_title: Aspose.Cells for .NET API Reference
description: Könnyen hozzáadhat digitális aláírásokat a meglévő Excel-fájlokhoz az Aspose.Cells for .NET segítségével.
type: docs
weight: 30
url: /hu/net/excel-workbook/add-digital-signature-to-an-already-signed-excel-file/
---
Ebben a lépésenkénti útmutatóban elmagyarázzuk azt a C# forráskódot, amely lehetővé teszi digitális aláírás hozzáadását egy már aláírt Excel-fájlhoz az Aspose.Cells for .NET segítségével. Kövesse az alábbi lépéseket új digitális aláírás hozzáadásához egy meglévő Excel-fájlhoz.

## 1. lépés: Állítsa be a forrás- és kimeneti könyvtárakat

```csharp
// forráskönyvtár
string sourceDir = RunExamples.Get_SourceDirectory();

// Kimeneti könyvtár
string outputDir = RunExamples.Get_OutputDirectory();
```

Ebben az első lépésben meghatározzuk azokat a forrás- és kimeneti könyvtárakat, amelyek a meglévő Excel-fájl betöltéséhez és a fájl új digitális aláírással történő mentéséhez lesznek használva.

## 2. lépés: Töltse be a meglévő Excel fájlt

```csharp
// Töltse be a már aláírt Excel-munkafüzetet
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
```

 Itt betöltjük a már aláírt Excel fájlt a`Workbook` osztályú Aspose.Cells.

## 3. lépés: A digitális aláírások gyűjteményének létrehozása

```csharp
// Digitális aláírásgyűjtemény létrehozása
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
```

 A digitális aláírások új gyűjteményét hozzuk létre a`DigitalSignatureCollection` osztály.

## 4. lépés: Hozzon létre egy új tanúsítványt

```csharp
// Hozzon létre egy új tanúsítványt
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
```

Itt létrehozunk egy új tanúsítványt a megadott fájlból és jelszóból.

## 5. lépés: Adjon hozzá egy új digitális aláírást a gyűjteményhez

```csharp
// Hozzon létre egy új digitális aláírást
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added a new digital signature to the already signed workbook.", DateTime.Now);

// Adja hozzá a digitális aláírást a gyűjteményhez
dsCollection.Add(signature);
```

 Új digitális aláírást hozunk létre a`DigitalSignature` osztályba, és adja hozzá a digitális aláírások gyűjteményéhez.

## 6. lépés: Adja hozzá a digitális aláírások gyűjteményét a munkafüzethez

```csharp
//Adja hozzá a digitális aláírások gyűjteményét a munkafüzethez
workbook.AddDigitalSignature(dsCollection);
```

 A digitális aláírások gyűjteményét hozzáadjuk a meglévő Excel munkafüzethez a`AddDigitalSignature()` módszer.

## 7. lépés: Mentse el és zárja be a munkafüzetet

```csharp
// Mentse el a munkafüzetet és zárja be
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
```

Az új digitális aláírással ellátott munkafüzetet elmentjük a megadott kimeneti könyvtárba, majd bezárjuk és felszabadítjuk a kapcsolódó erőforrásokat.

### Minta forráskód a digitális aláírás hozzáadása egy már aláírt Excel-fájlhoz az Aspose.Cells for .NET használatával 
```csharp
//Forrás könyvtár
string sourceDir = RunExamples.Get_SourceDirectory();
//Kimeneti könyvtár
string outputDir = RunExamples.Get_OutputDirectory();
//Tanúsítványfájl és jelszava
string certFileName = sourceDir + "AsposeDemo.pfx";
string password = "aspose";
//Új digitális aláírás hozzáadásához töltse be a már digitálisan aláírt munkafüzetet
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
//Hozza létre a digitális aláírásgyűjteményt
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
//Hozzon létre új tanúsítványt
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
//Hozzon létre új digitális aláírást, és adja hozzá a digitális aláírásgyűjteményhez
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added new digital signature in existing digitally signed workbook.", DateTime.Now);
dsCollection.Add(signature);
//Digitális aláírásgyűjtemény hozzáadása a munkafüzetbe
workbook.AddDigitalSignature(dsCollection);
//Mentse el a munkafüzetet és dobja ki.
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
Console.WriteLine("AddDigitalSignatureToAnAlreadySignedExcelFile executed successfully.\r\n");
```

## Következtetés

Gratulálok ! Most megtanulta, hogyan adhat hozzá digitális aláírást egy már aláírt Excel-fájlhoz az Aspose.Cells for .NET segítségével. A digitális aláírások további biztonsági réteget adnak az Excel-fájlokhoz, biztosítva azok hitelességét és integritását.

### GYIK

#### K: Mi az Aspose.Cells for .NET?

V: Az Aspose.Cells for .NET egy hatékony osztálykönyvtár, amely lehetővé teszi a .NET-fejlesztők számára, hogy könnyedén hozzanak létre, módosítsanak, konvertáljanak és kezeljenek Excel fájlokat.

#### K: Mi az a digitális aláírás egy Excel-fájlban?

V: Az Excel fájlban lévő digitális aláírás egy elektronikus védjegy, amely garantálja a dokumentum hitelességét, sértetlenségét és eredetét. Annak ellenőrzésére szolgál, hogy a fájlt nem módosították-e az aláírása óta, és megbízható forrásból származik-e.

#### K: Milyen előnyökkel jár, ha digitális aláírást ad egy Excel-fájlhoz?

V: Digitális aláírás hozzáadása egy Excel-fájlhoz számos előnnyel jár, beleértve a jogosulatlan módosítások elleni védelmet, az adatok integritásának biztosítását, a dokumentum szerzőjének hitelesítését, valamint a benne található információk iránti bizalmat.

#### K: Hozzáadhatok több digitális aláírást egy Excel-fájlhoz?

V: Igen, az Aspose.Cells lehetővé teszi több digitális aláírás hozzáadását egy Excel-fájlhoz. Létrehozhat digitális aláírásgyűjteményt, és egy művelettel hozzáadhatja őket a fájlhoz.

#### K: Milyen követelmények vonatkoznak a digitális aláírás Excel-fájlhoz való hozzáadására?

V: Ha digitális aláírást szeretne hozzáadni egy Excel-fájlhoz, érvényes digitális tanúsítványra van szüksége, amelyet a dokumentum aláírására használunk. A digitális aláírás hozzáadása előtt győződjön meg arról, hogy rendelkezik a megfelelő tanúsítvánnyal és jelszóval.