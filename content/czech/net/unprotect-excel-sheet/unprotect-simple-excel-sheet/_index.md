---
title: Odemkněte jednoduchý list Excelu
linktitle: Odemkněte jednoduchý list Excelu
second_title: Aspose.Cells for .NET API Reference
description: Přečtěte si, jak zrušit ochranu tabulky Excel pomocí Aspose.Cells pro .NET. Výukový program krok za krokem v C#.
type: docs
weight: 30
url: /cs/net/unprotect-excel-sheet/unprotect-simple-excel-sheet/
---
V tomto tutoriálu vás provedeme kroky potřebnými k odemknutí jednoduché tabulky Excel pomocí knihovny Aspose.Cells pro .NET.

## Krok 1: Příprava prostředí

Než začnete, ujistěte se, že máte na svém počítači nainstalovaný Aspose.Cells for .NET. Stáhněte si knihovnu z oficiálních stránek Aspose a postupujte podle dodaných pokynů k instalaci.

## Krok 2: Konfigurace cesty k adresáři dokumentu

 V poskytnutém zdrojovém kódu musíte zadat cestu k adresáři, kde se nachází soubor Excel, který chcete odemknout. Upravte`dataDir` proměnnou nahrazením "VÁŠ ADRESÁŘ DOKUMENTŮ" absolutní cestou k adresáři na vašem počítači.

```csharp
//Cesta k adresáři dokumentů.
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
```

## Krok 3: Vytvoření objektu sešitu

Chcete-li začít, musíme vytvořit objekt Workbook, který představuje náš soubor Excel. Použijte konstruktor třídy Workbook a zadejte úplnou cestu k souboru Excel, který chcete otevřít.

```csharp
// Vytvoření instance objektu sešitu
Workbook workbook = new Workbook(dataDir + "book1.xls");
```

## Krok 4: Přístup k tabulce

 Dále musíme přejít na první list v souboru aplikace Excel. Použijte`Worksheets` vlastnost objektu Workbook pro přístup ke kolekci listů, pak použijte`[0]` index pro přístup k prvnímu listu.

```csharp
// Přístup k prvnímu listu v souboru aplikace Excel
Worksheet worksheet = workbook.Worksheets[0];
```

## Krok 5: Odemknutí tabulky

 Nyní odemkneme list pomocí`Unprotect()` metoda objektu Worksheet. Tato metoda nevyžaduje heslo.

```csharp
// Zrušení ochrany listu bez hesla
worksheet.Unprotect();
```

## Krok 6: Uložení odemčeného souboru Excel

Jakmile je tabulka odemčena, můžeme uložit konečný soubor Excel. Použijte`Save()` k zadání úplné cesty výstupního souboru a formátu uložení.

```csharp
// Uložení sešitu
workbook.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```
### Ukázka zdrojového kódu pro Unprotect Simple Excel Sheet pomocí Aspose.Cells pro .NET 
```csharp
//Cesta k adresáři dokumentů.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Vytvoření instance objektu sešitu
Workbook workbook = new Workbook(dataDir + "book1.xls");
// Přístup k prvnímu listu v souboru aplikace Excel
Worksheet worksheet = workbook.Worksheets[0];
// Zrušení ochrany listu bez hesla
worksheet.Unprotect();
// Uložení sešitu
workbook.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## Závěr

gratuluji! Nyní jste se naučili, jak odemknout jednoduchou excelovou tabulku pomocí Aspose.Cells pro .NET. Podle kroků v tomto kurzu můžete tuto funkci snadno použít na své vlastní projekty.

Neváhejte a prozkoumejte další funkce Aspose.Cells
pro pokročilejší operace se soubory Excel.

### Nejčastější dotazy

#### Otázka: Jaká opatření mám učinit při odemykání tabulky Excel?

Odpověď: Při odemykání tabulky aplikace Excel se ujistěte, že máte potřebná oprávnění pro přístup k souboru. Ujistěte se také, že používáte správnou metodu odemknutí a zadejte správné heslo, pokud je to možné.

#### Otázka: Jak zjistím, zda je tabulka chráněna heslem?

 Odpověď: Můžete zkontrolovat, zda je list chráněn heslem, pomocí vlastností nebo metod poskytovaných knihovnou Aspose.Cells pro .NET. Můžete například použít`IsProtected()` metoda objektu Worksheet pro kontrolu, zda je list chráněn.

#### Otázka: Při pokusu o odemknutí tabulky dostávám výjimku. Co bych měl dělat ?

Odpověď: Pokud při odemykání tabulky narazíte na výjimku, ujistěte se, že jste správně zadali cestu k souboru aplikace Excel a zkontrolujte, zda máte potřebná oprávnění k přístupu k němu. Pokud problém přetrvává, neváhejte kontaktovat podporu Aspose.Cells pro další pomoc.