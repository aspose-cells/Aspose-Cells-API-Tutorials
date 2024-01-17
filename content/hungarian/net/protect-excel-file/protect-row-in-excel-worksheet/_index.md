---
title: Sor védelme az Excel munkalapon
linktitle: Sor védelme az Excel munkalapon
second_title: Aspose.Cells for .NET API Reference
description: Ebből az oktatóanyagból megtudhatja, hogyan védheti meg az Excel-táblázatok sorait az Aspose.Cells for .NET használatával. Lépésről lépésre bemutató C# nyelven.
type: docs
weight: 60
url: /hu/net/protect-excel-file/protect-row-in-excel-worksheet/
---
Ebben az oktatóanyagban néhány C#-forráskódot tekintünk meg, amely az Aspose.Cells könyvtárat használja az Excel-táblázat sorainak védelmére. Végigjárjuk a kód minden lépését, és elmagyarázzuk, hogyan működik. Gondosan kövesse az utasításokat a kívánt eredmény eléréséhez.

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

Ebben a lépésben meghatározzuk a táblázat soraira alkalmazandó stílust. Használja a következő kódot:

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

## 7. lépés: Az első sor zárolása

Ebben a lépésben a munkalap első sorát zároljuk. Használja a következő kódot:

```csharp
// Szerezze meg az első sor stílusát.
style = sheet.Cells.Rows[0].Style;
// Zárja le a stílust.
style. IsLocked = true;
// Alkalmazza a stílust az első sorra.
sheet.Cells.ApplyRowStyle(0, style);
```

## 8. lépés: A munkalap védelme

Most, hogy beállítottuk a stílusokat és zároltuk a sorokat, védjük meg a táblázatot. Használja a következő kódot:

```csharp
// Védje meg a munkalapot.
sheet.Protect(ProtectionType.All);
```

## 9. lépés: Az Excel fájl mentése

Végül elmentjük a módosított Excel fájlt. Használja a következő kódot:

```csharp
// Mentse el az Excel fájlt.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Ügyeljen arra, hogy a módosított Excel-fájl mentéséhez a megfelelő útvonalat adja meg.

### Minta forráskód a Protect Row In Excel munkalaphoz az Aspose.Cells for .NET használatával 
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
// Határozza meg a styleflag objektumot.
StyleFlag flag;
// Lapozzon át a munkalap összes oszlopán, és oldja fel őket.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    flag = new StyleFlag();
    flag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
// Szerezze meg az első sor stílusát.
style = sheet.Cells.Rows[0].Style;
// Zárd be.
style.IsLocked = true;
//Példányosítsa a zászlót.
flag = new StyleFlag();
// Állítsa be a zár beállítását.
flag.Locked = true;
// Alkalmazza a stílust az első sorra.
sheet.Cells.ApplyRowStyle(0, style, flag);
// Védje a lapot.
sheet.Protect(ProtectionType.All);
// Mentse el az excel fájlt.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## Következtetés

Gratulálok ! Most már rendelkezik C#-forráskóddal, amely lehetővé teszi az Excel-táblázat sorainak védelmét az Aspose.Cells .NET-könyvtár használatával. Ügyeljen arra, hogy gondosan kövesse a lépéseket, és testreszabja a kódot az Ön egyedi igényei szerint.

### GYIK (Gyakran Ismételt Kérdések)

#### Működik ez a kód az Excel legújabb verzióival?

Igen, ez a kód működik az Excel legújabb verzióival, beleértve az Excel 2010 és újabb formátumú fájlokat is.

#### A munkalap összes sora helyett csak bizonyos sorokat védhetek?

Igen, módosíthatja a kódot a védeni kívánt sorok megadásához. Ennek megfelelően módosítania kell a hurkot és az indexeket.

#### Hogyan tudom újra feloldani a lezárt vonalakat?

 Használhatja a`IsLocked` módszere a`Style` objektum értékének beállításához`false` és oldja fel a sorokat.

#### Lehetséges több munkalapot védeni ugyanabban az Excel-munkafüzetben?

Igen, megismételheti a munkalap létrehozásának, a stílus beállításának és a védelemnek a lépéseit a munkafüzet minden egyes munkalapjához.

#### Hogyan tudom megváltoztatni a táblázatvédelmi jelszót?

 A jelszót a gombbal módosíthatja`Protect` metódust, és argumentumként új jelszót adunk meg.