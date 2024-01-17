---
title: Kép beszúrása a fejléc láblécébe
linktitle: Kép beszúrása a fejléc láblécébe
second_title: Aspose.Cells for .NET API Reference
description: Ismerje meg, hogyan illeszthet be képet egy Excel-dokumentum fejlécébe vagy láblécébe az Aspose.Cells for .NET segítségével. Lépésről lépésre útmutató forráskóddal C# nyelven.
type: docs
weight: 60
url: /hu/net/excel-page-setup/insert-image-in-header-footer/
---
A kép beszúrásának lehetősége egy Excel-dokumentum fejlécébe vagy láblécébe nagyon hasznos lehet a jelentések testreszabásához vagy vállalati logók hozzáadásához. Ebben a cikkben lépésről lépésre bemutatjuk, hogyan illeszthet be egy képet egy Excel-dokumentum fejlécébe vagy láblécébe az Aspose.Cells for .NET segítségével. Megtanulja, hogyan érheti el ezt a C# forráskód használatával.

## 1. lépés: A környezet beállítása

Mielőtt elkezdené, győződjön meg arról, hogy az Aspose.Cells for .NET telepítve van a gépén. Hozzon létre egy új projektet is a kívánt fejlesztői környezetben.

## 2. lépés: Importálja a szükséges könyvtárakat

A kódfájlban importálja az Aspose.Cells használatához szükséges könyvtárakat. Itt van a megfelelő kód:

```csharp
using Aspose.Cells;
```

## 3. lépés: Állítsa be a dokumentumkönyvtárat

Állítsa be azt a könyvtárat, ahol a dolgozni kívánt Excel-dokumentum található. Használja a következő kódot a könyvtár beállításához:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

Feltétlenül adja meg a teljes könyvtár elérési utat.

## 4. lépés: Munkafüzet objektum létrehozása

A munkafüzet objektum azt az Excel-dokumentumot jelöli, amellyel dolgozni fog. A következő kóddal hozhatja létre:

```csharp
Workbook workbook = new Workbook();
```

Ezzel egy új üres munkafüzet objektumot hoz létre.

## 5. lépés: A kép URL-jének tárolása

Határozza meg a fejlécbe vagy láblécbe beszúrni kívánt kép URL-jét vagy elérési útját. A kép URL-jének tárolásához használja a következő kódot:

```csharp
string logo_url = dataDir + "aspose-logo.jpg";
```

Győződjön meg arról, hogy a megadott elérési út helyes, és a kép létezik ezen a helyen.

## 6. lépés: Nyissa meg a képfájlt

A képfájl megnyitásához egy FileStream objektumot használunk, és kiolvassuk a bináris adatokat a képből. Itt van a megfelelő kód:

```csharp
FileStream inFile;
byte[] binaryData;

inFile = new System.IO.FileStream(logo_url, System.IO.FileMode.Open, System.IO.FileAccess.Read);
binaryData = new Byte[inFile.Length];
long bytesRead = inFile.Read(binaryData, 0, (int)inFile.Length);
```

Győződjön meg arról, hogy a kép elérési útja helyes, és rendelkezik-e a megfelelő jogosultságokkal a hozzáféréshez.

## 7. lépés: A PageSetup konfigurálása

A PageSetup objektum az Excel dokumentum oldalbeállításainak megadására szolgál, beleértve a fejlécet és a láblécet. Használja a következő kódot az első munkalap PageSetup objektumának lekéréséhez:

```csharp
PageSetup pageSetup = workbook. Worksheets

[0].PageSetup;
```

Ez lehetővé teszi a munkafüzet első munkalapjának oldalbeállításainak elérését.

## 8. lépés: A kép hozzáadása a fejléchez

A PageSetup objektum SetHeaderPicture() metódusával állítsa be a képet az oldalfejléc középső részébe. Itt van a megfelelő kód:

```csharp
pageSetup.SetHeaderPicture(1, binaryData);
```

Ez hozzáadja a megadott képet az oldal fejlécéhez.

## 9. lépés: Szkript hozzáadása a fejléchez

Ha szkriptet szeretne hozzáadni az oldal fejlécéhez, használja a PageSetup objektum SetHeader() metódusát. Itt van a megfelelő kód:

```csharp
pageSetup.SetHeader(1, "&G");
```

Ez hozzáadja a megadott szkriptet az oldal fejlécéhez. Ebben a példában az „&G” szkript megjeleníti az oldalszámot.

## 10. lépés: Adja hozzá a lap nevét a fejléchez

A lap nevének az oldalfejlécben való megjelenítéséhez használja újra a PageSetup objektum SetHeader() metódusát. Itt van a megfelelő kód:

```csharp
pageSetup.SetHeader(2, "&A");
```

