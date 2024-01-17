---
title: Upravit rozsahy v listu aplikace Excel
linktitle: Upravit rozsahy v listu aplikace Excel
second_title: Aspose.Cells for .NET API Reference
description: Naučte se upravovat konkrétní rozsahy v excelové tabulce pomocí Aspose.Cells pro .NET. Výukový program krok za krokem v C#.
type: docs
weight: 20
url: /cs/net/protect-excel-file/edit-ranges-in-excel-worksheet/
---
Microsoft Excel je výkonný nástroj pro vytváření a správu tabulek, který nabízí mnoho funkcí pro kontrolu a zabezpečení dat. Jednou z takových funkcí je umožnit uživatelům upravovat určité rozsahy v listu a zároveň chránit ostatní části. V tomto tutoriálu vás krok za krokem provedeme implementací této funkce pomocí Aspose.Cells for .NET, oblíbené knihovny pro programovou práci se soubory Excelu.

Použití Aspose.Cells for .NET vám umožní snadno manipulovat s rozsahy v tabulkovém procesoru Excel, poskytuje uživatelsky přívětivé rozhraní a pokročilé funkce. Chcete-li uživatelům umožnit upravovat konkrétní rozsahy v tabulce Excel pomocí Aspose.Cells for .NET, postupujte podle níže uvedených kroků.
## Krok 1: Nastavení prostředí

Ujistěte se, že máte ve vývojovém prostředí nainstalovaný Aspose.Cells for .NET. Stáhněte si knihovnu z oficiálních stránek Aspose a podívejte se do dokumentace pro pokyny k instalaci.

## Krok 2: Inicializace sešitu a listu

Chcete-li začít, musíme vytvořit nový sešit a získat odkaz na list, kde chceme povolit změny rozsahů. K tomu použijte následující kód:

```csharp
// Cesta k adresáři dokumentů.
string dataDir = "YOUR DOCUMENTS DIRECTORY";
// Vytvořte adresář, pokud ještě neexistuje.
bool exists = System.IO.Directory.Exists(dataDir);
if (! exists)
     System.IO.Directory.CreateDirectory(dataDir);

// Vytvořte instanci nového sešitu
Workbook workbook = new Workbook();

// Získat první list (výchozí)
Worksheet sheet = workbook.Worksheets[0];
```

 V tomto úryvku kódu nejprve definujeme cestu k adresáři, kam bude soubor Excel uložen. Dále vytvoříme novou instanci`Workbook` třídy a získejte odkaz na první pracovní list pomocí`Worksheets` vlastnictví.

## Krok 3: Získejte upravitelné rozsahy

Nyní musíme načíst rozsahy, ve kterých chceme povolit úpravy. Použijte následující kód:

```csharp
// Získejte upravitelné rozsahy
ProtectedRangeCollection EditableRanges = Sheet.AllowEditRanges;
```

## Krok 4: Nastavte chráněný rozsah

Před povolením úprav rozsahů musíme definovat chráněný rozsah. Zde je postup:

```csharp
// Definujte chráněný rozsah
ProtectedRange ProtectedRange;

// Vytvořte rozsah
int index = ModifiableRanges.Add("r2", 1, 1, 3, 3);
rangeProtected = rangesEditable[index];
```

 V tomto kódu vytvoříme novou instanci`ProtectedRange` třídy a použijte`Add` metoda k určení rozsahu, který se má chránit.

## Krok 5: Zadejte heslo

Chcete-li zvýšit zabezpečení, můžete zadat heslo pro chráněný rozsah. Zde je postup:

```csharp
// Zadejte heslo
protectedBeach.Password = "YOUR_PASSWORD";
```

## Krok 6: Chraňte pracovní list

Nyní, když jsme nastavili chráněný rozsah, můžeme chránit list, aby se zabránilo neoprávněným úpravám. Použijte následující kód:

```csharp
// Chraňte pracovní list
leaf.Protect(ProtectionType.All);
```

## Krok 7: Uložte soubor Excel

Nakonec uložíme soubor Excel s provedenými změnami. Zde je potřebný kód:

```csharp
// Uložte soubor aplikace Excel
workbook.Save(dataDir + "protectedrange.out.xls");
```

### Ukázkový zdrojový kód pro úpravy rozsahů v pracovním listu aplikace Excel pomocí Aspose.Cells pro .NET 
```csharp
//Cesta k adresáři dokumentů.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Vytvořte adresář, pokud ještě není přítomen.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);

// Vytvořte nový sešit
Workbook book = new Workbook();

// Získejte první (výchozí) list
Worksheet sheet = book.Worksheets[0];

// Získejte možnosti Povolit úpravy rozsahů
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;

// Definujte ProtectedRange
ProtectedRange proteced_range;

// Vytvořte rozsah
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
proteced_range = allowRanges[idx];

// Zadejte heslo
proteced_range.Password = "YOUR_PASSWORD";

// Chraňte list
sheet.Protect(ProtectionType.All);

// Uložte soubor aplikace Excel
book.Save(dataDir + "protectedrange.out.xls");
```

## Závěr

gratuluji! Naučili jste se, jak umožnit uživatelům upravovat konkrétní rozsahy v excelové tabulce pomocí Aspose.Cells for .NET. Nyní můžete tuto techniku použít ve svých vlastních projektech a zlepšit zabezpečení souborů aplikace Excel.


#### Nejčastější dotazy

#### Otázka: Proč bych měl používat Aspose.Cells for .NET k úpravě rozsahů v tabulce aplikace Excel?

Odpověď: Aspose.Cells for .NET nabízí výkonné a snadno použitelné rozhraní API pro práci se soubory aplikace Excel. Poskytuje pokročilé funkce, jako je manipulace s rozsahem, ochrana listu atd.

#### Otázka: Mohu v listu nastavit více upravitelných rozsahů?

 Odpověď: Ano, můžete definovat více upravitelných rozsahů pomocí`Add` metoda`ProtectedRangeCollection` sbírka. Každý rozsah může mít vlastní nastavení ochrany.

####  Otázka: Je možné odstranit upravitelný rozsah po jeho definování?

 Odpověď: Ano, můžete použít`RemoveAt` metoda`ProtectedRangeCollection` kolekce k odstranění konkrétního upravitelného rozsahu zadáním jeho indexu.

#### Otázka: Jak mohu otevřít chráněný soubor Excel po jeho uložení?

Odpověď: Chcete-li otevřít chráněný soubor Excel, budete muset zadat heslo zadané při vytváření chráněného rozsahu. Heslo uschovejte na bezpečném místě, abyste zabránili ztrátě přístupu k datům.