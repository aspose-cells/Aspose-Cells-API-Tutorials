---
title: Povolit uživateli upravovat rozsahy v listu aplikace Excel
linktitle: Povolit uživateli upravovat rozsahy v listu aplikace Excel
second_title: Aspose.Cells for .NET API Reference
description: Umožněte uživatelům upravovat konkrétní rozsahy v tabulce Excel pomocí Aspose.Cells for .NET. Průvodce krok za krokem se zdrojovým kódem v C#.
type: docs
weight: 10
url: /cs/net/protect-excel-file/allow-user-to-edit-ranges-in-excel-worksheet/
---
V této příručce vás provedeme tím, jak používat Aspose.Cells pro .NET, aby uživatel mohl upravovat konkrétní rozsahy v tabulce aplikace Excel. Chcete-li provést tento úkol, postupujte podle následujících kroků.

## Krok 1: Nastavení prostředí

Ujistěte se, že jste nastavili vývojové prostředí a nainstalovali Aspose.Cells for .NET. Nejnovější verzi knihovny si můžete stáhnout z oficiálních stránek Aspose.

## Krok 2: Importujte požadované jmenné prostory

Ve svém projektu C# importujte potřebné jmenné prostory pro práci s Aspose.Cells:

```csharp
using Aspose.Cells;
```

## Krok 3: Nastavení cesty k adresáři dokumentů

 Prohlásit a`dataDir` proměnnou zadejte cestu k adresáři, kam chcete uložit vygenerovaný soubor Excel:

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Nezapomeňte vyměnit`"YOUR_DOCUMENT_DIRECTORY"` se správnou cestou ve vašem systému.

## Krok 4: Vytvoření objektu sešitu

Vytvořte instanci nového objektu Workbook, který představuje sešit Excel, který chcete vytvořit:

```csharp
Workbook book = new Workbook();
```

## Krok 5: Přístup k prvnímu listu

Přejděte na první list v sešitu aplikace Excel pomocí následujícího kódu:

```csharp
Worksheet sheet = book.Worksheets[0];
```

## Krok 6: Načtení povolených rozsahů úprav

 Získejte kolekci povolených rozsahů úprav pomocí`AllowEditRanges` vlastnictví:

```csharp
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
```

## Krok 7: Definujte chráněný rozsah

 Definujte chráněný rozsah pomocí`Add` metoda`AllowEditRanges` sbírka:

```csharp
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
protectedRange protectedRange = allowRanges[idx];
```

Zde jsme vytvořili chráněný rozsah "r2", který sahá od buňky A1 do buňky C3.

## Krok 8: Zadání hesla

 Zadejte heslo pro chráněný rozsah pomocí`Password` vlastnictví:

```csharp
protectedRange.Password = "YOUR_PASSWORD";
```

 Nezapomeňte vyměnit`"YOUR_PASSWORD"` s požadovaným heslem.

## Krok 9: Ochrana listu

 Chraňte pracovní list pomocí`Protect` metoda`Worksheet` objekt:

```csharp
sheet.Protect(ProtectionType.All);
```

To ochrání tabulku tím, že zabrání jakýmkoli úpravám mimo povolené rozsahy.

## Krok 10: Registrace

  Excel soubor

 Uložte vygenerovaný soubor Excel pomocí`Save` metoda`Workbook` objekt:

```csharp
book.Save(dataDir + "protectedrange.out.xls");
```

Nezapomeňte zadat požadovaný název souboru a správnou cestu.

### Ukázkový zdrojový kód pro Povolit uživateli upravovat rozsahy v listu Excel pomocí Aspose.Cells for .NET 
```csharp
//Cesta k adresáři dokumentů.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Vytvořte adresář, pokud ještě není přítomen.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Vytvořte nový sešit
Workbook book = new Workbook();
// Získejte první (výchozí) list
Worksheet sheet = book.Worksheets[0];
// Získejte možnosti Povolit úpravy rozsahů
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
// Definujte ProtectedRange
ProtectedRange proteced_range;
// Vytvořte rozsah
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
proteced_range = allowRanges[idx];
// Zadejte heslo
proteced_range.Password = "123";
// Chraňte list
sheet.Protect(ProtectionType.All);
// Uložte soubor aplikace Excel
book.Save(dataDir + "protectedrange.out.xls");
```

## Závěr

Nyní jste se naučili, jak používat Aspose.Cells pro .NET, abyste umožnili uživateli upravovat konkrétní rozsahy v tabulce Excel. Neváhejte dále prozkoumat funkce nabízené Aspose.Cells, abyste splnili své specifické potřeby.


### Nejčastější dotazy

#### 1. Jak umožnit uživateli upravovat konkrétní rozsahy v tabulce Excel?

 Můžete použít`ProtectedRangeCollection` třídy k definování povolených rozsahů úprav. Použijte`Add` způsob vytvoření nového chráněného rozsahu s požadovanými buňkami.

#### 2. Mohu nastavit heslo pro autorizované rozsahy úprav?

 Ano, můžete zadat heslo pomocí`Password` vlastnictvím`ProtectedRange` objekt. To omezí přístup pouze uživatelům s heslem.

#### 3. Jak mohu chránit tabulku, jakmile jsou nastaveny povolené rozsahy?

 Použijte`Protect` metoda`Worksheet` objekt k ochraně listu. Tím zabráníte jakýmkoli změnám mimo povolené rozsahy a případně budete vyzváni k zadání hesla, pokud jste nějaké zadali.