---
title: Usuń ochronę prostego arkusza Excel
linktitle: Usuń ochronę prostego arkusza Excel
second_title: Aspose.Cells dla .NET API odniesienia
description: Dowiedz się, jak odblokować arkusz kalkulacyjny Excel za pomocą Aspose.Cells dla .NET. Samouczek krok po kroku w języku C#.
type: docs
weight: 30
url: /pl/net/unprotect-excel-sheet/unprotect-simple-excel-sheet/
---
W tym samouczku przeprowadzimy Cię przez kroki wymagane do odblokowania prostego arkusza kalkulacyjnego Excel przy użyciu biblioteki Aspose.Cells dla .NET.

## Krok 1: Przygotowanie środowiska

Zanim zaczniesz, upewnij się, że masz zainstalowany Aspose.Cells for .NET na swoim komputerze. Pobierz bibliotekę z oficjalnej strony Aspose i postępuj zgodnie z dostarczonymi instrukcjami instalacji.

## Krok 2: Konfiguracja ścieżki katalogu dokumentów

 W dostarczonym kodzie źródłowym musisz określić ścieżkę katalogu, w którym znajduje się plik Excel, który chcesz odblokować. Zmodyfikuj`dataDir` zmienną, zastępując „TWOJ KATALOG DOKUMENTÓW” bezwzględną ścieżką katalogu na twoim komputerze.

```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
```

## Krok 3: Tworzenie obiektu skoroszytu

Na początek musimy utworzyć obiekt Workbook reprezentujący nasz plik Excel. Użyj konstruktora klasy Workbook i określ pełną ścieżkę pliku Excel do otwarcia.

```csharp
// Tworzenie instancji obiektu skoroszytu
Workbook workbook = new Workbook(dataDir + "book1.xls");
```

## Krok 4: Dostęp do arkusza kalkulacyjnego

 Następnie musimy przejść do pierwszego arkusza w pliku Excel. Użyj`Worksheets` właściwości obiektu Workbook, aby uzyskać dostęp do kolekcji arkuszy, a następnie użyj metody`[0]` indeks, aby uzyskać dostęp do pierwszego arkusza.

```csharp
// Dostęp do pierwszego arkusza w pliku Excel
Worksheet worksheet = workbook.Worksheets[0];
```

## Krok 5: Odblokowanie arkusza kalkulacyjnego

 Teraz odblokujemy arkusz za pomocą`Unprotect()` metoda obiektu Worksheet. Ta metoda nie wymaga hasła.

```csharp
// Odbezpieczanie arkusza bez hasła
worksheet.Unprotect();
```

## Krok 6: Zapisanie odblokowanego pliku Excel

Po odblokowaniu arkusza kalkulacyjnego możemy zapisać ostateczny plik Excel. Użyj`Save()` metodę określającą pełną ścieżkę pliku wyjściowego i format zapisu.

```csharp
// Zapisywanie skoroszytu
workbook.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```
### Przykładowy kod źródłowy dla opcji Unprotect Simple Excel Sheet przy użyciu Aspose.Cells dla .NET 
```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Tworzenie instancji obiektu skoroszytu
Workbook workbook = new Workbook(dataDir + "book1.xls");
// Dostęp do pierwszego arkusza w pliku Excel
Worksheet worksheet = workbook.Worksheets[0];
// Odbezpieczanie arkusza bez hasła
worksheet.Unprotect();
// Zapisywanie skoroszytu
workbook.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## Wniosek

Gratulacje! Nauczyłeś się teraz, jak odblokować prosty arkusz kalkulacyjny Excel przy użyciu Aspose.Cells dla .NET. Wykonując kroki opisane w tym samouczku, możesz łatwo zastosować tę funkcję do własnych projektów.

Zachęcamy do zapoznania się z dodatkowymi funkcjami Aspose.Cells
do bardziej zaawansowanych operacji na plikach Excel.

### Często zadawane pytania

#### P: Jakie środki ostrożności należy podjąć podczas odblokowywania arkusza kalkulacyjnego Excel?

Odp.: Odblokowując arkusz kalkulacyjny Excel, upewnij się, że masz niezbędne uprawnienia dostępu do pliku. Pamiętaj także, aby użyć prawidłowej metody odblokowania i podać prawidłowe hasło, jeśli ma to zastosowanie.

#### P: Skąd mam wiedzieć, czy arkusz kalkulacyjny jest chroniony hasłem?

 Odp.: Możesz sprawdzić, czy arkusz jest chroniony hasłem, korzystając z właściwości lub metod dostarczonych przez bibliotekę Aspose.Cells dla .NET. Można na przykład użyć`IsProtected()` metoda obiektu Worksheet w celu sprawdzenia, czy arkusz jest chroniony.

#### P: Podczas próby odblokowania arkusza kalkulacyjnego pojawia się wyjątek. Co powinienem zrobić ?

Odp.: Jeśli podczas odblokowywania arkusza kalkulacyjnego napotkasz wyjątek, upewnij się, że poprawnie określiłeś ścieżkę do pliku Excel i sprawdź, czy masz niezbędne uprawnienia dostępu do niego. Jeśli problem będzie się powtarzał, skontaktuj się z obsługą Aspose.Cells w celu uzyskania dalszej pomocy.