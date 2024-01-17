---
title: Xades aláírás támogatás
linktitle: Xades aláírás támogatás
second_title: Aspose.Cells for .NET API Reference
description: Ismerje meg, hogyan adhat hozzá Xades-aláírást egy Excel-fájlhoz az Aspose.Cells for .NET használatával.
type: docs
weight: 190
url: /hu/net/excel-workbook/xades-signature-support/
---
Ebben a cikkben lépésről lépésre elmagyarázzuk az alábbi C# forráskódot, amely a Xades aláírások támogatásáról szól az Aspose.Cells könyvtár .NET-hez használatával. Megtudhatja, hogyan használhatja ezt a könyvtárat Xades digitális aláírás hozzáadására egy Excel fájlhoz. Áttekintést adunk az aláírási folyamatról és annak végrehajtásáról is. Kövesse az alábbi lépéseket a meggyőző eredmények eléréséhez.

## 1. lépés: Határozza meg a forrás- és kimeneti könyvtárakat
Kezdésként meg kell határoznunk a forrás- és kimeneti könyvtárakat a kódunkban. Ezek a könyvtárak jelzik, hol találhatók a forrásfájlok, és hová kerül a kimeneti fájl mentése. Itt van a megfelelő kód:

```csharp
// Forrás könyvtár
string sourceDir = RunExamples.Get_SourceDirectory();
// Kimeneti könyvtár
string outputDir = RunExamples.Get_OutputDirectory();
```

Ügyeljen arra, hogy szükség szerint módosítsa a könyvtár elérési útjait.

## 2. lépés: Az Excel-munkafüzet betöltése
A következő lépés az Excel munkafüzet betöltése, amelyre a Xades digitális aláírást szeretnénk hozzáadni. Íme a kód a munkafüzet betöltéséhez:

```csharp
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
```

Ügyeljen arra, hogy helyesen adja meg a forrásfájl nevét a kódban.

## 3. lépés: A digitális aláírás konfigurálása
Most konfiguráljuk a Xades digitális aláírást a szükséges információk megadásával. Meg kell adnunk a digitális tanúsítványt tartalmazó PFX fájlt, valamint a hozzá tartozó jelszót. Itt van a megfelelő kód:

```csharp
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
```

Ügyeljen arra, hogy a „pfxPassword” szót a tényleges jelszavával cserélje ki, a „pfxFile” szót pedig a PFX fájl elérési útjával.

## 4. lépés: A digitális aláírás hozzáadása
Most, hogy beállítottuk a digitális aláírást, hozzáadhatjuk az Excel munkafüzethez. Itt van a megfelelő kód:

```csharp
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
```

Ez a lépés hozzáadja a Xades digitális aláírást az Excel-munkafüzethez.

## 5. lépés: Mentse el a munkafüzetet az aláírással
Végül mentjük az Excel munkafüzetet a digitális aláírással. Itt van a megfelelő kód:

```csharp
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
```

Ügyeljen arra, hogy a kimeneti fájl nevét igényeinek megfelelően alakítsa át.

### Minta forráskód a Xades Signature Support támogatásához az Aspose.Cells for .NET használatával 
```csharp
//Forrás könyvtár
string sourceDir = RunExamples.Get_SourceDirectory();
//Kimeneti könyvtár
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

## Következtetés
Gratulálok ! Megtanulta, hogyan használhatja az Aspose.Cells könyvtárat .NET-hez Xades digitális aláírás hozzáadására Excel-fájlhoz. Az ebben a cikkben ismertetett lépések követésével megvalósíthatja ezt a funkciót saját projektjeiben. Nyugodtan kísérletezzen még többet a könyvtárral, és fedezze fel az általa kínált egyéb hatékony funkciókat.

### GYIK

#### K: Mi az a Xades?

V: A Xades egy fejlett elektronikus aláírási szabvány, amelyet a digitális dokumentumok integritásának és hitelességének biztosítására használnak.

#### K: Használhatok más típusú digitális aláírásokat az Aspose.Cells-szel?

V: Igen, az Aspose.Cells más típusú digitális aláírásokat is támogat, például az XMLDSig aláírásokat és a PKCS#7 aláírásokat.

#### K: Alkalmazhatok aláírást az Excel-fájlokon kívül más fájltípusokra is?
 
V: Igen, az Aspose.Cells lehetővé teszi a digitális aláírások alkalmazását más támogatott fájltípusokhoz is, például Word-, PDF- és PowerPoint-fájlokhoz.