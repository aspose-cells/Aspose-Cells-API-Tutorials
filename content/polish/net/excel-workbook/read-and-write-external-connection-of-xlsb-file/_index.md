---
title: Odczyt i zapis połączenia zewnętrznego pliku XLSB
linktitle: Odczyt i zapis połączenia zewnętrznego pliku XLSB
second_title: Aspose.Cells dla .NET API odniesienia
description: Dowiedz się, jak czytać i modyfikować połączenia zewnętrzne pliku XLSB przy użyciu Aspose.Cells dla .NET.
type: docs
weight: 130
url: /pl/net/excel-workbook/read-and-write-external-connection-of-xlsb-file/
---
Odczytywanie i zapisywanie połączeń zewnętrznych w pliku XLSB jest niezbędne do manipulowania danymi ze źródeł zewnętrznych w skoroszytach programu Excel. Dzięki Aspose.Cells dla .NET możesz łatwo odczytywać i zapisywać połączenia zewnętrzne, wykonując następujące kroki:

## Krok 1: Określ katalog źródłowy i katalog wyjściowy

Najpierw musisz określić katalog źródłowy, w którym znajduje się plik XLSB zawierający połączenie zewnętrzne, a także katalog wyjściowy, w którym chcesz zapisać zmodyfikowany plik. Oto jak to zrobić za pomocą Aspose.Cells:

```csharp
// katalog źródłowy
string sourceDir = RunExamples.Get_SourceDirectory();

// Katalog wyjściowy
string outputDir = RunExamples.Get_OutputDirectory();
```

## Krok 2: Załaduj źródłowy plik Excel XLSB

Następnie musisz załadować źródłowy plik Excel XLSB, na którym chcesz wykonać operacje odczytu i zapisu połączenia zewnętrznego. Oto przykładowy kod:

```csharp
// Załaduj źródłowy plik Excel XLSB
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
```

## Krok 3: Przeczytaj i zmodyfikuj połączenie zewnętrzne

Po załadowaniu pliku można uzyskać dostęp do pierwszego połączenia zewnętrznego, które w rzeczywistości jest połączeniem z bazą danych. Możesz czytać i modyfikować różne właściwości połączenia zewnętrznego. Oto jak:

```csharp
// Przeczytaj pierwsze połączenie zewnętrzne, które jest połączeniem z bazą danych
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;

// Wyświetl nazwę połączenia z bazą danych, polecenie i informacje o połączeniu
Console.WriteLine("Connection name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);

// Zmodyfikuj nazwę połączenia
dbCon.Name = "NewCustomer";
```

## Krok 4: Zapisz wyjściowy plik Excel XLSB

Po dokonaniu niezbędnych zmian możesz zapisać zmodyfikowany plik Excel XLSB w określonym katalogu wyjściowym. Oto jak to zrobić:

```csharp
// Zapisz wyjściowy plik Excel XLSB
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

### Przykładowy kod źródłowy do zewnętrznego połączenia odczytu i zapisu pliku XLSB przy użyciu Aspose.Cells dla .NET 
```csharp
//Katalog źródłowy
string sourceDir = RunExamples.Get_SourceDirectory();
//Katalog wyjściowy
string outputDir = RunExamples.Get_OutputDirectory();
//Załaduj źródłowy plik Excel Xlsb
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
//Przeczytaj pierwsze połączenie zewnętrzne, które w rzeczywistości jest połączeniem DB
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;
//Wydrukuj nazwę, polecenie i informacje o połączeniu połączenia DB
Console.WriteLine("Connection Name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);
//Zmodyfikuj nazwę połączenia
dbCon.Name = "NewCust";
//Zapisz plik Excel Xlsb
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

## Wniosek

Odczytywanie i zapisywanie połączeń zewnętrznych w pliku XLSB umożliwia manipulowanie danymi ze źródeł zewnętrznych w skoroszytach programu Excel. Dzięki Aspose.Cells dla .NET możesz łatwo uzyskać dostęp do połączeń zewnętrznych, czytać i modyfikować informacje o połączeniach oraz zapisywać zmiany. Eksperymentuj z własnymi plikami XLSB i wykorzystaj moc połączeń zewnętrznych w aplikacjach Excel.

### Często zadawane pytania

#### P: Co to jest połączenie zewnętrzne w pliku XLSB?
    
Odpowiedź: Połączenie zewnętrzne w pliku XLSB oznacza połączenie nawiązane z zewnętrznym źródłem danych, takim jak baza danych. Umożliwia import danych z tego zewnętrznego źródła do skoroszytu programu Excel.

#### P: Czy mogę mieć wiele połączeń zewnętrznych w pliku XLSB?
     
Odp.: Tak, w pliku XLSB możesz mieć wiele połączeń zewnętrznych. Można nimi zarządzać indywidualnie, uzyskując dostęp do każdego obiektu połączenia.

#### P: Jak mogę odczytać szczegóły połączenia zewnętrznego w pliku XLSB za pomocą Aspose.Cells?
     
Odp.: Możesz użyć funkcjonalności zapewnianej przez Aspose.Cells, aby uzyskać dostęp do właściwości połączenia zewnętrznego, takich jak nazwa połączenia, skojarzone polecenie i informacje o połączeniu.

#### P: Czy można modyfikować połączenie zewnętrzne w pliku XLSB za pomocą Aspose.Cells?
     
O: Tak, możesz modyfikować właściwości połączenia zewnętrznego, takie jak nazwa połączenia, aby dostosować je do swoich potrzeb. Aspose.Cells zapewnia metody wprowadzania tych zmian.

#### P: Jak mogę zapisać zmiany wprowadzone w połączeniu zewnętrznym w pliku XLSB za pomocą Aspose.Cells?
     
Odp.: Po dokonaniu niezbędnych zmian w połączeniu zewnętrznym możesz po prostu zapisać zmodyfikowany plik Excel XLSB, korzystając z odpowiedniej metody dostarczonej przez Aspose.Cells.