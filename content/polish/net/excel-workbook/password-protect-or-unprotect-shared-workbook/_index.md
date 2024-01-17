---
title: Chroń hasłem lub nie chroń udostępnionego skoroszytu
linktitle: Chroń hasłem lub nie chroń udostępnionego skoroszytu
second_title: Aspose.Cells dla .NET API odniesienia
description: Dowiedz się, jak zabezpieczyć hasłem lub wyłączyć ochronę udostępnionego skoroszytu za pomocą Aspose.Cells dla .NET.
type: docs
weight: 120
url: /pl/net/excel-workbook/password-protect-or-unprotect-shared-workbook/
---
Ochrona udostępnionego skoroszytu hasłem jest ważna dla zapewnienia prywatności danych. Dzięki Aspose.Cells dla .NET możesz łatwo chronić lub usuwać ochronę udostępnionego skoroszytu za pomocą haseł. Wykonaj poniższe kroki, aby uzyskać pożądane rezultaty:

## Krok 1: Określ katalog wyjściowy

Najpierw musisz określić katalog wyjściowy, w którym zostanie zapisany chroniony plik Excel. Oto jak to zrobić za pomocą Aspose.Cells:

```csharp
// Katalog wyjściowy
string outputDir = RunExamples.Get_OutputDirectory();
```

## Krok 2: Utwórz pusty plik Excel

Następnie możesz utworzyć pusty plik Excel, na którym chcesz zastosować ochronę lub brak ochrony. Oto przykładowy kod:

```csharp
// Utwórz pusty skoroszyt programu Excel
Workbook wb = new Workbook();
```

## Krok 3: Chroń lub wyłącz ochronę udostępnionego skoroszytu

Po utworzeniu skoroszytu możesz chronić lub wyłączyć ochronę udostępnionego skoroszytu, podając odpowiednie hasło. Oto jak:

```csharp
// Chroń udostępniony skoroszyt hasłem
wb.ProtectSharedWorkbook("1234");

// Odkomentuj tę linię, aby wyłączyć ochronę udostępnionego skoroszytu
// wb.UnprotectSharedWorkbook("1234");
```

## Krok 4: Zapisz wyjściowy plik Excel

Po zastosowaniu ochrony lub braku ochrony możesz zapisać chroniony plik Excel w określonym katalogu wyjściowym. Oto jak to zrobić:

```csharp
// Zapisz wyjściowy plik Excel
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

### Przykładowy kod źródłowy dla ochrony hasłem lub niechronienia udostępnionego skoroszytu przy użyciu Aspose.Cells dla .NET 
```csharp
//Katalog wyjściowy
string outputDir = RunExamples.Get_OutputDirectory();
//Utwórz pusty plik Excel
Workbook wb = new Workbook();
//Chroń udostępniony skoroszyt hasłem
wb.ProtectSharedWorkbook("1234");
//Odkomentuj ten wiersz, aby wyłączyć ochronę udostępnionego skoroszytu
//wb.UnprotectSharedWorkbook("1234");
//Zapisz wyjściowy plik Excel
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

## Wniosek

Ochrona lub dezaktywacja udostępnionego skoroszytu hasłem jest niezbędna do zapewnienia bezpieczeństwa danych. Dzięki Aspose.Cells dla .NET możesz łatwo dodać tę funkcjonalność do swoich plików Excel. Wykonując czynności opisane w tym przewodniku, możesz skutecznie chronić lub wyłączać ochronę udostępnionych skoroszytów za pomocą haseł. Eksperymentuj z własnymi plikami Excel i pamiętaj o bezpieczeństwie swoich wrażliwych danych.

### Często zadawane pytania

#### P: Jakie rodzaje ochrony mogę zastosować do skoroszytu udostępnionego Aspose.Cells?
    
Odp.: Dzięki Aspose.Cells możesz chronić udostępniony skoroszyt, określając hasło, aby zapobiec nieautoryzowanemu dostępowi, modyfikacji lub usunięciu danych.

#### P: Czy mogę chronić udostępniony skoroszyt bez podawania hasła?
    
Odp.: tak, możesz chronić udostępniony skoroszyt bez podawania hasła. Dla większego bezpieczeństwa zaleca się jednak użycie silnego hasła.

#### P: Jak mogę wyłączyć ochronę skoroszytu udostępnionego Aspose.Cells?
    
Odp.: Aby wyłączyć ochronę udostępnionego skoroszytu, musisz podać to samo hasło, które zostało użyte podczas ochrony skoroszytu. Umożliwia to usunięcie zabezpieczeń i swobodny dostęp do danych.

#### P: Czy ochrona udostępnionego skoroszytu wpływa na funkcje i formuły w skoroszycie?
    
Odp.: gdy chronisz udostępniony skoroszyt, użytkownicy nadal mają dostęp do funkcji i formuł znajdujących się w skoroszycie. Ochrona wpływa tylko na zmiany strukturalne w skoroszycie.