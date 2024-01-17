---
title: Excel munkalapok másolása munkafüzetek között
linktitle: Excel munkalapok másolása munkafüzetek között
second_title: Aspose.Cells for .NET API Reference
description: Könnyen másolhat munkalapokat Excel-munkafüzetek között az Aspose.Cells for .NET segítségével.
type: docs
weight: 30
url: /hu/net/excel-copy-worksheet/excel-copy-worksheets-between-workbooks/
---
Ebben az oktatóanyagban végigvezetjük a munkalapok Excel-munkafüzetek közötti másolásának lépésein a .NET Aspose.Cells könyvtárával. A feladat végrehajtásához kövesse az alábbi utasításokat.

## 1. lépés: Előkészítés

Győződjön meg arról, hogy telepítette az Aspose.Cells for .NET fájlt, és létrehozott egy C#-projektet az előnyben részesített integrált fejlesztői környezetben (IDE).

## 2. lépés: Állítsa be a dokumentumkönyvtár elérési útját

 Nyilatkozni a`dataDir` változót, és inicializálja a dokumentumkönyvtár elérési útjával. Például :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Feltétlenül cserélje ki`"YOUR_DOCUMENTS_DIRECTORY"` a címtár tényleges elérési útjával.

## 3. lépés: Határozza meg a bemeneti fájl elérési útját

 Nyilatkozz egy`InputPath` változót, és inicializálja annak az Excel-fájlnak a teljes elérési útjával, amelyből a táblázatot másolni szeretné. Például :

```csharp
string InputPath = dataDir + "book1.xls";
```

 Győződjön meg arról, hogy rendelkezik az Excel fájllal`book1.xls` a dokumentumok könyvtárában, vagy adja meg a megfelelő fájlnevet és helyet.

## 4. lépés: Hozzon létre egy első Excel-munkafüzetet

 Használja a`Workbook` osztályú Aspose.Cells az első Excel-munkafüzet létrehozásához és a megadott fájl megnyitásához:

```csharp
Workbook excelWorkbook0 = new Workbook(InputPath);
```

## 5. lépés: Hozzon létre egy második Excel-munkafüzetet

Hozzon létre egy második Excel-munkafüzetet:

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## 6. lépés: Másolja át a munkalapot az első munkafüzetből a második munkafüzetbe

 Használja a`Copy`módszer az első munkalap másolására az első munkafüzetből a második munkafüzetbe:

```csharp
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
```

## 7. lépés: Mentse el az Excel fájlt

Mentse el a másolt táblázatot tartalmazó Excel-fájlt:

```csharp
excelWorkbook1.Save(dataDir + "Copy WorksheetsBetweenWorkbooks_out.xls");
```

Feltétlenül adja meg a kimeneti fájl kívánt elérési útját és fájlnevét.

### Minta forráskód az Excel munkalapok munkafüzetek között másolásához az Aspose.Cells for .NET használatával 
```csharp
// dokumentumok könyvtárának elérési útja.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Hozzon létre egy munkafüzetet.
// Nyisson meg egy fájlt az első könyvben.
Workbook excelWorkbook0 = new Workbook(InputPath);
// Hozzon létre egy másik munkafüzetet.
Workbook excelWorkbook1 = new Workbook();
// Másolja át az első könyv első lapját a második könyvbe.
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
// Mentse el a fájlt.
excelWorkbook1.Save(dataDir + "CopyWorksheetsBetweenWorkbooks_out.xls");
```

## Következtetés

Gratulálok ! Most megtanulta, hogyan másolhat munkalapokat Excel-munkafüzetek között az Aspose.Cells for .NET használatával. Nyugodtan használhatja ezt a módszert saját projektjeiben az Excel-fájlok hatékony kezeléséhez.

### GYIK

#### K. Milyen könyvtárakra van szükség az Aspose.Cells for .NET használatához?

A. Az Aspose.Cells for .NET használatához tartalmaznia kell az Aspose.Cells könyvtárat a projektben. Győződjön meg arról, hogy megfelelően hivatkozott erre a könyvtárra az integrált fejlesztői környezetben (IDE).

#### K. Az Aspose.Cells támogat más Excel fájlformátumokat, például az XLSX-et?

A. Igen, az Aspose.Cells különféle Excel fájlformátumokat támogat, beleértve az XLSX, XLS, CSV, HTML és még sok más formátumot. Ezeket a fájlformátumokat az Aspose.Cells for .NET szolgáltatásaival kezelheti.

#### K. Testreszabhatom az elrendezési beállításokat a táblázat másolásakor?

A.  Igen, testreszabhatja az oldalbeállítási beállításokat a táblázat másolásakor a tulajdonságok használatával`PageSetup` tárgy. Megadhat oldalfejlécet, láblécet, margót, tájolást stb.