---
title: Zarządzaj rozmiarem papieru programu Excel
linktitle: Zarządzaj rozmiarem papieru programu Excel
second_title: Aspose.Cells dla .NET API odniesienia
description: Dowiedz się, jak zarządzać rozmiarem papieru w programie Excel za pomocą Aspose.Cells dla .NET. Samouczek krok po kroku z kodem źródłowym w języku C#.
type: docs
weight: 70
url: /pl/net/excel-page-setup/manage-excel-paper-size/
---
tym samouczku poprowadzimy Cię krok po kroku, jak zarządzać rozmiarem papieru w dokumencie Excel za pomocą Aspose.Cells dla .NET. Pokażemy Ci, jak skonfigurować rozmiar papieru przy użyciu kodu źródłowego C#.

## Krok 1: Konfigurowanie środowiska

Upewnij się, że masz zainstalowany Aspose.Cells for .NET na swoim komputerze. Utwórz także nowy projekt w preferowanym środowisku programistycznym.

## Krok 2: Zaimportuj niezbędne biblioteki

W pliku kodu zaimportuj biblioteki potrzebne do pracy z Aspose.Cells. Oto odpowiedni kod:

```csharp
using Aspose.Cells;
```

## Krok 3: Ustaw katalog dokumentów

Ustaw katalog, w którym znajduje się dokument Excel, z którym chcesz pracować. Użyj poniższego kodu, aby ustawić katalog:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

Pamiętaj, aby podać pełną ścieżkę katalogu.

## Krok 4: Tworzenie obiektu skoroszytu

Obiekt Workbook reprezentuje dokument Excel, z którym będziesz pracować. Możesz go utworzyć za pomocą następującego kodu:

```csharp
Workbook workbook = new Workbook();
```

Spowoduje to utworzenie nowego, pustego obiektu skoroszytu.

## Krok 5: Dostęp do pierwszego arkusza

Aby uzyskać dostęp do pierwszego arkusza kalkulacyjnego dokumentu Excel, użyj następującego kodu:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

Umożliwi to pracę z pierwszym arkuszem w skoroszycie.

## Krok 6: Konfiguracja rozmiaru papieru

Użyj właściwości PageSetup.PaperSize obiektu Worksheet, aby ustawić rozmiar papieru. W tym przykładzie ustawimy rozmiar papieru na A4. Oto odpowiedni kod:

```csharp
worksheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
```

Spowoduje to ustawienie rozmiaru papieru arkusza kalkulacyjnego na A4.

## Krok 7: Zapisywanie skoroszytu

Aby zapisać zmiany w skoroszycie, użyj metody Save() obiektu Workbook. Oto odpowiedni kod:

```csharp
workbook.Save(dataDir + "ManagePaperSize_out.xls");
```

Spowoduje to zapisanie skoroszytu ze zmianami w określonym katalogu.

### Przykładowy kod źródłowy do zarządzania rozmiarem papieru programu Excel przy użyciu Aspose.Cells dla .NET 
```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Tworzenie instancji obiektu skoroszytu
Workbook workbook = new Workbook();
// Dostęp do pierwszego arkusza w pliku Excel
Worksheet worksheet = workbook.Worksheets[0];
// Ustawianie rozmiaru papieru na A4
worksheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
// Zapisz skoroszyt.
workbook.Save(dataDir + "ManagePaperSize_out.xls");
```
## Wniosek

Nauczyłeś się teraz, jak zarządzać rozmiarem papieru w dokumencie Excel za pomocą Aspose.Cells dla .NET. Ten samouczek przeprowadził Cię przez każdy etap procesu, od konfiguracji środowiska po zapisanie zmian. Możesz teraz wykorzystać tę wiedzę, aby dostosować rozmiar papieru dokumentów Excel.

### Często zadawane pytania

#### P1: Czy mogę ustawić niestandardowy rozmiar papieru inny niż A4?

Odpowiedź 1: Tak, Aspose.Cells obsługuje wiele predefiniowanych rozmiarów papieru, a także możliwość ustawienia niestandardowego rozmiaru papieru poprzez określenie żądanych wymiarów.

#### P2: Jak mogę sprawdzić bieżący rozmiar papieru w dokumencie Excel?

 Odpowiedź 2: Możesz użyć`PageSetup.PaperSize` własność`Worksheet` obiekt, aby uzyskać aktualnie ustawiony rozmiar papieru.

#### P3: Czy można ustawić dodatkowe marginesy strony w zależności od rozmiaru papieru?

 A3: Tak, możesz użyć`PageSetup.LeftMargin`, `PageSetup.RightMargin`, `PageSetup.TopMargin` I`PageSetup.BottomMargin` właściwości, aby ustawić dodatkowe marginesy strony poza rozmiarem papieru.

#### P4: Czy ta metoda działa w przypadku wszystkich formatów plików Excel, takich jak .xls i .xlsx?

O4: Tak, ta metoda działa zarówno w przypadku plików w formacie .xls, jak i .xlsx.

#### P5: Czy mogę zastosować różne rozmiary papieru do różnych arkuszy w tym samym skoroszycie?

 O5: Tak, możesz zastosować różne rozmiary papieru do różnych arkuszy w tym samym skoroszycie, korzystając z opcji`PageSetup.PaperSize` właściwość każdego arkusza.