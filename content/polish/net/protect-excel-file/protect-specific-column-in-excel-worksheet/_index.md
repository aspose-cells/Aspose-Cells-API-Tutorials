---
title: Chroń określoną kolumnę w arkuszu programu Excel
linktitle: Chroń określoną kolumnę w arkuszu programu Excel
second_title: Aspose.Cells dla .NET API odniesienia
description: Dowiedz się, jak chronić określoną kolumnę w arkuszu Excel za pomocą Aspose.Cells dla .NET. Przewodnik krok po kroku w języku C#.
type: docs
weight: 80
url: /pl/net/protect-excel-file/protect-specific-column-in-excel-worksheet/
---
Podczas pracy z arkuszami programu Excel w języku C# często konieczne jest zabezpieczenie określonych kolumn, aby zapobiec przypadkowym modyfikacjom. W tym samouczku przeprowadzimy Cię przez proces ochrony określonej kolumny w arkuszu programu Excel przy użyciu biblioteki Aspose.Cells dla .NET. Wyjaśnimy krok po kroku kod źródłowy C# wymagany do tego zadania. Więc zacznijmy!

## Omówienie ochrony określonych kolumn w arkuszu programu Excel

Ochrona określonych kolumn w arkuszu programu Excel gwarantuje, że kolumny te pozostaną zablokowane i nie będzie można ich modyfikować bez odpowiedniej autoryzacji. Jest to szczególnie przydatne, gdy chcesz ograniczyć dostęp do edycji niektórych danych lub formuł, jednocześnie umożliwiając użytkownikom interakcję z pozostałą częścią arkusza. Biblioteka Aspose.Cells dla .NET zapewnia kompleksowy zestaw funkcji do programowego manipulowania plikami Excel, w tym ochronę kolumn.

## Konfigurowanie środowiska

Zanim zaczniemy, upewnij się, że masz zainstalowaną bibliotekę Aspose.Cells for .NET w swoim środowisku programistycznym. Możesz pobrać bibliotekę z oficjalnej strony Aspose i zainstalować ją za pomocą dostarczonego instalatora.

## Tworzenie nowego skoroszytu i arkusza

Aby rozpocząć ochronę określonych kolumn, musimy utworzyć nowy skoroszyt i arkusz za pomocą Aspose.Cells dla .NET. Oto fragment kodu:

```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENT DIRECTORY";

// Utwórz katalog, jeśli jeszcze nie istnieje.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);

// Utwórz nowy skoroszyt.
Workbook wb = new Workbook();

// Utwórz obiekt arkusza i uzyskaj pierwszy arkusz.
Worksheet sheet = wb.Worksheets[0];
```

Pamiętaj, aby zastąpić „KATALOG TWOJEGO DOKUMENTU” rzeczywistą ścieżką katalogu, w którym chcesz zapisać plik Excel.

## Definiowanie stylu i obiektów flagi stylu

Aby ustawić określone style i flagi zabezpieczające dla kolumn, musimy zdefiniować styl i obiekty flagi stylu. Oto fragment kodu:

```csharp
// Zdefiniuj obiekt stylu.
Style style;

// Zdefiniuj obiekt flagi stylu.
StyleFlag flag;
```

## Przechodzenie przez kolumny i odblokowywanie ich

Następnie musimy przejść przez wszystkie kolumny w arkuszu i je odblokować. Dzięki temu wszystkie kolumny będą edytowalne z wyjątkiem tej, którą chcemy chronić. Oto fragment kodu:

```csharp
// Przejdź przez wszystkie kolumny w arkuszu i odblokuj je.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    flag = new StyleFlag();
    flag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
```

## Blokowanie określonej kolumny

Teraz zablokujmy konkretną kolumnę. W tym przykładzie zablokujemy pierwszą kolumnę (indeks kolumny 0). Oto fragment kodu:

```csharp
// Uzyskaj styl pierwszej kolumny.
style = sheet.Cells.Columns[0].Style;

// Zablokuj to.
style.IsLocked = true;
```

