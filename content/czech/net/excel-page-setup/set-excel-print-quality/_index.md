---
title: Nastavte kvalitu tisku Excel
linktitle: Nastavte kvalitu tisku Excel
second_title: Aspose.Cells for .NET API Reference
description: Naučte se spravovat a přizpůsobovat soubory Excel, včetně možností tisku pomocí Aspose.Cells pro .NET.
type: docs
weight: 160
url: /cs/net/excel-page-setup/set-excel-print-quality/
---
V této příručce vysvětlíme, jak nastavit kvalitu tisku excelové tabulky pomocí Aspose.Cells for .NET. Pro splnění tohoto úkolu vás krok za krokem provedeme poskytnutým zdrojovým kódem C#.

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

## Krok 5: Přístup k prvnímu listu

Přejděte na první list v sešitu aplikace Excel pomocí následujícího kódu:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Krok 6: Nastavení kvality tisku

Chcete-li nastavit kvalitu tisku listu, použijte následující kód:

```csharp
worksheet.PageSetup.PrintQuality = 180;
```

Zde jsme nastavili kvalitu tisku na 180 dpi, ale tuto hodnotu si můžete upravit podle svých potřeb.

## Krok 7: Uložení sešitu aplikace Excel

 Chcete-li uložit sešit Excel s definovanou kvalitou tisku, použijte`Save` metoda objektu Workbook:

```csharp
workbook.Save(dataDir + "SetPrintQuality_out.xls");
```

Tím se uloží sešit aplikace Excel s názvem souboru "SetPrintQuality_out.xls" do určeného adresáře.

### Ukázkový zdrojový kód pro nastavení kvality tisku Excel pomocí Aspose.Cells pro .NET 
```csharp
//Cesta k adresáři dokumentů.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Vytvoření instance objektu sešitu
Workbook workbook = new Workbook();
// Přístup k prvnímu listu v souboru aplikace Excel
Worksheet worksheet = workbook.Worksheets[0];
// Nastavení kvality tisku listu na 180 dpi
worksheet.PageSetup.PrintQuality = 180;
// Uložte sešit.
workbook.Save(dataDir + "SetPrintQuality_out.xls");
```

## Závěr

gratuluji! Naučili jste se, jak nastavit kvalitu tisku excelové tabulky pomocí Aspose.Cells for .NET. Nyní můžete přizpůsobit kvalitu tisku svých souborů Excel podle svých specifických preferencí a potřeb.

## Nejčastější dotazy


#### 1. Mohu přizpůsobit kvalitu tisku různých listů ve stejném souboru aplikace Excel?

Ano, kvalitu tisku každého listu můžete individuálně přizpůsobit tak, že přejdete na odpovídající objekt Worksheet a nastavíte vhodnou kvalitu tisku.

#### 2. Jaké další možnosti tisku mohu upravit pomocí Aspose.Cells pro .NET?

Kromě kvality tisku můžete přizpůsobit různé další možnosti tisku, jako jsou okraje, orientace stránky, měřítko tisku atd.

#### 3. Podporuje Aspose.Cells for .NET různé formáty souborů Excel?

Ano, Aspose.Cells for .NET podporuje širokou škálu formátů souborů Excel včetně XLSX, XLS, CSV, HTML, PDF atd.