---
title: Wstaw obraz w stopce nagłówka
linktitle: Wstaw obraz w stopce nagłówka
second_title: Aspose.Cells dla .NET API odniesienia
description: Dowiedz się, jak wstawić obraz do nagłówka lub stopki dokumentu Excel przy użyciu Aspose.Cells dla .NET. Przewodnik krok po kroku z kodem źródłowym w języku C#.
type: docs
weight: 60
url: /pl/net/excel-page-setup/insert-image-in-header-footer/
---
Możliwość wstawienia obrazu w nagłówku lub stopce dokumentu Excel może być bardzo przydatna przy dostosowywaniu raportów lub dodawaniu logo firmy. W tym artykule poprowadzimy Cię krok po kroku, jak wstawić obraz w nagłówku lub stopce dokumentu Excel za pomocą Aspose.Cells dla .NET. Dowiesz się, jak to osiągnąć, korzystając z kodu źródłowego C#.

## Krok 1: Konfigurowanie środowiska

Zanim zaczniesz, upewnij się, że masz zainstalowany Aspose.Cells for .NET na swoim komputerze. Utwórz także nowy projekt w preferowanym środowisku programistycznym.

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

## Krok 5: Zapisywanie adresu URL obrazu

Zdefiniuj adres URL lub ścieżkę obrazu, który chcesz wstawić w nagłówku lub stopce. Użyj poniższego kodu, aby zapisać adres URL obrazu:

```csharp
string logo_url = dataDir + "aspose-logo.jpg";
```

Upewnij się, że określona ścieżka jest poprawna i obraz istnieje w tej lokalizacji.

## Krok 6: Otwieranie pliku obrazu

Aby otworzyć plik obrazu, użyjemy obiektu FileStream i odczytamy dane binarne z obrazu. Oto odpowiedni kod:

```csharp
FileStream inFile;
byte[] binaryData;

inFile = new System.IO.FileStream(logo_url, System.IO.FileMode.Open, System.IO.FileAccess.Read);
binaryData = new Byte[inFile.Length];
long bytesRead = inFile.Read(binaryData, 0, (int)inFile.Length);
```

Upewnij się, że ścieżka obrazu jest poprawna i masz odpowiednie uprawnienia dostępu do niego.

## Krok 7: Konfiguracja PageSetup

Obiekt PageSetup służy do ustawiania ustawień strony dokumentu Excel, w tym nagłówka i stopki. Użyj poniższego kodu, aby uzyskać obiekt PageSetup z pierwszego arkusza:

```csharp
PageSetup pageSetup = workbook. Worksheets

[0].PageSetup;
```

Umożliwi to dostęp do ustawień strony pierwszego arkusza w skoroszycie.

## Krok 8: Dodanie obrazu do nagłówka

Użyj metody SetHeaderPicture() obiektu PageSetup, aby ustawić obraz w środkowej części nagłówka strony. Oto odpowiedni kod:

```csharp
pageSetup.SetHeaderPicture(1, binaryData);
```

Spowoduje to dodanie określonego obrazu do nagłówka strony.

## Krok 9: Dodanie skryptu do nagłówka

Aby dodać skrypt do nagłówka strony, użyj metody SetHeader() obiektu PageSetup. Oto odpowiedni kod:

```csharp
pageSetup.SetHeader(1, "&G");
```

Spowoduje to dodanie określonego skryptu do nagłówka strony. W tym przykładzie skrypt „&G” wyświetla numer strony.

## Krok 10: Dodaj nazwę arkusza do nagłówka

Aby wyświetlić nazwę arkusza w nagłówku strony, użyj ponownie metody SetHeader() obiektu PageSetup. Oto odpowiedni kod:

```csharp
pageSetup.SetHeader(2, "&A");
```

Spowoduje to dodanie nazwy arkusza do nagłówka strony. Do przedstawienia nazwy arkusza używany jest skrypt „&A”.

## Krok 11: Zapisywanie skoroszytu

Aby zapisać zmiany w skoroszycie, użyj metody Save() obiektu Workbook. Oto odpowiedni kod:

```csharp
workbook.Save(dataDir + "InsertImageInHeaderFooter_out.xls");
```

