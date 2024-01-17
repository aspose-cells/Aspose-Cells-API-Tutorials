---
title: Přidat nový list ve výukovém programu Excel C#
linktitle: Přidat nový list v aplikaci Excel
second_title: Aspose.Cells for .NET API Reference
description: Přečtěte si, jak přidat nový list v Excelu pomocí Aspose.Cells for .NET. Krok za krokem tutoriál se zdrojovým kódem v C#.
type: docs
weight: 20
url: /cs/net/excel-worksheet-csharp-tutorials/add-new-sheet-in-excel-csharp-tutorial/
---
tomto tutoriálu krok za krokem vysvětlíme zdrojový kód C# pro přidání nového listu v Excelu pomocí Aspose.Cells for .NET. Přidání nového listu do sešitu aplikace Excel je běžnou operací při vytváření sestav nebo manipulaci s daty. Aspose.Cells je výkonná knihovna, která usnadňuje manipulaci a generování souborů Excel pomocí .NET. Chcete-li tento kód pochopit a implementovat, postupujte podle následujících kroků.

## Krok 1: Nastavení adresáře dokumentů

Prvním krokem je definování adresáře dokumentu, kam bude soubor Excel uložen. Pokud adresář neexistuje, vytvoříme jej pomocí následujícího kódu:

```csharp
//Cesta k adresáři dokumentů.
string dataDir = "YOUR DOCUMENTS DIRECTORY";
// Vytvořte adresář, pokud ještě neexistuje.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
System.IO.Directory.CreateDirectory(dataDir);
```

Nezapomeňte nahradit „VAŠE ADRESÁŘ DOKUMENTŮ“ příslušnou cestou k adresáři vašich dokumentů.

## Krok 2: Vytvoření instance objektu sešitu

Druhým krokem je vytvoření instance objektu Workbook, který představuje sešit aplikace Excel. Použijte následující kód:

```csharp
Workbook workbook = new Workbook();
```

Tento objekt bude použit k přidání nového listu a provádění dalších operací v sešitu aplikace Excel.

## Krok 3: Přidání nového listu

Třetím krokem je přidání nového listu do objektu Sešit. Použijte následující kód:

```csharp
int index = workbook. Worksheets. Add();
Worksheet worksheet = workbook.Worksheets[index];
```

Tím se do objektu Workbook přidá nový list a získáte odkaz na tento list pomocí jeho indexu.

## Krok 4: Nastavení názvu nového listu

Čtvrtým krokem je pojmenování nového listu. K nastavení názvu listu můžete použít následující kód:

```csharp
worksheet.Name = "My Worksheet";
```

Nahraďte "My Spreadsheet" požadovaným názvem pro nový list.

## Krok 5: Uložení souboru Excel

Nakonec posledním krokem je uložení souboru Excel. Použijte následující kód:

```csharp
string filePath = dataDir + "output.out.xls";
workbook.Save(filePath);
```

Tím se sešit aplikace Excel s novým listem uloží do vámi určeného adresáře dokumentů.

### Ukázkový zdrojový kód pro Add New Sheet In Excel C# Tutorial pomocí Aspose.Cells for .NET 
```csharp
//Cesta k adresáři dokumentů.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Vytvořte adresář, pokud ještě není přítomen.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
	System.IO.Directory.CreateDirectory(dataDir);
// Vytvoření instance objektu sešitu
Workbook workbook = new Workbook();
// Přidání nového listu do objektu Sešit
int i = workbook.Worksheets.Add();
// Získání odkazu na nově přidaný list předáním jeho indexu listu
Worksheet worksheet = workbook.Worksheets[i];
// Nastavení názvu nově přidaného listu
worksheet.Name = "My Worksheet";
// Uložení souboru Excel
workbook.Save(dataDir + "output.out.xls");
```

## Závěr

Nyní jste se naučili, jak přidat nový list v aplikaci Excel pomocí Aspose.Cells pro .NET. Tuto metodu můžete použít k manipulaci a generování souborů Excel pomocí C#. Aspose.Cells nabízí mnoho výkonných funkcí pro zjednodušení manipulace se soubory aplikace Excel ve vašich aplikacích.

### Často kladené otázky (FAQ)

#### Mohu používat Aspose.Cells s jinými programovacími jazyky než C#?

Ano, Aspose.Cells podporuje více programovacích jazyků, jako je Java, Python, Ruby a mnoho dalších.

#### Mohu přidat formátování do buněk v nově vytvořeném listu?

Ano, můžete použít formátování na buňky pomocí metod poskytovaných třídou Worksheet Aspose.Cells. Můžete nastavit styl buňky, změnit barvu pozadí, použít ohraničení atd.

#### Jak získám přístup k datům buněk z nového listu?

K datům buněk můžete přistupovat pomocí vlastností a metod poskytovaných třídou Worksheet Aspose.Cells. Můžete například použít vlastnost Cells pro přístup ke konkrétní buňce a načtení nebo úpravu její hodnoty.

#### Podporuje Aspose.Cells vzorce v Excelu?

Ano, Aspose.Cells podporuje vzorce Excelu. Vzorce v buňkách listu můžete nastavit pomocí metody SetFormula třídy Cell.
