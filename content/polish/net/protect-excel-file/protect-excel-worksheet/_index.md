---
title: Chroń arkusz programu Excel
linktitle: Chroń arkusz programu Excel
second_title: Aspose.Cells dla .NET API odniesienia
description: W tym samouczku dowiesz się, jak chronić arkusz kalkulacyjny Excel za pomocą Aspose.Cells dla .NET. Przewodnik krok po kroku w języku C#.
type: docs
weight: 50
url: /pl/net/protect-excel-file/protect-excel-worksheet/
---
tym samouczku przyjrzymy się kodowi źródłowemu C#, który używa biblioteki Aspose.Cells do ochrony arkusza kalkulacyjnego Excel. Przejdziemy przez każdy krok kodu i wyjaśnimy, jak to działa. Aby uzyskać pożądane rezultaty, postępuj zgodnie z instrukcjami.

## Krok 1: Warunki wstępne

Zanim zaczniesz, upewnij się, że zainstalowałeś bibliotekę Aspose.Cells dla .NET. Można go pobrać z oficjalnej strony Aspose. Upewnij się także, że masz najnowszą wersję programu Visual Studio lub innego środowiska programistycznego C#.

## Krok 2: Zaimportuj wymagane przestrzenie nazw

Aby skorzystać z biblioteki Aspose.Cells, musimy zaimportować do naszego kodu niezbędne przestrzenie nazw. Dodaj następujące wiersze na górze pliku źródłowego C#:

```csharp
using Aspose.Cells;
using System.IO;
```

## Krok 3: Załaduj plik Excel

W tym kroku załadujemy plik Excel, który chcemy chronić. Pamiętaj o podaniu prawidłowej ścieżki do katalogu zawierającego plik Excel. Aby przesłać plik, użyj poniższego kodu:

```csharp
// Ścieżka do katalogu dokumentów.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Utwórz strumień plików zawierający plik Excel do otwarcia.
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);

// Utwórz instancję obiektu skoroszytu.
//Otwórz plik Excel poprzez strumień plików.
Workbook excel = new Workbook(fstream);
```

 Pamiętaj o wymianie`"YOUR_DOCUMENTS_DIR"` z odpowiednią ścieżką do katalogu dokumentów.

## Krok 4: Uzyskaj dostęp do arkusza kalkulacyjnego

Teraz, gdy załadowaliśmy plik Excel, możemy uzyskać dostęp do pierwszego arkusza. Użyj poniższego kodu, aby uzyskać dostęp do pierwszego arkusza:

```csharp
// Dostęp do pierwszego arkusza w pliku Excel.
Worksheet worksheet = excel.Worksheets[0];
```

## Krok 5: Chroń arkusz

Na tym etapie zabezpieczymy arkusz kalkulacyjny hasłem. Użyj poniższego kodu, aby zabezpieczyć arkusz kalkulacyjny:

```csharp
// Chroń arkusz hasłem.
worksheet.Protect(ProtectionType.All, "YOUR_PASSWORD", null);
```

 Zastępować`"YOUR_PASSWORD"` hasłem, którego chcesz używać do ochrony arkusza kalkulacyjnego.

## Krok 6: Zapisz zmodyfikowany plik Excel Teraz, gdy już go zabezpieczyliśmy

é arkusza kalkulacyjnego, zapiszemy zmodyfikowany plik Excel w domyślnym formacie. Użyj poniższego kodu, aby zapisać plik Excel:

```csharp
// Zapisz zmodyfikowany plik Excel w formacie domyślnym.
excel.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Upewnij się, że podałeś poprawną ścieżkę do zapisania zmodyfikowanego pliku Excel.

## Krok 7: Zamknij strumień plików

Aby zwolnić wszystkie zasoby, musimy zamknąć strumień pliku używany do ładowania pliku Excel. Użyj poniższego kodu, aby zamknąć strumień pliku:

```csharp
// Zamknij strumień plików, aby zwolnić wszystkie zasoby.
fstream.Close();
```

Pamiętaj, aby uwzględnić ten krok na końcu kodu.


### Przykładowy kod źródłowy programu Protect Excel Worksheet przy użyciu Aspose.Cells dla .NET 
```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Tworzenie strumienia plików zawierającego plik Excel do otwarcia
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Tworzenie instancji obiektu skoroszytu
// Otwieranie pliku Excel poprzez strumień pliku
Workbook excel = new Workbook(fstream);
// Dostęp do pierwszego arkusza w pliku Excel
Worksheet worksheet = excel.Worksheets[0];
// Ochrona arkusza hasłem
worksheet.Protect(ProtectionType.All, "aspose", null);
// Zapisanie zmodyfikowanego pliku Excel w formacie domyślnym
excel.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
// Zamknięcie strumienia plików w celu zwolnienia wszystkich zasobów
fstream.Close();
```

## Wniosek

Gratulacje! Masz teraz kod źródłowy C#, który pozwala chronić arkusz kalkulacyjny Excel przy użyciu biblioteki Aspose.Cells dla .NET. Postępuj dokładnie zgodnie z instrukcjami i dostosuj kod do swoich konkretnych potrzeb.

### Często zadawane pytania (często zadawane pytania)

#### Czy można chronić wiele arkuszy kalkulacyjnych w jednym pliku Excel?

Odp.: Tak, możesz chronić wiele arkuszy w jednym pliku Excel, powtarzając kroki 4-6 dla każdego arkusza.

#### Jak mogę określić konkretne uprawnienia dla autoryzowanych użytkowników?

 Odp.: Możesz skorzystać z dodatkowych opcji udostępnianych przez`Protect`metoda określania konkretnych uprawnień dla autoryzowanych użytkowników. Więcej informacji można znaleźć w dokumentacji Aspose.Cells.

#### Czy mogę zabezpieczyć sam plik Excel hasłem?

O: Tak, możesz zabezpieczyć hasłem sam plik Excel, korzystając z innych metod udostępnianych przez bibliotekę Aspose.Cells. Konkretne przykłady można znaleźć w dokumentacji.

#### Czy biblioteka Aspose.Cells obsługuje inne formaty plików Excel?

O: Tak, biblioteka Aspose.Cells obsługuje szeroką gamę formatów plików Excel, w tym XLSX, XLSM, XLSB, CSV itp.