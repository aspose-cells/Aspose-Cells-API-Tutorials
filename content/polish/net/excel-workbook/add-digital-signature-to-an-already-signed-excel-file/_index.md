---
title: Dodaj podpis cyfrowy do już podpisanego pliku Excel
linktitle: Dodaj podpis cyfrowy do już podpisanego pliku Excel
second_title: Aspose.Cells dla .NET API odniesienia
description: Z łatwością dodawaj podpisy cyfrowe do istniejących plików Excel za pomocą Aspose.Cells dla .NET.
type: docs
weight: 30
url: /pl/net/excel-workbook/add-digital-signature-to-an-already-signed-excel-file/
---
W tym przewodniku krok po kroku wyjaśnimy dostarczony kod źródłowy C#, który pozwoli Ci dodać podpis cyfrowy do już podpisanego pliku Excel przy użyciu Aspose.Cells dla .NET. Wykonaj poniższe czynności, aby dodać nowy podpis cyfrowy do istniejącego pliku Excel.

## Krok 1: Ustaw katalogi źródłowe i wyjściowe

```csharp
// katalog źródłowy
string sourceDir = RunExamples.Get_SourceDirectory();

// Katalog wyjściowy
string outputDir = RunExamples.Get_OutputDirectory();
```

tym pierwszym kroku definiujemy katalogi źródłowe i wyjściowe, które zostaną użyte do załadowania istniejącego pliku Excel i zapisania pliku z nowym podpisem cyfrowym.

## Krok 2: Załaduj istniejący plik Excel

```csharp
// Załaduj już podpisany skoroszyt programu Excel
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
```

 Tutaj ładujemy już podpisany plik Excel za pomocą`Workbook` klasa Aspose.Cells.

## Krok 3: Utwórz kolekcję podpisów cyfrowych

```csharp
// Utwórz kolekcję podpisów cyfrowych
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
```

 Tworzymy nową kolekcję podpisów cyfrowych za pomocą`DigitalSignatureCollection` klasa.

## Krok 4: Utwórz nowy certyfikat

```csharp
// Utwórz nowy certyfikat
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
```

Tutaj tworzymy nowy certyfikat z podanego pliku i hasła.

## Krok 5: Dodaj nowy podpis cyfrowy do kolekcji

```csharp
// Utwórz nowy podpis cyfrowy
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added a new digital signature to the already signed workbook.", DateTime.Now);

// Dodaj podpis cyfrowy do kolekcji
dsCollection.Add(signature);
```

 Tworzymy nowy podpis cyfrowy za pomocą`DigitalSignature` class i dodaj ją do kolekcji podpisów cyfrowych.

## Krok 6: Dodaj kolekcję podpisów cyfrowych do skoroszytu

```csharp
//Dodaj kolekcję podpisów cyfrowych do skoroszytu
workbook.AddDigitalSignature(dsCollection);
```

 Do istniejącego skoroszytu programu Excel dodajemy kolekcję podpisów cyfrowych za pomocą`AddDigitalSignature()` metoda.

## Krok 7: Zapisz i zamknij skoroszyt

```csharp
// Zapisz skoroszyt i zamknij go
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
```

Zapisujemy skoroszyt z nowym podpisem cyfrowym w określonym katalogu wyjściowym, następnie zamykamy go i zwalniamy powiązane zasoby.

### Przykładowy kod źródłowy funkcji dodawania podpisu cyfrowego do już podpisanego pliku Excel przy użyciu Aspose.Cells dla platformy .NET 
```csharp
//Katalog źródłowy
string sourceDir = RunExamples.Get_SourceDirectory();
//Katalog wyjściowy
string outputDir = RunExamples.Get_OutputDirectory();
//Plik certyfikatu i jego hasło
string certFileName = sourceDir + "AsposeDemo.pfx";
string password = "aspose";
//Załaduj skoroszyt, który jest już podpisany cyfrowo, aby dodać nowy podpis cyfrowy
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
//Utwórz kolekcję podpisów cyfrowych
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
//Utwórz nowy certyfikat
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
//Utwórz nowy podpis cyfrowy i dodaj go do kolekcji podpisów cyfrowych
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added new digital signature in existing digitally signed workbook.", DateTime.Now);
dsCollection.Add(signature);
//Dodaj kolekcję podpisów cyfrowych do skoroszytu
workbook.AddDigitalSignature(dsCollection);
//Zapisz skoroszyt i usuń go.
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
Console.WriteLine("AddDigitalSignatureToAnAlreadySignedExcelFile executed successfully.\r\n");
```

## Wniosek

Gratulacje! Nauczyłeś się teraz, jak dodać podpis cyfrowy do już podpisanego pliku Excel przy użyciu Aspose.Cells dla .NET. Podpisy cyfrowe dodają dodatkową warstwę zabezpieczeń do plików Excel, zapewniając ich autentyczność i integralność.

### Często zadawane pytania

#### P: Co to jest Aspose.Cells dla .NET?

O: Aspose.Cells dla .NET to potężna biblioteka klas, która pozwala programistom .NET z łatwością tworzyć, modyfikować, konwertować i manipulować plikami Excel.

#### P: Co to jest podpis cyfrowy w pliku Excel?

Odp.: Podpis cyfrowy w pliku Excel to znak elektroniczny gwarantujący autentyczność, integralność i pochodzenie dokumentu. Służy do sprawdzenia, czy plik nie był modyfikowany od momentu podpisania i czy pochodzi z wiarygodnego źródła.

#### P: Jakie są korzyści z dodania podpisu cyfrowego do pliku Excel?

Odp.: Dodanie podpisu cyfrowego do pliku Excel zapewnia szereg korzyści, w tym ochronę przed nieautoryzowanymi zmianami, zapewnienie integralności danych, uwierzytelnienie autora dokumentu i pewność zawartych w nim informacji.

#### P: Czy mogę dodać wiele podpisów cyfrowych do pliku Excel?

O: Tak, Aspose.Cells umożliwia dodanie wielu podpisów cyfrowych do pliku Excel. Możesz utworzyć kolekcję podpisów cyfrowych i dodać je do pliku w jednej operacji.

#### P: Jakie są wymagania dotyczące dodawania podpisu cyfrowego do pliku Excel?

Odp.: Aby dodać podpis cyfrowy do pliku Excel, potrzebujesz ważnego certyfikatu cyfrowego, który będzie używany do podpisania dokumentu. Przed dodaniem podpisu cyfrowego upewnij się, że masz prawidłowy certyfikat i hasło.