---
title: Ustaw orientację strony programu Excel
linktitle: Ustaw orientację strony programu Excel
second_title: Aspose.Cells dla .NET API odniesienia
description: Dowiedz się, jak krok po kroku ustawić orientację strony programu Excel za pomocą Aspose.Cells dla .NET. Uzyskaj zoptymalizowane wyniki.
type: docs
weight: 130
url: /pl/net/excel-page-setup/set-excel-page-orientation/
---
W dzisiejszej erze cyfrowej arkusze kalkulacyjne Excel odgrywają kluczową rolę w organizowaniu i analizowaniu danych. Czasami konieczne staje się dostosowanie układu i wyglądu dokumentów Excel do konkretnych wymagań. Jednym z takich dostosowań jest ustawienie orientacji strony, która określa, czy drukowana strona będzie w trybie pionowym, czy poziomym. W tym samouczku omówimy proces ustawiania orientacji strony programu Excel przy użyciu Aspose.Cells, potężnej biblioteki do programowania .NET. Zanurzmy się!

## Zrozumienie znaczenia ustawienia orientacji strony w programie Excel

Orientacja strony dokumentu Excel wpływa na sposób wyświetlania zawartości po wydrukowaniu. Domyślnie Excel używa orientacji pionowej, w której strona jest wyższa niż szersza. Jednak w niektórych scenariuszach bardziej odpowiednia może być orientacja pozioma, w której strona jest szersza niż wysoka. Na przykład podczas drukowania szerokich tabel, wykresów lub diagramów orientacja pozioma zapewnia lepszą czytelność i reprezentację wizualną.

## Eksplorowanie biblioteki Aspose.Cells dla platformy .NET

Aspose.Cells to bogata w funkcje biblioteka, która umożliwia programistom programowe tworzenie, manipulowanie i konwertowanie plików Excel. Zapewnia szeroką gamę interfejsów API do wykonywania różnych zadań, w tym ustawiania orientacji strony. Zanim zagłębimy się w kod, upewnij się, że masz bibliotekę Aspose.Cells dodaną do swojego projektu .NET.

## Krok 1: Konfiguracja katalogu dokumentów

Zanim zaczniemy pracować z plikiem Excel, musimy skonfigurować katalog dokumentów. Zastąp symbol zastępczy „TWOJ KATALOG DOKUMENTÓW” we fragmencie kodu rzeczywistą ścieżką do katalogu, w którym chcesz zapisać plik wyjściowy.

```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENT DIRECTORY";
```

## Krok 2: Tworzenie instancji obiektu skoroszytu

Aby pracować z plikiem Excel, musimy utworzyć instancję klasy Workbook dostarczonej przez Aspose.Cells. Ta klasa reprezentuje cały plik Excel i udostępnia metody i właściwości umożliwiające manipulowanie jego zawartością.

```csharp
// Tworzenie instancji obiektu skoroszytu
Workbook workbook = new Workbook();
```

## Krok 3: Dostęp do arkusza w pliku Excel

Następnie musimy uzyskać dostęp do arkusza w pliku Excel, w którym chcemy ustawić orientację strony. W tym przykładzie będziemy pracować z pierwszym arkuszem (indeks 0) skoroszytu.

```csharp
// Dostęp do pierwszego arkusza w pliku Excel
Worksheet worksheet = workbook.Worksheets[0];
```

## Krok 4: Ustawienie orientacji strony na Pionową

Teraz czas ustawić orientację strony. Aspose.Cells udostępnia właściwość PageSetup dla każdego arkusza, która pozwala nam dostosować różne ustawienia związane ze stroną. Aby ustawić orientację strony, musimy przypisać wartość PageOrientationType.Portrait do właściwości Orientation obiektu PageSetup.

```csharp
// Ustawianie orientacji na Portret
worksheet.PageSetup.Orientation = PageOrientationType.Portrait;
```

## Krok 5: Zapisywanie skoroszytu

Po dokonaniu niezbędnych zmian w arkuszu możemy zapisać zmodyfikowany obiekt Workbook do pliku. Metoda Save klasy Workbook akceptuje ścieżkę pliku, w którym zostanie zapisany plik wyjściowy

.

```csharp
// Zapisz skoroszyt.
workbook.Save(dataDir + "PageOrientation_out.xls");
```

### Przykładowy kod źródłowy dla Ustaw orientację strony programu Excel przy użyciu Aspose.Cells dla .NET 

```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Tworzenie instancji obiektu skoroszytu
Workbook workbook = new Workbook();
// Dostęp do pierwszego arkusza w pliku Excel
Worksheet worksheet = workbook.Worksheets[0];
// Ustawianie orientacji na Portret
worksheet.PageSetup.Orientation = PageOrientationType.Portrait;
// Zapisz skoroszyt.
workbook.Save(dataDir + "PageOrientation_out.xls");
```

## Wniosek

tym samouczku nauczyliśmy się, jak ustawić orientację strony Excela za pomocą Aspose.Cells dla .NET. Postępując zgodnie ze szczegółowym przewodnikiem, możesz łatwo dostosować orientację strony plików Excel zgodnie ze swoimi konkretnymi wymaganiami. Aspose.Cells zapewnia kompleksowy zestaw interfejsów API do manipulowania dokumentami Excel, dając pełną kontrolę nad ich wyglądem i zawartością. Zacznij odkrywać możliwości Aspose.Cells i usprawnij swoje zadania automatyzacji w programie Excel.

## Często zadawane pytania

#### P1: Czy mogę ustawić orientację strony na poziomą zamiast pionową?

 A1: Tak, absolutnie! Zamiast przypisywać`PageOrientationType.Portrait` wartość, możesz użyć`PageOrientationType.Landscape` aby ustawić orientację strony na poziomą.

#### P2: Czy Aspose.Cells obsługuje inne formaty plików oprócz Excela?

Odpowiedź 2: Tak, Aspose.Cells obsługuje szeroką gamę formatów plików, w tym XLS, XLSX, CSV, HTML, PDF i wiele innych. Zapewnia interfejsy API do tworzenia, manipulowania i konwertowania plików w różnych formatach.

#### P3: Czy mogę ustawić różne orientacje strony dla różnych arkuszy w tym samym pliku Excel?

 O3: Tak, możesz ustawić różne orientacje strony dla różnych arkuszy kalkulacyjnych, uzyskując dostęp do`PageSetup` obiekt każdego arkusza indywidualnie i modyfikowanie jego`Orientation` odpowiednio własność.

#### P4: Czy Aspose.Cells jest kompatybilny zarówno z .NET Framework, jak i .NET Core?

O4: Tak, Aspose.Cells jest kompatybilny zarówno z .NET Framework, jak i .NET Core. Obsługuje szeroką gamę wersji .NET, dzięki czemu można go używać w różnych środowiskach programistycznych.
