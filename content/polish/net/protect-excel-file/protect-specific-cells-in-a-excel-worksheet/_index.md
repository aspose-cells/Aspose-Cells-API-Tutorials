---
title: Chroń określone komórki w arkuszu programu Excel
linktitle: Chroń określone komórki w arkuszu programu Excel
second_title: Aspose.Cells dla .NET API odniesienia
description: Dowiedz się, jak chronić określone komórki w programie Excel za pomocą Aspose.Cells dla .NET. Samouczek krok po kroku w języku C#.
type: docs
weight: 70
url: /pl/net/protect-excel-file/protect-specific-cells-in-a-excel-worksheet/
---
W tym samouczku przyjrzymy się kodowi źródłowemu C#, który używa biblioteki Aspose.Cells do ochrony określonych komórek w arkuszu kalkulacyjnym Excel. Przejdziemy przez każdy krok kodu i wyjaśnimy, jak to działa. Postępuj zgodnie z instrukcjami, aby uzyskać pożądane rezultaty.

## Krok 1: Warunki wstępne

Zanim zaczniesz, upewnij się, że zainstalowałeś bibliotekę Aspose.Cells dla .NET. Można go pobrać z oficjalnej strony Aspose. Upewnij się także, że masz najnowszą wersję programu Visual Studio lub innego środowiska programistycznego C#.

## Krok 2: Zaimportuj wymagane przestrzenie nazw

Aby skorzystać z biblioteki Aspose.Cells, musimy zaimportować do naszego kodu niezbędne przestrzenie nazw. Dodaj następujące wiersze na górze pliku źródłowego C#:

```csharp
using Aspose.Cells;
```

## Krok 3: Tworzenie skoroszytu programu Excel

W tym kroku utworzymy nowy skoroszyt programu Excel. Użyj poniższego kodu, aby utworzyć skoroszyt programu Excel:

```csharp
// Ścieżka do katalogu dokumentów.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Utwórz nowy skoroszyt.
Workbook wb = new Workbook();
```

 Pamiętaj o wymianie`"YOUR_DOCUMENTS_DIR"` z odpowiednią ścieżką do katalogu dokumentów.

## Krok 4: Tworzenie arkusza kalkulacyjnego

Teraz, gdy utworzyliśmy skoroszyt programu Excel, utwórzmy arkusz i zdobądźmy pierwszy arkusz. Użyj następującego kodu:

```csharp
// Utwórz obiekt arkusza kalkulacyjnego i uzyskaj pierwszy arkusz.
Worksheet sheet = wb.Worksheets[0];
```

## Krok 5: Definiowanie stylu

W tym kroku zdefiniujemy styl, który ma zostać zastosowany do określonych komórek. Użyj następującego kodu:

```csharp
// Definicja obiektu stylu.
Styling styling;
```

## Krok 6: Pętla odblokowująca wszystkie kolumny

Teraz przejdziemy przez wszystkie kolumny w arkuszu i odblokujemy je. Użyj następującego kodu:

```csharp
// Przejdź przez wszystkie kolumny w arkuszu i odblokuj je.
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style);
}
```

## Krok 7: Blokowanie określonych komórek

Na tym etapie zablokujemy określone komórki. Użyj następującego kodu:

```csharp
//Blokowanie wszystkich trzech komórek... tj. A1, B1, C1.
style = sheet.Cells["A1"].GetStyle();
style. IsLocked = true;
sheet.Cells["A1"].SetStyle(style);

style = sheet.Cells["B1"].GetStyle();
style. IsLocked = true;
sheet.Cells["B1"].SetStyle(style);

style = sheet.Cells["C1"].GetStyle();
style. IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
```

## Krok 8: Ochrona arkusza

Na koniec zabezpieczymy arkusz, aby zapobiec modyfikacji określonych komórek. Użyj następującego kodu:

```csharp
// Chroń arkusz.
sheet.Protect(ProtectionType.All);
```

## Krok 9: Zapisywanie pliku Excel

Zapiszemy teraz zmodyfikowany plik Excel. Użyj następującego kodu:

```csharp
// Zapisz plik Excela.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Upewnij się, że podałeś poprawną ścieżkę do zapisania zmodyfikowanego pliku Excel.

### Przykładowy kod źródłowy funkcji Chroń określone komórki w arkuszu programu Excel przy użyciu Aspose.Cells dla platformy .NET 
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
// Zdefiniuj obiekt styleflag
StyleFlag styleflag;
// Przejdź przez wszystkie kolumny w arkuszu i odblokuj je.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    styleflag = new StyleFlag();
    styleflag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, styleflag);
}
// Zablokuj trzy komórki...tj. A1, B1, C1.
style = sheet.Cells["A1"].GetStyle();
style.IsLocked = true;
sheet.Cells["A1"].SetStyle(style);
style = sheet.Cells["B1"].GetStyle();
style.IsLocked = true;
sheet.Cells["B1"].SetStyle(style);
style = sheet.Cells["C1"].GetStyle();
style.IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
// Wreszcie, chroń arkusz teraz.
sheet.Protect(ProtectionType.All);
// Zapisz plik Excela.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```


## Wniosek

Gratulacje! Masz teraz kod źródłowy języka C#, który umożliwia ochronę określonych komórek w arkuszu programu Excel przy użyciu biblioteki Aspose.Cells dla platformy .NET. Zachęcamy do dostosowania kodu do własnych potrzeb.

### Często zadawane pytania (często zadawane pytania)

#### Czy ten kod działa z najnowszymi wersjami programu Excel?

Tak, ten kod działa z najnowszymi wersjami programu Excel, w tym z plikami w formacie Excel 2010 i nowszym.

#### Czy mogę chronić inne komórki oprócz A1, B1 i C1?

Tak, możesz zmodyfikować kod, aby zablokować inne określone komórki, dostosowując odniesienia do komórek w odpowiednich wierszach kodu.

#### Jak mogę ponownie odblokować zablokowane komórki?

 Możesz użyć`SetStyle` metoda z`IsLocked` Ustawić`false` aby odblokować komórki.

#### Czy mogę dodać więcej arkuszy do skoroszytu?

 Tak, możesz dodać inne arkusze do skoroszytu za pomocą`Worksheets.Add()`metodę i powtórz kroki ochrony komórek dla każdego arkusza.

#### Jak mogę zmienić format zapisu pliku Excel?

 Możesz zmienić format zapisu za pomocą`SaveFormat` metodę o żądanym formacie, na przykład`SaveFormat.Xlsx` dla programu Excel 2007 i nowszych wersji.