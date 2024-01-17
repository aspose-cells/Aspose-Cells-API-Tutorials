---
title: Állítsa be az Excel méretezési tényezőjét
linktitle: Állítsa be az Excel méretezési tényezőjét
second_title: Aspose.Cells for .NET API Reference
description: Tanulja meg az Excel-fájlok egyszerű kezelését és a méretezési tényező testreszabását az Aspose.Cells for .NET segítségével.
type: docs
weight: 180
url: /hu/net/excel-page-setup/set-excel-scaling-factor/
---
Ebben az útmutatóban végigvezetjük, hogyan állíthatja be a méretezési tényezőt egy Excel-táblázatban az Aspose.Cells for .NET használatával. A feladat végrehajtásához kövesse az alábbi lépéseket.

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

## 6. lépés: Állítsa be a méretezési tényezőt

Állítsa be a skálázási tényezőt a következő kóddal:

```csharp
worksheet.PageSetup.Zoom = 100;
```

Itt 100-ra állítottuk a méretezési tényezőt, ami azt jelenti, hogy a táblázat a normál méret 100%-ában jelenik meg nyomtatáskor.

## 7. lépés: Az Excel-munkafüzet mentése

 Az Excel-munkafüzet meghatározott méretezési tényezővel történő mentéséhez használja a`Save` a munkafüzet objektum metódusa:

```csharp
workbook.Save(dataDir + "ScalingFactor_out.xls");
```

Ezzel elmenti az Excel-munkafüzetet „ScalingFactor_out.xls” fájlnévvel a megadott könyvtárba.

### Minta forráskód a Set Excel Scaling Factorhoz az Aspose.Cells for .NET használatával 
```csharp
// dokumentumok könyvtárának elérési útja.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Munkafüzet objektum példányosítása
Workbook workbook = new Workbook();
// Az Excel fájl első munkalapjának elérése
Worksheet worksheet = workbook.Worksheets[0];
// A méretezési tényező beállítása 100-ra
worksheet.PageSetup.Zoom = 100;
// Mentse el a munkafüzetet.
workbook.Save(dataDir + "ScalingFactor_out.xls");
```

## Következtetés

Gratulálok ! Megtanulta, hogyan állíthatja be a méretezési tényezőt egy Excel-táblázatban az Aspose.Cells for .NET használatával. A méretezési tényező lehetővé teszi a táblázat méretének beállítását nyomtatáskor az optimális megjelenítés érdekében.

### GYIK

#### 1. Hogyan állíthat be skálázási tényezőt az Excel-táblázatban az Aspose.Cells for .NET segítségével?

 Használja a`Zoom` tulajdona a`PageSetup`objektumot a méretezési tényező beállításához. Például,`worksheet.PageSetup.Zoom = 100;` a skálázási tényezőt 100%-ra állítja.

#### 2. Testreszabhatom a méretezési tényezőt az igényeim szerint?

 Igen, módosíthatja a méretezési tényezőt a hozzárendelt érték módosításával`Zoom` ingatlan. Például,`worksheet.PageSetup.Zoom = 75;` a skálázási tényezőt 75%-ra állítja.

#### 3. Elmenthető az Excel munkafüzet a megadott méretezési tényezővel?

 Igen, használhatod a`Save` módszere a`Workbook` objektumot az Excel-munkafüzet elmentéséhez a megadott méretezési tényezővel.