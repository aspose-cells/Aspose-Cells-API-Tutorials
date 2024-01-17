---
title: Távolítsa el a munkalap paneleket
linktitle: Távolítsa el a munkalap paneleket
second_title: Aspose.Cells for .NET API Reference
description: Lépésről lépésre útmutató ablaktáblák eltávolításához egy Excel-munkalapról az Aspose.Cells for .NET használatával.
type: docs
weight: 120
url: /hu/net/excel-display-settings-csharp-tutorials/remove-panes-of-worksheet/
---
Ebben az oktatóanyagban elmagyarázzuk, hogyan távolíthat el ablaktáblákat egy Excel-munkalapról az Aspose.Cells for .NET használatával. Kövesse az alábbi lépéseket a kívánt eredmény eléréséhez:

## 1. lépés: A környezet beállítása

Győződjön meg arról, hogy telepítette az Aspose.Cells for .NET fájlt, és beállította a fejlesztői környezetet. Ezenkívül győződjön meg arról, hogy rendelkezik az Excel-fájl másolatával, amelyből eltávolítani szeretné az ablaktáblákat.

## 2. lépés: Importálja a szükséges függőségeket

Adja hozzá a szükséges direktívákat az Aspose.Cells osztályainak használatához:

```csharp
using Aspose.Cells;
```

## 3. lépés: Kód inicializálása

Kezdje azzal, hogy inicializálja az Excel-dokumentumokat tartalmazó könyvtár elérési útját:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## 4. lépés: Az Excel fájl megnyitása

 Példányosítson egy újat`Workbook` objektumot, és nyissa meg az Excel fájlt a`Open` módszer:

```csharp
Workbook book = new Workbook(dataDir + "Book1.xls");
```

## 5. lépés: Határozza meg az aktív cellát

 Állítsa be a munkalap aktív celláját a`ActiveCell` ingatlan:

```csharp
book.Worksheets[0].ActiveCell = "A20";
```

## 6. lépés: Az ablaktáblák törlése

 Távolítsa el az ablaktáblákat a munkalapablakból a`RemoveSplit` módszer:

```csharp
book.Worksheets[0].RemoveSplit();
```

## 7. lépés: Módosítások mentése

Mentse el az Excel fájlban végzett módosításokat:

```csharp
book.Save(dataDir + "output.xls");
```

### Minta forráskód a munkalap ablaktábláinak eltávolításához az Aspose.Cells segítségével .NET-hez 
```csharp
// dokumentumok könyvtárának elérési útja.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Példányosítson egy új munkafüzetet, és nyisson meg egy sablonfájlt
Workbook book = new Workbook(dataDir + "Book1.xls");
// Állítsa be az aktív cellát
book.Worksheets[0].ActiveCell = "A20";
// A munkalap ablak felosztása
book.Worksheets[0].RemoveSplit();
// Mentse el az excel fájlt
book.Save(dataDir + "output.xls");
```

## Következtetés

Ebből az oktatóanyagból megtanulta, hogyan távolíthat el ablaktáblákat egy Excel-munkalapról az Aspose.Cells for .NET használatával. A leírt lépések követésével egyszerűen testreszabhatja Excel-fájlok megjelenését és viselkedését.

### Gyakran Ismételt Kérdések (GYIK)

#### Mi az Aspose.Cells a .NET számára?

Az Aspose.Cells for .NET egy népszerű szoftverkönyvtár az Excel-fájlok kezeléséhez .NET-alkalmazásokban.

#### Hogyan állíthatom be egy munkalap aktív celláját az Aspose.Cells-ben?

 Az aktív cellát a gombbal állíthatja be`ActiveCell` Munkalap objektum tulajdonsága.

#### Csak vízszintes vagy függőleges ablaktáblákat távolíthatok el a munkalapablakból?

 Igen, az Aspose.Cells használatával csak vízszintes vagy függőleges ablaktáblákat távolíthat el a megfelelő módszerekkel, mint pl`RemoveHorizontalSplit` vagy`RemoveVerticalSplit`.

#### Az Aspose.Cells csak .xls formátumú Excel-fájlokkal működik?

Nem, az Aspose.Cells különféle Excel fájlformátumokat támogat, beleértve az .xls és .xlsx fájlokat.
	