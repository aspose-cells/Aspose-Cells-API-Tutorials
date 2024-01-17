---
title: Zaktualizuj element formuły dodatku Power Query
linktitle: Zaktualizuj element formuły dodatku Power Query
second_title: Aspose.Cells dla .NET API odniesienia
description: Dowiedz się, jak aktualizować elementy formuł Power Query w plikach Excel przy użyciu Aspose.Cells dla platformy .NET.
type: docs
weight: 160
url: /pl/net/excel-workbook/update-power-query-formula-item/
---
Aktualizowanie elementu formuły dodatku Power Query jest typową operacją podczas pracy z danymi w plikach Excel. Dzięki Aspose.Cells dla .NET możesz łatwo zaktualizować element formuły Power Query, wykonując następujące kroki:

## Krok 1: Określ katalogi źródłowe i wyjściowe

Najpierw musisz określić katalog źródłowy, w którym znajduje się plik Excel zawierający formuły Power Query do aktualizacji, a także katalog wyjściowy, w którym chcesz zapisać zmodyfikowany plik. Oto jak to zrobić za pomocą Aspose.Cells:

```csharp
// katalog źródłowy
string SourceDir = RunExamples.Get_SourceDirectory();

// Katalog wyjściowy
string outputDir = RunExamples.Get_OutputDirectory();
```

## Krok 2: Załaduj źródłowy skoroszyt programu Excel

Następnie należy załadować źródłowy skoroszyt programu Excel, w którym chcesz zaktualizować element formuły Power Query. Oto jak to zrobić:

```csharp
// Załaduj źródłowy skoroszyt programu Excel
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
```

## Krok 3: Przeglądaj i aktualizuj elementy formuły dodatku Power Query

Po załadowaniu skoroszytu możesz przejść do kolekcji formuł dodatku Power Query i przeglądać każdą formułę oraz jej elementy. W tym przykładzie szukamy elementu formuły o nazwie „Źródło” i aktualizujemy jego wartość. Oto przykładowy kod umożliwiający aktualizację elementu formuły dodatku Power Query:

```csharp
// Uzyskaj dostęp do kolekcji formuł dodatku Power Query
DataMashup mashupData = workbook.DataMashup;

// Przeglądaj formuły dodatku Power Query i ich elementy w pętli
foreach(PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
     foreach(PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
     {
         if (item.Name == "Source")
         {
             item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
         }
     }
}
```

## Krok 4: Zapisz wyjściowy skoroszyt programu Excel

Po zaktualizowaniu elementu formuły dodatku Power Query można zapisać zmodyfikowany skoroszyt programu Excel w określonym katalogu wyjściowym. Oto jak to zrobić:

```csharp
// Zapisz wyjściowy skoroszyt programu Excel
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.\r\n");
```

### Przykładowy kod źródłowy aktualizacji elementu formuły Power Query przy użyciu Aspose.Cells dla platformy .NET 
```csharp
// Katalogi robocze
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
DataMashup mashupData = workbook.DataMashup;
foreach (PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
	foreach (PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
	{
		if (item.Name == "Source")
		{
			item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
		}
	}
}
// Zapisz skoroszyt wyjściowy.
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.");
```

## Wniosek

Aktualizowanie elementów formuł Power Query jest niezbędną operacją podczas używania Aspose.Cells do manipulowania i przetwarzania danych w plikach Excel. Wykonując powyższe kroki, możesz łatwo zaktualizować elementy formuły

### Często zadawane pytania

#### P: Co to jest dodatek Power Query w programie Excel?
     
Odp.: Power Query to funkcja programu Excel, która pomaga zbierać, przekształcać i ładować dane z różnych źródeł. Oferuje potężne narzędzia do czyszczenia, łączenia i przekształcania danych przed zaimportowaniem ich do Excela.

#### P: Skąd mam wiedzieć, czy element formuły dodatku Power Query został pomyślnie zaktualizowany?
    A: After running the Power Query Formula Item Update, you can check if the operation was successful by viewing the output and ensuring that the output Excel file was created correctly.

#### P: Czy mogę zaktualizować wiele elementów formuł dodatku Power Query jednocześnie?
    
Odp.: Tak, możesz przeglądać kolekcję elementów formuł dodatku Power Query w pętli i aktualizować wiele elementów w jednej pętli, w zależności od konkretnych potrzeb.

#### P: Czy są inne operacje, które mogę wykonać na formułach Power Query za pomocą Aspose.Cells?
    
Odp.: Tak, Aspose.Cells oferuje pełen zakres funkcji do pracy z formułami Power Query, w tym tworzenie, usuwanie, kopiowanie i wyszukiwanie formuł w skoroszycie programu Excel.