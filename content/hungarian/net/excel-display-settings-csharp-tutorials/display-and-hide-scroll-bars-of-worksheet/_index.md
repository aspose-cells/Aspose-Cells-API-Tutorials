---
title: A munkalap görgetősávjainak megjelenítése és elrejtése
linktitle: A munkalap görgetősávjainak megjelenítése és elrejtése
second_title: Aspose.Cells for .NET API Reference
description: Görgetősávok megjelenítése vagy elrejtése az Excel-munkalapon az Aspose.Cells for .NET használatával.
type: docs
weight: 50
url: /hu/net/excel-display-settings-csharp-tutorials/display-and-hide-scroll-bars-of-worksheet/
---
Ebben az oktatóanyagban bemutatjuk, hogyan jeleníthet meg vagy rejthet el függőleges és vízszintes görgetősávokat egy Excel-munkalapon C# forráskóddal az Aspose.Cells for .NET segítségével. Kövesse az alábbi lépéseket a kívánt eredmény eléréséhez.

## 1. lépés: Importálja a szükséges könyvtárakat

Győződjön meg arról, hogy telepítette az Aspose.Cells könyvtárat .NET-hez, és importálja a szükséges könyvtárakat a C# projektbe.

```csharp
using Aspose.Cells;
using System.IO;
```

## 2. lépés: Állítsa be a könyvtár elérési útját, és nyissa meg az Excel fájlt

 Állítsa be az Excel fájlt tartalmazó könyvtár elérési útját, majd nyissa meg a fájlt egy fájlfolyam létrehozásával és egy`Workbook` tárgy.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## 3. lépés: Görgetősávok elrejtése

 Használja a`IsVScrollBarVisible` és`IsHScrollBarVisible` tulajdonságai a`Workbook.Settings` objektumot a munkalap függőleges és vízszintes görgetősávjának elrejtéséhez.

```csharp
workbook.Settings.IsVScrollBarVisible = false;
workbook.Settings.IsHScrollBarVisible = false;
```

## 4. lépés: Mentse el a változtatásokat

 Miután elvégezte a szükséges módosításokat, mentse el a módosított Excel fájlt a`Save` módszere a`Workbook` tárgy.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Minta forráskód a munkalap görgetősávjainak megjelenítéséhez és elrejtéséhez az Aspose.Cells for .NET használatával 

```csharp
// dokumentumok könyvtárának elérési útja.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// A megnyitandó Excel fájlt tartalmazó fájlfolyam létrehozása
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Munkafüzet objektum példányosítása
// Az Excel fájl megnyitása a fájlfolyamon keresztül
Workbook workbook = new Workbook(fstream);
// Az Excel fájl függőleges görgetősávjának elrejtése
workbook.Settings.IsVScrollBarVisible = false;
// Az Excel fájl vízszintes görgetősávjának elrejtése
workbook.Settings.IsHScrollBarVisible = false;
// A módosított Excel fájl mentése
workbook.Save(dataDir + "output.xls");
// A fájlfolyam bezárása az összes erőforrás felszabadításához
fstream.Close();
```

### Következtetés

Ez a részletes útmutató bemutatja, hogyan jeleníthet meg vagy rejthet el függőleges és vízszintes görgetősávokat egy Excel-táblázatban az Aspose.Cells for .NET segítségével. A mellékelt C# forráskód használatával egyszerűen testreszabhatja az Excel-fájlok görgetősávjainak megjelenítését.

### Gyakran Ismételt Kérdések (GYIK)

#### Mi az Aspose.Cells a .NET számára?

Az Aspose.Cells for .NET egy hatékony könyvtár az Excel-fájlok kezeléséhez .NET-alkalmazásokban.

#### Hogyan telepíthetem az Aspose.Cells for .NET fájlt?

 Az Aspose.Cells for .NET telepítéséhez le kell töltenie a megfelelő csomagot innen[Aspose Releases](https://releases/aspose.com/cells/net/) és add hozzá a .NET projektedhez.

#### Hogyan jeleníthetek meg vagy rejthetek el görgetősávokat egy Excel-táblázatban az Aspose.Cells for .NET segítségével?

 Használhatja a`IsVScrollBarVisible` és`IsHScrollBarVisible` tulajdonságai a`Workbook.Settings` objektumot a függőleges és vízszintes görgetősáv megjelenítéséhez vagy elrejtéséhez egy Excel-munkalapon.

#### Milyen más Excel-fájlformátumokat támogat az Aspose.Cells for .NET?

Az Aspose.Cells for .NET számos Excel fájlformátumot támogat, például XLS, XLSX, CSV, HTML, PDF stb.