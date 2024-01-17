---
title: Možnosti Fit To Excel Pages
linktitle: Možnosti Fit To Excel Pages
second_title: Aspose.Cells for .NET API Reference
description: Naučte se, jak automaticky přizpůsobit stránky v excelové tabulce pomocí Aspose.Cells for .NET.
type: docs
weight: 30
url: /cs/net/excel-page-setup/fit-to-excel-pages-options/
---
V tomto článku vás krok za krokem provedeme vysvětlením následujícího zdrojového kódu C#: Možnosti přizpůsobení Excel Pages pomocí Aspose.Cells for .NET. K provedení této operace použijeme knihovnu Aspose.Cells pro .NET. Chcete-li nakonfigurovat přizpůsobení na stránky v aplikaci Excel, postupujte podle následujících kroků.

## Krok 1: Vytvoření sešitu
Prvním krokem je vytvoření sešitu. Chystáme se vytvořit instanci objektu Workbook. Zde je kód pro vytvoření sešitu:

```csharp
// Cesta k adresáři dokumentů
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Vytvořte instanci objektu sešitu
Workbook workbook = new Workbook();
```

## Krok 2: Přístup k pracovnímu listu
Nyní, když jsme vytvořili sešit, musíme přejít na první list. Pro přístup k prvnímu listu použijeme index 0. Zde je kód pro přístup:

```csharp
// Přístup k prvnímu listu v sešitu
Worksheet worksheet = workbook.Worksheets[0];
```

## Krok 3: Nastavení Přizpůsobit na stránky
 V tomto kroku nakonfigurujeme úpravu stránek listu. Budeme používat`FitToPagesTall` a`FitToPagesWide` vlastnosti`PageSetup` objekt k určení požadovaného počtu stránek pro výšku a šířku listu. Zde je kód pro to:

```csharp
// Nakonfigurujte počet stránek pro výšku listu
worksheet.PageSetup.FitToPagesTall = 1;

// Nakonfigurujte počet stránek na šířku listu
worksheet.PageSetup.FitToPagesWide = 1;
```

## Krok 4: Uložení sešitu
 Nyní, když jsme nakonfigurovali přizpůsobení na stránky, můžeme sešit uložit. Budeme používat`Save` metoda objektu Workbook k tomu. Zde je kód pro uložení sešitu:

```csharp
// Uložte sešit
workbook.Save(dataDir + "FitToPagesOptions_out.xls");
```

### Ukázkový zdrojový kód pro možnosti Fit To Excel Pages pomocí Aspose.Cells pro .NET 
```csharp
//Cesta k adresáři dokumentů.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Vytvoření instance objektu sešitu
Workbook workbook = new Workbook();
// Přístup k prvnímu listu v souboru aplikace Excel
Worksheet worksheet = workbook.Worksheets[0];
// Nastavení počtu stránek, na které bude délka listu roztažena
worksheet.PageSetup.FitToPagesTall = 1;
//Nastavení počtu stránek, na které bude šířka listu roztažena
worksheet.PageSetup.FitToPagesWide = 1;
// Uložte sešit.
workbook.Save(dataDir + "FitToPagesOptions_out.xls");
```

## Závěr
V tomto článku jsme se naučili, jak nakonfigurovat přizpůsobení na stránky v Excelu pomocí Aspose.Cells for .NET. Prošli jsme následujícími kroky: vytvoření sešitu, přístup k listu, konfigurace přizpůsobení na stránky a uložení sešitu. Nyní můžete tyto znalosti využít k úpravě tabulek na požadované stránky.

### Nejčastější dotazy

#### Otázka: Jak mohu nainstalovat Aspose.Cells pro .NET?

A: Chcete-li nainstalovat Aspose.Cells pro .NET, můžete použít správce balíčků NuGet v sadě Visual Studio. Najděte balíček "Aspose.Cells" a nainstalujte jej do svého projektu.

#### Otázka: Mohu přizpůsobit stránky na výšku i na šířku?

 Odpověď: Ano, můžete upravit výšku i šířku listu pomocí`FitToPagesTall` a`FitToPagesWide` vlastnosti. Pro každý rozměr můžete zadat požadovaný počet stránek.

#### Otázka: Jak mohu přizpůsobit možnosti Přizpůsobit stránkám?

Odpověď: Kromě určení počtu stránek můžete také přizpůsobit další možnosti přizpůsobení na stránky, jako je měřítko listu, orientace papíru, okraje a další. Použijte vlastnosti dostupné v`PageSetup` objekt pro toto.

#### Otázka: Mohu použít Aspose.Cells pro .NET ke zpracování existujících sešitů?

Odpověď: Ano, můžete použít Aspose.Cells pro .NET k otevření a úpravě existujících sešitů. Můžete přistupovat k listům, buňkám, vzorcům, stylům a dalším položkám sešitu a provádět různé operace.