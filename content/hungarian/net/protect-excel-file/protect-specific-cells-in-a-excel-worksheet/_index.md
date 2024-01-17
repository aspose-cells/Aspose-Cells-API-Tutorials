---
title: Adott cellák védelme egy Excel-munkalapon
linktitle: Adott cellák védelme egy Excel-munkalapon
second_title: Aspose.Cells for .NET API Reference
description: Ismerje meg, hogyan védhet meg bizonyos cellákat az Excelben az Aspose.Cells for .NET segítségével. Lépésről lépésre bemutató C# nyelven.
type: docs
weight: 70
url: /hu/net/protect-excel-file/protect-specific-cells-in-a-excel-worksheet/
---
Ebben az oktatóanyagban a C# forráskódot tekintjük meg, amely az Aspose.Cells könyvtárat használja az Excel-táblázat egyes celláinak védelmére. Végigjárjuk a kód minden lépését, és elmagyarázzuk, hogyan működik. Gondosan kövesse az utasításokat a kívánt eredmény eléréséhez.

## 1. lépés: Előfeltételek

Mielőtt elkezdené, győződjön meg arról, hogy telepítette a .NET Aspose.Cells könyvtárát. Az Aspose hivatalos webhelyéről szerezheti be. Győződjön meg arról is, hogy a Visual Studio vagy bármely más C# fejlesztői környezet legújabb verziójával rendelkezik.

## 2. lépés: Importálja a szükséges névtereket

Az Aspose.Cells könyvtár használatához importálnunk kell a szükséges névtereket a kódunkba. Adja hozzá a következő sorokat a C# forrásfájl tetejéhez:

```csharp
using Aspose.Cells;
```

## 3. lépés: Excel-munkafüzet létrehozása

Ebben a lépésben létrehozunk egy új Excel-munkafüzetet. Használja a következő kódot Excel-munkafüzet létrehozásához:

```csharp
// A dokumentumok könyvtár elérési útja.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Hozzon létre egy új munkafüzetet.
Workbook wb = new Workbook();
```

 Feltétlenül cserélje ki`"YOUR_DOCUMENTS_DIR"` a dokumentumkönyvtár megfelelő elérési útjával.

## 4. lépés: Táblázat létrehozása

Most, hogy elkészítettük az Excel munkafüzetet, hozzunk létre egy munkalapot, és szerezzük be az első lapot. Használja a következő kódot:

```csharp
// Hozzon létre egy táblázatkezelő objektumot, és szerezze be az első lapot.
Worksheet sheet = wb.Worksheets[0];
```

## 5. lépés: A stílus meghatározása

Ebben a lépésben meghatározzuk az adott cellákra alkalmazandó stílust. Használja a következő kódot:

```csharp
// A stílusobjektum meghatározása.
Styling styling;
```

## 6. lépés: Hurok az összes oszlop feloldásához

Most végigpörgetjük a munkalap összes oszlopát, és feloldjuk őket. Használja a következő kódot:

```csharp
// Lapozzon át a munkalap összes oszlopán, és oldja fel őket.
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style);
}
```

## 7. lépés: Adott cellák zárolása

Ebben a lépésben bizonyos cellákat zárolunk. Használja a következő kódot:

```csharp
//Mindhárom cella lezárása... azaz A1, B1, C1.
style = sheet.Cells["A1"].GetStyle();
style. IsLocked = true;
sheet.Cells["A1"].SetStyle(style);

style = sheet.Cells["B1"].GetStyle();
style. IsLocked = true;
sheet.Cells["B1"].SetStyle(style);

style = sheet.Cells["C1"].GetStyle();
style. IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
```

## 8. lépés: A munkalap védelme

Végül megvédjük a munkalapot, hogy megakadályozzuk bizonyos cellák módosítását. Használja a következő kódot:

```csharp
// Védje meg a munkalapot.
sheet.Protect(ProtectionType.All);
```

## 9. lépés: Az Excel fájl mentése

Most mentjük a módosított Excel fájlt. Használja a következő kódot:

```csharp
// Mentse el az Excel fájlt.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Ügyeljen arra, hogy a módosított Excel-fájl mentéséhez a megfelelő útvonalat adja meg.

### Forráskód minta speciális cellák védelméhez egy Excel-munkalapon az Aspose.Cells for .NET használatával 
```csharp
// dokumentumok könyvtárának elérési útja.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Hozzon létre könyvtárat, ha még nincs jelen.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Hozzon létre egy új munkafüzetet.
Workbook wb = new Workbook();
// Hozzon létre egy munkalap objektumot, és szerezze be az első lapot.
Worksheet sheet = wb.Worksheets[0];
// Határozza meg a stílusobjektumot.
Style style;
// Határozza meg a styleflag objektumot
StyleFlag styleflag;
// Lapozzon át a munkalap összes oszlopán, és oldja fel őket.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    styleflag = new StyleFlag();
    styleflag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, styleflag);
}
// Zárja be a három cellát...azaz A1, B1, C1.
style = sheet.Cells["A1"].GetStyle();
style.IsLocked = true;
sheet.Cells["A1"].SetStyle(style);
style = sheet.Cells["B1"].GetStyle();
style.IsLocked = true;
sheet.Cells["B1"].SetStyle(style);
style = sheet.Cells["C1"].GetStyle();
style.IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
// Végül most védje meg a lapot.
sheet.Protect(ProtectionType.All);
// Mentse el az excel fájlt.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```


## Következtetés

Gratulálok ! Most már rendelkezik C#-forráskóddal, amely lehetővé teszi az Excel-munkalap egyes celláinak védelmét a .NET Aspose.Cells könyvtárával. Nyugodtan testreszabhatja a kódot az Ön egyedi igényei szerint.

### GYIK (Gyakran Ismételt Kérdések)

#### Működik ez a kód az Excel legújabb verzióival?

Igen, ez a kód működik az Excel legújabb verzióival, beleértve az Excel 2010 és újabb formátumú fájlokat is.

#### Megvédhetek más sejteket az A1, B1 és C1 mellett?

Igen, módosíthatja a kódot más meghatározott cellák zárolásához, ha módosítja a megfelelő kódsorokban található cellahivatkozásokat.

#### Hogyan tudom újra feloldani a zárolt cellákat?

 Te tudod használni`SetStyle` módszerrel`IsLocked` állítva`false` cellák feloldásához.

#### Hozzáadhatok több munkalapot a munkafüzethez?

 Igen, a munkafüzethez hozzáadhat további munkalapokat a`Worksheets.Add()`módszert, és ismételje meg a cellavédelmi lépéseket minden munkalapon.

#### Hogyan tudom megváltoztatni az Excel fájl mentési formátumát?

 A mentési formátumot a gombbal módosíthatja`SaveFormat` módszert például a kívánt formátummal`SaveFormat.Xlsx` Excel 2007 és újabb verziókhoz.