---
title: Állítsa be az Excel első oldalszámát
linktitle: Állítsa be az Excel első oldalszámát
second_title: Aspose.Cells for .NET API Reference
description: Ismerje meg, hogyan állíthatja be az első oldalszámot az Excelben az Aspose.Cells for .NET használatával.
type: docs
weight: 90
url: /hu/net/excel-page-setup/set-excel-first-page-number/
---
Ebben az oktatóanyagban végigvezetjük, hogyan állíthatja be az első oldalszámot az Excelben az Aspose.Cells for .NET használatával. A folyamat szemléltetésére C# forráskódot fogunk használni.

## 1. lépés: A környezet beállítása

Győződjön meg arról, hogy az Aspose.Cells for .NET telepítve van a gépén. Hozzon létre egy új projektet is a kívánt fejlesztői környezetben.

## 2. lépés: Importálja a szükséges könyvtárakat

A kódfájlban importálja az Aspose.Cells használatához szükséges könyvtárakat. Itt van a megfelelő kód:

```csharp
using Aspose.Cells;
```

## 3. lépés: Állítsa be az adatkönyvtárat

Állítsa be az adatkönyvtárat, ahová menteni szeretné a módosított Excel fájlt. Használja a következő kódot:

```csharp
string dataDir = "YOUR DATA DIRECTORY";
```

Feltétlenül adja meg a teljes könyvtár elérési utat.

## 4. lépés: A munkafüzet és a munkalap létrehozása

Hozzon létre egy új munkafüzet objektumot, és navigáljon a munkafüzet első munkalapjára a következő kóddal:

```csharp
Workbook workbook = new Workbook();
Worksheet worksheet = workbook.Worksheets[0];
```

Ezzel létrehoz egy üres munkafüzetet egy munkalappal.

## 5. lépés: Az első oldal számának beállítása

Állítsa be a munkalap oldalainak első oldalának számát a következő kóddal:

```csharp
worksheet.PageSetup.FirstPageNumber = 2;
```

Ezzel az első oldalszám 2 lesz.

## 6. lépés: A módosított munkafüzet mentése

Mentse el a módosított munkafüzetet a következő kóddal:

```csharp
workbook.Save(dataDir + "OutputFileName.xls");
```

Ez elmenti a módosított munkafüzetet a megadott adatkönyvtárba.

### Minta forráskód a Set Excel First Page Number (Aspose.Cells for .NET) használatával 
```csharp
// dokumentumok könyvtárának elérési útja.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Munkafüzet objektum példányosítása
Workbook workbook = new Workbook();
// Az Excel fájl első munkalapjának elérése
Worksheet worksheet = workbook.Worksheets[0];
// A munkalap oldalainak első oldalszámának beállítása
worksheet.PageSetup.FirstPageNumber = 2;
// Mentse el a munkafüzetet.
workbook.Save(dataDir + "SetFirstPageNumber_out.xls");
```

## Következtetés

Most megtanulta, hogyan állíthatja be az első oldalszámot az Excelben az Aspose.Cells for .NET használatával. Ez az oktatóanyag végigvezeti a folyamat minden lépésén, a környezet beállításától az első oldalszám beállításáig. Ezt a tudást most felhasználhatja az Excel-fájlok oldalszámozásának testreszabására.

### GYIK

#### 1. kérdés: Beállíthatok különböző első oldalszámot minden munkalaphoz?

 V1: Igen, minden munkalaphoz más első oldalszámot állíthat be, ha eléri a`FirstPageNumber`az adott munkalap tulajdonsága`PageSetup` tárgy.

#### 2. kérdés: Hogyan ellenőrizhetem egy meglévő táblázat első oldalszámát?

 2. válasz: Meglévő munkalap első oldalszámát ellenőrizheti a`FirstPageNumber` tulajdona a`PageSetup` az adott munkalapnak megfelelő objektum.

#### 3. kérdés: Alapértelmezés szerint az oldalszámozás mindig 1-től kezdődik?

3. válasz: Igen, az oldalszámozás alapértelmezés szerint 1-től kezdődik az Excelben. Használhatja azonban az oktatóanyagban látható kódot egy másik első oldalszám beállításához.

#### 4. kérdés: Maradandóak az első oldalszám módosításai a szerkesztett Excel-fájlban?

4. válasz: Igen, az első oldalszámon végrehajtott módosítások véglegesen mentésre kerülnek a módosított Excel fájlba.

#### 5. kérdés: Működik ez a módszer minden Excel fájlformátumhoz, például .xls és .xlsx?

5. válasz: Igen, ez a módszer az Aspose.Cells által támogatott összes Excel-fájlformátum esetén működik, beleértve az .xls-t és az .xlsx-et is.