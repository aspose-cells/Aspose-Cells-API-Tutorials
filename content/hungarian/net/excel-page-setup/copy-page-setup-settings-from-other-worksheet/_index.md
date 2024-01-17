---
title: Másolja az oldalbeállítási beállításokat egy másik munkalapról
linktitle: Másolja az oldalbeállítási beállításokat egy másik munkalapról
second_title: Aspose.Cells for .NET API Reference
description: Ismerje meg, hogyan másolhatja át az oldalkonfigurációs beállításokat egyik táblázatból a másikba az Aspose.Cells for .NET segítségével. Lépésről lépésre szóló útmutató a könyvtár használatának optimalizálásához.
type: docs
weight: 10
url: /hu/net/excel-page-setup/copy-page-setup-settings-from-other-worksheet/
---
Ebben a cikkben lépésről lépésre elmagyarázzuk a következő C#-forráskódot: Oldalkonfigurációs beállítások másolása egy másik táblázatból az Aspose.Cells for .NET segítségével. A művelet végrehajtásához a .NET Aspose.Cells könyvtárát fogjuk használni. Ha át szeretné másolni az oldalbeállítási beállításokat egyik munkalapról a másikra, kövesse az alábbi lépéseket.

## 1. lépés: A munkafüzet létrehozása
Az első lépés egy munkafüzet létrehozása. Esetünkben az Aspose.Cells könyvtár által biztosított Workbook osztályt fogjuk használni. Íme a kód a munkafüzet létrehozásához:

```csharp
Workbook wb = new Workbook();
```

## 2. lépés: Tesztmunkalapok hozzáadása
A munkafüzet elkészítése után tesztmunkalapokat kell hozzáadnunk. Ebben a példában két munkalapot adunk hozzá. Íme a kód két munkalap hozzáadásához:

```csharp
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
```

## 3. lépés: Hozzáférés a munkalapokhoz
Most, hogy hozzáadtuk a munkalapokat, el kell érnünk őket, hogy módosíthassuk a beállításaikat. A "TestSheet1" és a "TestSheet2" munkalapokat a nevükkel fogjuk elérni. Íme a kód a hozzáféréshez:

```csharp
Worksheet TestSheet1 = wb. Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb. Worksheets["TestSheet2"];
```

## 4. lépés: A papírméret beállítása
 Ebben a lépésben beállítjuk a "TestSheet1" munkalap papírméretét. Használjuk a`PageSetup.PaperSize` tulajdonság a papírméret beállításához. Például a papírméretet "PaperA3ExtraTransverse"-re állítjuk. Íme a kód ehhez:

```csharp
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
```

## 5. lépés: Oldalbeállítási beállítások másolása
Most átmásoljuk az oldal konfigurációs beállításait a "TestSheet1" munkalapról a "TestSheet2"-re. Használjuk a`PageSetup.Copy` módszer ennek a műveletnek a végrehajtására. Íme a kód ehhez:

```csharp
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
```

## 6. lépés: Papírméretek nyomtatása
 Az oldalbeállítási beállítások másolása után kinyomtatjuk a két munkalap papírméretét. Használni fogjuk`Console.WriteLine` a papírméretek megjelenítéséhez. Íme a kód ehhez:

```csharp
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
```

### Minta forráskód az oldalbeállítási beállítások másolása más munkalapról az Aspose.Cells for .NET használatával 
```csharp
//Munkafüzet létrehozása
Workbook wb = new Workbook();
//Adjon hozzá két teszt munkalapot
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
//Mindkét munkalap elérése TestSheet1 és TestSheet2 néven
Worksheet TestSheet1 = wb.Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb.Worksheets["TestSheet2"];
//Állítsa a TestSheet1 papírméretét PaperA3ExtraTransverse értékre
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
//Nyomtassa ki mindkét munkalap papírméretét
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
//Másolja a PageSetup-ot a TestSheet1-ből a TestSheet2-be
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
//Nyomtassa ki mindkét munkalap papírméretét
Console.WriteLine("After Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("After Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
Console.WriteLine("CopyPageSetupSettingsFromSourceWorksheetToDestinationWorksheet executed successfully.\r\n");
```

## Következtetés
Ebből a cikkből megtudtuk, hogyan másolhatja át az oldalkonfigurációs beállításokat egyik munkalapról a másikra az Aspose.Cells for .NET segítségével. A következő lépéseken mentünk keresztül: munkafüzet létrehozása, tesztmunkalapok hozzáadása, munkalapok elérése, papírméret beállítása, oldalbeállítási beállítások másolása, papírméretek nyomtatása. Mostantól ezt a tudást felhasználhatja az oldalkonfigurációs beállítások másolására saját projektjeibe.

### GYIK

#### K: Másolhatom az oldalkonfigurációs beállításokat a különböző munkafüzet-példányok között?

 V: Igen, átmásolhatja az oldalbeállítási beállításokat a különböző munkafüzet-példányok között a segítségével`PageSetup.Copy` Az Aspose.Cells könyvtár módszere.

#### K: Másolhatok más oldalbeállítási beállításokat, például tájolást vagy margókat?

 V: Igen, más oldalbeállítási beállításokat is másolhat a segítségével`PageSetup.Copy` módszer a megfelelő opciókkal. Például másolhatja a tájolást a használatával`CopyOptions.Orientation` és margók használatával`CopyOptions.Margins`.

#### K: Honnan tudhatom, hogy milyen lehetőségek állnak rendelkezésre a papírmérethez?

V: Az Aspose.Cells könyvtár API-referenciájában megtekintheti a papírmérethez rendelkezésre álló lehetőségeket. Van egy enum ún`PaperSizeType` amely felsorolja a különböző támogatott papírméreteket.

#### K: Hogyan tölthetem le az Aspose.Cells könyvtárat .NET-hez?

 V: Letöltheti az Aspose.Cells könyvtárat a .NET-hez innen[Aspose Releases](https://releases.aspose.com/cells/net). Vannak ingyenes próbaverziók, valamint fizetős licencek kereskedelmi használatra.

#### K: Az Aspose.Cells könyvtár támogat más programozási nyelveket?

V: Igen, az Aspose.Cells könyvtár több programozási nyelvet támogat, beleértve a C#-t, Java-t, Python-t és még sok mást.