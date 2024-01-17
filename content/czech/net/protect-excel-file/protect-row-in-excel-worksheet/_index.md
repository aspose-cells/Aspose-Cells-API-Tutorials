---
title: Chránit řádek v listu aplikace Excel
linktitle: Chránit řádek v listu aplikace Excel
second_title: Aspose.Cells for .NET API Reference
description: V tomto tutoriálu zjistíte, jak chránit řádky tabulky Excel pomocí Aspose.Cells for .NET. Výukový program krok za krokem v C#.
type: docs
weight: 60
url: /cs/net/protect-excel-file/protect-row-in-excel-worksheet/
---
V tomto tutoriálu se podíváme na nějaký zdrojový kód C#, který používá knihovnu Aspose.Cells k ochraně řádků v tabulce Excel. Projdeme si každý krok kódu a vysvětlíme, jak to funguje. Pečlivě dodržujte pokyny, abyste dosáhli požadovaných výsledků.

## Krok 1: Předpoklady

Než začnete, ujistěte se, že jste nainstalovali knihovnu Aspose.Cells pro .NET. Můžete jej získat z oficiálních stránek Aspose. Také se ujistěte, že máte nejnovější verzi sady Visual Studio nebo jiného vývojového prostředí C#.

## Krok 2: Importujte požadované jmenné prostory

Abychom mohli používat knihovnu Aspose.Cells, musíme do našeho kódu importovat potřebné jmenné prostory. Přidejte následující řádky na začátek zdrojového souboru C#:

```csharp
using Aspose.Cells;
```

## Krok 3: Vytvoření excelového sešitu

V tomto kroku vytvoříme nový excelový sešit. K vytvoření sešitu aplikace Excel použijte následující kód:

```csharp
// Cesta k adresáři dokumentů.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Vytvořte nový sešit.
Workbook wb = new Workbook();
```

 Nezapomeňte vyměnit`"YOUR_DOCUMENTS_DIR"` s příslušnou cestou k adresáři vašich dokumentů.

## Krok 4: Vytvoření tabulky

Nyní, když jsme vytvořili sešit Excel, vytvořte list a získejte první list. Použijte následující kód:

```csharp
// Vytvořte objekt tabulky a získejte první list.
Worksheet sheet = wb.Worksheets[0];
```

## Krok 5: Definování stylu

V tomto kroku definujeme styl, který se použije na řádky tabulky. Použijte následující kód:

```csharp
// Definice objektu stylu.
Styling styling;
```

## Krok 6: Smyčkou odemkněte všechny sloupce

Nyní projdeme všechny sloupce v listu a odemkneme je. Použijte následující kód:

```csharp
// Projděte všechny sloupce v listu a odemkněte je.
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style);
}
```

## Krok 7: Uzamčení prvního řádku

V tomto kroku uzamkneme první řádek listu. Použijte následující kód:

```csharp
// Získejte styl prvního řádku.
style = sheet.Cells.Rows[0].Style;
// Zamkněte styl.
style. IsLocked = true;
// Použijte styl na první řádek.
sheet.Cells.ApplyRowStyle(0, style);
```

## Krok 8: Ochrana listu

Nyní, když jsme nastavili styly a zamkli řádky, pojďme chránit tabulku. Použijte následující kód:

```csharp
// Chraňte pracovní list.
sheet.Protect(ProtectionType.All);
```

## Krok 9: Uložení souboru Excel

Nakonec upravený soubor Excel uložíme. Použijte následující kód:

```csharp
// Uložte soubor aplikace Excel.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Ujistěte se, že jste zadali správnou cestu k uložení upraveného souboru Excel.

### Ukázkový zdrojový kód pro Protect Row In Excel Worksheet pomocí Aspose.Cells pro .NET 
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

gratuluji! Nyní máte zdrojový kód C#, který vám umožňuje chránit řádky v tabulce Excel pomocí knihovny Aspose.Cells pro .NET. Ujistěte se, že pečlivě dodržujete kroky a přizpůsobte kód svým konkrétním potřebám.

### Často kladené otázky (FAQ)

#### Funguje tento kód s nejnovějšími verzemi Excelu?

Ano, tento kód funguje s nejnovějšími verzemi Excelu, včetně souborů ve formátu Excel 2010 a vyšším.

#### Mohu chránit pouze určité řádky namísto všech řádků v listu?

Ano, kód můžete upravit tak, aby specifikoval konkrétní řádky, které chcete chránit. Podle toho budete muset upravit smyčku a indexy.

#### Jak mohu znovu odemknout zamčené linky?

 Můžete použít`IsLocked` metoda`Style` objekt, kterému chcete hodnotu nastavit`false` a odemknout řádky.

#### Je možné chránit více listů ve stejném sešitu aplikace Excel?

Ano, můžete opakovat kroky vytvoření listu, nastavení stylu a ochrany pro každý list v sešitu.

#### Jak mohu změnit heslo pro ochranu tabulky?

 Heslo můžete změnit pomocí`Protect` a zadáním nového hesla jako argumentu.