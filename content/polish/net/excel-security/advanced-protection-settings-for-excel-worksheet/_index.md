---
title: Zaawansowane ustawienia ochrony arkusza programu Excel
linktitle: Zaawansowane ustawienia ochrony arkusza programu Excel
second_title: Aspose.Cells dla .NET API odniesienia
description: Chroń swoje pliki Excel, ustawiając zaawansowane ustawienia ochrony za pomocą Aspose.Cells dla .NET.
type: docs
weight: 10
url: /pl/net/excel-security/advanced-protection-settings-for-excel-worksheet/
---
W tym samouczku przeprowadzimy Cię przez etapy konfigurowania zaawansowanych ustawień ochrony arkusza kalkulacyjnego Excel przy użyciu biblioteki Aspose.Cells dla platformy .NET. Aby ukończyć to zadanie, postępuj zgodnie z poniższymi instrukcjami.

## Krok 1: Przygotowanie

Upewnij się, że zainstalowałeś Aspose.Cells dla .NET i utworzyłeś projekt C# w preferowanym zintegrowanym środowisku programistycznym (IDE).

## Krok 2: Ustaw ścieżkę katalogu dokumentów

 Zadeklaruj`dataDir` zmienną i zainicjuj ją ścieżką do katalogu dokumentów. Na przykład :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Pamiętaj o wymianie`"YOUR_DOCUMENTS_DIRECTORY"` z rzeczywistą ścieżką do katalogu.

## Krok 3: Utwórz strumień pliku, aby otworzyć plik Excel

 Stwórz`FileStream` obiekt zawierający plik Excel do otwarcia:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 Upewnij się, że masz plik Excel`book1.xls` w katalogu dokumentów lub podaj poprawną nazwę pliku i lokalizację.

## Krok 4: Utwórz instancję obiektu skoroszytu i otwórz plik Excel

 Użyj`Workbook`class z Aspose.Cells, aby utworzyć instancję obiektu Workbook i otworzyć określony plik Excel poprzez strumień pliku:

```csharp
Workbook excel = new Workbook(fstream);
```

## Krok 5: Uzyskaj dostęp do pierwszego arkusza

Przejdź do pierwszego arkusza pliku Excel:

```csharp
Worksheet worksheet = excel.Worksheets[0];
```

## Krok 6: Ustaw ustawienia ochrony arkusza

Użyj właściwości obiektu arkusza kalkulacyjnego, aby zgodnie z potrzebami ustawić ustawienia ochrony arkusza. Na przykład :

```csharp
worksheet.Protection.AllowDeletingColumn = false;
worksheet.Protection.AllowDeletingRow = false;
worksheet.Protection.AllowEditingContent = false;
worksheet.Protection.AllowEditingObject = false;
// ... Ustaw inne ustawienia ochrony według potrzeb...
```

## Krok 7: Zapisz zmodyfikowany plik Excel

 Zapisz zmodyfikowany plik Excel za pomocą`Save` metoda obiektu Workbook:

```csharp
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

Pamiętaj, aby określić żądaną ścieżkę i nazwę pliku wyjściowego.

## Krok 8: Zamknij strumień plików

Po zapisaniu zamknij strumień pliku, aby zwolnić wszystkie powiązane zasoby:

```csharp
fstream.Close();
```
	
### Przykładowy kod źródłowy zaawansowanych ustawień ochrony dla arkusza programu Excel przy użyciu Aspose.Cells dla .NET 
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
// Ograniczanie użytkownikom możliwości usuwania kolumn arkusza
worksheet.Protection.AllowDeletingColumn = false;
// Ograniczanie użytkownikom możliwości usuwania wierszy arkusza
worksheet.Protection.AllowDeletingRow = false;
// Ograniczanie użytkownikom możliwości edytowania zawartości arkusza
worksheet.Protection.AllowEditingContent = false;
// Ograniczanie użytkownikom możliwości edycji obiektów arkusza
worksheet.Protection.AllowEditingObject = false;
// Ograniczanie użytkownikom możliwości edycji scenariuszy arkusza
worksheet.Protection.AllowEditingScenario = false;
//Ograniczanie użytkowników do filtrowania
worksheet.Protection.AllowFiltering = false;
// Zezwalanie użytkownikom na formatowanie komórek arkusza
worksheet.Protection.AllowFormattingCell = true;
// Zezwalanie użytkownikom na formatowanie wierszy arkusza
worksheet.Protection.AllowFormattingRow = true;
// Zezwalanie użytkownikom na wstawianie kolumn w arkuszu
worksheet.Protection.AllowFormattingColumn = true;
// Zezwalanie użytkownikom na wstawianie hiperłączy w arkuszu
worksheet.Protection.AllowInsertingHyperlink = true;
// Zezwalanie użytkownikom na wstawianie wierszy w arkuszu
worksheet.Protection.AllowInsertingRow = true;
// Zezwalanie użytkownikom na wybieranie zablokowanych komórek arkusza
worksheet.Protection.AllowSelectingLockedCell = true;
// Zezwalanie użytkownikom na wybieranie odblokowanych komórek arkusza
worksheet.Protection.AllowSelectingUnlockedCell = true;
// Zezwalanie użytkownikom na sortowanie
worksheet.Protection.AllowSorting = true;
// Zezwalanie użytkownikom na korzystanie z tabel przestawnych w arkuszu
worksheet.Protection.AllowUsingPivotTable = true;
// Zapisanie zmodyfikowanego pliku Excel
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
// Zamknięcie strumienia plików w celu zwolnienia wszystkich zasobów
fstream.Close();
```

## Wniosek

Gratulacje! Nauczyłeś się teraz, jak ustawić zaawansowane ustawienia ochrony arkusza kalkulacyjnego Excel przy użyciu Aspose.Cells dla .NET. Wykorzystaj tę wiedzę, aby zabezpieczyć swoje pliki Excel i ograniczyć działania użytkowników.

### Często zadawane pytania

#### P: Jak mogę utworzyć nowy projekt C# w moim środowisku IDE?

Odp.: kroki tworzenia nowego projektu C# mogą się różnić w zależności od używanego IDE. Szczegółowe instrukcje znajdziesz w dokumentacji swojego IDE.

#### P: Czy można ustawić niestandardowe ustawienia ochrony inne niż te wymienione w samouczku?

O: Tak, Aspose.Cells oferuje szeroką gamę ustawień ochrony, które możesz dostosować do swoich konkretnych potrzeb. Więcej szczegółów znajdziesz w dokumentacji Aspose.Cells.

#### P: Jaki jest format pliku używany do zapisania zmodyfikowanego pliku Excel w przykładowym kodzie?

Odp.: W przykładowym kodzie zmodyfikowany plik Excel jest zapisany w formacie Excel 97–2003 (.xls). W razie potrzeby możesz wybrać inne formaty obsługiwane przez Aspose.Cells.

#### P: Jak mogę uzyskać dostęp do innych arkuszy w pliku Excel?

 Odp.: Dostęp do innych arkuszy można uzyskać za pomocą indeksu lub nazwy arkusza, na przykład:`Worksheet worksheet = excel.Worksheets[1];` Lub`Worksheet worksheet = excel.Worksheets[" SheetName"];`.