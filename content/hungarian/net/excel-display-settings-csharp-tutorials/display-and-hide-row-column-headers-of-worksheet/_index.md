---
title: munkalap soroszlopfejléceinek megjelenítése és elrejtése
linktitle: munkalap soroszlopfejléceinek megjelenítése és elrejtése
second_title: Aspose.Cells for .NET API Reference
description: A sor- és oszlopfejlécek megjelenítése vagy elrejtése az Excel-munkalapon az Aspose.Cells for .NET használatával.
type: docs
weight: 40
url: /hu/net/excel-display-settings-csharp-tutorials/display-and-hide-row-column-headers-of-worksheet/
---
Ebben az oktatóanyagban bemutatjuk, hogyan jelenítheti meg vagy rejtheti el egy Excel-munkalap sor- és oszlopfejlécét C# forráskóddal az Aspose.Cells for .NET segítségével. Kövesse az alábbi lépéseket a kívánt eredmény eléréséhez.

## 1. lépés: Importálja a szükséges könyvtárakat

Győződjön meg arról, hogy telepítette az Aspose.Cells könyvtárat .NET-hez, és importálja a szükséges könyvtárakat a C# projektbe.

```csharp
using Aspose.Cells;
using System.IO;
```

## 2. lépés: Állítsa be a könyvtár elérési útját, és nyissa meg az Excel fájlt

 Állítsa be az Excel fájlt tartalmazó könyvtár elérési útját, majd nyissa meg a fájlt egy fájlfolyam létrehozásával és egy`Workbook` tárgy.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## 3. lépés: Lépjen az első munkalapra, és rejtse el a sor- és oszlopfejléceket

 Nyissa meg az Excel fájl első munkalapját a`Worksheets` tulajdona a`Workbook` tárgy. Ezután használja a`IsRowColumnHeadersVisible` tulajdona a`Worksheet` objektumot a sor- és oszlopfejlécek elrejtéséhez.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. IsRowColumnHeadersVisible = false;
```

## 4. lépés: Mentse el a változtatásokat

 Miután elvégezte a szükséges módosításokat, mentse el a módosított Excel fájlt a`Save` módszere a`Workbook` tárgy.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Minta forráskód a munkalapok soroszlopfejléceinek megjelenítéséhez és elrejtéséhez az Aspose.Cells for .NET használatával 
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
// A sorok és oszlopok fejlécének elrejtése
worksheet.IsRowColumnHeadersVisible = false;
// A módosított Excel fájl mentése
workbook.Save(dataDir + "output.xls");
// A fájlfolyam bezárása az összes erőforrás felszabadításához
fstream.Close(); 
```

## Következtetés

Ez a részletes útmutató bemutatja, hogyan jelenítheti meg vagy rejtheti el a sor- és oszlopfejléceket egy Excel-táblázatban az Aspose.Cells for .NET használatával. A mellékelt C# forráskód használatával egyszerűen testreszabhatja az Excel-fájlok fejléceinek megjelenítését.

### Gyakran Ismételt Kérdések (GYIK)

#### Mi az Aspose.Cells a .NET számára?

Az Aspose.Cells for .NET egy hatékony könyvtár az Excel-fájlok kezeléséhez .NET-alkalmazásokban.

#### Hogyan telepíthetem az Aspose.Cells for .NET fájlt?

 Az Aspose.Cells for .NET telepítéséhez le kell töltenie a megfelelő csomagot innen[Aspose Releases](https://releases/aspose.com/cells/net/) és add hozzá a .NET projektedhez.

#### Hogyan jeleníthetem meg vagy rejthetem el egy Excel-táblázat sor- és oszlopfejlécét az Aspose.Cells for .NET segítségével?

 Használhatja a`IsRowColumnHeadersVisible` tulajdona a`Worksheet`objektumot a sor- és oszlopfejlécek megjelenítéséhez vagy elrejtéséhez. Állítsa be`true` hogy megmutassa nekik és`false` hogy elrejtse őket.

#### Milyen más Excel-fájlformátumokat támogat az Aspose.Cells for .NET?

Az Aspose.Cells for .NET különféle Excel-fájlformátumokat támogat, mint például az XLS, XLSX, CSV, HTML, PDF és még sok más.
