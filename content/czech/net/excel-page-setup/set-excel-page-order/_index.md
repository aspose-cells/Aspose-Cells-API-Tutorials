---
title: Nastavte pořadí stránek aplikace Excel
linktitle: Nastavte pořadí stránek aplikace Excel
second_title: Aspose.Cells for .NET API Reference
description: Krok za krokem průvodce nastavením pořadí stránek v Excelu pomocí Aspose.Cells pro .NET. Zahrnuty podrobné pokyny a zdrojový kód.
type: docs
weight: 120
url: /cs/net/excel-page-setup/set-excel-page-order/
---
tomto článku vás krok za krokem provedeme vysvětlením následujícího zdrojového kódu C# pro nastavení pořadí stránek aplikace Excel pomocí Aspose.Cells for .NET. Ukážeme vám, jak nastavit adresář dokumentů, vytvořit instanci objektu Workbook, získat referenci PageSetup, nastavit pořadí tisku stránky a uložit sešit.

## Krok 1: Nastavení adresáře dokumentů

 Než začnete, musíte nakonfigurovat adresář dokumentů, kam chcete soubor aplikace Excel uložit. Můžete zadat cestu k adresáři nahrazením hodnoty`dataDir` proměnná s vlastní cestou.

```csharp
//Cesta k adresáři dokumentů.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

## Krok 2: Vytvoření instance objektu sešitu

Prvním krokem je vytvoření instance objektu Workbook. Toto představuje excelový sešit, se kterým budeme pracovat.

```csharp
// Vytvořte instanci objektu sešitu
Workbook workbook = new Workbook();
```

## Krok 3: Získání reference PageSetup

Dále musíme získat referenci objektu PageSetup listu, na kterém chceme nastavit pořadí stránek.

```csharp
// Získejte odkaz PageSetup listu
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## Krok 4: Nastavení pořadí tisku stránek

Nyní můžeme nastavit pořadí tisku stránek. V tomto příkladu používáme možnost "OverThenDown", což znamená, že stránky budou vytištěny zleva doprava a poté shora dolů.

```csharp
// Nastavte pořadí tisku stránky na "OverThenDown"
pageSetup.Order = PrintOrderType.OverThenDown;
```

## Krok 5: Uložení sešitu

Nakonec sešit Excel uložíme se změnami pořadí stránek.

```csharp
// Uložte sešit
workbook.Save(dataDir + "SetPageOrder_out.xls");
```

### Ukázkový zdrojový kód pro Set Excel Page Order pomocí Aspose.Cells pro .NET 
```csharp
//Cesta k adresáři dokumentů.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Vytvoření instance objektu sešitu
Workbook workbook = new Workbook();
// Získání odkazu na PageSetup listu
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Nastavení pořadí tisku stránek přes a dolů
pageSetup.Order = PrintOrderType.OverThenDown;
// Uložte sešit.
workbook.Save(dataDir + "SetPageOrder_out.xls");
```

## Závěr

V tomto tutoriálu jsme vysvětlili, jak nastavit pořadí stránek v souboru aplikace Excel pomocí Aspose.Cells for .NET. Podle uvedených kroků můžete snadno nakonfigurovat adresář dokumentů, vytvořit instanci objektu Workbook, získat referenci PageSetup, nastavit pořadí tisku stránky a uložit sešit.

### FAQ

#### Q1: Proč je důležité nastavit pořadí stránek v souboru aplikace Excel?

Definování pořadí stránek v souboru aplikace Excel je důležité, protože určuje, jak budou stránky vytištěny nebo zobrazeny. Zadáním konkrétního pořadí můžete data logicky uspořádat a usnadnit čtení nebo tisk souboru.

#### Q2: Mohu použít jiné objednávky tisku stránky s Aspose.Cells pro .NET?

Ano, Aspose.Cells for .NET podporuje vícestránkové tiskové objednávky, jako jsou „DownThenOver“, „OverThenDown“, „DownThenOverThenDownAgain“ atd. Můžete si vybrat ten, který nejlépe vyhovuje vašim potřebám.

#### Q3: Mohu nastavit další možnosti pro tisk stránek pomocí Aspose.Cells pro .NET?

Ano, můžete nastavit různé možnosti tisku stránky, jako je měřítko, orientace, okraje atd., pomocí vlastností objektu PageSetup v Aspose.Cells for .NET.

#### Q4: Podporuje Aspose.Cells for .NET další formáty souborů aplikace Excel?

Ano, Aspose.Cells for .NET podporuje širokou škálu formátů souborů Excel, jako jsou XLSX, XLS, CSV, HTML, PDF atd. Mezi těmito formáty můžete snadno převádět pomocí funkcí, které knihovna poskytuje.