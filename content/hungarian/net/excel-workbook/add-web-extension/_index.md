---
title: Webbővítmény hozzáadása
linktitle: Webbővítmény hozzáadása
second_title: Aspose.Cells for .NET API Reference
description: Könnyen hozzáadhat webbővítményt Excel-munkafüzeteihez az Aspose.Cells for .NET segítségével.
type: docs
weight: 40
url: /hu/net/excel-workbook/add-web-extension/
---
Ebben a lépésről lépésre bemutatott oktatóanyagban elmagyarázzuk azt a C# forráskódot, amely lehetővé teszi webbővítmény hozzáadását az Aspose.Cells for .NET használatával. Kövesse az alábbi lépéseket webbővítmény hozzáadásához az Excel-munkafüzethez.

## 1. lépés: Állítsa be a kimeneti könyvtárat

```csharp
// Kimeneti könyvtár
string outDir = RunExamples.Get_OutputDirectory();
```

Ebben az első lépésben meghatározzuk azt a kimeneti könyvtárat, ahová a módosított Excel-munkafüzet mentésre kerül.

## 2. lépés: Hozzon létre egy új munkafüzetet

```csharp
// Hozzon létre egy új munkafüzetet
Workbook workbook = new Workbook();
```

Itt egy új Excel-munkafüzetet készítünk a`Workbook` osztály az Aspose.Cells-től.

## 3. lépés: Nyissa meg a webbővítmények gyűjteményét

```csharp
// Hozzáférés a webbővítmények gyűjteményéhez
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
```

 Az Excel munkafüzet webbővítménygyűjteményét a`WebExtensions` tulajdona a`Worksheets` tárgy.

## 4. lépés: Új webbővítmény hozzáadása

```csharp
// Új webbővítmény hozzáadása
int extensionIndex = extensions.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
```

Új webbővítményt adunk a bővítménygyűjteményhez. Meghatározzuk a kiterjesztés hivatkozási azonosítóját, az áruház nevét és az áruház típusát.

## 5. lépés: Nyissa meg a webbővítmény munkaablak gyűjteményét

```csharp
// Nyissa meg a webbővítmény munkaablak-gyűjteményét
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
```

 Az Excel munkafüzet webbővítmény munkaablak-gyűjteményét a következővel érhetjük el`WebExtensionTaskPanes` tulajdona a`Worksheets` tárgy.

## 6. lépés: Új munkaablak hozzáadása

```csharp
// Új munkaablak hozzáadása
int taskPaneIndex = taskPanes.Add();
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane. IsVisible = true;
taskPane. DockState = "right";
taskPane. WebExtension = extension;
```

Új munkaablakot adunk a munkaablak-gyűjteményhez. Beállítjuk a panel láthatóságát, dokkolási állapotát és a kapcsolódó webbővítményt.

## 7. lépés: Mentse el és zárja be a munkafüzetet

```csharp
// Mentse és zárja be a munkafüzetet
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

A módosított munkafüzetet elmentjük a megadott kimeneti könyvtárba, majd bezárjuk.

### Minta forráskód az Add Web Extensionhez az Aspose.Cells for .NET használatával 
```csharp
//Forrás könyvtár
string outDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook();
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
int extensionIndex = extensions.Add();
int taskPaneIndex = taskPanes.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane.IsVisible = true;
taskPane.DockState = "right";
taskPane.WebExtension = extension;
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

## Következtetés

Gratulálok ! Most megtanulta, hogyan adhat hozzá webbővítményt az Aspose.Cells for .NET használatával. Kísérletezzen a kóddal, és fedezze fel az Aspose.Cells további funkcióit, hogy a legtöbbet hozza ki az Excel-munkafüzetek webbővítményeinek kezeléséből.

## GYIK

#### K: Mi az a webbővítmény egy Excel-munkafüzetben?

V: Az Excel-munkafüzet webbővítménye egy olyan összetevő, amely webalkalmazások integrálásával lehetővé teszi további funkciók hozzáadását az Excelhez. Interaktív funkciókat, egyéni irányítópultokat, külső integrációkat és egyebeket kínálhat.

#### K: Hogyan adhatunk webbővítményt az Excel-munkafüzethez az Aspose.Cells segítségével?

 V: Ha webbővítményt szeretne hozzáadni egy Excel-munkafüzethez az Aspose.Cells segítségével, kövesse a lépésről lépésre található útmutatónkban található lépéseket. Használja a`WebExtensionCollection` és`WebExtensionTaskPaneCollection` osztályokat a webbővítmény és a kapcsolódó munkaablak hozzáadásához és konfigurálásához.

#### K: Milyen adatok szükségesek a webbővítmény hozzáadásához?

V: Webbővítmény hozzáadásakor meg kell adnia a bővítmény SKU-azonosítóját, az üzlet nevét és az üzlet típusát. Ez az információ segít a bővítmény azonosításában és helyes betöltésében.

#### K: Hozzáadhatok több webbővítményt egyetlen Excel-munkafüzethez?

 V: Igen, több webbővítményt is hozzáadhat egyetlen Excel-munkafüzethez. Használja a`Add` a webbővítmények gyűjteményének módszerét az egyes bővítmények hozzáadásához, majd társítsa őket a megfelelő munkaablakokhoz.