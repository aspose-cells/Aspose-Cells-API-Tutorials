---
title: Excel Skopiuj arkusz z innego skoroszytu
linktitle: Excel Skopiuj arkusz z innego skoroszytu
second_title: Aspose.Cells dla .NET API odniesienia
description: Z łatwością kopiuj arkusz programu Excel z jednego skoroszytu do drugiego za pomocą Aspose.Cells dla .NET.
type: docs
weight: 10
url: /pl/net/excel-copy-worksheet/excel-copy-worksheet-from-other-workbook/
---
W tym samouczku przeprowadzimy Cię przez proces kopiowania arkusza programu Excel z innego skoroszytu przy użyciu biblioteki Aspose.Cells dla platformy .NET. Aby ukończyć to zadanie, postępuj zgodnie z poniższymi instrukcjami.

## Krok 1: Przygotowanie

Zanim zaczniesz, upewnij się, że zainstalowałeś Aspose.Cells dla .NET i utworzyłeś projekt C# w preferowanym zintegrowanym środowisku programistycznym (IDE).

## Krok 2: Ustaw ścieżkę katalogu dokumentów

 Zadeklaruj`dataDir` zmienną i zainicjuj ją ścieżką do katalogu dokumentów. Na przykład :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Pamiętaj o wymianie`"YOUR_DOCUMENTS_DIRECTORY"` z rzeczywistą ścieżką do katalogu.

## Krok 3: Utwórz nowy skoroszyt programu Excel

 Użyj`Workbook` class z Aspose.Cells, aby utworzyć nowy skoroszyt programu Excel:

```csharp
Workbook excelWorkbook0 = new Workbook();
```

## Krok 4: Pobierz pierwszy arkusz w skoroszycie

Przejdź do pierwszego arkusza w skoroszycie, używając indeksu 0:

```csharp
Worksheet ws0 = excelWorkbook0.Worksheets[0];
```

## Krok 5: Dodaj dane do wierszy nagłówka (A1:A4)

 Użyć`for` pętla dodająca dane do wierszy nagłówka (A1:A4):

```csharp
for (int i = 0; i < 5; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Header row {0}", i));
}
```

## Krok 6: Dodaj szczegółowe dane (A5:A999)

 Użyj innego`for` pętla do dodawania szczegółowych danych (A5:A999):

```csharp
for (int i = 5; i < 1000; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Detail row {0}", i));
}
```

## Krok 7: Ustaw opcje układu

 Ustaw opcje ustawień strony dla arkusza za pomocą`PageSetup` obiekt:

```csharp
PageSetup pagesetup = ws0.PageSetup;
pagesetup.PrintTitleRows = "$1:$5";
```

## Krok 8: Utwórz kolejny skoroszyt programu Excel

Utwórz kolejny skoroszyt programu Excel:

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## Krok 9: Pobierz pierwszy arkusz z drugiego skoroszytu

Przejdź do pierwszego arkusza w drugim skoroszycie:

```csharp
Worksheet ws1 = excelWorkbook1.Worksheets[0];
```

## Krok 10: Nazwij arkusz

nazwij ogień

wyspa obliczeniowa:

```csharp
ws1.Name = "MySheet";
```

## Krok 11: Skopiuj dane z pierwszego arkusza pierwszego skoroszytu do pierwszego arkusza drugiego skoroszytu

Skopiuj dane z pierwszego arkusza pierwszego skoroszytu do pierwszego arkusza drugiego skoroszytu:

```csharp
ws1.Copy(ws0);
```

## Krok 12: Zapisz plik Excel

Zapisz plik Excela:

```csharp
excelWorkbook1.Save(dataDir + "CopyWorkbookSheetToOther_out.xls");
```

Pamiętaj, aby określić żądaną ścieżkę i nazwę pliku wyjściowego.

### Przykładowy kod źródłowy programu Excel Kopiuj arkusz z innego skoroszytu za pomocą Aspose.Cells dla .NET 
```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Utwórz nowy skoroszyt.
Workbook excelWorkbook0 = new Workbook();
// Zdobądź pierwszy arkusz ćwiczeń w książce.
Worksheet ws0 = excelWorkbook0.Worksheets[0];
// Umieść trochę danych w wierszach nagłówka (A1:A4)
for (int i = 0; i < 5; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Header Row {0}", i));
}
// Umieść szczegółowe dane (A5:A999)
for (int i = 5; i < 1000; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Detail Row {0}", i));
}
// Zdefiniuj obiekt pagesetup na podstawie pierwszego arkusza.
PageSetup pagesetup = ws0.PageSetup;
// Na każdej stronie powtarza się pierwsze pięć wierszy...
// Można to zobaczyć w podglądzie wydruku.
pagesetup.PrintTitleRows = "$1:$5";
// Utwórz kolejny skoroszyt.
Workbook excelWorkbook1 = new Workbook();
// Zdobądź pierwszy arkusz ćwiczeń w książce.
Worksheet ws1 = excelWorkbook1.Worksheets[0];
// Nazwij arkusz.
ws1.Name = "MySheet";
// Skopiuj dane z pierwszego arkusza pierwszego skoroszytu do pliku
// pierwszy arkusz drugiego skoroszytu.
ws1.Copy(ws0);
// Zapisz plik Excela.
excelWorkbook1.Save(dataDir + "CopyWorksheetFromWorkbookToOther_out.xls");
```

## Wniosek

Gratulacje! Nauczyłeś się teraz, jak skopiować arkusz programu Excel z innego skoroszytu za pomocą Aspose.Cells dla .NET. Możesz użyć tej metody we własnych projektach, aby efektywnie manipulować plikami Excel.

### Często zadawane pytania

#### P. Jakie biblioteki są potrzebne do korzystania z Aspose.Cells dla .NET?

A. Aby używać Aspose.Cells dla .NET, musisz dołączyć bibliotekę Aspose.Cells do swojego projektu. Upewnij się, że poprawnie odniosłeś się do tej biblioteki w zintegrowanym środowisku programistycznym (IDE).

#### P. Czy Aspose.Cells obsługuje inne formaty plików Excel, takie jak XLSX?

A. Tak, Aspose.Cells obsługuje różne formaty plików Excel, w tym XLSX, XLS, CSV, HTML i wiele innych. Możesz manipulować tymi formatami plików, korzystając z funkcji Aspose.Cells dla .NET.

#### P. Czy mogę dostosować opcje układu podczas kopiowania arkusza?

A.  Tak, możesz dostosować opcje ustawień strony podczas kopiowania arkusza, korzystając z właściwości pliku`PageSetup` obiekt. Możesz określić nagłówki, stopki, marginesy, orientację strony itp.