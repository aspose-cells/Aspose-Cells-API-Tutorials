---
title: Obsługa podpisów Xades
linktitle: Obsługa podpisów Xades
second_title: Aspose.Cells dla .NET API odniesienia
description: Dowiedz się, jak dodać podpis Xades do pliku Excel przy użyciu Aspose.Cells dla .NET.
type: docs
weight: 190
url: /pl/net/excel-workbook/xades-signature-support/
---
tym artykule poprowadzimy Cię krok po kroku do wyjaśnienia poniższego kodu źródłowego C#, który dotyczy obsługi podpisów Xades przy użyciu biblioteki Aspose.Cells dla .NET. Dowiesz się jak wykorzystać tę bibliotekę do dodania podpisu cyfrowego Xades do pliku Excel. Przedstawimy Państwu także przebieg procesu podpisywania umowy i jego przebieg. Aby uzyskać jednoznaczne wyniki, wykonaj poniższe czynności.

## Krok 1: Zdefiniuj katalogi źródłowe i wyjściowe
Na początek musimy zdefiniować katalogi źródłowe i wyjściowe w naszym kodzie. Katalogi te wskazują, gdzie znajdują się pliki źródłowe i gdzie zostanie zapisany plik wyjściowy. Oto odpowiedni kod:

```csharp
// Katalog źródłowy
string sourceDir = RunExamples.Get_SourceDirectory();
// Katalog wyjściowy
string outputDir = RunExamples.Get_OutputDirectory();
```

Pamiętaj, aby dostosować ścieżki katalogów zgodnie z potrzebami.

## Krok 2: Ładowanie skoroszytu programu Excel
Kolejnym krokiem jest wczytanie skoroszytu Excela, w którym chcemy dodać podpis cyfrowy Xades. Oto kod ładujący skoroszyt:

```csharp
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
```

Upewnij się, że nazwa pliku źródłowego została poprawnie określona w kodzie.

## Krok 3: Konfiguracja podpisu cyfrowego
Teraz skonfigurujemy podpis cyfrowy Xades, podając niezbędne informacje. Musimy określić plik PFX zawierający certyfikat cyfrowy, a także powiązane hasło. Oto odpowiedni kod:

```csharp
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
```

Pamiętaj, aby zastąpić „pfxPassword” rzeczywistym hasłem, a „pfxFile” ścieżką do pliku PFX.

## Krok 4: Dodanie podpisu cyfrowego
Teraz, gdy skonfigurowaliśmy podpis cyfrowy, możemy dodać go do skoroszytu programu Excel. Oto odpowiedni kod:

```csharp
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
```

Ten krok dodaje podpis cyfrowy Xades do skoroszytu programu Excel.

## Krok 5: Zapisywanie skoroszytu z podpisem
Na koniec zapisujemy skoroszyt programu Excel z dodanym podpisem cyfrowym. Oto odpowiedni kod:

```csharp
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
```

Pamiętaj, aby dostosować nazwę pliku wyjściowego do swoich potrzeb.

### Przykładowy kod źródłowy obsługi podpisów Xades przy użyciu Aspose.Cells dla .NET 
```csharp
//Katalog źródłowy
string sourceDir = RunExamples.Get_SourceDirectory();
//Katalog wyjściowy
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
Console.WriteLine("XAdESSignatureSupport executed successfully.");
```

## Wniosek
Gratulacje! Nauczyłeś się, jak używać biblioteki Aspose.Cells dla .NET, aby dodać podpis cyfrowy Xades do pliku Excel. Wykonując kroki opisane w tym artykule, będziesz mógł zaimplementować tę funkcjonalność we własnych projektach. Zachęcamy do dalszego eksperymentowania z biblioteką i odkrywania innych zaawansowanych funkcji, które oferuje.

### Często zadawane pytania

#### P: Co to jest Xades?

Odp.: Xades to zaawansowany standard podpisu elektronicznego stosowany w celu zapewnienia integralności i autentyczności dokumentów cyfrowych.

#### P: Czy mogę używać innych typów podpisów cyfrowych w Aspose.Cells?

O: Tak, Aspose.Cells obsługuje także inne typy podpisów cyfrowych, takie jak podpisy XMLDSig i podpisy PKCS#7.

#### P: Czy mogę zastosować podpis do innych typów plików niż pliki Excel?
 
Odp.: Tak, Aspose.Cells umożliwia także stosowanie podpisów cyfrowych do innych obsługiwanych typów plików, takich jak pliki Word, PDF i PowerPoint.