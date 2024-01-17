---
title: A beágyazott Mol fájl kibontása
linktitle: A beágyazott Mol fájl kibontása
second_title: Aspose.Cells for .NET API Reference
description: Ismerje meg, hogyan bonthat ki egyszerűen beágyazott MOL-fájlokat egy Excel-munkafüzetből az Aspose.Cells for .NET segítségével.
type: docs
weight: 90
url: /hu/net/excel-workbook/extract-embedded-mol-file/
---
Ebben az oktatóanyagban lépésről lépésre végigvezetjük, hogyan bonthat ki beágyazott MOL-fájlt egy Excel-munkafüzetből az Aspose.Cells könyvtár .NET-hez használatával. Megtanulja, hogyan böngészhet a munkafüzet lapjai között, hogyan bonthatja ki a megfelelő OLE objektumokat és mentheti a kibontott MOL fájlokat. A feladat sikeres végrehajtásához kövesse az alábbi lépéseket.

## 1. lépés: Határozza meg a forrás- és kimeneti könyvtárakat
Először is meg kell határoznunk a forrás- és kimeneti könyvtárakat a kódunkban. Ezek a könyvtárak jelzik, hogy hol található a forrás Excel-munkafüzet, és hová lesznek mentve a kibontott MOL-fájlok. Itt van a megfelelő kód:

```csharp
// Könyvtárak
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
```

Szükség esetén feltétlenül adja meg a megfelelő útvonalakat.

## 2. lépés: Az Excel-munkafüzet betöltése
A következő lépés a beágyazott OLE objektumokat és MOL fájlokat tartalmazó Excel munkafüzet betöltése. Íme a kód a munkafüzet betöltéséhez:

```csharp
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
```

Ügyeljen arra, hogy helyesen adja meg a forrásfájl nevét a kódban.

## 3. lépés: Haladjon át a lapokon, és bontsa ki a MOL fájlokat
Most végigfutjuk a munkafüzet minden egyes lapját, és kibontjuk a megfelelő OLE objektumokat, amelyek a MOL fájlokat tartalmazzák. Itt van a megfelelő kód:

```csharp
var index = 1;
foreach(Worksheet sheet in workbook.Worksheets)
{
     OleObjectCollection oles = sheet.OleObjects;
     foreach(OleObject ole in oles)
     {
         string fileName = outputDir + "OleObject" + index + ".mol";
         FileStream fs = File.Create(fileName);
         fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
         fs. Close();
         index++;
     }
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

Ez a kód végigfut a munkafüzet minden egyes lapján, lekéri az OLE objektumokat, és elmenti a kibontott MOL fájlokat a kimeneti könyvtárba.

### Minta forráskód az Embedded Mol fájl kibontásához az Aspose.Cells for .NET használatával 
```csharp
//könyvtárakat
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
var index = 1;
foreach (Worksheet sheet in workbook.Worksheets)
{
	OleObjectCollection oles = sheet.OleObjects;
	foreach (OleObject ole in oles)
	{
		string fileName = outputDir + "OleObject" + index + ".mol ";
		FileStream fs = File.Create(fileName);
		fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
		fs.Close();
		index++;
	}
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

## Következtetés
Gratulálok ! Megtanulta, hogyan lehet kicsomagolni egy beágyazott MOL-fájlt egy Excel-munkafüzetből az Aspose.Cells for .NET segítségével. Ezt a tudást most már használhatja MOL-fájlok kibontására saját Excel-munkafüzeteiből. Nyugodtan fedezze fel az Aspose.Cells könyvtárat, és ismerje meg további hatékony funkcióit.

### GYIK

#### K: Mi az a MOL fájl?
 
V: A MOL fájl egy fájlformátum, amelyet a kémiai szerkezetek ábrázolására használnak a számítási kémiában. Információkat tartalmaz az atomokról, kötésekről és egyéb molekuláris tulajdonságokról.

#### K: Működik ez a módszer minden Excel fájltípussal?

V: Igen, ez a módszer az Aspose.Cells által támogatott összes Excel-fájltípussal működik.

#### K: Kibonthatok több MOL fájlt egyszerre?

V: Igen, egyszerre több MOL-fájlt is kibonthat úgy, hogy a munkafüzet minden egyes lapján áthalad az OLE-objektumokon.