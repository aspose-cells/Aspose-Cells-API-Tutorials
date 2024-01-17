---
title: Usuń arkusz programu Excel według nazwy Samouczek C#
linktitle: Usuń arkusz programu Excel według nazwy
second_title: Aspose.Cells dla .NET API odniesienia
description: Z łatwością usuń określony arkusz programu Excel według nazwy, używając Aspose.Cells dla .NET. Szczegółowy tutorial z przykładami kodu.
type: docs
weight: 40
url: /pl/net/excel-worksheet-csharp-tutorials/delete-excel-worksheet-by-name-csharp-tutorial/
---
tym samouczku poprowadzimy Cię krok po kroku, aby wyjaśnić poniższy kod źródłowy C#, który może usunąć arkusz Excela za pomocą Aspose.Cells dla .NET, używając jego nazwy. Do każdego kroku dołączymy przykładowy kod, który pomoże Ci szczegółowo zrozumieć proces.

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

## Krok 4: Usuń arkusz według nazwy

 Aby usunąć arkusz z jego nazwy, możesz użyć metody`RemoveAt()` metoda`Worksheets` przedmiot`Workbook` obiekt. Jako parametr należy przekazać nazwę arkusza, który chcesz usunąć.

```csharp
// Usuń arkusz, używając jego nazwy
workbook.Worksheets.RemoveAt("Sheet1");
```

## Krok 5: Zapisz skoroszyt

 Po usunięciu arkusza możesz zapisać zmodyfikowany skoroszyt programu Excel za pomocą`Save()` metoda`Workbook` obiekt.

```csharp
// Zapisz skoroszyt programu Excel
workbook.Save(dataDir + "output.out.xls");
```


### Przykładowy kod źródłowy narzędzia Usuń arkusz programu Excel według nazwy Samouczek C# przy użyciu Aspose.Cells dla platformy .NET 
```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Tworzenie strumienia plików zawierającego plik Excel do otwarcia
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Tworzenie instancji obiektu skoroszytu
// Otwieranie pliku Excel poprzez strumień pliku
Workbook workbook = new Workbook(fstream);
// Usuwanie arkusza przy użyciu jego nazwy arkusza
workbook.Worksheets.RemoveAt("Sheet1");
// Zapisz skoroszyt
workbook.Save(dataDir + "output.out.xls");
```

## Wniosek

tym samouczku omówiliśmy krok po kroku proces usuwania arkusza kalkulacyjnego Excel według nazwy za pomocą Aspose.Cells dla .NET. Postępując zgodnie z podanymi przykładami kodu i objaśnieniami, powinieneś już dobrze rozumieć, jak wykonać to zadanie w aplikacjach C#. Aspose.Cells dla .NET oferuje kompleksowy zestaw funkcji do pracy z plikami Excel, umożliwiając łatwą manipulację arkuszami kalkulacyjnymi i powiązanymi danymi.

### Często zadawane pytania (FAQ)

#### Co to jest Aspose.Cells dla .NET?

Aspose.Cells dla .NET to potężna biblioteka, która pozwala programistom tworzyć, manipulować i konwertować pliki Excel w aplikacjach .NET. Oferuje szeroką gamę funkcji do pracy z arkuszami kalkulacyjnymi, komórkami, formułami, stylami i nie tylko.

#### Jak mogę zainstalować Aspose.Cells dla .NET?

Aby zainstalować Aspose.Cells dla .NET, możesz pobrać pakiet instalacyjny z Aspose Releases (https://releases.aspose.com/cells/net) i postępuj zgodnie z podanymi instrukcjami. Aby korzystać z biblioteki w swoich aplikacjach, będziesz potrzebować ważnej licencji.

#### Czy mogę usunąć wiele arkuszy jednocześnie?

Tak, możesz usunąć wiele arkuszy za pomocą Aspose.Cells dla .NET. Możesz po prostu powtórzyć krok usuwania dla każdego arkusza, który chcesz usunąć.

#### Jak sprawdzić, czy arkusz kalkulacyjny istnieje przed jego usunięciem?

 Przed usunięciem arkusza możesz sprawdzić, czy istnieje, korzystając z opcji`Contains()` metoda`Worksheets` przedmiot`Workbook` obiekt. Ta metoda przyjmuje nazwę arkusza kalkulacyjnego jako parametr i zwraca`true` jeśli arkusz kalkulacyjny istnieje, w przeciwnym razie zwraca`false`.

#### Czy można odzyskać usunięty arkusz kalkulacyjny?

Niestety po usunięciu arkusza kalkulacyjnego nie można go odzyskać bezpośrednio z pliku Excel. Zaleca się utworzenie kopii zapasowej pliku Excel przed usunięciem arkusza kalkulacyjnego, aby uniknąć utraty danych.