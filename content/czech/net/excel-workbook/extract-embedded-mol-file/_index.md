---
title: Extrahujte vložený soubor Mol
linktitle: Extrahujte vložený soubor Mol
second_title: Aspose.Cells for .NET API Reference
description: Naučte se snadno extrahovat vložené soubory MOL z excelového sešitu pomocí Aspose.Cells for .NET.
type: docs
weight: 90
url: /cs/net/excel-workbook/extract-embedded-mol-file/
---
V tomto tutoriálu vás provedeme krok za krokem, jak extrahovat vložený soubor MOL ze sešitu aplikace Excel pomocí knihovny Aspose.Cells pro .NET. Naučíte se, jak procházet listy sešitu, extrahovat odpovídající objekty OLE a ukládat extrahované soubory MOL. Pro úspěšné dokončení tohoto úkolu postupujte podle následujících kroků.

## Krok 1: Definujte zdrojový a výstupní adresář
Nejprve musíme definovat zdrojový a výstupní adresář v našem kódu. Tyto adresáře označují, kde se nachází zdrojový excelový sešit a kam budou uloženy extrahované soubory MOL. Zde je odpovídající kód:

```csharp
// Adresáře
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
```

Ujistěte se, že jste podle potřeby určili vhodné cesty.

## Krok 2: Načtení sešitu aplikace Excel
Dalším krokem je načtení sešitu aplikace Excel obsahující vložené objekty OLE a soubory MOL. Zde je kód pro načtení sešitu:

```csharp
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
```

Ujistěte se, že jste v kódu správně zadali název zdrojového souboru.

## Krok 3: Projděte listy a extrahujte soubory MOL
Nyní budeme procházet každý list v sešitu a extrahovat odpovídající objekty OLE, které obsahují soubory MOL. Zde je odpovídající kód:

```csharp
var index = 1;
foreach(Worksheet sheet in workbook.Worksheets)
{
     OleObjectCollection oles = sheet.OleObjects;
     foreach(OleObject ole in oles)
     {
         string fileName = outputDir + "OleObject" + index + ".mol";
         FileStream fs = File.Create(fileName);
         fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
         fs. Close();
         index++;
     }
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

Tento kód prochází každý list v sešitu, načte objekty OLE a uloží extrahované soubory MOL do výstupního adresáře.

### Ukázka zdrojového kódu pro Extract Embedded Mol File pomocí Aspose.Cells pro .NET 
```csharp
//adresáře
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
var index = 1;
foreach (Worksheet sheet in workbook.Worksheets)
{
	OleObjectCollection oles = sheet.OleObjects;
	foreach (OleObject ole in oles)
	{
		string fileName = outputDir + "OleObject" + index + ".mol ";
		FileStream fs = File.Create(fileName);
		fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
		fs.Close();
		index++;
	}
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

## Závěr
gratuluji! Naučili jste se, jak extrahovat vložený soubor MOL z excelového sešitu pomocí Aspose.Cells for .NET. Nyní můžete tyto znalosti použít k extrahování souborů MOL z vašich vlastních excelových sešitů. Neváhejte prozkoumat knihovnu Aspose.Cells dále a dozvědět se o jejích dalších výkonných funkcích.

### Nejčastější dotazy

#### Otázka: Co je soubor MOL?
 
Odpověď: Soubor MOL je formát souboru používaný k reprezentaci chemických struktur ve výpočetní chemii. Obsahuje informace o atomech, vazbách a dalších molekulárních vlastnostech.

#### Otázka: Funguje tato metoda se všemi typy souborů aplikace Excel?

Odpověď: Ano, tato metoda funguje se všemi typy souborů Excel podporovanými Aspose.Cells.

#### Otázka: Mohu extrahovat více souborů MOL najednou?

Odpověď: Ano, můžete extrahovat více souborů MOL najednou procházením objektů OLE na každém listu v sešitu.