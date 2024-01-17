---
title: Fit To Excel Pages Options
linktitle: Fit To Excel Pages Options
second_title: Aspose.Cells for .NET API Reference
description: Ismerje meg, hogyan igazíthat automatikusan oldalakat egy Excel-táblázatba az Aspose.Cells for .NET segítségével.
type: docs
weight: 30
url: /hu/net/excel-page-setup/fit-to-excel-pages-options/
---
Ebben a cikkben lépésről lépésre elmagyarázzuk a következő C#-forráskódot: Fit to Excel Pages Options with Aspose.Cells for .NET. A művelet végrehajtásához a .NET Aspose.Cells könyvtárát fogjuk használni. Kövesse az alábbi lépéseket az oldalakhoz való illeszkedés konfigurálásához az Excelben.

## 1. lépés: Munkafüzet létrehozása
Az első lépés egy munkafüzet létrehozása. Egy munkafüzet objektumot fogunk példányosítani. Íme a kód a munkafüzet létrehozásához:

```csharp
// A dokumentumok könyvtárának elérési útja
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Munkafüzet objektum példányosítása
Workbook workbook = new Workbook();
```

## 2. lépés: A munkalap elérése
Most, hogy elkészítettük a munkafüzetet, az első munkalapra kell navigálnunk. Az első lap eléréséhez a 0 indexet fogjuk használni. Íme a kód a hozzáféréshez:

```csharp
// Hozzáférés a munkafüzet első munkalapjához
Worksheet worksheet = workbook.Worksheets[0];
```

## 3. lépés: Az Oldalhoz igazítás beállítása
 Ebben a lépésben a munkalap oldalaihoz konfiguráljuk a beállítást. Használjuk a`FitToPagesTall` és`FitToPagesWide` tulajdonságai a`PageSetup` objektumot a kívánt oldalszám megadásához a munkalap magasságához és szélességéhez. Íme a kód ehhez:

```csharp
// Állítsa be az oldalak számát a munkalap magasságához
worksheet.PageSetup.FitToPagesTall = 1;

// Állítsa be az oldalak számát a munkalap szélességéhez
worksheet.PageSetup.FitToPagesWide = 1;
```

## 4. lépés: A munkafüzet mentése
 Most, hogy beállítottuk az oldalakhoz igazítást, elmenthetjük a munkafüzetet. Használjuk a`Save` a Workbook objektum metódusa ehhez. Íme a kód a munkafüzet mentéséhez:

```csharp
// Mentse el a munkafüzetet
workbook.Save(dataDir + "FitToPagesOptions_out.xls");
```

### Minta forráskód a Fit To Excel Pages opciókhoz az Aspose.Cells for .NET használatával 
```csharp
// dokumentumok könyvtárának elérési útja.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Munkafüzet objektum példányosítása
Workbook workbook = new Workbook();
// Az Excel fájl első munkalapjának elérése
Worksheet worksheet = workbook.Worksheets[0];
// Az oldalak számának beállítása, amelyre a munkalap kiterjedjen
worksheet.PageSetup.FitToPagesTall = 1;
//Az oldalak számának beállítása, amelyre a munkalap szélessége kiterjed
worksheet.PageSetup.FitToPagesWide = 1;
// Mentse el a munkafüzetet.
workbook.Save(dataDir + "FitToPagesOptions_out.xls");
```

## Következtetés
Ebből a cikkből megtudtuk, hogyan konfigurálhatja az oldalakhoz való illeszkedést az Excelben az Aspose.Cells for .NET használatával. A következő lépéseken mentünk keresztül: a munkafüzet létrehozása, a munkalap elérése, az oldalakhoz való illeszkedés konfigurálása és a munkafüzet mentése. Mostantól ezt a tudást felhasználhatja táblázatainak a kívánt oldalakra való igazításához.

### GYIK

#### K: Hogyan telepíthetem az Aspose.Cells for .NET fájlt?

V: Az Aspose.Cells for .NET telepítéséhez használja a Visual Studio NuGet csomagkezelőjét. Keresse meg az "Aspose.Cells" csomagot, és telepítse a projektbe.

#### K: Beilleszthetem az oldalakat mind a magasságba, mind a szélességbe?

 V: Igen, a munkalap magasságát és szélességét is beállíthatja a`FitToPagesTall` és`FitToPagesWide` tulajdonságait. Minden mérethez megadhatja a kívánt oldalszámot.

#### K: Hogyan szabhatom testre az Oldalhoz igazítás opciókat?

V: Az oldalak számának megadása mellett más oldalakhoz igazítási beállításokat is testre szabhat, például a munkalap méretarányát, a papírtájolást, a margókat stb. Használja az elérhető tulajdonságokat a`PageSetup` tárgy erre.

#### K: Használhatom az Aspose.Cells for .NET programot meglévő munkafüzetek feldolgozására?

V: Igen, az Aspose.Cells for .NET segítségével megnyithatja és szerkesztheti a meglévő munkafüzeteket. Különféle műveletek végrehajtásához hozzáférhet a munkalapokhoz, cellákhoz, képletekhez, stílusokhoz és egyéb munkafüzetelemekhez.