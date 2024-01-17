---
title: Frissítse a Power Query képletelemet
linktitle: Frissítse a Power Query képletelemet
second_title: Aspose.Cells for .NET API Reference
description: Ismerje meg, hogyan frissítheti a Power Query képletelemeit Excel-fájlokban az Aspose.Cells for .NET használatával.
type: docs
weight: 160
url: /hu/net/excel-workbook/update-power-query-formula-item/
---
Power Query képletelemek frissítése gyakori művelet az Excel-fájlokban lévő adatok kezelésekor. Az Aspose.Cells for .NET segítségével egyszerűen frissítheti a Power Query képletelemeit az alábbi lépések végrehajtásával:

## 1. lépés: Adja meg a forrás- és kimeneti könyvtárakat

Először is meg kell adnia azt a forráskönyvtárat, amelyben a frissítendő Power Query képleteket tartalmazó Excel-fájl található, valamint azt a kimeneti könyvtárat, ahová a módosított fájlt menteni szeretné. A következőképpen teheti meg az Aspose.Cells használatával:

```csharp
// forráskönyvtár
string SourceDir = RunExamples.Get_SourceDirectory();

// Kimeneti könyvtár
string outputDir = RunExamples.Get_OutputDirectory();
```

## 2. lépés: Töltse be a forrás Excel-munkafüzetet

Ezután be kell töltenie azt a forrás Excel-munkafüzetet, amelyen frissíteni szeretné a Power Query képletelemet. Íme, hogyan kell csinálni:

```csharp
// Töltse be a forrás Excel-munkafüzetet
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
```

## 3. lépés: Tallózás és frissítés a Power Query képlet elemei között

munkafüzet betöltése után navigálhat a Power Query képletgyűjteményéhez, és böngészhet az egyes képletek és elemeik között. Ebben a példában a "Forrás" nevű képletelemet keressük, és frissítjük az értékét. Íme egy példakód egy Power Query képletelem frissítéséhez:

```csharp
// Hozzáférés a Power Query képletgyűjteményéhez
DataMashup mashupData = workbook.DataMashup;

// Lapozzon át a Power Query képleteken és elemeiken
foreach(PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
     foreach(PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
     {
         if (item.Name == "Source")
         {
             item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
         }
     }
}
```

## 4. lépés: Mentse el a kimeneti Excel-munkafüzetet

Miután frissítette a Power Query képletelemet, mentheti a módosított Excel-munkafüzetet a megadott kimeneti könyvtárba. Íme, hogyan kell csinálni:

```csharp
// Mentse el a kimeneti Excel-munkafüzetet
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.\r\n");
```

### Minta forráskód a Power Query képletelem frissítéséhez az Aspose.Cells for .NET használatával 
```csharp
// Munkakönyvtárak
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
DataMashup mashupData = workbook.DataMashup;
foreach (PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
	foreach (PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
	{
		if (item.Name == "Source")
		{
			item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
		}
	}
}
// Mentse el a kimeneti munkafüzetet.
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.");
```

## Következtetés

A Power Query képletelemeinek frissítése elengedhetetlen művelet az Aspose.Cells használatával az Excel-fájlok adatainak manipulálására és feldolgozására. A fenti lépések követésével könnyedén frissítheti a képletelemeket

### GYIK

#### K: Mi az a Power Query az Excelben?
     
V: A Power Query egy olyan szolgáltatás az Excelben, amely segít különböző forrásokból származó adatok összegyűjtésében, átalakításában és betöltésében. Hatékony eszközöket kínál az adatok megtisztításához, kombinálásához és átalakításához, mielőtt azokat Excelbe importálná.

#### K: Honnan tudhatom, hogy a Power Query képletelemek frissítése sikeres volt?
    A: After running the Power Query Formula Item Update, you can check if the operation was successful by viewing the output and ensuring that the output Excel file was created correctly.

#### K: Frissíthetek egyszerre több Power Query képletelemet?
    
V: Igen, a Power Query képletelem-gyűjteményét végigcsinálhatja, és egyetlen ciklusban frissíthet több elemet, egyedi igényeitől függően.

#### K: Vannak más műveletek, amelyeket az Aspose.Cells segítségével végrehajthatok a Power Query képletekkel?
    
V: Igen, az Aspose.Cells a szolgáltatások teljes skáláját kínálja a Power Query képletekkel való munkavégzéshez, beleértve a képletek létrehozását, törlését, másolását és keresését egy Excel-munkafüzetben.