---
title: Oldalméretek lekérése
linktitle: Oldalméretek lekérése
second_title: Aspose.Cells for .NET API Reference
description: Ismerje meg, hogyan kérheti le az oldalméreteket Excelben az Aspose.Cells for .NET használatával. Lépésről lépésre útmutató forráskóddal C# nyelven.
type: docs
weight: 40
url: /hu/net/excel-page-setup/get-page-dimensions/
---
Az Aspose.Cells for .NET egy hatékony könyvtár, amely lehetővé teszi a fejlesztők számára, hogy programozottan dolgozzanak Microsoft Excel fájlokkal. Funkciók széles skáláját kínálja az Excel dokumentumok kezeléséhez, beleértve az oldalméretek lekérését is. Ebben az oktatóanyagban végigvezetjük az oldalméretek lekérésének lépésein az Aspose.Cells for .NET használatával.

## 1. lépés: Hozzon létre egy példányt a Workbook osztályból

A kezdéshez létre kell hoznunk egy példányt a Workbook osztályból, amely az Excel munkafüzetet képviseli. Ez a következő kóddal érhető el:

```csharp
Workbook book = new Workbook();
```

## 2. lépés: Hozzáférés a táblázathoz

Ezután a munkafüzetben arra a munkalapra kell navigálnunk, ahol be akarjuk állítani az oldalméreteket. Ebben a példában tegyük fel, hogy az első munkalappal szeretnénk dolgozni. A következő kóddal érhetjük el:

```csharp
Worksheet sheet = book.Worksheets[0];
```

## 3. lépés: Állítsa be a papírméretet A2-re, és a nyomtatási szélességet és magasságot hüvelykben adja meg

Most beállítjuk a papírméretet A2-re, és kinyomtatjuk az oldal szélességét és magasságát hüvelykben. Ez a következő kóddal érhető el:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("A2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## 4. lépés: Állítsa a papírméretet A3-ra, és a nyomtatási szélességet és magasságot hüvelykben adja meg

Ezután beállítjuk a papírméretet A3-ra, és kinyomtatjuk az oldal szélességét és magasságát hüvelykben. Itt van a megfelelő kód:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("A3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## 5. lépés: Állítsa be a papírméretet A4-re, és a nyomtatási szélességet és magasságot hüvelykben adja meg

Most beállítjuk a papírméretet A4-re, és kinyomtatjuk az oldal szélességét és magasságát hüvelykben. Íme a kód:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("A4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## 6. lépés: Állítsa a papírméretet Letter értékre, és nyomtassa ki a szélességet és magasságot hüvelykben

Végül a papírméretet Letterre állítjuk, és kinyomtatjuk az oldal szélességét és magasságát hüvelykben. Íme a kód:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("Letter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

### Minta forráskód az oldalméretek lekéréséhez az Aspose.Cells for .NET használatával 
```csharp
// Hozzon létre egy példányt a munkafüzet osztályból
Workbook book = new Workbook();
// Az első munkalap elérése
Worksheet sheet = book.Worksheets[0];
// Állítsa be a papírméretet A2-re, és nyomtassa a papír szélességét és magasságát hüvelykben
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Állítsa be a papírméretet A3-ra, és nyomtassa a papír szélességét és magasságát hüvelykben
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Állítsa be a papírméretet A4-re, és nyomtassa a papír szélességét és magasságát hüvelykben
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Állítsa a papírméretet Letter értékre, és nyomtassa a papír szélességét és magasságát hüvelykben
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
Console.WriteLine("GetPageDimensions executed successfully.\r\n");
```

## Következtetés

Gratulálok ! Megtanulta, hogyan kérheti le az oldalméreteket az Aspose.Cells for .NET használatával. Ez a funkció akkor lehet hasznos, ha konkrét műveleteket kell végrehajtania az Excel-fájlok oldalméretei alapján.

Ne felejtse el tovább vizsgálni az Aspose.Cells dokumentációját, hogy felfedezze az általa kínált összes hatékony funkciót.

### GYIK

#### 1. Milyen más papírméreteket támogat az Aspose.Cells for .NET?

Az Aspose.Cells for .NET számos papírméretet támogat, beleértve az A1, A5, B4, B5, Executive, Legal, Letter és még sok más papírméretet. A támogatott papírméretek teljes listáját a dokumentációban tekintheti meg.

#### 2. Beállíthatok egyéni oldalméreteket az Aspose.Cells segítségével .NET-hez?

Igen, egyéni oldalméreteket állíthat be a kívánt szélesség és magasság megadásával. Az Aspose.Cells teljes rugalmasságot kínál az oldalméretek testreszabásához az Ön igényei szerint.

#### 3. Megadhatom az oldal méreteit hüvelyktől eltérő mértékegységben?

Igen, az Aspose.Cells for .NET lehetővé teszi az oldalméretek különböző mértékegységekben, például hüvelykben, centiméterben, milliméterben és pontban történő megadását.

#### 4. Az Aspose.Cells for .NET támogatja az oldalbeállítások egyéb szerkesztési funkcióit?

Igen, az Aspose.Cells a funkciók teljes skáláját kínálja az oldalbeállítások szerkesztéséhez, beleértve a margók, tájolás, fejlécek és láblécek beállítását stb.