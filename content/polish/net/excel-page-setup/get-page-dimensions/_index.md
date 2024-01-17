---
title: Pobierz wymiary strony
linktitle: Pobierz wymiary strony
second_title: Aspose.Cells dla .NET API odniesienia
description: Dowiedz się, jak pobrać wymiary strony w programie Excel przy użyciu Aspose.Cells dla .NET. Przewodnik krok po kroku z kodem źródłowym w języku C#.
type: docs
weight: 40
url: /pl/net/excel-page-setup/get-page-dimensions/
---
Aspose.Cells dla .NET to potężna biblioteka, która umożliwia programistom programową pracę z plikami Microsoft Excel. Oferuje szeroką gamę funkcji do manipulowania dokumentami Excel, w tym możliwość uzyskania wymiarów strony. W tym samouczku przeprowadzimy Cię przez kroki pobierania wymiarów strony za pomocą Aspose.Cells dla .NET.

## Krok 1: Utwórz instancję klasy Workbook

Na początek musimy utworzyć instancję klasy Workbook, która reprezentuje skoroszyt programu Excel. Można to osiągnąć za pomocą następującego kodu:

```csharp
Workbook book = new Workbook();
```

## Krok 2: Dostęp do arkusza kalkulacyjnego

Następnie musimy przejść do arkusza w skoroszycie, w którym chcemy ustawić wymiary strony. W tym przykładzie załóżmy, że chcemy pracować z pierwszym arkuszem. Dostęp do niego możemy uzyskać za pomocą następującego kodu:

```csharp
Worksheet sheet = book.Worksheets[0];
```

## Krok 3: Ustaw rozmiar papieru na A2 oraz szerokość i wysokość druku w calach

Teraz ustawimy rozmiar papieru na A2 i wydrukujemy szerokość i wysokość strony w calach. Można to osiągnąć za pomocą następującego kodu:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("A2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Krok 4: Ustaw rozmiar papieru na A3 oraz szerokość i wysokość druku w calach

Następnie ustawimy rozmiar papieru na A3 i wydrukujemy szerokość i wysokość strony w calach. Oto odpowiedni kod:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("A3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Krok 5: Ustaw rozmiar papieru na A4 oraz szerokość i wysokość druku w calach

Ustawimy teraz rozmiar papieru na A4 i wydrukujemy szerokość i wysokość strony w calach. Oto kod:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("A4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Krok 6: Ustaw rozmiar papieru na Letter i wydrukuj szerokość i wysokość w calach

Na koniec ustawimy rozmiar papieru na Letter i wydrukujemy szerokość i wysokość strony w calach. Oto kod:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("Letter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

### Przykładowy kod źródłowy narzędzia Pobierz wymiary strony przy użyciu Aspose.Cells dla platformy .NET 
```csharp
// Utwórz instancję klasy Workbook
Workbook book = new Workbook();
// Uzyskaj dostęp do pierwszego arkusza
Worksheet sheet = book.Worksheets[0];
// Ustaw rozmiar papieru na A2 i wydrukuj szerokość i wysokość papieru w calach
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Ustaw rozmiar papieru na A3 i wydrukuj szerokość i wysokość papieru w calach
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Ustaw rozmiar papieru na A4 i wydrukuj szerokość i wysokość papieru w calach
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Ustaw rozmiar papieru na Letter i wydrukuj szerokość i wysokość papieru w calach
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
Console.WriteLine("GetPageDimensions executed successfully.\r\n");
```

## Wniosek

Gratulacje! Nauczyłeś się, jak pobierać wymiary strony za pomocą Aspose.Cells dla .NET. Ta funkcja może być przydatna, gdy trzeba wykonać określone operacje w oparciu o wymiary strony w plikach Excel.

Nie zapomnij dokładniej zapoznać się z dokumentacją Aspose.Cells, aby odkryć wszystkie zaawansowane funkcje, jakie oferuje.

### Często zadawane pytania

#### 1. Jakie inne rozmiary papieru obsługuje Aspose.Cells for .NET?

Aspose.Cells dla .NET obsługuje różne rozmiary papieru, w tym A1, A5, B4, B5, Executive, Legal, Letter i wiele innych. Pełną listę obsługiwanych rozmiarów papieru można znaleźć w dokumentacji.

#### 2. Czy mogę ustawić niestandardowe wymiary strony za pomocą Aspose.Cells dla .NET?

Tak, możesz ustawić niestandardowe wymiary strony, określając żądaną szerokość i wysokość. Aspose.Cells oferuje pełną elastyczność w dostosowywaniu wymiarów strony do Twoich potrzeb.

#### 3. Czy mogę uzyskać wymiary strony w jednostkach innych niż cale?

Tak, Aspose.Cells dla .NET pozwala uzyskać wymiary strony w różnych jednostkach, w tym calach, centymetrach, milimetrach i punktach.

#### 4. Czy Aspose.Cells for .NET obsługuje inne funkcje edycji ustawień strony?

Tak, Aspose.Cells oferuje pełen zakres funkcji do edycji ustawień strony, w tym ustawianie marginesów, orientacji, nagłówków i stopek itp.