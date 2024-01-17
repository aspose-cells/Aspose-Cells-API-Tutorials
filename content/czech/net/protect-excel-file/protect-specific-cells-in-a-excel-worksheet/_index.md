---
title: Chraňte konkrétní buňky v listu aplikace Excel
linktitle: Chraňte konkrétní buňky v listu aplikace Excel
second_title: Aspose.Cells for .NET API Reference
description: Naučte se, jak chránit konkrétní buňky v Excelu pomocí Aspose.Cells pro .NET. Výukový program krok za krokem v C#.
type: docs
weight: 70
url: /cs/net/protect-excel-file/protect-specific-cells-in-a-excel-worksheet/
---
V tomto tutoriálu se podíváme na zdrojový kód C#, který používá knihovnu Aspose.Cells k ochraně konkrétních buněk v excelové tabulce. Projdeme si každý krok kódu a vysvětlíme, jak to funguje. Pečlivě dodržujte pokyny, abyste dosáhli požadovaných výsledků.

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

V tomto kroku definujeme styl, který se použije na konkrétní buňky. Použijte následující kód:

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

## Krok 7: Uzamčení konkrétních buněk

V tomto kroku uzamkneme konkrétní buňky. Použijte následující kód:

```csharp
//Zamykání všech tří buněk... tj. A1, B1, C1.
style = sheet.Cells["A1"].GetStyle();
style. IsLocked = true;
sheet.Cells["A1"].SetStyle(style);

style = sheet.Cells["B1"].GetStyle();
style. IsLocked = true;
sheet.Cells["B1"].SetStyle(style);

style = sheet.Cells["C1"].GetStyle();
style. IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
```

## Krok 8: Ochrana listu

Nakonec list ochráníme, aby nedošlo k úpravě konkrétních buněk. Použijte následující kód:

```csharp
// Chraňte pracovní list.
sheet.Protect(ProtectionType.All);
```

## Krok 9: Uložení souboru Excel

Nyní uložíme upravený soubor Excel. Použijte následující kód:

```csharp
// Uložte soubor aplikace Excel.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Ujistěte se, že jste zadali správnou cestu k uložení upraveného souboru Excel.

### Ukázkový zdrojový kód pro Chránit specifické buňky v pracovním listu aplikace Excel pomocí Aspose.Cells pro .NET 
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
// Definujte objekt styleflag
StyleFlag styleflag;
// Projděte všechny sloupce v listu a odemkněte je.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    styleflag = new StyleFlag();
    styleflag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, styleflag);
}
// Zamkněte tři buňky...tj. A1, B1, C1.
style = sheet.Cells["A1"].GetStyle();
style.IsLocked = true;
sheet.Cells["A1"].SetStyle(style);
style = sheet.Cells["B1"].GetStyle();
style.IsLocked = true;
sheet.Cells["B1"].SetStyle(style);
style = sheet.Cells["C1"].GetStyle();
style.IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
// Nakonec nyní list chraňte.
sheet.Protect(ProtectionType.All);
// Uložte soubor aplikace Excel.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```


## Závěr

gratuluji! Nyní máte zdrojový kód C#, který vám umožňuje chránit konkrétní buňky v listu aplikace Excel pomocí knihovny Aspose.Cells pro .NET. Neváhejte a upravte kód tak, aby vyhovoval vašim konkrétním potřebám.

### Často kladené otázky (FAQ)

#### Funguje tento kód s nejnovějšími verzemi Excelu?

Ano, tento kód funguje s nejnovějšími verzemi Excelu, včetně souborů ve formátu Excel 2010 a vyšším.

#### Mohu chránit jiné buňky kromě A1, B1 a C1?

Ano, můžete upravit kód tak, aby zamykal další konkrétní buňky úpravou odkazů na buňky v odpovídajících řádcích kódu.

#### Jak mohu znovu odemknout uzamčené buňky?

 Můžeš použít`SetStyle` metoda s`IsLocked` nastaven na`false` k odemknutí buněk.

#### Mohu do sešitu přidat další listy?

 Ano, do sešitu můžete přidat další listy pomocí`Worksheets.Add()` opakujte kroky ochrany buněk pro každý list.

#### Jak mohu změnit formát uložení souboru Excel?

 Formát uložení můžete změnit pomocí`SaveFormat` například metoda s požadovaným formátem`SaveFormat.Xlsx` pro Excel 2007 a novější.