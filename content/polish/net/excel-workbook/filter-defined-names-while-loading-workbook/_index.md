---
title: Filtruj zdefiniowane nazwy podczas ładowania skoroszytu
linktitle: Filtruj zdefiniowane nazwy podczas ładowania skoroszytu
second_title: Aspose.Cells dla .NET API odniesienia
description: Dowiedz się, jak filtrować zdefiniowane nazwy podczas ładowania skoroszytu programu Excel za pomocą Aspose.Cells dla .NET.
type: docs
weight: 100
url: /pl/net/excel-workbook/filter-defined-names-while-loading-workbook/
---
Podczas pracy ze skoroszytami programu Excel w aplikacji .NET często konieczne jest filtrowanie danych podczas ładowania. Aspose.Cells dla .NET to potężna biblioteka umożliwiająca łatwe manipulowanie skoroszytami programu Excel. W tym przewodniku pokażemy, jak filtrować nazwy zdefiniowane podczas ładowania skoroszytu za pomocą Aspose.Cells dla .NET. Wykonaj te proste kroki, aby uzyskać pożądane rezultaty:

## Krok 1: Określ opcje ładowania

Najpierw musisz określić opcje ładowania, aby zdefiniować zachowanie ładowania skoroszytu. W naszym przypadku chcemy zignorować nazwy ustawione przy ładowaniu. Oto jak to zrobić za pomocą Aspose.Cells:

```csharp
// Określa opcje ładowania
LoadOptions opts = new LoadOptions();

// Nie ładuj zdefiniowanych nazw
opts. LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
```

## Krok 2: Załaduj skoroszyt

Po skonfigurowaniu opcji ładowania możesz załadować skoroszyt programu Excel z pliku źródłowego. Pamiętaj, aby podać poprawną ścieżkę pliku. Oto przykładowy kod:

```csharp
// Załaduj skoroszyt
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
```

## Krok 3: Zapisz przefiltrowany skoroszyt

Po załadowaniu skoroszytu możesz w razie potrzeby wykonać inne operacje lub edytować. Następnie możesz zapisać przefiltrowany skoroszyt w pliku wyjściowym. Oto jak:

```csharp
// Zapisz przefiltrowany skoroszyt programu Excel
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
```

### Przykładowy kod źródłowy dla nazw zdefiniowanych przez filtr podczas ładowania skoroszytu przy użyciu Aspose.Cells dla .NET 
```csharp
//Określ opcje ładowania
LoadOptions opts = new LoadOptions();
//Nie chcemy ładować zdefiniowanych nazw
opts.LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
//Załaduj skoroszyt
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
//Zapisz wyjściowy plik Excel, spowoduje to złamanie formuły w C1
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
Console.WriteLine("FilterDefinedNamesWhileLoadingWorkbook executed successfully.");
```

## Wniosek

Filtrowanie zdefiniowanych nazw podczas ładowania skoroszytu programu Excel może mieć kluczowe znaczenie w przypadku wielu aplikacji. Aspose.Cells dla .NET ułatwia to zadanie, zapewniając elastyczne opcje ładowania i filtrowania danych. Wykonując kroki opisane w tym przewodniku, będziesz w stanie skutecznie odfiltrować zdefiniowane nazwy i osiągnąć pożądane wyniki w skoroszytach programu Excel.


### Często zadawane pytania

#### P: Czy Aspose.Cells obsługuje inne języki programowania oprócz C#?
    
O: Tak, Aspose.Cells to wieloplatformowa biblioteka obsługująca wiele języków programowania, takich jak Java, Python, C++i wiele więcej.

#### P: Czy mogę filtrować inne typy danych podczas ładowania skoroszytu za pomocą Aspose.Cells?
    
O: Tak, Aspose.Cells oferuje szereg opcji filtrowania danych, w tym formuły, style, makra itp.

#### P: Czy Aspose.Cells zachowuje formatowanie i właściwości oryginalnego skoroszytu?
    
Odp.: Tak, Aspose.Cells zachowuje formatowanie, style, formuły i inne właściwości oryginalnego skoroszytu podczas pracy z plikami Excel.