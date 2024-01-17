---
title: Arkusz przenoszenia programu Excel
linktitle: Arkusz przenoszenia programu Excel
second_title: Aspose.Cells dla .NET API odniesienia
description: Z łatwością przenieś arkusz do skoroszytu programu Excel za pomocą Aspose.Cells dla .NET.
type: docs
weight: 40
url: /pl/net/excel-copy-worksheet/excel-move-worksheet/
---
tym samouczku przeprowadzimy Cię przez kolejne etapy przenoszenia arkusza do skoroszytu programu Excel przy użyciu biblioteki Aspose.Cells dla platformy .NET. Aby ukończyć to zadanie, postępuj zgodnie z poniższymi instrukcjami.


## Krok 1: Przygotowanie

Upewnij się, że zainstalowałeś Aspose.Cells dla .NET i utworzyłeś projekt C# w preferowanym zintegrowanym środowisku programistycznym (IDE).

## Krok 2: Ustaw ścieżkę katalogu dokumentów

 Zadeklaruj`dataDir` zmienną i zainicjuj ją ścieżką do katalogu dokumentów. Na przykład :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Pamiętaj o wymianie`"YOUR_DOCUMENTS_DIRECTORY"` z rzeczywistą ścieżką do katalogu.

## Krok 3: Zdefiniuj ścieżkę pliku wejściowego

 Zadeklaruj`InputPath` zmienną i zainicjuj ją pełną ścieżką istniejącego pliku Excel, który chcesz zmodyfikować. Na przykład :

```csharp
string InputPath = dataDir + "book1.xls";
```

 Upewnij się, że masz plik Excel`book1.xls` w katalogu dokumentów lub podaj poprawną nazwę pliku i lokalizację.

## Krok 4: Otwórz plik Excel

 Użyj`Workbook` klasa Aspose.Cells, aby otworzyć określony plik Excel:

```csharp
Workbook wb = new Workbook(InputPath);
```

## Krok 5: Pobierz kolekcję arkuszy kalkulacyjnych

 Stwórz`WorksheetCollection` obiekt odnoszący się do arkuszy w skoroszycie:

```csharp
WorksheetCollection sheets = wb.Worksheets;
```

## Krok 6: Zdobądź pierwszy arkusz

Pobierz pierwszy arkusz w skoroszycie:

```csharp
Worksheet worksheet = sheets[0];
```

## Krok 7: Przenieś arkusz

 Użyj`MoveTo` metoda przeniesienia pierwszego arkusza na trzecią pozycję w skoroszycie:

```csharp
worksheet.MoveTo(2);
```

## Krok 8: Zapisz zmodyfikowany plik Excel

Zapisz plik Excel z przeniesionym arkuszem:

```csharp
wb.Save(dataDir + "MoveWorksheet_out.xls");
```

Pamiętaj, aby określić żądaną ścieżkę i nazwę pliku wyjściowego.

### Przykładowy kod źródłowy programu Excel Move Worksheet przy użyciu Aspose.Cells dla .NET 
```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Otwórz istniejący plik Excela.
Workbook wb = new Workbook(InputPath);
// Utwórz obiekt Arkusze w odniesieniu do
// arkusze Zeszytu ćwiczeń.
WorksheetCollection sheets = wb.Worksheets;
// Zdobądź pierwszy arkusz.
Worksheet worksheet = sheets[0];
// Przenieś pierwszy arkusz na trzecią pozycję w skoroszycie.
worksheet.MoveTo(2);
// Zapisz plik Excela.
wb.Save(dataDir + "MoveWorksheet_out.xls");
```

## Wniosek

Gratulacje! Nauczyłeś się teraz, jak przenieść arkusz do skoroszytu programu Excel za pomocą Aspose.Cells dla .NET. Możesz użyć tej metody we własnych projektach, aby efektywnie manipulować plikami Excel.

### Często zadawane pytania

#### P. Czy mogę przenieść arkusz w inne miejsce w tym samym skoroszycie programu Excel?

A.  Tak, możesz przenieść arkusz w inne miejsce w tym samym skoroszycie programu Excel, używając`MoveTo` metoda obiektu Worksheet. Wystarczy podać indeks pozycji docelowej w skoroszycie.

#### P. Czy mogę przenieść arkusz do innego skoroszytu programu Excel?

A.  Tak, możesz przenieść arkusz do innego skoroszytu programu Excel za pomocą`MoveTo` metoda obiektu Worksheet. Wystarczy określić indeks pozycji docelowej w docelowym skoroszycie.

#### P. Czy dostarczony kod źródłowy współpracuje z innymi formatami plików Excel, takimi jak XLSX?

A. Tak, dostarczony kod źródłowy współpracuje z innymi formatami plików Excel, w tym XLSX. Aspose.Cells dla .NET obsługuje różne formaty plików Excel, umożliwiając manipulowanie i przenoszenie arkusza do różnych typów plików.

#### P. Jak mogę określić ścieżkę i nazwę pliku wyjściowego podczas zapisywania zmodyfikowanego pliku Excel?

A.  Podczas zapisywania zmodyfikowanego pliku Excel użyj opcji`Save` metoda obiektu Workbook określająca pełną ścieżkę i nazwę pliku wyjściowego. Pamiętaj o podaniu odpowiedniego rozszerzenia pliku, np.`.xls` Lub`.xlsx`, w zależności od żądanego formatu pliku.