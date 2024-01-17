---
title: Hivatkozástípusok észlelése
linktitle: Hivatkozástípusok észlelése
second_title: Aspose.Cells for .NET API Reference
description: Hivatkozástípusok észlelése egy Excel-munkafüzetben az Aspose.Cells for .NET segítségével.
type: docs
weight: 80
url: /hu/net/excel-workbook/detect-link-types/
---
Ebben az oktatóanyagban lépésről lépésre végigvezetjük a megadott C#-forráskódon, amely lehetővé teszi a hivatkozástípusok észlelését egy Excel-munkafüzetben az Aspose.Cells for .NET segítségével. A művelet végrehajtásához kövesse az alábbi lépéseket.

## 1. lépés: Állítsa be a forráskönyvtárat

```csharp
// forráskönyvtár
string SourceDir = RunExamples.Get_SourceDirectory();
```

Ebben az első lépésben meghatározzuk azt a forráskönyvtárat, ahol a hivatkozásokat tartalmazó Excel-munkafüzet található.

## 2. lépés: Töltse be az Excel-munkafüzetet

```csharp
// Töltse be az Excel munkafüzetet
Workbook workbook = new Workbook(SourceDir + "LinkTypes.xlsx");
```

Az Excel munkafüzetet a forrásfájl elérési útjával töltjük be.

## 3. lépés: Szerezze be a táblázatot

```csharp
// Az első munkalap beszerzése (alapértelmezett)
Worksheet worksheet = workbook.Worksheets[0];
```

 Megkapjuk a munkafüzet első munkalapját. Meg tudod változtatni a`[0]` indexet, hogy szükség esetén hozzáférjen egy adott munkalaphoz.

## 4. lépés: Hozzon létre egy cellatartományt

```csharp
// Hozzon létre egy A1:B3 cellatartományt
Range range = worksheet.Cells.CreateRange("A1", "A7");
```

Létrehozunk egy cellatartományt, ebben a példában az A1 cellától az A7 celláig. Szükség szerint módosíthatja a cellahivatkozásokat.

## 5. lépés: Helyezze a hiperhivatkozásokat hatótávolságba

```csharp
// Szerezze be a hiperhivatkozásokat a tartományban
Hyperlink[] hyperlinks = range.Hyperlinks;
```

A megadott tartományban lévő összes hiperhivatkozást megkapjuk.

## 6. lépés: Tallózás a hiperhivatkozások között és a hivatkozástípusok megtekintése

```csharp
foreach (Hyperlink link in hyperlinks)
{
Console.WriteLine(link.TextToDisplay + ": " + link.LinkType);
}
```

Végigfutunk minden hivatkozáson, és megjelenítjük a megjelenített szöveget és a kapcsolódó hivatkozástípust.

### Minta forráskód a hivatkozástípusok észleléséhez az Aspose.Cells for .NET használatával 
```csharp
//forráskönyvtár
string SourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(SourceDir + "LinkTypes.xlsx");
// Szerezd meg az első (alapértelmezett) munkalapot
Worksheet worksheet = workbook.Worksheets[0];
// Hozzon létre egy A2:B3 tartományt
Range range = worksheet.Cells.CreateRange("A1", "A7");
// A hiperhivatkozások hatótávolsága
Hyperlink[] hyperlinks = range.Hyperlinks;
foreach (Hyperlink link in hyperlinks)
{
	Console.WriteLine(link.TextToDisplay + ": " + link.LinkType);
}
Console.WriteLine("DetectLinkTypes executed successfully.");
```

## Következtetés

Gratulálok ! Megtanulta, hogyan észlelhet hivatkozástípusokat egy Excel-munkafüzetben az Aspose.Cells for .NET segítségével. Ez a funkció lehetővé teszi az Excel-munkafüzetekben található hivatkozások használatát. Folytassa az Aspose.Cells szolgáltatásainak felfedezésével Excel-munkafüzet-feldolgozási képességeinek bővítéséhez.

### GYIK

#### K: Hogyan telepíthetem az Aspose.Cells for .NET fájlt a projektembe?

 V: Az Aspose.Cells for .NET programot a NuGet csomagkezelővel telepítheti. Keressen rá[Aspose Releases](https://releases.aspose.com/cells/net) a NuGet Package Manager konzolban, és telepítse a legújabb verziót.

#### K: Érzékelhetek-e hivatkozástípusokat adott munkalapokon az első munkalap helyett?

 V: Igen, módosíthatja a`workbook.Worksheets[0]` indexet egy adott munkalap eléréséhez. Például a második lap eléréséhez használja a`workbook.Worksheets[1]`.

#### K: Lehetséges módosítani a tartományban észlelt hivatkozások típusát?

V: Igen, böngészhet a hiperhivatkozások között, és szerkesztési műveleteket végezhet, például frissítheti az URL-eket vagy eltávolíthatja a nem kívánt hivatkozásokat.

#### K: Milyen típusú hivatkozások lehetségesek az Aspose.Cells for .NET-ben?

V: A lehetséges hivatkozástípusok közé tartoznak a hiperhivatkozások, más munkalapokra mutató hivatkozások, külső fájlokra mutató hivatkozások, webhelyekre mutató hivatkozások stb.

#### K: Az Aspose.Cells for .NET támogatja az új hivatkozások létrehozását egy táblázatban?

 V: Igen, az Aspose.Cells for .NET támogatja az új hivatkozások létrehozását a`Hyperlink` osztályt és a hozzá tartozó tulajdonságokat. Hozzáadhat hiperhivatkozásokat, hivatkozásokat URL-ekre, hivatkozásokat más táblázatokra stb.

#### K: Használhatom az Aspose.Cells for .NET fájlt webes alkalmazásokban?

V: Igen, az Aspose.Cells for .NET használható webalkalmazásokban. Beágyazhatja az ASP.NET-be, az ASP.NET Core-ba és más .NET-alapú webes keretrendszerekbe.

#### K: Vannak-e fájlméret-korlátozások az Aspose.Cells for .NET használatakor?

V: Az Aspose.Cells for .NET külön korlátozás nélkül képes feldolgozni nagy Excel-munkafüzeteket. A tényleges fájlméretet azonban korlátozhatják a rendelkezésre álló rendszererőforrások.