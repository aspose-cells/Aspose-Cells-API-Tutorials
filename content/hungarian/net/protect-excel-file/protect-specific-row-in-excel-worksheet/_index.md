---
title: Adott sor védelme az Excel munkalapon
linktitle: Adott sor védelme az Excel munkalapon
second_title: Aspose.Cells for .NET API Reference
description: Adott sorok védelme az Excelben az Aspose.Cells for .NET segítségével. Útmutató lépésről lépésre a bizalmas adatok védelméhez.
type: docs
weight: 90
url: /hu/net/protect-excel-file/protect-specific-row-in-excel-worksheet/
---
bizalmas adatok védelme egy Excel-táblázatban elengedhetetlen az információbiztonság érdekében. Az Aspose.Cells for .NET hatékony megoldást kínál az Excel-táblázat egyes sorainak védelmére. Ez az útmutató végigvezeti Önt, hogyan védhet meg egy adott sort egy Excel-munkalapon a mellékelt C# forráskód használatával. Kövesse ezeket az egyszerű lépéseket az Excel-fájlok sorvédelmének beállításához.

## 1. lépés: Importálja a szükséges könyvtárakat

A kezdéshez győződjön meg arról, hogy az Aspose.Cells for .NET telepítve van a rendszerén. Az Aspose.Cells funkcióinak használatához hozzá kell adnia a megfelelő hivatkozásokat a C# projekthez. Íme a kód a szükséges könyvtárak importálásához:

```csharp
// Adja hozzá a szükséges hivatkozásokat
using Aspose.Cells;
```

## 2. lépés: Excel-munkafüzet és táblázat létrehozása

A szükséges könyvtárak importálása után létrehozhat egy új Excel-munkafüzetet és egy új munkalapot. Íme, hogyan kell csinálni:

```csharp
// dokumentumok könyvtárának elérési útja.
string dataDir = "YOUR DOCUMENTS DIRECTORY";

// Hozzon létre egy könyvtárat, ha még nem létezik.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
     System.IO.Directory.CreateDirectory(dataDir);

// Hozzon létre egy új munkafüzetet.
Workbook wb = new Workbook();

// Hozzon létre egy táblázatkezelő objektumot, és szerezze be az első lapot.
Worksheet sheet = wb.Worksheets[0];
```

## 3. lépés: A stílus és a stíluszászló beállítása

Most beállítjuk a cella stílusát és a stílusjelzőt, hogy feloldja a munkalap összes oszlopát. Itt van a szükséges kód:

```csharp
// Állítsa be a stílusobjektumot.
Styling styling;

// Állítsa be a styleflag objektumot.
StyleFlag flag;

// Lapozzon végig a munkalap összes oszlopán, és oldja fel a zárolást.
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     flag = new StyleFlag();
     flag. Locked = true;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
```

## 4. lépés: Védje meg az adott vonalat

Most megvédjük az adott sort a munkalapon. Az első sort zárolni fogjuk, hogy megakadályozzuk a módosításokat. Itt van, hogyan:

```csharp
// Szerezze meg az első sor stílusát.
style = sheet.Cells.Rows[0].Style;

// Zárd be.
style. IsLocked = true;

//Példányosítsa a zászlót.
flag = new StyleFlag();

// Állítsa be a zárolási paramétert.
flag. Locked = true;

// Alkalmazza a stílust az első sorra.
sheet.Cells.ApplyRowStyle(0, style, flag);
```

## 5. lépés: A munkalap védelme

Végül a teljes Excel munkalapot védjük, hogy megakadályozzuk a jogosulatlan módosításokat. Itt van, hogyan:

```csharp
// Védje meg a munkalapot.
sheet.Protect(ProtectionType.All);
```

## 6. lépés: Mentse el a védett Excel-fájlt

Ha végzett az Excel munkalap adott sorának védelmével, mentheti a védett Excel fájlt a rendszerébe. Itt van, hogyan:

```csharp
// Mentse el az Excel fájlt.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Az alábbi lépések végrehajtása után sikeresen védett egy adott sort az Excel-táblázatban az Aspose.Cells for .NET segítségével.

### Forráskód minta Adott sorok védelme Excel-munkalaphoz az Aspose.Cells for .NET használatával 
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

Az Excel-fájlokban található adatok védelme kulcsfontosságú az illetéktelen hozzáférés és a nem kívánt módosítások megelőzése érdekében. A .NET-hez készült Aspose.Cells könyvtár használatával könnyedén megvédheti az Excel-táblázat egyes sorait a mellékelt C# forráskód használatával. Kövesse ezt a lépésenkénti útmutatót, hogy további biztonsági réteget adjon Excel-fájljaihoz.

### GYIK

#### Működik az adott sorvédelem az Excel összes verziójában?

Igen, az Aspose.Cells for .NET használatával meghatározott sorvédelem az Excel összes támogatott verziójában működik.

#### Megvédhetek több konkrét sort egy Excel-táblázatban?

Igen, több konkrét sort is védhet az útmutatóban leírt hasonló módszerekkel.

#### Hogyan oldhatom fel egy adott sor zárolását egy Excel-táblázatban?

 Egy adott sor zárolásának feloldásához ennek megfelelően módosítania kell a forráskódot a`IsLocked` módszere a`Style` tárgy.