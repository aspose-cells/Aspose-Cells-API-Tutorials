---
title: Nastavte oblast tisku aplikace Excel
linktitle: Nastavte oblast tisku aplikace Excel
second_title: Aspose.Cells for .NET API Reference
description: Krok za krokem průvodce nastavením oblasti tisku aplikace Excel pomocí Aspose.Cells pro .NET. Snadno optimalizujte a přizpůsobte své excelové sešity.
type: docs
weight: 140
url: /cs/net/excel-page-setup/set-excel-print-area/
---
Použití Aspose.Cells pro .NET může značně usnadnit správu a manipulaci se soubory aplikace Excel v aplikacích .NET. V této příručce vám ukážeme, jak nastavit oblast tisku excelového sešitu pomocí Aspose.Cells for .NET. Pro splnění tohoto úkolu vás krok za krokem provedeme poskytnutým zdrojovým kódem C#.

## Krok 1: Nastavení prostředí

Než začnete, ujistěte se, že jste nastavili vývojové prostředí a nainstalovali Aspose.Cells for .NET. Nejnovější verzi knihovny si můžete stáhnout z oficiálních stránek Aspose.

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

Vytvořte instanci objektu Workbook, který představuje sešit aplikace Excel, který chcete vytvořit:

```csharp
Workbook workbook = new Workbook();
```

## Krok 5: Získání reference PageSetup listu

Chcete-li nastavit oblast tisku, musíme nejprve získat referenci z PageSetup listu. K získání reference použijte následující kód:

```csharp
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## Krok 6: Určení rozsahu buněk oblasti tisku

Nyní, když máme odkaz PageSetup, můžeme určit rozsah buněk, které tvoří oblast tisku. V tomto příkladu nastavíme jako oblast tisku rozsah buněk od A1 do T35. Použijte následující kód:

```csharp
pageSetup.PrintArea = "A1:T35";
```

Rozsah buněk můžete upravit podle svých potřeb.

## Krok 7: Uložení sešitu aplikace Excel

 Chcete-li uložit sešit Excel s definovanou oblastí tisku, použijte`Save` metoda objektu Workbook:

```csharp
workbook.Save(dataDir + "SetPrintArea_out.xls");
```

Tím se uloží sešit aplikace Excel s názvem souboru "SetPrintArea_out.xls" do zadaného adresáře.

### Ukázkový zdrojový kód pro Set Excel Print Area pomocí Aspose.Cells pro .NET 
```csharp
//Cesta k adresáři dokumentů.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Vytvoření instance objektu sešitu
Workbook workbook = new Workbook();
// Získání odkazu na PageSetup listu
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Určení rozsahu buněk (od buňky A1 do buňky T35) oblasti tisku
pageSetup.PrintArea = "A1:T35";
// Uložte sešit.
workbook.Save(dataDir + "SetPrintArea_out.xls");
```

## Závěr

gratuluji! Nyní jste se naučili, jak nastavit oblast tisku excelového sešitu pomocí Aspose.Cells for .NET. Tato výkonná a uživatelsky přívětivá knihovna výrazně usnadňuje práci se soubory aplikace Excel ve vašich aplikacích .NET. Pokud máte další otázky nebo narazíte na nějaké potíže, neváhejte se podívat na oficiální dokumentaci Aspose.Cells, kde najdete další informace a zdroje.

### FAQ

#### 1. Mohu dále upravit rozvržení oblasti tisku, jako je orientace a okraje?

Ano, máte přístup k dalším vlastnostem PageSetup, jako je orientace stránky, okraje, měřítko atd., abyste dále přizpůsobili rozvržení oblasti tisku.

#### 2. Podporuje Aspose.Cells for .NET další formáty souborů Excel, jako jsou XLSX a CSV?

Ano, Aspose.Cells for .NET podporuje různé formáty souborů Excel včetně XLSX, XLS, CSV, HTML, PDF a mnoha dalších.

#### 3. Je Aspose.Cells for .NET kompatibilní se všemi verzemi .NET Framework?

Aspose.Cells for .NET je kompatibilní s rozhraním .NET Framework 2.0 nebo novějším, včetně verzí 3.5, 4.0, 4.5, 4.6 atd.