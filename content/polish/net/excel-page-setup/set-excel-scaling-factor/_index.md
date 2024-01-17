---
title: Ustaw współczynnik skalowania programu Excel
linktitle: Ustaw współczynnik skalowania programu Excel
second_title: Aspose.Cells dla .NET API odniesienia
description: Naucz się łatwo manipulować plikami Excel i dostosowywać współczynnik skalowania za pomocą Aspose.Cells dla .NET.
type: docs
weight: 180
url: /pl/net/excel-page-setup/set-excel-scaling-factor/
---
tym przewodniku przeprowadzimy Cię przez proces ustawiania współczynnika skalowania w arkuszu kalkulacyjnym Excel przy użyciu Aspose.Cells dla .NET. Aby wykonać to zadanie, wykonaj poniższe czynności.

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

## Krok 6: Ustaw współczynnik skalowania

Ustaw współczynnik skalowania, korzystając z następującego kodu:

```csharp
worksheet.PageSetup.Zoom = 100;
```

Tutaj ustawiliśmy współczynnik skalowania na 100, co oznacza, że po wydrukowaniu arkusz kalkulacyjny będzie wyświetlany w 100% normalnego rozmiaru.

## Krok 7: Zapisywanie skoroszytu programu Excel

 Aby zapisać skoroszyt programu Excel ze zdefiniowanym współczynnikiem skalowania, użyj opcji`Save` metoda obiektu Workbook:

```csharp
workbook.Save(dataDir + "ScalingFactor_out.xls");
```

Spowoduje to zapisanie skoroszytu programu Excel o nazwie pliku „ScalingFactor_out.xls” w określonym katalogu.

### Przykładowy kod źródłowy dla Ustaw współczynnik skalowania programu Excel przy użyciu Aspose.Cells dla .NET 
```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Tworzenie instancji obiektu skoroszytu
Workbook workbook = new Workbook();
// Dostęp do pierwszego arkusza w pliku Excel
Worksheet worksheet = workbook.Worksheets[0];
// Ustawienie współczynnika skalowania na 100
worksheet.PageSetup.Zoom = 100;
// Zapisz skoroszyt.
workbook.Save(dataDir + "ScalingFactor_out.xls");
```

## Wniosek

Gratulacje! Nauczyłeś się, jak ustawić współczynnik skalowania w arkuszu kalkulacyjnym Excel przy użyciu Aspose.Cells dla .NET. Współczynnik skalowania umożliwia dostosowanie rozmiaru arkusza kalkulacyjnego podczas drukowania w celu uzyskania optymalnego wyświetlania.

### Często zadawane pytania

#### 1. Jak ustawić współczynnik skalowania w arkuszu Excel za pomocą Aspose.Cells dla .NET?

 Użyj`Zoom` własność`PageSetup`obiekt, aby ustawić współczynnik skalowania. Na przykład,`worksheet.PageSetup.Zoom = 100;` ustawi współczynnik skalowania na 100%.

#### 2. Czy mogę dostosować współczynnik skalowania do swoich potrzeb?

 Tak, możesz dostosować współczynnik skalowania, zmieniając wartość przypisaną do`Zoom` nieruchomość. Na przykład,`worksheet.PageSetup.Zoom = 75;` ustawi współczynnik skalowania na 75%.

#### 3. Czy można zapisać skoroszyt Excela ze zdefiniowanym współczynnikiem skalowania?

 Tak, możesz skorzystać z`Save` metoda`Workbook` obiekt, aby zapisać skoroszyt programu Excel ze zdefiniowanym współczynnikiem skalowania.