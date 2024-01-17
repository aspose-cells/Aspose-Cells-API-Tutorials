---
title: Dodaj arkusz programu Excel do istniejącego skoroszytu. Samouczek C#
linktitle: Dodaj arkusz programu Excel do istniejącego skoroszytu
second_title: Aspose.Cells dla .NET API odniesienia
description: łatwością dodawaj nowy arkusz do istniejącego skoroszytu programu Excel za pomocą Aspose.Cells dla .NET. Samouczek krok po kroku z przykładami kodu.
type: docs
weight: 10
url: /pl/net/excel-worksheet-csharp-tutorials/add-excel-worksheet-to-existing-workbook-csharp-tutorial/
---
W tym samouczku poprowadzimy Cię krok po kroku do wyjaśnienia poniższego kodu źródłowego C#, który pomaga dodać nowy arkusz do istniejącego skoroszytu programu Excel przy użyciu Aspose.Cells dla .NET. Do każdego kroku dołączymy przykładowy kod, który pomoże Ci szczegółowo zrozumieć proces.

## Krok 1: Zdefiniuj katalog dokumentów

Aby rozpocząć, musisz ustawić ścieżkę katalogu, w którym znajduje się plik Excel. Zastąp „KATALOG TWOJEGO DOKUMENTU” w kodzie rzeczywistą ścieżką do pliku Excel.

```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENT DIRECTORY";
```

## Krok 2: Utwórz strumień plików i otwórz plik Excel

 Następnie musisz utworzyć strumień pliku i otworzyć plik Excel za pomocą`FileStream` klasa.

```csharp
// Utwórz strumień pliku zawierający plik Excel do otwarcia
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

## Krok 3: Utwórz instancję obiektu skoroszytu

 Po otwarciu pliku Excel należy utworzyć instancję pliku`Workbook`obiekt. Obiekt ten reprezentuje skoroszyt programu Excel i oferuje różne metody i właściwości umożliwiające manipulowanie skoroszytem.

```csharp
// Utwórz instancję obiektu skoroszytu
// Otwórz plik Excel poprzez przepływ plików
Workbook workbook = new Workbook(fstream);
```

## Krok 4: Dodaj nowy arkusz do skoroszytu

 Aby dodać nowy arkusz do skoroszytu, możesz użyć metody`Worksheets.Add()` metoda`Workbook` obiekt. Metoda ta zwraca indeks nowo dodanego arkusza.

```csharp
// Dodaj nowy arkusz do skoroszytu Skoroszyt
int i = workbook. Worksheets. Add();
```

## Krok 5: Ustaw nową nazwę arkusza

 Możesz ustawić nazwę nowo dodanego arkusza za pomocą`Name` własność`Worksheet` obiekt.

```csharp
// Uzyskaj odniesienie do nowego dodanego arkusza, przekazując jego indeks arkusza
Worksheet worksheet = workbook.Worksheets[i];
// Zdefiniuj nazwę nowego arkusza
worksheet.Name = "My Worksheet";
```

## Krok 6: Zapisz plik Excel

 Po dodaniu nowego arkusza i ustaleniu jego nazwy możesz zapisać zmodyfikowany plik Excel za pomocą`Save()` metoda`Workbook` obiekt.

```csharp
// Zapisz plik Excela
workbook.Save(dataDir + "output.out.xls");
```

## Krok 7: Zamknij strumień plików i zwolnij zasoby

Na koniec ważne jest zamknięcie strumienia plików, aby zwolnić wszystkie powiązane z nim zasoby.

```csharp
// Zamknij strumień plików, aby zwolnić wszystkie zasoby
fstream.Close();
```

### Przykładowy kod źródłowy dla dodawania arkusza programu Excel do istniejącego skoroszytu Samouczek C# przy użyciu Aspose.Cells dla .NET 
```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Tworzenie strumienia plików zawierającego plik Excel do otwarcia
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Tworzenie instancji obiektu skoroszytu
// Otwieranie pliku Excel poprzez strumień pliku
Workbook workbook = new Workbook(fstream);
// Dodanie nowego arkusza do obiektu Workbook
int i = workbook.Worksheets.Add();
// Uzyskanie odniesienia do nowo dodanego arkusza poprzez przekazanie jego indeksu arkusza
Worksheet worksheet = workbook.Worksheets[i];
// Ustawianie nazwy nowo dodanego arkusza
worksheet.Name = "My Worksheet";
// Zapisywanie pliku Excel
workbook.Save(dataDir + "output.out.xls");
// Zamknięcie strumienia plików w celu zwolnienia wszystkich zasobów
fstream.Close();
```

## Wniosek

W tym samouczku omówiliśmy krok po kroku proces dodawania nowego Fire Connect do istniejącego skoroszytu programu Excel przy użyciu Aspose.Cells dla .NET. Postępując zgodnie z podanymi przykładami kodu i objaśnieniami, powinieneś już dobrze rozumieć, jak wykonać to zadanie w aplikacjach C#. Aspose.Cells dla .NET oferuje kompleksowy zestaw funkcji do pracy z plikami Excel, umożliwiając wydajną automatyzację różnych zadań związanych z Excelem.

### Często zadawane pytania (FAQ)

#### Co to jest Aspose.Cells dla .NET?

Aspose.Cells dla .NET to potężna biblioteka .NET, która pozwala programistom tworzyć, manipulować i konwertować pliki Excel w swoich aplikacjach. Oferuje szeroką gamę funkcji do pracy z arkuszami kalkulacyjnymi, komórkami, formułami, stylami i nie tylko.

#### Jak mogę zainstalować Aspose.Cells dla .NET?

Aby zainstalować Aspose.Cells dla .NET, możesz pobrać pakiet instalacyjny z Aspose Releases (https://releases.aspose.com/cells/net) i postępuj zgodnie z dostarczonymi instrukcjami instalacji. Będziesz także potrzebować ważnej licencji na korzystanie z biblioteki w swoich aplikacjach.

#### Czy mogę dodać wiele arkuszy kalkulacyjnych za pomocą Aspose.Cells dla .NET?

 Tak, możesz dodać wiele arkuszy do jednego pliku Excel za pomocą Aspose.Cells dla .NET. Możesz skorzystać z`Worksheets.Add()` metoda`Workbook` obiekt, aby dodać nowe arkusze w różnych pozycjach skoroszytu.

#### Jak sformatować komórki w pliku Excel?

Aspose.Cells dla .NET oferuje różne metody i właściwości formatowania komórek w pliku Excel. Możesz ustawić wartości komórek, zastosować opcje formatowania, takie jak styl czcionki, kolor, wyrównanie, obramowania i inne. Zobacz dokumentację i przykładowy kod dostarczony przez Aspose.Cells, aby uzyskać bardziej szczegółowe informacje na temat formatowania komórek.

#### Czy Aspose.Cells for .NET jest kompatybilny z różnymi wersjami Excela?

Tak, Aspose.Cells dla .NET jest kompatybilny z różnymi wersjami programu Excel, w tym Excel 2003, Excel 2007, Excel 2010, Excel 2013, Excel 2016, Excel 2019 i Excel dla Office 365. Obsługuje zarówno format .xls, jak i nowszy . formacie xlsx.