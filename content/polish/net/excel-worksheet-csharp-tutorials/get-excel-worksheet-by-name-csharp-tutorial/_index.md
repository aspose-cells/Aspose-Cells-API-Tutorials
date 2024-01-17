---
title: Pobierz arkusz programu Excel według nazwy — samouczek C#
linktitle: Pobierz arkusz programu Excel według nazwy
second_title: Aspose.Cells dla .NET API odniesienia
description: Dowiedz się, jak uzyskać arkusz programu Excel według nazwy za pomocą Aspose.Cells dla .NET. Samouczek krok po kroku z przykładami kodu.
type: docs
weight: 50
url: /pl/net/excel-worksheet-csharp-tutorials/get-excel-worksheet-by-name-csharp-tutorial/
---
W tym samouczku poprowadzimy Cię krok po kroku, aby wyjaśnić poniższy kod źródłowy C#, który może uzyskać arkusz programu Excel przy użyciu Aspose.Cells dla .NET, używając jego nazwy. Do każdego kroku dołączymy przykładowy kod, który pomoże Ci szczegółowo zrozumieć proces.

## Krok 1: Zdefiniuj katalog dokumentów

Aby rozpocząć, musisz ustawić ścieżkę katalogu, w którym znajduje się plik Excel. Zastąp „KATALOG TWOJEGO DOKUMENTU” w kodzie rzeczywistą ścieżką do pliku Excel.

```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENT DIRECTORY";
```

## Krok 2: Ustaw ścieżkę wejściową pliku Excel

Następnie musisz ustawić ścieżkę wejściową pliku Excel, który chcesz otworzyć. Ta ścieżka zostanie użyta do utworzenia strumienia plików.

```csharp
// Ścieżka wejściowa pliku Excel
string InputPath = dataDir + "book1.xlsx";
```

## Krok 3: Utwórz strumień plików i otwórz plik Excel

 Następnie musisz utworzyć strumień pliku i otworzyć plik Excel za pomocą`FileStream` klasa.

```csharp
// Utwórz strumień pliku zawierający plik Excel do otwarcia
FileStream fstream = new FileStream(InputPath, FileMode.Open);
```

## Krok 4: Utwórz instancję obiektu skoroszytu

 Po otwarciu pliku Excel należy utworzyć instancję pliku`Workbook`obiekt. Obiekt ten reprezentuje skoroszyt programu Excel i oferuje różne metody i właściwości umożliwiające manipulowanie skoroszytem.

```csharp
// Utwórz instancję obiektu skoroszytu
// Otwórz plik Excel poprzez przepływ plików
Workbook workbook = new Workbook(fstream);
```

## Krok 5: Uzyskaj dostęp do arkusza według nazwy

Aby uzyskać dostęp do określonego arkusza według nazwy, możesz użyć metody`Worksheets` własność`Workbook` obiekt i indeksuj nazwę arkusza.

```csharp
// Uzyskaj dostęp do arkusza, używając jego nazwy arkusza
Worksheet worksheet = workbook.Worksheets["Sheet1"];
```

## Krok 6: Uzyskaj dostęp do określonej komórki

 Po przejściu do żądanego arkusza możesz przejść do określonej komórki za pomocą`Cells` własność`Worksheet` obiekt i indeksuj odwołanie do komórki.

```csharp
// Dostęp do określonej komórki
Cell cell = worksheet.Cells["A1"];
```

## Krok 7: Pobierz wartość komórki

 Na koniec możesz pobrać wartość komórki za pomocą metody`Value` własność`Cell` obiekt.

```csharp
// Pobierz wartość komórki
Console.WriteLine(cell.Value);
```

### Przykładowy kod źródłowy dla samouczka Pobierz arkusz programu Excel według nazwy C# przy użyciu Aspose.Cells dla .NET 
```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xlsx";
// Tworzenie strumienia plików zawierającego plik Excel do otwarcia
FileStream fstream = new FileStream(InputPath, FileMode.Open);
// Tworzenie instancji obiektu skoroszytu
// Otwieranie pliku Excel poprzez strumień pliku
Workbook workbook = new Workbook(fstream);
// Dostęp do arkusza przy użyciu jego nazwy
Worksheet worksheet = workbook.Worksheets["Sheet1"];
Cell cell = worksheet.Cells["A1"];
Console.WriteLine(cell.Value);
```

## Wniosek

W tym samouczku omówiliśmy krok po kroku proces uzyskiwania określonego arkusza programu Excel według jego nazwy przy użyciu Aspose.Cells dla .NET. Możesz teraz wykorzystać tę wiedzę do wydajnego i dokładnego manipulowania i przetwarzania danych w plikach Excel.

### Często zadawane pytania (FAQ)

#### Co to jest Aspose.Cells dla .NET?

Aspose.Cells dla .NET to potężna biblioteka, która pozwala programistom tworzyć, manipulować i konwertować pliki Excel w aplikacjach .NET. Oferuje szeroką gamę funkcji do pracy z arkuszami, komórkami, formułami, stylami i nie tylko.

#### Jak mogę zainstalować Aspose.Cells dla .NET?

Aby zainstalować Aspose.Cells dla .NET, możesz pobrać pakiet instalacyjny z Aspose.Releases (https://releases.aspose.com/cells/net) i postępuj zgodnie z podanymi instrukcjami. Aby korzystać z biblioteki w swoich aplikacjach, będziesz potrzebować ważnej licencji.

#### Czy mogę uzyskać arkusz programu Excel, używając jego nazwy w Aspose.Cells dla .NET?

 Tak, możesz uzyskać arkusz programu Excel, używając jego nazwy w Aspose.Cells dla .NET. Możesz skorzystać z`Worksheets` własność`Workbook` obiekt i zindeksuj nazwę arkusza, aby uzyskać do niego dostęp.

#### Co się stanie, jeśli nazwa arkusza nie istnieje w pliku Excel?

Jeśli określona nazwa arkusza nie istnieje w pliku Excel, przy próbie uzyskania dostępu do tego arkusza zostanie zgłoszony wyjątek. Przed uzyskaniem dostępu do arkusza sprawdź, czy nazwa arkusza została wpisana poprawnie i czy istnieje w pliku Excel.

#### Czy mogę używać Aspose.Cells for .NET do manipulowania danymi komórek w arkuszu?

Tak, Aspose.Cells dla .NET oferuje wiele funkcji do manipulowania danymi komórek w arkuszu. Możesz czytać i zapisywać wartości komórek, stosować formaty, dodawać formuły, łączyć komórki, wykonywać operacje matematyczne i nie tylko. Biblioteka zapewnia kompleksowy interfejs do pracy z danymi komórkowymi w programie Excel.