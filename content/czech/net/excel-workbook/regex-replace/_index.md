---
title: Nahradit regulární výraz
linktitle: Nahradit regulární výraz
second_title: Aspose.Cells for .NET API Reference
description: Naučte se, jak provést náhradu Regex v souborech Excel pomocí Aspose.Cells for .NET.
type: docs
weight: 140
url: /cs/net/excel-workbook/regex-replace/
---
Nahrazování textu na základě regulárních výrazů (Regex) je běžným úkolem při manipulaci s daty v souborech Excel. S Aspose.Cells for .NET můžete snadno provést nahrazení Regex pomocí následujících kroků:

## Krok 1: Zadejte zdrojový adresář a výstupní adresář

Nejprve musíte zadat zdrojový adresář, kde se nachází soubor Excel obsahující data, která mají být nahrazena, a také výstupní adresář, kam chcete upravený soubor uložit. Zde je návod, jak to udělat pomocí Aspose.Cells:

```csharp
// zdrojový adresář
string sourceDir = RunExamples.Get_SourceDirectory();

// Výstupní adresář
string outputDir = RunExamples.Get_OutputDirectory();
```

## Krok 2: Načtěte zdrojový soubor Excel

Dále musíte načíst zdrojový soubor Excel, na kterém chcete provést náhradu Regex. Jak na to:

```csharp
// Načtěte zdrojový soubor Excel
Workbook workbook = new Workbook(sourceDir + "SampleRegexReplace.xlsx");
```

## Krok 3: Proveďte výměnu Regex

Po nahrání souboru můžete nastavit možnosti nahrazení, včetně rozlišení velkých a malých písmen a přesné shody obsahu buněk. Zde je ukázkový kód pro provedení nahrazení Regex:

```csharp
// Nastavte možnosti výměny
ReplaceOptions replace = new ReplaceOptions();
replace.CaseSensitive = false;
replace.MatchEntireCellContents = false;

// Definujte, že vyhledávací klíč je regulární výraz
replace. RegexKey = true;

// Proveďte výměnu Regex
workbook. Replace("\\bKIM\\b", "^^^TIM^^^", replace);
```

## Krok 4: Uložte výstupní soubor Excel

Po dokončení nahrazení Regex můžete uložit upravený soubor Excel do určeného výstupního adresáře. Jak na to:

```csharp
// Uložte výstupní soubor aplikace Excel
workbook.Save(outputDir + "RegexReplace_out.xlsx");
Console.WriteLine("RegexReplace executed successfully.\r\n");
```

### Ukázkový zdrojový kód pro Regex Replace pomocí Aspose.Cells pro .NET 
```csharp
//Zdrojový adresář
string sourceDir = RunExamples.Get_SourceDirectory();
//Výstupní adresář
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "SampleRegexReplace.xlsx");
ReplaceOptions replace = new ReplaceOptions();
replace.CaseSensitive = false;
replace.MatchEntireCellContents = false;
// Nastavením na hodnotu true označíte, že hledaný klíč je regulární výraz
replace.RegexKey = true;
workbook.Replace("\\bKIM\\b", "^^^TIM^^^", replace);
workbook.Save(outputDir + "RegexReplace_out.xlsx");
Console.WriteLine("RegexReplace executed successfully.");
```

## Závěr

Nahrazení regulárního výrazu je výkonná technika pro dynamickou úpravu dat v souboru aplikace Excel. S Aspose.Cells for .NET můžete snadno provést náhradu Regex podle výše uvedených kroků. Experimentujte s vlastními regulárními výrazy a využijte flexibilitu, kterou nabízí Aspose.Cells.

### Nejčastější dotazy

#### Otázka: Co je náhrada Regex?
    
Odpověď: Nahrazení regulárního výrazu je technika používaná k nahrazení textových vzorů založených na regulárních výrazech v souboru aplikace Excel. To umožňuje rychlé a přesné změny dat.

#### Otázka: Rozlišují se při výměně Regex velká a malá písmena?
    
Odpověď: Ne, pomocí Aspose.Cells můžete určit, zda má nahrazení Regex rozlišovat malá a velká písmena nebo ne. Tuto funkci máte plně pod kontrolou.

#### Otázka: Jak mohu určit přesnou shodu obsahu buňky při nahrazení Regex?
    
Odpověď: Aspose.Cells vám umožňuje definovat, zda má náhrada Regex přesně odpovídat obsahu buňky nebo ne. Tuto možnost si můžete upravit podle svých potřeb.

#### Otázka: Mohu použít pokročilé regulární výrazy při nahrazení Regex za Aspose.Cells?
    
Odpověď: Ano, Aspose.Cells podporuje pokročilé regulární výrazy, které vám umožňují provádět složité a sofistikované náhrady v souborech aplikace Excel.

#### Otázka: Jak mohu zkontrolovat, zda byla výměna Regex úspěšná?
    
Odpověď: Po provedení nahrazení Regex můžete ověřit, zda byla operace úspěšná, zkontrolováním výstupu a zajištěním, že výstupní soubor Excel byl vytvořen správně.
	