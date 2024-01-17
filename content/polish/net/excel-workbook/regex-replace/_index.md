---
title: Regex Zamień
linktitle: Regex Zamień
second_title: Aspose.Cells dla .NET API odniesienia
description: Dowiedz się, jak wykonać zamianę wyrażeń regularnych w plikach Excel przy użyciu Aspose.Cells dla .NET.
type: docs
weight: 140
url: /pl/net/excel-workbook/regex-replace/
---
Zastępowanie tekstu na podstawie wyrażeń regularnych (Regex) jest częstym zadaniem podczas manipulacji danymi w plikach Excel. Dzięki Aspose.Cells dla .NET możesz łatwo wykonać zamianę wyrażenia regularnego, wykonując następujące kroki:

## Krok 1: Określ katalog źródłowy i katalog wyjściowy

Przede wszystkim należy określić katalog źródłowy, w którym znajduje się plik Excel zawierający dane do zamiany, a także katalog wyjściowy, w którym chcemy zapisać zmodyfikowany plik. Oto jak to zrobić za pomocą Aspose.Cells:

```csharp
// katalog źródłowy
string sourceDir = RunExamples.Get_SourceDirectory();

// Katalog wyjściowy
string outputDir = RunExamples.Get_OutputDirectory();
```

## Krok 2: Załaduj źródłowy plik Excel

Następnie musisz załadować źródłowy plik Excel, na którym chcesz wykonać zamianę wyrażenia regularnego. Oto jak to zrobić:

```csharp
// Załaduj źródłowy plik Excel
Workbook workbook = new Workbook(sourceDir + "SampleRegexReplace.xlsx");
```

## Krok 3: Wykonaj zamianę wyrażenia regularnego

Po przesłaniu pliku możesz ustawić opcje zastępowania, w tym uwzględnianie wielkości liter i dokładne dopasowanie zawartości komórek. Oto przykładowy kod do wykonania zamiany Regex:

```csharp
// Ustaw opcje wymiany
ReplaceOptions replace = new ReplaceOptions();
replace.CaseSensitive = false;
replace.MatchEntireCellContents = false;

// Zdefiniuj, że klucz wyszukiwania jest wyrażeniem regularnym
replace. RegexKey = true;

// Wykonaj zamianę wyrażenia regularnego
workbook. Replace("\\bKIM\\b", "^^^TIM^^^", replace);
```

## Krok 4: Zapisz wyjściowy plik Excel

Po zakończeniu zastępowania wyrażeń regularnych możesz zapisać zmodyfikowany plik Excel w określonym katalogu wyjściowym. Oto jak to zrobić:

```csharp
// Zapisz wyjściowy plik Excel
workbook.Save(outputDir + "RegexReplace_out.xlsx");
Console.WriteLine("RegexReplace executed successfully.\r\n");
```

### Przykładowy kod źródłowy Regex Zamień przy użyciu Aspose.Cells dla .NET 
```csharp
//Katalog źródłowy
string sourceDir = RunExamples.Get_SourceDirectory();
//Katalog wyjściowy
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "SampleRegexReplace.xlsx");
ReplaceOptions replace = new ReplaceOptions();
replace.CaseSensitive = false;
replace.MatchEntireCellContents = false;
// Ustaw na true, aby wskazać, że wyszukiwanym kluczem jest wyrażenie regularne
replace.RegexKey = true;
workbook.Replace("\\bKIM\\b", "^^^TIM^^^", replace);
workbook.Save(outputDir + "RegexReplace_out.xlsx");
Console.WriteLine("RegexReplace executed successfully.");
```

## Wniosek

Zastępowanie wyrażeń regularnych to zaawansowana technika dynamicznego modyfikowania danych w pliku Excel. Dzięki Aspose.Cells dla .NET możesz łatwo wykonać zamianę wyrażenia regularnego, wykonując kroki opisane powyżej. Eksperymentuj z własnymi wyrażeniami regularnymi i skorzystaj z elastyczności oferowanej przez Aspose.Cells.

### Często zadawane pytania

#### P: Co to jest zamiana Regex?
    
Odp.: Zastępowanie wyrażeń regularnych to technika używana do zastępowania wzorców tekstowych na podstawie wyrażeń regularnych w pliku Excel. Pozwala to na szybkie i dokładne zmiany danych.

#### P: Czy w przypadku zamiany Regex rozróżniana jest wielkość liter?
    
O: Nie, za pomocą Aspose.Cells możesz określić, czy podczas zastępowania wyrażenia regularnego ma być uwzględniana wielkość liter, czy nie. Masz pełną kontrolę nad tą funkcją.

#### P: Jak mogę określić dokładne dopasowanie zawartości komórek podczas zastępowania wyrażenia regularnego?
    
O: Aspose.Cells pozwala określić, czy zamiana wyrażenia regularnego powinna dokładnie odpowiadać zawartości komórki, czy nie. Możesz dostosować tę opcję do swoich potrzeb.

#### P: Czy mogę używać zaawansowanych wyrażeń regularnych podczas zastępowania wyrażenia regularnego przez Aspose.Cells?
    
O: Tak, Aspose.Cells obsługuje zaawansowane wyrażenia regularne, umożliwiając wykonywanie złożonych i wyrafinowanych zamian w plikach Excel.

#### P: Jak mogę sprawdzić, czy wymiana Regex powiodła się?
    
Odp.: Po zastąpieniu wyrażenia regularnego możesz sprawdzić, czy operacja się powiodła, sprawdzając dane wyjściowe i upewniając się, że wyjściowy plik Excel został poprawnie utworzony.
	