---
title: Filtrovat definovaná jména při načítání sešitu
linktitle: Filtrovat definovaná jména při načítání sešitu
second_title: Aspose.Cells for .NET API Reference
description: Přečtěte si, jak filtrovat definované názvy při načítání sešitu aplikace Excel pomocí Aspose.Cells for .NET.
type: docs
weight: 100
url: /cs/net/excel-workbook/filter-defined-names-while-loading-workbook/
---
Při práci s excelovými sešity v .NET aplikaci je často nutné filtrovat data při zatížení. Aspose.Cells for .NET je výkonná knihovna pro snadnou manipulaci s excelovými sešity. V této příručce vám ukážeme, jak filtrovat názvy definované při načítání sešitu pomocí Aspose.Cells for .NET. Chcete-li dosáhnout požadovaných výsledků, postupujte podle těchto jednoduchých kroků:

## Krok 1: Zadejte možnosti načítání

Nejprve musíte určit možnosti načítání, abyste definovali chování sešitu. V našem případě chceme ignorovat názvy nastavené při načítání. Zde je návod, jak to udělat pomocí Aspose.Cells:

```csharp
// Určuje možnosti načítání
LoadOptions opts = new LoadOptions();

// Nenačítat definovaná jména
opts. LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
```

## Krok 2: Načtěte sešit

Jakmile jsou nakonfigurovány možnosti načítání, můžete načíst sešit aplikace Excel ze zdrojového souboru. Ujistěte se, že jste zadali správnou cestu k souboru. Zde je ukázkový kód:

```csharp
// Načtěte sešit
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
```

## Krok 3: Uložte filtrovaný sešit

Po načtení sešitu můžete provádět další operace nebo úpravy podle potřeby. Poté můžete filtrovaný sešit uložit do výstupního souboru. Zde je postup:

```csharp
// Uložte filtrovaný sešit aplikace Excel
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
```

### Ukázkový zdrojový kód pro filtrem definovaná jména při načítání sešitu pomocí Aspose.Cells pro .NET 
```csharp
//Zadejte možnosti zatížení
LoadOptions opts = new LoadOptions();
//Nechceme načítat definovaná jména
opts.LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
//Načtěte sešit
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
//Uložte výstupní soubor Excel, rozbije vzorec v C1
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
Console.WriteLine("FilterDefinedNamesWhileLoadingWorkbook executed successfully.");
```

## Závěr

Filtrování definovaných názvů při načítání sešitu aplikace Excel může být pro mnoho aplikací zásadní. Aspose.Cells for .NET tento úkol usnadňuje tím, že poskytuje flexibilní možnosti pro načítání a filtrování dat. Podle kroků v této příručce budete moci efektivně odfiltrovat definované názvy a dosáhnout požadovaných výsledků v sešitech aplikace Excel.


### Nejčastější dotazy

#### Otázka: Podporuje Aspose.Cells jiné programovací jazyky kromě C#?
    
Odpověď: Ano, Aspose.Cells je multiplatformní knihovna, která podporuje mnoho programovacích jazyků, jako je Java, Python, C++a mnoho dalších.

#### Otázka: Mohu filtrovat jiné typy dat při načítání sešitu pomocí Aspose.Cells?
    
Odpověď: Ano, Aspose.Cells nabízí řadu možností filtrování dat včetně vzorců, stylů, maker atd.

#### Otázka: Zachová Aspose.Cells formátování a vlastnosti původního sešitu?
    
Odpověď: Ano, Aspose.Cells zachovává formátování, styly, vzorce a další vlastnosti původního sešitu při práci se soubory Excel.