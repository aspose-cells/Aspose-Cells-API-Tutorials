---
title: Přidat webové rozšíření
linktitle: Přidat webové rozšíření
second_title: Aspose.Cells for .NET API Reference
description: Pomocí Aspose.Cells for .NET můžete snadno přidat webové rozšíření do sešitů aplikace Excel.
type: docs
weight: 40
url: /cs/net/excel-workbook/add-web-extension/
---
V tomto tutoriálu krok za krokem vysvětlíme poskytnutý zdrojový kód C#, který vám umožní přidat webové rozšíření pomocí Aspose.Cells for .NET. Chcete-li do sešitu aplikace Excel přidat webové rozšíření, postupujte podle následujících kroků.

## Krok 1: Nastavte výstupní adresář

```csharp
// Výstupní adresář
string outDir = RunExamples.Get_OutputDirectory();
```

V tomto prvním kroku definujeme výstupní adresář, kam bude uložen upravený excelový sešit.

## Krok 2: Vytvořte nový sešit

```csharp
// Vytvořte nový sešit
Workbook workbook = new Workbook();
```

Zde vytváříme nový excelový sešit pomocí`Workbook` třídy od Aspose.Cells.

## Krok 3: Přístup ke kolekci webových rozšíření

```csharp
// Přístup ke kolekci webových rozšíření
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
```

 Ke kolekci webových rozšíření v excelovém sešitu přistupujeme pomocí`WebExtensions` vlastnictvím`Worksheets` objekt.

## Krok 4: Přidejte nové webové rozšíření

```csharp
// Přidejte nové webové rozšíření
int extensionIndex = extensions.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
```

Do kolekce rozšíření přidáváme nové webové rozšíření. Definujeme referenční ID, název obchodu a typ obchodu rozšíření.

## Krok 5: Přístup ke kolekci podokna úloh pro rozšíření webu

```csharp
// Přístup ke kolekci podokna úloh webového rozšíření
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
```

 Ke kolekci podoken úloh rozšíření Excel Workbook Web Extension přistupujeme pomocí`WebExtensionTaskPanes` vlastnictvím`Worksheets` objekt.

## Krok 6: Přidejte nové podokno úloh

```csharp
// Přidat nové podokno úloh
int taskPaneIndex = taskPanes.Add();
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane. IsVisible = true;
taskPane. DockState = "right";
taskPane. WebExtension = extension;
```

Do kolekce podokna úloh přidáváme nové podokno úloh. Nastavíme viditelnost panelu, jeho stav ukotvení a související webové rozšíření.

## Krok 7: Uložte a zavřete sešit

```csharp
// Uložte a zavřete sešit
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

Upravený sešit uložíme do zadaného výstupního adresáře a poté jej zavřeme.

### Ukázkový zdrojový kód pro Add Web Extension pomocí Aspose.Cells pro .NET 
```csharp
//Zdrojový adresář
string outDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook();
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
int extensionIndex = extensions.Add();
int taskPaneIndex = taskPanes.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane.IsVisible = true;
taskPane.DockState = "right";
taskPane.WebExtension = extension;
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

## Závěr

gratuluji! Nyní jste se naučili, jak přidat webové rozšíření pomocí Aspose.Cells pro .NET. Experimentujte s kódem a prozkoumejte další funkce Aspose.Cells, abyste co nejlépe využili manipulaci s webovými rozšířeními ve vašich excelových sešitech.

## Nejčastější dotazy

#### Otázka: Co je webové rozšíření v sešitu aplikace Excel?

Odpověď: Webové rozšíření v sešitu aplikace Excel je komponenta, která umožňuje přidat do Excelu další funkce integrací webových aplikací. Může nabídnout interaktivní funkce, vlastní řídicí panely, externí integrace a další.

#### Otázka: Jak přidat webové rozšíření do sešitu aplikace Excel pomocí Aspose.Cells?

 Odpověď: Chcete-li přidat webové rozšíření do sešitu aplikace Excel pomocí Aspose.Cells, můžete postupovat podle kroků uvedených v našem podrobném průvodci. Použijte`WebExtensionCollection` a`WebExtensionTaskPaneCollection` třídy k přidání a konfiguraci webového rozšíření a přidruženého podokna úloh.

#### Otázka: Jaké informace jsou nutné k přidání webového rozšíření?

Odpověď: Při přidávání webového rozšíření musíte zadat ID SKU rozšíření, název obchodu a typ obchodu. Tyto informace pomáhají rozšíření správně identifikovat a načíst.

#### Otázka: Mohu do jednoho excelového sešitu přidat více webových rozšíření?

 Odpověď: Ano, do jednoho excelového sešitu můžete přidat více webových rozšíření. Použijte`Add` metodu kolekce webových rozšíření pro přidání jednotlivých rozšíření a poté je přidružte k odpovídajícím podoknům úloh.