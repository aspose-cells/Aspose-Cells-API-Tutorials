---
title: Excel munkalap másolása más munkafüzetből
linktitle: Excel munkalap másolása más munkafüzetből
second_title: Aspose.Cells for .NET API Reference
description: Az Aspose.Cells for .NET segítségével egyszerűen másolhat Excel-munkalapot egyik munkafüzetből a másikba.
type: docs
weight: 10
url: /hu/net/excel-copy-worksheet/excel-copy-worksheet-from-other-workbook/
---
Ebben az oktatóanyagban végigvezetjük az Excel-munkalap egy másik munkafüzetből való másolásának lépésein az Aspose.Cells könyvtár .NET-hez segítségével. A feladat végrehajtásához kövesse az alábbi utasításokat.

## 1. lépés: Előkészítés

Mielőtt elkezdené, győződjön meg arról, hogy telepítette az Aspose.Cells for .NET programot, és létrehozott egy C#-projektet a kívánt integrált fejlesztői környezetben (IDE).

## 2. lépés: Állítsa be a dokumentumkönyvtár elérési útját

 Nyilatkozni a`dataDir` változót, és inicializálja a dokumentumkönyvtár elérési útjával. Például :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Feltétlenül cserélje ki`"YOUR_DOCUMENTS_DIRECTORY"` a címtár tényleges elérési útjával.

## 3. lépés: Hozzon létre egy új Excel-munkafüzetet

 Használja a`Workbook` osztály az Aspose.Cells-ből egy új Excel-munkafüzet létrehozásához:

```csharp
Workbook excelWorkbook0 = new Workbook();
```

## 4. lépés: Szerezze be az első munkalapot a munkafüzetben

Lépjen a munkafüzet első munkalapjára a 0 index használatával:

```csharp
Worksheet ws0 = excelWorkbook0.Worksheets[0];
```

## 5. lépés: Adjon hozzá adatokat a fejlécsorokhoz (A1:A4)

 Használj`for` hurok adatok hozzáadásához a fejlécsorokhoz (A1:A4):

```csharp
for (int i = 0; i < 5; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Header row {0}", i));
}
```

## 6. lépés: Részletes adatok hozzáadása (A5:A999)

 Használj másikat`for` hurok részletes adatok hozzáadásához (A5:A999):

```csharp
for (int i = 5; i < 1000; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Detail row {0}", i));
}
```

## 7. lépés: Állítsa be az elrendezési beállításokat

 Állítsa be a munkalap oldalbeállítási beállításait a`PageSetup` tárgy:

```csharp
PageSetup pagesetup = ws0.PageSetup;
pagesetup.PrintTitleRows = "$1:$5";
```

## 8. lépés: Hozzon létre egy másik Excel-munkafüzetet

Hozzon létre egy másik Excel-munkafüzetet:

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## 9. lépés: Szerezze be az első munkalapot a második munkafüzetből

Lépjen a második munkafüzet első munkalapjára:

```csharp
Worksheet ws1 = excelWorkbook1.Worksheets[0];
```

## 10. lépés: Nevezze el a munkalapot

nevezd el a tüzet

számítási sziget:

```csharp
ws1.Name = "MySheet";
```

## 11. lépés: Másolja át az adatokat az első munkafüzet első munkalapjáról a második munkafüzet első munkalapjára

Másolja át az adatokat az első munkafüzet első munkalapjáról a második munkafüzet első munkalapjára:

```csharp
ws1.Copy(ws0);
```

## 12. lépés: Mentse el az Excel fájlt

Mentse el az Excel fájlt:

```csharp
excelWorkbook1.Save(dataDir + "CopyWorkbookSheetToOther_out.xls");
```

Feltétlenül adja meg a kimeneti fájl kívánt elérési útját és fájlnevét.

### Minta forráskód az Excel munkalap másolása más munkafüzetből az Aspose.Cells for .NET használatával 
```csharp
// dokumentumok könyvtárának elérési útja.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Hozzon létre egy új munkafüzetet.
Workbook excelWorkbook0 = new Workbook();
// Szerezd meg a könyv első feladatlapját.
Worksheet ws0 = excelWorkbook0.Worksheets[0];
// Helyezzen el néhány adatot a fejlécsorokba (A1:A4)
for (int i = 0; i < 5; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Header Row {0}", i));
}
// Adjon meg néhány részletes adatot (A5:A999)
for (int i = 5; i < 1000; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Detail Row {0}", i));
}
// Határozzon meg egy oldalbeállítási objektumot az első munkalap alapján.
PageSetup pagesetup = ws0.PageSetup;
// Az első öt sor ismétlődik minden oldalon...
// Nyomtatási képen látható.
pagesetup.PrintTitleRows = "$1:$5";
// Hozzon létre egy másik munkafüzetet.
Workbook excelWorkbook1 = new Workbook();
// Szerezd meg a könyv első feladatlapját.
Worksheet ws1 = excelWorkbook1.Worksheets[0];
// Nevezze el a munkalapot.
ws1.Name = "MySheet";
// Másolja az adatokat az első munkafüzet első munkalapjáról a
// a második munkafüzet első munkalapja.
ws1.Copy(ws0);
// Mentse el az excel fájlt.
excelWorkbook1.Save(dataDir + "CopyWorksheetFromWorkbookToOther_out.xls");
```

## Következtetés

Gratulálok ! Most megtanulta, hogyan másoljon Excel-munkalapot egy másik munkafüzetből az Aspose.Cells for .NET segítségével. Nyugodtan használhatja ezt a módszert saját projektjeiben az Excel-fájlok hatékony kezeléséhez.

### GYIK

#### K. Milyen könyvtárakra van szükség az Aspose.Cells for .NET használatához?

A. Az Aspose.Cells for .NET használatához tartalmaznia kell az Aspose.Cells könyvtárat a projektben. Győződjön meg arról, hogy megfelelően hivatkozott erre a könyvtárra az integrált fejlesztői környezetben (IDE).

#### K. Az Aspose.Cells támogat más Excel fájlformátumokat, például az XLSX-et?

A. Igen, az Aspose.Cells különféle Excel fájlformátumokat támogat, beleértve az XLSX, XLS, CSV, HTML és még sok más formátumot. Ezeket a fájlformátumokat az Aspose.Cells for .NET szolgáltatásaival kezelheti.

#### K. Testreszabhatom az elrendezési beállításokat a munkalap másolásakor?

A.  Igen, testreszabhatja az oldalbeállítási beállításokat a munkalap másolásakor a tulajdonságok használatával`PageSetup` tárgy. Megadhat oldalfejlécet, láblécet, margót, tájolást stb.