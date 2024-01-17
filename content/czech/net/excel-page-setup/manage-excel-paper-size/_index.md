---
title: Správa velikosti papíru aplikace Excel
linktitle: Správa velikosti papíru aplikace Excel
second_title: Aspose.Cells for .NET API Reference
description: Naučte se spravovat velikost papíru v Excelu pomocí Aspose.Cells pro .NET. Krok za krokem tutoriál se zdrojovým kódem v C#.
type: docs
weight: 70
url: /cs/net/excel-page-setup/manage-excel-paper-size/
---
tomto tutoriálu vás krok za krokem provedeme, jak spravovat velikost papíru v dokumentu aplikace Excel pomocí Aspose.Cells pro .NET. Ukážeme vám, jak nakonfigurovat velikost papíru pomocí zdrojového kódu C#.

## Krok 1: Nastavení prostředí

Ujistěte se, že máte na svém počítači nainstalovaný Aspose.Cells for .NET. Vytvořte také nový projekt ve vámi preferovaném vývojovém prostředí.

## Krok 2: Importujte potřebné knihovny

Do souboru kódu importujte knihovny potřebné pro práci s Aspose.Cells. Zde je odpovídající kód:

```csharp
using Aspose.Cells;
```

## Krok 3: Nastavte adresář dokumentů

Nastavte adresář, kde se nachází Excelový dokument, se kterým chcete pracovat. K nastavení adresáře použijte následující kód:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

Nezapomeňte zadat úplnou cestu k adresáři.

## Krok 4: Vytvoření objektu sešitu

Objekt Workbook představuje dokument Excel, se kterým budete pracovat. Můžete jej vytvořit pomocí následujícího kódu:

```csharp
Workbook workbook = new Workbook();
```

Tím se vytvoří nový prázdný objekt sešit.

## Krok 5: Přístup k prvnímu listu

Chcete-li získat přístup k první tabulce dokumentu aplikace Excel, použijte následující kód:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

To vám umožní pracovat s prvním listem v sešitu.

## Krok 6: Nastavení velikosti papíru

K nastavení velikosti papíru použijte vlastnost PageSetup.PaperSize objektu Worksheet. V tomto příkladu nastavíme velikost papíru na A4. Zde je odpovídající kód:

```csharp
worksheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
```

Tím nastavíte velikost tabulkového papíru na A4.

## Krok 7: Uložení sešitu

Chcete-li uložit změny do sešitu, použijte metodu Save() objektu Sešit. Zde je odpovídající kód:

```csharp
workbook.Save(dataDir + "ManagePaperSize_out.xls");
```

Tím se sešit uloží se změnami do zadaného adresáře.

### Ukázkový zdrojový kód pro správu velikosti papíru Excel pomocí Aspose.Cells pro .NET 
```csharp
//Cesta k adresáři dokumentů.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Vytvoření instance objektu sešitu
Workbook workbook = new Workbook();
// Přístup k prvnímu listu v souboru aplikace Excel
Worksheet worksheet = workbook.Worksheets[0];
// Nastavení velikosti papíru na A4
worksheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
// Uložte sešit.
workbook.Save(dataDir + "ManagePaperSize_out.xls");
```
## Závěr

Nyní jste se naučili, jak spravovat velikost papíru v dokumentu aplikace Excel pomocí Aspose.Cells pro .NET. Tento tutoriál vás provede každým krokem procesu, od nastavení prostředí až po uložení změn. Nyní můžete tyto znalosti použít k přizpůsobení velikosti papíru vašich dokumentů aplikace Excel.

### FAQ

#### Q1: Mohu nastavit vlastní formát papíru jiný než A4?

Odpověď 1: Ano, Aspose.Cells podporuje různé předdefinované velikosti papíru a také možnost nastavit vlastní velikost papíru zadáním požadovaných rozměrů.

#### Q2: Jak zjistím aktuální velikost papíru v dokumentu aplikace Excel?

 A2: Můžete použít`PageSetup.PaperSize` vlastnictvím`Worksheet` objekt, abyste získali aktuálně nastavenou velikost papíru.

#### Q3: Je možné nastavit extra okraje stránky s velikostí papíru?

 A3: Ano, můžete použít`PageSetup.LeftMargin`, `PageSetup.RightMargin`, `PageSetup.TopMargin` a`PageSetup.BottomMargin` vlastnosti pro nastavení dalších okrajů stránky kromě velikosti papíru.

#### Q4: Funguje tato metoda pro všechny formáty souborů aplikace Excel, například .xls a .xlsx?

Odpověď 4: Ano, tato metoda funguje pro formáty souborů .xls i .xlsx.

#### Q5: Mohu použít různé velikosti papíru na různé listy ve stejném sešitu?

 A5: Ano, můžete použít různé velikosti papíru na různé listy ve stejném sešitu pomocí`PageSetup.PaperSize` vlastnost každého listu.