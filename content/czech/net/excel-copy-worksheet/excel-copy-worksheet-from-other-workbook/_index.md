---
title: Excel Kopírovat list z jiného sešitu
linktitle: Excel Kopírovat list z jiného sešitu
second_title: Aspose.Cells for .NET API Reference
description: Jednoduše zkopírujte excelový list z jednoho sešitu do druhého pomocí Aspose.Cells for .NET.
type: docs
weight: 10
url: /cs/net/excel-copy-worksheet/excel-copy-worksheet-from-other-workbook/
---
V tomto tutoriálu vás provedeme kroky ke zkopírování listu aplikace Excel z jiného sešitu pomocí knihovny Aspose.Cells pro .NET. Dokončete tento úkol podle níže uvedených pokynů.

## Krok 1: Příprava

Než začnete, ujistěte se, že jste nainstalovali Aspose.Cells for .NET a vytvořili projekt C# ve vašem preferovaném integrovaném vývojovém prostředí (IDE).

## Krok 2: Nastavte cestu k adresáři dokumentu

 Prohlásit a`dataDir` proměnnou a inicializujte ji s cestou k adresáři vašich dokumentů. Například :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Nezapomeňte vyměnit`"YOUR_DOCUMENTS_DIRECTORY"` se skutečnou cestou k vašemu adresáři.

## Krok 3: Vytvořte nový excelový sešit

 Použijte`Workbook` třídy z Aspose.Cells a vytvořte nový excelový sešit:

```csharp
Workbook excelWorkbook0 = new Workbook();
```

## Krok 4: Získejte první list v sešitu

Přejděte na první list v sešitu pomocí indexu 0:

```csharp
Worksheet ws0 = excelWorkbook0.Worksheets[0];
```

## Krok 5: Přidejte data do řádků záhlaví (A1:A4)

 Použijte a`for` smyčka pro přidání dat do řádků záhlaví (A1:A4):

```csharp
for (int i = 0; i < 5; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Header row {0}", i));
}
```

## Krok 6: Přidejte podrobné údaje (A5:A999)

 Použijte jiný`for` smyčka pro přidání podrobných dat (A5:A999):

```csharp
for (int i = 5; i < 1000; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Detail row {0}", i));
}
```

## Krok 7: Nastavte možnosti rozvržení

 Nastavte možnosti nastavení stránky pro list pomocí`PageSetup` objekt:

```csharp
PageSetup pagesetup = ws0.PageSetup;
pagesetup.PrintTitleRows = "$1:$5";
```

## Krok 8: Vytvořte další sešit aplikace Excel

Vytvořte další excelový sešit:

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## Krok 9: Získejte první list z druhého sešitu

Přejděte na první list ve druhém sešitu:

```csharp
Worksheet ws1 = excelWorkbook1.Worksheets[0];
```

## Krok 10: Pojmenujte list

pojmenovat oheň

výpočetní ostrov:

```csharp
ws1.Name = "MySheet";
```

## Krok 11: Zkopírujte data z prvního listu prvního sešitu do prvního listu druhého sešitu

Zkopírujte data z prvního listu prvního sešitu do prvního listu druhého sešitu:

```csharp
ws1.Copy(ws0);
```

## Krok 12: Uložte soubor Excel

Uložte soubor Excel:

```csharp
excelWorkbook1.Save(dataDir + "CopyWorkbookSheetToOther_out.xls");
```

Nezapomeňte zadat požadovanou cestu a název souboru pro výstupní soubor.

### Ukázkový zdrojový kód pro Excel Kopírování listu z jiného sešitu pomocí Aspose.Cells pro .NET 
```csharp
//Cesta k adresáři dokumentů.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Vytvořte nový sešit.
Workbook excelWorkbook0 = new Workbook();
// Získejte první pracovní list v knize.
Worksheet ws0 = excelWorkbook0.Worksheets[0];
// Vložte nějaká data do řádků záhlaví (A1:A4)
for (int i = 0; i < 5; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Header Row {0}", i));
}
// Vložte nějaké podrobné údaje (A5:A999)
for (int i = 5; i < 1000; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Detail Row {0}", i));
}
// Definujte objekt nastavení stránky na základě prvního listu.
PageSetup pagesetup = ws0.PageSetup;
// Prvních pět řádků se na každé stránce opakuje...
// Je to vidět v náhledu tisku.
pagesetup.PrintTitleRows = "$1:$5";
// Vytvořte další sešit.
Workbook excelWorkbook1 = new Workbook();
// Získejte první pracovní list v knize.
Worksheet ws1 = excelWorkbook1.Worksheets[0];
// Pojmenujte pracovní list.
ws1.Name = "MySheet";
// Zkopírujte data z prvního listu prvního sešitu do
// první pracovní list druhého sešitu.
ws1.Copy(ws0);
// Uložte soubor aplikace Excel.
excelWorkbook1.Save(dataDir + "CopyWorksheetFromWorkbookToOther_out.xls");
```

## Závěr

gratuluji! Nyní jste se naučili, jak zkopírovat excelový list z jiného sešitu pomocí Aspose.Cells for .NET. Neváhejte použít tuto metodu ve svých vlastních projektech k efektivní manipulaci se soubory Excel.

### Nejčastější dotazy

#### Q. Jaké knihovny jsou potřebné k použití Aspose.Cells pro .NET?

A. Chcete-li používat Aspose.Cells pro .NET, musíte do projektu zahrnout knihovnu Aspose.Cells. Ujistěte se, že jste na tuto knihovnu správně odkazovali ve vašem integrovaném vývojovém prostředí (IDE).

#### Q. Podporuje Aspose.Cells další formáty souborů Excel, jako je XLSX?

A. Ano, Aspose.Cells podporuje různé formáty souborů Excel včetně XLSX, XLS, CSV, HTML a mnoha dalších. S těmito formáty souborů můžete manipulovat pomocí funkcí Aspose.Cells for .NET.

#### Q. Mohu přizpůsobit možnosti rozložení při kopírování listu?

A.  Ano, můžete upravit možnosti nastavení stránky při kopírování listu pomocí vlastností souboru`PageSetup` objekt. Můžete určit záhlaví stránky, zápatí, okraje, orientaci atd.