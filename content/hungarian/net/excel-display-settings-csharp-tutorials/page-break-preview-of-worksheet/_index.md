---
title: Oldaltörés előnézeti munkalap
linktitle: Oldaltörés előnézeti munkalap
second_title: Aspose.Cells for .NET API Reference
description: Lépésről lépésre útmutató a munkalap oldaltörési előnézetének megjelenítéséhez az Aspose.Cells for .NET használatával.
type: docs
weight: 110
url: /hu/net/excel-display-settings-csharp-tutorials/page-break-preview-of-worksheet/
---
Ebben az oktatóanyagban elmagyarázzuk, hogyan jeleníthető meg egy munkalap oldaltörési előnézete az Aspose.Cells for .NET használatával. Kövesse az alábbi lépéseket a kívánt eredmény eléréséhez:

## 1. lépés: A környezet beállítása

Győződjön meg arról, hogy telepítette az Aspose.Cells for .NET fájlt, és beállította a fejlesztői környezetet. Győződjön meg arról is, hogy rendelkezik annak az Excel-fájlnak a másolatával, amelyen meg szeretné jeleníteni az oldaltörés előnézetét.

## 2. lépés: Importálja a szükséges függőségeket

Adja hozzá a szükséges direktívákat az Aspose.Cells osztályainak használatához:

```csharp
using Aspose.Cells;
using System.IO;
```

## 3. lépés: Kód inicializálása

Kezdje azzal, hogy inicializálja az Excel-dokumentumokat tartalmazó könyvtár elérési útját:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## 4. lépés: Az Excel fájl megnyitása

 Hozzon létre egy`FileStream` a megnyitandó Excel fájlt tartalmazó objektum:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 Példányosítás a`Workbook` objektumot, és nyissa meg az Excel fájlt a fájlfolyam segítségével:

```csharp
Workbook workbook = new Workbook(fstream);
```

## 5. lépés: Hozzáférés a Táblázathoz

Keresse meg az első munkalapot az Excel fájlban:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## 6. lépés: Oldalonkénti előnézet megjelenítése

Oldalonkénti előnézet engedélyezése a táblázathoz:

```csharp
worksheet. IsPageBreakPreview = true;
```

## 7. lépés: Módosítások mentése

Mentse el az Excel fájlban végzett módosításokat:

```csharp
workbook.Save(dataDir + "output.xls");
```

## 8. lépés: A fájlfolyam bezárása

Az összes erőforrás felszabadításához zárja be a fájlfolyamot:

```csharp
fstream.Close();
```

### Minta forráskód a munkalap oldaltörési előnézetéhez az Aspose.Cells for .NET használatával 
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
// A munkalap megjelenítése oldaltörés előnézetben
worksheet.IsPageBreakPreview = true;
// A módosított Excel fájl mentése
workbook.Save(dataDir + "output.xls");
// A fájlfolyam bezárása az összes erőforrás felszabadításához
fstream.Close();
```

## Következtetés

Ebben az oktatóanyagban megtanulta, hogyan jelenítheti meg egy munkalap oldaltörés előnézetét az Aspose.Cells for .NET használatával. A leírt lépések követésével egyszerűen szabályozhatja Excel-fájlok megjelenését és elrendezését.

### Gyakran Ismételt Kérdések (GYIK)

#### Mi az Aspose.Cells a .NET számára?

Az Aspose.Cells for .NET egy népszerű szoftverkönyvtár az Excel-fájlok kezeléséhez .NET-alkalmazásokban.

#### Megjeleníthetem egy adott munkalap oldalankénti előnézetét a teljes munkalap helyett?

Igen, az Aspose.Cells használatával engedélyezheti az oldaltörés előnézetét egy adott munkalaphoz a megfelelő Worksheet objektum elérésével.

#### Az Aspose.Cells támogatja az Excel egyéb fájlszerkesztési funkcióit?

Igen, az Aspose.Cells funkciók széles skáláját kínálja az Excel-fájlok szerkesztéséhez és kezeléséhez, például adatok hozzáadásához, formázásához, diagramok létrehozásához stb.

#### Az Aspose.Cells csak .xls formátumú Excel-fájlokkal működik?

Nem, az Aspose.Cells különféle Excel fájlformátumokat támogat, beleértve az .xls és .xlsx fájlokat.
	