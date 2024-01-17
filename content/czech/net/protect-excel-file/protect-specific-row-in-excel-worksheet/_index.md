---
title: Chránit konkrétní řádek v listu aplikace Excel
linktitle: Chránit konkrétní řádek v listu aplikace Excel
second_title: Aspose.Cells for .NET API Reference
description: Chraňte konkrétní řádek v aplikaci Excel pomocí Aspose.Cells pro .NET. Podrobný průvodce zabezpečením vašich důvěrných dat.
type: docs
weight: 90
url: /cs/net/protect-excel-file/protect-specific-row-in-excel-worksheet/
---
Ochrana důvěrných dat v tabulce Excel je nezbytná pro zajištění bezpečnosti informací. Aspose.Cells for .NET nabízí výkonné řešení pro ochranu konkrétních řádků v tabulce aplikace Excel. Tato příručka vás provede ochranou konkrétního řádku v listu aplikace Excel pomocí dodaného zdrojového kódu C#. Chcete-li nastavit ochranu řádků v souborech aplikace Excel, postupujte podle těchto jednoduchých kroků.

## Krok 1: Importujte požadované knihovny

Chcete-li začít, ujistěte se, že máte v systému nainstalovaný Aspose.Cells for .NET. Abyste mohli používat funkce Aspose.Cells, musíte do svého projektu v jazyce C# přidat příslušné odkazy. Zde je kód pro import požadovaných knihoven:

```csharp
// Přidejte potřebné reference
using Aspose.Cells;
```

## Krok 2: Vytvoření excelového sešitu a tabulky

Po importu požadovaných knihoven můžete vytvořit nový excelový sešit a nový list. Jak na to:

```csharp
//Cesta k adresáři dokumentů.
string dataDir = "YOUR DOCUMENTS DIRECTORY";

// Vytvořte adresář, pokud ještě neexistuje.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
     System.IO.Directory.CreateDirectory(dataDir);

// Vytvořte nový sešit.
Workbook wb = new Workbook();

// Vytvořte objekt tabulky a získejte první list.
Worksheet sheet = wb.Worksheets[0];
```

## Krok 3: Nastavení stylu a příznaku stylu

Nyní nastavíme styl buňky a příznak stylu, abychom odemkli všechny sloupce v listu. Zde je potřebný kód:

```csharp
// Nastavte objekt stylu.
Styling styling;

// Nastavte objekt styleflag.
StyleFlag flag;

// Projděte všechny sloupce v listu a odemkněte je.
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     flag = new StyleFlag();
     flag. Locked = true;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
```

## Krok 4: Chraňte konkrétní linku

Nyní budeme chránit konkrétní řádek v listu. Zamkneme první řadu, abychom zabránili jakékoli změně. Zde je postup:

```csharp
// Získejte styl prvního řádku.
style = sheet.Cells.Rows[0].Style;

// Zamknout to.
style. IsLocked = true;

//Vytvořte vlajku.
flag = new StyleFlag();

// Nastavte parametr zámku.
flag. Locked = true;

// Použijte styl na první řádek.
sheet.Cells.ApplyRowStyle(0, style, flag);
```

## Krok 5: Ochrana listu

Nakonec ochráníme celý excelový list, abychom zabránili neoprávněným úpravám. Zde je postup:

```csharp
// Chraňte pracovní list.
sheet.Protect(ProtectionType.All);
```

## Krok 6: Uložte chráněný soubor aplikace Excel

Jakmile dokončíte ochranu konkrétního řádku v listu aplikace Excel, můžete chráněný soubor aplikace Excel uložit do systému. Zde je postup:

```csharp
// Uložte soubor aplikace Excel.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Po provedení těchto kroků úspěšně ochráníte konkrétní řádek v tabulce Excel pomocí Aspose.Cells for .NET.

### Ukázkový zdrojový kód pro Protect Specific Row In Excel Worksheet pomocí Aspose.Cells pro .NET 
```csharp
//Cesta k adresáři dokumentů.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Vytvořte adresář, pokud ještě není přítomen.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Vytvořte nový sešit.
Workbook wb = new Workbook();
// Vytvořte objekt listu a získejte první list.
Worksheet sheet = wb.Worksheets[0];
// Definujte objekt stylu.
Style style;
// Definujte objekt styleflag.
StyleFlag flag;
// Projděte všechny sloupce v listu a odemkněte je.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    flag = new StyleFlag();
    flag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
// Získejte styl první řady.
style = sheet.Cells.Rows[0].Style;
// Zamknout to.
style.IsLocked = true;
//Vytvořte vlajku.
flag = new StyleFlag();
// Nastavte nastavení zámku.
flag.Locked = true;
// Použijte styl na první řádek.
sheet.Cells.ApplyRowStyle(0, style, flag);
// Chraňte list.
sheet.Protect(ProtectionType.All);
// Uložte soubor aplikace Excel.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## Závěr

Ochrana dat v souborech aplikace Excel je zásadní, aby se zabránilo neoprávněnému přístupu nebo nechtěným změnám. Pomocí knihovny Aspose.Cells pro .NET můžete snadno chránit konkrétní řádky v tabulce Excel pomocí dodaného zdrojového kódu C#. Chcete-li do souborů aplikace Excel přidat další vrstvu zabezpečení, postupujte podle tohoto podrobného průvodce.

### Nejčastější dotazy

#### Funguje konkrétní ochrana řádků ve všech verzích Excelu?

Ano, konkrétní ochrana řádků pomocí Aspose.Cells for .NET funguje ve všech podporovaných verzích Excelu.

#### Mohu chránit více konkrétních řádků v tabulce Excel?

Ano, pomocí podobných metod popsaných v této příručce můžete chránit více konkrétních řádků.

#### Jak mohu odemknout konkrétní řádek v tabulce Excel?

 Chcete-li odemknout konkrétní řádek, musíte odpovídajícím způsobem upravit zdrojový kód pomocí`IsLocked` metoda`Style` objekt.