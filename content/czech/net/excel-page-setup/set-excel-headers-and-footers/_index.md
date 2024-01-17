---
title: Nastavit záhlaví a zápatí aplikace Excel
linktitle: Nastavit záhlaví a zápatí aplikace Excel
second_title: Aspose.Cells for .NET API Reference
description: Přečtěte si, jak nastavit záhlaví a zápatí v Excelu pomocí Aspose.Cells pro .NET.
type: docs
weight: 100
url: /cs/net/excel-page-setup/set-excel-headers-and-footers/
---

tomto tutoriálu vám krok za krokem ukážeme, jak nastavit záhlaví a zápatí v Excelu pomocí Aspose.Cells pro .NET. Pro ilustraci procesu použijeme zdrojový kód C#.

## Krok 1: Nastavení prostředí

Ujistěte se, že máte na svém počítači nainstalovaný Aspose.Cells for .NET. Vytvořte také nový projekt ve vámi preferovaném vývojovém prostředí.

## Krok 2: Importujte potřebné knihovny

Do souboru kódu importujte knihovny potřebné pro práci s Aspose.Cells. Zde je odpovídající kód:

```csharp
using Aspose.Cells;
```

## Krok 3: Nastavte Data Directory

Nastavte datový adresář, kam chcete uložit upravený soubor Excel. Použijte následující kód:

```csharp
string dataDir = "YOUR DATA DIRECTORY";
```

Nezapomeňte zadat úplnou cestu k adresáři.

## Krok 4: Vytvoření sešitu a listu

Vytvořte nový objekt Workbook a přejděte na první list v sešitu pomocí následujícího kódu:

```csharp
Workbook excel = new Workbook();
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
```

Tím vytvoříte prázdný sešit s listem a poskytnete přístup k objektu PageSetup tohoto listu.

## Krok 5: Nastavení záhlaví

 Nastavte záhlaví tabulky pomocí`SetHeader` metody objektu PageSetup. Zde je ukázkový kód:

```csharp
pageSetup.SetHeader(0, "&A");
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
```

Tím se nastaví název listu, aktuální datum a čas a název souboru v záhlaví.

## Krok 6: Definování zápatí

 Nastavte zápatí tabulky pomocí`SetFooter` metody objektu PageSetup. Zde je ukázkový kód:

```csharp
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
pageSetup.SetFooter(1, "&P");
pageSetup.SetFooter(2, "&N");
```

Tím se nastaví textový řetězec, aktuální číslo stránky a celkový počet stránek v zápatí.

## Krok 7: Uložení upraveného sešitu

Uložte upravený sešit pomocí následujícího kódu:

```csharp
excel.Save(dataDir + "OutputFileName.xls");
```

Tím se upravený sešit uloží do zadaného datového adresáře.

### Ukázkový zdrojový kód pro Set Excel Headers and Footer pomocí Aspose.Cells for .NET 
```csharp
//Cesta k adresáři dokumentů.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Vytvoření instance objektu sešitu
Workbook excel = new Workbook();
// Získání odkazu na PageSetup listu
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
// Nastavení názvu listu v levé části záhlaví
pageSetup.SetHeader(0, "&A");
//Nastavení aktuálního data a aktuálního času ve střední části záhlaví
// a změna písma záhlaví
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
// Nastavení aktuálního názvu souboru v pravé části záhlaví a změna
// písmo záhlaví
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
// Nastavení řetězce v levé části zápatí a změna písma
// části tohoto řetězce ("123")
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
// Nastavení aktuálního čísla stránky ve střední části zápatí
pageSetup.SetFooter(1, "&P");
// Nastavení počtu stránek v pravé části zápatí
pageSetup.SetFooter(2, "&N");
// Uložte sešit.
excel.Save(dataDir + "SetHeadersAndFooters_out.xls");
```


## Závěr

Nyní jste se naučili, jak nastavit záhlaví a zápatí v Excelu pomocí Aspose.Cells pro .NET. Tento kurz vás provede každým krokem procesu, od nastavení prostředí až po uložení upraveného sešitu. Neváhejte dále prozkoumat funkce Aspose.Cells, abyste mohli provádět další manipulace se svými soubory Excel.

### Často kladené otázky (FAQ)

#### 1. Jak mohu nainstalovat Aspose.Cells for .NET na svůj systém?
Chcete-li nainstalovat Aspose.Cells for .NET, musíte si stáhnout instalační balíček z oficiálních stránek Aspose a postupovat podle pokynů uvedených v dokumentaci.

#### 2. Funguje tato metoda se všemi verzemi aplikace Excel?
Ano, metoda nastavení záhlaví a zápatí pomocí Aspose.Cells for .NET funguje se všemi podporovanými verzemi Excelu.

#### 3. Mohu dále upravit záhlaví a zápatí?
Ano, Aspose.Cells nabízí širokou škálu funkcí pro přizpůsobení záhlaví a zápatí, včetně umístění textu, barvy, písma, čísel stránek a dalších.

#### 4. Jak mohu přidat dynamické informace do záhlaví a zápatí?
Pomocí speciálních proměnných a formátovacích kódů můžete do záhlaví a zápatí přidat dynamické informace, jako je aktuální datum, čas, název souboru, číslo stránky atd.

#### 5. Mohu odstranit záhlaví a zápatí po jejich nastavení?
 Ano, můžete odstranit záhlaví a zápatí pomocí`ClearHeaderFooter` metoda`PageSetup` objekt. Tím se obnoví výchozí záhlaví a zápatí.