Spowoduje to zapisanie skoroszytu ze zmianami w określonym katalogu.

## Krok 12: Zamykanie strumienia plików

Po odczytaniu danych binarnych z obrazu pamiętaj o zamknięciu FileStream, aby zwolnić zasoby. Użyj poniższego kodu, aby zamknąć FileStream:

```csharp
inFile.Close();
```

Pamiętaj, aby zawsze zamykać FileStreams po zakończeniu ich używania.

### Przykładowy kod źródłowy dla Wstaw obraz w stopce nagłówka przy użyciu Aspose.Cells dla .NET 
```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENT DIRECTORY";
//Tworzenie obiektu skoroszytu
Workbook workbook = new Workbook();
// Tworzenie zmiennej łańcuchowej do przechowywania adresu URL logo/zdjęcia
string logo_url = dataDir + "aspose-logo.jpg";
// Deklarowanie obiektu FileStream
FileStream inFile;
// Deklarowanie tablicy bajtów
byte[] binaryData;
// Utworzenie instancji obiektu FileStream w celu otwarcia logo/obrazka w strumieniu
inFile = new System.IO.FileStream(logo_url, System.IO.FileMode.Open, System.IO.FileAccess.Read);
// Tworzenie instancji tablicy bajtów rozmiaru obiektu FileStream
binaryData = new Byte[inFile.Length];
// Odczytuje blok bajtów ze strumienia i zapisuje dane w danym buforze tablicy bajtów.
long bytesRead = inFile.Read(binaryData, 0, (int)inFile.Length);
// Tworzenie obiektu PageSetup w celu pobrania ustawień strony pierwszego arkusza skoroszytu
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Ustawienie logo/obrazka w środkowej części nagłówka strony
pageSetup.SetHeaderPicture(1, binaryData);
// Ustawianie skryptu dla logo/zdjęcia
pageSetup.SetHeader(1, "&G");
// Ustawienie nazwy arkusza w prawej części nagłówka strony ze skryptem
pageSetup.SetHeader(2, "&A");
// Zapisywanie skoroszytu
workbook.Save(dataDir + "InsertImageInHeaderFooter_out.xls");
//Zamknięcie obiektu FileStream
inFile.Close();       
```
## Wniosek

Gratulacje! Teraz wiesz, jak wstawić obraz w nagłówku lub stopce dokumentu Excel przy użyciu Aspose.Cells dla .NET. Ten samouczek przeprowadził Cię przez każdy etap procesu, od skonfigurowania środowiska po zapisanie zmodyfikowanego skoroszytu. Możesz swobodnie eksperymentować z funkcjami Aspose.Cells, aby tworzyć spersonalizowane i profesjonalne dokumenty Excel.

### Często zadawane pytania

#### P1: Czy można wstawić wiele obrazów w nagłówku lub stopce dokumentu Excel?

O1: Tak, możesz wstawić wiele obrazów do nagłówka lub stopki dokumentu Excel, powtarzając kroki 8 i 9 dla każdego dodatkowego obrazu.

#### P2: Jakie formaty obrazów są obsługiwane podczas wstawiania w nagłówku lub stopce?
O2: Aspose.Cells obsługuje wiele popularnych formatów obrazów, takich jak JPEG, PNG, GIF, BMP itp.

#### P3: Czy mogę dodatkowo dostosować wygląd nagłówka lub stopki?

O3: Tak, możesz użyć specjalnych skryptów i kodów w celu dalszego formatowania i dostosowania wyglądu nagłówka lub stopki. Więcej informacji na temat opcji dostosowywania można znaleźć w dokumentacji Aspose.Cells.

#### P4: Czy Aspose.Cells współpracuje z różnymi wersjami programu Excel?

O4: Tak, Aspose.Cells jest kompatybilny z różnymi wersjami programu Excel, w tym Excel 2003, Excel 2007, Excel 2010, Excel 2013, Excel 2016 i Excel 2019.

#### P5: Czy można wstawiać obrazy w innych częściach dokumentu Excel, takich jak komórki lub wykresy?

O5: Tak, Aspose.Cells zapewnia rozbudowaną funkcjonalność wstawiania obrazów do różnych części dokumentu Excel, w tym do komórek, wykresów i obiektów rysunkowych.