---
title: Excel Wyczyść wszystkie podziały stron
linktitle: Excel Wyczyść wszystkie podziały stron
second_title: Aspose.Cells dla .NET API odniesienia
description: Dowiedz się, jak usunąć wszystkie podziały stron w programie Excel za pomocą Aspose.Cells dla .NET. Samouczek krok po kroku dotyczący czyszczenia plików Excel.
type: docs
weight: 20
url: /pl/net/excel-page-breaks/excel-clear-all-page-breaks/
---

Usuwanie podziałów stron w pliku Excel jest niezbędnym krokiem podczas obsługi raportów lub arkuszy kalkulacyjnych. W tym samouczku poprowadzimy Cię krok po kroku przez zrozumienie i wdrożenie dostarczonego kodu źródłowego C# w celu usunięcia wszystkich podziałów stron w pliku Excel przy użyciu biblioteki Aspose.Cells dla .NET.

## Krok 1: Przygotowanie środowiska

 Zanim zaczniesz, upewnij się, że masz zainstalowany Aspose.Cells for .NET na swoim komputerze. Bibliotekę można pobrać ze strony[Wydania Aspose](https://releases.aspose.com/cells/net) zainstaluj go, postępując zgodnie z dostarczonymi instrukcjami.

Po zakończeniu instalacji utwórz nowy projekt C# w preferowanym zintegrowanym środowisku programistycznym (IDE) i zaimportuj bibliotekę Aspose.Cells dla .NET.

## Krok 2: Konfiguracja ścieżki katalogu dokumentów

 W dostarczonym kodzie źródłowym musisz określić ścieżkę katalogu, w którym chcesz zapisać wygenerowany plik Excel. Zmodyfikuj`dataDir` zmienną, zastępując „TWOJ KATALOG DOKUMENTÓW” bezwzględną ścieżką katalogu na twoim komputerze.

```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
```

## Krok 3: Tworzenie obiektu skoroszytu

Na początek musimy utworzyć obiekt Workbook reprezentujący nasz plik Excel. Można to osiągnąć za pomocą klasy Workbook dostarczonej przez Aspose.Cells.

```csharp
// Tworzenie instancji obiektu skoroszytu
Workbook workbook = new Workbook();
```

## Krok 4: Usuń podziały stron

 Teraz usuniemy wszystkie podziały stron w naszym arkuszu programu Excel. W przykładowym kodzie używamy`Clear()` metody poziomego i pionowego podziału strony, aby je wszystkie usunąć.

```csharp
workbook.Worksheets[0].HorizontalPageBreaks.Clear();
workbook.Worksheets[0].VerticalPageBreaks.Clear();
```

## Krok 5: Zapisywanie pliku Excel

 Po usunięciu wszystkich podziałów stron możemy zapisać ostateczny plik Excel. Użyj`Save()` metodę określającą pełną ścieżkę pliku wyjściowego.

```csharp
// Zapisz plik Excela.
workbook.Save(dataDir + "ClearingPageBreaks_out.xls");
```

### Przykładowy kod źródłowy programu Excel Wyczyść wszystkie podziały stron za pomocą Aspose.Cells dla .NET 

```csharp

//Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Tworzenie instancji obiektu skoroszytu
Workbook workbook = new Workbook();
// Usuwanie wszystkich podziałów stron
workbook.Worksheets[0].HorizontalPageBreaks.Clear();
workbook.Worksheets[0].VerticalPageBreaks.Clear();
// Zapisz plik Excela.
workbook.Save(dataDir + "ClearAllPageBreaks_out.xls");

```

## Wniosek

tym samouczku nauczyliśmy się, jak usunąć wszystkie podziały stron w pliku Excel za pomocą Aspose.Cells dla .NET. Wykonując podane kroki, możesz łatwo zarządzać i usuwać niechciane podziały stron w dynamicznie generowanych plikach Excel. Zachęcamy do dalszego odkrywania funkcji oferowanych przez Aspose.Cells w celu uzyskania bardziej zaawansowanych operacji.

### Często zadawane pytania

#### P: Czy Aspose.Cells dla .NET jest bezpłatną biblioteką?

Odp.: Aspose.Cells dla .NET jest biblioteką komercyjną, ale oferuje bezpłatną wersję próbną, której można użyć do oceny jej funkcjonalności.

#### P: Czy usunięcie podziałów stron wpływa na inne elementy arkusza?

Odp.: Nie, usunięcie podziałów stron powoduje jedynie zmianę samych podziałów stron i nie ma wpływu na żadne inne dane ani formatowanie w arkuszu.

#### P: Czy mogę selektywnie usunąć niektóre określone podziały stron w programie Excel?

Odp.: Tak, dzięki Aspose.Cells możesz indywidualnie uzyskać dostęp do każdego podziału strony i usunąć go, jeśli to konieczne, przy użyciu odpowiednich metod.

#### P: Jakie inne formaty plików Excel są obsługiwane przez Aspose.Cells dla .NET?

Odp.: Aspose.Cells dla .NET obsługuje różne formaty plików Excel, takie jak XLSX, XLSM, CSV, HTML, PDF itp.

