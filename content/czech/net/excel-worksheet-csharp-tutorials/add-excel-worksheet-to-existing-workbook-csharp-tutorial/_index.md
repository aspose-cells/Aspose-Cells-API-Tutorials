---
title: Přidat pracovní list aplikace Excel do existujícího sešitu C# Tutoriál
linktitle: Přidat sešit Excel do existujícího sešitu
second_title: Aspose.Cells for .NET API Reference
description: Pomocí Aspose.Cells for .NET můžete snadno přidat nový list do existujícího sešitu aplikace Excel. Výukový program krok za krokem s příklady kódu.
type: docs
weight: 10
url: /cs/net/excel-worksheet-csharp-tutorials/add-excel-worksheet-to-existing-workbook-csharp-tutorial/
---
V tomto tutoriálu vás krok za krokem provedeme vysvětlením níže uvedeného zdrojového kódu C#, který pomáhá přidat nový list do existujícího sešitu aplikace Excel pomocí Aspose.Cells for .NET. Ke každému kroku zahrneme ukázkový kód, který vám pomůže podrobně porozumět procesu.

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

## Krok 4: Přidejte do sešitu nový list

 Chcete-li do sešitu přidat nový list, můžete použít`Worksheets.Add()` metoda`Workbook` objekt. Tato metoda vrátí index nově přidaného listu.

```csharp
// Přidejte nový list do sešitu
int i = workbook. Worksheets. Add();
```

## Krok 5: Nastavte název nového listu

 Název nově přidaného listu můžete nastavit pomocí`Name` vlastnictvím`Worksheet` objekt.

```csharp
// Získejte odkaz na nový přidaný list předáním jeho indexu listu
Worksheet worksheet = workbook.Worksheets[i];
// Definujte název nového listu
worksheet.Name = "My Worksheet";
```

## Krok 6: Uložte soubor Excel

 Jakmile přidáte nový list a nastavíte jeho název, můžete upravený soubor Excel uložit pomocí`Save()` metoda`Workbook` objekt.

```csharp
// Uložte soubor aplikace Excel
workbook.Save(dataDir + "output.out.xls");
```

## Krok 7: Zavřete Streamování souborů a Uvolněte zdroje

Nakonec je důležité zavřít datový proud souboru, aby se uvolnily všechny prostředky s ním spojené.

```csharp
// Zavřete datový proud souboru, abyste uvolnili všechny prostředky
fstream.Close();
```

### Ukázkový zdrojový kód pro Add Excel Worksheet to Existing Workbook C# Tutorial pomocí Aspose.Cells for .NET 
```csharp
//Cesta k adresáři dokumentů.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Vytvoření datového proudu souboru obsahujícího soubor Excel, který se má otevřít
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Vytvoření instance objektu sešitu
// Otevření souboru aplikace Excel prostřednictvím datového proudu souborů
Workbook workbook = new Workbook(fstream);
// Přidání nového listu do objektu Sešit
int i = workbook.Worksheets.Add();
// Získání odkazu na nově přidaný list předáním jeho indexu listu
Worksheet worksheet = workbook.Worksheets[i];
// Nastavení názvu nově přidaného listu
worksheet.Name = "My Worksheet";
// Uložení souboru Excel
workbook.Save(dataDir + "output.out.xls");
// Zavřením datového proudu souborů uvolníte všechny zdroje
fstream.Close();
```

## Závěr

V tomto tutoriálu jsme probrali krok za krokem proces přidávání nového fire Connect do existujícího excelového sešitu pomocí Aspose.Cells for .NET. Podle uvedených příkladů kódu a poskytnutých vysvětlení byste nyní měli dobře rozumět tomu, jak provést tento úkol ve vašich aplikacích C#. Aspose.Cells for .NET nabízí komplexní sadu funkcí pro práci se soubory aplikace Excel, což vám umožní efektivně automatizovat různé úkoly související s Excelem.

### Často kladené otázky (FAQ)

#### Co je Aspose.Cells pro .NET?

Aspose.Cells for .NET je výkonná knihovna .NET, která umožňuje vývojářům vytvářet, manipulovat a převádět soubory aplikace Excel v jejich aplikacích. Nabízí širokou škálu funkcí pro práci s tabulkami, buňkami, vzorci, styly a dalšími.

#### Jak mohu nainstalovat Aspose.Cells pro .NET?

Chcete-li nainstalovat Aspose.Cells pro .NET, můžete si stáhnout instalační balíček z Aspose Releases (https://releases.aspose.com/cells/net) a postupujte podle dodaných pokynů k instalaci. K používání knihovny ve vašich aplikacích budete také potřebovat platnou licenci.

#### Mohu přidat více tabulek pomocí Aspose.Cells pro .NET?

 Ano, pomocí Aspose.Cells for .NET můžete do jednoho souboru aplikace Excel přidat více listů. Můžete použít`Worksheets.Add()` metoda`Workbook` objekt pro přidání nových listů na různá místa v sešitu.

#### Jak mohu formátovat buňky v souboru aplikace Excel?

Aspose.Cells for .NET nabízí různé metody a vlastnosti formátování buněk v souboru aplikace Excel. Můžete nastavit hodnoty buněk, použít možnosti formátování, jako je styl písma, barva, zarovnání, ohraničení a další. Podrobnější informace o formátování buněk naleznete v dokumentaci a ukázkovém kódu poskytnutém Aspose.Cells.

#### Je Aspose.Cells for .NET kompatibilní s různými verzemi Excelu?

Ano, Aspose.Cells for .NET je kompatibilní s různými verzemi Excelu včetně Excel 2003, Excel 2007, Excel 2010, Excel 2013, Excel 2016, Excel 2019 a Excel pro Office 365. Podporuje formát .xls i novější . formát xlsx.