## Stosowanie stylów do kolumn

Po zablokowaniu konkretnej kolumny musimy zastosować do niej styl i flagę. Oto fragment kodu:

```csharp
//Utwórz instancję flagi.
flag = new StyleFlag();

// Ustaw ustawienie blokady.
flag.Locked = true;

// Zastosuj styl do pierwszej kolumny.
sheet.Cells.Columns[0].ApplyStyle(style, flag);
```

## Ochrona arkusza

Aby zakończyć ochronę, musimy zabezpieczyć arkusz, aby mieć pewność, że zablokowanych kolumn nie będzie można modyfikować. Oto fragment kodu:

```csharp
// Chroń prześcieradło.
sheet.Protect(ProtectionType.All);
```

## Zapisywanie pliku Excel

Na koniec zapiszemy zmodyfikowany plik Excel w wybranej lokalizacji. Oto fragment kodu:

```csharp
// Zapisz plik Excela.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Pamiętaj, aby zastąpić „output.out.xls” żądaną nazwą pliku i rozszerzeniem.

### Przykładowy kod źródłowy dla funkcji Chroń określoną kolumnę w arkuszu programu Excel przy użyciu Aspose.Cells dla platformy .NET 
```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Utwórz katalog, jeśli jeszcze nie istnieje.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Utwórz nowy skoroszyt.
Workbook wb = new Workbook();
// Utwórz obiekt arkusza i uzyskaj pierwszy arkusz.
Worksheet sheet = wb.Worksheets[0];
// Zdefiniuj obiekt stylu.
Style style;
// Zdefiniuj obiekt styleflag.
StyleFlag flag;
// Przejdź przez wszystkie kolumny w arkuszu i odblokuj je.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    flag = new StyleFlag();
    flag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
// Uzyskaj styl pierwszej kolumny.
style = sheet.Cells.Columns[0].Style;
// Zablokuj to.
style.IsLocked = true;
//Utwórz instancję flagi.
flag = new StyleFlag();
// Ustaw ustawienie blokady.
flag.Locked = true;
// Zastosuj styl do pierwszej kolumny.
sheet.Cells.Columns[0].ApplyStyle(style, flag);
// Chroń prześcieradło.
sheet.Protect(ProtectionType.All);
// Zapisz plik Excela.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## Wniosek

W tym samouczku wyjaśniliśmy krok po kroku proces ochrony określonej kolumny w arkuszu programu Excel przy użyciu biblioteki Aspose.Cells for .NET. Zaczęliśmy od utworzenia nowego skoroszytu i arkusza, zdefiniowania stylu i obiektów flagi stylu, a następnie przystąpiliśmy do odblokowywania i blokowania określonych kolumn. Na koniec zabezpieczyliśmy arkusz i zapisaliśmy zmodyfikowany plik Excel. Postępując zgodnie z tym przewodnikiem, powinieneś być teraz w stanie chronić określone kolumny w arkuszach programu Excel przy użyciu języków C# i Aspose.Cells dla .NET.

### Często zadawane pytania (FAQ)

#### Czy mogę chronić wiele kolumn za pomocą tej metody?

Tak, możesz chronić wiele kolumn, odpowiednio modyfikując kod. Po prostu przejdź przez żądany zakres kolumn i zastosuj style blokowania i flagi.

#### Czy możliwe jest zabezpieczenie chronionego arkusza hasłem?

 Tak, możesz dodać ochronę hasłem do chronionego arkusza, podając hasło podczas wywoływania`Protect` metoda.

#### Czy Aspose.Cells dla .NET obsługuje inne formaty plików Excel?

Tak, Aspose.Cells dla .NET obsługuje różne formaty plików Excel, w tym XLS, XLSX, XLSM i inne.

#### Czy mogę chronić określone wiersze zamiast kolumn?

Tak, możesz zmodyfikować kod, aby chronić określone wiersze zamiast kolumn, stosując style i flagi do komórek wierszy zamiast komórek kolumn.