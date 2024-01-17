---
title: Excel Kopiuj arkusze między skoroszytami
linktitle: Excel Kopiuj arkusze między skoroszytami
second_title: Aspose.Cells dla .NET API odniesienia
description: Z łatwością kopiuj arkusze między skoroszytami programu Excel za pomocą Aspose.Cells dla .NET.
type: docs
weight: 30
url: /pl/net/excel-copy-worksheet/excel-copy-worksheets-between-workbooks/
---
tym samouczku przeprowadzimy Cię przez kolejne kroki kopiowania arkuszy między skoroszytami programu Excel przy użyciu biblioteki Aspose.Cells dla platformy .NET. Aby ukończyć to zadanie, postępuj zgodnie z poniższymi instrukcjami.

## Krok 1: Przygotowanie

Upewnij się, że zainstalowałeś Aspose.Cells dla .NET i utworzyłeś projekt C# w preferowanym zintegrowanym środowisku programistycznym (IDE).

## Krok 2: Ustaw ścieżkę katalogu dokumentów

 Zadeklaruj`dataDir` zmienną i zainicjuj ją ścieżką do katalogu dokumentów. Na przykład :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Pamiętaj o wymianie`"YOUR_DOCUMENTS_DIRECTORY"` z rzeczywistą ścieżką do katalogu.

## Krok 3: Zdefiniuj ścieżkę pliku wejściowego

 Zadeklaruj`InputPath` zmienną i zainicjuj ją pełną ścieżką pliku Excel, z którego chcesz skopiować arkusz kalkulacyjny. Na przykład :

```csharp
string InputPath = dataDir + "book1.xls";
```

 Upewnij się, że masz plik Excel`book1.xls` w katalogu dokumentów lub podaj poprawną nazwę pliku i lokalizację.

## Krok 4: Utwórz pierwszy skoroszyt programu Excel

 Użyj`Workbook` klasa Aspose.Cells, aby utworzyć pierwszy skoroszyt programu Excel i otworzyć określony plik:

```csharp
Workbook excelWorkbook0 = new Workbook(InputPath);
```

## Krok 5: Utwórz drugi skoroszyt programu Excel

Utwórz drugi skoroszyt programu Excel:

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## Krok 6: Skopiuj arkusz z pierwszego skoroszytu do drugiego skoroszytu

 Użyj`Copy`metoda kopiowania pierwszego arkusza z pierwszego skoroszytu do drugiego skoroszytu:

```csharp
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
```

## Krok 7: Zapisz plik Excel

Zapisz plik Excel zawierający skopiowany arkusz kalkulacyjny:

```csharp
excelWorkbook1.Save(dataDir + "Copy WorksheetsBetweenWorkbooks_out.xls");
```

Pamiętaj, aby określić żądaną ścieżkę i nazwę pliku wyjściowego.

### Przykładowy kod źródłowy programu Excel Kopiuj arkusze między skoroszytami przy użyciu Aspose.Cells dla .NET 
```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Utwórz skoroszyt.
// Otwórz plik w pierwszej książce.
Workbook excelWorkbook0 = new Workbook(InputPath);
// Utwórz kolejny skoroszyt.
Workbook excelWorkbook1 = new Workbook();
// Skopiuj pierwszy arkusz pierwszej książki do drugiej książki.
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
// Zapisz plik.
excelWorkbook1.Save(dataDir + "CopyWorksheetsBetweenWorkbooks_out.xls");
```

## Wniosek

Gratulacje! Nauczyłeś się teraz, jak kopiować arkusze między skoroszytami programu Excel przy użyciu Aspose.Cells dla .NET. Możesz użyć tej metody we własnych projektach, aby efektywnie manipulować plikami Excel.

### Często zadawane pytania

#### P. Jakie biblioteki są potrzebne do korzystania z Aspose.Cells dla .NET?

A. Aby używać Aspose.Cells dla .NET, musisz dołączyć bibliotekę Aspose.Cells do swojego projektu. Upewnij się, że poprawnie odniosłeś się do tej biblioteki w zintegrowanym środowisku programistycznym (IDE).

#### P. Czy Aspose.Cells obsługuje inne formaty plików Excel, takie jak XLSX?

A. Tak, Aspose.Cells obsługuje różne formaty plików Excel, w tym XLSX, XLS, CSV, HTML i wiele innych. Możesz manipulować tymi formatami plików, korzystając z funkcji Aspose.Cells dla .NET.

#### P. Czy mogę dostosować opcje układu podczas kopiowania arkusza kalkulacyjnego?

A.  Tak, możesz dostosować opcje ustawień strony podczas kopiowania arkusza kalkulacyjnego, korzystając z właściwości pliku`PageSetup` obiekt. Możesz określić nagłówki, stopki, marginesy, orientację strony itp.