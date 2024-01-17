---
title: Wyświetlaj i ukrywaj linie siatki arkusza kalkulacyjnego
linktitle: Wyświetlaj i ukrywaj linie siatki arkusza kalkulacyjnego
second_title: Aspose.Cells dla .NET API odniesienia
description: Kontroluj wyświetlanie linii siatki w arkuszu programu Excel za pomocą Aspose.Cells dla .NET.
type: docs
weight: 30
url: /pl/net/excel-display-settings-csharp-tutorials/display-and-hide-gridlines-of-worksheet/
---
W tym samouczku pokażemy, jak wyświetlać i ukrywać linie siatki w arkuszu programu Excel przy użyciu kodu źródłowego C# z Aspose.Cells dla .NET. Wykonaj poniższe kroki, aby uzyskać pożądany rezultat.

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

## Krok 3: Przejdź do pierwszego arkusza i ukryj linie siatki

 Uzyskaj dostęp do pierwszego arkusza w pliku Excel za pomocą`Worksheets` własność`Workbook` obiekt. Następnie użyj`IsGridlinesVisible` własność`Worksheet` obiekt, aby ukryć linie siatki.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet.IsGridlinesVisible = false;
```

## Krok 4: Zapisz zmiany

 Po dokonaniu niezbędnych zmian zapisz zmodyfikowany plik Excel za pomocą`Save` metoda`Workbook` obiekt.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Przykładowy kod źródłowy do wyświetlania i ukrywania linii siatki arkusza przy użyciu Aspose.Cells dla .NET 

```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Tworzenie strumienia plików zawierającego plik Excel do otwarcia
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Tworzenie instancji obiektu skoroszytu
// Otwieranie pliku Excel poprzez strumień pliku
Workbook workbook = new Workbook(fstream);
// Dostęp do pierwszego arkusza w pliku Excel
Worksheet worksheet = workbook.Worksheets[0];
// Ukrywanie linii siatki pierwszego arkusza pliku Excel
worksheet.IsGridlinesVisible = false;
// Zapisanie zmodyfikowanego pliku Excel
workbook.Save(dataDir + "output.xls");
// Zamknięcie strumienia plików w celu zwolnienia wszystkich zasobów
fstream.Close();
```

## Wniosek

Ten przewodnik krok po kroku pokazał, jak pokazywać i ukrywać linie siatki w arkuszu kalkulacyjnym Excel przy użyciu Aspose.Cells dla .NET. Korzystając z dostarczonego kodu źródłowego C#, możesz łatwo dostosować wyświetlanie linii siatki w plikach Excel.

### Często zadawane pytania (FAQ)

#### Co to jest Aspose.Cells dla .NET?

Aspose.Cells dla .NET to potężna biblioteka do manipulowania plikami Excel w aplikacjach .NET.

#### Jak mogę zainstalować Aspose.Cells dla .NET?

 Aby zainstalować Aspose.Cells dla .NET, musisz pobrać odpowiedni pakiet z[Wydania Aspose](https://releases/aspose.com/cells/net/) i dodaj go do swojego projektu .NET.

#### Jak mogę pokazać lub ukryć linie siatki w arkuszu kalkulacyjnym Excel za pomocą Aspose.Cells dla .NET?

 Możesz skorzystać z`IsGridlinesVisible` własność`Worksheet` obiekt, aby pokazać lub ukryć linie siatki. Ustaw to na`true` żeby im pokazać i`false` żeby je ukryć.

#### Jakie inne formaty plików Excel są obsługiwane przez Aspose.Cells dla .NET?

Aspose.Cells dla .NET obsługuje różne formaty plików Excel, takie jak XLS, XLSX, CSV, HTML, PDF i wiele innych.

