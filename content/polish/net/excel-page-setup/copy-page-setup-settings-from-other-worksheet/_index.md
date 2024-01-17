---
title: Skopiuj ustawienia ustawień strony z innego arkusza
linktitle: Skopiuj ustawienia ustawień strony z innego arkusza
second_title: Aspose.Cells dla .NET API odniesienia
description: Dowiedz się, jak skopiować ustawienia konfiguracji strony z jednego arkusza kalkulacyjnego do drugiego za pomocą Aspose.Cells dla .NET. Przewodnik krok po kroku dotyczący optymalizacji wykorzystania tej biblioteki.
type: docs
weight: 10
url: /pl/net/excel-page-setup/copy-page-setup-settings-from-other-worksheet/
---
W tym artykule poprowadzimy Cię krok po kroku do wyjaśnienia następującego kodu źródłowego C#: Skopiuj ustawienia konfiguracji strony z innego arkusza kalkulacyjnego za pomocą Aspose.Cells dla .NET. Do wykonania tej operacji użyjemy biblioteki Aspose.Cells dla .NET. Jeśli chcesz skopiować ustawienia ustawień strony z jednego arkusza do drugiego, wykonaj poniższe czynności.

## Krok 1: Tworzenie skoroszytu
Pierwszym krokiem jest utworzenie skoroszytu. W naszym przypadku skorzystamy z klasy Workbook udostępnionej przez bibliotekę Aspose.Cells. Oto kod umożliwiający utworzenie skoroszytu:

```csharp
Workbook wb = new Workbook();
```

## Krok 2: Dodawanie arkuszy testowych
Po utworzeniu skoroszytu musimy dodać arkusze testowe. W tym przykładzie dodamy dwa arkusze. Oto kod umożliwiający dodanie dwóch arkuszy:

```csharp
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
```

## Krok 3: Dostęp do arkuszy ćwiczeń
Teraz, gdy dodaliśmy arkusze, musimy uzyskać do nich dostęp, aby móc zmienić ich ustawienia. Dostęp do arkuszy „TestSheet1” i „TestSheet2” uzyskamy, używając ich nazw. Oto kod umożliwiający dostęp do niego:

```csharp
Worksheet TestSheet1 = wb. Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb. Worksheets["TestSheet2"];
```

## Krok 4: Ustawianie rozmiaru papieru
 W tym kroku ustawimy rozmiar papieru arkusza „TestSheet1”. Będziemy korzystać z`PageSetup.PaperSize` właściwość umożliwiająca ustawienie rozmiaru papieru. Przykładowo ustawimy rozmiar papieru na „PaperA3ExtraTransverse”. Oto kod do tego:

```csharp
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
```

## Krok 5: Kopiowanie ustawień ustawień strony
Teraz skopiujemy ustawienia konfiguracji strony z arkusza „TestSheet1” do „TestSheet2”. Będziemy korzystać z`PageSetup.Copy` sposób wykonania tej operacji. Oto kod do tego:

```csharp
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
```

## Krok 6: Drukowanie rozmiarów papieru
 Po skopiowaniu ustawień ustawień strony wydrukujemy rozmiary papieru obu arkuszy. Użyjemy`Console.WriteLine` aby wyświetlić rozmiary papieru. Oto kod do tego:

```csharp
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
```

### Przykładowy kod źródłowy dla opcji Kopiuj ustawienia ustawień strony z innego arkusza przy użyciu Aspose.Cells dla .NET 
```csharp
//Utwórz skoroszyt
Workbook wb = new Workbook();
//Dodaj dwa arkusze testowe
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
//Uzyskaj dostęp do obu arkuszy jako Arkusz Testowy1 i Arkusz Testowy2
Worksheet TestSheet1 = wb.Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb.Worksheets["TestSheet2"];
//Ustaw rozmiar papieru arkusza testowego 1 na PaperA3ExtraTransverse
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
//Wydrukuj rozmiar papieru obu arkuszy
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
//Skopiuj ustawienie PageSetup z arkusza testowego1 do arkusza testowego2
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
//Wydrukuj rozmiar papieru obu arkuszy
Console.WriteLine("After Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("After Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
Console.WriteLine("CopyPageSetupSettingsFromSourceWorksheetToDestinationWorksheet executed successfully.\r\n");
```

## Wniosek
tym artykule dowiedzieliśmy się, jak kopiować ustawienia konfiguracji strony z jednego arkusza do drugiego za pomocą Aspose.Cells dla .NET. Wykonaliśmy następujące kroki: utworzenie skoroszytu, dodanie arkuszy testowych, uzyskanie dostępu do arkuszy kalkulacyjnych, ustawienie rozmiaru papieru, skopiowanie ustawień ustawień strony i wydrukowanie rozmiarów papieru. Teraz możesz wykorzystać tę wiedzę do kopiowania ustawień konfiguracyjnych strony do własnych projektów.

### Często zadawane pytania

#### P: Czy mogę kopiować ustawienia konfiguracji strony między różnymi instancjami skoroszytu?

 Odp.: Tak, możesz kopiować ustawienia ustawień strony między różnymi instancjami skoroszytu za pomocą pliku`PageSetup.Copy` metoda biblioteki Aspose.Cells.

#### P: Czy mogę skopiować inne ustawienia ustawień strony, takie jak orientacja lub marginesy?

 O: Tak, możesz skopiować inne ustawienia ustawień strony za pomocą pliku`PageSetup.Copy` metodę z odpowiednimi opcjami. Na przykład możesz skopiować orientację za pomocą`CopyOptions.Orientation` i marże`CopyOptions.Margins`.

#### P: Skąd mam wiedzieć, jakie opcje są dostępne dla rozmiaru papieru?

Odp.: Możesz sprawdzić dokumentację API biblioteki Aspose.Cells, aby zapoznać się z dostępnymi opcjami rozmiaru papieru. Istnieje wyliczenie tzw`PaperSizeType` która zawiera listę różnych obsługiwanych rozmiarów papieru.

#### P: Jak mogę pobrać bibliotekę Aspose.Cells dla .NET?

 O: Możesz pobrać bibliotekę Aspose.Cells dla .NET z[Wydania Aspose](https://releases.aspose.com/cells/net). Dostępne są bezpłatne wersje próbne, a także płatne licencje do użytku komercyjnego.

#### P: Czy biblioteka Aspose.Cells obsługuje inne języki programowania?

O: Tak, biblioteka Aspose.Cells obsługuje wiele języków programowania, w tym C#, Java, Python i wiele innych.