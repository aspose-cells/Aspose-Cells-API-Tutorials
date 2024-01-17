---
title: Zezwalaj na wiodący apostrof
linktitle: Zezwalaj na wiodący apostrof
second_title: Aspose.Cells dla .NET API odniesienia
description: Zezwalaj na wiodący apostrof w skoroszytach programu Excel za pomocą Aspose.Cells dla .NET.
type: docs
weight: 60
url: /pl/net/excel-workbook/allow-leading-apostrophe/
---
tym samouczku krok po kroku wyjaśnimy dostarczony kod źródłowy C#, który umożliwi użycie początkowego apostrofu w skoroszycie programu Excel przy użyciu Aspose.Cells dla .NET. Aby wykonać tę operację, wykonaj poniższe czynności.

## Krok 1: Ustaw katalogi źródłowe i wyjściowe

```csharp
// katalog źródłowy
string sourceDir = RunExamples.Get_SourceDirectory();
// Katalog wyjściowy
string outputDir = RunExamples.Get_OutputDirectory();
```

W tym pierwszym kroku definiujemy katalogi źródłowe i wyjściowe dla plików Excel.

## Krok 2: Utwórz instancję obiektu WorkbookDesigner

```csharp
// Utwórz instancję obiektu WorkbookDesigner
WorkbookDesigner designer = new WorkbookDesigner();
```

 Tworzymy instancję`WorkbookDesigner` klasa z Aspose.Cells.

## Krok 3: Załaduj skoroszyt programu Excel

```csharp
// Załaduj skoroszyt programu Excel
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
designer.Workbook = workbook;
```

Ładujemy skoroszyt programu Excel z określonego pliku i wyłączamy automatyczną konwersję początkowych apostrofów na styl tekstu.

## Krok 4: Ustaw źródło danych

```csharp
// Zdefiniuj źródło danych dla skoroszytu projektanta
List<DataObject> list = new List<DataObject>
{
new DataObject
{
Id=1,
Name = "demo"
},
new DataObject
{
ID=2,
Name = "'demo"
}
};
designer.SetDataSource("sampleData", list);
```

 Definiujemy listę obiektów danych i używamy metody`SetDataSource` metoda ustawiania źródła danych dla skoroszytu projektanta.

## Krok 5: Przetwarzaj inteligentne znaczniki

```csharp
// Przetwarzaj inteligentne znaczniki
designer. Process();
```

 Używamy`Process` metoda przetwarzania inteligentnych znaczników w skoroszycie projektanta.

## Krok 6: Zapisz zmodyfikowany skoroszyt programu Excel

```csharp
// Zapisz zmodyfikowany skoroszyt programu Excel
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
```

Zapisujemy zmodyfikowany skoroszyt programu Excel z wprowadzonymi zmianami.

### Przykładowy kod źródłowy dla opcji Zezwalaj na wiodący apostrof przy użyciu Aspose.Cells dla .NET 
```csharp
//Katalog źródłowy
string sourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
// Tworzenie instancji obiektu WorkbookDesigner
WorkbookDesigner designer = new WorkbookDesigner();
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
// Otwórz arkusz kalkulacyjny projektanta zawierający inteligentne znaczniki
designer.Workbook = workbook;
List<DataObject> list = new List<DataObject>
{
	new DataObject
	{
		 Id =1,
		 Name = "demo"
	},
	new DataObject
	{
		Id=2,
		Name = "'demo"
	}
};
// Ustaw źródło danych dla arkusza kalkulacyjnego projektanta
designer.SetDataSource("sampleData", list);
// Przetwarzaj inteligentne znaczniki
designer.Process();
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
Console.WriteLine("AllowLeadingApostrophe executed successfully.");
```

## Wniosek

Gratulacje! Nauczyłeś się, jak zezwolić na użycie początkowego apostrofu w skoroszycie programu Excel przy użyciu Aspose.Cells dla .NET. Eksperymentuj z własnymi danymi, aby jeszcze bardziej dostosować skoroszyty programu Excel.

### Często zadawane pytania

#### P: Jakie jest uprawnienie do apostrofu wiodącego w skoroszycie programu Excel?

Odp.: Zezwolenie na początkowy apostrof w skoroszycie programu Excel umożliwia prawidłowe wyświetlanie danych rozpoczynających się od apostrofu bez konwertowania ich na styl tekstu. Jest to przydatne, jeśli chcesz zachować apostrof jako część danych.

#### P: Dlaczego muszę wyłączyć automatyczną konwersję początkowych apostrofów?

O: Wyłączając automatyczną konwersję wiodących cudzysłowów, możesz zachować ich użycie w swoich danych. Pozwala to uniknąć niezamierzonej modyfikacji danych podczas otwierania skoroszytu programu Excel lub manipulowania nim.

#### P: Jak ustawić źródło danych w skoroszycie projektanta?

 Odp.: Aby ustawić źródło danych w skoroszycie projektanta, możesz użyć metody`SetDataSource` metoda określająca nazwę źródła danych i listę odpowiednich obiektów danych.

#### P: Czy zezwolenie na początkowy apostrof wpływa na inne dane w skoroszycie programu Excel?

Odpowiedź: Nie, dopuszczenie apostrofu wiodącego wpływa tylko na dane rozpoczynające się od apostrofu. Pozostałe dane w skoroszycie programu Excel pozostają niezmienione.

#### P: Czy mogę używać tej funkcji z innymi formatami plików Excel?

O: Tak, możesz używać tej funkcji z innymi formatami plików Excel obsługiwanymi przez Aspose.Cells, takimi jak .xls, .xlsm itp.