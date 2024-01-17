---
title: Podgląd podziału strony w arkuszu
linktitle: Podgląd podziału strony w arkuszu
second_title: Aspose.Cells dla .NET API odniesienia
description: Przewodnik krok po kroku pokazujący podgląd podziału strony w arkuszu przy użyciu Aspose.Cells dla .NET.
type: docs
weight: 110
url: /pl/net/excel-display-settings-csharp-tutorials/page-break-preview-of-worksheet/
---
W tym samouczku wyjaśnimy, jak wyświetlić podgląd podziału strony w arkuszu za pomocą Aspose.Cells dla .NET. Wykonaj następujące kroki, aby uzyskać pożądany rezultat:

## Krok 1: Konfigurowanie środowiska

Upewnij się, że zainstalowałeś Aspose.Cells dla .NET i skonfiguruj środowisko programistyczne. Upewnij się także, że masz kopię pliku Excel, w którym chcesz wyświetlić podgląd podziału strony.

## Krok 2: Zaimportuj niezbędne zależności

Dodaj niezbędne dyrektywy, aby korzystać z klas z Aspose.Cells:

```csharp
using Aspose.Cells;
using System.IO;
```

## Krok 3: Inicjalizacja kodu

Zacznij od zainicjowania ścieżki do katalogu zawierającego dokumenty Excel:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## Krok 4: Otwieranie pliku Excel

 Stwórz`FileStream` obiekt zawierający plik Excel do otwarcia:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 Utwórz instancję a`Workbook` obiekt i otwórz plik Excel, korzystając ze strumienia pliku:

```csharp
Workbook workbook = new Workbook(fstream);
```

## Krok 5: Dostęp do arkusza kalkulacyjnego

Przejdź do pierwszego arkusza w pliku Excel:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Krok 6: Wyświetlanie podglądu stron

Włącz podgląd stronicowania dla arkusza kalkulacyjnego:

```csharp
worksheet. IsPageBreakPreview = true;
```

## Krok 7: Zapisywanie zmian

Zapisz zmiany wprowadzone w pliku Excel:

```csharp
workbook.Save(dataDir + "output.xls");
```

## Krok 8: Zamknięcie strumienia plików

Zamknij strumień plików, aby zwolnić wszystkie zasoby:

```csharp
fstream.Close();
```

### Przykładowy kod źródłowy podglądu podziału strony w arkuszu przy użyciu Aspose.Cells dla .NET 
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
// Wyświetlanie arkusza w podglądzie podziału strony
worksheet.IsPageBreakPreview = true;
// Zapisanie zmodyfikowanego pliku Excel
workbook.Save(dataDir + "output.xls");
// Zamknięcie strumienia plików w celu zwolnienia wszystkich zasobów
fstream.Close();
```

## Wniosek

W tym samouczku nauczyłeś się wyświetlać podgląd podziału strony w arkuszu przy użyciu Aspose.Cells dla .NET. Wykonując opisane kroki, możesz łatwo kontrolować wygląd i układ plików Excel.

### Często zadawane pytania (FAQ)

#### Co to jest Aspose.Cells dla .NET?

Aspose.Cells dla .NET to popularna biblioteka oprogramowania do manipulowania plikami Excel w aplikacjach .NET.

#### Czy mogę wyświetlić podgląd poszczególnych stron konkretnego arkusza zamiast całego arkusza?

Tak, używając Aspose.Cells możesz włączyć podgląd podziału strony dla konkretnego arkusza, uzyskując dostęp do odpowiedniego obiektu arkusza.

#### Czy Aspose.Cells obsługuje inne funkcje edycji plików Excel?

Tak, Aspose.Cells oferuje szeroką gamę funkcji do edycji i manipulowania plikami Excel, takich jak dodawanie danych, formatowanie, tworzenie wykresów itp.

#### Czy Aspose.Cells działa tylko z plikami Excel w formacie .xls?

Nie, Aspose.Cells obsługuje różne formaty plików Excel, w tym .xls i .xlsx.
	