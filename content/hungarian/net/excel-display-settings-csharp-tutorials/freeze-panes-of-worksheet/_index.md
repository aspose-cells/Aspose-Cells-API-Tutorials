---
title: A munkalap ablaktábláinak lefagyasztása
linktitle: A munkalap ablaktábláinak lefagyasztása
second_title: Aspose.Cells for .NET API Reference
description: Az Aspose.Cells for .NET segítségével könnyedén kezelheti az Excel-munkalap lefagyasztott ablaktábláit.
type: docs
weight: 70
url: /hu/net/excel-display-settings-csharp-tutorials/freeze-panes-of-worksheet/
---
Ebben az oktatóanyagban bemutatjuk, hogyan zárolhat ablaktáblákat egy Excel-munkalapon C# forráskóddal az Aspose.Cells for .NET segítségével. Kövesse az alábbi lépéseket a kívánt eredmény eléréséhez.

## 1. lépés: Importálja a szükséges könyvtárakat

Győződjön meg arról, hogy telepítette az Aspose.Cells könyvtárat .NET-hez, és importálja a szükséges könyvtárakat a C# projektbe.

```csharp
using Aspose.Cells;
```

## 2. lépés: Állítsa be a könyvtár elérési útját, és nyissa meg az Excel fájlt

 Állítsa be az Excel-fájlt tartalmazó könyvtár elérési útját, majd nyissa meg a fájlt az a`Workbook` tárgy.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## 3. lépés: Lépjen a táblázatba, és alkalmazza a panel zárolási beállításait

 Keresse meg az első munkalapot az Excel fájlban a`Worksheet` tárgy. Ezután használja a`FreezePanes` módszert a panelzár beállításainak alkalmazására.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. FreezePanes(3, 2, 3, 2);
```

A fenti példában az ablaktáblák a 3. sor és a 2. oszlop cellájához vannak zárva.

## 4. lépés: Mentse el a változtatásokat

 Miután elvégezte a szükséges módosításokat, mentse el a módosított Excel fájlt a`Save` módszere a`Workbook` tárgy.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Minta forráskód a munkalap ablaktábláinak rögzítéséhez az Aspose.Cells for .NET használatával 

```csharp
// dokumentumok könyvtárának elérési útja.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// A megnyitandó Excel fájlt tartalmazó fájlfolyam létrehozása
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Munkafüzet objektum példányosítása
// Az Excel fájl megnyitása a fájlfolyamon keresztül
Workbook workbook = new Workbook(fstream);
// Az Excel fájl első munkalapjának elérése
Worksheet worksheet = workbook.Worksheets[0];
// Az ablaktáblák rögzítési beállításainak alkalmazása
worksheet.FreezePanes(3, 2, 3, 2);
// A módosított Excel fájl mentése
workbook.Save(dataDir + "output.xls");
// A fájlfolyam bezárása az összes erőforrás felszabadításához
fstream.Close();
```

## Következtetés

Ez a részletes útmutató bemutatja, hogyan zárolhat ablaktáblákat egy Excel-táblázatban az Aspose.Cells for .NET használatával. A mellékelt C#-forráskód használatával egyszerűen testreszabhatja az ablaktáblák zárolási beállításait, így jobban rendszerezheti és megjelenítheti adatait Excel-fájlokban.

### Gyakran Ismételt Kérdések (GYIK)

#### Mi az Aspose.Cells a .NET számára?

Az Aspose.Cells for .NET egy hatékony könyvtár az Excel-fájlok kezeléséhez .NET-alkalmazásokban.

#### Hogyan telepíthetem az Aspose.Cells for .NET fájlt?

 Az Aspose.Cells for .NET telepítéséhez le kell töltenie a megfelelő csomagot innen[Aspose Releases](https://releases/aspose.com/cells/net/) és add hozzá a .NET projektedhez.

#### Hogyan zárolható ablaktáblák egy Excel-munkalapon az Aspose.Cells for .NET használatával?

 Használhatja a`FreezePanes` módszere a`Worksheet` objektum a munkalap ablaktábláinak zárolásához. Sor- és oszlopindexek megadásával adja meg a zárolni kívánt cellákat.

#### Testreszabhatom a panelzár beállításait az Aspose.Cells for .NET segítségével?

 Igen, a`FreezePanes` módszerrel megadhatja, hogy mely cellákat zárolja szükség szerint, megadva a megfelelő sor- és oszlopindexeket.
