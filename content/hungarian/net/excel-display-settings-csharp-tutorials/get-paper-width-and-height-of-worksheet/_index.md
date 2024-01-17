---
title: Szerezze be a papírszélességet és a munkalap magasságát
linktitle: Szerezze be a papírszélességet és a munkalap magasságát
second_title: Aspose.Cells for .NET API Reference
description: Hozzon létre egy lépésről lépésre szóló útmutatót a következő C#-forráskód leírásához, amellyel az Aspose.Cells for .NET segítségével meghatározhatja a táblázatok papírszélességét és magasságát.
type: docs
weight: 80
url: /hu/net/excel-display-settings-csharp-tutorials/get-paper-width-and-height-of-worksheet/
---
Ebben az oktatóanyagban lépésről lépésre elmagyarázzuk a következő C#-forráskódot, amellyel az Aspose.Cells for .NET segítségével meghatározhatja egy munkalap papírszélességét és magasságát. Kövesse az alábbi lépéseket:

## 1. lépés: A munkafüzet létrehozása
 Kezdje új munkafüzet létrehozásával a`Workbook` osztály:

```csharp
Workbook wb = new Workbook();
```

## 2. lépés: Nyissa meg az első munkalapot
 Ezután lépjen a munkafüzet első munkalapjára a gombbal`Worksheet` osztály:

```csharp
Worksheet ws = wb.Worksheets[0];
```

## 3. lépés: Állítsa a papírméretet A2-re, és mutassa meg a papír szélességét és magasságát hüvelykben
 Használja a`PaperSize` tulajdona a`PageSetup` objektummal állítsa be a papírméretet A2-re, majd használja a`PaperWidth` és`PaperHeight` tulajdonságokkal, hogy megkapja a papír szélességét és magasságát. Jelenítse meg ezeket az értékeket a`Console.WriteLine` módszer:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

## 4. lépés: Ismételje meg a lépéseket más papírméretekhez
Ismételje meg az előző lépéseket, módosítsa a papírméretet A3-ra, A4-re és Letterre, majd jelenítse meg az egyes méretekhez tartozó papírszélesség és -magasság értékeket:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

### Minta forráskód a Get Paper Width and Height Of Worksheet alkalmazáshoz az Aspose.Cells for .NET használatával 

```csharp
//Munkafüzet létrehozása
Workbook wb = new Workbook();
//Az első munkalap elérése
Worksheet ws = wb.Worksheets[0];
//Állítsa be a papírméretet A2-re, és nyomtassa a papír szélességét és magasságát hüvelykben
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Állítsa be a papírméretet A3-ra, és nyomtassa a papír szélességét és magasságát hüvelykben
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Állítsa be a papírméretet A4-re, és nyomtassa a papír szélességét és magasságát hüvelykben
ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Állítsa a papírméretet Letter értékre, és nyomtassa a papír szélességét és magasságát hüvelykben
ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```


## Következtetés

Megtanulta az Aspose.Cells for .NET használatát a táblázatok papírszélességének és magasságának meghatározásához. Ez a funkció hasznos lehet az Excel-dokumentumok konfigurálásához és pontos elrendezéséhez.

### Gyakran Ismételt Kérdések (GYIK)

#### Mi az Aspose.Cells a .NET számára?

Az Aspose.Cells for .NET egy hatékony könyvtár az Excel-fájlok kezeléséhez és feldolgozásához .NET-alkalmazásokban. Számos funkciót kínál Excel-fájlok létrehozásához, módosításához, konvertálásához és elemzéséhez.

#### Hogyan szerezhetem be a táblázat papírméretét az Aspose.Cells for .NET segítségével?

 Használhatja a`PageSetup` osztálya a`Worksheet` objektumot a papírméret eléréséhez. Használja a`PaperSize` tulajdonság a papírméret és a`PaperWidth` és`PaperHeight` tulajdonságokkal, hogy megkapja a papír szélességét és magasságát.

#### Milyen papírméreteket támogat az Aspose.Cells for .NET?

Az Aspose.Cells for .NET támogatja az általánosan használt papírméretek széles skáláját, mint például az A2, A3, A4 és Letter, valamint sok más egyéni méretet.

#### Testreszabhatom a táblázatok papírméretét az Aspose.Cells for .NET segítségével?

 Igen, beállíthat egyéni papírméretet a pontos szélesség és magasság méretének megadásával a`PaperWidth` és`PaperHeight` tulajdonságai a`PageSetup` osztály.