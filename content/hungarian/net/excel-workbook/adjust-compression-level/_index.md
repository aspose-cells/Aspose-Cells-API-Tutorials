---
title: Állítsa be a tömörítési szintet
linktitle: Állítsa be a tömörítési szintet
second_title: Aspose.Cells for .NET API Reference
description: Csökkentse Excel-munkafüzeteinek méretét a tömörítési szint beállításával az Aspose.Cells for .NET segítségével.
type: docs
weight: 50
url: /hu/net/excel-workbook/adjust-compression-level/
---
Ebben a lépésenkénti oktatóanyagban elmagyarázzuk a mellékelt C# forráskódot, amely lehetővé teszi a tömörítési szint beállítását az Aspose.Cells for .NET használatával. Kövesse az alábbi lépéseket az Excel-munkafüzet tömörítési szintjének beállításához.

## 1. lépés: Állítsa be a forrás- és kimeneti könyvtárakat

```csharp
// forráskönyvtár
string sourceDir = RunExamples.Get_SourceDirectory();
// Kimeneti könyvtár
string outDir = RunExamples.Get_OutputDirectory();
```

Ebben az első lépésben meghatározzuk az Excel fájlok forrás- és kimeneti könyvtárát.

## 2. lépés: Töltse be az Excel-munkafüzetet

```csharp
// Töltse be az Excel munkafüzetet
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
```

 megadott fájlból betöltjük az Excel munkafüzetet a`Workbook` osztály az Aspose.Cells-től.

## 3. lépés: Állítsa be a biztonsági mentési beállításokat

```csharp
// Határozza meg a biztonsági mentési beállításokat
XlsbSaveOptions options = new XlsbSaveOptions();
```

 Létrehozunk egy példányt a`XlsbSaveOptions` osztályt a mentési beállítások megadásához.

## 4. lépés: Állítsa be a tömörítési szintet (1. szint)

```csharp
// Állítsa be a tömörítési szintet (1. szint)
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
let elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 1): " + elapsedMs);
```

 A tömörítési szintet beállítással állítjuk be`CompressionType` nak nek`Level1`. Ezután ezzel a tömörítési beállítással mentjük az Excel munkafüzetet.

## 5. lépés: Állítsa be a tömörítési szintet (6. szint)

```csharp
// Állítsa be a tömörítési szintet (6. szint)
options.CompressionType = OoxmlCompressionType.Level6;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 6): " + elapsedMs);
```

 Megismételjük a folyamatot a tömörítési szint beállításához`Level6` és ezzel a lehetőséggel mentse az Excel-munkafüzetet.

## 6. lépés: Állítsa be a tömörítési szintet (9. szint)

```csharp
// Állítsa be a tömörítési szintet (9. szint)
options.CompressionType = OoxmlCompressionType.Level9;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 9): " + elapsedMs);
```

 Utoljára megismételjük a folyamatot a tömörítési szint beállításához`Level9` és ezzel a lehetőséggel mentse az Excel-munkafüzetet.

### Minta forráskód a tömörítési szint beállításához az Aspose.Cells for .NET használatával 
```csharp
//Forrás könyvtár
string sourceDir = RunExamples.Get_SourceDirectory();
string outDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
XlsbSaveOptions options = new XlsbSaveOptions();
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
var elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 1 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level6;
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 6 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level9;
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 9 Elapsed Time: " + elapsedMs);
Console.WriteLine("AdjustCompressionLevel executed successfully.");
```

## Következtetés

Gratulálok ! Megtanulta, hogyan állíthatja be a tömörítési szintet egy Excel-munkafüzetben az Aspose.Cells for .NET használatával. Kísérletezzen a különböző szintű tömörítésekkel, hogy megtalálja az igényeinek leginkább megfelelőt.

### GYIK

#### K: Mit jelent a tömörítés egy Excel-munkafüzetben?

V: Az Excel-munkafüzetben a tömörítés a fájlméret csökkentésének folyamata tömörítési algoritmusok használatával. Ez csökkenti a szükséges tárterületet, és javítja a teljesítményt a fájl betöltésekor és manipulálásakor.

#### K: Milyen szintű tömörítés érhető el az Aspose.Cells segítségével?

V: Az Aspose.Cells segítségével 1-től 9-ig állíthatja a tömörítési szintet. Minél magasabb a tömörítési szint, annál kisebb lesz a fájlméret, de növelheti a feldolgozási időt is.

#### K: Hogyan válasszam ki a megfelelő tömörítési szintet az Excel-munkafüzetemhez?

V: A tömörítési szint kiválasztása az Ön egyedi igényeitől függ. Ha a maximális tömörítést szeretné elérni, és a feldolgozási idő nem jelent problémát, választhatja a 9. szintet. Ha kompromisszumot szeretne a fájlméret és a feldolgozási idő között, választhat egy köztes szintet.

#### K: A tömörítés befolyásolja az adatok minőségét az Excel-munkafüzetben?

V: Nem, a tömörítés nincs hatással az Excel-munkafüzet adatminőségére. Egyszerűen csökkenti a fájl méretét tömörítési technikákkal anélkül, hogy magát az adatokat megváltoztatná.

#### K: Beállíthatom a tömörítési szintet az Excel fájl mentése után?

V: Nem, miután elmentette az Excel-fájlt egy adott tömörítési szinttel, később nem módosíthatja a tömörítési szintet. Ha módosítani szeretné, újra el kell mentenie a fájlt az új tömörítési szinttel.