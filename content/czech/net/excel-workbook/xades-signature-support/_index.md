---
title: Podpora podpisů Xades
linktitle: Podpora podpisů Xades
second_title: Aspose.Cells for .NET API Reference
description: Naučte se, jak přidat podpis Xades do souboru aplikace Excel pomocí Aspose.Cells for .NET.
type: docs
weight: 190
url: /cs/net/excel-workbook/xades-signature-support/
---
tomto článku vás krok za krokem provedeme vysvětlením níže uvedeného zdrojového kódu C#, který se týká podpory podpisů Xades pomocí knihovny Aspose.Cells pro .NET. Zjistíte, jak pomocí této knihovny přidat digitální podpis Xades do souboru aplikace Excel. Poskytneme vám také přehled o procesu podepisování a jeho provedení. Chcete-li získat přesvědčivé výsledky, postupujte podle níže uvedených kroků.

## Krok 1: Definujte zdrojový a výstupní adresář
Abychom mohli začít, musíme v našem kódu definovat zdrojový a výstupní adresář. Tyto adresáře označují, kde jsou umístěny zdrojové soubory a kde bude uložen výstupní soubor. Zde je odpovídající kód:

```csharp
// Zdrojový adresář
string sourceDir = RunExamples.Get_SourceDirectory();
// Výstupní adresář
string outputDir = RunExamples.Get_OutputDirectory();
```

Nezapomeňte upravit cesty k adresářům podle potřeby.

## Krok 2: Načtení sešitu aplikace Excel
Dalším krokem je načtení excelového sešitu, do kterého chceme přidat digitální podpis Xades. Zde je kód pro načtení sešitu:

```csharp
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
```

Ujistěte se, že jste v kódu správně zadali název zdrojového souboru.

## Krok 3: Konfigurace digitálního podpisu
Nyní nakonfigurujeme digitální podpis Xades poskytnutím potřebných informací. Musíme zadat soubor PFX obsahující digitální certifikát a také související heslo. Zde je odpovídající kód:

```csharp
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
```

Nezapomeňte nahradit „pfxPassword“ svým skutečným heslem a „pfxFile“ cestou k souboru PFX.

## Krok 4: Přidání digitálního podpisu
Nyní, když jsme nakonfigurovali digitální podpis, můžeme jej přidat do sešitu aplikace Excel. Zde je odpovídající kód:

```csharp
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
```

Tento krok přidá digitální podpis Xades do sešitu aplikace Excel.

## Krok 5: Uložení sešitu s podpisem
Nakonec sešit Excel uložíme s přidaným digitálním podpisem. Zde je odpovídající kód:

```csharp
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
```

Nezapomeňte upravit název výstupního souboru podle svých potřeb.

### Ukázkový zdrojový kód pro Xades Signature Support pomocí Aspose.Cells pro .NET 
```csharp
//Zdrojový adresář
string sourceDir = RunExamples.Get_SourceDirectory();
//Výstupní adresář
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
Console.WriteLine("XAdESSignatureSupport executed successfully.");
```

## Závěr
gratuluji! Naučili jste se používat knihovnu Aspose.Cells pro .NET k přidání digitálního podpisu Xades do souboru aplikace Excel. Podle kroků uvedených v tomto článku budete moci implementovat tuto funkci do svých vlastních projektů. Nebojte se s knihovnou více experimentovat a objevovat další výkonné funkce, které nabízí.

### Nejčastější dotazy

#### Otázka: Co je Xades?

Odpověď: Xades je pokročilý standard elektronického podpisu používaný k zajištění integrity a pravosti digitálních dokumentů.

#### Otázka: Mohu s Aspose.Cells používat jiné typy digitálních podpisů?

Odpověď: Ano, Aspose.Cells také podporuje jiné typy digitálních podpisů, jako jsou podpisy XMLDSig a podpisy PKCS#7.

#### Otázka: Mohu použít podpis na jiné typy souborů než soubory Excel?
 
Odpověď: Ano, Aspose.Cells také umožňuje použití digitálních podpisů na další podporované typy souborů, jako jsou soubory Word, PDF a PowerPoint.