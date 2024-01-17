---
title: Nastavte možnosti tisku aplikace Excel
linktitle: Nastavte možnosti tisku aplikace Excel
second_title: Aspose.Cells for .NET API Reference
description: Naučte se snadno manipulovat se soubory aplikace Excel a přizpůsobovat možnosti tisku pomocí Aspose.Cells pro .NET.
type: docs
weight: 150
url: /cs/net/excel-page-setup/set-excel-print-options/
---
V této příručce vás provedeme nastavením možností tisku pro sešit aplikace Excel pomocí Aspose.Cells for .NET. Pro splnění tohoto úkolu vás krok za krokem provedeme poskytnutým zdrojovým kódem C#.

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

Chcete-li nastavit možnosti tisku, musíme nejprve získat odkaz PageSetup z listu. K získání reference použijte následující kód:

```csharp
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## Krok 6: Povolte tisk čar mřížky

Chcete-li povolit tisk čar mřížky, použijte následující kód:

```csharp
pageSetup. PrintGridlines = true;
```

## Krok 7: Povolte tisk záhlaví řádků/sloupců

Chcete-li povolit tisk záhlaví řádků a sloupců, použijte následující kód:

```csharp
pageSetup.PrintHeadings = true;
```

## Krok 8: Povolení režimu černobílého tisku

Chcete-li povolit tisk listu v černobílém režimu, použijte následující kód:

```csharp
pageSetup.BlackAndWhite = true;
```

## Krok 9: Povolení tisku zpětné vazby

Chcete-li povolit tisk komentářů tak, jak se objevují v tabulce, použijte následující kód:

```csharp
pageSetup.PrintComments = PrintCommentsType.PrintInPlace;
```

## Krok 10: Povolte tisk v režimu konceptu

Chcete-li povolit tisk tabulky v režimu konceptu, použijte následující kód:

```csharp
pageSetup.PrintDraft = true;
```

## Krok 11: Povolte tisk chyb buněk jako N/A

Chcete-li umožnit tisk chyb buněk jako

  než N/A, použijte následující kód:

```csharp
pageSetup.PrintErrors = PrintErrorsType.PrintErrorsNA;
```

## Krok 12: Uložení sešitu aplikace Excel

 Chcete-li uložit sešit Excel s nastavenými možnostmi tisku, použijte`Save` metoda objektu Workbook:

```csharp
workbook.Save(dataDir + "OtherPrintOptions_out.xls");
```

Tím se uloží sešit aplikace Excel s názvem souboru "OtherPrintOptions_out.xls" do zadaného adresáře.

### Ukázkový zdrojový kód pro Set Excel Print Options pomocí Aspose.Cells pro .NET 
```csharp
//Cesta k adresáři dokumentů.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Vytvoření instance objektu sešitu
Workbook workbook = new Workbook();
// Získání odkazu na PageSetup listu
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Umožňuje tisknout mřížku
pageSetup.PrintGridlines = true;
// Umožňuje tisk záhlaví řádků/sloupců
pageSetup.PrintHeadings = true;
// Umožňuje tisk listu v černobílém režimu
pageSetup.BlackAndWhite = true;
// Umožňuje tisknout komentáře, jak jsou zobrazeny na listu
pageSetup.PrintComments = PrintCommentsType.PrintInPlace;
// Umožňuje tisk listu v kvalitě konceptu
pageSetup.PrintDraft = true;
// Umožňuje tisknout chyby buněk jako N/A
pageSetup.PrintErrors = PrintErrorsType.PrintErrorsNA;
// Uložte sešit.
workbook.Save(dataDir + "OtherPrintOptions_out.xls");
```
## Závěr

Nyní jste se naučili, jak nastavit možnosti tisku pro sešit aplikace Excel pomocí Aspose.Cells pro .NET. Tato výkonná a uživatelsky přívětivá knihovna vám umožňuje snadno a efektivně přizpůsobit nastavení tisku vašich excelových sešitů.

### Nejčastější dotazy


#### 1. Mohu dále upravit možnosti tisku, jako jsou okraje nebo orientace stránky?

Ano, Aspose.Cells for .NET nabízí širokou škálu přizpůsobitelných možností tisku, jako jsou okraje, orientace stránky, měřítko atd.

#### 2. Podporuje Aspose.Cells for .NET další formáty souborů Excel?

Ano, Aspose.Cells for .NET podporuje různé formáty souborů Excel, jako jsou XLSX, XLS, CSV, HTML, PDF atd.

#### 3. Je Aspose.Cells for .NET kompatibilní se všemi verzemi .NET Framework?

Aspose.Cells for .NET je kompatibilní s rozhraním .NET Framework 2.0 nebo novějším, včetně verzí 3.5, 4.0, 4.5, 4.6 atd.