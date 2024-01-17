---
title: Chroń określony wiersz w arkuszu programu Excel
linktitle: Chroń określony wiersz w arkuszu programu Excel
second_title: Aspose.Cells dla .NET API odniesienia
description: Chroń określony wiersz w programie Excel za pomocą Aspose.Cells dla .NET. Przewodnik krok po kroku dotyczący zabezpieczania poufnych danych.
type: docs
weight: 90
url: /pl/net/protect-excel-file/protect-specific-row-in-excel-worksheet/
---
Ochrona poufnych danych w arkuszu kalkulacyjnym Excel jest niezbędna do zapewnienia bezpieczeństwa informacji. Aspose.Cells dla .NET oferuje potężne rozwiązanie do ochrony określonych wierszy w arkuszu kalkulacyjnym Excel. Ten przewodnik przeprowadzi Cię przez proces ochrony określonego wiersza w arkuszu programu Excel przy użyciu dostarczonego kodu źródłowego C#. Wykonaj te proste kroki, aby skonfigurować ochronę wierszy w plikach Excel.

## Krok 1: Zaimportuj wymagane biblioteki

Aby rozpocząć, upewnij się, że masz zainstalowany Aspose.Cells for .NET w swoim systemie. Musisz także dodać odpowiednie odniesienia w swoim projekcie C#, aby móc korzystać z funkcjonalności Aspose.Cells. Oto kod umożliwiający zaimportowanie wymaganych bibliotek:

```csharp
// Dodaj niezbędne odniesienia
using Aspose.Cells;
```

## Krok 2: Tworzenie skoroszytu i arkusza kalkulacyjnego programu Excel

Po zaimportowaniu wymaganych bibliotek możesz utworzyć nowy skoroszyt programu Excel i nowy arkusz. Oto jak to zrobić:

```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENTS DIRECTORY";

// Utwórz katalog, jeśli jeszcze nie istnieje.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
     System.IO.Directory.CreateDirectory(dataDir);

// Utwórz nowy skoroszyt.
Workbook wb = new Workbook();

// Utwórz obiekt arkusza kalkulacyjnego i uzyskaj pierwszy arkusz.
Worksheet sheet = wb.Worksheets[0];
```

## Krok 3: Ustawianie stylu i flagi stylu

Teraz ustawimy styl komórki i flagę stylu, aby odblokować wszystkie kolumny w arkuszu. Oto niezbędny kod:

```csharp
// Ustaw obiekt stylu.
Styling styling;

// Ustaw obiekt styleflag.
StyleFlag flag;

// Przejdź przez wszystkie kolumny w arkuszu i odblokuj je.
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     flag = new StyleFlag();
     flag. Locked = true;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
```

## Krok 4: Chroń konkretną linię

Teraz będziemy chronić konkretny wiersz w arkuszu. Zablokujemy pierwszy rząd, aby zapobiec jakimkolwiek modyfikacjom. Oto jak:

```csharp
// Zdobądź styl pierwszej linii.
style = sheet.Cells.Rows[0].Style;

// Zablokuj to.
style. IsLocked = true;

//Utwórz instancję flagi.
flag = new StyleFlag();

// Ustaw parametr blokady.
flag. Locked = true;

// Zastosuj styl do pierwszej linii.
sheet.Cells.ApplyRowStyle(0, style, flag);
```

## Krok 5: Ochrona arkusza

Wreszcie zabezpieczymy cały arkusz Excela, aby zapobiec nieautoryzowanym modyfikacjom. Oto jak:

```csharp
// Chroń arkusz.
sheet.Protect(ProtectionType.All);
```

## Krok 6: Zapisz chroniony plik Excel

Po zakończeniu zabezpieczania określonego wiersza w arkuszu programu Excel możesz zapisać chroniony plik Excel w swoim systemie. Oto jak:

```csharp
// Zapisz plik Excela.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Po wykonaniu tych kroków pomyślnie zabezpieczysz określony wiersz w arkuszu kalkulacyjnym Excel przy użyciu Aspose.Cells dla .NET.

### Przykładowy kod źródłowy dla funkcji Chroń określony wiersz w arkuszu programu Excel przy użyciu Aspose.Cells dla platformy .NET 
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
// Zdobądź styl pierwszego rzędu.
style = sheet.Cells.Rows[0].Style;
// Zablokuj to.
style.IsLocked = true;
//Utwórz instancję flagi.
flag = new StyleFlag();
// Ustaw ustawienie blokady.
flag.Locked = true;
// Zastosuj styl do pierwszego wiersza.
sheet.Cells.ApplyRowStyle(0, style, flag);
// Chroń prześcieradło.
sheet.Protect(ProtectionType.All);
// Zapisz plik Excela.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## Wniosek

Ochrona danych w plikach Excel ma kluczowe znaczenie, aby zapobiec nieautoryzowanemu dostępowi lub niechcianym modyfikacjom. Korzystając z biblioteki Aspose.Cells dla .NET, możesz łatwo chronić określone wiersze w arkuszu kalkulacyjnym Excel, korzystając z dostarczonego kodu źródłowego C#. Postępuj zgodnie z tym przewodnikiem krok po kroku, aby dodać dodatkową warstwę zabezpieczeń do plików Excel.

### Często zadawane pytania

#### Czy określona ochrona wierszy działa we wszystkich wersjach programu Excel?

Tak, specyficzna ochrona wierszy przy użyciu Aspose.Cells dla .NET działa we wszystkich obsługiwanych wersjach programu Excel.

#### Czy mogę chronić wiele określonych wierszy w arkuszu kalkulacyjnym Excel?

Tak, możesz chronić wiele określonych wierszy, korzystając z podobnych metod opisanych w tym przewodniku.

#### Jak odblokować określony wiersz w arkuszu kalkulacyjnym Excel?

 Aby odblokować określony wiersz, należy odpowiednio zmodyfikować kod źródłowy za pomocą`IsLocked` metoda`Style` obiekt.