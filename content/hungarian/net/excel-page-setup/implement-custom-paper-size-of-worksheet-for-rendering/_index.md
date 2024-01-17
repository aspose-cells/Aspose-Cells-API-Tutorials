---
title: Valósítson meg egyedi papírméretű munkalapot a rendereléshez
linktitle: Valósítson meg egyedi papírméretű munkalapot a rendereléshez
second_title: Aspose.Cells for .NET API Reference
description: Útmutató lépésről lépésre egyéni munkalapméret megvalósításához az Aspose.Cells for .NET segítségével. Állítsa be a méreteket, adjon hozzá üzenetet, és mentse el PDF-ként.
type: docs
weight: 50
url: /hu/net/excel-page-setup/implement-custom-paper-size-of-worksheet-for-rendering/
---
A munkalap egyéni méretének megvalósítása nagyon hasznos lehet, ha meghatározott méretű PDF-dokumentumot szeretne létrehozni. Ebben az oktatóanyagban megtudjuk, hogyan használhatja az Aspose.Cells for .NET alkalmazást egy munkalap egyéni méretének beállítására, majd a dokumentum mentésére PDF formátumban.

## 1. lépés: A kimeneti mappa létrehozása

Mielőtt elkezdené, létre kell hoznia egy kimeneti mappát, ahová a generált PDF fájl mentésre kerül. A kimeneti mappához bármilyen elérési utat használhat.

```csharp
// Kimeneti könyvtárak
string outputDir = "YOUR_OUTPUT_FOLDER";
```

Ügyeljen arra, hogy a kimeneti mappa megfelelő elérési útját adja meg.

## 2. lépés: A munkafüzet objektum létrehozása

kezdéshez létre kell hoznia egy munkafüzet objektumot az Aspose.Cells használatával. Ez az objektum képviseli a táblázatot.

```csharp
// Hozza létre a munkafüzet objektumot
Workbook wb = new Workbook();
```

## 3. lépés: Hozzáférés az első munkalaphoz

A munkafüzet objektum létrehozása után hozzáférhet az első munkalaphoz.

```csharp
// Hozzáférés az első munkalaphoz
Worksheet ws = wb.Worksheets[0];
```

## 4. lépés: Egyéni munkalapméret beállítása

 Mostantól egyéni munkalapméretet állíthat be a segítségével`CustomPaperSize(width, height)` a PageSetup osztály metódusa.

```csharp
// Egyéni munkalapméret beállítása (hüvelykben)
ws.PageSetup.CustomPaperSize(6, 4);
```

Ebben a példában a munkalap méretét 6 hüvelyk szélesre és 4 hüvelyk magasra állítottuk be.

## 5. lépés: Hozzáférés a B4 cellához

Ezt követően egy adott cellát érhetünk el a munkalapon. Ebben az esetben elérjük a B4 cellát.

```csharp
// Hozzáférés a B4 cellához
Cell b4 = ws.Cells["B4"];
```

## 6. lépés: Az üzenet hozzáadása a B4 cellába

 Mostantól üzenetet adhatunk a B4 cellához a`PutValue(value)` módszer.

```csharp
// Adja hozzá az üzenetet a B4 cellába
b4.PutValue("PDF page size: 6.00 x 4.00 inches");
```

Ebben a példában a "PDF oldalméret: 6,00" x 4,00" üzenetet adtuk a B4 cellába.

## 7. lépés: Mentse el a munkalapot PDF formátumban

 Végül a munkalapot PDF formátumba menthetjük a`Save(filePath)` a munkafüzet objektum metódusa.

```csharp
// Mentse el a munkalapot PDF formátumban
wb.Save(outputDir + "outputCustomPaperSize.pdf");
```

Adja meg a generált PDF fájl kívánt elérési útját a korábban létrehozott kimeneti mappa használatával.

### Forráskód minta az Aspose.Cells for .NET használatával történő megjelenítéshez egyedi papírméret munkalap megvalósításához 
```csharp
//Kimeneti könyvtár
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//Munkafüzet objektum létrehozása
Workbook wb = new Workbook();
//Az első munkalap elérése
Worksheet ws = wb.Worksheets[0];
//Állítsa be az egyéni papírméretet hüvelykben
ws.PageSetup.CustomPaperSize(6, 4);
//Hozzáférés a B4 cellához
Cell b4 = ws.Cells["B4"];
//Adja hozzá az üzenetet a B4 cellába
b4.PutValue("Pdf Page Dimensions: 6.00 x 4.00 in");
//Mentse el a munkafüzetet pdf formátumban
wb.Save(outputDir + "outputCustomPaperSize.pdf");
```

## Következtetések

Ebben az oktatóanyagban megtanulta, hogyan valósíthat meg egyéni méretű munkalapot az Aspose.Cells for .NET használatával. Ezekkel a lépésekkel megadhatja a munkalapok méretét, majd elmentheti a dokumentumokat PDF formátumban. Reméljük, hogy ez az útmutató segített megérteni az egyéni táblázatméretek megvalósításának folyamatát.

### Gyakran Ismételt Kérdések (GYIK)

#### 1. kérdés: Tovább szabhatom a táblázat elrendezését?

Igen, az Aspose.Cells számos lehetőséget kínál a munkalap elrendezésének testreszabására. Beállíthat egyéni méreteket, oldaltájolást, margókat, fej- és láblécet és még sok mást.

#### 2. kérdés: Milyen egyéb kimeneti formátumokat támogat az Aspose.Cells?

Az Aspose.Cells számos különböző kimeneti formátumot támogat, beleértve a PDF, XLSX, XLS, CSV, HTML, TXT és még sok más formátumot. Kiválaszthatja a kívánt kimeneti formátumot igényei szerint.