---
title: Określ autora podczas zabezpieczania zapisu skoroszytu programu Excel
linktitle: Określ autora podczas zabezpieczania zapisu skoroszytu programu Excel
second_title: Aspose.Cells dla .NET API odniesienia
description: Dowiedz się, jak chronić i dostosowywać skoroszyty programu Excel za pomocą Aspose.Cells dla .NET. Samouczek krok po kroku w języku C#.
type: docs
weight: 30
url: /pl/net/excel-security/specify-author-while-write-protecting-excel-workbook/
---

W tym samouczku pokażemy, jak określić autora podczas zabezpieczania skoroszytu programu Excel przed zapisem przy użyciu biblioteki Aspose.Cells dla .NET.

## Krok 1: Przygotowanie środowiska

Zanim zaczniesz, upewnij się, że masz zainstalowany Aspose.Cells for .NET na swoim komputerze. Pobierz bibliotekę z oficjalnej strony Aspose i postępuj zgodnie z dostarczonymi instrukcjami instalacji.

## Krok 2: Konfiguracja katalogów źródłowych i wyjściowych

 dostarczonym kodzie źródłowym musisz określić katalogi źródłowy i wyjściowy. Zmodyfikuj`sourceDir` I`outputDir` zmienne, zastępując „TWOJ KATALOG ŹRÓDŁOWY” i „TWOJ KATALOG WYJŚCIOWY” odpowiednimi ścieżkami bezwzględnymi na komputerze.

```csharp
// Katalog źródłowy
string sourceDir = "PATH TO YOUR SOURCE DIRECTORY";

// Katalog wyjściowy
string outputDir = "YOUR OUTPUT DIRECTORY PATH";
```

## Krok 3: Tworzenie pustego skoroszytu programu Excel

Na początek tworzymy obiekt Workbook reprezentujący pusty skoroszyt programu Excel.

```csharp
// Utwórz pusty skoroszyt.
Workbook wb = new Workbook();
```

## Krok 4: Zabezpieczenie zapisu hasłem

 Następnie określamy hasło do zapisu zabezpieczającego skoroszyt programu Excel za pomocą`WriteProtection.Password` właściwość obiektu Workbook.

```csharp
// Napisz, chroń skoroszyt hasłem.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";
```

## Krok 5: Specyfikacja autora

 Teraz określamy autora skoroszytu programu Excel za pomocą`WriteProtection.Author` właściwość obiektu Workbook.

```csharp
// Określ autora podczas zapisu skoroszytu zabezpieczającego.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";
```

## Krok 6: Chroniony kopią zapasową skoroszyt programu Excel

 Po określeniu ochrony przed zapisem i autora możemy zapisać skoroszyt programu Excel w formacie XLSX za pomocą`Save()` metoda.

```csharp
// Zapisz skoroszyt w formacie XLSX.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");
```

### Przykładowy kod źródłowy narzędzia Określ autora podczas ochrony zapisu w skoroszycie programu Excel przy użyciu Aspose.Cells dla platformy .NET 
```csharp
//Katalog źródłowy
string sourceDir = "YOUR SOURCE DIRECTORY";

//Katalog wyjściowy
string outputDir = "YOUR OUTPUT DIRECTORY";

// Utwórz pusty skoroszyt.
Workbook wb = new Workbook();

// Napisz, chroń skoroszyt hasłem.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";

// Określ autora podczas zapisu skoroszytu zabezpieczającego.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";

// Zapisz skoroszyt w formacie XLSX.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");

```

## Wniosek

Gratulacje! Nauczyłeś się teraz, jak określić autora podczas zabezpieczania skoroszytu programu Excel przed zapisem za pomocą Aspose.Cells dla .NET. Możesz zastosować te kroki do własnych projektów, aby chronić i dostosowywać skoroszyty programu Excel.

Zachęcamy do dalszego odkrywania funkcji Aspose.Cells dla .NET w celu uzyskania bardziej zaawansowanych operacji na plikach Excel.

## Często zadawane pytania

#### P: Czy mogę zapisać skoroszyt programu Excel bez podawania hasła?

 O: Tak, możesz użyć obiektu Workbook`WriteProtect()` bez podawania hasła w celu ochrony skoroszytu programu Excel przed zapisem. Spowoduje to ograniczenie zmian w skoroszycie bez konieczności podawania hasła.

#### P: Jak usunąć ochronę przed zapisem ze skoroszytu programu Excel?

 Odp.: Aby usunąć ochronę przed zapisem ze skoroszytu programu Excel, możesz użyć metody`Unprotect()` metoda obiektu Worksheet lub`RemoveWriteProtection()` metoda obiektu Workbook, w zależności od konkretnego przypadku użycia. .

#### P: Zapomniałem hasła, aby chronić skoroszyt programu Excel. Co mogę zrobić ?

Odp.: Jeśli nie pamiętasz hasła chroniącego skoroszyt programu Excel, nie możesz go bezpośrednio usunąć. Możesz jednak spróbować użyć wyspecjalizowanych narzędzi innych firm, które zapewniają funkcje odzyskiwania hasła do chronionych plików Excel.

#### P: Czy można określić wielu autorów podczas zabezpieczania skoroszytu programu Excel przed zapisem?

Odp.: Nie, biblioteka Aspose.Cells for .NET umożliwia określenie jednego autora podczas ochrony skoroszytu programu Excel przed zapisem. Jeśli chcesz określić wielu autorów, będziesz musiał rozważyć niestandardowe rozwiązania poprzez bezpośrednią manipulację plikiem Excel.