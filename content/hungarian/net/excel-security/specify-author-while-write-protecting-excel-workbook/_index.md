---
title: Írás közben adja meg a szerzőt Az Excel munkafüzet védelme
linktitle: Írás közben adja meg a szerzőt Az Excel munkafüzet védelme
second_title: Aspose.Cells for .NET API Reference
description: Ismerje meg, hogyan védheti meg és szabhatja testre Excel-munkafüzeteit az Aspose.Cells for .NET segítségével. Lépésről lépésre bemutató C# nyelven.
type: docs
weight: 30
url: /hu/net/excel-security/specify-author-while-write-protecting-excel-workbook/
---

Ebben az oktatóanyagban bemutatjuk, hogyan adhatja meg a szerzőt, amikor egy Excel-munkafüzet írásvédelmét használja az Aspose.Cells .NET könyvtár használatával.

## 1. lépés: A környezet előkészítése

Mielőtt elkezdené, győződjön meg arról, hogy az Aspose.Cells for .NET telepítve van a gépén. Töltse le a könyvtárat az Aspose hivatalos webhelyéről, és kövesse a mellékelt telepítési utasításokat.

## 2. lépés: A forrás- és kimeneti könyvtárak konfigurálása

 megadott forráskódban meg kell adnia a forrás- és kimeneti könyvtárat. Módosítsa a`sourceDir` és`outputDir` változókat úgy, hogy a "FORRÁS KÖNYVTÁRA" és a "KIMENETI KÖNYVTÁR" helyére cseréli a megfelelő abszolút elérési utat a gépén.

```csharp
// Forrás könyvtár
string sourceDir = "PATH TO YOUR SOURCE DIRECTORY";

// Kimeneti könyvtár
string outputDir = "YOUR OUTPUT DIRECTORY PATH";
```

## 3. lépés: Hozzon létre egy üres Excel-munkafüzetet

Kezdésként létrehozunk egy munkafüzet objektumot, amely egy üres Excel-munkafüzetet képvisel.

```csharp
// Üres munkafüzet létrehozása.
Workbook wb = new Workbook();
```

## 4. lépés: Írásvédelem jelszóval

 Ezután jelszót adunk meg az Excel munkafüzet írásvédelméhez a`WriteProtection.Password` a munkafüzet objektum tulajdonsága.

```csharp
// Írásvédelmi munkafüzet jelszóval.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";
```

## 5. lépés: A szerző specifikációja

 Most megadjuk az Excel munkafüzet szerzőjét a`WriteProtection.Author` a munkafüzet objektum tulajdonsága.

```csharp
// Írásvédelmi munkafüzet közben adja meg a szerzőt.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";
```

## 6. lépés: Védett Excel-munkafüzet biztonsági mentése

 Az írásvédelem és a szerző megadása után az Excel-munkafüzetet XLSX formátumban menthetjük el a`Save()` módszer.

```csharp
// Mentse el a munkafüzetet XLSX formátumban.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");
```

### Minta forráskód a Szerző megadása írás közbeni védelem Excel munkafüzethez az Aspose.Cells for .NET használatával 
```csharp
//Forrás könyvtár
string sourceDir = "YOUR SOURCE DIRECTORY";

//Kimeneti könyvtár
string outputDir = "YOUR OUTPUT DIRECTORY";

// Üres munkafüzet létrehozása.
Workbook wb = new Workbook();

// Írásvédelmi munkafüzet jelszóval.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";

// Írásvédelmi munkafüzet közben adja meg a szerzőt.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";

// Mentse el a munkafüzetet XLSX formátumban.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");

```

## Következtetés

Gratulálok ! Most megtanulta, hogyan kell megadni a szerzőt Excel-munkafüzet írásvédelméhez az Aspose.Cells for .NET segítségével. Ezeket a lépéseket saját projektjeire is alkalmazhatja az Excel-munkafüzetek védelmére és testreszabására.

Nyugodtan fedezze fel az Aspose.Cells for .NET szolgáltatásait az Excel-fájlok fejlettebb műveleteihez.

## GYIK

#### K: Írhatok-e védett Excel-munkafüzetet jelszó megadása nélkül?

 V: Igen, használhatja a munkafüzet objektumot`WriteProtect()` módszert jelszó megadása nélkül az Excel-munkafüzet írásvédelméhez. Ez jelszó megadása nélkül korlátozza a munkafüzet módosításait.

#### K: Hogyan távolíthatom el az írásvédelmet egy Excel-munkafüzetből?

 V: Az írásvédelem eltávolításához egy Excel-munkafüzetből használhatja a`Unprotect()` metódusa a Munkalap objektum vagy a`RemoveWriteProtection()` a munkafüzet objektum metódusát, az adott használati esettől függően. .

#### K: Elfelejtettem a jelszót az Excel-munkafüzet védelmére. Mit tehetek ?

V: Ha elfelejtette az Excel-munkafüzet védelmét szolgáló jelszót, nem távolíthatja el közvetlenül. Megpróbálhat azonban olyan speciális, harmadik féltől származó eszközöket használni, amelyek jelszó-helyreállítási funkciókat biztosítanak a védett Excel-fájlokhoz.

#### K: Lehetséges több szerzőt megadni egy Excel-munkafüzet írásvédelmében?

V: Nem, az Aspose.Cells for .NET könyvtár lehetővé teszi egyetlen szerző megadását az Excel-munkafüzet írásvédelméhez. Ha több szerzőt szeretne megadni, akkor egyéni megoldásokat kell mérlegelnie az Excel-fájl közvetlen manipulálásával.