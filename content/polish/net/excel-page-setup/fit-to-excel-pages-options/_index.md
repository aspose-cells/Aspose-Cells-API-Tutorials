---
title: Opcje dopasowania do stron programu Excel
linktitle: Opcje dopasowania do stron programu Excel
second_title: Aspose.Cells dla .NET API odniesienia
description: Dowiedz się, jak automatycznie dopasowywać strony w arkuszu kalkulacyjnym Excel za pomocą Aspose.Cells dla .NET.
type: docs
weight: 30
url: /pl/net/excel-page-setup/fit-to-excel-pages-options/
---
W tym artykule poprowadzimy Cię krok po kroku do wyjaśnienia następującego kodu źródłowego C#: Dopasuj do opcji stron programu Excel przy użyciu Aspose.Cells dla .NET. Do wykonania tej operacji użyjemy biblioteki Aspose.Cells dla .NET. Wykonaj poniższe czynności, aby skonfigurować dopasowanie do stron w programie Excel.

## Krok 1: Tworzenie skoroszytu
Pierwszym krokiem jest utworzenie skoroszytu. Zamierzamy utworzyć instancję obiektu Workbook. Oto kod umożliwiający utworzenie skoroszytu:

```csharp
// Ścieżka do katalogu dokumentów
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Utwórz instancję obiektu skoroszytu
Workbook workbook = new Workbook();
```

## Krok 2: Dostęp do arkusza
Teraz, gdy utworzyliśmy skoroszyt, musimy przejść do pierwszego arkusza. Aby uzyskać dostęp do pierwszego arkusza, użyjemy indeksu 0. Oto kod umożliwiający dostęp do niego:

```csharp
// Dostęp do pierwszego arkusza w skoroszycie
Worksheet worksheet = workbook.Worksheets[0];
```

## Krok 3: Ustawianie dopasowania do stron
 W tym kroku skonfigurujemy dopasowanie do stron arkusza. Będziemy korzystać z`FitToPagesTall` I`FitToPagesWide` właściwości`PageSetup` obiekt, aby określić żądaną liczbę stron dla wysokości i szerokości arkusza. Oto kod do tego:

```csharp
// Skonfiguruj liczbę stron dla wysokości arkusza
worksheet.PageSetup.FitToPagesTall = 1;

// Skonfiguruj liczbę stron dla szerokości arkusza
worksheet.PageSetup.FitToPagesWide = 1;
```

## Krok 4: Zapisywanie skoroszytu
 Teraz, gdy skonfigurowaliśmy dopasowanie do stron, możemy zapisać skoroszyt. Będziemy korzystać z`Save` w tym celu metodę obiektu Workbook. Oto kod umożliwiający zapisanie skoroszytu:

```csharp
// Zapisz skoroszyt
workbook.Save(dataDir + "FitToPagesOptions_out.xls");
```

### Przykładowy kod źródłowy opcji Dopasuj do stron programu Excel przy użyciu Aspose.Cells dla .NET 
```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Tworzenie instancji obiektu skoroszytu
Workbook workbook = new Workbook();
// Dostęp do pierwszego arkusza w pliku Excel
Worksheet worksheet = workbook.Worksheets[0];
// Ustawienie liczby stron, do których zostanie rozciągnięta długość arkusza
worksheet.PageSetup.FitToPagesTall = 1;
//Ustawienie liczby stron, do których zostanie rozciągnięta szerokość arkusza
worksheet.PageSetup.FitToPagesWide = 1;
// Zapisz skoroszyt.
workbook.Save(dataDir + "FitToPagesOptions_out.xls");
```

## Wniosek
W tym artykule dowiedzieliśmy się, jak skonfigurować dopasowanie do stron w programie Excel przy użyciu Aspose.Cells dla .NET. Wykonaliśmy następujące kroki: utworzenie skoroszytu, uzyskanie dostępu do arkusza, skonfigurowanie dopasowania do stron i zapisanie skoroszytu. Teraz możesz wykorzystać tę wiedzę, aby dostosować swoje arkusze kalkulacyjne do żądanych stron.

### Często zadawane pytania

#### P: Jak mogę zainstalować Aspose.Cells dla .NET?

Odp.: Aby zainstalować Aspose.Cells dla .NET, możesz użyć menedżera pakietów NuGet w programie Visual Studio. Znajdź pakiet „Aspose.Cells” i zainstaluj go w swoim projekcie.

#### P: Czy mogę dopasować strony zarówno pod względem wysokości, jak i szerokości?

 Odp.: Tak, możesz dostosować zarówno wysokość, jak i szerokość arkusza za pomocą`FitToPagesTall` I`FitToPagesWide` nieruchomości. Możesz określić żądaną liczbę stron dla każdego wymiaru.

#### P: Jak mogę dostosować opcje Dopasuj do stron?

Odp.: Oprócz określenia liczby stron można także dostosować inne opcje dopasowania do stron, takie jak skala arkusza, orientacja papieru, marginesy i inne. Skorzystaj z właściwości dostępnych w pliku`PageSetup` obiekt do tego.

#### P: Czy mogę używać Aspose.Cells for .NET do przetwarzania istniejących skoroszytów?

Odp.: Tak, możesz używać Aspose.Cells for .NET do otwierania i edytowania istniejących skoroszytów. Możesz uzyskiwać dostęp do arkuszy, komórek, formuł, stylów i innych elementów skoroszytu, aby wykonywać różne operacje.