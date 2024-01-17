---
title: Ustaw obszar wydruku programu Excel
linktitle: Ustaw obszar wydruku programu Excel
second_title: Aspose.Cells dla .NET API odniesienia
description: Przewodnik krok po kroku, jak ustawić obszar wydruku Excel przy użyciu Aspose.Cells dla .NET. Z łatwością optymalizuj i dostosowuj skoroszyty programu Excel.
type: docs
weight: 140
url: /pl/net/excel-page-setup/set-excel-print-area/
---
Korzystanie z Aspose.Cells dla .NET może znacznie ułatwić zarządzanie i manipulowanie plikami Excel w aplikacjach .NET. W tym przewodniku pokażemy, jak ustawić obszar wydruku skoroszytu programu Excel za pomocą Aspose.Cells dla .NET. Poprowadzimy Cię krok po kroku przez dostarczony kod źródłowy C#, aby wykonać to zadanie.

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

Aby ustawić obszar wydruku, musimy najpierw uzyskać odwołanie z PageSetup arkusza. Użyj poniższego kodu, aby uzyskać referencję:

```csharp
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## Krok 6: Określenie zakresu komórek obszaru wydruku

Teraz, gdy mamy odwołanie do PageSetup, możemy określić zakres komórek tworzących obszar wydruku. W tym przykładzie jako obszar wydruku ustawimy zakres komórek od A1 do T35. Użyj następującego kodu:

```csharp
pageSetup.PrintArea = "A1:T35";
```

Możesz dostosować zakres komórek do swoich potrzeb.

## Krok 7: Zapisywanie skoroszytu programu Excel

 Aby zapisać skoroszyt programu Excel ze zdefiniowanym obszarem wydruku, użyj opcji`Save` metoda obiektu Workbook:

```csharp
workbook.Save(dataDir + "SetPrintArea_out.xls");
```

Spowoduje to zapisanie skoroszytu programu Excel z nazwą pliku „SetPrintArea_out.xls” w określonym katalogu.

### Przykładowy kod źródłowy dla Ustaw obszar wydruku programu Excel przy użyciu Aspose.Cells dla .NET 
```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Tworzenie instancji obiektu skoroszytu
Workbook workbook = new Workbook();
// Uzyskanie odniesienia do PageSetup arkusza
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Określenie zakresu komórek (od komórki A1 do komórki T35) obszaru wydruku
pageSetup.PrintArea = "A1:T35";
// Zapisz skoroszyt.
workbook.Save(dataDir + "SetPrintArea_out.xls");
```

## Wniosek

Gratulacje! Nauczyłeś się teraz, jak ustawić obszar wydruku skoroszytu programu Excel przy użyciu Aspose.Cells dla .NET. Ta potężna i przyjazna dla użytkownika biblioteka znacznie ułatwia pracę z plikami Excel w aplikacjach .NET. Jeśli masz dodatkowe pytania lub napotkasz jakiekolwiek trudności, zapoznaj się z oficjalną dokumentacją Aspose.Cells, aby uzyskać więcej informacji i zasobów.

### Często zadawane pytania

#### 1. Czy mogę dodatkowo dostosować układ obszaru wydruku, np. orientację i marginesy?

Tak, możesz uzyskać dostęp do innych właściwości PageSetup, takich jak orientacja strony, marginesy, skala itp., aby jeszcze bardziej dostosować układ obszaru wydruku.

#### 2. Czy Aspose.Cells dla .NET obsługuje inne formaty plików Excel, takie jak XLSX i CSV?

Tak, Aspose.Cells dla .NET obsługuje różne formaty plików Excel, w tym XLSX, XLS, CSV, HTML, PDF i wiele innych.

#### 3. Czy Aspose.Cells for .NET jest kompatybilny ze wszystkimi wersjami .NET Framework?

Aspose.Cells dla .NET jest kompatybilny z .NET Framework 2.0 lub nowszym, w tym wersjami 3.5, 4.0, 4.5, 4.6 itd.