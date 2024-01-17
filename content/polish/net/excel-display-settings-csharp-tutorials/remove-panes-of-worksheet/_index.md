---
title: Usuń okienka arkusza
linktitle: Usuń okienka arkusza
second_title: Aspose.Cells dla .NET API odniesienia
description: Przewodnik krok po kroku dotyczący usuwania okienek z arkusza programu Excel przy użyciu Aspose.Cells dla .NET.
type: docs
weight: 120
url: /pl/net/excel-display-settings-csharp-tutorials/remove-panes-of-worksheet/
---
W tym samouczku wyjaśnimy, jak usunąć okienka z arkusza programu Excel za pomocą Aspose.Cells dla .NET. Wykonaj następujące kroki, aby uzyskać pożądany rezultat:

## Krok 1: Konfigurowanie środowiska

Upewnij się, że zainstalowałeś Aspose.Cells dla .NET i skonfiguruj środowisko programistyczne. Upewnij się także, że masz kopię pliku Excel, z którego chcesz usunąć panele.

## Krok 2: Zaimportuj niezbędne zależności

Dodaj niezbędne dyrektywy, aby korzystać z klas z Aspose.Cells:

```csharp
using Aspose.Cells;
```

## Krok 3: Inicjalizacja kodu

Zacznij od zainicjowania ścieżki do katalogu zawierającego dokumenty Excel:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## Krok 4: Otwieranie pliku Excel

 Utwórz instancję nowego`Workbook` obiekt i otwórz plik Excel za pomocą metody`Open` metoda:

```csharp
Workbook book = new Workbook(dataDir + "Book1.xls");
```

## Krok 5: Zdefiniuj aktywną komórkę

 Ustaw aktywną komórkę arkusza za pomocą`ActiveCell` nieruchomość:

```csharp
book.Worksheets[0].ActiveCell = "A20";
```

## Krok 6: Usuwanie paneli

 Usuń panele z okna arkusza za pomocą`RemoveSplit` metoda:

```csharp
book.Worksheets[0].RemoveSplit();
```

## Krok 7: Zapisywanie zmian

Zapisz zmiany wprowadzone w pliku Excel:

```csharp
book.Save(dataDir + "output.xls");
```

### Przykładowy kod źródłowy narzędzia Usuń panele arkusza przy użyciu Aspose.Cells dla platformy .NET 
```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Utwórz instancję nowego skoroszytu i otwórz plik szablonu
Workbook book = new Workbook(dataDir + "Book1.xls");
// Ustaw aktywną komórkę
book.Worksheets[0].ActiveCell = "A20";
// Podziel okno arkusza
book.Worksheets[0].RemoveSplit();
// Zapisz plik Excela
book.Save(dataDir + "output.xls");
```

## Wniosek

W tym samouczku nauczyłeś się, jak usuwać okienka z arkusza programu Excel za pomocą Aspose.Cells dla .NET. Wykonując opisane kroki, możesz łatwo dostosować wygląd i zachowanie plików Excel.

### Często zadawane pytania (FAQ)

#### Co to jest Aspose.Cells dla .NET?

Aspose.Cells dla .NET to popularna biblioteka oprogramowania do manipulowania plikami Excel w aplikacjach .NET.

#### Jak ustawić aktywną komórkę arkusza w Aspose.Cells?

 Możesz ustawić aktywną komórkę za pomocą`ActiveCell`właściwość obiektu Worksheet.

#### Czy z okna arkusza mogę usunąć tylko panele poziome lub pionowe?

 Tak, używając Aspose.Cells, możesz usunąć tylko poziome lub pionowe panele, stosując odpowiednie metody, takie jak`RemoveHorizontalSplit` Lub`RemoveVerticalSplit`.

#### Czy Aspose.Cells działa tylko z plikami Excel w formacie .xls?

Nie, Aspose.Cells obsługuje różne formaty plików Excel, w tym .xls i .xlsx.
	