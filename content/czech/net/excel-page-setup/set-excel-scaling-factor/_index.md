---
title: Nastavit Excel Scaling Factor
linktitle: Nastavit Excel Scaling Factor
second_title: Aspose.Cells for .NET API Reference
description: Naučte se snadno manipulovat se soubory aplikace Excel a přizpůsobit faktor měřítka pomocí Aspose.Cells for .NET.
type: docs
weight: 180
url: /cs/net/excel-page-setup/set-excel-scaling-factor/
---
této příručce vás provedeme nastavením měřítka v tabulce Excel pomocí Aspose.Cells for .NET. Chcete-li provést tento úkol, postupujte podle následujících kroků.

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

## Krok 6: Nastavte faktor měřítka

Nastavte faktor měřítka pomocí následujícího kódu:

```csharp
worksheet.PageSetup.Zoom = 100;
```

Zde jsme nastavili faktor měřítka na 100, což znamená, že tabulka se při tisku zobrazí ve 100 % normální velikosti.

## Krok 7: Uložení sešitu aplikace Excel

 Chcete-li uložit sešit aplikace Excel s definovaným faktorem měřítka, použijte`Save` metoda objektu Workbook:

```csharp
workbook.Save(dataDir + "ScalingFactor_out.xls");
```

Tím se uloží excelový sešit s názvem souboru "ScalingFactor_out.xls" do zadaného adresáře.

### Ukázkový zdrojový kód pro Set Excel Scaling Factor pomocí Aspose.Cells pro .NET 
```csharp
//Cesta k adresáři dokumentů.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Vytvoření instance objektu sešitu
Workbook workbook = new Workbook();
// Přístup k prvnímu listu v souboru aplikace Excel
Worksheet worksheet = workbook.Worksheets[0];
// Nastavení měřítka na 100
worksheet.PageSetup.Zoom = 100;
// Uložte sešit.
workbook.Save(dataDir + "ScalingFactor_out.xls");
```

## Závěr

gratuluji! Naučili jste se, jak nastavit měřítko v excelové tabulce pomocí Aspose.Cells pro .NET. Faktor měřítka umožňuje upravit velikost tabulky při tisku pro optimální zobrazení.

### Nejčastější dotazy

#### 1. Jak nastavit faktor měřítka v tabulce Excel s Aspose.Cells pro .NET?

 Použijte`Zoom` vlastnictvím`PageSetup`objekt pro nastavení měřítka. Například,`worksheet.PageSetup.Zoom = 100;` nastaví faktor měřítka na 100 %.

#### 2. Mohu upravit faktor měřítka podle svých potřeb?

 Ano, faktor měřítka můžete upravit změnou hodnoty přiřazené k`Zoom` vlastnictví. Například,`worksheet.PageSetup.Zoom = 75;` nastaví faktor měřítka na 75 %.

#### 3. Je možné uložit excelový sešit s definovaným měřítkem?

 Ano, můžete použít`Save` metoda`Workbook` objekt k uložení sešitu aplikace Excel s definovaným faktorem měřítka.