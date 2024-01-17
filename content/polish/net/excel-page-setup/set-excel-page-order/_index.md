---
title: Ustaw kolejność stron w programie Excel
linktitle: Ustaw kolejność stron w programie Excel
second_title: Aspose.Cells dla .NET API odniesienia
description: Przewodnik krok po kroku dotyczący ustawiania kolejności stron w programie Excel przy użyciu Aspose.Cells dla .NET. W zestawie szczegółowe instrukcje i kod źródłowy.
type: docs
weight: 120
url: /pl/net/excel-page-setup/set-excel-page-order/
---
tym artykule poprowadzimy Cię krok po kroku, aby wyjaśnić następujący kod źródłowy C#, aby ustawić kolejność stron w Excelu za pomocą Aspose.Cells dla .NET. Pokażemy Ci, jak skonfigurować katalog dokumentów, utworzyć instancję obiektu Workbook, uzyskać odwołanie do PageSetup, ustawić kolejność drukowania stron i zapisać skoroszyt.

## Krok 1: Konfiguracja katalogu dokumentów

 Zanim zaczniesz, musisz skonfigurować katalog dokumentów, w którym chcesz zapisać plik Excel. Możesz określić ścieżkę katalogu, zastępując wartość`dataDir` zmienną z własną ścieżką.

```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

## Krok 2: Tworzenie instancji obiektu skoroszytu

Pierwszym krokiem jest utworzenie instancji obiektu Workbook. Reprezentuje skoroszyt programu Excel, z którym będziemy pracować.

```csharp
// Utwórz instancję obiektu skoroszytu
Workbook workbook = new Workbook();
```

## Krok 3: Uzyskanie odniesienia do PageSetup

Następnie musimy uzyskać odwołanie do obiektu PageSetup arkusza, w którym chcemy ustawić kolejność stron.

```csharp
// Uzyskaj odwołanie do PageSetup arkusza
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## Krok 4: Ustawianie kolejności drukowania stron

Teraz możemy ustawić kolejność drukowania stron. W tym przykładzie używamy opcji „OverThenDown”, co oznacza, że strony będą drukowane od lewej do prawej, a następnie od góry do dołu.

```csharp
// Ustaw kolejność drukowania stron na „OverThenDown”
pageSetup.Order = PrintOrderType.OverThenDown;
```

## Krok 5: Zapisywanie skoroszytu

Na koniec zapisujemy skoroszyt programu Excel ze zmianami kolejności stron.

```csharp
// Zapisz skoroszyt
workbook.Save(dataDir + "SetPageOrder_out.xls");
```

### Przykładowy kod źródłowy dla Ustaw kolejność stron w programie Excel przy użyciu Aspose.Cells dla .NET 
```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Tworzenie instancji obiektu skoroszytu
Workbook workbook = new Workbook();
// Uzyskanie odniesienia do PageSetup arkusza
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Ustawienie kolejności drukowania stron od góry do dołu
pageSetup.Order = PrintOrderType.OverThenDown;
// Zapisz skoroszyt.
workbook.Save(dataDir + "SetPageOrder_out.xls");
```

## Wniosek

W tym samouczku wyjaśniliśmy, jak ustawić kolejność stron w pliku Excel za pomocą Aspose.Cells dla .NET. Wykonując podane kroki, możesz łatwo skonfigurować katalog dokumentów, utworzyć instancję obiektu Workbook, uzyskać odwołanie do PageSetup, ustawić kolejność drukowania stron i zapisać skoroszyt.

### Często zadawane pytania

#### P1: Dlaczego ważne jest ustawienie kolejności stron w pliku Excel?

Określenie kolejności stron w pliku Excel jest ważne, ponieważ określa sposób drukowania lub wyświetlania stron. Określając konkretną kolejność, możesz logicznie uporządkować dane i ułatwić odczytanie lub wydrukowanie pliku.

#### P2: Czy mogę używać innych zamówień drukowania stron z Aspose.Cells dla .NET?

Tak, Aspose.Cells dla .NET obsługuje wielostronicowe polecenia drukowania, takie jak „DownThenOver”, „OverThenDown”, „DownThenOverThenDownAgain” itp. Możesz wybrać ten, który najlepiej odpowiada Twoim potrzebom.

#### P3: Czy mogę ustawić dodatkowe opcje drukowania stron za pomocą Aspose.Cells dla .NET?

Tak, możesz ustawić różne opcje drukowania strony, takie jak skala, orientacja, marginesy itp., korzystając z właściwości obiektu PageSetup w Aspose.Cells dla .NET.

#### P4: Czy Aspose.Cells dla .NET obsługuje inne formaty plików Excel?

Tak, Aspose.Cells dla .NET obsługuje szeroką gamę formatów plików Excel, takich jak XLSX, XLS, CSV, HTML, PDF itp. Możesz łatwo konwertować pomiędzy tymi formatami, korzystając z funkcji udostępnianych przez bibliotekę.