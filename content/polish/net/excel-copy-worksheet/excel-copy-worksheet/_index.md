---
title: Arkusz kopiowania programu Excel
linktitle: Arkusz kopiowania programu Excel
second_title: Aspose.Cells dla .NET API odniesienia
description: Skopiuj jeden arkusz Excela do drugiego za pomocą Aspose.Cells dla .NET.
type: docs
weight: 20
url: /pl/net/excel-copy-worksheet/excel-copy-worksheet/
---

W tym przewodniku wyjaśnimy, jak skopiować arkusz programu Excel przy użyciu biblioteki Aspose.Cells dla .NET. Dostarczymy Ci kod źródłowy C# i przeprowadzimy Cię przez kroki niezbędne do wykonania tego zadania. Na koniec pokażemy oczekiwany rezultat. Aby rozpocząć, postępuj zgodnie z poniższymi instrukcjami.

## Krok 1: Przygotowanie

Zanim zaczniesz, upewnij się, że zainstalowałeś Aspose.Cells dla .NET i utworzyłeś projekt C# w preferowanym zintegrowanym środowisku programistycznym (IDE). Upewnij się także, że masz kopię pliku Excel, którym chcesz manipulować.

## Krok 2: Zaimportuj wymagane biblioteki

 W pliku źródłowym C# zaimportuj niezbędne biblioteki z Aspose.Cells za pomocą`using` dyrektywa:

```csharp
using Aspose.Cells;
```

## Krok 3: Ustaw ścieżkę pliku

 Zadeklaruj`dataDir` zmienną i zainicjuj ją katalogiem zawierającym plik Excel. Na przykład :

```csharp
string dataDir = "PATH_TO_YOUR_DOCUMENT_DIRECTORY";
```

 Pamiętaj o wymianie`"PATH_TO_YOUR_DOCUMENT_DIRECTORY"` z rzeczywistą ścieżką do katalogu.

## Krok 4: Załaduj istniejący plik Excel

 Użyj`Workbook` class z Aspose.Cells, aby otworzyć istniejący plik Excel. Użyj`InputPath` zmienna określająca ścieżkę pliku:

```csharp
string InputPath = dataDir + "book1.xls";
Workbook wb = new Workbook(InputPath);
```

 Upewnij się, że wymieniłeś`"book1.xls"` z rzeczywistą nazwą pliku Excel.

## Krok 5: Skopiuj arkusz

 Teraz skopiujemy istniejący arkusz do nowego arkusza. Użyj`Worksheets` własność`Workbook` obiekt umożliwiający dostęp do kolekcji arkuszy:

```csharp
WorksheetCollection sheets = wb.Worksheets;
```

 Następnie użyj`AddCopy` metoda kopiowania określonego arkusza. Na przykład, aby skopiować „Arkusz 1”:

```csharp
sheets.AddCopy("Sheet1");
```

## Krok 6: Zapisz plik Excel

 Użyj`Save` metoda`Workbook` obiekt, aby zapisać zmiany w nowym pliku:

```csharp
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

Pamiętaj, aby określić żądaną ścieżkę i nazwę pliku wyjściowego.

### Przykładowy kod źródłowy programu Excel Copy Worksheet przy użyciu Aspose.Cells dla .NET 

```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Otwórz istniejący plik Excel.
Workbook wb = new Workbook(InputPath);
// Utwórz obiekt Arkusze w odniesieniu do
// arkusze Zeszytu ćwiczeń.
WorksheetCollection sheets = wb.Worksheets;
// Skopiuj dane do nowego arkusza z istniejącego
// arkusz w skoroszycie.
sheets.AddCopy("Sheet1");
// Zapisz plik Excela.
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

## Wniosek

Gratulacje! Nauczyłeś się teraz, jak skopiować arkusz programu Excel za pomocą Aspose.Cells dla .NET. Ten przewodnik krok po kroku pokazał, jak zaimportować niezbędne biblioteki, załadować istniejący plik Excel, skopiować arkusz i zapisać zmodyfikowany plik. Możesz użyć tej metody we własnych projektach, aby efektywnie manipulować plikami Excel.

### Często zadawane pytania

#### P. Czy Aspose.Cells jest kompatybilny z innymi językami programowania?

A. Tak, Aspose.Cells obsługuje wiele języków programowania, w tym C#, Java, Python i wiele innych.

#### P. Czy mogę skopiować arkusz do innego skoroszytu programu Excel?

A.  Tak, możesz skorzystać z`AddCopy` metoda kopiowania arkusza do innego skoroszytu programu Excel.

#### P. Czy Aspose.Cells zachowuje formuły i formatowanie podczas kopiowania arkusza?

A. Tak, Aspose.Cells zachowuje formuły, formatowanie i inne właściwości podczas kopiowania arkusza.

#### P. Czy Aspose.Cells wymaga licencji do użytku komercyjnego?

A. Tak, Aspose.Cells jest produktem komercyjnym i wymaga zakupu licencji do użytku komercyjnego. Więcej informacji licencyjnych można znaleźć na oficjalnej stronie Aspose.