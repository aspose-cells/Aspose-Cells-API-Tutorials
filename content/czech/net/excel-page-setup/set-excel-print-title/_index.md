---
title: Nastavte název tisku aplikace Excel
linktitle: Nastavte název tisku aplikace Excel
second_title: Aspose.Cells for .NET API Reference
description: Naučte se snadno manipulovat se soubory aplikace Excel a přizpůsobovat možnosti tisku pomocí Aspose.Cells for .NET.
type: docs
weight: 170
url: /cs/net/excel-page-setup/set-excel-print-title/
---
V této příručce vás provedeme nastavením tiskových titulků v excelové tabulce pomocí Aspose.Cells pro .NET. Chcete-li provést tento úkol, postupujte podle následujících kroků.

## Krok 1: Nastavení prostředí

Ujistěte se, že jste nastavili vývojové prostředí a nainstalovali Aspose.Cells for .NET. Nejnovější verzi knihovny si můžete stáhnout z oficiálních stránek Aspose.

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

## Krok 5: Přístup k prvnímu listu

Přejděte na první list v sešitu aplikace Excel pomocí následujícího kódu:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Krok 6: Definování titulkových sloupců

Definujte sloupce nadpisů pomocí následujícího kódu:

```csharp
pageSetup.PrintTitleColumns = "$A:$B";
```

Zde jsme definovali sloupce A a B jako titulní sloupce. Tuto hodnotu můžete upravit podle svých potřeb.

## Krok 7: Definování titulků

Definujte řádky nadpisů pomocí následujícího kódu:

```csharp
pageSetup.PrintTitleRows = "$1:$2";
```

Řádky 1 a 2 jsme definovali jako titulní řádky. Tyto hodnoty můžete upravit podle svých potřeb.

## Krok 8: Uložení sešitu aplikace Excel

 Chcete-li uložit sešit Excel s definovanými názvy tisku, použijte`Save` metoda objektu Workbook:

```csharp
workbook.Save(dataDir + "SetPrintTitle_out.xls");
```

Tím se uloží sešit aplikace Excel s názvem souboru "SetPrintTitle_out.xls" do zadaného adresáře.

### Ukázkový zdrojový kód pro Set Excel Print Title pomocí Aspose.Cells pro .NET 
```csharp
//Cesta k adresáři dokumentů.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Vytvoření instance objektu sešitu
Workbook workbook = new Workbook();
// Získání odkazu na PageSetup listu
Aspose.Cells.PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Definování čísel sloupců A a B jako titulních sloupců
pageSetup.PrintTitleColumns = "$A:$B";
// Definování čísel řádků 1 a 2 jako titulních řádků
pageSetup.PrintTitleRows = "$1:$2";
// Uložte sešit.
workbook.Save(dataDir + "SetPrintTitle_out.xls");
```

## Závěr

gratuluji! Naučili jste se, jak nastavit tiskové titulky v excelové tabulce pomocí Aspose.Cells pro .NET. Názvy tisku umožňují zobrazit konkrétní řádky a sloupce na každé vytištěné stránce, což usnadňuje čtení a odkazy na data.

### Nejčastější dotazy

#### 1. Mohu v Excelu nastavit názvy tisku pro konkrétní sloupce?

 Ano, s Aspose.Cells pro .NET můžete nastavit konkrétní sloupce jako názvy tisku pomocí`PrintTitleColumns` vlastnictvím`PageSetup` objekt.

#### 2. Je možné definovat názvy sloupců i tiskových řádků?

 Ano, můžete nastavit názvy sloupců i řádků tisku pomocí`PrintTitleColumns` a`PrintTitleRows` vlastnosti`PageSetup` objekt.

#### 3. Jaká další nastavení rozložení mohu upravit pomocí Aspose.Cells pro .NET?

Pomocí Aspose.Cells for .NET můžete přizpůsobit různá nastavení rozvržení stránky, jako jsou okraje, orientace stránky, měřítko tisku a další.