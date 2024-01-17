---
title: Nastavte číslo první stránky aplikace Excel
linktitle: Nastavte číslo první stránky aplikace Excel
second_title: Aspose.Cells for .NET API Reference
description: Přečtěte si, jak nastavit číslo první stránky v Excelu pomocí Aspose.Cells for .NET.
type: docs
weight: 90
url: /cs/net/excel-page-setup/set-excel-first-page-number/
---
V tomto tutoriálu vás provedeme tím, jak nastavit číslo první stránky v Excelu pomocí Aspose.Cells for .NET. Pro ilustraci procesu použijeme zdrojový kód C#.

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
Workbook workbook = new Workbook();
Worksheet worksheet = workbook.Worksheets[0];
```

Tím vytvoříte prázdný sešit s pracovním listem.

## Krok 5: Nastavení čísla první stránky

Pomocí následujícího kódu nastavte číslo první stránky listu listu:

```csharp
worksheet.PageSetup.FirstPageNumber = 2;
```

Tím nastavíte číslo první stránky na 2.

## Krok 6: Uložení upraveného sešitu

Uložte upravený sešit pomocí následujícího kódu:

```csharp
workbook.Save(dataDir + "OutputFileName.xls");
```

Tím se upravený sešit uloží do zadaného datového adresáře.

### Ukázkový zdrojový kód pro Set Excel First Page Number pomocí Aspose.Cells for .NET 
```csharp
//Cesta k adresáři dokumentů.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Vytvoření instance objektu sešitu
Workbook workbook = new Workbook();
// Přístup k prvnímu listu v souboru aplikace Excel
Worksheet worksheet = workbook.Worksheets[0];
// Nastavení čísla první stránky stránek listu
worksheet.PageSetup.FirstPageNumber = 2;
// Uložte sešit.
workbook.Save(dataDir + "SetFirstPageNumber_out.xls");
```

## Závěr

Nyní jste se naučili, jak nastavit číslo první stránky v Excelu pomocí Aspose.Cells for .NET. Tento tutoriál vás provede každým krokem procesu, od nastavení prostředí až po nastavení čísla první stránky. Nyní můžete tyto znalosti použít k přizpůsobení číslování stránek v souborech aplikace Excel.

### FAQ

#### Q1: Mohu pro každý list nastavit jiné číslo první stránky?

 A1: Ano, můžete nastavit jiné číslo první stránky pro každý list přístupem k`FirstPageNumber`vlastnost příslušného listu`PageSetup` objekt.

#### Q2: Jak mohu zkontrolovat číslo první stránky existující tabulky?

 A2: Číslo první stránky existujícího listu můžete zkontrolovat přístupem k`FirstPageNumber` vlastnictvím`PageSetup` objekt odpovídající tomuto listu.

#### Q3: Začíná číslování stránek ve výchozím nastavení vždy od 1?

A3: Ano, číslování stránek začíná v Excelu ve výchozím nastavení od 1. Můžete však použít kód zobrazený v tomto kurzu k nastavení jiného čísla první stránky.

#### Q4: Jsou změny čísla první stránky v upraveném souboru Excel trvalé?

A4: Ano, změny provedené v čísle první stránky jsou trvale uloženy v upraveném souboru Excel.

#### Q5: Funguje tato metoda pro všechny formáty souborů aplikace Excel, jako jsou .xls a .xlsx?

Odpověď 5: Ano, tato metoda funguje pro všechny formáty souborů aplikace Excel podporované Aspose.Cells, včetně .xls a .xlsx.