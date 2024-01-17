---
title: Ustaw tytuł wydruku programu Excel
linktitle: Ustaw tytuł wydruku programu Excel
second_title: Aspose.Cells dla .NET API odniesienia
description: Naucz się łatwo manipulować plikami Excel i dostosowywać opcje drukowania za pomocą Aspose.Cells dla .NET.
type: docs
weight: 170
url: /pl/net/excel-page-setup/set-excel-print-title/
---
W tym przewodniku przeprowadzimy Cię przez proces ustawiania tytułów wydruku w arkuszu kalkulacyjnym Excel przy użyciu Aspose.Cells dla .NET. Aby wykonać to zadanie, wykonaj poniższe czynności.

## Krok 1: Konfigurowanie środowiska

Upewnij się, że skonfigurowałeś środowisko programistyczne i zainstalowałeś Aspose.Cells dla .NET. Możesz pobrać najnowszą wersję biblioteki z oficjalnej strony Aspose.

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

## Krok 5: Dostęp do pierwszego arkusza

Przejdź do pierwszego arkusza w skoroszycie programu Excel, używając następującego kodu:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Krok 6: Definiowanie kolumn tytułowych

Zdefiniuj kolumny tytułowe, używając następującego kodu:

```csharp
pageSetup.PrintTitleColumns = "$A:$B";
```

Tutaj zdefiniowaliśmy kolumny A i B jako kolumny tytułowe. Możesz dostosować tę wartość do swoich potrzeb.

## Krok 7: Definiowanie linii tytułu

Zdefiniuj linie tytułowe za pomocą następującego kodu:

```csharp
pageSetup.PrintTitleRows = "$1:$2";
```

Zdefiniowaliśmy wiersze 1 i 2 jako wiersze tytułowe. Możesz dostosować te wartości do swoich potrzeb.

## Krok 8: Zapisywanie skoroszytu programu Excel

 Aby zapisać skoroszyt programu Excel ze zdefiniowanymi tytułami wydruku, użyj opcji`Save` metoda obiektu Workbook:

```csharp
workbook.Save(dataDir + "SetPrintTitle_out.xls");
```

Spowoduje to zapisanie skoroszytu programu Excel z nazwą pliku „SetPrintTitle_out.xls” w określonym katalogu.

### Przykładowy kod źródłowy dla Ustaw tytuł wydruku programu Excel przy użyciu Aspose.Cells dla .NET 
```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Tworzenie instancji obiektu skoroszytu
Workbook workbook = new Workbook();
// Uzyskanie odniesienia do PageSetup arkusza
Aspose.Cells.PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Definiowanie numerów kolumn A i B jako kolumn tytułowych
pageSetup.PrintTitleColumns = "$A:$B";
// Definiowanie numerów wierszy 1 i 2 jako wierszy tytułowych
pageSetup.PrintTitleRows = "$1:$2";
// Zapisz skoroszyt.
workbook.Save(dataDir + "SetPrintTitle_out.xls");
```

## Wniosek

Gratulacje! Nauczyłeś się, jak ustawić tytuły wydruku w arkuszu kalkulacyjnym Excel przy użyciu Aspose.Cells dla .NET. Tytuły wydruków umożliwiają wyświetlenie określonych wierszy i kolumn na każdej drukowanej stronie, dzięki czemu dane są łatwiejsze do odczytania i łatwiejsze do odniesienia.

### Często zadawane pytania

#### 1. Czy mogę ustawić tytuły wydruku dla poszczególnych kolumn w programie Excel?

 Tak, z Aspose.Cells dla .NET możesz ustawić określone kolumny jako tytuły do druku za pomocą`PrintTitleColumns` własność`PageSetup` obiekt.

#### 2. Czy można zdefiniować tytuły kolumn i wierszy wydruku?

 Tak, możesz ustawić drukowanie tytułów kolumn i wierszy za pomocą`PrintTitleColumns` I`PrintTitleRows` właściwości`PageSetup` obiekt.

#### 3. Jakie inne ustawienia układu mogę dostosować za pomocą Aspose.Cells dla .NET?

Dzięki Aspose.Cells dla .NET możesz dostosować różne ustawienia układu strony, takie jak marginesy, orientacja strony, skala druku i inne.