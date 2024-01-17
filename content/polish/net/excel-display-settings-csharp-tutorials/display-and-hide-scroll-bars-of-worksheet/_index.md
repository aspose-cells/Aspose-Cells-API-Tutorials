---
title: Wyświetlaj i ukrywaj paski przewijania arkusza
linktitle: Wyświetlaj i ukrywaj paski przewijania arkusza
second_title: Aspose.Cells dla .NET API odniesienia
description: Wyświetlaj lub ukrywaj paski przewijania w arkuszu programu Excel za pomocą Aspose.Cells dla .NET.
type: docs
weight: 50
url: /pl/net/excel-display-settings-csharp-tutorials/display-and-hide-scroll-bars-of-worksheet/
---
W tym samouczku pokażemy, jak wyświetlić lub ukryć pionowe i poziome paski przewijania w arkuszu programu Excel przy użyciu kodu źródłowego C# z Aspose.Cells dla .NET. Wykonaj poniższe kroki, aby uzyskać pożądany rezultat.

## Krok 1: Zaimportuj niezbędne biblioteki

Upewnij się, że zainstalowałeś bibliotekę Aspose.Cells dla .NET i zaimportuj niezbędne biblioteki do swojego projektu C#.

```csharp
using Aspose.Cells;
using System.IO;
```

## Krok 2: Ustaw ścieżkę katalogu i otwórz plik Excel

 Ustaw ścieżkę do katalogu zawierającego plik Excel, a następnie otwórz plik, tworząc strumień pliku i tworząc instancję pliku`Workbook` obiekt.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## Krok 3: Ukryj paski przewijania

 Użyj`IsVScrollBarVisible` I`IsHScrollBarVisible` właściwości`Workbook.Settings` obiekt, aby ukryć pionowe i poziome paski przewijania arkusza.

```csharp
workbook.Settings.IsVScrollBarVisible = false;
workbook.Settings.IsHScrollBarVisible = false;
```

## Krok 4: Zapisz zmiany

 Po dokonaniu niezbędnych zmian zapisz zmodyfikowany plik Excel za pomocą`Save` metoda`Workbook` obiekt.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Przykładowy kod źródłowy do wyświetlania i ukrywania pasków przewijania arkusza przy użyciu Aspose.Cells dla .NET 

```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Tworzenie strumienia plików zawierającego plik Excel do otwarcia
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Tworzenie instancji obiektu skoroszytu
// Otwieranie pliku Excel poprzez strumień pliku
Workbook workbook = new Workbook(fstream);
// Ukrywanie pionowego paska przewijania pliku Excel
workbook.Settings.IsVScrollBarVisible = false;
// Ukrywanie poziomego paska przewijania pliku Excel
workbook.Settings.IsHScrollBarVisible = false;
// Zapisanie zmodyfikowanego pliku Excel
workbook.Save(dataDir + "output.xls");
// Zamknięcie strumienia plików w celu zwolnienia wszystkich zasobów
fstream.Close();
```

### Wniosek

Ten przewodnik krok po kroku pokazał, jak wyświetlić lub ukryć pionowe i poziome paski przewijania w arkuszu kalkulacyjnym Excel przy użyciu Aspose.Cells dla .NET. Korzystając z dostarczonego kodu źródłowego C#, możesz łatwo dostosować wyświetlanie pasków przewijania w plikach Excel.

### Często zadawane pytania (FAQ)

#### Co to jest Aspose.Cells dla .NET?

Aspose.Cells dla .NET to potężna biblioteka do manipulowania plikami Excel w aplikacjach .NET.

#### Jak mogę zainstalować Aspose.Cells dla .NET?

 Aby zainstalować Aspose.Cells dla .NET, musisz pobrać odpowiedni pakiet z[Wydania Aspose](https://releases/aspose.com/cells/net/) i dodaj go do swojego projektu .NET.

#### Jak mogę wyświetlić lub ukryć paski przewijania w arkuszu kalkulacyjnym Excel za pomocą Aspose.Cells dla .NET?

 Możesz skorzystać z`IsVScrollBarVisible` I`IsHScrollBarVisible` właściwości`Workbook.Settings` obiekt, aby wyświetlić lub ukryć odpowiednio pionowy i poziomy pasek przewijania w arkuszu programu Excel.

#### Jakie inne formaty plików Excel są obsługiwane przez Aspose.Cells dla .NET?

Aspose.Cells dla .NET obsługuje różne formaty plików Excel, takie jak XLS, XLSX, CSV, HTML, PDF itp.