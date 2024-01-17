---
title: Chroń wiersz w arkuszu programu Excel
linktitle: Chroń wiersz w arkuszu programu Excel
second_title: Aspose.Cells dla .NET API odniesienia
description: W tym samouczku dowiesz się, jak chronić wiersze arkusza kalkulacyjnego Excel za pomocą Aspose.Cells dla .NET. Samouczek krok po kroku w języku C#.
type: docs
weight: 60
url: /pl/net/protect-excel-file/protect-row-in-excel-worksheet/
---
W tym samouczku przyjrzymy się kodowi źródłowemu C#, który używa biblioteki Aspose.Cells do ochrony wierszy w arkuszu kalkulacyjnym programu Excel. Przejdziemy przez każdy krok kodu i wyjaśnimy, jak to działa. Postępuj zgodnie z instrukcjami, aby uzyskać pożądane rezultaty.

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

W tym kroku zdefiniujemy styl, który zostanie zastosowany do wierszy arkusza kalkulacyjnego. Użyj następującego kodu:

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

## Krok 7: Blokowanie pierwszej linii

W tym kroku zablokujemy pierwszy wiersz arkusza. Użyj następującego kodu:

```csharp
// Zdobądź styl pierwszej linii.
style = sheet.Cells.Rows[0].Style;
// Zablokuj styl.
style. IsLocked = true;
// Zastosuj styl do pierwszej linii.
sheet.Cells.ApplyRowStyle(0, style);
```

## Krok 8: Ochrona arkusza

Teraz, gdy ustawiliśmy style i zablokowaliśmy wiersze, chrońmy arkusz kalkulacyjny. Użyj następującego kodu:

```csharp
// Chroń arkusz.
sheet.Protect(ProtectionType.All);
```

## Krok 9: Zapisywanie pliku Excel

Na koniec zapiszemy zmodyfikowany plik Excel. Użyj następującego kodu:

```csharp
// Zapisz plik Excela.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Upewnij się, że podałeś poprawną ścieżkę do zapisania zmodyfikowanego pliku Excel.

### Przykładowy kod źródłowy narzędzia Protect Row In Excel przy użyciu Aspose.Cells dla .NET 
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
// Zdefiniuj obiekt styleflag.
StyleFlag flag;
// Przejdź przez wszystkie kolumny w arkuszu i odblokuj je.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    flag = new StyleFlag();
    flag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
// Zdobądź styl pierwszego rzędu.
style = sheet.Cells.Rows[0].Style;
// Zablokuj to.
style.IsLocked = true;
//Utwórz instancję flagi.
flag = new StyleFlag();
// Ustaw ustawienie blokady.
flag.Locked = true;
// Zastosuj styl do pierwszego wiersza.
sheet.Cells.ApplyRowStyle(0, style, flag);
// Chroń prześcieradło.
sheet.Protect(ProtectionType.All);
// Zapisz plik Excela.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## Wniosek

Gratulacje! Masz teraz kod źródłowy C#, który pozwala chronić wiersze w arkuszu kalkulacyjnym Excel przy użyciu biblioteki Aspose.Cells dla .NET. Postępuj dokładnie zgodnie z instrukcjami i dostosuj kod do swoich konkretnych potrzeb.

### Często zadawane pytania (często zadawane pytania)

#### Czy ten kod działa z najnowszymi wersjami programu Excel?

Tak, ten kod działa z najnowszymi wersjami programu Excel, w tym z plikami w formacie Excel 2010 i nowszym.

#### Czy mogę chronić tylko określone wiersze zamiast wszystkich wierszy w arkuszu?

Tak, możesz zmodyfikować kod, aby określić konkretne wiersze, które chcesz chronić. Będziesz musiał odpowiednio dostosować pętlę i indeksy.

#### Jak mogę ponownie odblokować zablokowane linie?

 Możesz skorzystać z`IsLocked` metoda`Style` obiekt, dla którego chcesz ustawić wartość`false` i odblokuj rzędy.

#### Czy można chronić wiele arkuszy w tym samym skoroszycie programu Excel?

Tak, możesz powtórzyć kroki tworzenia arkusza, ustawiania stylu i ochrony każdego arkusza w skoroszycie.

#### Jak mogę zmienić hasło zabezpieczające arkusz kalkulacyjny?

 Hasło możesz zmienić za pomocą przycisku`Protect` metodę i podanie nowego hasła jako argumentu.