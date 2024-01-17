---
title: Dostosuj poziom kompresji
linktitle: Dostosuj poziom kompresji
second_title: Aspose.Cells dla .NET API odniesienia
description: Zmniejsz rozmiar skoroszytów programu Excel, dostosowując poziom kompresji za pomocą Aspose.Cells dla .NET.
type: docs
weight: 50
url: /pl/net/excel-workbook/adjust-compression-level/
---
W tym samouczku krok po kroku wyjaśnimy dostarczony kod źródłowy C#, który pozwoli Ci dostosować poziom kompresji za pomocą Aspose.Cells dla .NET. Wykonaj poniższe czynności, aby dostosować poziom kompresji w skoroszycie programu Excel.

## Krok 1: Ustaw katalogi źródłowe i wyjściowe

```csharp
// katalog źródłowy
string sourceDir = RunExamples.Get_SourceDirectory();
// Katalog wyjściowy
string outDir = RunExamples.Get_OutputDirectory();
```

W tym pierwszym kroku definiujemy katalogi źródłowe i wyjściowe dla plików Excel.

## Krok 2: Załaduj skoroszyt programu Excel

```csharp
// Załaduj skoroszyt programu Excel
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
```

Ładujemy skoroszyt programu Excel z określonego pliku za pomocą metody`Workbook` klasa z Aspose.Cells.

## Krok 3: Ustaw opcje tworzenia kopii zapasowych

```csharp
// Zdefiniuj opcje tworzenia kopii zapasowych
XlsbSaveOptions options = new XlsbSaveOptions();
```

 Tworzymy instancję`XlsbSaveOptions` class, aby ustawić opcje zapisywania.

## Krok 4: Dostosuj poziom kompresji (poziom 1)

```csharp
// Dostosuj poziom kompresji (poziom 1)
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
let elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 1): " + elapsedMs);
```

 Poziom kompresji regulujemy poprzez ustawienie`CompressionType` Do`Level1`. Następnie zapisujemy skoroszyt programu Excel z określoną opcją kompresji.

## Krok 5: Dostosuj poziom kompresji (poziom 6)

```csharp
// Dostosuj poziom kompresji (poziom 6)
options.CompressionType = OoxmlCompressionType.Level6;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 6): " + elapsedMs);
```

 Powtarzamy proces, aby dostosować poziom kompresji`Level6` i zapisz skoroszyt programu Excel z tą opcją.

## Krok 6: Dostosuj poziom kompresji (poziom 9)

```csharp
// Dostosuj poziom kompresji (poziom 9)
options.CompressionType = OoxmlCompressionType.Level9;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 9): " + elapsedMs);
```

 Powtarzamy proces po raz ostatni, aby dostosować poziom kompresji`Level9` i zapisz skoroszyt programu Excel z tą opcją.

### Przykładowy kod źródłowy dla opcji Dostosuj poziom kompresji przy użyciu Aspose.Cells dla .NET 
```csharp
//Katalog źródłowy
string sourceDir = RunExamples.Get_SourceDirectory();
string outDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
XlsbSaveOptions options = new XlsbSaveOptions();
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
var elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 1 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level6;
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 6 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level9;
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 9 Elapsed Time: " + elapsedMs);
Console.WriteLine("AdjustCompressionLevel executed successfully.");
```

## Wniosek

Gratulacje! Nauczyłeś się, jak dostosować poziom kompresji w skoroszycie programu Excel przy użyciu Aspose.Cells dla .NET. Eksperymentuj z różnymi poziomami kompresji, aby znaleźć ten, który najlepiej odpowiada Twoim potrzebom.

### Często zadawane pytania

#### P: Co to jest kompresja w skoroszycie programu Excel?

Odp.: Kompresja w skoroszycie programu Excel to proces zmniejszania rozmiaru pliku przy użyciu algorytmów kompresji. Zmniejsza to wymaganą przestrzeń dyskową i poprawia wydajność podczas ładowania pliku i manipulowania nim.

#### P: Jakie poziomy kompresji są dostępne w Aspose.Cells?

Odp.: Za pomocą Aspose.Cells możesz dostosować poziom kompresji od 1 do 9. Im wyższy poziom kompresji, tym mniejszy będzie rozmiar pliku, ale może to również wydłużyć czas przetwarzania.

#### P: Jak wybrać odpowiedni poziom kompresji dla skoroszytu programu Excel?

Odp.: Wybór poziomu kompresji zależy od konkretnych potrzeb. Jeśli chcesz, aby maksymalna kompresja i czas przetwarzania nie stanowiły problemu, możesz wybrać poziom 9. Jeśli wolisz kompromis pomiędzy rozmiarem pliku a czasem przetwarzania, możesz wybrać poziom pośredni.

#### P: Czy kompresja wpływa na jakość danych w skoroszycie programu Excel?

Odp.: Nie, kompresja nie wpływa na jakość danych w skoroszycie programu Excel. Po prostu zmniejsza rozmiar pliku za pomocą technik kompresji, bez zmiany samych danych.

#### P: Czy mogę dostosować poziom kompresji po zapisaniu pliku Excel?

Odp.: Nie, po zapisaniu pliku Excel z określonym poziomem kompresji nie można później dostosować poziomu kompresji. Jeśli chcesz go zmodyfikować, konieczne będzie ponowne zapisanie pliku z nowym poziomem kompresji.