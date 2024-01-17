---
title: Állítsa be az Excel fejléceit és lábléceit
linktitle: Állítsa be az Excel fejléceit és lábléceit
second_title: Aspose.Cells for .NET API Reference
description: Ismerje meg, hogyan állíthat be fejlécet és láblécet az Excelben az Aspose.Cells for .NET használatával.
type: docs
weight: 100
url: /hu/net/excel-page-setup/set-excel-headers-and-footers/
---

Ebben az oktatóanyagban lépésről lépésre bemutatjuk, hogyan állíthat be fejlécet és láblécet az Excelben az Aspose.Cells for .NET használatával. A folyamat szemléltetésére C# forráskódot fogunk használni.

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
Workbook excel = new Workbook();
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
```

Ez létrehoz egy üres munkafüzetet egy munkalappal, és hozzáférést biztosít a munkalap PageSetup objektumához.

## 5. lépés: Fejlécek beállítása

 Állítsa be a táblázatfejléceket a`SetHeader` a PageSetup objektum metódusai. Itt van egy minta kód:

```csharp
pageSetup.SetHeader(0, "&A");
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
```

Ez beállítja a munkalap nevét, az aktuális dátumot és időt, valamint a fájl nevét a fejlécekben.

## 6. lépés: Láblécek meghatározása

 Állítsa be a táblázat lábléceit a`SetFooter` a PageSetup objektum metódusai. Itt van egy minta kód:

```csharp
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
pageSetup.SetFooter(1, "&P");
pageSetup.SetFooter(2, "&N");
```

Ez beállítja a szöveges karakterláncot, az aktuális oldalszámot és a láblécekben lévő oldalak teljes számát.

## 7. lépés: A módosított munkafüzet mentése

Mentse el a módosított munkafüzetet a következő kóddal:

```csharp
excel.Save(dataDir + "OutputFileName.xls");
```

Ez elmenti a módosított munkafüzetet a megadott adatkönyvtárba.

### Minta forráskód az Excel fejlécek és láblécek beállításához az Aspose.Cells for .NET használatával 
```csharp
// dokumentumok könyvtárának elérési útja.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Munkafüzet objektum példányosítása
Workbook excel = new Workbook();
// A munkalap PageSetup hivatkozásának beszerzése
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
// A munkalap nevének beállítása a fejléc bal oldalán
pageSetup.SetHeader(0, "&A");
//Az aktuális dátum és pontos idő beállítása a fejléc középső részében
// és módosítsa a fejléc betűtípusát
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
// Állítsa be az aktuális fájl nevét a fejléc jobb oldalán, és módosítsa a
// a fejléc betűtípusa
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
// Karakterlánc beállítása a lábléc bal oldalán és a betűtípus módosítása
// ennek a karakterláncnak egy részének ("123")
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
// Az aktuális oldalszám beállítása a lábléc középső részén
pageSetup.SetFooter(1, "&P");
// Az oldalszám beállítása a lábléc jobb oldalán
pageSetup.SetFooter(2, "&N");
// Mentse el a munkafüzetet.
excel.Save(dataDir + "SetHeadersAndFooters_out.xls");
```


## Következtetés

Most megtanulta, hogyan állíthat be fejlécet és láblécet az Excelben az Aspose.Cells for .NET használatával. Ez az oktatóanyag végigvezeti a folyamat minden lépésén, a környezet beállításától a módosított munkafüzet mentéséig. Nyugodtan fedezze fel az Aspose.Cells szolgáltatásait, hogy további manipulációkat végezhessen az Excel-fájlokban.

### Gyakran Ismételt Kérdések (GYIK)

#### 1. Hogyan telepíthetem a rendszeremre az Aspose.Cells for .NET fájlt?
Az Aspose.Cells for .NET telepítéséhez le kell töltenie a telepítőcsomagot az Aspose hivatalos webhelyéről, és követnie kell a dokumentációban található utasításokat.

#### 2. Működik ez a módszer az Excel összes verziójával?
Igen, az Aspose.Cells for .NET segítségével fejlécek és láblécek beállításának módja az Excel összes támogatott verziójával működik.

#### 3. Tovább szabhatom a fejléceket és lábléceket?
Igen, az Aspose.Cells funkciók széles skáláját kínálja a fejlécek és láblécek testreszabásához, beleértve a szöveg elhelyezését, színét, betűtípusát, oldalszámait és még sok mást.

#### 4. Hogyan adhatok dinamikus információkat a fejlécekhez és láblécekhez?
Speciális változók és formázási kódok segítségével dinamikus információkat, például aktuális dátumot, időt, fájlnevet, oldalszámot stb. adhat hozzá a fejlécekhez és a láblécekhez.

#### 5. Eltávolíthatom a fejléceket és lábléceket beállítása után?
 Igen, a fejléceket és lábléceket a`ClearHeaderFooter` módszere a`PageSetup` tárgy. Ez visszaállítja az alapértelmezett fejléceket és lábléceket.