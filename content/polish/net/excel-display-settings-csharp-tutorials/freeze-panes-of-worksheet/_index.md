---
title: Zablokuj okienka arkusza
linktitle: Zablokuj okienka arkusza
second_title: Aspose.Cells dla .NET API odniesienia
description: Z łatwością manipuluj blokowanymi okienkami arkusza programu Excel za pomocą Aspose.Cells dla .NET.
type: docs
weight: 70
url: /pl/net/excel-display-settings-csharp-tutorials/freeze-panes-of-worksheet/
---
W tym samouczku pokażemy, jak blokować okienka w arkuszu programu Excel przy użyciu kodu źródłowego C# z Aspose.Cells dla .NET. Wykonaj poniższe kroki, aby uzyskać pożądany rezultat.

## Krok 1: Zaimportuj niezbędne biblioteki

Upewnij się, że zainstalowałeś bibliotekę Aspose.Cells dla .NET i zaimportuj niezbędne biblioteki do swojego projektu C#.

```csharp
using Aspose.Cells;
```

## Krok 2: Ustaw ścieżkę katalogu i otwórz plik Excel

 Ustaw ścieżkę do katalogu zawierającego plik Excel, a następnie otwórz plik, tworząc instancję a`Workbook` obiekt.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## Krok 3: Przejdź do arkusza kalkulacyjnego i zastosuj ustawienia blokady panelu

 Przejdź do pierwszego arkusza w pliku Excel za pomocą`Worksheet` obiekt. Następnie użyj`FreezePanes` metoda zastosowania ustawień blokady panelu.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. FreezePanes(3, 2, 3, 2);
```

W powyższym przykładzie szyby są zablokowane w komórce w wierszu 3 i kolumnie 2.

## Krok 4: Zapisz zmiany

 Po dokonaniu niezbędnych zmian zapisz zmodyfikowany plik Excel za pomocą`Save` metoda`Workbook` obiekt.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Przykładowy kod źródłowy dla Zamroź panele arkusza przy użyciu Aspose.Cells dla .NET 

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
// Stosowanie ustawień blokowania okienek
worksheet.FreezePanes(3, 2, 3, 2);
// Zapisanie zmodyfikowanego pliku Excel
workbook.Save(dataDir + "output.xls");
// Zamknięcie strumienia plików w celu zwolnienia wszystkich zasobów
fstream.Close();
```

## Wniosek

Ten przewodnik krok po kroku pokazał, jak blokować okienka w arkuszu kalkulacyjnym Excel przy użyciu Aspose.Cells dla .NET. Korzystając z dostarczonego kodu źródłowego C#, możesz łatwo dostosować ustawienia blokady panelu, aby lepiej organizować i wizualizować dane w plikach Excel.

### Często zadawane pytania (FAQ)

#### Co to jest Aspose.Cells dla .NET?

Aspose.Cells dla .NET to potężna biblioteka do manipulowania plikami Excel w aplikacjach .NET.

#### Jak mogę zainstalować Aspose.Cells dla .NET?

 Aby zainstalować Aspose.Cells dla .NET, musisz pobrać odpowiedni pakiet z[Wydania Aspose](https://releases/aspose.com/cells/net/) i dodaj go do swojego projektu .NET.

#### Jak zablokować okienka w arkuszu programu Excel za pomocą Aspose.Cells dla .NET?

 Możesz skorzystać z`FreezePanes` metoda`Worksheet` obiekt, aby zablokować panele arkusza. Określ komórki do zablokowania, podając indeksy wierszy i kolumn.

#### Czy mogę dostosować ustawienia blokady panelu za pomocą Aspose.Cells dla .NET?

 Tak, korzystając z`FreezePanes` możesz określić, które komórki mają zostać zablokowane, podając odpowiednie indeksy wierszy i kolumn.
