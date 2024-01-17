---
title: Edytuj zakresy w arkuszu programu Excel
linktitle: Edytuj zakresy w arkuszu programu Excel
second_title: Aspose.Cells dla .NET API odniesienia
description: Dowiedz się, jak edytować określone zakresy w arkuszu kalkulacyjnym Excel za pomocą Aspose.Cells dla .NET. Samouczek krok po kroku w języku C#.
type: docs
weight: 20
url: /pl/net/protect-excel-file/edit-ranges-in-excel-worksheet/
---
Microsoft Excel to potężne narzędzie do tworzenia arkuszy kalkulacyjnych i zarządzania nimi, oferujące wiele funkcji kontroli i zabezpieczania danych. Jedną z takich funkcji jest umożliwienie użytkownikom edytowania określonych zakresów w arkuszu przy jednoczesnej ochronie innych części. W tym samouczku poprowadzimy Cię krok po kroku, jak wdrożyć tę funkcjonalność przy użyciu Aspose.Cells dla .NET, popularnej biblioteki do programowej pracy z plikami Excel.

Korzystanie z Aspose.Cells dla .NET pozwoli Ci z łatwością manipulować zakresami w arkuszu kalkulacyjnym Excel, zapewniając przyjazny dla użytkownika interfejs i zaawansowane funkcje. Wykonaj poniższe kroki, aby umożliwić użytkownikom edycję określonych zakresów w arkuszu kalkulacyjnym Excel przy użyciu Aspose.Cells dla .NET.
## Krok 1: Konfigurowanie środowiska

Upewnij się, że w środowisku programistycznym zainstalowano Aspose.Cells for .NET. Pobierz bibliotekę z oficjalnej strony Aspose i sprawdź dokumentację zawierającą instrukcje instalacji.

## Krok 2: Inicjowanie skoroszytu i arkusza kalkulacyjnego

Na początek musimy utworzyć nowy skoroszyt i uzyskać odwołanie do arkusza, w którym chcemy zezwolić na zmianę zakresów. Aby to osiągnąć, użyj poniższego kodu:

```csharp
// Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENTS DIRECTORY";
// Utwórz katalog, jeśli jeszcze nie istnieje.
bool exists = System.IO.Directory.Exists(dataDir);
if (! exists)
     System.IO.Directory.CreateDirectory(dataDir);

// Utwórz wystąpienie nowego skoroszytu
Workbook workbook = new Workbook();

// Pobierz pierwszy arkusz (domyślnie)
Worksheet sheet = workbook.Worksheets[0];
```

 W tym fragmencie kodu najpierw definiujemy ścieżkę do katalogu, w którym zostanie zapisany plik Excel. Następnie tworzymy nową instancję pliku`Workbook` klasę i uzyskaj odwołanie do pierwszego arkusza za pomocą metody`Worksheets` nieruchomość.

## Krok 3: Uzyskaj edytowalne zakresy

Teraz musimy pobrać zakresy, w których chcemy zezwolić na modyfikację. Użyj następującego kodu:

```csharp
// Uzyskaj modyfikowalne zakresy
ProtectedRangeCollection EditableRanges = Sheet.AllowEditRanges;
```

## Krok 4: Ustaw chroniony zakres

Zanim umożliwimy modyfikację zakresów, musimy zdefiniować zakres chroniony. Oto jak:

```csharp
// Zdefiniuj chroniony zakres
ProtectedRange ProtectedRange;

// Utwórz zakres
int index = ModifiableRanges.Add("r2", 1, 1, 3, 3);
rangeProtected = rangesEditable[index];
```

 W tym kodzie tworzymy nową instancję klasy`ProtectedRange` klasę i użyj`Add` metoda określania zakresu do ochrony.

## Krok 5: Podaj hasło

Aby zwiększyć bezpieczeństwo, możesz określić hasło dla chronionego zakresu. Oto jak:

```csharp
// Określ hasło
protectedBeach.Password = "YOUR_PASSWORD";
```

## Krok 6: Chroń arkusz

Teraz, gdy ustawiliśmy chroniony zakres, możemy zabezpieczyć arkusz, aby zapobiec nieautoryzowanym modyfikacjom. Użyj następującego kodu:

```csharp
// Chroń arkusz
leaf.Protect(ProtectionType.All);
```

## Krok 7: Zapisz plik Excel

Na koniec zapisujemy plik Excel z dokonanymi zmianami. Oto niezbędny kod:

```csharp
// Zapisz plik Excela
workbook.Save(dataDir + "protectedrange.out.xls");
```

### Przykładowy kod źródłowy edycji zakresów w arkuszu programu Excel przy użyciu Aspose.Cells dla .NET 
```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Utwórz katalog, jeśli jeszcze nie istnieje.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);

// Utwórz wystąpienie nowego skoroszytu
Workbook book = new Workbook();

// Pobierz pierwszy (domyślny) arkusz
Worksheet sheet = book.Worksheets[0];

// Uzyskaj Zezwalaj na zakresy edycji
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;

// Zdefiniuj chroniony zakres
ProtectedRange proteced_range;

// Utwórz zakres
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
proteced_range = allowRanges[idx];

// Określ hasło
proteced_range.Password = "YOUR_PASSWORD";

// Chroń prześcieradło
sheet.Protect(ProtectionType.All);

// Zapisz plik Excela
book.Save(dataDir + "protectedrange.out.xls");
```

## Wniosek

Gratulacje! Nauczyłeś się, jak pozwolić użytkownikom na edycję określonych zakresów w arkuszu kalkulacyjnym Excel przy użyciu Aspose.Cells dla .NET. Możesz teraz zastosować tę technikę we własnych projektach i poprawić bezpieczeństwo swoich plików Excel.


#### Często zadawane pytania

#### P: Dlaczego powinienem używać Aspose.Cells dla .NET do edycji zakresów w arkuszu kalkulacyjnym Excel?

Odp.: Aspose.Cells dla .NET oferuje potężne i łatwe w użyciu API do pracy z plikami Excel. Zapewnia zaawansowane funkcje, takie jak manipulacja zakresami, ochrona arkusza itp.

#### P: Czy mogę ustawić wiele edytowalnych zakresów w arkuszu?

 O: Tak, możesz zdefiniować wiele edytowalnych zakresów za pomocą`Add` metoda`ProtectedRangeCollection` kolekcja. Każdy zakres może mieć własne ustawienia zabezpieczeń.

####  P: Czy można usunąć zakres edytowalny po jego zdefiniowaniu?

 Odp.: Tak, możesz użyć`RemoveAt` metoda`ProtectedRangeCollection` kolekcja, aby usunąć określony zakres edytowalny, określając jego indeks.

#### P: Jak mogę otworzyć chroniony plik Excel po jego zapisaniu?

Odp.: Aby otworzyć chroniony plik Excel, konieczne będzie podanie hasła określonego podczas tworzenia chronionego zakresu. Pamiętaj, aby zachować hasło w bezpiecznym miejscu, aby zapobiec utracie dostępu do danych.