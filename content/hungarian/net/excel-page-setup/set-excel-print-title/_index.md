---
title: Állítsa be az Excel nyomtatási címét
linktitle: Állítsa be az Excel nyomtatási címét
second_title: Aspose.Cells for .NET API Reference
description: Ismerje meg az Excel-fájlok egyszerű kezelését és a nyomtatási beállítások testreszabását az Aspose.Cells for .NET segítségével.
type: docs
weight: 170
url: /hu/net/excel-page-setup/set-excel-print-title/
---
Ebben az útmutatóban végigvezetjük, hogyan állíthat be nyomtatási címeket egy Excel-táblázatban az Aspose.Cells for .NET használatával. A feladat végrehajtásához kövesse az alábbi lépéseket.

## 1. lépés: A környezet beállítása

Győződjön meg arról, hogy beállította a fejlesztői környezetet, és telepítette az Aspose.Cells for .NET fájlt. A könyvtár legújabb verzióját letöltheti az Aspose hivatalos webhelyéről.

## 2. lépés: Importálja a szükséges névtereket

A C# projektben importálja a szükséges névtereket az Aspose.Cells használatához:

```csharp
using Aspose.Cells;
```

## 3. lépés: A dokumentumok könyvtár elérési útjának beállítása

 Nyilatkozni a`dataDir` változó megadja annak a könyvtárnak az elérési útját, ahová a generált Excel fájlt menteni szeretné:

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Feltétlenül cserélje ki`"YOUR_DOCUMENT_DIRECTORY"` a megfelelő elérési úttal a rendszeren.

## 4. lépés: Munkafüzet objektum létrehozása

Példányosítson egy munkafüzet objektumot, amely a létrehozni kívánt Excel-munkafüzetet képviseli:

```csharp
Workbook workbook = new Workbook();
```

## 5. lépés: Hozzáférés az első munkalaphoz

Keresse meg az Excel-munkafüzet első munkalapját a következő kóddal:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## 6. lépés: Címoszlopok meghatározása

Határozza meg a cím oszlopait a következő kóddal:

```csharp
pageSetup.PrintTitleColumns = "$A:$B";
```

Itt az A és B oszlopot címoszlopként határoztuk meg. Ezt az értéket igényei szerint állíthatja be.

## 7. lépés: Címsorok meghatározása

Határozza meg a címsorokat a következő kóddal:

```csharp
pageSetup.PrintTitleRows = "$1:$2";
```

Az 1. és 2. sort címsorként határoztuk meg. Ezeket az értékeket igényei szerint módosíthatja.

## 8. lépés: Az Excel-munkafüzet mentése

 Az Excel-munkafüzet a megadott nyomtatási címekkel történő mentéséhez használja a`Save` a munkafüzet objektum metódusa:

```csharp
workbook.Save(dataDir + "SetPrintTitle_out.xls");
```

Ezzel elmenti az Excel-munkafüzetet a „SetPrintTitle_out.xls” fájlnévvel a megadott könyvtárba.

### Minta forráskód a Set Excel Print Title használatához az Aspose.Cells for .NET használatával 
```csharp
// dokumentumok könyvtárának elérési útja.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Munkafüzet objektum példányosítása
Workbook workbook = new Workbook();
// A munkalap PageSetup hivatkozásának beszerzése
Aspose.Cells.PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Az A és B oszlopszámok címoszlopként történő meghatározása
pageSetup.PrintTitleColumns = "$A:$B";
// Az 1. és 2. sorszám meghatározása címsorként
pageSetup.PrintTitleRows = "$1:$2";
// Mentse el a munkafüzetet.
workbook.Save(dataDir + "SetPrintTitle_out.xls");
```

## Következtetés

Gratulálok ! Megtanulta, hogyan állíthat be nyomtatási címeket egy Excel-táblázatban az Aspose.Cells for .NET segítségével. A nyomtatási címek lehetővé teszik, hogy minden nyomtatott oldalon meghatározott sorokat és oszlopokat jelenítsen meg, megkönnyítve az adatok olvashatóságát és hivatkozását.

### GYIK

#### 1. Beállíthatok nyomtatási címeket bizonyos oszlopokhoz az Excelben?

 Igen, az Aspose.Cells for .NET segítségével bizonyos oszlopokat beállíthat nyomtatási címként a segítségével`PrintTitleColumns` tulajdona a`PageSetup` tárgy.

#### 2. Meghatározható-e mind az oszlop, mind a nyomtatott sor címe?

 Igen, a nyomtatási oszlop- és sorcímeket is beállíthatja a`PrintTitleColumns` és`PrintTitleRows` tulajdonságai a`PageSetup` tárgy.

#### 3. Milyen egyéb elrendezési beállításokat szabhatok testre az Aspose.Cells for .NET segítségével?

Az Aspose.Cells for .NET segítségével testreszabhatja a különféle oldalelrendezési beállításokat, például a margókat, az oldaltájolást, a nyomtatási léptéket stb.