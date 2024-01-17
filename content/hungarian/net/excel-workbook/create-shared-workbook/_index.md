---
title: Megosztott munkafüzet létrehozása
linktitle: Megosztott munkafüzet létrehozása
second_title: Aspose.Cells for .NET API Reference
description: Hozzon létre egy megosztott Excel-munkafüzetet az Aspose.Cells for .NET segítségével, hogy lehetővé tegye a párhuzamos adatkezelést.
type: docs
weight: 70
url: /hu/net/excel-workbook/create-shared-workbook/
---
Ebben az oktatóanyagban végigvezetjük a megadott C# forráskódon, amely lehetővé teszi megosztott munkafüzet létrehozását az Aspose.Cells for .NET használatával. A művelet végrehajtásához kövesse az alábbi lépéseket.

## 1. lépés: Állítsa be a kimeneti könyvtárat

```csharp
// Kimeneti könyvtár
string outputDir = RunExamples.Get_OutputDirectory();
```

Ebben az első lépésben meghatározzuk a kimeneti könyvtárat, ahová a megosztott munkafüzet mentésre kerül.

## 2. lépés: Hozzon létre egy munkafüzet-objektumot

```csharp
// Hozzon létre egy munkafüzet objektumot
Workbook wb = new Workbook();
```

Létrehozunk egy új munkafüzet objektumot, amely az Excel-munkafüzetünket fogja képviselni.

## 3. lépés: Engedélyezze a munkafüzet megosztását

```csharp
// Oszd meg a munkafüzetet
wb.Settings.Shared = true;
```

 A munkafüzet megosztási funkcióját a`Shared` a munkafüzet objektum tulajdonsága`true`.

## 4. lépés: Mentse el a megosztott munkafüzetet

```csharp
// Mentse el a megosztott munkafüzetet
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
```

A megosztott munkafüzetet a kimeneti fájl elérési útjának és nevének megadásával mentjük.

### Minta forráskód a Megosztott munkafüzet létrehozásához az Aspose.Cells segítségével .NET-hez 
```csharp
//Kimeneti könyvtár
string outputDir = RunExamples.Get_OutputDirectory();
//Munkafüzet objektum létrehozása
Workbook wb = new Workbook();
//Oszd meg a munkafüzetet
wb.Settings.Shared = true;
//Mentse el a megosztott munkafüzetet
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
Console.WriteLine("CreateSharedWorkbook executed successfully.\r\n");
```

## Következtetés

Gratulálok ! Megtanulta, hogyan hozhat létre megosztott munkafüzetet az Aspose.Cells for .NET használatával. A megosztott munkafüzetet több felhasználó is használhatja egyidejűleg az adatokon való együttműködéshez. Kísérletezzen saját adataival, és fedezze fel tovább az Aspose.Cells szolgáltatásait hatékony és személyre szabott Excel-munkafüzetek létrehozásához.

### GYIK

#### K: Mi az a megosztott munkafüzet?

V: A megosztott munkafüzet egy Excel-munkafüzet, amelyet több felhasználó is használhat egyidejűleg az adatokon való együttműködéshez. Minden felhasználó módosíthatja a munkafüzetet, a többi felhasználó pedig valós időben fogja látni a frissítéseket.

#### K: Hogyan lehet engedélyezni egy munkafüzet megosztását az Aspose.Cells for .NET-ben?

 V: A munkafüzet megosztásának engedélyezéséhez az Aspose.Cells for .NET-ben be kell állítania a`Shared` a munkafüzet objektum tulajdonsága`true`. Ez lehetővé teszi a felhasználók számára, hogy egyidejűleg dolgozzanak a munkafüzeten.

#### K: Korlátozhatom a felhasználói engedélyeket egy megosztott munkafüzetben?

V: Igen, az Excel biztonsági funkcióival korlátozhatja a felhasználói engedélyeket a megosztott munkafüzetekben. Minden egyes felhasználóhoz beállíthat konkrét engedélyeket, például szerkesztési, olvasási lehetőséget stb.

#### K: Hogyan oszthatom meg a munkafüzetet más felhasználókkal?

V: Miután létrehozta a megosztott munkafüzetet, megoszthatja azt más felhasználókkal az Excel-fájl elküldésével. Más felhasználók megnyithatják a fájlt, és egyidejűleg dolgozhatnak rajta.

#### K: Minden Excel-szolgáltatás támogatott a megosztott munkafüzetekben?

V: A legtöbb Excel-szolgáltatás támogatott a megosztott munkafüzetekben. Egyes speciális szolgáltatásoknak, például a makróknak és a bővítményeknek azonban korlátozásai lehetnek, ha megosztott munkafüzetben használják őket.