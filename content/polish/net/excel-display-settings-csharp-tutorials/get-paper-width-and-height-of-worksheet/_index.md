---
title: Uzyskaj szerokość i wysokość papieru w arkuszu
linktitle: Uzyskaj szerokość i wysokość papieru w arkuszu
second_title: Aspose.Cells dla .NET API odniesienia
description: Utwórz przewodnik krok po kroku wyjaśniający następujący kod źródłowy C#, aby uzyskać szerokość i wysokość papieru w arkuszu kalkulacyjnym za pomocą Aspose.Cells dla .NET.
type: docs
weight: 80
url: /pl/net/excel-display-settings-csharp-tutorials/get-paper-width-and-height-of-worksheet/
---
tym samouczku poprowadzimy Cię krok po kroku, aby wyjaśnić następujący kod źródłowy C#, aby uzyskać szerokość i wysokość papieru w arkuszu przy użyciu Aspose.Cells dla .NET. Wykonaj poniższe kroki:

## Krok 1: Utwórz skoroszyt
 Zacznij od utworzenia nowego skoroszytu za pomocą pliku`Workbook` klasa:

```csharp
Workbook wb = new Workbook();
```

## Krok 2: Uzyskaj dostęp do pierwszego arkusza
 Następnie przejdź do pierwszego arkusza w skoroszycie, używając przycisku`Worksheet` klasa:

```csharp
Worksheet ws = wb.Worksheets[0];
```

## Krok 3: Ustaw rozmiar papieru na A2 i pokaż szerokość i wysokość papieru w calach
 Użyj`PaperSize` własność`PageSetup` obiekt, aby ustawić rozmiar papieru na A2, a następnie użyj przycisku`PaperWidth` I`PaperHeight` właściwości, aby uzyskać odpowiednio szerokość i wysokość papieru. Wyświetl te wartości za pomocą`Console.WriteLine` metoda:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

## Krok 4: Powtórz kroki dla innych rozmiarów papieru
Powtórz poprzednie kroki, zmieniając rozmiar papieru na A3, A4 i Letter, a następnie wyświetlając wartości szerokości i wysokości papieru dla każdego rozmiaru:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

### Przykładowy kod źródłowy narzędzia Uzyskaj szerokość i wysokość papieru przy użyciu Aspose.Cells dla platformy .NET 

```csharp
//Utwórz skoroszyt
Workbook wb = new Workbook();
//Uzyskaj dostęp do pierwszego arkusza
Worksheet ws = wb.Worksheets[0];
//Ustaw rozmiar papieru na A2 i wydrukuj szerokość i wysokość papieru w calach
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Ustaw rozmiar papieru na A3 i wydrukuj szerokość i wysokość papieru w calach
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Ustaw rozmiar papieru na A4 i wydrukuj szerokość i wysokość papieru w calach
ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Ustaw rozmiar papieru na Letter i wydrukuj szerokość i wysokość papieru w calach
ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```


## Wniosek

Nauczyłeś się, jak używać Aspose.Cells dla .NET, aby uzyskać szerokość i wysokość papieru w arkuszu kalkulacyjnym. Ta funkcja może być przydatna do konfiguracji i precyzyjnego układu dokumentów Excel.

### Często zadawane pytania (FAQ)

#### Co to jest Aspose.Cells dla .NET?

Aspose.Cells dla .NET to potężna biblioteka do manipulowania i przetwarzania plików Excel w aplikacjach .NET. Oferuje wiele funkcji do tworzenia, modyfikowania, konwertowania i analizowania plików Excel.

#### Jak mogę uzyskać rozmiar papieru arkusza kalkulacyjnego za pomocą Aspose.Cells dla .NET?

 Możesz skorzystać z`PageSetup` klasa`Worksheet` obiekt, aby uzyskać dostęp do rozmiaru papieru. Użyj`PaperSize` właściwość, aby ustawić rozmiar papieru i`PaperWidth` I`PaperHeight` właściwości, aby uzyskać odpowiednio szerokość i wysokość papieru.

#### Jakie rozmiary papieru obsługuje Aspose.Cells dla .NET?

Aspose.Cells dla .NET obsługuje szeroką gamę powszechnie używanych rozmiarów papieru, takich jak A2, A3, A4 i Letter, a także wiele innych niestandardowych rozmiarów.

#### Czy mogę dostosować rozmiar papieru arkusza kalkulacyjnego za pomocą Aspose.Cells dla .NET?

 Tak, możesz ustawić niestandardowy rozmiar papieru, określając dokładne wymiary szerokości i wysokości za pomocą`PaperWidth` I`PaperHeight` właściwości`PageSetup` klasa.