Ezzel hozzáadja a munkalap nevét az oldal fejlécéhez. Az „&A” szkript a munkalap nevének megjelenítésére szolgál.

## 11. lépés: A munkafüzet mentése

A munkafüzet módosításainak mentéséhez használja a Munkafüzet objektum Save() metódusát. Itt van a megfelelő kód:

```csharp
workbook.Save(dataDir + "InsertImageInHeaderFooter_out.xls");
```

Ezzel elmenti a munkafüzetet a változtatásokkal a megadott könyvtárba.

## 12. lépés: A FileStream bezárása

A kép bináris adatainak kiolvasása után feltétlenül zárja be a FileStream-et az erőforrások felszabadításához. A FileStream bezárásához használja a következő kódot:

```csharp
inFile.Close();
```

Ügyeljen arra, hogy mindig zárja be a FileStreams alkalmazást, ha befejezte a használatukat.

### Minta forráskód az Insert Image In Header Footer funkcióhoz az Aspose.Cells for .NET használatával 
```csharp
// dokumentumok könyvtárának elérési útja.
string dataDir = "YOUR DOCUMENT DIRECTORY";
//Munkafüzet objektum létrehozása
Workbook workbook = new Workbook();
// Karakterlánc-változó létrehozása a logó/kép url-jének tárolására
string logo_url = dataDir + "aspose-logo.jpg";
// FileStream objektum deklarálása
FileStream inFile;
// Bájttömb deklarálása
byte[] binaryData;
// A FileStream objektum példányának létrehozása az embléma/kép megnyitásához az adatfolyamban
inFile = new System.IO.FileStream(logo_url, System.IO.FileMode.Open, System.IO.FileAccess.Read);
// A FileStream objektum méretének bájttömbjének példányosítása
binaryData = new Byte[inFile.Length];
// Beolvas egy bájtblokkot az adatfolyamból, és adatokat ír egy adott bájttömb pufferébe.
long bytesRead = inFile.Read(binaryData, 0, (int)inFile.Length);
// PageSetup objektum létrehozása a munkafüzet első munkalapjának oldalbeállításainak lekéréséhez
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// A logó/kép beállítása az oldal fejlécének középső részében
pageSetup.SetHeaderPicture(1, binaryData);
// A logó/kép szkriptjének beállítása
pageSetup.SetHeader(1, "&G");
// A munkalap nevének beállítása az oldal fejlécének jobb oldalán a szkripttel
pageSetup.SetHeader(2, "&A");
// A munkafüzet mentése
workbook.Save(dataDir + "InsertImageInHeaderFooter_out.xls");
//A FileStream objektum bezárása
inFile.Close();       
```
## Következtetés

Gratulálok ! Most már tudja, hogyan lehet képet beszúrni egy Excel-dokumentum fejlécébe vagy láblécébe az Aspose.Cells for .NET segítségével. Ez az oktatóanyag végigvezeti a folyamat minden lépésén, a környezet beállításától a módosított munkafüzet mentéséig. Nyugodtan kísérletezzen többet az Aspose.Cells szolgáltatásaival személyre szabott és professzionális Excel-dokumentumok létrehozásához.

### GYIK

#### 1. kérdés: Lehetséges több kép beszúrása egy Excel-dokumentum fejlécébe vagy láblécébe?

1. válasz: Igen, több képet is beszúrhat egy Excel-dokumentum fejlécébe vagy láblécébe a 8. és 9. lépés megismétlésével minden további képnél.

#### 2. kérdés: Milyen képformátumok támogatottak a fejlécbe vagy láblécbe történő beszúráshoz?
2. válasz: Az Aspose.Cells számos általános képformátumot támogat, például JPEG, PNG, GIF, BMP stb.

#### 3. kérdés: Tovább szabhatom a fejléc vagy lábléc megjelenését?

3. válasz: Igen, speciális szkriptek és kódok segítségével tovább formázhatja és testreszabhatja a fejléc vagy lábléc megjelenését. A testreszabási beállításokkal kapcsolatos további információkért tekintse meg az Aspose.Cells dokumentációját.

#### 4. kérdés: Az Aspose.Cells működik az Excel különböző verzióival?

4. válasz: Igen, az Aspose.Cells kompatibilis az Excel különböző verzióival, beleértve az Excel 2003, Excel 2007, Excel 2010, Excel 2013, Excel 2016 és Excel 2019 alkalmazásokat.

#### 5. kérdés: Lehetséges képeket beszúrni az Excel-dokumentum más részeibe, például cellákba vagy diagramokba?

5. válasz: Igen, az Aspose.Cells kiterjedt funkcionalitást biztosít képek beszúrására az Excel-dokumentum különböző részeibe, beleértve a cellákat, diagramokat és rajzobjektumokat.