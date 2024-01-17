---
title: Výukový program Odstranit pracovní list aplikace Excel podle indexu C#
linktitle: Odstranit sešit Excel podle indexu
second_title: Aspose.Cells for .NET API Reference
description: Pomocí Aspose.Cells for .NET můžete snadno odstranit konkrétní list aplikace Excel. Podrobný návod s příklady kódu.
type: docs
weight: 30
url: /cs/net/excel-worksheet-csharp-tutorials/delete-excel-worksheet-by-index-csharp-tutorial/
---
V tomto tutoriálu vás krok za krokem provedeme vysvětlením níže uvedeného zdrojového kódu C#, kterým je odstranění listu aplikace Excel pomocí Aspose.Cells for .NET. Ke každému kroku zahrneme ukázkový kód, který vám pomůže podrobně porozumět procesu.

## Krok 1: Definujte adresář dokumentů

Chcete-li začít, musíte nastavit cestu k adresáři, kde se nachází váš soubor Excel. Nahraďte "VÁŠ ADRESÁŘ DOKUMENTŮ" v kódu skutečnou cestou k souboru Excel.

```csharp
//Cesta k adresáři dokumentů.
string dataDir = "YOUR DOCUMENT DIRECTORY";
```

## Krok 2: Vytvořte datový proud a otevřete soubor Excel

 Dále musíte vytvořit souborový stream a otevřít soubor Excel pomocí`FileStream` třída.

```csharp
// Vytvořte datový proud obsahující soubor aplikace Excel, který chcete otevřít
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

## Krok 3: Vytvořte instanci objektu sešitu

 Po otevření souboru Excel je třeba vytvořit instanci a`Workbook`objekt. Tento objekt představuje sešit aplikace Excel a nabízí různé metody a vlastnosti pro manipulaci se sešitem.

```csharp
// Vytvořte instanci objektu sešitu
// Otevřete soubor aplikace Excel prostřednictvím toku souborů
Workbook workbook = new Workbook(fstream);
```

## Krok 4: Odstraňte list podle indexu

 Chcete-li odstranit list z jeho indexu, můžete použít`RemoveAt()` metoda`Worksheets` objekt`Workbook` objekt. Jako parametr musí být předán index listu, který chcete odstranit.

```csharp
// Odstraňte list pomocí indexu listu
workbook.Worksheets.RemoveAt(0);
```

## Krok 5: Uložte sešit

 Po odstranění listu můžete upravený sešit aplikace Excel uložit pomocí`Save()` metoda`Workbook` objekt.

```csharp
// Uložte sešit aplikace Excel
workbook.Save(dataDir + "output.out.xls");
```


### Ukázkový zdrojový kód pro výukový program Delete Excel Worksheet By Index C# pomocí Aspose.Cells for .NET 
```csharp
//Cesta k adresáři dokumentů.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Vytvoření datového proudu souboru obsahujícího soubor Excel, který se má otevřít
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Vytvoření instance objektu sešitu
// Otevření souboru aplikace Excel prostřednictvím datového proudu souborů
Workbook workbook = new Workbook(fstream);
//Odebrání listu pomocí jeho indexu listu
workbook.Worksheets.RemoveAt(0);
// Uložit sešit
workbook.Save(dataDir + "output.out.xls");
```

## Závěr

V tomto tutoriálu jsme se zabývali podrobným procesem odstranění listu aplikace Excel podle indexu pomocí Aspose.Cells pro .NET. Podle uvedených příkladů kódu a poskytnutých vysvětlení byste nyní měli dobře rozumět tomu, jak provést tento úkol ve vašich aplikacích C#. Aspose.Cells for .NET nabízí komplexní sadu funkcí pro práci se soubory aplikace Excel, což umožňuje snadnou manipulaci s listy a souvisejícími daty.

### Často kladené otázky (FAQ)

#### Co je Aspose.Cells pro .NET?

Aspose.Cells for .NET je výkonná knihovna, která umožňuje vývojářům vytvářet, manipulovat a převádět soubory Excel v jejich aplikacích .NET. Nabízí širokou škálu funkcí pro práci s listy, buňkami, vzorci, styly a dalšími.

#### Jak mohu nainstalovat Aspose.Cells pro .NET?

Chcete-li nainstalovat Aspose.Cells pro .NET, můžete si stáhnout instalační balíček z Aspose Releases (https://releases.aspose.com/cells/net) a postupujte podle uvedených pokynů. K používání knihovny ve vašich aplikacích budete potřebovat platnou licenci.

#### Mohu odstranit více listů najednou?

Ano, pomocí Aspose.Cells for .NET můžete odstranit více listů. Krok odstranění můžete jednoduše zopakovat pro každý list, který chcete odstranit.

#### Je možné obnovit smazaný list?

Bohužel, jakmile je list odstraněn, nelze jej obnovit přímo ze souboru aplikace Excel. Před odstraněním listu se doporučuje vytvořit zálohu souboru Excel, aby nedošlo ke ztrátě dat.

#### Je Aspose.Cells for .NET kompatibilní s různými verzemi Excelu?

Ano, Aspose.Cells for .NET je kompatibilní s různými verzemi Excelu včetně Excel 2003, Excel 2007, Excel 2010, Excel 2013, Excel 2016, Excel 2019 a Excel pro Office 365. Podporuje formáty souborů .xls a .xlsx.