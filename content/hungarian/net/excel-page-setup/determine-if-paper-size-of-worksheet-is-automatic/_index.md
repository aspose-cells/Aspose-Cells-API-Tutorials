---
title: Határozza meg, hogy a munkalap papírmérete automatikus-e
linktitle: Határozza meg, hogy a munkalap papírmérete automatikus-e
second_title: Aspose.Cells for .NET API Reference
description: Az Aspose.Cells for .NET segítségével megtudhatja, hogyan állapíthatja meg, hogy egy táblázat papírmérete automatikus-e.
type: docs
weight: 20
url: /hu/net/excel-page-setup/determine-if-paper-size-of-worksheet-is-automatic/
---
Ebben a cikkben lépésről lépésre elmagyarázzuk a következő C#-forráskódot: Az Aspose.Cells for .NET segítségével határozza meg, hogy egy munkalap papírmérete automatikus-e. A művelet végrehajtásához a .NET Aspose.Cells könyvtárát fogjuk használni. Kövesse az alábbi lépéseket annak meghatározásához, hogy egy munkalap papírmérete automatikus-e.

## 1. lépés: Munkafüzetek betöltése
Az első lépés a munkafüzetek betöltése. Két munkafüzetünk lesz: az egyikben le van tiltva az automatikus papírméret, a másikban pedig engedélyezve van az automatikus papírméret. Íme a kód a munkafüzetek betöltéséhez:

```csharp
// forráskönyvtár
string sourceDir = "YOUR_SOURCE_DIR";
// Kimeneti könyvtár
string outputDir = "YOUR_OUTPUT_DIRECTORY";

// Töltse be az első munkafüzetet az automatikus papírméret letiltásával
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");

// Töltse be a második munkafüzetet az automatikus papírmérettel
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
```

## 2. lépés: Hozzáférés a táblázatokhoz
Most, hogy betöltöttük a munkafüzeteket, el kell érnünk a munkalapokat, hogy ellenőrizhessük az automatikus papírméretet. A két munkafüzet első munkalapjára lépünk. Íme a kód a hozzáféréshez:

```csharp
//Ugrás az első munkafüzet első munkalapjára
Worksheet ws11 = wb1.Worksheets[0];

// Ugrás a második munkafüzet első munkalapjára
Worksheet ws12 = wb2.Worksheets[0];
```

## 3. lépés: Ellenőrizze az automatikus papírméretet
 Ebben a lépésben ellenőrizzük, hogy a munkalap papírmérete automatikus-e. Használjuk a`PageSetup.IsAutomaticPaperSize` ingatlan, hogy megszerezze ezeket az információkat. Ezután megjelenítjük az eredményt. Íme a kód ehhez:

```csharp
// Jelenítse meg az első munkalap IsAutomaticPaperSize tulajdonságát az első munkafüzetben
Console.WriteLine("First worksheet in first workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);

// Jelenítse meg az első munkalap IsAutomaticPaperSize tulajdonságát a második munkafüzetben
Console.WriteLine("First worksheet of second workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);

```

### Minta forráskód annak meghatározásához, hogy a munkalap papírmérete automatikus-e az Aspose.Cells for .NET használatával 
```csharp
//Forrás könyvtár
string sourceDir = "YOUR_SOURCE_DIRECTORY";
//Kimeneti könyvtár
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//Töltse be az első munkafüzetet, amelynek automatikus papírmérete hamis
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");
//Töltse be a második munkafüzetet, amelynek automatikus papírmérete igaz
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
//Mindkét munkafüzet első munkalapjának elérése
Worksheet ws11 = wb1.Worksheets[0];
Worksheet ws12 = wb2.Worksheets[0];
//Nyomtassa ki mindkét munkalap PageSetup.IsAutomaticPaperSize tulajdonságát
Console.WriteLine("First Worksheet of First Workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);
Console.WriteLine("First Worksheet of Second Workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);
Console.WriteLine();
Console.WriteLine("DetermineIfPaperSizeOfWorksheetIsAutomatic executed successfully.\r\n");
```


## Következtetés
Ebből a cikkből megtudtuk, hogyan állapítható meg, hogy egy munkalap papírmérete automatikus-e az Aspose.Cells for .NET használatával. A következő lépéseket követtük: a munkafüzetek betöltése,

hozzáférés a táblázatokhoz és az automatikus papírméret-ellenőrzés. Mostantól ezt a tudást felhasználhatja annak meghatározására, hogy a táblázatok papírmérete automatikus-e.

### GYIK

#### K: Hogyan tölthetek be munkafüzeteket az Aspose.Cells for .NET segítségével?

V: A munkafüzeteket az Aspose.Cells könyvtár Workbook osztályával töltheti be. Használja a Workbook.Load metódust a munkafüzet fájlból való betöltéséhez.

#### K: Ellenőrizhetem az automatikus papírméretet más táblázatoknál?

V: Igen, bármely munkalaphoz ellenőrizheti az automatikus papírméretet a megfelelő munkalapobjektum PageSetup.IsAutomaticPaperSize tulajdonságának elérésével.

#### K: Hogyan módosíthatom a táblázatok automatikus papírméretét?

V: Egy munkalap automatikus papírméretének megváltoztatásához használja a PageSetup.IsAutomaticPaperSize tulajdonságot, és állítsa be a kívánt értékre (igaz vagy hamis).

#### K: Milyen egyéb szolgáltatásokat kínál az Aspose.Cells for .NET?

V: Az Aspose.Cells for .NET számos szolgáltatást kínál a táblázatokkal való munkavégzéshez, például munkafüzetek létrehozásához, módosításához és konvertálásához, valamint adatok, képletek és formázások kezeléséhez.