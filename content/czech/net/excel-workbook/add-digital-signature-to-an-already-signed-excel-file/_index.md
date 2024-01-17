---
title: Přidejte digitální podpis do již podepsaného souboru aplikace Excel
linktitle: Přidejte digitální podpis do již podepsaného souboru aplikace Excel
second_title: Aspose.Cells for .NET API Reference
description: Snadno přidávejte digitální podpisy do stávajících souborů aplikace Excel pomocí Aspose.Cells pro .NET.
type: docs
weight: 30
url: /cs/net/excel-workbook/add-digital-signature-to-an-already-signed-excel-file/
---
V tomto podrobném průvodci vysvětlíme poskytnutý zdrojový kód C#, který vám umožní přidat digitální podpis do již podepsaného souboru Excel pomocí Aspose.Cells for .NET. Chcete-li přidat nový digitální podpis do existujícího souboru aplikace Excel, postupujte podle následujících kroků.

## Krok 1: Nastavte zdrojový a výstupní adresář

```csharp
// zdrojový adresář
string sourceDir = RunExamples.Get_SourceDirectory();

// Výstupní adresář
string outputDir = RunExamples.Get_OutputDirectory();
```

tomto prvním kroku definujeme zdrojové a výstupní adresáře, které budou použity k načtení stávajícího souboru Excel a uložení souboru s novým digitálním podpisem.

## Krok 2: Načtěte existující soubor Excel

```csharp
// Načtěte již podepsaný excelový sešit
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
```

 Zde načteme již podepsaný soubor Excel pomocí`Workbook` třídy Aspose.Cells.

## Krok 3: Vytvořte kolekci digitálních podpisů

```csharp
// Vytvořte kolekci digitálních podpisů
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
```

 Vytváříme novou kolekci digitálních podpisů pomocí`DigitalSignatureCollection` třída.

## Krok 4: Vytvořte nový certifikát

```csharp
// Vytvořte nový certifikát
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
```

Zde vytvoříme nový certifikát z poskytnutého souboru a hesla.

## Krok 5: Přidejte do sbírky nový digitální podpis

```csharp
// Vytvořte nový digitální podpis
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added a new digital signature to the already signed workbook.", DateTime.Now);

// Přidejte digitální podpis do sbírky
dsCollection.Add(signature);
```

 Vytvoříme nový digitální podpis pomocí`DigitalSignature` třídy a přidejte jej do sbírky digitálních podpisů.

## Krok 6: Přidejte do sešitu kolekci digitálních podpisů

```csharp
//Přidejte kolekci digitálních podpisů do sešitu
workbook.AddDigitalSignature(dsCollection);
```

 Sbírku digitálních podpisů přidáváme do stávajícího excelového sešitu pomocí`AddDigitalSignature()` metoda.

## Krok 7: Uložte a zavřete sešit

```csharp
// Uložte sešit a zavřete jej
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
```

Sešit s novým digitálním podpisem uložíme do určeného výstupního adresáře, poté jej zavřeme a uvolníme související prostředky.

### Ukázkový zdrojový kód pro přidání digitálního podpisu do již podepsaného souboru aplikace Excel pomocí Aspose.Cells for .NET 
```csharp
//Zdrojový adresář
string sourceDir = RunExamples.Get_SourceDirectory();
//Výstupní adresář
string outputDir = RunExamples.Get_OutputDirectory();
//Soubor certifikátu a jeho heslo
string certFileName = sourceDir + "AsposeDemo.pfx";
string password = "aspose";
//Chcete-li přidat nový digitální podpis, načtěte sešit, který je již digitálně podepsán
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
//Vytvořte kolekci digitálních podpisů
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
//Vytvořte nový certifikát
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
//Vytvořte nový digitální podpis a přidejte jej do sbírky digitálních podpisů
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added new digital signature in existing digitally signed workbook.", DateTime.Now);
dsCollection.Add(signature);
//Přidejte do sešitu kolekci digitálních podpisů
workbook.AddDigitalSignature(dsCollection);
//Uložte sešit a zlikvidujte jej.
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
Console.WriteLine("AddDigitalSignatureToAnAlreadySignedExcelFile executed successfully.\r\n");
```

## Závěr

gratuluji! Nyní jste se naučili, jak přidat digitální podpis do již podepsaného souboru Excel pomocí Aspose.Cells for .NET. Digitální podpisy dodávají vašim souborům Excel další vrstvu zabezpečení a zajišťují jejich pravost a integritu.

### FAQ

#### Otázka: Co je Aspose.Cells pro .NET?

Odpověď: Aspose.Cells for .NET je výkonná knihovna tříd, která umožňuje vývojářům .NET snadno vytvářet, upravovat, převádět a manipulovat se soubory aplikace Excel.

#### Otázka: Co je digitální podpis v souboru aplikace Excel?

Odpověď: Digitální podpis v souboru Excel je elektronická značka, která zaručuje pravost, integritu a původ dokumentu. Používá se k ověření, že soubor nebyl od podepsání změněn a pochází ze spolehlivého zdroje.

#### Otázka: Jaké jsou výhody přidání digitálního podpisu do souboru aplikace Excel?

Odpověď: Přidání digitálního podpisu do souboru Excel poskytuje několik výhod, včetně ochrany proti neoprávněným změnám, zajištění integrity dat, ověření autora dokumentu a poskytnutí důvěry v informace, které obsahuje.

#### Otázka: Mohu do souboru aplikace Excel přidat více digitálních podpisů?

Odpověď: Ano, Aspose.Cells vám umožňuje přidat více digitálních podpisů do souboru aplikace Excel. Můžete vytvořit kolekci digitálních podpisů a přidat je do souboru v jedné operaci.

#### Otázka: Jaké jsou požadavky na přidání digitálního podpisu do souboru aplikace Excel?

Odpověď: Chcete-li přidat digitální podpis do souboru aplikace Excel, potřebujete platný digitální certifikát, který bude použit k podepsání dokumentu. Před přidáním digitálního podpisu se ujistěte, že máte správný certifikát a heslo.