---
title: Chroń komórki w arkuszu programu Excel
linktitle: Chroń komórki w arkuszu programu Excel
second_title: Aspose.Cells dla .NET API odniesienia
description: Dowiedz się, jak chronić określone komórki w programie Excel za pomocą Aspose.Cells dla .NET. Samouczek krok po kroku w języku C#.
type: docs
weight: 30
url: /pl/net/protect-excel-file/protect-cells-in-excel-worksheet/
---
Microsoft Excel jest powszechnie używanym narzędziem do tworzenia arkuszy kalkulacyjnych i zarządzania nimi. Jedną z podstawowych funkcji programu Excel jest możliwość ochrony niektórych komórek w celu zachowania integralności danych. W tym samouczku poprowadzimy Cię krok po kroku, jak chronić określone komórki w arkuszu kalkulacyjnym Excel przy użyciu Aspose.Cells dla .NET. Aspose.Cells dla .NET to potężna biblioteka programistyczna, która ułatwia manipulowanie plikami Excel z dużą elastycznością i zaawansowanymi funkcjami. Postępuj zgodnie z podanymi instrukcjami, aby dowiedzieć się, jak chronić ważne komórki i zapewnić bezpieczeństwo danych.

## Krok 1: Konfigurowanie środowiska

Upewnij się, że w środowisku programistycznym zainstalowano Aspose.Cells for .NET. Pobierz bibliotekę z oficjalnej strony Aspose i sprawdź dokumentację zawierającą instrukcje instalacji.

## Krok 2: Inicjowanie skoroszytu i arkusza kalkulacyjnego

Na początek musimy utworzyć nowy skoroszyt i uzyskać odwołanie do arkusza, w którym chcemy chronić komórki. Użyj następującego kodu:

```csharp
// Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENTS DIRECTORY";
// Utwórz katalog, jeśli jeszcze nie istnieje.
bool exists = System.IO.Directory.Exists(dataDir);
if (! exists)
     System.IO.Directory.CreateDirectory(dataDir);

// Utwórz nowy skoroszyt
Workbook workbook = new Workbook();

// Zdobądź pierwszy arkusz
Worksheet sheet = workbook.Worksheets[0];
```

 W tym fragmencie kodu najpierw definiujemy ścieżkę do katalogu, w którym zostanie zapisany plik Excel. Następnie tworzymy nową instancję pliku`Workbook` klasę i uzyskaj odwołanie do pierwszego arkusza za pomocą metody`Worksheets` nieruchomość.

## Krok 3: Zdefiniuj styl komórki

Teraz musimy zdefiniować styl komórek, które chcemy chronić. Użyj następującego kodu:

```csharp
// Zdefiniuj obiekt stylu
Styling styling;

// Przejdź przez wszystkie kolumny w arkuszu i odblokuj je
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     leaf.Cells.Columns[(byte)i].ApplyStyle(style, new StyleFlag { Locked = true });
}
```

 W tym kodzie używamy pętli, aby przejść przez wszystkie kolumny w arkuszu i odblokować ich komórki, ustawiając styl`IsLocked` własność do`false` . Następnie korzystamy z`ApplyStyle` metoda zastosowania stylu do kolumn za pomocą`StyleFlag` flaga blokująca komórki.

## Krok 4: Chroń określone komórki

Teraz będziemy chronić konkretne komórki, które chcemy zablokować. Użyj następującego kodu:

```csharp
// Zablokuj trzy komórki: A1, B1, C1
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

 W tym kodzie styl każdej konkretnej komórki uzyskujemy za pomocą metody`GetStyle` metodę, a następnie ustawiamy`IsLocked` właściwość stylu do`true`aby zamknąć komórkę. Na koniec stosujemy zaktualizowany styl do każdej komórki za pomocą`SetStyle` metoda.

## Krok 5: Ochrona arkusza

Teraz, gdy zdefiniowaliśmy komórki do ochrony, możemy chronić sam arkusz. Użyj następującego kodu:

```csharp
// Chroń arkusz
leaf.Protect(ProtectionType.All);
```

 Ten kod używa`Protect` w tym przypadku metoda ochrony arkusza przy użyciu określonego typu ochrony`ProtectionType.All` który chroni wszystkie elementy w arkuszu.

## Krok 6: Zapisz plik Excel

Na koniec zapisujemy plik Excel z dokonanymi zmianami. Użyj następującego kodu:

```csharp
// Zapisz plik Excela
workbook.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

 W tym kodzie używamy`Save` metoda zapisania skoroszytu w określonym katalogu z rozszerzeniem`Excel97To2003` format.

### Przykładowy kod źródłowy narzędzia Protect Cells In Excel przy użyciu Aspose.Cells dla .NET 
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
wb.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

## Wniosek

Gratulacje! Nauczyłeś się, jak chronić określone komórki w arkuszu kalkulacyjnym Excel przy użyciu Aspose.Cells dla .NET. Możesz teraz zastosować tę technikę we własnych projektach i poprawić bezpieczeństwo swoich plików Excel.


### Często zadawane pytania

#### P: Dlaczego powinienem używać Aspose.Cells dla .NET do ochrony komórek w arkuszu kalkulacyjnym Excel?

Odp.: Aspose.Cells dla .NET to potężna biblioteka, która ułatwia pracę z plikami Excel. Oferuje zaawansowane funkcje ochrony komórek, odblokowywania zakresów itp.

#### P: Czy można chronić zakresy komórek zamiast pojedynczych komórek?

 Odp.: Tak, możesz zdefiniować określone zakresy komórek do ochrony za pomocą`ApplyStyle` metoda z odpowiednim`StyleFlag`.

#### P: Jak mogę otworzyć chroniony plik Excel po jego zapisaniu?

Odp.: Po otwarciu chronionego pliku Excel konieczne będzie podanie hasła określonego podczas ochrony arkusza.

#### P: Czy istnieją inne rodzaje zabezpieczeń, które mogę zastosować do arkusza kalkulacyjnego Excel?

Odp.: Tak, Aspose.Cells dla .NET obsługuje wiele rodzajów zabezpieczeń, takich jak ochrona konstrukcji, ochrona okien itp. Możesz wybrać odpowiedni rodzaj ochrony w zależności od potrzeb.