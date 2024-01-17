---
title: Ustaw nagłówki i stopki programu Excel
linktitle: Ustaw nagłówki i stopki programu Excel
second_title: Aspose.Cells dla .NET API odniesienia
description: Dowiedz się, jak ustawić nagłówki i stopki w programie Excel przy użyciu Aspose.Cells dla .NET.
type: docs
weight: 100
url: /pl/net/excel-page-setup/set-excel-headers-and-footers/
---

tym samouczku pokażemy Ci krok po kroku, jak ustawić nagłówki i stopki w programie Excel przy użyciu Aspose.Cells dla .NET. Do zilustrowania procesu użyjemy kodu źródłowego C#.

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
Workbook excel = new Workbook();
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
```

Spowoduje to utworzenie pustego skoroszytu z arkuszem i umożliwi dostęp do obiektu PageSetup tego arkusza.

## Krok 5: Ustawianie nagłówków

 Ustaw nagłówki arkusza kalkulacyjnego za pomocą`SetHeader` metody obiektu PageSetup. Oto przykładowy kod:

```csharp
pageSetup.SetHeader(0, "&A");
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
```

Spowoduje to ustawienie odpowiednio nazwy arkusza, bieżącej daty i godziny oraz nazwy pliku w nagłówkach.

## Krok 6: Definiowanie stopek

 Ustaw stopki arkusza kalkulacyjnego za pomocą`SetFooter` metody obiektu PageSetup. Oto przykładowy kod:

```csharp
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
pageSetup.SetFooter(1, "&P");
pageSetup.SetFooter(2, "&N");
```

Spowoduje to odpowiednio ustawienie ciągu tekstowego, numeru bieżącej strony i całkowitej liczby stron w stopce.

## Krok 7: Zapisywanie zmodyfikowanego skoroszytu

Zapisz zmodyfikowany skoroszyt, używając następującego kodu:

```csharp
excel.Save(dataDir + "OutputFileName.xls");
```

Spowoduje to zapisanie zmodyfikowanego skoroszytu w określonym katalogu danych.

### Przykładowy kod źródłowy dla ustawiania nagłówków i stopek programu Excel przy użyciu Aspose.Cells dla .NET 
```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Tworzenie instancji obiektu skoroszytu
Workbook excel = new Workbook();
// Uzyskanie odniesienia do PageSetup arkusza
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
// Ustawianie nazwy arkusza w lewej części nagłówka
pageSetup.SetHeader(0, "&A");
//Ustawianie aktualnej daty i aktualnej godziny w środkowej części nagłówka
// i zmianę czcionki nagłówka
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
// Ustawienie bieżącej nazwy pliku w prawej części nagłówka i zmiana pliku
// czcionka nagłówka
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
// Ustawienie ciągu znaków w lewej części stopki i zmiana czcionki
// części tego ciągu („123”)
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
// Ustawienie aktualnego numeru strony w środkowej części stopki
pageSetup.SetFooter(1, "&P");
// Ustawianie liczby stron w prawej części stopki
pageSetup.SetFooter(2, "&N");
// Zapisz skoroszyt.
excel.Save(dataDir + "SetHeadersAndFooters_out.xls");
```


## Wniosek

Nauczyłeś się teraz, jak ustawiać nagłówki i stopki w programie Excel przy użyciu Aspose.Cells dla .NET. Ten samouczek przeprowadził Cię przez każdy etap procesu, od skonfigurowania środowiska po zapisanie zmodyfikowanego skoroszytu. Zachęcamy do dalszego odkrywania funkcji Aspose.Cells w celu wykonywania dalszych manipulacji w plikach Excel.

### Często zadawane pytania (FAQ)

#### 1. Jak mogę zainstalować Aspose.Cells dla .NET w moim systemie?
Aby zainstalować Aspose.Cells dla .NET, należy pobrać pakiet instalacyjny z oficjalnej strony Aspose i postępować zgodnie z instrukcjami zawartymi w dokumentacji.

#### 2. Czy ta metoda działa ze wszystkimi wersjami Excela?
Tak, metoda ustawiania nagłówków i stopek za pomocą Aspose.Cells dla .NET działa ze wszystkimi obsługiwanymi wersjami programu Excel.

#### 3. Czy mogę dodatkowo dostosować nagłówki i stopki?
Tak, Aspose.Cells oferuje szeroką gamę funkcji umożliwiających dostosowywanie nagłówków i stopek, w tym rozmieszczenie tekstu, kolor, czcionkę, numery stron i inne.

#### 4. Jak mogę dodać dynamiczne informacje do nagłówków i stopek?
Możesz użyć specjalnych zmiennych i kodów formatujących, aby dodać dynamiczne informacje, takie jak bieżąca data, godzina, nazwa pliku, numer strony itp., do nagłówków i stopek.

#### 5. Czy mogę usunąć nagłówki i stopki po ich ustawieniu?
 Tak, możesz usunąć nagłówki i stopki za pomocą`ClearHeaderFooter` metoda`PageSetup` obiekt. Spowoduje to przywrócenie domyślnych nagłówków i stopek.