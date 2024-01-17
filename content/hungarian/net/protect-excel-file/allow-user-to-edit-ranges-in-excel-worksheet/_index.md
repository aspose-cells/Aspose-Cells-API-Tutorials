---
title: Engedélyezze a felhasználónak a tartományok szerkesztését az Excel munkalapon
linktitle: Engedélyezze a felhasználónak a tartományok szerkesztését az Excel munkalapon
second_title: Aspose.Cells for .NET API Reference
description: Lehetővé teszi a felhasználók számára, hogy meghatározott tartományokat szerkesztsenek egy Excel-táblázatban az Aspose.Cells for .NET használatával. Lépésről lépésre útmutató forráskóddal C# nyelven.
type: docs
weight: 10
url: /hu/net/protect-excel-file/allow-user-to-edit-ranges-in-excel-worksheet/
---
Ebben az útmutatóban bemutatjuk, hogyan használhatja az Aspose.Cells for .NET fájlt, amellyel lehetővé teszi a felhasználó számára, hogy meghatározott tartományokat szerkeszthessen egy Excel-táblázatban. A feladat végrehajtásához kövesse az alábbi lépéseket.

## 1. lépés: A környezet beállítása

Győződjön meg arról, hogy beállította a fejlesztői környezetet, és telepítette az Aspose.Cells for .NET fájlt. A könyvtár legújabb verzióját letöltheti az Aspose hivatalos webhelyéről.

## 2. lépés: Importálja a szükséges névtereket

A C# projektben importálja a szükséges névtereket az Aspose.Cells használatához:

```csharp
using Aspose.Cells;
```

## 3. lépés: A dokumentumok könyvtár elérési útjának beállítása

 Nyilatkozni a`dataDir` változó megadja annak a könyvtárnak az elérési útját, ahová a generált Excel fájlt menteni szeretné:

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Feltétlenül cserélje ki`"YOUR_DOCUMENT_DIRECTORY"` a megfelelő elérési úttal a rendszeren.

## 4. lépés: Munkafüzet objektum létrehozása

Példányosítson egy új munkafüzet objektumot, amely a létrehozni kívánt Excel-munkafüzetet képviseli:

```csharp
Workbook book = new Workbook();
```

## 5. lépés: Hozzáférés az első munkalaphoz

Keresse meg az Excel-munkafüzet első munkalapját a következő kóddal:

```csharp
Worksheet sheet = book.Worksheets[0];
```

## 6. lépés: Az engedélyezett módosítási tartományok lekérése

 Szerezze be az engedélyezett szerkesztési tartományok gyűjteményét a`AllowEditRanges` ingatlan:

```csharp
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
```

## 7. lépés: Határozzon meg egy védett tartományt

 Határozzon meg egy védett tartományt a`Add` módszere a`AllowEditRanges` Gyűjtemény:

```csharp
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
protectedRange protectedRange = allowRanges[idx];
```

Itt létrehoztunk egy védett „r2” tartományt, amely az A1 cellától a C3 celláig terjed.

## 8. lépés: Adja meg a jelszót

 Adjon meg jelszót a védett tartományhoz a gombbal`Password` ingatlan:

```csharp
protectedRange.Password = "YOUR_PASSWORD";
```

 Feltétlenül cserélje ki`"YOUR_PASSWORD"` a kívánt jelszóval.

## 9. lépés: A munkalap védelme

 Védje meg a munkalapot a`Protect` módszere a`Worksheet` tárgy:

```csharp
sheet.Protect(ProtectionType.All);
```

Ez megvédi a táblázatot azáltal, hogy megakadályozza a megengedett tartományokon kívüli módosításokat.

## 10. lépés: Regisztrálja a

  Excel fájl

 Mentse el a generált Excel fájlt a`Save` módszere a`Workbook` tárgy:

```csharp
book.Save(dataDir + "protectedrange.out.xls");
```

Feltétlenül adja meg a kívánt fájlnevet és a megfelelő elérési utat.

### Minta forráskód a tartományok szerkesztésének engedélyezése a felhasználók számára Excel-munkalapon az Aspose.Cells for .NET használatával 
```csharp
// dokumentumok könyvtárának elérési útja.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Hozzon létre könyvtárat, ha még nincs jelen.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Példányosítson egy új munkafüzetet
Workbook book = new Workbook();
// Szerezd meg az első (alapértelmezett) munkalapot
Worksheet sheet = book.Worksheets[0];
// Szerkessze meg a Tartományok engedélyezése lehetőséget
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
// Define ProtectedRange
ProtectedRange proteced_range;
// Hozd létre a tartományt
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
proteced_range = allowRanges[idx];
// Adja meg a jelszót
proteced_range.Password = "123";
// Védje a lapot
sheet.Protect(ProtectionType.All);
// Mentse el az Excel fájlt
book.Save(dataDir + "protectedrange.out.xls");
```

## Következtetés

Most megtanulta, hogyan használhatja az Aspose.Cells for .NET fájlt, amellyel lehetővé teszi a felhasználó számára, hogy meghatározott tartományokat szerkeszthessen egy Excel-táblázatban. Nyugodtan fedezze fel az Aspose.Cells által kínált funkciókat, hogy megfeleljen egyedi igényeinek.


### GYIK

#### 1. Hogyan engedélyezhető a felhasználónak, hogy meghatározott tartományokat szerkeszthessen az Excel táblázatban?

 Használhatja a`ProtectedRangeCollection` osztályt a megengedett módosítási tartományok meghatározásához. Használja a`Add` módszerrel új védett tartományt hozhat létre a kívánt cellákkal.

#### 2. Beállíthatok jelszót az engedélyezett módosítási tartományokhoz?

 Igen, megadhat jelszót a`Password` tulajdona a`ProtectedRange` tárgy. Ez csak a jelszóval rendelkező felhasználók számára korlátozza a hozzáférést.

#### 3. Hogyan védhetem meg a táblázatot a megengedett tartományok beállítása után?

 Használja a`Protect` módszere a`Worksheet` objektumot a munkalap védelmére. Ez megakadályozza a megengedett tartományokon kívüli változtatásokat, és esetleg jelszót kér, ha adott.