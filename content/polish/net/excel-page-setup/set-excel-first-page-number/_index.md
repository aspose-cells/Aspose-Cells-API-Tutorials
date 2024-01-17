---
title: Ustaw numer pierwszej strony programu Excel
linktitle: Ustaw numer pierwszej strony programu Excel
second_title: Aspose.Cells dla .NET API odniesienia
description: Dowiedz się, jak ustawić numer pierwszej strony w programie Excel przy użyciu Aspose.Cells dla .NET.
type: docs
weight: 90
url: /pl/net/excel-page-setup/set-excel-first-page-number/
---
W tym samouczku przeprowadzimy Cię przez proces ustawiania numeru pierwszej strony w programie Excel przy użyciu Aspose.Cells dla .NET. Do zilustrowania procesu użyjemy kodu źródłowego C#.

## Krok 1: Konfigurowanie środowiska

Upewnij się, że masz zainstalowany Aspose.Cells for .NET na swoim komputerze. Utwórz także nowy projekt w preferowanym środowisku programistycznym.

## Krok 2: Zaimportuj niezbędne biblioteki

W pliku kodu zaimportuj biblioteki potrzebne do pracy z Aspose.Cells. Oto odpowiedni kod:

```csharp
using Aspose.Cells;
```

## Krok 3: Ustaw katalog danych

Ustaw katalog danych, w którym chcesz zapisać zmodyfikowany plik Excel. Użyj następującego kodu:

```csharp
string dataDir = "YOUR DATA DIRECTORY";
```

Pamiętaj, aby podać pełną ścieżkę katalogu.

## Krok 4: Tworzenie skoroszytu i arkusza kalkulacyjnego

Utwórz nowy obiekt Workbook i przejdź do pierwszego arkusza w skoroszycie, używając następującego kodu:

```csharp
Workbook workbook = new Workbook();
Worksheet worksheet = workbook.Worksheets[0];
```

Spowoduje to utworzenie pustego skoroszytu z arkuszem.

## Krok 5: Ustawienie numeru pierwszej strony

Ustaw numer pierwszej strony stron arkusza, używając następującego kodu:

```csharp
worksheet.PageSetup.FirstPageNumber = 2;
```

Spowoduje to ustawienie numeru pierwszej strony na 2.

## Krok 6: Zapisywanie zmodyfikowanego skoroszytu

Zapisz zmodyfikowany skoroszyt, używając następującego kodu:

```csharp
workbook.Save(dataDir + "OutputFileName.xls");
```

Spowoduje to zapisanie zmodyfikowanego skoroszytu w określonym katalogu danych.

### Przykładowy kod źródłowy dla Ustaw numer pierwszej strony programu Excel przy użyciu Aspose.Cells dla .NET 
```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Tworzenie instancji obiektu skoroszytu
Workbook workbook = new Workbook();
// Dostęp do pierwszego arkusza w pliku Excel
Worksheet worksheet = workbook.Worksheets[0];
// Ustawianie numeru pierwszej strony arkusza kalkulacyjnego
worksheet.PageSetup.FirstPageNumber = 2;
// Zapisz skoroszyt.
workbook.Save(dataDir + "SetFirstPageNumber_out.xls");
```

## Wniosek

Nauczyłeś się teraz, jak ustawić numer pierwszej strony w programie Excel przy użyciu Aspose.Cells dla .NET. Ten samouczek przeprowadził Cię przez każdy etap procesu, od skonfigurowania środowiska po ustawienie numeru pierwszej strony. Możesz teraz wykorzystać tę wiedzę do dostosowania numeracji stron w plikach Excel.

### Często zadawane pytania

#### P1: Czy mogę ustawić inny numer pierwszej strony dla każdego arkusza?

 Odpowiedź 1: Tak, możesz ustawić inny numer pierwszej strony dla każdego arkusza, uzyskując dostęp do`FirstPageNumber`właściwość odpowiedniego arkusza`PageSetup` obiekt.

#### P2: Jak mogę sprawdzić numer pierwszej strony istniejącego arkusza kalkulacyjnego?

 A2: Możesz sprawdzić numer pierwszej strony istniejącego arkusza, uzyskując dostęp do`FirstPageNumber` własność`PageSetup` obiekt odpowiadający temu arkuszowi.

#### P3: Czy numeracja stron zawsze domyślnie zaczyna się od 1?

O3: Tak, numeracja stron domyślnie zaczyna się od 1 w Excelu. Możesz jednak użyć kodu pokazanego w tym samouczku, aby ustawić inny numer pierwszej strony.

#### P4: Czy zmiany numeru pierwszej strony są trwałe w edytowanym pliku Excel?

O4: Tak, zmiany wprowadzone w numerze pierwszej strony zostają trwale zapisane w zmodyfikowanym pliku Excel.

#### P5: Czy ta metoda działa w przypadku wszystkich formatów plików Excel, takich jak .xls i .xlsx?

O5: Tak, ta metoda działa dla wszystkich formatów plików Excel obsługiwanych przez Aspose.Cells, w tym .xls i .xlsx.