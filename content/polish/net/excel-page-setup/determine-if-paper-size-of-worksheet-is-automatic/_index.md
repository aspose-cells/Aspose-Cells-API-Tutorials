---
title: Określ, czy rozmiar papieru w arkuszu jest automatyczny
linktitle: Określ, czy rozmiar papieru w arkuszu jest automatyczny
second_title: Aspose.Cells dla .NET API odniesienia
description: Dowiedz się, jak określić, czy rozmiar papieru arkusza kalkulacyjnego jest automatyczny, za pomocą Aspose.Cells dla .NET.
type: docs
weight: 20
url: /pl/net/excel-page-setup/determine-if-paper-size-of-worksheet-is-automatic/
---
tym artykule poprowadzimy Cię krok po kroku do wyjaśnienia następującego kodu źródłowego C#: Ustal, czy rozmiar papieru w arkuszu kalkulacyjnym jest automatyczny, używając Aspose.Cells dla .NET. Do wykonania tej operacji użyjemy biblioteki Aspose.Cells dla .NET. Wykonaj poniższe czynności, aby określić, czy rozmiar papieru w arkuszu jest automatyczny.

## Krok 1: Ładowanie skoroszytów
Pierwszym krokiem jest załadowanie skoroszytów. Będziemy mieć dwa skoroszyty: jeden z wyłączonym automatycznym rozmiarem papieru, a drugi z włączonym automatycznym rozmiarem papieru. Oto kod ładujący skoroszyty:

```csharp
// katalog źródłowy
string sourceDir = "YOUR_SOURCE_DIR";
// Katalog wyjściowy
string outputDir = "YOUR_OUTPUT_DIRECTORY";

// Załaduj pierwszy skoroszyt z wyłączonym automatycznym rozmiarem papieru
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");

// Załaduj drugi skoroszyt z włączoną funkcją automatycznego rozmiaru papieru
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
```

## Krok 2: Dostęp do arkuszy kalkulacyjnych
Teraz, gdy załadowaliśmy skoroszyty, musimy uzyskać dostęp do arkuszy, aby sprawdzić automatyczny rozmiar papieru. Przejdziemy do pierwszego arkusza z dwóch skoroszytów. Oto kod umożliwiający dostęp do niego:

```csharp
//Przejdź do pierwszego arkusza pierwszego skoroszytu
Worksheet ws11 = wb1.Worksheets[0];

// Przejdź do pierwszego arkusza drugiego skoroszytu
Worksheet ws12 = wb2.Worksheets[0];
```

## Krok 3: Sprawdź automatyczny rozmiar papieru
 W tym kroku sprawdzimy, czy rozmiar papieru arkusza jest automatyczny. Będziemy korzystać z`PageSetup.IsAutomaticPaperSize` właściwość, aby uzyskać te informacje. Następnie wyświetlimy wynik. Oto kod do tego:

```csharp
// Wyświetl właściwość IsAutomaticPaperSize pierwszego arkusza w pierwszym skoroszycie
Console.WriteLine("First worksheet in first workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);

// Wyświetl właściwość IsAutomaticPaperSize pierwszego arkusza w drugim skoroszycie
Console.WriteLine("First worksheet of second workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);

```

### Przykładowy kod źródłowy dla określenia, czy rozmiar papieru w arkuszu jest automatyczny przy użyciu Aspose.Cells dla .NET 
```csharp
//Katalog źródłowy
string sourceDir = "YOUR_SOURCE_DIRECTORY";
//Katalog wyjściowy
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//Załaduj pierwszy skoroszyt, w którym automatyczny rozmiar papieru jest fałszywy
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");
//Załaduj drugi skoroszyt z ustawionym automatycznym rozmiarem papieru
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
//Uzyskaj dostęp do pierwszego arkusza obu skoroszytów
Worksheet ws11 = wb1.Worksheets[0];
Worksheet ws12 = wb2.Worksheets[0];
//Wydrukuj właściwość PageSetup.IsAutomaticPaperSize obu arkuszy
Console.WriteLine("First Worksheet of First Workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);
Console.WriteLine("First Worksheet of Second Workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);
Console.WriteLine();
Console.WriteLine("DetermineIfPaperSizeOfWorksheetIsAutomatic executed successfully.\r\n");
```


## Wniosek
tym artykule dowiedzieliśmy się, jak określić, czy rozmiar papieru w arkuszu kalkulacyjnym jest automatyczny przy użyciu Aspose.Cells dla .NET. Wykonaliśmy następujące kroki: załadowanie skoroszytów,

dostęp do arkuszy kalkulacyjnych i automatyczne sprawdzanie formatu papieru. Teraz możesz wykorzystać tę wiedzę, aby określić, czy rozmiar papieru w arkuszach kalkulacyjnych jest automatyczny.

### Często zadawane pytania

#### P: Jak mogę załadować skoroszyty za pomocą Aspose.Cells dla .NET?

Odp.: Możesz ładować skoroszyty za pomocą klasy Workbook z biblioteki Aspose.Cells. Użyj metody Workbook.Load, aby załadować skoroszyt z pliku.

#### P: Czy mogę sprawdzić automatyczny rozmiar papieru w innych arkuszach kalkulacyjnych?

Odp.: Tak, możesz sprawdzić automatyczny rozmiar papieru dla dowolnego arkusza, uzyskując dostęp do właściwości PageSetup.IsAutomaticPaperSize odpowiedniego obiektu Worksheet.

#### P: Jak mogę zmienić automatyczny rozmiar papieru arkusza kalkulacyjnego?

Odp.: Aby zmienić automatyczny rozmiar papieru w arkuszu, możesz użyć właściwości PageSetup.IsAutomaticPaperSize i ustawić dla niej żądaną wartość (prawda lub fałsz).

#### P: Jakie inne funkcje oferuje Aspose.Cells dla .NET?

Odp.: Aspose.Cells dla .NET oferuje wiele funkcji do pracy z arkuszami kalkulacyjnymi, takich jak tworzenie, modyfikowanie i konwertowanie skoroszytów, a także manipulowanie danymi, formułami i formatowaniem.