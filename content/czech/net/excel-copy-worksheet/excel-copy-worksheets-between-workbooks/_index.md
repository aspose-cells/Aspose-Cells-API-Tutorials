---
title: Kopírování listů aplikace Excel mezi sešity
linktitle: Kopírování listů aplikace Excel mezi sešity
second_title: Aspose.Cells for .NET API Reference
description: Pomocí Aspose.Cells for .NET můžete snadno kopírovat listy mezi sešity aplikace Excel.
type: docs
weight: 30
url: /cs/net/excel-copy-worksheet/excel-copy-worksheets-between-workbooks/
---
tomto tutoriálu vás provedeme kroky ke kopírování listů mezi sešity aplikace Excel pomocí knihovny Aspose.Cells pro .NET. Dokončete tento úkol podle níže uvedených pokynů.

## Krok 1: Příprava

Ujistěte se, že jste nainstalovali Aspose.Cells for .NET a vytvořili projekt C# ve vašem preferovaném integrovaném vývojovém prostředí (IDE).

## Krok 2: Nastavte cestu k adresáři dokumentu

 Prohlásit a`dataDir` proměnnou a inicializujte ji s cestou k adresáři vašich dokumentů. Například :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Nezapomeňte vyměnit`"YOUR_DOCUMENTS_DIRECTORY"` se skutečnou cestou k vašemu adresáři.

## Krok 3: Definujte cestu k vstupnímu souboru

 Prohlásit an`InputPath` proměnnou a inicializujte ji úplnou cestou k souboru aplikace Excel, ze kterého chcete tabulku zkopírovat. Například :

```csharp
string InputPath = dataDir + "book1.xls";
```

 Ujistěte se, že máte soubor Excel`book1.xls` v adresáři dokumentů nebo zadejte správný název souboru a umístění.

## Krok 4: Vytvořte první sešit aplikace Excel

 Použijte`Workbook` třídy Aspose.Cells k vytvoření prvního sešitu aplikace Excel a otevření zadaného souboru:

```csharp
Workbook excelWorkbook0 = new Workbook(InputPath);
```

## Krok 5: Vytvořte druhý sešit aplikace Excel

Vytvořte druhý excelový sešit:

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## Krok 6: Zkopírujte list z prvního sešitu do druhého sešitu

 Použijte`Copy`metoda kopírování prvního listu z prvního sešitu do druhého sešitu:

```csharp
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
```

## Krok 7: Uložte soubor aplikace Excel

Uložte soubor Excel obsahující zkopírovanou tabulku:

```csharp
excelWorkbook1.Save(dataDir + "Copy WorksheetsBetweenWorkbooks_out.xls");
```

Nezapomeňte zadat požadovanou cestu a název souboru pro výstupní soubor.

### Ukázkový zdrojový kód pro Excel Kopírování pracovních listů mezi sešity pomocí Aspose.Cells pro .NET 
```csharp
//Cesta k adresáři dokumentů.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Vytvořte sešit.
// Otevřete soubor do první knihy.
Workbook excelWorkbook0 = new Workbook(InputPath);
// Vytvořte další sešit.
Workbook excelWorkbook1 = new Workbook();
// Zkopírujte první list první knihy do druhé knihy.
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
// Uložte soubor.
excelWorkbook1.Save(dataDir + "CopyWorksheetsBetweenWorkbooks_out.xls");
```

## Závěr

gratuluji! Nyní jste se naučili, jak kopírovat listy mezi sešity aplikace Excel pomocí Aspose.Cells for .NET. Neváhejte použít tuto metodu ve svých vlastních projektech k efektivní manipulaci se soubory Excel.

### Nejčastější dotazy

#### Q. Jaké knihovny jsou potřebné k použití Aspose.Cells pro .NET?

A. Chcete-li používat Aspose.Cells pro .NET, musíte do projektu zahrnout knihovnu Aspose.Cells. Ujistěte se, že jste na tuto knihovnu správně odkazovali ve vašem integrovaném vývojovém prostředí (IDE).

#### Q. Podporuje Aspose.Cells další formáty souborů Excel, jako je XLSX?

A. Ano, Aspose.Cells podporuje různé formáty souborů Excel včetně XLSX, XLS, CSV, HTML a mnoha dalších. S těmito formáty souborů můžete manipulovat pomocí funkcí Aspose.Cells for .NET.

#### Otázka: Mohu přizpůsobit možnosti rozvržení při kopírování tabulky?

A.  Ano, můžete upravit možnosti nastavení stránky při kopírování tabulky pomocí vlastností souboru`PageSetup` objekt. Můžete určit záhlaví stránky, zápatí, okraje, orientaci atd.