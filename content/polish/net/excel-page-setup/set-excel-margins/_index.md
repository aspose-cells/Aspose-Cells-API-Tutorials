---
title: Ustaw marginesy programu Excel
linktitle: Ustaw marginesy programu Excel
second_title: Aspose.Cells dla .NET API odniesienia
description: Dowiedz się, jak ustawić marginesy w programie Excel przy użyciu Aspose.Cells dla .NET. Samouczek krok po kroku w języku C#.
type: docs
weight: 110
url: /pl/net/excel-page-setup/set-excel-margins/
---
W tym samouczku przeprowadzimy Cię krok po kroku, jak ustawić marginesy w programie Excel za pomocą Aspose.Cells dla .NET. Do zilustrowania procesu użyjemy kodu źródłowego C#.

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
WorksheetCollection worksheets = workbook. Worksheets;
Worksheet worksheet = worksheets[0];
```

Spowoduje to utworzenie pustego skoroszytu z arkuszem i umożliwi dostęp do tego arkusza.

## Krok 5: Ustawianie marginesów

Uzyskaj dostęp do obiektu PageSetup arkusza i ustaw marginesy przy użyciu właściwości BottomMargin, LeftMargin, RightMargin i TopMargin. Oto przykładowy kod:

```csharp
PageSetup pageSetup = worksheet.PageSetup;
pageSetup.BottomMargin = 2;
pageSetup.LeftMargin = 1;
pageSetup.RightMargin = 1;
pageSetup.TopMargin = 3;
```

Spowoduje to ustawienie odpowiednio dolnego, lewego, prawego i górnego marginesu arkusza.

## Krok 6: Zapisywanie zmodyfikowanego skoroszytu

Zapisz zmodyfikowany skoroszyt, używając następującego kodu:

```csharp
workbook.Save(dataDir + "OutputFileName.xls");
```

Spowoduje to zapisanie zmodyfikowanego skoroszytu w określonym katalogu danych.

### Przykładowy kod źródłowy dla Ustaw marginesy programu Excel przy użyciu Aspose.Cells dla .NET 
```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Utwórz obiekt skoroszytu
Workbook workbook = new Workbook();
// Pobierz arkusze ćwiczeń z zeszytu ćwiczeń
WorksheetCollection worksheets = workbook.Worksheets;
// Pobierz pierwszy (domyślny) arkusz
Worksheet worksheet = worksheets[0];
// Pobierz obiekt pagesetup
PageSetup pageSetup = worksheet.PageSetup;
// Ustaw dolny, lewy, prawy i górny margines strony
pageSetup.BottomMargin = 2;
pageSetup.LeftMargin = 1;
pageSetup.RightMargin = 1;
pageSetup.TopMargin = 3;
// Zapisz skoroszyt.
workbook.Save(dataDir + "SetMargins_out.xls");
```

## Wniosek

Nauczyłeś się teraz, jak ustawiać marginesy w programie Excel przy użyciu Aspose.Cells dla .NET. Ten samouczek przeprowadził Cię przez każdy etap procesu, od skonfigurowania środowiska po zapisanie zmodyfikowanego skoroszytu. Zachęcamy do dalszego odkrywania funkcji Aspose.Cells w celu wykonywania dalszych manipulacji w plikach Excel.

### FAQ (często zadawane pytania)

#### 1. Jak mogę określić niestandardowe marginesy dla mojego arkusza kalkulacyjnego?

 Możesz określić niestandardowe marginesy za pomocą`BottomMargin`, `LeftMargin`, `RightMargin` , I`TopMargin` właściwości`PageSetup` obiekt. Wystarczy ustawić żądane wartości dla każdej właściwości, aby w razie potrzeby dostosować marginesy.

#### 2. Czy mogę ustawić różne marginesy dla różnych arkuszy w tym samym skoroszycie?

 Tak, możesz ustawić różne marginesy dla każdego arkusza w tym samym skoroszycie. Wystarczy uzyskać dostęp do`PageSetup` obiekt każdego arkusza indywidualnie i ustaw określone marginesy dla każdego z nich.

#### 3. Czy zdefiniowane marginesy dotyczą także druku skoroszytu?

Tak, marginesy ustawione za pomocą Aspose.Cells mają zastosowanie również podczas drukowania skoroszytu. Określone marginesy zostaną uwzględnione podczas generowania wydruku skoroszytu.

#### 4. Czy mogę zmienić marginesy istniejącego pliku Excel za pomocą Aspose.Cells?

 Tak, możesz zmienić marginesy istniejącego pliku Excel, ładując plik za pomocą Aspose.Cells, uzyskując dostęp do każdego arkusza`PageSetup` obiektu i zmieniając wartości właściwości marginesów. Następnie zapisz zmodyfikowany plik, aby zastosować nowe marginesy.

#### 5. Jak usunąć marginesy z arkusza kalkulacyjnego?

 Aby usunąć marginesy z arkusza, możesz po prostu ustawić wartości parametru`BottomMargin`, `LeftMargin`, `RightMargin` I`TopMargin` właściwości do zera. Spowoduje to przywrócenie domyślnych marginesów (zwykle zero).