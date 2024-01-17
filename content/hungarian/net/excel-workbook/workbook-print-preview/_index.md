---
title: Munkafüzet nyomtatási előnézete
linktitle: Munkafüzet nyomtatási előnézete
second_title: Aspose.Cells for .NET API Reference
description: Ismerje meg, hogyan hozhat létre egy munkafüzet nyomtatási előnézetét az Aspose.Cells for .NET használatával.
type: docs
weight: 170
url: /hu/net/excel-workbook/workbook-print-preview/
---
munkafüzet nyomtatási előnézete alapvető funkció az Excel-fájlok Aspose.Cells for .NET segítségével történő kezelésekor. Könnyen létrehozhat nyomtatási előnézetet az alábbi lépésekkel:

## 1. lépés: Adja meg a forráskönyvtárat

Először is meg kell adnia azt a forráskönyvtárat, amelyben az előnézetet megtekinteni kívánt Excel-fájl található. Íme, hogyan kell csinálni:

```csharp
// forráskönyvtár
string sourceDir = RunExamples.Get_SourceDirectory();
```

## 2. lépés: Töltse be a munkafüzetet

Ezután be kell töltenie a munkafüzet munkafüzetet a megadott Excel fájlból. Íme, hogyan kell csinálni:

```csharp
// Töltse be a munkafüzet munkafüzetet
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
```

## 3. lépés: Konfigurálja a kép- és nyomtatási beállításokat

A nyomtatási előnézet létrehozása előtt szükség szerint konfigurálhatja a képet és a nyomtatási beállításokat. Ebben a példában az alapértelmezett beállításokat használjuk. Íme, hogyan kell csinálni:

```csharp
// Kép és nyomtatási lehetőségek
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
```

## 4. lépés: A munkafüzet nyomtatási előnézetének létrehozása

Most létrehozhatja a munkafüzet munkafüzet nyomtatási előnézetét a WorkbookPrintingPreview osztály használatával. Íme, hogyan kell csinálni:

```csharp
// A munkafüzet nyomtatási előnézete
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
```

## 5. lépés: A munkalap nyomtatási előnézetének létrehozása

Ha egy adott munkalap nyomtatási előnézetét szeretné létrehozni, használhatja a SheetPrintingPreview osztályt. Íme egy példa:

```csharp
// A munkalap nyomtatási előnézete
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Number of worksheet pages: " + preview2.EvaluatedPageCount);
```

### Minta forráskód a munkafüzet nyomtatási előnézetéhez az Aspose.Cells for .NET használatával 
```csharp
//Forrás könyvtár
string sourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Worksheet page count: " + preview2.EvaluatedPageCount);
Console.WriteLine("PrintPreview executed successfully.");
```

## Következtetés

A munkafüzet nyomtatási előnézetének létrehozása az Aspose.Cells for .NET hatékony szolgáltatása. A fenti lépések követésével könnyedén megtekintheti az Excel-munkafüzet előnézetét, és információkat kaphat a nyomtatandó oldalak számáról.

### GYIK

#### K: Hogyan adhatok meg egy másik forráskönyvtárat a munkafüzetem betöltéséhez?
    
 V: Használhatja a`Set_SourceDirectory` módszerrel egy másik forráskönyvtárat adhat meg. Például:`RunExamples.Set_SourceDirectory("Path_to_the_source_directory")`.

#### K: Testreszabhatom a képet és a nyomtatási beállításokat a nyomtatási előnézet létrehozásakor?
    
 V: Igen, testreszabhatja a kép- és nyomtatási beállításokat a tulajdonságok módosításával`ImageOrPrintOptions` tárgy. Például beállíthatja a képfelbontást, a kimeneti fájl formátumát stb.

#### K: Lehetséges nyomtatási előnézetet létrehozni több munkalaphoz egy munkafüzetben?
    
V: Igen, ismételheti a munkafüzet különböző munkalapjait, és minden laphoz nyomtatási előnézetet hozhat létre a`SheetPrintingPreview` osztály.

#### K: Hogyan menthetem el a nyomtatási előnézetet képként vagy PDF-fájlként?
    
 V: Használhatja`ToImage` vagy`ToPdf` a metódusa`WorkbookPrintingPreview` vagy`SheetPrintingPreview` objektumot a nyomtatási előnézet képként vagy PDF-fájlként történő mentéséhez.

#### K: Mit tehetek az elkészített nyomtatási előnézettel?
    
V: Miután létrehozta a nyomtatási előnézetet, megtekintheti azt a képernyőn, elmentheti képként vagy PDF-fájlként, vagy felhasználhatja más műveletekhez, például e-mailben történő küldéshez vagy nyomtatáshoz.
	