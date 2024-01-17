---
title: Excel munkalap másolása
linktitle: Excel munkalap másolása
second_title: Aspose.Cells for .NET API Reference
description: Másoljon át egy Excel-munkalapot a másikra az Aspose.Cells for .NET segítségével.
type: docs
weight: 20
url: /hu/net/excel-copy-worksheet/excel-copy-worksheet/
---

Ebben az útmutatóban elmagyarázzuk, hogyan lehet Excel-munkalapot másolni az Aspose.Cells könyvtár segítségével a .NET-hez. C# forráskódot biztosítunk, és végigvezetjük a feladat elvégzéséhez szükséges lépéseken. A végén megmutatjuk a várt eredményt. A kezdéshez kövesse az alábbi utasításokat.

## 1. lépés: Előkészítés

Mielőtt elkezdené, győződjön meg arról, hogy telepítette az Aspose.Cells for .NET programot, és létrehozott egy C#-projektet a kívánt integrált fejlesztői környezetben (IDE). Győződjön meg arról is, hogy rendelkezik a módosítani kívánt Excel-fájl másolatával.

## 2. lépés: Importálja a szükséges könyvtárakat

 A C# forrásfájlban importálja a szükséges könyvtárakat az Aspose.Cells fájlból a következővel`using` irányelv:

```csharp
using Aspose.Cells;
```

## 3. lépés: Állítsa be a fájl elérési útját

 Nyilatkozni a`dataDir` változót, és inicializálja az Excel fájlt tartalmazó könyvtárral. Például :

```csharp
string dataDir = "PATH_TO_YOUR_DOCUMENT_DIRECTORY";
```

 Feltétlenül cserélje ki`"PATH_TO_YOUR_DOCUMENT_DIRECTORY"` a címtár tényleges elérési útjával.

## 4. lépés: Töltse be a meglévő Excel fájlt

 Használja a`Workbook` osztályt az Aspose.Cells-ből a meglévő Excel-fájl megnyitásához. Használja a`InputPath` változó a fájl elérési útjának megadásához:

```csharp
string InputPath = dataDir + "book1.xls";
Workbook wb = new Workbook(InputPath);
```

 Győződjön meg arról, hogy kicserélte`"book1.xls"` az Excel-fájl tényleges nevével.

## 5. lépés: Másolja ki a munkalapot

 Most átmásoljuk a meglévő munkalapot egy új munkalapra. Használja a`Worksheets` tulajdona a`Workbook` objektum a munkalapgyűjtemény eléréséhez:

```csharp
WorksheetCollection sheets = wb.Worksheets;
```

 Ezután használja a`AddCopy` módszert a megadott munkalap másolásához. Például az „1. lap” másolásához:

```csharp
sheets.AddCopy("Sheet1");
```

## 6. lépés: Mentse el az Excel fájlt

 Használja a`Save` módszere a`Workbook` objektum a változtatások új fájlba mentéséhez:

```csharp
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

Feltétlenül adja meg a kimeneti fájl kívánt elérési útját és fájlnevét.

### Minta forráskód az Excel másolási munkalaphoz az Aspose.Cells for .NET használatával 

```csharp
// dokumentumok könyvtárának elérési útja.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Nyisson meg egy meglévő Excel-fájlt.
Workbook wb = new Workbook(InputPath);
// Hozzon létre egy Munkalapok objektumot a hivatkozással
// a munkafüzet lapjait.
WorksheetCollection sheets = wb.Worksheets;
// Adatok másolása egy új lapra egy meglévőről
// lapot a munkafüzetben.
sheets.AddCopy("Sheet1");
// Mentse el az Excel fájlt.
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

## Következtetés

Gratulálok ! Most megtanulta, hogyan másoljon Excel-munkalapot az Aspose.Cells for .NET használatával. Ez a lépésenkénti útmutató bemutatja, hogyan importálhatja a szükséges könyvtárakat, hogyan tölthet be egy meglévő Excel-fájlt, másolja a munkalapot és mentse a módosított fájlt. Nyugodtan használhatja ezt a módszert saját projektjeiben az Excel-fájlok hatékony kezeléséhez.

### GYIK

#### K. Az Aspose.Cells kompatibilis más programozási nyelvekkel?

A. Igen, az Aspose.Cells több programozási nyelvet támogat, beleértve a C#, Java, Python és még sok más nyelvet.

#### K. Másolhatok egy munkalapot egy másik Excel-munkafüzetbe?

A.  Igen, használhatod a`AddCopy` módszerrel másolhat egy munkalapot egy másik Excel-munkafüzetbe.

#### K. Az Aspose.Cells megőrzi a képleteket és a formázást a munkalap másolásakor?

A. Igen, az Aspose.Cells megőrzi a képleteket, a formázást és egyéb tulajdonságokat a munkalap másolásakor.

#### K. Az Aspose.Cells engedélyt igényel kereskedelmi használatra?

A. Igen, az Aspose.Cells kereskedelmi termék, és kereskedelmi használatra licenc megvásárlása szükséges. További licencinformációkat találhat az Aspose hivatalos honlapján.