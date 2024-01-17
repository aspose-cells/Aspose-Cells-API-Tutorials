---
title: Ustaw opcje drukowania programu Excel
linktitle: Ustaw opcje drukowania programu Excel
second_title: Aspose.Cells dla .NET API odniesienia
description: Naucz się manipulować plikami Excel i z łatwością dostosowywać opcje drukowania, korzystając z Aspose.Cells dla .NET.
type: docs
weight: 150
url: /pl/net/excel-page-setup/set-excel-print-options/
---
W tym przewodniku przeprowadzimy Cię przez proces ustawiania opcji drukowania skoroszytu programu Excel za pomocą Aspose.Cells dla .NET. Przeprowadzimy Cię krok po kroku przez dostarczony kod źródłowy C#, aby wykonać to zadanie.

## Krok 1: Konfigurowanie środowiska

Zanim zaczniesz, upewnij się, że skonfigurowałeś środowisko programistyczne i zainstalowałeś Aspose.Cells dla .NET. Możesz pobrać najnowszą wersję biblioteki z oficjalnej strony Aspose.

## Krok 2: Zaimportuj wymagane przestrzenie nazw

W swoim projekcie C# zaimportuj niezbędne przestrzenie nazw do pracy z Aspose.Cells:

```csharp
using Aspose.Cells;
```

## Krok 3: Ustawienie ścieżki do katalogu dokumentów

 Zadeklaruj`dataDir` zmienna określająca ścieżkę do katalogu, w którym chcesz zapisać wygenerowany plik Excel:

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Pamiętaj o wymianie`"YOUR_DOCUMENT_DIRECTORY"` z poprawną ścieżką w systemie.

## Krok 4: Tworzenie obiektu skoroszytu

Utwórz instancję obiektu Workbook reprezentującego skoroszyt programu Excel, który chcesz utworzyć:

```csharp
Workbook workbook = new Workbook();
```

## Krok 5: Uzyskanie odniesienia do PageSetup arkusza

Aby ustawić opcje drukowania, musimy najpierw uzyskać odwołanie do PageSetup z arkusza. Użyj poniższego kodu, aby uzyskać referencję:

```csharp
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## Krok 6: Włącz drukowanie linii siatki

Aby włączyć drukowanie linii siatki, użyj następującego kodu:

```csharp
pageSetup. PrintGridlines = true;
```

## Krok 7: Włącz drukowanie nagłówków wierszy/kolumn

Aby włączyć drukowanie nagłówków wierszy i kolumn, użyj następującego kodu:

```csharp
pageSetup.PrintHeadings = true;
```

## Krok 8: Włączanie trybu drukowania czarno-białego

Aby włączyć drukowanie arkusza w trybie czarno-białym, użyj następującego kodu:

```csharp
pageSetup.BlackAndWhite = true;
```

## Krok 9: Włączanie drukowania opinii

Aby umożliwić drukowanie komentarzy w formie, w jakiej pojawiają się w arkuszu kalkulacyjnym, użyj następującego kodu:

```csharp
pageSetup.PrintComments = PrintCommentsType.PrintInPlace;
```

## Krok 10: Włącz drukowanie w trybie roboczym

Aby włączyć drukowanie arkusza kalkulacyjnego w trybie roboczym, użyj następującego kodu:

```csharp
pageSetup.PrintDraft = true;
```

## Krok 11: Włącz drukowanie błędów komórek jako N/A

Aby umożliwić drukowanie błędów komórek jako

  niż nie dotyczy, użyj następującego kodu:

```csharp
pageSetup.PrintErrors = PrintErrorsType.PrintErrorsNA;
```

## Krok 12: Zapisywanie skoroszytu programu Excel

 Aby zapisać skoroszyt programu Excel z ustawionymi opcjami drukowania, użyj opcji`Save` metoda obiektu Workbook:

```csharp
workbook.Save(dataDir + "OtherPrintOptions_out.xls");
```

Spowoduje to zapisanie skoroszytu programu Excel z nazwą pliku „OtherPrintOptions_out.xls” w określonym katalogu.

### Przykładowy kod źródłowy dla Ustaw opcje drukowania programu Excel przy użyciu Aspose.Cells dla .NET 
```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Tworzenie instancji obiektu skoroszytu
Workbook workbook = new Workbook();
// Uzyskanie odniesienia do PageSetup arkusza
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Zezwalanie na drukowanie linii siatki
pageSetup.PrintGridlines = true;
// Zezwalanie na drukowanie nagłówków wierszy/kolumn
pageSetup.PrintHeadings = true;
// Umożliwia wydruk arkusza w trybie czarno-białym
pageSetup.BlackAndWhite = true;
// Zezwalanie na drukowanie komentarzy wyświetlanych w arkuszu
pageSetup.PrintComments = PrintCommentsType.PrintInPlace;
// Umożliwia drukowanie arkusza z jakością roboczą
pageSetup.PrintDraft = true;
// Zezwalanie na drukowanie błędów komórek jako N/A
pageSetup.PrintErrors = PrintErrorsType.PrintErrorsNA;
// Zapisz skoroszyt.
workbook.Save(dataDir + "OtherPrintOptions_out.xls");
```
## Wniosek

Nauczyłeś się teraz, jak ustawić opcje drukowania skoroszytu programu Excel przy użyciu Aspose.Cells dla .NET. Ta wydajna i przyjazna dla użytkownika biblioteka umożliwia łatwe i wydajne dostosowywanie ustawień drukowania skoroszytów programu Excel.

### Często zadawane pytania


#### 1. Czy mogę dodatkowo dostosować opcje drukowania, takie jak marginesy lub orientacja strony?

Tak, Aspose.Cells dla .NET oferuje szeroką gamę dostosowywalnych opcji drukowania, takich jak marginesy, orientacja strony, skala itp.

#### 2. Czy Aspose.Cells dla .NET obsługuje inne formaty plików Excel?

Tak, Aspose.Cells dla .NET obsługuje różne formaty plików Excel, takie jak XLSX, XLS, CSV, HTML, PDF itp.

#### 3. Czy Aspose.Cells for .NET jest kompatybilny ze wszystkimi wersjami .NET Framework?

Aspose.Cells dla .NET jest kompatybilny z .NET Framework 2.0 lub nowszym, w tym wersjami 3.5, 4.0, 4.5, 4.6 itd.