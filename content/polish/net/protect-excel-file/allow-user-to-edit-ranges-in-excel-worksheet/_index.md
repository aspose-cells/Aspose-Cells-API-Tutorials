---
title: Zezwalaj użytkownikowi na edycję zakresów w arkuszu programu Excel
linktitle: Zezwalaj użytkownikowi na edycję zakresów w arkuszu programu Excel
second_title: Aspose.Cells dla .NET API odniesienia
description: Zezwalaj użytkownikom na edycję określonych zakresów w arkuszu kalkulacyjnym Excel przy użyciu Aspose.Cells dla .NET. Przewodnik krok po kroku z kodem źródłowym w języku C#.
type: docs
weight: 10
url: /pl/net/protect-excel-file/allow-user-to-edit-ranges-in-excel-worksheet/
---
W tym przewodniku przeprowadzimy Cię przez proces korzystania z Aspose.Cells dla .NET, aby umożliwić użytkownikowi edycję określonych zakresów w arkuszu kalkulacyjnym Excel. Aby wykonać to zadanie, wykonaj poniższe czynności.

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

Utwórz instancję nowego obiektu skoroszytu reprezentującego skoroszyt programu Excel, który chcesz utworzyć:

```csharp
Workbook book = new Workbook();
```

## Krok 5: Dostęp do pierwszego arkusza

Przejdź do pierwszego arkusza w skoroszycie programu Excel, używając następującego kodu:

```csharp
Worksheet sheet = book.Worksheets[0];
```

## Krok 6: Pobieranie autoryzowanych zakresów modyfikacji

 Pobierz kolekcję dozwolonych zakresów edycji za pomocą`AllowEditRanges` nieruchomość:

```csharp
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
```

## Krok 7: Zdefiniuj chroniony zakres

 Zdefiniuj chroniony zakres za pomocą`Add` metoda`AllowEditRanges` kolekcja:

```csharp
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
protectedRange protectedRange = allowRanges[idx];
```

Tutaj utworzyliśmy chroniony zakres „r2”, który rozciąga się od komórki A1 do komórki C3.

## Krok 8: Określenie hasła

 Określ hasło dla chronionego zakresu za pomocą`Password` nieruchomość:

```csharp
protectedRange.Password = "YOUR_PASSWORD";
```

 Pamiętaj o wymianie`"YOUR_PASSWORD"` z żądanym hasłem.

## Krok 9: Ochrona arkusza

 Chroń arkusz za pomocą`Protect` metoda`Worksheet` obiekt:

```csharp
sheet.Protect(ProtectionType.All);
```

To ochroni arkusz kalkulacyjny, zapobiegając wszelkim modyfikacjom poza dozwolonym zakresem.

## Krok 10: Rejestracja

  plik Excel

 Zapisz wygenerowany plik Excel za pomocą`Save` metoda`Workbook` obiekt:

```csharp
book.Save(dataDir + "protectedrange.out.xls");
```

Pamiętaj, aby podać żądaną nazwę pliku i poprawną ścieżkę.

### Przykładowy kod źródłowy narzędzia Zezwalaj użytkownikowi na edycję zakresów w arkuszu programu Excel przy użyciu Aspose.Cells dla platformy .NET 
```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Utwórz katalog, jeśli jeszcze nie istnieje.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Utwórz wystąpienie nowego skoroszytu
Workbook book = new Workbook();
// Pobierz pierwszy (domyślny) arkusz
Worksheet sheet = book.Worksheets[0];
// Uzyskaj Zezwalaj na zakresy edycji
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
// Zdefiniuj chroniony zakres
ProtectedRange proteced_range;
// Utwórz zakres
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
proteced_range = allowRanges[idx];
// Określ hasło
proteced_range.Password = "123";
// Chroń prześcieradło
sheet.Protect(ProtectionType.All);
// Zapisz plik Excela
book.Save(dataDir + "protectedrange.out.xls");
```

## Wniosek

Nauczyłeś się teraz, jak używać Aspose.Cells dla .NET, aby umożliwić użytkownikowi edycję określonych zakresów w arkuszu kalkulacyjnym Excel. Zachęcamy do dalszego odkrywania funkcji oferowanych przez Aspose.Cells, aby spełnić Twoje specyficzne potrzeby.


### Często zadawane pytania

#### 1. Jak zezwolić użytkownikowi na edycję określonych zakresów w arkuszu kalkulacyjnym Excel?

 Możesz skorzystać z`ProtectedRangeCollection` class do zdefiniowania dozwolonych zakresów modyfikacji. Użyj`Add` metoda tworzenia nowego chronionego zakresu z żądanymi komórkami.

#### 2. Czy mogę ustawić hasło dla autoryzowanych zakresów modyfikacji?

 Tak, możesz określić hasło za pomocą`Password` własność`ProtectedRange` obiekt. Spowoduje to ograniczenie dostępu tylko do użytkowników posiadających hasło.

#### 3. Jak chronić arkusz kalkulacyjny po ustawieniu dozwolonych zakresów?

 Użyj`Protect` metoda`Worksheet` obiekt chroniący arkusz. Zapobiegnie to wszelkim zmianom poza dozwolonym zakresem, prawdopodobnie monitując o podanie hasła, jeśli je określiłeś.