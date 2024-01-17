---
title: Ukryj i odkryj arkusz
linktitle: Ukryj i odkryj arkusz
second_title: Aspose.Cells dla .NET API odniesienia
description: Potężna biblioteka do pracy z plikami Excel, w tym do tworzenia, modyfikowania i manipulowania danymi.
type: docs
weight: 90
url: /pl/net/excel-display-settings-csharp-tutorials/hide-and-unhide-worksheet/
---
W tym samouczku poprowadzimy Cię krok po kroku do wyjaśnienia następującego kodu źródłowego C#, który służy do ukrywania i pokazywania arkusza za pomocą Aspose.Cells dla .NET. Wykonaj poniższe kroki:

## Krok 1: Przygotowanie środowiska

Zanim zaczniesz, upewnij się, że masz zainstalowany Aspose.Cells for .NET w swoim systemie. Jeśli jeszcze go nie zainstalowałeś, możesz pobrać go z oficjalnej strony Aspose. Po zainstalowaniu możesz utworzyć nowy projekt w preferowanym zintegrowanym środowisku programistycznym (IDE).

## Krok 2: Zaimportuj wymagane przestrzenie nazw

W pliku źródłowym C# dodaj niezbędne przestrzenie nazw, aby móc korzystać z funkcji Aspose.Cells. Dodaj następujące wiersze na początku pliku:

```csharp
using Aspose.Cells;
using System.IO;
```

## Krok 3: Załaduj plik Excel

Przed ukryciem lub odkryciem arkusza należy załadować plik Excel do swojej aplikacji. Upewnij się, że plik Excel, którego chcesz użyć, znajduje się w tym samym katalogu, co Twój projekt. Użyj poniższego kodu, aby załadować plik Excel:

```csharp
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

Pamiętaj, aby zastąpić „ŚCIEŻKA DO KATALOGU DOKUMENTÓW” rzeczywistą ścieżką do katalogu zawierającego plik Excel.

## Krok 4: Uzyskaj dostęp do arkusza kalkulacyjnego

Po załadowaniu pliku Excel możesz przejść do arkusza, który chcesz ukryć lub odkryć. Użyj poniższego kodu, aby uzyskać dostęp do pierwszego arkusza w pliku:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Krok 5: Ukryj arkusz

 Teraz, gdy masz dostęp do arkusza, możesz go ukryć za pomocą`IsVisible` nieruchomość. Użyj poniższego kodu, aby ukryć pierwszy arkusz w pliku:

```csharp
worksheet. IsVisible = false;
```

## Krok 6: Wyświetl ponownie arkusz

Jeśli chcesz ponownie wyświetlić wcześniej ukryty arkusz, możesz użyć tego samego kodu, zmieniając wartość`IsVisible` nieruchomość. Użyj poniższego kodu, aby ponownie wyświetlić pierwszy arkusz:

```csharp
worksheet. IsVisible = true;
```

## Krok 7: Zapisz zmiany

Raz ty

  w razie potrzeby ukryłeś lub odkryłeś arkusz, musisz zapisać zmiany w pliku Excel. Użyj poniższego kodu, aby zapisać zmiany:

```csharp
workbook.Save(dataDir + "output.out.xls");
fstream.Close();
```

Upewnij się, że określono poprawną ścieżkę wyjściową, aby zapisać zmodyfikowany plik Excel.

### Przykładowy kod źródłowy arkusza Ukryj i odkryj przy użyciu Aspose.Cells dla .NET 

```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Tworzenie strumienia plików zawierającego plik Excel do otwarcia
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Tworzenie instancji obiektu skoroszytu poprzez otwarcie pliku Excel za pośrednictwem strumienia plików
Workbook workbook = new Workbook(fstream);
// Dostęp do pierwszego arkusza w pliku Excel
Worksheet worksheet = workbook.Worksheets[0];
// Ukrywanie pierwszego arkusza pliku Excel
worksheet.IsVisible = false;
// Pokazuje pierwszy arkusz pliku Excel
//Arkusz.IsVisible = true;
// Zapisanie zmodyfikowanego pliku Excel w domyślnym formacie (czyli Excel 2003).
workbook.Save(dataDir + "output.out.xls");
// Zamknięcie strumienia plików w celu zwolnienia wszystkich zasobów
fstream.Close();
```

## Wniosek

Gratulacje! Nauczyłeś się, jak ukrywać i wyświetlać arkusz kalkulacyjny za pomocą Aspose.Cells dla .NET. Możesz teraz używać tej funkcji do kontrolowania widoczności arkuszy kalkulacyjnych w plikach Excel.

### Często zadawane pytania (FAQ)

#### Jak mogę zainstalować Aspose.Cells dla .NET?

 Możesz zainstalować Aspose.Cells dla .NET, pobierając odpowiedni pakiet NuGet z[Wydania Aspose](https://releases/aspose.com/cells/net/) i dodanie go do projektu Visual Studio.

#### Jaka jest minimalna wymagana wersja .NET Framework do korzystania z Aspose.Cells dla .NET?

Aspose.Cells dla .NET obsługuje .NET Framework 2.0 i nowsze wersje.

#### Czy mogę otwierać i edytować istniejące pliki Excel za pomocą Aspose.Cells dla .NET?

Tak, możesz otwierać i edytować istniejące pliki Excel za pomocą Aspose.Cells dla .NET. Możesz uzyskać dostęp do arkuszy kalkulacyjnych, komórek, formuł i innych elementów pliku Excel.

#### Czy Aspose.Cells dla .NET obsługuje raportowanie i eksportowanie do innych formatów plików?

Tak, Aspose.Cells dla .NET obsługuje generowanie raportów i eksport do formatów takich jak PDF, HTML, CSV, TXT itp.

#### Czy modyfikacja pliku Excel jest trwała?

Tak, edycja pliku Excel jest trwała po jego zapisaniu. Przed wprowadzeniem jakichkolwiek zmian w oryginalnym pliku pamiętaj o zapisaniu kopii zapasowej.