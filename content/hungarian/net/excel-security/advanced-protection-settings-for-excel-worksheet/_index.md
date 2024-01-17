---
title: Speciális védelmi beállítások az Excel munkalaphoz
linktitle: Speciális védelmi beállítások az Excel munkalaphoz
second_title: Aspose.Cells for .NET API Reference
description: Védje Excel-fájljait az Aspose.Cells for .NET speciális védelmi beállításával.
type: docs
weight: 10
url: /hu/net/excel-security/advanced-protection-settings-for-excel-worksheet/
---
Ebben az oktatóanyagban végigvezetjük az Excel-táblázat speciális védelmi beállításainak a .NET-hez készült Aspose.Cells könyvtár használatával történő beállításának lépésein. A feladat végrehajtásához kövesse az alábbi utasításokat.

## 1. lépés: Előkészítés

Győződjön meg arról, hogy telepítette az Aspose.Cells for .NET fájlt, és létrehozott egy C#-projektet az előnyben részesített integrált fejlesztői környezetben (IDE).

## 2. lépés: Állítsa be a dokumentumkönyvtár elérési útját

 Nyilatkozni a`dataDir` változót, és inicializálja a dokumentumkönyvtár elérési útjával. Például :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Feltétlenül cserélje ki`"YOUR_DOCUMENTS_DIRECTORY"` a címtár tényleges elérési útjával.

## 3. lépés: Hozzon létre egy fájlfolyamot az Excel fájl megnyitásához

 Hozzon létre egy`FileStream` a megnyitandó Excel fájlt tartalmazó objektum:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 Győződjön meg arról, hogy rendelkezik az Excel fájllal`book1.xls` a dokumentumok könyvtárában, vagy adja meg a megfelelő fájlnevet és helyet.

## 4. lépés: Példányosítson egy munkafüzet objektumot, és nyissa meg az Excel fájlt

 Használja a`Workbook`osztályt az Aspose.Cells-ből egy Workbook objektum példányosításához, és a megadott Excel-fájl megnyitásához a fájlfolyamon keresztül:

```csharp
Workbook excel = new Workbook(fstream);
```

## 5. lépés: Nyissa meg az első munkalapot

Keresse meg az Excel fájl első munkalapját:

```csharp
Worksheet worksheet = excel.Worksheets[0];
```

## 6. lépés: Állítsa be a munkalap-védelmi beállításokat

A Munkalap objektum tulajdonságai segítségével szükség szerint állítsa be a munkalap védelmi beállításokat. Például :

```csharp
worksheet.Protection.AllowDeletingColumn = false;
worksheet.Protection.AllowDeletingRow = false;
worksheet.Protection.AllowEditingContent = false;
worksheet.Protection.AllowEditingObject = false;
// ... Szükség szerint állítson be további védelmi beállításokat...
```

## 7. lépés: Mentse el a módosított Excel-fájlt

 Mentse el a módosított Excel fájlt a`Save` a munkafüzet objektum metódusa:

```csharp
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

Feltétlenül adja meg a kimeneti fájl kívánt elérési útját és fájlnevét.

## 8. lépés: Zárja be a fájlfolyamot

Mentés után zárja be a fájlfolyamot az összes kapcsolódó erőforrás felszabadításához:

```csharp
fstream.Close();
```
	
### Minta forráskód a Speciális védelmi beállításokhoz az Excel munkalaphoz az Aspose.Cells for .NET használatával 
```csharp
// dokumentumok könyvtárának elérési útja.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// A megnyitandó Excel fájlt tartalmazó fájlfolyam létrehozása
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Munkafüzet objektum példányosítása
// Az Excel fájl megnyitása a fájlfolyamon keresztül
Workbook excel = new Workbook(fstream);
// Az Excel fájl első munkalapjának elérése
Worksheet worksheet = excel.Worksheets[0];
// A felhasználók korlátozása a munkalap oszlopainak törlésére
worksheet.Protection.AllowDeletingColumn = false;
// A felhasználók korlátozása a munkalap egy sorának törlésére
worksheet.Protection.AllowDeletingRow = false;
// A felhasználók korlátozása a munkalap tartalmának szerkesztésében
worksheet.Protection.AllowEditingContent = false;
// A felhasználók korlátozása a munkalap objektumainak szerkesztésére
worksheet.Protection.AllowEditingObject = false;
// A felhasználók korlátozása a munkalap forgatókönyveinek szerkesztésére
worksheet.Protection.AllowEditingScenario = false;
// felhasználók szűrésének korlátozása
worksheet.Protection.AllowFiltering = false;
// Lehetővé teszi a felhasználók számára a munkalap celláinak formázását
worksheet.Protection.AllowFormattingCell = true;
// Lehetővé teszi a felhasználók számára a munkalap sorainak formázását
worksheet.Protection.AllowFormattingRow = true;
// Lehetővé teszi a felhasználók számára, hogy oszlopokat szúrjanak be a munkalapba
worksheet.Protection.AllowFormattingColumn = true;
// Lehetővé teszi a felhasználók számára, hogy hiperhivatkozásokat szúrjanak be a munkalapba
worksheet.Protection.AllowInsertingHyperlink = true;
// Lehetővé teszi a felhasználók számára, hogy sorokat szúrjanak be a munkalapba
worksheet.Protection.AllowInsertingRow = true;
// Lehetővé teszi a felhasználók számára, hogy kijelöljék a munkalap zárolt celláit
worksheet.Protection.AllowSelectingLockedCell = true;
// Lehetővé teszi a felhasználók számára, hogy kijelöljék a munkalap zárolatlan celláit
worksheet.Protection.AllowSelectingUnlockedCell = true;
// Lehetővé teszi a felhasználók számára a rendezést
worksheet.Protection.AllowSorting = true;
// Lehetővé teszi a felhasználók számára, hogy pivot táblákat használjanak a munkalapon
worksheet.Protection.AllowUsingPivotTable = true;
// A módosított Excel fájl mentése
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
// A fájlfolyam bezárása az összes erőforrás felszabadításához
fstream.Close();
```

## Következtetés

Gratulálok ! Most megtanulta, hogyan állíthat be speciális védelmi beállításokat egy Excel-táblázathoz az Aspose.Cells for .NET segítségével. Használja ezt a tudást Excel-fájlok védelmére és a felhasználói műveletek korlátozására.

### GYIK

#### K: Hogyan hozhatok létre új C# projektet az IDE-ben?

V: Az új C#-projekt létrehozásának lépései a használt IDE-től függően változhatnak. A részletes utasításokat az IDE dokumentációjában találja.

#### K: Lehetséges az oktatóanyagban említettektől eltérő egyéni védelmi beállítások megadása?

V: Igen, az Aspose.Cells a védelmi beállítások széles skáláját kínálja, amelyeket személyre szabhat saját igényei szerint. További részletekért tekintse meg az Aspose.Cells dokumentációját.

#### K: Milyen fájlformátumot használnak a módosított Excel-fájl mentésére a mintakódban?

V: A mintakódban a módosított Excel fájl Excel 97-2003 (.xls) formátumban kerül mentésre. Szükség esetén választhat más, az Aspose.Cells által támogatott formátumokat is.

#### K: Hogyan érhetek el más munkalapokat az Excel fájlban?

 V: Más munkalapokat index vagy lapnév használatával érhet el, például:`Worksheet worksheet = excel.Worksheets[1];` vagy`Worksheet worksheet = excel.Worksheets[" SheetName"];`.