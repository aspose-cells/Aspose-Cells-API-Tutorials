---
title: Sdílený sešit chránit nebo zrušit ochranu heslem
linktitle: Sdílený sešit chránit nebo zrušit ochranu heslem
second_title: Aspose.Cells for .NET API Reference
description: Zjistěte, jak pomocí Aspose.Cells for .NET chránit heslem nebo zrušit ochranu sdíleného sešitu.
type: docs
weight: 120
url: /cs/net/excel-workbook/password-protect-or-unprotect-shared-workbook/
---
Ochrana sdíleného sešitu heslem je důležitá pro zajištění ochrany osobních údajů. S Aspose.Cells for .NET můžete snadno chránit nebo zrušit ochranu sdíleného sešitu pomocí hesel. Chcete-li získat požadované výsledky, postupujte podle následujících kroků:

## Krok 1: Zadejte výstupní adresář

Nejprve musíte určit výstupní adresář, kam bude chráněný soubor Excel uložen. Zde je návod, jak to udělat pomocí Aspose.Cells:

```csharp
// Výstupní adresář
string outputDir = RunExamples.Get_OutputDirectory();
```

## Krok 2: Vytvořte prázdný soubor Excel

Poté můžete vytvořit prázdný soubor aplikace Excel, na který chcete použít ochranu nebo zrušit ochranu. Zde je ukázkový kód:

```csharp
// Vytvořte prázdný sešit aplikace Excel
Workbook wb = new Workbook();
```

## Krok 3: Chraňte nebo zrušte ochranu sdíleného sešitu

Po vytvoření sešitu můžete chránit nebo zrušit ochranu sdíleného sešitu zadáním příslušného hesla. Zde je postup:

```csharp
// Chraňte sdílený sešit heslem
wb.ProtectSharedWorkbook("1234");

// Odkomentujte tento řádek, chcete-li odemknout sdílený sešit
// wb.UnprotectSharedWorkbook("1234");
```

## Krok 4: Uložte výstupní soubor Excel

Jakmile použijete ochranu nebo zrušení ochrany, můžete uložit chráněný soubor aplikace Excel do určeného výstupního adresáře. Jak na to:

```csharp
// Uložte výstupní soubor aplikace Excel
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

### Ukázkový zdrojový kód pro Password Protect or Unprotect Shared Workbook pomocí Aspose.Cells for .NET 
```csharp
//Výstupní adresář
string outputDir = RunExamples.Get_OutputDirectory();
//Vytvořte prázdný soubor Excel
Workbook wb = new Workbook();
//Chraňte sdílený sešit heslem
wb.ProtectSharedWorkbook("1234");
//Chcete-li zrušit ochranu sdíleného sešitu, odkomentujte tento řádek
//wb.UnprotectSharedWorkbook("1234");
//Uložte výstupní soubor aplikace Excel
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

## Závěr

Ochrana nebo zrušení ochrany sdíleného sešitu heslem je zásadní pro zajištění bezpečnosti dat. S Aspose.Cells for .NET můžete snadno přidat tuto funkci do svých souborů aplikace Excel. Podle kroků v této příručce můžete efektivně chránit nebo zrušit ochranu svých sdílených sešitů pomocí hesel. Experimentujte se svými vlastními soubory Excel a ujistěte se, že zachováte bezpečnost svých citlivých dat.

### Nejčastější dotazy

#### Otázka: Jaké typy ochrany mohu použít na sešit sdílený s Aspose.Cells?
    
Odpověď: Pomocí Aspose.Cells můžete chránit sdílený sešit zadáním hesla, které zabrání neoprávněnému přístupu, úpravám nebo vymazání dat.

#### Otázka: Mohu chránit sdílený sešit bez zadání hesla?
    
Odpověď: Ano, sdílený sešit můžete chránit bez zadání hesla. Pro lepší zabezpečení se však doporučuje používat silné heslo.

#### Otázka: Jak mohu zrušit ochranu sešitu sdíleného s Aspose.Cells?
    
Odpověď: Chcete-li odemknout sdílený sešit, musíte zadat stejné heslo, jaké bylo použito při ochraně sešitu. To umožňuje odstranění ochrany a volný přístup k datům.

#### Otázka: Má ochrana sdíleného sešitu vliv na funkce a vzorce v sešitu?
    
Odpověď: Když ochráníte sdílený sešit, uživatelé budou mít stále přístup k funkcím a vzorcům obsaženým v sešitu. Ochrana ovlivní pouze strukturální změny sešitu.