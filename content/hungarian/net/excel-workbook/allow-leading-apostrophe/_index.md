---
title: Vezető aposztróf engedélyezése
linktitle: Vezető aposztróf engedélyezése
second_title: Aspose.Cells for .NET API Reference
description: A vezető aposztróf engedélyezése az Excel-munkafüzetekben az Aspose.Cells for .NET segítségével.
type: docs
weight: 60
url: /hu/net/excel-workbook/allow-leading-apostrophe/
---
Ebben a lépésenkénti oktatóanyagban elmagyarázzuk a mellékelt C# forráskódot, amely lehetővé teszi a vezető aposztróf használatát egy Excel-munkafüzetben az Aspose.Cells for .NET használatával. A művelet végrehajtásához kövesse az alábbi lépéseket.

## 1. lépés: Állítsa be a forrás- és kimeneti könyvtárakat

```csharp
// forráskönyvtár
string sourceDir = RunExamples.Get_SourceDirectory();
// Kimeneti könyvtár
string outputDir = RunExamples.Get_OutputDirectory();
```

Ebben az első lépésben meghatározzuk az Excel fájlok forrás- és kimeneti könyvtárát.

## 2. lépés: Példányosítson egy WorkbookDesigner objektumot

```csharp
// Példányosítson egy WorkbookDesigner objektumot
WorkbookDesigner designer = new WorkbookDesigner();
```

 Létrehozunk egy példányt a`WorkbookDesigner` osztály az Aspose.Cells-től.

## 3. lépés: Töltse be az Excel-munkafüzetet

```csharp
// Töltse be az Excel munkafüzetet
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
designer.Workbook = workbook;
```

A megadott fájlból betöltjük az Excel munkafüzetet, és letiltjuk a kezdeti aposztrófok szövegstílusra való automatikus konvertálását.

## 4. lépés: Állítsa be az adatforrást

```csharp
// Határozza meg a tervezői munkafüzet adatforrását
List<DataObject> list = new List<DataObject>
{
new DataObject
{
Id=1,
Name = "demo"
},
new DataObject
{
ID=2,
Name = "'demo"
}
};
designer.SetDataSource("sampleData", list);
```

 Meghatározzuk az adatobjektumok listáját, és használjuk a`SetDataSource` módszer a tervezői munkafüzet adatforrásának beállításához.

## 5. lépés: Az intelligens jelölők feldolgozása

```csharp
// Intelligens jelölők feldolgozása
designer. Process();
```

 Használjuk a`Process` módszer az intelligens jelölők feldolgozására a tervezői munkafüzetben.

## 6. lépés: Mentse el a módosított Excel-munkafüzetet

```csharp
// Mentse el a módosított Excel-munkafüzetet
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
```

A módosított Excel munkafüzetet a végrehajtott változtatásokkal elmentjük.

### Minta forráskód az Allow Leading Apostrophe használatához Aspose.Cells for .NET-hez 
```csharp
//Forrás könyvtár
string sourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
// WorkbookDesigner objektum példányosítása
WorkbookDesigner designer = new WorkbookDesigner();
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
// Nyisson meg egy tervezői táblázatot, amely intelligens jelölőket tartalmaz
designer.Workbook = workbook;
List<DataObject> list = new List<DataObject>
{
	new DataObject
	{
		 Id =1,
		 Name = "demo"
	},
	new DataObject
	{
		Id=2,
		Name = "'demo"
	}
};
// Állítsa be a tervezői táblázat adatforrását
designer.SetDataSource("sampleData", list);
// Az intelligens jelölők feldolgozása
designer.Process();
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
Console.WriteLine("AllowLeadingApostrophe executed successfully.");
```

## Következtetés

Gratulálok ! Megtanulta, hogyan engedélyezheti a vezető aposztróf használatát egy Excel-munkafüzetben az Aspose.Cells for .NET segítségével. Kísérletezzen saját adataival az Excel-munkafüzetek további testreszabásához.

### GYIK

#### K: Mi a vezető aposztróf engedély egy Excel-munkafüzetben?

V: Ha engedélyezi a kezdeti aposztrófot egy Excel-munkafüzetben, akkor az aposztrófral kezdődő adatok helyesen jelennek meg anélkül, hogy szövegstílusra konvertálnák azokat. Ez akkor hasznos, ha az aposztrófot az adatok részeként szeretné megtartani.

#### K: Miért kell kikapcsolnom a kezdeti aposztrófok automatikus konvertálását?

V: Ha letiltja a vezető idézetek automatikus konvertálását, megőrizheti használatukat az adataiban. Ezzel elkerülhető az adatok nem kívánt módosítása az Excel-munkafüzet megnyitása vagy kezelése közben.

#### K: Hogyan állíthat be adatforrást a tervezői munkafüzetben?

 V: A tervezői munkafüzet adatforrásának beállításához használhatja a`SetDataSource` metódus, amely megadja az adatforrás nevét és a megfelelő adatobjektumok listáját.

#### K: A vezető aposztróf engedélyezése hatással van az Excel-munkafüzet egyéb adataira?

V: Nem, a vezető aposztróf engedélyezése csak az aposztrófpal kezdődő adatokat érinti. Az Excel-munkafüzet egyéb adatai változatlanok maradnak.

#### K: Használhatom ezt a funkciót más Excel fájlformátumokkal?

V: Igen, ezt a funkciót használhatja az Aspose.Cells által támogatott más Excel-fájlformátumokkal is, például .xls, .xlsm stb.